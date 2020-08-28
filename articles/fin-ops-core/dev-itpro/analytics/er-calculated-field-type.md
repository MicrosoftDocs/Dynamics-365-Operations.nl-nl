---
title: Ondersteuning van parameteraanroepen voor ER-gegevensbronnen van het type Berekend veld
description: Dit onderwerp biedt informatie over het gebruik van het type Berekend veld voor ER-gegevensbronnen.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 02d53f4326d8f31abf6ec7404575728837954bef
ms.sourcegitcommit: c9baf9a3b4552f0317b5ec87d252834f52df1b98
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665605"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="eeb8a-103">Ondersteuning van parameteraanroepen voor ER-gegevensbronnen van het type Berekend veld</span><span class="sxs-lookup"><span data-stu-id="eeb8a-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eeb8a-104">In dit onderwerp wordt uitgelegd hoe u een ER-gegevensbron (elektronische rapportage) kunt ontwerpen met behulp van het type **Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="eeb8a-105">Deze gegevensbron kan een ER-expressie bevatten die bij uitvoering kan worden bestuurd door de waarden van de parameterargumenten die zijn geconfigureerd in een binding die deze gegevensbron aanroept.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="eeb8a-106">Door parameteraanroepen voor een dergelijke gegevensbron te configureren, kunt u één gegevensbron in veel bindingen opnieuw gebruiken. Dit vermindert het totale aantal gegevensbronnen dat moet worden geconfigureerd in ER-modeltoewijzingen of ER-indelingen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="eeb8a-107">Het vereenvoudigt ook het geconfigureerde ER-onderdeel, wat de onderhoudskosten en de kosten van gebruik door andere gebruikers verlaagt.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eeb8a-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="eeb8a-108">Prerequisites</span></span>
<span data-ttu-id="eeb8a-109">Om de voorbeelden in dit onderwerp te kunnen voltooien, moet u toegang tot het volgende hebben:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="eeb8a-110">Maak gebruik van een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="eeb8a-111">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="eeb8a-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="eeb8a-112">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="eeb8a-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="eeb8a-113">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="eeb8a-113">System administrator</span></span>

- <span data-ttu-id="eeb8a-114">Toegang tot RCS (Regulatory Configuration Services) die zijn ingericht voor dezelfde tenant als Finance and Operations voor een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="eeb8a-115">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="eeb8a-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="eeb8a-116">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="eeb8a-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="eeb8a-117">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="eeb8a-117">System administrator</span></span>

<span data-ttu-id="eeb8a-118">U moet ook de volgende bestanden downloaden en lokaal opslaan.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="eeb8a-119">**Inhoud**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-119">**Content**</span></span>                           | <span data-ttu-id="eeb8a-120">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eeb8a-121">Voorbeeldconfiguratie van model voor ER-gegevens</span><span class="sxs-lookup"><span data-stu-id="eeb8a-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="eeb8a-122">Model voor het leren van parameteraanroepen.versie.1.xml</span><span class="sxs-lookup"><span data-stu-id="eeb8a-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="eeb8a-123">Voorbeeldconfiguratie van ER-metagegevens</span><span class="sxs-lookup"><span data-stu-id="eeb8a-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="eeb8a-124">Metagegevens voor het leren van parameteraanroepen.versie.1.xml</span><span class="sxs-lookup"><span data-stu-id="eeb8a-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="eeb8a-125">Voorbeeldconfiguratie van ER-modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="eeb8a-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="eeb8a-126">Toewijzing voor het leren van parameteraanroepen.versie.1.xml</span><span class="sxs-lookup"><span data-stu-id="eeb8a-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="eeb8a-127">Voorbeeldconfiguratie van ER-indeling</span><span class="sxs-lookup"><span data-stu-id="eeb8a-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="eeb8a-128">Indeling voor het leren van parameteraanroepen.versie.1.xml</span><span class="sxs-lookup"><span data-stu-id="eeb8a-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="eeb8a-129">Meld u aan bij uw RCS-exemplaar</span><span class="sxs-lookup"><span data-stu-id="eeb8a-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="eeb8a-130">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc. Eerst moet u in RCS de stappen uitvoeren in de procedure [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="eeb8a-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="eeb8a-131">Selecteer **Elektronische aangifte** in het standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="eeb8a-132">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="eeb8a-133">Importeer de gedownloade configuraties naar RCS in deze volgorde: gegevensmodel, metagegevens, modeltoewijzing, indeling.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="eeb8a-134">Voer de volgende stappen uit voor elke ER-configuratie:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="eeb8a-135">Selecteer **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="eeb8a-136">Selecteer **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="eeb8a-137">Selecteer **Bladeren** en selecteer vervolgens de vereiste ER-configuratie in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="eeb8a-138">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="eeb8a-139">De geleverde ER-oplossing controleren</span><span class="sxs-lookup"><span data-stu-id="eeb8a-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="eeb8a-140">Modeltoewijzing controleren</span><span class="sxs-lookup"><span data-stu-id="eeb8a-140">Review model mapping</span></span>

1. <span data-ttu-id="eeb8a-141">Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="eeb8a-142">Selecteer **Toewijzing voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="eeb8a-143">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-143">Select **Designer**.</span></span>
4. <span data-ttu-id="eeb8a-144">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="eeb8a-145">Deze ER-modeltoewijzing is ontworpen om het volgende te doen:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="eeb8a-146">Het ophalen van de lijst met btw-codes (**Btw**-gegevensbron) in de tabel **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="eeb8a-147">Het ophalen van de lijst met btw-transacties (**Trans**-gegevensbron) in de tabel **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="eeb8a-148">Het groeperen van opgehaalde trans acties (**GR**-gegevensbron) op btw-code.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="eeb8a-149">Het berekenen voor gegroepeerde transacties na geaggregeerde waarden per btw-code:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="eeb8a-150">Het optellen van btw-basiswaarden.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="eeb8a-151">Het optellen van btw-waarden.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-151">Sum of tax values.</span></span>
            - <span data-ttu-id="eeb8a-152">Het bepalen van het minimale toegepaste belastingtarief.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="eeb8a-153">Met de modeltoewijzing in deze configuratie wordt het basisgegevensmodel geïmplementeerd voor elke ER-indeling die voor dit model is gemaakt en in Finance and Operations wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="eeb8a-154">Dat betekent dat de inhoud van de gegevensbronnen **Btw** en **GR** worden weergegeven voor ER-indelingen zoals abstracte gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![De pagina Ontwerper modeltoewijzingen met Btw- en GR-gegevensbronnen](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="eeb8a-156">Sluit de pagina **Ontwerper modeltoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="eeb8a-157">Sluit de pagina **Modeltoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="eeb8a-158">Indeling controleren</span><span class="sxs-lookup"><span data-stu-id="eeb8a-158">Review format</span></span>

1. <span data-ttu-id="eeb8a-159">Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="eeb8a-160">Selecteer **Indeling voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="eeb8a-161">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-161">Select **Designer**.</span></span> <span data-ttu-id="eeb8a-162">Deze ER-indeling is ontworpen om het volgende te doen:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="eeb8a-163">Het genereren van een belastingaangifte in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="eeb8a-164">Het opgeven van de volgende belastingniveaus in de belastingaangifte: normaal, verlaagd en geen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="eeb8a-165">Het opgeven van meerdere details voor elk belastingniveau, met een verschillend aantal details op elk niveau.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Pagina Indelingsontwerper](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="eeb8a-167">Selecteer **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="eeb8a-168">Vouw de items **Model**, **Gegevens** en **Overzicht** uit.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="eeb8a-169">Het berekende veld **Model.Data.Summary.Level** bevat de expressie die de code van het belastingniveau (**Normaal**, **Verlaagd**, **Geen** of **Overige**) als een tekstwaarde retourneert voor elke belastingcode die in runtime kan worden opgehaald uit de gegevensbron **Model.Data.Summary**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Pagina Indelingsontwerper met details van het gegevensmodel Model voor het leren van parameteraanroepen](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="eeb8a-171">Vouw het item **Model**.**Data2** uit.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="eeb8a-172">Vouw het item **Model**.**Data2.Summary2** uit.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="eeb8a-173">De gegevensbron **Model**.**Data2.Summary2** is geconfigureerd om de transactiegegevens van de gegevensbron **Model.Data.Summary** te groeperen op belastingniveau (geretourneerd door het berekende veld **Model.Data.Summary.Level**) en de aggregaties te berekenen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Pagina Indelingsontwerper met details van de gegevensbron Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="eeb8a-175">Controleer de berekende velden **Model**.**Data2.Level1**, **Model**.**Data2.Level2** en **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="eeb8a-176">Deze berekende velden worden gebruikt om de lijst met **Model**.**Data2. Summary2**-records te filteren en alleen de records weer te geven die een bepaald belastingniveau vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="eeb8a-177">Sluit de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="eeb8a-178">Een afgeleide indeling maken</span><span class="sxs-lookup"><span data-stu-id="eeb8a-178">Create a derived format</span></span>
<span data-ttu-id="eeb8a-179">U kunt de opgegeven indeling verbeteren door één berekend veld toe te voegen om het vereiste belastingniveau te filteren in plaats van de drie velden **Model**.**Data2.Level1**, **Model**.**Data2.Level2** en **Model**.**Data2.Level3** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="eeb8a-180">Het vereiste belastingniveau kan worden opgegeven op de locatie waar dit nieuwe berekende veld wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="eeb8a-181">Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="eeb8a-182">Selecteer **Indeling voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="eeb8a-183">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="eeb8a-184">Selecteer **Afleiden van naam: Indeling voor het leren van parameteraanroepen, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="eeb8a-185">Voer in het veld **Naam** de tekst **Indeling voor het leren van parameteraanroepen** in.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="eeb8a-186">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="eeb8a-187">Een berekend parameterveld configureren dat een lijst met records retourneert</span><span class="sxs-lookup"><span data-stu-id="eeb8a-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="eeb8a-188">Het toevoegen van een nieuw berekend veld starten</span><span class="sxs-lookup"><span data-stu-id="eeb8a-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="eeb8a-189">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-189">Select **Designer**.</span></span>
2. <span data-ttu-id="eeb8a-190">Selecteer **Uitvouwen/Samenvouwen** om alle indelingsitems uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="eeb8a-191">Selecteer **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="eeb8a-192">Vouw het item **Model** uit.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="eeb8a-193">Selecteer het item **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="eeb8a-194">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-194">Select **Add**.</span></span>
7. <span data-ttu-id="eeb8a-195">Selecteer **Functies\\Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="eeb8a-196">Voer in het veld **Naam** de tekst **Niveaus** in.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="eeb8a-197">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="eeb8a-198">Een parameter definiëren voor het toevoegen van een berekend veld</span><span class="sxs-lookup"><span data-stu-id="eeb8a-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="eeb8a-199">Selecteer **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="eeb8a-200">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-200">Select **New**.</span></span>
3. <span data-ttu-id="eeb8a-201">Voer in het veld **Naam** de tekst **Belastingniveau** in.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="eeb8a-202">Selecteer in het veld **Type** de optie **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="eeb8a-203">Alleen primitieve gegevenstypen kunnen worden gebruikt om het type argument van de parameter op te geven.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="eeb8a-204">Daarom kunnen de typen **Lijst met records**, **Record** en **Opsomming** niet voor dit doel worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="eeb8a-205">Het maximum aantal parameters dat kan worden opgegeven voor één berekend veld is 8.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Lijst met parametergegevensbronnen](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="eeb8a-207">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-207">Select **OK**.</span></span>

<span data-ttu-id="eeb8a-208">Door deze parameter toe te voegen, geeft u de voorwaarde op die moet gelden om dit berekend veld aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="eeb8a-209">Wanneer u dit berekend veld aanroept, moet u het argument van de parameter **Belastingniveau** opgeven als een waarde met de indeling **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="eeb8a-210">Zorg dat u alleen parameters definieert voor de berekende velden die zich in een container **(** Lijst met records, **Record** of **Container**) bevinden.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="eeb8a-211">De geconfigureerde parameter is beschikbaar in de lijst met gegevensbronnen voor dit berekend veld.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="eeb8a-212">U kunt de parameter toevoegen aan de geconfigureerde expressie door **Gegevensbron toevoegen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Gegevensbronvelden](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="eeb8a-214">Een expressie definiëren voor het toevoegen van een berekend veld</span><span class="sxs-lookup"><span data-stu-id="eeb8a-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="eeb8a-215">Voer in het veld **Formule** het volgende in:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="eeb8a-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="eeb8a-217">Selecteer de parameter **Belastingniveau** in de lijst met gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="eeb8a-218">Selecteer **Gegevensbron toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="eeb8a-219">Maak de expressie in het veld **Formule** als volgt af:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="eeb8a-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Belastingniveau')**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="eeb8a-221">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-221">Select **Save**.</span></span>

    ![Informatie Gegevensbronveld](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="eeb8a-223">Sluit de pagina **Formuleontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="eeb8a-224">Het toevoegen van een nieuw berekend veld voltooien</span><span class="sxs-lookup"><span data-stu-id="eeb8a-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="eeb8a-225">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-225">Select **OK**.</span></span>

<span data-ttu-id="eeb8a-226">Op de pagina **Indelingsontwerper** heeft het geconfigureerde berekende parameterveld **Niveaus** een argument van het type **Tekenreeks** nodig.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Uitgevouwen lijst met berekende veldniveaus](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="eeb8a-228">Het geconfigureerde berekende veld gebruiken voor het binden van indelingselementen</span><span class="sxs-lookup"><span data-stu-id="eeb8a-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="eeb8a-229">Selecteer **Model.Data2.Levels** om het geconfigureerde berekende veld te selecteren.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="eeb8a-230">Selecteer het indelingselement **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="eeb8a-231">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-231">Select **Bind**.</span></span>
4. <span data-ttu-id="eeb8a-232">Selecteer **Ja** om de vervanging van de op dat moment gebruikte gegevensbron, **Niveau1**, door de nieuwe gegevensbron **Niveaus** in alle geneste opmaakelementen van het geselecteerde indelingselement te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="eeb8a-233">Toegepaste binding is opgebouwd als een aanroep van het berekende parameterveld.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="eeb8a-234">De naam van het gebonden indelingselement wordt onder de volgende voorwaarden standaard gebruikt als argument voor het berekende parameterveld:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="eeb8a-235">Het berekende veld is geconfigureerd voor het gebruik van één parameter.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="eeb8a-236">Het gegevens type van deze parameter is gedefinieerd als **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="eeb8a-237">Wanneer de naam van het gebonden indelingselement leeg is, wordt de naam van de gegevensbron van dit element gebruikt bij toegepaste binding.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="eeb8a-238">Selecteer het indelingselement **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="eeb8a-239">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-239">Select **Bind**.</span></span>
7. <span data-ttu-id="eeb8a-240">Selecteer **Ja** om de vervanging van de op dat moment gebruikte gegevensbron, **Niveau2**, door de nieuwe gegevensbron **Niveaus** in alle geneste opmaakelementen onder het geselecteerde indelingselement te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="eeb8a-241">Selecteer het indelingselement **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="eeb8a-242">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-242">Select **Bind**.</span></span>
10. <span data-ttu-id="eeb8a-243">Selecteer **Ja** om de vervanging van de op dat moment gebruikte gegevensbron, **Niveau3**, door de nieuwe gegevensbron **Niveaus** in alle geneste opmaakelementen onder het geselecteerde indelingselement te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="eeb8a-244">Wanneer u het argument van het berekende parameterveld voor het XML-element dat het belastingniveau vertegenwoordigt (bijvoorbeeld **Model.Data2.Levels("Verlaagd")** opgeeft als tekstwaarde), hoeft u dit niet meer te doen voor geneste XML-kenmerken. De bindingen nemen automatisch de waarde over van het argument dat is gedefinieerd op het bovenliggende niveau (**Model.Data2.Levels.aggregated.Base**, niet **Model.Data2.Levels("Verlaagd").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="eeb8a-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="eeb8a-245">Terugkerende aanroepen van berekende parametervelden worden niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="eeb8a-246">U kunt **Formule bewerken** selecteren en het standaard toegepaste argument van het berekende parameterveld in de geselecteerde binding wijzigen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="eeb8a-247">Als dit argument ontbreekt, kan dit in runtime leiden tot fouten. Gebruikers krijgen een melding over een dergelijke situatie wanneer de huidige indeling wordt gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Melding met validatiewaarschuwing](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="eeb8a-249">Een berekend parameterveld configureren dat een record retourneert</span><span class="sxs-lookup"><span data-stu-id="eeb8a-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="eeb8a-250">Wanneer een berekend parameterveld een record retourneert, moet u binding van afzonderlijke velden van deze record ondersteunen om elementen in te delen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="eeb8a-251">In dergelijke gevallen is er geen bovenliggende binding die de waarde van een argument bevat voor het aanroepen van een berekend parameterveld. Deze waarde moet worden gedefinieerd in de binding van het veld van één record.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="eeb8a-252">Het toevoegen van een nieuw berekend veld starten</span><span class="sxs-lookup"><span data-stu-id="eeb8a-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="eeb8a-253">Selecteer het item **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="eeb8a-254">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-254">Select **Add**.</span></span>
3. <span data-ttu-id="eeb8a-255">Selecteer **Functies\\Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="eeb8a-256">Voer in het veld **Naam** **LevelRecord** in.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="eeb8a-257">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="eeb8a-258">Een parameter definiëren voor het toevoegen van een berekend veld</span><span class="sxs-lookup"><span data-stu-id="eeb8a-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="eeb8a-259">Selecteer **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="eeb8a-260">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-260">Select **New**.</span></span>
3. <span data-ttu-id="eeb8a-261">Voer in het veld **Naam** de tekst **Belastingniveau** in.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="eeb8a-262">Selecteer in het veld **Type** de optie **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="eeb8a-263">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="eeb8a-264">Een expressie definiëren voor het toevoegen van een berekend veld</span><span class="sxs-lookup"><span data-stu-id="eeb8a-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="eeb8a-265">Voer in het veld **Formule** het volgende in:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="eeb8a-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="eeb8a-267">Selecteer de parameter **Belastingniveau**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="eeb8a-268">Selecteer **Gegevensbron toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="eeb8a-269">Voeg in het veld **Formule** de tekst **'Belastingniveau'))** toe aan wat u in stap 1 hebt ingevoerd om de expressie als volgt te voltooien:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="eeb8a-270">**FIRSTORNULL(\@.Levels('Belastingniveau'))**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="eeb8a-271">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-271">Select **Save**.</span></span>
6. <span data-ttu-id="eeb8a-272">Sluit de pagina **Formuleontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="eeb8a-273">Het toevoegen van een nieuw berekend veld voltooien</span><span class="sxs-lookup"><span data-stu-id="eeb8a-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="eeb8a-274">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="eeb8a-275">Het geconfigureerde berekende veld gebruiken om indelingselementen te binden</span><span class="sxs-lookup"><span data-stu-id="eeb8a-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="eeb8a-276">Vouw **Model.Data2.LevelRecord** uit om het geconfigureerde berekende veld te selecteren.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="eeb8a-277">Vouw de container **Model.Data2.LevelRecord.aggregated** van het geconfigureerde berekende veld uit.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="eeb8a-278">Selecteer het veld **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="eeb8a-279">Selecteer het indelingselement **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="eeb8a-280">Selecteer **Verbinding verbreken**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="eeb8a-281">Selecteer het indelingselement **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="eeb8a-282">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-282">Select **Bind**.</span></span>
8. <span data-ttu-id="eeb8a-283">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="eeb8a-284">Wijzig de expressie in **Model.Data2.LevelRecord("Geen").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Bijgewerkte expressie](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="eeb8a-286">Ongebruikte berekende velden verwijderen</span><span class="sxs-lookup"><span data-stu-id="eeb8a-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="eeb8a-287">Selecteer **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="eeb8a-288">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-288">Select **Delete**.</span></span>
3. <span data-ttu-id="eeb8a-289">Selecteer **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="eeb8a-290">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-290">Select **Delete**.</span></span>
5. <span data-ttu-id="eeb8a-291">Selecteer **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="eeb8a-292">Selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-292">Select **Delete**.</span></span>
7. <span data-ttu-id="eeb8a-293">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="eeb8a-294">U hebt hetzelfde berekende veld **Model.Data2.Levels** een aantal keer gebruikt in indelingsbindingen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="eeb8a-295">Het is veel eenvoudiger om één berekend veld te gebruiken en te onderhouden in plaats van dit voor meerdere soortgelijke velden te doen.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="eeb8a-296">Sluit de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="eeb8a-297">Aangepaste versie van een afgeleide indeling voltooien</span><span class="sxs-lookup"><span data-stu-id="eeb8a-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="eeb8a-298">Selecteer op het sneltabblad **Versies** de optie **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="eeb8a-299">Selecteer **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="eeb8a-300">Voltooide versie van een afgeleide indeling exporteren</span><span class="sxs-lookup"><span data-stu-id="eeb8a-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="eeb8a-301">Selecteer de indeling **Indeling voor het leren van parameteraanroepen (aangepast)** in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="eeb8a-302">Selecteer op het sneltabblad **Versies** de voltooide versie 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="eeb8a-303">Selecteer **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="eeb8a-304">Selecteer **Exporteren als XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="eeb8a-305">Sla de gedownloade configuratie lokaal op in de XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="eeb8a-306">ER-indelingen testen</span><span class="sxs-lookup"><span data-stu-id="eeb8a-306">Test ER formats</span></span> 
<span data-ttu-id="eeb8a-307">U kunt de initiële en verbeterde ER-indelingen uitvoeren om te controleren of de geconfigureerde berekende parametervelden goed werken.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="eeb8a-308">ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="eeb8a-308">Import ER configurations</span></span>
<span data-ttu-id="eeb8a-309">U kunt gecontroleerde configuraties vanuit RCS importeren door de ER-opslagplaats van het type **RCS** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="eeb8a-310">Als u de stappen in het onderwerp [Configuraties voor Elektronische rapportage (ER) importeren uit Regulatory Configuration Services (RCS)](rcs-download-configurations.md) al hebt uitgevoerd, gebruikt u de geconfigureerde ER-opslagplaats om de configuraties die eerder in dit onderwerp zijn besproken in uw omgeving te importeren.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="eeb8a-311">Volg anders deze stappen:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="eeb8a-312">Selecteer het bedrijf **DEMF** en selecteer in het standaarddashboard de optie **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="eeb8a-313">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="eeb8a-314">Importeer de configuraties vanuit het Microsoft Downloadcentrum in deze volgorde: gegevensmodel, modeltoewijzing, indeling.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="eeb8a-315">Voer de volgende stappen uit voor elke ER-configuratie:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="eeb8a-316">Selecteer **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="eeb8a-317">Selecteer **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="eeb8a-318">Selecteer **Bladeren** om de vereiste ER-configuratie in XML-indeling te selecteren.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="eeb8a-319">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-319">Select **OK**.</span></span>

4. <span data-ttu-id="eeb8a-320">Importeer de uit RCS geëxporteerde voltooide versie 1.1.1 van de indeling **Indeling voor het leren van parameteraanroepen (aangepast)**:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="eeb8a-321">Selecteer **Uitwisselen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="eeb8a-322">Selecteer **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="eeb8a-323">Selecteer **Bladeren** om de lokaal opgeslagen bestand **Indeling voor het leren van parameteroproepen (aangepast)** in de XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="eeb8a-324">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="eeb8a-325">ER-indelingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="eeb8a-325">Run ER formats</span></span>

1. <span data-ttu-id="eeb8a-326">Vouw in de configuratiestructuur de inhoud uit van het item **Model voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="eeb8a-327">Selecteer **Indeling voor het leren van parameteraanroepen**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="eeb8a-328">Selecteer **Uitvoeren** op het bovenste lint.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="eeb8a-329">Sla de lokaal gegenereerde uitvoer op.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="eeb8a-330">Selecteer het item **Indeling voor het leren van parameteraanroepen (aangepast)**.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="eeb8a-331">Selecteer **Uitvoeren** op het bovenste lint.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="eeb8a-332">Sla de gegenereerde uitvoer lokaal op.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="eeb8a-333">Vergelijk de inhoud van de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eeb8a-334">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="eeb8a-334">Additional resources</span></span>
[<span data-ttu-id="eeb8a-335">Formuleontwerper in elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="eeb8a-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)

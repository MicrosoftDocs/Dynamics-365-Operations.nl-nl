---
title: De parameters van een ER-indeling per rechtspersoon instellen
description: In dit onderwerp wordt uitgelegd hoe u de para meters van een ER-indeling (Elektronische rapportage) per rechts persoon kunt instellen.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: ca837026f18034cddb34d7a2d5a62002ed69106a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042752"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="60e4d-103">De parameters van een ER-indeling per rechtspersoon instellen</span><span class="sxs-lookup"><span data-stu-id="60e4d-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="60e4d-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="60e4d-104">Prerequisites</span></span>

<span data-ttu-id="60e4d-105">Als u deze stappen wilt voltooien, moet u eerst de stappen in het onderwerp [ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](er-app-specific-parameters-configure-format.md) uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="60e4d-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="60e4d-106">Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot Microsoft Dynamics 365 Finance (Finance) voor een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="60e4d-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="60e4d-107">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="60e4d-107">Electronic reporting developer</span></span>
- <span data-ttu-id="60e4d-108">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="60e4d-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="60e4d-109">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="60e4d-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="60e4d-110">ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="60e4d-110">Import ER configurations</span></span>

1.  <span data-ttu-id="60e4d-111">Meld u aan bij uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="60e4d-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="60e4d-112">Selecteer **Elektronische aangifte** in het standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="60e4d-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="60e4d-113">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="60e4d-114">Importeer in het huidige exemplaar van Finance de configuraties die u vanuit Regulatory Configuration Services (RCS) hebt geëxporteerd terwijl u de stappen in het onderwerp [ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](er-app-specific-parameters-configure-format.md) voltooide.</span><span class="sxs-lookup"><span data-stu-id="60e4d-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="60e4d-115">Voer de volgende stappen uit voor elke ER-configuratie (Elektronische rapportage) in de onderstaande volgorde: gegevensmodel, modeltoewijzing en indelingen.</span><span class="sxs-lookup"><span data-stu-id="60e4d-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="60e4d-116">Selecteer **Uitwisselen \> Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="60e4d-117">Selecteer **Bladeren** om het bestand voor de vereiste ER-configuratie in XML-indeling te selecteren.</span><span class="sxs-lookup"><span data-stu-id="60e4d-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="60e4d-118">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-118">Select **OK**.</span></span>
    
    <span data-ttu-id="60e4d-119">In de volgende afbeelding ziet u de configuraties die u moet hebben wanneer u klaar bent.</span><span class="sxs-lookup"><span data-stu-id="60e4d-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![Pagina ER-configuraties](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="60e4d-121">Parameters instellen voor het bedrijf DEMF</span><span class="sxs-lookup"><span data-stu-id="60e4d-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="60e4d-122">U kunt het ER-raamwerk gebruiken voor het instellen van toepassingsspecifieke parameters voor een ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="60e4d-123">Selecteer de rechtspersoon **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="60e4d-124">Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="60e4d-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="60e4d-125">Selecteer in het actievenster op het tabblad **Configuraties** in de groep **Specifieke toepassingsparameters** de optie **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="60e4d-127">Op de pagina **Specifieke toepassingsparameters** kunt u de regels voor de gegevensbron **Selector** van de indeling **Indeling voor het opzoeken van LE-gegevens** configureren.</span><span class="sxs-lookup"><span data-stu-id="60e4d-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="60e4d-128">Als de ER-basisindeling meerdere gegevensbronnen van het type **Zoekopdracht** bevat, moet u de gewenste gegevensbron selecteren op het sneltabblad **Zoekopdrachten** voordat u kunt beginnen met het configureren van de set regels voor de gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="60e4d-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="60e4d-129">Voor elke gegevensbron kunt u afzonderlijke regels configureren voor elke versie van de geselecteerde ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="60e4d-130">Alle set regels voor alle opzoekgegevensbronnen die beschikbaar zijn in de geselecteerde versie van de ER-basisindeling vormen de toepassingsspecifieke parameters voor de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="60e4d-131">Selecteer versie **1.1.1** van de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="60e4d-132">Selecteer op het sneltabblad **Voorwaarden** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="60e4d-133">Selecteer in het veld **Code** van de nieuwe record de vervolgkeuzepijl om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60e4d-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="60e4d-134">De zoekopdracht bevat de lijst met belastingcodes voor selectie.</span><span class="sxs-lookup"><span data-stu-id="60e4d-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="60e4d-135">Deze lijst wordt geretourneerd door de gegevensbron **Model.Data.Tax** die is geconfigureerd in de ER-basisindeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="60e4d-136">Omdat deze gegevensbron het veld **Naam** bevat, wordt de naam van elke belastingcode weergegeven in de zoek opdracht.</span><span class="sxs-lookup"><span data-stu-id="60e4d-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="60e4d-138">Selecteer de belastingcode **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="60e4d-139">Selecteer in het veld **Zoekresultaat** van de nieuwe record de vervolgkeuzepijl om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60e4d-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="60e4d-140">De lijst met waarden voor de indelingsopsomming TaxationLevel voor selectie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60e4d-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="60e4d-141">Als u Duits hebt geselecteerd als de voorkeurstaal van de gebruiker waarmee u bent aangemeld, worden de labels van de waarden in de zoekopdracht in het Duits weer gegeven, op voorwaarde dat deze zijn vertaald in de ER-basisindeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="60e4d-142">Als het label van een gegevensbron voor opzoeken is vertaald, wordt dit label ook weergegeven in de voorkeurstaal van de gebruiker op het tabblad **Zoekopdrachten**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="60e4d-144">Selecteer de waarde **Normale belasting**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="60e4d-145">Door deze record toe te voegen, definieert u de volgende regel: wanneer de gegevensbron **Selector** wordt aangevraagd en de belastingcode **VAT19** als een argument wordt doorgegeven, wordt **Normale belasting** geretourneerd als het aangevraagde belastingniveau.</span><span class="sxs-lookup"><span data-stu-id="60e4d-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="60e4d-146">Selecteer **Toevoegen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="60e4d-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="60e4d-147">Selecteer de belastingcode **InVAT19** in het veld **Code**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="60e4d-148">Selecteer de waarde **Normale belasting** in het veld **Zoekresultaat**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="60e4d-149">Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="60e4d-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="60e4d-150">Selecteer de belastingcode **InVAT7** in het veld **Code**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="60e4d-151">Selecteer de waarde **Verlaagde belasting** in het veld **Zoekresultaat**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="60e4d-152">Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="60e4d-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="60e4d-153">Selecteer de belastingcode **InVAT7** in het veld **Code**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="60e4d-154">Selecteer de waarde **Verlaagde belasting** in het veld **Zoekresultaat**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="60e4d-155">Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="60e4d-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="60e4d-156">Selecteer de belastingcode **THIRD** in het veld **Code**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="60e4d-157">Selecteer de waarde **Geen belasting** in het veld **Zoekresultaat**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="60e4d-158">Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="60e4d-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="60e4d-159">Selecteer de belastingcode **InVAT0** in het veld **Code**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="60e4d-160">Selecteer de waarde **Geen belasting** in het veld **Zoekresultaat**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="60e4d-161">Selecteer nogmaals **Toevoegen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="60e4d-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="60e4d-162">Selecteer de optie **\*Niet leeg\*** in het veld **Code**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="60e4d-163">Selecteer de waarde **Overig** in het veld **Zoekresultaat**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="60e4d-164">Door deze laatste record toe te voegen, definieert u de volgende regel: wanneer de gegevensbron die als een argument wordt doorgegeven, niet voldoet aan een van de vorige regels, wordt voor de gegevensbron voor opzoeken **Overig** geretourneerd als het aangevraagde belastingniveau.</span><span class="sxs-lookup"><span data-stu-id="60e4d-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="60e4d-166">Selecteer **Voltooid** in het veld **Status**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="60e4d-167">Wanneer u een ER-indelingsversie met de status **Voltooid** of **Gedeeld** uitvoert, moet deze set regels de status **Voltooid** hebben.</span><span class="sxs-lookup"><span data-stu-id="60e4d-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="60e4d-168">Anders wordt de uitvoering van de ER-basisindeling onderbroken wanneer wordt geprobeerd gegevens uit deze set regels te laden terwijl de gegevensbron voor opzoeken **Selector** wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="60e4d-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="60e4d-169">Wanneer u een ER-indelingsversie uitvoert met de status **Concept**, heeft de ER-basisindeling toegang tot deze set regels, ongeacht de status.</span><span class="sxs-lookup"><span data-stu-id="60e4d-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="60e4d-170">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-170">Select **Save**.</span></span>
18. <span data-ttu-id="60e4d-171">Sluit de pagina **Specifieke toepassingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="60e4d-172">De ER-indeling in het bedrijf DEMF uitvoeren</span><span class="sxs-lookup"><span data-stu-id="60e4d-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="60e4d-173">Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="60e4d-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="60e4d-174">Selecteer **Uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="60e4d-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="60e4d-175">Selecteer in het dialoogvenster dat verschijnt **OK**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="60e4d-176">Download het gegenereerde overzicht en sla dit lokaal op.</span><span class="sxs-lookup"><span data-stu-id="60e4d-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="60e4d-177">In het gegenereerde overzicht is de samenvatting van de belastingcode **InVAT7** op het niveau **Verlaagd** geplaatst en de samenvattingen van de belastingcodes **VAT19** en **InVA19** op het niveau **Normaal**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="60e4d-178">Dit gedrag wordt bepaald door de configuratie in de groep regels die afhankelijk is van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="60e4d-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="60e4d-179">Ga naar **Belasting \> Indirecte belastingen \> Btw \> Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="60e4d-180">Selecteer de belastingcode **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="60e4d-181">Selecteer in het actieven ster op het tabblad **Btw-code** in de groep **Query's** de optie **Geboekte btw** om informatie weer te geven over de belastingwaarde en het toegepaste belastingtarief per belastingcode.</span><span class="sxs-lookup"><span data-stu-id="60e4d-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Pagina Geboekte btw](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="60e4d-183">Sluit de pagina Geboekte btw.</span><span class="sxs-lookup"><span data-stu-id="60e4d-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="60e4d-184">Parameters instellen voor het bedrijf USMF</span><span class="sxs-lookup"><span data-stu-id="60e4d-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="60e4d-185">Selecteer de rechtspersoon **USMF**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="60e4d-186">Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="60e4d-187">Vouw in de configuratiestructuur de items **Model voor het leren van parameteraanroepen** en **Indeling voor het leren van parameteraanroepen** uit en selecteer de indeling **Indeling voor het opzoeken van LE-gegevens**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="60e4d-188">Selecteer in het actievenster op het tabblad **Configuraties** in de groep **Specifieke toepassingsparameters** de optie **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="60e4d-189">Selecteer versie **1.1.1** van de geselecteerde ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="60e4d-190">Selecteer op het sneltabblad **Voorwaarden** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="60e4d-191">Selecteer in het veld **Code** van de nieuwe record de vervolgkeuzepijl om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60e4d-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="60e4d-192">De zoekopdracht bevat nu de lijst met belastingcodes die kunnen worden geselecteerd voor het bedrijf **USMF**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="60e4d-194">Selecteer de belastingcode **VRIJSTELLING**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="60e4d-195">Selecteer de waarde **Geen belasting** in het veld **Zoekresultaat** van de nieuwe record.</span><span class="sxs-lookup"><span data-stu-id="60e4d-195">In the **Lookup resul**t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="60e4d-196">Selecteer opnieuw **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-196">Select **Add** again.</span></span>
11. <span data-ttu-id="60e4d-197">Selecteer de optie **\*Niet leeg\*** in het veld **Code** van de nieuwe record.</span><span class="sxs-lookup"><span data-stu-id="60e4d-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="60e4d-198">Selecteer de waarde **Normale belasting** in het veld **Zoekresultaat** van de nieuwe record.</span><span class="sxs-lookup"><span data-stu-id="60e4d-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="60e4d-199">Selecteer **Voltooid** in het veld **Status**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="60e4d-200">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-200">Select **Save**.</span></span>

    ![De ER-pagina Specifieke toepassingsparameters](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="60e4d-202">Sluit de pagina **Specifieke toepassingsparameters**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="60e4d-203">De ER-indeling in het bedrijf USMF uitvoeren</span><span class="sxs-lookup"><span data-stu-id="60e4d-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="60e4d-204">Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="60e4d-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="60e4d-205">Selecteer **Uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="60e4d-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="60e4d-206">Selecteer in het dialoogvenster dat verschijnt **OK**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="60e4d-207">Download het gegenereerde overzicht en sla dit lokaal op.</span><span class="sxs-lookup"><span data-stu-id="60e4d-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="60e4d-208">In het gegenereerde overzicht ziet u dat u nu dezelfde indeling hebt gebruikt voor een andere rechtspersoon, maar zonder wijzigingen aan te brengen in de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="60e4d-209">Van rechtspersonen afhankelijke parameters opnieuw gebruiken</span><span class="sxs-lookup"><span data-stu-id="60e4d-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="60e4d-210">Parameters exporteren</span><span class="sxs-lookup"><span data-stu-id="60e4d-210">Export parameters</span></span>

1.  <span data-ttu-id="60e4d-211">Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="60e4d-212">Selecteer **Rapportageconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="60e4d-213">Selecteer de indeling **Indeling voor het opzoeken van LE-gegevens** in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="60e4d-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="60e4d-214">Selecteer in het actievenster op het tabblad **Configuraties** in de groep **Specifieke toepassingsparameters** de optie **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="60e4d-215">Selecteer versie **1.1.1** van de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="60e4d-216">Selecteer **Exporteren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="60e4d-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="60e4d-217">Download het gegenereerde bestand en sla dit lokaal op.</span><span class="sxs-lookup"><span data-stu-id="60e4d-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="60e4d-218">De geconfigureerde verzameling toepassingsspecifieke parameters is nu geëxporteerd als een XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="60e4d-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="60e4d-219">Parameters importeren</span><span class="sxs-lookup"><span data-stu-id="60e4d-219">Import parameters</span></span>

1.  <span data-ttu-id="60e4d-220">Selecteer versie **1.1.2** van de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="60e4d-221">Selecteer **Importeren** in het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="60e4d-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="60e4d-222">Selecteer **Ja** als u wilt bevestigen dat de bestaande toepassingsspecifieke parameters voor deze indelingsversie wilt negeren.</span><span class="sxs-lookup"><span data-stu-id="60e4d-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="60e4d-223">Selecteer **Bladeren** om het bestand te zoeken dat de geëxporteerde toepassingsspecifieke parameters voor versie **1.1.1** bevat.</span><span class="sxs-lookup"><span data-stu-id="60e4d-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="60e4d-224">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-224">Select **OK**.</span></span>

    <span data-ttu-id="60e4d-225">Versie **1.1.2** van de ER-indeling heeft nu dezelfde toepassingsspecifieke parameters die u oorspronkelijk voor versie **1.1.1** hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="60e4d-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="60e4d-226">De toepassingsspecifieke parameters van een ER-indeling zijn afhankelijk van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="60e4d-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="60e4d-227">Als u de geconfigureerde toepassingsspecifieke parameters voor een rechtspersoon opnieuw wilt gebruiken voor een andere rechtspersoon, moet u deze exporteren terwijl u bent aangemeld bij de eerste rechtspersoon en deze vervolgens importeren nadat u zich hebt aangemeld bij de andere rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="60e4d-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="60e4d-228">U kunt deze aanpak ook gebruiken om toepassingsspecifieke parameters voor een ER-indeling die oorspronkelijk waren geconfigureerd in het ene exemplaar van Finance over te dragen naar een ander exemplaar van Finance.</span><span class="sxs-lookup"><span data-stu-id="60e4d-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="60e4d-229">Als u toepassingsspecifieke parameters voor één versie van een ER-indeling configureert en een hogere versie van dezelfde indeling in het huidige Finance-exemplaar importeert, worden de bestaande toepassingsspecifieke parameters niet toegepast voor de geïmporteerde versie.</span><span class="sxs-lookup"><span data-stu-id="60e4d-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="60e4d-230">Wanneer u een bestand selecteert om te importeren, wordt de structuur van de toepassingsspecifieke parameters in dat bestand vergeleken met de structuur van de bijbehorende gegevensbron van het type **Zoekopdracht** in de ER-indeling die is geselecteerd voor importeren.</span><span class="sxs-lookup"><span data-stu-id="60e4d-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="60e4d-231">De importbewerking wordt uitgevoerd wanneer de structuur van elke toepassingsspecifieke parameter overeenkomt met de structuur van de bijbehorende gegevensbron in de ER-indeling die is geselecteerd voor importeren.</span><span class="sxs-lookup"><span data-stu-id="60e4d-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="60e4d-232">Als de structuren niet overeenkomen, ontvangt u de waarschuwing dat de importbewerking niet kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="60e4d-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="60e4d-233">Als u de importbewerking afdwingt, worden de bestaande toepassingsspecifieke parameters voor de geselecteerde ER-indeling opgeruimd en moet u deze vanaf het begin instellen.</span><span class="sxs-lookup"><span data-stu-id="60e4d-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="60e4d-234">Relatie tussen toepassingsspecifieke parameters en een ER-indeling</span><span class="sxs-lookup"><span data-stu-id="60e4d-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="60e4d-235">De relatie tussen een ER-indeling en de toepassingsspecifieke parameters wordt vastgesteld op basis van de exemplaaronafhankelijke unieke id-code van de ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="60e4d-236">Wanneer u een ER-indeling uit Finance verwijdert, worden de toepassingsspecifieke parameters die zijn geconfigureerd voor de ER-indeling bewaard in het huidige exemplaar van Finance.</span><span class="sxs-lookup"><span data-stu-id="60e4d-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="60e4d-237">Deze kunnen worden geopend wanneer de ER-basisindeling weer wordt geïmporteerd in dit exemplaar van Finance.</span><span class="sxs-lookup"><span data-stu-id="60e4d-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="60e4d-238">Toepassingsspecifieke parameters openen via het ER-raamwerk</span><span class="sxs-lookup"><span data-stu-id="60e4d-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="60e4d-239">In het vorige voorbeeld hebt u via het ER-raamwerk toegang gekregen tot toepassingsspecifieke parameters van een ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="60e4d-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="60e4d-240">Met deze benadering kunt u de toegang tot de toepassingsspecifieke parameters van een specifieke ER-indeling niet beperken.</span><span class="sxs-lookup"><span data-stu-id="60e4d-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="60e4d-241">Voer de volgende stappen uit als u dergelijke beperkingen moet toepassen.</span><span class="sxs-lookup"><span data-stu-id="60e4d-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="60e4d-242">Gebruik een bestaand menu-item **ERSolutionAppSpecificParametersDesigner** of implementeer uw eigen menu-item **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual Studio-pagina](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="60e4d-244">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="60e4d-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="60e4d-245">Maak een nieuwe menu-itemknop en koppel deze aan de bijbehorende record in de tabel **ERSolutionTable** door de eigenschap **Gegevensbron** in te stellen op **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="60e4d-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual Studio-pagina](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="60e4d-247">Maak een eenvoudige knop en negeer de methode **Geklikt**, zoals wordt weer gegeven in het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="60e4d-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="60e4d-248">Met deze methode kunt u een unieke oplossings-id (gedefinieerd via de waarde voor **GUID**) opgeven om uitsluitend toegang te verlenen tot de toepassingsspecifieke parameters van een specifieke ER-indeling en afstammende kopieën die hiervan zijn afgeleid.</span><span class="sxs-lookup"><span data-stu-id="60e4d-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="60e4d-249">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="60e4d-249">Additional resources</span></span>

[<span data-ttu-id="60e4d-250">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="60e4d-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="60e4d-251">ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven</span><span class="sxs-lookup"><span data-stu-id="60e4d-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)

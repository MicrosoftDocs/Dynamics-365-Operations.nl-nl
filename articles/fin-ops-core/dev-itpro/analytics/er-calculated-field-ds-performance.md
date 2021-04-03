---
title: De prestaties van ER-oplossingen verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen
description: In dit onderwerp wordt uitgelegd hoe u de prestaties van ER-oplossingen (elektronische rapportage) kunt verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c63d64774b5b97a562da20655400078ed47c5675
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569220"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="d9ecc-103">De prestaties van ER-oplossingen verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen</span><span class="sxs-lookup"><span data-stu-id="d9ecc-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9ecc-104">In dit onderwerp wordt beschreven hoe u [prestatietraceringen](trace-execution-er-troubleshoot-perf.md) van uitgevoerde [ER-indelingen (elektronische rapportage)](general-electronic-reporting.md) kunt gebruiken om de prestaties te verbeteren door een gegevensbron **Berekend veld** met parameters te configureren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="d9ecc-105">Als onderdeel van het proces van het ontwerpen van ER-configuraties om elektronische documenten te genereren, definieert u de methode die wordt gebruikt om gegevens uit de toepassing te halen en deze in te voeren in de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="d9ecc-106">Door een ER-gegevensbron van het type **Berekend veld** met parameters te ontwerpen, kunt u het aantal databaseaanroepen verminderen en de tijd en kosten van het verzamelen van de details van het uitvoeren van de ER-indeling aanzienlijk beperken.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9ecc-107">Vereisten</span><span class="sxs-lookup"><span data-stu-id="d9ecc-107">Prerequisites</span></span>

- <span data-ttu-id="d9ecc-108">Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot een van de volgende [rollen](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="d9ecc-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="d9ecc-109">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="d9ecc-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="d9ecc-110">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="d9ecc-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d9ecc-111">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="d9ecc-111">System administrator</span></span>

- <span data-ttu-id="d9ecc-112">Het bedrijf moet worden ingesteld op **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="d9ecc-113">Volg de stappen in [bijlage 1](#appendix1) van dit onderwerp om de onderdelen van de Microsoft ER-voorbeeldoplossing te downloaden die vereist zijn om de voorbeelden in dit onderwerp te voltooien.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="d9ecc-114">Volg de stappen in [bijlage 2](#appendix2) van dit onderwerp om de minimale set ER-parameters te configureren die nodig is om het ER-framework te gebruiken om de prestaties van de Microsoft ER-voorbeeldoplossing te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="d9ecc-115">De ER-voorbeeldoplossing importeren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-115">Import the sample ER solution</span></span>

<span data-ttu-id="d9ecc-116">Stel dat u een ER-oplossing moet ontwerpen om een nieuw rapport te genereren waarin leverancierstransacties worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="d9ecc-117">Op dit moment kunt u de transacties voor een geselecteerde leverancier vinden op de pagina **Leverancierstransacties** (ga naar **Leveranciers** \> **Leveranciers** \> **Alle leveranciers**, selecteer een leverancier en selecteer in het actievenster op het tabblad **Leverancier** in de groep **Transacties** de optie **Transacties**).</span><span class="sxs-lookup"><span data-stu-id="d9ecc-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="d9ecc-118">U wilt echter alle leverancierstransacties tegelijk in één elektronisch document in XML-indeling hebben.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="d9ecc-119">Deze oplossing bestaat uit verschillende ER-configuraties met het vereiste gegevensmodel, de modeltoewijzing en indelingscomponenten.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="d9ecc-120">De eerste stap is om de ER-voorbeeldoplossing te importeren om een leverancierstransactierapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="d9ecc-121">Meld u aan bij het exemplaar van Microsoft Dynamics 365 Finance dat wordt ingericht voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="d9ecc-122">In dit onderwerp maakt en wijzigt u configuraties voor het voorbeeldbedrijf **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="d9ecc-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="d9ecc-123">Zorg ervoor dat deze configuratieprovider is toegevoegd aan uw exemplaar van Finance en als actief is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="d9ecc-124">Zie [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="d9ecc-125">Selecteer in het werkgebied **Elektronische rapportage** de tegel **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="d9ecc-126">Importeer op de pagina **Configuraties** de ER-configuraties die u als vereiste hebt gedownload in Finance, in de volgende volgorde: gegevensmodel, modeltoewijzing, indeling.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="d9ecc-127">Volg deze stappen voor elke configuratie:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="d9ecc-128">In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="d9ecc-129">Selecteer **Bladeren** en selecteer het juiste bestand voor de ER-configuratie in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="d9ecc-130">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-130">Select **OK**.</span></span>

![Geïmporteerde configuraties op de pagina Configuraties](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="d9ecc-132">De ER-voorbeeldoplossing controleren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="d9ecc-133">De modeltoewijzing controleren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-133">Review the model mapping</span></span>

1. <span data-ttu-id="d9ecc-134">Vouw op de pagina **Configuraties** in de configuratiestructuur **Prestatieverbeteringsmodel** uit en selecteer **Prestatieverbeteringstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d9ecc-135">Selecteer **Ontwerper** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d9ecc-136">Selecteer **Ontwerper** op de pagina **Model aan gegevensbrontoewijzing** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="d9ecc-137">Deze ER-modeltoewijzing is ontworpen om de volgende acties uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="d9ecc-138">De lijst met leverancierstransacties ophalen die zijn opgeslagen in de tabel VendTrans (gegevensbron **Trans**).</span><span class="sxs-lookup"><span data-stu-id="d9ecc-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="d9ecc-139">Voor elke transactie uit de tabel VendTable de record van een leverancier ophalen waarvoor de transactie is geboekt (gegevensbron **\#Vend**).</span><span class="sxs-lookup"><span data-stu-id="d9ecc-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9ecc-140">De gegevensbron **\#Vend** wordt geconfigureerd om de bijbehorende leveranciersrecord op te halen met behulp van de bestaande veel-op-één-relatie **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="d9ecc-141">Met de modeltoewijzing in deze configuratie wordt het basisgegevensmodel geïmplementeerd voor elke ER-indeling die voor dit model is gemaakt en in Finance wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="d9ecc-142">Dat betekent dat de inhoud van de gegevensbron **Trans** wordt weergegeven voor ER-indelingen zoals abstracte gegevensbronnen van het type **model**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Gegevensbron Trans op de pagina Ontwerper modeltoewijzing](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="d9ecc-144">Sluit de pagina **Ontwerper modeltoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="d9ecc-145">Sluit de pagina **Model aan gegevensbrontoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="d9ecc-146">Indeling controleren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-146">Review format</span></span>

1. <span data-ttu-id="d9ecc-147">Vouw op de pagina **Configuraties** in de configuratiestructuur **Prestatieverbeteringsmodel** uit en selecteer **Prestatieverbeteringsindeling**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="d9ecc-148">Selecteer **Ontwerper** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d9ecc-149">Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** de optie **Uitvouwen/Samenvouwen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="d9ecc-150">Vouw de items **Model**, **Gegevens** en **Transactie** uit.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="d9ecc-151">Deze ER-indeling is ontworpen om een rapport voor leverancierstransacties in XML-indeling te genereren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Indelingsgegevensbronnen en geconfigureerde bindingen van indelingselementen op de pagina Indelingsontwerper](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="d9ecc-153">Sluit de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="d9ecc-154">De ER-voorbeeldoplossing uitvoeren om de uitvoering te traceren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="d9ecc-155">Stel dat u klaar bent met het ontwerpen van de eerste versie van de ER-oplossing.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="d9ecc-156">U wilt deze nu testen in de oplossing in uw Finance-exemplaar en de uitvoeringsprestaties analyseren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="d9ecc-157">De ER-prestatietracering inschakelen</span><span class="sxs-lookup"><span data-stu-id="d9ecc-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="d9ecc-158">Selecteer het bedrijf **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="d9ecc-159">Volg de stappen in [De ER-prestatietracering inschakelen](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) om een prestatietracering te genereren terwijl er een ER-indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Dialoogvenster voor gebruikersparameters](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="d9ecc-161">De ER-indeling uitvoeren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-161">Run the ER format</span></span>

1. <span data-ttu-id="d9ecc-162">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d9ecc-163">Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor prestatieverbetering**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="d9ecc-164">Selecteer **Uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="d9ecc-165">De prestatietracering gebruiken om modeltoewijzingsprestaties te analyseren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="d9ecc-166">Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Prestatieverbeteringstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d9ecc-167">Selecteer **Ontwerper** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d9ecc-168">Selecteer **Ontwerper** op de pagina **Modeltoewijzingen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d9ecc-169">Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Prestatietracering**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d9ecc-170">Selecteer de meest recente tracering die is gegenereerd en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="d9ecc-171">Nieuwe informatie is nu beschikbaar voor bepaalde gegevensbronitems van de huidige modeltoewijzing:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="d9ecc-172">De werkelijke tijd die is besteed aan het ophalen van gegevens met behulp van de gegevensbron</span><span class="sxs-lookup"><span data-stu-id="d9ecc-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="d9ecc-173">Dezelfde tijd uitgedrukt als een percentage van de totale tijd die is besteed aan het uitvoeren van de gehele modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="d9ecc-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Details over de uitvoeringstijd op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="d9ecc-175">In het raster **Prestatiestatistieken** ziet u dat de gegevensbron **Trans** de tabel VendTrans één keer aanroept.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="d9ecc-176">De waarde **\[265\]\[Q:265\]** van de gegevensbron **Trans** geeft aan dat 265 leverancierstransacties uit de toepassingstabel zijn opgehaald en naar het gegevensmodel zijn geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="d9ecc-177">In het raster **Prestatiestatistieken** ziet u ook dat de huidige modeltoewijzing databaseaanvragen dupliceert wanneer de gegevensbron **\#Vend** wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="d9ecc-178">Deze duplicatie vindt plaats om de volgende redenen:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="d9ecc-179">De leverancierstabel wordt twee keer aangeroepen voor elk van de 265 herhaalde leverancierstransacties, voor een totaal van 530 aanroepen:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="d9ecc-180">Er wordt één oproep gedaan om het rekeningnummer van de leverancier in te voeren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="d9ecc-181">Er wordt één oproep gedaan om de naam van de leverancier in te voeren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="d9ecc-182">De leverancierstabel wordt aangeroepen voor elke herhaalde leverancierstransactie, hoewel de opgehaalde transacties slechts voor vijf leveranciers zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="d9ecc-183">Van de 530 aanroepen zijn er 525 duplicaten.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="d9ecc-184">In de volgende afbeelding ziet u het bericht dat u ontvangt over dubbele oproepen (databaseaanvragen).</span><span class="sxs-lookup"><span data-stu-id="d9ecc-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Bericht over dubbele databaseaanvragen op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="d9ecc-186">Van de totale uitvoeringstijd voor modeltoewijzingen (circa acht seconden), ziet u dat meer dan 80 procent (ongeveer zes seconden) is besteed aan het ophalen van waarden uit de VendTable-toepassingstabel.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="d9ecc-187">Dit percentage is te hoog voor twee kenmerken van vijf leveranciers, vergeleken met het volume gegevens in de VendTrans-toepassingstabel.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="d9ecc-188">Als u het aantal aanroepen wilt beperken dat wordt uitgevoerd om de leveranciersgegevens voor elke transactie te verkrijgen en om de prestaties van de modeltoewijzing te verbeteren, kunt u caching gebruiken voor de gegevensbron **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="d9ecc-189">De gegevensbron **Trans\\\#Vend** wordt tijdens runtime in de cache opgeslagen in het bereik van de huidige transactie van de gegevensbron **Trans**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="d9ecc-190">Door de gegevensbron **\#Vend** in de cache op te slaan, verlaagt u het aantal dubbele aanroepen van 525 naar 260, maar verwijdert u de duplicatie niet volledig.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="d9ecc-191">Als u de duplicatie volledig wilt elimineren, kunt u een nieuwe gegevensbron met parameters configureren voor het type **Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="d9ecc-192">De modeltoewijzing verbeteren op basis van informatie uit de uitvoeringstracering</span><span class="sxs-lookup"><span data-stu-id="d9ecc-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="d9ecc-193">De logica van de modeltoewijzing wijzigen</span><span class="sxs-lookup"><span data-stu-id="d9ecc-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="d9ecc-194">Volg deze stappen om caching en een gegevensbron van het type **Berekend veld** te gebruiken om dubbele oproepen naar de database te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="d9ecc-195">Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Prestatieverbeteringstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d9ecc-196">Selecteer **Ontwerper** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d9ecc-197">Selecteer **Ontwerper** op de pagina **Modeltoewijzingen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d9ecc-198">Voer op de pagina **Ontwerper modeltoewijzing** de volgende stappen uit om een gegevensbron van het type **Tabelrecords** toe te voegen om toegang te krijgen tot records in de VendTable-toepassingstabel:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="d9ecc-199">Vouw in het deelvenster **Typen gegevensbronnen** het item **Dynamics 365 for Operations** uit en selecteer **Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="d9ecc-200">Selecteer **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="d9ecc-201">Voer in het dialoogvenster in het veld **Naam** de tekst **Vend** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="d9ecc-202">Voer in het veld **Tabel** de waarde **VendTable** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="d9ecc-203">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-203">Select **OK**.</span></span>

5. <span data-ttu-id="d9ecc-204">U kunt alleen parameteraanroepen naar gegevensbronnen van het type **Berekend veld** uitvoeren als deze gegevensbronnen zich in een container bevinden.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="d9ecc-205">Voer daarom de volgende stappen uit om een gegevensbron van het type **Lege container** toe te voegen voor een nieuwe gegevensbron met parameters van het type **Berekend veld**:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="d9ecc-206">Vouw in het deelvenster **Typen gegevensbronnen** het item **Algemeen** uit en selecteer **Lege container**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="d9ecc-207">Selecteer **Basis toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="d9ecc-208">Voer in het dialoogvenster in het veld **Naam** de tekst **Box** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="d9ecc-209">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-209">Select **OK**.</span></span>

    ![Gegevensbron Box op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="d9ecc-211">Voer de volgende stappen uit om een gegevensbron met parameters toe te voegen voor het type **Berekend veld**:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="d9ecc-212">Selecteer **Box** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="d9ecc-213">Vouw in het deelvenster **Typen gegevensbronnen** het item **Functies** uit en selecteer **Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="d9ecc-214">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-214">Select **Add**.</span></span>
    4. <span data-ttu-id="d9ecc-215">Voer in het dialoogvenster in het veld **Naam** de tekst **Vend** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="d9ecc-216">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="d9ecc-217">Selecteer op de pagina **Formuleontwerper** de optie **Parameters** om de parameters op te geven die moeten worden opgegeven wanneer deze gegevensbron wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="d9ecc-218">Selecteer **Nieuw** in het dialoogvenster **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="d9ecc-219">Voer in het veld **Naam** de waarde **parmVendAccNumber** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="d9ecc-220">Selecteer in het veld **Type** de optie **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="d9ecc-221">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-221">Select **OK**.</span></span>
    11. <span data-ttu-id="d9ecc-222">Voer in het veld **Formule** de waarde **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="d9ecc-223">Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="d9ecc-224">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="d9ecc-225">Voer de volgende stappen uit om de toegevoegde gegevensbron te markeren als in cache opgeslagen tijdens de uitvoering:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="d9ecc-226">Selecteer **Box\\Vend** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="d9ecc-227">Selecteer **Cache**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9ecc-228">De gegevensbron **Box\\Vend** wordt tijdens runtime in de cache opgeslagen in het bereik van alle leverancierstransacties van de gegevensbron **Trans**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="d9ecc-229">Voer de volgende stappen uit om de geneste gegevensbron **Trans\\\#Vend** bij te werken zodat deze de gegevensbron **Box\\Vend** gebruikt:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="d9ecc-230">Vouw **Trans** uit in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="d9ecc-231">Selecteer de gegevensbron **Trans\\\#Vend** en selecteer vervolgens **Bewerken** \> **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="d9ecc-232">Voer op de pagina **Formuleontwerper** in het veld **Formule** de waarde **Box.Vend(\@.AccountNum)** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="d9ecc-233">Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="d9ecc-234">Selecteer **OK** om de wijzigingen in de geselecteerde gegevensbron te voltooien.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="d9ecc-235">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-235">Select **Save**.</span></span>

    ![Gegevensbron Vend op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="d9ecc-237">Sluit de pagina **Ontwerper modeltoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="d9ecc-238">Sluit de pagina **Modeltoewijzingen**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="d9ecc-239">De gewijzigde versie van de ER-modeltoewijzing voltooien</span><span class="sxs-lookup"><span data-stu-id="d9ecc-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="d9ecc-240">Op de pagina **Configuraties** op het sneltabblad **Versies** selecteert u versie **1.2** van de configuratie **Toewijzing voor prestatieverbetering**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="d9ecc-241">Selecteer **Status wijzigen** \> **Voltooien** en **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="d9ecc-242">De gewijzigde ER-oplossing uitvoeren om de uitvoering te traceren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="d9ecc-243">Herhaal de stappen uit het gedeelte [De ER-indeling uitvoeren](#run-format) eerder in dit onderwerp om een nieuwe prestatietracering te genereren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="d9ecc-244">De prestatietracering gebruiken om aanpassingen in de modeltoewijzing te analyseren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="d9ecc-245">Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Prestatieverbeteringstoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d9ecc-246">Selecteer **Ontwerper** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d9ecc-247">Selecteer **Ontwerper** op de pagina **Modeltoewijzingen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d9ecc-248">Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Prestatietracering**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d9ecc-249">Selecteer de meest recente tracering die is gegenereerd en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="d9ecc-250">Door uw aanpassingen in de modeltoewijzing worden er geen dubbele query's meer uitgevoerd in de database.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="d9ecc-251">Het aantal aanroepen naar databasetabellen en gegevensbronnen voor deze modeltoewijzing is ook beperkt.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Traceringsgegeven op de pagina Ontwerper modeltoewijzing 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="d9ecc-253">De totale uitvoeringstijd is ongeveer 20 keer verlaagd (van ongeveer 8 seconden tot ongeveer 400 milliseconden).</span><span class="sxs-lookup"><span data-stu-id="d9ecc-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="d9ecc-254">Hierdoor zijn de prestaties van de hele ER-oplossing verbeterd.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Traceringsgegeven op de pagina Ontwerper modeltoewijzing 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="d9ecc-256">Bijlage 1: De componenten van de Microsoft ER-voorbeeldoplossing downloaden</span><span class="sxs-lookup"><span data-stu-id="d9ecc-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="d9ecc-257">U moet de volgende bestanden downloaden en lokaal opslaan.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="d9ecc-258">Bestand</span><span class="sxs-lookup"><span data-stu-id="d9ecc-258">File</span></span>                                        | <span data-ttu-id="d9ecc-259">Inhoud</span><span class="sxs-lookup"><span data-stu-id="d9ecc-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="d9ecc-260">Versie 1 prestatieverbeteringsmodel</span><span class="sxs-lookup"><span data-stu-id="d9ecc-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="d9ecc-261">Voorbeeldconfiguratie van model voor ER-gegevens</span><span class="sxs-lookup"><span data-stu-id="d9ecc-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="d9ecc-262">Versie 1.1 toewijzing voor prestatieverbetering</span><span class="sxs-lookup"><span data-stu-id="d9ecc-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="d9ecc-263">Voorbeeldconfiguratie van ER-modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="d9ecc-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="d9ecc-264">Versie 1.1 indeling voor prestatieverbetering</span><span class="sxs-lookup"><span data-stu-id="d9ecc-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="d9ecc-265">Voorbeeldconfiguratie van ER-indeling</span><span class="sxs-lookup"><span data-stu-id="d9ecc-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="d9ecc-266">Bijlage 2: Het ER-raamwerk configureren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="d9ecc-267">Voordat u het ER-raamwerk kunt gebruiken om de prestaties van de Microsoft ER-voorbeeldoplossing te verbeteren, moet u de minimale set ER-parameters configureren.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="d9ecc-268">ER-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-268">Configure ER parameters</span></span>

1. <span data-ttu-id="d9ecc-269">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d9ecc-270">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="d9ecc-271">Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="d9ecc-272">Stel op het tabblad **Bijlagen** de volgende parameters in:</span><span class="sxs-lookup"><span data-stu-id="d9ecc-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="d9ecc-273">Selecteer in het veld **Configuraties** het type **Bestand** voor het bedrijf **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="d9ecc-274">Selecteer in de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** het type **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="d9ecc-275">Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d9ecc-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="d9ecc-276">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="d9ecc-277">Elke ER-configuratie die wordt toegevoegd, wordt gemarkeerd als het eigendom van een ER-configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="d9ecc-278">De ER-configuratieprovider die is geactiveerd in de werkruimte **Elektronische rapportage** wordt hiervoor gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="d9ecc-279">Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u ER-configuraties gaat toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="d9ecc-280">Alleen de eigenaar van een ER-configuratie kan de configuratie bewerken.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="d9ecc-281">Daarom moet een geschikte ER-configuratieprovider worden geactiveerd in de werkruimte **Elektronische rapportage**, voordat een ER-configuratie kan worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="d9ecc-282">De lijst met ER-configuratie providers bekijken</span><span class="sxs-lookup"><span data-stu-id="d9ecc-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="d9ecc-283">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d9ecc-284">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="d9ecc-285">Op de tabelpagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="d9ecc-286">Bekijk de inhoud van deze pagina.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-286">Review the contents of this page.</span></span> <span data-ttu-id="d9ecc-287">Als er al een record bestaat voor **Litware, Inc.**, kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#ActivateProvider), overslaan.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="d9ecc-288">Een nieuwe ER-configuratieprovider toevoegen</span><span class="sxs-lookup"><span data-stu-id="d9ecc-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="d9ecc-289">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d9ecc-290">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="d9ecc-291">Selecteer **Nieuw** op de pagina **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="d9ecc-292">Voer in het veld **Naam** de tekst **Litware, Inc.** in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="d9ecc-293">Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="d9ecc-294">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="d9ecc-295">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="d9ecc-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="d9ecc-296">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d9ecc-297">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Litware, Inc.** en selecteer **Instellen als actief**.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="d9ecc-298">Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d9ecc-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9ecc-299">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d9ecc-299">Additional resources</span></span>

- [<span data-ttu-id="d9ecc-300">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="d9ecc-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d9ecc-301">De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen</span><span class="sxs-lookup"><span data-stu-id="d9ecc-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="d9ecc-302">Ondersteuning van parameteraanroepen voor ER-gegevensbronnen van het type Berekend veld</span><span class="sxs-lookup"><span data-stu-id="d9ecc-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
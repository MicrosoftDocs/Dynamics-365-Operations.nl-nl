---
title: Rapport Opslag artikelprijzen vergelijken
description: Informatie over het genereren van een opslagrapport voor het vergelijken van artikelprijzen en vervolgens het doorbladeren en/of exporteren van het resultaat.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425643"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="fa8f6-103">Rapport Opslag artikelprijzen vergelijken</span><span class="sxs-lookup"><span data-stu-id="fa8f6-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa8f6-104">In dit onderwerp wordt uitgelegd hoe u een rapport **Opslag van artikelprijzen vergelijken** kunt uitvoeren en de uitvoer in digitale vorm beschikbaar kunt maken, als een interactieve pagina in Dynamics 365 Supply Chain Management of als een geëxporteerd document in verschillende indelingen.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="fa8f6-105">Bij het bekijken van het rapport in uw browser worden kolommen en samengevoegde balansen dynamisch aangepast, afhankelijk van de indeling die u hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="fa8f6-106">U kunt de resultaten sorteren, filteren, details van de gegevens bekijken en nog veel meer.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="fa8f6-107">Rapportresultaten worden opgeslagen in de gegevensentiteit **Artikelprijzen vergelijken**, waarmee u de resultaten kunt filteren en exporteren naar een indeling zoals CSV of Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="fa8f6-108">Het rapport **Opslag van artikelprijzen vergelijken** kan handig zijn wanneer de uitvoer veel regels bevat.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="fa8f6-109">De uitvoer zal bijvoorbeeld een groot aantal regels bevatten als u meer dan 40.000 artikelen hebt die een artikelprijs in behandeling hebben in de kostprijsberekeningsversie.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="fa8f6-110">Opslag van artikelprijzen vergelijken inschakelen</span><span class="sxs-lookup"><span data-stu-id="fa8f6-110">Enable compare item prices storage</span></span>

<span data-ttu-id="fa8f6-111">Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="fa8f6-112">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="fa8f6-113">Hier ziet u de functie als:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="fa8f6-114">**Module** - Kostenbeheer</span><span class="sxs-lookup"><span data-stu-id="fa8f6-114">**Module** - Cost management</span></span>
- <span data-ttu-id="fa8f6-115">**Functienaam** - Opslag van artikelprijzen vergelijken</span><span class="sxs-lookup"><span data-stu-id="fa8f6-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="fa8f6-116">Een rapport Opslag van artikelprijzen vergelijken genereren</span><span class="sxs-lookup"><span data-stu-id="fa8f6-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="fa8f6-117">Volg deze stappen om een rapport **Opslag van artikelprijzen vergelijken** te genereren en op te slaan:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="fa8f6-118">Ga naar **Kostenbeheer > Query's en rapporten > Rapporten met vooraf bepaalde kosten > Opslag artikelprijzen vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="fa8f6-119">Selecteer **Nieuw** om het deelvenster **Artikelprijzen vergelijken** te openen.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="fa8f6-120">Stel de volgende opties in om te definiëren welke prijzen moeten worden vergeleken in uw rapport:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="fa8f6-121">Geef op het sneltabblad **Parameters** het rapport een unieke **Naam** en gebruik de velden in de secties **Prijzen in behandeling om te vergelijken** en **Gebruikte prijzen voor vergelijking** om te definiëren welke prijzen en datums moeten worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="fa8f6-122">Stel op het sneltabblad **Op te nemen records** filters en beperkingen in om op te geven welke gegevens u in het rapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="fa8f6-123">Stel op het sneltabblad **Op de achtergrond uitvoeren** in hoe, wanneer en hoe vaak u het rapport wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="fa8f6-124">Dit rapport wordt altijd uitgevoerd als onderdeel van een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="fa8f6-125">Selecteer **OK** om de instellingen toe te passen en het deelvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="fa8f6-126">Nadat de batchtaak is voltooid, wordt deze vermeld op de pagina **Opslag artikelprijzen vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="fa8f6-127">U moet mogelijk de pagina vernieuwen om het rapport te kunnen bekijken.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="fa8f6-128">Het rapport Opslag artikelprijzen vergelijken verkennen</span><span class="sxs-lookup"><span data-stu-id="fa8f6-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="fa8f6-129">Nadat u een rapport hebt gegenereerd, kunt u het als volgt op elk gewenst moment weergeven en verkennen:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="fa8f6-130">Ga naar **Kostenbeheer > Query's en rapporten > Rapporten met vooraf bepaalde kosten > Opslag artikelprijzen vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="fa8f6-131">Selecteer een rapport in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-131">Select a report from the list.</span></span>

1. <span data-ttu-id="fa8f6-132">U kunt een van de volgende dingen doen:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-132">Do one of the following:</span></span>

    - <span data-ttu-id="fa8f6-133">Selecteer **Overzicht** om een overzicht van de resultaten van uw rapport weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="fa8f6-134">Selecteer **Details weergeven** om een gedetailleerdere weergave van uw rapport te krijgen</span><span class="sxs-lookup"><span data-stu-id="fa8f6-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="fa8f6-135">Nadat de geselecteerde weergave is geopend, kunt u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="fa8f6-136">Vrijwel elke kolomkop selecteren om de tabel te sorteren of filteren op waarden in die kolom, net als bij de meeste standaardformulieren in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="fa8f6-137">U kunt de kolom **Netto wijzigingsprijs%** niet sorteren of filteren omdat het een berekend veld is.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="fa8f6-138">De **dimensieweergave** selecteren om een deelvenster te openen waarin u kunt kiezen welke dimensiekolom u in het formulier wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="fa8f6-139">De optie **Instellingen opslaan** instellen op **Ja** als u deze instellingen wilt opslaan, zodat deze behouden blijven wanneer u het rapport de volgende keer opent.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="fa8f6-140">Selecteer **OK** om de instellingen toe te passen en te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="fa8f6-141">Een willekeurige rij in het formulier selecteren en vervolgens **Details weergeven** om meer informatie over het geselecteerde artikel weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="fa8f6-142">U kunt van hieruit inzoomen op de gegevens.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="fa8f6-143">Een willekeurige rij in het formulier selecteren en vervolgens **Vergelijkingsdiagram weergeven** selecteren om een interactieve grafische weergave van de resultaten te bekijken die betrekking hebben op het geselecteerde artikel.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="fa8f6-144">U kunt deze resultaten verkennen door verschillende grafische elementen te selecteren in de grafiek- en diagramlegenda.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="fa8f6-145">Een willekeurige rij in het formulier selecteren en vervolgens **Berekeningsdetails weergeven** om meer informatie over berekeningen met betrekking tot het geselecteerde artikel weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="fa8f6-146">U kunt van hieruit inzoomen op de gegevens.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="fa8f6-147">Het rapport Opslag artikelprijzen vergelijken exporteren</span><span class="sxs-lookup"><span data-stu-id="fa8f6-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="fa8f6-148">Elk rapport dat u genereert wordt opgeslagen in gegevensentiteit **Artikelprijzen vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="fa8f6-149">U kunt de standaardfuncties voor gegevensbeheer van Supply Chain Management gebruiken om gegevens van deze entiteit te exporteren naar elke ondersteunde gegevensindeling, inclusief CSV of Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="fa8f6-150">Hierna volgt een voorbeeld van het exporteren van een rapport **Opslag artikelprijzen vergelijken**:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="fa8f6-151">Ga naar **Systeembeheer > Werkgebieden > Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="fa8f6-152">Selecteer de knop **Exporteren** in de sectie **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="fa8f6-153">De pagina **Exporteren** wordt geopend, waarmee u uw exporttaak kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="fa8f6-154">Begin door uw taak een **groepsnaam** te geven.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="fa8f6-155">Selecteer in de sectie **Geselecteerde entiteiten** de optie **Entiteit toevoegen** om een dialoogvenster te openen waarin u de volgende opties kunt instellen:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="fa8f6-156">**Entiteitnaam** - Selecteer **Artikelprijzen vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="fa8f6-157">**Indeling van doelgegevens**: kies de indeling waarnaar u wilt exporteren.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="fa8f6-158">Selecteer **Toevoegen** om de nieuwe rij toe te voegen en selecteer vervolgens **Sluiten** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="fa8f6-159">Gewoonlijk exporteert u één rapport tegelijk.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="fa8f6-160">Hiervoor stelt u een **filter** in voor de rij die u zojuist hebt toegevoegd aan het deelvenster **Query**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="fa8f6-161">Hiermee kunt u definiëren welke rapporten uit de entiteit **Artikelprijzen vergelijken** u wilt opnemen in de export.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="fa8f6-162">Stel de volgende filteropties in om een enkel rapport te exporteren:</span><span class="sxs-lookup"><span data-stu-id="fa8f6-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="fa8f6-163">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een nieuwe rij toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="fa8f6-164">Stel **Tabel** in op **Artikelprijzen vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="fa8f6-165">Stel **Afgeleid tabel** in op **Artikelprijzen vergelijken**.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="fa8f6-166">Stel **Veld** in op het veld waarop u wilt filteren.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="fa8f6-167">Meestal zult u **Uitvoeringsnaam** of **Uitvoeringstijd** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="fa8f6-168">Stel **Criteria** in voor de waarde van het geselecteerde veld waarnaar u wilt zoeken (de naam van het rapport of het tijdstip waarop het rapport is gegenereerd).</span><span class="sxs-lookup"><span data-stu-id="fa8f6-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="fa8f6-169">Voeg zo nodig meer rijen toe aan de tabel **Bereik** totdat u een unieke identificatie hebt voor het gewenste rapport.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="fa8f6-170">Selecteer **OK** om de instellingen op te slaan en te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="fa8f6-171">Selecteer **Opslaan** om de instellingen voor exporteren op te slaan.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="fa8f6-172">Open het tabblad **Exportopties** en selecteer **Nu exporteren** om het exportbestand te genereren.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="fa8f6-173">De pagina **Uitvoeringsoverzicht** wordt geopend, waar u de status van uw exporttaak en een lijst met entiteiten kunt zien die zijn geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="fa8f6-174">Selecteer de entiteit **Artikelprijzen vergelijken** die worden vermeld in het gebied **Verwerkingsstatus entiteit** en selecteer vervolgens **Bestand downloaden** om de geëxporteerde gegevens van die entiteit te downloaden.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="fa8f6-175">Zie [Overzicht van Gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) voor meer informatie over het gebruik van gegevensbeheer voor het exporteren van gegevens.</span><span class="sxs-lookup"><span data-stu-id="fa8f6-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

---
title: Afdrukken van wavelabels instellen en gebruiken
description: In dit onderwerp wordt beschreven hoe u wavelabels afdrukt en hoe u dit kunt instellen.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6314fd25d8d8a0013984d484f57a832c26f82b5a
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "4425884"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="84162-103">Afdrukken van wavelabels instellen en gebruiken</span><span class="sxs-lookup"><span data-stu-id="84162-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84162-104">Het afdrukken van wavelabels is een alternatieve manier om labels af te drukken door de introductie van een nieuwe wavestapmethode waarmee u labels rechtstreeks vanuit de wavesjabloon kunt maken en afdrukken tijdens het uitvoeren van de wave.</span><span class="sxs-lookup"><span data-stu-id="84162-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="84162-105">Daarom zijn de labels al beschikbaar voordat de werknemers de werkorder op een mobiel apparaat uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="84162-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="84162-106">Werknemers kunnen de vereiste labels tijdens het orderverzamelen koppelen in plaats van na het orderverzamelen.</span><span class="sxs-lookup"><span data-stu-id="84162-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="84162-107">Bij het afdrukken van wavelabels wordt de Zebra Programming Language (ZPL) gebruikt om labelindelingen te maken.</span><span class="sxs-lookup"><span data-stu-id="84162-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="84162-108">Een labelindeling is onderverdeeld in drie secties (koptekst, hoofdtekst en voettekst) om labels met een herhalende structuur toe te staan.</span><span class="sxs-lookup"><span data-stu-id="84162-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="84162-109">Met wavelabelsjablonen wordt aangegeven welke labelindeling moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="84162-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="84162-110">Gebruikers kunnen opgeven welke printer wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="84162-110">Users can specify which printer is used.</span></span> <span data-ttu-id="84162-111">Ze kunnen ook labels op meerdere printers tegelijk afdrukken, als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="84162-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="84162-112">Op de pagina **Historie van wavelabels** ziet u een overzicht van alle labels die met deze instellingen zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="84162-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="84162-113">U kunt labels afdrukken en sorteren op basis van werkkopteksten, u kunt onderbrekingsetiketten afdrukken per werkkoptekst en u kunt labels voor containerinhoud, kisten en andere vergelijkbare labels afdrukken.</span><span class="sxs-lookup"><span data-stu-id="84162-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="84162-114">Deze functie vervangt niet de bestaande afdrukfuncties voor labels die zijn gebaseerd op documentroutering.</span><span class="sxs-lookup"><span data-stu-id="84162-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="84162-115">Bij het afdrukken van wavelabels kunt u de volgende uitbreidingen kiezen:</span><span class="sxs-lookup"><span data-stu-id="84162-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="84162-116">Labels afdrukken op basis van het aantal dozen op één werklijn, zonder gebruik te maken van containers.</span><span class="sxs-lookup"><span data-stu-id="84162-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="84162-117">(Een "doos" is een eenheid die is opgegeven op de regels van de eenheidsvolgordegroep.)</span><span class="sxs-lookup"><span data-stu-id="84162-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="84162-118">Druk verschillende labelreeksen af (bijvoorbeeld labels voor dozen en pallets).</span><span class="sxs-lookup"><span data-stu-id="84162-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="84162-119">Neem labelopsomming op (bijvoorbeeld 1/124, 2/124,... 124/124) en definieer het opsommingsbereik (bijvoorbeeld werkregel, laadregel of verzending).</span><span class="sxs-lookup"><span data-stu-id="84162-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="84162-120">Maak een vrachtbrief-id en druk deze af op labels voordat de vrachtbrief wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="84162-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="84162-121">Maak voor elke doos een unieke Serial Shipping Container Code (SSCC) en voeg deze op elk label toe.</span><span class="sxs-lookup"><span data-stu-id="84162-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="84162-122">Maak GS1-compatibele nummerreeksen voor vrachtbrief-Id's en SSCC's.</span><span class="sxs-lookup"><span data-stu-id="84162-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="84162-123">Druk labels opnieuw af vanaf mobiele apparaten of rich clients.</span><span class="sxs-lookup"><span data-stu-id="84162-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="84162-124">Maak labels ongeldig (bijvoorbeeld in korte orderverzamelscenario's) en druk ze opnieuw af.</span><span class="sxs-lookup"><span data-stu-id="84162-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="84162-125">Schoon de wavelbelhistorie op.</span><span class="sxs-lookup"><span data-stu-id="84162-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="84162-126">Verbeteringen in indelingen voor documentroutering worden gedeeld tussen documentrouteringsindelingen en wavelabelindelingen.</span><span class="sxs-lookup"><span data-stu-id="84162-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="84162-127">(Zie voor meer informatie [Documentrouteringsindeling voor nummerplaten](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="84162-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="84162-128">Deze uitbreidingen maken het efficiënter om dozen te labelen voor palletisering.</span><span class="sxs-lookup"><span data-stu-id="84162-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="84162-129">Dit is met name handig voor bedrijven die naar grote winkels verzenden waar ontvangstbewijzen van orders automatisch worden bevestigd door het scannen van elke doos afzonderlijk.</span><span class="sxs-lookup"><span data-stu-id="84162-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="84162-130">U kunt de configuratiescenario's die in dit onderwerp worden beschreven, afzonderlijk of in combinatie implementeren, afhankelijk van uw zakelijke vereisten.</span><span class="sxs-lookup"><span data-stu-id="84162-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="84162-131">U kunt verschillende wavelabelsjablonen ontwerpen die in de juiste volgorde worden uitgevoerd (zoals aangegeven in scenario 3).</span><span class="sxs-lookup"><span data-stu-id="84162-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="84162-132">U kunt bijvoorbeeld scenario 1 gebruiken om labels voor dozen af te drukken en scenario 2 om palletlabels af te drukken (als de grootte en samenstelling van pallets verschillen).</span><span class="sxs-lookup"><span data-stu-id="84162-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="84162-133">De functie Wavelabels afdrukken inschakelen</span><span class="sxs-lookup"><span data-stu-id="84162-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="84162-134">Voordat u de functie *Wavelabels afdrukken* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="84162-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="84162-135">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="84162-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="84162-136">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="84162-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="84162-137">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="84162-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="84162-138">**Functienaam:** *Wavelabels afdrukken*</span><span class="sxs-lookup"><span data-stu-id="84162-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="84162-139">Scenario 1: Wavelabels afdrukken waarbij één wavelabel wordt gegenereerd</span><span class="sxs-lookup"><span data-stu-id="84162-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="84162-140">Dit scenario laat zien hoe een bedrijf verzendlabels afdrukt voor een grote detailhandelaar die ontvangstbewijzen automatisch bevestigt door elke doos afzonderlijk te scannen.</span><span class="sxs-lookup"><span data-stu-id="84162-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="84162-141">Dit scenario toont de volledige stroom.</span><span class="sxs-lookup"><span data-stu-id="84162-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="84162-142">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="84162-142">Make demo data available</span></span>

<span data-ttu-id="84162-143">Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.</span><span class="sxs-lookup"><span data-stu-id="84162-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="84162-144">Controleer of de wavelabelmethode beschikbaar is</span><span class="sxs-lookup"><span data-stu-id="84162-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="84162-145">Mogelijk moet u de waveverwerkingsmethoden opnieuw genereren om de methode voor het afdrukken van wavelabels beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="84162-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="84162-146">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.</span><span class="sxs-lookup"><span data-stu-id="84162-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="84162-147">Controleer of **waveLabelPrinting** in de lijst staat.</span><span class="sxs-lookup"><span data-stu-id="84162-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="84162-148">Als dat niet zo is, selecteert u **Methoden opnieuw genereren** in het actievenster om deze toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="84162-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="84162-149">Een wavesjabloon configureren</span><span class="sxs-lookup"><span data-stu-id="84162-149">Configure a wave template</span></span>

<span data-ttu-id="84162-150">Met wavesjablonen kunt u specifieke exemplaren van wavemethoden koppelen aan een corresponderende wavelabelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="84162-151">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="84162-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="84162-152">Selecteer een sjabloon zoals **62 Standaardverzending**.</span><span class="sxs-lookup"><span data-stu-id="84162-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="84162-153">Verplaats op het sneltabblad **Methoden** de methode **Wavelabels afdrukken** naar de kolom **Geselecteerde methoden**.</span><span class="sxs-lookup"><span data-stu-id="84162-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="84162-154">Selecteer in de kolom **Geselecteerde methoden** de methode **Wavelabels afdrukken** en stel het veld **Wavestapcode** in op *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="84162-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="84162-155">Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="84162-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="84162-156">Een wavelabelindeling maken</span><span class="sxs-lookup"><span data-stu-id="84162-156">Create a wave label layout</span></span>

<span data-ttu-id="84162-157">De labelindeling bepaalt welke informatie op het label wordt afgedrukt en hoe deze wordt ingedeeld. Hier voert u de ZPL-code in die naar de printer wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="84162-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="84162-158">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelindelingen**.</span><span class="sxs-lookup"><span data-stu-id="84162-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="84162-159">Maak een record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="84162-160">**Labelindeling-id:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="84162-161">**Omschrijving:** *doos (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="84162-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="84162-162">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-163">Selecteer in het actievenster **Instellingen voor wavelabelrijen**.</span><span class="sxs-lookup"><span data-stu-id="84162-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="84162-164">De pagina **Instellingen voor wavelabelrijen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="84162-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="84162-165">Hier kunt u het dynamische deel van het label configureren.</span><span class="sxs-lookup"><span data-stu-id="84162-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="84162-166">Voeg een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-167">**Rij-id:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="84162-168">**Naam van tabelrij:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="84162-169">**Beginpositie rij:** *0*</span><span class="sxs-lookup"><span data-stu-id="84162-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="84162-170">Dit veld bepaalt de verticale positie waar de rij begint op het label.</span><span class="sxs-lookup"><span data-stu-id="84162-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="84162-171">**Rijhoogte:** *0*</span><span class="sxs-lookup"><span data-stu-id="84162-171">**Row height:** *0*</span></span>

        <span data-ttu-id="84162-172">Dit veld definieert de hoogte van elke rij (in punten) volgens de ZPL-standaard.</span><span class="sxs-lookup"><span data-stu-id="84162-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="84162-173">De rijhoogte is positief voor horizontale labels en negatief voor verticale labels.</span><span class="sxs-lookup"><span data-stu-id="84162-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="84162-174">Omdat dit voorbeeld slechts één rij bevat, kunt u de waarde instellen op *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="84162-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="84162-175">**Rijen per pagina:** *1*</span><span class="sxs-lookup"><span data-stu-id="84162-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="84162-176">Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="84162-177">Deze instelling zorgt ervoor dat een afzonderlijk ZPL-label wordt afgedrukt voor elke record in de tabel met wavelabels.</span><span class="sxs-lookup"><span data-stu-id="84162-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="84162-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="84162-178">Close the page.</span></span>
1. <span data-ttu-id="84162-179">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="84162-180">Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-181">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-182">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-183">**Veld:** *Werktype*</span><span class="sxs-lookup"><span data-stu-id="84162-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="84162-184">**Criteria:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="84162-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="84162-185">Met deze query zorgt u ervoor dat alleen werkregels van het orderverzameltype worden afgedrukt op het label, niet de werkregels van het wegzettype.</span><span class="sxs-lookup"><span data-stu-id="84162-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="84162-186">Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe.</span><span class="sxs-lookup"><span data-stu-id="84162-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="84162-187">Sluit het dialoogvenster Query-editor.</span><span class="sxs-lookup"><span data-stu-id="84162-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="84162-188">Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**.</span><span class="sxs-lookup"><span data-stu-id="84162-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="84162-189">Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst.</span><span class="sxs-lookup"><span data-stu-id="84162-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="84162-190">Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.</span><span class="sxs-lookup"><span data-stu-id="84162-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="84162-191">Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst.</span><span class="sxs-lookup"><span data-stu-id="84162-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="84162-192">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="84162-193">Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst.</span><span class="sxs-lookup"><span data-stu-id="84162-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="84162-194">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="84162-195">Er wordt één exemplaar van elk label afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="84162-196">Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren.</span><span class="sxs-lookup"><span data-stu-id="84162-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="84162-197">Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.</span><span class="sxs-lookup"><span data-stu-id="84162-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="84162-198">Uw label is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="84162-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="84162-199">Een wavelabeltype maken</span><span class="sxs-lookup"><span data-stu-id="84162-199">Create a wave label type</span></span>

<span data-ttu-id="84162-200">Wavelabeltypen worden gebruikt om wavelabelsjablonen te koppelen aan een eenheid op de volgordegroepsregels van de eenheid.</span><span class="sxs-lookup"><span data-stu-id="84162-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="84162-201">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabeltypen**.</span><span class="sxs-lookup"><span data-stu-id="84162-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="84162-202">Voeg een wavelabeltype met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="84162-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="84162-203">**Labeltype:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="84162-204">**Omschrijving:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="84162-205">Eenheidvolgordegroepen instellen</span><span class="sxs-lookup"><span data-stu-id="84162-205">Set up unit sequence groups</span></span>

<span data-ttu-id="84162-206">Stel vervolgens de eenheidsvolgordegroep in voor het wavelabeltype.</span><span class="sxs-lookup"><span data-stu-id="84162-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="84162-207">Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Volgordegroepen eenheid**.</span><span class="sxs-lookup"><span data-stu-id="84162-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="84162-208">Selecteer de groep **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="84162-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="84162-209">Stel voor de regel **Doos** het veld **Waveniveautype** in op *Doos*.</span><span class="sxs-lookup"><span data-stu-id="84162-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="84162-210">Een wavelabelsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="84162-210">Create a wave label template</span></span>

<span data-ttu-id="84162-211">Maak vervolgens de wavelabelsjabloon voor het wavelabeltype.</span><span class="sxs-lookup"><span data-stu-id="84162-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="84162-212">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelsjablonen**.</span><span class="sxs-lookup"><span data-stu-id="84162-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="84162-213">Voeg een waveniveausjabloon toe en stel de volgende waarden in de koptekst in:</span><span class="sxs-lookup"><span data-stu-id="84162-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="84162-214">**Naam van labelsjabloon:** *Dooslabels*</span><span class="sxs-lookup"><span data-stu-id="84162-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="84162-215">**Omschrijving:** *Dooslabels*</span><span class="sxs-lookup"><span data-stu-id="84162-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="84162-216">**Wavestapcode:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="84162-217">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="84162-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84162-218">Stel op het sneltabblad **Algemeen** het veld **Wavelabeltype** in op *Doos*.</span><span class="sxs-lookup"><span data-stu-id="84162-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="84162-219">Voeg op het sneltabblad **Sjabloondetails van wavelabels** een nieuwe rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="84162-220">**Labelindeling-id:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="84162-221">**Printernaam:** selecteer een geschikte ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="84162-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="84162-222">**Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)</span><span class="sxs-lookup"><span data-stu-id="84162-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="84162-223">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-224">Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken.</span><span class="sxs-lookup"><span data-stu-id="84162-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="84162-225">Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="84162-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="84162-226">Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-227">**Tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-228">**Afgeleide tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-229">**Veld:** *Accountnummer*</span><span class="sxs-lookup"><span data-stu-id="84162-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="84162-230">**Criteria:** Voer het betreffende accountnummer van de klant in.</span><span class="sxs-lookup"><span data-stu-id="84162-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="84162-231">Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="84162-232">Selecteer in het actievenster de optie **Query bewerken** om het dialoogvenster Query-editor te openen voor de hele labelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="84162-233">Voeg in het dialoogvenster Query-editor op het tabblad **Sortering** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-234">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-235">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-236">**Veld:** *Verwijzing ladingsregel-id (record-id)*</span><span class="sxs-lookup"><span data-stu-id="84162-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="84162-237">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="84162-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="84162-238">Selecteer **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="84162-239">U wordt gevraagd om de bewerking voor het opnieuw instellen van de groepering te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="84162-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="84162-240">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="84162-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="84162-241">Selecteer in het actievenster **Sjabloongroep voor wavelabel**.</span><span class="sxs-lookup"><span data-stu-id="84162-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="84162-242">Selecteer in het dialoogvenster **Sjabloongroep voor wavelabel** de rij waar het veld **Verwijzing veldnaam** is ingesteld op *Verwijzing ladingsregel-id* en schakel vervolgens het selectievakje **Labelbuild-id** in voor deze rij.</span><span class="sxs-lookup"><span data-stu-id="84162-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84162-243">Met deze instelling wordt één labelreeks ("doos 1 van X") per ladingsregel gemaakt in de hele wave, ongeacht de instelling van de werkgroepering.</span><span class="sxs-lookup"><span data-stu-id="84162-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="84162-244">Deze labelreeks kan worden afgedrukt op de labelindeling.</span><span class="sxs-lookup"><span data-stu-id="84162-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="84162-245">Nummerreeksuitbreidingen configureren</span><span class="sxs-lookup"><span data-stu-id="84162-245">Configure number sequence extensions</span></span>

<span data-ttu-id="84162-246">Nummerreeksuitbreidingen bepalen de GS1-naleving van specifieke nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="84162-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="84162-247">Deze configuratie is optioneel voor het huidige scenario.</span><span class="sxs-lookup"><span data-stu-id="84162-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="84162-248">Zie [Nummerreeksuitbreidingen configureren](../warehousing/configure-number-sequence-extensions.md) voor meer informatie en configuratie-instructies.</span><span class="sxs-lookup"><span data-stu-id="84162-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="84162-249">Een verkooporder maken en vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="84162-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="84162-250">Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="84162-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="84162-251">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="84162-252">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="84162-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="84162-253">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="84162-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84162-254">Voeg twee verkooporderregels toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="84162-255">Verkooporderregel 1:</span><span class="sxs-lookup"><span data-stu-id="84162-255">Sales order line 1:</span></span>

        - <span data-ttu-id="84162-256">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="84162-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="84162-257">**Hoeveelheid:** *9024*</span><span class="sxs-lookup"><span data-stu-id="84162-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="84162-258">**Eenheid:** *ea* (9024 ea = 376 dozen = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="84162-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="84162-259">Verkooporderregel 2:</span><span class="sxs-lookup"><span data-stu-id="84162-259">Sales order line 2:</span></span>

        - <span data-ttu-id="84162-260">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="84162-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="84162-261">**Hoeveelheid:** *9016*</span><span class="sxs-lookup"><span data-stu-id="84162-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="84162-262">**Eenheid:** *ea* (9016 ea = 322 dozen = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="84162-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="84162-263">De artikelen en hoeveelheden die hier worden vermeld, dienen alleen als voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="84162-264">Ze moeten de volgordegroep van de eenheid gebruiken die u eerder hebt gedefinieerd. Er moeten correcte eenheidsomrekeningen van *ea* naar *doos* naar *PL* zijn gedefinieerd en ze moeten op voorraad zijn in magazijn *62*.</span><span class="sxs-lookup"><span data-stu-id="84162-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="84162-265">Zie [Maateenheid en voorraadbeleid](unit-measure-stocking-policies.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="84162-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="84162-266">Selecteer verkooporderregel 1.</span><span class="sxs-lookup"><span data-stu-id="84162-266">Select sales order line 1.</span></span> <span data-ttu-id="84162-267">Selecteer in de sectie **Verkooporderregel** in het menu **Voorraad** de optie **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="84162-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="84162-268">Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren** en sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="84162-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="84162-269">Herhaal stap 4 en 5 voor verkooporderregel 2.</span><span class="sxs-lookup"><span data-stu-id="84162-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="84162-270">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="84162-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="84162-271">De volgende gebeurtenissen vinden plaats:</span><span class="sxs-lookup"><span data-stu-id="84162-271">The following events occur:</span></span>

    - <span data-ttu-id="84162-272">Het systeem verwerkt de gemaakte zending met behulp van de sjabloon die de stap voor het afdrukken van labels bevat.</span><span class="sxs-lookup"><span data-stu-id="84162-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="84162-273">De labelindeling wordt gebruikt om de indeling van het label te definiëren en het resultaat is een label dat wordt afgedrukt op de printer die is geselecteerd in de labelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="84162-274">Er worden wavelabels gegenereerd en afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="84162-275">Het aantal labels komt overeen met het aantal dozen (in dit voorbeeld 376 labels voor regel 1 en 322 labels voor regel 2).</span><span class="sxs-lookup"><span data-stu-id="84162-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="84162-276">Er wordt een nieuwe vrachtbrief-id gegenereerd voor de zendingen.</span><span class="sxs-lookup"><span data-stu-id="84162-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="84162-277">Als u de nummerreeksuitbreidingen hebt geconfigureerd, volgen de wavelabel-id's de nummernotatie **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="84162-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="84162-278">U kunt wavelabels weergeven en opnieuw afdrukken op de volgende pagina's.</span><span class="sxs-lookup"><span data-stu-id="84162-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="84162-279">Selecteer in het actievenster van elke pagina op het tabblad **Zendingen** in de groep **Verwante informatie** de optie **Wavelabels**.</span><span class="sxs-lookup"><span data-stu-id="84162-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="84162-280">Alle zendingen \> Details van zending</span><span class="sxs-lookup"><span data-stu-id="84162-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="84162-281">Alle ladingen \> Details van lading</span><span class="sxs-lookup"><span data-stu-id="84162-281">All loads \> Load details</span></span>
- <span data-ttu-id="84162-282">Alle waves</span><span class="sxs-lookup"><span data-stu-id="84162-282">All waves</span></span>
- <span data-ttu-id="84162-283">Wavelabels</span><span class="sxs-lookup"><span data-stu-id="84162-283">Wave labels</span></span>
- <span data-ttu-id="84162-284">Historie wavelabel</span><span class="sxs-lookup"><span data-stu-id="84162-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="84162-285">Scenario 2: Wavelabels afdrukken voor containers (zonder wavelabelrecords)</span><span class="sxs-lookup"><span data-stu-id="84162-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="84162-286">Met dit scenario kunt u wavelabels wanneer u containers gebruikt om artikelen automatisch in dozen te splitsen, zodat u geen wavelabelrecord hoeft te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="84162-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="84162-287">In dit geval fungeert de container-id als tijdelijke aanduiding voor de SSCC.</span><span class="sxs-lookup"><span data-stu-id="84162-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="84162-288">Dit zijn de belangrijkste verschillen tussen dit scenario en scenario 1:</span><span class="sxs-lookup"><span data-stu-id="84162-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="84162-289">**Sjablonen voor wavelabels:** u selecteert geen wavelabeltype in de sjabloon voor wavelabels en u hebt geen labelbuildgroepering nodig.</span><span class="sxs-lookup"><span data-stu-id="84162-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="84162-290">Anders configureert u de wavelabelsjabloon en gaat u op dezelfde manier naar de wavesjabloon als in scenario 1 wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="84162-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="84162-291">U moet het naar de wavelabeltype leeg laten om te voorkomen dat er wavelabels worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="84162-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="84162-292">**Indeling van wavelabels:** u configureert de instellingen voor de rij met de wavelabelindeling voor werkregels in plaats van wavelabelrecords.</span><span class="sxs-lookup"><span data-stu-id="84162-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="84162-293">U moet de rij-instelling voor de labelindeling configureren met de tabel **WHSWorkLine** in plaats van de tabel **WHSWaveLabel**.</span><span class="sxs-lookup"><span data-stu-id="84162-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="84162-294">De instelling **Rijen per pagina** bepaalt het aantal rijen dat de hoofdsectie zal hebben.</span><span class="sxs-lookup"><span data-stu-id="84162-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="84162-295">Deze configuratie is ook geschikt voor zakelijke scenario's waarbij meerdere verschillende artikelen in één gelabelde door of pallet worden verpakt. Dit verpakkingsproces kan worden gedefinieerd door het maken van werk (bijvoorbeeld werk dat is gegroepeerd op zending).</span><span class="sxs-lookup"><span data-stu-id="84162-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="84162-296">Dit scenario toont de volledige stroom.</span><span class="sxs-lookup"><span data-stu-id="84162-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="84162-297">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="84162-297">Make demo data available</span></span>

<span data-ttu-id="84162-298">Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.</span><span class="sxs-lookup"><span data-stu-id="84162-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="84162-299">Controleer of de wavelabelmethode beschikbaar is</span><span class="sxs-lookup"><span data-stu-id="84162-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="84162-300">Mogelijk moet u de waveverwerkingsmethoden opnieuw genereren om de methode voor het afdrukken van wavelabels beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="84162-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="84162-301">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.</span><span class="sxs-lookup"><span data-stu-id="84162-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="84162-302">Controleer of **waveLabelPrinting** in de lijst staat.</span><span class="sxs-lookup"><span data-stu-id="84162-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="84162-303">Als dat niet zo is, selecteert u **Methoden opnieuw genereren** in het actievenster om deze toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="84162-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="84162-304">Een wavesjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="84162-304">Set up a wave template</span></span>

<span data-ttu-id="84162-305">Met wavesjablonen kunt u specifieke exemplaren van wavemethoden koppelen aan een corresponderende wavelabelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="84162-306">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="84162-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="84162-307">Selecteer een sjabloon zoals **63 Containervorming**.</span><span class="sxs-lookup"><span data-stu-id="84162-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="84162-308">Verplaats op het sneltabblad **Methoden** de methode **Wavelabels afdrukken** naar de kolom **Geselecteerde methoden**.</span><span class="sxs-lookup"><span data-stu-id="84162-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="84162-309">Selecteer in de kolom **Geselecteerde methoden** de methode **Wavelabels afdrukken** en stel het veld **Wavestapcode** in op *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="84162-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="84162-310">Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="84162-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="84162-311">Een wavelabelindeling maken</span><span class="sxs-lookup"><span data-stu-id="84162-311">Create a wave label layout</span></span>

1. <span data-ttu-id="84162-312">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelindelingen**.</span><span class="sxs-lookup"><span data-stu-id="84162-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="84162-313">Maak een record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="84162-314">**Labelindeling-id:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="84162-315">**Omschrijving:** *doos (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="84162-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="84162-316">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-317">Selecteer in het actievenster **Instellingen voor wavelabelrijen**.</span><span class="sxs-lookup"><span data-stu-id="84162-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="84162-318">De pagina **Instellingen voor wavelabelrijen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="84162-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="84162-319">Hier kunt u het dynamische deel van het label configureren.</span><span class="sxs-lookup"><span data-stu-id="84162-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="84162-320">Voeg een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-321">**Rij-id:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="84162-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="84162-322">**Naam van tabelrij:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="84162-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="84162-323">**Beginpositie rij:** *500*</span><span class="sxs-lookup"><span data-stu-id="84162-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="84162-324">Dit veld bepaalt de verticale positie waar de rij begint op het label.</span><span class="sxs-lookup"><span data-stu-id="84162-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="84162-325">**Rijhoogte:** *-50*</span><span class="sxs-lookup"><span data-stu-id="84162-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="84162-326">In dit veld wordt de hoogte van elke rij gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="84162-326">This field defines the height of each row.</span></span> <span data-ttu-id="84162-327">De rijhoogte is positief voor horizontale labels en negatief voor verticale labels.</span><span class="sxs-lookup"><span data-stu-id="84162-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="84162-328">**Rijen per pagina:** *5*</span><span class="sxs-lookup"><span data-stu-id="84162-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="84162-329">Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="84162-330">Er worden verschillende ZPL-labels per taak afgedrukt, waarbij elke pagina maximaal vijf werkregels kan bevatten.</span><span class="sxs-lookup"><span data-stu-id="84162-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="84162-331">Als er bijvoorbeeld een label wordt afgedrukt voor een container met 12 regels, worden drie labels afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="84162-332">Als u een afzonderlijk label wilt afdrukken voor elke orderverzamelregel, stelt u deze waarde in op *1*.</span><span class="sxs-lookup"><span data-stu-id="84162-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="84162-333">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="84162-333">Close the page.</span></span>
1. <span data-ttu-id="84162-334">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="84162-335">Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-336">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-337">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-338">**Veld:** *Werktype*</span><span class="sxs-lookup"><span data-stu-id="84162-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="84162-339">**Criteria:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="84162-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="84162-340">Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe.</span><span class="sxs-lookup"><span data-stu-id="84162-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="84162-341">Sluit het dialoogvenster Query-editor.</span><span class="sxs-lookup"><span data-stu-id="84162-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="84162-342">Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**.</span><span class="sxs-lookup"><span data-stu-id="84162-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="84162-343">Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst.</span><span class="sxs-lookup"><span data-stu-id="84162-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="84162-344">Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.</span><span class="sxs-lookup"><span data-stu-id="84162-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="84162-345">Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst.</span><span class="sxs-lookup"><span data-stu-id="84162-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="84162-346">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="84162-347">Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst.</span><span class="sxs-lookup"><span data-stu-id="84162-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="84162-348">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="84162-349">Er wordt één exemplaar van elk label afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="84162-350">Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren.</span><span class="sxs-lookup"><span data-stu-id="84162-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="84162-351">Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.</span><span class="sxs-lookup"><span data-stu-id="84162-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="84162-352">Uw label is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="84162-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="84162-353">Een wavelabelsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="84162-353">Create a wave label template</span></span>

1. <span data-ttu-id="84162-354">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelsjablonen**.</span><span class="sxs-lookup"><span data-stu-id="84162-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="84162-355">Voeg een waveniveausjabloon toe en stel de volgende waarden in de koptekst in:</span><span class="sxs-lookup"><span data-stu-id="84162-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="84162-356">**Naam van labelsjabloon:** *Containerlabels*</span><span class="sxs-lookup"><span data-stu-id="84162-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="84162-357">**Omschrijving:** *Containerlabels*</span><span class="sxs-lookup"><span data-stu-id="84162-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="84162-358">**Wavestapcode:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="84162-359">**Magazijn:** *63*</span><span class="sxs-lookup"><span data-stu-id="84162-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="84162-360">Voeg op het sneltabblad **Sjabloondetails van wavelabels** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-361">**Labelindeling-id:** *Container*</span><span class="sxs-lookup"><span data-stu-id="84162-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="84162-362">**Printernaam:** selecteer een geschikte ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="84162-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="84162-363">**Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)</span><span class="sxs-lookup"><span data-stu-id="84162-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="84162-364">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-365">Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken.</span><span class="sxs-lookup"><span data-stu-id="84162-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="84162-366">Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="84162-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="84162-367">Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-368">**Tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-369">**Afgeleide tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-370">**Veld:** *Accountnummer*</span><span class="sxs-lookup"><span data-stu-id="84162-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="84162-371">**Criteria:** Voer het betreffende accountnummer van de klant in.</span><span class="sxs-lookup"><span data-stu-id="84162-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="84162-372">Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="84162-373">Nummerreeksuitbreidingen configureren</span><span class="sxs-lookup"><span data-stu-id="84162-373">Configure number sequence extensions</span></span>

<span data-ttu-id="84162-374">Nummerreeksuitbreidingen bepalen de GS1-naleving van specifieke nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="84162-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="84162-375">Deze configuratie is optioneel voor het huidige scenario.</span><span class="sxs-lookup"><span data-stu-id="84162-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="84162-376">Zie [Nummerreeksuitbreidingen configureren](../warehousing/configure-number-sequence-extensions.md) voor meer informatie en configuratie-instructies.</span><span class="sxs-lookup"><span data-stu-id="84162-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="84162-377">Een verkooporder maken en vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="84162-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="84162-378">Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="84162-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="84162-379">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="84162-380">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="84162-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="84162-381">**Magazijn:** *63*</span><span class="sxs-lookup"><span data-stu-id="84162-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="84162-382">Vijf verkooporderregels toevoegen:</span><span class="sxs-lookup"><span data-stu-id="84162-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="84162-383">Verkooporderregel 1:</span><span class="sxs-lookup"><span data-stu-id="84162-383">Sales order line 1:</span></span>

        - <span data-ttu-id="84162-384">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="84162-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="84162-385">**Hoeveelheid:** *10*</span><span class="sxs-lookup"><span data-stu-id="84162-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="84162-386">Verkooporderregel 2:</span><span class="sxs-lookup"><span data-stu-id="84162-386">Sales order line 2:</span></span>

        - <span data-ttu-id="84162-387">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="84162-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="84162-388">**Hoeveelheid:** *20*</span><span class="sxs-lookup"><span data-stu-id="84162-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="84162-389">Verkooporderregel 3:</span><span class="sxs-lookup"><span data-stu-id="84162-389">Sales order line 3:</span></span>

        - <span data-ttu-id="84162-390">**Artikelnummer:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="84162-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="84162-391">**Hoeveelheid:** *20*</span><span class="sxs-lookup"><span data-stu-id="84162-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="84162-392">Verkooporderregel 4:</span><span class="sxs-lookup"><span data-stu-id="84162-392">Sales order line 4:</span></span>

        - <span data-ttu-id="84162-393">**Artikelnummer:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="84162-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="84162-394">**Hoeveelheid:** *40*</span><span class="sxs-lookup"><span data-stu-id="84162-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="84162-395">Verkooporderregel 5:</span><span class="sxs-lookup"><span data-stu-id="84162-395">Sales order line 5:</span></span>

        - <span data-ttu-id="84162-396">**Artikelnummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="84162-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="84162-397">**Hoeveelheid:** *50*</span><span class="sxs-lookup"><span data-stu-id="84162-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="84162-398">De artikelen en hoeveelheden die hier worden vermeld, dienen alleen als voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="84162-399">Er moet voorraad aanwezig zijn in het opgegeven magazijn.</span><span class="sxs-lookup"><span data-stu-id="84162-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="84162-400">Selecteer verkooporderregel 1.</span><span class="sxs-lookup"><span data-stu-id="84162-400">Select sales order line 1.</span></span> <span data-ttu-id="84162-401">Selecteer in de sectie **Verkooporderregel** in het menu **Voorraad** de optie **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="84162-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="84162-402">Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren** en sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="84162-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="84162-403">Herhaal stap 4 en 5 elke extra verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="84162-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="84162-404">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="84162-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="84162-405">De volgende gebeurtenissen vinden plaats:</span><span class="sxs-lookup"><span data-stu-id="84162-405">The following events occur:</span></span>

    - <span data-ttu-id="84162-406">Het systeem verwerkt de gemaakte zending met de sjabloon die de stap voor het afdrukken van labels bevat.</span><span class="sxs-lookup"><span data-stu-id="84162-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="84162-407">De labelindeling wordt gebruikt om de indeling van het label te definiëren en het eindresultaat is een label met vijf regels dat wordt afgedrukt op de printer die is geselecteerd in de labelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="84162-408">Er wordt een nieuwe vrachtbrief-id gegenereerd voor de zendingen.</span><span class="sxs-lookup"><span data-stu-id="84162-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="84162-409">Als u de nummerreeksuitbreidingen hebt geconfigureerd, volgen de wavelabel-id's de nummernotatie **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="84162-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="84162-410">U kunt deze wavelabels opnieuw afdrukken via **Magazijnbeheer \> Query's en rapporten \> Historie van wavelabels**.</span><span class="sxs-lookup"><span data-stu-id="84162-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="84162-411">Scenario 3: Wavelabels afdrukken voor labels met meerdere lagen</span><span class="sxs-lookup"><span data-stu-id="84162-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="84162-412">In dit scenario ziet u hoe u de functie voor het afdrukken van wavelabels gebruikt wanneer voor de magazijnprocessen verschillende niveaus van verzendlabels nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="84162-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="84162-413">Het kan bijvoorbeeld voorkomen dat afzonderlijke labels voor dozen en pallets moeten worden afgedrukt en dat een onderbrekingslabel voor een hele zending moet worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="84162-414">Onderbrekingslabels zijn een afzonderlijk labeltype dat kan worden gebruikt als scheiding tussen rollen en containers, zoals labels voor de zendings-id en een streepjescode, zodat de labels gemakkelijk kunnen worden gesorteerd nadat ze zijn afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="84162-415">Het belangrijkste verschil tussen de configuratie van dit scenario en de configuratie van scenario 1 is, naast dat onderbrekingslabels zijn ingeschakeld, er meerdere wavelabeltypen moeten worden gekoppeld aan wavelabelsjablonen en aan regels voor de volgordegroep van de eenheid.</span><span class="sxs-lookup"><span data-stu-id="84162-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="84162-416">Als u deze configuratie wilt voltooien, stelt u de volgende elementen in voor dit scenario:</span><span class="sxs-lookup"><span data-stu-id="84162-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="84162-417">**Waveverwerkingsmethoden:** u markeert de wavelabelmethode als 'herhaalbaar', voegt deze twee (of meer) keer toe aan de wavesjabloon en stelt verschillende wavestapcodes in.</span><span class="sxs-lookup"><span data-stu-id="84162-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="84162-418">**Sjablonen voor wavelabels:** u configureert de wavelabelsjablonen en koppelt deze aan de wavesjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="84162-419">Elke wavelabelsjabloon heeft een eigen wavelabeltype.</span><span class="sxs-lookup"><span data-stu-id="84162-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="84162-420">**Indelingen van wavelabel:** u maakt meerdere wavelabelindelingen.</span><span class="sxs-lookup"><span data-stu-id="84162-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="84162-421">Er is een afzonderlijke labelindeling voor elke categorie labels en er is ook een indeling voor onderbrekingslabels.</span><span class="sxs-lookup"><span data-stu-id="84162-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="84162-422">Dit scenario toont de volledige stroom.</span><span class="sxs-lookup"><span data-stu-id="84162-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="84162-423">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="84162-423">Make demo data available</span></span>

<span data-ttu-id="84162-424">Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.</span><span class="sxs-lookup"><span data-stu-id="84162-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="84162-425">Een waveverwerkingsmethode instellen</span><span class="sxs-lookup"><span data-stu-id="84162-425">Set up a wave process method</span></span>

1. <span data-ttu-id="84162-426">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.</span><span class="sxs-lookup"><span data-stu-id="84162-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="84162-427">Controleer of **waveLabelPrinting** in de lijst staat.</span><span class="sxs-lookup"><span data-stu-id="84162-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="84162-428">Als dat niet zo is, selecteert u **Methoden opnieuw genereren** in het actievenster om deze toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="84162-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="84162-429">Voor de methode **waveLabelPrinting** schakelt u het selectievakje **Methode herhaalbaar maken** in.</span><span class="sxs-lookup"><span data-stu-id="84162-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="84162-430">Een wavesjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="84162-430">Set up a wave template</span></span>

1. <span data-ttu-id="84162-431">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="84162-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="84162-432">Selecteer een sjabloon zoals **62 Standaardverzending**.</span><span class="sxs-lookup"><span data-stu-id="84162-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="84162-433">Verplaats op het sneltabblad **Methoden** de methode **Wavelabels afdrukken** naar de kolom **Geselecteerde methoden**.</span><span class="sxs-lookup"><span data-stu-id="84162-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="84162-434">Wijs in de kolom **Geselecteerde methoden** een **wavestapcode** toe, zoals *doos*, aan de **Afdrukmethode voor wavelabels**.</span><span class="sxs-lookup"><span data-stu-id="84162-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="84162-435">Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="84162-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="84162-436">Verplaats de methode **Wavelabels afdrukken** nogmaals naar de kolom **Geselecteerde methoden**.</span><span class="sxs-lookup"><span data-stu-id="84162-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="84162-437">Wijs in de kolom **Geselecteerde methoden** een andere **wavestapcode** toe, zoals *pallet*, aan de tweede **Afdrukmethode voor wavelabels**.</span><span class="sxs-lookup"><span data-stu-id="84162-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="84162-438">Zie [Wavestapcodes](wave-step-codes.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="84162-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="84162-439">Drie wavelabelindelingen maken</span><span class="sxs-lookup"><span data-stu-id="84162-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="84162-440">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelindelingen**.</span><span class="sxs-lookup"><span data-stu-id="84162-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="84162-441">Maak een record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="84162-442">**Labelindeling-id:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="84162-443">**Omschrijving:** *doos (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="84162-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="84162-444">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-445">Selecteer in het actievenster **Instellingen voor wavelabelrijen**.</span><span class="sxs-lookup"><span data-stu-id="84162-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="84162-446">De pagina **Instellingen voor wavelabelrijen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="84162-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="84162-447">Hier kunt u het dynamische deel van het label configureren.</span><span class="sxs-lookup"><span data-stu-id="84162-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="84162-448">Voeg een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-449">**Rij-id:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="84162-450">**Naam van tabelrij:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="84162-451">**Beginpositie rij:** *0*</span><span class="sxs-lookup"><span data-stu-id="84162-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="84162-452">Dit veld bepaalt de verticale positie waar de rij begint op het label.</span><span class="sxs-lookup"><span data-stu-id="84162-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="84162-453">**Rijhoogte:** *0*</span><span class="sxs-lookup"><span data-stu-id="84162-453">**Row height:** *0*</span></span>

        <span data-ttu-id="84162-454">Dit veld definieert de hoogte van elke rij (in punten) volgens de ZPL-standaard.</span><span class="sxs-lookup"><span data-stu-id="84162-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="84162-455">De rijhoogte is positief voor horizontale labels en negatief voor verticale labels.</span><span class="sxs-lookup"><span data-stu-id="84162-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="84162-456">Omdat dit voorbeeld slechts één rij bevat, kunt u de waarde instellen op *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="84162-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="84162-457">**Rijen per pagina:** *1*</span><span class="sxs-lookup"><span data-stu-id="84162-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="84162-458">Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="84162-459">Deze instelling zorgt ervoor dat een afzonderlijk ZPL-label wordt afgedrukt voor elke record in de tabel met wavelabels.</span><span class="sxs-lookup"><span data-stu-id="84162-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="84162-460">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="84162-460">Close the page.</span></span>
1. <span data-ttu-id="84162-461">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="84162-462">Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-463">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-464">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-465">**Veld:** *Werktype*</span><span class="sxs-lookup"><span data-stu-id="84162-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="84162-466">**Criteria:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="84162-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="84162-467">Met deze query zorgt u ervoor dat alleen werkregels van het orderverzameltype worden afgedrukt op het label, niet de werkregels van het wegzettype.</span><span class="sxs-lookup"><span data-stu-id="84162-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="84162-468">Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe.</span><span class="sxs-lookup"><span data-stu-id="84162-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="84162-469">Sluit het dialoogvenster Query-editor.</span><span class="sxs-lookup"><span data-stu-id="84162-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="84162-470">Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**.</span><span class="sxs-lookup"><span data-stu-id="84162-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="84162-471">Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst.</span><span class="sxs-lookup"><span data-stu-id="84162-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="84162-472">Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.</span><span class="sxs-lookup"><span data-stu-id="84162-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="84162-473">Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst.</span><span class="sxs-lookup"><span data-stu-id="84162-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="84162-474">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="84162-475">Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst.</span><span class="sxs-lookup"><span data-stu-id="84162-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="84162-476">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="84162-477">Er wordt één exemplaar van elk label afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="84162-478">Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren.</span><span class="sxs-lookup"><span data-stu-id="84162-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="84162-479">Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.</span><span class="sxs-lookup"><span data-stu-id="84162-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="84162-480">Het eerste label is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="84162-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="84162-481">Maak een tweede indelingsrecord met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="84162-482">**Labelindeling-id:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="84162-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="84162-483">**Omschrijving:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="84162-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="84162-484">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-485">Selecteer in het actievenster **Instellingen voor wavelabelrijen**.</span><span class="sxs-lookup"><span data-stu-id="84162-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="84162-486">De pagina **Instellingen voor wavelabelrijen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="84162-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="84162-487">Hier kunt u het dynamische deel van het label configureren.</span><span class="sxs-lookup"><span data-stu-id="84162-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="84162-488">Voeg een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-489">**Rij-id:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="84162-490">**Naam van tabelrij:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="84162-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="84162-491">**Beginpositie rij:** *0*</span><span class="sxs-lookup"><span data-stu-id="84162-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="84162-492">Dit veld bepaalt de verticale positie waar de rij begint op het label.</span><span class="sxs-lookup"><span data-stu-id="84162-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="84162-493">**Rijhoogte:** *0*</span><span class="sxs-lookup"><span data-stu-id="84162-493">**Row height:** *0*</span></span>

        <span data-ttu-id="84162-494">Dit veld definieert de hoogte van elke rij (in punten) volgens de ZPL-standaard.</span><span class="sxs-lookup"><span data-stu-id="84162-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="84162-495">De rijhoogte is positief voor horizontale labels en negatief voor verticale labels.</span><span class="sxs-lookup"><span data-stu-id="84162-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="84162-496">Omdat dit voorbeeld slechts één rij bevat, kunt u de waarde instellen op *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="84162-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="84162-497">**Rijen per pagina:** *1*</span><span class="sxs-lookup"><span data-stu-id="84162-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="84162-498">Dit veld bepaalt het aantal rijen dat op elk label kan worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="84162-499">Deze instelling zorgt ervoor dat een afzonderlijk ZPL-label wordt afgedrukt voor elke record in de tabel met wavelabels.</span><span class="sxs-lookup"><span data-stu-id="84162-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="84162-500">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="84162-500">Close the page.</span></span>
1. <span data-ttu-id="84162-501">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="84162-502">Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-503">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-504">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-505">**Veld:** *Werktype*</span><span class="sxs-lookup"><span data-stu-id="84162-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="84162-506">**Criteria:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="84162-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="84162-507">Met deze query zorgt u ervoor dat alleen werkregels van het orderverzameltype worden afgedrukt op het label, niet de werkregels van het wegzettype.</span><span class="sxs-lookup"><span data-stu-id="84162-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="84162-508">Als u de vrachtbrief-id wilt kunnen afdrukken, selecteert u op het tabblad **Joins** de tabel **Werkregels** en voegt u de tabel **Zendingen** eraan toe.</span><span class="sxs-lookup"><span data-stu-id="84162-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="84162-509">Sluit het dialoogvenster Query-editor.</span><span class="sxs-lookup"><span data-stu-id="84162-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="84162-510">Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**.</span><span class="sxs-lookup"><span data-stu-id="84162-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="84162-511">Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de code in voor de vereiste koptekst.</span><span class="sxs-lookup"><span data-stu-id="84162-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="84162-512">Als u bijvoorbeeld Zebra-printers gebruikt, kunt u de volgende code gebruiken.</span><span class="sxs-lookup"><span data-stu-id="84162-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="84162-513">Voer in de **Hoofdsectie** in het veld **Labelhoofdtekst** ZPL-code in voor de vereiste hoofdtekst.</span><span class="sxs-lookup"><span data-stu-id="84162-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="84162-514">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="84162-515">Voer in de **Hoofdsectie** in het veld **Labelvoettekst** ZPL-code in voor de vereiste voettekst.</span><span class="sxs-lookup"><span data-stu-id="84162-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="84162-516">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="84162-517">Er wordt één exemplaar van elk label afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="84162-518">Als u meer exemplaren nodig hebt (bijvoorbeeld één exemplaar voor elke zijde van de pallet), stelt u de waarde **n** voor de sectie **\^PQn** in de voettekst in op het vereiste aantal exemplaren.</span><span class="sxs-lookup"><span data-stu-id="84162-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="84162-519">Als u bijvoorbeeld vier kopieën van elk label wilt afdrukken, geeft u **\^PQ4** op.</span><span class="sxs-lookup"><span data-stu-id="84162-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="84162-520">Het tweede label is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="84162-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="84162-521">Maak een derde indelingsrecord met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="84162-522">**Labelindeling-id:** *Onderbreking*</span><span class="sxs-lookup"><span data-stu-id="84162-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="84162-523">**Beschrijving:** *Onderbrekingslabel*</span><span class="sxs-lookup"><span data-stu-id="84162-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="84162-524">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-525">Het sneltabblad **Printertekstindeling** bevat drie secties waarin u printercode kunt schrijven: **koptekstsectie**, **hoofdsectie** en **voettekstsectie**.</span><span class="sxs-lookup"><span data-stu-id="84162-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="84162-526">Voer in de **Koptekstsectie** in het veld **Labelkoptekst** de ZPL-code in voor de vereiste koptekst.</span><span class="sxs-lookup"><span data-stu-id="84162-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="84162-527">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="84162-528">Deze keer is er geen hoofdtekst verplicht.</span><span class="sxs-lookup"><span data-stu-id="84162-528">This time, no body is required.</span></span> <span data-ttu-id="84162-529">Voer daarom alleen de vereiste tekst in de **Voettekstsectie** in.</span><span class="sxs-lookup"><span data-stu-id="84162-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="84162-530">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="84162-531">Het derde label is nu klaar voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="84162-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84162-532">Dit derde label is een onderbrekingslabel dat wordt gebruikt als scheiding tussen labelrollen.</span><span class="sxs-lookup"><span data-stu-id="84162-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="84162-533">Twee wavelabeltypen maken</span><span class="sxs-lookup"><span data-stu-id="84162-533">Create two wave label types</span></span>

1. <span data-ttu-id="84162-534">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabeltypen**.</span><span class="sxs-lookup"><span data-stu-id="84162-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="84162-535">Maak een record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="84162-536">**Labeltype:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="84162-537">**Omschrijving:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="84162-538">Maak een tweede record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="84162-539">**Labeltype:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="84162-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="84162-540">**Omschrijving:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="84162-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="84162-541">Eenheidvolgordegroepen instellen</span><span class="sxs-lookup"><span data-stu-id="84162-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="84162-542">Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Volgordegroepen eenheid**.</span><span class="sxs-lookup"><span data-stu-id="84162-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="84162-543">Selecteer of maak een groep **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="84162-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="84162-544">Stel voor de regel **Doos** het veld **Waveniveautype** in op *Doos*.</span><span class="sxs-lookup"><span data-stu-id="84162-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="84162-545">Stel voor de regel **PL** het veld **Waveniveautype** in op *Pallet*.</span><span class="sxs-lookup"><span data-stu-id="84162-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="84162-546">Wavelabelsjablonen maken</span><span class="sxs-lookup"><span data-stu-id="84162-546">Create wave label templates</span></span>

1. <span data-ttu-id="84162-547">Ga naar **Magazijnbeheer \> Instellingen \> Documentroutering \> Wavelabelsjablonen**.</span><span class="sxs-lookup"><span data-stu-id="84162-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="84162-548">Maak een labelsjabloon met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="84162-549">**Naam van labelsjabloon:** *Dooslabels*</span><span class="sxs-lookup"><span data-stu-id="84162-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="84162-550">**Omschrijving:** *Dooslabels*</span><span class="sxs-lookup"><span data-stu-id="84162-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="84162-551">**Wavestapcode:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="84162-552">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="84162-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84162-553">Op het sneltabblad **Algemeen** selecteert u een waarde zoals **Doos** in het veld *Wavelabeltype*.</span><span class="sxs-lookup"><span data-stu-id="84162-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="84162-554">Voeg op het sneltabblad **Sjabloondetails van wavelabels** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-555">**Labelindeling-id:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="84162-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="84162-556">**Printernaam:** selecteer een geschikte ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="84162-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="84162-557">**Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)</span><span class="sxs-lookup"><span data-stu-id="84162-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="84162-558">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-559">Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken.</span><span class="sxs-lookup"><span data-stu-id="84162-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="84162-560">Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="84162-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="84162-561">Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-562">**Tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-563">**Afgeleide tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-564">**Veld:** *Accountnummer*</span><span class="sxs-lookup"><span data-stu-id="84162-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="84162-565">**Criteria:** Voer het betreffende accountnummer van de klant in.</span><span class="sxs-lookup"><span data-stu-id="84162-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="84162-566">Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="84162-567">Selecteer in het actievenster de optie **Query bewerken** om het dialoogvenster Query-editor te openen voor de hele labelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="84162-568">Voeg in het dialoogvenster Query-editor op het tabblad **Sortering** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-569">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-570">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-571">**Veld:** *Verwijzing ladingsregel-id (record-id)*</span><span class="sxs-lookup"><span data-stu-id="84162-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="84162-572">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="84162-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="84162-573">Voeg een tweede rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="84162-574">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-575">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-576">**Veld:** *Zending-id*</span><span class="sxs-lookup"><span data-stu-id="84162-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="84162-577">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="84162-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="84162-578">Selecteer **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="84162-579">U wordt gevraagd om de bewerking voor het opnieuw instellen van de groepering te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="84162-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="84162-580">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="84162-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="84162-581">Selecteer in het actievenster **Sjabloongroep voor wavelabel**.</span><span class="sxs-lookup"><span data-stu-id="84162-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="84162-582">Stel in het dialoogvenster **Sjabloongroep voor wavelabel** de volgende waarden in voor de rij waarin het veld **Naam verwijzingsveld** is ingesteld op *Zending-id*:</span><span class="sxs-lookup"><span data-stu-id="84162-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="84162-583">**Onderbrekingslabel afdrukken:** schakel dit selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="84162-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="84162-584">**Labelindelings-id:** selecteer een onderbrekingslabel.</span><span class="sxs-lookup"><span data-stu-id="84162-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="84162-585">(Selecteer bijvoorbeeld de indeling *Onderbrekingslabel* die u eerder in dit scenario hebt gemaakt.)</span><span class="sxs-lookup"><span data-stu-id="84162-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="84162-586">**Printernaam:** selecteer de printer voor het onderbrekingslabel.</span><span class="sxs-lookup"><span data-stu-id="84162-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="84162-587">(Gewoonlijk moet u voor het splitsen van labelrollen dezelfde printer selecteren die is geselecteerd op het Het sneltabblad **Sjabloondetails van wavelabel**.</span><span class="sxs-lookup"><span data-stu-id="84162-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="84162-588">Er zijn echter andere scenario's mogelijk.)</span><span class="sxs-lookup"><span data-stu-id="84162-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="84162-589">Schakel het selectievakje **Labelbuild-id** in voor de rij waarin het veld *Naam verwijzingsveld* is ingesteld op **Verwijzing ladingsregel-id**.</span><span class="sxs-lookup"><span data-stu-id="84162-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84162-590">Met deze instelling wordt één labelreeks ("doos 1 van X") per ladingsregel gemaakt in de hele wave, ongeacht de instelling van de werkgroepering.</span><span class="sxs-lookup"><span data-stu-id="84162-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="84162-591">Deze labelreeks kan worden afgedrukt op een labelindeling.</span><span class="sxs-lookup"><span data-stu-id="84162-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="84162-592">Bovendien worden labels voor verschillende zendingen gescheiden door het geselecteerde onderbrekingslabel.</span><span class="sxs-lookup"><span data-stu-id="84162-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="84162-593">Selecteer **OK** om het dialoogvenster **Sjabloongroep voor wavelabel** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="84162-594">Maak een tweede labelsjabloon met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="84162-595">**Naam van labelsjabloon:** *Palletlabels*</span><span class="sxs-lookup"><span data-stu-id="84162-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="84162-596">**Omschrijving:** *Palletlabels*</span><span class="sxs-lookup"><span data-stu-id="84162-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="84162-597">**Wavestapcode:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="84162-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="84162-598">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="84162-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84162-599">Op het sneltabblad **Algemeen** selecteert u een waarde zoals **Pallet** in het veld *Wavelabeltype*.</span><span class="sxs-lookup"><span data-stu-id="84162-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="84162-600">Voeg op het sneltabblad **Sjabloondetails van wavelabels** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-601">**Labelindeling-id:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="84162-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="84162-602">**Printernaam:** selecteer een geschikte ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="84162-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="84162-603">**Query uitvoeren:** *Ja* (deze instelling is optioneel, maar wordt wel aanbevolen voor optimale prestaties.)</span><span class="sxs-lookup"><span data-stu-id="84162-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="84162-604">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="84162-605">Optioneel: als u een klantspecifiek labelontwerp instelt, moet u een query maken om het klantaccount te zoeken.</span><span class="sxs-lookup"><span data-stu-id="84162-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="84162-606">Ga naar het sneltabblad **Sjabloondetails van wavelabels** en selecteer **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="84162-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="84162-607">Voeg vervolgens in het dialoogvenster Query-editor op het tabblad **Bereik** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-608">**Tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-609">**Afgeleide tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="84162-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="84162-610">**Veld:** *Accountnummer*</span><span class="sxs-lookup"><span data-stu-id="84162-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="84162-611">**Criteria:** Voer het betreffende accountnummer van de klant in.</span><span class="sxs-lookup"><span data-stu-id="84162-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="84162-612">Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="84162-613">Selecteer in het actievenster de optie **Query bewerken** om het dialoogvenster Query-editor te openen voor de hele labelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="84162-614">Voeg in het dialoogvenster Query-editor op het tabblad **Sortering** een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="84162-615">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-616">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-617">**Veld:** *Verwijzing ladingsregel-id (record-id)*</span><span class="sxs-lookup"><span data-stu-id="84162-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="84162-618">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="84162-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="84162-619">Voeg een tweede rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="84162-620">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-621">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="84162-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="84162-622">**Veld:** *Zending-id*</span><span class="sxs-lookup"><span data-stu-id="84162-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="84162-623">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="84162-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="84162-624">Selecteer **OK** om het dialoogvenster Query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="84162-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="84162-625">U wordt gevraagd om de bewerking voor het opnieuw instellen van de groepering te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="84162-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="84162-626">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="84162-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="84162-627">Selecteer in het actievenster **Sjabloongroep voor wavelabel**.</span><span class="sxs-lookup"><span data-stu-id="84162-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="84162-628">Stel in het dialoogvenster **Sjabloongroep voor wavelabel** de volgende waarden in voor de rij waarin het veld **Naam verwijzingsveld** is ingesteld op *Zending-id*:</span><span class="sxs-lookup"><span data-stu-id="84162-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="84162-629">**Onderbrekingslabel afdrukken:** schakel dit selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="84162-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="84162-630">**Labelindelings-id:** selecteer een onderbrekingslabel.</span><span class="sxs-lookup"><span data-stu-id="84162-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="84162-631">(Selecteer bijvoorbeeld de indeling *Onderbrekingslabel* die u eerder in dit scenario hebt gemaakt.)</span><span class="sxs-lookup"><span data-stu-id="84162-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="84162-632">**Printernaam:** selecteer de printer voor het onderbrekingslabel.</span><span class="sxs-lookup"><span data-stu-id="84162-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="84162-633">(Gewoonlijk moet u voor het splitsen van labelrollen dezelfde printer selecteren die is geselecteerd op het Het sneltabblad **Sjabloondetails van wavelabel**.</span><span class="sxs-lookup"><span data-stu-id="84162-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="84162-634">Er zijn echter andere scenario's mogelijk.)</span><span class="sxs-lookup"><span data-stu-id="84162-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="84162-635">Schakel het selectievakje **Labelbuild-id** in voor de rij waarin het veld *Naam verwijzingsveld* is ingesteld op **Verwijzing ladingsregel-id**.</span><span class="sxs-lookup"><span data-stu-id="84162-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84162-636">Met deze instelling wordt één labelreeks ("doos 1 van X") per ladingsregel gemaakt in de hele wave, ongeacht de instelling van de werkgroepering.</span><span class="sxs-lookup"><span data-stu-id="84162-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="84162-637">Deze labelreeks kan worden afgedrukt op een labelindeling.</span><span class="sxs-lookup"><span data-stu-id="84162-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="84162-638">Bovendien worden labels voor verschillende zendingen gescheiden door het geselecteerde onderbrekingslabel.</span><span class="sxs-lookup"><span data-stu-id="84162-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="84162-639">Nummerreeksuitbreidingen configureren</span><span class="sxs-lookup"><span data-stu-id="84162-639">Configure number sequence extensions</span></span>

<span data-ttu-id="84162-640">Nummerreeksuitbreidingen bepalen de GS1-naleving van specifieke nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="84162-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="84162-641">Deze configuratie is optioneel voor het huidige scenario.</span><span class="sxs-lookup"><span data-stu-id="84162-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="84162-642">Zie [Nummerreeksuitbreidingen configureren](../warehousing/configure-number-sequence-extensions.md) voor meer informatie en configuratie-instructies.</span><span class="sxs-lookup"><span data-stu-id="84162-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="84162-643">Een verkooporder maken en vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="84162-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="84162-644">Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="84162-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="84162-645">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="84162-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="84162-646">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="84162-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="84162-647">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="84162-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="84162-648">Twee verkooporderregels toevoegen:</span><span class="sxs-lookup"><span data-stu-id="84162-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="84162-649">Verkooporderregel 1:</span><span class="sxs-lookup"><span data-stu-id="84162-649">Sales order line 1:</span></span>

        - <span data-ttu-id="84162-650">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="84162-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="84162-651">**Hoeveelheid:** *9024*</span><span class="sxs-lookup"><span data-stu-id="84162-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="84162-652">**Eenheid:** *ea* (9024 ea = 376 dozen = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="84162-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="84162-653">Verkooporderregel 2:</span><span class="sxs-lookup"><span data-stu-id="84162-653">Sales order line 2:</span></span>

        - <span data-ttu-id="84162-654">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="84162-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="84162-655">**Hoeveelheid:** *9016*</span><span class="sxs-lookup"><span data-stu-id="84162-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="84162-656">**Eenheid:** *ea* (9016 ea = 322 dozen = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="84162-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="84162-657">De artikelen en hoeveelheden die hier worden vermeld, dienen alleen als voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="84162-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="84162-658">Ze moeten de volgordegroep van de eenheid gebruiken die u eerder hebt gedefinieerd. Er moeten correcte eenheidsomrekeningen van *ea* naar *doos* naar *PL* zijn gedefinieerd en ze moeten op voorraad zijn in magazijn *62*.</span><span class="sxs-lookup"><span data-stu-id="84162-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="84162-659">Zie [Maateenheid en voorraadbeleid](unit-measure-stocking-policies.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="84162-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="84162-660">Selecteer verkooporderregel 1.</span><span class="sxs-lookup"><span data-stu-id="84162-660">Select sales order line 1.</span></span> <span data-ttu-id="84162-661">Selecteer in de sectie **Verkooporderregel** in het menu **Voorraad** de optie **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="84162-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="84162-662">Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren** en sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="84162-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="84162-663">Herhaal stap 4 en 5 voor verkooporderregel 2.</span><span class="sxs-lookup"><span data-stu-id="84162-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="84162-664">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="84162-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="84162-665">De volgende gebeurtenissen vinden plaats:</span><span class="sxs-lookup"><span data-stu-id="84162-665">The following events occur:</span></span> 

    - <span data-ttu-id="84162-666">Het systeem verwerkt de gemaakte zending met behulp van de sjabloon die de stap voor het afdrukken van labels bevat.</span><span class="sxs-lookup"><span data-stu-id="84162-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="84162-667">De labelindeling wordt gebruikt om de indeling van het label te definiëren en het resultaat is een label dat wordt afgedrukt op de printer die is geselecteerd in de labelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="84162-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="84162-668">Er worden wavelabels gegenereerd en afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="84162-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="84162-669">Het aantal labels komt overeen met het aantal dozen (in dit voorbeeld 376 labels voor regel 1, 322 labels voor regel 2, 47 PL-labels voor regel 1, 47 PL-labels voor regel 2 en twee onderbrekingslabels met de zending-id).</span><span class="sxs-lookup"><span data-stu-id="84162-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="84162-670">Er wordt een nieuwe vrachtbrief-id gegenereerd voor de zendingen.</span><span class="sxs-lookup"><span data-stu-id="84162-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="84162-671">Als u de nummerreeksuitbreidingen hebt geconfigureerd, volgen de wavelabel-id's de nummernotatie **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="84162-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="84162-672">U kunt wavelabels weergeven en opnieuw afdrukken op de volgende pagina's:</span><span class="sxs-lookup"><span data-stu-id="84162-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="84162-673">Alle zendingen \> Details van zending</span><span class="sxs-lookup"><span data-stu-id="84162-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="84162-674">Alle ladingen \> Details van lading</span><span class="sxs-lookup"><span data-stu-id="84162-674">All loads \> Load details</span></span>
- <span data-ttu-id="84162-675">Alle waves</span><span class="sxs-lookup"><span data-stu-id="84162-675">All waves</span></span>
- <span data-ttu-id="84162-676">Wavelabels</span><span class="sxs-lookup"><span data-stu-id="84162-676">Wave labels</span></span>
- <span data-ttu-id="84162-677">Historie wavelabel</span><span class="sxs-lookup"><span data-stu-id="84162-677">Wave label history</span></span>

<span data-ttu-id="84162-678">Voor de meeste van deze pagina's kunt u de relevante functie vinden door **Wavelabels** te selecteren in de groep **Verwante informatie** op het tabblad **Zendingen** van het actievenster.</span><span class="sxs-lookup"><span data-stu-id="84162-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>

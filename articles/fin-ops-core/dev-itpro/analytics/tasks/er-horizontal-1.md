---
title: 'ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 1: Indeling ontwerpen)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b616998738d6b6986f157d136fc56e061900ef41
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550527"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a><span data-ttu-id="eefc1-103">ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 1: Indeling ontwerpen)</span><span class="sxs-lookup"><span data-stu-id="eefc1-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1 - Design format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eefc1-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.</span><span class="sxs-lookup"><span data-stu-id="eefc1-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="eefc1-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="eefc1-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="eefc1-106">Voordat u deze stappen uitvoert, moet u eerst deze taakbegeleidingen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="eefc1-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="eefc1-107">'ER Een configuratieprovider maken en deze als actief markeren'</span><span class="sxs-lookup"><span data-stu-id="eefc1-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="eefc1-108">'ER Financiële dimensies gebruiken als gegevensbron (Deel 1: gegevensmodel ontwerpen)'</span><span class="sxs-lookup"><span data-stu-id="eefc1-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="eefc1-109">'ER Financiële dimensies gebruiken als gegevensbron (Deel 2: modeltoewijzing)'</span><span class="sxs-lookup"><span data-stu-id="eefc1-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="eefc1-110">U moet ook een lokale kopie van de sjabloon met een hier gevonden voorbeeldrapport downloaden en opslaan: [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="eefc1-110">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="eefc1-111">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="eefc1-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="eefc1-112">Een nieuwe rapportconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="eefc1-112">Create a new report configuration</span></span>
1. <span data-ttu-id="eefc1-113">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="eefc1-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="eefc1-114">Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="eefc1-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="eefc1-115">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="eefc1-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="eefc1-116">Typ in het veld Nieuw veld 'Indeling gebaseerd op gegevensmodel Voorbeeldmodel Financiële dimensies'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="eefc1-117">Gebruik het model dat vooraf als gegevensbron voor het nieuwe rapport is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eefc1-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="eefc1-118">Typ in het veld Naam Voorbeeldrapport met horizontaal uitvouwbare bereiken.</span><span class="sxs-lookup"><span data-stu-id="eefc1-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="eefc1-119">Voorbeeldrapport met horizontaal uitvouwbare bereiken</span><span class="sxs-lookup"><span data-stu-id="eefc1-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="eefc1-120">Typ in het veld Omschrijving Excel-uitvoer maken door dynamisch toevoegen van kolommen.</span><span class="sxs-lookup"><span data-stu-id="eefc1-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="eefc1-121">Excel-uitvoer maken door dynamisch toevoegen van kolommen</span><span class="sxs-lookup"><span data-stu-id="eefc1-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="eefc1-122">Selecteer Invoer in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="eefc1-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="eefc1-123">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="eefc1-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="eefc1-124">De rapportindeling ontwerpen</span><span class="sxs-lookup"><span data-stu-id="eefc1-124">Design the report format</span></span>
1. <span data-ttu-id="eefc1-125">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="eefc1-125">Click Designer.</span></span>
2. <span data-ttu-id="eefc1-126">Schakel de wisselknop Details weergeven in.</span><span class="sxs-lookup"><span data-stu-id="eefc1-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="eefc1-127">Klik in het actievenster op Importeren.</span><span class="sxs-lookup"><span data-stu-id="eefc1-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="eefc1-128">Klik op Importeren uit Excel.</span><span class="sxs-lookup"><span data-stu-id="eefc1-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="eefc1-129">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="eefc1-129">Click Attachments.</span></span>
    * <span data-ttu-id="eefc1-130">Importeer de sjabloon van het rapport.</span><span class="sxs-lookup"><span data-stu-id="eefc1-130">Import the report’s template.</span></span> <span data-ttu-id="eefc1-131">Gebruik het Excel-bestand dat u daarvoor hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="eefc1-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="eefc1-132">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="eefc1-132">Click New.</span></span>
7. <span data-ttu-id="eefc1-133">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="eefc1-133">Click File.</span></span>
8. <span data-ttu-id="eefc1-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eefc1-134">Close the page.</span></span>
9. <span data-ttu-id="eefc1-135">Typ of selecteer een waarde in het veld Sjabloon.</span><span class="sxs-lookup"><span data-stu-id="eefc1-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="eefc1-136">Selecteer de gedownloade sjabloon.</span><span class="sxs-lookup"><span data-stu-id="eefc1-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="eefc1-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eefc1-137">Click OK.</span></span>
    * <span data-ttu-id="eefc1-138">Voeg een nieuwe reeks toe om dynamisch Excel-uitvoer te maken met net zoveel kolommen als u (in het formulier van het gebruikersdialoogvenster) voor financiële dimensies hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="eefc1-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="eefc1-139">Elke cel voor elke kolom geeft één naam van de financiële dimensie weer.</span><span class="sxs-lookup"><span data-stu-id="eefc1-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="eefc1-140">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="eefc1-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="eefc1-141">Selecteer Excel-bereik in de structuur.</span><span class="sxs-lookup"><span data-stu-id="eefc1-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="eefc1-142">Typ in het veld Excel-bereik DimNames.</span><span class="sxs-lookup"><span data-stu-id="eefc1-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="eefc1-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="eefc1-143">DimNames</span></span>  
14. <span data-ttu-id="eefc1-144">Selecteer Horizontaal in het veld Replicatierichting.</span><span class="sxs-lookup"><span data-stu-id="eefc1-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="eefc1-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eefc1-145">Click OK.</span></span>
16. <span data-ttu-id="eefc1-146">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="eefc1-147">Klik op Omhoog.</span><span class="sxs-lookup"><span data-stu-id="eefc1-147">Click Move up.</span></span>
18. <span data-ttu-id="eefc1-148">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="eefc1-149">Klik op Knippen.</span><span class="sxs-lookup"><span data-stu-id="eefc1-149">Click Cut.</span></span>
20. <span data-ttu-id="eefc1-150">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="eefc1-151">Klik op Plakken.</span><span class="sxs-lookup"><span data-stu-id="eefc1-151">Click Paste.</span></span>
22. <span data-ttu-id="eefc1-152">Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="eefc1-153">Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical' uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="eefc1-154">Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>Vertical\Range<TransactionLine>: Vertical' uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="eefc1-155">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>Vertical\Range<TransactionLine>: Vertical'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="eefc1-156">Voeg een nieuwe reeks toe om dynamisch Excel-uitvoer te maken met net zoveel kolommen als u (in het formulier van het gebruikersdialoogvenster) voor financiële dimensies hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="eefc1-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="eefc1-157">Elke cel voor elke kolom geeft één waarde van de financiële dimensie weer voor elke aangiftetransactie.</span><span class="sxs-lookup"><span data-stu-id="eefc1-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="eefc1-158">Klik op Bereik toevoegen.</span><span class="sxs-lookup"><span data-stu-id="eefc1-158">Click Add Range.</span></span>
27. <span data-ttu-id="eefc1-159">Typ in het veld Excel-bereik DimValues.</span><span class="sxs-lookup"><span data-stu-id="eefc1-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="eefc1-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="eefc1-160">DimValues</span></span>  
28. <span data-ttu-id="eefc1-161">Selecteer Horizontaal in het veld Replicatierichting.</span><span class="sxs-lookup"><span data-stu-id="eefc1-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="eefc1-162">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eefc1-162">Click OK.</span></span>
30. <span data-ttu-id="eefc1-163">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="eefc1-164">Klik op Knippen.</span><span class="sxs-lookup"><span data-stu-id="eefc1-164">Click Cut.</span></span>
32. <span data-ttu-id="eefc1-165">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="eefc1-166">Klik op Plakken.</span><span class="sxs-lookup"><span data-stu-id="eefc1-166">Click Paste.</span></span>
34. <span data-ttu-id="eefc1-167">Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="eefc1-168">Indelingselementen aan gegevensbronnen toewijzen</span><span class="sxs-lookup"><span data-stu-id="eefc1-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="eefc1-169">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="eefc1-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="eefc1-170">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="eefc1-171">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="eefc1-172">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="eefc1-173">Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="eefc1-174">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="eefc1-175">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Code: tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="eefc1-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="eefc1-176">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-176">Click Bind.</span></span>
9. <span data-ttu-id="eefc1-177">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="eefc1-178">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="eefc1-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="eefc1-179">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-179">Click Bind.</span></span>
12. <span data-ttu-id="eefc1-180">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="eefc1-181">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Credit: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="eefc1-182">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-182">Click Bind.</span></span>
15. <span data-ttu-id="eefc1-183">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="eefc1-184">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Debet: werkelijk" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="eefc1-185">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-185">Click Bind.</span></span>
18. <span data-ttu-id="eefc1-186">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="eefc1-187">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Valuta: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="eefc1-188">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-188">Click Bind.</span></span>
21. <span data-ttu-id="eefc1-189">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="eefc1-190">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Datum: Datum".</span><span class="sxs-lookup"><span data-stu-id="eefc1-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="eefc1-191">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-191">Click Bind.</span></span>
24. <span data-ttu-id="eefc1-192">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="eefc1-193">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Boekstuk: tekenreeks" uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="eefc1-194">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-194">Click Bind.</span></span>
27. <span data-ttu-id="eefc1-195">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="eefc1-196">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="eefc1-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="eefc1-197">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-197">Click Bind.</span></span>
30. <span data-ttu-id="eefc1-198">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>Vertical\Range<TransactionLine>: Vertical'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="eefc1-199">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="eefc1-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="eefc1-200">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-200">Click Bind.</span></span>
33. <span data-ttu-id="eefc1-201">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="eefc1-202">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="eefc1-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="eefc1-203">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-203">Click Bind.</span></span>
36. <span data-ttu-id="eefc1-204">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="eefc1-205">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst".</span><span class="sxs-lookup"><span data-stu-id="eefc1-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="eefc1-206">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-206">Click Bind.</span></span>
39. <span data-ttu-id="eefc1-207">Vouw in de structuur 'model: Gegevensmodel Voorbeeldmodel Financiële dimensies\Instelling Dimensies: Recordlijst' uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="eefc1-208">Selecteer in de structuur 'model: Gegevensmodel Voorbeeldmodel Financiële dimensies\Instelling Dimensies: Recordlijst\Code: Tekenreeks' uit.</span><span class="sxs-lookup"><span data-stu-id="eefc1-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="eefc1-209">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="eefc1-210">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-210">Click Bind.</span></span>
43. <span data-ttu-id="eefc1-211">Selecteer in de structuur 'model: Gegevensmodel Voorbeeldmodel Financiële dimensies\Instelling Dimensies: Recordlijst'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="eefc1-212">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="eefc1-213">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-213">Click Bind.</span></span>
46. <span data-ttu-id="eefc1-214">Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span><span class="sxs-lookup"><span data-stu-id="eefc1-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="eefc1-215">Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Bedrijf: Tekenreeks".</span><span class="sxs-lookup"><span data-stu-id="eefc1-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="eefc1-216">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="eefc1-216">Click Bind.</span></span>
49. <span data-ttu-id="eefc1-217">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="eefc1-217">Click Save.</span></span>
50. <span data-ttu-id="eefc1-218">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eefc1-218">Close the page.</span></span>

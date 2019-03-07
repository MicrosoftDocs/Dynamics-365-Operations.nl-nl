---
title: Modeltoewijzingsconfiguraties gebruiken voor samengevoegde berekeningen op databaseniveau gebruiken
description: Deze procedure bevat informatie voor het ontwerpen van een nieuwe ER-modeltoewijzingsconfiguratie (elektronische aangifte) en past de ingebouwde ER-functies toe voor efficiënte statistische berekeningen.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a462a3997644a494b5cea89c9530ddba67c32450
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "313630"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="b6d2f-103">Modeltoewijzingsconfiguraties gebruiken voor samengevoegde berekeningen op databaseniveau gebruiken</span><span class="sxs-lookup"><span data-stu-id="b6d2f-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6d2f-104">Deze procedure bevat informatie voor het ontwerpen van een nieuwe ER-modeltoewijzingsconfiguratie (elektronische aangifte) en past de ingebouwde ER-functies toe voor efficiënte statistische berekeningen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="b6d2f-105">In deze procedure maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="b6d2f-106">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="b6d2f-107">Deze stappen kunnen worden voltooid met elke dataset.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="b6d2f-108">Voordat u deze stappen uitvoert, voert u eerst de stappen uit in de procedure “ER verbetert de efficiency van aggregatieberekeningen door ze uit te voeren op databaseniveau (Deel 1: Configuraties voorbereiden).”</span><span class="sxs-lookup"><span data-stu-id="b6d2f-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="b6d2f-109">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b6d2f-110">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="b6d2f-111">Selecteer in de structuur 'Intrastat-model\Intrastat-voorbeeldtoewijzing'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="b6d2f-112">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-112">Click Designer.</span></span>
5. <span data-ttu-id="b6d2f-113">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-113">Click Designer.</span></span>
6. <span data-ttu-id="b6d2f-114">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="b6d2f-115">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-115">Click Add root.</span></span>
    * <span data-ttu-id="b6d2f-116">Voeg een nieuwe gegevensbron toe die de records weergeeft die u wilt groeperen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="b6d2f-117">Typ "Transacties" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="b6d2f-118">Transacties</span><span class="sxs-lookup"><span data-stu-id="b6d2f-118">Transactions</span></span>  
9. <span data-ttu-id="b6d2f-119">Typ 'Intrastat' in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="b6d2f-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="b6d2f-120">Intrastat</span></span>  
10. <span data-ttu-id="b6d2f-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-121">Click OK.</span></span>
11. <span data-ttu-id="b6d2f-122">Selecteer in de structuur Functies\Groeperen op.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="b6d2f-123">Dit gegevensbrontype wordt gebruikt om in runtime een nieuwe gegevensbron te introduceren voor het groeperen van records en het berekenen van de vereiste aggregaties.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="b6d2f-124">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-124">Click Add root.</span></span>
13. <span data-ttu-id="b6d2f-125">Typ 'TransactionsGroups' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="b6d2f-126">Transactiegroepen</span><span class="sxs-lookup"><span data-stu-id="b6d2f-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="b6d2f-127">Klik op Groeperen op bewerken</span><span class="sxs-lookup"><span data-stu-id="b6d2f-127">Click Edit group by.</span></span>
15. <span data-ttu-id="b6d2f-128">Selecteer "Transactions" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="b6d2f-129">Selecteer de toegevoegde gegevensbron van het type ‘Recordlijst’ die de records aangeeft die u wilt groeperen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="b6d2f-130">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-130">Click Add field to.</span></span>
17. <span data-ttu-id="b6d2f-131">Klik op Wat groeperen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-131">Click What to group.</span></span>
18. <span data-ttu-id="b6d2f-132">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="b6d2f-133">Selecteer in de structuur 'Transacties\Richting'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="b6d2f-134">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-134">Click Add field to.</span></span>
21. <span data-ttu-id="b6d2f-135">Klik op Gegroepeerde velden.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="b6d2f-136">Selecteer het veld om het groeperingsniveau op te geven.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="b6d2f-137">Op basis van deze selectie stuurt de gegevensbron tijdens runtime zoveel transactiegroepen terug als er richtingcodes zijn waaraan wordt voldaan in de Intrastat-tabel.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="b6d2f-138">Selecteer in de structuur 'Transacties\Factuurbedrag(AmountMST)'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="b6d2f-139">Selecteer het veld om de bron voor de aggregatieberekening op te geven.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="b6d2f-140">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-140">Click Add field to.</span></span>
24. <span data-ttu-id="b6d2f-141">Klik op Aggregatievelden.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="b6d2f-142">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="b6d2f-143">Selecteer 'Totaal' in het veld Methode.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="b6d2f-144">Selecteer het aggregatietype.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="b6d2f-145">Typ 'SumOfAmountMST' in het veld Naam</span><span class="sxs-lookup"><span data-stu-id="b6d2f-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="b6d2f-146">Geef de naam op van deze aggregatie in de geconfigureerde gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="b6d2f-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-147">Click Save.</span></span>
    * <span data-ttu-id="b6d2f-148">Houd er rekening mee dat het veld 'Uitvoering in' aangeeft dat deze groepering in runtime wordt uitgevoerd in de SQL-database.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="b6d2f-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-149">Close the page.</span></span>
30. <span data-ttu-id="b6d2f-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-150">Click OK.</span></span>
31. <span data-ttu-id="b6d2f-151">Vouw in de structuur 'Totalen' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="b6d2f-152">Vouw in de structuur 'TransactionsGroups' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="b6d2f-153">Vouw in de structuur 'TransactionsGroups\aggregated' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="b6d2f-154">Selecteer in de structuur 'TransactionsGroups\aggregated\SumOfAmountMST'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="b6d2f-155">Selecteer in de structuur 'Totalen\Totale factuurwaarde(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="b6d2f-156">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-156">Click Bind.</span></span>
    * <span data-ttu-id="b6d2f-157">Op basis van deze instelling berekent deze gegevensbron de som van de waarden van het veld 'AmountMST' voor elke transactiegroep.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="b6d2f-158">Deze aggregatieberekening is beschikbaar als het item TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="b6d2f-159">Vouw in de structuur 'TransactionsGroups' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="b6d2f-160">Selecteer in de structuur 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="b6d2f-161">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-161">Click Edit.</span></span>
40. <span data-ttu-id="b6d2f-162">Klik op Groeperen op bewerken</span><span class="sxs-lookup"><span data-stu-id="b6d2f-162">Click Edit group by.</span></span>
41. <span data-ttu-id="b6d2f-163">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="b6d2f-164">Selecteer in de structuur 'Transacties\Factuurbedrag(AmountMST)'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="b6d2f-165">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-165">Click Add field to.</span></span>
44. <span data-ttu-id="b6d2f-166">Klik op Aggregatievelden.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="b6d2f-167">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="b6d2f-168">Selecteer 'Max' in het veld Methode.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="b6d2f-169">Typ in het veld Naam 'MaxOfAmountMST'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="b6d2f-170">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-170">Click Save.</span></span>
    * <span data-ttu-id="b6d2f-171">De uitvoering van de GROUPBY-gegevensbronnen kan dan met een aantal beperkingen worden vertaald naar het niveau van de SQL-database.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="b6d2f-172">Vertaling is mogelijk voor gegevensbronnen van het type 'Recordlijst' of voor gegevensbronnen die als een expressie worden weergegeven met de FILTER-functie.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="b6d2f-173">Dit kan ook worden uitgevoerd wanneer slechts één aggregatie wordt geconfigureerd voor één veld met groeperingsrecords.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="b6d2f-174">Houd er rekening mee dat hoewel er meer dan één aggregatie is geconfigureerd voor het veld AmountMST, het veld 'Uitvoering in' nog steeds aangeeft dat deze groepering in runtime wordt uitgevoerd in de SQL-database.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="b6d2f-175">Dit komt doordat slechts één aggregatie is gekoppeld aan het gegevensmodelitem en dat deze wordt gebruikt om in runtime gegevens op te halen uit deze gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="b6d2f-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-176">Close the page.</span></span>
50. <span data-ttu-id="b6d2f-177">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-177">Click OK.</span></span>
51. <span data-ttu-id="b6d2f-178">Vouw in de structuur 'TransactionsGroups' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="b6d2f-179">Vouw in de structuur 'TransactionsGroups\aggregated' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="b6d2f-180">Selecteer in de structuur 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="b6d2f-181">Selecteer in de structuur 'Totalen\Totale statistische waarde(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="b6d2f-182">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-182">Click Bind.</span></span>
56. <span data-ttu-id="b6d2f-183">Vouw in de structuur 'TransactionsGroups' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="b6d2f-184">Selecteer in de structuur 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="b6d2f-185">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-185">Click Edit.</span></span>
59. <span data-ttu-id="b6d2f-186">Klik op Groeperen op bewerken</span><span class="sxs-lookup"><span data-stu-id="b6d2f-186">Click Edit group by.</span></span>
    * <span data-ttu-id="b6d2f-187">Houd er rekening mee dat het veld 'Uitvoering in' aangeeft dat deze groepering in runtime in het geheugen wordt uitgevoerd omdat beide aggregaties van hetzelfde veld zijn gekoppeld aan de gegevensmodelitems.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="b6d2f-188">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="b6d2f-189">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-189">Click Delete.</span></span>
62. <span data-ttu-id="b6d2f-190">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-190">Click Yes.</span></span>
63. <span data-ttu-id="b6d2f-191">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-191">Click Delete.</span></span>
64. <span data-ttu-id="b6d2f-192">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-192">Click Yes.</span></span>
65. <span data-ttu-id="b6d2f-193">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-193">Click Add field to.</span></span>
66. <span data-ttu-id="b6d2f-194">Klik op Wat groeperen.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-194">Click What to group.</span></span>
67. <span data-ttu-id="b6d2f-195">Vouw in de structuur 'Basisproductrecord(Intrastat)' uit.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="b6d2f-196">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-196">Click Save.</span></span>
    * <span data-ttu-id="b6d2f-197">Het veld 'Uitvoering in' geeft aan dat deze groepering in runtime in het geheugen wordt uitgevoerd, hoewel er geen aggregaties zijn gedefinieerd en de geselecteerde gegevensbron van het type 'Tabelrecords' naar dezelfde Intrastat-tabel verwijst.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="b6d2f-198">Dit komt doordat de gegevensbron een aantal berekende velden bevat die nog niet kunnen worden omgezet naar het niveau van de SQL-database.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  


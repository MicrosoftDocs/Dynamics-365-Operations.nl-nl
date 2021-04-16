---
title: Een sjabloon voor vrije-tekstfacturen maken
description: In deze procedure wordt beschreven hoe u een sjabloon voor een terugkerende vrije-tekstfactuur maakt.
author: ShivamPandey-msft
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79f969d0e63458b5327950cfed98e0f3ba2cd7ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816311"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="14a22-103">Een sjabloon voor vrije-tekstfacturen maken</span><span class="sxs-lookup"><span data-stu-id="14a22-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14a22-104">Gebruik voor deze procedure het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="14a22-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="14a22-105">Deze procedure is bedoeld voor de gebruiker die verantwoordelijk is voor het beheren en verwerken van klantenfacturen.</span><span class="sxs-lookup"><span data-stu-id="14a22-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="14a22-106">Een sjabloon maken</span><span class="sxs-lookup"><span data-stu-id="14a22-106">Create a template</span></span>

1. <span data-ttu-id="14a22-107">Ga naar Klanten > Facturen > Terugkerende facturen > Vrije-tekstfactuursjablonen.</span><span class="sxs-lookup"><span data-stu-id="14a22-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="14a22-108">Met dit formulier kunt u sjablonen voor vrije-tekstfacturen maken met factuurregels, toeslagen, een boekhoudingsverdelingsjabloon en gegevens over grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="14a22-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="14a22-109">Klik op Nieuw om een nieuwe sjabloon voor een terugkerende vrije-tekstfactuur te maken.</span><span class="sxs-lookup"><span data-stu-id="14a22-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="14a22-110">Typ een waarde in het veld Sjabloonnaam.</span><span class="sxs-lookup"><span data-stu-id="14a22-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="14a22-111">"Sjabloonnaam" identificeert op unieke wijze een sjabloon voor vrije-tekstfacturen.</span><span class="sxs-lookup"><span data-stu-id="14a22-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="14a22-112">Twee sjablonen kunnen niet dezelfde "Sjabloonnaam" hebben.</span><span class="sxs-lookup"><span data-stu-id="14a22-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="14a22-113">Voer in het veld Beschrijving een omschrijving van de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="14a22-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="14a22-114">Vouw het tabblad Factuurregels uit.</span><span class="sxs-lookup"><span data-stu-id="14a22-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="14a22-115">Voer in het veld Beschrijving een omschrijving in voor de factuurregel.</span><span class="sxs-lookup"><span data-stu-id="14a22-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="14a22-116">Selecteer in het veld Hoofdrekening een opbrengstrekening.</span><span class="sxs-lookup"><span data-stu-id="14a22-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="14a22-117">U kunt de tegenrekening voor transacties van een klantkrediet voor het totaalbedrag van de factuur selecteren op de pagina Boekingsprofielen van klant.</span><span class="sxs-lookup"><span data-stu-id="14a22-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="14a22-118">Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="14a22-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="14a22-119">De btw-groep voor de huidige factuurregel. Dit is de standaard-btw-groep voor de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="14a22-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="14a22-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="14a22-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="14a22-121">Selecteer in het veld Btw-groep voor artikel de btw-groep voor artikel voor de huidige factuurregel.</span><span class="sxs-lookup"><span data-stu-id="14a22-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="14a22-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="14a22-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="14a22-123">Typ of bekijk in het veld Eenheidsprijs de prijs per eenheid voor factuurregel.</span><span class="sxs-lookup"><span data-stu-id="14a22-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="14a22-124">Dit bedrag wordt vermenigvuldigd met de waarde in het veld Hoeveelheid om het bedrag van de factuurregel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="14a22-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="14a22-125">Voeg een nieuwe regel toe aan een sjabloon voor een vrije-tekstfactuur.</span><span class="sxs-lookup"><span data-stu-id="14a22-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="14a22-126">Voer in het veld Beschrijving een omschrijving in voor de factuurregel.</span><span class="sxs-lookup"><span data-stu-id="14a22-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="14a22-127">Selecteer in het veld Hoofdrekening een opbrengstrekening.</span><span class="sxs-lookup"><span data-stu-id="14a22-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="14a22-128">U kunt de tegenrekening voor transacties van een klantkrediet voor het totaalbedrag van de factuur selecteren op de pagina Boekingsprofielen van klant.</span><span class="sxs-lookup"><span data-stu-id="14a22-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="14a22-129">Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="14a22-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="14a22-130">De btw-groep voor de huidige factuurregel. Dit is de standaard-btw-groep voor de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="14a22-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="14a22-131">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="14a22-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="14a22-132">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="14a22-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="14a22-133">De artikel-btw-groep voor de huidige factuurregel.</span><span class="sxs-lookup"><span data-stu-id="14a22-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="14a22-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="14a22-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="14a22-135">Het aantal eenheden voor de factuurregel invoeren of bekijken</span><span class="sxs-lookup"><span data-stu-id="14a22-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="14a22-136">Dit getal wordt vermenigvuldigd met de waarde in het veld Eenheidsprijs om het bedrag van de factuurregel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="14a22-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="14a22-137">De prijs per eenheid voor de factuurregel bekijken of invoeren.</span><span class="sxs-lookup"><span data-stu-id="14a22-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="14a22-138">Dit bedrag wordt vermenigvuldigd met de waarde in het veld Hoeveelheid om het bedrag van de factuurregel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="14a22-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="14a22-139">Bekijk en wijzig de boekhoudingsverdelingen voor een afzonderlijke regel en eventuele onderliggende regels.</span><span class="sxs-lookup"><span data-stu-id="14a22-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="14a22-140">Boekhoudingsverdelingen bepalen hoe een bedrag zal worden verwerkt, zoals hoe de omzet, btw of heffingen zal worden verwerkt op een factuur met vrije tekst.</span><span class="sxs-lookup"><span data-stu-id="14a22-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="14a22-141">Werk de boekhoudingsverdelingen voor de geselecteerde factuurregel bij.</span><span class="sxs-lookup"><span data-stu-id="14a22-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="14a22-142">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="14a22-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="14a22-143">Een vrije-tekstfactuur opslaan als een sjabloon</span><span class="sxs-lookup"><span data-stu-id="14a22-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="14a22-144">U kunt ook een bestaande vrije-tekstfactuur als een sjabloon opslaan.</span><span class="sxs-lookup"><span data-stu-id="14a22-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="14a22-145">Wanneer u Opslaan in sjabloon selecteert op het tabblad Factuur, moet u een naam en beschrijving voor de sjabloon opgeven.</span><span class="sxs-lookup"><span data-stu-id="14a22-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="14a22-146">Als er al een sjabloon met deze naam bestaat, wordt dit in een melding aangegeven.</span><span class="sxs-lookup"><span data-stu-id="14a22-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="14a22-147">U kunt nog steeds op OK klikken om deze sjabloon te vervangen.</span><span class="sxs-lookup"><span data-stu-id="14a22-147">You can still click on Ok to replace it.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
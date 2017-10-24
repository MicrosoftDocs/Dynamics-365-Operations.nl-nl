--- 
title: Een sjabloon voor vrije-tekstfacturen maken
description: Bij deze registratie wordt het demobedrijf USMF gebruikt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="497bd-103">Een sjabloon voor vrije-tekstfacturen maken</span><span class="sxs-lookup"><span data-stu-id="497bd-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="497bd-104">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="497bd-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="497bd-105">De opname is bedoeld voor de gebruiker die verantwoordelijk is voor het beheren en verwerken van klantenfacturen.</span><span class="sxs-lookup"><span data-stu-id="497bd-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="497bd-106">Ga naar Klanten > Facturen > Terugkerende facturen > Vrije-tekstfactuursjablonen.</span><span class="sxs-lookup"><span data-stu-id="497bd-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="497bd-107">Met dit formulier kunt u sjablonen voor vrije-tekstfacturen maken met factuurregels, toeslagen, een boekhoudingsverdelingsjabloon en gegevens over grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="497bd-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="497bd-108">Klik op Nieuw om een nieuwe sjabloon voor een terugkerende vrije-tekstfactuur te maken.</span><span class="sxs-lookup"><span data-stu-id="497bd-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="497bd-109">Typ een waarde in het veld Sjabloonnaam.</span><span class="sxs-lookup"><span data-stu-id="497bd-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="497bd-110">"Sjabloonnaam" identificeert op unieke wijze een sjabloon voor vrije-tekstfacturen.</span><span class="sxs-lookup"><span data-stu-id="497bd-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="497bd-111">Twee sjablonen kunnen niet dezelfde "Sjabloonnaam" hebben.</span><span class="sxs-lookup"><span data-stu-id="497bd-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="497bd-112">Voer in het veld Beschrijving een omschrijving van de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="497bd-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="497bd-113">Vouw het tabblad Factuurregels uit.</span><span class="sxs-lookup"><span data-stu-id="497bd-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="497bd-114">Voer in het veld Beschrijving een omschrijving in voor de factuurregel.</span><span class="sxs-lookup"><span data-stu-id="497bd-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="497bd-115">Selecteer in het veld Hoofdrekening een opbrengstrekening.</span><span class="sxs-lookup"><span data-stu-id="497bd-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="497bd-116">U kunt de tegenrekening voor transacties van een klantkrediet voor het totaalbedrag van de factuur selecteren op de pagina Boekingsprofielen van klant.</span><span class="sxs-lookup"><span data-stu-id="497bd-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="497bd-117">Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="497bd-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="497bd-118">De btw-groep voor de huidige factuurregel. Dit is de standaard-btw-groep voor de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="497bd-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="497bd-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="497bd-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="497bd-120">Selecteer in het veld Btw-groep voor artikel de btw-groep voor artikel voor de huidige factuurregel.</span><span class="sxs-lookup"><span data-stu-id="497bd-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="497bd-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="497bd-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="497bd-122">Typ of bekijk in het veld Eenheidsprijs de prijs per eenheid voor factuurregel.</span><span class="sxs-lookup"><span data-stu-id="497bd-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="497bd-123">Dit bedrag wordt vermenigvuldigd met de waarde in het veld Hoeveelheid om het bedrag van de factuurregel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="497bd-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="497bd-124">Voeg een nieuwe regel toe aan een sjabloon voor een vrije-tekstfactuur.</span><span class="sxs-lookup"><span data-stu-id="497bd-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="497bd-125">Voer in het veld Beschrijving een omschrijving in voor de factuurregel.</span><span class="sxs-lookup"><span data-stu-id="497bd-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="497bd-126">Selecteer in het veld Hoofdrekening een opbrengstrekening.</span><span class="sxs-lookup"><span data-stu-id="497bd-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="497bd-127">U kunt de tegenrekening voor transacties van een klantkrediet voor het totaalbedrag van de factuur selecteren op de pagina Boekingsprofielen van klant.</span><span class="sxs-lookup"><span data-stu-id="497bd-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="497bd-128">Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="497bd-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="497bd-129">De btw-groep voor de huidige factuurregel. Dit is de standaard-btw-groep voor de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="497bd-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="497bd-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="497bd-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="497bd-131">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="497bd-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="497bd-132">De artikel-btw-groep voor de huidige factuurregel.</span><span class="sxs-lookup"><span data-stu-id="497bd-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="497bd-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="497bd-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="497bd-134">Het aantal eenheden voor de factuurregel invoeren of bekijken</span><span class="sxs-lookup"><span data-stu-id="497bd-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="497bd-135">Dit getal wordt vermenigvuldigd met de waarde in het veld Eenheidsprijs om het bedrag van de factuurregel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="497bd-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="497bd-136">De prijs per eenheid voor de factuurregel bekijken of invoeren.</span><span class="sxs-lookup"><span data-stu-id="497bd-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="497bd-137">Dit bedrag wordt vermenigvuldigd met de waarde in het veld Hoeveelheid om het bedrag van de factuurregel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="497bd-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="497bd-138">Bekijk en wijzig de boekhoudingsverdelingen voor een afzonderlijke regel en eventuele onderliggende regels.</span><span class="sxs-lookup"><span data-stu-id="497bd-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="497bd-139">Boekhoudingsverdelingen bepalen hoe een bedrag zal worden verwerkt, zoals hoe de omzet, btw of heffingen zal worden verwerkt op een factuur met vrije tekst.</span><span class="sxs-lookup"><span data-stu-id="497bd-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="497bd-140">Werk de boekhoudingsverdelingen voor de geselecteerde factuurregel bij.</span><span class="sxs-lookup"><span data-stu-id="497bd-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="497bd-141">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="497bd-141">Click Close.</span></span>



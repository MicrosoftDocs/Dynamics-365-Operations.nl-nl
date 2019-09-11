---
title: Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep
description: In dit onderwerp wordt beschreven hoe u het facturenregister gebruikt om facturen te maken.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7d72c1d98100d1313109e8b5e55df02e2163174
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867697"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="a97df-103">Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep</span><span class="sxs-lookup"><span data-stu-id="a97df-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a97df-104">In dit onderwerp wordt beschreven hoe u het facturenregister gebruikt om facturen te maken.</span><span class="sxs-lookup"><span data-stu-id="a97df-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="a97df-105">Gebruik vervolgens de facturenpool om de factuur af te stemmen op een inkooporder en de onkosten te finaliseren op de pagina voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="a97df-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="a97df-106">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="a97df-106">Create a purchase order</span></span>
1. <span data-ttu-id="a97df-107">Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="a97df-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="a97df-108">Selecteer **Nieuw** om een inkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="a97df-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="a97df-109">Selecteer in het veld **Leverancierrekening** de vervolgkeuzelijst om een leverancier te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a97df-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="a97df-110">Selecteer bijvoorbeeld leverancier **1001**.</span><span class="sxs-lookup"><span data-stu-id="a97df-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="a97df-111">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a97df-111">Select **OK**.</span></span>
5. <span data-ttu-id="a97df-112">Selecteer in het veld **Artikelnummer** de het artikelnummer van de service in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="a97df-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="a97df-113">Selecteer bijvoorbeeld **S0001**.</span><span class="sxs-lookup"><span data-stu-id="a97df-113">For example, select **S0001**.</span></span> <span data-ttu-id="a97df-114">Het nettobedrag is 75,00.</span><span class="sxs-lookup"><span data-stu-id="a97df-114">The net amount is 75.00.</span></span>  <span data-ttu-id="a97df-115">Dat is het bedrag dat we verwachten op de factuur.</span><span class="sxs-lookup"><span data-stu-id="a97df-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="a97df-116">Selecteer in het actievenster de optie **Inkoop**.</span><span class="sxs-lookup"><span data-stu-id="a97df-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="a97df-117">Selecteer **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="a97df-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="a97df-118">Een factuur maken en boeken</span><span class="sxs-lookup"><span data-stu-id="a97df-118">Create and post and invoice</span></span>
1. <span data-ttu-id="a97df-119">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Facturenregister**.</span><span class="sxs-lookup"><span data-stu-id="a97df-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="a97df-120">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a97df-120">Select **New**.</span></span>
3. <span data-ttu-id="a97df-121">Open de zoekopdracht om de naam te selecteren van het facturenregister dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a97df-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="a97df-122">Selecteer de naam van het facturenregister dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a97df-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="a97df-123">Selecteer **Regels** om het register te openen en onkostenregels in te voeren.</span><span class="sxs-lookup"><span data-stu-id="a97df-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="a97df-124">Selecteer een leverancier in de zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="a97df-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="a97df-125">Selecteer bijvoorbeeld leverancier **1001**.</span><span class="sxs-lookup"><span data-stu-id="a97df-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="a97df-126">Voer in het veld **Factuur** het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="a97df-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="a97df-127">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="a97df-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="a97df-128">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="a97df-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="a97df-129">Open in het veld **Inkooporder** de vervolgkeuzelijst om de inkooporder te selecteren die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a97df-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="a97df-130">Markeer in het veld **Goedgekeurd door** een fiatteur in de vervolgkeuzelijst en klik op **Selecteren** om die fiatteur te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a97df-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="a97df-131">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="a97df-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="a97df-132">Open een factuur vanuit de pool en vereffen deze met een inkooporder om het factureringsproces te voltooien</span><span class="sxs-lookup"><span data-stu-id="a97df-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="a97df-133">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Facturenpool**.</span><span class="sxs-lookup"><span data-stu-id="a97df-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="a97df-134">Selecteer **Inkooporder** om een leveranciersfactuur te maken op basis van de factuur in de pool.</span><span class="sxs-lookup"><span data-stu-id="a97df-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="a97df-135">Selecteer de factuur die u wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="a97df-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="a97df-136">Selecteer **Vereffeningsstatus bijwerken** om de vereffening te voltooien.</span><span class="sxs-lookup"><span data-stu-id="a97df-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="a97df-137">Selecteer **Opties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a97df-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="a97df-138">Selecteer **Weergave wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="a97df-138">Select **Change view**.</span></span>
7. <span data-ttu-id="a97df-139">Selecteer **Rasterweergave**.</span><span class="sxs-lookup"><span data-stu-id="a97df-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="a97df-140">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="a97df-140">Select **Post**.</span></span>
9. <span data-ttu-id="a97df-141">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="a97df-141">Close the form.</span></span>
10. <span data-ttu-id="a97df-142">Ga in het navigatievenster naar **Modules > Leveranciers > Leveranciers > Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="a97df-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="a97df-143">Selecteer de leverancier die op de inkooporder staat vermeld.</span><span class="sxs-lookup"><span data-stu-id="a97df-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="a97df-144">Selecteer bijvoorbeeld leverancier **1001**.</span><span class="sxs-lookup"><span data-stu-id="a97df-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="a97df-145">Selecteer **Leverancier** in het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="a97df-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="a97df-146">Selecteer **Transacties**.</span><span class="sxs-lookup"><span data-stu-id="a97df-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="a97df-147">Selecteer de factuur die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a97df-147">Select the invoice that you created.</span></span> <span data-ttu-id="a97df-148">De toerekening van het facturenregister is omgekeerd en geboekt naar de juiste onkostenrekening.</span><span class="sxs-lookup"><span data-stu-id="a97df-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


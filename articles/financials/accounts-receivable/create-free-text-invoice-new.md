---
title: Vrije-tekstfacturen maken
description: In dit onderwerp wordt uitgelegd hoe u vrije-tekstfacturen maakt.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4498f5c9ce0e3830ffe1857c0363ca962561fc59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836767"
---
# <a name="create-free-text-invoices"></a><span data-ttu-id="0ddde-103">Vrije-tekstfacturen maken</span><span class="sxs-lookup"><span data-stu-id="0ddde-103">Create free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ddde-104">In dit onderwerp wordt uitgelegd hoe u vrije-tekstfacturen maakt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="0ddde-105">Gebruik voor de procedure het demobedrijf **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="0ddde-106">Een vrije-tekstfactuur invoeren</span><span class="sxs-lookup"><span data-stu-id="0ddde-106">Create a free text invoice</span></span>

1. <span data-ttu-id="0ddde-107">Ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="0ddde-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-108">Select **New**.</span></span>
3. <span data-ttu-id="0ddde-109">Selecteer een waarde in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="0ddde-110">De rekening die als de klantrekening wordt geselecteerd, wordt standaard als de factuurrekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="0ddde-111">De boekhoudstatus begint met **Onderhanden** als de factuur niet is geboekt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="0ddde-112">Het factuurnummer wordt toegewezen wanneer de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="0ddde-113">Als u SEPA-mandaten (Single Euro Payments Area) gebruikt, wordt het mandaat voor automatische afschrijving automatisch ingevoerd wanneer u de klantrekening selecteert.</span><span class="sxs-lookup"><span data-stu-id="0ddde-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="0ddde-114">Voer een waarde in het veld **Beschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="0ddde-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="0ddde-115">Geef in het veld **Hoofdrekening** een rekeningnummer op dat geen dimensies heeft.</span><span class="sxs-lookup"><span data-stu-id="0ddde-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="0ddde-116">Verderop in dit onderwerp gaat u dimensies invoeren.</span><span class="sxs-lookup"><span data-stu-id="0ddde-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="0ddde-117">U kunt ook een of meerdere tekens voor de hoofdrekening invoeren en de zoekopdracht gebruiken om uw rekening te zoeken.</span><span class="sxs-lookup"><span data-stu-id="0ddde-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="0ddde-118">Selecteer het sneltabblad **Regeldetails** om dimensies aan de hoofdrekening toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="0ddde-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="0ddde-119">Selecteer het tabblad **Financiële dimensieregel**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="0ddde-120">De dimensies gelden uitsluitend voor de geselecteerde regel.</span><span class="sxs-lookup"><span data-stu-id="0ddde-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="0ddde-121">De btw-groep wordt overgenomen van de klant.</span><span class="sxs-lookup"><span data-stu-id="0ddde-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="0ddde-122">Als de klant geen btw-groep heeft, wordt de btw-groep van de hoofdrekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="0ddde-123">De btw-groep van het artikel wordt overgenomen van de hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="0ddde-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="0ddde-124">Als de hoofdrekening geen btw-groep voor het artikel heeft, wordt de in de btw-parameters in het grootboek opgegeven btw-groep voor het artikel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="0ddde-125">Optioneel: voer in het veld **Hoeveelheid** een getal in.</span><span class="sxs-lookup"><span data-stu-id="0ddde-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="0ddde-126">Optioneel: voer een getal in het veld **Eenheidsprijs** in.</span><span class="sxs-lookup"><span data-stu-id="0ddde-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="0ddde-127">Het bedrag wordt berekend als de hoeveelheid keer de eenheidsprijs.</span><span class="sxs-lookup"><span data-stu-id="0ddde-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="0ddde-128">U kunt die berekening echter negeren door een bedrag in te voeren.</span><span class="sxs-lookup"><span data-stu-id="0ddde-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="0ddde-129">Selecteer **Btw** om de voor de factuur berekende btw te bekijken.</span><span class="sxs-lookup"><span data-stu-id="0ddde-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="0ddde-130">U kunt de btw-bedragen op deze pagina bekijken of u kunt de bedragen op het tabblad **Correctie** negeren.</span><span class="sxs-lookup"><span data-stu-id="0ddde-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="0ddde-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-131">Select **OK**.</span></span>
12. <span data-ttu-id="0ddde-132">Selecteer **Toeslagen** om een toeslag aan de factuur toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="0ddde-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="0ddde-133">Voer een waarde in het veld **Toeslagcode** in.</span><span class="sxs-lookup"><span data-stu-id="0ddde-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="0ddde-134">Voer een getal in het veld **Waarde van toeslagen** in.</span><span class="sxs-lookup"><span data-stu-id="0ddde-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="0ddde-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0ddde-135">Close the page.</span></span>
16. <span data-ttu-id="0ddde-136">Selecteer **Totalen** om een overzicht van de factuurdetails en -totalen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="0ddde-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="0ddde-137">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-137">Select **Close**.</span></span>
18. <span data-ttu-id="0ddde-138">Selecteer **Boeken** om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="0ddde-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="0ddde-139">U hebt nog altijd een mogelijkheid om te annuleren voordat u werkelijk boekt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="0ddde-140">U kunt de timing van het afdrukken van facturen wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0ddde-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="0ddde-141">Selecteer **Huidige** om elke factuur af te drukken wanneer deze wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="0ddde-142">Selecteer **Na** om af te drukken nadat alle facturen zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="0ddde-143">Als u wilt wijzigen hoe de kredietlimiet van de klant wordt gecontroleerd voordat de factuur wordt geboekt, wijzigt u de waarde in het veld **Kredietlimiettype**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="0ddde-144">Als u de factuur wilt afdrukken, stelt u de optie in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="0ddde-145">Als u de factuur wilt boeken, stelt u de optie in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="0ddde-146">U kunt de factuur afdrukken zonder deze te boeken.</span><span class="sxs-lookup"><span data-stu-id="0ddde-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="0ddde-147">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="0ddde-148">Regels kopiëren</span><span class="sxs-lookup"><span data-stu-id="0ddde-148">Copy lines</span></span>
<span data-ttu-id="0ddde-149">Als u regels in een vrije-tekstfactuur wilt kopiëren, selecteert u een of meer regels en selecteert u vervolgens **Geselecteerde regels kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="0ddde-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="0ddde-150">U kunt opgeven hoeveel kopieën u wilt maken en u kunt ook notities en bijlagen kopiëren.</span><span class="sxs-lookup"><span data-stu-id="0ddde-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="0ddde-151">U kunt de verdelingen kopiëren of opnieuw laten maken wanneer u boekt.</span><span class="sxs-lookup"><span data-stu-id="0ddde-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="0ddde-152">Nadat u de regels hebt gekopieerd, kunt u de gegevens zo nodig bewerken.</span><span class="sxs-lookup"><span data-stu-id="0ddde-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="0ddde-153">Een vrije-tekstfactuur maken op basis van een sjabloon</span><span class="sxs-lookup"><span data-stu-id="0ddde-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="0ddde-154">U kunt een vrije-tekstfactuur maken op basis van een sjabloon.</span><span class="sxs-lookup"><span data-stu-id="0ddde-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="0ddde-155">Wanneer u **Nieuw van sjabloon** op het tabblad **Factuur** selecteert, kunt u een sjabloonnaam en de klantrekening voor de nieuwe vrije-tekstfactuur selecteren.</span><span class="sxs-lookup"><span data-stu-id="0ddde-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="0ddde-156">Standaardwaarden, zoals de betalingsvoorwaarden en betalingsmethode, kunnen automatisch van de klant worden overgenomen, of u kunt de waarden gebruiken die zijn opgeslagen in de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="0ddde-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="0ddde-157">Er wordt een nieuwe vrije-tekstfactuur gemaakt en u kunt de waarden indien nodig bewerken.</span><span class="sxs-lookup"><span data-stu-id="0ddde-157">A new free text invoice is created, and you can edit the values as you require.</span></span>

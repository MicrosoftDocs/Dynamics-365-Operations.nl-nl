---
title: Belasting wordt niet berekend of het belastingbedrag is nul
description: Dit onderwerp biedt informatie die kan helpen bij het oplossen van problemen als het belastingbedrag 0 (nul) is of als de belasting niet wordt berekend.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020110"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="7eb66-103">Belasting wordt niet berekend of het belastingbedrag is nul</span><span class="sxs-lookup"><span data-stu-id="7eb66-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7eb66-104">Een transactie kan een regelbedrag hebben dat niet 0 (nul) is, maar de belasting wordt niet berekend of het berekende belastingbedrag is 0.</span><span class="sxs-lookup"><span data-stu-id="7eb66-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="7eb66-105">Volg de stappen in de volgende secties zoals vereist om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="7eb66-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="7eb66-106">Controleer of de juiste belastingcodes zijn geselecteerd door de transactie</span><span class="sxs-lookup"><span data-stu-id="7eb66-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="7eb66-107">Als de transactie niet de juiste belastingcodes selecteert of als er helemaal geen belastingcodes worden geselecteerd, wordt er geen belasting berekend.</span><span class="sxs-lookup"><span data-stu-id="7eb66-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="7eb66-108">Volg deze stappen om te controleren of de juiste belastingcodes worden geselecteerd door de transactie.</span><span class="sxs-lookup"><span data-stu-id="7eb66-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="7eb66-109">Controleer op de transactieregel, op het sneltabblad **Regeldetails**, op het tabblad **Instellingen**, in de sectie **Btw** of de juiste belastinggroepen zijn geselecteerd in de velden **Btw-groep artikel** en **Btw-groep**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="7eb66-110">Als de juiste belastinggroepen niet zijn geselecteerd, selecteer ze dan.</span><span class="sxs-lookup"><span data-stu-id="7eb66-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="7eb66-111">[![Velden Btw-groep artikel en Btw-groep](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="7eb66-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="7eb66-112">Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-groepen**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="7eb66-113">Selecteer de juiste btw-groep en maak vervolgens op het sneltabblad **Instellingen** een notitie van de belastingcode in het veld **Btw-code**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="7eb66-114">[![Pagina met Btw-groepen](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="7eb66-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="7eb66-115">Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-groepen artikel**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="7eb66-116">Selecteer de juiste btw-groep voor het artikel en controleer vervolgens op het sneltabblad **Instellingen** of de belastingcode in het veld **Btw-code** overeenkomt met de belastingcode van de btw-groep.</span><span class="sxs-lookup"><span data-stu-id="7eb66-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="7eb66-117">[![Pagina met Btw-groepen artikelen](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="7eb66-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="7eb66-118">Als de belastingcodes niet overeenkomen, moet u de btw-code voor een van de groepen bijwerken.</span><span class="sxs-lookup"><span data-stu-id="7eb66-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="7eb66-119">Controleer of de geselecteerde belastingcodes niet zijn vrijgesteld en of ze het juiste belastingtarief hebben</span><span class="sxs-lookup"><span data-stu-id="7eb66-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="7eb66-120">Als de belastingcodes zijn vrijgesteld of als het belastingtarief 0 (nul) is, is het resultaat van de belastingberekening 0.</span><span class="sxs-lookup"><span data-stu-id="7eb66-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="7eb66-121">Volg deze stappen om te bepalen of de geselecteerde belastingcodes zijn vrijgesteld en om te controleren of het juiste belastingtarief op deze codes wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="7eb66-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="7eb66-122">Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-groepen**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="7eb66-123">Selecteer de juiste btw-groep en controleer vervolgens op het sneltabblad **Instellingen** of het selectievakje **Vrijstelling** leeg is.</span><span class="sxs-lookup"><span data-stu-id="7eb66-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="7eb66-124">Als dit is geselecteerd, maakt u het leeg.</span><span class="sxs-lookup"><span data-stu-id="7eb66-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="7eb66-125">[![Selectievakje Vrijstelling op de pagina Btw-groepen](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="7eb66-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="7eb66-126">Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="7eb66-127">Selecteer de betreffende btw-code en controleer of het belastingtarief in het veld **Waarde** niet 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="7eb66-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="7eb66-128">Als het 0 is, moet u het veld bijwerken met het juiste belastingtarief.</span><span class="sxs-lookup"><span data-stu-id="7eb66-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="7eb66-129">[![Waarde veld op de pagina Waarden btw-codes](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="7eb66-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="7eb66-130">Bepaal of nul het juiste belastingbedrag is</span><span class="sxs-lookup"><span data-stu-id="7eb66-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="7eb66-131">In sommige gevallen is het juist als het belastingbedrag 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="7eb66-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="7eb66-132">Volg deze stappen om te bepalen of 0 het juiste belastingbedrag voor uw transactie is.</span><span class="sxs-lookup"><span data-stu-id="7eb66-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="7eb66-133">Ga naar **Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="7eb66-134">Controleer op het tabblad **Btw** in het veld **Berekeningsmethode** of **Totaal** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="7eb66-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="7eb66-135">[![Het veld Berekeningsmethode op de pagina Grootboekparameters](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="7eb66-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="7eb66-136">Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="7eb66-137">Selecteer de juiste btw-code, selecteer **Berekening** \> **Marginale basis** en controleer of de marginale basis is ingesteld op **Nettobedrag factuursaldo** of **Totaal factuur incl. andere btw-bedragen**.</span><span class="sxs-lookup"><span data-stu-id="7eb66-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="7eb66-138">Zie [Totaal factuur incl. andere btw-bedragen](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7eb66-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="7eb66-139">Als de juiste waarden zijn ingesteld in stap 2 en 4, bepaalt u of het totaalbedrag van de transactie 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="7eb66-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="7eb66-140">Als het totaalbedrag 0 is, is een belastingbedrag van 0 het verwachte resultaat.</span><span class="sxs-lookup"><span data-stu-id="7eb66-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="7eb66-141">Omdat de belastingberekening wordt gebaseerd op het totaalbedrag van het factuursaldo en niet op elke regel, wordt het belastingbedrag van 0 toegewezen aan elke regel na de belastingberekening.</span><span class="sxs-lookup"><span data-stu-id="7eb66-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="7eb66-142">Bekijk of er een aanpassing bestaat</span><span class="sxs-lookup"><span data-stu-id="7eb66-142">Determine whether customization exists</span></span>

<span data-ttu-id="7eb66-143">Als u de stappen in de vorige secties hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat.</span><span class="sxs-lookup"><span data-stu-id="7eb66-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="7eb66-144">Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="7eb66-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

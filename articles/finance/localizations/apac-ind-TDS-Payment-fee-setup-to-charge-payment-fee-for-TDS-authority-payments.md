---
title: Bijzondere betalingskosten instellen voor betalingen aan een TDS-dienst
description: In dit onderwerp wordt uitgelegd hoe u bijzondere betalingskosten moet instellen die worden berekend voor de belasting die wordt ingehouden op de bron (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023163"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="1c90e-103">Bijzondere betalingskosten instellen voor betalingen aan een TDS-dienst</span><span class="sxs-lookup"><span data-stu-id="1c90e-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c90e-104">In dit onderwerp wordt uitgelegd hoe u bijzondere betalingskosten moet instellen die worden berekend voor de belasting die wordt ingehouden op de bron (TDS).</span><span class="sxs-lookup"><span data-stu-id="1c90e-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="1c90e-105">Ga naar **Leveranciers \> Betalingsinstelling \> Bijzondere betalingskosten**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="1c90e-106">[![Pagina Bijzondere betalingskosten](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="1c90e-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="1c90e-107">Selecteer **Nieuw** om bijzondere betalingskosten te maken en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="1c90e-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="1c90e-108">Selecteer het type bijzondere betalingskosten in het veld **Type bijzondere kosten**:</span><span class="sxs-lookup"><span data-stu-id="1c90e-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="1c90e-109">**None**</span><span class="sxs-lookup"><span data-stu-id="1c90e-109">**None**</span></span>
    - <span data-ttu-id="1c90e-110">**Rente**: rente wordt in rekening gebracht over te late betalingen die zijn gedaan aan de TDS-dienstleverancier.</span><span class="sxs-lookup"><span data-stu-id="1c90e-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="1c90e-111">**Andere**: overige kosten worden in rekening gebracht over te late betalingen die zijn gedaan aan de TDS-dienstleverancier.</span><span class="sxs-lookup"><span data-stu-id="1c90e-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="1c90e-112">Als u **Rente** of **Andere** selecteert, wordt het veld **Toeslag** automatisch ingesteld op **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="1c90e-113">Als u **Rente** of **Andere** in het veld **Veldtype** hebt geselecteerd, selecteert u in het veld **Hoofdrekening** de grootboekrekening waar u de rente of andere toeslagen naar wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="1c90e-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="1c90e-114">Voer de andere vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="1c90e-114">Enter the other required details.</span></span>
6. <span data-ttu-id="1c90e-115">Selecteer in het actievenster **Instellingen van bijzondere betalingskosten** om de pagina **Instellingen van bijzondere betalingskosten** te openen, waar u bijzondere betalingskosten kunt instellen voor verschillende combinaties van banken, betalingsmethoden, betalingsspecificaties, valuta's en datumintervallen.</span><span class="sxs-lookup"><span data-stu-id="1c90e-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="1c90e-116">[![Pagina Instellingen van bijzondere betalingskosten](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="1c90e-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="1c90e-117">Geef op het tabblad **Overzicht** in het veld **Groeperingen** op voor welke banken u de bijzondere betalingskosten wilt instellen:</span><span class="sxs-lookup"><span data-stu-id="1c90e-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="1c90e-118">**Tabel**: de bijzondere betalingskosten gelden voor een specifieke bankrekening.</span><span class="sxs-lookup"><span data-stu-id="1c90e-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="1c90e-119">**Groep**: de betalingskosten gelden voor een specifieke bankgroep.</span><span class="sxs-lookup"><span data-stu-id="1c90e-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="1c90e-120">**Alle**: de bijzondere betalingskosten gelden voor alle bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="1c90e-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="1c90e-121">Als u **Tabel** of **Groep** hebt geselecteerd in het veld **Groeperingen**, selecteert u in het veld **Bankrelatie** de specifieke bankrekening of bankgroep waar u de bijzondere betalingskosten voor in wilt stellen.</span><span class="sxs-lookup"><span data-stu-id="1c90e-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="1c90e-122">In het veld **Betalingsmethode** selecteert u de betalingsmethode die u wilt gebruiken voor betaling van bijzondere betalingskosten.</span><span class="sxs-lookup"><span data-stu-id="1c90e-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="1c90e-123">Selecteer in het veld **Betalingsspecificatie** de betalingsspecificatiecode die is gegenereerd op de pagina **Betalingsspecificatie**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="1c90e-124">De betalingsspecificatie wordt gebruikt met de betalingsmethoden van EFT (Electronic Funds Transfer).</span><span class="sxs-lookup"><span data-stu-id="1c90e-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="1c90e-125">Selecteer in het veld **Betalingsvaluta** de valuta die de bijzondere betalingskosten activeert.</span><span class="sxs-lookup"><span data-stu-id="1c90e-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="1c90e-126">Alleen transacties die de geselecteerde valuta gebruiken, kunnen de bijzondere kosten activeren.</span><span class="sxs-lookup"><span data-stu-id="1c90e-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="1c90e-127">Als u dit veld leeg laat, worden de bijzondere kosten door alle valuta's geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="1c90e-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="1c90e-128">Selecteer de berekeningsmethode in het veld **Percentage/bedrag**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="1c90e-129">De opties zijn **Bedrag**, **Percentage** en **Interval**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="1c90e-130">Geef in het veld **Bedrag van bijzondere kosten** het bedrag van de bijzondere kosten op als een percentage van de betaling of als het bedrag voor één betaling.</span><span class="sxs-lookup"><span data-stu-id="1c90e-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="1c90e-131">Selecteer in het veld **Valuta van kosten** de valutacode voor de bijzondere kosten op.</span><span class="sxs-lookup"><span data-stu-id="1c90e-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="1c90e-132">Selecteer op het tabblad **Algemeen** om de details voor de geselecteerde bankrekening weer te geven of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1c90e-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="1c90e-133">[![Tabblad Algemeen](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="1c90e-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="1c90e-134">Voer in het veld **Minimum** het minimumtransactiebedrag in dat de bijzondere kosten activeert.</span><span class="sxs-lookup"><span data-stu-id="1c90e-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="1c90e-135">Voer in het veld **Maximum** het maximumtransactiebedrag in dat de bijzondere kosten activeert.</span><span class="sxs-lookup"><span data-stu-id="1c90e-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="1c90e-136">Definieer in de velden **Begindatum** en **Einddatum** een datumbereik voor het berekenen van de bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="1c90e-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="1c90e-137">Geef in het veld **Minimale bijzondere kosten** het bedrag van de bijzondere kosten op als een percentage van de betaling of als het bedrag voor één betaling.</span><span class="sxs-lookup"><span data-stu-id="1c90e-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="1c90e-138">Selecteer in het veld **Btw-groep** de btw-groep die u wilt gebruiken om de btw voor het bedrag van de bijzondere kosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="1c90e-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="1c90e-139">Selecteer in het veld **Btw-groep voor artikel** de artikel-btw-groep die u wilt gebruiken om de artikel-btw voor het bedrag van de bijzondere kosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="1c90e-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="1c90e-140">Selecteer het tabblad **Interval**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="1c90e-141">[![Tabblad Interval](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="1c90e-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="1c90e-142">Voer in het veld **Dagen** het aantal dagen in tussen de boekingsdatum (kortingsdatum) van de betaling en de vervaldatum van de promesse.</span><span class="sxs-lookup"><span data-stu-id="1c90e-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="1c90e-143">Selecteer in het veld **Percentage/bedrag** of de specificatie een percentage of een ingesteld bedrag is.</span><span class="sxs-lookup"><span data-stu-id="1c90e-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="1c90e-144">Voer in het veld **Minimale bijzondere kosten** het bedrag in van de bijzondere kosten als een percentage van de betaling of als het bedrag voor één betaling.</span><span class="sxs-lookup"><span data-stu-id="1c90e-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="1c90e-145">Sluit de pagina **Instellingen van bijzondere betalingskosten**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="1c90e-146">Sluit de pagina **Bijzondere betalingskosten**.</span><span class="sxs-lookup"><span data-stu-id="1c90e-146">Close the **Payment fee** page.</span></span>

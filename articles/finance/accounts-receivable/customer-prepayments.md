---
title: Vooruitbetalingen door klanten
description: In dit onderwerp wordt uitgelegd hoe u vooruitbetalingen van klanten (ook wel klantdeposito's genoemd) kunt instellen en verwerken.
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019415"
---
# <a name="customer-prepayments"></a><span data-ttu-id="73f3e-103">Vooruitbetalingen door klanten</span><span class="sxs-lookup"><span data-stu-id="73f3e-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73f3e-104">Vooruitbetalingen van klanten worden gebruikt wanneer u een betaling ontvangt van een klant, maar er geen factuur is waarmee de betaling kan worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="73f3e-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="73f3e-105">Dit type betalingen wordt ook wel klantdeposito's of klantstortingen genoemd.</span><span class="sxs-lookup"><span data-stu-id="73f3e-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="73f3e-106">Het proces van het instellen en werken met vooruitbetalingen van klanten bestaat uit de volgende basisstappen.</span><span class="sxs-lookup"><span data-stu-id="73f3e-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="73f3e-107">Maak een klantboekingsprofiel voor vooruitbetalingen.</span><span class="sxs-lookup"><span data-stu-id="73f3e-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="73f3e-108">Stel de parameter **Boekingsprofiel met journaalboekstuk van vooruitbetaling** in.</span><span class="sxs-lookup"><span data-stu-id="73f3e-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="73f3e-109">Maak een klantbetalingsjournaal en schakel op elke regel het selectievakje **Journaalboekstuk van vooruitbetaling** in.</span><span class="sxs-lookup"><span data-stu-id="73f3e-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="73f3e-110">Boek het klantbetalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="73f3e-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="73f3e-111">Nadat een factuur is gegenereerd, vereffent u de vooruitbetaling met deze met de pagina **Openstaande transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="73f3e-112">Een klantboekingsprofiel voor vooruitbetalingen maken</span><span class="sxs-lookup"><span data-stu-id="73f3e-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="73f3e-113">Doorgaans wilt u, wanneer u vooruitbetalingen of stortingen van uw klanten accepteert voordat goederen of services worden geleverd, of voordat er een factuur in het systeem bestaat, het contante geld registreren als een passivum in plaats van een activum in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="73f3e-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="73f3e-114">De vereisten voor het registreren van deze bedragen in uw grootboek kunnen echter verschillen, afhankelijk van uw land of regio.</span><span class="sxs-lookup"><span data-stu-id="73f3e-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="73f3e-115">Raadpleeg daarom uw accountants over eventuele lokale regelgeving.</span><span class="sxs-lookup"><span data-stu-id="73f3e-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="73f3e-116">In het algemeen is het proces voor het maken van een boekingsprofiel dat kan worden gebruikt voor vooruitbetalingen hetzelfde als het proces voor het maken van andere boekingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="73f3e-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="73f3e-117">Het belangrijkste verschil is de hoofdrekening die u selecteert in het veld **Totaalrekening**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="73f3e-118">Zie [Boekingsprofielen van klant](customer-posting-profiles.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="73f3e-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="73f3e-119">Parameters voor vooruitbetalingen van klanten definiëren</span><span class="sxs-lookup"><span data-stu-id="73f3e-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="73f3e-120">Er zijn twee belangrijke parameters voor klanten waar u rekening mee moet houden wanneer u het systeem voor vooruitbetalingen voor klanten configureert.</span><span class="sxs-lookup"><span data-stu-id="73f3e-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="73f3e-121">Ga als volgt te werk om de parameters te configureren.</span><span class="sxs-lookup"><span data-stu-id="73f3e-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="73f3e-122">Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="73f3e-123">Optioneel: stel op het tabblad **Grootboek en btw** op het sneltabblad **Betaling** de optie **BTW op journaalboekstuk van vooruitbetaling** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="73f3e-124">Selecteer in het veld **Boekingsprofiel met journaalboekstuk van vooruitbetaling** het klantboekingsprofiel dat moet worden gebruikt wanneer vooruitbetalingen van klanten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="73f3e-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="73f3e-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="73f3e-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="73f3e-126">Journaalboekstukken van vooruitbetaling van klanten maken</span><span class="sxs-lookup"><span data-stu-id="73f3e-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="73f3e-127">Wanneer u het klantbetalingsjournaal maakt, moet u voor elke vooruitbetaling de optie **Journaalboekstuk van vooruitbetaling** instellen op **Ja** op de pagina **Journaal met betalingen van klant**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="73f3e-128">Volg deze stappen om een klantbetaling te maken.</span><span class="sxs-lookup"><span data-stu-id="73f3e-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="73f3e-129">Ga naar **Klanten \> Betalingen \> Journaal met betalingen van klant**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="73f3e-130">Selecteer **Nieuw** om een journaal te maken.</span><span class="sxs-lookup"><span data-stu-id="73f3e-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="73f3e-131">Selecteer in het veld **Naam** de journaalnaam die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="73f3e-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="73f3e-132">Als u de optie **BTW op journaalboekstuk van vooruitbetaling** in de vorige procedure op **Ja** instelt, moet u een journaalnaam selecteren waarbij de parameter **Btw is inbegrepen in bedrag** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="73f3e-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="73f3e-133">Optioneel: voer in het veld **Omschrijving** een uitgebreide omschrijving in.</span><span class="sxs-lookup"><span data-stu-id="73f3e-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="73f3e-134">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="73f3e-134">Select **Lines**.</span></span>
6. <span data-ttu-id="73f3e-135">Als er geen lege regel bestaat, selecteert u **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="73f3e-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="73f3e-136">Voer in het veld **Datum** de datum in waarop de vooruitbetaling moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="73f3e-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="73f3e-137">Selecteer in het veld **Rekening** de klant voor de vooruitbetaling.</span><span class="sxs-lookup"><span data-stu-id="73f3e-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="73f3e-138">Optioneel: voer in het veld **Omschrijving** een uitgebreide omschrijving van de transactie in.</span><span class="sxs-lookup"><span data-stu-id="73f3e-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="73f3e-139">Voer in het veld **Credit** het bedrag van de vooruitbetaling in.</span><span class="sxs-lookup"><span data-stu-id="73f3e-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="73f3e-140">Selecteer in het veld **Tegenrekening** de rekening waar de betaling mee moet worden verrekend.</span><span class="sxs-lookup"><span data-stu-id="73f3e-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="73f3e-141">Selecteer bijvoorbeeld de bank of hoofdrekening waar u de betaling naar wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="73f3e-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="73f3e-142">Selecteer in het veld **Betalingsmethode** de betalingsmethode van de klant.</span><span class="sxs-lookup"><span data-stu-id="73f3e-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="73f3e-143">Stel op het tabblad **Betaling** de optie **Journaalboekstuk van vooruitbetaling** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="73f3e-144">Herhaal stap 7 t/m 13 voor elke extra vooruitbetaling die moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="73f3e-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="73f3e-145">Selecteer **Boeken** om het journaal te voltooien.</span><span class="sxs-lookup"><span data-stu-id="73f3e-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="73f3e-146">Vooruitbetalingen met facturen vereffenen</span><span class="sxs-lookup"><span data-stu-id="73f3e-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="73f3e-147">U kunt de werkruimte **Klantbetalingen** gebruiken om eenvoudig betalingen te vinden en te vereffenen die nog niet volledig zijn vereffend.</span><span class="sxs-lookup"><span data-stu-id="73f3e-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="73f3e-148">Selecteer in het dashboard **Start** de tegel **Klantbetalingen**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="73f3e-149">Zoek in de sectie **Klanttransacties** op het tabblad **Betalingen niet vereffend** naar de te vereffenen betaling en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="73f3e-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="73f3e-150">Selecteer **Transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="73f3e-151">Schakel het selectievakje **Markeren** in voor de factuur en de betaling die wordt vereffend.</span><span class="sxs-lookup"><span data-stu-id="73f3e-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="73f3e-152">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="73f3e-152">Select **Post**.</span></span>

<span data-ttu-id="73f3e-153">Zie [Vereffeningsoverzicht](/cash-bank-management/settlement-overview.md) voor meer informatie over het vereffenen van openstaande transacties.</span><span class="sxs-lookup"><span data-stu-id="73f3e-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>

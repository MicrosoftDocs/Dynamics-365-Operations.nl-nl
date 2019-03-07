---
title: Tarieven voor klantbetalingen vaststellen
description: Maak betalingskosten voor klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5acb202d46ef39376a01ca592f60926786d11186
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "354823"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="c2fd2-103">Tarieven voor klantbetalingen vaststellen</span><span class="sxs-lookup"><span data-stu-id="c2fd2-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2fd2-104">Maak betalingskosten voor klantbetalingen.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="c2fd2-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c2fd2-106">Ga naar Klanten > Betalingsinstelling > Betalingskosten.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="c2fd2-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-107">Click New.</span></span>
3. <span data-ttu-id="c2fd2-108">Typ een ID van bijzondere kosten in het veld ID van bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="c2fd2-109">De ID van bijzondere kosten wordt weergegeven in betalingsjournalen. Maak deze dus beschrijvend om te begrijpen welke bijzondere kosten in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="c2fd2-110">Geef in het veld Naam een naam voor de bijzondere kosten op.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="c2fd2-111">Typ in het veld Beschrijving van bijzondere kosten een omschrijving voor de bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="c2fd2-112">Selecteer of de bijzondere kosten in rekening worden gebracht aan de klant of aan een grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="c2fd2-113">Als de bijzondere kosten aan de klant in rekening worden gebracht, selecteert u Klant.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="c2fd2-114">Als de bijzondere kosten in rekening worden gebracht aan uw organisatie als onkosten, selecteert u Grootboek.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="c2fd2-115">Selecteer Klant voor deze taak.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="c2fd2-116">Selecteer het type journaal dat deze bijzondere betalingskosten kan gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="c2fd2-117">Als deze kosten worden gebruikt voor klantbetalingen, zal het journaaltype waarschijnlijk Klantbetaling zijn.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="c2fd2-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-118">Click Save.</span></span>
9. <span data-ttu-id="c2fd2-119">Klik op Instellingen van bijzondere betalingskosten.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="c2fd2-120">De instelling van bijzondere kosten wordt gebruikt om de criteria te definiëren voor wanneer de bijzondere kosten voor betaling in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="c2fd2-121">Zo kunt u bijvoorbeeld definiëren dat de kosten worden berekend als de bankrekening USMF OPER en de betalingsmethode cheque is.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="c2fd2-122">Selecteer Tabel, Groep of Alle om te definiëren aan welke bankrekeningen deze bijzondere kosten in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="c2fd2-123">Als u Alle selecteert, kunnen deze kosten in rekening worden gebracht aan alle bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="c2fd2-124">Als u Tabel selecteert, kunnen deze bijzondere kosten alleen in rekening worden gebracht aan de bankrekening die u selecteert.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="c2fd2-125">Als u Groep selecteert, kunnen deze kosten alleen in rekening worden gebracht aan de bankrekeningen in de geselecteerde bankgroep.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="c2fd2-126">Selecteer een bankgroep of een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="c2fd2-127">Als u Tabel hebt geselecteerd, worden met de zoekopdracht bankrekeningen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="c2fd2-128">Als u Groep hebt geselecteerd, worden met de zoekopdracht bankgroepen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="c2fd2-129">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="c2fd2-130">Selecteer de betalingsmethode waarvoor deze bijzondere kosten in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="c2fd2-131">Zo kunt u bijvoorbeeld bijzondere kosten in rekening brengen aan uw klanten als zij betalingen als cheque uitvoeren in plaats van als elektronische betaling.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="c2fd2-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="c2fd2-133">Voer, indien relevant, een betalingsvaluta in.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="c2fd2-134">De betalingsvaluta wordt gebruikt als extra criterium voor het in rekening brengen van de bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="c2fd2-135">Zo kan uw bank bijvoorbeeld extra bijzondere kosten in rekening brengen voor betalingen die in de valuta USD worden ontvangen, omdat zij doorgaans alleen transacties uitvoeren in de valuta EUR.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="c2fd2-136">Selecteer of de bijzondere kosten een percentage, bedrag of interval zijn.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="c2fd2-137">Voer een percentage of bedrag van de bijzondere kosten in.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="c2fd2-138">Als in het veld Percentage/Bedrag de waarde Procent wordt gebruikt, is de hier ingevoerde waarde een percentage.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="c2fd2-139">Als in het veld Percentage/Bedrag de waarde Bedrag wordt gebruikt, is de waarde die u hier invoert een bedrag.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="c2fd2-140">Als de waarde in het veld Percentage/Bedrag Interval is, gebruikt u het tabblad Interval om de niveaus te definiëren.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="c2fd2-141">Selecteer in het veld Valuta van kosten de valuta van de bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="c2fd2-142">Dit is de valuta waarin de bijzondere kosten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="c2fd2-143">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="c2fd2-143">Click Save.</span></span>


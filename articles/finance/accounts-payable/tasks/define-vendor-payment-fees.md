---
title: Bijzondere kosten voor leveranciersbetalingen definiëren
description: Stel bijzondere kosten voor leveranciersbetalingen in.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52321851a1aa588a0bbe238e366a28d503665988
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979333"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="76f6b-103">Bijzondere kosten voor leveranciersbetalingen definiëren</span><span class="sxs-lookup"><span data-stu-id="76f6b-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76f6b-104">Stel bijzondere kosten voor leveranciersbetalingen in.</span><span class="sxs-lookup"><span data-stu-id="76f6b-104">Set up vendor payment fees.</span></span> <span data-ttu-id="76f6b-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="76f6b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="76f6b-106">Ga naar Leveranciers > Betalingsinstelling > Betalingskosten.</span><span class="sxs-lookup"><span data-stu-id="76f6b-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="76f6b-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76f6b-107">Click New.</span></span>
3. <span data-ttu-id="76f6b-108">Typ een waarde in het veld ID van bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="76f6b-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="76f6b-109">De id van bijzondere kosten moet aangeven wanneer deze kosten worden gebruikt, zoals "EFT-kosten".</span><span class="sxs-lookup"><span data-stu-id="76f6b-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="76f6b-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="76f6b-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="76f6b-111">Typ een waarde in het veld Beschrijving van bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="76f6b-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="76f6b-112">Voeg een omschrijving toe om nadere details te verstrekken over wanneer de kosten in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="76f6b-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="76f6b-113">Selecteer in het veld Toeslag de optie Leverancier of Grootboek.</span><span class="sxs-lookup"><span data-stu-id="76f6b-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="76f6b-114">Grootboek wordt gebruikt wanneer het tarief in rekening wordt gebracht aan uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="76f6b-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="76f6b-115">Leverancier wordt gebruikt wanneer de kosten in rekening worden gebracht aan de leverancier.</span><span class="sxs-lookup"><span data-stu-id="76f6b-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="76f6b-116">Voer een hoofdrekening in waaraan de bijzondere kosten in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="76f6b-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="76f6b-117">Deze optie is alleen beschikbaar als Grootboek wordt geselecteerd als optie bij Toeslag.</span><span class="sxs-lookup"><span data-stu-id="76f6b-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="76f6b-118">Selecteer het journaal waarin deze kosten kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="76f6b-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="76f6b-119">Voor bijzondere kosten leveranciersbetaling selecteert u het journaal "Voorschot van leverancier".</span><span class="sxs-lookup"><span data-stu-id="76f6b-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="76f6b-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="76f6b-120">Click Save.</span></span>
10. <span data-ttu-id="76f6b-121">Klik op Instellingen van bijzondere betalingskosten.</span><span class="sxs-lookup"><span data-stu-id="76f6b-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="76f6b-122">Ga naar de instellingen voor de bijzondere betalingskosten om te definiëren wanneer de kosten standaard moeten worden opgenoemn in het journaal dat u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="76f6b-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="76f6b-123">Selecteer Tabel, Groep of Alle.</span><span class="sxs-lookup"><span data-stu-id="76f6b-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="76f6b-124">Tabel wordt gebruikt om één bankrekening te selecteren, Groep wordt gebruikt om een bankgroep te selecteren en Alle dient om deze kosten in te stellen voor alle bankrekeningen</span><span class="sxs-lookup"><span data-stu-id="76f6b-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="76f6b-125">Selecteer een bankgroep of een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="76f6b-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="76f6b-126">De zoekopdracht geeft bankgroepen weer als u Groep hebt geselecteerd en bankrekeningen als u Tabel hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="76f6b-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="76f6b-127">Selecteer de betalingsmethode waarvoor deze bijzondere kosten in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="76f6b-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="76f6b-128">Selecteer de betalingsspecificatie voor de geselecteerde betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="76f6b-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="76f6b-129">De betalingsspecificatie wordt gebruikt met de betalingsmethoden van EFT (Electronic Funds Transfer).</span><span class="sxs-lookup"><span data-stu-id="76f6b-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="76f6b-130">Selecteer of de bijzondere kosten een percentage, bedrag of interval zijn.</span><span class="sxs-lookup"><span data-stu-id="76f6b-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="76f6b-131">Voer het percentage of bedrag van de bijzondere kosten in.</span><span class="sxs-lookup"><span data-stu-id="76f6b-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="76f6b-132">Als Kosten een percentage is, voert u het percentage in.</span><span class="sxs-lookup"><span data-stu-id="76f6b-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="76f6b-133">Als Kosten een bedrag is, voert u het bedrag van de bijzondere kosten in.</span><span class="sxs-lookup"><span data-stu-id="76f6b-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="76f6b-134">Als Kosten een interval is, gebruikt u het tabblad Interval om de gelaagde kosten te definiëren.</span><span class="sxs-lookup"><span data-stu-id="76f6b-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="76f6b-135">Selecteer in het veld Valuta van kosten de valuta waarvoor de bijzondere kosten worden berekend.</span><span class="sxs-lookup"><span data-stu-id="76f6b-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="76f6b-136">Deze valuta is voor de bijzondere kosten.</span><span class="sxs-lookup"><span data-stu-id="76f6b-136">This currency is for the fee.</span></span> <span data-ttu-id="76f6b-137">De betalingsvaluta wordt gebruikt om te bepalen wanneer de regel voor bijzondere kosten moet worden beoordeeld op basis van de valuta van de betaling.</span><span class="sxs-lookup"><span data-stu-id="76f6b-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="76f6b-138">Zo kan uw bank bijvoorbeeld bijzondere kosten in rekening brengen wanneer een betaling wordt gedaan in EUR, terwijl voor alle andere betalingen geen kosten worden berekend.</span><span class="sxs-lookup"><span data-stu-id="76f6b-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="76f6b-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="76f6b-139">Click Save.</span></span>


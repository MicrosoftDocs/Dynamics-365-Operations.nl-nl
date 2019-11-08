---
title: Betalingen aanmaken voor klanten met mandaten voor automatische afschrijving
description: In deze procedure ziet u hoe u een automatisch ISO20022-afschrijvingsbestand genereert voor een klant waarvoor automatische afschrijving is geconfigureerd en die een factuur moet betalen.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 129c5291a29994f91ef325aa9b9a3b54a0e958d6
ms.sourcegitcommit: 807dec193cd163c9f5d949e744cfde40f2eb24b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2019
ms.locfileid: "2468950"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="f5bd1-103">Betalingen aanmaken voor klanten met mandaten voor automatische afschrijving</span><span class="sxs-lookup"><span data-stu-id="f5bd1-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5bd1-104">In deze procedure ziet u hoe u een automatisch ISO20022-afschrijvingsbestand genereert voor een klant waarvoor automatische afschrijving is geconfigureerd en die een factuur moet betalen.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="f5bd1-105">Maken en boeken van een factuur zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="f5bd1-106">In plaats van een te betalen factuur kunt u een mandaat in een journaal selecteren voordat een betalingsbestand wordt gegenereerd, om een scenario met vooruitbetaling door de klant te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="f5bd1-107">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="f5bd1-108">Dit is de vijfde van vijf procedures die het proces weergeven voor innen van klantbetalingen via configuraties voor elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f5bd1-109">U moet alle voorgaande taken hebben voltooid voordat u deze taak kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="f5bd1-110">U moet eerst configuraties voor elektronische rapportage van klantbetaling importeren, methode van betalingen configureren en uw bedrijfs- en klantgegevens instellen.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="f5bd1-111">Een vrije-tekstfactuur met gegevens voor automatische afschrijving boeken</span><span class="sxs-lookup"><span data-stu-id="f5bd1-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="f5bd1-112">Ga naar Klanten > Facturen > Alle vrije-tekstfacturen.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="f5bd1-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-113">Click New.</span></span>
3. <span data-ttu-id="f5bd1-114">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="f5bd1-115">Selecteer bijvoorbeeld DE-010.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="f5bd1-116">Typ of selecteer een waarde in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="f5bd1-117">2: Huidige gebeurtenis: het huidige product wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-117">For example.</span></span> <span data-ttu-id="f5bd1-118">selecteer Elektronisch.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-118">select Electronic.</span></span>  
5. <span data-ttu-id="f5bd1-119">Typ of selecteer een waarde in het veld Mandaat-id voor automatische afschrijving.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="f5bd1-120">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-120">Click Add line.</span></span>
7. <span data-ttu-id="f5bd1-121">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="f5bd1-122">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="f5bd1-123">Voer in het veld Eenheidsprijs een getal in.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="f5bd1-124">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-124">Click Post.</span></span>
11. <span data-ttu-id="f5bd1-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="f5bd1-126">Een betaling maken</span><span class="sxs-lookup"><span data-stu-id="f5bd1-126">Create a payment</span></span>
1. <span data-ttu-id="f5bd1-127">Ga naar Klanten > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f5bd1-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-128">Click New.</span></span>
3. <span data-ttu-id="f5bd1-129">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="f5bd1-130">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-130">Click Lines.</span></span>
5. <span data-ttu-id="f5bd1-131">Klik op Betalingsvoorstel.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="f5bd1-132">Klik op Betalingsvoorstel maken.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="f5bd1-133">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="f5bd1-134">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-134">Click Filter.</span></span>
9. <span data-ttu-id="f5bd1-135">Selecteer in de lijst de rij voor de tabel Klanttransacties en het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="f5bd1-136">U kunt alle criteria voor het selecteren van te betalen klanttransacties toepassen.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="f5bd1-137">Gebruik voor dit voorbeeld 'Elektronisch' als de betalingsmethode om transacties te filteren.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="f5bd1-138">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="f5bd1-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-139">Click OK.</span></span>
12. <span data-ttu-id="f5bd1-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-140">Click OK.</span></span>
13. <span data-ttu-id="f5bd1-141">Klik op Betalingen maken.</span><span class="sxs-lookup"><span data-stu-id="f5bd1-141">Click Create payments.</span></span>
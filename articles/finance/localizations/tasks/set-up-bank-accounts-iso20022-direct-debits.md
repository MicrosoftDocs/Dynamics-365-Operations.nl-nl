---
title: Klanten en bankrekeningen van klanten instellen voor ISO20022-automatische overschrijvingen
description: Deze taak voert u door het instellen van een bankrekening voor een klant en een mandaat voor automatische afschrijving van een klant die zijn vereist voor het genereren van het klantenbetalingsbestand zoals ISO20022 automatische afschrijving.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b09d7d203f1bb58fad26a109962005affa6d307
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144902"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="1be36-103">Klanten en bankrekeningen van klanten instellen voor ISO20022-automatische overschrijvingen</span><span class="sxs-lookup"><span data-stu-id="1be36-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1be36-104">Deze taak voert u door het instellen van een bankrekening voor een klant en een mandaat voor automatische afschrijving van een klant die zijn vereist voor het genereren van het klantenbetalingsbestand zoals ISO20022 automatische afschrijving.</span><span class="sxs-lookup"><span data-stu-id="1be36-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="1be36-105">Afhankelijk van de indelingen voor klantenbetalinge die zijn geconfigureerd, kan extra informatie zijn vereist voor een klant of een klantenbankrekening, die niet in deze procedure wordt behandeld.</span><span class="sxs-lookup"><span data-stu-id="1be36-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="1be36-106">Deze taak werd gemaakt met het demobedrijf DEMF met een primair adres van een rechtspersoon in Duitsland.</span><span class="sxs-lookup"><span data-stu-id="1be36-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="1be36-107">Dit is de vierde van vijf taken die het proces voor klantenbetalingen toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="1be36-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="1be36-108">Een bankrekening voor een klant instellen</span><span class="sxs-lookup"><span data-stu-id="1be36-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="1be36-109">Ga naar Klanten > Klanten > Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="1be36-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="1be36-110">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1be36-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1be36-111">Filter bijvoorbeeld op het veld Rekening met een waarde van 'DE-010'.</span><span class="sxs-lookup"><span data-stu-id="1be36-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="1be36-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1be36-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1be36-113">Klik in het actievenster op Klant.</span><span class="sxs-lookup"><span data-stu-id="1be36-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="1be36-114">Klik op Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="1be36-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="1be36-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1be36-115">Click New.</span></span>
7. <span data-ttu-id="1be36-116">Typ een waarde in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="1be36-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="1be36-117">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="1be36-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1be36-118">Voer bijvoorbeeld 'EUR bank' in.</span><span class="sxs-lookup"><span data-stu-id="1be36-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="1be36-119">Typ of selecteer een waarde in het veld Bankgroepen.</span><span class="sxs-lookup"><span data-stu-id="1be36-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="1be36-120">Typ een waarde in het veld IBAN.</span><span class="sxs-lookup"><span data-stu-id="1be36-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="1be36-121">Voer bijvoorbeeld 'DE36200400000628808808' in.</span><span class="sxs-lookup"><span data-stu-id="1be36-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="1be36-122">Typ een waarde in het veld SWIFT-code.</span><span class="sxs-lookup"><span data-stu-id="1be36-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="1be36-123">Voer bijvoorbeeld 'COBADEFFXXX' in.</span><span class="sxs-lookup"><span data-stu-id="1be36-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="1be36-124">Merk op dat SWIFT/BIC niet voor veel betalingsindelingen is vereist. Het wordt echter wel aanbevolen om het te registreren voor een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="1be36-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="1be36-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1be36-125">Click Save.</span></span>
13. <span data-ttu-id="1be36-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1be36-126">Close the page.</span></span>
14. <span data-ttu-id="1be36-127">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="1be36-127">Click Edit.</span></span>
15. <span data-ttu-id="1be36-128">Vouw de sectie van Standaardwaarden betaling uit.</span><span class="sxs-lookup"><span data-stu-id="1be36-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="1be36-129">Typ of selecteer een waarde in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="1be36-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="1be36-130">Een mandaat voor automatische afschrijving toevoegen</span><span class="sxs-lookup"><span data-stu-id="1be36-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="1be36-131">Vouw de sectie Mandaten voor automatische afschrijving uit.</span><span class="sxs-lookup"><span data-stu-id="1be36-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="1be36-132">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1be36-132">Click Add.</span></span>
3. <span data-ttu-id="1be36-133">Typ of selecteer een waarde in het veld Bankrekening van crediteur.</span><span class="sxs-lookup"><span data-stu-id="1be36-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="1be36-134">Selecteer bijvoorbeeld DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="1be36-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="1be36-135">Voer een datum in het veld Handtekening in.</span><span class="sxs-lookup"><span data-stu-id="1be36-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="1be36-136">Klik op Ja om de datum te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="1be36-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="1be36-137">Typ of selecteer een waarde in het veld Locatie handtekening.</span><span class="sxs-lookup"><span data-stu-id="1be36-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="1be36-138">Voer in het veld Verwacht aantal betalingen een getal in.</span><span class="sxs-lookup"><span data-stu-id="1be36-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="1be36-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1be36-139">Click OK.</span></span>
9. <span data-ttu-id="1be36-140">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1be36-140">Click Save.</span></span>


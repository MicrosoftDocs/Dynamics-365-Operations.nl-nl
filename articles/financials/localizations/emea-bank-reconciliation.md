---
title: Bankafschriften en betalingsafstemming voor de EU
description: Dit onderwerp bevat een overzicht van de functionaliteit die u kunt gebruiken om betalingsgegevens van banken af te stemmen in indelingen die door Europese landen worden gebruikt.
author: neserovleo
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 267994
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: db48eec38185692f5d3f67503feba64bcdd71035
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="bank-statement-and-payment-reconciliation-for-the-eu"></a><span data-ttu-id="e0b85-103">Bankafschriften en betalingsafstemming voor de EU</span><span class="sxs-lookup"><span data-stu-id="e0b85-103">Bank statement and payment reconciliation for the EU</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e0b85-104">Dit onderwerp bevat een overzicht van de functionaliteit die u kunt gebruiken om betalingsgegevens van banken af te stemmen in indelingen die door Europese landen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e0b85-104">This topic provides an overview of the functionality that you can use to reconcile payment information from banks in formats that are used by European countries.</span></span>

<span data-ttu-id="e0b85-105">In Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition kunt u transacties importeren vanuit banken en deze transacties vereffenen voor bestaande transacties.</span><span class="sxs-lookup"><span data-stu-id="e0b85-105">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can import transactions from banks and settle these transactions against existing transactions.</span></span> <span data-ttu-id="e0b85-106">In Europa kunt u dit doen voor de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="e0b85-106">In Europe, you can do this for the following scenarios:</span></span>

-   <span data-ttu-id="e0b85-107">Bankafschriften importeren</span><span class="sxs-lookup"><span data-stu-id="e0b85-107">Importing bank statements</span></span>
-   <span data-ttu-id="e0b85-108">Betalingen importeren</span><span class="sxs-lookup"><span data-stu-id="e0b85-108">Importing payments</span></span>
-   <span data-ttu-id="e0b85-109">Retourbestanden importeren</span><span class="sxs-lookup"><span data-stu-id="e0b85-109">Importing return files</span></span>

## <a name="bank-statements"></a><span data-ttu-id="e0b85-110">Bankafschriften</span><span class="sxs-lookup"><span data-stu-id="e0b85-110">Bank statements</span></span>
<span data-ttu-id="e0b85-111">Een *bankafschrift* of *rekeningoverzicht* is een overzicht van financiële transacties die hebben plaatsgevonden in een bepaalde periode op een bankrekening van een bedrijf met een financiële instelling.</span><span class="sxs-lookup"><span data-stu-id="e0b85-111">A *bank statement* or *account statement* is a summary of financial transactions that have occurred over a given period on a bank account held by a company with a financial institution.</span></span> <span data-ttu-id="e0b85-112">U kunt een bankafschrift importeren in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0b85-112">In Finance and Operations you can import a bank statement.</span></span> <span data-ttu-id="e0b85-113">Het is belangrijk om geïmporteerde transacties te vereffenen met bestaande transacties, en om het begin- en eindsaldo van de bankrekeningen te verifiëren.</span><span class="sxs-lookup"><span data-stu-id="e0b85-113">It is important to settle imported transactions with existing transactions as well as verify the opening and ending balance of the bank accounts.</span></span> <span data-ttu-id="e0b85-114">De volgende lijst bevat de ondersteunde Europese indelingen.</span><span class="sxs-lookup"><span data-stu-id="e0b85-114">The following list includes the supported European formats.</span></span>

-   <span data-ttu-id="e0b85-115">Europese bestandsindelingen geavanceerde bankafstemming.</span><span class="sxs-lookup"><span data-stu-id="e0b85-115">Advanced bank reconciliation European file formats.</span></span> <span data-ttu-id="e0b85-116">Zie voor meer informatie [Overzicht van geavanceerde bankafstemming](../cash-bank-management/advanced-bank-reconciliation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e0b85-116">For more information, see [Advanced bank reconciliation overview](../cash-bank-management/advanced-bank-reconciliation-overview.md).</span></span>
-   <span data-ttu-id="e0b85-117">ISO 20022 camt.053 berichtbestandsindeling bankafschrift</span><span class="sxs-lookup"><span data-stu-id="e0b85-117">ISO 20022 camt.053 bank statement message file format.</span></span>
-   <span data-ttu-id="e0b85-118">Bestandsindeling CODA-bankafschrift</span><span class="sxs-lookup"><span data-stu-id="e0b85-118">CODA bank statement file format.</span></span> <span data-ttu-id="e0b85-119">Zie [CODA-bankafschrift](emea-bel-coda-bank-statement-import.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e0b85-119">For more information, see [CODA bank statement](emea-bel-coda-bank-statement-import.md).</span></span>

## <a name="customer-and-vendor-payments-import-and-return-messages"></a><span data-ttu-id="e0b85-120">Import- en retourberichten van klant- en leveranciersbetalingen</span><span class="sxs-lookup"><span data-stu-id="e0b85-120">Customer and vendor payments import and return messages</span></span>
<span data-ttu-id="e0b85-121">Naast een bankafschrift kunnen banken specifieke berichten verschaffen met informatie over betalingen van klanten en leveranciers, die kunnen worden geïmporteerd in Finance and Operations en afgestemd met klant- en leverancierstransacties.</span><span class="sxs-lookup"><span data-stu-id="e0b85-121">In addition to a bank statement, banks can provide specific messages, containing information about customer and vendor payments, which can be imported into Finance and Operations and reconciled with customer and vendor transactions.</span></span> <span data-ttu-id="e0b85-122">Wanneer een bedrijf informatie over inkomende klantbetalingstransacties van de bank moet ontvangen, kunnen de importindelingen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e0b85-122">When a company needs to receive information about incoming customer payments transactions from the bank, the import formats can be used.</span></span> <span data-ttu-id="e0b85-123">Voor bedrijven die gebruikmaken van automatische afschrijving en kredietoverdracht, kunnen de retourberichten worden ontvangen om de status bij te werken van betalingen die eerder zijn geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="e0b85-123">For companies that use direct debit and credit transfer, the return messages can be received to update the status of payments that were previously exported.</span></span> <span data-ttu-id="e0b85-124">Het verschil tussen importindelingen en retourindelingen is dat retouren meestal zijn bedoeld om al gemaakte betalingsjournaalregels bij te werken (ze kunnen worden gemaakt wanneer automatische afschrijvingen of kredietoverdrachten zijn geïnitieerd) in plaats van nieuwe regels te maken.</span><span class="sxs-lookup"><span data-stu-id="e0b85-124">The difference between import formats and return formats is that returns are targeted mostly to update already created payment journal lines (they can be created when direct debit or credit transfer were initiated) instead of creating new lines.</span></span> <span data-ttu-id="e0b85-125">Sommige complexe importindelingen kunnen ook retourscenario's omvatten.</span><span class="sxs-lookup"><span data-stu-id="e0b85-125">Some complex import formats can also include return scenarios.</span></span> <span data-ttu-id="e0b85-126">In het volgende voorbeeld wordt getoond hoe deze verdeling moet worden geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="e0b85-126">The following example shows how this division should be implemented.</span></span>

### <a name="import-formats"></a><span data-ttu-id="e0b85-127">Importindelingen</span><span class="sxs-lookup"><span data-stu-id="e0b85-127">Import formats</span></span>

-   <span data-ttu-id="e0b85-128">ISO 20022 [camt.054](emea-ISO20022-file-formats.md) bankmeldingsbericht</span><span class="sxs-lookup"><span data-stu-id="e0b85-128">ISO 20022 [camt.054](emea-ISO20022-file-formats.md) bank notification message</span></span>
-   <span data-ttu-id="e0b85-129">[Nets-importindeling](emea-nor-nets-import-format.md) - Complexe functie voor Noorse betalingsindelingen</span><span class="sxs-lookup"><span data-stu-id="e0b85-129">[Nets import format](emea-nor-nets-import-format.md) - Complex feature for Norwegian payment formats</span></span>
-   <span data-ttu-id="e0b85-130">[ESR](emea-che-esr-customer-payments-import.md)-klantbetalingen importeren</span><span class="sxs-lookup"><span data-stu-id="e0b85-130">[ESR](emea-che-esr-customer-payments-import.md) customer payments import</span></span>
-   <span data-ttu-id="e0b85-131">Importbetalingsindelingen voor Zweden - BankGirot Max- en BankGirot OCR-indelingen</span><span class="sxs-lookup"><span data-stu-id="e0b85-131">Import payment formats for Sweden - BankGirot Max and BankGirot OCR formats</span></span>

### <a name="return-formats"></a><span data-ttu-id="e0b85-132">Retourindelingen</span><span class="sxs-lookup"><span data-stu-id="e0b85-132">Return formats</span></span>

-   <span data-ttu-id="e0b85-133">ISO 20022 [pain.002](emea-ISO20022-file-formats.md) betalingsstatusrapport</span><span class="sxs-lookup"><span data-stu-id="e0b85-133">ISO 20022 [pain.002](emea-ISO20022-file-formats.md) payment status report</span></span>
-   <span data-ttu-id="e0b85-134">(DNK) BetalingsserviceBasis-returformat: retourindeling voor Betalingsservice-exportindeling voor klanten</span><span class="sxs-lookup"><span data-stu-id="e0b85-134">(DNK) BetalingsserviceBasis-returformat – Return format for customer Betalingsservice export format</span></span>
-   <span data-ttu-id="e0b85-135">[Importbetalingsindelingen voor Zweden](emea-swe-payment-formats-import.md) -Bankgirot Autogiro-retouren</span><span class="sxs-lookup"><span data-stu-id="e0b85-135">[Import payment formats for Sweden](emea-swe-payment-formats-import.md) - Bankgirot Autogiro returns</span></span>
-   <span data-ttu-id="e0b85-136">(SWE) BankGirot-retour: retourindeling leveranciersbetalingen. Dit komt overeen met de Bankgirot-exportindeling</span><span class="sxs-lookup"><span data-stu-id="e0b85-136">(SWE) BankGirot return – Vendor payments return format, which corresponds to Bankgirot export format</span></span>




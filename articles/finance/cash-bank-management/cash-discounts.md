---
title: Contantkortingen
description: Contantkortingen worden ingesteld en gedeeld voor Leveranciers en Klanten.  De beschikbare contantkorting kan op de klant- of leveranciersfactuur worden gedefinieerd en deze wordt toegepast als de factuur wordt betaald binnen de datum voor de contantkorting.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 139fb4fdb7d4f8034bff5e9668dc794f29fb327e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442105"
---
# <a name="cash-discounts"></a><span data-ttu-id="1e0dd-104">Contantkortingen</span><span class="sxs-lookup"><span data-stu-id="1e0dd-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e0dd-105">Contantkortingen worden ingesteld en gedeeld voor Leveranciers en Klanten.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="1e0dd-106">De beschikbare contantkorting kan op de klant- of leveranciersfactuur worden gedefinieerd en deze wordt toegepast als de factuur wordt betaald binnen de datum voor de contantkorting.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="1e0dd-107">Contantkortingen</span><span class="sxs-lookup"><span data-stu-id="1e0dd-107">Cash discounts</span></span>

<span data-ttu-id="1e0dd-108">Contantkortingen voor zowel klanten als leveranciers kunnen op de pagina Contantkortingen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="1e0dd-109">Ook kunt u met behulp van het veld Volgende kortingscode een reeks contantkortingen maken die elkaar opvolgen, telkens wanneer de datum van de vorige contantkorting verloopt.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="1e0dd-110">Zie “Voorbeeld: reeks contantkortingen” verderop in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="1e0dd-111">Als de factuur, credittransactie (een betaling of creditnota) of beide worden ingevoerd in een andere valuta dan de valuta voor boekhouding van de rechtspersoon, wordt de contantkorting berekend aan de hand van de wisselkoers op basis van de datum van de betaling of de creditnota.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="1e0dd-112">Als de factuur en het creditdocument worden ingevoerd in verschillende rechtspersonen en de valuta's voor boekhouding van de rechtspersonen verschillend zijn, wordt de wisselkoers gebruikt van de rechtspersoon van de factuur op de datum van het creditdocument.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="1e0dd-113">Zie “Voorbeeld: wisselkoersen voor contantkortingen” verderop in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="1e0dd-114">Standaardvolgorde van de hoofdrekening voor contantkortingen</span><span class="sxs-lookup"><span data-stu-id="1e0dd-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="1e0dd-115">Als een factuur wordt vereffend binnen de tijd waarin een contactkorting kan worden gegeven, wordt de contantkorting automatisch geboekt volgens de volgende standaardprioriteit naar een grootboekrekening voor contantkortingen:</span><span class="sxs-lookup"><span data-stu-id="1e0dd-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="1e0dd-116">De hoofdrekening die is opgegeven in het veld Alternatieve contantkortingsrekening van de pagina Openstaande transacties vereffenen van de klant of de pagina Openstaande transacties vereffenen van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="1e0dd-117">De hoofdrekening die is opgegeven in het veld Contantkorting van de klant of het veld Contantkorting van leverancier van de grootboekboekingsgroep die is toegewezen aan de btw-code van de factuur.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="1e0dd-118">Configureer grootboekboekingsgroepen op de pagina Grootboekboekingsgroepen en wijs deze toe aan btw-codes op de pagina Btw-codes.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="1e0dd-119">De hoofdrekening voor boeking op de pagina Contantkortingen in het veld Hoofdrekening voor klantkortingen of het veld Hoofdrekening voor leverancierskortingen voor de contantkortingscode van de klant of leverancier op de vereffende factuur.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="1e0dd-120">De hoofdrekening voor contantkortingen, zoals gedefinieerd op de pagina Rekeningen voor automatische transacties.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="1e0dd-121">Voorbeeld: reeksen contantkortingen</span><span class="sxs-lookup"><span data-stu-id="1e0dd-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="1e0dd-122">Stel als volgt drie contantkortingscodes in:</span><span class="sxs-lookup"><span data-stu-id="1e0dd-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="1e0dd-123">Code 5D10%: er wordt een contantkorting van 10% gegeven als de factuur binnen 5 dagen wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="1e0dd-124">Code 10D5%: er wordt een contantkorting van 5% gegeven als de factuur binnen 10 dagen wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="1e0dd-125">Code 14D2%: er wordt een contantkorting van 2% gegeven als de factuur binnen 14 dagen wordt betaald.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="1e0dd-126">In het veld Volgende kortingscode:</span><span class="sxs-lookup"><span data-stu-id="1e0dd-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="1e0dd-127">10D5% voor de code 5D10%.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="1e0dd-128">14D2% voor de code 10D5%.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="1e0dd-129">Voor de code 14D2% laat u het veld Volgende kortingscode leeg.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="1e0dd-130">De drie contantkortingen volgen elkaar op wanneer de betaaldatum de vorige contantkortingsdatum op de factuur overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="1e0dd-131">Slechts één contantkorting wordt toegekend wanneer de factuur wordt betaald, afhankelijk van welke contantkorting aan bod is in de reeks kortingen.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="1e0dd-132">Voorbeeld: wisselkoersen voor contantkortingen</span><span class="sxs-lookup"><span data-stu-id="1e0dd-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="1e0dd-133">De valuta voor boekhouding van de rechtspersoon is EUR en de volgende wisselkoersen zijn opgegeven voor USD:</span><span class="sxs-lookup"><span data-stu-id="1e0dd-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="1e0dd-134">1 februari = 110</span><span class="sxs-lookup"><span data-stu-id="1e0dd-134">February 1 = 110</span></span>
-   <span data-ttu-id="1e0dd-135">1 maart = 80</span><span class="sxs-lookup"><span data-stu-id="1e0dd-135">March 1 = 80</span></span>

<span data-ttu-id="1e0dd-136">Op 15 februari wordt een factuur geboekt voor 1000 USD met contantkortingsvoorwaarden van 20D2%.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="1e0dd-137">Het factuurbedrag in de valuta voor boekhouding is 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="1e0dd-138">Een betaling van 980 USD wordt vereffend met de factuur op 1 maart.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="1e0dd-139">Het bedrag van de contantkorting is 20 USD.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="1e0dd-140">Het bedrag van de betaling in de valuta voor boekhouding is 784 EUR.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="1e0dd-141">Het bedrag van de contantkorting in de valuta voor boekhouding wordt berekend op basis van de wisselkoers op 1 maart: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="1e0dd-142">Als de optie Contantkortingen berekenen voor gedeeltelijke betalingen is geselecteerd op de pagina's Parameters van module Klanten of Parameters van module Leveranciers, wordt de wisselkoers gebruikt die geldt op de datum van elke deelbetaling.</span><span class="sxs-lookup"><span data-stu-id="1e0dd-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 


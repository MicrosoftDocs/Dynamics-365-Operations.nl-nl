---
title: Btw-specificatie per grootboektransactie (rapport)
description: In dit onderwerp wordt uitgelegd hoe u het rapport btw-specificatie per grootboektransactie kunt gebruiken om informatie weer te geven en af te drukken over grootboektransacties waarvoor btw wordt berekend.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815255"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="9d48a-103">Btw-specificatie per grootboektransactie (rapport)</span><span class="sxs-lookup"><span data-stu-id="9d48a-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d48a-104">In dit onderwerp wordt uitgelegd hoe u het rapport **Btw-specificatie per grootboektransactie** kunt gebruiken om informatie weer te geven en af te drukken over grootboektransacties waarvoor btw wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="9d48a-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="9d48a-105">Btw-rekeningen versus niet-btw-rekeningen</span><span class="sxs-lookup"><span data-stu-id="9d48a-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="9d48a-106">In het rapport **Btw-specificatie per grootboektransactie** worden btw-transacties weergegeven voor zowel btw-rekeningen als niet-btw-rekeningen.</span><span class="sxs-lookup"><span data-stu-id="9d48a-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="9d48a-107">Deze rekeningen worden op de volgende manier ingedeeld:</span><span class="sxs-lookup"><span data-stu-id="9d48a-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="9d48a-108">**Belasting rekening** – een rekening wordt gezien als een belastingrekening wanneer een btw-transactie wordt geboekt, en de hoofdrekening op de **Btw**-journaal regel een btw-rekening is, zoals een rekening voor verschuldigde btw of een rekening voor te ontvangen btw.</span><span class="sxs-lookup"><span data-stu-id="9d48a-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="9d48a-109">**Niet-belasting rekening** – een rekening wordt gezien als een niet-belastingrekening wanneer een btw-transactie wordt geboekt, en de hoofdrekening op de originele transactie niet-belastingrekening is, zoals een rekening voor inkomstenrekening of een uitgavenrekening.</span><span class="sxs-lookup"><span data-stu-id="9d48a-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="9d48a-110">Voor btw-rekeningen worden de kolommen **Oorsprong**, **Te ontvangen btw** en **Verschuldigde btw** in het rapport weergegeven met **0** (nul).</span><span class="sxs-lookup"><span data-stu-id="9d48a-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="9d48a-111">Voor niet-belastingrekeningen bevatten deze kolommen bedragen.</span><span class="sxs-lookup"><span data-stu-id="9d48a-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="9d48a-112">De gegevens in het rapport filteren</span><span class="sxs-lookup"><span data-stu-id="9d48a-112">Filtering the data on the report</span></span>

<span data-ttu-id="9d48a-113">Wanneer u dit rapport genereert, zijn de volgende standaardvelden beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9d48a-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="9d48a-114">U kunt deze velden gebruiken om de gegevens te filteren die in het rapport worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9d48a-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="9d48a-115">Veld</span><span class="sxs-lookup"><span data-stu-id="9d48a-115">Field</span></span>                      | <span data-ttu-id="9d48a-116">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9d48a-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="9d48a-117">Datum</span><span class="sxs-lookup"><span data-stu-id="9d48a-117">Date</span></span>                       | <span data-ttu-id="9d48a-118">Gebruik de velden in de secties **Van** en **Naar** om een datumbereik voor de btw-transacties te definiëren.</span><span class="sxs-lookup"><span data-stu-id="9d48a-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="9d48a-119">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="9d48a-119">Main account</span></span>               | <span data-ttu-id="9d48a-120">Gebruik de velden in de secties **Van** en **Naar** om een datumbereik voor de hoofdrekeningen te definiëren.</span><span class="sxs-lookup"><span data-stu-id="9d48a-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="9d48a-121">Btw-code</span><span class="sxs-lookup"><span data-stu-id="9d48a-121">Sales tax code</span></span>             | <span data-ttu-id="9d48a-122">Gebruik de velden in de secties **Van** en **Naar** om een datumbereik voor btw-codes te definiëren.</span><span class="sxs-lookup"><span data-stu-id="9d48a-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="9d48a-123">Groepering</span><span class="sxs-lookup"><span data-stu-id="9d48a-123">Grouping</span></span>                   | <span data-ttu-id="9d48a-124">Selecteer of het rapport moet worden gegroepeerd op grootboekrekening of btw-code.</span><span class="sxs-lookup"><span data-stu-id="9d48a-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="9d48a-125">Subtotaal per btw-code</span><span class="sxs-lookup"><span data-stu-id="9d48a-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="9d48a-126">Stel deze optie in op **Ja** als u subtotalen per btw-code wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="9d48a-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="9d48a-127">Alleen totalen</span><span class="sxs-lookup"><span data-stu-id="9d48a-127">Totals only</span></span>                | <span data-ttu-id="9d48a-128">Stel deze optie in op **Ja** als u alleen totalen wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="9d48a-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="9d48a-129">Alleen hoofdrekeningen</span><span class="sxs-lookup"><span data-stu-id="9d48a-129">Main accounts only</span></span>         | <span data-ttu-id="9d48a-130">Stel deze optie in op **Ja** als u alleen de hoofdrekeningen in het rapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="9d48a-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="9d48a-131">Alleen niet-btw-rekeningen weergeven in het rapport</span><span class="sxs-lookup"><span data-stu-id="9d48a-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="9d48a-132">Als u alleen niet-btw-rekeningen wilt weergeven in het rapport, stelt u een filtervoorwaarde in, zoals een asterisk (\*), zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="9d48a-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Rapport met niet-belastingrekeningen](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
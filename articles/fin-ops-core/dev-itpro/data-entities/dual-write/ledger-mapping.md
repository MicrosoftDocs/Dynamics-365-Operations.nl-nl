---
title: Geïntegreerd grootboek
description: In dit onderwerp wordt de integratie van grootboekgegevens tussen Finance and Operations en andere Dynamics 365-toepassingen via Common Data Service beschreven.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6f1a1c7329f0936147fb8f7a8e0e9fea14f7dd4b
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173010"
---
# <a name="integrated-ledger"></a><span data-ttu-id="50cff-103">Geïntegreerd grootboek</span><span class="sxs-lookup"><span data-stu-id="50cff-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="50cff-104">In een bedrijfstoepassing definiëren grootboekgegevens de basisinstelling van de manier waarop een bedrijf zaken doet.</span><span class="sxs-lookup"><span data-stu-id="50cff-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="50cff-105">Zo beschreven grootboekgegevens bijvoorbeeld het fiscaal jaar dat het bedrijf volgt, de valuta's waarin het bedrijf handelt en de rekeningen die worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="50cff-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="50cff-106">In dit onderwerp wordt de integratie van deze financiële kerngegevens beschreven.</span><span class="sxs-lookup"><span data-stu-id="50cff-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="50cff-107">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="50cff-107">Templates</span></span>

<span data-ttu-id="50cff-108">Grootboekgegevens omvatten een verzameling financiële basisentiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="50cff-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="50cff-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="50cff-109">Finance and Operations apps</span></span>      | <span data-ttu-id="50cff-110">Modelgestuurde app in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="50cff-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="50cff-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="50cff-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="50cff-112">Valuta's</span><span class="sxs-lookup"><span data-stu-id="50cff-112">Currencies</span></span>                       | <span data-ttu-id="50cff-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="50cff-113">transactioncurrencies</span></span>            |
<span data-ttu-id="50cff-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="50cff-114">FiscalCalendar</span></span>                   | <span data-ttu-id="50cff-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="50cff-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="50cff-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="50cff-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="50cff-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="50cff-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="50cff-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="50cff-118">ExchRateType</span></span>                     | <span data-ttu-id="50cff-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="50cff-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="50cff-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="50cff-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="50cff-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="50cff-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="50cff-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="50cff-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="50cff-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="50cff-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="50cff-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="50cff-124">MainAccountCategory</span></span>              | <span data-ttu-id="50cff-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="50cff-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="50cff-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="50cff-126">MainAccount</span></span>                      | <span data-ttu-id="50cff-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="50cff-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="50cff-128">Grootboek</span><span class="sxs-lookup"><span data-stu-id="50cff-128">Ledger</span></span>                           | <span data-ttu-id="50cff-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="50cff-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="50cff-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="50cff-130">ExchangeRates</span></span>                    | <span data-ttu-id="50cff-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="50cff-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="50cff-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="50cff-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="50cff-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="50cff-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="50cff-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="50cff-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="50cff-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="50cff-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="50cff-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="50cff-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="50cff-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="50cff-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="50cff-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="50cff-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="50cff-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="50cff-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]





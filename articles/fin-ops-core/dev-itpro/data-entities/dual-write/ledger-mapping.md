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
ms.openlocfilehash: 6bf1c554f56c1424da9fde98f67f80a6b7c95461
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019719"
---
# <a name="integrated-ledger"></a><span data-ttu-id="353c4-103">Geïntegreerd grootboek</span><span class="sxs-lookup"><span data-stu-id="353c4-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="353c4-104">In een bedrijfstoepassing definiëren grootboekgegevens de basisinstelling van de manier waarop een bedrijf zaken doet.</span><span class="sxs-lookup"><span data-stu-id="353c4-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="353c4-105">Zo beschreven grootboekgegevens bijvoorbeeld het fiscaal jaar dat het bedrijf volgt, de valuta's waarin het bedrijf handelt en de rekeningen die worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="353c4-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="353c4-106">In dit onderwerp wordt de integratie van deze financiële kerngegevens beschreven.</span><span class="sxs-lookup"><span data-stu-id="353c4-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="353c4-107">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="353c4-107">Templates</span></span>

<span data-ttu-id="353c4-108">Grootboekgegevens omvatten een verzameling financiële basisentiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="353c4-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="353c4-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="353c4-109">Finance and Operations apps</span></span>      | <span data-ttu-id="353c4-110">Andere Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="353c4-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="353c4-111">Valuta's</span><span class="sxs-lookup"><span data-stu-id="353c4-111">Currencies</span></span>                       | <span data-ttu-id="353c4-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="353c4-112">transactioncurrencies</span></span>
<span data-ttu-id="353c4-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="353c4-113">FiscalCalendar</span></span>                   | <span data-ttu-id="353c4-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="353c4-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="353c4-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="353c4-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="353c4-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="353c4-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="353c4-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="353c4-117">ExchRateType</span></span>                     | <span data-ttu-id="353c4-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="353c4-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="353c4-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="353c4-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="353c4-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="353c4-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="353c4-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="353c4-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="353c4-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="353c4-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="353c4-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="353c4-123">MainAccountCategory</span></span>              | <span data-ttu-id="353c4-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="353c4-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="353c4-125">MainAccount</span><span class="sxs-lookup"><span data-stu-id="353c4-125">MainAccount</span></span>                      | <span data-ttu-id="353c4-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="353c4-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="353c4-127">Grootboek</span><span class="sxs-lookup"><span data-stu-id="353c4-127">Ledger</span></span>                           | <span data-ttu-id="353c4-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="353c4-128">msdyn\_ledgers</span></span>
<span data-ttu-id="353c4-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="353c4-129">ExchangeRates</span></span>                    | <span data-ttu-id="353c4-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="353c4-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="353c4-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="353c4-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="353c4-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="353c4-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="353c4-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="353c4-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="353c4-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="353c4-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="353c4-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="353c4-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="353c4-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="353c4-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="353c4-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="353c4-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="353c4-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="353c4-138">msdyn\_chartofaccounts.md</span></span>


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





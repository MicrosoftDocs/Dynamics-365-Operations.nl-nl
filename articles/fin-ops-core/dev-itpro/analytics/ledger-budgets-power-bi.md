---
title: Werkelijk vs. budget Power BI-inhoud
description: In dit onderwerp wordt de Power BI-inhoud Werkelijk vs. budget besproken. Er wordt uitgelegd hoe u de rapporten kunt openen en u vindt informatie over het gegevensmodel.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568568"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="fe09d-104">Werkelijk vs. budget Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="fe09d-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe09d-105">In dit onderwerp wordt de Microsoft Power BI-inhoud **Werkelijk vs. budget** besproken.</span><span class="sxs-lookup"><span data-stu-id="fe09d-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="fe09d-106">U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="fe09d-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="fe09d-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="fe09d-107">Overview</span></span>

<span data-ttu-id="fe09d-108">De Power BI-inhoud **Werkelijk vs. budget** is gemaakt voor personen die verantwoordelijk zijn voor het controleren van werkelijke versus budget-prestaties in hun organisatie.</span><span class="sxs-lookup"><span data-stu-id="fe09d-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="fe09d-109">De Power BI-inhoud **Werkelijk vs. budget** biedt inzicht in uw budgetafwijkingen.</span><span class="sxs-lookup"><span data-stu-id="fe09d-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="fe09d-110">U kunt het budget voor het huidige jaar analyseren op rekeningcategorie, budgetcode, hoofdrekening, omschrijvingen van hoofdrekeningen of boekperiode, om beter inzicht te verkrijgen in de oorzaken van eventuele afwijkingen.</span><span class="sxs-lookup"><span data-stu-id="fe09d-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="fe09d-111">Toegang tot de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="fe09d-111">Accessing the Power BI content</span></span>
<span data-ttu-id="fe09d-112">Rapporten uit de Power BI-inhoud **Werkelijk vs. budget** worden weergegeven in de werkgebieden **Grootboekbudgetten en prognoses** en **CFO**.</span><span class="sxs-lookup"><span data-stu-id="fe09d-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="fe09d-113">Rapporten die zijn opgenomen in de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="fe09d-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="fe09d-114">De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud **Werkelijk vs. budget**.</span><span class="sxs-lookup"><span data-stu-id="fe09d-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="fe09d-115">Rapport</span><span class="sxs-lookup"><span data-stu-id="fe09d-115">Report</span></span>                      | <span data-ttu-id="fe09d-116">Metrische gegevens</span><span class="sxs-lookup"><span data-stu-id="fe09d-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe09d-117">Onkosten - werkelijk versus gebudgetteerd</span><span class="sxs-lookup"><span data-stu-id="fe09d-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="fe09d-118">Totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="fe09d-118">Total expenses this year</span></span></li><li><span data-ttu-id="fe09d-119">Gebudgetteerde totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="fe09d-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="fe09d-120">Opbrengst - werkelijk versus gebudgetteerd</span><span class="sxs-lookup"><span data-stu-id="fe09d-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="fe09d-121">Totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="fe09d-121">Total revenue this year</span></span></li><li><span data-ttu-id="fe09d-122">Gebudgetteerde totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="fe09d-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="fe09d-123">Uitgaven</span><span class="sxs-lookup"><span data-stu-id="fe09d-123">Expense</span></span>                     | <ul><li><span data-ttu-id="fe09d-124">Totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="fe09d-124">Total expenses this year</span></span></li><li><span data-ttu-id="fe09d-125">Doel voor onkosten op basis van budget</span><span class="sxs-lookup"><span data-stu-id="fe09d-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="fe09d-126">Opbrengst</span><span class="sxs-lookup"><span data-stu-id="fe09d-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="fe09d-127">Totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="fe09d-127">Total revenue this year</span></span></li><li><span data-ttu-id="fe09d-128">Doel voor omzet op basis van budget</span><span class="sxs-lookup"><span data-stu-id="fe09d-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="fe09d-129">Netto-inkomsten</span><span class="sxs-lookup"><span data-stu-id="fe09d-129">Net income</span></span>                  | <ul><li><span data-ttu-id="fe09d-130">Netto-inkomsten dit jaar</span><span class="sxs-lookup"><span data-stu-id="fe09d-130">Net income this year</span></span></li><li><span data-ttu-id="fe09d-131">Doel voor netto-inkomsten op basis van budget</span><span class="sxs-lookup"><span data-stu-id="fe09d-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="fe09d-132">Het gegevensmodel en de gegevensentiteiten begrijpen</span><span class="sxs-lookup"><span data-stu-id="fe09d-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="fe09d-133">Entiteit</span><span class="sxs-lookup"><span data-stu-id="fe09d-133">Entity</span></span>                    | <span data-ttu-id="fe09d-134">Inhoud</span><span class="sxs-lookup"><span data-stu-id="fe09d-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fe09d-135">Grootboekactiviteiten</span><span class="sxs-lookup"><span data-stu-id="fe09d-135">General Ledger Activities</span></span> | <span data-ttu-id="fe09d-136">Transactiebedragen voor het grootboek</span><span class="sxs-lookup"><span data-stu-id="fe09d-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="fe09d-137">Budgetactiviteiten</span><span class="sxs-lookup"><span data-stu-id="fe09d-137">Budget Activities</span></span>         | <span data-ttu-id="fe09d-138">Transactiebedragen voor het budgetregister</span><span class="sxs-lookup"><span data-stu-id="fe09d-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="fe09d-139">Hoofdrekeningen</span><span class="sxs-lookup"><span data-stu-id="fe09d-139">Main Accounts</span></span>             | <span data-ttu-id="fe09d-140">Hoofdrekeningen om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="fe09d-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="fe09d-141">Fiscale kalenders</span><span class="sxs-lookup"><span data-stu-id="fe09d-141">Fiscal Calendars</span></span>          | <span data-ttu-id="fe09d-142">Fiscale kalenders om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="fe09d-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="fe09d-143">Grootboeken</span><span class="sxs-lookup"><span data-stu-id="fe09d-143">Ledgers</span></span>                   | <span data-ttu-id="fe09d-144">Grootboeken die kunnen worden gebruikt om het rapport te filteren naar het huidige grootboek</span><span class="sxs-lookup"><span data-stu-id="fe09d-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="fe09d-145">Budgetcodes</span><span class="sxs-lookup"><span data-stu-id="fe09d-145">Budget Codes</span></span>              | <span data-ttu-id="fe09d-146">Budgetcodes om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="fe09d-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="fe09d-147">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="fe09d-147">Legal Entities</span></span>            | <span data-ttu-id="fe09d-148">Rechtspersonen die kunnen worden gebruikt om het rapport te filteren naar de huidige rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="fe09d-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
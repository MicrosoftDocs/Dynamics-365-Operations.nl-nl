---
title: Werkelijk vs. budget Power BI-inhoud
description: In dit onderwerp wordt de Power BI-inhoud Werkelijk vs. budget besproken. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten die zijn opgenomen in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c801544e9e37a528203f5a1730aa8cb526d63dbf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553733"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="75e4c-104">Werkelijk vs. budget Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="75e4c-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75e4c-105">In dit onderwerp wordt de Power BI-inhoud **Werkelijk vs. budget** besproken.</span><span class="sxs-lookup"><span data-stu-id="75e4c-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="75e4c-106">U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="75e4c-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="75e4c-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="75e4c-107">Overview</span></span>

<span data-ttu-id="75e4c-108">De Power BI-inhoud **Werkelijk vs. budget** is gemaakt voor personen die verantwoordelijk zijn voor het controleren van werkelijke versus budget-prestaties in hun organisatie.</span><span class="sxs-lookup"><span data-stu-id="75e4c-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="75e4c-109">De Power BI-inhoud **Werkelijk vs. budget** biedt inzicht in uw budgetafwijkingen.</span><span class="sxs-lookup"><span data-stu-id="75e4c-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="75e4c-110">U kunt het budget voor het huidige jaar analyseren op rekeningcategorie, budgetcode, hoofdrekening, omschrijvingen van hoofdrekeningen of boekperiode, om beter inzicht te verkrijgen in de oorzaken van eventuele afwijkingen.</span><span class="sxs-lookup"><span data-stu-id="75e4c-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="75e4c-111">Toegang tot de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="75e4c-111">Accessing the Power BI content</span></span>
<span data-ttu-id="75e4c-112">Rapporten uit de Power BI-inhoud **Werkelijk vs. budget** worden weergegeven in de werkgebieden **Grootboekbudgetten en prognoses** en **CFO**.</span><span class="sxs-lookup"><span data-stu-id="75e4c-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="75e4c-113">Rapporten die zijn opgenomen in de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="75e4c-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="75e4c-114">De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud **Werkelijk vs. budget**.</span><span class="sxs-lookup"><span data-stu-id="75e4c-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="75e4c-115">Rapport</span><span class="sxs-lookup"><span data-stu-id="75e4c-115">Report</span></span>                      | <span data-ttu-id="75e4c-116">Metrische gegevens</span><span class="sxs-lookup"><span data-stu-id="75e4c-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="75e4c-117">Onkosten - werkelijk versus gebudgetteerd</span><span class="sxs-lookup"><span data-stu-id="75e4c-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="75e4c-118">Totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="75e4c-118">Total expenses this year</span></span></li><li><span data-ttu-id="75e4c-119">Gebudgetteerde totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="75e4c-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="75e4c-120">Opbrengst - werkelijk versus gebudgetteerd</span><span class="sxs-lookup"><span data-stu-id="75e4c-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="75e4c-121">Totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="75e4c-121">Total revenue this year</span></span></li><li><span data-ttu-id="75e4c-122">Gebudgetteerde totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="75e4c-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="75e4c-123">Uitgaven</span><span class="sxs-lookup"><span data-stu-id="75e4c-123">Expense</span></span>                     | <ul><li><span data-ttu-id="75e4c-124">Totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="75e4c-124">Total expenses this year</span></span></li><li><span data-ttu-id="75e4c-125">Doel voor onkosten op basis van budget</span><span class="sxs-lookup"><span data-stu-id="75e4c-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="75e4c-126">Opbrengst</span><span class="sxs-lookup"><span data-stu-id="75e4c-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="75e4c-127">Totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="75e4c-127">Total revenue this year</span></span></li><li><span data-ttu-id="75e4c-128">Doel voor omzet op basis van budget</span><span class="sxs-lookup"><span data-stu-id="75e4c-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="75e4c-129">Netto-inkomsten</span><span class="sxs-lookup"><span data-stu-id="75e4c-129">Net income</span></span>                  | <ul><li><span data-ttu-id="75e4c-130">Netto-inkomsten dit jaar</span><span class="sxs-lookup"><span data-stu-id="75e4c-130">Net income this year</span></span></li><li><span data-ttu-id="75e4c-131">Doel voor netto-inkomsten op basis van budget</span><span class="sxs-lookup"><span data-stu-id="75e4c-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="75e4c-132">Het gegevensmodel en de gegevensentiteiten begrijpen</span><span class="sxs-lookup"><span data-stu-id="75e4c-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="75e4c-133">Entiteit</span><span class="sxs-lookup"><span data-stu-id="75e4c-133">Entity</span></span>                    | <span data-ttu-id="75e4c-134">Inhoud</span><span class="sxs-lookup"><span data-stu-id="75e4c-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75e4c-135">Grootboekactiviteiten</span><span class="sxs-lookup"><span data-stu-id="75e4c-135">General Ledger Activities</span></span> | <span data-ttu-id="75e4c-136">Transactiebedragen voor het grootboek</span><span class="sxs-lookup"><span data-stu-id="75e4c-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="75e4c-137">Budgetactiviteiten</span><span class="sxs-lookup"><span data-stu-id="75e4c-137">Budget Activities</span></span>         | <span data-ttu-id="75e4c-138">Transactiebedragen voor het budgetregister</span><span class="sxs-lookup"><span data-stu-id="75e4c-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="75e4c-139">Hoofdrekeningen</span><span class="sxs-lookup"><span data-stu-id="75e4c-139">Main Accounts</span></span>             | <span data-ttu-id="75e4c-140">Hoofdrekeningen om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="75e4c-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="75e4c-141">Fiscale kalenders</span><span class="sxs-lookup"><span data-stu-id="75e4c-141">Fiscal Calendars</span></span>          | <span data-ttu-id="75e4c-142">Fiscale kalenders om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="75e4c-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="75e4c-143">Grootboeken</span><span class="sxs-lookup"><span data-stu-id="75e4c-143">Ledgers</span></span>                   | <span data-ttu-id="75e4c-144">Grootboeken die kunnen worden gebruikt om het rapport te filteren naar het huidige grootboek</span><span class="sxs-lookup"><span data-stu-id="75e4c-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="75e4c-145">Budgetcodes</span><span class="sxs-lookup"><span data-stu-id="75e4c-145">Budget Codes</span></span>              | <span data-ttu-id="75e4c-146">Budgetcodes om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="75e4c-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="75e4c-147">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="75e4c-147">Legal Entities</span></span>            | <span data-ttu-id="75e4c-148">Rechtspersonen die kunnen worden gebruikt om het rapport te filteren naar de huidige rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="75e4c-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |

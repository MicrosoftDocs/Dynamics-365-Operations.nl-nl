---
title: Power BI-inhoud Werkelijk vs. budget
description: In dit onderwerp wordt de Power BI-inhoud Werkelijk vs. budget besproken. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten die zijn opgenomen in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: afa8e07505283531c97663f35b208d82d69d2b42
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="bee27-104">Power BI-inhoud Werkelijk vs. budget</span><span class="sxs-lookup"><span data-stu-id="bee27-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bee27-105">In dit onderwerp wordt de Microsoft Power BI-inhoud **Werkelijk vs. budget** besproken.</span><span class="sxs-lookup"><span data-stu-id="bee27-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="bee27-106">U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="bee27-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="bee27-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="bee27-107">Overview</span></span>

<span data-ttu-id="bee27-108">De Power BI-inhoud **Werkelijk vs. budget** is gemaakt voor personen die verantwoordelijk zijn voor het controleren van werkelijke versus budget-prestaties in hun organisatie.</span><span class="sxs-lookup"><span data-stu-id="bee27-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="bee27-109">De Power BI-inhoud **Werkelijk vs. budget** biedt inzicht in uw budgetafwijkingen.</span><span class="sxs-lookup"><span data-stu-id="bee27-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="bee27-110">U kunt het budget voor het huidige jaar analyseren op rekeningcategorie, budgetcode, hoofdrekening, omschrijvingen van hoofdrekeningen of boekperiode, om beter inzicht te verkrijgen in de oorzaken van eventuele afwijkingen.</span><span class="sxs-lookup"><span data-stu-id="bee27-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="bee27-111">Toegang tot de Power BI-inhoud verkrijgen</span><span class="sxs-lookup"><span data-stu-id="bee27-111">Accessing the Power BI content</span></span>
<span data-ttu-id="bee27-112">Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), vindt u de rapporten uit de Power BI-inhoud **Werkelijk vs. budget** in de werkgebieden **Grootboekbudgetten en prognoses** en **CFO**.</span><span class="sxs-lookup"><span data-stu-id="bee27-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="bee27-113">Rapporten die zijn opgenomen in de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="bee27-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="bee27-114">De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud **Werkelijk vs. budget**.</span><span class="sxs-lookup"><span data-stu-id="bee27-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="bee27-115">Rapport</span><span class="sxs-lookup"><span data-stu-id="bee27-115">Report</span></span>                      | <span data-ttu-id="bee27-116">Metrische gegevens</span><span class="sxs-lookup"><span data-stu-id="bee27-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="bee27-117">Onkosten - werkelijk versus gebudgetteerd</span><span class="sxs-lookup"><span data-stu-id="bee27-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="bee27-118">Totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="bee27-118">Total expenses this year</span></span></li><li><span data-ttu-id="bee27-119">Gebudgetteerde totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="bee27-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="bee27-120">Opbrengst - werkelijk versus gebudgetteerd</span><span class="sxs-lookup"><span data-stu-id="bee27-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="bee27-121">Totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="bee27-121">Total revenue this year</span></span></li><li><span data-ttu-id="bee27-122">Gebudgetteerde totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="bee27-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="bee27-123">Uitgaven</span><span class="sxs-lookup"><span data-stu-id="bee27-123">Expense</span></span>                     | <ul><li><span data-ttu-id="bee27-124">Totale kosten dit jaar</span><span class="sxs-lookup"><span data-stu-id="bee27-124">Total expenses this year</span></span></li><li><span data-ttu-id="bee27-125">Doel voor onkosten op basis van budget</span><span class="sxs-lookup"><span data-stu-id="bee27-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="bee27-126">Opbrengst</span><span class="sxs-lookup"><span data-stu-id="bee27-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="bee27-127">Totale omzet dit jaar</span><span class="sxs-lookup"><span data-stu-id="bee27-127">Total revenue this year</span></span></li><li><span data-ttu-id="bee27-128">Doel voor omzet op basis van budget</span><span class="sxs-lookup"><span data-stu-id="bee27-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="bee27-129">Netto-inkomsten</span><span class="sxs-lookup"><span data-stu-id="bee27-129">Net income</span></span>                  | <ul><li><span data-ttu-id="bee27-130">Netto-inkomsten dit jaar</span><span class="sxs-lookup"><span data-stu-id="bee27-130">Net income this year</span></span></li><li><span data-ttu-id="bee27-131">Doel voor netto-inkomsten op basis van budget</span><span class="sxs-lookup"><span data-stu-id="bee27-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="bee27-132">De Power BI-inhoud uitbreiden</span><span class="sxs-lookup"><span data-stu-id="bee27-132">Extending the Power BI content</span></span>
<span data-ttu-id="bee27-133">Met behulp van de inhoudpakketten die beschikbaar zijn in Microsoft Dynamics Lifecycle Services (LCS) kunt u grondige analyses verschaffen aan personen die zich niet bij Microsoft Dynamics 365 aanmelden.</span><span class="sxs-lookup"><span data-stu-id="bee27-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="bee27-134">U kunt deze inhoudpakketten wijzigen zodat ze andere rapporten of visuele elementen bevatten, en de inhoudpakketten vervolgens publiceren naar uw Power BI.com-tenant voor analyse.</span><span class="sxs-lookup"><span data-stu-id="bee27-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="bee27-135">U vindt de Power BI-inhoud **Werkelijk vs. budget** in de bibliotheek voor gedeelde materialen in LCS.</span><span class="sxs-lookup"><span data-stu-id="bee27-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="bee27-136">Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="bee27-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="bee27-137">Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="bee27-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="bee27-138">Het gegevensmodel en de gegevensentiteiten begrijpen</span><span class="sxs-lookup"><span data-stu-id="bee27-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="bee27-139">Entiteit</span><span class="sxs-lookup"><span data-stu-id="bee27-139">Entity</span></span>                    | <span data-ttu-id="bee27-140">Inhoud</span><span class="sxs-lookup"><span data-stu-id="bee27-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="bee27-141">Grootboekactiviteiten</span><span class="sxs-lookup"><span data-stu-id="bee27-141">General Ledger Activities</span></span> | <span data-ttu-id="bee27-142">Transactiebedragen voor het grootboek</span><span class="sxs-lookup"><span data-stu-id="bee27-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="bee27-143">Budgetactiviteiten</span><span class="sxs-lookup"><span data-stu-id="bee27-143">Budget Activities</span></span>         | <span data-ttu-id="bee27-144">Transactiebedragen voor het budgetregister</span><span class="sxs-lookup"><span data-stu-id="bee27-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="bee27-145">Hoofdrekeningen</span><span class="sxs-lookup"><span data-stu-id="bee27-145">Main Accounts</span></span>             | <span data-ttu-id="bee27-146">Hoofdrekeningen om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="bee27-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="bee27-147">Fiscale kalenders</span><span class="sxs-lookup"><span data-stu-id="bee27-147">Fiscal Calendars</span></span>          | <span data-ttu-id="bee27-148">Fiscale kalenders om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="bee27-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="bee27-149">Grootboeken</span><span class="sxs-lookup"><span data-stu-id="bee27-149">Ledgers</span></span>                   | <span data-ttu-id="bee27-150">Grootboeken die kunnen worden gebruikt om het rapport te filteren naar het huidige grootboek</span><span class="sxs-lookup"><span data-stu-id="bee27-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="bee27-151">Budgetcodes</span><span class="sxs-lookup"><span data-stu-id="bee27-151">Budget Codes</span></span>              | <span data-ttu-id="bee27-152">Budgetcodes om rapporten op te filteren</span><span class="sxs-lookup"><span data-stu-id="bee27-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="bee27-153">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="bee27-153">Legal Entities</span></span>            | <span data-ttu-id="bee27-154">Rechtspersonen die kunnen worden gebruikt om het rapport te filteren naar de huidige rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="bee27-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |


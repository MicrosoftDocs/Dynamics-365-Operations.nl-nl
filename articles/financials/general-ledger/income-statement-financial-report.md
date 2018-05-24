---
title: Financieel rapport inkomensoverzicht
description: In dit artikel wordt het standaardrapport voor inkomensoverzichten beschreven. In dit artikel worden ook de bouwstenen beschreven die aan dit rapport zijn gekoppeld.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9310508082ff710cd040b74519044f5a90c23988
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="098a3-104">Financieel rapport inkomensoverzicht</span><span class="sxs-lookup"><span data-stu-id="098a3-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="098a3-105">In dit artikel wordt het standaardrapport voor inkomensoverzichten beschreven.</span><span class="sxs-lookup"><span data-stu-id="098a3-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="098a3-106">In dit artikel worden ook de bouwstenen beschreven die aan dit rapport zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="098a3-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="098a3-107">Standaardrapport inkomensoverzicht</span><span class="sxs-lookup"><span data-stu-id="098a3-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="098a3-108">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="098a3-108">Default report</span></span>             | <span data-ttu-id="098a3-109">Functie</span><span class="sxs-lookup"><span data-stu-id="098a3-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="098a3-110">Inkomensoverzicht – Standaard</span><span class="sxs-lookup"><span data-stu-id="098a3-110">Income Statement – Default</span></span> | <span data-ttu-id="098a3-111">Biedt een weergave van de winstgevendheid van de organisatie voor de huidige periode en ook voor het jaar tot heden.</span><span class="sxs-lookup"><span data-stu-id="098a3-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="098a3-112">Bouwstenen</span><span class="sxs-lookup"><span data-stu-id="098a3-112">Building blocks</span></span>
<span data-ttu-id="098a3-113">In het financiële rapport van het inkomensoverzicht worden de volgende bouwstenen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="098a3-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="098a3-114">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="098a3-114">Default report</span></span>             | <span data-ttu-id="098a3-115">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="098a3-115">Row definition</span></span>                     | <span data-ttu-id="098a3-116">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="098a3-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="098a3-117">Inkomensoverzicht: standaard</span><span class="sxs-lookup"><span data-stu-id="098a3-117">Income Statement - Default</span></span> | <span data-ttu-id="098a3-118">Samengevat inkomensoverzicht: standaard</span><span class="sxs-lookup"><span data-stu-id="098a3-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="098a3-119">Periodiek en jaar tot heden: standaard</span><span class="sxs-lookup"><span data-stu-id="098a3-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="098a3-120">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="098a3-120">Row definition</span></span>

<span data-ttu-id="098a3-121">De rijdefinitie, Samengevat inkomensoverzicht: standaard, bevat een sectie voor elk onderdeel van een traditioneel inkomensoverzicht.</span><span class="sxs-lookup"><span data-stu-id="098a3-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="098a3-122">De dimensie Categorie van hoofdrekening wordt gebruikt om deze rijdefinitie te maken.</span><span class="sxs-lookup"><span data-stu-id="098a3-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="098a3-123">Zo kan iedereen het rapport genereren zonder wijzigingen te hoeven aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="098a3-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="098a3-124">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="098a3-124">Column Definition</span></span>

<span data-ttu-id="098a3-125">De kolomdefinities bevatten verschillende typen kolommen om verschillende detailniveaus en financiële gegevens te verschaffen.</span><span class="sxs-lookup"><span data-stu-id="098a3-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="098a3-126">**Periodiek en jaar tot heden: standaardkolomtypen:**</span><span class="sxs-lookup"><span data-stu-id="098a3-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="098a3-127">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="098a3-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="098a3-128">**FD**: financiële gegevens voor de huidige periode</span><span class="sxs-lookup"><span data-stu-id="098a3-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="098a3-129">**FD**: financiële gegevens voor jaar tot heden</span><span class="sxs-lookup"><span data-stu-id="098a3-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="098a3-130">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="098a3-130">Additional resources</span></span>
--------

[<span data-ttu-id="098a3-131">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="098a3-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="098a3-132">Financiële rapporten weergeven</span><span class="sxs-lookup"><span data-stu-id="098a3-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="098a3-133">Blog met financiële rapportage van Dynamics</span><span class="sxs-lookup"><span data-stu-id="098a3-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)





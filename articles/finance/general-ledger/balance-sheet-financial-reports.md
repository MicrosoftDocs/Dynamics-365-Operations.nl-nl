---
title: Financiële rapporten balans
description: In dit artikel worden de standaardrapporten voor balansen beschreven. Hierin worden ook de bouwstenen beschreven die aan deze rapporten zijn gekoppeld.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177128"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="47bd5-104">Financiële rapporten balans</span><span class="sxs-lookup"><span data-stu-id="47bd5-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47bd5-105">In dit artikel worden de standaardrapporten voor balansen beschreven.</span><span class="sxs-lookup"><span data-stu-id="47bd5-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="47bd5-106">Hierin worden ook de bouwstenen beschreven die aan deze rapporten zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="47bd5-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="47bd5-107">Standaardbalansrapporten</span><span class="sxs-lookup"><span data-stu-id="47bd5-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="47bd5-108">Er zijn twee standaardbalansrapporten.</span><span class="sxs-lookup"><span data-stu-id="47bd5-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="47bd5-109">In één rapport zijn de secties gestapeld.</span><span class="sxs-lookup"><span data-stu-id="47bd5-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="47bd5-110">In het andere rapport worden de secties naast elkaar weergegeven.</span><span class="sxs-lookup"><span data-stu-id="47bd5-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="47bd5-111">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="47bd5-111">Default report</span></span>                       | <span data-ttu-id="47bd5-112">Functie</span><span class="sxs-lookup"><span data-stu-id="47bd5-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47bd5-113">Balans – Standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="47bd5-114">Bevat een weergave van de financiële positie van de organisatie voor het jaar.</span><span class="sxs-lookup"><span data-stu-id="47bd5-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="47bd5-115">Balans naast elkaar - Standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="47bd5-116">Bevat een weergave van de financiële positie van de organisatie voor het jaar.</span><span class="sxs-lookup"><span data-stu-id="47bd5-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="47bd5-117">Activa en passiva en het eigen vermogen van de aandeelhouder worden naast elkaar weergegeven.</span><span class="sxs-lookup"><span data-stu-id="47bd5-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="47bd5-118">Bouwstenen</span><span class="sxs-lookup"><span data-stu-id="47bd5-118">Building blocks</span></span>
<span data-ttu-id="47bd5-119">In de financiële rapporten van de balans worden de volgende bouwstenen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="47bd5-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="47bd5-120">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="47bd5-120">Default report</span></span>                       | <span data-ttu-id="47bd5-121">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="47bd5-121">Row definition</span></span>                       | <span data-ttu-id="47bd5-122">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="47bd5-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="47bd5-123">Balans: standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="47bd5-124">Balans: standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="47bd5-125">Jaar tot heden en afwijking: standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="47bd5-126">Balans naast elkaar - Standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="47bd5-127">Balans naast elkaar - Standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="47bd5-128">Kolom Jaar tot heden: standaard</span><span class="sxs-lookup"><span data-stu-id="47bd5-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="47bd5-129">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="47bd5-129">Row definition</span></span>

<span data-ttu-id="47bd5-130">De rijdefinities voor beide balansrapporten bevatten secties voor elk onderdeel van een traditionele balans.</span><span class="sxs-lookup"><span data-stu-id="47bd5-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="47bd5-131">Het rapport waarin secties naast elkaar worden weergegeven, bevat een kolomeinde, zodat de passiva en het eigen vermogen van de eigenaar naast activa worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="47bd5-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="47bd5-132">De dimensie Categorie van hoofdrekening wordt gebruikt om beide rijdefinities te maken.</span><span class="sxs-lookup"><span data-stu-id="47bd5-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="47bd5-133">Zo kan iedereen de rapporten genereren zonder wijzigingen te hoeven aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="47bd5-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="47bd5-134">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="47bd5-134">Column definition</span></span>

<span data-ttu-id="47bd5-135">De kolomdefinities bevatten verschillende typen kolommen om verschillende detailniveaus en financiële gegevens te verschaffen.</span><span class="sxs-lookup"><span data-stu-id="47bd5-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="47bd5-136">**Jaar tot heden en afwijking: standaardkolomtypen:**</span><span class="sxs-lookup"><span data-stu-id="47bd5-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="47bd5-137">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="47bd5-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="47bd5-138">**FD**: financiële gegevens voor jaar tot heden voor het huidige jaar</span><span class="sxs-lookup"><span data-stu-id="47bd5-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="47bd5-139">**FD**: financiële gegevens voor jaar tot heden voor het afgelopen jaar</span><span class="sxs-lookup"><span data-stu-id="47bd5-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="47bd5-140">**CALC**: de afwijking na aftrek van afgelopen jaar van dit jaar</span><span class="sxs-lookup"><span data-stu-id="47bd5-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="47bd5-141">**Kolom Jaar tot heden: standaard:**</span><span class="sxs-lookup"><span data-stu-id="47bd5-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="47bd5-142">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="47bd5-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="47bd5-143">**FD**: financiële gegevens voor jaar tot heden voor het huidige jaar</span><span class="sxs-lookup"><span data-stu-id="47bd5-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="47bd5-144">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="47bd5-144">Additional resources</span></span>
--------

[<span data-ttu-id="47bd5-145">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="47bd5-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="47bd5-146">Financiële rapporten weergeven</span><span class="sxs-lookup"><span data-stu-id="47bd5-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="47bd5-147">Blog met financiële rapportage van Dynamics</span><span class="sxs-lookup"><span data-stu-id="47bd5-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



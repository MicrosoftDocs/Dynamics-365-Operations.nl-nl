---
title: Winstgevendheid van klanten en producten beoordelen
description: In dit artikel wordt uitgelegd hoe u door middel van de real-time analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Microsoft Dynamics 365 for Retail en deze kunt onderzoeken en er kennis uit kunt destilleren.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 84a9e0b3936adcf2ed99fddca77dd57dfedeb050
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="b9c40-103">Winstgevendheid van klanten en producten beoordelen</span><span class="sxs-lookup"><span data-stu-id="b9c40-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b9c40-104">In dit artikel wordt uitgelegd hoe u door middel van de real-time analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Microsoft Dynamics 365 for Retail en deze kunt onderzoeken en er kennis uit kunt destilleren.</span><span class="sxs-lookup"><span data-stu-id="b9c40-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="b9c40-105">Als onderdeel van Dynamics 365 for Retail kunnen gebruikers winstgevendheid onderzoeken voor de beste klanten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="b9c40-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="b9c40-106">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="b9c40-106">Sales amount</span></span>
-   <span data-ttu-id="b9c40-107">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="b9c40-107">Quantity</span></span>
-   <span data-ttu-id="b9c40-108">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="b9c40-108">Gross profit margin</span></span>
-   <span data-ttu-id="b9c40-109">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="b9c40-109">Margin percentage</span></span>

<span data-ttu-id="b9c40-110">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste klanten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="b9c40-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="b9c40-111">Werkgebied **Beheer van detailhandelwinkel** &gt; **Retail** &gt; **Kanalen** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="b9c40-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="b9c40-112">Sectie **Query's en rapporten** &gt; **Retail** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="b9c40-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="b9c40-113">Zo kunnen gebruikers ook winstgevendheid onderzoeken van de beste producten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="b9c40-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="b9c40-114">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="b9c40-114">Sales amount</span></span>
-   <span data-ttu-id="b9c40-115">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="b9c40-115">Quantity</span></span>
-   <span data-ttu-id="b9c40-116">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="b9c40-116">Gross profit margin</span></span>
-   <span data-ttu-id="b9c40-117">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="b9c40-117">Margin percentage</span></span>

<span data-ttu-id="b9c40-118">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste producten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="b9c40-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="b9c40-119">Werkgebied **Beheer van detailhandelwinkel** &gt; **Retail** &gt; **Kanalen** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="b9c40-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="b9c40-120">Werkgebied **Categorie- en productbeheer** &gt; **Retail** &gt; **Producten en categorieën** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="b9c40-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="b9c40-121">Sectie **Query's en rapporten** &gt; **Retail** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="b9c40-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>





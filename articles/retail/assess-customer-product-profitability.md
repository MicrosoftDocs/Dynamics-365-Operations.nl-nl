---
title: Winstgevendheid van klanten en producten beoordelen
description: In dit artikel wordt beschreven hoe u door middel van de real-time analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Dynamics 365 Retail en deze kunt onderzoeken en er kennis uit kunt destilleren.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5a9bebf948bd4602556f70a5a79690621a03261e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023585"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="907f2-103">Winstgevendheid van klanten en producten beoordelen</span><span class="sxs-lookup"><span data-stu-id="907f2-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="907f2-104">In dit artikel wordt beschreven hoe u door middel van de real-time analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Dynamics 365 Retail en deze kunt onderzoeken en er kennis uit kunt destilleren.</span><span class="sxs-lookup"><span data-stu-id="907f2-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="907f2-105">Als onderdeel van Retail kunnen gebruikers rentabiliteit onderzoeken voor de beste klanten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="907f2-105">As part of Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="907f2-106">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="907f2-106">Sales amount</span></span>
- <span data-ttu-id="907f2-107">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="907f2-107">Quantity</span></span>
- <span data-ttu-id="907f2-108">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="907f2-108">Gross profit margin</span></span>
- <span data-ttu-id="907f2-109">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="907f2-109">Margin percentage</span></span>

<span data-ttu-id="907f2-110">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste klanten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="907f2-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="907f2-111">Werkgebied **Beheer van detailhandelwinkel** &gt; **Retail** &gt; **Kanalen** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="907f2-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="907f2-112">Sectie **Query's en rapporten** &gt; **Retail** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="907f2-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="907f2-113">Zo kunnen gebruikers ook winstgevendheid onderzoeken van de beste producten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="907f2-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="907f2-114">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="907f2-114">Sales amount</span></span>
- <span data-ttu-id="907f2-115">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="907f2-115">Quantity</span></span>
- <span data-ttu-id="907f2-116">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="907f2-116">Gross profit margin</span></span>
- <span data-ttu-id="907f2-117">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="907f2-117">Margin percentage</span></span>

<span data-ttu-id="907f2-118">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste producten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="907f2-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="907f2-119">Werkgebied **Beheer van detailhandelwinkel** &gt; **Retail** &gt; **Kanalen** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="907f2-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="907f2-120">Werkgebied **Categorie- en productbeheer** &gt; **Retail** &gt; **Producten en categorieën** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="907f2-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="907f2-121">Sectie **Query's en rapporten** &gt; **Retail** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="907f2-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>

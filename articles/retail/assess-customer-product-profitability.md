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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.contentlocale: nl-nl
ms.lasthandoff: 01/04/2019

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="6d1fc-103">Winstgevendheid van klanten en producten beoordelen</span><span class="sxs-lookup"><span data-stu-id="6d1fc-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6d1fc-104">In dit artikel wordt uitgelegd hoe u door middel van de real-time analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Microsoft Dynamics 365 for Retail en deze kunt onderzoeken en er kennis uit kunt destilleren.</span><span class="sxs-lookup"><span data-stu-id="6d1fc-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="6d1fc-105">Als onderdeel van Dynamics 365 for Retail kunnen gebruikers winstgevendheid onderzoeken voor de beste klanten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="6d1fc-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6d1fc-106">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="6d1fc-106">Sales amount</span></span>
- <span data-ttu-id="6d1fc-107">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="6d1fc-107">Quantity</span></span>
- <span data-ttu-id="6d1fc-108">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="6d1fc-108">Gross profit margin</span></span>
- <span data-ttu-id="6d1fc-109">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="6d1fc-109">Margin percentage</span></span>

<span data-ttu-id="6d1fc-110">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste klanten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="6d1fc-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6d1fc-111">Werkgebied **Beheer van detailhandelwinkel** &gt; **Retail** &gt; **Kanalen** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="6d1fc-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="6d1fc-112">Sectie **Query's en rapporten** &gt; **Retail** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="6d1fc-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="6d1fc-113">Zo kunnen gebruikers ook winstgevendheid onderzoeken van de beste producten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="6d1fc-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6d1fc-114">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="6d1fc-114">Sales amount</span></span>
- <span data-ttu-id="6d1fc-115">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="6d1fc-115">Quantity</span></span>
- <span data-ttu-id="6d1fc-116">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="6d1fc-116">Gross profit margin</span></span>
- <span data-ttu-id="6d1fc-117">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="6d1fc-117">Margin percentage</span></span>

<span data-ttu-id="6d1fc-118">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste producten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="6d1fc-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6d1fc-119">Werkgebied **Beheer van detailhandelwinkel** &gt; **Retail** &gt; **Kanalen** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="6d1fc-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6d1fc-120">Werkgebied **Categorie- en productbeheer** &gt; **Retail** &gt; **Producten en categorieën** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="6d1fc-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6d1fc-121">Sectie **Query's en rapporten** &gt; **Retail** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="6d1fc-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


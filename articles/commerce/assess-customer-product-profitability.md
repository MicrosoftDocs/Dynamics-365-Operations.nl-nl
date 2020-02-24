---
title: Winstgevendheid van klanten en producten beoordelen
description: In dit artikel wordt beschreven hoe u door middel van de realtime analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Dynamics 365 Commerce en deze kunt onderzoeken en er kennis uit kunt destilleren.
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
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022082"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="0c460-103">Winstgevendheid van klanten en producten beoordelen</span><span class="sxs-lookup"><span data-stu-id="0c460-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c460-104">In dit artikel wordt beschreven hoe u door middel van de realtime analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Dynamics 365 Commerce en deze kunt onderzoeken en er kennis uit kunt destilleren.</span><span class="sxs-lookup"><span data-stu-id="0c460-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="0c460-105">Als onderdeel van Commerce kunnen gebruikers rentabiliteit onderzoeken voor de beste klanten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="0c460-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="0c460-106">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="0c460-106">Sales amount</span></span>
- <span data-ttu-id="0c460-107">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0c460-107">Quantity</span></span>
- <span data-ttu-id="0c460-108">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="0c460-108">Gross profit margin</span></span>
- <span data-ttu-id="0c460-109">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="0c460-109">Margin percentage</span></span>

<span data-ttu-id="0c460-110">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste klanten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="0c460-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="0c460-111">Werkgebied **Winkelbeheer** &gt; **Retail en Commerce** &gt; **Kanalen** &gt; **Winkelbeheer** &gt; **Rapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="0c460-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="0c460-112">Sectie **Query's en rapporten** &gt; **Retail en Commerce** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="0c460-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="0c460-113">Zo kunnen gebruikers ook winstgevendheid onderzoeken van de beste producten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="0c460-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="0c460-114">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="0c460-114">Sales amount</span></span>
- <span data-ttu-id="0c460-115">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0c460-115">Quantity</span></span>
- <span data-ttu-id="0c460-116">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="0c460-116">Gross profit margin</span></span>
- <span data-ttu-id="0c460-117">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="0c460-117">Margin percentage</span></span>

<span data-ttu-id="0c460-118">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste producten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="0c460-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="0c460-119">Werkgebied **Winkelbeheer** &gt; **Retail en Commerce** &gt; **Kanalen** &gt; **Winkelbeheer** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="0c460-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="0c460-120">Werkgebied **Categorie- en productbeheer** &gt; **Retail en Commerce** &gt; **Producten en categorieën** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="0c460-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="0c460-121">Sectie **Query's en rapporten** &gt; **Retail en Commerce** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="0c460-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>

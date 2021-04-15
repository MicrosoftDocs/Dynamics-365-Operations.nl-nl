---
title: Winstgevendheid van klanten en producten beoordelen
description: In dit artikel wordt beschreven hoe u door middel van de realtime analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Dynamics 365 Commerce en deze kunt onderzoeken en er kennis uit kunt destilleren.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 80a2f38f2b3f039b17556116d6aea738faa1db50
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797324"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="6e251-103">Winstgevendheid van klanten en producten beoordelen</span><span class="sxs-lookup"><span data-stu-id="6e251-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6e251-104">In dit artikel wordt beschreven hoe u door middel van de realtime analyses in het geheugen toegang krijgt tot gegeven over de winstgevendheid van uw klanten en producten in Dynamics 365 Commerce en deze kunt onderzoeken en er kennis uit kunt destilleren.</span><span class="sxs-lookup"><span data-stu-id="6e251-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="6e251-105">Als onderdeel van Commerce kunnen gebruikers rentabiliteit onderzoeken voor de beste klanten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="6e251-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6e251-106">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="6e251-106">Sales amount</span></span>
- <span data-ttu-id="6e251-107">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="6e251-107">Quantity</span></span>
- <span data-ttu-id="6e251-108">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="6e251-108">Gross profit margin</span></span>
- <span data-ttu-id="6e251-109">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="6e251-109">Margin percentage</span></span>

<span data-ttu-id="6e251-110">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste klanten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="6e251-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6e251-111">Werkgebied **Winkelbeheer** &gt; **Retail en Commerce** &gt; **Kanalen** &gt; **Winkelbeheer** &gt; **Rapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="6e251-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="6e251-112">Sectie **Query's en rapporten** &gt; **Retail en Commerce** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Beste klanten**</span><span class="sxs-lookup"><span data-stu-id="6e251-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="6e251-113">Zo kunnen gebruikers ook winstgevendheid onderzoeken van de beste producten (10 tot 100) op verschillende niveaus van de organisatiehiërarchie, op basis van een van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="6e251-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6e251-114">Verkoopbedrag</span><span class="sxs-lookup"><span data-stu-id="6e251-114">Sales amount</span></span>
- <span data-ttu-id="6e251-115">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="6e251-115">Quantity</span></span>
- <span data-ttu-id="6e251-116">Brutowinstmarge</span><span class="sxs-lookup"><span data-stu-id="6e251-116">Gross profit margin</span></span>
- <span data-ttu-id="6e251-117">Margepercentage</span><span class="sxs-lookup"><span data-stu-id="6e251-117">Margin percentage</span></span>

<span data-ttu-id="6e251-118">Voor deze beoordeling kunt u het kant-en-klare rapport **Beste producten** gebruiken, dat u vanuit de volgende locaties kunt openen:</span><span class="sxs-lookup"><span data-stu-id="6e251-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6e251-119">Werkgebied **Winkelbeheer** &gt; **Retail en Commerce** &gt; **Kanalen** &gt; **Winkelbeheer** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="6e251-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6e251-120">Werkgebied **Categorie- en productbeheer** &gt; **Retail en Commerce** &gt; **Producten en categorieën** &gt; **Beheer van detailhandelwinkel** &gt; **Rapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="6e251-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6e251-121">Sectie **Query's en rapporten** &gt; **Retail en Commerce** &gt; **Query's en rapporten** &gt; **Verkooprapporten** &gt; **Rapport Topproducten**</span><span class="sxs-lookup"><span data-stu-id="6e251-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Opties voor het voorkomen van kortingen voor detailhandelproducten
description: Er zijn verschillende redenen waarom detailhandelaren willen voorkomen dat voor bepaalde producten korting wordt verleend, zoals bij een promotie of tijdens de verkoop op het POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 822bd39bca3a95f073bacea90a8ee58eada50ae2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022179"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="64d2d-103">Opties voor het voorkomen van kortingen voor detailhandelproducten</span><span class="sxs-lookup"><span data-stu-id="64d2d-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64d2d-104">Er zijn verschillende redenen waarom detailhandelaren willen voorkomen dat voor bepaalde producten korting wordt verleend, zoals bij een promotie of tijdens de verkoop op het POS.</span><span class="sxs-lookup"><span data-stu-id="64d2d-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="64d2d-105">De volgende opties vindt u op het tabblad **Commerce** van uitgegeven producten. Hiermee kunt u het product configureren om alle of handmatige kortingen te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="64d2d-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="64d2d-106">De instellingen kunnen ook worden opgegeven op categorieniveau vanuit de hiërarchie van detailhandelcategorieën.</span><span class="sxs-lookup"><span data-stu-id="64d2d-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="64d2d-107">**Alle kortingen voorkomen**: selecteer deze optie om te voorkomen dat alle soorten kortingen worden toegepast op dit product.</span><span class="sxs-lookup"><span data-stu-id="64d2d-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="64d2d-108">Het gaat hierbij om acties zoals combinatiekortingen, volume- en drempelkortingen, en handmatige regel- en transactiekortingen die tijdens een verkoop worden toegepast door een POS-gebruiker.</span><span class="sxs-lookup"><span data-stu-id="64d2d-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="64d2d-109">**Handmatige kortingen voorkomen**: selecteer deze optie alleen om handmatige regel- of transactiekortingen te voorkomen die tijdens een verkoop worden toegepast door een POS-gebruiker.</span><span class="sxs-lookup"><span data-stu-id="64d2d-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="64d2d-110">Producten waarvoor deze optie is geselecteerd, komen nog steeds in aanmerking voor promoties, combinatiekortingen en volume- en drempelkortingen.</span><span class="sxs-lookup"><span data-stu-id="64d2d-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="64d2d-111">Deze instellingen beperken niet de werking van prijsoverschrijvingen omdat die de basisprijs instellen en niet als een korting gelden.</span><span class="sxs-lookup"><span data-stu-id="64d2d-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="64d2d-112">[![Veld Kortingen voorkomen](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="64d2d-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
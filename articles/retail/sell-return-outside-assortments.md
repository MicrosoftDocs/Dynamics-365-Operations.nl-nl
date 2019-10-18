---
title: Producten verkopen en terugsturen die geen deel uitmaken van een winkelassortiment
description: Met Dynamics 365 Retail kunt u producten buiten assortimenten verkopen en retourneren
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ae6bac983ddb4d4a217fe83c8f68c5a87ccd6a47
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024932"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="ea412-103">Producten verkopen en terugsturen die geen deel uitmaken van een winkelassortiment</span><span class="sxs-lookup"><span data-stu-id="ea412-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea412-104">Een gangbaar scenario voor elke detailhandelaar is dat hij aan hun klanten producten verkoop of retouren van de klanten accepteert, zelfs als hij de specifieke producten niet voert in zijn winkel (met andere woorden, de producten zijn niet geassorteerd aan de winkel).</span><span class="sxs-lookup"><span data-stu-id="ea412-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="ea412-105">Hierna vindt u enkele typische scenario's:</span><span class="sxs-lookup"><span data-stu-id="ea412-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="ea412-106">Een detailhandelaar voert in een bepaalde winkel niet alle producten uit zijn assortiment.</span><span class="sxs-lookup"><span data-stu-id="ea412-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="ea412-107">De overige producten worden opgeslagen in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="ea412-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="ea412-108">De winkelmedewerker kan de klant helpen door te zoeken of bladeren naar de producten in het magazijn, ze toe te voegen aan de winkelwagen en het afrekenen voltooien door een leveringsmethode te selecteren, zoals verzending naar een adres vanuit het magazijn of de klant het product laten afhalen bij de huidige winkel of een andere winkel.</span><span class="sxs-lookup"><span data-stu-id="ea412-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="ea412-109">Een detailhandelaar voert specifieke producten niet in de winkel of heeft ze niet op voorraad in de winkel die de klant bezocht, maar de producten zijn beschikbaar in andere winkels.</span><span class="sxs-lookup"><span data-stu-id="ea412-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="ea412-110">De winkelmedewerker kan de klant helpen door te zoeken of bladeren naar de producten in de andere winkel, ze toe te voegen aan de winkelwagen en het afrekenen voltooien door een leveringsmethode te selecteren.</span><span class="sxs-lookup"><span data-stu-id="ea412-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="ea412-111">Een detailhandelaar heeft veel winkels in en rond een bepaalde plaats of postcode en wil de klanten niet dwingen om producten te retourneren in dezelfde winkel als waar ze zijn gekocht.</span><span class="sxs-lookup"><span data-stu-id="ea412-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="ea412-112">In plaats daarvan kunnen klanten producten retourneren in elke winkel.</span><span class="sxs-lookup"><span data-stu-id="ea412-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="ea412-113">Deze algemene scenario's zijn beschikbaar voor detailhandelaren die Retail gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ea412-113">Those common scenarios are available for retailers using Retail.</span></span> <span data-ttu-id="ea412-114">Met Retail kunt u onder meer:</span><span class="sxs-lookup"><span data-stu-id="ea412-114">With Retail, you can:</span></span>

+ <span data-ttu-id="ea412-115">Zoeken naar producten in andere winkels of door de lijst bladeren.</span><span class="sxs-lookup"><span data-stu-id="ea412-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="ea412-116">Alle vrijgegeven producten doorzoeken of erdoor bladeren.</span><span class="sxs-lookup"><span data-stu-id="ea412-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="ea412-117">Cash and carry-transacties of klantorders maken.</span><span class="sxs-lookup"><span data-stu-id="ea412-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="ea412-118">Leveringsopties voor klantorders selecteren.</span><span class="sxs-lookup"><span data-stu-id="ea412-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="ea412-119">Producten in de huidige winkel of een andere winkel afhalen.</span><span class="sxs-lookup"><span data-stu-id="ea412-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="ea412-120">Een order in de huidige winkel of een andere winkel annuleren.</span><span class="sxs-lookup"><span data-stu-id="ea412-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="ea412-121">Een order retourneren met of zonder kassabon in de huidige winkel of een andere winkel.</span><span class="sxs-lookup"><span data-stu-id="ea412-121">Return an order with or without the receipt at the current store or another store.</span></span>

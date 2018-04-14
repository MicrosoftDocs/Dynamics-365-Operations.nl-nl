--- 
title: " Detailhandelsprijscorrecties"
description: Deze procedure doorloopt het maken van een prijscorrectie voor detailhandel.
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 191f48bc5b56bef9fe08c266db8cd49ce7cbc620
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="fc6bc-103"> Detailhandelsprijscorrecties</span><span class="sxs-lookup"><span data-stu-id="fc6bc-103">Retail price adjustments</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fc6bc-104">Deze procedure doorloopt het maken van een prijscorrectie voor detailhandel.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="fc6bc-105">Een detailhandelsprijscorrectie kan de verkoopprijs van een artikel rechtstreeks instellen of de basisverkoopprijs of handelsovereenkomstverkoopprijs wijzigen.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="fc6bc-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="fc6bc-107">Klik op Prijzen- en kortingsbeheer.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="fc6bc-108">Klik op het tabblad Prijscorrecties.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="fc6bc-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-109">Click New.</span></span>
    * <span data-ttu-id="fc6bc-110">Van hieruit kunt u alle meest gangbare gebruikte prijs- en kortingregels maken, waaronder detailhandelskortingen, prijscorrecties, handelsovereenkomstjournalen en categorieprijsregels.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="fc6bc-111">Klik op Prijscorrectie.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="fc6bc-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="fc6bc-113">Vouw de sectie Regels uit.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="fc6bc-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-114">Click Add.</span></span>
    * <span data-ttu-id="fc6bc-115">Typ voor dit voorbeeld '81126' in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="fc6bc-116">Voer vervolgens '10.0' in het veld Kortingspercentage in.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="fc6bc-117">Een prijscorrectie van het type kortingspercentage verlaagt een basisverkoopprijs of een handelsovereenkomstverkoopprijs.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="fc6bc-118">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-118">Click Add.</span></span>
    * <span data-ttu-id="fc6bc-119">Typ voor dit voorbeeld '81125' in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="fc6bc-120">Selecteer vervolgens 'Contantkortingsbedrag' in het veld Kortingsmethode.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="fc6bc-121">Voer ten slotte '5.0' in het veld Contantkortingsbedrag in.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="fc6bc-122">Een korting van het type contantkortingsbedrag is een bedrag dat af wordt gehaald van een basisprijs of een handelsovereenkomstprijs.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="fc6bc-123">Klik op Prijsgroepen.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-123">Click Price groups.</span></span>
    * <span data-ttu-id="fc6bc-124">Selecteer 'RP-Houston' in het veld Prijsgroep.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="fc6bc-125">Hierdoor wordt de prijscorrectie gekoppeld aan de Houston-winkel.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="fc6bc-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-126">Click Save.</span></span>
11. <span data-ttu-id="fc6bc-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-127">Close the page.</span></span>
12. <span data-ttu-id="fc6bc-128">Selecteer 'Ingeschakeld' in het veld Status.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="fc6bc-129">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-129">Click Save.</span></span>
14. <span data-ttu-id="fc6bc-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-130">Close the page.</span></span>
15. <span data-ttu-id="fc6bc-131">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="fc6bc-131">Refresh the page.</span></span>



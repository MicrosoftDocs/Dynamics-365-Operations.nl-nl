---
title: Acties en kortingen
description: Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240937"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="7a2e0-103">Acties en kortingen</span><span class="sxs-lookup"><span data-stu-id="7a2e0-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a2e0-104">Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7a2e0-105">U kunt in Commerce prijscorrecties uitvoeren voor producten en ook kortingen instellen die worden toegepast op een regelartikel of een transactie bij het POS, in een callcenter-verkooporder of in een online order.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="7a2e0-106">Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="7a2e0-107">Voor zowel prijscorrecties als kortingen kunt u een enkele begindatum en einddatum of een terugkerende periode, een kortingscode en enkele aanvullende kenmerken opgeven.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="7a2e0-108">Prijscorrecties en kortingen kunnen worden toegepast op producten, varianten of categorieën.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="7a2e0-109">Als meer dan één korting op een product van toepassing is, kan een klant een van de kortingen of een gecombineerde korting ontvangen, afhankelijk van de configuratie van de korting.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="7a2e0-110">In Commerce wordt automatisch de korting of combinatie van kortingen toegepast die de beste prijs voor de klant oplevert.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="7a2e0-111">Wanneer u een prijscorrectie of een korting instelt, moet u controleren of de prijsgroepen zijn toegewezen aan de juiste kanalen, catalogi, aansluitingen of loyaliteitsprogramma's voor het toepassen van de korting.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="7a2e0-112">Bovendien stelt u, als u automatisch de korting-id wilt genereren, nummerreeksen in op de pagina **Commerce-parameters** voordat u een nieuwe prijscorrectie of korting definieert.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="7a2e0-113">U kunt een prijscorrectie of korting verwijderen.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="7a2e0-114">Statistische informatie gaat echter verloren.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="7a2e0-115">Typen korting</span><span class="sxs-lookup"><span data-stu-id="7a2e0-115">Types of discounts</span></span>

<span data-ttu-id="7a2e0-116">Er zijn veel typen korting:</span><span class="sxs-lookup"><span data-stu-id="7a2e0-116">There are many types of discounts:</span></span>

- <span data-ttu-id="7a2e0-117">**Eenvoudige korting** - Eén percentage of bedrag.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="7a2e0-118">**Hoeveelheidskorting** – Een korting die wordt toegepast wanneer twee of meer producten worden aangeschaft.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="7a2e0-119">**Combinatiekorting** – Een korting die wordt toegepast als een specifieke combinatie van producten wordt aangeschaft.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="7a2e0-120">**Drempelkorting** – Een korting die wordt toegepast wanneer het transactietotaal hoger is dan een bepaald bedrag.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="7a2e0-121">**Korting op basis van betalingsmethode** - een korting die wordt toegepast wanneer het transactietotaal meer dan een opgegeven bedrag is en een bepaalde betalingsmethode (bijvoorbeeld contant, creditcard of bankpas) wordt gebruikt voor de betaling.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="7a2e0-122">**Korting op verzendkosten** : een korting die wordt toegepast wanneer het transactietotaal meer is dan een opgegeven bedrag en een specifieke leveringsmethode (bijvoorbeeld een verzending van twee dagen of een nachtverzending) wordt gebruikt voor de order.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="7a2e0-123">Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="7a2e0-124">De prijsgroepen kunnen vervolgens aan kanalen, catalogi, aansluitingen en loyaliteitsprogramma's worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="7a2e0-125">De combinatiekorting en de drempelkorting hebben de eigenschappen 'Niet-kortingsproducten tellen' en 'Niet-kortingsproducten tellen naar drempel'.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="7a2e0-126">Als deze eigenschappen zijn ingeschakeld, kan een artikel dat niet voor korting in aanmerking komt nog steeds een transactie kwalificeren voor de korting, maar krijgt het artikel dat niet in aanmerking komt de korting niet.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="7a2e0-127">Als u bijvoorbeeld een combinatiekorting met twee regels maakt, A en B, waarbij een klant 10% korting krijgt voor beide artikelen maar voor artikel A de configuratie 'Alle kortingen voorkomen' is ingeschakeld, wordt hierdoor meestal artikel A niet in de korting opgenomen.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="7a2e0-128">Als de eigenschap 'Niet-kortingsproducten tellen' echter is ingeschakeld, kan artikel A worden gebruikt voor kwalificatie voor de combinatiekorting. De korting van 10% wordt echter alleen toegepast op artikel B. Op de drempelkorting is vergelijkbare logica van toepassing.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="7a2e0-129">De eigenschap 'Niet-kortingsproducten tellen naar drempel' heeft echter een extra mogelijkheid in vergelijking met de eigenschap 'Niet-kortingsproducten tellen' van de combinatiekortingen.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="7a2e0-130">Als de drempelkorting is ingeschakeld en als er een artikel met een bestaande korting is waarmee een artikel geen andere kortingen zou kunnen krijgen, kan de betaalde prijs voor dit artikel voldoen aan de drempel, maar krijgt dit artikel niet de aanvullende korting.</span><span class="sxs-lookup"><span data-stu-id="7a2e0-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

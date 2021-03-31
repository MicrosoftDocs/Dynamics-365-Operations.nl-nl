---
title: Acties en kortingen
description: Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: d64632d7726fa5093bd04232790cae3f75938ae5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231218"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="58352-103">Acties en kortingen</span><span class="sxs-lookup"><span data-stu-id="58352-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="58352-104">Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="58352-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="58352-105">U kunt in Commerce prijscorrecties uitvoeren voor producten en ook kortingen instellen die worden toegepast op een regelartikel of een transactie bij het POS, in een callcenter-verkooporder of in een online order.</span><span class="sxs-lookup"><span data-stu-id="58352-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="58352-106">Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="58352-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="58352-107">Voor zowel prijscorrecties als kortingen kunt u een enkele begindatum en einddatum of een terugkerende periode, een kortingscode en enkele aanvullende kenmerken opgeven.</span><span class="sxs-lookup"><span data-stu-id="58352-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="58352-108">Prijscorrecties en kortingen kunnen worden toegepast op producten, varianten of categorieën.</span><span class="sxs-lookup"><span data-stu-id="58352-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="58352-109">Als meer dan één korting op een product van toepassing is, kan een klant een van de kortingen of een gecombineerde korting ontvangen, afhankelijk van de configuratie van de korting.</span><span class="sxs-lookup"><span data-stu-id="58352-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="58352-110">In Commerce wordt automatisch de korting of combinatie van kortingen toegepast die de beste prijs voor de klant oplevert.</span><span class="sxs-lookup"><span data-stu-id="58352-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="58352-111">Wanneer u een prijscorrectie of een korting instelt, moet u controleren of de prijsgroepen zijn toegewezen aan de juiste kanalen, catalogi, aansluitingen of loyaliteitsprogramma's voor het toepassen van de korting.</span><span class="sxs-lookup"><span data-stu-id="58352-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="58352-112">Bovendien stelt u, als u automatisch de korting-id wilt genereren, nummerreeksen in op de pagina **Commerce-parameters** voordat u een nieuwe prijscorrectie of korting definieert.</span><span class="sxs-lookup"><span data-stu-id="58352-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="58352-113">U kunt een prijscorrectie of korting verwijderen.</span><span class="sxs-lookup"><span data-stu-id="58352-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="58352-114">Statistische informatie gaat echter verloren.</span><span class="sxs-lookup"><span data-stu-id="58352-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="58352-115">Typen korting</span><span class="sxs-lookup"><span data-stu-id="58352-115">Types of discounts</span></span>

<span data-ttu-id="58352-116">Er zijn veel typen korting:</span><span class="sxs-lookup"><span data-stu-id="58352-116">There are many types of discounts:</span></span>

- <span data-ttu-id="58352-117">**Eenvoudige korting** - Eén percentage of bedrag.</span><span class="sxs-lookup"><span data-stu-id="58352-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="58352-118">**Hoeveelheidskorting** – Een korting die wordt toegepast wanneer twee of meer producten worden aangeschaft.</span><span class="sxs-lookup"><span data-stu-id="58352-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="58352-119">**Combinatiekorting** – Een korting die wordt toegepast als een specifieke combinatie van producten wordt aangeschaft.</span><span class="sxs-lookup"><span data-stu-id="58352-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="58352-120">**Drempelkorting** – Een korting die wordt toegepast wanneer het transactietotaal hoger is dan een bepaald bedrag.</span><span class="sxs-lookup"><span data-stu-id="58352-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="58352-121">**Korting op basis van betalingsmethode** - een korting die wordt toegepast wanneer het transactietotaal meer dan een opgegeven bedrag is en een bepaalde betalingsmethode (bijvoorbeeld contant, creditcard of bankpas) wordt gebruikt voor de betaling.</span><span class="sxs-lookup"><span data-stu-id="58352-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="58352-122">**Korting op verzendkosten** : een korting die wordt toegepast wanneer het transactietotaal meer is dan een opgegeven bedrag en een specifieke leveringsmethode (bijvoorbeeld een verzending van twee dagen of een nachtverzending) wordt gebruikt voor de order.</span><span class="sxs-lookup"><span data-stu-id="58352-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="58352-123">Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="58352-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="58352-124">De prijsgroepen kunnen vervolgens aan kanalen, catalogi, aansluitingen en loyaliteitsprogramma's worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="58352-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
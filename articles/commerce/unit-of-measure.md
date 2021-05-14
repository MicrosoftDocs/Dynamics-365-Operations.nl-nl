---
title: Instellingen maateenheid toepassen
description: In dit onderwerp worden instellingen van de maateenheid beschreven en hoe u deze toepast in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c5750ae506978dfac842eebf4ba6036322bdd7f
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937575"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="1df7d-103">Instellingen maateenheid toepassen</span><span class="sxs-lookup"><span data-stu-id="1df7d-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1df7d-104">In dit onderwerp worden instellingen van de maateenheid beschreven en hoe u deze toepast in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1df7d-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1df7d-105">Een product kan worden verkocht in verschillende eenheden, zoals 'stuk', 'paar' en 'dozijn'.</span><span class="sxs-lookup"><span data-stu-id="1df7d-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="1df7d-106">In Commerce Headquarters kan de maateenheid voor een product worden gedefinieerd en weergegeven op een e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="1df7d-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="1df7d-107">Als een detailhandelaar bijvoorbeeld een product per stuk of per dozijn verkoopt, kunnen de beschikbare maateenheden tegelijk met de andere productgegevens worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1df7d-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="1df7d-108">In het onderstaande voorbeeld is een maateenheid per **st** (stuk) geconfigureerd voor een product in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1df7d-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Voorbeeld van een product dat is geconfigureerd met een maateenheid in Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="1df7d-110">Ondersteuning voor het toepassen en weergeven van de maateenheid is beschikbaar vanaf Commerce versie 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="1df7d-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="1df7d-111">Instellingen maateenheid</span><span class="sxs-lookup"><span data-stu-id="1df7d-111">Unit of measure settings</span></span>

<span data-ttu-id="1df7d-112">U kunt weergave-instellingen voor maateenheden definiëren in Commerce Site Builder, in **Site-instellingen \> Extensies \> Maateenheid voor producten weergeven**.</span><span class="sxs-lookup"><span data-stu-id="1df7d-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="1df7d-113">Er zijn drie ondersteunde instellingen:</span><span class="sxs-lookup"><span data-stu-id="1df7d-113">There are three supported settings:</span></span>

- <span data-ttu-id="1df7d-114">**Niet weergeven**: wanneer deze instelling is geselecteerd, wordt de maateenheid voor het product niet weergegeven op de e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="1df7d-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="1df7d-115">Dit is het standaardgedrag.</span><span class="sxs-lookup"><span data-stu-id="1df7d-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="1df7d-116">**Weergeven bij het kopen van producten**: wanneer deze instelling is geselecteerd, wordt de maateenheid weergegeven bij productgegevens, winkelwagen, kassa, orderhistorie en orderdetailpagina's.</span><span class="sxs-lookup"><span data-stu-id="1df7d-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="1df7d-117">**Weergeven bij het zoeken en kopen van producten**: wanneer deze instelling is geselecteerd, wordt de maateenheid weergegeven op de pagina's waar u producten kunt kopen en tijdens het zoeken naar producten.</span><span class="sxs-lookup"><span data-stu-id="1df7d-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="1df7d-118">Als onderdeel van dit gedrag worden maateenheden weergegeven in zoekresultaten en productverzamelingsmodules.</span><span class="sxs-lookup"><span data-stu-id="1df7d-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1df7d-119">Weergave-instellingen voor maateenheden zijn beschikbaar vanaf Commerce versie 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="1df7d-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="1df7d-120">Als u een oudere versie van Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="1df7d-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="1df7d-121">Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer instructies.</span><span class="sxs-lookup"><span data-stu-id="1df7d-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="1df7d-122">Modules die maateenheidsinstellingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="1df7d-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="1df7d-123">Modules die de maateenheidsinstellingen gebruiken, omvatten de modules koopvak, verlanglijst, winkelwagen, pictogram van winkelwagen, containerzoekresultaten, productverzameling en orderdetails.</span><span class="sxs-lookup"><span data-stu-id="1df7d-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="1df7d-124">In het voorbeeld in de volgende afbeelding ziet u op een pagina met productdetails (PDP) de maateenheid (**st**) voor een product.</span><span class="sxs-lookup"><span data-stu-id="1df7d-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Voorbeeld van een PDP met de maateenheid](./media/Productunit-PDP.png)

<span data-ttu-id="1df7d-126">In het voorbeeld in de volgende afbeelding ziet u op een productverzamelingsmodule de maateenheid (**st**) voor een product.</span><span class="sxs-lookup"><span data-stu-id="1df7d-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Voorbeeld van een productverzamelingsmodule met de maateenheid](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="1df7d-128">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1df7d-128">Additional resources</span></span>

[<span data-ttu-id="1df7d-129">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="1df7d-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1df7d-130">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="1df7d-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1df7d-131">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="1df7d-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1df7d-132">Accountbeheerpagina's en -modules</span><span class="sxs-lookup"><span data-stu-id="1df7d-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="1df7d-133">Updates voor SDK's en modulebibliotheken</span><span class="sxs-lookup"><span data-stu-id="1df7d-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Module winkelwagenpictogram
description: In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411084"
---
# <a name="cart-icon-module"></a><span data-ttu-id="94d99-103">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="94d99-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94d99-104">In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="94d99-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="94d99-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="94d99-105">Overview</span></span>

<span data-ttu-id="94d99-106">De module winkelwagenpictogram geeft de winkelwagen weer in de koptekstmodule van de pagina en toont het aantal artikelen in de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="94d99-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="94d99-107">De module winkelwagenpictogram geeft ook een overzicht van winkelwagen (ook wel minikar genoemd) wanneer de cursor boven het winkelwagenpictogram wordt gehouden.</span><span class="sxs-lookup"><span data-stu-id="94d99-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="94d99-108">De minikar geeft de gebruiker een overzicht van de artikelen in de winkelwagen zonder dat u naar de pagina Winkelwagen hoeft te navigeren.</span><span class="sxs-lookup"><span data-stu-id="94d99-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="94d99-109">Daarnaast kunnen gebruikers ook rechtstreeks naar de afhandelingspagina gaan als ze tevreden zijn over het overzicht.</span><span class="sxs-lookup"><span data-stu-id="94d99-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="94d99-110">Hierdoor is er minder paginanavigatie nodig en wordt de afhandeling versneld.</span><span class="sxs-lookup"><span data-stu-id="94d99-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="94d99-111">De volgende afbeelding toont een voorbeeld van een winkelwagenpictogrammodule waarin een minikar wordt weergegeven in de Fabrikam-koptekst.</span><span class="sxs-lookup"><span data-stu-id="94d99-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Voorbeeld van een winkelwagenpictogrammodule](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="94d99-113">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="94d99-113">Module properties</span></span>

- <span data-ttu-id="94d99-114">**Minikar weergeven**: indien waar, kan met deze eigenschap een winkelwagenoverzicht (minikar) worden weergegeven wanneer de cursor boven het winkelwagenpictogram wordt gehouden.</span><span class="sxs-lookup"><span data-stu-id="94d99-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="94d99-115">Deze functionaliteit wordt alleen ondersteund voor viewports op een bureaublad.</span><span class="sxs-lookup"><span data-stu-id="94d99-115">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="94d99-116">Een module winkelwagenpictogram toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="94d99-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="94d99-117">Zie [Koptekstmodule](author-header-module.md) om een module winkelwagenpictogram toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="94d99-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="94d99-118">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="94d99-118">Additional resources</span></span>

[<span data-ttu-id="94d99-119">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="94d99-119">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="94d99-120">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="94d99-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="94d99-121">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="94d99-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="94d99-122">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="94d99-122">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="94d99-123">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="94d99-123">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="94d99-124">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="94d99-124">Footer module</span></span>](author-footer-module.md)

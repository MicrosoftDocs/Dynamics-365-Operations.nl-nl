---
title: Een variantgroep maken
description: In dit onderwerp wordt beschreven hoe u een maat-, stijl- of kleurvariantgroep kunt maken voor een product in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001870"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="d3f1a-103">Een variantgroep maken</span><span class="sxs-lookup"><span data-stu-id="d3f1a-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d3f1a-104">In dit onderwerp wordt beschreven hoe u een maat-, stijl- of kleurvariantgroep kunt maken voor een product in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d3f1a-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d3f1a-105">Overview</span></span>

<span data-ttu-id="d3f1a-106">Dynamics 365 Commerce ondersteunt meerdere varianten voor producten.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="d3f1a-107">Het is ideaal om variantgroepen voor verschillende productcategorieën in te stellen.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="d3f1a-108">U kunt bijvoorbeeld een maatgroep maken voor t-shirts met de maten extra small, small, medium, large en extra large, of een kleurgroep maken om alle beschikbare kleuren van een product op te nemen.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="d3f1a-109">U moet variantgroepen toevoegen voordat u producten toevoegt.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="d3f1a-110">In dit onderwerp wordt een maatgroep gemaakt en geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="d3f1a-111">Vergelijkbare procedures kunnen worden gebruikt voor het toevoegen en configureren van stijlgroepen en kleurgroepen.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="d3f1a-112">Een maatgroep maken</span><span class="sxs-lookup"><span data-stu-id="d3f1a-112">Create a size group</span></span>

<span data-ttu-id="d3f1a-113">Volg deze stappen om een maatgroep te maken.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="d3f1a-114">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Variantgroepen \> Maatgroepen**.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="d3f1a-115">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d3f1a-116">Voer in het vak **Maatgroep** een unieke naam voor de maatgroep in.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="d3f1a-117">Voer in het vak **Omschrijving** een passende beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="d3f1a-118">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="d3f1a-119">Kenmerken toevoegen aan de maatgroep</span><span class="sxs-lookup"><span data-stu-id="d3f1a-119">Add attributes to the size group</span></span>

<span data-ttu-id="d3f1a-120">Volg deze stappen om kenmerken aan een maatgroep toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="d3f1a-121">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Variantgroepen \> Maatgroepen**</span><span class="sxs-lookup"><span data-stu-id="d3f1a-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="d3f1a-122">Selecteer een maatgroep in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="d3f1a-123">Selecteer **Toevoegen** onder **Maatgroepregels**.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="d3f1a-124">Voer in het vak **Maat** een tekenreeks die staat voor de maat (bijvoorbeeld 'XL').</span><span class="sxs-lookup"><span data-stu-id="d3f1a-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="d3f1a-125">Voer in het vak **Maatnaam** een naam in voor de maat (bijvoorbeeld 'Extra Large').</span><span class="sxs-lookup"><span data-stu-id="d3f1a-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="d3f1a-126">Voer in het vak **Aanvullingsgewicht** een getal in dat staat voor het aanvullingsgewicht.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="d3f1a-127">Voer in het vak **Getal in streepjescode** een getal in dat staat voor de streepjescode.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="d3f1a-128">Voer in het vak **Weergavevolgorde** een getal voor de weergavevolgorde in.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="d3f1a-129">Selecteer **Opslaan** in het actievenster wanneer u klaar bent met het toevoegen van maten.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="d3f1a-130">De volgende afbeelding toont een voorbeeld van een maatgroep voor 'hemdmaten'.</span><span class="sxs-lookup"><span data-stu-id="d3f1a-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Een maatgroep maken](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="d3f1a-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d3f1a-132">Additional resources</span></span>

[<span data-ttu-id="d3f1a-133">Overzicht van Productgegevens</span><span class="sxs-lookup"><span data-stu-id="d3f1a-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d3f1a-134">Detailhandelproducten instellen</span><span class="sxs-lookup"><span data-stu-id="d3f1a-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="d3f1a-135">Productdimensies</span><span class="sxs-lookup"><span data-stu-id="d3f1a-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)

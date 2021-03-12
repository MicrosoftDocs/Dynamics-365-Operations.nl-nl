---
title: Een afzetkanaalnavigatiehiërarchie maken
description: In dit onderwerp wordt beschreven hoe u een kanaalnavigatiehiërarchie maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89e24496d35ea0a02bd985f76d7579e1914d9290
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972977"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="920b9-103">Een afzetkanaalnavigatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="920b9-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="920b9-104">In dit onderwerp wordt beschreven hoe u een kanaalnavigatiehiërarchie maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="920b9-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="920b9-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="920b9-105">Overview</span></span>

<span data-ttu-id="920b9-106">Met een kanaalnavigatiehiërarchie kunt u producten groeperen en indelen in categorieën, zodat de producten online of op verkooppunten (POS) kunnen worden bezocht.</span><span class="sxs-lookup"><span data-stu-id="920b9-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="920b9-107">Een afzetkanaalnavigatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="920b9-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="920b9-108">Voer de volgende stappen uit om een navigatiehiërarchie voor een kanaal te maken.</span><span class="sxs-lookup"><span data-stu-id="920b9-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="920b9-109">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Kanaalnavigatiecategorieën**.</span><span class="sxs-lookup"><span data-stu-id="920b9-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="920b9-110">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="920b9-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="920b9-111">Voer in het vak **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="920b9-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="920b9-112">Voer in het vak **Omschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="920b9-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="920b9-113">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="920b9-113">Select **Create**.</span></span>
1. <span data-ttu-id="920b9-114">Selecteer in het actievenster **Nieuw categorieknooppunt** om een hoofdknooppunt te maken.</span><span class="sxs-lookup"><span data-stu-id="920b9-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="920b9-115">Voer in het vak **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="920b9-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="920b9-116">Voer in het vak **Omschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="920b9-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="920b9-117">Voer in het vak **Beschrijvende naam** een beschrijvende naam in.</span><span class="sxs-lookup"><span data-stu-id="920b9-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="920b9-118">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="920b9-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="920b9-119">In de volgende afbeelding ziet u een voorbeeld van een hoofdknooppunt.</span><span class="sxs-lookup"><span data-stu-id="920b9-119">The following image shows a example root node.</span></span>

![Voorbeeld hoofdknooppunt](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="920b9-121">Navigatiecategorieknooppunten maken</span><span class="sxs-lookup"><span data-stu-id="920b9-121">Create navigation category nodes</span></span>

<span data-ttu-id="920b9-122">Voer de volgende stappen uit om extra navigatiecategorieknooppunten te maken die de productcategorieën in het kanaal vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="920b9-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="920b9-123">Selecteer in het navigatievenster het bovenliggende knooppunt waaraan u een categorie wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="920b9-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="920b9-124">Klik in het actievenster op **Nieuw categorieknooppunt**.</span><span class="sxs-lookup"><span data-stu-id="920b9-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="920b9-125">Voer in het vak **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="920b9-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="920b9-126">Voer in het vak **Omschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="920b9-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="920b9-127">Voer in het vak **Beschrijvende naam** een beschrijvende naam in.</span><span class="sxs-lookup"><span data-stu-id="920b9-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="920b9-128">Voer in het vak **Weergavevolgorde** een weergavevolgorde in (optioneel).</span><span class="sxs-lookup"><span data-stu-id="920b9-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="920b9-129">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="920b9-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="920b9-130">In de volgende afbeelding ziet u een voorbeeld van een voltooide kanaalnavigatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="920b9-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Voorbeeld kanaalhiërarchie](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="920b9-132">Producten aan categorieknooppunten toevoegen</span><span class="sxs-lookup"><span data-stu-id="920b9-132">Add products to category nodes</span></span>

<span data-ttu-id="920b9-133">Voer de volgende stappen uit om producten toe te voegen aan categorieknooppunten.</span><span class="sxs-lookup"><span data-stu-id="920b9-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="920b9-134">Selecteer een categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="920b9-134">Select a category node.</span></span>
1. <span data-ttu-id="920b9-135">Selecteer **Toevoegen** onder **Producten**.</span><span class="sxs-lookup"><span data-stu-id="920b9-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="920b9-136">Zoek de nieuwe producten die u wilt toevoegen aan de hand van het productnummer of de productnaam en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="920b9-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="920b9-137">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="920b9-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="920b9-138">Producten toevoegen aan een knooppunt in de kanaalnavigatiehiërarchie is niet genoeg om de producten te laten weergeven in een geselecteerd kanaal. De producten moeten ook onder een product worden geassorteerd.</span><span class="sxs-lookup"><span data-stu-id="920b9-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="920b9-139">De volgende afbeelding toont een voorbeeldknooppunt met toegevoegde producten.</span><span class="sxs-lookup"><span data-stu-id="920b9-139">The following image shows an example node with products added.</span></span>

![Producten toegevoegd aan een categorieknooppunt](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="920b9-141">Productkenmerkgroepen toevoegen aan categorieknooppunten</span><span class="sxs-lookup"><span data-stu-id="920b9-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="920b9-142">U moet kenmerkgroepen maken voordat u ze aan een knooppunt in de kanaalnavigatiehiërarchie kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="920b9-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="920b9-143">Voer deze stappen uit om een productkenmerkgroep aan een categorieknooppunt toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="920b9-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="920b9-144">Selecteer een categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="920b9-144">Select a category node.</span></span>
1. <span data-ttu-id="920b9-145">Selecteer **Toevoegen** onder **Productkenmerkgroep**.</span><span class="sxs-lookup"><span data-stu-id="920b9-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="920b9-146">Zoek de kenmerkgroepen die u wilt toevoegen en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="920b9-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="920b9-147">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="920b9-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="920b9-148">De volgende afbeelding toont een voorbeeldknooppunt met toegevoegde productkenmerkgroepen.</span><span class="sxs-lookup"><span data-stu-id="920b9-148">The following image shows a sample node with product attribute groups added.</span></span>

![Productkenmerkgroepen op een knooppunt](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="920b9-150">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="920b9-150">Additional resources</span></span>

[<span data-ttu-id="920b9-151">Assortimenten instellen</span><span class="sxs-lookup"><span data-stu-id="920b9-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="920b9-152">Kenmerken en kenmerkgroepen beheren</span><span class="sxs-lookup"><span data-stu-id="920b9-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)

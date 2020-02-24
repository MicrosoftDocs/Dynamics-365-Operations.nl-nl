---
title: Een nieuw product maken
description: In dit onderwerp wordt beschreven hoe u een nieuw product maakt in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001960"
---
# <a name="create-a-new-product"></a><span data-ttu-id="b5f16-103">Een nieuw product maken</span><span class="sxs-lookup"><span data-stu-id="b5f16-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b5f16-104">In dit onderwerp wordt beschreven hoe u een nieuw product maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5f16-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5f16-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b5f16-105">Overview</span></span>

<span data-ttu-id="b5f16-106">Een product wordt voornamelijk gedefinieerd door een productnummer, -naam en -beschrijving.</span><span class="sxs-lookup"><span data-stu-id="b5f16-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="b5f16-107">Andere gegevens zijn echter ook vereist om een product of service te beschrijven:</span><span class="sxs-lookup"><span data-stu-id="b5f16-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="b5f16-108">Een nieuw product maken</span><span class="sxs-lookup"><span data-stu-id="b5f16-108">Create a new product</span></span>

1. <span data-ttu-id="b5f16-109">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Producten per categorie**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="b5f16-110">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b5f16-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b5f16-111">Selecteer in vervolgkeuzelijst **Producttype** de optie **Artikel** of **Service**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="b5f16-112">Selecteer in de vervolgkeuzelijst **Productsubtype** de optie **Product** (als het product geen varianten heeft) of **Productmodel** (als het product varianten heeft).</span><span class="sxs-lookup"><span data-stu-id="b5f16-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="b5f16-113">Voer in het vak **Productnummer** een productnummer in als dat nog niet is ingevuld.</span><span class="sxs-lookup"><span data-stu-id="b5f16-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="b5f16-114">Voer in het vak **Productnaam** een productnaam in.</span><span class="sxs-lookup"><span data-stu-id="b5f16-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="b5f16-115">Voer in het vak **Zoeknaam** een zoeknaam in.</span><span class="sxs-lookup"><span data-stu-id="b5f16-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="b5f16-116">Selecteer in de vervolgkeuzelijst **Retail-categorie** een geschikte categorie.</span><span class="sxs-lookup"><span data-stu-id="b5f16-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="b5f16-117">Als het product een kit is, selecteert u **Ja** bij **Productkit**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="b5f16-118">Als het productsubtype productmodel is, stelt u de **Productdimensiegroep** zo in dat de ondersteunde varianten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b5f16-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="b5f16-119">Opties zijn onder andere **Kleur**, **Grootte**, **Stijl** en **Configuratie**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="b5f16-120">Mogelijk moet u extra productdimensiegroepen maken.</span><span class="sxs-lookup"><span data-stu-id="b5f16-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="b5f16-121">Selecteer in de vervolgkeuzelijst **Configuratietechnologie** een geschikte optie.</span><span class="sxs-lookup"><span data-stu-id="b5f16-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="b5f16-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-122">Select **OK**.</span></span>

<span data-ttu-id="b5f16-123">De volgende afbeelding toont een voorbeeldproduct dat wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b5f16-123">The following image shows an example product being added.</span></span>

![Een product maken](media/create-new-product.png)

<span data-ttu-id="b5f16-125">Wanneer een product wordt toegevoegd, kunt u er extra gegevens voor instellen, zoals **Productbeschrijving**, **Variantgroepen**, **Dimensiegroepen**, **Productkenmerken** en **Gerelateerde producten**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="b5f16-126">In de volgende afbeelding ziet u de aanvullende gegevens van een product.</span><span class="sxs-lookup"><span data-stu-id="b5f16-126">The following image shows a product's additional details.</span></span>

![Productgegevens](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="b5f16-128">Productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="b5f16-128">Create product variants</span></span>

<span data-ttu-id="b5f16-129">Als het productsubtype **Productmodel** is, moeten er specifieke varianten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b5f16-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="b5f16-130">Volg deze stappen om productvarianten te maken.</span><span class="sxs-lookup"><span data-stu-id="b5f16-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="b5f16-131">Selecteer **Productvarianten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b5f16-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="b5f16-132">Als er variantgroepen in het actievenster zijn geselecteerd, selecteert u \**Variantsuggesties*.</span><span class="sxs-lookup"><span data-stu-id="b5f16-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="b5f16-133">Selecteer de varianten die u voor het product wilt ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="b5f16-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="b5f16-134">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="b5f16-135">Een product vrijgeven</span><span class="sxs-lookup"><span data-stu-id="b5f16-135">Release a product</span></span>

<span data-ttu-id="b5f16-136">Om een product te verkopen, moet het eerst aan een rechtspersoon worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="b5f16-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="b5f16-137">Selecteer **Producten vrijgeven** op de productpagina.</span><span class="sxs-lookup"><span data-stu-id="b5f16-137">From the product page, select **Release products**.</span></span>

    ![Product vrijgeven](media/create-new-product-3.png)

1. <span data-ttu-id="b5f16-139">Selecteer het product dat u wilt vrijgeven en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-139">Select the product to release, and then select **Next**.</span></span>

    ![Producten kiezen om vrij te geven](media/create-new-product-4.png)

1. <span data-ttu-id="b5f16-141">Selecteer de set productvarianten die u wilt vrijgeven en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Productvarianten kiezen om vrij te geven](media/create-new-product-5.png)

1. <span data-ttu-id="b5f16-143">Selecteer de rechtspersoon en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-143">Select the legal entity, and then select **Next**.</span></span>

    ![Rechtspersoon kiezen](media/create-new-product-6.png)

1. <span data-ttu-id="b5f16-145">Selecteer **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-145">Select **Finish**.</span></span>

    ![Productvrijgave voltooien](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="b5f16-147">Een vrijgegeven product configureren</span><span class="sxs-lookup"><span data-stu-id="b5f16-147">Configure a released product</span></span>

<span data-ttu-id="b5f16-148">Nadat een product is vrijgegeven, is er verdere configuratie nodig, zoals het toevoegen van een prijs aan het product.</span><span class="sxs-lookup"><span data-stu-id="b5f16-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="b5f16-149">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Vrijgegeven producten per categorie**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="b5f16-150">Selecteer het productcategorieknooppunt voor het product dat is vrijgegeven en selecteer het product in de productenlijst.</span><span class="sxs-lookup"><span data-stu-id="b5f16-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="b5f16-151">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b5f16-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="b5f16-152">Configureer in de sectie **Inkoop** eventuele vereiste eigenschappen, zoals **Eenheid**, **Prijs** en **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="b5f16-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="b5f16-153">Selecteer **Valideren** in het actievenster om ervoor te zorgen dat er geen fouten worden gemeld voor ontbrekende velden.</span><span class="sxs-lookup"><span data-stu-id="b5f16-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="b5f16-154">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b5f16-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="b5f16-155">In de volgende afbeelding ziet u een voorbeeldconfiguratie voor een vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="b5f16-155">The following image shows an example configuration for a released product.</span></span>

![Een vrijgegeven product configureren](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="b5f16-157">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b5f16-157">Additional resources</span></span>

[<span data-ttu-id="b5f16-158">Rechtspersonen maken</span><span class="sxs-lookup"><span data-stu-id="b5f16-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="b5f16-159">Een variantgroep maken</span><span class="sxs-lookup"><span data-stu-id="b5f16-159">Create a variant group</span></span>](create-variant-group.md) 

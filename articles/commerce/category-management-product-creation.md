---
title: Productcategorieën en producten beheren
description: In dit onderwerp wordt beschreven hoe merchandisingmanagers productcategorieën gebruiken om relaties tussen de producthiërarchie en vrijgegeven productdetails in Commerce te beheren.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 95a4bac6beeaf5fad449027d93132fc1499288a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215481"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="11f70-103">Productcategorieën en producten beheren</span><span class="sxs-lookup"><span data-stu-id="11f70-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="11f70-104">In dit onderwerp wordt een verbeterde manier beschreven om de productcategorieën en producten te beheren in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="11f70-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="11f70-105">Dankzij deze verbeteringen kunnen merchandisingmanagers een overzicht met producteigenschappen weergeven die worden gedeeld tussen de producthiërarchie en details van vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="11f70-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="11f70-106">Voor meer informatie over het beheren van productcategorieën selecteert u in het werkgebied **Categorie- en productbeheer** de tegel **Producthiërarchie in Commerce**.</span><span class="sxs-lookup"><span data-stu-id="11f70-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="11f70-107">U ziet de verbeterde structuur van de pagina **Producthiërarchie in Commerce**.</span><span class="sxs-lookup"><span data-stu-id="11f70-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="11f70-108">In eerdere versies van de app waren producteigenschappen onderverdeeld in *basisproducteigenschappen* en *detailhandelproducteigenschappen*, op basis van het bereik van hun toepassing.</span><span class="sxs-lookup"><span data-stu-id="11f70-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="11f70-109">Eigenschappen van detailhandelproducten zijn *globaal* in hun toepassingsbereik.</span><span class="sxs-lookup"><span data-stu-id="11f70-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="11f70-110">Dit betekent dat voor een bepaalde producteigenschap dezelfde waarde wordt gedeeld door alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="11f70-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="11f70-111">Basisproducteigenschappen daarentegen zijn *specifieke eigenschappen voor rechtspersonen*.</span><span class="sxs-lookup"><span data-stu-id="11f70-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="11f70-112">De waarde van een bepaalde basisproducteigenschap kan dus verschillen tussen rechtspersonen, op basis van individuele zakelijke behoeften van elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="11f70-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="11f70-113">Met de verbeterde opzet voor producteigenschappen blijven producteigenschappen logisch gescheiden, op basis van hun toepassing in een groep, om de formulierstructuur voor details van vrijgegeven producten te weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="11f70-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Groepering van de velden op basis van het toepassingsbereik van de eigenschappen](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="11f70-115">U kunt schakelen tussen het beheren van specifieke eigenschappen voor rechtspersonen voor alle rechtspersonen en het beheren van deze eigenschappen voor een specifieke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="11f70-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="11f70-116">Als u eigenschappen wilt beheren voor alle rechtspersonen, selecteert u **Weergeven voor alle rechtspersonen** (of **Bewerken voor alle rechtspersonen**).</span><span class="sxs-lookup"><span data-stu-id="11f70-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Weergeven/bewerken voor alle rechtspersonen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="11f70-118">Als u eigenschappen wilt beheren voor een specifieke rechtspersoon, selecteert u **Weergeven voor een specifieke rechtspersoon** (of **Bewerken voor een specifieke rechtspersoon**).</span><span class="sxs-lookup"><span data-stu-id="11f70-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Weergeven/bewerken voor een specifieke rechtspersoon](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="11f70-120">In de verbeterde productcategoriestructuur kan een merchandisingmanager nu ook standaardwaarden definiëren voor een aanvullende reeks producteigenschappen op het niveau van een individuele categorie.</span><span class="sxs-lookup"><span data-stu-id="11f70-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="11f70-121">Wanneer de producten worden gemaakt, nemen ze deze standaardwaarden voor producteigenschappen over, op basis van de koppeling van deze eigenschappen met een individuele categorie uit de producthiërarchie.</span><span class="sxs-lookup"><span data-stu-id="11f70-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="11f70-122">Deze overgenomen producteigenschappen kunnen ook worden aangepast voor elk product om te voldoen aan individuele zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="11f70-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="11f70-123">Eigenschappen selecteren om producten uit de pagina Productcategorie in Commerce bij te werken</span><span class="sxs-lookup"><span data-stu-id="11f70-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="11f70-124">Gebruik de nieuwe uitgebreide structuur voor producteigenschappen om te selecteren welke producteigenschappen moeten worden verplaatst naar de bijbehorende producten.</span><span class="sxs-lookup"><span data-stu-id="11f70-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="11f70-125">Op de pagina **Producthiërarchie in Commerce** selecteert u in het actievenster **Categorie** en vervolgens **Producten bijwerken** om het dialoogvenster **Producten bijwerken** te openen.</span><span class="sxs-lookup"><span data-stu-id="11f70-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Het dialoogvenster Producten bijwerken](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Productcategorieën en producten detailhandel beheren
description: In dit onderwerp wordt beschreven hoe merchandisingmanagers de detailhandelproductcategorieën gebruiken om relaties tussen de detailhandelproducthiërarchie en vrijgegeven productdetails te beheren.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "344680"
---
# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="d4f2a-103">Productcategorieën en producten detailhandel beheren</span><span class="sxs-lookup"><span data-stu-id="d4f2a-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="d4f2a-104">In dit onderwerp wordt een verbeterde manier beschreven om de detailhandelproductcategorieën en producten te beheren in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d4f2a-105">Dankzij deze verbeteringen kunnen merchandisingmanagers een overzicht met producteigenschappen weergeven die worden gedeeld tussen de detailhandelproducthiërarchie en details van vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="d4f2a-106">Voor meer informatie over het beheren van Retail-productcategorieën selecteert u in het werkgebied **Categorie- en productbeheer** de tegel **Producthiërarchie detailhandel**.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="d4f2a-107">U ziet de verbeterde structuur van de pagina **Producthiërarchie detailhandel**.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="d4f2a-108">In eerdere versies van Retail waren producteigenschappen onderverdeeld in *basisproducteigenschappen* en *detailhandelproducteigenschappen*, op basis van het bereik van hun toepassing.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="d4f2a-109">Eigenschappen van detailhandelproducten zijn *globaal* in hun toepassingsbereik.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="d4f2a-110">Dit betekent dat voor een bepaalde producteigenschap dezelfde waarde wordt gedeeld door alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="d4f2a-111">Basisproducteigenschappen daarentegen zijn *specifieke eigenschappen voor rechtspersonen*.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="d4f2a-112">De waarde van een bepaalde basisproducteigenschap kan dus verschillen tussen rechtspersonen, op basis van individuele zakelijke behoeften van elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="d4f2a-113">Met de verbeterde opzet voor producteigenschappen in de detailhandel blijven producteigenschappen logisch gescheiden, op basis van hun toepassing in een groep, om de formulierstructuur voor details van vrijgegeven producten te weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Groepering van de velden op basis van het toepassingsbereik van de eigenschappen](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="d4f2a-115">U kunt schakelen tussen het beheren van specifieke eigenschappen voor rechtspersonen voor alle rechtspersonen en het beheren van deze eigenschappen voor een specifieke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="d4f2a-116">Als u eigenschappen wilt beheren voor alle rechtspersonen, selecteert u **Weergeven voor alle rechtspersonen** (of **Bewerken voor alle rechtspersonen**).</span><span class="sxs-lookup"><span data-stu-id="d4f2a-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Weergeven/bewerken voor alle rechtspersonen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="d4f2a-118">Als u eigenschappen wilt beheren voor een specifieke rechtspersoon, selecteert u **Weergeven voor een specifieke rechtspersoon** (of **Bewerken voor een specifieke rechtspersoon**).</span><span class="sxs-lookup"><span data-stu-id="d4f2a-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Weergeven/bewerken voor een specifieke rechtspersoon](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="d4f2a-120">In de verbeterde productstructuur voor detailhandelproducten kan een merchandisingmanager nu ook standaardwaarden definiëren voor een aanvullende reeks producteigenschappen op het niveau van een individuele categorie.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="d4f2a-121">Wanneer de producten worden gemaakt, nemen ze deze standaardwaarden voor producteigenschappen over, op basis van de koppeling van deze eigenschappen met een individuele categorie uit de hiërarchie voor detailhandelproducten.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="d4f2a-122">Deze overgenomen producteigenschappen kunnen ook worden aangepast voor elk product om te voldoen aan individuele zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="d4f2a-123">Eigenschappen selecteren om producten uit de pagina Productcategorie van detailhandel bij te werken</span><span class="sxs-lookup"><span data-stu-id="d4f2a-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="d4f2a-124">Gebruik de nieuwe uitgebreide structuur voor producteigenschappen om te selecteren welke producteigenschappen moeten worden verplaatst naar de bijbehorende producten.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="d4f2a-125">Op de pagina **Producthiërarchie detailhandel** selecteert u in het actievenster **Categorie** en vervolgens **Producten bijwerken** om het dialoogvenster **Producten bijwerken** te openen.</span><span class="sxs-lookup"><span data-stu-id="d4f2a-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Het dialoogvenster Producten bijwerken](media/NewUpdateProductsEnhancedView.PNG)

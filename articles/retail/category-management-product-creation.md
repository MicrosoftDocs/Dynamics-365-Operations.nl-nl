---
title: Productcategoriebeheer
description: "In dit onderwerp wordt beschreven hoe merchandisingmanagers de detailhandelproductcategorieën gebruiken om relaties tussen de detailhandelproducthiërarchie en vrijgegeven productdetails te beheren."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: nl-nl
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="1ee46-103">Verbeterd categorie- en productbeheer</span><span class="sxs-lookup"><span data-stu-id="1ee46-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="1ee46-104">In dit onderwerp wordt een verbeterde manier beschreven om de detailhandelproductcategorieën en producten te beheren in Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1ee46-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="1ee46-105">Dankzij deze verbeteringen kunnen merchandisingmanagers een algemeen overzicht met producteigenschappen weergeven tussen de detailhandelproducthiërarchie en details van vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="1ee46-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="1ee46-106">Voor meer informatie over het beheren van detailhandelproductcategorieën gaat u naar **Producthiërarchie detailhandel** in het werkgebied **Categorie- en productbeheer** en geeft u de verbeterde structuur van de pagina **Productcategorie detailhandel** weer.</span><span class="sxs-lookup"><span data-stu-id="1ee46-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Werkgebied categorie- en productbeheer](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="1ee46-108">In eerdere versies waren producteigenschappen onderverdeeld in **basisproducteigenschappen** en **detailhandelproducteigenschappen**, op basis van het bereik van hun toepassing.</span><span class="sxs-lookup"><span data-stu-id="1ee46-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="1ee46-109">**Detailhandelproducteigenschappen** zijn *algemeen* voor het toepassingsbereik, wat inhoudt dat voor een bepaalde **detailhandelproducteigenschap** dezelfde waarde wordt gedeeld door alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="1ee46-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="1ee46-110">**Basisproducteigenschappen** zijn *specifieke eigenschappen voor rechtspersonen*.</span><span class="sxs-lookup"><span data-stu-id="1ee46-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="1ee46-111">De waarde van een bepaalde **basisproducteigenschap** kan dus verschillen tussen rechtspersonen, op basis van individuele zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="1ee46-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="1ee46-112">Met de verbeterde opzet voor producteigenschappen in de detailhandel blijven producteigenschappen logisch gescheiden, op basis van hun toepassing binnen een groep, om de formulierstructuur voor details van vrijgegeven producten te weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="1ee46-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Groepering van de velden op basis van hun toepassingsbereik](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="1ee46-114">U kunt schakelen tussen het beheren van specifieke eigenschappen voor rechtspersonen voor alle rechtspersonen en het beheren van deze eigenschappen voor een specifieke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="1ee46-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="1ee46-115">Selecteer hiervoor **Weergeven/bewerken voor alle rechtspersonen** of **Weergeven/bewerken voor een specifieke rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="1ee46-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Schakelen tussen één persoon en alle rechtspersonen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Schakelen tussen één persoon en alle rechtspersonen](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="1ee46-118">Ten opzichte van vorige versies kan een merchandisingmanager in de nieuwe productstructuur voor detailhandelproducten ook standaardwaarden definiëren voor een aanvullende reeks producteigenschappen op het niveau van een individuele categorie.</span><span class="sxs-lookup"><span data-stu-id="1ee46-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="1ee46-119">Bij het maken van producten worden deze standaardwaarden voor producteigenschappen overgenomen door een product, op basis van de koppeling met een individuele categorie uit de hiërarchie voor detailhandelproducten.</span><span class="sxs-lookup"><span data-stu-id="1ee46-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="1ee46-120">Deze overgenomen producteigenschappen kunnen ook worden aangepast voor elk product om te voldoen aan individuele zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="1ee46-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="1ee46-121">Eigenschappen selecteren om producten uit het formulier Productcategorie van detailhandel bij te werken</span><span class="sxs-lookup"><span data-stu-id="1ee46-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="1ee46-122">Gebruik de nieuwe uitgebreide structuur voor producteigenschappen om te selecteren welke producteigenschappen moeten worden verplaatst naar de bijbehorende producten.</span><span class="sxs-lookup"><span data-stu-id="1ee46-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Nieuwe uitgebreide weergave van Producten bijwerken](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="1ee46-124">Merchandisingmanagers kunnen deze overgenomen producteigenschappen voor elk product overnemen om te voldoen aan individuele zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="1ee46-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>



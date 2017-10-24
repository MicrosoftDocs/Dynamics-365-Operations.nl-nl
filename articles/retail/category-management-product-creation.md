---
title: "Productcategorieën beheren en maken"
description: "In dit onderwerp worden de verbeteringen beschreven die zijn aangebracht in de beheerervaring voor detailhandelproductcategorieën. Dankzij deze verbeteringen kunnen merchandisingmanagers een relatie tussen de detailhandelproducthiërarchie en details van vrijgegeven producten leggen."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: nl-nl
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="ebb15-104">Productcategorieën beheren en maken</span><span class="sxs-lookup"><span data-stu-id="ebb15-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="ebb15-105">Dankzij verbeteringen in de beheerervaring voor productcategorieën voor de detailhandel kunnen merchandisingmanagers een relatie tussen de detailhandelproducthiërarchie en details van vrijgegeven producten leggen.</span><span class="sxs-lookup"><span data-stu-id="ebb15-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="ebb15-106">Als u deze verbeteringen wilt bekijken, selecteert u in het werkgebied **Categorie- en productbeheer** de optie **Producthiërarchie detailhandel** om de nieuwe structuur van de pagina **Productcategorie van detailhandel** te bekijken.</span><span class="sxs-lookup"><span data-stu-id="ebb15-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="ebb15-107">In eerdere versies waren producteigenschappen onderverdeeld in basisproducteigenschappen en detailhandelproducteigenschappen, op basis van het bereik van hun toepassing.</span><span class="sxs-lookup"><span data-stu-id="ebb15-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="ebb15-108">Detailhandelproducteigenschappen waren *algemeen*.</span><span class="sxs-lookup"><span data-stu-id="ebb15-108">Retail product properties were *global*.</span></span> <span data-ttu-id="ebb15-109">Dit betekent dat voor een bepaalde producteigenschap dezelfde waarde wordt gedeeld door alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="ebb15-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="ebb15-110">Basisproducteigenschappen waren *specifieke eigenschappen voor rechtspersonen*.</span><span class="sxs-lookup"><span data-stu-id="ebb15-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="ebb15-111">De eigenschap van een bepaald product kan dus verschillen tussen rechtspersonen, op basis van individuele zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="ebb15-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="ebb15-112">Met deze verbeteringen voor producteigenschappen in de detailhandelproductcategorie blijven we de velden scheiden, op basis van hun toepassing binnen een groep, om de formulierstructuur voor details van vrijgegeven producten te weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="ebb15-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="ebb15-113">U kunt schakelen tussen het beheren van specifieke eigenschappen voor rechtspersonen voor alle rechtspersonen en het beheren van deze eigenschappen voor een specifieke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ebb15-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="ebb15-114">Selecteer **Weergeven/bewerken voor alle rechtspersonen** of **Weergeven/bewerken voor een specifieke rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="ebb15-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="ebb15-115">Merchandisingmanagers kunnen ook standaardwaarden voor een aanvullende reeks producteigenschappen op het niveau van een individuele categorie definiëren.</span><span class="sxs-lookup"><span data-stu-id="ebb15-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="ebb15-116">Waarden van deze eigenschappen worden overgenomen door een product, op basis van hun koppeling met een categorie op het moment dat het product is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ebb15-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="ebb15-117">Eigenschappen selecteren om producten uit het formulier Productcategorie van detailhandel bij te werken</span><span class="sxs-lookup"><span data-stu-id="ebb15-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="ebb15-118">U kunt logische groeperingseigenschappen gebruiken om op te geven welke producteigenschappen moeten worden doorgegeven aan gekoppelde producten.</span><span class="sxs-lookup"><span data-stu-id="ebb15-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="ebb15-119">Merchandisingmanagers kunnen deze overgenomen producteigenschappen voor elk product overnemen om te voldoen aan individuele zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="ebb15-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


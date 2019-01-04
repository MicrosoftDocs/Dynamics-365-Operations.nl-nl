---
title: "Detailhandelhiërarchieën"
description: "In dit artikel worden detailhandelhiërarchieën in Microsoft Dynamics 365 for Retail beschreven."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 198c8da336f3e225c5d6da2eb02c86581dc9b4d6
ms.contentlocale: nl-nl
ms.lasthandoff: 01/04/2019

---

# <a name="retail-hierarchies"></a><span data-ttu-id="33d2a-103">Detailhandelhiërarchieën</span><span class="sxs-lookup"><span data-stu-id="33d2a-103">Retail hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33d2a-104">In dit artikel worden detailhandelhiërarchieën in Microsoft Dynamics 365 for Retail beschreven.</span><span class="sxs-lookup"><span data-stu-id="33d2a-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="33d2a-105">U kunt één detailhandelcategoriehiërarchie maken om alle producten die u via uw detailhandelkanalen verkoopt, in te delen.</span><span class="sxs-lookup"><span data-stu-id="33d2a-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="33d2a-106">U kunt detailhandelproducthiërarchieën gebruiken voor het categoriseren of groeperen van producten.</span><span class="sxs-lookup"><span data-stu-id="33d2a-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="33d2a-107">Deze producten kunt u vervolgens gebruiken om productassortimenten en klantloyaliteitsprogramma's te maken.</span><span class="sxs-lookup"><span data-stu-id="33d2a-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="33d2a-108">U kunt tevens productkenmerken en -eigenschappen toewijzen, een prijsstructuur toewijzen, de producten in productpromoties opnemen en producten gebruiken voor rapportages.</span><span class="sxs-lookup"><span data-stu-id="33d2a-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="33d2a-109">U kunt één detailhandelcategoriehiërarchie maken die alle producten en categorieën in uw organisatie vertegenwoordigt. U kunt deze categoriehiërarchie vervolgens voor meerdere doeleinden gebruiken.</span><span class="sxs-lookup"><span data-stu-id="33d2a-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="33d2a-110">Het is ook mogelijk om meerdere detailhandelcategoriehiërarchieën te maken voor speciale doeleinden, zoals productpromoties.</span><span class="sxs-lookup"><span data-stu-id="33d2a-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="33d2a-111">Als u een detailhandelproducthiërarchie maakt, moet u een type categoriehiërarchie toewijzen om het doel van de categoriehiërarchie te identificeren.</span><span class="sxs-lookup"><span data-stu-id="33d2a-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="33d2a-112">Er wordt bijvoorbeeld alleen naar producthiërarchieën verwezen die het type **Detailhandelnavigatiehïerarchie** hebben toegewezen gekregen wanneer u online of in een verkooppunt in producten op categorie bladert.</span><span class="sxs-lookup"><span data-stu-id="33d2a-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="33d2a-113">Typen detailhandelhiërarchie</span><span class="sxs-lookup"><span data-stu-id="33d2a-113">Retail hierarchy types</span></span>

<span data-ttu-id="33d2a-114">In de volgende tabel worden de beschikbare typen detailhandelcategoriehiërarchieën en het algemene doel van de afzonderlijke typen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="33d2a-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="33d2a-115">Type categoriehiërarchie</span><span class="sxs-lookup"><span data-stu-id="33d2a-115">Category hierarchy type</span></span>       | <span data-ttu-id="33d2a-116">Doel</span><span class="sxs-lookup"><span data-stu-id="33d2a-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="33d2a-117">Producthiërarchie detailhandel</span><span class="sxs-lookup"><span data-stu-id="33d2a-117">Retail product hierarchy</span></span>      | <span data-ttu-id="33d2a-118">Gebruik dit hiërarchietype om de algemene producthiërarchie voor uw organisatie te definiëren.</span><span class="sxs-lookup"><span data-stu-id="33d2a-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="33d2a-119">U kunt dit hiërarchietype gebruiken voor merchandising, prijzen en promoties, rapportage en assortimentplanning.</span><span class="sxs-lookup"><span data-stu-id="33d2a-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="33d2a-120">Er kan aan dit hiërarchietype slechts één detailhandelproducthiërarchie worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="33d2a-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="33d2a-121">Aanvullende detailhandelhiërarchie</span><span class="sxs-lookup"><span data-stu-id="33d2a-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="33d2a-122">Gebruik dit hiërarchietype voor eventuele aanvullende detailhandelcategoriehiërarchieën die u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="33d2a-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="33d2a-123">In de lente is er bijvoorbeeld een promotie voor zwemkleding.</span><span class="sxs-lookup"><span data-stu-id="33d2a-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="33d2a-124">Daarom neemt u uw zwemkledingproducten op in een aparte categoriehiërarchie en past u speciale promotieprijzen toe op de verschillende productcategorieën.</span><span class="sxs-lookup"><span data-stu-id="33d2a-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="33d2a-125">Detailhandelnavigatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="33d2a-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="33d2a-126">Gebruik dit hiërarchietype om producten te groeperen en organiseren in categorieën zodat u online of in POS in producten kunt bladeren.</span><span class="sxs-lookup"><span data-stu-id="33d2a-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="33d2a-127">U kunt gebruikmaken van een detailhandelcategoriehiërarchie voor het structureren van uw producten, zodat u productkenmerken en -eigenschappen kunt instellen en onderhouden op het categorieniveau.</span><span class="sxs-lookup"><span data-stu-id="33d2a-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="33d2a-128">Deze kenmerken en eigenschappen omvatten instellingen voor productdimensies en POS-instellingen.</span><span class="sxs-lookup"><span data-stu-id="33d2a-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="33d2a-129">Alle producten die u aan de categorieën toewijst, nemen de kenmerken en eigenschappen die u definieert automatisch over.</span><span class="sxs-lookup"><span data-stu-id="33d2a-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="33d2a-130">Het is ook mogelijk om de eigenschapinstellingen van een product naar meerdere producten tegelijk in een geselecteerde categorie te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="33d2a-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>


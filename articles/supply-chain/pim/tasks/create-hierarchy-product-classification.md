---
title: Een hiërarchie van productclassificatie maken
description: Deze procedure laat zien hoe u een nieuwe categoriehiërarchie maakt en een type hiërarchie van basisproductcodes toewijst.
author: ShylaThompson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4e2fdc62d7faa73efa78092d7754d3fa1213a94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809369"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="aa1d5-103">Een hiërarchie van productclassificatie maken</span><span class="sxs-lookup"><span data-stu-id="aa1d5-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa1d5-104">Deze procedure laat zien hoe u een nieuwe categoriehiërarchie maakt en een type hiërarchie van basisproductcodes toewijst.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="aa1d5-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aa1d5-106">Deze procedure is bedoeld voor de categoriebeheerder.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="aa1d5-107">De nieuwe categoriehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="aa1d5-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="aa1d5-108">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Instellen > Categorieën en kenmerken > Categoriehiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="aa1d5-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-109">Click **New**.</span></span>
3. <span data-ttu-id="aa1d5-110">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="aa1d5-111">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="aa1d5-112">Klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="aa1d5-113">De hiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="aa1d5-113">Build the hierarchy</span></span>
1. <span data-ttu-id="aa1d5-114">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-114">Click **New** category node.</span></span>
2. <span data-ttu-id="aa1d5-115">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="aa1d5-116">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="aa1d5-117">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="aa1d5-118">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-118">Click **New** category node.</span></span>
6. <span data-ttu-id="aa1d5-119">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="aa1d5-120">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="aa1d5-121">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="aa1d5-122">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-122">Click **New** category node.</span></span>
10. <span data-ttu-id="aa1d5-123">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="aa1d5-124">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="aa1d5-125">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="aa1d5-126">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-126">Click **New** category node.</span></span>
14. <span data-ttu-id="aa1d5-127">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="aa1d5-128">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="aa1d5-129">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="aa1d5-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="aa1d5-131">De hiërarchie classificeren</span><span class="sxs-lookup"><span data-stu-id="aa1d5-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="aa1d5-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="aa1d5-133">Klik in het **Actievenster** op **Categoriehiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="aa1d5-134">Klik op **Hiërarchietype koppelen**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="aa1d5-135">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-135">Click **New**.</span></span>
5. <span data-ttu-id="aa1d5-136">Selecteer een optie in het veld **Type categoriehiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="aa1d5-137">Selecteer het type **Type categoriehiërarchie van basisproduct voor productclassificatie**.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="aa1d5-138">Klik in het veld **Categoriehiërarchie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aa1d5-139">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="aa1d5-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="aa1d5-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="aa1d5-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
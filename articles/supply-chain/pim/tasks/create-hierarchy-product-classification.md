---
title: Een hiërarchie van productclassificatie maken
description: Deze procedure laat zien hoe u een nieuwe categoriehiërarchie maakt en een type hiërarchie van basisproductcodes toewijst.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74be72ac5787273e13692abdb9db18be4c5ccc08
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966950"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="95c1b-103">Een hiërarchie van productclassificatie maken</span><span class="sxs-lookup"><span data-stu-id="95c1b-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95c1b-104">Deze procedure laat zien hoe u een nieuwe categoriehiërarchie maakt en een type hiërarchie van basisproductcodes toewijst.</span><span class="sxs-lookup"><span data-stu-id="95c1b-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="95c1b-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="95c1b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="95c1b-106">Deze procedure is bedoeld voor de categoriebeheerder.</span><span class="sxs-lookup"><span data-stu-id="95c1b-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="95c1b-107">De nieuwe categoriehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="95c1b-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="95c1b-108">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Instellen > Categorieën en kenmerken > Categoriehiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="95c1b-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-109">Click **New**.</span></span>
3. <span data-ttu-id="95c1b-110">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="95c1b-111">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="95c1b-112">Klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="95c1b-113">De hiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="95c1b-113">Build the hierarchy</span></span>
1. <span data-ttu-id="95c1b-114">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="95c1b-114">Click **New** category node.</span></span>
2. <span data-ttu-id="95c1b-115">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="95c1b-116">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="95c1b-117">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="95c1b-118">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="95c1b-118">Click **New** category node.</span></span>
6. <span data-ttu-id="95c1b-119">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="95c1b-120">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="95c1b-121">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="95c1b-122">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="95c1b-122">Click **New** category node.</span></span>
10. <span data-ttu-id="95c1b-123">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="95c1b-124">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="95c1b-125">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="95c1b-126">Klik op **Nieuw** categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="95c1b-126">Click **New** category node.</span></span>
14. <span data-ttu-id="95c1b-127">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="95c1b-128">Typ in het veld **Code** een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="95c1b-129">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="95c1b-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="95c1b-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="95c1b-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="95c1b-131">De hiërarchie classificeren</span><span class="sxs-lookup"><span data-stu-id="95c1b-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="95c1b-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="95c1b-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="95c1b-133">Klik in het **Actievenster** op **Categoriehiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="95c1b-134">Klik op **Hiërarchietype koppelen**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="95c1b-135">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-135">Click **New**.</span></span>
5. <span data-ttu-id="95c1b-136">Selecteer een optie in het veld **Type categoriehiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="95c1b-137">Selecteer het type **Type categoriehiërarchie van basisproduct voor productclassificatie**.</span><span class="sxs-lookup"><span data-stu-id="95c1b-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="95c1b-138">Klik in het veld **Categoriehiërarchie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="95c1b-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="95c1b-139">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="95c1b-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="95c1b-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="95c1b-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="95c1b-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="95c1b-141">Close the page.</span></span>


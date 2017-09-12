--- 
title: "Een hiërarchie van productclassificatie maken"
description: "Deze procedure laat zien hoe u een nieuwe categoriehiërarchie maakt en een type hiërarchie van basisproductcodes toewijst."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="9d8b9-103">Een hiërarchie van productclassificatie maken</span><span class="sxs-lookup"><span data-stu-id="9d8b9-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d8b9-104">Deze procedure laat zien hoe u een nieuwe categoriehiërarchie maakt en een type hiërarchie van basisproductcodes toewijst.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="9d8b9-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9d8b9-106">Deze procedure is bedoeld voor de categoriebeheerder.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="9d8b9-107">De nieuwe categoriehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="9d8b9-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="9d8b9-108">Ga naar Productgegevensbeheer > Instellingen > Categorieën en kenmerken > Categoriehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="9d8b9-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-109">Click New.</span></span>
3. <span data-ttu-id="9d8b9-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9d8b9-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9d8b9-112">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="9d8b9-113">De hiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="9d8b9-113">Build the hierarchy</span></span>
1. <span data-ttu-id="9d8b9-114">Klik op Nieuw categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-114">Click New category node.</span></span>
2. <span data-ttu-id="9d8b9-115">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="9d8b9-116">Typ een waarde in het veld Code.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="9d8b9-117">Typ een waarde in het veld Beschrijvende naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="9d8b9-118">Klik op Nieuw categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-118">Click New category node.</span></span>
6. <span data-ttu-id="9d8b9-119">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="9d8b9-120">Typ een waarde in het veld Code.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="9d8b9-121">Typ een waarde in het veld Beschrijvende naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="9d8b9-122">Klik op Nieuw categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-122">Click New category node.</span></span>
10. <span data-ttu-id="9d8b9-123">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="9d8b9-124">Typ een waarde in het veld Code.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="9d8b9-125">Typ een waarde in het veld Beschrijvende naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="9d8b9-126">Klik op Nieuw categorieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-126">Click New category node.</span></span>
14. <span data-ttu-id="9d8b9-127">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="9d8b9-128">Typ een waarde in het veld Code.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="9d8b9-129">Typ een waarde in het veld Beschrijvende naam.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="9d8b9-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="9d8b9-131">De hiërarchie classificeren</span><span class="sxs-lookup"><span data-stu-id="9d8b9-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="9d8b9-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="9d8b9-133">Klik in het actievenster op Categoriehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="9d8b9-134">Klik op Gekoppeld hiërarchietype.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="9d8b9-135">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-135">Click New.</span></span>
5. <span data-ttu-id="9d8b9-136">Selecteer een optie in het veld Type categoriehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="9d8b9-137">Selecteer het type hiërarchie van basisproductcodes voor productclassificatie.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="9d8b9-138">Klik in het veld Categoriehiërarchie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9d8b9-139">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9d8b9-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9d8b9-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-141">Close the page.</span></span>



--- 
title: Een recordsjabloon maken om de invoer van gegevens te vergemakkelijken
description: In deze procedure wordt voorgedaan hoe u een recordsjabloon kunt maken, zodat vaak gebruikte veldwaarden niet expliciet moeten worden ingevoerd voor elke nieuwe record.
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6f8d804133f8e9c6f47420d41df8d9430381e2fe
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="9ee1e-103">Een recordsjabloon maken om de invoer van gegevens te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="9ee1e-103">Create a record template to facilitate data entry</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ee1e-104">In deze procedure wordt voorgedaan hoe u een recordsjabloon kunt maken, zodat vaak gebruikte veldwaarden niet expliciet moeten worden ingevoerd voor elke nieuwe record.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="9ee1e-105">In deze procedure maakt u een nieuwe record voor nieuwe laptops die u wilt laten toevoegen aan uw vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="9ee1e-106">In deze procedure wordt het voorbeeldbedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="9ee1e-107">Ga naar Vaste activa > Vaste activa > Vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="9ee1e-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-108">Click New.</span></span>
3. <span data-ttu-id="9ee1e-109">Typ of selecteer een waarde in het veld Groep vaste activa.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="9ee1e-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9ee1e-111">Voer bijvoorbeeld 'Corporate lead-laptop' in.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="9ee1e-112">Typ een waarde in het veld Zoeknaam.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="9ee1e-113">Voer bijvoorbeeld 'laptop' in.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="9ee1e-114">Vouw de sectie Technische informatie uit.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="9ee1e-115">Typ een waarde in het veld Merk.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="9ee1e-116">Typ een waarde in het veld Model.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="9ee1e-117">Typ een waarde in het veld Bouwjaar.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="9ee1e-118">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="9ee1e-119">Klik op Recordinfo.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-119">Click Record info.</span></span>
12. <span data-ttu-id="9ee1e-120">Klik op Gebruikersjabloon.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-120">Click User template.</span></span>
13. <span data-ttu-id="9ee1e-121">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9ee1e-122">Voer bijvoorbeeld 'Corporate laptop' in.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="9ee1e-123">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9ee1e-124">Voer bijvoorbeeld 'Corporate laptop' in.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="9ee1e-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-125">Click OK.</span></span>
16. <span data-ttu-id="9ee1e-126">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="9ee1e-126">Click Close.</span></span>



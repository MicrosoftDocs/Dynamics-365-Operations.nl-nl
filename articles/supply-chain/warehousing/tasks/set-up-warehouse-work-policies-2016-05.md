--- 
title: 'Werkbeleid magazijn instellen '
description: In magazijnprocessen wordt niet altijd magazijnwerk opgenomen.
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 22e359ee2ded2315c588c2dd5c3d62dee0440adf
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="998d0-103">Werkbeleid magazijn instellen </span><span class="sxs-lookup"><span data-stu-id="998d0-103">Set up warehouse work policies</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="998d0-104">In magazijnprocessen wordt niet altijd magazijnwerk opgenomen.</span><span class="sxs-lookup"><span data-stu-id="998d0-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="998d0-105">Door een werkbeleid te definiëren kunt u voorkomen dat werk wordt gemaakt voor het verzamelen en wegzetten van grondstoffen voor afgewerkte goederen voor een reeks producten op specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="998d0-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="998d0-106">Het demobedrijf USMF is gebruikt om deze registratie te maken.</span><span class="sxs-lookup"><span data-stu-id="998d0-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="998d0-107">Voor deze taakbegeleiding is de toepassing Dynamics AX 7.0.1 of later vereist.</span><span class="sxs-lookup"><span data-stu-id="998d0-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="998d0-108">Ga naar Magazijnbeheer > Instellingen > Werk > Werkbeleid.</span><span class="sxs-lookup"><span data-stu-id="998d0-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="998d0-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="998d0-109">Click New.</span></span>
3. <span data-ttu-id="998d0-110">Typ in het veld Werkbeleidsnaam 'Geen weggezet werk'.</span><span class="sxs-lookup"><span data-stu-id="998d0-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="998d0-111">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="998d0-111">Click Save.</span></span>
5. <span data-ttu-id="998d0-112">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="998d0-112">Click Add.</span></span>
6. <span data-ttu-id="998d0-113">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="998d0-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="998d0-114">Selecteer in het veld Werkordertype 'Eindproducten wegzetten'.</span><span class="sxs-lookup"><span data-stu-id="998d0-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="998d0-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="998d0-115">Click Add.</span></span>
9. <span data-ttu-id="998d0-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="998d0-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="998d0-117">Selecteer in het veld Werkordertype 'Coproducten en bijproducten wegzetten'.</span><span class="sxs-lookup"><span data-stu-id="998d0-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="998d0-118">Vouw de sectie Voorraadlocaties uit.</span><span class="sxs-lookup"><span data-stu-id="998d0-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="998d0-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="998d0-119">Click Add.</span></span>
13. <span data-ttu-id="998d0-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="998d0-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="998d0-121">Voer in de magazijnlijst '51' in.</span><span class="sxs-lookup"><span data-stu-id="998d0-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="998d0-122">Typ of selecteer '001' in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="998d0-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="998d0-123">Vouw de sectie Producten uit.</span><span class="sxs-lookup"><span data-stu-id="998d0-123">Expand the Products section.</span></span>
17. <span data-ttu-id="998d0-124">Selecteer 'Geselecteerd' in het veld Productselectie.</span><span class="sxs-lookup"><span data-stu-id="998d0-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="998d0-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="998d0-125">Click Add.</span></span>
19. <span data-ttu-id="998d0-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="998d0-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="998d0-127">Typ of selecteer 'L0101' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="998d0-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="998d0-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="998d0-128">Click Save.</span></span>



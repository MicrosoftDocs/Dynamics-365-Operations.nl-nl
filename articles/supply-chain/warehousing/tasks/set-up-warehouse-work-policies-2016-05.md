---
title: De magazijnwerkbeleidsregels (toepassing, mei 2016)
description: In magazijnprocessen wordt niet altijd magazijnwerk opgenomen.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "335319"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="8eb95-103">De magazijnwerkbeleidsregels (toepassing, mei 2016)</span><span class="sxs-lookup"><span data-stu-id="8eb95-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8eb95-104">In magazijnprocessen wordt niet altijd magazijnwerk opgenomen.</span><span class="sxs-lookup"><span data-stu-id="8eb95-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="8eb95-105">Door een werkbeleid te definiëren kunt u voorkomen dat werk wordt gemaakt voor het verzamelen en wegzetten van grondstoffen voor afgewerkte goederen voor een reeks producten op specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="8eb95-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="8eb95-106">Het demobedrijf USMF is gebruikt om deze registratie te maken.</span><span class="sxs-lookup"><span data-stu-id="8eb95-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="8eb95-107">Voor deze taakbegeleiding is de toepassing Dynamics AX 7.0.1 of hoger vereist.</span><span class="sxs-lookup"><span data-stu-id="8eb95-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="8eb95-108">Ga naar Magazijnbeheer > Instellingen > Werk > Werkbeleid.</span><span class="sxs-lookup"><span data-stu-id="8eb95-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="8eb95-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8eb95-109">Click New.</span></span>
3. <span data-ttu-id="8eb95-110">Typ in het veld Werkbeleidsnaam 'Geen weggezet werk'.</span><span class="sxs-lookup"><span data-stu-id="8eb95-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="8eb95-111">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8eb95-111">Click Save.</span></span>
5. <span data-ttu-id="8eb95-112">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8eb95-112">Click Add.</span></span>
6. <span data-ttu-id="8eb95-113">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8eb95-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="8eb95-114">Selecteer in het veld Werkordertype 'Eindproducten wegzetten'.</span><span class="sxs-lookup"><span data-stu-id="8eb95-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="8eb95-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8eb95-115">Click Add.</span></span>
9. <span data-ttu-id="8eb95-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8eb95-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="8eb95-117">Selecteer in het veld Werkordertype 'Coproducten en bijproducten wegzetten'.</span><span class="sxs-lookup"><span data-stu-id="8eb95-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="8eb95-118">Vouw de sectie Voorraadlocaties uit.</span><span class="sxs-lookup"><span data-stu-id="8eb95-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="8eb95-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8eb95-119">Click Add.</span></span>
13. <span data-ttu-id="8eb95-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8eb95-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="8eb95-121">Voer in de magazijnlijst '51' in.</span><span class="sxs-lookup"><span data-stu-id="8eb95-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="8eb95-122">Typ of selecteer '001' in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="8eb95-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="8eb95-123">Vouw de sectie Producten uit.</span><span class="sxs-lookup"><span data-stu-id="8eb95-123">Expand the Products section.</span></span>
17. <span data-ttu-id="8eb95-124">Selecteer 'Geselecteerd' in het veld Productselectie.</span><span class="sxs-lookup"><span data-stu-id="8eb95-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="8eb95-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8eb95-125">Click Add.</span></span>
19. <span data-ttu-id="8eb95-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8eb95-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="8eb95-127">Typ of selecteer 'L0101' in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="8eb95-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="8eb95-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8eb95-128">Click Save.</span></span>


--- 
title: Geavanceerde regels voor journalen maken
description: Deze procedure begeleidt u bij het maken van geavanceerde regels voor journalen.
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1bb1663b0f5d7e6a550e1ffd2ee2edf3771a13b3
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="ffbc1-103">Geavanceerde regels voor journalen maken</span><span class="sxs-lookup"><span data-stu-id="ffbc1-103">Create advanced rules for journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffbc1-104">Deze procedure begeleidt u bij het maken van geavanceerde regels voor journalen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="ffbc1-105">Dit omvat het instellen van journaalcontrole en boekingsbeperkingen voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="ffbc1-106">Deze procedure gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="ffbc1-107">Journaalcontrole instellen</span><span class="sxs-lookup"><span data-stu-id="ffbc1-107">Set up journal control</span></span>
1. <span data-ttu-id="ffbc1-108">Ga naar Grootboek > Journaalinstellingen > Journaalnamen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="ffbc1-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ffbc1-110">Klik op Journaalcontrole.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-110">Click Journal control.</span></span>
4. <span data-ttu-id="ffbc1-111">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-111">Click Add.</span></span>
5. <span data-ttu-id="ffbc1-112">Klik in het veld Bedrijfsrekeningen op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ffbc1-113">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ffbc1-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ffbc1-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-115">Click Add.</span></span>
9. <span data-ttu-id="ffbc1-116">Klik in het veld Rekeningstructuur op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ffbc1-117">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="ffbc1-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ffbc1-119">Klik in het veld Segment op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="ffbc1-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ffbc1-121">Klik in het veld Vanaf waarde op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ffbc1-122">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="ffbc1-123">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="ffbc1-124">Klik in het veld Tot waarde op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="ffbc1-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="ffbc1-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="ffbc1-127">Boekingsbeperkingen instellen</span><span class="sxs-lookup"><span data-stu-id="ffbc1-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="ffbc1-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-128">Close the page.</span></span>
2. <span data-ttu-id="ffbc1-129">Klik op Boekingsbeperkingen.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="ffbc1-130">Selecteer Per gebruikersgroep in Hoe wilt u de boekingsbeperkingen instellen?</span><span class="sxs-lookup"><span data-stu-id="ffbc1-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="ffbc1-131">Schakel in de structuur het selectievakje 'de groep waarvoor u boeking voor deze journaalnaam wilt toestaan.' in.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="ffbc1-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-132">Click OK.</span></span>



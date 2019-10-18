---
title: Geavanceerde regels voor journalen maken
description: Deze procedure begeleidt u bij het maken van geavanceerde regels voor journalen.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3eb34ac419aeab3663a8931d022abf7bcbfddd37
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186228"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="f0d7d-103">Geavanceerde regels voor journalen maken</span><span class="sxs-lookup"><span data-stu-id="f0d7d-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0d7d-104">Deze procedure begeleidt u bij het maken van geavanceerde regels voor journalen.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="f0d7d-105">Dit omvat het instellen van journaalcontrole en boekingsbeperkingen voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="f0d7d-106">Deze procedure gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="f0d7d-107">Journaalcontrole instellen</span><span class="sxs-lookup"><span data-stu-id="f0d7d-107">Set up journal control</span></span>
1. <span data-ttu-id="f0d7d-108">Ga in het **navigatievenster** naar **Modules > Grootboek > Journaalinstellingen > Journaalnamen**.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="f0d7d-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f0d7d-110">Klik in het **actievenster** op **Journaalcontrole**.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="f0d7d-111">Klik op het sneltabblad **Welke rekeningtypen kunnen worden geboekt?** op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="f0d7d-112">Klik in het veld **Bedrijfsrekeningen** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f0d7d-113">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f0d7d-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f0d7d-115">Klik op het sneltabblad **Welke segmentwaarden zijn geldig voor dit journaal?** op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="f0d7d-116">Klik in het veld **Rekeningstructuur** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f0d7d-117">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f0d7d-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f0d7d-119">Klik in het veld **Segment** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f0d7d-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f0d7d-121">Klik in het veld **Vanaf waarde** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f0d7d-122">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f0d7d-123">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f0d7d-124">Klik in het veld **Tot waarde** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="f0d7d-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="f0d7d-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="f0d7d-127">Boekingsbeperkingen instellen</span><span class="sxs-lookup"><span data-stu-id="f0d7d-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="f0d7d-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-128">Close the page.</span></span>
2. <span data-ttu-id="f0d7d-129">Klik op **Boekingsbeperkingen**.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="f0d7d-130">Selecteer Per gebruikersgroep in **Hoe wilt u de boekingsbeperkingen instellen?**</span><span class="sxs-lookup"><span data-stu-id="f0d7d-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="f0d7d-131">Schakel in de structuur het selectievakje 'de groep waarvoor u boeking voor deze journaalnaam wilt toestaan.' in.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="f0d7d-132">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0d7d-132">Click **OK**.</span></span>


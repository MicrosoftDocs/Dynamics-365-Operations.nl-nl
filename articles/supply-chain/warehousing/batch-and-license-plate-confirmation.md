---
title: Bevestiging van batch en nummerplaat
description: In dit onderwerp wordt beschreven hoe u bevestiging van batch en nummerplaat instelt en toepast vanaf een mobiel apparaat.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6454335989fe03a7332b6fb956667850896ffaf4
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="690f2-103">Bevestiging van batch en nummerplaat</span><span class="sxs-lookup"><span data-stu-id="690f2-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="690f2-104">Met batchbevestiging kunt u bevestigen dat de juiste batch van het mobiele apparaat wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="690f2-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="690f2-105">Tijdens de eerste verzameling van werk voor alleen batch erboven-items waarbij batch erboven aangeeft dat de rangorde van de batch hoger is dan de locatie in de zoekhiërarchie, moet u controleren of de verzamelde batch overeenkomt met de batch op de werkregel.</span><span class="sxs-lookup"><span data-stu-id="690f2-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="690f2-106">Met bevestiging van nummerplaat kunt u bevestigen dat de juiste nummerplaat van het mobiele apparaat wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="690f2-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="690f2-107">Bij het verzamelen van werk vanaf een faseringslocatie moet u controleren of de nummerplaat die wordt verzameld, overeenkomt met de nummerplaat die aan het werk is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="690f2-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="690f2-108">Als het werk wordt gestart door een nummerplaat te scannen, wordt deze bevestigingsstap overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="690f2-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="690f2-109">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="690f2-109">Where it applies</span></span>
<span data-ttu-id="690f2-110">Bevestiging is van toepassing in de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="690f2-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="690f2-111">Batchbevestiging is van toepassing op de eerste verzamelingen van werk voor batch erboven-items.</span><span class="sxs-lookup"><span data-stu-id="690f2-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="690f2-112">Nummerplaatbevestiging is van toepassing op verzamelingen van faseringslocaties.</span><span class="sxs-lookup"><span data-stu-id="690f2-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="690f2-113">Bevestiging van batch en nummerplaat instellen</span><span class="sxs-lookup"><span data-stu-id="690f2-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="690f2-114">U kunt de batch- en nummerplaatbevestiging configureren via de menuopties van mobiele apparaten.</span><span class="sxs-lookup"><span data-stu-id="690f2-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="690f2-115">Voer de menuopties voor het mobiele apparaat onder de werkbevestigingsinstellingen in.</span><span class="sxs-lookup"><span data-stu-id="690f2-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="690f2-116">Selecteer de optie voor batch- of nummerplaatbevestiging.</span><span class="sxs-lookup"><span data-stu-id="690f2-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="690f2-117">Beide opties zijn beschikbaar voor verzamelingen van het werktype waarvoor geen automatische bevestiging is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="690f2-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


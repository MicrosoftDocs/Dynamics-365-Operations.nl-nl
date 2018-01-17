---
title: Weergave oudere batches in magazijn op een mobiel apparaat configureren
description: In dit onderwerp wordt beschreven hoe u een mobiel apparaat instelt voor het weergeven van locaties met batches die ouder zijn dan de huidige locatie van een werkregel.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations, Core
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 68477589ee43dcd7d6258ad259d2f0b8cf0050ca
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="a5555-103">Weergave oudere batches in magazijn op een mobiel apparaat configureren</span><span class="sxs-lookup"><span data-stu-id="a5555-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a5555-104">Met de configuratie van **Weergave oudere batches in magazijn** kunt u een lijst met locaties weergeven met batches die ouder zijn dan de huidige locatie van de werkregel.</span><span class="sxs-lookup"><span data-stu-id="a5555-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="a5555-105">De lijst met locaties die wordt weergegeven bevat informatie over de batches die ouder zijn op de locatie met de vervaldatum en de fysieke voorraad van elke batch.</span><span class="sxs-lookup"><span data-stu-id="a5555-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="a5555-106">U kunt kiezen om uit een nieuwe locatie te verzamelen of door te gaan met de huidige locatie.</span><span class="sxs-lookup"><span data-stu-id="a5555-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="a5555-107">In een nieuwe locatie verzamelen: als u een nieuwe locatie voor het verzamelen selecteert, wordt de huidige werkregel bijgewerkt met de nieuwe locatie en wordt het werk zoals gebruikelijk voortgezet met de nieuwe locatie.</span><span class="sxs-lookup"><span data-stu-id="a5555-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="a5555-108">De nieuwe locatie is alleen geldig als er een voldoende beschikbare hoeveelheid is voor de hele werkregel.</span><span class="sxs-lookup"><span data-stu-id="a5555-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="a5555-109">Als de vereiste hoeveelheid niet beschikbaar is, wordt de werkregel niet bijgewerkt en wordt de lijst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a5555-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="a5555-110">Doorgaan met orderverzamelen van de huidige locatie: als u met de huidige locatie van de werkregel doorgaat, worden de hoeveelheden voor de werkregel van de oorspronkelijke locatie verzameld.</span><span class="sxs-lookup"><span data-stu-id="a5555-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a5555-111">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="a5555-111">Where it applies</span></span>
<span data-ttu-id="a5555-112">Oudere batches in magazijn weergeven wordt geconfigureerd in menuopties van mobiele apparaten en beïnvloedt het verzamelen voor de onderste artikelen in de batch.</span><span class="sxs-lookup"><span data-stu-id="a5555-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="a5555-113">Weergave oudere batches in magazijn instellen</span><span class="sxs-lookup"><span data-stu-id="a5555-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="a5555-114">De configuratie **Weergave oudere batches in magazijn** is beschikbaar in menuopties van mobiele apparaten wanneer de optie **Oudste batch verzamelen** is ingesteld op **Waarschuwen**.</span><span class="sxs-lookup"><span data-stu-id="a5555-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="a5555-115">Stel onder **Magazijnbeheer** > **Instellingen** > **Mobiel apparaat** > **Menuopties voor mobiel apparaat** de menuoptie **Bestaand werk gebruiken** in op **Ja** en selecteer **Waarschuwen** in het veld **Oudste batch verzamelen**.</span><span class="sxs-lookup"><span data-stu-id="a5555-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 



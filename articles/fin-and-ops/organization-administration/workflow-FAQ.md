---
title: Veelgestelde vragen workflow
description: In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/01/2019
ms.locfileid: "773203"
---
# <a name="workflow-system"></a><span data-ttu-id="7227c-103">Workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="7227c-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7227c-104">In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.</span><span class="sxs-lookup"><span data-stu-id="7227c-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="7227c-105">Meldingen</span><span class="sxs-lookup"><span data-stu-id="7227c-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="7227c-106">Waarom worden er meerdere meldingen ontvangen wanneer een werkitem wordt afgewezen?</span><span class="sxs-lookup"><span data-stu-id="7227c-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="7227c-107">Wanneer een werkitem wordt afgewezen, wordt dat werkitem als afgewezen voltooid.</span><span class="sxs-lookup"><span data-stu-id="7227c-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="7227c-108">Een andere werkitem wordt gemaakt en toegewezen aan de aanvrager.</span><span class="sxs-lookup"><span data-stu-id="7227c-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="7227c-109">Dit betekent dat er een melding naar de aanvrager voor het afgewezen werkitem gaat en een aparte melding naar de gebruiker die is toegewezen aan het nieuwe werkitem waarvoor 'wijziging is aangevraagd'.</span><span class="sxs-lookup"><span data-stu-id="7227c-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="7227c-110">Elke melding is voor een ander werkitem, maar doordat de meldingen op elkaar lijken kan er verwarring ontstaan.</span><span class="sxs-lookup"><span data-stu-id="7227c-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="7227c-111">We proberen dit in een toekomstige versie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="7227c-111">We are looking at ways to improve this in a future release.</span></span>

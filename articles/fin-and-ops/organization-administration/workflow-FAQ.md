---
title: Veelgestelde vragen workflow
description: In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509286"
---
# <a name="workflow-system"></a><span data-ttu-id="4c604-103">Workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="4c604-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c604-104">In dit onderwerp worden antwoorden op veelgestelde vragen over het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gegeven.</span><span class="sxs-lookup"><span data-stu-id="4c604-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="4c604-105">Meldingen</span><span class="sxs-lookup"><span data-stu-id="4c604-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="4c604-106">Waarom worden er meerdere meldingen ontvangen wanneer een werkitem wordt afgewezen?</span><span class="sxs-lookup"><span data-stu-id="4c604-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="4c604-107">Wanneer een werkitem wordt afgewezen, wordt dat werkitem als afgewezen voltooid.</span><span class="sxs-lookup"><span data-stu-id="4c604-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="4c604-108">Een andere werkitem wordt gemaakt en toegewezen aan de aanvrager.</span><span class="sxs-lookup"><span data-stu-id="4c604-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="4c604-109">Dit betekent dat er een melding naar de aanvrager voor het afgewezen werkitem gaat en een aparte melding naar de gebruiker die is toegewezen aan het nieuwe werkitem waarvoor 'wijziging is aangevraagd'.</span><span class="sxs-lookup"><span data-stu-id="4c604-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="4c604-110">Elke melding is voor een ander werkitem, maar doordat de meldingen op elkaar lijken kan er verwarring ontstaan.</span><span class="sxs-lookup"><span data-stu-id="4c604-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="4c604-111">We proberen dit in een toekomstige versie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="4c604-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="4c604-112">Waarom mislukt het exporteren van mijn werkstromen?</span><span class="sxs-lookup"><span data-stu-id="4c604-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="4c604-113">Er geldt momenteel een beperking in de functie voor het exporteren van werkstromen waardoor namen van werkstromen niet langer kunnen zijn dan 48 tekens.</span><span class="sxs-lookup"><span data-stu-id="4c604-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="4c604-114">Als u een naam gebruikt die langer is dan 48 tekens, kan het foutbericht 'Server kon de aanvraag niet verifiëren' worden weergegeven en/of kan worden voorkomen dat een bestand wordt geëxporteerd zonder bestandstype.</span><span class="sxs-lookup"><span data-stu-id="4c604-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="4c604-115">Het volgende blogbericht bevat nadere details: [Problemen bij het exporteren van werkstromen oplossen](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="4c604-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

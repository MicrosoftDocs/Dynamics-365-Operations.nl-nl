---
title: Een productieorder plannen
description: Deze procedure toont hoe u een productieorder plant.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7ee023f39cc5d02b0f5b80fbb3ae3ad0c9774
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "346359"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="f326e-103">Een productieorder plannen</span><span class="sxs-lookup"><span data-stu-id="f326e-103">Schedule a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f326e-104">Deze procedure toont hoe u een productieorder plant.</span><span class="sxs-lookup"><span data-stu-id="f326e-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="f326e-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f326e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f326e-106">Dit is de derde procedure van zeven die de productieorderlevenscyclus beschrijven.</span><span class="sxs-lookup"><span data-stu-id="f326e-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="f326e-107">Een productieorder plannen</span><span class="sxs-lookup"><span data-stu-id="f326e-107">Schedule a production order</span></span>
1. <span data-ttu-id="f326e-108">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="f326e-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="f326e-109">Selecteer een productieorder met de status Geschat.</span><span class="sxs-lookup"><span data-stu-id="f326e-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="f326e-110">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="f326e-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="f326e-111">Klik op Taken plannen.</span><span class="sxs-lookup"><span data-stu-id="f326e-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="f326e-112">De parameters voor planning worden ingesteld op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="f326e-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="f326e-113">U kunt de parameters instellen voor specifieke gebruikers of alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="f326e-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="f326e-114">Selecteer in het veld Planningsrichting de optie 'Verder vanaf vandaag'.</span><span class="sxs-lookup"><span data-stu-id="f326e-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="f326e-115">Voer in het veld Planningsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="f326e-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="f326e-116">Schakel het selectievakje Eindige capaciteit in of uit.</span><span class="sxs-lookup"><span data-stu-id="f326e-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="f326e-117">Schakel het selectievakje Eindig materiaal in of uit.</span><span class="sxs-lookup"><span data-stu-id="f326e-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="f326e-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f326e-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="f326e-119">De resultaten van planning weergeven</span><span class="sxs-lookup"><span data-stu-id="f326e-119">View the scheduling results</span></span>
1. <span data-ttu-id="f326e-120">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="f326e-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="f326e-121">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="f326e-121">Click All jobs.</span></span>
    * <span data-ttu-id="f326e-122">Deze pagina toont de geplande taken die u zojuist hebt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="f326e-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="f326e-123">Vouw de sectie Planning uit of samen.</span><span class="sxs-lookup"><span data-stu-id="f326e-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="f326e-124">Op het sneltabblad Planning kunt u de geplande datum en tijd weergeven.</span><span class="sxs-lookup"><span data-stu-id="f326e-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="f326e-125">Klik op Query's.</span><span class="sxs-lookup"><span data-stu-id="f326e-125">Click Inquiries.</span></span>
5. <span data-ttu-id="f326e-126">Klik op Capaciteitsbelasting.</span><span class="sxs-lookup"><span data-stu-id="f326e-126">Click Capacity load.</span></span>
    * <span data-ttu-id="f326e-127">De pagina Capaciteitsbelasting toont de capaciteit die is gereserveerd via taakplanning, het totale aantal uren dat momenteel is gereserveerd voor de resource en het aantal uren dat beschikbaar is voor taakplanning voor de resource.</span><span class="sxs-lookup"><span data-stu-id="f326e-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="f326e-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f326e-128">Close the page.</span></span>
7. <span data-ttu-id="f326e-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f326e-129">Close the page.</span></span>


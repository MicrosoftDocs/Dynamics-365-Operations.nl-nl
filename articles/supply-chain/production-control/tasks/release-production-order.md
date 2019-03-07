---
title: Een productieorder vrijgeven
description: Deze procedure laat zien hoe u een productieorder vrijgeeft.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 917fe1ef826c9b112be29ebce78ebd750652db64
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "345071"
---
# <a name="release-a-production-order"></a><span data-ttu-id="632b3-103">Een productieorder vrijgeven</span><span class="sxs-lookup"><span data-stu-id="632b3-103">Release a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="632b3-104">Deze procedure laat zien hoe u een productieorder vrijgeeft.</span><span class="sxs-lookup"><span data-stu-id="632b3-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="632b3-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="632b3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="632b3-106">Dit is de vierde procedure van zeven die de productieorderlevenscyclus beschrijven.</span><span class="sxs-lookup"><span data-stu-id="632b3-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="632b3-107">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="632b3-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="632b3-108">Selecteer in het raster een productieorder met de status Gepland.</span><span class="sxs-lookup"><span data-stu-id="632b3-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="632b3-109">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="632b3-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="632b3-110">Klik op Vrijgave.</span><span class="sxs-lookup"><span data-stu-id="632b3-110">Click Release.</span></span>
    * <span data-ttu-id="632b3-111">Op deze pagina kunt u de vrijgave bevestigen van het geselecteerde bereik van productieorders.</span><span class="sxs-lookup"><span data-stu-id="632b3-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="632b3-112">Klik op Selecteren als u orders wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="632b3-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="632b3-113">De stap Vrijgave geeft aan wanneer de productieorder aan de werkvloer van productie wordt vrijgegeven zodat de werkvloeroperators de voortgang van productietaken kunnen melden.</span><span class="sxs-lookup"><span data-stu-id="632b3-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="632b3-114">Productiedocumenten die relevante informatie over het verwerken van de taken bevatten kunnen worden uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="632b3-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="632b3-115">Het magazijnwerk voor het verzamelen van grondstoffen wordt gegenereerd voor de artikelen die voor het magazijnproces zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="632b3-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="632b3-116">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="632b3-116">Click the General tab.</span></span>
    * <span data-ttu-id="632b3-117">Selecteer welke productierapporten moeten worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="632b3-117">Select which production reports should be printed.</span></span> <span data-ttu-id="632b3-118">Het taakkaartrapport drukt een pagina af voor elke geplande taak en vereist dat de productieorder wordt gepland op taakniveau.</span><span class="sxs-lookup"><span data-stu-id="632b3-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="632b3-119">Het rapport bevat informatie over de geplande begin- en eindtijd, de te produceren hoeveelheid en welke resource de taak verwerkt.</span><span class="sxs-lookup"><span data-stu-id="632b3-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="632b3-120">Het routetaakrapport verzamelt dezelfde informatie over dezelfde pagina, maar drukt geen pagina af voor elke taak.</span><span class="sxs-lookup"><span data-stu-id="632b3-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="632b3-121">Het routekaartrapport geeft alleen de bewerkingen weer maar niet de taken.</span><span class="sxs-lookup"><span data-stu-id="632b3-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="632b3-122">Daarom vereist dit rapport geen taakplanning, maar kan het worden gebruikt wanneer productieorders op het bewerkingsniveau worden gepland.</span><span class="sxs-lookup"><span data-stu-id="632b3-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="632b3-123">Klik op het selectievakje Routekaart afdrukken.</span><span class="sxs-lookup"><span data-stu-id="632b3-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="632b3-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="632b3-124">Click OK.</span></span>
7. <span data-ttu-id="632b3-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="632b3-125">Close the page.</span></span>


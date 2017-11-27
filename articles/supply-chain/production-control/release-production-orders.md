---
title: Productieorders vrijgeven
description: Een vrijgegeven productieorder is een order die is geautoriseerd voor productie. De term Vrijgegeven wordt gebruikt om een status in de levenscyclus van de productieorder te beschrijven, waar de productieorder beschikbaar is voor uitvoering op de productiewerkvloer en voor magazijnprocessen.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9b9009c714445871c15363c26829da812e56c688
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="release-production-orders"></a><span data-ttu-id="ea026-104">Productieorders vrijgeven</span><span class="sxs-lookup"><span data-stu-id="ea026-104">Release production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ea026-105">Een vrijgegeven productieorder is een order die is geautoriseerd voor productie.</span><span class="sxs-lookup"><span data-stu-id="ea026-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="ea026-106">De term Vrijgegeven wordt gebruikt om een status in de levenscyclus van de productieorder te beschrijven, waar de productieorder beschikbaar is voor uitvoering op de productiewerkvloer en voor magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="ea026-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="ea026-107">Kenmerken van de status Vrijgegeven</span><span class="sxs-lookup"><span data-stu-id="ea026-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="ea026-108">De status **Vrijgegeven** is een van de statussen in de levenscyclus voor productieorders.</span><span class="sxs-lookup"><span data-stu-id="ea026-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="ea026-109">Productieorders met de status **Vrijgegeven** zijn beschikbaar voor uitvoering op de productiewerkvloer en voor magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="ea026-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="ea026-110">De status **Vrijgegeven** heeft de volgende kenmerken:</span><span class="sxs-lookup"><span data-stu-id="ea026-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="ea026-111">Een productieorder kan de status **Vrijgegeven** krijgen van de productieorder of via het gebruik van een batchproces.</span><span class="sxs-lookup"><span data-stu-id="ea026-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="ea026-112">De productieorder kan ook automatisch worden bijgewerkt vanuit geplande productieorders die zijn gefiatteerd door gebruikmaking van het veld **Time fence voor fiattering** op de pagina te **Hoofdplan**.</span><span class="sxs-lookup"><span data-stu-id="ea026-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="ea026-113">De status **Vrijgegeven** is het signaal voor de werkvloeroperators (operators) om de uitvoering van de productietaken op de werkvloer te starten.</span><span class="sxs-lookup"><span data-stu-id="ea026-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="ea026-114">Productiedocumenten, zoals routekaarten, routetaken en takenkaarten bevatten informatie over productietaken en kunnen worden uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="ea026-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="ea026-115">Voor materialen die fysiek zijn gereserveerd, wordt magazijnwerk gegenereerd om materialen voor de productieorder te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="ea026-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="ea026-116">Taken vrijgeven aan de werkvloer</span><span class="sxs-lookup"><span data-stu-id="ea026-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="ea026-117">Nadat een productieorder is vrijgegeven, zijn de productietaken die verband houden met de order zichtbaar en gereed voor registratie.</span><span class="sxs-lookup"><span data-stu-id="ea026-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="ea026-118">De operators kunnen taakregistraties maken, zoals Starten, Stoppen en Voltooid, op ofwel de pagina **Taakkaartterminal** of op de pagina **Taakkaartapparaat**.</span><span class="sxs-lookup"><span data-stu-id="ea026-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="ea026-119">De geregistreerde tijd en hoeveelheid worden automatisch overgebracht van de registratiepagina's naar productiejournalen, om de verbruikte tijd en hoeveelheid bij te houden.</span><span class="sxs-lookup"><span data-stu-id="ea026-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="ea026-120">Routekaarten</span><span class="sxs-lookup"><span data-stu-id="ea026-120">Route cards</span></span>
<span data-ttu-id="ea026-121">Met een routekaart beschikt u over een overzicht van informatie uit route- en bewerkingsinstellingen en uit bewerkings- en taakplanningsmethoden.</span><span class="sxs-lookup"><span data-stu-id="ea026-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="ea026-122">Routetaken</span><span class="sxs-lookup"><span data-stu-id="ea026-122">Route jobs</span></span>
<span data-ttu-id="ea026-123">Een routetaak vermeldt elke taak van een bewerking in detail en omvat installatie, proces, wachtrij en transporttijden.</span><span class="sxs-lookup"><span data-stu-id="ea026-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="ea026-124">Een bewerking, zoals lakken, kan bijvoorbeeld afzonderlijke taken vereisen, zoals instellingstijd, uitvoeringstijd voor het lakproces en wachttijd voor het drogen.</span><span class="sxs-lookup"><span data-stu-id="ea026-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="ea026-125">Taakkaarten</span><span class="sxs-lookup"><span data-stu-id="ea026-125">Job cards</span></span>
<span data-ttu-id="ea026-126">Een taakkaart bevat de afzonderlijke taaknummers van een bepaalde bewerking.</span><span class="sxs-lookup"><span data-stu-id="ea026-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="ea026-127">Per pagina wordt één taak weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ea026-127">One job appears on each page.</span></span> <span data-ttu-id="ea026-128">De taken op een taakkaart en de geschatte tijden worden opgehaald uit de instellingsgegevens voor routes en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ea026-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="ea026-129">Vanaf een taakkaart kunt u de pagina **Productiejournaalregels**, **taakkaart** openen.</span><span class="sxs-lookup"><span data-stu-id="ea026-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="ea026-130">Personen die bronnen voor bedrijfsactiviteiten beheren, kunnen feedback geven over het productieproces.</span><span class="sxs-lookup"><span data-stu-id="ea026-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="ea026-131">De kaart bevat velden waarin u verbruiksstatistieken en informatie, zoals de fouthoeveelheid, kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="ea026-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="ea026-132">Magazijnwerk voor het verzamelen van grondstoffen</span><span class="sxs-lookup"><span data-stu-id="ea026-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="ea026-133">Werkzaamheden voor het verzamelen van grondstoffen worden gegenereerd tijdens de vrijgave.</span><span class="sxs-lookup"><span data-stu-id="ea026-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="ea026-134">Werk wordt alleen gegenereerd voor de hoeveelheid materialen die fysiek werd gereserveerd voor de productieorder voordat de order werd vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="ea026-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="ea026-135">De volgende instellingen zijn vereist om magazijnwerk te genereren voor orderverzameling van grondstoffen:</span><span class="sxs-lookup"><span data-stu-id="ea026-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="ea026-136">Een locatierichtlijn voor het verzamelen van grondstoffen die bepaalt op welke magazijnlocatie de materialen moeten worden verzameld</span><span class="sxs-lookup"><span data-stu-id="ea026-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="ea026-137">Een wavesjabloon voor grondstoffen, waarin het beleid voor de uitvoering van magazijnwerkzaamheden is geconfigureerd</span><span class="sxs-lookup"><span data-stu-id="ea026-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="ea026-138">Een productie-invoerlocatie die bepaalt waar de materialen worden geplaatst</span><span class="sxs-lookup"><span data-stu-id="ea026-138">A production input location that determines where materials are put</span></span>






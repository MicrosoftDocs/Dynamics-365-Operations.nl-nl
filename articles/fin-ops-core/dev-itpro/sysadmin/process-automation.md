---
title: Procesautomatisering
description: Dit onderwerp biedt informatie over de manier waarop procesautomatisering eenvoudige planning van processen voor de batchserver mogelijk maakt.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: afbef26cb7b37bafb34f12cc20a88fb4aea9f343
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885246"
---
# <a name="process-automation"></a><span data-ttu-id="e393d-103">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="e393d-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e393d-104">Procesautomatisering maakt eenvoudige planning van processen voor de batchserver mogelijk.</span><span class="sxs-lookup"><span data-stu-id="e393d-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="e393d-105">De bijgewerkte kalenderweergave van het geplande werk maakt het eindgebruikers mogelijk geplande en voltooide werkzaamheden weer te geven en daarop actie te ondernemen.</span><span class="sxs-lookup"><span data-stu-id="e393d-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="e393d-106">Administratie</span><span class="sxs-lookup"><span data-stu-id="e393d-106">Administration</span></span>

<span data-ttu-id="e393d-107">De centrale beheerpagina voor alle procesautomatiseringen vindt u in de module Systeembeheer onder het menu **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="e393d-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="e393d-108">Op deze pagina worden alle geautomatiseerde processen (reeksen) vermeld die in het systeem zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e393d-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="e393d-109">U kunt hiermee ook rechtstreeks vanaf deze pagina nieuwe procesautomatiseringen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e393d-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="e393d-110">Nadat u een reeks hebt ingesteld, kunt u elke reeks in deze lijst beheren.</span><span class="sxs-lookup"><span data-stu-id="e393d-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="e393d-111">U kunt ervoor kiezen om de gehele reeks te bewerken, deze te verwijderen, alle exemplaren weer te geven in een lijstweergave of de reeks uit te schakelen als u het geplande werk voor een tijdje wilt onderbreken.</span><span class="sxs-lookup"><span data-stu-id="e393d-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="e393d-112">Alle processen die in functiebeheer zijn uitgeschakeld, worden niet weergegeven wanneer de functie is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e393d-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="e393d-113">Bovendien worden met de planningsengine voor procesautomatisering geen exemplaren of achtergrondprocessen gepland voor een uitgeschakelde functie.</span><span class="sxs-lookup"><span data-stu-id="e393d-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="e393d-114">Als u de functie opnieuw inschakelt, worden alle in het verleden geplande gebeurtenissen of achtergrondprocessen onmiddellijk uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e393d-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="e393d-115">Kalenderweergave</span><span class="sxs-lookup"><span data-stu-id="e393d-115">Calendar view</span></span>

<span data-ttu-id="e393d-116">Een van de belangrijkste voordelen van procesautomatisering is de mogelijkheid om het geplande werk in een eenvoudige kalenderweergave te bekijken.</span><span class="sxs-lookup"><span data-stu-id="e393d-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="e393d-117">In deze weergave kunt u het werk per week bekijken.</span><span class="sxs-lookup"><span data-stu-id="e393d-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="e393d-118">U ziet deze weergave wordt aan de rechterkant van de pagina **Procesautomatisering**.</span><span class="sxs-lookup"><span data-stu-id="e393d-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="e393d-119">De weergave wordt gevuld met het geplande werk voor de geselecteerde reeks.</span><span class="sxs-lookup"><span data-stu-id="e393d-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="e393d-120">[![Kalender met procesautomatisering](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="e393d-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="e393d-121">Wijzigingen in exemplaren</span><span class="sxs-lookup"><span data-stu-id="e393d-121">Occurrence changes</span></span>

<span data-ttu-id="e393d-122">Elk exemplaar kan worden gewijzigd zonder dat dit gevolgen heeft voor andere exemplaren die zijn gedefinieerd in de reeks waaruit ze afkomstig zijn.</span><span class="sxs-lookup"><span data-stu-id="e393d-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="e393d-123">U kunt exemplaren van gepland werk bewerken vanuit de kalenderweergave door de knop **Weergeven/bewerken** te selecteren en op **Exemplaar** te klikken.</span><span class="sxs-lookup"><span data-stu-id="e393d-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="e393d-124">Op deze pagina hebt u toegang tot alle instellingen die oorspronkelijk werden weergegeven in de configuratiewizard van de reeks. U kunt hier een eenmalige wijziging aanbrengen in het geselecteerde exemplaar.</span><span class="sxs-lookup"><span data-stu-id="e393d-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="e393d-125">U kunt gepland werk ook uitschakelen door de knop **Uitschakelen** te selecteren in de kalenderweergave.</span><span class="sxs-lookup"><span data-stu-id="e393d-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="e393d-126">Documentatie voor ontwikkelaars</span><span class="sxs-lookup"><span data-stu-id="e393d-126">Developer documentation</span></span>

<span data-ttu-id="e393d-127">Met het raamwerk voor procesautomatisering kunnen ontwikkelaars het raamwerk voor procesautomatisering uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="e393d-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="e393d-128">De documentatie van [Raamwerk voor procesautomatisering](../process-automation/process-automation-framework.md) bevat informatie over de manier waarop u aangepaste processen kunt maken die moeten worden uitgevoerd door de batchserver die is gepland met de wizard voor procesautomatisering en die automatisch in de kalenderweergave wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e393d-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>

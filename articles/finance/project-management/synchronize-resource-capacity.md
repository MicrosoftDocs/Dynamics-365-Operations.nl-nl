---
title: Resourcecapaciteit synchroniseren
description: Dit onderwerp bevat informatie over het synchroniseren van de capaciteit van een resource in kalenders en projecten.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760512"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="45a81-103">Resourcecapaciteit synchroniseren</span><span class="sxs-lookup"><span data-stu-id="45a81-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45a81-104">De processen voor resourcesynchronisatie helpen ervoor te zorgen dat informatie voor de kalender en basiskalender doorvloeien naar de planning van projectresources.</span><span class="sxs-lookup"><span data-stu-id="45a81-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="45a81-105">Als de kalender wordt gewijzigd, voeren de processen de vereiste updates door bij de planning van projectresources.</span><span class="sxs-lookup"><span data-stu-id="45a81-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="45a81-106">De processen helpen ook de prestaties te verbeteren, omdat de resourcegegevens van de kalender van tevoren worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="45a81-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="45a81-107">Daarom wordt resourceplanningsinformatie sneller bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="45a81-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="45a81-108">Het wordt aangeraden om de processen als batch in te plannen in plaats van een voor een.</span><span class="sxs-lookup"><span data-stu-id="45a81-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="45a81-109">Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de informatie voor het laatst is gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="45a81-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="45a81-110">Als de inclusieve datums niet worden gebruikt, kunnen lacunes optreden tijdens de datumsynchronisatie.</span><span class="sxs-lookup"><span data-stu-id="45a81-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendersynchronisatie](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="45a81-112">Vergaarde resourcecapaciteit synchroniseren</span><span class="sxs-lookup"><span data-stu-id="45a81-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="45a81-113">Het synchronisatieproces is ontworpen om alle resourcekalenderinformatie te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="45a81-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="45a81-114">Deze informatie omvat basiskalenderinformatie over de wijzigingen in de tabel met de resourcekalendercapaciteit van het project.</span><span class="sxs-lookup"><span data-stu-id="45a81-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="45a81-115">Als nieuwe resources aan het project worden toegevoegd, zorgt synchronisatie ervoor dat de bijgewerkte agendagegevens beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="45a81-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="45a81-116">Deze synchronisatie kan op elk gewenst moment worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="45a81-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="45a81-117">Het wordt aangeraden om een batch te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="45a81-117">We recommend that you use a batch.</span></span> <span data-ttu-id="45a81-118">De opties zijn beschikbaar tijdens het synchroniseren van capaciteitsreserveringen.</span><span class="sxs-lookup"><span data-stu-id="45a81-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="45a81-119">Selecteer **Projectbeheer en boekhouding** &gt; **Periodiek** &gt; **Capaciteitsynchronisatie** &gt; **Vergaarde resourcecapaciteit synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="45a81-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="45a81-120">Stel de opties in de volgende tabel in.</span><span class="sxs-lookup"><span data-stu-id="45a81-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="45a81-121">Optie</span><span class="sxs-lookup"><span data-stu-id="45a81-121">Option</span></span>      | <span data-ttu-id="45a81-122">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="45a81-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="45a81-123">Periodecode</span><span class="sxs-lookup"><span data-stu-id="45a81-123">Period code</span></span> | <span data-ttu-id="45a81-124">Selecteer eventueel de datumintervalcode voor het grootboek om de begin- en einddatums in te stellen voor het synchronisatieproces voor vergaarde resourcecapaciteit.</span><span class="sxs-lookup"><span data-stu-id="45a81-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="45a81-125">Begindatum</span><span class="sxs-lookup"><span data-stu-id="45a81-125">Start date</span></span>  | <span data-ttu-id="45a81-126">Voer de begindatum in voor het synchronisatieproces voor vergaarde resourcecapaciteit.</span><span class="sxs-lookup"><span data-stu-id="45a81-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="45a81-127">Einddatum</span><span class="sxs-lookup"><span data-stu-id="45a81-127">End date</span></span>    | <span data-ttu-id="45a81-128">Voer de einddatum in voor het synchronisatieproces voor vergaarde resourcecapaciteit.</span><span class="sxs-lookup"><span data-stu-id="45a81-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="45a81-129">[![Synchronisatieproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="45a81-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>

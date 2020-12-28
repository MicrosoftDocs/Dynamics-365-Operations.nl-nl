---
title: Classificatieprofielen
description: In dit onderwerp wordt beschreven hoe u de gegevens voor beoordelingsprofielen instelt.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c54e7457813774027debd301d9a0bf8ce1b6d47
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646375"
---
# <a name="rating-profiles"></a><span data-ttu-id="89883-103">Classificatieprofielen</span><span class="sxs-lookup"><span data-stu-id="89883-103">Rating profiles</span></span>

<span data-ttu-id="89883-104">Een beoordelingsprofiel lijkt op een logistiek contract (maar niet een wettelijk contract).</span><span class="sxs-lookup"><span data-stu-id="89883-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="89883-105">Het wordt gebruikt om de transporttarieven voor ladingen te bepalen.</span><span class="sxs-lookup"><span data-stu-id="89883-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="89883-106">Elk beoordelingsprofiel is uniek voor een vervoerder.</span><span class="sxs-lookup"><span data-stu-id="89883-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="89883-107">In het profiel koppelt u de vervoerder aan een tariefmodel.</span><span class="sxs-lookup"><span data-stu-id="89883-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="89883-108">Het tariefmodel definieert de tariefbasistoewijzingen en de tariefbasis.</span><span class="sxs-lookup"><span data-stu-id="89883-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="89883-109">De tariefbasis bepaalt het tarief van de vervoerder.</span><span class="sxs-lookup"><span data-stu-id="89883-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="89883-110">U kunt een beoordelingsprofiel instellen met behulp van een pagina met een overzicht van alle bestaande beoordelingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="89883-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="89883-111">U kunt ook een beoordelingsprofiel rechtstreeks instellen vanaf de vervoerder.</span><span class="sxs-lookup"><span data-stu-id="89883-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="89883-112">In beide gevallen is de informatie die u voor het beoordelingsprofiel hebt ingesteld, hetzelfde.</span><span class="sxs-lookup"><span data-stu-id="89883-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="89883-113">Een beoordelingsprofiel maken of bewerken op de pagina Beoordelingsprofielen</span><span class="sxs-lookup"><span data-stu-id="89883-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="89883-114">Op de pagina **Beoordelingsprofielen** kunt u alle beschikbare beoordelingsprofielen controleren.</span><span class="sxs-lookup"><span data-stu-id="89883-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="89883-115">U kunt ook bestaande profielen bewerken en nieuwe profielen maken.</span><span class="sxs-lookup"><span data-stu-id="89883-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="89883-116">Ga naar **Transportbeheer \> Instellingen \> Beoordeling \> Beoordelingsprofiel**.</span><span class="sxs-lookup"><span data-stu-id="89883-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="89883-117">Selecteer in het actievenster **Nieuw** om een nieuw beoordelingsprofiel toe te voegen aan het raster of selecteer **Bewerken** om een bestaand profiel te bewerken.</span><span class="sxs-lookup"><span data-stu-id="89883-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="89883-118">Stel in de rij voor het nieuwe of bestaande beoordelingsprofiel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="89883-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="89883-119">**Beoordelingsprofiel**: voer een unieke id in voor het beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="89883-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="89883-120">**Naam**: voer een beschrijvende naam in voor het beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="89883-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="89883-121">**Vervoerder**: selecteer een vervoerder.</span><span class="sxs-lookup"><span data-stu-id="89883-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="89883-122">Het beoordelingsprofiel dat u instelt, wordt ook weergegeven op de pagina **Vervoerders** voor de geselecteerde vervoerder.</span><span class="sxs-lookup"><span data-stu-id="89883-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="89883-123">**Locatie** en **Magazijn**: Selecteer een locatie en magazijn.</span><span class="sxs-lookup"><span data-stu-id="89883-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="89883-124">**Tarief-engine**: selecteer de tarief-engine voor het beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="89883-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="89883-125">**Tariefmodel**: selecteer het tariefmodel voor het beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="89883-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="89883-126">U kunt het tariefmodel gebruiken om een type tariefbasis en een tariefbasis te definiëren.</span><span class="sxs-lookup"><span data-stu-id="89883-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="89883-127">Zie voor meer informatie [Tariefmodellen instellen](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="89883-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="89883-128">**Transittijdengine**: selecteer de transittijdengine voor het beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="89883-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="89883-129">**Brandstofindex**: selecteer de brandstofindex van de vervoerder voor het beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="89883-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="89883-130">**Begindatum en -tijd** en **Einddatum en -tijd**: definieer de periode waarin het beoordelingsprofiel actief moet zijn.</span><span class="sxs-lookup"><span data-stu-id="89883-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="89883-131">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="89883-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="89883-132">Een beoordelingsprofiel direct op de pagina Vervoerders maken of bewerken</span><span class="sxs-lookup"><span data-stu-id="89883-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="89883-133">Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Vervoerders**.</span><span class="sxs-lookup"><span data-stu-id="89883-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="89883-134">Selecteer een vervoerder in de lijst.</span><span class="sxs-lookup"><span data-stu-id="89883-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="89883-135">Selecteer in het sneltabblad **Beoordelingsprofiel** de optie **Nieuw** om een beoordelingsprofiel te maken.</span><span class="sxs-lookup"><span data-stu-id="89883-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="89883-136">Stel de velden in voor het nieuwe beoordelingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="89883-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="89883-137">Deze velden komen overeen met de velden op de pagina **Beoordelingsprofielen**, zoals beschreven in het vorige gedeelte van dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="89883-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="89883-138">Profielen die op de pagina **Vervoerders** worden gemaakt, worden ook weergegeven op de pagina **Beoordelingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="89883-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>

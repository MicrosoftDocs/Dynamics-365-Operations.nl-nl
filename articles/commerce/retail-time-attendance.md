---
title: Tijd- en aanwezigheidsbeheer in Retail
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor beheer van Tijd en aanwezigheid in Dynamics 365 Commerce.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e28df09ecb592ae7df360d1b2d0bf06339c1410d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989372"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="156be-103">Tijd- en aanwezigheidsbeheer in Retail</span><span class="sxs-lookup"><span data-stu-id="156be-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="156be-104">In dit onderwerp worden de scenario's beschreven die worden ondersteund voor beheer van Tijd en aanwezigheid in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="156be-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="156be-105">Het instellen en inplannen van medewerkers beheren</span><span class="sxs-lookup"><span data-stu-id="156be-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="156be-106">initiële configuratie</span><span class="sxs-lookup"><span data-stu-id="156be-106">Initial configuration</span></span>

- <span data-ttu-id="156be-107">Voer de stappen in de configuratiewizard uit.</span><span class="sxs-lookup"><span data-stu-id="156be-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="156be-108">Werknemers registreren als tijdregistratiewerknemers.</span><span class="sxs-lookup"><span data-stu-id="156be-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="156be-109">De planning van de werknemersplannen</span><span class="sxs-lookup"><span data-stu-id="156be-109">Plan worker schedules</span></span>

- <span data-ttu-id="156be-110">Profielen toepassen met behulp van de werkplanner.</span><span class="sxs-lookup"><span data-stu-id="156be-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="156be-111">Zie [Profielen met behulp van werkplanner toepassen](https://technet.microsoft.com/library/aa551234.aspx) voor meer informatie over werktijdprofielen.</span><span class="sxs-lookup"><span data-stu-id="156be-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="156be-112">Zie voor informatie over de configuratiestappen [Tijd en aanwezigheid instellen](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="156be-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="156be-113">Commerce-specifieke configuratie</span><span class="sxs-lookup"><span data-stu-id="156be-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="156be-114">Schakel een functionaliteitprofiel voor tijdklok in voor medewerkers voor wie u tijdregistratie wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="156be-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="156be-115">Klik op **POS-functionaliteitsprofielen** &gt; **Functies** &gt; **POS-tijdregistraties** &gt; **Tijdregistratie inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="156be-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="156be-116">Configureer verkooppuntmachtigingsgroepen om de machtiging Registraties tijdklok weergeven in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="156be-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="156be-117">Met deze machtiging kan een gebruiker de prikklokregistraties van andere werknemers in de winkel bekijken (en van alle andere winkels waaraan de gebruiker is gekoppeld via het adresboek).</span><span class="sxs-lookup"><span data-stu-id="156be-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="156be-118">U wilt mogelijk deze machtiging inschakelen voor een managerrol maar niet voor de rol van een kassamedewerker.</span><span class="sxs-lookup"><span data-stu-id="156be-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="156be-119">Klik op **POS-machtigingsgroepen** &gt; **Registraties tijdklok weergeven**.</span><span class="sxs-lookup"><span data-stu-id="156be-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="156be-120">Tijd registreren</span><span class="sxs-lookup"><span data-stu-id="156be-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="156be-121">Tijdregistraties van kassiers en niet-kassiers</span><span class="sxs-lookup"><span data-stu-id="156be-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="156be-122">Op POS:</span><span class="sxs-lookup"><span data-stu-id="156be-122">On POS:</span></span>

    - <span data-ttu-id="156be-123">Inklokbewerkingen:</span><span class="sxs-lookup"><span data-stu-id="156be-123">Clock-in operations:</span></span>

        - <span data-ttu-id="156be-124">Meld u aan met een niet-ladebewerking of een nieuwe ploegendienst.</span><span class="sxs-lookup"><span data-stu-id="156be-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="156be-125">Selecteer een tijdklokbewerking.</span><span class="sxs-lookup"><span data-stu-id="156be-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="156be-126">Selecteer de gewenste bewerking:</span><span class="sxs-lookup"><span data-stu-id="156be-126">Select a desired operation:</span></span>

            - <span data-ttu-id="156be-127">Inklokken</span><span class="sxs-lookup"><span data-stu-id="156be-127">Clock-in</span></span>
            - <span data-ttu-id="156be-128">Pauze voor werk</span><span class="sxs-lookup"><span data-stu-id="156be-128">Break for Work</span></span>
            - <span data-ttu-id="156be-129">Lunchpauze</span><span class="sxs-lookup"><span data-stu-id="156be-129">Break for Lunch</span></span>
            - <span data-ttu-id="156be-130">Uitklokken</span><span class="sxs-lookup"><span data-stu-id="156be-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="156be-131">Huidige status</span><span class="sxs-lookup"><span data-stu-id="156be-131">Current state</span></span></th>
        <th><span data-ttu-id="156be-132">Beschikbare bewerkingen</span><span class="sxs-lookup"><span data-stu-id="156be-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="156be-133">Inklokken</span><span class="sxs-lookup"><span data-stu-id="156be-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="156be-134">Pauze voor werk</span><span class="sxs-lookup"><span data-stu-id="156be-134">Break for Work</span></span></li>
        <li><span data-ttu-id="156be-135">Lunchpauze</span><span class="sxs-lookup"><span data-stu-id="156be-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="156be-136">Uitklokken</span><span class="sxs-lookup"><span data-stu-id="156be-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="156be-137">Pauze voor werk</span><span class="sxs-lookup"><span data-stu-id="156be-137">Break for Work</span></span></td>
        <td><span data-ttu-id="156be-138">Inklokken</span><span class="sxs-lookup"><span data-stu-id="156be-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="156be-139">Lunchpauze</span><span class="sxs-lookup"><span data-stu-id="156be-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="156be-140">Inklokken</span><span class="sxs-lookup"><span data-stu-id="156be-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="156be-141">Uitklokken</span><span class="sxs-lookup"><span data-stu-id="156be-141">Clock-out</span></span></td>
        <td><span data-ttu-id="156be-142">Inklokken</span><span class="sxs-lookup"><span data-stu-id="156be-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="156be-143">[![Statussen van tijdklok](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="156be-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="156be-144">Bekijk het bevestigingsbericht weergeven, en controleer of de huidige activiteitstijd correct is.</span><span class="sxs-lookup"><span data-stu-id="156be-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="156be-145">Logboek:</span><span class="sxs-lookup"><span data-stu-id="156be-145">Logbook:</span></span>

    - <span data-ttu-id="156be-146">Klik op **Logboek** om prikklokactiviteit weer te geven.</span><span class="sxs-lookup"><span data-stu-id="156be-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="156be-147">Gebruik de tijdsfilters om verschillende tijdvensters te selecteren.</span><span class="sxs-lookup"><span data-stu-id="156be-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="156be-148">Als u met meerdere opslaglocaties werkt, ziet u hier uw tijdregistraties uit alle winkels waar u tijd hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="156be-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="156be-149">U kunt het opslagfilter gebruiken om tijdregistraties van een geselecteerde opslag te bekijken.</span><span class="sxs-lookup"><span data-stu-id="156be-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="156be-150">Verschillende tijdzones:</span><span class="sxs-lookup"><span data-stu-id="156be-150">Different time zones:</span></span>

    - <span data-ttu-id="156be-151">Als u tijd weergeeft vanaf een andere locatie (voor het kassierslogboek of door **Registraties tijdklok weergeven** te gebruiken voor een managerscenario), en die locatie zich in een andere tijdzone bevindt, worden de tijdrecords die u ziet, omgezet naar uw plaatselijke tijdzone.</span><span class="sxs-lookup"><span data-stu-id="156be-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="156be-152">U bent bijvoorbeeld een manager voor twee winkels, één in Arizona en andere in Nevada.</span><span class="sxs-lookup"><span data-stu-id="156be-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="156be-153">Een kassamedewerker klokt zich in om 9:00 uur 's ochtends</span><span class="sxs-lookup"><span data-stu-id="156be-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="156be-154">in Arizona.</span><span class="sxs-lookup"><span data-stu-id="156be-154">in Arizona.</span></span> <span data-ttu-id="156be-155">Op dat moment is de tijd in Nevada 8:00 's morgens.</span><span class="sxs-lookup"><span data-stu-id="156be-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="156be-156">Daarom wordt de tijdregistratie gemarkeerd als 8 A.M. als u zich in de winkel in Nevada bevindt en de records voor tijdregistratie bekijkt.</span><span class="sxs-lookup"><span data-stu-id="156be-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="156be-157">Tijdregistraties werknemers weergeven</span><span class="sxs-lookup"><span data-stu-id="156be-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="156be-158">Bekijk de tijdregistraties van de werknemers en filter op opslag- of activiteitstype</span><span class="sxs-lookup"><span data-stu-id="156be-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="156be-159">Op POS:</span><span class="sxs-lookup"><span data-stu-id="156be-159">On POS:</span></span>

- <span data-ttu-id="156be-160">Selecteer **Registraties tijdklok weergeven**.</span><span class="sxs-lookup"><span data-stu-id="156be-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="156be-161">U ziet de activiteiten van de tijdklokregistratie van alle werknemers die zijn toegewezen aan dezelfde opslag als waaraan u bent toegewezen.</span><span class="sxs-lookup"><span data-stu-id="156be-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="156be-162">U kunt het activiteitstype gebruiken en filters opslaan om tijdregistraties te filteren.</span><span class="sxs-lookup"><span data-stu-id="156be-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="156be-163">Tijdregistraties verwerken en beheren</span><span class="sxs-lookup"><span data-stu-id="156be-163">Process and manage time registrations</span></span>

<span data-ttu-id="156be-164">Een Commerce-gebruiker volgt de workflow om tijdregistraties te berekenen, goed te keuren en naar salaris over te brengen.</span><span class="sxs-lookup"><span data-stu-id="156be-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="156be-165">Primaire bewerkingen</span><span class="sxs-lookup"><span data-stu-id="156be-165">Primary operations</span></span>

- <span data-ttu-id="156be-166">Berekenen</span><span class="sxs-lookup"><span data-stu-id="156be-166">Calculate</span></span>
- <span data-ttu-id="156be-167">Goedkeuren</span><span class="sxs-lookup"><span data-stu-id="156be-167">Approve</span></span>
- <span data-ttu-id="156be-168">Indienen voor salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="156be-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="156be-169">Overige veelgebruikte bewerkingen</span><span class="sxs-lookup"><span data-stu-id="156be-169">Other common operations</span></span>

- <span data-ttu-id="156be-170">Massaal uitklokken</span><span class="sxs-lookup"><span data-stu-id="156be-170">Bulk Clock-out</span></span>
- <span data-ttu-id="156be-171">Verzuim registreren</span><span class="sxs-lookup"><span data-stu-id="156be-171">Register Absence</span></span>

<span data-ttu-id="156be-172">Zie [Registraties van procestijd en -aanwezigheid](https://technet.microsoft.com/library/aa573180.aspx) voor meer informatie over het verwerken van tijd- en aanwezigheidsregistraties.</span><span class="sxs-lookup"><span data-stu-id="156be-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>

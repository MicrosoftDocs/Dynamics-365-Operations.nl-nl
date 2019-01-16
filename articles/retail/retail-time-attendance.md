---
title: Tijd- en aanwezigheidsbeheer in Retail
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor beheer van tijd en aanwezigheid in Microsoft Dynamics 365 for Retail.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 4c54909a02376a62a72a986e634649fa0ae54284
ms.contentlocale: nl-nl
ms.lasthandoff: 01/04/2019

---

# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="4a7c0-103">Tijd- en aanwezigheidsbeheer in Retail</span><span class="sxs-lookup"><span data-stu-id="4a7c0-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4a7c0-104">In dit onderwerp worden de scenario's beschreven die worden ondersteund voor beheer van tijd en aanwezigheid in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="4a7c0-105">Het instellen en inplannen van medewerkers beheren</span><span class="sxs-lookup"><span data-stu-id="4a7c0-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="4a7c0-106"> initiële configuratie</span><span class="sxs-lookup"><span data-stu-id="4a7c0-106">Initial configuration</span></span>

- <span data-ttu-id="4a7c0-107">Voer de stappen in de configuratiewizard uit.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="4a7c0-108">Werknemers registreren als tijdregistratiewerknemers.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="4a7c0-109">De planning van de werknemersplannen</span><span class="sxs-lookup"><span data-stu-id="4a7c0-109">Plan worker schedules</span></span>

- <span data-ttu-id="4a7c0-110">Profielen toepassen met behulp van de werkplanner.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="4a7c0-111">Zie [Profielen met behulp van werkplanner toepassen](https://technet.microsoft.com/library/aa551234.aspx) voor meer informatie over werktijdprofielen.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="4a7c0-112">Zie voor informatie over de configuratiestappen [Tijd en aanwezigheid instellen](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a7c0-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="4a7c0-113">Detailhandelspecifieke configuratie</span><span class="sxs-lookup"><span data-stu-id="4a7c0-113">Retail-specific configuration</span></span>

- <span data-ttu-id="4a7c0-114">Schakel een functionaliteitprofiel voor tijdklok in voor medewerkers voor wie u tijdregistratie wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="4a7c0-115">Klik op **POS-functionaliteitsprofielen** &gt; **Functies** &gt; **POS-tijdregistraties** &gt; **Tijdregistratie inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="4a7c0-116">Configureer verkooppuntmachtigingsgroepen om de machtiging Registraties tijdklok weergeven in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="4a7c0-117">Met deze machtiging kan een gebruiker de prikklokregistraties van andere werknemers in de winkel bekijken (en van alle andere winkels waaraan de gebruiker is gekoppeld via het adresboek).</span><span class="sxs-lookup"><span data-stu-id="4a7c0-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="4a7c0-118">U wilt mogelijk deze machtiging inschakelen voor een managerrol maar niet voor de rol van een kassamedewerker.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="4a7c0-119">Klik op **POS-machtigingsgroepen** &gt; **Registraties tijdklok weergeven**.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="4a7c0-120">Tijd registreren</span><span class="sxs-lookup"><span data-stu-id="4a7c0-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="4a7c0-121">Tijdregistraties van kassiers en niet-kassiers</span><span class="sxs-lookup"><span data-stu-id="4a7c0-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="4a7c0-122">Op POS:</span><span class="sxs-lookup"><span data-stu-id="4a7c0-122">On POS:</span></span>

    - <span data-ttu-id="4a7c0-123">Inklokbewerkingen:</span><span class="sxs-lookup"><span data-stu-id="4a7c0-123">Clock-in operations:</span></span>

        - <span data-ttu-id="4a7c0-124">Meld u aan met een niet-ladebewerking of een nieuwe ploegendienst.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="4a7c0-125">Selecteer een tijdklokbewerking.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="4a7c0-126">Selecteer de gewenste bewerking:</span><span class="sxs-lookup"><span data-stu-id="4a7c0-126">Select a desired operation:</span></span>

            - <span data-ttu-id="4a7c0-127">Inklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-127">Clock-in</span></span>
            - <span data-ttu-id="4a7c0-128">Pauze voor werk</span><span class="sxs-lookup"><span data-stu-id="4a7c0-128">Break for Work</span></span>
            - <span data-ttu-id="4a7c0-129">Lunchpauze</span><span class="sxs-lookup"><span data-stu-id="4a7c0-129">Break for Lunch</span></span>
            - <span data-ttu-id="4a7c0-130">Uitklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="4a7c0-131">Huidige status</span><span class="sxs-lookup"><span data-stu-id="4a7c0-131">Current state</span></span></th>
        <th><span data-ttu-id="4a7c0-132">Beschikbare bewerkingen</span><span class="sxs-lookup"><span data-stu-id="4a7c0-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="4a7c0-133">Inklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="4a7c0-134">Pauze voor werk</span><span class="sxs-lookup"><span data-stu-id="4a7c0-134">Break for Work</span></span></li>
        <li><span data-ttu-id="4a7c0-135">Lunchpauze</span><span class="sxs-lookup"><span data-stu-id="4a7c0-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="4a7c0-136">Uitklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="4a7c0-137">Pauze voor werk</span><span class="sxs-lookup"><span data-stu-id="4a7c0-137">Break for Work</span></span></td>
        <td><span data-ttu-id="4a7c0-138">Inklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="4a7c0-139">Lunchpauze</span><span class="sxs-lookup"><span data-stu-id="4a7c0-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="4a7c0-140">Inklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="4a7c0-141">Uitklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-141">Clock-out</span></span></td>
        <td><span data-ttu-id="4a7c0-142">Inklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="4a7c0-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="4a7c0-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="4a7c0-144">Bekijk het bevestigingsbericht weergeven, en controleer of de huidige activiteitstijd correct is.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="4a7c0-145">Logboek:</span><span class="sxs-lookup"><span data-stu-id="4a7c0-145">Logbook:</span></span>

    - <span data-ttu-id="4a7c0-146">Klik op **Logboek** om prikklokactiviteit weer te geven.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="4a7c0-147">Gebruik de tijdsfilters om verschillende tijdvensters te selecteren.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="4a7c0-148">Als u met meerdere opslaglocaties werkt, ziet u hier uw tijdregistraties uit alle winkels waar u tijd hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="4a7c0-149">U kunt het opslagfilter gebruiken om tijdregistraties van een geselecteerde opslag te bekijken.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="4a7c0-150">Verschillende tijdzones:</span><span class="sxs-lookup"><span data-stu-id="4a7c0-150">Different time zones:</span></span>

    - <span data-ttu-id="4a7c0-151">Als u tijd weergeeft vanaf een andere locatie (voor het kassierslogboek of door **Registraties tijdklok weergeven** te gebruiken voor een managerscenario), en die locatie zich in een andere tijdzone bevindt, worden de tijdrecords die u ziet, omgezet naar uw plaatselijke tijdzone.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="4a7c0-152">U bent bijvoorbeeld een manager voor twee winkels, één in Arizona en andere in Nevada.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="4a7c0-153">Een kassamedewerker klokt zich in om 9:00 uur 's ochtends</span><span class="sxs-lookup"><span data-stu-id="4a7c0-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="4a7c0-154">in Arizona.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-154">in Arizona.</span></span> <span data-ttu-id="4a7c0-155">Op dat moment is de tijd in Nevada 8:00 's morgens.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="4a7c0-156">Daarom wordt de tijdregistratie gemarkeerd als 8 A.M. als u zich in de winkel in Nevada bevindt en de records voor tijdregistratie bekijkt.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="4a7c0-157">Tijdregistraties werknemers weergeven</span><span class="sxs-lookup"><span data-stu-id="4a7c0-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="4a7c0-158">Bekijk de tijdregistraties van de werknemers en filter op opslag- of activiteitstype</span><span class="sxs-lookup"><span data-stu-id="4a7c0-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="4a7c0-159">Op POS:</span><span class="sxs-lookup"><span data-stu-id="4a7c0-159">On POS:</span></span>

- <span data-ttu-id="4a7c0-160">Selecteer **Registraties tijdklok weergeven**.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="4a7c0-161">U ziet de activiteiten van de tijdklokregistratie van alle werknemers die zijn toegewezen aan dezelfde opslag als waaraan u bent toegewezen.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="4a7c0-162">U kunt het activiteitstype gebruiken en filters opslaan om tijdregistraties te filteren.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="4a7c0-163">Tijdregistraties verwerken en beheren</span><span class="sxs-lookup"><span data-stu-id="4a7c0-163">Process and manage time registrations</span></span>

<span data-ttu-id="4a7c0-164">Een gebruiker in Dynamics 365 for Retail volgt de werkstroom om tijdregistraties te berekenen, goed te keuren en naar de salarisadministratie over te brengen.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="4a7c0-165">Primaire bewerkingen</span><span class="sxs-lookup"><span data-stu-id="4a7c0-165">Primary operations</span></span>

- <span data-ttu-id="4a7c0-166">Berekenen</span><span class="sxs-lookup"><span data-stu-id="4a7c0-166">Calculate</span></span>
- <span data-ttu-id="4a7c0-167">Goedkeuren</span><span class="sxs-lookup"><span data-stu-id="4a7c0-167">Approve</span></span>
- <span data-ttu-id="4a7c0-168">Indienen voor salarisadministratie</span><span class="sxs-lookup"><span data-stu-id="4a7c0-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="4a7c0-169">Overige veelgebruikte bewerkingen</span><span class="sxs-lookup"><span data-stu-id="4a7c0-169">Other common operations</span></span>

- <span data-ttu-id="4a7c0-170">Massaal uitklokken</span><span class="sxs-lookup"><span data-stu-id="4a7c0-170">Bulk Clock-out</span></span>
- <span data-ttu-id="4a7c0-171">Verzuim registreren</span><span class="sxs-lookup"><span data-stu-id="4a7c0-171">Register Absence</span></span>

<span data-ttu-id="4a7c0-172">Zie [Registraties van procestijd en -aanwezigheid](https://technet.microsoft.com/library/aa573180.aspx) voor meer informatie over het verwerken van tijd- en aanwezigheidsregistraties.</span><span class="sxs-lookup"><span data-stu-id="4a7c0-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>


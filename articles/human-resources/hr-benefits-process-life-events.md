---
title: Levensgebeurtenissen verwerken
description: Tijdens de levenscyclus van werknemers in Microsoft Dynamics 365 Human Resources, kan iedere werknemer verschillende levensgebeurteniswijzigingen ondergaan.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 461f90c3da8fa5b2db14b6dd67a0c19f7eabe867
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793796"
---
# <a name="process-life-events"></a><span data-ttu-id="e9561-103">Levensgebeurtenissen verwerken</span><span class="sxs-lookup"><span data-stu-id="e9561-103">Process life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9561-104">Tijdens de levenscyclus van werknemers in Microsoft Dynamics 365 Human Resources, kan iedere werknemer verschillende levensgebeurteniswijzigingen ondergaan.</span><span class="sxs-lookup"><span data-stu-id="e9561-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="e9561-105">Bijvoorbeeld een huwelijk, verandering van werk of wijziging van gezinsleden of begunstigden.</span><span class="sxs-lookup"><span data-stu-id="e9561-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="e9561-106">Als u levensgebeurtenissen wilt gebruiken, moet u levensgebeurtenissen inschakelen in het formulier voor parameters voor vergoedingen en opties voor de levensgebeurtenissen instellen voor plantypen.</span><span class="sxs-lookup"><span data-stu-id="e9561-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="e9561-107">Voordat u de levensgebeurtenissen kunt verwerken, moet u al minimaal eenmaal een open inschrijving hebben uitgevoerd tijdens een aanstellingstijdvak.</span><span class="sxs-lookup"><span data-stu-id="e9561-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="e9561-108">In de Verenigde Staten vindt een open inschrijving meestal eenmaal per jaar plaats.</span><span class="sxs-lookup"><span data-stu-id="e9561-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="e9561-109">Buiten de Verenigde Staten kan de open inschrijving worden uitgevoerd op het moment van de aanstelling.</span><span class="sxs-lookup"><span data-stu-id="e9561-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="e9561-110">Een medewerker hoeft geen vergoedingsplan te selecteren om te zorgen dat levensgebeurtenissen worden verwerkt, maar de medewerker moeten wel zijn opgenomen in de verwerking van een openstaande inschrijving.</span><span class="sxs-lookup"><span data-stu-id="e9561-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="e9561-111">Gebruik de levensgebeurtenisverwerking wanneer u medewerkers hebt met levensgebeurtenissen die op een toekomstige datum plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="e9561-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="e9561-112">Met deze gebeurtenis worden alle levensgebeurtenissen verwerkt die nog niet zijn verwerkt (zoals toekomstige levensgebeurtenissen of levensgebeurtenissen die zijn toegevoegd en die niet specifiek zijn voor een bepaalde medewerker – een voorbeeld is een nieuwe vergoeding).</span><span class="sxs-lookup"><span data-stu-id="e9561-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="e9561-113">Realtime levensgebeurtenissen zijn verborgen.</span><span class="sxs-lookup"><span data-stu-id="e9561-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="e9561-114">Als het bijvoorbeeld vandaag 1 februari is, op 14 februari medewerker Joe Smith volgens de planning rechtspersonen wijzigt u en de levensgebeurtenisverwerking voor 15 februari uitvoert, worden alle gebeurtenissen tot en met 15 februari verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e9561-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="e9561-115">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Levensgebeurtenissen verwerken**.</span><span class="sxs-lookup"><span data-stu-id="e9561-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="e9561-116">Geef in het dialoogvenster **Levensgebeurtenisproces uitvoeren** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="e9561-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="e9561-117">Veld</span><span class="sxs-lookup"><span data-stu-id="e9561-117">Field</span></span> | <span data-ttu-id="e9561-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e9561-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e9561-119">**Inschrijvingsperiode**</span><span class="sxs-lookup"><span data-stu-id="e9561-119">**Enrollment period**</span></span> | <span data-ttu-id="e9561-120">De inschrijvingsperiode waarvoor de levensgebeurtenissen moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e9561-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="e9561-121">**Rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="e9561-121">**Legal entity**</span></span> | <span data-ttu-id="e9561-122">De rechtspersoon waarvoor levensgebeurtenissen moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e9561-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="e9561-123">**Datum van levensgebeurtenis**</span><span class="sxs-lookup"><span data-stu-id="e9561-123">**Life event date**</span></span> | <span data-ttu-id="e9561-124">Het systeem verwerkt alle gebeurtenissen tijdens de inschrijvingsperiode die plaatsvinden tot en met deze datum.</span><span class="sxs-lookup"><span data-stu-id="e9561-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="e9561-125">**Medewerker**</span><span class="sxs-lookup"><span data-stu-id="e9561-125">**Worker**</span></span> | <span data-ttu-id="e9561-126">De medewerker waarvoor levensgebeurtenissen moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e9561-126">The worker to process life events for.</span></span> <span data-ttu-id="e9561-127">Als u dit veld leeg laat, worden de levensgebeurtenissen voor alle medewerkers verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e9561-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="e9561-128">Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="e9561-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="e9561-129">Voer gegevens in voor het proces.</span><span class="sxs-lookup"><span data-stu-id="e9561-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="e9561-130">Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9561-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="e9561-131">Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9561-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="e9561-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9561-132">Select **OK**.</span></span> <span data-ttu-id="e9561-133">Het proces wordt uitgevoerd met de parameters die u instelt.</span><span class="sxs-lookup"><span data-stu-id="e9561-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="e9561-134">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9561-134">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Geschiktheid voor inschrijving verwerken
description: In dit artikel wordt uitgelegd hoe u het proces voor het bepalen van de geschiktheid voor inschrijving uitvoert.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d978982213e713e362798c49aa57e6dc8b7a862
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230011"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="a2d9d-103">Geschiktheid voor inschrijving verwerken</span><span class="sxs-lookup"><span data-stu-id="a2d9d-103">Process enrollment eligibility</span></span>

<span data-ttu-id="a2d9d-104">In dit artikel wordt uitgelegd hoe u het proces voor het bepalen van de geschiktheid voor inschrijving uitvoert.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="a2d9d-105">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Geschiktheid voor inschrijving verwerken**.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="a2d9d-106">Geef in het dialoogvenster **Geschiktheidsproces voor inschrijving op vergoedingen uitvoeren** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="a2d9d-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="a2d9d-107">Veld</span><span class="sxs-lookup"><span data-stu-id="a2d9d-107">Field</span></span> | <span data-ttu-id="a2d9d-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a2d9d-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a2d9d-109">**Inschrijvingsperiode**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-109">**Enrollment period**</span></span> | <span data-ttu-id="a2d9d-110">De inschrijvingsperiode waarvoor de geschiktheid voor inschrijving moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="a2d9d-111">**Rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-111">**Legal entity**</span></span> | <span data-ttu-id="a2d9d-112">De rechtspersoon waarvoor de geschiktheid voor inschrijving moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="a2d9d-113">**Medewerker**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-113">**Worker**</span></span> | <span data-ttu-id="a2d9d-114">De medewerker waarvoor de geschiktheid voor inschrijving moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="a2d9d-115">Als u dit veld leeg laat, wordt de geschiktheid voor inschrijving voor alle medewerkers verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="a2d9d-116">**Vergoedingsplan**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-116">**Benefit plan**</span></span> | <span data-ttu-id="a2d9d-117">Het vergoedingsplan waarvoor de geschiktheid voor inschrijving moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="a2d9d-118">Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="a2d9d-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="a2d9d-119">Voer gegevens in voor het proces.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="a2d9d-120">Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="a2d9d-121">Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="a2d9d-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-122">Select **OK**.</span></span> <span data-ttu-id="a2d9d-123">Het proces wordt uitgevoerd met de parameters die u instelt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="a2d9d-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="a2d9d-125">Procesresultaten weergeven</span><span class="sxs-lookup"><span data-stu-id="a2d9d-125">View Process Results</span></span>

<span data-ttu-id="a2d9d-126">In dit artikel wordt uitgelegd hoe u de resultaten van het geschiktheidsproces weergeeft.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="a2d9d-127">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Procesresultaten**.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="a2d9d-128">In het formulier **Procesresultaten** zijn de volgende velden opgegeven:</span><span class="sxs-lookup"><span data-stu-id="a2d9d-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="a2d9d-129">Veld</span><span class="sxs-lookup"><span data-stu-id="a2d9d-129">Field</span></span> | <span data-ttu-id="a2d9d-130">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="a2d9d-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a2d9d-131">**Proces-ID**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-131">**Process ID**</span></span> | <span data-ttu-id="a2d9d-132">De unieke id voor de combinatie van werknemer, rechtspersoon en procesuitvoering.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="a2d9d-133">**Procestype**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-133">**Process type**</span></span> | <span data-ttu-id="a2d9d-134">Hiermee wordt het proces aangegeven dat is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-134">This identifies the process that was run.</span></span> <span data-ttu-id="a2d9d-135">Bijvoorbeeld: registratie.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="a2d9d-136">**Tijdstempel**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-136">**Time stamp**</span></span> | <span data-ttu-id="a2d9d-137">De tijd waarop het geschiktheidsproces is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="a2d9d-138">**Rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-138">**Legal entity**</span></span> | <span data-ttu-id="a2d9d-139">De rechtspersoon die tijdens het registratieproces is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="a2d9d-140">**Werknemer**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-140">**Worker**</span></span> | <span data-ttu-id="a2d9d-141">De werknemer die is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="a2d9d-142">\*\*Plan</span><span class="sxs-lookup"><span data-stu-id="a2d9d-142">\*\*Plan</span></span> | <span data-ttu-id="a2d9d-143">Het vergoedingsplan waarvoor de registratie is gedaan.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="a2d9d-144">**Geschiktheidsregel**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-144">**Eligibility rule**</span></span> | <span data-ttu-id="a2d9d-145">De geschiktheidsregel die is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="a2d9d-146">Als er een fout is opgetreden voordat de geschiktheid werd uitgevoerd, is dit leeg.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="a2d9d-147">Bijvoorbeeld: als er geen compensatie voor een werknemer is gedefinieerd, wordt het geschiktheidsproces niet uitgevoerd en blijft dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="a2d9d-148">**Resulterende status**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-148">**Result status**</span></span> | <span data-ttu-id="a2d9d-149">Dit komt wel of niet in aanmerking.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="a2d9d-150">De status van het resultaat komt niet in aanmerking als de werknemer niet voldoet aan de criteria voor de geschiktheidsregel, als er vereiste informatie ontbreekt voor de werknemer, zoals een betalingsfrequentie of vaste compensatie, of als er gegevens ontbreken in het vergoedingsplan waardoor werknemers niet kunnen worden ingeschreven.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="a2d9d-151">**Resulterend bericht**</span><span class="sxs-lookup"><span data-stu-id="a2d9d-151">**Result message**</span></span> | <span data-ttu-id="a2d9d-152">Geeft aan waarom een werknemer niet in aanmerking komt voor een vergoedingsplan of is geslaagd voor een geschiktheidsregel.</span><span class="sxs-lookup"><span data-stu-id="a2d9d-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |


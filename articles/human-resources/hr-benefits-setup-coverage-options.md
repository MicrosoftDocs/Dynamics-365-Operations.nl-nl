---
title: Opties voor dekking maken
description: Dekkingsopties in Microsoft Dynamics 365 Human Resources zijn dekkingsniveaus voor de selectie van een deelnemer in een vergoedingsplan of -programma.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e1d5fc80d93e41626da8eb5bdf8f389fb0bd531
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466177"
---
# <a name="create-coverage-options"></a><span data-ttu-id="96ac8-103">Opties voor dekking maken</span><span class="sxs-lookup"><span data-stu-id="96ac8-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="96ac8-104">Dekkingsopties in Microsoft Dynamics 365 Human Resources zijn dekkingsniveaus voor de selectie van een deelnemer in een vergoedingsplan of -programma.</span><span class="sxs-lookup"><span data-stu-id="96ac8-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="96ac8-105">Dekkingsopties kunnen bijvoorbeeld **Alleen werknemer** zijn voor een medisch plan of **2x salaris** voor een levensverzekeringsplan.</span><span class="sxs-lookup"><span data-stu-id="96ac8-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="96ac8-106">Nadat u dit hebt gedefinieerd, kunt u de dekkingsopties voor vergoedingen opnieuw gebruiken.</span><span class="sxs-lookup"><span data-stu-id="96ac8-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="96ac8-107">U kunt een optie aan een of meer plannen koppelen.</span><span class="sxs-lookup"><span data-stu-id="96ac8-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="96ac8-108">Nadat u de dekkingsopties hebt gedefinieerd, koppelt u de dekkingsopties aan een type vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="96ac8-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="96ac8-109">Het plantype wordt vervolgens gekoppeld aan een vergoedingsplan of -programma.</span><span class="sxs-lookup"><span data-stu-id="96ac8-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="96ac8-110">De dekkingsopties die aan een plantype zijn gekoppeld, zijn beschikbaar voor alle plannen die met dat plantype worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="96ac8-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="96ac8-111">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Dekkingsopties**.</span><span class="sxs-lookup"><span data-stu-id="96ac8-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="96ac8-112">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="96ac8-112">Select **New**.</span></span>

3. <span data-ttu-id="96ac8-113">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="96ac8-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="96ac8-114">Veld</span><span class="sxs-lookup"><span data-stu-id="96ac8-114">Field</span></span> | <span data-ttu-id="96ac8-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="96ac8-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="96ac8-116">**Dekkingsoptie**</span><span class="sxs-lookup"><span data-stu-id="96ac8-116">**Coverage option**</span></span> | <span data-ttu-id="96ac8-117">Een unieke naam voor de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="96ac8-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="96ac8-118">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="96ac8-118">**Description**</span></span> | <span data-ttu-id="96ac8-119">Een omschrijving van de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="96ac8-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="96ac8-120">**Dekkingscode**</span><span class="sxs-lookup"><span data-stu-id="96ac8-120">**Coverage code**</span></span> | <span data-ttu-id="96ac8-121">Met dekkingscodes worden minimum- en maximumbedragen toegewezen aan elk in type persoon dat in aanmerking komt voor de dekking.</span><span class="sxs-lookup"><span data-stu-id="96ac8-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="96ac8-122">Een dekkingscode geeft aan wie is gedekt of hoeveel dekking er voor een plantype is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="96ac8-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="96ac8-123">U kunt het bedrag van de dekking uitdrukken als een bedrag in euro's of een percentage.</span><span class="sxs-lookup"><span data-stu-id="96ac8-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="96ac8-124">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="96ac8-124">For example:</span></span></br></br><span data-ttu-id="96ac8-125">- **Werknemer+1** – om hiervoor in aanmerking te komen, moet de werknemer één gezinslid hebben geselecteerd (als er meer dan één persoon wordt geselecteerd, komt de werknemer niet meer in aanmerking).</span><span class="sxs-lookup"><span data-stu-id="96ac8-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="96ac8-126">- **Werknemer+familie** - om hiervoor in aanmerking te komen, moet de werknemer ten minste twee gezinsleden hebben geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="96ac8-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="96ac8-127">**Maximum aantal**</span><span class="sxs-lookup"><span data-stu-id="96ac8-127">**Maximum number**</span></span> | <span data-ttu-id="96ac8-128">Het maximale aantal gezinsleden.</span><span class="sxs-lookup"><span data-stu-id="96ac8-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="96ac8-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="96ac8-129">**Status**</span></span> | <span data-ttu-id="96ac8-130">De status van de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="96ac8-130">The status of the coverage option.</span></span> <span data-ttu-id="96ac8-131">Als de status van de dekkingsoptie is ingesteld op Inactief, kan de dekkingsoptie niet worden geselecteerd voor plantypen.</span><span class="sxs-lookup"><span data-stu-id="96ac8-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="96ac8-132">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="96ac8-132">**Percent**</span></span> | <span data-ttu-id="96ac8-133">Het percentage.</span><span class="sxs-lookup"><span data-stu-id="96ac8-133">The percent amount.</span></span> <span data-ttu-id="96ac8-134">Dit veld is alleen actief als '% x salaris' is geselecteerd in het veld Dekkingscode.</span><span class="sxs-lookup"><span data-stu-id="96ac8-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="96ac8-135">**Deler**</span><span class="sxs-lookup"><span data-stu-id="96ac8-135">**Divisor**</span></span> | <span data-ttu-id="96ac8-136">De deler die bij de berekening moet worden gebruikt wanneer u de dekkingscode '% x salaris' selecteert.</span><span class="sxs-lookup"><span data-stu-id="96ac8-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="96ac8-137">**Minimumpercentage**</span><span class="sxs-lookup"><span data-stu-id="96ac8-137">**Percent minimum**</span></span> | <span data-ttu-id="96ac8-138">Het minimumpercentage wanneer u de dekkingscode Percentage selecteert.</span><span class="sxs-lookup"><span data-stu-id="96ac8-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="96ac8-139">**Maximumpercentage**</span><span class="sxs-lookup"><span data-stu-id="96ac8-139">**Percent maximum**</span></span> | <span data-ttu-id="96ac8-140">Het maximumpercentage wanneer u de dekkingscode Percentage selecteert.</span><span class="sxs-lookup"><span data-stu-id="96ac8-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="96ac8-141">Koppel onder **Geschiktheidsopties voor persoonlijke contactpersonen** de juiste geschiktheidsoptie voor persoonlijke contactpersonen aan elke dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="96ac8-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="96ac8-142">Geef onder **Selfservice** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="96ac8-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="96ac8-143">Veld</span><span class="sxs-lookup"><span data-stu-id="96ac8-143">Field</span></span> | <span data-ttu-id="96ac8-144">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="96ac8-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="96ac8-145">**Bijdragebedrag werknemer toestaan**</span><span class="sxs-lookup"><span data-stu-id="96ac8-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="96ac8-146">Geeft aan of werknemers het bijdragebedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="96ac8-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="96ac8-147">Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het bijdragebedrag dat de werknemer invoert via de selfservice voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="96ac8-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="96ac8-148">**Dekkingsbedrag werknemer toestaan**</span><span class="sxs-lookup"><span data-stu-id="96ac8-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="96ac8-149">Geeft aan of werknemers het dekkingsbedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="96ac8-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="96ac8-150">Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het dekkingsbedrag dat de werknemer invoert in Werknemerselfservice.</span><span class="sxs-lookup"><span data-stu-id="96ac8-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="96ac8-151">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="96ac8-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
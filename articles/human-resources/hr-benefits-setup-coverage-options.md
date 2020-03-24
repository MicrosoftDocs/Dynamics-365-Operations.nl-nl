---
title: Opties voor dekking maken
description: Dekkingsopties in Microsoft Dynamics 365 Human Resources zijn dekkingsniveaus die een deelnemer aan een vergoedingsplan of -programma kan kiezen, zoals 'Alleen werknemer' voor een medisch plan of '2x salaris' voor een levensverzekeringsplan.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092701"
---
# <a name="create-coverage-options"></a><span data-ttu-id="85e4f-103">Opties voor dekking maken</span><span class="sxs-lookup"><span data-stu-id="85e4f-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="85e4f-104">Dekkingsopties in Microsoft Dynamics 365 Human Resources zijn dekkingsniveaus die een deelnemer aan een vergoedingsplan of -programma kan kiezen, zoals 'Alleen werknemer' voor een medisch plan of '2x salaris' voor een levensverzekeringsplan.</span><span class="sxs-lookup"><span data-stu-id="85e4f-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="85e4f-105">Nadat de opties voor vergoedingsdekking zijn gedefinieerd, worden deze opnieuw bruikbaar en kunt u een optie aan een of meer plannen koppelen.</span><span class="sxs-lookup"><span data-stu-id="85e4f-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="85e4f-106">Zodra de dekkingsopties zijn gedefinieerd, koppelt u de dekkingsopties aan een type vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="85e4f-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="85e4f-107">Het plantype wordt vervolgens gekoppeld aan een vergoedingsplan of -programma.</span><span class="sxs-lookup"><span data-stu-id="85e4f-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="85e4f-108">De dekkingsopties die aan een plantype zijn gekoppeld, zijn beschikbaar voor alle plannen die met dat plantype worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="85e4f-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="85e4f-109">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Dekkingsopties**.</span><span class="sxs-lookup"><span data-stu-id="85e4f-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="85e4f-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="85e4f-110">Select **New**.</span></span>

3. <span data-ttu-id="85e4f-111">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="85e4f-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="85e4f-112">Veld</span><span class="sxs-lookup"><span data-stu-id="85e4f-112">Field</span></span> | <span data-ttu-id="85e4f-113">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85e4f-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="85e4f-114">**Dekkingsoptie**</span><span class="sxs-lookup"><span data-stu-id="85e4f-114">**Coverage option**</span></span> | <span data-ttu-id="85e4f-115">Een unieke naam voor de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="85e4f-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="85e4f-116">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="85e4f-116">**Description**</span></span> | <span data-ttu-id="85e4f-117">Een omschrijving van de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="85e4f-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="85e4f-118">**Dekkingscode**</span><span class="sxs-lookup"><span data-stu-id="85e4f-118">**Coverage code**</span></span> | <span data-ttu-id="85e4f-119">Met dekkingscodes worden minimum- en maximumbedragen toegewezen aan elk in type persoon dat in aanmerking komt voor de dekking.</span><span class="sxs-lookup"><span data-stu-id="85e4f-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="85e4f-120">Een dekkingscode geeft aan wie is gedekt of hoeveel dekking er voor een plantype is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="85e4f-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="85e4f-121">U kunt het bedrag van de dekking uitdrukken als een bedrag in euro's of een percentage.</span><span class="sxs-lookup"><span data-stu-id="85e4f-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="85e4f-122">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="85e4f-122">For example:</span></span></br></br><span data-ttu-id="85e4f-123">- **Werknemer+1** – om hiervoor in aanmerking te komen, moet de werknemer één gezinslid hebben geselecteerd (als er meer dan één persoon wordt geselecteerd, komt de werknemer niet meer in aanmerking).</span><span class="sxs-lookup"><span data-stu-id="85e4f-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="85e4f-124">- **Werknemer+familie** - om hiervoor in aanmerking te komen, moet de werknemer ten minste twee gezinsleden hebben geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="85e4f-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="85e4f-125">**Maximum aantal**</span><span class="sxs-lookup"><span data-stu-id="85e4f-125">**Maximum number**</span></span> | <span data-ttu-id="85e4f-126">Het maximale aantal gezinsleden.</span><span class="sxs-lookup"><span data-stu-id="85e4f-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="85e4f-127">**Status**</span><span class="sxs-lookup"><span data-stu-id="85e4f-127">**Status**</span></span> | <span data-ttu-id="85e4f-128">De status van de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="85e4f-128">The status of the coverage option.</span></span> <span data-ttu-id="85e4f-129">Als de status van de dekkingsoptie is ingesteld op Inactief, kan de dekkingsoptie niet worden geselecteerd voor plantypen.</span><span class="sxs-lookup"><span data-stu-id="85e4f-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="85e4f-130">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="85e4f-130">**Percent**</span></span> | <span data-ttu-id="85e4f-131">Het percentage.</span><span class="sxs-lookup"><span data-stu-id="85e4f-131">The percent amount.</span></span> <span data-ttu-id="85e4f-132">Dit veld is alleen actief als '% x salaris' is geselecteerd in het veld Dekkingscode.</span><span class="sxs-lookup"><span data-stu-id="85e4f-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="85e4f-133">**Deler**</span><span class="sxs-lookup"><span data-stu-id="85e4f-133">**Divisor**</span></span> | <span data-ttu-id="85e4f-134">De deler die bij de berekening moet worden gebruikt wanneer u de dekkingscode '% x salaris' selecteert.</span><span class="sxs-lookup"><span data-stu-id="85e4f-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="85e4f-135">**Minimumpercentage**</span><span class="sxs-lookup"><span data-stu-id="85e4f-135">**Percent minimum**</span></span> | <span data-ttu-id="85e4f-136">Het minimumpercentage wanneer u de dekkingscode Percentage selecteert.</span><span class="sxs-lookup"><span data-stu-id="85e4f-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="85e4f-137">**Maximumpercentage**</span><span class="sxs-lookup"><span data-stu-id="85e4f-137">**Percent maximum**</span></span> | <span data-ttu-id="85e4f-138">Het maximumpercentage wanneer u de dekkingscode Percentage selecteert.</span><span class="sxs-lookup"><span data-stu-id="85e4f-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="85e4f-139">Koppel onder **Geschiktheidsopties voor persoonlijke contactpersonen** de juiste geschiktheidsoptie voor persoonlijke contactpersonen aan elke dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="85e4f-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="85e4f-140">Geef onder **Selfservice** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="85e4f-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="85e4f-141">Veld</span><span class="sxs-lookup"><span data-stu-id="85e4f-141">Field</span></span> | <span data-ttu-id="85e4f-142">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="85e4f-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="85e4f-143">**Bijdragebedrag werknemer toestaan**</span><span class="sxs-lookup"><span data-stu-id="85e4f-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="85e4f-144">Geeft aan of werknemers het bijdragebedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="85e4f-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="85e4f-145">Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het bijdragebedrag dat de werknemer invoert via de selfservice voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="85e4f-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="85e4f-146">**Dekkingsbedrag werknemer toestaan**</span><span class="sxs-lookup"><span data-stu-id="85e4f-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="85e4f-147">Geeft aan of werknemers het dekkingsbedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="85e4f-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="85e4f-148">Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het dekkingsbedrag dat de werknemer invoert in Werknemerselfservice.</span><span class="sxs-lookup"><span data-stu-id="85e4f-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="85e4f-149">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="85e4f-149">Select **Save**.</span></span> 

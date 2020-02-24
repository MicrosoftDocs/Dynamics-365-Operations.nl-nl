---
title: Dekkingsopties maken
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008564"
---
# <a name="create-coverage-options"></a><span data-ttu-id="f14c6-102">Dekkingsopties maken</span><span class="sxs-lookup"><span data-stu-id="f14c6-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f14c6-103">Dekkingsopties in Microsoft Dynamics 365 Human Resources zijn dekkingsniveaus die een deelnemer aan een vergoedingsplan of -programma kan kiezen, zoals 'Alleen werknemer' voor een medisch plan of '2x salaris' voor een levensverzekeringsplan.</span><span class="sxs-lookup"><span data-stu-id="f14c6-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="f14c6-104">Nadat de opties voor vergoedingsdekking zijn gedefinieerd, worden deze opnieuw bruikbaar en kunt u een optie aan een of meer plannen koppelen.</span><span class="sxs-lookup"><span data-stu-id="f14c6-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="f14c6-105">Zodra de dekkingsopties zijn gedefinieerd, koppelt u de dekkingsopties aan een type vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="f14c6-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="f14c6-106">Het plantype wordt vervolgens gekoppeld aan een vergoedingsplan of -programma.</span><span class="sxs-lookup"><span data-stu-id="f14c6-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="f14c6-107">De dekkingsopties die aan een plantype zijn gekoppeld, zijn beschikbaar voor alle plannen die met dat plantype worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f14c6-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="f14c6-108">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Dekkingsopties**.</span><span class="sxs-lookup"><span data-stu-id="f14c6-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="f14c6-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f14c6-109">Select **New**.</span></span>

3. <span data-ttu-id="f14c6-110">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="f14c6-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f14c6-111">Veld</span><span class="sxs-lookup"><span data-stu-id="f14c6-111">Field</span></span> | <span data-ttu-id="f14c6-112">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f14c6-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f14c6-113">**Dekkingsoptie**</span><span class="sxs-lookup"><span data-stu-id="f14c6-113">**Coverage option**</span></span> | <span data-ttu-id="f14c6-114">Een unieke naam voor de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="f14c6-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="f14c6-115">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="f14c6-115">**Description**</span></span> | <span data-ttu-id="f14c6-116">Een omschrijving van de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="f14c6-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="f14c6-117">**Dekkingscode**</span><span class="sxs-lookup"><span data-stu-id="f14c6-117">**Coverage code**</span></span> | <span data-ttu-id="f14c6-118">Met dekkingscodes worden minimum- en maximumbedragen toegewezen aan elk in type persoon dat in aanmerking komt voor de dekking.</span><span class="sxs-lookup"><span data-stu-id="f14c6-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="f14c6-119">Een dekkingscode geeft aan wie is gedekt of hoeveel dekking er voor een plantype is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="f14c6-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="f14c6-120">U kunt het bedrag van de dekking uitdrukken als een bedrag in euro's of een percentage.</span><span class="sxs-lookup"><span data-stu-id="f14c6-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="f14c6-121">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="f14c6-121">For example:</span></span></br></br><span data-ttu-id="f14c6-122">- **Werknemer+1** – om hiervoor in aanmerking te komen, moet de werknemer één gezinslid hebben geselecteerd (als er meer dan één persoon wordt geselecteerd, komt de werknemer niet meer in aanmerking).</span><span class="sxs-lookup"><span data-stu-id="f14c6-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="f14c6-123">- **Werknemer+familie** - om hiervoor in aanmerking te komen, moet de werknemer ten minste twee gezinsleden hebben geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f14c6-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="f14c6-124">**Maximum aantal**</span><span class="sxs-lookup"><span data-stu-id="f14c6-124">**Maximum number**</span></span> | <span data-ttu-id="f14c6-125">Het maximale aantal gezinsleden.</span><span class="sxs-lookup"><span data-stu-id="f14c6-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="f14c6-126">**Status**</span><span class="sxs-lookup"><span data-stu-id="f14c6-126">**Status**</span></span> | <span data-ttu-id="f14c6-127">De status van de dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="f14c6-127">The status of the coverage option.</span></span> <span data-ttu-id="f14c6-128">Als de status van de dekkingsoptie is ingesteld op Inactief, kan de dekkingsoptie niet worden geselecteerd voor plantypen.</span><span class="sxs-lookup"><span data-stu-id="f14c6-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="f14c6-129">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="f14c6-129">**Percent**</span></span> | <span data-ttu-id="f14c6-130">Het percentage.</span><span class="sxs-lookup"><span data-stu-id="f14c6-130">The percent amount.</span></span> <span data-ttu-id="f14c6-131">Dit veld is alleen actief als '% x salaris' is geselecteerd in het veld Dekkingscode.</span><span class="sxs-lookup"><span data-stu-id="f14c6-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="f14c6-132">**Deler**</span><span class="sxs-lookup"><span data-stu-id="f14c6-132">**Divisor**</span></span> | <span data-ttu-id="f14c6-133">De deler die bij de berekening moet worden gebruikt wanneer u de dekkingscode '% x salaris' selecteert.</span><span class="sxs-lookup"><span data-stu-id="f14c6-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="f14c6-134">**Minimumpercentage**</span><span class="sxs-lookup"><span data-stu-id="f14c6-134">**Percent minimum**</span></span> | <span data-ttu-id="f14c6-135">Het minimumpercentage wanneer u de dekkingscode Percentage selecteert.</span><span class="sxs-lookup"><span data-stu-id="f14c6-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="f14c6-136">**Maximumpercentage**</span><span class="sxs-lookup"><span data-stu-id="f14c6-136">**Percent maximum**</span></span> | <span data-ttu-id="f14c6-137">Het maximumpercentage wanneer u de dekkingscode Percentage selecteert.</span><span class="sxs-lookup"><span data-stu-id="f14c6-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="f14c6-138">Koppel onder **Geschiktheidsopties voor persoonlijke contactpersonen** de juiste geschiktheidsoptie voor persoonlijke contactpersonen aan elke dekkingsoptie.</span><span class="sxs-lookup"><span data-stu-id="f14c6-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="f14c6-139">Geef onder **Selfservice** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="f14c6-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="f14c6-140">Veld</span><span class="sxs-lookup"><span data-stu-id="f14c6-140">Field</span></span> | <span data-ttu-id="f14c6-141">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f14c6-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f14c6-142">**Bijdragebedrag werknemer toestaan**</span><span class="sxs-lookup"><span data-stu-id="f14c6-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="f14c6-143">Geeft aan of werknemers het bijdragebedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="f14c6-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f14c6-144">Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het bijdragebedrag dat de werknemer invoert via de selfservice voor vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="f14c6-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="f14c6-145">**Dekkingsbedrag werknemer toestaan**</span><span class="sxs-lookup"><span data-stu-id="f14c6-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="f14c6-146">Geeft aan of werknemers het dekkingsbedrag voor vergoedingen via selfservice mogen wijzigen wanneer ze vergoedingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="f14c6-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f14c6-147">Als u dit selectievakje inschakelt, worden de parameters van het vergoedingsplan berekend op basis van het dekkingsbedrag dat de werknemer invoert in Werknemerselfservice.</span><span class="sxs-lookup"><span data-stu-id="f14c6-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="f14c6-148">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f14c6-148">Select **Save**.</span></span> 

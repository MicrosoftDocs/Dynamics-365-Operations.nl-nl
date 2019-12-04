---
title: Een aanstellingsprocessjabloon maken in Attract
description: Dit onderwerp biedt informatie over het maken van een aanstellingsprocessjabloon in Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 82046d43cf7366b760c140bdb8b017337b4f41da
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832553"
---
# <a name="create-a-hiring-process-template-in-attract"></a><span data-ttu-id="8fa42-103">Een aanstellingsprocessjabloon maken in Attract</span><span class="sxs-lookup"><span data-stu-id="8fa42-103">Create a hiring process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8fa42-104">Een *aanstellingsprocessjabloon* bevat alle activiteiten die moeten worden opgenomen als onderdeel van het aanstellingsproces voor een functie.</span><span class="sxs-lookup"><span data-stu-id="8fa42-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="8fa42-105">In dit onderwerp worden de elementen van een processjabloon in Microsoft Dynamics 365 Talent: Attract beschreven.</span><span class="sxs-lookup"><span data-stu-id="8fa42-105">This topic describes the elements of a process template in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="8fa42-106">Ook wordt uitgelegd hoe u een sjabloon maakt.</span><span class="sxs-lookup"><span data-stu-id="8fa42-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="8fa42-107">Sjabloon maken maakt deel uit van de Uitgebreide invoegtoepassing voor aanstellingen voor Attract.</span><span class="sxs-lookup"><span data-stu-id="8fa42-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="8fa42-108">Sjabloonbeheer</span><span class="sxs-lookup"><span data-stu-id="8fa42-108">Template management</span></span>

<span data-ttu-id="8fa42-109">Organisaties kunnen beslissen of teamleden of alleen beheerders processjablonen kunnen maken in Attract.</span><span class="sxs-lookup"><span data-stu-id="8fa42-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="8fa42-110">Als u sjabloonbeheer wilt configureren, gaat u naar **Beheercentrum** \> **Sjabloonbeheer**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="8fa42-111">Als u teamleden hun eigen sjablonen wilt laten maken, schakelt u sjabloonbeheer in.</span><span class="sxs-lookup"><span data-stu-id="8fa42-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="8fa42-112">Als u sjabloonbeheer niet inschakelt, kunnen alleen beheerders sjablonen maken.</span><span class="sxs-lookup"><span data-stu-id="8fa42-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="8fa42-113">Standaardsjabloon</span><span class="sxs-lookup"><span data-stu-id="8fa42-113">Default template</span></span>

<span data-ttu-id="8fa42-114">Alleen beheerders kunnen de standaardsjabloon instellen.</span><span class="sxs-lookup"><span data-stu-id="8fa42-114">Only admins can set the default template.</span></span> <span data-ttu-id="8fa42-115">De standaardsjabloon wordt gebruikt als geen sjabloon is geselecteerd wanneer een functie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8fa42-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="8fa42-116">Als u de standaardsjabloon wilt instellen, gaat u naar **Beheercentrum** \> **Sjabloonbeheer**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="8fa42-117">Op de kaart voor de sjabloon die de standaardsjabloon worden moet, selecteert u de ellipsisknop (**...**) en selecteert u vervolgens **Als standaard instellen**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="8fa42-118">Een processjabloon maken</span><span class="sxs-lookup"><span data-stu-id="8fa42-118">Create a process template</span></span>

<span data-ttu-id="8fa42-119">Beheerders, wervers en aanstellend managers kunnen processjablonen maken.</span><span class="sxs-lookup"><span data-stu-id="8fa42-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="8fa42-120">Een processjabloon bestaat uit *fasen* en *activiteiten*.</span><span class="sxs-lookup"><span data-stu-id="8fa42-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="8fa42-121">Fasen groeperen een of meer activiteiten.</span><span class="sxs-lookup"><span data-stu-id="8fa42-121">Stages group together one or more activities.</span></span> <span data-ttu-id="8fa42-122">Standaard heeft elke processjabloon Prospect-, Sollicitatie- en Aanbiedingsactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="8fa42-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="8fa42-123">De fasen die deze activiteiten bevatten, kunnen worden hernoemd.</span><span class="sxs-lookup"><span data-stu-id="8fa42-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="8fa42-124">U kunt meer fasen toevoegen door **+ Nieuwe fase** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="8fa42-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="8fa42-125">U kunt activiteiten aan een fase toevoegen door ze naar de juiste fase te slepen of door erop te dubbelklikken in de activiteitenlijst.</span><span class="sxs-lookup"><span data-stu-id="8fa42-125">You can add activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="8fa42-126">Fasenamen zijn zichtbaar voor kandidaten op de pagina **Sollicitatiestatus**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="8fa42-127">U moet dit feit overwegen wanneer u namen voor fasen kiest.</span><span class="sxs-lookup"><span data-stu-id="8fa42-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="8fa42-128">Zie voor meer informatie over activiteiten, [Activiteiten in aanstellingsprocessen](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="8fa42-128">To learn more about activities, see [Activities in hiring processes](./activities-attract.md).</span></span>

<span data-ttu-id="8fa42-129">Volg deze stappen om een aanstellingsprocessjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="8fa42-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="8fa42-130">Ga naar **Sjablonen**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="8fa42-131">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-131">Select **New**.</span></span>
3. <span data-ttu-id="8fa42-132">Voer in het veld **Sjabloonnaam** een naam in voor de sjabloon en selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="8fa42-133">Selecteer in de lijst **Het goedkeuringsproces kiezen** de optie **Standaard** om goedkeuring te vereisen voor een functie.</span><span class="sxs-lookup"><span data-stu-id="8fa42-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="8fa42-134">Selecteer of u prospects inschakelt of uitschakelt.</span><span class="sxs-lookup"><span data-stu-id="8fa42-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="8fa42-135">Optioneel: voeg fasen toe of verwijder fasen.</span><span class="sxs-lookup"><span data-stu-id="8fa42-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="8fa42-136">Als u een fase wilt toevoegen, selecteert u **+ Nieuwe fase**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="8fa42-137">Als u een fase wilt verwijderen, plaatst u de aanwijzer boven de fase en selecteert u vervolgens de prullenbakknop die wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8fa42-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8fa42-138">De fasen Prospect, Sollicitatie en Aanbieding kunnen niet worden verwijderd, maar ze kunnen wel worden hernoemd.</span><span class="sxs-lookup"><span data-stu-id="8fa42-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="8fa42-139">Optioneel: voeg activiteiten toe of verwijder activiteiten.</span><span class="sxs-lookup"><span data-stu-id="8fa42-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="8fa42-140">Als u een activiteit wilt toevoegen, sleept u deze van de activiteitenlijst aan de rechterkant naar de gewenste fase.</span><span class="sxs-lookup"><span data-stu-id="8fa42-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="8fa42-141">Of dubbelklik op de activiteit en selecteer vervolgens de fase waaraan u deze wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8fa42-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="8fa42-142">Als u een activiteit wilt verwijderen, vouwt u deze uit en selecteert u de prullenbakknop in de koptekst van de activiteit.</span><span class="sxs-lookup"><span data-stu-id="8fa42-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="8fa42-143">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8fa42-143">Select **Save**.</span></span>

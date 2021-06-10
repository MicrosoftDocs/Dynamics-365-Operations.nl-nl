---
title: Vaardigheden configureren
description: U kunt de vaardigheden van uw werknemer bijhouden in Dynamics 365 Human Resources. U kunt ook opgeven welke vaardigheden voor een bepaalde functie zijn vereist.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076554"
---
# <a name="configure-skills"></a><span data-ttu-id="c761e-104">Vaardigheden configureren</span><span class="sxs-lookup"><span data-stu-id="c761e-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c761e-105">U kunt de vaardigheden van uw werknemer bijhouden in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c761e-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c761e-106">U kunt ook opgeven welke vaardigheden voor een bepaalde functie zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="c761e-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="c761e-107">Voorbeelden van de vaardigheden die u kunt bijhouden zijn:</span><span class="sxs-lookup"><span data-stu-id="c761e-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="c761e-108">Supervisie - vermogen om toe te zien op het werk van anderen.</span><span class="sxs-lookup"><span data-stu-id="c761e-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="c761e-109">Leiderschap - vermogen om leiding te geven aan medewerkers en bedrijfseenheden.</span><span class="sxs-lookup"><span data-stu-id="c761e-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="c761e-110">Planning: mogelijkheid om vooruit te kijken, visies te ontwikkelen en uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="c761e-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="c761e-111">HTML - vermogen om HTML-code te schrijven.</span><span class="sxs-lookup"><span data-stu-id="c761e-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="c761e-112">Als u nog geen vaardigheidstypen en beoordelingsmodellen hebt ingesteld, moet u er een aantal toevoegen voordat u vaardigheden kunt maken.</span><span class="sxs-lookup"><span data-stu-id="c761e-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="c761e-113">De volgende personen kunnen vaardigheden voor een werknemer invoeren:</span><span class="sxs-lookup"><span data-stu-id="c761e-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="c761e-114">Werknemers kunnen vaardigheden voor zichzelf invoeren in Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="c761e-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="c761e-115">Voor deze vaardigheden is goedkeuring van de manager vereist.</span><span class="sxs-lookup"><span data-stu-id="c761e-115">These skills require manager approval.</span></span>
- <span data-ttu-id="c761e-116">Managers kunnen vaardigheden voor hun werknemers invoeren.</span><span class="sxs-lookup"><span data-stu-id="c761e-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="c761e-117">U kunt een werkstroom maken waarmee deze vaardigheden automatisch worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="c761e-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="c761e-118">Een vaardigheidstype maken</span><span class="sxs-lookup"><span data-stu-id="c761e-118">Create a skill type</span></span>

<span data-ttu-id="c761e-119">Vaardigheidstypen zijn categorieën waaronder afzonderlijke vaardigheden vallen, zoals Administratie of Verkoop.</span><span class="sxs-lookup"><span data-stu-id="c761e-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="c761e-120">Selecteer **Koppelingen** in het werkgebied **Werknemersontwikkeling**.</span><span class="sxs-lookup"><span data-stu-id="c761e-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="c761e-121">Selecteer **Vaardigheidstypen** onder **Competentie-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="c761e-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="c761e-122">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c761e-122">Select **New**.</span></span>

4. <span data-ttu-id="c761e-123">Vul de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="c761e-123">Complete the following fields:</span></span>

   - <span data-ttu-id="c761e-124">**Vaardigheidstype**: voer een unieke naam voor het vaardigheidstype in.</span><span class="sxs-lookup"><span data-stu-id="c761e-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="c761e-125">**Omschrijving**: voer een omschrijving voor het vaardigheidstype in.</span><span class="sxs-lookup"><span data-stu-id="c761e-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="c761e-126">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c761e-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="c761e-127">Een beoordelingsmodel maken</span><span class="sxs-lookup"><span data-stu-id="c761e-127">Create a rating model</span></span>

<span data-ttu-id="c761e-128">Beoordelingsmodellen helpen te beoordelen wat het werkelijke vaardigheidsniveau van een persoon is, het niveau dat ze moeten zien te bereiken of het vaardigheidsniveau dat ze voor een taak moeten hebben.</span><span class="sxs-lookup"><span data-stu-id="c761e-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="c761e-129">Aan elk niveau in een beoordelingsmodel wordt een factor toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c761e-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="c761e-130">Selecteer **Koppelingen** in het werkgebied **Werknemersontwikkeling**.</span><span class="sxs-lookup"><span data-stu-id="c761e-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="c761e-131">Selecteer **Beoordelingsmodellen** onder **Competentie-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="c761e-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="c761e-132">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c761e-132">Select **New**.</span></span>

4. <span data-ttu-id="c761e-133">Vul de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="c761e-133">Complete the following fields:</span></span>

   - <span data-ttu-id="c761e-134">**Beoordeling**: voer een naam in voor het beoordelingsmodel, zoals **Vaardigheden**.</span><span class="sxs-lookup"><span data-stu-id="c761e-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="c761e-135">**Omschrijving**: voer een omschrijving in voor het beoordelingsmodel, zoals **Vaardigheidsbeoordelingen**.</span><span class="sxs-lookup"><span data-stu-id="c761e-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="c761e-136">Selecteer **Nieuw** in de sectie **Niveaus**.</span><span class="sxs-lookup"><span data-stu-id="c761e-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="c761e-137">Vul de volgende velden in voor elk niveau dat u wilt toevoegen:</span><span class="sxs-lookup"><span data-stu-id="c761e-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="c761e-138">**Niveau**: voer een naam voor het niveau in.</span><span class="sxs-lookup"><span data-stu-id="c761e-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="c761e-139">**Omschrijving**: voer een omschrijving in voor het niveau.</span><span class="sxs-lookup"><span data-stu-id="c761e-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="c761e-140">**Factor**: voer een factorwaarde in van 0-9.</span><span class="sxs-lookup"><span data-stu-id="c761e-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="c761e-141">Factorwaarden worden gebruikt om scores te normaliseren van vaardigheden die verschillende beoordelingsmodellen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c761e-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="c761e-142">Elk niveau moet een unieke factor hebben.</span><span class="sxs-lookup"><span data-stu-id="c761e-142">Each level must have a unique factor.</span></span> <span data-ttu-id="c761e-143">Niveaus met een hogere factorwaarden zijn belangrijker in een beoordelingsmodel.</span><span class="sxs-lookup"><span data-stu-id="c761e-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="c761e-144">Ga indien nodig door met het toevoegen van niveaus.</span><span class="sxs-lookup"><span data-stu-id="c761e-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="c761e-145">U kunt tot maximaal 10 niveaus invoeren voor elk beoordelingsmodel.</span><span class="sxs-lookup"><span data-stu-id="c761e-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="c761e-146">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c761e-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="c761e-147">Een vaardigheid maken</span><span class="sxs-lookup"><span data-stu-id="c761e-147">Create a skill</span></span>

<span data-ttu-id="c761e-148">Voordat u een vaardigheid kunt toewijzen, een zoekopdracht voor vaardigheidstoewijzingen of een vaardigheidsprofiel kunt maken, moet u informatie over de vaardigheden op de pagina **Vaardigheden** invoeren.</span><span class="sxs-lookup"><span data-stu-id="c761e-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="c761e-149">Voor elke vaardigheid kunt u een vaardigheidstype en een beoordelingsmodel selecteren.</span><span class="sxs-lookup"><span data-stu-id="c761e-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="c761e-150">Selecteer **Koppelingen** in het werkgebied **Werknemersontwikkeling**.</span><span class="sxs-lookup"><span data-stu-id="c761e-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="c761e-151">Selecteer **Vaardigheden** onder **Competentie-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="c761e-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="c761e-152">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c761e-152">Select **New**.</span></span>

4. <span data-ttu-id="c761e-153">Vul de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="c761e-153">Complete the following fields:</span></span>

   - <span data-ttu-id="c761e-154">**Vaardigheid**: voer een naam voor de vaardigheid in.</span><span class="sxs-lookup"><span data-stu-id="c761e-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="c761e-155">**Omschrijving**: voer een omschrijving voor de vaardigheid in.</span><span class="sxs-lookup"><span data-stu-id="c761e-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="c761e-156">**Beoordeling**: selecteer het beoordelingsmodel dat u voor deze vaardigheid wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c761e-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="c761e-157">**Vaardigheidstype**: selecteer een vaardigheidstype in de lijst met vaardigheidstypen.</span><span class="sxs-lookup"><span data-stu-id="c761e-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="c761e-158">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c761e-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c761e-159">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c761e-159">See also</span></span>

[<span data-ttu-id="c761e-160">Vaardigheden invoeren</span><span class="sxs-lookup"><span data-stu-id="c761e-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="c761e-161">Vaardigheden toewijzen</span><span class="sxs-lookup"><span data-stu-id="c761e-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
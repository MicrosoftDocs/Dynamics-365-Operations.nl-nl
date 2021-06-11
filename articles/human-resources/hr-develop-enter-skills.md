---
title: Vaardigheden invoeren
description: Werknemers en managers kunnen vaardigheden invoeren in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076586"
---
# <a name="enter-skills"></a><span data-ttu-id="35759-103">Vaardigheden invoeren</span><span class="sxs-lookup"><span data-stu-id="35759-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="35759-104">U kunt gewenste vaardigheden of werkelijke vaardigheden voor werknemers, sollicitanten of contactpersonen invoeren in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="35759-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="35759-105">Een gewenste vaardigheid is een vaardigheid die een persoon van plan is te verwerven.</span><span class="sxs-lookup"><span data-stu-id="35759-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="35759-106">Een werkelijke vaardigheid is een vaardigheid die iemand op dat moment heeft.</span><span class="sxs-lookup"><span data-stu-id="35759-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="35759-107">Een werkstroom maken voor het automatisch goedkeuren van vaardigheden</span><span class="sxs-lookup"><span data-stu-id="35759-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="35759-108">Als u vaardigheden wilt invoeren zonder dat deze hoeven te worden goedgekeurd, moet u een werkstroom maken om vaardigheden automatisch goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="35759-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="35759-109">Vaardigheden die door werknemers worden ingevoerd, moeten altijd door de manager worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="35759-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="35759-110">Met deze werkstroom worden alleen vaardigheden automatisch goedgekeurd die door managers zijn ingevoerd namens hun werknemers.</span><span class="sxs-lookup"><span data-stu-id="35759-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="35759-111">In de werkruimte **Personeelsbeheer** selecteert u **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="35759-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="35759-112">Selecteer onder **Instellen** de optie **Werkstromen voor Human resources**.</span><span class="sxs-lookup"><span data-stu-id="35759-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="35759-113">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="35759-113">Select **New**.</span></span>

4. <span data-ttu-id="35759-114">Selecteer **Werknemersvaardigheden** in het deelvenster **Werkstroom maken**.</span><span class="sxs-lookup"><span data-stu-id="35759-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="35759-115">[![Werkstroom voor werknemersvaardigheden selecteren](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="35759-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="35759-116">Selecteer **Openen** in het dialoogvenster **Dit bestand openen?**.</span><span class="sxs-lookup"><span data-stu-id="35759-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="35759-117">Voer uw inloggegevens in wanneer dit gevraagd wordt.</span><span class="sxs-lookup"><span data-stu-id="35759-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="35759-118">Selecteer in de werkstroomeditor het element van de werkstroom **Vaardigheden goedkeuren** en sleep het naar het canvas.</span><span class="sxs-lookup"><span data-stu-id="35759-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="35759-119">[![Element van werkstroom Vaardigheden goedkeuren selecteren](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="35759-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="35759-120">Koppel het element **Begin** aan het element **Vaardigheden goedkeuren 1** en koppel het element **Vaardigheden goedkeuren 1** aan het element **Einde**.</span><span class="sxs-lookup"><span data-stu-id="35759-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="35759-121">U moet mogelijk naar beneden bladeren om het element **Einde** te zien.</span><span class="sxs-lookup"><span data-stu-id="35759-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="35759-122">U kunt dit element dichter naar de andere elementen slepen.</span><span class="sxs-lookup"><span data-stu-id="35759-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="35759-123">[![Werkstroomelementen koppelen](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="35759-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="35759-124">Dubbelklik op het element van de werkstroom **Vaardigheden goedkeuren 1** en klik vervolgens met de rechtermuisknop op het element **Stap 1**.</span><span class="sxs-lookup"><span data-stu-id="35759-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="35759-125">Klik met de rechtermuisknop op het element **Stap 1** en selecteer vervolgens **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="35759-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="35759-126">Selecteer **Voorwaarde** op de linkernavigatiebalk in het venster **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="35759-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="35759-127">Selecteer **Deze stap alleen uitvoeren als aan de volgende voorwaarde wordt voldaan**.</span><span class="sxs-lookup"><span data-stu-id="35759-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="35759-128">Selecteer **Voorwaarde toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="35759-128">Select **Add condition**.</span></span> <span data-ttu-id="35759-129">Na **Waar** selecteert u **Vaardigheden selfservice werknemers** en vervolgens selecteert u **Vaardigheden selfservice werknemers.Persoon**.</span><span class="sxs-lookup"><span data-stu-id="35759-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="35759-130">Na **is** selecteert u **veld** en vervolgens selecteert u **Relatie van gebruiker tot persoon.Persoon**.</span><span class="sxs-lookup"><span data-stu-id="35759-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="35759-131">[![Voorwaarde opgeven](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="35759-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="35759-132">Selecteer **Toewijzing** op de linkernavigatiebalk.</span><span class="sxs-lookup"><span data-stu-id="35759-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="35759-133">Selecteer **Hiërarchie** op het tabblad **Toewijzingstype**.</span><span class="sxs-lookup"><span data-stu-id="35759-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="35759-134">Selecteer **Managementhiërarchie** in het veld **Hiërarchietype:** op het tabblad **Hiërarchie selecteren**.</span><span class="sxs-lookup"><span data-stu-id="35759-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="35759-135">[![Managementhiërarchie opgeven](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="35759-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="35759-136">Selecteer **Sluiten**, selecteer **Werkstroom** in de canvas-breadcrumb en selecteer vervolgens **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="35759-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="35759-137">Zie [Overzicht van werkstroomsysteem](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json) voor meer informatie over het maken van werkstromen.</span><span class="sxs-lookup"><span data-stu-id="35759-137">For more information about creating workflows, see [Workflow system overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="35759-138">Vaardigheden voor een werknemer invoeren</span><span class="sxs-lookup"><span data-stu-id="35759-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="35759-139">Selecteer een werknemer.</span><span class="sxs-lookup"><span data-stu-id="35759-139">Select a worker.</span></span>

2. <span data-ttu-id="35759-140">Selecteer **Persoon** op de actiebalk van de pagina **Werknemer** en selecteer vervolgens **Vaardigheden**.</span><span class="sxs-lookup"><span data-stu-id="35759-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="35759-141">Vul op de pagina **Vaardigheden** de volgende velden in voor elke vaardigheid:</span><span class="sxs-lookup"><span data-stu-id="35759-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="35759-142">**Vaardigheid**: selecteer een vaardigheid.</span><span class="sxs-lookup"><span data-stu-id="35759-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="35759-143">**Niveautype**: selecteer **Werkelijk** voor een vaardigheid die de werknemer al heeft of selecteer **Doel** voor een vaardigheid waar de werknemer aan werkt.</span><span class="sxs-lookup"><span data-stu-id="35759-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="35759-144">**Niveau**: selecteer een niveau voor de vaardigheid van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="35759-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="35759-145">**Niveaudatum**: selecteer een datum in de kalenderfunctie.</span><span class="sxs-lookup"><span data-stu-id="35759-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="35759-146">**Examinator**: selecteer indien van toepassing een examinator in de lijst.</span><span class="sxs-lookup"><span data-stu-id="35759-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="35759-147">U kunt de zoekopdracht filteren.</span><span class="sxs-lookup"><span data-stu-id="35759-147">You can filter your search.</span></span>
   - <span data-ttu-id="35759-148">**Jaren ervaring**: voer de jaren aan ervaring in.</span><span class="sxs-lookup"><span data-stu-id="35759-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="35759-149">**Geverifieerd**: als de vaardigheid is geverifieerd, schakelt u het selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="35759-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="35759-150">**Geverifieerd door**: voer de naam van de controleur in.</span><span class="sxs-lookup"><span data-stu-id="35759-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="35759-151">Wanneer u klaar bent met het invoeren van vaardigheden, selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="35759-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="35759-152">Zie ook</span><span class="sxs-lookup"><span data-stu-id="35759-152">See also</span></span>

[<span data-ttu-id="35759-153">Vaardigheden configureren</span><span class="sxs-lookup"><span data-stu-id="35759-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="35759-154">Vaardigheden toewijzen</span><span class="sxs-lookup"><span data-stu-id="35759-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
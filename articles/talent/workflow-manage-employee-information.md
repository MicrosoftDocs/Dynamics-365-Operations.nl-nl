---
title: Informatie over werknemers beheren met behulp van workflows
description: In dit onderwerp wordt uitgelegd hoe u de workflowmogelijkheid voor Human resources kunt gebruiken om werknemersgegevens te beheren. U kunt bijvoorbeeld een workflow aan een positie koppelen en een goedkeuringsworkflow configureren die wordt gestart wanneer werknemers hun record wijzigen.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2dc4671e0b68dffe30fe73d8c95113481673a27a
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="bb76a-104">Informatie over werknemers beheren met behulp van workflows</span><span class="sxs-lookup"><span data-stu-id="bb76a-104">Use workflows to manage employee information</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bb76a-105">In dit onderwerp wordt uitgelegd hoe u de workflowmogelijkheid voor Human resources kunt gebruiken om werknemersgegevens te beheren.</span><span class="sxs-lookup"><span data-stu-id="bb76a-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="bb76a-106">U kunt bijvoorbeeld een workflow aan een positie koppelen en een goedkeuringsworkflow configureren die wordt gestart wanneer werknemers hun record wijzigen.</span><span class="sxs-lookup"><span data-stu-id="bb76a-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="bb76a-107">De workflowmogelijkheid voor Human resources biedt een groot aantal workflows voor het beheren van human resources-activiteiten.</span><span class="sxs-lookup"><span data-stu-id="bb76a-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="bb76a-108">Bovendien zijn er vele opties beschikbaar zodat u specifieke workflows kunt wijzigen en deze aan een rapportagehiërarchie kunt koppelen.</span><span class="sxs-lookup"><span data-stu-id="bb76a-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="bb76a-109">Workflows zijn beschikbaar om wijzigingen in verschillende typen werknemersinformatie gemakkelijker te beheren.</span><span class="sxs-lookup"><span data-stu-id="bb76a-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="bb76a-110">U kunt een workflow koppelen aan een positie.</span><span class="sxs-lookup"><span data-stu-id="bb76a-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="bb76a-111">Vervolgens wordt er, als werknemers hun werknemersrecord wijzigen, een workflow gestart die moet worden goedgekeurd voordat de nieuwe informatie wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="bb76a-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="bb76a-112">Workflows worden vooraf gedefinieerd voor de volgende typen informatie om wijzigingen efficiënt te beheren en uw werknemersgegevens nauwkeurig te houden:</span><span class="sxs-lookup"><span data-stu-id="bb76a-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="bb76a-113">Identificatienummers</span><span class="sxs-lookup"><span data-stu-id="bb76a-113">Identification numbers</span></span>
-   <span data-ttu-id="bb76a-114">Cursussen</span><span class="sxs-lookup"><span data-stu-id="bb76a-114">Courses</span></span>
-   <span data-ttu-id="bb76a-115">Opleiding</span><span class="sxs-lookup"><span data-stu-id="bb76a-115">Education</span></span>
-   <span data-ttu-id="bb76a-116">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="bb76a-116">Image</span></span>
-   <span data-ttu-id="bb76a-117">Geleende artikelen</span><span class="sxs-lookup"><span data-stu-id="bb76a-117">Loaned items</span></span>
-   <span data-ttu-id="bb76a-118">Beroepservaring</span><span class="sxs-lookup"><span data-stu-id="bb76a-118">Professional experience</span></span>
-   <span data-ttu-id="bb76a-119">Projectervaring</span><span class="sxs-lookup"><span data-stu-id="bb76a-119">Project experience</span></span>
-   <span data-ttu-id="bb76a-120">Vaardigheden</span><span class="sxs-lookup"><span data-stu-id="bb76a-120">Skills</span></span>
-   <span data-ttu-id="bb76a-121">Vertrouwensposities</span><span class="sxs-lookup"><span data-stu-id="bb76a-121">Positions of trust</span></span>
-   <span data-ttu-id="bb76a-122">Acties van Human Resources</span><span class="sxs-lookup"><span data-stu-id="bb76a-122">Human resources actions</span></span>
-   <span data-ttu-id="bb76a-123">Cursusregistratie</span><span class="sxs-lookup"><span data-stu-id="bb76a-123">Course registration</span></span>

<span data-ttu-id="bb76a-124">Wanneer werknemers worden aangesteld of overgeplaatst of wanneer hun dienstverband wordt beëindigd, kan de workflow een controleproces bevatten.</span><span class="sxs-lookup"><span data-stu-id="bb76a-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="bb76a-125">Op deze manier kan een document worden herzien of kunnen de voorwaarden van een actie als onderdeel van de workflow worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="bb76a-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="bb76a-126">Wanneer het controleproces is voltooid, wordt het document of de actie voltooid en wordt de workflow verplaatst naar een laatste goedkeuringsstap.</span><span class="sxs-lookup"><span data-stu-id="bb76a-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="bb76a-127">Een workflow koppelen aan een positiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="bb76a-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="bb76a-128">U kunt een workflow koppelen aan elke hiërarchie die u configureert.</span><span class="sxs-lookup"><span data-stu-id="bb76a-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="bb76a-129">Als bijvoorbeeld een positie is gekoppeld aan een matrixrapportagehiërarchie, kunt u een workflow configureren waarmee onkosten voor een bepaald project worden doorgestuurd naar de projectleider in plaats van de manager van de werknemer die is gekoppeld aan die positie.</span><span class="sxs-lookup"><span data-stu-id="bb76a-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="bb76a-130">Als u een nieuwe workflow wilt maken of een bestaande workflow wilt wijzigen op de pagina **Workflow voor Human resources**, klikt u op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="bb76a-131">Selecteer een workflow in de lijst om de workflowontwerper te starten.</span><span class="sxs-lookup"><span data-stu-id="bb76a-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="bb76a-132">U kunt de ontwerper gebruiken om een nieuwe workflow te maken of om de stappen in een bestaande workflow te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="bb76a-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="bb76a-133">Wanneer u een bestaande workflow wijzigt, worden uw wijzigingen opgeslagen als een nieuwe versie.</span><span class="sxs-lookup"><span data-stu-id="bb76a-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="bb76a-134">U kunt dus altijd teruggaan naar een vorige versie als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="bb76a-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="bb76a-135">Een workflow voor Human resources configureren</span><span class="sxs-lookup"><span data-stu-id="bb76a-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="bb76a-136">Voer de volgende stappen uit om een eenvoudige workflow te configureren die wordt gestart wanneer werknemers een wijziging van hun persoonlijke identificatienummer aanvragen.</span><span class="sxs-lookup"><span data-stu-id="bb76a-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="bb76a-137">Klik op de pagina **Human resources-workflows** op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="bb76a-138">Selecteer in de lijst met beschikbare workflows **Identificatienummers**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="bb76a-139">Klik op **Uitvoeren** om de workflowontwerper te starten en voer vervolgens uw gebruikersnaam en wachtwoord in wanneer u dat wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="bb76a-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="bb76a-140">Sleep het element **Identificatienummer goedkeuren** vanuit de lijst met workflowelementen naar het ontwerperscanvas.</span><span class="sxs-lookup"><span data-stu-id="bb76a-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="bb76a-141">Verbind het goedkeuringselement met **Starten** en **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="bb76a-142">Dubbelklik op **Element goedkeuren** en klik vervolgens met de rechtermuisknop en selecteer **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="bb76a-143">Voer de volgende stappen uit om werkiteminstructies toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="bb76a-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="bb76a-144">Selecteer **Toewijzing** en selecteer vervolgens **Hiërarchie** onder het toewijzingstype.</span><span class="sxs-lookup"><span data-stu-id="bb76a-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="bb76a-145">Selecteer onder de sectie **Hiërarchie** **Configureerbare hiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="bb76a-146">Voeg een stopvoorwaarde toe en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bb76a-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="bb76a-147">Voer eventuele extra instructies uit (er mogen geen extra waarschuwingen aanwezig zijn).</span><span class="sxs-lookup"><span data-stu-id="bb76a-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="bb76a-148">Klik op **Opslaan en afsluiten**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-148">Click **Save and close**.</span></span> <span data-ttu-id="bb76a-149">Activeer de nieuwe workflow wanneer het dialoogvenster wordt geopend en selecteer **Actief maken**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="bb76a-150">Ga naar **Human Resources** &gt; **Posities** &gt; **Positiehiërarchietypen**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="bb76a-151">Selecteer **Matrix**.</span><span class="sxs-lookup"><span data-stu-id="bb76a-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="bb76a-152">Voeg de workflow **Identificatienummer van werknemer** aan de lijst toe.</span><span class="sxs-lookup"><span data-stu-id="bb76a-152">Add the **Worker identification number** workflow to the list.</span></span>






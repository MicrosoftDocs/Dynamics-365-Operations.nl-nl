---
title: Een nieuw project maken
description: Dit onderwerp biedt informatie over het maken van een nieuw project.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760513"
---
# <a name="create-a-new-project"></a><span data-ttu-id="783fd-103">Een nieuw project maken</span><span class="sxs-lookup"><span data-stu-id="783fd-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="783fd-104">Voer de volgende stappen uit om een nieuw project te maken.</span><span class="sxs-lookup"><span data-stu-id="783fd-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="783fd-105">Selecteer op de pagina **Projectbeheer** de optie **Nieuw project** en voer de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="783fd-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="783fd-106">**Projecttype:** Tijd en materiaal</span><span class="sxs-lookup"><span data-stu-id="783fd-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="783fd-107">**Projectnaam:** Xyz-upgrade fase 2</span><span class="sxs-lookup"><span data-stu-id="783fd-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="783fd-108">**Projectgroep:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="783fd-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="783fd-109">**Projectcontract-id:** 00000002</span><span class="sxs-lookup"><span data-stu-id="783fd-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="783fd-110">Selecteer **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="783fd-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="783fd-111">Een resource toewijzen aan een project</span><span class="sxs-lookup"><span data-stu-id="783fd-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="783fd-112">Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de record van de werknemer waarvoor u eerder competenties hebt geconfigureerd. Open vervolgens de werknemerrecord.</span><span class="sxs-lookup"><span data-stu-id="783fd-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="783fd-113">Selecteer in het actievenster op het tabblad **Project** in de groep **Instellingen** de optie **Projecten toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="783fd-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="783fd-114">Filter op de pagina **Projecttoewijzingen voor resourcevalidatie** op het tabblad **Projecten** het veld **Het project toevoegen aan geselecteerde projecten** op het project **XYZ-upgrade Fase 2**.</span><span class="sxs-lookup"><span data-stu-id="783fd-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="783fd-115">Selecteer een project in het deelvenster **Resterende projecten** en selecteer de pijlknop om het toe te voegen aan het deelvenster **Geselecteerde projecten**.</span><span class="sxs-lookup"><span data-stu-id="783fd-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="783fd-116">Indien nodig kunt u ook categorieën aan een resource toewijzen.</span><span class="sxs-lookup"><span data-stu-id="783fd-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="783fd-117">Het categorietype is **Kosten** of **Opbrengst**.</span><span class="sxs-lookup"><span data-stu-id="783fd-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="783fd-118">Uw organisatie bepaalt het categorietype.</span><span class="sxs-lookup"><span data-stu-id="783fd-118">The category type is determined by your organization.</span></span> <span data-ttu-id="783fd-119">Als er geen categorieën zijn toegewezen voor een resource, wordt in Finance de standaardcategorie voor uurtarieven voor kosten en opbrengsten opgezocht.</span><span class="sxs-lookup"><span data-stu-id="783fd-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="783fd-120">Kenmerken voor projectresource en rollen configureren</span><span class="sxs-lookup"><span data-stu-id="783fd-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="783fd-121">Een projectmanager kan de resourcingfunctionaliteit van het project gebruiken om de rollen te maken die het project vereist.</span><span class="sxs-lookup"><span data-stu-id="783fd-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="783fd-122">Rollen kunnen worden gebruikt als tijdens het reserveren van resources nog geen bevestigde resources bekend zijn.</span><span class="sxs-lookup"><span data-stu-id="783fd-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="783fd-123">Met rollen kunt u resources tijdelijk reserveren als gepland, zodat u de projectplanningsfasen kunt voortzetten.</span><span class="sxs-lookup"><span data-stu-id="783fd-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="783fd-124">[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="783fd-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="783fd-125">**Scenario:** Contoso is aangezocht om een project van het type Tijd en materiaal uit te voeren, dat een goedgekeurd projectcharter heeft.</span><span class="sxs-lookup"><span data-stu-id="783fd-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="783fd-126">De juniorprojectmanager is nog bezig de reikwijdte van het project te bepalen.</span><span class="sxs-lookup"><span data-stu-id="783fd-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="783fd-127">De resourcemanager identificeert momenteel specifieke resources die worden gereserveerd om aan het nieuwe project te werken.</span><span class="sxs-lookup"><span data-stu-id="783fd-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="783fd-128">Vanwege de kritieke aard van het project heeft de projectsponsor om de senior projectmanager gevraagd als een van de rollen.</span><span class="sxs-lookup"><span data-stu-id="783fd-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="783fd-129">De resourcemanager moet de nieuwe resource verkrijgen en de rol in het systeem definiëren, voor het geval de junior projectmanager de resourcegegevens tijdens de projectplanning nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="783fd-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="783fd-130">De volgende stappen geven weer hoe de resourcemanager rol Senior projectmanager kan configureren en er resourcekenmerken aan kan toewijzen.</span><span class="sxs-lookup"><span data-stu-id="783fd-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="783fd-131">Later kan de worden gebruikt om te zoeken naar beschikbare resources die voldoen aan de vereiste resourcecompetenties.</span><span class="sxs-lookup"><span data-stu-id="783fd-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="783fd-132">Selecteer op de pagina **Rollen instellen** de optie **Nieuw** en voer de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="783fd-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="783fd-133">**Rol-ID:** Senior projectmanager</span><span class="sxs-lookup"><span data-stu-id="783fd-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="783fd-134">**Beschrijving:** Senior projectmanager</span><span class="sxs-lookup"><span data-stu-id="783fd-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="783fd-135">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="783fd-135">Select **Create**.</span></span>
3. <span data-ttu-id="783fd-136">Selecteer de rol **Senior projectmanager** en selecteer **Kenmerken configureren**.</span><span class="sxs-lookup"><span data-stu-id="783fd-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="783fd-137">Selecteer in het veld **Type kenmerk** de waarde **Vaardigheid**.</span><span class="sxs-lookup"><span data-stu-id="783fd-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="783fd-138">Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u zoekt.</span><span class="sxs-lookup"><span data-stu-id="783fd-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="783fd-139">Selecteer in het veld **Type kenmerk** de waarde **Getuigschrift**.</span><span class="sxs-lookup"><span data-stu-id="783fd-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="783fd-140">Voer in het veld **Beschikbare kenmerken** het type getuigschrift in waarnaar u zoekt.</span><span class="sxs-lookup"><span data-stu-id="783fd-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="783fd-141">Een projectresource toewijzen aan een project</span><span class="sxs-lookup"><span data-stu-id="783fd-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="783fd-142">Op de pagina **Alle projecten** selecteert u het project **XYZ-upgrade Fase 2**.</span><span class="sxs-lookup"><span data-stu-id="783fd-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="783fd-143">Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="783fd-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="783fd-144">Selecteer in het veld **Rol** de waarde **Teamlid**.</span><span class="sxs-lookup"><span data-stu-id="783fd-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="783fd-145">Selecteer **Boeken vanuit kalender**.</span><span class="sxs-lookup"><span data-stu-id="783fd-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="783fd-146">Selecteer op de pagina **Resourcebeschikbaarheid** de optie **Weergave-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="783fd-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="783fd-147">Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="783fd-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="783fd-148">**Indeling voor weergave datumbereik:** Dag</span><span class="sxs-lookup"><span data-stu-id="783fd-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="783fd-149">**Beschikbaarheidsomschrijvingen weergeven:** Ja</span><span class="sxs-lookup"><span data-stu-id="783fd-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="783fd-150">**Resterende capaciteit weergeven:** Ja</span><span class="sxs-lookup"><span data-stu-id="783fd-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="783fd-151">Selecteer in de lijst van resources een resource.</span><span class="sxs-lookup"><span data-stu-id="783fd-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="783fd-152">Selecteer **Vast boek** en **Volledige capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="783fd-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="783fd-153">Een resource aan een standaardrol toewijzen</span><span class="sxs-lookup"><span data-stu-id="783fd-153">Assign a resource to a default role</span></span>

<span data-ttu-id="783fd-154">Om project- of resourcemanagers te helpen, kan verder worden ingezoomd op de resources die voor een project kunnen worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="783fd-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="783fd-155">U kunt een standaardrol aan een bestaande resource toewijzen of aan nieuw verworven resource.</span><span class="sxs-lookup"><span data-stu-id="783fd-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="783fd-156">Toen bijvoorbeeld Daniel werd aangenomen, had hij de ervaring en vaardigheden voor de rol Bedrijfsanalist.</span><span class="sxs-lookup"><span data-stu-id="783fd-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="783fd-157">De resourcemanager heeft deze rol toegewezen als Daniel's standaardrol.</span><span class="sxs-lookup"><span data-stu-id="783fd-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="783fd-158">Daartoe heeft de resourcemanager Daniel toegevoegd aan een groep bedrijfsanalisten die beschikbaar zijn voor het werken aan projecten.</span><span class="sxs-lookup"><span data-stu-id="783fd-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="783fd-159">Tijdens resourcereservering kunnen de projectmanagers de rolresources filteren die beschikbaar zijn om aan projecten te werken.</span><span class="sxs-lookup"><span data-stu-id="783fd-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="783fd-160">Ze kunnen deze informatie als een criterium gebruiken wanneer ze de beslissingsanalyse met meerdere criteria uitvoeren tijdens het vervullen van resources.</span><span class="sxs-lookup"><span data-stu-id="783fd-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="783fd-161">Ze kunnen ook andere resourcekenmerken aan het filter toevoegen, om te zoeken naar resources die bepaalde vaardigheden, opleiding, en ervaring hebben voor een bepaald project.</span><span class="sxs-lookup"><span data-stu-id="783fd-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="783fd-162">**Scenario:** Een goedgekeurd project is van start gegaan en de rol Senior projectmanager is gereserveerd als geplande resource tijdens de projectplanningsfase.</span><span class="sxs-lookup"><span data-stu-id="783fd-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="783fd-163">De resourcemanager heeft nu een resource verworven om de rol van Senior projectmanager te vervullen.</span><span class="sxs-lookup"><span data-stu-id="783fd-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="783fd-164">Selecteer op de pagina **Resourcelijst** de waarde **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="783fd-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="783fd-165">Selecteer op de pagina **Resourcerol** de optie **Nieuw** en voer de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="783fd-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="783fd-166">**Ingangsdatum:** voer de huidige datum in.</span><span class="sxs-lookup"><span data-stu-id="783fd-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="783fd-167">**Vervaldatum:** voer **Nooit** in.</span><span class="sxs-lookup"><span data-stu-id="783fd-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="783fd-168">**Rol:** voer **Senior projectmanager** in.</span><span class="sxs-lookup"><span data-stu-id="783fd-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="783fd-169">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="783fd-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="783fd-170">Voeg op het tabblad **Competenties** de vaardigheid **Projectbeheer** en het getuigschrift **PMP** toe.</span><span class="sxs-lookup"><span data-stu-id="783fd-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>

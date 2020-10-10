---
title: Een projectteam maken
description: Dit onderwerp biedt informatie over het maken en beheren van projectteams.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760514"
---
# <a name="create-a-project-team"></a><span data-ttu-id="39331-103">Een projectteam maken</span><span class="sxs-lookup"><span data-stu-id="39331-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39331-104">Om de rollen te gebruiken die eerder in een project zijn geconfigureerd, moet een projectmanager de rollen aan het project koppelen.</span><span class="sxs-lookup"><span data-stu-id="39331-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="39331-105">Voor een project kunnen meerdere rollen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="39331-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="39331-106">Om verwarring te voorkomen, worden deze rollen automatisch gelabeld tijdens de reservering.</span><span class="sxs-lookup"><span data-stu-id="39331-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="39331-107">Als de projectmanager drie software-engineers nodig heeft, worden bijvoorbeeld automatisch drie software-engineerrollen gegenereerd met de labels **Software-engineer 1**, **Software-engineer 2** en **Software-engineer 3**.</span><span class="sxs-lookup"><span data-stu-id="39331-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="39331-108">Als voor de rol eerder rolkenmerken zijn ingesteld, worden deze toegepast als filter in zoekopdrachten naar een resource.</span><span class="sxs-lookup"><span data-stu-id="39331-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="39331-109">Aanvullende kenmerken kunnen indien nodig worden toegevoegd om het zoeken te verfijnen.</span><span class="sxs-lookup"><span data-stu-id="39331-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="39331-110">Weergave-instellingen kunnen ook worden aangepast voor een betere weergave van de beschikbaarheid van resources.</span><span class="sxs-lookup"><span data-stu-id="39331-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="39331-111">Er zijn opties voor weergave van beschikbaarheid per uur, dag, week, maand, kwartaal en jaar.</span><span class="sxs-lookup"><span data-stu-id="39331-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="39331-112">Er is ook een optie om beschikbaar en resterende capaciteit van resources weer te geven.</span><span class="sxs-lookup"><span data-stu-id="39331-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="39331-113">Deze optie is handig voor tijdbeheer, wanneer u beschikbare tijd voor activiteiten of resourcebeschikbaarheid raamt.</span><span class="sxs-lookup"><span data-stu-id="39331-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="39331-114">De projectmanager kan een rol op de pagina selecteren en vervolgens, als er een beschikbare resource is die aan de vereisten voldoet, daarvoor een resource reserveren die de rol vervult.</span><span class="sxs-lookup"><span data-stu-id="39331-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="39331-115">De resources hoeven niet op dit moment in de planningsfase te worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="39331-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="39331-116">Wanneer u een WBS maakt, kunt u rollen vervangen door bemande resources voor het project.</span><span class="sxs-lookup"><span data-stu-id="39331-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="39331-117">Als rollen worden vervangen door bemande rollen in de WBS, werkt de resourceconfiguratie automatisch de projectteamlijst en de planning bij.</span><span class="sxs-lookup"><span data-stu-id="39331-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="39331-118">[![Projectteamlijst die zowel rollen als werkelijke resources bevat](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="39331-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="39331-119">De projectmanager heeft verschillende opties om een resource op een project te boeken, zoals **Resterende capaciteit**, **Volledige capaciteit**, **Percentage van capaciteit** en **Uren opgeven**.</span><span class="sxs-lookup"><span data-stu-id="39331-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="39331-120">Deze boekingsopties kunnen op elk moment worden geannuleerd als de resourcetoewijzingen wijzigen.</span><span class="sxs-lookup"><span data-stu-id="39331-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="39331-121">Twee typen boeking worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="39331-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="39331-122">**Vast boeken**: De resourcereservering is goedgekeurd en is bevestigd om aan de taak te werken voor de opgegeven periode.</span><span class="sxs-lookup"><span data-stu-id="39331-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="39331-123">**Variabel boeken**: De resourcereservering is voorlopig ingesteld om aan de taak te werken voor de opgegeven periode.</span><span class="sxs-lookup"><span data-stu-id="39331-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="39331-124">De onderstaande procedure licht toe hoe u een projectteam maakt.</span><span class="sxs-lookup"><span data-stu-id="39331-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="39331-125">Een projectteam maken</span><span class="sxs-lookup"><span data-stu-id="39331-125">Create a project team</span></span>

1. <span data-ttu-id="39331-126">Selecteer een project op de lijstpagina **Alle projecten** en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="39331-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="39331-127">Voer op het tabblad **Projectteam en planning** in het veld **Planning einddatum** de begindatum van het schema plus één maand in.</span><span class="sxs-lookup"><span data-stu-id="39331-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="39331-128">Als bijvoorbeeld de planningbegindatum 24 juni 2017 is (24-06-2017), voert u **24-07-2017** in.</span><span class="sxs-lookup"><span data-stu-id="39331-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="39331-129">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="39331-129">Select **Add**.</span></span>
4. <span data-ttu-id="39331-130">Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Senior projectmanager**.</span><span class="sxs-lookup"><span data-stu-id="39331-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="39331-131">Selecteer **Vereiste competenties**.</span><span class="sxs-lookup"><span data-stu-id="39331-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="39331-132">Op de pagina **Kenmerken kiezen** zijn de kenmerken die u eerder hebt ingesteld voor de rol Senior projectmanager automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="39331-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="39331-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="39331-133">Select **OK**.</span></span>
7. <span data-ttu-id="39331-134">Voer op de pagina **Rollen toevoegen aan project** in het veld **Aantal resources** de waarde **1** in.</span><span class="sxs-lookup"><span data-stu-id="39331-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="39331-135">In het veld **Resource** geeft de zoekopdracht alle resources weer die de vereiste competenties hebben.</span><span class="sxs-lookup"><span data-stu-id="39331-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="39331-136">Selecteer **Daniel Goldschmidt** en **Maken**.</span><span class="sxs-lookup"><span data-stu-id="39331-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="39331-137">Selecteer op de pagina **Project** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="39331-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="39331-138">Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Teamlid**.</span><span class="sxs-lookup"><span data-stu-id="39331-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="39331-139">Voer in het veld **Aantal resources** de waarde **5** in.</span><span class="sxs-lookup"><span data-stu-id="39331-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="39331-140">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="39331-140">Select **Create**.</span></span>
12. <span data-ttu-id="39331-141">Selecteer op de pagina **Projecten** de optie **Voorzien in resource**.</span><span class="sxs-lookup"><span data-stu-id="39331-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="39331-142">Projectteams bewaken</span><span class="sxs-lookup"><span data-stu-id="39331-142">Monitor project teams</span></span>
1. <span data-ttu-id="39331-143">Selecteer op de pagina **Alle projecten** de koppeling **Project-ID** voor het project **XYZ-upgrade Fase 2**.</span><span class="sxs-lookup"><span data-stu-id="39331-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="39331-144">Controleer op het sneltabblad **Projectteam en planning** of de daar vermelde projectresources correct zijn.</span><span class="sxs-lookup"><span data-stu-id="39331-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
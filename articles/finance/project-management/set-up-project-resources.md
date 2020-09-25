---
title: Projectresources instellen
description: Dit onderwerp bevat informatie over het instellen of aanvragen van projectresources.
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760518"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="c4533-103">Projectresources instellen</span><span class="sxs-lookup"><span data-stu-id="c4533-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4533-104">U moet een kalender configureren en deze aan een werknemer of een medewerker (uitvoerende) koppelen.</span><span class="sxs-lookup"><span data-stu-id="c4533-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="c4533-105">De kalender wordt gebruikt om het project en de werktijd van de resources te plannen, die voor het project zijn gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="c4533-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="c4533-106">Tijdens het configureren van de kalender kunnen projectmanagers resources herverdelen in het kader van optimalisatie van de resources.</span><span class="sxs-lookup"><span data-stu-id="c4533-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="c4533-107">Op basis van het kalenderplan kunnen beperkingen aan resources worden opgelegd.</span><span class="sxs-lookup"><span data-stu-id="c4533-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="c4533-108">U kunt een kalender instellen op de pagina **Kalenders**.</span><span class="sxs-lookup"><span data-stu-id="c4533-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="c4533-109">Wanneer u een werknemer als een projectresource instelt, u kunt kiezen uit de werknemers die werken in het bedrijf waarvoor u resources instelt.</span><span class="sxs-lookup"><span data-stu-id="c4533-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="c4533-110">U kunt ook werknemers selecteren van andere bedrijven binnen uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="c4533-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="c4533-111">Dit zijn intercompany-resources.</span><span class="sxs-lookup"><span data-stu-id="c4533-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="c4533-112">In de volgende procedures wordt beschreven hoe u een werknemer configureert als een projectresource binnen uw bedrijf en hoe u een intercompany-projectresource configureert.</span><span class="sxs-lookup"><span data-stu-id="c4533-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="c4533-113">Een medewerker instellen als een projectresource</span><span class="sxs-lookup"><span data-stu-id="c4533-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="c4533-114">Selecteer op de pagina **Medewerkers** in de lijst **Medewerkers** de medewerker die u als projectresource toevoegt en open de record van de medewerker.</span><span class="sxs-lookup"><span data-stu-id="c4533-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="c4533-115">In het actievenster selecteert u **Project** &gt; **Instellen** &gt; **Projectinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="c4533-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="c4533-116">Selecteer een kalender en sluit vervolgens de pagina.</span><span class="sxs-lookup"><span data-stu-id="c4533-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="c4533-117">U kunt ook standaardprojecten voor een resource opgeven als een type toewijzing vooraf.</span><span class="sxs-lookup"><span data-stu-id="c4533-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="c4533-118">Voorafgaande toewijzingen kunnen worden gebruikt wanneer de resource- of projectmanager van tevoren al weet aan welke projecten de resource zal gaan werken.</span><span class="sxs-lookup"><span data-stu-id="c4533-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="c4533-119">Voorafgaande toewijzingen kunnen plaatsvinden op basis van aanvragen van een projectsponsor of klant.</span><span class="sxs-lookup"><span data-stu-id="c4533-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="c4533-120">Als u voorafgaande toewijzingen wilt uitvoeren voor een project, selecteert u het gewenste project op de pagina **Projecten toewijzen** op het tabblad **Projecten** in de lijst **Resterende projecten**.</span><span class="sxs-lookup"><span data-stu-id="c4533-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="c4533-121">Een intercompany-resource instellen</span><span class="sxs-lookup"><span data-stu-id="c4533-121">Set up an intercompany resource</span></span>

<span data-ttu-id="c4533-122">Wanneer u een werknemer als een intercompany-resource instelt, moet u de instellingen uitvoeren in het bedrijf dat de werknemer uitleent en in het bedrijf dat de werknemer leent.</span><span class="sxs-lookup"><span data-stu-id="c4533-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="c4533-123">In het uitlenende bedrijf</span><span class="sxs-lookup"><span data-stu-id="c4533-123">In the lending company</span></span>

1. <span data-ttu-id="c4533-124">Controleer in Finance of het uitlenende bedrijf is geselecteerd en voer de bovenstaande procedure Een werknemer instellen als een projectresource uit.</span><span class="sxs-lookup"><span data-stu-id="c4533-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="c4533-125">Selecteer op de pagina **Intercompany-boekhouding** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c4533-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="c4533-126">Selecteer in het veld **Rechtspersoon-ID** het uitlenende bedrijf.</span><span class="sxs-lookup"><span data-stu-id="c4533-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="c4533-127">Vul de resterende velden in met de vereiste waarden en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c4533-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="c4533-128">Selecteer op de pagina **Prijs overboeken** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c4533-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="c4533-129">Selecteer in het veld **Lenende rechtspersoon** het betreffende bedrijf.</span><span class="sxs-lookup"><span data-stu-id="c4533-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="c4533-130">Als u aan het lenende bedrijf alleen de resource wilt uitlenen die u hebt gemaakt aan het begin van deze sectie, selecteert u in het veld **Resource** de naam van de resource die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c4533-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="c4533-131">Als u alle resources in het uitlenende bedrijf beschikbaar wilt stellen voor het lenende bedrijf, laat u het veld **Resource** leeg.</span><span class="sxs-lookup"><span data-stu-id="c4533-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="c4533-132">Stel op de pagina **Projectbeheer- en boekhoudingsparameters** op het tabblad **Intercompany** de optie **Intercompany-resourceplanning en urenstaten inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c4533-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="c4533-133">In het lenende bedrijf</span><span class="sxs-lookup"><span data-stu-id="c4533-133">In the borrowing company</span></span>

- <span data-ttu-id="c4533-134">Voer op de pagina **Resourcelijst** in het zoekfilter de naam in van de resource die u hebt gemaakt in de vorige procedure voor het uitlenende bedrijf, om te controleren of de naam voorkomt in de lijst met resources voor het lenende bedrijf.</span><span class="sxs-lookup"><span data-stu-id="c4533-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="c4533-135">Projectresources aanvragen</span><span class="sxs-lookup"><span data-stu-id="c4533-135">Request project resources</span></span>
<span data-ttu-id="c4533-136">De planningsfunctionaliteit voor projectresources biedt resourcemanagers alleen de mogelijkheid om bemande resources te distribueren voor taken of projecten.</span><span class="sxs-lookup"><span data-stu-id="c4533-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="c4533-137">Als u deze functionaliteit wilt inschakelen, voert u de volgende taken uit of controleert u of ze zijn voltooid:</span><span class="sxs-lookup"><span data-stu-id="c4533-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="c4533-138">Nummerreeksen instellen.</span><span class="sxs-lookup"><span data-stu-id="c4533-138">Set up number sequences.</span></span>
- <span data-ttu-id="c4533-139">Workflows voor projectbeheer en boekhouding instellen.</span><span class="sxs-lookup"><span data-stu-id="c4533-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="c4533-140">Workflows voor resourceaanvraag inschakelen.</span><span class="sxs-lookup"><span data-stu-id="c4533-140">Enable resource request workflows.</span></span>

<span data-ttu-id="c4533-141">Nadat u deze taken hebt voltooid, kunt u zo nodig de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="c4533-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="c4533-142">Een resourceaanvraag maken op basis van een variabel geboekte bemande resource.</span><span class="sxs-lookup"><span data-stu-id="c4533-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="c4533-143">Resourceaanvragen bewaken.</span><span class="sxs-lookup"><span data-stu-id="c4533-143">Monitor resource requests.</span></span>
- <span data-ttu-id="c4533-144">Resourceaanvragen vervullen.</span><span class="sxs-lookup"><span data-stu-id="c4533-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="c4533-145">Een bemande resource aanvragen vanuit een projectstructuur.</span><span class="sxs-lookup"><span data-stu-id="c4533-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="c4533-146">Resources boeken voor een project zonder een aanvraag voor een bemande resource.</span><span class="sxs-lookup"><span data-stu-id="c4533-146">Book resources to a project without having a request for a staffed resource.</span></span>

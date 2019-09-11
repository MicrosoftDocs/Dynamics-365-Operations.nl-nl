---
title: Onderhoudsmedewerkers van voorkeur instellen
description: In dit onderwerp wordt uitgelegd hoe u onderhoudsmedewerkers van voorkeur instelt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887406"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="084d1-103">Onderhoudsmedewerkers van voorkeur</span><span class="sxs-lookup"><span data-stu-id="084d1-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="084d1-104">U kunt een voorkeur instellen maken met betrekking tot welke onderhoudsmedewerkers moeten worden toegewezen om werkorders te voltooien tijdens de planning van werkorders.</span><span class="sxs-lookup"><span data-stu-id="084d1-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="084d1-105">Het gebruik van deze functionaliteit is optioneel, maar het kan u helpen om een keuze te maken voor de meest gekwalificeerde onderhoudsmedewerker om een taak te voltooien, op basis van vaardigheden en competenties van medewerkers.</span><span class="sxs-lookup"><span data-stu-id="084d1-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="084d1-106">Daarom worden bij de planning van werkorders de instellingen in **Onderhoudsmedewerkers van voorkeur** gebruikt om te bepalen of een specifieke onderhoudsmedewerker of medewerkersgroep moet worden gepland voor een werkorder.</span><span class="sxs-lookup"><span data-stu-id="084d1-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="084d1-107">Er worden alleen onderhoudsmedewerkers gepland die beschikbaar zijn op de planningstijd.</span><span class="sxs-lookup"><span data-stu-id="084d1-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="084d1-108">Als een voorkeursinstelling voor onderhoudsmedewerkers overeenkomt met een werkorder tijdens de planning, maar de onderhoudsmedewerker is toegewezen aan andere taken, wordt de werkorder gepland voor een andere, beschikbare onderhoudsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="084d1-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="084d1-109">Voordat u onderhoudsmedewerkers van voorkeur kunt instellen, moet u de onderhoudsmedewerkers en medewerkersgroepen instellen die beschikbaar moeten zijn voor selectie.</span><span class="sxs-lookup"><span data-stu-id="084d1-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="084d1-110">Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor informatie over het instellen van onderhoudsmedewerkers en medewerkersgroepen.</span><span class="sxs-lookup"><span data-stu-id="084d1-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="084d1-111">Medewerkers van voorkeur instellen</span><span class="sxs-lookup"><span data-stu-id="084d1-111">Set up preferred workers</span></span>

<span data-ttu-id="084d1-112">Een onderhoudsmedewerker of medewerkersgroep kan worden gerelateerd aan een bepaald(e)</span><span class="sxs-lookup"><span data-stu-id="084d1-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="084d1-113">Handel</span><span class="sxs-lookup"><span data-stu-id="084d1-113">trade</span></span>  
- <span data-ttu-id="084d1-114">variant van een onderhoudstaaktype</span><span class="sxs-lookup"><span data-stu-id="084d1-114">maintenance job type variant</span></span>  
- <span data-ttu-id="084d1-115">type onderhoudstaak</span><span class="sxs-lookup"><span data-stu-id="084d1-115">maintenance job type</span></span>  
- <span data-ttu-id="084d1-116">categorie onderhoudstaaktype</span><span class="sxs-lookup"><span data-stu-id="084d1-116">maintenance job type category</span></span>  
- <span data-ttu-id="084d1-117">activum</span><span class="sxs-lookup"><span data-stu-id="084d1-117">asset</span></span>  
- <span data-ttu-id="084d1-118">activumtype</span><span class="sxs-lookup"><span data-stu-id="084d1-118">asset type</span></span>  

<span data-ttu-id="084d1-119">of een combinatie van deze selecties.</span><span class="sxs-lookup"><span data-stu-id="084d1-119">or a combination of those selections.</span></span> <span data-ttu-id="084d1-120">Hoe meer selecties u voor dezelfde record maakt, hoe specifieker uw instellingen zijn.</span><span class="sxs-lookup"><span data-stu-id="084d1-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="084d1-121">Klik op **Activabeheer** > **Instellingen** > **Medewerkers** > **Onderhoudsmedewerkers van voorkeur**.</span><span class="sxs-lookup"><span data-stu-id="084d1-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="084d1-122">Klik op **Nieuw** om een nieuwe registratie te maken.</span><span class="sxs-lookup"><span data-stu-id="084d1-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="084d1-123">Maak eerst een standaardinstelling voor onderhoudsmedewerkers of medewerkersgroepen zonder selecties in de lijst met opsommingstekens hierboven.</span><span class="sxs-lookup"><span data-stu-id="084d1-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="084d1-124">Dit betekent dat u alleen een selectie maakt in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur**.</span><span class="sxs-lookup"><span data-stu-id="084d1-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="084d1-125">In de volgende afbeelding ziet u een voorbeeld in de eerste record waarin Aanvragen is geselecteerd als de onderhoudsmedewerkergroep van voorkeur.</span><span class="sxs-lookup"><span data-stu-id="084d1-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="084d1-126">De standaardinstellingen worden gebruikt tijdens de planning van de werkorder als er geen andere, specifiekere combinatie overeenkomt met de inhoud van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="084d1-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="084d1-127">Herhaal stap 2 om een nieuwe record te maken.</span><span class="sxs-lookup"><span data-stu-id="084d1-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="084d1-128">Maak de vereiste selecties, afhankelijk van het detailniveau voor de medewerker of medewerkersgroep van voorkeur.</span><span class="sxs-lookup"><span data-stu-id="084d1-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="084d1-129">*Voorbeeld*: in de volgende afbeelding is in de zesde record de onderhoudsmedewerker Shawn Richardson geselecteerd als medewerker van voorkeur.</span><span class="sxs-lookup"><span data-stu-id="084d1-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="084d1-130">Hij wordt automatisch geselecteerd tijdens de planning van een werkorder met het activum CH-BP1-03-02 en het onderhoudstaaktype Beoordeling van faciliteit als hij op de geplande tijd beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="084d1-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="084d1-131">Wanneer er een onderhoudsmedewerker van voorkeur wordt geselecteerd tijdens de planning van de werkorder, doorloopt Activabeheer alle records met **onderhoudsmedewerkers van voorkeur** om deze op een mogelijke overeenkomst te controleren, waarbij altijd de meest specifieke combinatie eerst wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="084d1-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="084d1-132">Als er geen overeenkomst wordt gevonden, wordt de standaardrecord met een selectie in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="084d1-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Figuur 1](media/02-work-order-scheduling.png)

<span data-ttu-id="084d1-134">U kunt ook verantwoordelijke onderhoudswerkers instellen die kunnen worden geselecteerd wanneer een onderhoudsverzoek of werkorder wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="084d1-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="084d1-135">In **Alle werkorders** en **Alle onderhoudsverzoeken** kunt u zo nodig de selectie bewerken.</span><span class="sxs-lookup"><span data-stu-id="084d1-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="084d1-136">Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="084d1-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="084d1-137">Tijdens de planning van werkorders worden verschillende scores berekend om te bepalen welke medewerkers de taken met betrekking tot een werkorder moeten voltooien (deze scores worden ingesteld via **Parameters voor activabeheer** > **Planning werkorder**).</span><span class="sxs-lookup"><span data-stu-id="084d1-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="084d1-138">Als twee of meer onderhoudsmedewerkers of verantwoordelijke onderhoudsmedewerkers dezelfde score krijgen tijdens de werkorderplanning, wordt een willekeurige medewerker geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="084d1-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="084d1-139">Anders is het altijd de medewerker met de hoogste score die wordt toegewezen om een werkorder te voltooien.</span><span class="sxs-lookup"><span data-stu-id="084d1-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>


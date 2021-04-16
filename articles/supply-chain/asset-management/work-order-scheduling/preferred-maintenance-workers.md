---
title: Onderhoudsmedewerkers van voorkeur instellen
description: In dit onderwerp wordt uitgelegd hoe u onderhoudsmedewerkers van voorkeur instelt in Activabeheer.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5b044e4616555559be51b0846327b1d55bfe47b3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822534"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="acea6-103">Onderhoudsmedewerkers van voorkeur instellen</span><span class="sxs-lookup"><span data-stu-id="acea6-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="acea6-104">Tijdens de planning van werkorders kunt u een voorkeur instellen met betrekking tot welke onderhoudsmedewerker of mederwerkersgroep u wilt toewijzen om de werkorder te voltooien.</span><span class="sxs-lookup"><span data-stu-id="acea6-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="acea6-105">Het gebruik van deze functionaliteit is optioneel, maar het kan u helpen om een keuze te maken voor de meest gekwalificeerde onderhoudsmedewerker om een taak te voltooien, op basis van vaardigheden en competenties van medewerkers.</span><span class="sxs-lookup"><span data-stu-id="acea6-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="acea6-106">Er worden alleen onderhoudsmedewerkers gepland die beschikbaar zijn op de planningstijd.</span><span class="sxs-lookup"><span data-stu-id="acea6-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="acea6-107">Als een voorkeursinstelling voor een onderhoudsmedewerker tijdens de planning overeenkomt met een werkorder, maar de onderhoudsmedewerker al is toegewezen aan andere taken, wordt de werkorder gepland voor een andere, beschikbare onderhoudsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="acea6-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="acea6-108">Voordat u voorkeursonderhoudsmedewerkers kunt instellen, moet u eerst de onderhoudsmedewerkers en medewerkersgroepen instellen.</span><span class="sxs-lookup"><span data-stu-id="acea6-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="acea6-109">Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor een beschrijving van hoe u onderhoudsmedewerkers en medewerkersgroepen instelt.</span><span class="sxs-lookup"><span data-stu-id="acea6-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="acea6-110">Medewerkers van voorkeur instellen</span><span class="sxs-lookup"><span data-stu-id="acea6-110">Set up preferred workers</span></span>

<span data-ttu-id="acea6-111">Een voorkeursonderhoudsmedewerker of medewerkersgroep kan worden gerelateerd aan een of meer van de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="acea6-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="acea6-112">Handel</span><span class="sxs-lookup"><span data-stu-id="acea6-112">trade</span></span>  
- <span data-ttu-id="acea6-113">variant van een onderhoudstaaktype</span><span class="sxs-lookup"><span data-stu-id="acea6-113">maintenance job type variant</span></span>  
- <span data-ttu-id="acea6-114">type onderhoudstaak</span><span class="sxs-lookup"><span data-stu-id="acea6-114">maintenance job type</span></span>  
- <span data-ttu-id="acea6-115">categorie onderhoudstaaktype</span><span class="sxs-lookup"><span data-stu-id="acea6-115">maintenance job type category</span></span>  
- <span data-ttu-id="acea6-116">activum</span><span class="sxs-lookup"><span data-stu-id="acea6-116">asset</span></span>  
- <span data-ttu-id="acea6-117">activumtype</span><span class="sxs-lookup"><span data-stu-id="acea6-117">asset type</span></span>  

<span data-ttu-id="acea6-118">Hoe meer selecties u voor dezelfde record maakt, hoe specifieker uw instellingen zijn.</span><span class="sxs-lookup"><span data-stu-id="acea6-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="acea6-119">Klik op **Activabeheer** > **Instellingen** > **Medewerkers** > **Onderhoudsmedewerkers van voorkeur**.</span><span class="sxs-lookup"><span data-stu-id="acea6-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="acea6-120">Klik op **Nieuw** om een nieuwe registratie te maken.</span><span class="sxs-lookup"><span data-stu-id="acea6-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="acea6-121">Maak eerst een 'standaard'onderhoudsmedewerker of -medewerkersgroep.</span><span class="sxs-lookup"><span data-stu-id="acea6-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="acea6-122">Dit betekent dat u alleen een selectie maakt in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur**.</span><span class="sxs-lookup"><span data-stu-id="acea6-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="acea6-123">In onderstaande schermafbeelding ziet u een voorbeeld in de eerste record waarin Aanvragen is geselecteerd als de **Voorkeursonderhoudsmedewerkersgroep**.</span><span class="sxs-lookup"><span data-stu-id="acea6-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="acea6-124">De standaardinstellingen worden gebruikt tijdens de planning van de werkorder als er geen andere, specifiekere combinatie overeenkomt met de inhoud van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="acea6-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="acea6-125">Herhaal stap 2 om een nieuwe record te maken.</span><span class="sxs-lookup"><span data-stu-id="acea6-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="acea6-126">Maak de vereiste selecties, afhankelijk van het detailniveau voor de medewerker of medewerkersgroep van voorkeur.</span><span class="sxs-lookup"><span data-stu-id="acea6-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="acea6-127">*Voorbeeld*: in onderstaande schermafbeelding is in de zesde record de onderhoudsmedewerker Shawn Richardson geselecteerd als voorkeursmedewerker.</span><span class="sxs-lookup"><span data-stu-id="acea6-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="acea6-128">Hij wordt tijdens de planning van een werkorder met het activum CH-BP1-03-02 en het onderhoudstaaktype Beoordeling van faciliteit automatisch geselecteerd als hij op de geplande tijd beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="acea6-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="acea6-129">Wanneer er een onderhoudsmedewerker van voorkeur wordt geselecteerd tijdens de planning van de werkorder, doorloopt Activabeheer alle records met **onderhoudsmedewerkers van voorkeur** om deze op een mogelijke overeenkomst te controleren, waarbij altijd de meest specifieke combinatie eerst wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="acea6-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="acea6-130">Als er geen overeenkomst wordt gevonden, wordt de standaardrecord met een selectie in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="acea6-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Figuur 1](media/02-work-order-scheduling.png)

<span data-ttu-id="acea6-132">U kunt ook *verantwoordelijke* onderhoudswerkers instellen; deze kunnen worden geselecteerd wanneer een onderhoudsverzoek of werkorder wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="acea6-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="acea6-133">U kunt de selectie in **Alle werkorders** en **Alle onderhoudsverzoeken** zo nodig bewerken.</span><span class="sxs-lookup"><span data-stu-id="acea6-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="acea6-134">Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="acea6-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="acea6-135">Tijdens de planning van werkorders worden verschillende scores berekend om te bepalen welke medewerkers de taken met betrekking tot een werkorder moeten voltooien (deze scores worden ingesteld via **Parameters voor activabeheer** > **Planning werkorder**).</span><span class="sxs-lookup"><span data-stu-id="acea6-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="acea6-136">Als twee of meer onderhoudsmedewerkers of verantwoordelijke onderhoudsmedewerkers dezelfde score krijgen tijdens de werkorderplanning, wordt een willekeurige medewerker geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="acea6-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="acea6-137">Anders is het altijd de medewerker met de hoogste score die wordt toegewezen om een werkorder te voltooien.</span><span class="sxs-lookup"><span data-stu-id="acea6-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
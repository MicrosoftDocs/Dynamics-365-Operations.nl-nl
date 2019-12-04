---
title: Kandidaatbronnen bijhouden in Attract
description: Dit onderwerp bevat informatie over het bijhouden van de bron voor kandidaatprofielen en -sollicitaties.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832643"
---
# <a name="track-candidate-sources-in-attract"></a><span data-ttu-id="aa421-103">Kandidaatbronnen bijhouden in Attract</span><span class="sxs-lookup"><span data-stu-id="aa421-103">Track candidate sources in Attract</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="aa421-104">Functionaliteit die in dit onderwerp wordt vermeld, is beschikbaar als onderdeel van een preview-versie.</span><span class="sxs-lookup"><span data-stu-id="aa421-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="aa421-105">De inhoud en de functies kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="aa421-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="aa421-106">Als u deze functie wilt gebruiken, vraagt u een beheerder om deze in te schakelen via de **Beheerinstellingen** in Attract.</span><span class="sxs-lookup"><span data-stu-id="aa421-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="aa421-107">Een toekomstige versie bevat rapporten voor het bijhouden van bronnen.</span><span class="sxs-lookup"><span data-stu-id="aa421-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="aa421-108">Zie voor meer informatie [Toegang tot voorbeeldfuncties in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="aa421-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="aa421-109">Als kandidaten solliciteren op een functie, wordt in Attract automatisch de bron van hun sollicitaties bijgehouden. Hierdoor kunt u beschikken over waardevolle informatie waarmee u uw inspanningen met betrekking tot personeelswerving beter kunt inzetten.</span><span class="sxs-lookup"><span data-stu-id="aa421-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="aa421-110">Wervers en aanstellende managers kunnen ook een sollicitatiebron selecteren tijdens het handmatig toevoegen van een kandidaat aan een functie of talentenpool.</span><span class="sxs-lookup"><span data-stu-id="aa421-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="aa421-111">U kunt de sollicitatiebron in de activiteitdetails van de sollicitatie bekijken op het tabblad **Activiteit**, alsmede in de sollicitatiehistorie die beschikbaar is onder **Profiel** in talentenpools.</span><span class="sxs-lookup"><span data-stu-id="aa421-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="aa421-112">U kunt de profielbron van een kandidaat vinden in de kandidaatdetails op het tabblad **Profiel** in zowel sollicitaties als talentenpools.</span><span class="sxs-lookup"><span data-stu-id="aa421-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="aa421-113">U kunt processjablonen vinden in de [Uitgebreide invoegtoepassing voor aanstellingen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="aa421-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="aa421-114">Vooraf geconfigureerde bronnen</span><span class="sxs-lookup"><span data-stu-id="aa421-114">Pre-configured sources</span></span>

<span data-ttu-id="aa421-115">De standaardlijst met bronnen bevat de meest voorkomende sollicitatiebronnen.</span><span class="sxs-lookup"><span data-stu-id="aa421-115">The default source list contains common application sources.</span></span> <span data-ttu-id="aa421-116">Sommige brontypen, zoals **Functiebord** en **Sociaal netwerk**, bevatten aanvullende brondetails.</span><span class="sxs-lookup"><span data-stu-id="aa421-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="aa421-117">Bijvoorbeeld: **Sociaal netwerk** bevat Facebook en Twitter.</span><span class="sxs-lookup"><span data-stu-id="aa421-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="aa421-118">Met het brontype **Verwijzing** kunt u een interne werknemer als verwijzing opgeven.</span><span class="sxs-lookup"><span data-stu-id="aa421-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="aa421-119">De standaardlijst met bronnen bron bevat de volgende vooraf geconfigureerde bronnen:</span><span class="sxs-lookup"><span data-stu-id="aa421-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="aa421-120">Attract-vacaturesite</span><span class="sxs-lookup"><span data-stu-id="aa421-120">Attract career site</span></span>

-   <span data-ttu-id="aa421-121">Bureau</span><span class="sxs-lookup"><span data-stu-id="aa421-121">Agency</span></span>

-   <span data-ttu-id="aa421-122">Vacaturebeurs</span><span class="sxs-lookup"><span data-stu-id="aa421-122">Career Fair</span></span>

-   <span data-ttu-id="aa421-123">Bedrijfsmarketing</span><span class="sxs-lookup"><span data-stu-id="aa421-123">Company Marketing</span></span>

-   <span data-ttu-id="aa421-124">Conferenties en beurzen</span><span class="sxs-lookup"><span data-stu-id="aa421-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="aa421-125">Beroepsvereniging</span><span class="sxs-lookup"><span data-stu-id="aa421-125">Professional Association</span></span>

-   <span data-ttu-id="aa421-126">Functiebord</span><span class="sxs-lookup"><span data-stu-id="aa421-126">Job board</span></span>

    -   <span data-ttu-id="aa421-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="aa421-127">Indeed</span></span>

    -   <span data-ttu-id="aa421-128">Seek</span><span class="sxs-lookup"><span data-stu-id="aa421-128">Seek</span></span>

    -   <span data-ttu-id="aa421-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="aa421-129">CareerBuilder</span></span>

    -   <span data-ttu-id="aa421-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="aa421-130">Google Jobs</span></span>

    -   <span data-ttu-id="aa421-131">Xing</span><span class="sxs-lookup"><span data-stu-id="aa421-131">Xing</span></span>

    -   <span data-ttu-id="aa421-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="aa421-132">Glassdoor</span></span>

    -   <span data-ttu-id="aa421-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="aa421-133">Monster Jobs</span></span>

-   <span data-ttu-id="aa421-134">Tijdschriften en publicaties</span><span class="sxs-lookup"><span data-stu-id="aa421-134">Magazines & Publications</span></span>

-   <span data-ttu-id="aa421-135">Sociaal netwerk</span><span class="sxs-lookup"><span data-stu-id="aa421-135">Social Network</span></span>

    -   <span data-ttu-id="aa421-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="aa421-136">Facebook</span></span>

    -   <span data-ttu-id="aa421-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="aa421-137">Twitter</span></span>

-   <span data-ttu-id="aa421-138">Werving op universiteiten</span><span class="sxs-lookup"><span data-stu-id="aa421-138">University Recruiting</span></span>

-   <span data-ttu-id="aa421-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="aa421-139">LinkedIn</span></span>

-   <span data-ttu-id="aa421-140">Advertenties</span><span class="sxs-lookup"><span data-stu-id="aa421-140">Classifieds</span></span>

-   <span data-ttu-id="aa421-141">Verwijzing</span><span class="sxs-lookup"><span data-stu-id="aa421-141">Referral</span></span>

-   <span data-ttu-id="aa421-142">Toegevoegd door werver</span><span class="sxs-lookup"><span data-stu-id="aa421-142">Added by Recruiter</span></span>

-   <span data-ttu-id="aa421-143">Overig</span><span class="sxs-lookup"><span data-stu-id="aa421-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="aa421-144">De lijst met bronnen aanpassen</span><span class="sxs-lookup"><span data-stu-id="aa421-144">Customize the source list</span></span> 

<span data-ttu-id="aa421-145">U kunt de lijst met bronnen aanpassen om aanvullende sollicitatiebronnen op te nemen.</span><span class="sxs-lookup"><span data-stu-id="aa421-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="aa421-146">Als u deze lijst wilt aanpassen, volgt u de instructies in [Optiesets uitbreiden in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="aa421-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="aa421-147">Bewerk de entiteit **TalentSource** om aanvullende bronnen op te nemen.</span><span class="sxs-lookup"><span data-stu-id="aa421-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="aa421-148">Als u een negatieve impact op de gebruikersinterface (UI) wilt voorkomen, moet u de **TalentCategory**-opsommingswaarden (geen namen) niet bewerken of verwijderen voor het volgende:</span><span class="sxs-lookup"><span data-stu-id="aa421-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="aa421-149">**Verwijzing**</span><span class="sxs-lookup"><span data-stu-id="aa421-149">**Referral**</span></span>
- <span data-ttu-id="aa421-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="aa421-150">**LinkedIn**</span></span>
- <span data-ttu-id="aa421-151">**Overig**</span><span class="sxs-lookup"><span data-stu-id="aa421-151">**Other**</span></span>

<span data-ttu-id="aa421-152">In plaats daarvan kunt u de **TalentSource**-opsomming uitbreiden om andere typen bronnen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="aa421-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>

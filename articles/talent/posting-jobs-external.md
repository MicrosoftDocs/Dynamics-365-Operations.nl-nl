---
title: Functies publiceren naar externe vacaturesites via Attract
description: In dit onderwerp wordt uitgelegd hoe u Dynamics 365 for Talent - Attract gebruikt voor het publiceren van functies naar externe wervingssites
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590477"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="42d29-103">Functies publiceren naar externe vacaturesites via Attract</span><span class="sxs-lookup"><span data-stu-id="42d29-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42d29-104">U wilt uw openstaande posities aan zoveel mogelijk kandidaten voorleggen.</span><span class="sxs-lookup"><span data-stu-id="42d29-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="42d29-105">Wervingssites, zoals Broadbean, helpen u bij het realiseren van dit doel.</span><span class="sxs-lookup"><span data-stu-id="42d29-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="42d29-106">Met Microsoft Dynamics 365 Talent: Attract kunt u nu functies publiceren naar Broadbean en Microsoft biedt voortdurend nieuwe aanbiedingen in dit gebied.</span><span class="sxs-lookup"><span data-stu-id="42d29-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="42d29-107">Functies naar Broadbean publiceren</span><span class="sxs-lookup"><span data-stu-id="42d29-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="42d29-108">Voordat u functies naar Broadbean kunt publiceren, moet u de Broadbean-integratie configureren.</span><span class="sxs-lookup"><span data-stu-id="42d29-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="42d29-109">Als u functies naar externe sites wilt publiceren, moet u over de [Uitgebreide invoegtoepassing voor aanstellingen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) beschikken.</span><span class="sxs-lookup"><span data-stu-id="42d29-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="42d29-110">Als u functies naar Broadbean wilt publiceren via Attract, moet u beschikken over een Broadbean-abonnement.</span><span class="sxs-lookup"><span data-stu-id="42d29-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="42d29-111">Van deze functie kan momenteel een voorbeeld worden bekeken.</span><span class="sxs-lookup"><span data-stu-id="42d29-111">This feature is currently in preview.</span></span> <span data-ttu-id="42d29-112">Als u de functie wilt proberen, moet u [deze inschakelen in de beheerinstellingen van Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="42d29-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="42d29-113">Broadbean-integratie configureren</span><span class="sxs-lookup"><span data-stu-id="42d29-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="42d29-114">Meld u aan bij Attract als beheerder.</span><span class="sxs-lookup"><span data-stu-id="42d29-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="42d29-115">Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek van de pagina en selecteer vervolgens **Beheercentrum**.</span><span class="sxs-lookup"><span data-stu-id="42d29-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="42d29-116">Schakel de integratie in op het tabblad **Functiebordinstellingen** in de sectie **Broadbean-integratie inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="42d29-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="42d29-117">Neem contact op met Broadbean en voer uw gegevens in **Gebruikersnaam, Client-ID, Coderingstoken** in.</span><span class="sxs-lookup"><span data-stu-id="42d29-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="42d29-118">Uw Broadbean-referenties zijn gevoelig en vertrouwelijk.</span><span class="sxs-lookup"><span data-stu-id="42d29-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="42d29-119">Bewaar deze daarom zorgvuldig en deel ze op verantwoorde wijze.</span><span class="sxs-lookup"><span data-stu-id="42d29-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="42d29-120">Iedereen met een beheerdersrol in Attract kan deze referenties weergeven.</span><span class="sxs-lookup"><span data-stu-id="42d29-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="42d29-121">Microsoft en Attract zijn niet betrokken bij het maken en onderhouden van deze waarden.</span><span class="sxs-lookup"><span data-stu-id="42d29-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="42d29-122">Het is uw verantwoordelijkheid ze om up-to-date te houden in Attract en te werken met Broadbean om eventuele problemen op te lossen die betrekking hebben op uw referenties.</span><span class="sxs-lookup"><span data-stu-id="42d29-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="42d29-123">Een functie naar Broadbean publiceren</span><span class="sxs-lookup"><span data-stu-id="42d29-123">Post a job to Broadbean</span></span>

<span data-ttu-id="42d29-124">Nadat Broadbean is ingeschakeld, kunnen wervers en beheerders er een functie naar publiceren.</span><span class="sxs-lookup"><span data-stu-id="42d29-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="42d29-125">U kunt een sollicitatie-URL voor de functie hebben.</span><span class="sxs-lookup"><span data-stu-id="42d29-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="42d29-126">Open in Attract de functie die u wilt publiceren naar Broadbean.</span><span class="sxs-lookup"><span data-stu-id="42d29-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="42d29-127">Selecteer in de sectie **Publicaties** de knop **Nu publiceren** die hoort bij Broadbean.</span><span class="sxs-lookup"><span data-stu-id="42d29-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="42d29-128">Volg de instructies in het Broadbean-venster.</span><span class="sxs-lookup"><span data-stu-id="42d29-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="42d29-129">Attract geeft de volgende gegevens door naar Broadbean:</span><span class="sxs-lookup"><span data-stu-id="42d29-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="42d29-130">Aanvraag-ID</span><span class="sxs-lookup"><span data-stu-id="42d29-130">Request ID</span></span>
- <span data-ttu-id="42d29-131">Functie</span><span class="sxs-lookup"><span data-stu-id="42d29-131">Job title</span></span>
- <span data-ttu-id="42d29-132">Taakomschrijving</span><span class="sxs-lookup"><span data-stu-id="42d29-132">Job description</span></span>
- <span data-ttu-id="42d29-133">Functielocatie</span><span class="sxs-lookup"><span data-stu-id="42d29-133">Job location</span></span>
- <span data-ttu-id="42d29-134">Sollicitatie-URL</span><span class="sxs-lookup"><span data-stu-id="42d29-134">Apply URL</span></span>
- <span data-ttu-id="42d29-135">Informatie van wervingsbureau</span><span class="sxs-lookup"><span data-stu-id="42d29-135">Recruiter information</span></span>

<span data-ttu-id="42d29-136">Nadat in Broadbean de publicatie is voltooid, wordt in de sectie **Publicaties** van de functie in Attract de Broadbean-status als **Gepubliceerd** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="42d29-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="42d29-137">Voor Broadbean is het veld **Bedrijfstak** vereist.</span><span class="sxs-lookup"><span data-stu-id="42d29-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="42d29-138">Momenteel is dit veld standaard ingesteld op **IT**.</span><span class="sxs-lookup"><span data-stu-id="42d29-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="42d29-139">U kunt de waarde echter wijzigen voor de juiste bedrijfstak in het venster voor Broadbean-functiepublicatie.</span><span class="sxs-lookup"><span data-stu-id="42d29-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="42d29-140">Het duurt enige tijd voordat Broadbean de publicatie van uw functie naar alle door u geselecteerde functieborden heeft voltooid.</span><span class="sxs-lookup"><span data-stu-id="42d29-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="42d29-141">Daarom kan er enige vertraging optreden voordat Attract een statusupdate voor de functie geeft.</span><span class="sxs-lookup"><span data-stu-id="42d29-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="42d29-142">Een Broadbean-functiepublicatie weergeven</span><span class="sxs-lookup"><span data-stu-id="42d29-142">View a Broadbean job posting</span></span>

<span data-ttu-id="42d29-143">Nadat u een functie naar Broadbean hebt gepubliceerd, kunt u deze weergeven via Attract.</span><span class="sxs-lookup"><span data-stu-id="42d29-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="42d29-144">Open in Attract de functie die u wilt weergeven in Broadbean.</span><span class="sxs-lookup"><span data-stu-id="42d29-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="42d29-145">Selecteer in de sectie **Publicaties** de ellipsknop (**...**) die hoort bij Broadbean en selecteer vervolgens **Weergave**.</span><span class="sxs-lookup"><span data-stu-id="42d29-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="42d29-146">De Broadbean-functiepublicatie wordt weergegeven in een nieuw venster.</span><span class="sxs-lookup"><span data-stu-id="42d29-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="42d29-147">Een Broadbean-functiepublicatie bijwerken</span><span class="sxs-lookup"><span data-stu-id="42d29-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="42d29-148">U kunt een Broadbean-functiepublicatie op twee manieren bijwerken.</span><span class="sxs-lookup"><span data-stu-id="42d29-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="42d29-149">Open in Attract de functie die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="42d29-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="42d29-150">Selecteer in de sectie **Publicaties** de knop **Publicatie bijwerken** die hoort bij Broadbean.</span><span class="sxs-lookup"><span data-stu-id="42d29-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="42d29-151">Bewerk de publicatie in het Broadbean-venster.</span><span class="sxs-lookup"><span data-stu-id="42d29-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="42d29-152">– of –</span><span class="sxs-lookup"><span data-stu-id="42d29-152">–or–</span></span>

1. <span data-ttu-id="42d29-153">Open in Attract de functie die u wilt weergeven in Broadbean.</span><span class="sxs-lookup"><span data-stu-id="42d29-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="42d29-154">Selecteer in de sectie **Publicaties** de ellipsknop (**...**) die hoort bij Broadbean en selecteer vervolgens **Weergave**.</span><span class="sxs-lookup"><span data-stu-id="42d29-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="42d29-155">Bewerk in het Broadbean-venster de functiedetails en publiceer de functie opnieuw.</span><span class="sxs-lookup"><span data-stu-id="42d29-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="42d29-156">De functiedetails in Attract worden niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="42d29-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="42d29-157">Een Broadbean-functiepublicatie verwijderen</span><span class="sxs-lookup"><span data-stu-id="42d29-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="42d29-158">U kunt desgewenst een functiepublicatie uit Broadbean verwijderen.</span><span class="sxs-lookup"><span data-stu-id="42d29-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="42d29-159">Open in Attract de functie die u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="42d29-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="42d29-160">Selecteer in de sectie **Publicaties** de ellipsknop (**...**) die hoort bij Broadbean en selecteer vervolgens **Publicatie verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="42d29-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="42d29-161">Na de functie uit Broadbean is verwijderd, bevat het Broadbean-item in Attract de knop **Nu publiceren**.</span><span class="sxs-lookup"><span data-stu-id="42d29-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="42d29-162">De aanwezigheid van deze knop geeft aan dat de functie is verwijderd en opnieuw kan worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="42d29-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="42d29-163">Problemen met Broadbean-integratie oplossen</span><span class="sxs-lookup"><span data-stu-id="42d29-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="42d29-164">Als u problemen hebt met het publiceren van een functie naar Broadbean, probeert u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="42d29-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="42d29-165">Controleer of de Broadbean-referenties die u hebt ingevoerd in Attract, geldig en juist zijn.</span><span class="sxs-lookup"><span data-stu-id="42d29-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="42d29-166">Als de referenties geldig en juist zijn, neemt u contact op met [Broadbean-ondersteuning](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="42d29-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="42d29-167">Als het probleem zich blijft voordoen, neemt u contact op met [Microsoft-ondersteuning](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="42d29-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

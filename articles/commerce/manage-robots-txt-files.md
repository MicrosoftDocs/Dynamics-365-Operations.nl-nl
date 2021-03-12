---
title: Robots.txt-bestanden beheren
description: In dit onderwerp wordt beschreven hoe u robots.txt-bestanden beheert in Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2e25a584121b700e566c29dbfe3fbbd72bf998cc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982536"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="18c11-103">Robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="18c11-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="18c11-104">In dit onderwerp wordt beschreven hoe u robots.txt-bestanden beheert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="18c11-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="18c11-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="18c11-105">Overview</span></span>

<span data-ttu-id="18c11-106">De uitsluitingsstandaard voor robots, of robots.txt, is een standaard die websites gebruiken om te communiceren met webrobots.</span><span class="sxs-lookup"><span data-stu-id="18c11-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="18c11-107">Hiermee worden webrobots geïnstrueerd over de gebieden van een website die niet bezocht mogen worden.</span><span class="sxs-lookup"><span data-stu-id="18c11-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="18c11-108">Robots worden vaak gebruikt door zoekmachines om websites te indexeren.</span><span class="sxs-lookup"><span data-stu-id="18c11-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="18c11-109">Als u robots wilt uitsluiten van een server, maakt u een bestand op de server.</span><span class="sxs-lookup"><span data-stu-id="18c11-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="18c11-110">In dit bestand geeft u een toegangsbeleid voor robots op.</span><span class="sxs-lookup"><span data-stu-id="18c11-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="18c11-111">Het bestand moet toegankelijk zijn via HTTP op de lokale URL **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="18c11-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="18c11-112">Met het robots.txt-bestand kunnen zoekmachines de inhoud op uw site indexeren.</span><span class="sxs-lookup"><span data-stu-id="18c11-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="18c11-113">Met Dynamics 365 Commerce kunt u een robots.txt-bestand voor uw domein uploaden.</span><span class="sxs-lookup"><span data-stu-id="18c11-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="18c11-114">Voor elk domein in uw Commerce-omgeving kunt u één robots.txt-bestand uploaden en aan dat domein koppelen.</span><span class="sxs-lookup"><span data-stu-id="18c11-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="18c11-115">Ga voor meer informatie over het robots.txt-bestand naar de [pagina's voor webrobots](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="18c11-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="18c11-116">Een robots.txt-bestand uploaden</span><span class="sxs-lookup"><span data-stu-id="18c11-116">Upload a robots.txt file</span></span>

<span data-ttu-id="18c11-117">Nadat u uw robots.txt-bestand hebt gemaakt en bewerkt volgens de [standaard voor robotuitsluiting](https://www.robotstxt.org/orig.html), moet u ervoor zorgen dat het bestand toegankelijk is op de computer waarop u de Commerce-ontwerpfunctie gaat gebruiken.</span><span class="sxs-lookup"><span data-stu-id="18c11-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="18c11-118">Het bestand moet de naam **robots.txt** hebben.</span><span class="sxs-lookup"><span data-stu-id="18c11-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="18c11-119">Voor de beste resultaten moet deze in indeling hebben die wordt vermeld in de standaard.</span><span class="sxs-lookup"><span data-stu-id="18c11-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="18c11-120">Elke Commerce-klant is verantwoordelijk voor het valideren en onderhouden van de inhoud van zijn of haar eigen robots.txt-bestand.</span><span class="sxs-lookup"><span data-stu-id="18c11-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="18c11-121">Als u een robots.txt-bestand wilt uploaden, moet u bij Commerce zijn aangemeld als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="18c11-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="18c11-122">Volg deze stappen om een robots.txt-bestand te uploaden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="18c11-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="18c11-123">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="18c11-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="18c11-124">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="18c11-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="18c11-125">Selecteer **Robots.txt** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="18c11-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="18c11-126">In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="18c11-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="18c11-127">Selecteer **Beheren** om een robots.txt-bestand te uploaden voor een domein in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="18c11-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="18c11-128">Selecteer in het menu aan de rechterkant de knop **Uploaden** (de omhoog wijzende pijl) naast het domein dat aan het robots.txt-bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="18c11-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="18c11-129">Er verschijnt een dialoogvenster waarin u naar het bestand kunt bladeren.</span><span class="sxs-lookup"><span data-stu-id="18c11-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="18c11-130">Selecteer in dit dialoogvenster het robots.txt-bestand dat u wilt uploaden voor het gekoppelde domein en selecteer vervolgens **Openen** om het uploaden te voltooien.</span><span class="sxs-lookup"><span data-stu-id="18c11-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="18c11-131">Tijdens het uploaden wordt geverifieerd of het bestand een tekstbestand is, maar de inhoud van het bestand wordt niet gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="18c11-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="18c11-132">Een robots.txt-bestand downloaden</span><span class="sxs-lookup"><span data-stu-id="18c11-132">Download a robots.txt file</span></span>

<span data-ttu-id="18c11-133">Volg deze stappen om een robots.txt-bestand te downloaden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="18c11-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="18c11-134">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="18c11-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="18c11-135">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="18c11-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="18c11-136">Selecteer **Robots.txt** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="18c11-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="18c11-137">In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="18c11-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="18c11-138">Selecteer **Beheren** om een robots.txt-bestand te downloaden voor een domein in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="18c11-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="18c11-139">Selecteer in het menu aan de rechterkant de knop **Downloaden** (de omlaag wijzende pijl) naast het domein dat aan het robots.txt-bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="18c11-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="18c11-140">Er verschijnt een dialoogvenster waarin u naar het bestand kunt bladeren.</span><span class="sxs-lookup"><span data-stu-id="18c11-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="18c11-141">Ga in het dialoogvenster naar de gewenste locatie op uw lokale station, bevestig of voer een bestandsnaam in en selecteer vervolgens **Opslaan** om de download te voltooien.</span><span class="sxs-lookup"><span data-stu-id="18c11-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="18c11-142">Deze procedure kan alleen worden gebruikt om robots.txt-bestanden te downloaden die eerder zijn geüpload via de Commerce-ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="18c11-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="18c11-143">Een robots.txt-bestand verwijderen</span><span class="sxs-lookup"><span data-stu-id="18c11-143">Delete a robots.txt file</span></span>

<span data-ttu-id="18c11-144">Volg deze stappen om een robots.txt-bestand te verwijderen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="18c11-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="18c11-145">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="18c11-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="18c11-146">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="18c11-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="18c11-147">Selecteer **Robots.txt** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="18c11-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="18c11-148">In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="18c11-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="18c11-149">Selecteer **Beheren** om een robots.txt-bestand te verwijderen voor een domein in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="18c11-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="18c11-150">Selecteer in het menu aan de rechterkant de knop **Verwijderen** (de prullenbak) naast het domein dat aan het robots.txt-bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="18c11-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="18c11-151">Er verschijnt een venster waarin u naar het bestand kunt bladeren.</span><span class="sxs-lookup"><span data-stu-id="18c11-151">A file browser window appears.</span></span>
6. <span data-ttu-id="18c11-152">Selecteer in dit venster het robots.txt-bestand dat u wilt verwijderen voor het gekoppelde domein en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="18c11-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="18c11-153">Er verschijnt een waarschuwingsvenster.</span><span class="sxs-lookup"><span data-stu-id="18c11-153">A warning message box appears.</span></span>
7. <span data-ttu-id="18c11-154">Selecteer in dit berichtvak de optie **Verwijderen** om de verwijdering van het robots.txt-bestand te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="18c11-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="18c11-155">Deze procedure kan alleen worden gebruikt om robots.txt-bestanden te verwijderen die eerder zijn geüpload via de Commerce-ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="18c11-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18c11-156">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="18c11-156">Additional resources</span></span>

[<span data-ttu-id="18c11-157">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="18c11-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="18c11-158">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="18c11-158">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="18c11-159">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="18c11-159">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="18c11-160">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="18c11-160">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="18c11-161">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="18c11-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="18c11-162">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="18c11-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="18c11-163">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="18c11-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="18c11-164">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="18c11-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="18c11-165">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="18c11-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="18c11-166">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="18c11-166">Enable location-based store detection</span></span>](enable-store-detection.md)

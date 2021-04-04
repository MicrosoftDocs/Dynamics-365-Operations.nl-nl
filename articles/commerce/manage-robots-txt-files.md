---
title: robots.txt-bestanden beheren
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
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477703"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="636ae-103">robots.txt-bestanden beheren</span><span class="sxs-lookup"><span data-stu-id="636ae-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="636ae-104">In dit onderwerp wordt beschreven hoe u robots.txt-bestanden beheert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="636ae-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="636ae-105">De uitsluitingsstandaard voor robots, of robots.txt, is een standaard die websites gebruiken om te communiceren met webrobots.</span><span class="sxs-lookup"><span data-stu-id="636ae-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="636ae-106">Hiermee worden webrobots geïnstrueerd over de gebieden van een website die niet bezocht mogen worden.</span><span class="sxs-lookup"><span data-stu-id="636ae-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="636ae-107">Robots worden vaak gebruikt door zoekmachines om websites te indexeren.</span><span class="sxs-lookup"><span data-stu-id="636ae-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="636ae-108">Als u robots wilt uitsluiten van een server, maakt u een bestand op de server.</span><span class="sxs-lookup"><span data-stu-id="636ae-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="636ae-109">In dit bestand geeft u een toegangsbeleid voor robots op.</span><span class="sxs-lookup"><span data-stu-id="636ae-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="636ae-110">Het bestand moet toegankelijk zijn via HTTP op de lokale URL **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="636ae-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="636ae-111">Met het robots.txt-bestand kunnen zoekmachines de inhoud op uw site indexeren.</span><span class="sxs-lookup"><span data-stu-id="636ae-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="636ae-112">Met Dynamics 365 Commerce kunt u een robots.txt-bestand voor uw domein uploaden.</span><span class="sxs-lookup"><span data-stu-id="636ae-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="636ae-113">Voor elk domein in uw Commerce-omgeving kunt u één robots.txt-bestand uploaden en aan dat domein koppelen.</span><span class="sxs-lookup"><span data-stu-id="636ae-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="636ae-114">Ga voor meer informatie over het robots.txt-bestand naar de [pagina's voor webrobots](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="636ae-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="636ae-115">Een robots.txt-bestand uploaden</span><span class="sxs-lookup"><span data-stu-id="636ae-115">Upload a robots.txt file</span></span>

<span data-ttu-id="636ae-116">Nadat u uw robots.txt-bestand hebt gemaakt en bewerkt volgens de [standaard voor robotuitsluiting](https://www.robotstxt.org/orig.html), moet u ervoor zorgen dat het bestand toegankelijk is op de computer waarop u de Commerce-ontwerpfunctie gaat gebruiken.</span><span class="sxs-lookup"><span data-stu-id="636ae-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="636ae-117">Het bestand moet de naam **robots.txt** hebben.</span><span class="sxs-lookup"><span data-stu-id="636ae-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="636ae-118">Voor de beste resultaten moet deze in indeling hebben die wordt vermeld in de standaard.</span><span class="sxs-lookup"><span data-stu-id="636ae-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="636ae-119">Elke Commerce-klant is verantwoordelijk voor het valideren en onderhouden van de inhoud van zijn of haar eigen robots.txt-bestand.</span><span class="sxs-lookup"><span data-stu-id="636ae-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="636ae-120">Als u een robots.txt-bestand wilt uploaden, moet u bij Commerce zijn aangemeld als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="636ae-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="636ae-121">Volg deze stappen om een robots.txt-bestand te uploaden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="636ae-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="636ae-122">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="636ae-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="636ae-123">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="636ae-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="636ae-124">Selecteer **Robots.txt** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="636ae-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="636ae-125">In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="636ae-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="636ae-126">Selecteer **Beheren** om een robots.txt-bestand te uploaden voor een domein in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="636ae-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="636ae-127">Selecteer in het menu aan de rechterkant de knop **Uploaden** (de omhoog wijzende pijl) naast het domein dat aan het robots.txt-bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="636ae-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="636ae-128">Er verschijnt een dialoogvenster waarin u naar het bestand kunt bladeren.</span><span class="sxs-lookup"><span data-stu-id="636ae-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="636ae-129">Selecteer in dit dialoogvenster het robots.txt-bestand dat u wilt uploaden voor het gekoppelde domein en selecteer vervolgens **Openen** om het uploaden te voltooien.</span><span class="sxs-lookup"><span data-stu-id="636ae-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="636ae-130">Tijdens het uploaden wordt geverifieerd of het bestand een tekstbestand is, maar de inhoud van het bestand wordt niet gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="636ae-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="636ae-131">Een robots.txt-bestand downloaden</span><span class="sxs-lookup"><span data-stu-id="636ae-131">Download a robots.txt file</span></span>

<span data-ttu-id="636ae-132">Volg deze stappen om een robots.txt-bestand te downloaden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="636ae-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="636ae-133">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="636ae-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="636ae-134">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="636ae-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="636ae-135">Selecteer **Robots.txt** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="636ae-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="636ae-136">In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="636ae-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="636ae-137">Selecteer **Beheren** om een robots.txt-bestand te downloaden voor een domein in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="636ae-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="636ae-138">Selecteer in het menu aan de rechterkant de knop **Downloaden** (de omlaag wijzende pijl) naast het domein dat aan het robots.txt-bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="636ae-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="636ae-139">Er verschijnt een dialoogvenster waarin u naar het bestand kunt bladeren.</span><span class="sxs-lookup"><span data-stu-id="636ae-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="636ae-140">Ga in het dialoogvenster naar de gewenste locatie op uw lokale station, bevestig of voer een bestandsnaam in en selecteer vervolgens **Opslaan** om de download te voltooien.</span><span class="sxs-lookup"><span data-stu-id="636ae-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="636ae-141">Deze procedure kan alleen worden gebruikt om robots.txt-bestanden te downloaden die eerder zijn geüpload via de Commerce-ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="636ae-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="636ae-142">Een robots.txt-bestand verwijderen</span><span class="sxs-lookup"><span data-stu-id="636ae-142">Delete a robots.txt file</span></span>

<span data-ttu-id="636ae-143">Volg deze stappen om een robots.txt-bestand te verwijderen in Commerce.</span><span class="sxs-lookup"><span data-stu-id="636ae-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="636ae-144">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="636ae-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="636ae-145">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="636ae-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="636ae-146">Selecteer **Robots.txt** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="636ae-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="636ae-147">In het hoofdgedeelte van het venster wordt een lijst weergegeven met alle domeinen die aan uw omgeving zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="636ae-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="636ae-148">Selecteer **Beheren** om een robots.txt-bestand te verwijderen voor een domein in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="636ae-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="636ae-149">Selecteer in het menu aan de rechterkant de knop **Verwijderen** (de prullenbak) naast het domein dat aan het robots.txt-bestand is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="636ae-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="636ae-150">Er verschijnt een venster waarin u naar het bestand kunt bladeren.</span><span class="sxs-lookup"><span data-stu-id="636ae-150">A file browser window appears.</span></span>
6. <span data-ttu-id="636ae-151">Selecteer in dit venster het robots.txt-bestand dat u wilt verwijderen voor het gekoppelde domein en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="636ae-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="636ae-152">Er verschijnt een waarschuwingsvenster.</span><span class="sxs-lookup"><span data-stu-id="636ae-152">A warning message box appears.</span></span>
7. <span data-ttu-id="636ae-153">Selecteer in dit berichtvak de optie **Verwijderen** om de verwijdering van het robots.txt-bestand te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="636ae-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="636ae-154">Deze procedure kan alleen worden gebruikt om robots.txt-bestanden te verwijderen die eerder zijn geüpload via de Commerce-ontwerpfunctie.</span><span class="sxs-lookup"><span data-stu-id="636ae-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="636ae-155">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="636ae-155">Additional resources</span></span>

[<span data-ttu-id="636ae-156">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="636ae-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="636ae-157">Een nieuwe e-commerce-tenant implementeren</span><span class="sxs-lookup"><span data-stu-id="636ae-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="636ae-158">Een e-commerce-site maken</span><span class="sxs-lookup"><span data-stu-id="636ae-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="636ae-159">Een Dynamics 365 Commerce-site koppelen aan een online kanaal</span><span class="sxs-lookup"><span data-stu-id="636ae-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="636ae-160">URL-omleidingen in bulk uploaden</span><span class="sxs-lookup"><span data-stu-id="636ae-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="636ae-161">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="636ae-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="636ae-162">Aangepaste pagina's voor gebruikersaanmeldingen instellen</span><span class="sxs-lookup"><span data-stu-id="636ae-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="636ae-163">Meerdere B2C-tenants configureren in een Commerce-omgeving</span><span class="sxs-lookup"><span data-stu-id="636ae-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="636ae-164">Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen</span><span class="sxs-lookup"><span data-stu-id="636ae-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="636ae-165">Detectie van winkels op basis van de locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="636ae-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

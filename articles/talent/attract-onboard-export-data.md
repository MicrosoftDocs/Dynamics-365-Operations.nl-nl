---
title: Gegevens exporteren uit Attract en Onboard
description: Exporteer gegevens uit Dynamics 365 Talent Attract en Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975929"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="582e7-103">Gegevens exporteren uit Attract en Onboard</span><span class="sxs-lookup"><span data-stu-id="582e7-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="582e7-104">Zoals is aangekondigd in [Het buiten gebruik stellen van Dynamics 365 Talent: Attract- en Dynamics 365 Talent: Onboard-apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), stellen we Dynamics 365 Talent: Attract en Dynamics 365 Talent: Onboard buiten gebruik op 1 februari 2022.</span><span class="sxs-lookup"><span data-stu-id="582e7-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="582e7-105">Om u te helpen bij de migratie naar een ander product, bieden beide apps nu mogelijkheden voor gegevensexport.</span><span class="sxs-lookup"><span data-stu-id="582e7-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="582e7-106">Gegevens exporteren vanuit Attract</span><span class="sxs-lookup"><span data-stu-id="582e7-106">Export data from Attract</span></span>

<span data-ttu-id="582e7-107">U kunt uw gegevens exporteren zonder de toegang tot uw omgeving te beperken.</span><span class="sxs-lookup"><span data-stu-id="582e7-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="582e7-108">U kunt dit bijvoorbeeld doen voor testdoeleinden of om inzicht te krijgen in onze gegevensstructuur.</span><span class="sxs-lookup"><span data-stu-id="582e7-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="582e7-109">Wanneer u klaar bent om te migreren, beperkt u de toegang tot uw Attract-omgeving met behulp van de instructies na deze procedure.</span><span class="sxs-lookup"><span data-stu-id="582e7-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="582e7-110">Zorg dat u de gegevens opnieuw exporteert.</span><span class="sxs-lookup"><span data-stu-id="582e7-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="582e7-111">Ga naar [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="582e7-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="582e7-112">Selecteer onder **Gegevensexport** de optie **Een gegevensexport aanvragen**.</span><span class="sxs-lookup"><span data-stu-id="582e7-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="582e7-113">Een gegevensexport aanvragen vanuit Attract</span><span class="sxs-lookup"><span data-stu-id="582e7-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="582e7-114">Wanneer het berichtvenster **De aanvraag wordt verwerkt** wordt weergegeven, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="582e7-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="582e7-115">De gegevensexport kan 20 minuten in beslag nemen, afhankelijk van de grootte van de export.</span><span class="sxs-lookup"><span data-stu-id="582e7-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="582e7-116">Wanneer de export is voltooid, selecteert u de knop **Downloaden** ernaast.</span><span class="sxs-lookup"><span data-stu-id="582e7-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="582e7-117">Alle gegevensexports zijn zeven dagen beschikbaar. Daarna vervalt de **Download**-koppeling.</span><span class="sxs-lookup"><span data-stu-id="582e7-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="582e7-118">De download bevat een ZIP-bestand met uw Attract-gegevens, waaronder de volgende mappen:</span><span class="sxs-lookup"><span data-stu-id="582e7-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="582e7-119">Mapnaam</span><span class="sxs-lookup"><span data-stu-id="582e7-119">Folder name</span></span> | <span data-ttu-id="582e7-120">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="582e7-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="582e7-121">Beheerinstellingen</span><span class="sxs-lookup"><span data-stu-id="582e7-121">Admin settings</span></span> | <span data-ttu-id="582e7-122">Configuraties van het Attract-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="582e7-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="582e7-123">Kandidaten</span><span class="sxs-lookup"><span data-stu-id="582e7-123">Candidates</span></span> | <span data-ttu-id="582e7-124">Alle kandidaten die aan banen of talentgroepen zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="582e7-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="582e7-125">E-mailsjablonen</span><span class="sxs-lookup"><span data-stu-id="582e7-125">Email templates</span></span> | <span data-ttu-id="582e7-126">Alle e-mailsjablonen die voor de omgeving zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="582e7-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="582e7-127">Sjablonen voor baanaanbiedingspakketten</span><span class="sxs-lookup"><span data-stu-id="582e7-127">Job offer package templates</span></span> | <span data-ttu-id="582e7-128">Alle sjablonen voor baanaanbiedingen die zijn gemaakt, plus de bijbehorende configuraties.</span><span class="sxs-lookup"><span data-stu-id="582e7-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="582e7-129">Regelsets voor baanaanbiedingen</span><span class="sxs-lookup"><span data-stu-id="582e7-129">Job offer rule sets</span></span> |  <span data-ttu-id="582e7-130">Alle regelsetbestanden die zijn geüpload voor aanbiedingsbeheer.</span><span class="sxs-lookup"><span data-stu-id="582e7-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="582e7-131">Sjablonen voor baanaanbiedingen</span><span class="sxs-lookup"><span data-stu-id="582e7-131">Job offer templates</span></span> | <span data-ttu-id="582e7-132">Alle sjablonen voor baanaanbiedingsdocumenten die voor de omgeving zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="582e7-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="582e7-133">Vacatures</span><span class="sxs-lookup"><span data-stu-id="582e7-133">Job openings</span></span> | <span data-ttu-id="582e7-134">Alle aangemaakte banen.</span><span class="sxs-lookup"><span data-stu-id="582e7-134">All created jobs.</span></span> <span data-ttu-id="582e7-135">Verwijderde banen worden niet geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="582e7-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="582e7-136">De submappen bevatten sollicitaties van kandidaten, met submappen voor bijlagen van sollicitaties en aanbiedingspakketten, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="582e7-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="582e7-137">Vacaturesjablonen</span><span class="sxs-lookup"><span data-stu-id="582e7-137">Job opening templates</span></span> | <span data-ttu-id="582e7-138">Baanverwerkingssjablonen die in de omgeving zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="582e7-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="582e7-139">Talentenpools</span><span class="sxs-lookup"><span data-stu-id="582e7-139">Talent pools</span></span> | <span data-ttu-id="582e7-140">Alle gemaakte talentgroepen, lijsten van hun deelnemers en de kandidatenlijsten voor de talentgroepen.</span><span class="sxs-lookup"><span data-stu-id="582e7-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="582e7-141">Medewerkers</span><span class="sxs-lookup"><span data-stu-id="582e7-141">Workers</span></span> | <span data-ttu-id="582e7-142">Lijst van alle medewerkers in de omgeving, plus hun rollen.</span><span class="sxs-lookup"><span data-stu-id="582e7-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="582e7-143">(basismap)</span><span class="sxs-lookup"><span data-stu-id="582e7-143">(root folder)</span></span> | <span data-ttu-id="582e7-144">Een JSON-schemabestand waarin de gegevensstructuurvelden worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="582e7-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="582e7-145">Toegang tot Attract beperken</span><span class="sxs-lookup"><span data-stu-id="582e7-145">Restrict access to Attract</span></span>

<span data-ttu-id="582e7-146">Wanneer u klaar bent om te migreren, beperkt u de toegang van niet-beheerders tot de Attract-omgeving en exporteert u uw gegevens.</span><span class="sxs-lookup"><span data-stu-id="582e7-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="582e7-147">Het beperken van de toegang tot de Attract-omgeving is permanent en kan niet ongedaan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="582e7-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="582e7-148">Sla deze stap over als u wilt dat niet-beheerders de toegang tot uw omgeving behouden.</span><span class="sxs-lookup"><span data-stu-id="582e7-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="582e7-149">Ga naar [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="582e7-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="582e7-150">Om de toegang van niet-beheerders tot de Attract-omgeving te beperken, selecteert u onder **Toegang tot deze app beperken** de optie **Toegang nu beperken**.</span><span class="sxs-lookup"><span data-stu-id="582e7-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="582e7-151">Door de toegang te beperken, wordt ook de publicatie van gepubliceerde actieve banen opgeheven.</span><span class="sxs-lookup"><span data-stu-id="582e7-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="582e7-152">Toegang van niet-beheerders tot Attract beperken</span><span class="sxs-lookup"><span data-stu-id="582e7-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="582e7-153">Wanneer u de waarschuwing **Dit is een permanente wijziging** ziet, selecteert u **Toegang beperken** om de toegang van gebruikers die geen beheerder zijn permanent te beperken vanuit deze omgeving.</span><span class="sxs-lookup"><span data-stu-id="582e7-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="582e7-154">Als u deze stap nog niet wilt uitvoeren, selecteert u **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="582e7-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="582e7-155">Waarschuwing dat het beperken van de toegang een permanente wijziging is</span><span class="sxs-lookup"><span data-stu-id="582e7-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="582e7-156">Beheerders blijven toegang houden tot de gegevensexport- en persoonlijke rapportpagina's wanneer u de toegang tot de Attract-omgeving hebt beperkt.</span><span class="sxs-lookup"><span data-stu-id="582e7-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="582e7-157">Gegevens exporteren vanuit Onboard</span><span class="sxs-lookup"><span data-stu-id="582e7-157">Export data from Onboard</span></span>

<span data-ttu-id="582e7-158">Wanneer u klaar bent, kunt u sjablonen, gidsen en kandidaatgegevens downloaden van Onboard.</span><span class="sxs-lookup"><span data-stu-id="582e7-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="582e7-159">Ga naar [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="582e7-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="582e7-160">Selecteer onder **Gegevensexport** de optie **Een gegevensexport aanvragen**.</span><span class="sxs-lookup"><span data-stu-id="582e7-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="582e7-161">Een gegevensexport aanvragen vanuit Onboard</span><span class="sxs-lookup"><span data-stu-id="582e7-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="582e7-162">Wanneer het berichtvenster **De aanvraag wordt verwerkt** wordt weergegeven, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="582e7-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="582e7-163">De gegevensexport kan 20 minuten in beslag nemen, afhankelijk van de grootte van de export.</span><span class="sxs-lookup"><span data-stu-id="582e7-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="582e7-164">Wanneer de export is voltooid, selecteert u de knop **Downloaden** ernaast.</span><span class="sxs-lookup"><span data-stu-id="582e7-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="582e7-165">Gegevensexport downloaden van Onboard</span><span class="sxs-lookup"><span data-stu-id="582e7-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="582e7-166">Uw gegevensexport is zeven dagen beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="582e7-166">Your data export is available for seven days.</span></span> <span data-ttu-id="582e7-167">Na zeven dagen vervalt de **Download**koppeling en moet u een nieuwe exportaanvraag indienen als u de gegevens opnieuw moet downloaden.</span><span class="sxs-lookup"><span data-stu-id="582e7-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="582e7-168">Wanneer u een nieuwe gegevensexport start, vervallen eventuele bestaande downloads wanneer de nieuwe export is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="582e7-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="582e7-169">De download is een ZIP-bestand dat het volgende bevat:</span><span class="sxs-lookup"><span data-stu-id="582e7-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="582e7-170">Een map **Sjablonen** die uw Onboard-sjablonen in de Word-documentindeling bevat.</span><span class="sxs-lookup"><span data-stu-id="582e7-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="582e7-171">Een map **Gidsen** die uw Onboard-gidsen in de Word-documentindeling bevat.</span><span class="sxs-lookup"><span data-stu-id="582e7-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="582e7-172">Zie ook</span><span class="sxs-lookup"><span data-stu-id="582e7-172">See also</span></span>

[<span data-ttu-id="582e7-173">Dynamics 365 Talent: Attract- en Dynamics 365 Talent: Onboard-apps buiten gebruik stellen</span><span class="sxs-lookup"><span data-stu-id="582e7-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
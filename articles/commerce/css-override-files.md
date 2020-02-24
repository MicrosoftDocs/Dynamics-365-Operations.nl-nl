---
title: Werken met CSS-overschrijvingsbestanden
description: In dit onderwerp wordt beschreven waarom, wanneer en hoe u CSS-overschrijvingsbestanden (Cascading Style Sheets) gebruikt in Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3c40145ea76296c1b8df9284af820534e3c869d4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001847"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="e460e-103">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="e460e-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e460e-104">In dit onderwerp wordt beschreven waarom, wanneer en hoe u CSS-overschrijvingsbestanden (Cascading Style Sheets) gebruikt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e460e-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e460e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="e460e-105">Overview</span></span>

<span data-ttu-id="e460e-106">Permanente sitestijlen moeten doorgaans worden afgehandeld via het thema van een site.</span><span class="sxs-lookup"><span data-stu-id="e460e-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="e460e-107">Thema's bieden de fundamentele CSS- en stijlinstellingen voor de modules op elke pagina van uw site.</span><span class="sxs-lookup"><span data-stu-id="e460e-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="e460e-108">Thema's worden gemaakt met behulp van de Dynamics 365 Commerce-SDK en ze worden geïmplementeerd op uw websites via Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e460e-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e460e-109">Met mogelijkheden voor het opsporen van themafouten en module-interfaceconfiguraties in de SDK kunnen site-ontwikkelaar aanpasbare en samenhangende site-ontwerppakketten maken.</span><span class="sxs-lookup"><span data-stu-id="e460e-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="e460e-110">Wanneer deze ontwerppakketten worden geïmplementeerd op een site, kunnen site-auteurs zich concentreren op het maken, bewerken en publiceren van inhoud in plaats van op siteontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="e460e-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="e460e-111">Gezien de gebruikelijke levenscyclus van een thema kan de afhankelijkheid van ontwikkelaars om stijlwijzigingen door te voeren via de SDK en de LCS-implementatiepijplijn in sommige scenario's belemmerend zijn.</span><span class="sxs-lookup"><span data-stu-id="e460e-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="e460e-112">Prototypen of hotfixes voor de site kunnen omslachtig lijken als de SDK niet is geconfigureerd of als u geen tijd hebt om te wachten op een LCS-implementatie.</span><span class="sxs-lookup"><span data-stu-id="e460e-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="e460e-113">In deze scenario's kunnen CSS-overschrijvingsbestanden uitkomst bieden.</span><span class="sxs-lookup"><span data-stu-id="e460e-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="e460e-114">In de Commerce-ontwerpprogramma's kunnen geverifieerde gebruikers een CSS-bestand uploaden en vervolgens activeren om het thema van een site te negeren.</span><span class="sxs-lookup"><span data-stu-id="e460e-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="e460e-115">De overhead van SDK- of LCS-implementatie is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="e460e-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="e460e-116">De overschrijvingen die in een CSS-overschrijvingsbestand zijn opgegeven, kunnen zo klein zijn als één tekststijlwijziging of zo verstrekkend als een volledige merkrevisie zijn.</span><span class="sxs-lookup"><span data-stu-id="e460e-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="e460e-117">Houd rekening met de volgende beperkingen voordat u CSS-overschrijvingsbestanden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="e460e-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="e460e-118">Er kan altijd slechts één CSS-overschrijvingsbestand tegelijk actief zijn op een site.</span><span class="sxs-lookup"><span data-stu-id="e460e-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="e460e-119">Daarom moeten alle actieve overschrijvingen aanwezig zijn in één overschrijvingsbestand.</span><span class="sxs-lookup"><span data-stu-id="e460e-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="e460e-120">Hoewel u de overschrijvingen in de Commerce-ontwerpprogramma's kunt bekijken, zijn er geen speciale foutopsporingsfuncties om fouten te identificeren die door de overschrijvingen worden geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="e460e-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="e460e-121">Met andere woorden, wanneer u CSS-overschrijvingsbestanden gebruikt, hebt u niet dezelfde toolset die de SDK biedt voor module- en ontwerpvalidatie.</span><span class="sxs-lookup"><span data-stu-id="e460e-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="e460e-122">Desondanks bieden CSS-overschrijvingsbestanden een snelle manier om een ontwerpprototype te maken of een hotfix te implementeren voordat een volledige thema-update wordt ontwikkeld en geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="e460e-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="e460e-123">Een CSS-overschrijvingsbestand maken</span><span class="sxs-lookup"><span data-stu-id="e460e-123">Create a CSS override file</span></span>

<span data-ttu-id="e460e-124">Als u een CSS-overschrijvingsbestand wilt maken, kunt u een IDE- (Integrated Development Environment), tekst of broncode-editor gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e460e-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="e460e-125">U kunt standaard foutopsporingsprogramma's in uw browser gebruiken om stijlselecties, eigenschappen en waarden op uw bestaande site te identificeren.</span><span class="sxs-lookup"><span data-stu-id="e460e-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="e460e-126">In de meeste browsers kunt u waarden wijzigen en deze wijzigingen bekijken in het foutopsporingsprogramma.</span><span class="sxs-lookup"><span data-stu-id="e460e-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="e460e-127">Nadat u de wijzigingen hebt geïdentificeerd die u wilt aanbrengen, kunt u deze opslaan in uw eigen CSS-bestand.</span><span class="sxs-lookup"><span data-stu-id="e460e-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="e460e-128">Een CSS-overschrijvingsbestand uploaden</span><span class="sxs-lookup"><span data-stu-id="e460e-128">Upload a CSS override file</span></span>

<span data-ttu-id="e460e-129">Volg deze stappen om een CSS-bestand naar uw site te uploaden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="e460e-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e460e-130">Ga in de ontwerpfuncties naar uw site.</span><span class="sxs-lookup"><span data-stu-id="e460e-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="e460e-131">Selecteer **Ontwerp** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="e460e-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e460e-132">Afhankelijk van de versie van de Commerce-ontwerpprogramma's die u gebruikt, moet u mogelijk **Instellingen** in het navigatievenster uitvouwen voordat u **Ontwerp** kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="e460e-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="e460e-133">Selecteer boven in het hoofdontwerpvenster het tabblad **CSS-overschrijving** als dit nog niet is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e460e-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="e460e-134">Onder **Beschikbare CSS-overschrijvingen** de optie **CSS-bestand uploaden**.</span><span class="sxs-lookup"><span data-stu-id="e460e-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="e460e-135">Verkenner wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="e460e-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="e460e-136">Blader in Verkenner naar en selecteer een CSS-bestand en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="e460e-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="e460e-137">Het geüploade CSS-bestand wordt nu weergegeven onder **Beschikbare CSS-overschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="e460e-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="e460e-138">Een CSS-overschrijvingsbestand bekijken</span><span class="sxs-lookup"><span data-stu-id="e460e-138">Preview a CSS override file</span></span>

<span data-ttu-id="e460e-139">Als u een CSS-overschrijvingsbestand wilt bekijken voordat u het actief maakt op uw live site, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="e460e-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="e460e-140">Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand waarvan u een voorbeeld wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="e460e-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="e460e-141">Selecteer naast de CSS-bestandsnaam de optie **Site bekijken**.</span><span class="sxs-lookup"><span data-stu-id="e460e-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="e460e-142">Selecteer in het dialoogvenster **Een URL selecteren** de URL van de site waarvoor u de toegepaste overschrijving wilt bekijken en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e460e-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="e460e-143">Als er meerdere varianten zijn voor de geselecteerde URL, selecteert u de gewenste variant in het dialoogvenster **Variaties bekijken** dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e460e-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="e460e-144">Er wordt een nieuw browsertabblad of -venster geopend waarin u uw stijloverschrijvingen voor uw site kunt valideren.</span><span class="sxs-lookup"><span data-stu-id="e460e-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="e460e-145">U kunt de URL vervolgens delen met andere geverifieerde commerce-gebruikers voor revisie en feedback.</span><span class="sxs-lookup"><span data-stu-id="e460e-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="e460e-146">Een CSS-overschrijvingsbestand op uw live site activeren</span><span class="sxs-lookup"><span data-stu-id="e460e-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="e460e-147">Nadat u het CSS-overschrijvingsbestand hebt bekeken en goedgekeurd, kunt u het op uw live site activeren.</span><span class="sxs-lookup"><span data-stu-id="e460e-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="e460e-148">Er kan altijd slechts één CSS-overschrijvingsbestand tegelijk actief zijn op uw site.</span><span class="sxs-lookup"><span data-stu-id="e460e-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="e460e-149">Als u een nieuw overschrijvingsbestand activeert, wordt het vorige overschrijvingsbestand gedeactiveerd.</span><span class="sxs-lookup"><span data-stu-id="e460e-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="e460e-150">Zorg er daarom voor dat alle vereiste overschrijvingen aanwezig zijn in één CSS-overschrijvingsbestand.</span><span class="sxs-lookup"><span data-stu-id="e460e-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="e460e-151">Ga als volgt te werk om een CSS-overschrijvingsbestand te activeren.</span><span class="sxs-lookup"><span data-stu-id="e460e-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="e460e-152">Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand dat u wilt activeren.</span><span class="sxs-lookup"><span data-stu-id="e460e-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="e460e-153">Onder de CSS-bestandsnaam selecteert u **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="e460e-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="e460e-154">Het overschrijvingsbestand wordt onmiddellijk actief op uw live site.</span><span class="sxs-lookup"><span data-stu-id="e460e-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="e460e-155">Een CSS-overschrijvingsbestand op uw live site deactiveren</span><span class="sxs-lookup"><span data-stu-id="e460e-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="e460e-156">Ga als volgt te werk om een CSS-overschrijvingsbestand op uw site te deactiveren.</span><span class="sxs-lookup"><span data-stu-id="e460e-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="e460e-157">Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand dat u wilt deactiveren.</span><span class="sxs-lookup"><span data-stu-id="e460e-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="e460e-158">Onder de CSS-bestandsnaam selecteert u **Deactiveren**.</span><span class="sxs-lookup"><span data-stu-id="e460e-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="e460e-159">Het overschrijvingsbestand wordt onmiddellijk inactief op uw live site.</span><span class="sxs-lookup"><span data-stu-id="e460e-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="e460e-160">Voor toegang tot extra opties voor CSS-overschrijvingsbestanden selecteert u het beletselteken (**...**) naast de CSS-bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="e460e-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="e460e-161">De opties **Downloaden**, **Naam wijzigen** en **Vervangen** zijn handig voor snelle wijzigingen in een bestaand CSS-overschrijvingsbestand.</span><span class="sxs-lookup"><span data-stu-id="e460e-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e460e-162">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="e460e-162">Additional resources</span></span>

[<span data-ttu-id="e460e-163">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="e460e-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e460e-164">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="e460e-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e460e-165">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="e460e-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e460e-166">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="e460e-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e460e-167">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="e460e-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e460e-168">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="e460e-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="e460e-169">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="e460e-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

---
title: Werken met CSS-overschrijvingsbestanden
description: In dit onderwerp wordt beschreven waarom, wanneer en hoe u CSS-overschrijvingsbestanden (Cascading Style Sheets) gebruikt in Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ef96070fe77b46622667301c7c7c402909ee7dfc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799488"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="3a154-103">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="3a154-103">Work with CSS override files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3a154-104">In dit onderwerp wordt beschreven waarom, wanneer en hoe u CSS-overschrijvingsbestanden (Cascading Style Sheets) gebruikt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3a154-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3a154-105">Permanente sitestijlen moeten doorgaans worden afgehandeld via het thema van een site.</span><span class="sxs-lookup"><span data-stu-id="3a154-105">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="3a154-106">Thema's bieden de fundamentele CSS- en stijlinstellingen voor de modules op elke pagina van uw site.</span><span class="sxs-lookup"><span data-stu-id="3a154-106">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="3a154-107">Thema's worden gemaakt met behulp van de Dynamics 365 Commerce-SDK en ze worden geïmplementeerd op uw websites via Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3a154-107">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3a154-108">Met mogelijkheden voor het opsporen van themafouten en module-interfaceconfiguraties in de SDK kunnen site-ontwikkelaar aanpasbare en samenhangende site-ontwerppakketten maken.</span><span class="sxs-lookup"><span data-stu-id="3a154-108">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="3a154-109">Wanneer deze ontwerppakketten worden geïmplementeerd op een site, kunnen site-auteurs zich concentreren op het maken, bewerken en publiceren van inhoud in plaats van op siteontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="3a154-109">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="3a154-110">Gezien de gebruikelijke levenscyclus van een thema kan de afhankelijkheid van ontwikkelaars om stijlwijzigingen door te voeren via de SDK en de LCS-implementatiepijplijn in sommige scenario's belemmerend zijn.</span><span class="sxs-lookup"><span data-stu-id="3a154-110">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="3a154-111">Prototypen of hotfixes voor de site kunnen omslachtig lijken als de SDK niet is geconfigureerd of als u geen tijd hebt om te wachten op een LCS-implementatie.</span><span class="sxs-lookup"><span data-stu-id="3a154-111">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="3a154-112">In deze scenario's kunnen CSS-overschrijvingsbestanden uitkomst bieden.</span><span class="sxs-lookup"><span data-stu-id="3a154-112">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="3a154-113">In de Commerce-ontwerpprogramma's kunnen geverifieerde gebruikers een CSS-bestand uploaden en vervolgens activeren om het thema van een site te negeren.</span><span class="sxs-lookup"><span data-stu-id="3a154-113">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="3a154-114">De overhead van SDK- of LCS-implementatie is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="3a154-114">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="3a154-115">De overschrijvingen die in een CSS-overschrijvingsbestand zijn opgegeven, kunnen zo klein zijn als één tekststijlwijziging of zo verstrekkend als een volledige merkrevisie zijn.</span><span class="sxs-lookup"><span data-stu-id="3a154-115">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="3a154-116">Houd rekening met de volgende beperkingen voordat u CSS-overschrijvingsbestanden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="3a154-116">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="3a154-117">Er kan altijd slechts één CSS-overschrijvingsbestand tegelijk actief zijn op een site.</span><span class="sxs-lookup"><span data-stu-id="3a154-117">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="3a154-118">Daarom moeten alle actieve overschrijvingen aanwezig zijn in één overschrijvingsbestand.</span><span class="sxs-lookup"><span data-stu-id="3a154-118">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="3a154-119">Hoewel u de overschrijvingen in de Commerce-ontwerpprogramma's kunt bekijken, zijn er geen speciale foutopsporingsfuncties om fouten te identificeren die door de overschrijvingen worden geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="3a154-119">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="3a154-120">Met andere woorden, wanneer u CSS-overschrijvingsbestanden gebruikt, hebt u niet dezelfde toolset die de SDK biedt voor module- en ontwerpvalidatie.</span><span class="sxs-lookup"><span data-stu-id="3a154-120">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="3a154-121">Desondanks bieden CSS-overschrijvingsbestanden een snelle manier om een ontwerpprototype te maken of een hotfix te implementeren voordat een volledige thema-update wordt ontwikkeld en geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="3a154-121">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="3a154-122">Een CSS-overschrijvingsbestand maken</span><span class="sxs-lookup"><span data-stu-id="3a154-122">Create a CSS override file</span></span>

<span data-ttu-id="3a154-123">Als u een CSS-overschrijvingsbestand wilt maken, kunt u een IDE- (Integrated Development Environment), tekst of broncode-editor gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3a154-123">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="3a154-124">U kunt standaard foutopsporingsprogramma's in uw browser gebruiken om stijlselecties, eigenschappen en waarden op uw bestaande site te identificeren.</span><span class="sxs-lookup"><span data-stu-id="3a154-124">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="3a154-125">In de meeste browsers kunt u waarden wijzigen en deze wijzigingen bekijken in het foutopsporingsprogramma.</span><span class="sxs-lookup"><span data-stu-id="3a154-125">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="3a154-126">Nadat u de wijzigingen hebt geïdentificeerd die u wilt aanbrengen, kunt u deze opslaan in uw eigen CSS-bestand.</span><span class="sxs-lookup"><span data-stu-id="3a154-126">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="3a154-127">Een CSS-overschrijvingsbestand uploaden</span><span class="sxs-lookup"><span data-stu-id="3a154-127">Upload a CSS override file</span></span>

<span data-ttu-id="3a154-128">Volg deze stappen om een CSS-bestand naar uw site te uploaden in Commerce.</span><span class="sxs-lookup"><span data-stu-id="3a154-128">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3a154-129">Ga in de ontwerpfuncties naar uw site.</span><span class="sxs-lookup"><span data-stu-id="3a154-129">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="3a154-130">Selecteer **Ontwerp** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="3a154-130">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a154-131">Afhankelijk van de versie van de Commerce-ontwerpprogramma's die u gebruikt, moet u mogelijk **Instellingen** in het navigatievenster uitvouwen voordat u **Ontwerp** kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="3a154-131">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="3a154-132">Selecteer boven in het hoofdontwerpvenster het tabblad **CSS-overschrijving** als dit nog niet is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3a154-132">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="3a154-133">Onder **Beschikbare CSS-overschrijvingen** de optie **CSS-bestand uploaden**.</span><span class="sxs-lookup"><span data-stu-id="3a154-133">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="3a154-134">Verkenner wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="3a154-134">A File Explorer window appears.</span></span>
1. <span data-ttu-id="3a154-135">Blader in Verkenner naar en selecteer een CSS-bestand en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="3a154-135">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="3a154-136">Het geüploade CSS-bestand wordt nu weergegeven onder **Beschikbare CSS-overschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="3a154-136">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="3a154-137">Een CSS-overschrijvingsbestand bekijken</span><span class="sxs-lookup"><span data-stu-id="3a154-137">Preview a CSS override file</span></span>

<span data-ttu-id="3a154-138">Als u een CSS-overschrijvingsbestand wilt bekijken voordat u het actief maakt op uw live site, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="3a154-138">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="3a154-139">Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand waarvan u een voorbeeld wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="3a154-139">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="3a154-140">Selecteer naast de CSS-bestandsnaam de optie **Site bekijken**.</span><span class="sxs-lookup"><span data-stu-id="3a154-140">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="3a154-141">Selecteer in het dialoogvenster **Een URL selecteren** de URL van de site waarvoor u de toegepaste overschrijving wilt bekijken en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a154-141">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="3a154-142">Als er meerdere varianten zijn voor de geselecteerde URL, selecteert u de gewenste variant in het dialoogvenster **Variaties bekijken** dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3a154-142">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="3a154-143">Er wordt een nieuw browsertabblad of -venster geopend waarin u uw stijloverschrijvingen voor uw site kunt valideren.</span><span class="sxs-lookup"><span data-stu-id="3a154-143">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="3a154-144">U kunt de URL vervolgens delen met andere geverifieerde commerce-gebruikers voor revisie en feedback.</span><span class="sxs-lookup"><span data-stu-id="3a154-144">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="3a154-145">Een CSS-overschrijvingsbestand op uw live site activeren</span><span class="sxs-lookup"><span data-stu-id="3a154-145">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="3a154-146">Nadat u het CSS-overschrijvingsbestand hebt bekeken en goedgekeurd, kunt u het op uw live site activeren.</span><span class="sxs-lookup"><span data-stu-id="3a154-146">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="3a154-147">Er kan altijd slechts één CSS-overschrijvingsbestand tegelijk actief zijn op uw site.</span><span class="sxs-lookup"><span data-stu-id="3a154-147">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="3a154-148">Als u een nieuw overschrijvingsbestand activeert, wordt het vorige overschrijvingsbestand gedeactiveerd.</span><span class="sxs-lookup"><span data-stu-id="3a154-148">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="3a154-149">Zorg er daarom voor dat alle vereiste overschrijvingen aanwezig zijn in één CSS-overschrijvingsbestand.</span><span class="sxs-lookup"><span data-stu-id="3a154-149">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="3a154-150">Ga als volgt te werk om een CSS-overschrijvingsbestand te activeren.</span><span class="sxs-lookup"><span data-stu-id="3a154-150">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="3a154-151">Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand dat u wilt activeren.</span><span class="sxs-lookup"><span data-stu-id="3a154-151">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="3a154-152">Onder de CSS-bestandsnaam selecteert u **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="3a154-152">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="3a154-153">Het overschrijvingsbestand wordt onmiddellijk actief op uw live site.</span><span class="sxs-lookup"><span data-stu-id="3a154-153">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="3a154-154">Een CSS-overschrijvingsbestand op uw live site deactiveren</span><span class="sxs-lookup"><span data-stu-id="3a154-154">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="3a154-155">Ga als volgt te werk om een CSS-overschrijvingsbestand op uw site te deactiveren.</span><span class="sxs-lookup"><span data-stu-id="3a154-155">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="3a154-156">Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand dat u wilt deactiveren.</span><span class="sxs-lookup"><span data-stu-id="3a154-156">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="3a154-157">Onder de CSS-bestandsnaam selecteert u **Deactiveren**.</span><span class="sxs-lookup"><span data-stu-id="3a154-157">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="3a154-158">Het overschrijvingsbestand wordt onmiddellijk inactief op uw live site.</span><span class="sxs-lookup"><span data-stu-id="3a154-158">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="3a154-159">Voor toegang tot extra opties voor CSS-overschrijvingsbestanden selecteert u het beletselteken (**...**) naast de CSS-bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="3a154-159">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="3a154-160">De opties **Downloaden**, **Naam wijzigen** en **Vervangen** zijn handig voor snelle wijzigingen in een bestaand CSS-overschrijvingsbestand.</span><span class="sxs-lookup"><span data-stu-id="3a154-160">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a154-161">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="3a154-161">Additional resources</span></span>

[<span data-ttu-id="3a154-162">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="3a154-162">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3a154-163">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="3a154-163">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3a154-164">Werken met vooraf ingestelde stijlen</span><span class="sxs-lookup"><span data-stu-id="3a154-164">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="3a154-165">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="3a154-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="3a154-166">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="3a154-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="3a154-167">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="3a154-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3a154-168">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="3a154-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3a154-169">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="3a154-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

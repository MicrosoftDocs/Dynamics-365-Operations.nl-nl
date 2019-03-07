---
title: Verbinding maken met het Help-systeem
description: In dit onderwerp worden de onderdelen van het Help-systeem beschreven voor Microsoft Dynamics 365 for Finance and Operations en vindt u een overzicht van de wijze waarop u deze verbindt. Daarnaast wordt beknopt aangegeven hoe u aangepaste Help maakt.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "317724"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="422e1-103">Verbinding maken met het Help-systeem</span><span class="sxs-lookup"><span data-stu-id="422e1-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="422e1-104">In dit onderwerp worden de onderdelen van het Help-systeem voor Microsoft Dynamics 365 for Finance and Operations beschreven.</span><span class="sxs-lookup"><span data-stu-id="422e1-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="422e1-105">Het bevat een overzicht van hoe deze onderdelen met elkaar zijn verbonden, en een samenvatting hoe u aangepaste Help kunt maken.</span><span class="sxs-lookup"><span data-stu-id="422e1-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="422e1-106">Help-architectuur</span><span class="sxs-lookup"><span data-stu-id="422e1-106">Help architecture</span></span>

<span data-ttu-id="422e1-107">De volgende afbeelding toont de onderdelen van het Help-systeem van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="422e1-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="422e1-108">Het in-product Help-systeem haalt artikelen op uit de Finance and Operations-site op https://docs.microsoft.com, evenals taakbegeleidingen die zijn opgeslagen in Business Process Modeler in Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="422e1-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="422e1-109">De functies die in het diagram zijn aangegeven met een sterretje (\*) zijn gepland, maar zijn nog niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="422e1-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="422e1-110">[![Help-architectuur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="422e1-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="422e1-111">Verbinding maken met het Help-systeem</span><span class="sxs-lookup"><span data-stu-id="422e1-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="422e1-112">Het tabblad **Taakbegeleidingen** is momenteel niet beschikbaar in Microsoft Dynamics 365 for Talent en Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="422e1-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="422e1-113">Wij werken er momenteel aan om deze functionaliteit in een toekomstige versie beschikbaar te stellen.</span><span class="sxs-lookup"><span data-stu-id="422e1-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="422e1-114">De taakbegeleidingen in de ervaring Aan de slag in Talent blijven beschikbaar om de basisfunctionaliteit uit te leggen.</span><span class="sxs-lookup"><span data-stu-id="422e1-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="422e1-115">Procedurele hulp is ook beschikbaar op de website docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) voor zowel Retail als Talent.</span><span class="sxs-lookup"><span data-stu-id="422e1-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="422e1-116">Met de pagina **Systeemparameters** verbinden systeembeheerders de delen van het Help-systeem voor een implementatie.</span><span class="sxs-lookup"><span data-stu-id="422e1-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="422e1-117">[![Formulier Systeemparameters met Help-instellingen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="422e1-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="422e1-118">Voer op de pagina **Systeemparameters** de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="422e1-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="422e1-119">De eerste keer dat u het tabblad **Help** opent, moet u verbinding maken met Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="422e1-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="422e1-120">Let erop dat u op de koppeling in het midden van het formulier klikt. Wacht op de verbinding, sluit het dialoogvenster en klik op **OK** om de pagina **Systeemparameters** op te halen.</span><span class="sxs-lookup"><span data-stu-id="422e1-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="422e1-121">[![Verbinden met LCS](./media/connect-to-lcs-crop-1024x365.png "Verbinden met LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="422e1-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="422e1-122">Selecteer het project Lifecycle Services om verbinding mee te maken.</span><span class="sxs-lookup"><span data-stu-id="422e1-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="422e1-123">Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.</span><span class="sxs-lookup"><span data-stu-id="422e1-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="422e1-124">Voor Finance and Operations selecteert u voor Microsoft-inhoud de meest recente APQC Unified Library voor Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="422e1-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="422e1-125">Voor Retail brengen we binnenkort een bibliotheek uit.</span><span class="sxs-lookup"><span data-stu-id="422e1-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="422e1-126">U hoeft geen bibliotheek te selecteren voor Talent: de verbinding met de juiste bibliotheek wordt voor u ingesteld.</span><span class="sxs-lookup"><span data-stu-id="422e1-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="422e1-127">Stel de weergavevolgorde van de BPM-bibliotheken in.</span><span class="sxs-lookup"><span data-stu-id="422e1-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="422e1-128">Dit bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.</span><span class="sxs-lookup"><span data-stu-id="422e1-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="422e1-129">Wanneer u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en op het tabblad **Taakbegeleidingen** klikken. U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="422e1-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="422e1-130">Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.</span><span class="sxs-lookup"><span data-stu-id="422e1-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="422e1-131">Vertaalde taakbegeleidingen weergeven</span><span class="sxs-lookup"><span data-stu-id="422e1-131">Showing translated task guides</span></span>

<span data-ttu-id="422e1-132">Vertaalde taakbegeleidingen zijn voor het eerst verzonden in de APQC Unified Library van mei 2016 en de Aan de slag-bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="422e1-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="422e1-133">Als u in Finance and Operations gelokaliseerde help met taakbegeleiding wilt zien, moet u ervoor zorgen verbonden te zijn met de bibliotheek van de mei-versie.</span><span class="sxs-lookup"><span data-stu-id="422e1-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="422e1-134">De taal waarin een taakbegeleiding wordt weergegeven, wordt voor elke gebruiker bepaald door de instellingen voor taal onder **Opties** &gt; **Voorkeuren**.</span><span class="sxs-lookup"><span data-stu-id="422e1-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="422e1-135">Hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de Finance and Operations-client de vertaalde namen van taakbegeleidingen niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="422e1-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="422e1-136">Ook zijn op dit moment alleen de taakbegeleidingen die in februari 2016 zijn uitgebracht beschikbaar in vertaling in de bibliotheek voor mei.</span><span class="sxs-lookup"><span data-stu-id="422e1-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="422e1-137">Wij zullen een bijgewerkte bibliotheek met extra vertalingen uitbrengen.</span><span class="sxs-lookup"><span data-stu-id="422e1-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="422e1-138">Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.</span><span class="sxs-lookup"><span data-stu-id="422e1-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="422e1-139">Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.</span><span class="sxs-lookup"><span data-stu-id="422e1-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="422e1-140">Aangepaste Help maken</span><span class="sxs-lookup"><span data-stu-id="422e1-140">Creating custom help</span></span>

<span data-ttu-id="422e1-141">U kunt taakbegeleiders maken om aangepaste Help te maken of een website te koppelen aan het Help-venster.</span><span class="sxs-lookup"><span data-stu-id="422e1-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="422e1-142">Aangepaste Help maken met taakbegeleiders</span><span class="sxs-lookup"><span data-stu-id="422e1-142">Create custom help with task guides</span></span>

<span data-ttu-id="422e1-143">U kunt voor aangepaste Help voor uw implementatie van Finance and Operations en voor Retail maken door taakregistraties te maken die uw implementatie weerspiegelen en ze op te slaan in een LCS-bibliotheek voor bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="422e1-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="422e1-144">U kunt geen aangepaste taakbegeleidingen voor Talent maken.</span><span class="sxs-lookup"><span data-stu-id="422e1-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="422e1-145">Voor partners: als u een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten.</span><span class="sxs-lookup"><span data-stu-id="422e1-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="422e1-146">U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens uw kopie openen, hierin taakregistraties openen, deze wijzigen en de registraties met uw wijzigingen opslaan.</span><span class="sxs-lookup"><span data-stu-id="422e1-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="422e1-147">Zie [Een taakregistratie voor een documentatie of training maken](../../dev-itpro/user-interface/task-recorder.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="422e1-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="422e1-148">Verbinding maken met een aangepaste site</span><span class="sxs-lookup"><span data-stu-id="422e1-148">Connect a custom site</span></span>

<span data-ttu-id="422e1-149">Microsoft heeft een whitepaper en voorbeeldcode beschikbaar gesteld waarin wordt beschreven hoe u een aangepaste Help-site maakt en koppelt aan het Help-venster.</span><span class="sxs-lookup"><span data-stu-id="422e1-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="422e1-150">Ga voor meer informatie naar:</span><span class="sxs-lookup"><span data-stu-id="422e1-150">For more information, see:</span></span>

- [<span data-ttu-id="422e1-151">Aangepaste Help maken voor Finance and Operations (whitepaper)</span><span class="sxs-lookup"><span data-stu-id="422e1-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="422e1-152">Custom help GitHub repository</span><span class="sxs-lookup"><span data-stu-id="422e1-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="422e1-153">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="422e1-153">Additional resources</span></span>

[<span data-ttu-id="422e1-154">Help-overzicht</span><span class="sxs-lookup"><span data-stu-id="422e1-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="422e1-155">Overzicht taakrecorder</span><span class="sxs-lookup"><span data-stu-id="422e1-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="422e1-156">Een taakregistratie voor een documentatie of training maken</span><span class="sxs-lookup"><span data-stu-id="422e1-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)

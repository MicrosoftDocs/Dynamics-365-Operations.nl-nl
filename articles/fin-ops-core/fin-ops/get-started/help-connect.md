---
title: De Help-ervaring voor Finance and Operations-apps configureren
description: Dit onderwerp biedt informatie over de onderdelen van het Help-systeem voor sommige Microsoft Dynamics 365-apps.
author: margoc
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82bb9a09e6d302b0d453ceb5131da039769b58fb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745684"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="5caef-103">De Help-ervaring voor Finance and Operations-apps configureren</span><span class="sxs-lookup"><span data-stu-id="5caef-103">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5caef-104">In dit onderwerp vindt u een overzicht van de onderdelen van het Help-systeem voor Finance and Operations-apps, zoals Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce en Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5caef-104">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5caef-105">Ook wordt uitgelegd hoe u deze onderdelen verbindt en u vindt een overzicht van het proces voor het maken van aangepaste Help.</span><span class="sxs-lookup"><span data-stu-id="5caef-105">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="5caef-106">Help-architectuur</span><span class="sxs-lookup"><span data-stu-id="5caef-106">Help architecture</span></span>

<span data-ttu-id="5caef-107">Finance and Operations-apps bevatten conceptuele overzichten en andere onderwerpen die op de [https://docs.microsoft.com/dynamics365](/dynamics365/)-site worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="5caef-107">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="5caef-108">Deze inhoud kan vervolgens worden geopend vanuit het deelvenster **Help** in het product.</span><span class="sxs-lookup"><span data-stu-id="5caef-108">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="5caef-109">De volgende afbeelding toont de onderdelen van het Help-systeem.</span><span class="sxs-lookup"><span data-stu-id="5caef-109">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="5caef-110">[![Help-architectuur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="5caef-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="5caef-111">De Help van het product haalt artikelen op van docs.microsoft.com en andere verbonden websites.</span><span class="sxs-lookup"><span data-stu-id="5caef-111">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="5caef-112">Daarnaast worden taakbegeleidingen opgehaald die zijn opgeslagen in Modelleertool bedrijfsprocessen in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5caef-112">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="5caef-113">Taakbegeleidingen toevoegen</span><span class="sxs-lookup"><span data-stu-id="5caef-113">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="5caef-114">Het tabblad **Taakbegeleidingen** is momenteel niet beschikbaar in Human Resources of Commerce.</span><span class="sxs-lookup"><span data-stu-id="5caef-114">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="5caef-115">De taakbegeleidingen in de ervaring Aan de slag in Human Resources blijven echter beschikbaar om de basisfunctionaliteit uit te leggen.</span><span class="sxs-lookup"><span data-stu-id="5caef-115">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="5caef-116">Procedurele Help is beschikbaar op de site [https://docs.microsoft.com/dynamics365](/dynamics365/) voor zowel Human Resources als Commerce.</span><span class="sxs-lookup"><span data-stu-id="5caef-116">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="5caef-117">Op de pagina **Systeemparameters** kunnen systeembeheerders de toegang tot relevante bibliotheken voor taakbegeleidingen configureren voor een implementatie.</span><span class="sxs-lookup"><span data-stu-id="5caef-117">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="5caef-118">Voordat u Help kunt configureren, moet u zich aanmelden met een account in de dezelfde tenant als de tenant waarin de app is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="5caef-118">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="5caef-119">Een LCS-bibliotheek kan niet worden verbonden vanuit een exemplaar van de app die wordt uitgevoerd op een lokale virtuele harde schijf (VHD).</span><span class="sxs-lookup"><span data-stu-id="5caef-119">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="5caef-120">[![Formulier Systeemparameters met Help-instellingen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="5caef-120">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="5caef-121&quot;>Als u taakbegeleidingen voor een oplossing wilt configureren, volgt u deze stappen op de pagina **Systeemparameters**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;5caef-121&quot;>To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id=&quot;5caef-122&quot;>De eerste keer dat u het tabblad **Help** opent, moet u verbinding maken met Lifecycle Services.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;5caef-122&quot;>The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id=&quot;5caef-123&quot;>Let erop dat u de koppeling in het midden van het formulier selecteert. Wacht op de verbinding, sluit het dialoogvenster en selecteer **OK** om de pagina **Systeemparameters** te openen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;5caef-123&quot;>Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id=&quot;5caef-124&quot;>[![Verbinden met LCS](./media/connect-to-lcs-crop-1024x365.png &quot;Verbinden met LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="5caef-124">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="5caef-125">Selecteer het project Lifecycle Services om verbinding mee te maken.</span><span class="sxs-lookup"><span data-stu-id="5caef-125">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="5caef-126">Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.</span><span class="sxs-lookup"><span data-stu-id="5caef-126">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="5caef-127">Stel de weergavevolgorde van de BPM-bibliotheken in.</span><span class="sxs-lookup"><span data-stu-id="5caef-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="5caef-128">Dit weergavevolgorde bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.</span><span class="sxs-lookup"><span data-stu-id="5caef-128">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="5caef-129">Wanneer u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en het tabblad **Taakbegeleidingen** selecteren. U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="5caef-129">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="5caef-130">Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.</span><span class="sxs-lookup"><span data-stu-id="5caef-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="5caef-131">Vertaalde taakbegeleidingen weergeven</span><span class="sxs-lookup"><span data-stu-id="5caef-131">Showing translated task guides</span></span>

<span data-ttu-id="5caef-132">Vertaalde taakbegeleidingen zijn voor het eerst uitgebracht in de APQC Unified Library van mei 2016 en de Aan de slag-bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="5caef-132">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="5caef-133">Als u gelokaliseerde Help met taakbegeleiding wilt zien, moet u ervoor zorgen dat uw Dynamics 365-oplossing is verbonden met de bibliotheek van mei 2016.</span><span class="sxs-lookup"><span data-stu-id="5caef-133">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="5caef-134">Gebruikers kunnen de taal wijzigen waarin een taakbegeleiding wordt weergegeven door de taalinstellingen onder **Opties** &gt; **Voorkeuren** te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="5caef-134">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="5caef-135">Hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de client de vertaalde namen van taakbegeleidingen niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5caef-135">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="5caef-136">Daarnaast zijn in de bibliotheek van mei 2016 alleen vertalingen beschikbaar voor de taakbegeleidingen die in februari 2016 zijn uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="5caef-136">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="5caef-137">Microsoft brengt een bijgewerkte bibliotheek met extra vertalingen uit.</span><span class="sxs-lookup"><span data-stu-id="5caef-137">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="5caef-138">Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.</span><span class="sxs-lookup"><span data-stu-id="5caef-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="5caef-139">Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.</span><span class="sxs-lookup"><span data-stu-id="5caef-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="5caef-140">Aangepaste Help toevoegen</span><span class="sxs-lookup"><span data-stu-id="5caef-140">Adding custom Help</span></span>

<span data-ttu-id="5caef-141">U kunt taakbegeleidingen maken om aangepaste Help te maken of een aangepaste Help-website koppelen aan het deelvenster **Help**.</span><span class="sxs-lookup"><span data-stu-id="5caef-141">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="5caef-142">Aangepaste Help maken met taakbegeleidingen</span><span class="sxs-lookup"><span data-stu-id="5caef-142">Create custom Help by using task guides</span></span>

<span data-ttu-id="5caef-143">U kunt aangepaste Help voor de ondersteunde apps maken door taakregistraties te maken die uw implementatie weerspiegelen en deze op te slaan in een bedrijfsprocesbibliotheek in LCS.</span><span class="sxs-lookup"><span data-stu-id="5caef-143">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="5caef-144">U kunt geen aangepaste taakbegeleidingen voor Human Resources maken.</span><span class="sxs-lookup"><span data-stu-id="5caef-144">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="5caef-145">Als u een partner bent en een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten.</span><span class="sxs-lookup"><span data-stu-id="5caef-145">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="5caef-146">U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens de taakregistraties in de kopie openen, deze bewerken en uw wijzigingen opslaan.</span><span class="sxs-lookup"><span data-stu-id="5caef-146">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="5caef-147">Zie [Resources voor Taakrecorder](../../dev-itpro/user-interface/task-recorder.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5caef-147">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="5caef-148">Verbinding maken met een aangepaste Help-site</span><span class="sxs-lookup"><span data-stu-id="5caef-148">Connect a custom Help site</span></span>

<span data-ttu-id="5caef-149">Finance and Operations-apps worden zelden in hun kant-en-klare vorm gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5caef-149">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="5caef-150">In plaats daarvan wordt de oplossing aangepast en uitgebreid om aan de behoeften van de organisatie te voldoen.</span><span class="sxs-lookup"><span data-stu-id="5caef-150">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="5caef-151">U kunt de Help-ervaring ook aanpassen en uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="5caef-151">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="5caef-152">U kunt bijvoorbeeld aangepaste Help toevoegen aan het deelvenster **Help** in het product.</span><span class="sxs-lookup"><span data-stu-id="5caef-152">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="5caef-153">Microsoft heeft een toolkit geleverd waarmee u aangepaste Help kunt implementeren en kunt koppelen aan het deelvenster **Help**.</span><span class="sxs-lookup"><span data-stu-id="5caef-153">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="5caef-154">Zie [Overzicht van aangepaste Help](../../dev-itpro/help/custom-help-overview.md) voor informatie over het instellen van een aangepaste Help-oplossing die is gekoppeld aan het deelvenster **Help**.</span><span class="sxs-lookup"><span data-stu-id="5caef-154">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="5caef-155">Als u wilt samenwerken met Microsoft aan hulpprogramma's en processen voor het aanpassen van de Help, vult u het formulier in op [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="5caef-155">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="5caef-156">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5caef-156">See also</span></span>

[<span data-ttu-id="5caef-157">Help-systeem</span><span class="sxs-lookup"><span data-stu-id="5caef-157">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="5caef-158">Overzicht van aangepaste Help</span><span class="sxs-lookup"><span data-stu-id="5caef-158">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="5caef-159">Resources voor Taakrecorder</span><span class="sxs-lookup"><span data-stu-id="5caef-159">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="5caef-160">Documentatie of training maken met Taakrecorder</span><span class="sxs-lookup"><span data-stu-id="5caef-160">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="5caef-161">Custom Help GitHub repository</span><span class="sxs-lookup"><span data-stu-id="5caef-161">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
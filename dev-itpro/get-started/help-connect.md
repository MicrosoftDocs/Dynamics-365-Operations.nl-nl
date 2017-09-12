---
title: Het Help-systeem verbinden
description: In dit onderwerp worden de onderdelen van het Help-systeem voor Microsoft Dynamics 365 for Finance and Operations beschreven en vindt u een overzicht van de wijze waarop u deze verbindt. Daarnaast wordt beknopt aangegeven hoe u aangepaste Help maakt.
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="1686b-103">Het Help-systeem verbinden</span><span class="sxs-lookup"><span data-stu-id="1686b-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1686b-104">In dit onderwerp worden de onderdelen van het Help-systeem voor Microsoft Dynamics 365 for Finance and Operations beschreven.</span><span class="sxs-lookup"><span data-stu-id="1686b-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1686b-105">Het bevat een overzicht van hoe deze onderdelen met elkaar zijn verbonden, en een samenvatting hoe u aangepaste Help kunt maken.</span><span class="sxs-lookup"><span data-stu-id="1686b-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="1686b-106">Help-architectuur</span><span class="sxs-lookup"><span data-stu-id="1686b-106">Help architecture</span></span>
<span data-ttu-id="1686b-107">De volgende afbeelding toont de onderdelen van het Help-systeem van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1686b-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="1686b-108">Het in-product Help-systeem haalt artikelen op uit de Finance and Operations-site op https://docs.microsoft.com, evenals taakbegeleidingen die zijn opgeslagen in Business Process Modeler in Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1686b-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="1686b-109">De functies die in het diagram zijn aangegeven met een sterretje (\*) zijn gepland, maar zijn nog niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="1686b-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="1686b-110">[![Help-architectuur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="1686b-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="1686b-111">Verbinding maken met het Help-systeem</span><span class="sxs-lookup"><span data-stu-id="1686b-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="1686b-112">Het tabblad **Taakbegeleidingen** is momenteel niet beschikbaar in Microsoft Dynamics 365 for Talent en Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1686b-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1686b-113">Wij werken er momenteel aan om deze functionaliteit in een toekomstige versie beschikbaar te stellen.</span><span class="sxs-lookup"><span data-stu-id="1686b-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="1686b-114">De taakbegeleidingen in de ervaring Aan de slag in Talent blijven beschikbaar om de basisfunctionaliteit uit te leggen.</span><span class="sxs-lookup"><span data-stu-id="1686b-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="1686b-115">Procedurele help is ook beschikbaar op de website docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) voor zowel Retail als Talent.</span><span class="sxs-lookup"><span data-stu-id="1686b-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="1686b-116">Met de pagina **Systeemparameters** verbinden systeembeheerders de delen van het Help-systeem voor een implementatie.</span><span class="sxs-lookup"><span data-stu-id="1686b-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="1686b-117">[![Formulier Systeemparameters met Help-instellingen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Voer de volgende stappen uit op de pagina **Systeemparameters**:</span><span class="sxs-lookup"><span data-stu-id="1686b-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1686b-118">De eerste keer dat u het tabblad **Help** opent, moet u verbinding maken met Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="1686b-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="1686b-119">Zorg ervoor dat u op de koppeling in het midden van het formulier klikt, wacht op de verbinding, sluit het dialoogvenster en klik op **OK** om de pagina **Systeemparameters** op te halen.[![Verbinden met LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="1686b-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="1686b-120">Selecteer het project Lifecycle Services om verbinding mee te maken.</span><span class="sxs-lookup"><span data-stu-id="1686b-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="1686b-121">Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.</span><span class="sxs-lookup"><span data-stu-id="1686b-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="1686b-122">Voor Finance and Operations selecteert u voor Microsoft-inhoud de 2017 februari QPC Unified Library voor Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1686b-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="1686b-123">Voor Retail brengen we in juli een bibliotheek uit.</span><span class="sxs-lookup"><span data-stu-id="1686b-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="1686b-124">U hoeft geen bibliotheek te selecteren voor Talent: de verbinding met de juiste bibliotheek wordt voor u ingesteld.</span><span class="sxs-lookup"><span data-stu-id="1686b-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="1686b-125">Stel de weergavevolgorde van de BPM-bibliotheken in.</span><span class="sxs-lookup"><span data-stu-id="1686b-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="1686b-126">Dit bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.</span><span class="sxs-lookup"><span data-stu-id="1686b-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="1686b-127">Nadat u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en op het tabblad **Taakbegeleidingen** klikken.</span><span class="sxs-lookup"><span data-stu-id="1686b-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="1686b-128">U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1686b-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="1686b-129">Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.</span><span class="sxs-lookup"><span data-stu-id="1686b-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="1686b-130">Vertaalde taakbegeleidingen weergeven</span><span class="sxs-lookup"><span data-stu-id="1686b-130">Showing translated task guides</span></span>

<span data-ttu-id="1686b-131">Vertaalde taakbegeleidingen zijn voor het eerst verzonden in de APQC Unified Library van mei 2016 en de Aan de slag-bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="1686b-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="1686b-132">Als u in Finance and Operations gelokaliseerde help met taakbegeleiding wilt zien, moet u ervoor zorgen verbonden te zijn met de bibliotheek van de mei-versie.</span><span class="sxs-lookup"><span data-stu-id="1686b-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="1686b-133">De taal waarin een taakbegeleiding wordt weergegeven, wordt voor elke gebruiker bepaald door de instellingen voor taal onder **Opties** &gt; **Voorkeuren**.</span><span class="sxs-lookup"><span data-stu-id="1686b-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="1686b-134">Hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de Finance and Operations-client de vertaalde namen van taakbegeleidingen niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1686b-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="1686b-135">Ook zijn op dit moment alleen de taakbegeleidingen die in februari 2016 zijn uitgebracht beschikbaar in vertaling in de bibliotheek voor mei.</span><span class="sxs-lookup"><span data-stu-id="1686b-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="1686b-136">Wij zullen een bijgewerkte bibliotheek met extra vertalingen uitbrengen.</span><span class="sxs-lookup"><span data-stu-id="1686b-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="1686b-137">Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.</span><span class="sxs-lookup"><span data-stu-id="1686b-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="1686b-138">Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.</span><span class="sxs-lookup"><span data-stu-id="1686b-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="1686b-139">Aangepaste Help maken</span><span class="sxs-lookup"><span data-stu-id="1686b-139">Creating custom help</span></span>
<span data-ttu-id="1686b-140">U kunt voor aangepaste Help voor uw implementatie van Finance and Operations en voor Retail maken door taakregistraties te maken die uw implementatie weerspiegelen en ze op te slaan in een LCS-bibliotheek voor bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="1686b-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="1686b-141">U kunt geen aangepaste taakbegeleidingen voor Talent maken.</span><span class="sxs-lookup"><span data-stu-id="1686b-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="1686b-142">Voor partners: als u een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten.</span><span class="sxs-lookup"><span data-stu-id="1686b-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="1686b-143">U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens uw kopie openen, hierin taakregistraties openen, deze wijzigen en de registraties met uw wijzigingen opslaan.</span><span class="sxs-lookup"><span data-stu-id="1686b-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="1686b-144">Zie [Een taakregistratie voor een documentatie of training maken](../user-interface/task-recorder.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1686b-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="1686b-145">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1686b-145">See also</span></span>
--------

[<span data-ttu-id="1686b-146">Help-overzicht</span><span class="sxs-lookup"><span data-stu-id="1686b-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="1686b-147">Overzicht taakrecorder</span><span class="sxs-lookup"><span data-stu-id="1686b-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="1686b-148">Een taakregistratie voor een documentatie of training maken</span><span class="sxs-lookup"><span data-stu-id="1686b-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)






---
title: De uitvoeringsinterface voor de werkvloer ontwerpen
description: In dit onderwerp wordt beschreven hoe u de inhoud van de gebruikersinterface ontwerpt voor elke configuratie.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 786ea9a3da98e9f1812b007d4301cb47680e6894
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077573"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="3b276-103">De uitvoeringsinterface voor de werkvloer ontwerpen</span><span class="sxs-lookup"><span data-stu-id="3b276-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3b276-104">U kunt de inhoud van de gebruikersinterface ontwerpen voor elke configuratie die wordt gebruikt door de uitvoeringsinterface van de werkvloer.</span><span class="sxs-lookup"><span data-stu-id="3b276-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="3b276-105">Werknemers in de ene werkcel moeten bijvoorbeeld mogelijk taakinstructies kunnen openen op de productievloer, terwijl in een andere werkcel de instructies niet nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="3b276-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="3b276-106">In dat geval moeten er twee configuraties worden gemaakt, één met een knop voor het openen van documentbijlagen en één zonder deze knop.</span><span class="sxs-lookup"><span data-stu-id="3b276-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="3b276-107">Een tabblad ontwerpen</span><span class="sxs-lookup"><span data-stu-id="3b276-107">Design a tab</span></span>

<span data-ttu-id="3b276-108">Op de pagina **Uitvoering werkvloer configureren** kunt u tabbladen maken en configureren door **Tabbladen ontwerpen** te selecteren in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="3b276-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="3b276-109">Elk tabblad is verdeeld in vier secties, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3b276-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="3b276-110">![Indeling van tabbladen](media/pfe-tab-layout.png "Indeling van tabbladen")</span><span class="sxs-lookup"><span data-stu-id="3b276-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="3b276-111">De volgende elementen worden in de afbeelding weergegeven:</span><span class="sxs-lookup"><span data-stu-id="3b276-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="3b276-112">Primaire werkbalk</span><span class="sxs-lookup"><span data-stu-id="3b276-112">Primary toolbar</span></span>
1. <span data-ttu-id="3b276-113">Secundaire werkbalk</span><span class="sxs-lookup"><span data-stu-id="3b276-113">Secondary toolbar</span></span>
1. <span data-ttu-id="3b276-114">Hoofdweergave</span><span class="sxs-lookup"><span data-stu-id="3b276-114">Main view</span></span>
1. <span data-ttu-id="3b276-115">Gedetailleerde weergave</span><span class="sxs-lookup"><span data-stu-id="3b276-115">Detailed view</span></span>

<span data-ttu-id="3b276-116">Voer de volgende stappen uit om een nieuw tabblad te maken en te configureren:</span><span class="sxs-lookup"><span data-stu-id="3b276-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="3b276-117">Ga naar **Productiebeheer &gt; Instellingen &gt; Productie-uitvoering**.</span><span class="sxs-lookup"><span data-stu-id="3b276-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="3b276-118">Selecteer **Tabbladen ontwerpen** in het actievenster om de pagina **Tabbladen ontwerpen** te openen.</span><span class="sxs-lookup"><span data-stu-id="3b276-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="3b276-119">![De pagina Tabbladen ontwerpen](media/pfe-design-tabs.png "De pagina Tabbladen ontwerpen")</span><span class="sxs-lookup"><span data-stu-id="3b276-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="3b276-120">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="3b276-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="3b276-121">Geef de koptekst van de pagina de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="3b276-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="3b276-122">**Tabbladnaam**: geef een naam op voor het tabblad.</span><span class="sxs-lookup"><span data-stu-id="3b276-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="3b276-123">**Hoofdweergave**: maak een selectie uit de vooraf gedefinieerde takenlijsten (*Actieve taken*, *Alle taken* of *Mijn machine*).</span><span class="sxs-lookup"><span data-stu-id="3b276-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="3b276-124">**Detailweergave**: selecteer uit een lege waarde of **Taakdetails**.</span><span class="sxs-lookup"><span data-stu-id="3b276-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="3b276-125">Als u de lege waarde selecteert, wordt op het tabblad geen gedetailleerde weergave weergegeven. Als u **Taakdetails selecteert**, bevat de gedetailleerde weergave een gedetailleerde omschrijving van de taak die in de takenlijst in de hoofdweergave is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3b276-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="3b276-126">Kies in de sectie **Primaire werkbalk** welke knoppen beschikbaar moeten zijn op de primaire werkbalk.</span><span class="sxs-lookup"><span data-stu-id="3b276-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="3b276-127">De kolom **Beschikbare acties** geeft een lijst weer met alle knoppen die kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3b276-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="3b276-128">De kolommen **Geselecteerde acties** geeft een lijst weer met alle knoppen die in de huidige configuratie zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="3b276-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="3b276-129">Gebruik de knoppen tussen de kolommen om geselecteerde artikelen naar wens tussen de kolommen te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="3b276-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="3b276-130">Gebruik de knoppen omhoog en omlaag naast de kolom **Geselecteerde acties** om de volgorde te bepalen waarin de knoppen in de gebruikersinterface worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3b276-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="3b276-131">Kies in de sectie **Secundaire** **werkbalk** welke knoppen beschikbaar moeten zijn op de secundaire werkbalk.</span><span class="sxs-lookup"><span data-stu-id="3b276-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="3b276-132">De kolom **Beschikbare acties** geeft een lijst weer met alle knoppen die kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3b276-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="3b276-133">De kolommen **Geselecteerde acties** geeft een lijst weer met alle knoppen die in de huidige configuratie zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="3b276-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="3b276-134">Gebruik de knoppen tussen de kolommen om geselecteerde artikelen naar wens tussen de kolommen te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="3b276-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="3b276-135">Gebruik de knoppen omhoog en omlaag naast de kolom **Geselecteerde acties** om de volgorde te bepalen waarin de knoppen in de gebruikersinterface worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3b276-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="3b276-136">Een tabblad aan een configuratie koppelen</span><span class="sxs-lookup"><span data-stu-id="3b276-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="3b276-137">Nadat u alle benodigde tabbladen hebt ontworpen, kunt u deze aan een configuratie koppelen.</span><span class="sxs-lookup"><span data-stu-id="3b276-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="3b276-138">Ga naar **Productiebeheer &gt; Instellingen &gt; Uitvoering werkvloer configureren**.</span><span class="sxs-lookup"><span data-stu-id="3b276-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="3b276-139">![Uitvoering productievloer configureren](media/pfe-config-prod-floor-execution.png "Uitvoering productievloer configureren")</span><span class="sxs-lookup"><span data-stu-id="3b276-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="3b276-140">Selecteer op de snelle tab **Tabblad selecteren** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3b276-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="3b276-141">Er wordt een nieuwe rij aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3b276-141">A new row is added to the grid.</span></span> <span data-ttu-id="3b276-142">Selecteer voor deze nieuwe rij de naam van een tabblad dat u aan de configuratie wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3b276-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="3b276-143">Ga zo nodig verder om extra tabbladen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3b276-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="3b276-144">Gebruik de knoppen **Omhoog verplaatsen** en **Omlaag verplaatsen** op de werkbalk om de tabbladen naar wens te rangschikken.</span><span class="sxs-lookup"><span data-stu-id="3b276-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="3b276-145">De tabbladen worden van links naar rechts weergegeven in de volgorde die op de bovenstaande schermopname wordt weergegeven (het tabblad bovenaan wordt links weergegeven).</span><span class="sxs-lookup"><span data-stu-id="3b276-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>

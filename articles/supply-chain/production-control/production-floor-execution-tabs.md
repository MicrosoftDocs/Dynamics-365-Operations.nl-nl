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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664267"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="f8d91-103">De uitvoeringsinterface voor de werkvloer ontwerpen</span><span class="sxs-lookup"><span data-stu-id="f8d91-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f8d91-104">U kunt de inhoud van de gebruikersinterface ontwerpen voor elke configuratie die wordt gebruikt door de uitvoeringsinterface van de werkvloer.</span><span class="sxs-lookup"><span data-stu-id="f8d91-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="f8d91-105">Werknemers in de ene werkcel moeten bijvoorbeeld mogelijk taakinstructies kunnen openen op de productievloer, terwijl in een andere werkcel de instructies niet nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="f8d91-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="f8d91-106">In dat geval moeten er twee configuraties worden gemaakt, één met een knop voor het openen van documentbijlagen en één zonder deze knop.</span><span class="sxs-lookup"><span data-stu-id="f8d91-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="f8d91-107">Een tabblad ontwerpen</span><span class="sxs-lookup"><span data-stu-id="f8d91-107">Design a tab</span></span>

<span data-ttu-id="f8d91-108">Op de pagina **Uitvoering werkvloer configureren** kunt u tabbladen maken en configureren door **Tabbladen ontwerpen** te selecteren in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f8d91-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="f8d91-109">Elk tabblad is verdeeld in vier secties, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8d91-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="f8d91-110">![Indeling van tabbladen](media/pfe-tab-layout.png "Indeling van tabbladen")</span><span class="sxs-lookup"><span data-stu-id="f8d91-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="f8d91-111">De volgende elementen worden in de afbeelding weergegeven:</span><span class="sxs-lookup"><span data-stu-id="f8d91-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="f8d91-112">Primaire werkbalk</span><span class="sxs-lookup"><span data-stu-id="f8d91-112">Primary toolbar</span></span>
1. <span data-ttu-id="f8d91-113">Secundaire werkbalk</span><span class="sxs-lookup"><span data-stu-id="f8d91-113">Secondary toolbar</span></span>
1. <span data-ttu-id="f8d91-114">Hoofdweergave</span><span class="sxs-lookup"><span data-stu-id="f8d91-114">Main view</span></span>
1. <span data-ttu-id="f8d91-115">Gedetailleerde weergave</span><span class="sxs-lookup"><span data-stu-id="f8d91-115">Detailed view</span></span>

<span data-ttu-id="f8d91-116">Voer de volgende stappen uit om een nieuw tabblad te maken en te configureren:</span><span class="sxs-lookup"><span data-stu-id="f8d91-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="f8d91-117">Ga naar **Productiebeheer &gt; Instellingen &gt; Productie-uitvoering**.</span><span class="sxs-lookup"><span data-stu-id="f8d91-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="f8d91-118">Selecteer **Tabbladen ontwerpen** in het actievenster om de pagina **Tabbladen ontwerpen** te openen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="f8d91-119">![De pagina Tabbladen ontwerpen](media/pfe-design-tabs.png "De pagina Tabbladen ontwerpen")</span><span class="sxs-lookup"><span data-stu-id="f8d91-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="f8d91-120">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f8d91-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="f8d91-121">Geef de koptekst van de pagina de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="f8d91-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="f8d91-122">**Tabbladnaam**: geef een naam op voor het tabblad.</span><span class="sxs-lookup"><span data-stu-id="f8d91-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="f8d91-123">**Hoofdweergave**: selecteer uit twee vooraf gedefinieerde takenlijsten (*Actieve taken* of *Alle taken*).</span><span class="sxs-lookup"><span data-stu-id="f8d91-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="f8d91-124">**Detailweergave**: selecteer uit een lege waarde of **Taakdetails**.</span><span class="sxs-lookup"><span data-stu-id="f8d91-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="f8d91-125">Als u de lege waarde selecteert, wordt op het tabblad geen gedetailleerde weergave weergegeven. Als u **Taakdetails selecteert**, bevat de gedetailleerde weergave een gedetailleerde omschrijving van de taak die in de takenlijst in de hoofdweergave is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f8d91-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="f8d91-126">Kies in de sectie **Primaire werkbalk** welke knoppen beschikbaar moeten zijn op de primaire werkbalk.</span><span class="sxs-lookup"><span data-stu-id="f8d91-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="f8d91-127">De kolom **Beschikbare acties** geeft een lijst weer met alle knoppen die kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f8d91-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="f8d91-128">De kolommen **Geselecteerde acties** geeft een lijst weer met alle knoppen die in de huidige configuratie zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="f8d91-129">Gebruik de knoppen tussen de kolommen om geselecteerde artikelen naar wens tussen de kolommen te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="f8d91-130">Gebruik de knoppen omhoog en omlaag naast de kolom **Geselecteerde acties** om de volgorde te bepalen waarin de knoppen in de gebruikersinterface worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8d91-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="f8d91-131">Kies in de sectie **Secundaire** **werkbalk** welke knoppen beschikbaar moeten zijn op de secundaire werkbalk.</span><span class="sxs-lookup"><span data-stu-id="f8d91-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="f8d91-132">De kolom **Beschikbare acties** geeft een lijst weer met alle knoppen die kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f8d91-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="f8d91-133">De kolommen **Geselecteerde acties** geeft een lijst weer met alle knoppen die in de huidige configuratie zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="f8d91-134">Gebruik de knoppen tussen de kolommen om geselecteerde artikelen naar wens tussen de kolommen te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="f8d91-135">Gebruik de knoppen omhoog en omlaag naast de kolom **Geselecteerde acties** om de volgorde te bepalen waarin de knoppen in de gebruikersinterface worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8d91-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="f8d91-136">Een tabblad aan een configuratie koppelen</span><span class="sxs-lookup"><span data-stu-id="f8d91-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="f8d91-137">Nadat u alle benodigde tabbladen hebt ontworpen, kunt u deze aan een configuratie koppelen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="f8d91-138">Ga naar **Productiebeheer &gt; Instellingen &gt; Uitvoering werkvloer configureren**.</span><span class="sxs-lookup"><span data-stu-id="f8d91-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="f8d91-139">![Uitvoering productievloer configureren](media/pfe-config-prod-floor-execution.png "Uitvoering productievloer configureren")</span><span class="sxs-lookup"><span data-stu-id="f8d91-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="f8d91-140">Selecteer op de snelle tab **Tabblad selecteren** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f8d91-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="f8d91-141">Er wordt een nieuwe rij aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f8d91-141">A new row is added to the grid.</span></span> <span data-ttu-id="f8d91-142">Selecteer voor deze nieuwe rij de naam van een tabblad dat u aan de configuratie wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="f8d91-143">Ga zo nodig verder om extra tabbladen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="f8d91-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="f8d91-144">Gebruik de knoppen **Omhoog verplaatsen** en **Omlaag verplaatsen** op de werkbalk om de tabbladen naar wens te rangschikken.</span><span class="sxs-lookup"><span data-stu-id="f8d91-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="f8d91-145">De tabbladen worden van links naar rechts weergegeven in de volgorde die op de bovenstaande schermopname wordt weergegeven (het tabblad bovenaan wordt links weergegeven).</span><span class="sxs-lookup"><span data-stu-id="f8d91-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>

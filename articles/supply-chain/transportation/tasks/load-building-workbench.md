---
title: Workbench voor ladingopbouw
description: In dit onderwerp wordt beschreven hoe u werkt met de workbench voor ladingopbouw.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 480006a6d091acdf5c88fdbf0d9e625088d660d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247233"
---
# <a name="load-building-workbench"></a><span data-ttu-id="c1c38-103">Workbench voor ladingopbouw</span><span class="sxs-lookup"><span data-stu-id="c1c38-103">Load building workbench</span></span>

<span data-ttu-id="c1c38-104">Met de workbench voor ladingopbouw kunt u strategieën voor ladingopbouw toepassen wanneer u ladingen maakt.</span><span class="sxs-lookup"><span data-stu-id="c1c38-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="c1c38-105">Een strategie voor ladingopbouw maken</span><span class="sxs-lookup"><span data-stu-id="c1c38-105">Create a load building strategy</span></span>

<span data-ttu-id="c1c38-106">U gebruikt strategieën voor ladingopbouw om automatisch ladingen op te bouwen.</span><span class="sxs-lookup"><span data-stu-id="c1c38-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="c1c38-107">Deze mogelijkheid kan nuttig zijn in de volgende situaties:</span><span class="sxs-lookup"><span data-stu-id="c1c38-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="c1c38-108">Als u regelmatig een specifieke set producten verzendt, helpen laadstrategieën tijd te besparen, omdat u niet elke keer dezelfde lading hoeft op te bouwen.</span><span class="sxs-lookup"><span data-stu-id="c1c38-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="c1c38-109">Als u half volle ladingen wilt vermijden om de efficiëntie te maximaliseren, kunnen laadstrategieën helpen elke lading zo veel mogelijk te vullen.</span><span class="sxs-lookup"><span data-stu-id="c1c38-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="c1c38-110">Een klasse voor een strategie voor ladingopbouw met de naam `TMSLoadBuildingVolumeStrategy` biedt een strategie voor ladingopbouw die *de op volume gebaseerde ladingopbouwstrategie* wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="c1c38-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="c1c38-111">Met deze strategie kunt u de maximumwaarden gebruiken die worden opgegeven voor hoogte en gewicht in de ladingsjabloon. U kunt ook de instellingen overschrijven door nieuwe waarden in te voeren.</span><span class="sxs-lookup"><span data-stu-id="c1c38-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="c1c38-112">Deze strategie is de enige strategie die kant en klaar wordt meegeleverd.</span><span class="sxs-lookup"><span data-stu-id="c1c38-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="c1c38-113">(Misschien hebt u wel een aantal aangepaste strategieën.)</span><span class="sxs-lookup"><span data-stu-id="c1c38-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="c1c38-114">Als u de kant-en-klare *op volume gebaseerde ladingopbouwstrategie* wilt gebruiken, selecteert u deze strategie in het veld **Ladingopbouwstrategie** op de pagina **Workbench voor ladingopbouw** (**Transportbeheer &gt; Planning &gt; Workbench voor ladingopbouw**).</span><span class="sxs-lookup"><span data-stu-id="c1c38-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="c1c38-115">Volg deze stappen om een ladingopbouwstrategie te maken.</span><span class="sxs-lookup"><span data-stu-id="c1c38-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="c1c38-116">Ga naar **Transportbeheer &gt; Instellen &gt; Lading opbouwen &gt; Ladingopbouwstrategieën**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="c1c38-117">Selecteer in het actievenster de optie **Lijst met klassen genereren** om er zeker van te zijn dat u beschikt over de meest recente versies van alle beschikbare klassen.</span><span class="sxs-lookup"><span data-stu-id="c1c38-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="c1c38-118">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c1c38-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c1c38-119">Voer een unieke naam in voor de strategie, selecteer de klasse voor de strategie voor ladingopbouw en voer een omschrijving in.</span><span class="sxs-lookup"><span data-stu-id="c1c38-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="c1c38-120">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c1c38-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c1c38-121">Selecteer **Parameters** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c1c38-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="c1c38-122">Selecteer op de pagina **De parameters van de belastingsbouwstrategie** de optie **Volumecapaciteit** in de lijst en voer vervolgens in het veld **Waarde** het percentage van de totale volumecapaciteit van de lading in dat moet worden toegepast voor de nieuwe strategie voor ladingopbouw.</span><span class="sxs-lookup"><span data-stu-id="c1c38-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="c1c38-123">Selecteer **Gewichtcapaciteit** in de lijst en voer vervolgens in het veld **Waarde** het percentage van de totale gewichtcapaciteit van de lading in dat moet worden toegepast voor de nieuwe strategie voor ladingopbouw.</span><span class="sxs-lookup"><span data-stu-id="c1c38-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="c1c38-124">Sluit de pagina **De parameters van de belastingsbouwstrategie**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="c1c38-125">Sluit de pagina **Ladingopbouwstrategieën**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="c1c38-126">U kunt nu de ladingopbouwstrategie toewijzen aan een sjabloon voor ladingopbouw.</span><span class="sxs-lookup"><span data-stu-id="c1c38-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="c1c38-127">U kunt deze ook rechtstreeks gebruiken in de workbench voor ladingplanning.</span><span class="sxs-lookup"><span data-stu-id="c1c38-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="c1c38-128">Een strategie voor ladingopbouw gebruiken in de workbench voor ladingopbouw</span><span class="sxs-lookup"><span data-stu-id="c1c38-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="c1c38-129">Ga naar **Transportbeheer &gt; Planning &gt; Workbench voor ladingopbouw**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="c1c38-130">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="c1c38-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="c1c38-131">Selecteer een strategie in het veld **Strategie voor ladingopbouw**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="c1c38-132">Als u een sjabloon voor ladingopbouw hebt gedefinieerd en hieraan de strategie voor ladingopbouw hebt toegewezen, selecteert u in het actievenster op het tabblad **Sjablonen beheren** de optie **Sjabloon toepassen**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="c1c38-133">Selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu **Sjabloon voor ladingopbouw toepassen** een sjabloon in het veld **Naam van ladingopbouwsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="c1c38-134">Selecteer in het sneltabblad **Volgorde laadsjablonen** een of meer [laadsjablonen](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="c1c38-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="c1c38-135">De workbench zal de lading proberen in te passen in deze typen containers, in de hier opgegeven volgorde.</span><span class="sxs-lookup"><span data-stu-id="c1c38-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="c1c38-136">Normaal gesproken moet u de kleinste containers boven aan de lijst plaatsen, zodat u zeker weet dat de kleinst mogelijke container als eerste wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="c1c38-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="c1c38-137">Selecteer **Ladingen voorstellen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c1c38-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="c1c38-138">Controleer de voorgestelde ladingen en de voorgestelde ladingsregels.</span><span class="sxs-lookup"><span data-stu-id="c1c38-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="c1c38-139">Selecteer in het actievenster de optie **Ladingen maken** om ladingen te maken die zijn gebaseerd op de brondocumentregels op het sneltabblad **Voorgestelde ladingregels**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="c1c38-140">Sluit de pagina **Workbench voor ladingopbouw**.</span><span class="sxs-lookup"><span data-stu-id="c1c38-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
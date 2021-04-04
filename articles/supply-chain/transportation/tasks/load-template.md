---
title: Sjablonen laden
description: In dit onderwerp wordt beschreven hoe u laadsjablonen instelt en hoe u een laadsjabloon koppelt aan een nieuwe lading.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 80004b5d22e1cf81c1ffa9f74c2c479e1561df72
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247209"
---
# <a name="load-templates"></a><span data-ttu-id="9b336-103">Sjablonen laden</span><span class="sxs-lookup"><span data-stu-id="9b336-103">Load templates</span></span>

<span data-ttu-id="9b336-104">Wanneer u een nieuwe lading maakt, kunt u een laadsjabloon toewijzen.</span><span class="sxs-lookup"><span data-stu-id="9b336-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="9b336-105">De laadsjabloon bevat informatie over apparatuur en over maateenheden zoals de hoogte, breedte, diepte en het volume van de lading.</span><span class="sxs-lookup"><span data-stu-id="9b336-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="9b336-106">In dit onderwerp wordt beschreven hoe u laadsjablonen instelt en hoe u een laadsjabloon koppelt aan een nieuwe lading.</span><span class="sxs-lookup"><span data-stu-id="9b336-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="9b336-107">Een laadsjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="9b336-107">Set up a load template</span></span>

1. <span data-ttu-id="9b336-108">Ga naar **Transportbeheer \> Instellen \> Lading opbouwen \> Laadsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="9b336-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="9b336-109">Selecteer in het actievenster **Nieuw** om een nieuwe sjabloon toe te voegen of **Bewerken** om een bestaande sjabloon te bewerken.</span><span class="sxs-lookup"><span data-stu-id="9b336-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="9b336-110">Stel in de rij voor de nieuwe of bestaande sjabloon de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="9b336-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="9b336-111">**Ladingssjabloon-id**: voer een unieke id in voor de laadsjabloon.</span><span class="sxs-lookup"><span data-stu-id="9b336-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="9b336-112">**Apparatuur**: selecteer de apparatuur die moet worden gebruikt om de lading te verzenden.</span><span class="sxs-lookup"><span data-stu-id="9b336-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="9b336-113">**Laadhoogte**, **Laadbreedte** en **Laaddiepte**: voer de afmetingen van de lading in.</span><span class="sxs-lookup"><span data-stu-id="9b336-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="9b336-114">**Maximaal toegestane ladingvolume** en **Maximaal toegestane ladinggewicht**: voer het maximaal toegestane volume en gewicht van de lading in.</span><span class="sxs-lookup"><span data-stu-id="9b336-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="9b336-115">**Maximaal toegestaan brutogewicht**: voer het maximaal toegestane brutogewicht van de lading in.</span><span class="sxs-lookup"><span data-stu-id="9b336-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="9b336-116">Het brutogewicht omvat zowel tarragewicht als laadgewicht.</span><span class="sxs-lookup"><span data-stu-id="9b336-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="9b336-117">**Maximumaantal vrachtstukken**: voer het maximumaantal vrachtstukken in dat de lading kan bevatten.</span><span class="sxs-lookup"><span data-stu-id="9b336-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="9b336-118">**Stapellading op vloer**: schakel dit selectievakje in als u laden op vloer wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9b336-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="9b336-119">Bij een vloerlading worden dozen binnen de container van vloer tot plafond en van wand tot wand gestapeld om de capaciteit te maximaliseren.</span><span class="sxs-lookup"><span data-stu-id="9b336-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="9b336-120">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="9b336-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="9b336-121">Een laadsjabloon aan een nieuwe lading koppelen</span><span class="sxs-lookup"><span data-stu-id="9b336-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="9b336-122">Ga naar **Transportbeheer \> Planning \> Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="9b336-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="9b336-123">Selecteer in het bovenste gedeelte van de pagina een van de volgende tabbladen, afhankelijk van het type brondocument waarvoor u een lading maakt: **Verzendingen**, **Verkoopregels**, **Transferregels** of **Inkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="9b336-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="9b336-124">Selecteer het specifieke document waarvoor u de lading wilt plannen.</span><span class="sxs-lookup"><span data-stu-id="9b336-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="9b336-125">Selecteer in het actievenster op het tabblad **Vraag en aanbod** in de groep **Toevoegen** de optie **Aan nieuwe lading**.</span><span class="sxs-lookup"><span data-stu-id="9b336-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="9b336-126">Selecteer in het dialoogvenster **Laadsjabloon** in het veld **Laadsjabloon-ID** de toe te passen sjabloon.</span><span class="sxs-lookup"><span data-stu-id="9b336-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="9b336-127">Selecteer **OK** om de sjabloon toe te passen.</span><span class="sxs-lookup"><span data-stu-id="9b336-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
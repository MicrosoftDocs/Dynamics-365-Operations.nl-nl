---
title: Artikel waar gebruikt
description: In dit onderwerp wordt uitgelegd hoe u een overzicht krijgt van waar een artikel wordt gebruikt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511108e689c10e27a42253d95b02e5394f9eb713
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652351"
---
# <a name="item-where-used"></a><span data-ttu-id="c48dc-103">Artikel waar gebruikt</span><span class="sxs-lookup"><span data-stu-id="c48dc-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c48dc-104">U kunt een berekening uitvoeren voor een specifiek artikel om een overzicht te krijgen van waar het artikel is gebruikt in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="c48dc-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="c48dc-105">De resultaten geven de context aan waarin het artikel tijdens de levensduur is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c48dc-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="c48dc-106">De pagina **Artikel waar gebruikt** kan worden geopend vanuit het hoofdmenu van Activabeheer en via de volgende pagina's:</span><span class="sxs-lookup"><span data-stu-id="c48dc-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="c48dc-107">Activumstuklijst</span><span class="sxs-lookup"><span data-stu-id="c48dc-107">Asset BOM</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="c48dc-108">Reserveonderdelen in de standaardinstellingen van het activatype</span><span class="sxs-lookup"><span data-stu-id="c48dc-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

- [<span data-ttu-id="c48dc-109">Artikelprognose voor prognose van standaardwaarden van onderhoudstaaktype</span><span class="sxs-lookup"><span data-stu-id="c48dc-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="c48dc-110">Onderhoudsprognose werkorder</span><span class="sxs-lookup"><span data-stu-id="c48dc-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="c48dc-111">Opdracht tot inkoop voor werkorder</span><span class="sxs-lookup"><span data-stu-id="c48dc-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="c48dc-112">Inkoop werkorder</span><span class="sxs-lookup"><span data-stu-id="c48dc-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="c48dc-113">Een berekening van het verbruik van een artikel uitvoeren</span><span class="sxs-lookup"><span data-stu-id="c48dc-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="c48dc-114">Klik op **Activabeheer** > **Query's** > **Artikel waar gebruikt** of selecteer de knop **Artikel waar gebruikt** op een van de eerder vermelde pagina's.</span><span class="sxs-lookup"><span data-stu-id="c48dc-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="c48dc-115">Selecteer in het dialoogvenster **Artikel waar gebruikt** het artikel waarvoor u de berekening wilt uitvoeren in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="c48dc-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="c48dc-116">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de artikelregels moeten zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="c48dc-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="c48dc-117">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activafoutregels voor een functionele locatie weergegeven op het hoogste niveau.</span><span class="sxs-lookup"><span data-stu-id="c48dc-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="c48dc-118">Daarom kan de relatie/hoeveelheid op een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="c48dc-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="c48dc-119">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle artikelregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="c48dc-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="c48dc-120">Selecteer Ja in het gedeelte **Opnemen** voor de wisselknoppen die u in de berekening wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="c48dc-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="c48dc-121">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="c48dc-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="c48dc-122">Selecteer op het tabblad **Artikel waar gebruikt** in de actievenstergroepen **Groeperen op** de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c48dc-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c48dc-123">De geselecteerde knoppen **Groeperen op** worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="c48dc-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c48dc-124">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="c48dc-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="c48dc-125">Als u dimensies wilt weergeven die gerelateerd zijn aan het artikel, klikt u op **Dimensies weergeven** en selecteert u de dimensies die u wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="c48dc-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="c48dc-126">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c48dc-126">Example</span></span>

<span data-ttu-id="c48dc-127">In de volgende afbeelding ziet u een voorbeeld van een berekening van het verbruik van een artikel voor artikelnummer 1000.</span><span class="sxs-lookup"><span data-stu-id="c48dc-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Voorbeeld van een berekening van het verbruik van een artikel](media/12-controlling-and-reporting.png)


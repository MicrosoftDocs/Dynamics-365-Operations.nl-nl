---
title: Controle van werkuren
description: In dit onderwerp wordt de controle van werkuren in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0d2f4e86b5dec84d4a24db6a4f9f9f16f6a765bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425337"
---
# <a name="work-hour-control"></a><span data-ttu-id="e0c78-103">Controle van werkuren</span><span class="sxs-lookup"><span data-stu-id="e0c78-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e0c78-104">In Activabeheer kunt u uren berekenen om een overzicht te krijgen van de werkelijke uren ten opzichte van budgeturen voor activa, functionele locaties of werkorders.</span><span class="sxs-lookup"><span data-stu-id="e0c78-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="e0c78-105">Werkelijke uren worden gebaseerd op geboekte transacties.</span><span class="sxs-lookup"><span data-stu-id="e0c78-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="e0c78-106">Controle van werkuren voor activa, functionele locaties en werkorders</span><span class="sxs-lookup"><span data-stu-id="e0c78-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="e0c78-107">De berekeningen voor activa, functionele locaties en werkorders zijn bijna identiek.</span><span class="sxs-lookup"><span data-stu-id="e0c78-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="e0c78-108">Het enige verschil is dat u voor activa en functionele locaties ook subactiva en sublocaties kunt opnemen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="e0c78-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="e0c78-109">De datum is de transactiedatum waarop de registratie is vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="e0c78-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="e0c78-110">Klik op **Activabeheer** > **Query's** > **Activa** > **Uurcontrole activa**, **Uurcontrole voor functionele locatie** of **Activabeheer** > **Query's** > **Werkorders** > **Uurcontrole voor werkorder**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="e0c78-111">Het betreffende dialoogvenster **Uurcontrole** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="e0c78-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="e0c78-112">Selecteer in het dialoogvenster **Uurcontrole activa** / **Uurcontrole voor functionele locatie** / **Uurcontrole voor werkorder** een periode die moet worden berekend in de velden **Begindatum** en **Einddatum**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="e0c78-113">Selecteer zo nodig een **financiële-dimensieset** die in de berekening moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="e0c78-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="e0c78-114">Selecteer Ja voor de wisselknop **Nul overslaan** als u geen resultaten wilt weergeven met nul uren.</span><span class="sxs-lookup"><span data-stu-id="e0c78-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="e0c78-115">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor uurcontrole zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="e0c78-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="e0c78-116">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een hiërarchie met meerdere niveaus voor functionele locaties hebt, worden alle uurcontroleregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="e0c78-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="e0c78-117">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle uurcontroleregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="e0c78-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="e0c78-118">Selecteer Ja voor de wisselknop **Subactiva opnemen** om kosten gerelateerd aan subactiva als afzonderlijke regels weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e0c78-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="e0c78-119">Als u de zoekopdracht wilt beperken, kunt u specifieke activa/functionele locaties/werkorders selecteren op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="e0c78-120">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="e0c78-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="e0c78-121">Klik op de pagina **Uurcontrole activa** op de knoppen **Groeperen op** om het vereiste detailniveau van de berekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e0c78-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="e0c78-122">De geselecteerde knoppen **Groeperen op** worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="e0c78-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="e0c78-123">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="e0c78-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="e0c78-124">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="e0c78-124">Example</span></span>

<span data-ttu-id="e0c78-125">In onderstaande schermafbeelding ziet u een voorbeeld van een berekening van een **Uurcontrole activa**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="e0c78-126">In het veld **Oorspronkelijk budget** worden budgeturen uit de werkorderprognose weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e0c78-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="e0c78-127">In het veld **Werkelijke uren** worden geboekte uren voor werkorders weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e0c78-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="e0c78-128">In het veld **Toegezegde uren** wordt het totale aantal uren weergegeven dat uw bedrijf heeft toegezegd met betrekking tot werkorders.</span><span class="sxs-lookup"><span data-stu-id="e0c78-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Voorbeeld van een berekening van uurcontrole activa](media/04-controlling-and-reporting.png)

<span data-ttu-id="e0c78-130">U kunt uren ook berekenen door meerdere activa te selecteren in **Alle activa** of **Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="e0c78-131">Vervolgens klikt u op de knop **Uurcontrole** op het sneltabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="e0c78-132">De geselecteerde activa worden automatisch ingevoegd in het veld **Activum** op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="e0c78-133">Klik op **OK** in het dialoogvenster **Uurcontrole activa** om de berekening voor de geselecteerde activa weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e0c78-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="e0c78-134">Dezelfde procedure kan worden uitgevoerd voor functionele locaties in **Alle functionele locaties** of **Actieve functionele locaties** en voor werkorders in **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="e0c78-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>



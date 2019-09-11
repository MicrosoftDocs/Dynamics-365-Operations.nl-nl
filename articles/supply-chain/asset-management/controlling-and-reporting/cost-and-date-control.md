---
title: Kosten- en datumcontrole
description: In dit onderwerp worden kosten- en datumcontrole in Activabeheer uitgelegd.
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
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918390"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="36cbe-103">Kosten- en datumcontrole</span><span class="sxs-lookup"><span data-stu-id="36cbe-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="36cbe-104">In Activabeheer kunt u kosten berekenen om een overzicht te krijgen van de werkelijke kosten ten opzichte van budgetkosten voor activa, functionele locaties en werkorders.</span><span class="sxs-lookup"><span data-stu-id="36cbe-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="36cbe-105">Werkelijke kosten worden gebaseerd op geboekte transacties.</span><span class="sxs-lookup"><span data-stu-id="36cbe-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="36cbe-106">U kunt ook een datumberekening maken als u geplande begin- en einddatums wilt vergelijken met de werkelijke begin- en einddatums van werkorders.</span><span class="sxs-lookup"><span data-stu-id="36cbe-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="36cbe-107">Kostenbeheer voor activa, functionele locaties en werkorders</span><span class="sxs-lookup"><span data-stu-id="36cbe-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="36cbe-108">De berekeningen voor activa, functionele locaties en werkorders zijn bijna identiek.</span><span class="sxs-lookup"><span data-stu-id="36cbe-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="36cbe-109">Het enige verschil is dat u voor activa en functionele locaties ook subactiva en sublocaties kunt opnemen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="36cbe-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="36cbe-110">De datum is de transactiedatum waarop de registratie is vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="36cbe-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="36cbe-111">Klik op **Activabeheer** > **Query's** > **Activa** > **Kostenbeheer activa**, **Kostenbeheer voor functionele locatie** of **Activabeheer** > **Query's** > **Werkorders** > **Kostenbeheer voor werkorder**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="36cbe-112">Selecteer in het dialoogvenster **Kostenbeheer activa** / **Kostenbeheer voor functionele locatie** / **Kostenbeheer voor werkorder** een periode die moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="36cbe-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="36cbe-113">Selecteer zo nodig een financiële-dimensieset die in de berekening moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="36cbe-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="36cbe-114">Selecteer Ja voor de wisselknop **Nul overslaan** als u geen resultaten wilt weergeven met nul kosten.</span><span class="sxs-lookup"><span data-stu-id="36cbe-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="36cbe-115">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor kostencontrole moeten zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="36cbe-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="36cbe-116">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een hiërarchie met meerdere niveaus voor functionele locaties hebt, worden alle kostenbeheerregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="36cbe-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="36cbe-117">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle kostenbeheerregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="36cbe-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="36cbe-118">Selecteer Ja voor de wisselknop **Openstaande toegezegde kosten weergeven** als u die kolom wilt opnemen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="36cbe-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="36cbe-119">Selecteer Ja voor de wisselknop **Subactiva opnemen** om kosten gerelateerd aan subactiva als afzonderlijke regels weer te geven.</span><span class="sxs-lookup"><span data-stu-id="36cbe-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="36cbe-120">Als u de zoekopdracht wilt beperken, kunt u specifieke activa/functionele locaties/werkorders selecteren op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="36cbe-121">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="36cbe-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="36cbe-122">In de volgende afbeelding ziet u een voorbeeld van het dialoogvenster **Kostenbeheer activa**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![Figuur 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="36cbe-124">Klik in de actievenstergroepen **Groeperen op** op de pagina **Kostenbeheer activa** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="36cbe-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="36cbe-125">De geselecteerde knoppen in het actievenster zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="36cbe-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="36cbe-126">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="36cbe-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="36cbe-127">In de volgende afbeelding ziet u een voorbeeld van berekeningsresultaten in **Kostenbeheer activa**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![Figuur 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="36cbe-129">U kunt kosten ook berekenen door meerdere activa te selecteren in **Alle activa** of **Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="36cbe-130">Vervolgens klikt u op de knop **Kostenbeheer** op het tabblad **Algemeen**. In het dialoogvenster **Kostenbeheer activa** worden de geselecteerde activa automatisch ingevoegd in het veld **Activum** op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="36cbe-131">Klik op **OK** om een kostenberekening voor de geselecteerde activa weer te geven.</span><span class="sxs-lookup"><span data-stu-id="36cbe-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="36cbe-132">Dezelfde procedure kan worden uitgevoerd voor functionele locaties in **Alle functionele locaties** of **Actieve functionele locaties** en voor werkorders in **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="36cbe-133">In het veld **Oorspronkelijk budget** worden budgetkosten uit de werkorderprognose weergegeven.</span><span class="sxs-lookup"><span data-stu-id="36cbe-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="36cbe-134">In het veld **Toegezegde kosten** wordt het totale bedrag weergegeven van de onkosten die de rechtspersoon zelf heeft toegezegd te betalen.</span><span class="sxs-lookup"><span data-stu-id="36cbe-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="36cbe-135">Het veld **Openstaande toegezegde kosten** bevat de toezeggingen die moeten worden betaald voor artikelen, uren en services die u hebt besteld of ontvangen, maar nog niet hebt betaald.</span><span class="sxs-lookup"><span data-stu-id="36cbe-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="36cbe-136">Wanneer alle verbruiksregistraties zijn geboekt, worden de gerelateerde kosten in het veld **Werkelijke kosten** opgenomen.</span><span class="sxs-lookup"><span data-stu-id="36cbe-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="36cbe-137">Datumbeheer werkorder</span><span class="sxs-lookup"><span data-stu-id="36cbe-137">Work order date control</span></span>

<span data-ttu-id="36cbe-138">Gebruik deze pagina om een overzicht te krijgen van verwachte begin- en einddatums in vergelijking met de werkelijke begin- en einddatums van werkorders.</span><span class="sxs-lookup"><span data-stu-id="36cbe-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="36cbe-139">Klik op **Activabeheer** > **Query's** > **Werkorders** > **Datumbeheer werkorder**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="36cbe-140">Klik op **Berekenen**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="36cbe-141">Selecteer een functionele locatie in het veld **Functionele locatie**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="36cbe-142">Voeg in de velden **Begindatum** en **Einddatum** de periode in waarvoor u de berekening wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="36cbe-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="36cbe-143">Alle werkorders met een verwachte begindatum in de periode worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="36cbe-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="36cbe-144">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-144">Click **OK**.</span></span>

6. <span data-ttu-id="36cbe-145">Klik in de actievenstergroepen **Groeperen op** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="36cbe-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="36cbe-146">De geselecteerde knoppen in het actievenster zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="36cbe-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="36cbe-147">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="36cbe-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="36cbe-148">In de volgende afbeelding ziet u een voorbeeld van berekeningsresultaten in **Datumbeheer werkorder**.</span><span class="sxs-lookup"><span data-stu-id="36cbe-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![Figuur 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="36cbe-150">Het veld **Gemiddelde beginvertraging** geeft het verschil in dagen aan tussen de geplande begindatum voor een werkorder vergeleken met de werkelijke begindatum.</span><span class="sxs-lookup"><span data-stu-id="36cbe-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="36cbe-151">Als de werkelijke begindatum bijvoorbeeld twee dagen vóór de geplande begindatum valt, wordt in dit veld de waarde -2 weergegeven.</span><span class="sxs-lookup"><span data-stu-id="36cbe-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="36cbe-152">Het veld **Gemiddelde eindvertraging** geeft het verschil in dagen aan tussen de geplande einddatum voor een werkorder vergeleken met de werkelijke einddatum.</span><span class="sxs-lookup"><span data-stu-id="36cbe-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="36cbe-153">Als de werkelijke einddatum bijvoorbeeld drie dagen na de geplande einddatum valt, wordt in dit veld de waarde 3 weergegeven.</span><span class="sxs-lookup"><span data-stu-id="36cbe-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="36cbe-154">In de velden **Voorvallen** wordt aangegeven hoe vaak afwijkingen plaatsvinden ten aanzien van de geplande en werkelijke begindatum en geplande en werkelijke einddatum van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="36cbe-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>


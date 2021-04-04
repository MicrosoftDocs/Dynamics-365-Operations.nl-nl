---
title: Kosten- en datumcontrole
description: In dit onderwerp worden kosten- en datumcontrole in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7072cb8c3f76be5869239aa0acab6cf3ff268e32
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253777"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="c0bcc-103">Kosten- en datumcontrole</span><span class="sxs-lookup"><span data-stu-id="c0bcc-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c0bcc-104">In Activabeheer kunt u kosten berekenen om een overzicht te krijgen van de werkelijke kosten ten opzichte van budgetkosten voor activa, functionele locaties en werkorders.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="c0bcc-105">Werkelijke kosten worden gebaseerd op geboekte transacties.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="c0bcc-106">U kunt ook een datumberekening maken als u geplande begin- en einddatums wilt vergelijken met de werkelijke begin- en einddatums van werkorders.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="c0bcc-107">Kostenbeheer voor activa, functionele locaties en werkorders</span><span class="sxs-lookup"><span data-stu-id="c0bcc-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="c0bcc-108">De berekeningen voor activa, functionele locaties en werkorders zijn bijna identiek.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="c0bcc-109">Het enige verschil is dat u voor activa en functionele locaties ook subactiva en sublocaties kunt opnemen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="c0bcc-110">De datum is de transactiedatum waarop de registratie is vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="c0bcc-111">Klik op **Activabeheer** > **Query's** > **Activa** > **Kostenbeheer activa**, **Kostenbeheer voor functionele locatie** of **Activabeheer** > **Query's** > **Werkorders** > **Kostenbeheer voor werkorder**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="c0bcc-112">Selecteer in het dialoogvenster **Kostenbeheer activa** / **Kostenbeheer voor functionele locatie** / **Kostenbeheer voor werkorder** een tijdbereik dat moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="c0bcc-113">Selecteer zo nodig een financiële-dimensieset die in de berekening moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="c0bcc-114">Selecteer Ja voor de wisselknop **Nul overslaan** als u geen resultaten wilt weergeven met nul kosten.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="c0bcc-115">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor kostencontrole moeten zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="c0bcc-116">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een hiërarchie met meerdere niveaus voor functionele locaties hebt, worden alle kostenbeheerregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="c0bcc-117">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle kostenbeheerregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="c0bcc-118">Selecteer Ja voor de wisselknop **Openstaande toegezegde kosten weergeven** als u die kolom wilt opnemen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="c0bcc-119">Selecteer Ja voor de wisselknop **Subactiva opnemen** om kosten gerelateerd aan subactiva als afzonderlijke regels weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="c0bcc-120">Als u de zoekopdracht wilt beperken, kunt u specifieke activa/functionele locaties/werkorders selecteren op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="c0bcc-121">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="c0bcc-122">In de volgende afbeelding ziet u een voorbeeld van het dialoogvenster **Kostenbeheer activa**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Dialoogvenster Kostenbeheer activa](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="c0bcc-124">Klik op de pagina **Kostenbeheer activa** op de knoppen **Groeperen op** om het vereiste detailniveau van de berekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c0bcc-125">De geselecteerde knoppen **Groeperen op** worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c0bcc-126">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="c0bcc-127">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c0bcc-127">Example</span></span>

<span data-ttu-id="c0bcc-128">In de onderstaande schermopname ziet u een voorbeeld van berekeningsresultaten in **Kostenbeheer activa**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="c0bcc-129">In het veld **Oorspronkelijk budget** worden budgetkosten uit de werkorderprognose weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="c0bcc-130">In het veld **Toegezegde kosten** wordt het totale bedrag weergegeven van de onkosten die de rechtspersoon zelf heeft toegezegd te betalen.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="c0bcc-131">Het veld **Openstaande toegezegde kosten** bevat de toezeggingen die moeten worden betaald voor artikelen, uren en services die u hebt besteld of ontvangen, maar nog niet hebt betaald.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="c0bcc-132">Het veld **Werkelijke kosten** bevat gerelateerde kosten nadat alle verbruiksregistraties zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Voorbeeld van berekeningsresultaten in Kostenbeheer activa](media/02-controlling-and-reporting.png)

<span data-ttu-id="c0bcc-134">U kunt kosten ook berekenen door meerdere activa te selecteren in **Alle activa** of **Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="c0bcc-135">Vervolgens klikt u op de knop **Kostenbeheer** op het tabblad **Algemeen**. In het dialoogvenster **Kostenbeheer activa** worden de geselecteerde activa automatisch ingevoegd in het veld **Activum** op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="c0bcc-136">Klik op **OK** om een kostenberekening voor de geselecteerde activa weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="c0bcc-137">Dezelfde procedure kan worden uitgevoerd voor functionele locaties in **Alle functionele locaties** of **Actieve functionele locaties** en voor werkorders in **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="c0bcc-138">Datumbeheer werkorder</span><span class="sxs-lookup"><span data-stu-id="c0bcc-138">Work order date control</span></span>

<span data-ttu-id="c0bcc-139">Gebruik deze pagina om een overzicht te krijgen van verwachte begin- en einddatums in vergelijking met de werkelijke begin- en einddatums van werkorders.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="c0bcc-140">Klik op **Activabeheer** > **Query's** > **Werkorders** > **Datumbeheer werkorder**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="c0bcc-141">Klik op **Berekenen**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="c0bcc-142">Selecteer een functionele locatie in het veld **Functionele locatie**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="c0bcc-143">Voeg in de velden **Begindatum** en **Einddatum** het bereik in waarvoor u de berekening wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="c0bcc-144">Alle werkorders met een verwachte begindatum in het bereik worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="c0bcc-145">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-145">Click **OK**.</span></span>

6. <span data-ttu-id="c0bcc-146">Klik op de knoppen **Groeperen op** om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c0bcc-147">De geselecteerde knoppen **Groeperen op** worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c0bcc-148">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="c0bcc-149">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c0bcc-149">Example</span></span>

<span data-ttu-id="c0bcc-150">In de volgende schermopname ziet u een voorbeeld van berekeningsresultaten in **Datumbeheer werkorder**.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="c0bcc-151">Het veld **Gemiddelde beginvertraging** geeft het verschil in dagen aan tussen de geplande begindatum voor een werkorder vergeleken met de werkelijke begindatum.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="c0bcc-152">Als de werkelijke begindatum bijvoorbeeld twee dagen vóór de geplande begindatum valt, wordt in dit veld de waarde -2 weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="c0bcc-153">Het veld **Gemiddelde eindvertraging** geeft het verschil in dagen aan tussen de geplande einddatum voor een werkorder vergeleken met de werkelijke einddatum.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="c0bcc-154">Als de werkelijke einddatum bijvoorbeeld drie dagen na de geplande einddatum valt, wordt in dit veld de waarde 3 weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="c0bcc-155">In de velden **Voorvallen** wordt aangegeven hoe vaak afwijkingen plaatsvinden ten aanzien van de geplande en werkelijke begindatum en geplande en werkelijke einddatum van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="c0bcc-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Voorbeeld van berekeningsresultaten in Datumbeheer werkorder](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
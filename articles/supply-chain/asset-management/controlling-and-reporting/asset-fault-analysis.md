---
title: Foutanalyse activum
description: In dit onderwerp worden foutanalyses voor activa in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 674e10b94711b00e526af4af0e0c0afddd05e62c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022370"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="c65b5-103">Foutanalyse activum</span><span class="sxs-lookup"><span data-stu-id="c65b5-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c65b5-104">In Activabeheer kunt u foutregistraties voor activa analyseren om een overzicht weer te geven van het totale aantal fouten dat tijdens een bepaalde periode is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="c65b5-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="c65b5-105">Foutregistraties kunnen vanuit verschillende perspectieven worden geanalyseerd, bijvoorbeeld met de focus op activa, activatypen, functionele locaties, foutsymptomen of fouttypen.</span><span class="sxs-lookup"><span data-stu-id="c65b5-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="c65b5-106">Klik op **Activabeheer** > **Query's** > **Activafout** > **Foutanalyse activum**.</span><span class="sxs-lookup"><span data-stu-id="c65b5-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="c65b5-107">In het dialoogvenster **Berekening van foutanalyse voor activa** kunt u het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de activafoutregels met betrekking tot functionele locaties moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="c65b5-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="c65b5-108">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activafoutregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="c65b5-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="c65b5-109">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle activafoutregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="c65b5-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="c65b5-110">Als u de zoekopdracht wilt beperken, kunt u specifieke activa, foutdatums, foutoorzaken en probleemoplossingen selecteren op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="c65b5-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="c65b5-111">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="c65b5-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="c65b5-112">Klik op het tabblad **Foutanalyse activum** op een of meer knoppen **Groeperen op** om het gewenste detailniveau weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c65b5-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="c65b5-113">Geactiveerde knoppen zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="c65b5-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="c65b5-114">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="c65b5-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="c65b5-115">Klik op **Berekeningen bijwerken** om uw selecties op het scherm weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c65b5-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="c65b5-116">Telkens wanneer u een knop **Groeperen op** activeert of deactiveert, moet u niet vergeten op de knop **Berekeningen bijwerken** te klikken.</span><span class="sxs-lookup"><span data-stu-id="c65b5-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="c65b5-117">Dit is vereist omdat een grote hoeveelheid gegevens wordt verwerkt terwijl u de foutwaarschijnlijkheid opnieuw berekent.</span><span class="sxs-lookup"><span data-stu-id="c65b5-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="c65b5-118">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="c65b5-118">Examples</span></span>

<span data-ttu-id="c65b5-119">Er zijn veel manieren om foutregistraties te analyseren.</span><span class="sxs-lookup"><span data-stu-id="c65b5-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="c65b5-120">Deze sectie bevat vijf voorbeelden van hoe verschillende gegevensselecties meer inzicht en details kunnen bieden bij het analyseren van foutregistraties voor activa.</span><span class="sxs-lookup"><span data-stu-id="c65b5-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="c65b5-121">Groeperen op symptomen</span><span class="sxs-lookup"><span data-stu-id="c65b5-121">Group by symptoms</span></span>

<span data-ttu-id="c65b5-122">In de onderstaande schermafbeelding is alleen de knop **Symptoom** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="c65b5-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="c65b5-123">Er zijn foutregistraties uitgevoerd voor drie foutsymptomen: Luchtlek, Gesprongen zekering en Vastgelopen apparatuur.</span><span class="sxs-lookup"><span data-stu-id="c65b5-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="c65b5-124">In de kolom **Waarschijnlijkheidspercentage** zijn alle percentages bij elkaar 100%.</span><span class="sxs-lookup"><span data-stu-id="c65b5-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="c65b5-125">De waarschijnlijkheid is gebaseerd op alle **symptoomregistraties** in deze foutanalyse.</span><span class="sxs-lookup"><span data-stu-id="c65b5-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Figuur 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="c65b5-127">Groeperen op symptomen en tijdsperiode</span><span class="sxs-lookup"><span data-stu-id="c65b5-127">Group by symptoms and time period</span></span>

<span data-ttu-id="c65b5-128">In de onderstaande schermafbeelding worden **Jaar** en **Maand** toegevoegd om aan te geven hoe u tijdens een geselecteerde periode foutregistraties kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="c65b5-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="c65b5-129">De foutsymptomen worden nu weergegeven als registraties per jaar/maand.</span><span class="sxs-lookup"><span data-stu-id="c65b5-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="c65b5-130">Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor elke maand optelt, komt u uit op 100%.</span><span class="sxs-lookup"><span data-stu-id="c65b5-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="c65b5-131">De waarschijnlijkheid is gebaseerd op de **symptoomregistraties** in deze foutanalyse.</span><span class="sxs-lookup"><span data-stu-id="c65b5-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="c65b5-132">Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een foutsymptoom om nader te onderzoeken of het aantal registraties voor dit foutsymptoom kan worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="c65b5-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figuur 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="c65b5-134">Groeperen op meerdere symptomen en activa</span><span class="sxs-lookup"><span data-stu-id="c65b5-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="c65b5-135">De combinatie van activa en een activumtype wordt gebruikt als basis voor de berekeningen die worden weergegeven in de drie onderstaande schermafbeeldingen, die steeds gedetailleerder worden.</span><span class="sxs-lookup"><span data-stu-id="c65b5-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="c65b5-136">Over het algemeen geldt dat de knoppen in de actievenstergroepen **Groeperen op datum**, **Groeperen op activum**, **Groeperen op functionele locatie** en de knop **Fout** (fout-id) periodes of activarelaties bevatten.</span><span class="sxs-lookup"><span data-stu-id="c65b5-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="c65b5-137">De knoppen **Symptoom**, **Gebied**, **Type**, **Oorzaak** en **Oplossing** zijn categorisaties die in foutbeheer worden gebruikt om foutregistraties te analyseren en probleemgebieden te identificeren.</span><span class="sxs-lookup"><span data-stu-id="c65b5-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="c65b5-138">**Groeperen op symptoom, activum en activatype**</span><span class="sxs-lookup"><span data-stu-id="c65b5-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="c65b5-139">In de onderstaande schermafbeelding zijn **Activum** en **Activumtype** toegevoegd om meer details te bieden over foutregistraties.</span><span class="sxs-lookup"><span data-stu-id="c65b5-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="c65b5-140">De foutsymptomen zijn nu opgesplitst in combinaties van **Activum** / **Activumtype** / **Symptoom**.</span><span class="sxs-lookup"><span data-stu-id="c65b5-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="c65b5-141">Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor de combinatie van **Activum** / **Activumtype** / **Symptoom** optelt, komt u uit op 100%.</span><span class="sxs-lookup"><span data-stu-id="c65b5-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="c65b5-142">De waarschijnlijkheid is gebaseerd op **symptoomregistraties** in deze foutanalyse.</span><span class="sxs-lookup"><span data-stu-id="c65b5-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="c65b5-143">Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een foutsymptoom om nader te onderzoeken of het aantal registraties voor dit foutsymptoom kan worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="c65b5-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figuur 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="c65b5-145">**Groeperen op twee symptomen, activum en activatype**</span><span class="sxs-lookup"><span data-stu-id="c65b5-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="c65b5-146">In de onderstaande schermafbeelding is **Gebied** toegevoegd aan **Symptoom**, **Activum** en **Activumtype** om meer details te bieden over foutregistraties.</span><span class="sxs-lookup"><span data-stu-id="c65b5-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="c65b5-147">Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor de combinatie van **Activum** / **Activumtype** / **Symptoom** voor een activum optelt, komt u uit op 100%.</span><span class="sxs-lookup"><span data-stu-id="c65b5-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="c65b5-148">De waarschijnlijkheid is gebaseerd op de combinatie van **Symptoom** en **Gebied** in deze foutanalyse.</span><span class="sxs-lookup"><span data-stu-id="c65b5-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="c65b5-149">Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een foutgebied om nader te onderzoeken of het aantal registraties voor dit foutgebied kan worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="c65b5-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Figuur 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="c65b5-151">**Groeperen op drie symptomen, activum en activatype**</span><span class="sxs-lookup"><span data-stu-id="c65b5-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="c65b5-152">In de onderstaande schermafbeelding is **Type** toegevoegd en de meest gedetailleerde berekening wordt in dit voorbeeld weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c65b5-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="c65b5-153">Als u in de kolom **Waarschijnlijkheidspercentage** alle percentages voor de combinatie van **Activum** / **Activumtype** / **Symptoom** voor een activum optelt, komt u uit op 100%.</span><span class="sxs-lookup"><span data-stu-id="c65b5-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="c65b5-154">De waarschijnlijkheid is gebaseerd op de combinatie van **Symptoom**, **Gebied** en **Type** in deze foutanalyse.</span><span class="sxs-lookup"><span data-stu-id="c65b5-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="c65b5-155">Als u een groot aantal regels voor een activum hebt, maar een groot percentage op een regel staat, is dit een indicatie van een fouttype om nader te onderzoeken of het aantal registraties voor dit fouttype kan worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="c65b5-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Figuur 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="c65b5-157">Voor een overzicht van alle gemaakte foutregistraties voor werkorders en onderhoudsverzoeken klikt u op **Activabeheer** > **Query's** > **Activafout** > **Activafouten**.</span><span class="sxs-lookup"><span data-stu-id="c65b5-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="c65b5-158">Selecteer op de pagina **Activafouten** een activumfoutregistratie en vouw het deelvenster **Verwante informatie** uit om informatie over de bijbehorende werkorder of het bijbehorende onderhoudsverzoek weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c65b5-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>


---
title: Verbruiksrapporten maken
description: In dit onderwerp wordt uitgelegd hoe u rapporten over verbruik maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216431"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="e651a-103">Verbruiksrapporten maken</span><span class="sxs-lookup"><span data-stu-id="e651a-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e651a-104">Wanneer u verbruiksregistraties voor werkorders in Activabeheer hebt gemaakt en geboekt, zijn er twee rapporten beschikbaar om verbruiksgegevens weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e651a-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="e651a-105">Het rapport Activaverbruik</span><span class="sxs-lookup"><span data-stu-id="e651a-105">Asset consumption report</span></span>

<span data-ttu-id="e651a-106">Wanneer u verbruik voor werkorders hebt geboekt, kunt u een verbruiksrapport voor activa afdrukken.</span><span class="sxs-lookup"><span data-stu-id="e651a-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="e651a-107">In het rapport worden uren, uurkosten, artikelkosten en geboekte onkosten voor activa weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e651a-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="e651a-108">Klik op **Activabeheer** > **Rapporten** > **Activa** > **Activaverbruik**.</span><span class="sxs-lookup"><span data-stu-id="e651a-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="e651a-109">Selecteer in het dialoogvenster **Activaverbruik** de parameters en het detailniveau dat u wilt zien door **Ja** te selecteren voor de relevante wisselknoppen en een niveau voor functionele locaties in de sectie **Weergeven** in te voegen.</span><span class="sxs-lookup"><span data-stu-id="e651a-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="e651a-110">U kunt het veld **Niveaus** gebruiken om aan te geven hoe gedetailleerd de regels voor activa moeten zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="e651a-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="e651a-111">Als u bijvoorbeeld het getal 1 invoert in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle activa voor een functionele locatie weergegeven op het hoogste niveau. Daarom kan een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="e651a-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="e651a-112">Als u het getal 0 in het veld **Niveaus** invoert, wordt er een gedetailleerd resultaat met alle activa weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="e651a-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="e651a-113">Selecteer **Ja** voor de wisselknop **Som van alle subactiva** als u de totalen voor elk subactivum in het rapport wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="e651a-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="e651a-114">Selecteer een datuminterval in de sectie **Datums**.</span><span class="sxs-lookup"><span data-stu-id="e651a-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="e651a-115">Geef op op het sneltabblad **Bestemming** op of u het rapport op het scherm wilt weergeven, wilt afdrukken of wilt opslaan als bestand of e-mailbericht.</span><span class="sxs-lookup"><span data-stu-id="e651a-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="e651a-116">U kunt zo nodig specifieke activa selecteren die in het rapport moeten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e651a-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="e651a-117">Klik op het sneltabblad **Op te nemen records** op **Filter** en voeg de activa toe die u in het rapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="e651a-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="e651a-118">Klik op **OK** om het rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="e651a-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="e651a-119">Het rapport Werkorderverbruik</span><span class="sxs-lookup"><span data-stu-id="e651a-119">Work order consumption report</span></span>

<span data-ttu-id="e651a-120">Wanneer u verbruik voor werkorders hebt geboekt, kunt u een verbruiksrapport voor werkorders afdrukken.</span><span class="sxs-lookup"><span data-stu-id="e651a-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="e651a-121">In het rapport worden uren, uurkosten, artikelkosten en geboekte onkosten voor werkorders weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e651a-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="e651a-122">Klik op **Activabeheer** > **Rapporten** > **Werkorders** > **Werkorderverbruik**.</span><span class="sxs-lookup"><span data-stu-id="e651a-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="e651a-123">Selecteer in het dialoogvenster **Werkorderverbruik** de parameters die u in het rapport wilt opnemen door **Ja** te selecteren voor de relevante wisselknoppen in de sectie **Weergeven**.</span><span class="sxs-lookup"><span data-stu-id="e651a-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="e651a-124">Selecteer een datuminterval in de sectie **Datums**.</span><span class="sxs-lookup"><span data-stu-id="e651a-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="e651a-125">Geef op op het sneltabblad **Bestemming** op of u het rapport op het scherm wilt weergeven, wilt afdrukken of wilt opslaan als bestand of e-mailbericht.</span><span class="sxs-lookup"><span data-stu-id="e651a-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="e651a-126">U kunt zo nodig specifieke werkorders selecteren die in het rapport moeten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e651a-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="e651a-127">Klik op het sneltabblad **Op te nemen records** op **Filter** en voeg de werkorders toe die u in het rapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="e651a-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="e651a-128">Klik op **OK** om het rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="e651a-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="e651a-129">U kunt ook een [werkorderrapport](../work-orders/work-order-report.md) genereren dat meer werkordergegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="e651a-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>


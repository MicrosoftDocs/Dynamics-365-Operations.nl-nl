---
title: Capaciteitsbelasting berekenen
description: In dit onderwerp wordt uitgelegd hoe u de capaciteitsbelasting berekent in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a9b235ecedf3399c79ee081a9fe7e2423045fa5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260053"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="a7d1c-103">Capaciteitsbelasting berekenen</span><span class="sxs-lookup"><span data-stu-id="a7d1c-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="a7d1c-104">In Activabeheer kunt u de capaciteitsbelasting berekenen voor:</span><span class="sxs-lookup"><span data-stu-id="a7d1c-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="a7d1c-105">onderhoudsschemaregels</span><span class="sxs-lookup"><span data-stu-id="a7d1c-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="a7d1c-106">werkorders die nog niet zijn gepland</span><span class="sxs-lookup"><span data-stu-id="a7d1c-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="a7d1c-107">geplande werkorders</span><span class="sxs-lookup"><span data-stu-id="a7d1c-107">scheduled work orders</span></span>

<span data-ttu-id="a7d1c-108">Dit is handig als u een overzicht wilt weergeven van de verwachte capaciteitsbelasting voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="a7d1c-109">De berekening van de capaciteitsbelasting kan worden uitgevoerd voor alle activa of geselecteerde activa.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="a7d1c-110">U kunt ook een berekening uitvoeren voor activiteiten voor uitvaltijd of werkordergroepen.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="a7d1c-111">Klik op **Activabeheer** > **Query's** > **Capaciteitsbelasting** of **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** / **Actieve werkordergroepen** > selecteer de werkordergroep in de lijst > de knop **Capaciteitsbelasting** of **Activabeheer** > **Algemeen** > **Activiteiten voor uitvaltijd voor onderhoud** > **Alle activiteiten voor uitvaltijd voor onderhoud** / **Actieve activiteiten voor uitvaltijd voor onderhoud** > selecteer de activiteit voor uitvaltijd voor onderhoud in de lijst > de knop **Capaciteitsbelasting**.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="a7d1c-112">Selecteer in het dialoogvenster **Capaciteitsbelasting berekenen** een periode voor de berekening in de velden **Begindatum/-tijd** en **Einddatum/-tijd**.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="a7d1c-113">Selecteer Ja voor de wisselknop **Onderhoudsschema opnemen** als u onderhoudsschemaregels wilt opnemen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="a7d1c-114">Selecteer Ja voor de wisselknop **Werkorder opnemen** als u werkordertaken wilt opnemen in de berekening.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="a7d1c-115">Gebruik het veld **Niveau** om aan te geven hoe gedetailleerd u de capaciteitsbelastingsregels wilt berekenen met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="a7d1c-116">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsschemaregels en werkorders voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="a7d1c-117">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle onderhoudsschemaregels en alle werkorders weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="a7d1c-118">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="a7d1c-119">Klik in de groepen **Groeperen op...** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="a7d1c-120">In de onderstaande schermopname worden de geselecteerde knoppen **Groeperen op** in blauwe kleur gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="a7d1c-121">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-121">Click on a button to activate or deactivate it.</span></span>

    ![Figuur 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="a7d1c-123">Zie [Capaciteitsbelasting voor geplande werkorders berekenen](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md) als u zich alleen wilt richten op capaciteitsplanning voor geplande werkorders.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
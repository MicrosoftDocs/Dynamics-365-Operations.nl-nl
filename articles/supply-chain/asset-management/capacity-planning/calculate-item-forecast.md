---
title: Artikelprognose berekenen
description: In dit onderwerp wordt uitgelegd hoe u een artikelprognose berekent in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f8f38ac7bfb270f648cd561da50ee5477721ab47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425560"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="d6b42-103">Artikelprognose berekenen</span><span class="sxs-lookup"><span data-stu-id="d6b42-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d6b42-104">Net zoals u de capaciteitsbelasting kunt berekenen, zoals in de vorige sectie is beschreven, kunt u ook artikelprognoses berekenen voor:</span><span class="sxs-lookup"><span data-stu-id="d6b42-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="d6b42-105">onderhoudsschemaregels</span><span class="sxs-lookup"><span data-stu-id="d6b42-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="d6b42-106">werkorders die nog niet zijn gepland</span><span class="sxs-lookup"><span data-stu-id="d6b42-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="d6b42-107">geplande werkorders</span><span class="sxs-lookup"><span data-stu-id="d6b42-107">scheduled work orders</span></span>

<span data-ttu-id="d6b42-108">Dit is handig als u een overzicht wilt weergeven van het verwachte artikelverbruik (reserveonderdelen en andere artikelen die nodig zijn voor het voltooien van werkorders) gedurende een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="d6b42-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="d6b42-109">De berekening van een artikelprognose kan worden uitgevoerd voor alle activa of geselecteerde activa.</span><span class="sxs-lookup"><span data-stu-id="d6b42-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="d6b42-110">U kunt ook een berekening uitvoeren voor een activiteit voor uitvaltijd voor onderhoud activiteit (**Alle activiteiten voor uitvaltijd voor onderhoud** of **Actieve activiteiten voor uitvaltijd voor onderhoud**) of een werkordergroep (**Alle werkordergroepen** of **Actieve werkordergroepen**).</span><span class="sxs-lookup"><span data-stu-id="d6b42-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="d6b42-111">Klik op **Activabeheer** > **Query's** > **Artikelprognose** of **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** / **Actieve werkordergroepen** > selecteer de werkordergroep in de lijst > de knop **Artikelprognose** of **Activabeheer** > **Algemeen** > **Activiteiten voor uitvaltijd voor onderhoud** > **Alle activiteiten voor uitvaltijd voor onderhoud** / **Actieve activiteiten voor uitvaltijd voor onderhoud** > selecteer de activiteit voor uitvaltijd voor onderhoud in de lijst > de knop **Artikelprognose**.</span><span class="sxs-lookup"><span data-stu-id="d6b42-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="d6b42-112">Selecteer in het dialoogvenster **Artikelprognose berekenen** een periode voor de berekening in de velden **Begindatum/-tijd** en **Einddatum/-tijd**.</span><span class="sxs-lookup"><span data-stu-id="d6b42-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="d6b42-113">Selecteer Ja voor de wisselknop **Onderhoudsschema opnemen** als u onderhoudsschemaregels wilt opnemen in de prognoseberekening.</span><span class="sxs-lookup"><span data-stu-id="d6b42-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="d6b42-114">Selecteer Ja voor de wisselknop **Werkorder opnemen** als u werkordertaken wilt opnemen in de prognoseberekening.</span><span class="sxs-lookup"><span data-stu-id="d6b42-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="d6b42-115">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de prognoseregels moeten zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="d6b42-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="d6b42-116">Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsschemaregels en werkorders voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="d6b42-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="d6b42-117">Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle onderhoudsschemaregels en alle werkorders weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="d6b42-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="d6b42-118">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="d6b42-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="d6b42-119">Klik in de groepen **Groeperen op...** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d6b42-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d6b42-120">In de onderstaande schermopname worden de geselecteerde knoppen **Groeperen op** in blauwe kleur gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="d6b42-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="d6b42-121">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="d6b42-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="d6b42-122">Klik op de knop **Dimensies weergeven** als u de product-, opslag- of traceringsdimensies wilt weergeven die betrekking hebben op de artikelen.</span><span class="sxs-lookup"><span data-stu-id="d6b42-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="d6b42-123">Schakel de relevante selectievakjes in en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6b42-123">Select the relevant check boxes, and click **OK**.</span></span>

![Figuur 1](media/02-capacity-planning.png)

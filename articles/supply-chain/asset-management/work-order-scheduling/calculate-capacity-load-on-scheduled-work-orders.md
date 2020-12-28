---
title: Capaciteitsbelasting voor geplande werkorders berekenen
description: In dit onderwerp wordt uitgelegd hoe u capaciteitsbelasting kunt berekenen voor geplande werkorders in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
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
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425581"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="dd674-103">Capaciteitsbelasting voor geplande werkorders berekenen</span><span class="sxs-lookup"><span data-stu-id="dd674-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="dd674-104">U kunt de capaciteitsbelasting voor geplande werkorders berekenen om een overzicht te krijgen van de werkbelasting van resources voor een specifieke periode.</span><span class="sxs-lookup"><span data-stu-id="dd674-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="dd674-105">Er kunnen berekeningen worden uitgevoerd voor de volgende resources: onderhoudsmedewerkers, medewerkersgroepen, hulpmiddelen en activa.</span><span class="sxs-lookup"><span data-stu-id="dd674-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="dd674-106">Klik op **Activabeheer** > **Query's** > **Planning** > **Capaciteitsbelasting**.</span><span class="sxs-lookup"><span data-stu-id="dd674-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="dd674-107">Selecteer in het dialoogvenster **Capaciteitsbelasting berekenen** in het veld **Weergeven** het belastingtype dat u wilt berekenen: **Capaciteit**, **Gereserveerd** of **Rest**.</span><span class="sxs-lookup"><span data-stu-id="dd674-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="dd674-108">Selecteer **Ja** voor de wisselknop **Nul overslaan** als u geen resultaten voor nul wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="dd674-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="dd674-109">Selecteer de resourcetypen waarvoor u de capaciteitsbelasting wilt berekenen door **Ja** te selecteren voor de relevante wisselknoppen: **Medewerker**, **Onderhoudsmedewerkersgroep**, **Hulpmiddel** en **Activum**.</span><span class="sxs-lookup"><span data-stu-id="dd674-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="dd674-110">Selecteer de begindatum voor de berekening in het veld **Begindatum**.</span><span class="sxs-lookup"><span data-stu-id="dd674-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="dd674-111">Selecteer in het veld **Intervaltype** het interval voor de berekening: **Dag**, **Week**, **Maand** of **Kwartaal**.</span><span class="sxs-lookup"><span data-stu-id="dd674-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="dd674-112">In het veld **Periodefrequentie** voegt u het aantal intervallen in dat u wilt berekenen.</span><span class="sxs-lookup"><span data-stu-id="dd674-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="dd674-113">Als u bijvoorbeeld **Dag** hebt geselecteerd als het type interval en u typt het getal 5 in dit veld, wordt er een berekening van vijf dagen vanaf de begindatum uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="dd674-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="dd674-114">Klik op **OK** om de berekening te starten.</span><span class="sxs-lookup"><span data-stu-id="dd674-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="dd674-115">De volgende afbeelding laat het resultaat zien van een berekening die drie weken omvat voor het belastingtype **Gereserveerd**.</span><span class="sxs-lookup"><span data-stu-id="dd674-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Figuur 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="dd674-117">Als u het belastingtype **Capaciteit** of **Rest** selecteert voor de berekening, wordt hetzelfde resultaat weergegeven als er geen reserveringen zijn gemaakt voor de resources in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="dd674-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="dd674-118">Zie [Capaciteitsbelasting berekenen](../capacity-planning/calculate-capacity-load.md) voor informatie over het berekenen van de capaciteitsbelasting voor onderhoudsschemaregels en niet geplande werkorders.</span><span class="sxs-lookup"><span data-stu-id="dd674-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>


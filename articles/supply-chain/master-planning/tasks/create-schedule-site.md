---
title: Een planning voor een vestiging maken
description: Deze procedure laat zien hoe u productieorders plant die nog niet voor een vestiging zijn gestart.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1273297a7a48da11b1448f153a151c2a7b461d0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148050"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="44681-103">Een planning voor een vestiging maken</span><span class="sxs-lookup"><span data-stu-id="44681-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44681-104">Deze procedure laat zien hoe u productieorders plant die nog niet voor een vestiging zijn gestart.</span><span class="sxs-lookup"><span data-stu-id="44681-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="44681-105">Het demobedrijf USMF wordt gebruikt om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="44681-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="44681-106">Productieorders identificeren die niet zijn gestart</span><span class="sxs-lookup"><span data-stu-id="44681-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="44681-107">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="44681-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="44681-108">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="44681-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="44681-109">Filter bijvoorbeeld op het veld Vestiging met een waarde van '1'.</span><span class="sxs-lookup"><span data-stu-id="44681-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="44681-110">1 staat voor een vestiging in USMF.</span><span class="sxs-lookup"><span data-stu-id="44681-110">1 represents a site in USMF.</span></span> <span data-ttu-id="44681-111">Als u geen USMF gebruikt, selecteert u een vestiging van uw eigen bedrijf.</span><span class="sxs-lookup"><span data-stu-id="44681-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="44681-112">Open de kolomfilter Status.</span><span class="sxs-lookup"><span data-stu-id="44681-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="44681-113">Pas een filter op het veld "Status" toe met een waarde van "Gepland" met behulp van de filteroperator "is exact".</span><span class="sxs-lookup"><span data-stu-id="44681-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="44681-114">Een planning maken</span><span class="sxs-lookup"><span data-stu-id="44681-114">Create a schedule</span></span>
1. <span data-ttu-id="44681-115">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="44681-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="44681-116">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="44681-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="44681-117">Klik op Taken plannen.</span><span class="sxs-lookup"><span data-stu-id="44681-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="44681-118">Selecteer in het veld Planningsrichting de optie "Terug vanaf leveringsdatum".</span><span class="sxs-lookup"><span data-stu-id="44681-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="44681-119">Selecteer Nee in het veld Eindige capaciteit.</span><span class="sxs-lookup"><span data-stu-id="44681-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="44681-120">Selecteer Nee in het veld Eindig materiaal.</span><span class="sxs-lookup"><span data-stu-id="44681-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="44681-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="44681-121">Click OK.</span></span>
    * <span data-ttu-id="44681-122">Dit kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="44681-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="44681-123">Het resultaat van geplande productieorders weergeven</span><span class="sxs-lookup"><span data-stu-id="44681-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="44681-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="44681-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="44681-125">U kunt elke rij markeren.</span><span class="sxs-lookup"><span data-stu-id="44681-125">You can mark any row.</span></span>  
2. <span data-ttu-id="44681-126">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="44681-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="44681-127">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="44681-127">Click All jobs.</span></span>
    * <span data-ttu-id="44681-128">Op deze pagina kunt u de lijst met taken bekijken.</span><span class="sxs-lookup"><span data-stu-id="44681-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="44681-129">Op het tabblad Planning kunt u de begindatum en de einddatum voor een taak zien.</span><span class="sxs-lookup"><span data-stu-id="44681-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="44681-130">Klik op Materialen.</span><span class="sxs-lookup"><span data-stu-id="44681-130">Click Materials.</span></span>
    * <span data-ttu-id="44681-131">Op deze pagina kunt u het geschatte materiaalverbruik voor de bewerkingen op de productieorder en de huidige beschikbare voorraad bekijken.</span><span class="sxs-lookup"><span data-stu-id="44681-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  


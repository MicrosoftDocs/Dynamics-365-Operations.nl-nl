---
title: Een planning voor een vestiging maken
description: Deze procedure laat zien hoe u productieorders plant die nog niet voor een vestiging zijn gestart.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9059080fcd77a5317ce4226de6aad38b0066500
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425462"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="75b37-103">Een planning voor een vestiging maken</span><span class="sxs-lookup"><span data-stu-id="75b37-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75b37-104">Deze procedure laat zien hoe u productieorders plant die nog niet voor een vestiging zijn gestart.</span><span class="sxs-lookup"><span data-stu-id="75b37-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="75b37-105">Het demobedrijf USMF wordt gebruikt om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="75b37-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="75b37-106">Productieorders identificeren die niet zijn gestart</span><span class="sxs-lookup"><span data-stu-id="75b37-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="75b37-107">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="75b37-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="75b37-108">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="75b37-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="75b37-109">Filter bijvoorbeeld op het veld Vestiging met een waarde van '1'.</span><span class="sxs-lookup"><span data-stu-id="75b37-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="75b37-110">1 staat voor een vestiging in USMF.</span><span class="sxs-lookup"><span data-stu-id="75b37-110">1 represents a site in USMF.</span></span> <span data-ttu-id="75b37-111">Als u geen USMF gebruikt, selecteert u een vestiging van uw eigen bedrijf.</span><span class="sxs-lookup"><span data-stu-id="75b37-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="75b37-112">Open de kolomfilter Status.</span><span class="sxs-lookup"><span data-stu-id="75b37-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="75b37-113">Pas een filter op het veld "Status" toe met een waarde van "Gepland" met behulp van de filteroperator "is exact".</span><span class="sxs-lookup"><span data-stu-id="75b37-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="75b37-114">Een planning maken</span><span class="sxs-lookup"><span data-stu-id="75b37-114">Create a schedule</span></span>
1. <span data-ttu-id="75b37-115">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="75b37-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="75b37-116">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="75b37-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="75b37-117">Klik op Taken plannen.</span><span class="sxs-lookup"><span data-stu-id="75b37-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="75b37-118">Selecteer in het veld Planningsrichting de optie "Terug vanaf leveringsdatum".</span><span class="sxs-lookup"><span data-stu-id="75b37-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="75b37-119">Selecteer Nee in het veld Eindige capaciteit.</span><span class="sxs-lookup"><span data-stu-id="75b37-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="75b37-120">Selecteer Nee in het veld Eindig materiaal.</span><span class="sxs-lookup"><span data-stu-id="75b37-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="75b37-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="75b37-121">Click OK.</span></span>
    * <span data-ttu-id="75b37-122">Dit kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="75b37-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="75b37-123">Het resultaat van geplande productieorders weergeven</span><span class="sxs-lookup"><span data-stu-id="75b37-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="75b37-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="75b37-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="75b37-125">U kunt elke rij markeren.</span><span class="sxs-lookup"><span data-stu-id="75b37-125">You can mark any row.</span></span>  
2. <span data-ttu-id="75b37-126">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="75b37-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="75b37-127">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="75b37-127">Click All jobs.</span></span>
    * <span data-ttu-id="75b37-128">Op deze pagina kunt u de lijst met taken bekijken.</span><span class="sxs-lookup"><span data-stu-id="75b37-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="75b37-129">Op het tabblad Planning kunt u de begindatum en de einddatum voor een taak zien.</span><span class="sxs-lookup"><span data-stu-id="75b37-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="75b37-130">Klik op Materialen.</span><span class="sxs-lookup"><span data-stu-id="75b37-130">Click Materials.</span></span>
    * <span data-ttu-id="75b37-131">Op deze pagina kunt u het geschatte materiaalverbruik voor de bewerkingen op de productieorder en de huidige beschikbare voorraad bekijken.</span><span class="sxs-lookup"><span data-stu-id="75b37-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  


---
title: Dezelfde batch voor een verkooporder reserveren
description: In dit artikel wordt beschreven hoe u een product instelt om de reservering van voorraad voor één batch van voorraad toe te staan.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce750745d6f094a296b43827568ee1745179de2d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017271"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="9e712-103">Dezelfde batch voor een verkooporder reserveren</span><span class="sxs-lookup"><span data-stu-id="9e712-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e712-104">In dit artikel wordt beschreven hoe u een product instelt om de reservering van voorraad voor één batch van voorraad toe te staan.</span><span class="sxs-lookup"><span data-stu-id="9e712-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="9e712-105">Met reserveringen uit dezelfde batch kunt u voorraad reserveren voor een verkooporderregel uit één voorraadbatch.</span><span class="sxs-lookup"><span data-stu-id="9e712-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="9e712-106">Een klant die behang bestelt, kan bijvoorbeeld aangeven dat de volledige order uit dezelfde batch of partij moet worden gehaald om verschillen tussen de rollen te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="9e712-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="9e712-107">Als u een product wilt instellen voor reservering uit dezelfde batch, moeten de volgende instellingen actief zijn in de artikelmodelgroep, traceringsdimensiegroep en opslagdimensiegroepen die u aan het product toewijst:</span><span class="sxs-lookup"><span data-stu-id="9e712-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="9e712-108">**Artikelmodelgroepen** : in de artikelmodelgroep moeten de velden **Dezelfde batchselectie** en **Behoeften consolideren** zijn geselecteerd in de veldgroep **Reservering** voor voorraadbeleid.</span><span class="sxs-lookup"><span data-stu-id="9e712-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="9e712-109">**Traceringsdimensiegroepen** : in de traceringsdimensiegroep moet het veld **In behoefteplan opnemen volgens dimensie** zijn geselecteerd voor het batchnummer.</span><span class="sxs-lookup"><span data-stu-id="9e712-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="9e712-110">**Opslagdimensiegroepen** : in de opslagdimensiegroep moet het veld **In behoefteplan opnemen volgens dimensie** zijn geselecteerd voor **Locatie** en **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="9e712-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="9e712-111">Als u voorraad reserveert voor een product op een verkooporderregel die is ingesteld voor selectie uit dezelfde batch, probeert het systeem de bestelde hoeveelheid te reserveren uit één voorraadbatch.</span><span class="sxs-lookup"><span data-stu-id="9e712-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="9e712-112">Hierbij wordt rekening gehouden met eventuele specifieke batchkenmerkbehoeften.</span><span class="sxs-lookup"><span data-stu-id="9e712-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="9e712-113">Als de hoeveelheid niet uit één batch kan worden gehaald, wordt de pagina **Conflict door reservering van dezelfde batch** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9e712-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="9e712-114">Deze pagina geeft de uitgiften en ook de acties weer die u kunt uitvoeren om door te gaan met de reservering.</span><span class="sxs-lookup"><span data-stu-id="9e712-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="9e712-115">De volgende omstandigheden kunnen voorkomen dat de batch wordt gereserveerd:</span><span class="sxs-lookup"><span data-stu-id="9e712-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="9e712-116">Het veld **Reservering blokkeren** voor verkoop van de batchbeschikkingscode heeft de markering **Geblokkeerd**.</span><span class="sxs-lookup"><span data-stu-id="9e712-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="9e712-117">De batchdatum is verlopen op basis van de vervaldatum en eventuele van toepassing zijnde verkoopbare dagen voor de klant.</span><span class="sxs-lookup"><span data-stu-id="9e712-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="9e712-118">Het artikel kan nog in aanmerking komen voor reservering als de artikelmodelgroep voor het artikel een FEFO (First Expiry First Out)-datumcontrole heeft en als de houdbaarheidsdatum is geselecteerd als orderverzamelcriterium.</span><span class="sxs-lookup"><span data-stu-id="9e712-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="9e712-119">Er zijn onvoldoende houdbaarheidsdagen resterend voor de batch op basis van de vervaldatum en houdbaarheidsdatum plus eventuele van toepassing zijnde verkoopbare dagen voor de klant.</span><span class="sxs-lookup"><span data-stu-id="9e712-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="9e712-120">Voor artikelen die zijn gekoppeld aan een opslagdimensiegroep waarvoor **Magazijnbeheerprocessen gebruiken** is ingeschakeld, kunt u specifieke batchnummers reserveren door een reserveringshiërarchie te gebruiken met de gedefinieerde voorraaddimensie voor batchnummers die boven de locatiedimensie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="9e712-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="9e712-121">Via de pagina **Batchreservering** voor verkoop- en transferorderregels kunt u ook meerdere regels selecteren en reserveren op basis van de beschikbare batchnummers.</span><span class="sxs-lookup"><span data-stu-id="9e712-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="9e712-122">Zie [Flexibel reseveringsbeleid voor dimensies op magazijnniveau](../warehousing/flexible-warehouse-level-dimension-reservation.md) voor meer informatie over wat u moet doen als u een reserveringshiërarchie gebruikt die de batchnummerdimensie onder de locatie bevat.</span><span class="sxs-lookup"><span data-stu-id="9e712-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>

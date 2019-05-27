---
title: Dezelfde batch voor een verkooporder reserveren
description: In dit artikel wordt beschreven hoe u een product instelt om de reservering van voorraad voor één batch van voorraad toe te staan.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6089d07b0f8bc1a36703b5b1c2f24af72770d5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568300"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="b6dcc-103">Dezelfde batch voor een verkooporder reserveren</span><span class="sxs-lookup"><span data-stu-id="b6dcc-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6dcc-104">In dit artikel wordt beschreven hoe u een product instelt om de reservering van voorraad voor één batch van voorraad toe te staan.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="b6dcc-105">Met reserveringen uit dezelfde batch kunt u voorraad reserveren voor een verkooporderregel uit één voorraadbatch.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="b6dcc-106">Een klant die behang bestelt, kan bijvoorbeeld aangeven dat de volledige order uit dezelfde batch of partij moet worden gehaald om verschillen tussen de rollen te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="b6dcc-107">Als u een product wilt instellen voor reservering uit dezelfde batch, moeten de volgende instellingen actief zijn in de artikelmodelgroep, traceringsdimensiegroep en opslagdimensiegroepen die u aan het product toewijst:</span><span class="sxs-lookup"><span data-stu-id="b6dcc-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="b6dcc-108">**Artikelmodelgroepen**: in de artikelmodelgroep moeten de velden **Dezelfde batchselectie** en **Behoeften consolideren** zijn geselecteerd in de veldgroep **Reservering** voor voorraadbeleid.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="b6dcc-109">**Traceringsdimensiegroepen**: in de traceringsdimensiegroep moet het veld **In behoefteplan opnemen volgens dimensie** zijn geselecteerd voor het batchnummer.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="b6dcc-110">**Opslagdimensiegroepen**: in de opslagdimensiegroep moet het veld **In behoefteplan opnemen volgens dimensie** zijn geselecteerd voor **Locatie** en **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="b6dcc-111">Als u voorraad reserveert voor een product op een verkooporderregel die is ingesteld voor selectie uit dezelfde batch, wordt door Microsoft Dynamics 365 for Finance and Operations geprobeerd de bestelde hoeveelheid te reserveren uit één voorraadbatch.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="b6dcc-112">Hierbij wordt rekening gehouden met eventuele specifieke batchkenmerkbehoeften.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="b6dcc-113">Als de hoeveelheid niet uit één batch kan worden gehaald, wordt de pagina **Conflict door reservering van dezelfde batch** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="b6dcc-114">Deze pagina geeft de uitgiften en ook de acties weer die u kunt uitvoeren om door te gaan met de reservering.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="b6dcc-115">De volgende omstandigheden kunnen voorkomen dat de batch wordt gereserveerd:</span><span class="sxs-lookup"><span data-stu-id="b6dcc-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="b6dcc-116">Het veld **Reservering blokkeren** voor verkoop van de batchbeschikkingscode heeft de markering **Geblokkeerd**.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="b6dcc-117">De batchdatum is verlopen op basis van de vervaldatum en eventuele van toepassing zijnde verkoopbare dagen voor de klant.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="b6dcc-118">Het artikel kan nog in aanmerking komen voor reservering als de artikelmodelgroep voor het artikel een FEFO (First Expiry First Out)-datumcontrole heeft en als de houdbaarheidsdatum is geselecteerd als orderverzamelcriterium.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="b6dcc-119">Er zijn onvoldoende houdbaarheidsdagen resterend voor de batch op basis van de vervaldatum en houdbaarheidsdatum plus eventuele van toepassing zijnde verkoopbare dagen voor de klant.</span><span class="sxs-lookup"><span data-stu-id="b6dcc-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





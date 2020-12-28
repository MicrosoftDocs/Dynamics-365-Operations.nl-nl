---
title: Gebeurtenissen in app voor magazijnbeheer
description: In dit onderwerp wordt de verwerking van gebeurtenissen in de app voor magazijnbeheer beschreven die wordt gebruikt om gebeurtenisberichten van de app voor magazijnbeheer te verwerken als onderdeel van een batchtaak.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425304"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="7dc81-103">Verwerking van gebeurtenissen in de app voor magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="7dc81-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dc81-104">Batchtaken die worden uitgevoerd in Supply Chain Management kunnen gegevens uit een wachtrij verwerken voor de verwerking van gebeurtenissen die zijn uitgegeven door de app voor magazijnbeheer om zo nodig te reageren op de gesignaleerde gebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="7dc81-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="7dc81-105">Deze functie voegt relevante gebeurtenissen toe aan de wachtrij als reactie op bepaalde typen acties die door medewerkers met de app worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7dc81-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="7dc81-106">Een voorbeeld is dat bij gebruik van de functie **Transferorders maken en verwerken vanuit de app voor magazijnbeheer** de koptekst en regels van de transferorder worden gemaakt en bijgewerkt in de back-end wanneer de batchtaak **Gebeurtenissen van de app voor magazijnbeheer verwerken** wordt uitgevoerd door het systeem.</span><span class="sxs-lookup"><span data-stu-id="7dc81-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="7dc81-107">De functie Gebeurtenissen van de app voor magazijnbeheer verwerken inschakelen</span><span class="sxs-lookup"><span data-stu-id="7dc81-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="7dc81-108">Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem.</span><span class="sxs-lookup"><span data-stu-id="7dc81-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="7dc81-109">Beheerders kunnen gebruikmaken van de pagina voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="7dc81-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="7dc81-110">De functie Gebeurtenissen van de app voor magazijnbeheer verwerken staat vermeld als:</span><span class="sxs-lookup"><span data-stu-id="7dc81-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="7dc81-111">**Module** - Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="7dc81-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="7dc81-112">**Functienaam**: gebeurtenissen van de app voor magazijnbeheer verwerken</span><span class="sxs-lookup"><span data-stu-id="7dc81-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="7dc81-113">Een batchtaak instellen om gebeurtenissen van de app voor magazijnbeheer te verwerken</span><span class="sxs-lookup"><span data-stu-id="7dc81-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="7dc81-114">Gebeurtenissen in app voor magazijnbeheer verwerken</span><span class="sxs-lookup"><span data-stu-id="7dc81-114">Process warehouse app events</span></span>

<span data-ttu-id="7dc81-115">Stel een geplande batc taak in om de gebeurtenissen van de app voor magazijnbeheer te verwerken voor het maken van transferorders en regelupdates.</span><span class="sxs-lookup"><span data-stu-id="7dc81-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="7dc81-116">Ga naar **Magazijnbeheer \> Periodieke taken \> Gebeurtenissen in app voor magazijnbeheer verwerken**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="7dc81-117">Het dialoogvenster Gebeurtenissen in app voor magazijnbeheer verwerken wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="7dc81-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="7dc81-118">Vouw het sneltabblad **Op de achtergrond uitvoeren** uit en stel **Batchverwerking** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="7dc81-119">Selecteer op het tabblad **Op de achtergrond uitvoeren** de optie **Terugkeer**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="7dc81-120">Het dialoogvenster **Terugkeerpatroon definiëren** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="7dc81-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="7dc81-121">Stel het uitvoeringsschema in voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="7dc81-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="7dc81-122">Selecteer **OK** om terug te gaan naar het dialoogvenster **Gebeurtenissen in app voor magazijnbeheer verwerken**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="7dc81-123">Selecteer **OK** in het dialoogvenster **Gebeurtenissen in app voor magazijnbeheer verwerken** om de batchtaak aan de batchwachtrij toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="7dc81-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="7dc81-124">Query's uitvoeren op gebeurtenissen in app voor magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="7dc81-124">Query warehouse app events</span></span>

<span data-ttu-id="7dc81-125">U kunt de gebeurtenissenwachtrij en gebeurtenisberichten die zijn gegenereerd door de magazijnapp weergeven door naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer** te gaan.</span><span class="sxs-lookup"><span data-stu-id="7dc81-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="7dc81-126">Het standaardproces voor de gebeurtenissenwachtrij</span><span class="sxs-lookup"><span data-stu-id="7dc81-126">The standard event queue process</span></span>

<span data-ttu-id="7dc81-127">De wachtrij met gebeurtenissen in de app voor magazijnbeheer wordt doorgaans gebruikt met de volgende beschreven stroom:</span><span class="sxs-lookup"><span data-stu-id="7dc81-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="7dc81-128">Er wordt een gebeurtenis aan de wachtrij toegevoegd met een gebeurtenisbericht.</span><span class="sxs-lookup"><span data-stu-id="7dc81-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="7dc81-129">Het nieuwe bericht heeft in eerste instantie de gebeurtenisstatus **Wachten**, wat betekent dat de batchtaak **Gebeurtenissen in app voor magazijnbeheer verwerken** dit bericht niet ophaalt en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="7dc81-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="7dc81-130">Zodra de status van het bericht is gewijzigd in **In wachtrij**, wordt de gebeurtenis opgehaald en verwerkt door de batchtaak **Gebeurtenissen in app voor magazijnbeheer verwerken**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="7dc81-131">Met de batchtaak worden de statuswaarden bijgewerkt naar **Voltooid** of **Mislukt**, afhankelijk van het feit of het aangevraagde proces mogelijk was.</span><span class="sxs-lookup"><span data-stu-id="7dc81-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="7dc81-132">Wanneer alle gerelateerde gebeurtenisberichten zijn **Voltooid**, wordt de gebeurtenis uit de wachtrij verwijderd.</span><span class="sxs-lookup"><span data-stu-id="7dc81-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="7dc81-133">Zie [Transferorder maken vanuit proces van app voor magazijnbeheer](create-transfer-order-from-warehouse-app.md) voor een gedetailleerd voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="7dc81-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="7dc81-134">Gebeurtenisfouten afhandelen</span><span class="sxs-lookup"><span data-stu-id="7dc81-134">Handle event errors</span></span>

<span data-ttu-id="7dc81-135">Als onderdeel van de verwerking van magazijngebeurtenissen ontvangt de aangevraagde berichtactiviteit mogelijk geen processen van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="7dc81-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="7dc81-136">In dit geval wordt het gebeurtenisbericht gewijzigd in **Mislukt**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="7dc81-137">U kunt de informatie in **Batchlogboek** gebruiken om de oorzaak van problemen op te lossen en de benodigde actie te ondernemen.</span><span class="sxs-lookup"><span data-stu-id="7dc81-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="7dc81-138">Zie [Transferorder maken vanuit app voor magazijnbeheer](create-transfer-order-from-warehouse-app.md) voor een gedetailleerd voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="7dc81-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="7dc81-139">U kunt een bericht over een mislukte gebeurtenis in de app voor magazijnbeheer als volgt opnieuw instellen:</span><span class="sxs-lookup"><span data-stu-id="7dc81-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="7dc81-140">Ga naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="7dc81-141">Zoek en selecteer op het sneltabblad **Gebeurtenisberichten van de app voor magazijnbeheer** een relevante gebeurtenis waarvoor **Mislukt** wordt weergegeven in de kolom **Gebeurtenisstatus**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="7dc81-142">Selecteer **Opnieuw instellen** op de werkbalk **Gebeurtenisberichten van de app voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="7dc81-143">Ga door met werken totdat alle relevante berichten opnieuw zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="7dc81-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="7dc81-144">U kunt een gebeurtenisbericht **Mislukt** ook verwijderen met de optie **Verwijderen** op de werkbalk **Gebeurtenisberichten van de app voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="7dc81-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>

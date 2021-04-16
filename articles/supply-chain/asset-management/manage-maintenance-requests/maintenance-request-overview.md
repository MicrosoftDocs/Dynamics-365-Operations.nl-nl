---
title: Onderhoudsverzoeken
description: Dit onderwerp bevat een overzicht van het beheer van onderhoudsverzoeken in Activabeheer.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dceb179d0a17d8025d88c5945b9571de65c86449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838605"
---
# <a name="maintenance-requests"></a><span data-ttu-id="9cf64-103">Onderhoudsaanvragen</span><span class="sxs-lookup"><span data-stu-id="9cf64-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9cf64-104">Onderhoudsverzoeken zijn notities of verklaringen die zijn gemaakt om een manager of planner te informeren dat een activum mogelijk onderhoud of reparatie nodig heeft, maar zonder dat een werkorder wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9cf64-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="9cf64-105">Als de inhoud van een onderhoudsverzoek als geldig wordt beschouwd, kan een werkorder worden gemaakt op basis van het onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="9cf64-106">Onderhoudsverzoeken kunnen worden gemaakt voor elk activum in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="9cf64-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="9cf64-107">Er kunnen verschillende soorten onderhoudsverzoeken worden gemaakt, afhankelijk van de manier waarop uw bedrijf onderhoudsverzoeken gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cf64-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="9cf64-108">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="9cf64-108">Here are some examples:</span></span>

- <span data-ttu-id="9cf64-109">Onderhoudsaanvragen</span><span class="sxs-lookup"><span data-stu-id="9cf64-109">Maintenance requests</span></span>
- <span data-ttu-id="9cf64-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9cf64-110">Notes</span></span>
- <span data-ttu-id="9cf64-111">Correcties of verbeteringen</span><span class="sxs-lookup"><span data-stu-id="9cf64-111">Corrections or enhancements</span></span>
- <span data-ttu-id="9cf64-112">Investeringen</span><span class="sxs-lookup"><span data-stu-id="9cf64-112">Investments</span></span>
- <span data-ttu-id="9cf64-113">Depotreparatie (dit type wordt gebruikt wanneer u activa van een andere locatie ontvangt, zodat u een onderhouds- of reparatietaak kunt uitvoeren, en het activum retourneert nadat de taak is voltooid.)</span><span class="sxs-lookup"><span data-stu-id="9cf64-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="9cf64-114">Onderhoudsverzoeken weergeven</span><span class="sxs-lookup"><span data-stu-id="9cf64-114">View maintenance requests</span></span>

<span data-ttu-id="9cf64-115">Als u onderhoudsaanvragen wilt weergeven, selecteert u **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Alle onderhoudsverzoeken**, **Actieve onderhoudsverzoeken** of **De onderhoudsverzoeken van mijn functionele locatie**.</span><span class="sxs-lookup"><span data-stu-id="9cf64-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="9cf64-116">Elke lijstpagina bevat een deel van de informatie die is gerelateerd aan een onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Onderhoudsverzoeken weergeven](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="9cf64-118">Gebruik de pagina met de lijst **De onderhoudsverzoeken van mijn functionele locatie** om een lijst met onderhoudsverzoeken weer te geven die functionele locaties bevatten waaraan u bent gerelateerd als werknemer of activa die zijn geïnstalleerd op functionele locaties waaraan u bent gerelateerd als werknemer.</span><span class="sxs-lookup"><span data-stu-id="9cf64-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="9cf64-119">(Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor informatie over het instellen van onderhoudsmedewerkers en functionele locaties.)</span><span class="sxs-lookup"><span data-stu-id="9cf64-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="9cf64-120">Hoewel klantaccountinformatie beschikbaar is in Activaservicebeheer (extern onderhoud), is deze niet beschikbaar in Activabeheer (intern onderhoud).</span><span class="sxs-lookup"><span data-stu-id="9cf64-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="9cf64-121">Als u de detailweergave van een record wilt openen, selecteert u op de pagina met de lijst **Alle onderhoudsverzoeken** in rasterweergave een koppeling in kolom **Onderhoudsverzoek**.</span><span class="sxs-lookup"><span data-stu-id="9cf64-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Details van onderhoudsverzoek weergeven](media/02-manage-maintenance-requests.png)

<span data-ttu-id="9cf64-123">De knoppen in het actievenster zijn geordend op tabbladen.</span><span class="sxs-lookup"><span data-stu-id="9cf64-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="9cf64-124">In de volgende tabel worden kort de knoppen beschreven die betrekking hebben op Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="9cf64-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="9cf64-125">Knopnaam</span><span class="sxs-lookup"><span data-stu-id="9cf64-125">Button name</span></span>                      | <span data-ttu-id="9cf64-126">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9cf64-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="9cf64-127">Bewerken</span><span class="sxs-lookup"><span data-stu-id="9cf64-127">Edit</span></span>                             | <span data-ttu-id="9cf64-128">Bewerk het geselecteerde artikel onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-129">Nieuw</span><span class="sxs-lookup"><span data-stu-id="9cf64-129">New</span></span>                              | <span data-ttu-id="9cf64-130">Maak een nieuw onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="9cf64-131">Verwijderen</span><span class="sxs-lookup"><span data-stu-id="9cf64-131">Delete</span></span>                           | <span data-ttu-id="9cf64-132">Verwijder het geselecteerde onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-133">Werkordergroep</span><span class="sxs-lookup"><span data-stu-id="9cf64-133">Work order pool</span></span>                  | <span data-ttu-id="9cf64-134">Verbind het geselecteerde onderhoudsverzoek aan een werkordergroep.</span><span class="sxs-lookup"><span data-stu-id="9cf64-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="9cf64-135">Werkorder</span><span class="sxs-lookup"><span data-stu-id="9cf64-135">Work order</span></span>                       | <span data-ttu-id="9cf64-136">Maak een werkorder op basis van het geselecteerde onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-137">Fout in activum</span><span class="sxs-lookup"><span data-stu-id="9cf64-137">Asset fault</span></span>                      | <span data-ttu-id="9cf64-138">Klik op **Activafouten**, waar u een foutregistratie op het geselecteerde onderhoudsverzoek kunt maken.</span><span class="sxs-lookup"><span data-stu-id="9cf64-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-139">Werkorders</span><span class="sxs-lookup"><span data-stu-id="9cf64-139">Work orders</span></span>                      | <span data-ttu-id="9cf64-140">Geen een lijst met alle werkorders weer die verbonden zijn aan het geselecteerde onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-141">Status van onderhoudsverzoek bijwerken</span><span class="sxs-lookup"><span data-stu-id="9cf64-141">Update maintenance request state</span></span> | <span data-ttu-id="9cf64-142">Werk de status van het onderhoudsverzoek bij.</span><span class="sxs-lookup"><span data-stu-id="9cf64-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="9cf64-143">Logboek levenscyclusstatus</span><span class="sxs-lookup"><span data-stu-id="9cf64-143">Lifecycle state log</span></span>              | <span data-ttu-id="9cf64-144">Geef een logboek weer waarin de levenscyclusstatussen van het geselecteerde onderhoudsverzoek worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9cf64-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-145">Details van het onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="9cf64-145">Maintenance request details</span></span>      | <span data-ttu-id="9cf64-146">Druk een rapport af met de details van het geselecteerde onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-147">Geleend activum verzenden</span><span class="sxs-lookup"><span data-stu-id="9cf64-147">Send loan asset</span></span>                  | <span data-ttu-id="9cf64-148">Selecteer een geleend activum dat een tijdelijke vervanging moet zijn voor het activum dat is geselecteerd op het geselecteerde onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="9cf64-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="9cf64-149">Een geleend activum retourneren</span><span class="sxs-lookup"><span data-stu-id="9cf64-149">Return loan asset</span></span>                | <span data-ttu-id="9cf64-150">Registreer het geleende activum als geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="9cf64-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
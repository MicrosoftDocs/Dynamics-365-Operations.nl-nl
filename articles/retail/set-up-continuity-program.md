---
title: Continuïteitsprogramma's instellen voor callcenters
description: In dit artikel wordt beschreven hoe u een continuïteitsprogramma instelt voor een callcenter.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 369856f33c6da49b6c6b3f51f42c99a8f07fe777
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "320967"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="e7a2c-103">Continuïteitsprogramma's instellen voor callcenters</span><span class="sxs-lookup"><span data-stu-id="e7a2c-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7a2c-104">In dit artikel wordt beschreven hoe u een continuïteitsprogramma instelt voor een callcenter.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="e7a2c-105">In een continuïteitsprogramma, dat ook bekend staat als een terugkerend orderprogramma, ontvangen klanten regelmatige productzendingen op basis van een vooraf gedefinieerde planning.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="e7a2c-106">Elke zending kan een ander product bevatten, zoals in het geval van een boek-van-de-maand club, of hetzelfde product kan herhaaldelijk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="e7a2c-107">Als u een continuïteitsprogrammma instelt, moet u de volgende taken uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="e7a2c-108">Stel de continuïteitsparameters op de **Parameters van callcenter** in.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="e7a2c-109">Maak een continuïteitsprogramma waarmee details worden opgegeven, zoals het betalingsschema, de timing van de zendingen en of de facturering vooraf gebeurt.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="e7a2c-110">U moet ook een lijst met producten toevoegen die in het continuïteitsprogramma zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="e7a2c-111">Elk product ontvangt een gebeurtenis-ID die opeenvolgend wordt toegewezen, te beginnen met 1.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="e7a2c-112">Met de gebeurtenis-ID's wordt de volgorde bepaald waarin de producten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="e7a2c-113">Als klanten een ander product in elke zending ontvangen, worden de producten achtereenvolgens op basis van de bijbehorende gebeurtenis-ID's verzonden, te beginnen met de huidige gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="e7a2c-114">Als klanten hetzelfde product in elke zending ontvangen, bevat de lijst slechts één product dat een gebeurtenis-ID heeft.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="e7a2c-115">Dezelfde gebeurtenis komt herhaaldelijk voor.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="e7a2c-116">U kunt opgeven hoe vaak u elke gebeurtenis wordt herhaald.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="e7a2c-117">Maak vervolgens een bovenliggend product dat het continuïteitsprogramma vertegenwoordigt dat u in taak 2 hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="e7a2c-118">Als u dit product aan een verkooporder toevoegt, wordt de pagina **Continuïteit** geopend.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="e7a2c-119">U kunt die pagina vervolgens gebruiken om de werkelijke continuïteitsorder te maken.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="e7a2c-120">Met het bovenliggende product worden de afzonderlijke producten die de klant in elke zending ontvangt, niet opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="e7a2c-121">Nadat u een continuïteitsprogramma hebt ingesteld zoals hierboven beschreven , kunt u een continuïteitsorder maken voor een klant.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="e7a2c-122">U moet mogelijk ook de volgende aanvullende onderhoudstaken uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="e7a2c-123">**De huidige continuïteitsgebeurtenisperiode bijwerken**: stel een batchtaak in waarmee aan het systeem wordt doorgegeven wat de huidige gebeurtenisperiode is.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="e7a2c-124">**Onderliggende continuïteitsorders maken**: maak onderliggende orders op basis van de bovenliggende continuïteitsorder.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="e7a2c-125">**Continuïteitsbetalingen verwerken**: facturering en meldingen verwerken voor betalingen die zijn gekoppeld aan continuïteitsverkooporders.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="e7a2c-126">**Continuïteitsregels uitbreiden** (indien nodig): breid het aantal keren uit dat een continuïteitsgebeurtenis kan worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="e7a2c-127">De herhaling van zendingen kan vervolgens worden uitgebreid buiten de limiet die is ingesteld in het veld **Drempel voor continuïteitsherhaling** in de parameters van het callcenter.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="e7a2c-128">**Een continuïteitsupdate uitvoeren** (indien nodig): synchroniseer wijzigingen tussen het continuïteitsprogramma en de bovenliggende continuïteitsverkooporders.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="e7a2c-129">**Bovenliggende continuïteitsregels en -orders sluiten**: sluit continuïteitsorders.</span><span class="sxs-lookup"><span data-stu-id="e7a2c-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>

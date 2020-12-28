---
title: Het eigendom van consignatievoorraad wijzigen op basis van de productievraag
description: Deze procedure laat zien hoe u de eigenaar van de consignatievoorraad wijzigt van de leverancier in uw rechtspersoon wanneer er vraag is naar de voorraad in productie.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425713"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="ee33f-103">Het eigendom van consignatievoorraad wijzigen op basis van de productievraag</span><span class="sxs-lookup"><span data-stu-id="ee33f-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee33f-104">Deze procedure laat zien hoe u de eigenaar van de consignatievoorraad wijzigt van de leverancier in uw rechtspersoon wanneer er vraag is naar de voorraad in productie.</span><span class="sxs-lookup"><span data-stu-id="ee33f-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="ee33f-105">Deze wijziging van eigendom wordt uitgevoerd door een wijzigingslogboek van het voorraadeigendom te maken en te boeken.</span><span class="sxs-lookup"><span data-stu-id="ee33f-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="ee33f-106">De regels van het eigendomwijzigingslogboek kunnen handmatig worden gemaakt of, zoals deze opname laat zien, worden gebaseerd op de bestaande productievraag.</span><span class="sxs-lookup"><span data-stu-id="ee33f-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="ee33f-107">Gewoonlijk voert een werkvloersupervisor deze taak uit.</span><span class="sxs-lookup"><span data-stu-id="ee33f-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="ee33f-108">U kunt deze procedure gebruiken in het demobedrijf USMF of voor uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="ee33f-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="ee33f-109">Als u uw eigen gegevens gebruikt, moet u voldoen aan de volgende vereisten: een voorraadjournaalnaam die is ingesteld voor de wijziging van het voorraadeigendom, fysiek geregistreerde voorhanden artikelen in het bezit van de leverancier, en een of meer productieorderregels voor het materiaal.</span><span class="sxs-lookup"><span data-stu-id="ee33f-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="ee33f-110">Deze procedure is voor een functie die in Dynamics 365 for Operations, versie 1611 is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="ee33f-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="ee33f-111">Uitgaande zendingsprocessen worden niet out-of-the-box ondersteund en de verwerking van de automatische eigendomsjournalen wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="ee33f-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="ee33f-112">Een voorraadeigendomsjournaal maken</span><span class="sxs-lookup"><span data-stu-id="ee33f-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="ee33f-113">Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Wijziging aan voorraadeigendom.</span><span class="sxs-lookup"><span data-stu-id="ee33f-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="ee33f-114">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ee33f-114">Click New.</span></span>
    * <span data-ttu-id="ee33f-115">Het wijzigingslogboek van het voorraadeigendom wordt gebruikt om de eigenaar van consignatievoorraad van de leverancier te wijzigen in de huidige rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ee33f-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="ee33f-116">Deze wijziging van eigendom wordt uitgevoerd door de voorhanden voorraad vrij te geven die eigendom is van de leverancier en die voorraad vervolgens te ontvangen voor de huidige rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ee33f-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="ee33f-117">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="ee33f-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="ee33f-118">U kunt alleen voorraadjournaalnamen selecteren die het journaaltype Wijziging aan eigendom hebben.</span><span class="sxs-lookup"><span data-stu-id="ee33f-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="ee33f-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ee33f-119">Click OK.</span></span>
5. <span data-ttu-id="ee33f-120">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="ee33f-120">Click Functions.</span></span>
6. <span data-ttu-id="ee33f-121">Klik op Journaalregels maken op basis van productieorders.</span><span class="sxs-lookup"><span data-stu-id="ee33f-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="ee33f-122">U kunt de wijziging van het eigendomproces starten door alle productieregels te zoeken met vraag naar verbruik van grondstoffen.</span><span class="sxs-lookup"><span data-stu-id="ee33f-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="ee33f-123">Selecteer een optie in het veld Op te nemen voorraaduitgiftestatussen.</span><span class="sxs-lookup"><span data-stu-id="ee33f-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="ee33f-124">Met deze optie kunt u filteren op de uitgiftestatus van de voorraadtransacties.</span><span class="sxs-lookup"><span data-stu-id="ee33f-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="ee33f-125">U kunt bijvoorbeeld journaalregels maken voor voorraad met de status Verzameld en fysiek gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="ee33f-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="ee33f-126">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="ee33f-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="ee33f-127">In deze sectie kunt u aanvullende filterbewerkingen toepassen.</span><span class="sxs-lookup"><span data-stu-id="ee33f-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="ee33f-128">U kunt bijvoorbeeld een specifieke grondstoffendatum selecteren.</span><span class="sxs-lookup"><span data-stu-id="ee33f-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="ee33f-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ee33f-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="ee33f-130">De wijzigingen in het voorraadeigendomsjournaal boeken</span><span class="sxs-lookup"><span data-stu-id="ee33f-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="ee33f-131">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="ee33f-131">Click Post.</span></span>
    * <span data-ttu-id="ee33f-132">Wanneer het journaal wordt geboekt, wordt de voorraad die in het bezit is van de leverancier vrijgegeven door een verwijzing voor Wijziging aan eigendom.</span><span class="sxs-lookup"><span data-stu-id="ee33f-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="ee33f-133">Vervolgens wordt de voorraad ontvangen als voorhanden voorraad met een voorraadtransactie die met een inkooporderproductontvangstbon wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="ee33f-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="ee33f-134">Merk op dat alleen transacties worden gemaakt die samenhangen met het geboekte journaal.</span><span class="sxs-lookup"><span data-stu-id="ee33f-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="ee33f-135">Er worden geen verwachte voorraadtransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ee33f-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="ee33f-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ee33f-136">Click OK.</span></span>
3. <span data-ttu-id="ee33f-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ee33f-137">Close the page.</span></span>


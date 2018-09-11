--- 
title: Een consignatieaanvullingsorder maken
description: Deze procedure laat zien hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren.
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 686a4bc1e9d752cc6d33354d03ba3c536c0854dc
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="e9a98-103">Een consignatieaanvullingsorder maken</span><span class="sxs-lookup"><span data-stu-id="e9a98-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9a98-104">Deze procedure laat zien hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="e9a98-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="e9a98-105">Het laat ook zien hoe u een ontvangst van producten registreert zodat de consignatievoorraad als voorhanden voorraad wordt geregistreerd die eigendom is van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="e9a98-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="e9a98-106">Deze procdure wordt gewoonlijk uitgevoerd door een inkoper.</span><span class="sxs-lookup"><span data-stu-id="e9a98-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="e9a98-107">U kunt deze begeleiding gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="e9a98-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="e9a98-108">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e9a98-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="e9a98-109">Een consignatieaanvullingsorder maken</span><span class="sxs-lookup"><span data-stu-id="e9a98-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="e9a98-110">Ga naar Inkoop en sourcing > Consignatie > Consignatieaanvullingsorders.</span><span class="sxs-lookup"><span data-stu-id="e9a98-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="e9a98-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e9a98-111">Click New.</span></span>
3. <span data-ttu-id="e9a98-112">Selecteer in het veld Leveranciersrekening de leverancier US-104.</span><span class="sxs-lookup"><span data-stu-id="e9a98-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="e9a98-113">U moet een leverancier selecteren die als eigenaar is geregistreerd op de pagina Voorraadeigenaren.</span><span class="sxs-lookup"><span data-stu-id="e9a98-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="e9a98-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e9a98-114">Click OK.</span></span>
5. <span data-ttu-id="e9a98-115">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e9a98-115">Click Add line.</span></span>
6. <span data-ttu-id="e9a98-116">Typ M9211CI in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e9a98-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="e9a98-117">U moet een artikel selecteren dat is ingesteld voor consignatievoorraad.</span><span class="sxs-lookup"><span data-stu-id="e9a98-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="e9a98-118">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="e9a98-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="e9a98-119">Typ een datum in het veld Gevraagde leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="e9a98-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="e9a98-120">De aangevraagde en bevestigde datums worden door de MRP-engine gebruikt voor de verwachte ontvangst van de goederen.</span><span class="sxs-lookup"><span data-stu-id="e9a98-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="e9a98-121">Typ een datum in het veld Bevestigde leveringsdatum.</span><span class="sxs-lookup"><span data-stu-id="e9a98-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="e9a98-122">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="e9a98-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="e9a98-123">Klik op het tabblad Voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="e9a98-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="e9a98-124">Vernieuw de pagina om de eigenaar weer te geven in het veld Eigenaar voorraaddimensies.</span><span class="sxs-lookup"><span data-stu-id="e9a98-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="e9a98-125">Leverancier US-104 is nu vermeld als de eigenaar.</span><span class="sxs-lookup"><span data-stu-id="e9a98-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="e9a98-126">Controleer de status van de voorraadtransactie</span><span class="sxs-lookup"><span data-stu-id="e9a98-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="e9a98-127">Klik op Voorraad.</span><span class="sxs-lookup"><span data-stu-id="e9a98-127">Click Inventory.</span></span>
2. <span data-ttu-id="e9a98-128">Klik op Transacties.</span><span class="sxs-lookup"><span data-stu-id="e9a98-128">Click Transactions.</span></span>
3. <span data-ttu-id="e9a98-129">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e9a98-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e9a98-130">Let op dat het veld Ontvangst op Besteld is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e9a98-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="e9a98-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e9a98-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="e9a98-132">Artikelen ontvangen</span><span class="sxs-lookup"><span data-stu-id="e9a98-132">Receive items</span></span>
1. <span data-ttu-id="e9a98-133">Klik op Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="e9a98-133">Click Product receipt.</span></span>
2. <span data-ttu-id="e9a98-134">Typ een waarde in het veld Externe productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="e9a98-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="e9a98-135">Typ in het veld Hoeveelheid een aantal dat lager is dan het aantal dat hier wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e9a98-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="e9a98-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e9a98-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="e9a98-137">Controleer de voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="e9a98-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="e9a98-138">Klik op Voorraad.</span><span class="sxs-lookup"><span data-stu-id="e9a98-138">Click Inventory.</span></span>
2. <span data-ttu-id="e9a98-139">Klik op Voorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9a98-139">Click On-hand.</span></span>
3. <span data-ttu-id="e9a98-140">Klik op Overzicht.</span><span class="sxs-lookup"><span data-stu-id="e9a98-140">Click Overview.</span></span>
    * <span data-ttu-id="e9a98-141">De artikelen die zijn ontvangen als consignatievoorraad en die eigendom zijn van de leverancier, zijn voorhanden in de voorraad.</span><span class="sxs-lookup"><span data-stu-id="e9a98-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="e9a98-142">De resterende hoeveelheid op de consignatieaanvullingsorder wordt weergegeven in het veld Totaal van order.</span><span class="sxs-lookup"><span data-stu-id="e9a98-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="e9a98-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e9a98-143">Close the page.</span></span>
5. <span data-ttu-id="e9a98-144">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="e9a98-144">Click Close.</span></span>



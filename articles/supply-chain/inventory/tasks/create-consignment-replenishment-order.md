---
title: Een consignatieaanvullingsorder maken
description: In dit onderwerp wordt uitgelegd hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren.
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e993190150e2d82088390d8db4b7c5ada2b0161
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018348"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="eed4f-103">Een consignatieaanvullingsorder maken</span><span class="sxs-lookup"><span data-stu-id="eed4f-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eed4f-104">In dit onderwerp wordt uitgelegd hoe u een consignatieaanvullingsorder maakt waarin u de verwachte levering van een leverancier in de consignatievoorraad kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="eed4f-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="eed4f-105">Het laat ook zien hoe u een ontvangst van producten registreert zodat de consignatievoorraad als voorhanden voorraad wordt geregistreerd die eigendom is van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="eed4f-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="eed4f-106">Deze procdure wordt gewoonlijk uitgevoerd door een inkoper.</span><span class="sxs-lookup"><span data-stu-id="eed4f-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="eed4f-107">U kunt deze begeleiding gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="eed4f-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="eed4f-108">Deze procedure is voor een functie die in Dynamics 365 for Operations, versie 1611 is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="eed4f-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="eed4f-109">Een consignatieaanvullingsorder maken</span><span class="sxs-lookup"><span data-stu-id="eed4f-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="eed4f-110">Ga in het navigatievenster naar **Modules > Inkoopbeheer > Consignatie > Consignatieaanvullingsorders**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="eed4f-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-111">Select **New**.</span></span>
3. <span data-ttu-id="eed4f-112">In het veld **Leveranciersrekening** selecteert u leverancier **US-104** (u moet een leverancier selecteren die als eigenaar wordt vermeld op de pagina **Voorraadeigenaren** ).</span><span class="sxs-lookup"><span data-stu-id="eed4f-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="eed4f-113">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-113">Select **OK**.</span></span>
5. <span data-ttu-id="eed4f-114">Selecteer **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-114">Select **Add line**.</span></span>
6. <span data-ttu-id="eed4f-115">Typ `M9211CI` in het veld **Artikelnummer** (u moet een artikel selecteren dat is ingesteld voor consignatievoorraad).</span><span class="sxs-lookup"><span data-stu-id="eed4f-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="eed4f-116">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="eed4f-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="eed4f-117">Typ een datum in het veld **Gevraagde leveringsdatum**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="eed4f-118">De aangevraagde en bevestigde datums worden door de MRP-engine gebruikt voor de verwachte ontvangst van de goederen.</span><span class="sxs-lookup"><span data-stu-id="eed4f-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="eed4f-119">Typ een datum in het veld **Bevestigde leveringsdatum**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="eed4f-120">Vouw de sectie **Regeldetails** uit.</span><span class="sxs-lookup"><span data-stu-id="eed4f-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="eed4f-121">Selecteer het tabblad **Voorraaddimensies**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="eed4f-122">Vernieuw de pagina om de eigenaar weer te geven in het veld **Eigenaar voorraaddimensies**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="eed4f-123">Leverancier US-104 is nu vermeld als de eigenaar.</span><span class="sxs-lookup"><span data-stu-id="eed4f-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="eed4f-124">Controleer de status van de voorraadtransactie</span><span class="sxs-lookup"><span data-stu-id="eed4f-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="eed4f-125">Selecteer **Voorraadmodel**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="eed4f-126">Selecteer **Transacties**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="eed4f-127">In de gewenste rij is het veld **Ontvangst** op **Besteld** ingesteld.</span><span class="sxs-lookup"><span data-stu-id="eed4f-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="eed4f-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eed4f-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="eed4f-129">Artikelen ontvangen</span><span class="sxs-lookup"><span data-stu-id="eed4f-129">Receive items</span></span>
1. <span data-ttu-id="eed4f-130">Selecteer **Productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="eed4f-131">Typ een waarde in het veld **Externe productontvangstbon**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="eed4f-132">Typ in het veld **Hoeveelheid** een aantal dat lager is dan het aantal dat hier wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eed4f-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="eed4f-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="eed4f-134">Controleer de voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="eed4f-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="eed4f-135">Selecteer **Voorraadmodel**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="eed4f-136">Selecteer **Voorhanden**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="eed4f-137">Selecteer **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-137">Select **Overview**.</span></span> <span data-ttu-id="eed4f-138">De artikelen die zijn ontvangen als consignatievoorraad en die eigendom zijn van de leverancier, zijn voorhanden in de voorraad.</span><span class="sxs-lookup"><span data-stu-id="eed4f-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="eed4f-139">De resterende hoeveelheid op de consignatieaanvullingsorder wordt weergegeven in het veld **Totaal van order**.</span><span class="sxs-lookup"><span data-stu-id="eed4f-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="eed4f-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eed4f-140">Close the page.</span></span>


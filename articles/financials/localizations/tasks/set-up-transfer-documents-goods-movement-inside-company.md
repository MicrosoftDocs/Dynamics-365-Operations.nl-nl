---
title: De overboekingsdocumenten instellen voor goederenverplaatsing in een bedrijf
description: Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69542df1384bb36d89e2df5e5bc5fbe3dbe3c4cf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "311836"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="4f37f-103">De overboekingsdocumenten instellen voor goederenverplaatsing in een bedrijf</span><span class="sxs-lookup"><span data-stu-id="4f37f-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f37f-104">Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt.</span><span class="sxs-lookup"><span data-stu-id="4f37f-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="4f37f-105">Deze procedure is alleen beschikbaar voor rechtspersonen met een primair adres in Litouwen.</span><span class="sxs-lookup"><span data-stu-id="4f37f-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="4f37f-106">De procedure is gemaakt met het demobedrijf DEMF met een primair adres in Litouwen.</span><span class="sxs-lookup"><span data-stu-id="4f37f-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="4f37f-107">Voordat u deze procedure kunt uitvoeren, moet u de procedure "Overboekingsdocumenten instellen voor goederenverplaatsing binnen een bedrijf" voltooien.</span><span class="sxs-lookup"><span data-stu-id="4f37f-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="4f37f-108">Deze procedure is alleen bedoeld voor voorraadboekhouders.</span><span class="sxs-lookup"><span data-stu-id="4f37f-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="4f37f-109">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="4f37f-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="4f37f-110">Een transferorder maken</span><span class="sxs-lookup"><span data-stu-id="4f37f-110">Create a transfer order</span></span>
1. <span data-ttu-id="4f37f-111">Ga naar Voorraadbeheer > Inkomende orders > Transferorder.</span><span class="sxs-lookup"><span data-stu-id="4f37f-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="4f37f-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4f37f-112">Click New.</span></span>
3. <span data-ttu-id="4f37f-113">Typ of selecteer een waarde in het veld Van magazijn.</span><span class="sxs-lookup"><span data-stu-id="4f37f-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="4f37f-114">Typ of selecteer een waarde in het veld Naar magazijn.</span><span class="sxs-lookup"><span data-stu-id="4f37f-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="4f37f-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4f37f-115">Click Add.</span></span>
6. <span data-ttu-id="4f37f-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4f37f-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="4f37f-117">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="4f37f-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="4f37f-118">Transportgegevens invoeren voor de transferorder</span><span class="sxs-lookup"><span data-stu-id="4f37f-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="4f37f-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4f37f-119">Click Save.</span></span>
2. <span data-ttu-id="4f37f-120">Klik in het actievenster op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="4f37f-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="4f37f-121">Klik op Transportgegevens.</span><span class="sxs-lookup"><span data-stu-id="4f37f-121">Click Transportation details.</span></span>
4. <span data-ttu-id="4f37f-122">Selecteer Ja in de veld Transportgegevens afdrukken.</span><span class="sxs-lookup"><span data-stu-id="4f37f-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="4f37f-123">Typ of selecteer een waarde in het veld Afgegeven goederen.</span><span class="sxs-lookup"><span data-stu-id="4f37f-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="4f37f-124">Typ een waarde in het veld Verpakking.</span><span class="sxs-lookup"><span data-stu-id="4f37f-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="4f37f-125">Typ een waarde in het veld Risiconiveau van de lading.</span><span class="sxs-lookup"><span data-stu-id="4f37f-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="4f37f-126">Typ of selecteer een waarde in het veld Vervoerder.</span><span class="sxs-lookup"><span data-stu-id="4f37f-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="4f37f-127">Typ of selecteer een waarde in het veld Model.</span><span class="sxs-lookup"><span data-stu-id="4f37f-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="4f37f-128">Typ een waarde in het veld Registratienummer.</span><span class="sxs-lookup"><span data-stu-id="4f37f-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="4f37f-129">Typ een waarde in het veld Trailerregistratienummer.</span><span class="sxs-lookup"><span data-stu-id="4f37f-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="4f37f-130">Typ of selecteer een waarde in het veld Chauffeur.</span><span class="sxs-lookup"><span data-stu-id="4f37f-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="4f37f-131">Typ een waarde in het veld Naam chauffeur.</span><span class="sxs-lookup"><span data-stu-id="4f37f-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="4f37f-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4f37f-132">Click Save.</span></span>
15. <span data-ttu-id="4f37f-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4f37f-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="4f37f-134">Pakbon voor de niet-geboekte transferferorder weergeven</span><span class="sxs-lookup"><span data-stu-id="4f37f-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="4f37f-135">Klik op Pakbon.</span><span class="sxs-lookup"><span data-stu-id="4f37f-135">Click Packing slip.</span></span>
2. <span data-ttu-id="4f37f-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4f37f-136">Click OK.</span></span>
3. <span data-ttu-id="4f37f-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4f37f-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="4f37f-138">Pakbon voor de geboekte transferferorder weergeven</span><span class="sxs-lookup"><span data-stu-id="4f37f-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="4f37f-139">Klik in het actievenster op Transferorder.</span><span class="sxs-lookup"><span data-stu-id="4f37f-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="4f37f-140">Klik in het actievenster op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="4f37f-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="4f37f-141">Klik op Verzenden transferorders.</span><span class="sxs-lookup"><span data-stu-id="4f37f-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="4f37f-142">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="4f37f-142">Click the General tab.</span></span>
5. <span data-ttu-id="4f37f-143">Selecteer een optie in het veld Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="4f37f-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="4f37f-144">Klik op het tabblad Overzicht.</span><span class="sxs-lookup"><span data-stu-id="4f37f-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="4f37f-145">Typ een waarde in het veld Pakbon.</span><span class="sxs-lookup"><span data-stu-id="4f37f-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="4f37f-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4f37f-146">Click OK.</span></span>
9. <span data-ttu-id="4f37f-147">Klik in het actievenster op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="4f37f-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="4f37f-148">Klik op Pakbon.</span><span class="sxs-lookup"><span data-stu-id="4f37f-148">Click Packing slip.</span></span>
11. <span data-ttu-id="4f37f-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4f37f-149">Click OK.</span></span>


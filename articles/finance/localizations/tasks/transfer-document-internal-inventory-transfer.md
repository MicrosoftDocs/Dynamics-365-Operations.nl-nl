---
title: Een overboekingsdocument genereren voor een interne voorraadoverboeking
description: Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cb0d3d51bf30717f05a4daf1a098565d5d48621
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441987"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="47761-103">Een overboekingsdocument genereren voor een interne voorraadoverboeking</span><span class="sxs-lookup"><span data-stu-id="47761-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47761-104">Deze procedure laat zien hoe u overboekingsdocumenten voor goederenverplaatsing binnen een bedrijf maakt.</span><span class="sxs-lookup"><span data-stu-id="47761-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="47761-105">Deze procedure is alleen beschikbaar voor rechtspersonen met een primair adres in Litouwen.</span><span class="sxs-lookup"><span data-stu-id="47761-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="47761-106">De procedure is gemaakt met het demobedrijf DEMF met een primair adres in Litouwen.</span><span class="sxs-lookup"><span data-stu-id="47761-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="47761-107">Voordat u deze procedure kunt uitvoeren, moet u de procedure Overboekingsdocumenten instellen voor goederenverplaatsing binnen een bedrijf voltooien.</span><span class="sxs-lookup"><span data-stu-id="47761-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="47761-108">Deze procedure is alleen bedoeld voor voorraadboekhouders.</span><span class="sxs-lookup"><span data-stu-id="47761-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="47761-109">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="47761-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="47761-110">Een transferorder maken</span><span class="sxs-lookup"><span data-stu-id="47761-110">Create a transfer order</span></span>
1. <span data-ttu-id="47761-111">Ga naar Voorraadbeheer > Inkomende orders > Transferorder.</span><span class="sxs-lookup"><span data-stu-id="47761-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="47761-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="47761-112">Click New.</span></span>
3. <span data-ttu-id="47761-113">Typ of selecteer een waarde in het veld Van magazijn.</span><span class="sxs-lookup"><span data-stu-id="47761-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="47761-114">Typ of selecteer een waarde in het veld Naar magazijn.</span><span class="sxs-lookup"><span data-stu-id="47761-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="47761-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="47761-115">Click Add.</span></span>
6. <span data-ttu-id="47761-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="47761-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="47761-117">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="47761-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="47761-118">Transportgegevens invoeren voor de transferorder</span><span class="sxs-lookup"><span data-stu-id="47761-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="47761-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="47761-119">Click Save.</span></span>
2. <span data-ttu-id="47761-120">Klik in het actievenster op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="47761-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="47761-121">Klik op Transportgegevens.</span><span class="sxs-lookup"><span data-stu-id="47761-121">Click Transportation details.</span></span>
4. <span data-ttu-id="47761-122">Selecteer Ja in de veld Transportgegevens afdrukken.</span><span class="sxs-lookup"><span data-stu-id="47761-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="47761-123">Typ of selecteer een waarde in het veld Afgegeven goederen.</span><span class="sxs-lookup"><span data-stu-id="47761-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="47761-124">Typ een waarde in het veld Verpakking.</span><span class="sxs-lookup"><span data-stu-id="47761-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="47761-125">Typ een waarde in het veld Risiconiveau van de lading.</span><span class="sxs-lookup"><span data-stu-id="47761-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="47761-126">Typ of selecteer een waarde in het veld Vervoerder.</span><span class="sxs-lookup"><span data-stu-id="47761-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="47761-127">Typ of selecteer een waarde in het veld Model.</span><span class="sxs-lookup"><span data-stu-id="47761-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="47761-128">Typ een waarde in het veld Registratienummer.</span><span class="sxs-lookup"><span data-stu-id="47761-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="47761-129">Typ een waarde in het veld Trailerregistratienummer.</span><span class="sxs-lookup"><span data-stu-id="47761-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="47761-130">Typ of selecteer een waarde in het veld Chauffeur.</span><span class="sxs-lookup"><span data-stu-id="47761-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="47761-131">Typ een waarde in het veld Naam chauffeur.</span><span class="sxs-lookup"><span data-stu-id="47761-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="47761-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="47761-132">Click Save.</span></span>
15. <span data-ttu-id="47761-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="47761-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="47761-134">Pakbon voor de niet-geboekte transferferorder weergeven</span><span class="sxs-lookup"><span data-stu-id="47761-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="47761-135">Klik op Pakbon.</span><span class="sxs-lookup"><span data-stu-id="47761-135">Click Packing slip.</span></span>
2. <span data-ttu-id="47761-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="47761-136">Click OK.</span></span>
3. <span data-ttu-id="47761-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="47761-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="47761-138">Pakbon voor de geboekte transferferorder weergeven</span><span class="sxs-lookup"><span data-stu-id="47761-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="47761-139">Klik in het actievenster op Transferorder.</span><span class="sxs-lookup"><span data-stu-id="47761-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="47761-140">Klik in het actievenster op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="47761-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="47761-141">Klik op Verzenden transferorders.</span><span class="sxs-lookup"><span data-stu-id="47761-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="47761-142">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="47761-142">Click the General tab.</span></span>
5. <span data-ttu-id="47761-143">Selecteer een optie in het veld Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="47761-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="47761-144">Klik op het tabblad Overzicht.</span><span class="sxs-lookup"><span data-stu-id="47761-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="47761-145">Typ een waarde in het veld Pakbon.</span><span class="sxs-lookup"><span data-stu-id="47761-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="47761-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="47761-146">Click OK.</span></span>
9. <span data-ttu-id="47761-147">Klik in het actievenster op Verzenden.</span><span class="sxs-lookup"><span data-stu-id="47761-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="47761-148">Klik op Pakbon.</span><span class="sxs-lookup"><span data-stu-id="47761-148">Click Packing slip.</span></span>
11. <span data-ttu-id="47761-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="47761-149">Click OK.</span></span>


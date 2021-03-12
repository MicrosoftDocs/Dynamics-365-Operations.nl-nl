---
title: Problemen met ladingopbouw en zendingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met ladingopbouw en zendingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994024"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="b543e-103">Problemen met ladingopbouw en zendingen oplossen</span><span class="sxs-lookup"><span data-stu-id="b543e-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b543e-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met ladingopbouw en zendingen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b543e-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="b543e-105">Het volgende foutbericht wordt weergegeven: "U kunt geen ladingsregel maken voor deze orderregel omdat deze voorraaddimensies bevat die ongeldig zijn...'</span><span class="sxs-lookup"><span data-stu-id="b543e-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b543e-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="b543e-106">Issue description</span></span>

<span data-ttu-id="b543e-107">Het volgende foutbericht wordt weergegeven wanneer u een retourverkooporder probeert vrij te geven aan het magazijn:</span><span class="sxs-lookup"><span data-stu-id="b543e-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="b543e-108">U kunt geen ladingsregel maken voor deze orderregel omdat deze voorraaddimensies bevat die ongeldig zijn.</span><span class="sxs-lookup"><span data-stu-id="b543e-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="b543e-109">U kunt niet verwijzen naar voorraaddimensies die zich onder de locatiedimensie in de reserveringshiërarchie bevinden.</span><span class="sxs-lookup"><span data-stu-id="b543e-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="b543e-110">Verwijder de ongeldige dimensies uit de orderregel.</span><span class="sxs-lookup"><span data-stu-id="b543e-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b543e-111">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="b543e-111">Issue resolution</span></span>

<span data-ttu-id="b543e-112">Helaas ondersteunt het product geen ladingsverwerking voor een verkoopretourproces.</span><span class="sxs-lookup"><span data-stu-id="b543e-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="b543e-113">Daarom kunt u de retourverkooporder niet vrijgeven aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="b543e-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="b543e-114">Op verkoopordertransacties kunt u niet verwijzen naar voorraaddimensies die zich onder de **Locatie**-dimensie in de reserveringshiërarchie bevinden.</span><span class="sxs-lookup"><span data-stu-id="b543e-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="b543e-115">Verwijder de ongeldige dimensies uit de orderregel om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="b543e-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="b543e-116">Het volgende fout bericht wordt weergegeven: "Een van de regels bevindt zich al in een lading.</span><span class="sxs-lookup"><span data-stu-id="b543e-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="b543e-117">Vrijgeven aan magazijn is niet mogelijk."</span><span class="sxs-lookup"><span data-stu-id="b543e-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b543e-118">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="b543e-118">Issue description</span></span>

<span data-ttu-id="b543e-119">Als u handmatig taken maakt of als u het proces zo instelt dat er al ladingen zijn gemaakt voordat de verkooporderregel wordt ingevoerd, is de veronderstelling dat de volgende vrijgave handmatig wordt uitgevoerd en dat de route en beoordeling van de lading wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b543e-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="b543e-120">In een ander mogelijk scenario probeert u een automatische vrijgave aan het magazijn uit te voeren, maar tijdens het waveproces kan er geen werk worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b543e-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="b543e-121">Daarom wordt toch een openstaande zending of lading gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b543e-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="b543e-122">Deze openstaande zending of lading blokkeert vervolgens alle pogingen om de order automatisch vrij te geven, totdat u de openstaande zending of lading verwijdert of de wave handmatig opnieuw verwerkt.</span><span class="sxs-lookup"><span data-stu-id="b543e-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b543e-123">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="b543e-123">Issue resolution</span></span>

<span data-ttu-id="b543e-124">U kunt alleen vrijgeven vanaf de verkooporderpagina of automatische vrijgave uitvoeren vanaf de vrijgaveverkooporderpagina als er geen lading bestaat voorafgaand aan de vrijgave aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="b543e-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="b543e-125">De lading wordt automatisch gemaakt nadat de wave is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="b543e-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="b543e-126">Het volgende foutbericht wordt weergegeven: "De correctie van het afleveringsbewijs kan niet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="b543e-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="b543e-127">Het afleveringsbewijs bevat alleen artikelen die onder magazijnbeheerprocessen vallen, aangezien deze niet worden ondersteund door afleveringsbewijscorrectie."</span><span class="sxs-lookup"><span data-stu-id="b543e-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b543e-128">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="b543e-128">Issue description</span></span>

<span data-ttu-id="b543e-129">Nadat u een afleveringsbewijs hebt geboekt, kunt u deze niet meer annuleren, omdat de knop **Annuleren** niet beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="b543e-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="b543e-130">U kunt het afleveringsbewijs ook niet corrigeren.</span><span class="sxs-lookup"><span data-stu-id="b543e-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="b543e-131">Als u dat probeert, wordt dit foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b543e-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b543e-132">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="b543e-132">Issue resolution</span></span>

<span data-ttu-id="b543e-133">Als u geboekte pakbonnen wilt corrigeren voor artikelen die zijn ingeschakeld voor geavanceerd magazijnbeheer (WMS), moet u de boeking uitvoeren vanuit de lading, niet rechtstreeks vanuit de order.</span><span class="sxs-lookup"><span data-stu-id="b543e-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="b543e-134">Hoe kan ik werk maken vanuit uitgaande ladingen in plaats van waves?</span><span class="sxs-lookup"><span data-stu-id="b543e-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="b543e-135">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="b543e-135">Issue description</span></span>

<span data-ttu-id="b543e-136">Dit is een manier om dit probleem te reproduceren.</span><span class="sxs-lookup"><span data-stu-id="b543e-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="b543e-137">Maak een uitgaande lading met een verkooporde of een transferorder.</span><span class="sxs-lookup"><span data-stu-id="b543e-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="b543e-138">Geef de lading vrij naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="b543e-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="b543e-139">U ziet dat er nog geen orderverzamelingwerk is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="b543e-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b543e-140">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="b543e-140">Issue resolution</span></span>

<span data-ttu-id="b543e-141">Als werk onmiddellijk moet worden gegenereerd wanneer de lading wordt vrijgegeven, moet u de wavesjabloon dienovereenkomstig configureren.</span><span class="sxs-lookup"><span data-stu-id="b543e-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="b543e-142">Stel op de wavesjabloon de volgende opties in op *Ja*:</span><span class="sxs-lookup"><span data-stu-id="b543e-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="b543e-143">Het maken van waves automatiseren</span><span class="sxs-lookup"><span data-stu-id="b543e-143">Automate wave creation</span></span>
- <span data-ttu-id="b543e-144">Wave verwerken bij vrijgave door magazijn</span><span class="sxs-lookup"><span data-stu-id="b543e-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="b543e-145">Vrijgave wave automatiseren</span><span class="sxs-lookup"><span data-stu-id="b543e-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="b543e-146">Ik kan een gedeeltelijk verzonden lading niet opnieuw vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="b543e-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b543e-147">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="b543e-147">Issue description</span></span>

<span data-ttu-id="b543e-148">U kunt een gedeeltelijk verzonden lading niet vrijgeven aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="b543e-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="b543e-149">Wanneer u de vrijgave aan het magazijn uitvoert, wordt er een bericht weergegeven dat de bewerking is voltooid, maar gebeurt er niets en wordt er geen werk gemaakt voor de resterende hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="b543e-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="b543e-150">Dit probleem treedt op wanneer u de transportladingsfunctie gebruikt en er een onvolledige reservering is.</span><span class="sxs-lookup"><span data-stu-id="b543e-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b543e-151">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="b543e-151">Issue resolution</span></span>

<span data-ttu-id="b543e-152">[KB-probleem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Gedeeltelijk verzonden ladingen kunnen opnieuw in een wave worden geplaatst en verwerkt") is in [release 10.0.15 gecorrigeerd](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="b543e-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>

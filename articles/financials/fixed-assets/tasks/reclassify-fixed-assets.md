--- 
title: Vaste activa opnieuw classificeren
description: Als u een activum opnieuw wilt classificeren, moet u dit overbrengen naar een nieuwe vaste-activagroep of er een nieuw vaste-activanummer aan toewijzen binnen dezelfde groep.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 02afc142187aed55e5186d83069c5419fc900106
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="fa2bd-103">Vaste activa opnieuw classificeren</span><span class="sxs-lookup"><span data-stu-id="fa2bd-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa2bd-104">Als u een activum opnieuw wilt classificeren, moet u dit overbrengen naar een nieuwe vaste-activagroep of er een nieuw vaste-activanummer aan toewijzen binnen dezelfde groep.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="fa2bd-105">Wanneer een vast activum opnieuw wordt ingedeeld:</span><span class="sxs-lookup"><span data-stu-id="fa2bd-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="fa2bd-106">• Alle waardemodellen voor het bestaande vaste activum worden gemaakt voor het nieuwe vaste activum.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="fa2bd-107">Informatie die was ingesteld voor het oorspronkelijke vaste activum is naar het nieuwe vaste activum gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="fa2bd-108">De status van de waardemodellen voor het oorspronkelijke vaste activum is Gesloten.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="fa2bd-109">• De nieuwe waardemodellen van het nieuwe vaste activum bevatten de datum van het opnieuw classificeren in het veld Verwervingsdatum.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="fa2bd-110">De datum in het veld Uitvoeringsdatum afschrijving is gekopieerd uit de oorspronkelijke activumgegevens.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="fa2bd-111">Als de afschrijving al is begonnen, geeft het veld Datum waarop de afschrijving het laatst is uitgevoerd de datum van het opnieuw classificeren weer.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="fa2bd-112">• De bestaande vaste-activatransacties voor het oorspronkelijke vaste activum zijn geannuleerd en opnieuw gegenereerd voor het nieuwe vaste activum.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="fa2bd-113">Ga naar Vaste activa > Periodieke taken > Herclassificatie.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="fa2bd-114">Selecteer in het veld Vaste-activagroep de groep die u opnieuw wilt classificeren.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-114">In the Fixed asset group field, select the group to reclassify.</span></span>
3. <span data-ttu-id="fa2bd-115">Selecteer in het veld Vaste-activanummer het activanummer van het activum dat u opnieuw wilt classificeren.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="fa2bd-116">Selecteer in het veld Nieuwe groep vaste activa een groep waarnaar u het vaste activum wilt overboeken.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="fa2bd-117">Als de nieuwe vaste-activagroep aan een nummerreeks is gekoppeld, wordt het veld Nieuw nummer voor vaste activa bijgewerkt met het nummer uit de nummerreeks voor de nieuwe vaste-activagroep.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="fa2bd-118">Anders wordt het veld Nieuw nummer voor vaste activa bijgewerkt met het nummer uit de nummerreeks die is geconfigureerd op de pagina Vaste-activaparameters.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="fa2bd-119">Als op de pagina Vaste-activaparameters geen nummerrreeks is geconfigureerd, typ dan een nummer in het veld Nieuw nummer voor vaste activa .</span><span class="sxs-lookup"><span data-stu-id="fa2bd-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="fa2bd-120">Typ een datum in het datumveld Datum herclassificatie.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="fa2bd-121">Typ of selecteer een waarde in het veld Boekstuknummering.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="fa2bd-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-122">Click OK.</span></span>



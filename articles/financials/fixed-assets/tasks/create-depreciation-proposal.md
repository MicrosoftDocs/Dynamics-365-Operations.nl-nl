--- 
title: Een afschrijvingsvoorstel maken
description: Deze procedure beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa.
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="56738-103">Een afschrijvingsvoorstel maken</span><span class="sxs-lookup"><span data-stu-id="56738-103">Create a depreciation proposal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56738-104">Deze procedure beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="56738-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="56738-105">Deze taak gebruikt het USMF-demobedrijf en de accountantsrol.</span><span class="sxs-lookup"><span data-stu-id="56738-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="56738-106">Afschrijvingsvoorstel maken</span><span class="sxs-lookup"><span data-stu-id="56738-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="56738-107">Ga naar Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken.</span><span class="sxs-lookup"><span data-stu-id="56738-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="56738-108">Klik in het veld Naam van journaal op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="56738-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="56738-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="56738-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="56738-110">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="56738-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="56738-111">Selecteer de optie Afschrijving samenvatten als u maandelijkse afschrijvingen in één journaalregel wilt samenvatten.</span><span class="sxs-lookup"><span data-stu-id="56738-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="56738-112">Als de waarde van Einddatum bijvoorbeeld 31 maart 2015 is, kan de volgende beschrijving worden gegenereerd: 'Afschrijving sinds 31 januari 2015'.</span><span class="sxs-lookup"><span data-stu-id="56738-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="56738-113">Het veld Datum op de voorgestelde journaalregels wordt dan ingesteld op 31 maart 2015.</span><span class="sxs-lookup"><span data-stu-id="56738-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="56738-114">Het afschrijvingsvoorstel kan worden gefilterd op activa, activagroep, of andere criteria met de optie Filteren.</span><span class="sxs-lookup"><span data-stu-id="56738-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="56738-115">Wanneer u het formulier Verwervingsvoorstellen of afschrijvingsvoorstellen maken voor vaste activa gebruikt, kunt u de afschrijving in batches voorstellen.</span><span class="sxs-lookup"><span data-stu-id="56738-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="56738-116">Dit is wat we voorstellen voor grotere voorstellen die meer systeembronnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="56738-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="56738-117">Als u de batchoptie selecteert, kunt u in die tijd nog andere taken voltooien.</span><span class="sxs-lookup"><span data-stu-id="56738-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="56738-118">Wanneer u op deze manier afschrijving voorstelt, wordt de afschrijving berekend voor waardemodellen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="56738-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="56738-119">Klik op Journaal maken.</span><span class="sxs-lookup"><span data-stu-id="56738-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="56738-120">Afschrijvingsinvoer controleren</span><span class="sxs-lookup"><span data-stu-id="56738-120">Review depreciation entries</span></span>
1. <span data-ttu-id="56738-121">Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="56738-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="56738-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="56738-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="56738-123">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="56738-123">Click Lines.</span></span>
4. <span data-ttu-id="56738-124">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="56738-124">Click Post.</span></span>



---
title: Een afschrijvingsvoorstel maken
description: Dit onderwerp beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90c24e9d89c055ea95ca5f25cd85ef4042476a90
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867602"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="ae7eb-103">Een afschrijvingsvoorstel maken</span><span class="sxs-lookup"><span data-stu-id="ae7eb-103">Create a depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae7eb-104">Dit onderwerp beschrijft hoe afschrijvingsbatchvoorstellen werken en verklaart hoe u afschrijving kunt voorstellen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="ae7eb-105">Deze taak gebruikt het USMF-demobedrijf en de accountantsrol.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="ae7eb-106">Een afschrijvingsvoorstel maken</span><span class="sxs-lookup"><span data-stu-id="ae7eb-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="ae7eb-107">Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken**.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="ae7eb-108">Selecteer in het veld **Journaalnaam** een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="ae7eb-109">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="ae7eb-110">Selecteer de optie **Afschrijving samenvatten** als u maandelijkse afschrijvingen in één journaalregel wilt samenvatten.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="ae7eb-111">Als de waarde van Einddatum bijvoorbeeld 31 maart 2015 is, kan de volgende beschrijving worden gegenereerd: 'Afschrijving sinds 31 januari 2015'.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-111">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="ae7eb-112">Het veld **Datum** op de voorgestelde journaalregels wordt dan ingesteld op 31 maart 2015.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="ae7eb-113">Het afschrijvingsvoorstel kan worden gefilterd op activa, activagroep, of andere criteria met de optie **Filteren**.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="ae7eb-114">Wanneer u het formulier **Verwervingsvoorstellen of afschrijvingsvoorstellen maken voor vaste activa** gebruikt, kunt u de afschrijving in batches voorstellen.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="ae7eb-115">Dit is wat we voorstellen voor grotere voorstellen die meer systeembronnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="ae7eb-116">Als u de batchoptie selecteert, kunt u in die tijd nog andere taken voltooien.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="ae7eb-117">Wanneer u op deze manier afschrijving voorstelt, wordt de afschrijving berekend voor waardemodellen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="ae7eb-118">Selecteer **Journaal maken**.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="ae7eb-119">Afschrijvingsinvoer controleren</span><span class="sxs-lookup"><span data-stu-id="ae7eb-119">Review depreciation entries</span></span>
1. <span data-ttu-id="ae7eb-120">Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ae7eb-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ae7eb-122">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="ae7eb-122">Select **Lines**.</span></span>
4. <span data-ttu-id="ae7eb-123">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="ae7eb-123">Select **Post**.</span></span>


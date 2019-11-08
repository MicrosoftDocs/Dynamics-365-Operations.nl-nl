---
title: Afschrijving van vaste activa in verschillende rechtspersonen berekenen
description: Een afschrijving van vaste activa kan in één stap worden uitgevoerd voor alle rechtspersonen.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187010"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="f21f2-103">Afschrijving van vaste activa in verschillende rechtspersonen berekenen</span><span class="sxs-lookup"><span data-stu-id="f21f2-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f21f2-104">Een afschrijving van vaste activa kan in één stap worden uitgevoerd voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="f21f2-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="f21f2-105">Deze procedure laat zien hoe u het proces instelt en uitvoert voor meerdere rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="f21f2-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="f21f2-106">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="f21f2-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="f21f2-107">Afschrijvingsjournalen voor het hele bedrijf instellen</span><span class="sxs-lookup"><span data-stu-id="f21f2-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="f21f2-108">Ga naar Vaste activa > Instellen > Parameters vaste activa.</span><span class="sxs-lookup"><span data-stu-id="f21f2-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="f21f2-109">Vouw de sectie Voorstellen voor vaste activa uit.</span><span class="sxs-lookup"><span data-stu-id="f21f2-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="f21f2-110">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f21f2-110">Click Add.</span></span>
4. <span data-ttu-id="f21f2-111">Typ of selecteer een waarde in het veld Boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="f21f2-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="f21f2-112">Typ of selecteer een waarde in het veld Journaalnaam.</span><span class="sxs-lookup"><span data-stu-id="f21f2-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="f21f2-113">Herhaal de journaalinstellingen op de pagina Vaste-activaparameters voor elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="f21f2-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="f21f2-114">Afschrijving uitvoeren</span><span class="sxs-lookup"><span data-stu-id="f21f2-114">Depreciation run</span></span>
1. <span data-ttu-id="f21f2-115">Ga naar Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken.</span><span class="sxs-lookup"><span data-stu-id="f21f2-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="f21f2-116">Typ of selecteer een waarde in het veld Boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="f21f2-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="f21f2-117">De journaalnaam wordt standaard ingesteld op basis van de vaste-activaparameters.</span><span class="sxs-lookup"><span data-stu-id="f21f2-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="f21f2-118">De naam kan hier worden gewijzigd voor de huidige rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="f21f2-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="f21f2-119">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="f21f2-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="f21f2-120">Selecteer de rechtspersonen die in de afschrijvingsuitvoering moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f21f2-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="f21f2-121">Alleen rechtspersonen met journalen die zijn ingesteld voor voorstellen voor vaste activa op de pagina Voorstellen voor vaste activa worden weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f21f2-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="f21f2-122">Selecteer Ja in het veld Journalen boeken.</span><span class="sxs-lookup"><span data-stu-id="f21f2-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="f21f2-123">Filtervelden omvatten alle vaste activa, groepen en boeken voor de rechtspersonen die zijn geselecteerd voor deze afschrijvingsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="f21f2-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="f21f2-124">De optie Batchverwerking is standaard ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f21f2-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="f21f2-125">Als deze optie is ingeschakeld, wordt het proces voor maken en boeken van het afschrijvingsjournaal op de achtergrond uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f21f2-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="f21f2-126">Klik op Journaal maken.</span><span class="sxs-lookup"><span data-stu-id="f21f2-126">Click Create journal.</span></span>
6. <span data-ttu-id="f21f2-127">Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="f21f2-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

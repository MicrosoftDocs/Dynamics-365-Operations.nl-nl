--- 
title: Afschrijving van vaste activa in verschillende rechtspersonen berekenen
description: Deze procedure laat zien hoe u het afschrijvingsproces instelt en uitvoert voor meerdere rechtspersonen.
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4221acf200f41ca39803bcd56c1b05e0d87bd948
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="79bad-103">Afschrijving van vaste activa in verschillende rechtspersonen berekenen</span><span class="sxs-lookup"><span data-stu-id="79bad-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79bad-104">Een afschrijving van vaste activa kan in één stap worden uitgevoerd voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="79bad-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="79bad-105">Deze procedure laat zien hoe u het proces instelt en uitvoert voor meerdere rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="79bad-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="79bad-106">Hiervoor wordt de rol Accountant gebruikt.</span><span class="sxs-lookup"><span data-stu-id="79bad-106">It uses the accountant role.</span></span>  

<span data-ttu-id="79bad-107">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="79bad-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="79bad-108">Deeltaak voor stappen (16): afschrijvingsjournalen voor het hele bedrijf instellen</span><span class="sxs-lookup"><span data-stu-id="79bad-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="79bad-109">U moet eerst de journalen instellen die in elke rechtspersoon moeten worden gebruikt in de afschrijving voor het hele bedrijf.</span><span class="sxs-lookup"><span data-stu-id="79bad-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="79bad-110">Ga naar Vaste activa > Instellen > Parameters vaste activa.</span><span class="sxs-lookup"><span data-stu-id="79bad-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="79bad-111">Vouw de sectie Voorstellen voor vaste activa uit.</span><span class="sxs-lookup"><span data-stu-id="79bad-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="79bad-112">Maak een record met de journaalnaam die moet worden gebruikt voor elke boekingslaag in de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="79bad-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="79bad-113">Als boeken niet naar het grootboek worden geboekt, moet de boekingslaag Geen worden geselecteerd met het bijbehorende journaal.</span><span class="sxs-lookup"><span data-stu-id="79bad-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="79bad-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="79bad-114">Click Add.</span></span> 
4. <span data-ttu-id="79bad-115">Typ of selecteer een waarde in het veld Boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="79bad-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="79bad-116">Typ of selecteer een waarde in het veld Journaalnaam.</span><span class="sxs-lookup"><span data-stu-id="79bad-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="79bad-117">Herhaal de journaalinstellingen op de pagina Vaste-activaparameters voor elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="79bad-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="79bad-118">Deeltaak: afschrijving berekenen</span><span class="sxs-lookup"><span data-stu-id="79bad-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="79bad-119">Op de pagina Afschrijvingsvoorstel maken kunt u uw afschrijvingsjournaal voor rechtspersonen starten.</span><span class="sxs-lookup"><span data-stu-id="79bad-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="79bad-120">Ga naar Vaste activa > Journaalboekingen > Afschrijvingsvoorstel maken.</span><span class="sxs-lookup"><span data-stu-id="79bad-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="79bad-121">Typ of selecteer een waarde in het veld Boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="79bad-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="79bad-122">De journaalnaam wordt standaard ingesteld op basis van de vaste-activaparameters.</span><span class="sxs-lookup"><span data-stu-id="79bad-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="79bad-123">De naam kan hier worden gewijzigd voor de huidige rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="79bad-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="79bad-124">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="79bad-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="79bad-125">Selecteer de rechtspersonen die in de afschrijvingsuitvoering moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="79bad-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="79bad-126">Alleen rechtspersonen met journalen die zijn ingesteld voor voorstellen voor vaste activa op de pagina Voorstellen voor vaste activa worden weergegeven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="79bad-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="79bad-127">Indien ingeschakeld worden met de optie Journalen boeken de afschrijvingsjournalen automatisch geboekt wanneer ze worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="79bad-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="79bad-128">Als deze optie niet is geselecteerd, worden de journalen gemaakt, maar niet geboekt, zodat u de details vóór het boeken kunt bekijken.</span><span class="sxs-lookup"><span data-stu-id="79bad-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="79bad-129">Selecteer Ja in het veld Journalen boeken.</span><span class="sxs-lookup"><span data-stu-id="79bad-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="79bad-130">Filtervelden omvatten alle vaste activa, groepen en boeken voor de rechtspersonen die zijn geselecteerd voor deze afschrijvingsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="79bad-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="79bad-131">De optie Batchverwerking is standaard ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="79bad-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="79bad-132">Als deze optie is ingeschakeld, wordt het proces voor maken en boeken van het afschrijvingsjournaal op de achtergrond uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="79bad-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="79bad-133">Klik op Journaal maken.</span><span class="sxs-lookup"><span data-stu-id="79bad-133">Click Create journal.</span></span> 
10. <span data-ttu-id="79bad-134">U moet de afschrijvingsjournalen bekijken die in de betreffende rechtspersonen zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="79bad-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="79bad-135">Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="79bad-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>


--- 
title: Aanmaningen verwerken
description: Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: fe76f2934360580c4015ea13225b9228cc2780b9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="b9487-103">Aanmaningen verwerken</span><span class="sxs-lookup"><span data-stu-id="b9487-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9487-104">Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt.</span><span class="sxs-lookup"><span data-stu-id="b9487-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="b9487-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b9487-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="b9487-106">Een aanmaningsreeks instellen op het boekingsprofiel</span><span class="sxs-lookup"><span data-stu-id="b9487-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="b9487-107">Ga naar Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant.</span><span class="sxs-lookup"><span data-stu-id="b9487-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="b9487-108">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b9487-108">Click Edit.</span></span>
    * <span data-ttu-id="b9487-109">Selecteer een aanmaningsreeks in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="b9487-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="b9487-110">Als u geen aanmaningen wilt genereren voor transacties met dit boekingsprofiel, laat u het veld leeg.</span><span class="sxs-lookup"><span data-stu-id="b9487-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="b9487-111">Met het tabblad Tabelbeperking kunt u de methode wijzigen waarmee aanmaningen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="b9487-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="b9487-112">Als dit veld is ingesteld op Ja, worden aanmaningen gemaakt voor dit boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="b9487-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="b9487-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b9487-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="b9487-114">Aanmaningen maken</span><span class="sxs-lookup"><span data-stu-id="b9487-114">Create collection letters</span></span>
1. <span data-ttu-id="b9487-115">Ga naar Crediteren en aanmaningen > Aanmaning > Aanmaningen maken.</span><span class="sxs-lookup"><span data-stu-id="b9487-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="b9487-116">U moet de transactietypen selecteren waarvoor u aanmaningen wilt verzamelen.</span><span class="sxs-lookup"><span data-stu-id="b9487-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="b9487-117">Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.</span><span class="sxs-lookup"><span data-stu-id="b9487-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="b9487-118">Selecteer een optie in het veld Aanmaning.</span><span class="sxs-lookup"><span data-stu-id="b9487-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="b9487-119">Voer de datum van de aanmaning in.</span><span class="sxs-lookup"><span data-stu-id="b9487-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="b9487-120">Er zijn twee boekingsprofielopties: Rekening: gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor elke rentenota.</span><span class="sxs-lookup"><span data-stu-id="b9487-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="b9487-121">Selecteren - Gebruik het boekingsprofiel dat u selecteert in het veld Boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="b9487-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="b9487-122">Selecteer een boekingsprofiel als u 'Boekingsprofiel gebruiken van' hebt gewijzigd in 'Selecteren'.</span><span class="sxs-lookup"><span data-stu-id="b9487-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="b9487-123">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="b9487-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="b9487-124">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="b9487-124">Click Filter.</span></span>
6. <span data-ttu-id="b9487-125">Voer in het veld Criteria een klant-id in.</span><span class="sxs-lookup"><span data-stu-id="b9487-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="b9487-126">U kunt bijvoorbeeld 'US-001' invoeren.</span><span class="sxs-lookup"><span data-stu-id="b9487-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="b9487-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9487-127">Click OK.</span></span>
8. <span data-ttu-id="b9487-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9487-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="b9487-129">Aanmaningen afdrukken</span><span class="sxs-lookup"><span data-stu-id="b9487-129">Print collection letters</span></span>
1. <span data-ttu-id="b9487-130">Ga naar Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken.</span><span class="sxs-lookup"><span data-stu-id="b9487-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="b9487-131">Selecteer 'Gemaakt' in het veld Status.</span><span class="sxs-lookup"><span data-stu-id="b9487-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="b9487-132">Selecteer 'Niet afgedrukt' in het veld Afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="b9487-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="b9487-133">Klik op Afdrukken.</span><span class="sxs-lookup"><span data-stu-id="b9487-133">Click Print.</span></span>
5. <span data-ttu-id="b9487-134">Klik op Notitie bij aanmaning.</span><span class="sxs-lookup"><span data-stu-id="b9487-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="b9487-135">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="b9487-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="b9487-136">De afsluitdatum voor boekingen opgeven</span><span class="sxs-lookup"><span data-stu-id="b9487-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="b9487-137">Klik op OK om de aanmaning af te drukken.</span><span class="sxs-lookup"><span data-stu-id="b9487-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="b9487-138">De aanmaning boeken</span><span class="sxs-lookup"><span data-stu-id="b9487-138">Post the collection letter</span></span>
1. <span data-ttu-id="b9487-139">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="b9487-139">Click Post.</span></span>
2. <span data-ttu-id="b9487-140">Voer de boekingsdatum voor de aanmaning in</span><span class="sxs-lookup"><span data-stu-id="b9487-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="b9487-141">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="b9487-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b9487-142">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b9487-142">Click OK.</span></span>
5. <span data-ttu-id="b9487-143">Selecteer 'Geboekt' in het veld Status.</span><span class="sxs-lookup"><span data-stu-id="b9487-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="b9487-144">Selecteer een optie in het veld Afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="b9487-144">In the Printed field, select an option.</span></span>



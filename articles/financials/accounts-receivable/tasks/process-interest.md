---
title: Rente verwerken
description: Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fba25c900461fbbf4db0cd3b93847d258704ab4e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842876"
---
# <a name="process-interest"></a><span data-ttu-id="450f7-103">Rente verwerken</span><span class="sxs-lookup"><span data-stu-id="450f7-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="450f7-104">Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt.</span><span class="sxs-lookup"><span data-stu-id="450f7-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="450f7-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="450f7-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="450f7-106">Rente instellen in het boekingsprofiel</span><span class="sxs-lookup"><span data-stu-id="450f7-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="450f7-107">Ga naar Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant.</span><span class="sxs-lookup"><span data-stu-id="450f7-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="450f7-108">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="450f7-108">Click Edit.</span></span>
    * <span data-ttu-id="450f7-109">Selecteer een rentecode in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="450f7-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="450f7-110">Als u geen rente wilt berekenen voor transacties met dit boekingsprofiel, laat u het veld leeg.</span><span class="sxs-lookup"><span data-stu-id="450f7-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="450f7-111">Met het tabblad Tabelbeperking kunt u de methode wijzigen waarop rente wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="450f7-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="450f7-112">Als dit veld is ingesteld op Ja, wordt rente berekend voor dit boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="450f7-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="450f7-113">Rente berekenen</span><span class="sxs-lookup"><span data-stu-id="450f7-113">Calculate interest</span></span>
1. <span data-ttu-id="450f7-114">Ga naar Crediteringen en aanmaningen > Rente > Rentenota's maken.</span><span class="sxs-lookup"><span data-stu-id="450f7-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="450f7-115">U moet de transactietypen selecteren waarvoor u rente wilt berekenen.</span><span class="sxs-lookup"><span data-stu-id="450f7-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="450f7-116">Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.</span><span class="sxs-lookup"><span data-stu-id="450f7-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="450f7-117">Als u Rente selecteert, wordt rente op rente berekend.</span><span class="sxs-lookup"><span data-stu-id="450f7-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="450f7-118">U kunt de wetten die de berekening van rente op rente bepalen controleren voordat u deze transacties opneemt.</span><span class="sxs-lookup"><span data-stu-id="450f7-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="450f7-119">Er wordt rente berekend vanaf deze datum tot aan de "Einddatum".</span><span class="sxs-lookup"><span data-stu-id="450f7-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="450f7-120">Als u geen specifieke "Begindatum" opgeeft, worden alle niet-geboekte rentenota's geannuleerd en wordt de rente opnieuw berekend vanaf de transactiedatum.</span><span class="sxs-lookup"><span data-stu-id="450f7-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="450f7-121">Voer de datum van de rentenota in.</span><span class="sxs-lookup"><span data-stu-id="450f7-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="450f7-122">Er zijn drie boekingsprofielopties: Rekening - gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor iedere rentenota.</span><span class="sxs-lookup"><span data-stu-id="450f7-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="450f7-123">Selecteren - Gebruik het boekingsprofiel dat u selecteert in het veld Boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="450f7-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="450f7-124">Transactie - Gebruik het afzonderlijke boekingsprofiel van transacties waarbij rente wordt berekend voor elke rentenota.</span><span class="sxs-lookup"><span data-stu-id="450f7-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="450f7-125">Transacties waaraan geen boekingsprofiel is toegewezen maken gebruik van het boekingsprofiel dat is opgegeven in het gebied Grootboek en btw van het formulier Parameters van module Klanten.</span><span class="sxs-lookup"><span data-stu-id="450f7-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="450f7-126">Selecteer hier een boekingsprofiel als u "Boekingsprofiel gebruiken van" hebt gewijzigd in "Selecteren".</span><span class="sxs-lookup"><span data-stu-id="450f7-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="450f7-127">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="450f7-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="450f7-128">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="450f7-128">Click Filter.</span></span>
5. <span data-ttu-id="450f7-129">Voer in het veld Criteria een klant-id in.</span><span class="sxs-lookup"><span data-stu-id="450f7-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="450f7-130">U kunt bijvoorbeeld 'US-001' invoeren.</span><span class="sxs-lookup"><span data-stu-id="450f7-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="450f7-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="450f7-131">Click OK.</span></span>
7. <span data-ttu-id="450f7-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="450f7-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="450f7-133">Rentenota's afdrukken</span><span class="sxs-lookup"><span data-stu-id="450f7-133">Print interest notes</span></span>
1. <span data-ttu-id="450f7-134">Ga naar Crediteringen en aanmaningen > Rente > Rentenota's controleren en verwerken.</span><span class="sxs-lookup"><span data-stu-id="450f7-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="450f7-135">Selecteer 'Gemaakt' in het veld Status.</span><span class="sxs-lookup"><span data-stu-id="450f7-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="450f7-136">Selecteer 'Niet afgedrukt' in het veld Afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="450f7-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="450f7-137">Klik op Afdrukken.</span><span class="sxs-lookup"><span data-stu-id="450f7-137">Click Print.</span></span>
5. <span data-ttu-id="450f7-138">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="450f7-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="450f7-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="450f7-139">Click OK.</span></span>
7. <span data-ttu-id="450f7-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="450f7-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="450f7-141">De rentenota boeken</span><span class="sxs-lookup"><span data-stu-id="450f7-141">Post the interest note</span></span>
1. <span data-ttu-id="450f7-142">Selecteer een rentenota die gereed is om te worden geboekt (status is Gemaakt).</span><span class="sxs-lookup"><span data-stu-id="450f7-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="450f7-143">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="450f7-143">Click Post.</span></span>
3. <span data-ttu-id="450f7-144">Voer de boekingsdatum voor de rentenota in.</span><span class="sxs-lookup"><span data-stu-id="450f7-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="450f7-145">Schakel Ja in om een grootboektransactie te maken voor elke rentenota.</span><span class="sxs-lookup"><span data-stu-id="450f7-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="450f7-146">Als u Ja niet inschakelt, wordt de rente op alle rentenota's aan de klant opgeteld en in één transactie naar het grootboek geboekt.</span><span class="sxs-lookup"><span data-stu-id="450f7-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="450f7-147">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="450f7-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="450f7-148">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="450f7-148">Click OK.</span></span>
6. <span data-ttu-id="450f7-149">Selecteer 'Geboekt' in het veld Status.</span><span class="sxs-lookup"><span data-stu-id="450f7-149">In the Status field, select 'Posted'.</span></span>


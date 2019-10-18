---
title: Rente verwerken
description: Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188758"
---
# <a name="process-interest"></a><span data-ttu-id="eab25-103">Rente verwerken</span><span class="sxs-lookup"><span data-stu-id="eab25-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eab25-104">Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt.</span><span class="sxs-lookup"><span data-stu-id="eab25-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="eab25-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eab25-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="eab25-106">Rente instellen in het boekingsprofiel</span><span class="sxs-lookup"><span data-stu-id="eab25-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="eab25-107">Ga in het **navigatievenster** naar **Modules > Crediteringen en aanmaningen > Instellen > Boekingsprofielen van klant**.</span><span class="sxs-lookup"><span data-stu-id="eab25-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="eab25-108">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="eab25-108">Click **Edit**.</span></span>
3. <span data-ttu-id="eab25-109">Selecteer op het sneltabblad **Instellingen** in het veld **Rentecode** een rentecode in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="eab25-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="eab25-110">Als u geen rente wilt berekenen voor transacties met dit boekingsprofiel, laat u het veld leeg.</span><span class="sxs-lookup"><span data-stu-id="eab25-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="eab25-111">Via het sneltabblad **Tabelbeperking** kunt u de methode wijzigen waarop rente wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="eab25-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="eab25-112">Als dit veld is ingesteld op Ja, wordt rente berekend voor dit boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="eab25-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="eab25-113">Rente berekenen</span><span class="sxs-lookup"><span data-stu-id="eab25-113">Calculate interest</span></span>
1. <span data-ttu-id="eab25-114">Ga in het **navigatievenster** naar **Modules > Crediteringen en aanmaningen > Rente > Rentenota's maken**.</span><span class="sxs-lookup"><span data-stu-id="eab25-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="eab25-115">U moet de transactietypen selecteren waarvoor u rente wilt berekenen.</span><span class="sxs-lookup"><span data-stu-id="eab25-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="eab25-116">Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.</span><span class="sxs-lookup"><span data-stu-id="eab25-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="eab25-117">Als u **Rente** instelt op Ja, wordt rente op rente berekend.</span><span class="sxs-lookup"><span data-stu-id="eab25-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="eab25-118">U kunt de wetten die de berekening van rente op rente bepalen controleren voordat u deze transacties opneemt.</span><span class="sxs-lookup"><span data-stu-id="eab25-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="eab25-119">Voer in het veld **Begindatum** een begindatum voor de berekening van rente in.</span><span class="sxs-lookup"><span data-stu-id="eab25-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="eab25-120">Als u geen specifieke **begindatum** opgeeft, worden alle niet-geboekte rentenota's geannuleerd en wordt de rente opnieuw berekend vanaf de transactiedatum.</span><span class="sxs-lookup"><span data-stu-id="eab25-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="eab25-121">Voer in het veld **Einddatum** een einddatum voor de berekening van rente in.</span><span class="sxs-lookup"><span data-stu-id="eab25-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="eab25-122">Selecteer een optie in het veld **Boekingsprofiel gebruiken van**.</span><span class="sxs-lookup"><span data-stu-id="eab25-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="eab25-123">Er zijn drie boekingsprofielopties:</span><span class="sxs-lookup"><span data-stu-id="eab25-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="eab25-124">Rekening – Gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor iedere rentenota.</span><span class="sxs-lookup"><span data-stu-id="eab25-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="eab25-125">Selecteren - Gebruik het boekingsprofiel dat u selecteert in het veld Boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="eab25-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="eab25-126">Transactie - Gebruik het afzonderlijke boekingsprofiel van transacties waarbij rente wordt berekend voor elke rentenota.</span><span class="sxs-lookup"><span data-stu-id="eab25-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="eab25-127">Transacties waaraan geen boekingsprofiel is toegewezen maken gebruik van het boekingsprofiel dat is opgegeven in het gebied Grootboek en btw van het formulier Parameters van module Klanten.</span><span class="sxs-lookup"><span data-stu-id="eab25-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="eab25-128">Vouw het sneltabblad **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="eab25-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="eab25-129">Klik op **Filter**.</span><span class="sxs-lookup"><span data-stu-id="eab25-129">Click **Filter**.</span></span>
9. <span data-ttu-id="eab25-130">Voer in het veld **Criteria** een klant-id in.</span><span class="sxs-lookup"><span data-stu-id="eab25-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="eab25-131">U kunt bijvoorbeeld 'US-001' invoeren.</span><span class="sxs-lookup"><span data-stu-id="eab25-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="eab25-132">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="eab25-132">Click **OK**.</span></span>
7. <span data-ttu-id="eab25-133">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="eab25-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="eab25-134">Rentenota's afdrukken</span><span class="sxs-lookup"><span data-stu-id="eab25-134">Print interest notes</span></span>
1. <span data-ttu-id="eab25-135">Ga in het **navigatievenster** naar **Modules > Crediteringen en aanmaningen > Rente > Rentenota's controleren en verwerken**.</span><span class="sxs-lookup"><span data-stu-id="eab25-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="eab25-136">Selecteer Gemaakt in het veld **Status**.</span><span class="sxs-lookup"><span data-stu-id="eab25-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="eab25-137">Selecteer Niet afgedrukt in het veld **Afgedrukt**.</span><span class="sxs-lookup"><span data-stu-id="eab25-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="eab25-138">Klik op **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="eab25-138">Click **Print**.</span></span>
5. <span data-ttu-id="eab25-139">Vouw het sneltabblad **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="eab25-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="eab25-140">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="eab25-140">Click **OK**.</span></span>
7. <span data-ttu-id="eab25-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eab25-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="eab25-142">De rentenota boeken</span><span class="sxs-lookup"><span data-stu-id="eab25-142">Post the interest note</span></span>
1. <span data-ttu-id="eab25-143">Selecteer een rentenota die gereed is om te worden geboekt (status is Gemaakt).</span><span class="sxs-lookup"><span data-stu-id="eab25-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="eab25-144">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="eab25-144">Click **Post**.</span></span>
3. <span data-ttu-id="eab25-145">Voer de boekingsdatum voor de rentenota in.</span><span class="sxs-lookup"><span data-stu-id="eab25-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="eab25-146">Schakel Ja in om een grootboektransactie te maken voor elke rentenota.</span><span class="sxs-lookup"><span data-stu-id="eab25-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="eab25-147">Als u Ja niet inschakelt, wordt de rente op alle rentenota's aan de klant opgeteld en in één transactie naar het grootboek geboekt.</span><span class="sxs-lookup"><span data-stu-id="eab25-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="eab25-148">Vouw het sneltabblad **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="eab25-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="eab25-149">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="eab25-149">Click **OK**.</span></span>
6. <span data-ttu-id="eab25-150">Selecteer Geboekt in het veld **Status**.</span><span class="sxs-lookup"><span data-stu-id="eab25-150">In the **Status** field, select 'Posted'.</span></span>


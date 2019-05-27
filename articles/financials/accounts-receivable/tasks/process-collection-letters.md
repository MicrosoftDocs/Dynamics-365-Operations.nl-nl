---
title: Aanmaningen verwerken
description: Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549624"
---
# <a name="process-collection-letters"></a><span data-ttu-id="36271-103">Aanmaningen verwerken</span><span class="sxs-lookup"><span data-stu-id="36271-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36271-104">Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt.</span><span class="sxs-lookup"><span data-stu-id="36271-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="36271-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="36271-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="36271-106">Een aanmaningsreeks instellen op het boekingsprofiel</span><span class="sxs-lookup"><span data-stu-id="36271-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="36271-107">Ga naar **Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant**.</span><span class="sxs-lookup"><span data-stu-id="36271-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="36271-108">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="36271-108">Click **Edit**.</span></span>
3. <span data-ttu-id="36271-109">Selecteer een aanmaningsreeks in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="36271-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="36271-110">Als u geen aanmaningen wilt genereren voor transacties met dit boekingsprofiel, laat u het veld leeg.</span><span class="sxs-lookup"><span data-stu-id="36271-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="36271-111">Vouw het tabblad Tabelbeperkingen uit om de methode te wijzigen waarmee aanmaningen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="36271-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="36271-112">Als dit veld is ingesteld op **Ja**, worden aanmaningen gemaakt voor dit boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="36271-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="36271-113">Aanmaningen maken</span><span class="sxs-lookup"><span data-stu-id="36271-113">Create collection letters</span></span>
1. <span data-ttu-id="36271-114">Ga naar **Crediteren en aanmaningen > Aanmaning > Aanmaningen maken**.</span><span class="sxs-lookup"><span data-stu-id="36271-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="36271-115">Selecteer de transactietypen waarvoor u aanmaningen wilt verzamelen.</span><span class="sxs-lookup"><span data-stu-id="36271-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="36271-116">Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.</span><span class="sxs-lookup"><span data-stu-id="36271-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="36271-117">Selecteer een optie in het veld **Aanmaning**.</span><span class="sxs-lookup"><span data-stu-id="36271-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="36271-118">Voer de datum van de aanmaning in.</span><span class="sxs-lookup"><span data-stu-id="36271-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="36271-119">Selecteer een boekingsprofiel als u **Boekingsprofiel gebruiken van** hebt gewijzigd in **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="36271-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="36271-120">Er zijn twee boekingsprofielopties:</span><span class="sxs-lookup"><span data-stu-id="36271-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="36271-121">**Rekening** – Gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor iedere rentenota.</span><span class="sxs-lookup"><span data-stu-id="36271-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="36271-122">**Selecteren** - Gebruik het boekingsprofiel dat u selecteert in het veld **Boekingsprofiel**.</span><span class="sxs-lookup"><span data-stu-id="36271-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="36271-123">Vouw de sectie **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="36271-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="36271-124">Klik op **Filter**.</span><span class="sxs-lookup"><span data-stu-id="36271-124">Click **Filter**.</span></span>
7. <span data-ttu-id="36271-125">Voer in het veld **Criteria** een klant-id in.</span><span class="sxs-lookup"><span data-stu-id="36271-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="36271-126">U kunt bijvoorbeeld 'US-001' invoeren.</span><span class="sxs-lookup"><span data-stu-id="36271-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="36271-127">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="36271-127">Click **OK**.</span></span>
9. <span data-ttu-id="36271-128">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="36271-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="36271-129">Aanmaningen afdrukken</span><span class="sxs-lookup"><span data-stu-id="36271-129">Print collection letters</span></span>
1. <span data-ttu-id="36271-130">Ga naar **Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken**.</span><span class="sxs-lookup"><span data-stu-id="36271-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="36271-131">Selecteer **Gemaakt** in het veld **Status**.</span><span class="sxs-lookup"><span data-stu-id="36271-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="36271-132">Selecteer **Niet afgedrukt** in het veld **Afgedrukt**.</span><span class="sxs-lookup"><span data-stu-id="36271-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="36271-133">Klik op **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="36271-133">Click **Print**.</span></span>
5. <span data-ttu-id="36271-134">Klik op **Notitie bij aanmaning**.</span><span class="sxs-lookup"><span data-stu-id="36271-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="36271-135">Vouw de sectie **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="36271-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="36271-136">Geef de afsluitdatum voor boekingen op.</span><span class="sxs-lookup"><span data-stu-id="36271-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="36271-137">Klik op **OK** om de aanmaning af te drukken.</span><span class="sxs-lookup"><span data-stu-id="36271-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="36271-138">Boek de aanmaning.</span><span class="sxs-lookup"><span data-stu-id="36271-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="36271-139">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="36271-139">Click **Post**.</span></span>
   2. <span data-ttu-id="36271-140">Voer de boekingsdatum voor de aanmaning in</span><span class="sxs-lookup"><span data-stu-id="36271-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="36271-141">Vouw de sectie **Op te nemen records** uit.</span><span class="sxs-lookup"><span data-stu-id="36271-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="36271-142">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="36271-142">Click **OK**.</span></span>
   5. <span data-ttu-id="36271-143">Selecteer **Geboekt** in het veld **Status**.</span><span class="sxs-lookup"><span data-stu-id="36271-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="36271-144">Selecteer een optie in het veld **Afgedrukt**.</span><span class="sxs-lookup"><span data-stu-id="36271-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="36271-145">Aanmaningen op klantniveau beheren</span><span class="sxs-lookup"><span data-stu-id="36271-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="36271-146">U kunt ook aanmaningen op het klantenniveau instellen zodat de aanmaningscode voor elke transactie wordt bijgehouden, maar de verwerking van de aanmaning wordt gebaseerd op één aanmaningsniveau dat wordt opgeslagen voor de klant.</span><span class="sxs-lookup"><span data-stu-id="36271-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="36271-147">Deze ene aanmaning bevat alle achterstallige transacties voor de klant.</span><span class="sxs-lookup"><span data-stu-id="36271-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="36271-148">Omdat de respijtdagen nu op het klantenniveau worden bijgehouden, wordt de volgende aanmaning pas verzonden als het aantal respijtdagen voor de volgende aanmaning in de reeks is verstreken, hoewel transacties achterstallig worden als de laatste aanmaning is verzonden.</span><span class="sxs-lookup"><span data-stu-id="36271-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="36271-149">Met deze optie beperkt u het aantal aanmaningen dat u per klant verzendt.</span><span class="sxs-lookup"><span data-stu-id="36271-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="36271-150">De klant configureren om aanmaningen op klantniveau te beheren</span><span class="sxs-lookup"><span data-stu-id="36271-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="36271-151">Ga naar **Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en klik op het tabblad **Aanmaningen**.</span><span class="sxs-lookup"><span data-stu-id="36271-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="36271-152">Wijzig de waarde van **Aanmaning maken per** in **Klant**.</span><span class="sxs-lookup"><span data-stu-id="36271-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="36271-153">Ga naar **Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken**.</span><span class="sxs-lookup"><span data-stu-id="36271-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="36271-154">Voor de klant wordt slechts één aanmaning met alle achterstallige transacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="36271-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="36271-155">Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode</span><span class="sxs-lookup"><span data-stu-id="36271-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="36271-156">Als u betalingen en creditnota's opneemt in de transacties die worden opgenomen in de aanmaningen, hebt u mogelijk betalingen of creditnota's die een aanmaning activeren.</span><span class="sxs-lookup"><span data-stu-id="36271-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="36271-157">U kunt bepalen hoe betalingen en creditnota's de aanmaningscode de aanmaningscode bepalen door de waarde van de parameter **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="36271-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="36271-158">Ga als volgt te werk om betalingen en creditnota's te negeren bij het berekenen van de aanmaningscode.</span><span class="sxs-lookup"><span data-stu-id="36271-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="36271-159">Ga naar **Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en klik op het tabblad **Aanmaningen**.</span><span class="sxs-lookup"><span data-stu-id="36271-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="36271-160">Wijzig de waarde van **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="36271-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

---
title: Voorbeeld van de verwerking van aanmaningen
description: In dit onderwerp wordt een voorbeeld bekeken van het proces van het maken, afdrukken en boeken van aanmaningen.
author: JodiChristiansen
manager: AnnBe
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df4252513f9e3a02632561b4e465c98edc888ea7
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558306"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="3cc04-103">Voorbeeld van de verwerking van aanmaningen</span><span class="sxs-lookup"><span data-stu-id="3cc04-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cc04-104">In dit onderwerp wordt een voorbeeld bekeken van het proces van het maken, afdrukken en boeken van aanmaningen.</span><span class="sxs-lookup"><span data-stu-id="3cc04-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="3cc04-105">Het voorbeeld is gebaseerd op de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** in Crediteringen en aanmaningen.</span><span class="sxs-lookup"><span data-stu-id="3cc04-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="3cc04-106">Het gebruikt gegevens in het demobedrijf USMF en een nieuwe klant, US-045.</span><span class="sxs-lookup"><span data-stu-id="3cc04-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="3cc04-107">Om te beginnen gaat u naar **Klanten \> Klanten \> Alle klanten**. Vervolgens selecteert u **Nieuw** en voert u vervolgens de vereiste informatie in om klant US-045 te maken.</span><span class="sxs-lookup"><span data-stu-id="3cc04-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="3cc04-108">Voer als u gereed bent de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="3cc04-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="3cc04-109">Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningsreeks instellen** en stel de aanmaningsreeks in zoals wordt weergegeven in de volgende tabel die is toegewezen aan het klantboekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="3cc04-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="3cc04-110">Aanmaningscode</span><span class="sxs-lookup"><span data-stu-id="3cc04-110">Collection   letter code</span></span>      |     <span data-ttu-id="3cc04-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3cc04-111">Description</span></span>                           |     <span data-ttu-id="3cc04-112">Valuta</span><span class="sxs-lookup"><span data-stu-id="3cc04-112">Currency</span></span>      |     <span data-ttu-id="3cc04-113">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="3cc04-113">Main   account</span></span>        |     <span data-ttu-id="3cc04-114">Bijzondere kosten in valuta</span><span class="sxs-lookup"><span data-stu-id="3cc04-114">Fee   in currency</span></span>     |     <span data-ttu-id="3cc04-115">Minimum achterstallig saldo</span><span class="sxs-lookup"><span data-stu-id="3cc04-115">Minimum   over</span></span>        |     <span data-ttu-id="3cc04-116">Dagen blokkeren</span><span class="sxs-lookup"><span data-stu-id="3cc04-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="3cc04-117">Aanmaning 1</span><span class="sxs-lookup"><span data-stu-id="3cc04-117">Collection   letter 1</span></span>         |     <span data-ttu-id="3cc04-118">Tweede melding met bijzondere kosten</span><span class="sxs-lookup"><span data-stu-id="3cc04-118">Second   notification with fee</span></span>        |     <span data-ttu-id="3cc04-119">USD</span><span class="sxs-lookup"><span data-stu-id="3cc04-119">USD</span></span>           |                           |     <span data-ttu-id="3cc04-120">0,00</span><span class="sxs-lookup"><span data-stu-id="3cc04-120">0.00</span></span>                  |     <span data-ttu-id="3cc04-121">0,00</span><span class="sxs-lookup"><span data-stu-id="3cc04-121">0.00</span></span>                  |     <span data-ttu-id="3cc04-122">2</span><span class="sxs-lookup"><span data-stu-id="3cc04-122">2</span></span>                 |
|     <span data-ttu-id="3cc04-123">Aanmaning 2</span><span class="sxs-lookup"><span data-stu-id="3cc04-123">Collection   letter 2</span></span>         |     <span data-ttu-id="3cc04-124">Tweede melding met bijzondere kosten</span><span class="sxs-lookup"><span data-stu-id="3cc04-124">Second   notification with fee</span></span>        |     <span data-ttu-id="3cc04-125">USC</span><span class="sxs-lookup"><span data-stu-id="3cc04-125">USC</span></span>           |     <span data-ttu-id="3cc04-126">403150</span><span class="sxs-lookup"><span data-stu-id="3cc04-126">403150</span></span>                |     <span data-ttu-id="3cc04-127">20.00</span><span class="sxs-lookup"><span data-stu-id="3cc04-127">20.00</span></span>                 |     <span data-ttu-id="3cc04-128">10.00</span><span class="sxs-lookup"><span data-stu-id="3cc04-128">10.00</span></span>                 |     <span data-ttu-id="3cc04-129">3</span><span class="sxs-lookup"><span data-stu-id="3cc04-129">3</span></span>                 |
|     <span data-ttu-id="3cc04-130">Aanmaning</span><span class="sxs-lookup"><span data-stu-id="3cc04-130">Collection</span></span>                    |     <span data-ttu-id="3cc04-131">Laatste melding met bijzondere kosten</span><span class="sxs-lookup"><span data-stu-id="3cc04-131">Final   notification with fee</span></span>         |     <span data-ttu-id="3cc04-132">USD</span><span class="sxs-lookup"><span data-stu-id="3cc04-132">USD</span></span>           |     <span data-ttu-id="3cc04-133">403150</span><span class="sxs-lookup"><span data-stu-id="3cc04-133">403150</span></span>                |     <span data-ttu-id="3cc04-134">50.00</span><span class="sxs-lookup"><span data-stu-id="3cc04-134">50.00</span></span>                 |     <span data-ttu-id="3cc04-135">100.00</span><span class="sxs-lookup"><span data-stu-id="3cc04-135">100.00</span></span>                |     <span data-ttu-id="3cc04-136">15</span><span class="sxs-lookup"><span data-stu-id="3cc04-136">15</span></span>                |

<span data-ttu-id="3cc04-137">In de volgende afbeelding wordt de informatie in de tabel weergegeven zoals deze op de pagina **Aanmaningen** zou verschijnen.</span><span class="sxs-lookup"><span data-stu-id="3cc04-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="3cc04-138">[![Een aanmaningsreeks instellen](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="3cc04-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="3cc04-139">U moet nu de twee parameters instellen die voor dit voorbeeld zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="3cc04-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="3cc04-140">Ga naar **Crediteringen en aanmaningens \> Instellingen \> Parameters van module Klanten** en voer deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-141">Stel op het tabblad **Aanmaningen** de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="3cc04-142">Zorg ervoor dat het veld **Aanmaning maken per** is ingesteld op **Klant**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="3cc04-143">[![Parameters van de module Klanten instellen voor aanmaningen](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="3cc04-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="3cc04-144">Ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**, selecteer **Nieuw** en voer vervolgens deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-145">Selecteer **US-045** in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="3cc04-146">Voer in het veld **Factuurdatum** de waarde **15-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="3cc04-147">Voer in het veld **Vervaldatum** de waarde **16-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="3cc04-148">Voer op het sneltabblad **Factuurregels** in het veld **Hoofdrekening** de waarde **401100** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="3cc04-149">Voer in het veld **Eenheidsprijs** **500.00** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="3cc04-150">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-150">Select **Post**.</span></span>

    <span data-ttu-id="3cc04-151">U moet nu twee creditnota's voor de klant invoeren.</span><span class="sxs-lookup"><span data-stu-id="3cc04-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="3cc04-152">Selecteer **Nieuw** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-153">Selecteer **US-045** in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="3cc04-154">Voer in het veld **Factuurdatum** de waarde **15-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="3cc04-155">Voer in het veld **Vervaldatum** de waarde **16-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="3cc04-156">Voer op het sneltabblad **Factuurregels** in het veld **Hoofdrekening** de waarde **401100** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="3cc04-157">Voer **-100,00** in het veld **Eenheidsprijs** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="3cc04-158">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-158">Select **Post**.</span></span>

5. <span data-ttu-id="3cc04-159">Herhaal stap 4 maar geef **-200,00** op in het veld **Eenheidsprijs**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="3cc04-160">Ga naar **Klanten \> Klanten \> Alle klanten** en selecteer klant **US-045**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="3cc04-161">Selecteer vervolgens in het actievenster **Transacties \> Transactes** om de klanttransacties te bekijken die u eerder hebt geboekt.</span><span class="sxs-lookup"><span data-stu-id="3cc04-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="3cc04-162">[![De geboekte klanttransacties controleren](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="3cc04-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="3cc04-163">U moet nu aanmaningen maken voor klant US-045.</span><span class="sxs-lookup"><span data-stu-id="3cc04-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="3cc04-164">Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen maken** en voer deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-165">Stel de opties **Factuur** en **Creditnota** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="3cc04-166">Het veld **Aanmaning** moet standaard worden ingesteld op **Aanmaning per klant**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="3cc04-167">Voer in het veld **Aanmaningsdatum** de waarde **19-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="3cc04-168">Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** en voeg vervolgens in het veld **Klantrekening** de waarde **US-045** toe.</span><span class="sxs-lookup"><span data-stu-id="3cc04-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="3cc04-169">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-169">Select **OK**.</span></span>
    5. <span data-ttu-id="3cc04-170">Selecteer **OK** om aanmaningen te maken.</span><span class="sxs-lookup"><span data-stu-id="3cc04-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="3cc04-171">Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen controleren en verwerken** en voer deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-172">De aanmaningscode op zowel de koptekst als de transactieregels is **Aanmaning 1**, omdat deze aanmaning de eerste aan aanmaning in de reeks is.</span><span class="sxs-lookup"><span data-stu-id="3cc04-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="3cc04-173">(Als u de transactieregels wilt weergeven, moet u mogelijk het sneltabblad **Transacties** selecteren.)</span><span class="sxs-lookup"><span data-stu-id="3cc04-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="3cc04-174">[![Controleren of dezelfde aanmaningscode wordt weergegeven in de koptekst en op de regels](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="3cc04-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="3cc04-175">Selecteer **Boeken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="3cc04-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="3cc04-176">Voer in het veld **Boekingsdatum** de waarde **19-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="3cc04-177">U moet nu opnieuw aanmaningen maken voor klant US-045.</span><span class="sxs-lookup"><span data-stu-id="3cc04-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="3cc04-178">Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen maken** en voer deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-179">Stel de opties **Factuur** en **Creditnota** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="3cc04-180">Het veld **Aanmaning** moet standaard worden ingesteld op **Aanmaning per klant**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="3cc04-181">Voer in het veld **Aanmaningsdatum** de waarde **23-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="3cc04-182">Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** en voeg vervolgens in het veld **Klantrekening** de waarde **US-045** toe.</span><span class="sxs-lookup"><span data-stu-id="3cc04-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="3cc04-183">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-183">Select **OK**.</span></span>
    5. <span data-ttu-id="3cc04-184">Selecteer **OK** om aanmaningen te maken.</span><span class="sxs-lookup"><span data-stu-id="3cc04-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="3cc04-185">Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen controleren en verwerken** en voer deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-186">De aanmaningscode in de koptekst is **Aanmaning 1**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="3cc04-187">De code op de transactieregels is echter **Aanmaning 2**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="3cc04-188">[![Controleert of verschillende aanmaningscodes worden weergegeven in de koptekst en op de regels](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="3cc04-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="3cc04-189">De codes verschillen omdat de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="3cc04-190">Boek deze aanmaning niet.</span><span class="sxs-lookup"><span data-stu-id="3cc04-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="3cc04-191">Ga naar **Crediteringen en aanmaningen \> Instellen \> Parameters van module Klanten** en stel vervolgens op het tabblad **Aanmaningen** de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="3cc04-192">[![De optie Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode instellen op Nee](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="3cc04-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="3cc04-193">U moet nu opnieuw aanmaningen maken voor klant US-045.</span><span class="sxs-lookup"><span data-stu-id="3cc04-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="3cc04-194">Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen maken** en voer deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="3cc04-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="3cc04-195">Stel de opties **Factuur** en **Creditnota** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="3cc04-196">Het veld **Aanmaning** moet standaard worden ingesteld op **Aanmaning per klant**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="3cc04-197">Voer in het veld **Aanmaningsdatum** de waarde **23-01-2021** in.</span><span class="sxs-lookup"><span data-stu-id="3cc04-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="3cc04-198">Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** en voeg vervolgens in het veld **Klantrekening** de waarde **US-045** toe.</span><span class="sxs-lookup"><span data-stu-id="3cc04-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="3cc04-199">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-199">Select **OK**.</span></span>
    5. <span data-ttu-id="3cc04-200">Selecteer **OK** om aanmaningen te maken.</span><span class="sxs-lookup"><span data-stu-id="3cc04-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="3cc04-201">Ga naar **Crediteringen en aanmaningen \> Aanmaning \> Aanmaningen controleren en verwerken**. U ziet nu dat de aanmaningscode op zowel de koptekst als de transactieregels **Aanmaning 2** is.</span><span class="sxs-lookup"><span data-stu-id="3cc04-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="3cc04-202">[![Opnieuw tonen dat dezelfde aanmaningscode wordt weergegeven in de koptekst en op de regels](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="3cc04-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="3cc04-203">Op beide plekken wordt dezelfde code weergegeven omdat de optie **Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode** nu is ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="3cc04-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>

---
title: Ontbrekende openingssaldi in jaarafsluiting
description: In dit onderwerp wordt uitgelegd waarom openingssaldi kunnen ontbreken wanneer u een jaar afsluit en hoe u deze saldi opnieuw kunt opbouwen als ze ontbreken.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028557"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="051d6-103">Ontbrekende openingssaldi in jaarafsluiting</span><span class="sxs-lookup"><span data-stu-id="051d6-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="051d6-104">In dit onderwerp wordt uitgelegd waarom openingssaldi kunnen ontbreken wanneer u een jaar afsluit en hoe u deze saldi opnieuw kunt opbouwen als ze ontbreken.</span><span class="sxs-lookup"><span data-stu-id="051d6-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="051d6-105">Symptoom</span><span class="sxs-lookup"><span data-stu-id="051d6-105">Symptom</span></span>

<span data-ttu-id="051d6-106">Waarom zijn er geen beginsaldi na het uitvoeren van de jaarafsluiting van het grootboek?</span><span class="sxs-lookup"><span data-stu-id="051d6-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="051d6-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="051d6-107">Resolution</span></span>

<span data-ttu-id="051d6-108">Controleer het volgende als u een jaar in het grootboek hebt afgesloten en vervolgens een proefbalans hebt gegenereerd waarin geen openingssaldi voor het volgende boekjaar worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="051d6-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="051d6-109">Als het veld **Vorige afsluiting ongedaan maken** is ingesteld op **Ja**, wordt de vorige jaarafsluiting voor hetzelfde boekjaar ongedaan gemaakt.</span><span class="sxs-lookup"><span data-stu-id="051d6-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="051d6-110">Wanneer u een proces uitvoert om de jaarafsluiting ongedaan te maken, worden alle boekingen voor eind- en openingssaldi verwijderd, alsof het jaar nooit is afgesloten.</span><span class="sxs-lookup"><span data-stu-id="051d6-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="051d6-111">De boekstukken worden ook verwijderd.</span><span class="sxs-lookup"><span data-stu-id="051d6-111">The vouchers are also deleted.</span></span> <span data-ttu-id="051d6-112">Het jaarafsluitingsproces wordt niet automatisch opnieuw uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="051d6-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="051d6-113">U moet het proces opnieuw starten en deze keer de optie **Vorige afsluiting ongedaan maken** bijwerken naar **Nee**.</span><span class="sxs-lookup"><span data-stu-id="051d6-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="051d6-114">Dit scenario wordt behandeld in het onderwerp over jaarafsluiting in de veelgestelde vragen.</span><span class="sxs-lookup"><span data-stu-id="051d6-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="051d6-115">Zie [Veelgestelde vragen over jaarafsluitingsactiviteiten](faq-year-end-activities.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="051d6-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="051d6-116">Symptoom</span><span class="sxs-lookup"><span data-stu-id="051d6-116">Symptom</span></span>

<span data-ttu-id="051d6-117">Ik heb een jaarafsluiting uitgevoerd met de optie **Vorige afsluiting ongedaan maken** ingesteld op **Nee** en ik heb nog steeds geen openingssaldi voor mijn boekjaar.</span><span class="sxs-lookup"><span data-stu-id="051d6-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="051d6-118">Oplossing</span><span class="sxs-lookup"><span data-stu-id="051d6-118">Resolution</span></span>

<span data-ttu-id="051d6-119">Controleer eerst de status van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="051d6-119">First check the status of the batch job.</span></span> <span data-ttu-id="051d6-120">Het afsluiten van een jaar omvat een aantal afzonderlijke taken, maar de belangrijkste stap is de batchtaak met de taakbeschrijving **Stap 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="051d6-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="051d6-121">Het boeken van de openingstransacties, en eventueel de afsluittransacties, naar het grootboek vindt plaats tijdens deze stap.</span><span class="sxs-lookup"><span data-stu-id="051d6-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="051d6-122">[![Lijst batchhistorie](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="051d6-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="051d6-123">Als deze stap is beëindigd, maar u geen openingssaldi ziet op de querypagina **Proefbalans** (**Grootboek > Query's en rapporten > Proefbalans**), bekijkt u de resultaten van de batchtaak voor de jaarafsluiting om te zien of de stap voor het opnieuw opbouwen van saldi is voltooid.</span><span class="sxs-lookup"><span data-stu-id="051d6-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="051d6-124">[![Resultaten van batchtaak voor jaarafsluiting](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="051d6-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="051d6-125">Als deze stap om welke reden dan ook mislukt, zijn de openingstransacties en eventuele afsluittransacties waarschijnlijk geboekt.</span><span class="sxs-lookup"><span data-stu-id="051d6-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="051d6-126">U kunt via de querypagina **Boekstuktransacties** controleren of de grootboektransacties zijn geboekt door het boekstuknummer en de datum op te geven die in het dialoogvenster voor de jaarafsluiting zijn opgegeven voor het jaar dat u hebt afgesloten (**Grootboek > Query's en rapporten > Boekstuktransacties**).</span><span class="sxs-lookup"><span data-stu-id="051d6-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="051d6-127">[![Query Boekstuktransacties](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="051d6-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="051d6-128">Als de openingsboektukken, en eventueel de afsluitingsboekstukken, aanwezig zijn, hoeft u de jaarafsluiting niet opnieuw uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="051d6-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="051d6-129">Zie in plaats daarvan de volgende sectie voor informatie over hoe u verder kunt gaan.</span><span class="sxs-lookup"><span data-stu-id="051d6-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="051d6-130">Symptoom</span><span class="sxs-lookup"><span data-stu-id="051d6-130">Symptom</span></span>

<span data-ttu-id="051d6-131">Moet ik het hele proces voor de jaarafsluiting opnieuw uitvoeren als de stap voor het opnieuw opbouwen van saldi in de jaarafsluiting is mislukt?</span><span class="sxs-lookup"><span data-stu-id="051d6-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="051d6-132">Oplossing</span><span class="sxs-lookup"><span data-stu-id="051d6-132">Resolution</span></span>

<span data-ttu-id="051d6-133">Met de stap voor het opnieuw opbouwen van saldi worden de grootboeksaldi bijgewerkt die worden gebruikt wanneer de query Proefbalans wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="051d6-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="051d6-134">Dit is de laatste stap in het jaarafsluitingsproces.</span><span class="sxs-lookup"><span data-stu-id="051d6-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="051d6-135">Als dit de enige stap is die mislukt, zijn de grootboektransacties geboekt.</span><span class="sxs-lookup"><span data-stu-id="051d6-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="051d6-136">In dat geval hoeft u de jaarafsluiting niet opnieuw uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="051d6-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="051d6-137">U kunt het proces voor het handmatig opnieuw opbouwen van de saldi uitvoeren via de pagina **Financiële dimensiesets** (**Grootboek > Rekeningschema > Dimensies > Financiële dimensiesets**).</span><span class="sxs-lookup"><span data-stu-id="051d6-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="051d6-138">[![De knop Saldi opnieuw opbouwen op de pagina Financiële dimensiesets](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="051d6-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="051d6-139">Als de verwerking van deze stap lang duurt, raden we u aan de aanbevolen procedures voor financiële dimensiesets te bekijken die worden beschreven in [Aanbevolen procedures voor het bijwerken van financiële dimensiesets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="051d6-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 


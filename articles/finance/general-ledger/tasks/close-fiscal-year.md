---
title: Het boekjaar afsluiten
description: Deze procedure legt de stappen uit in het proces voor jaarafsluiting dat saldi naar een nieuw boekjaar overboekt.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c12f0842f6e8edf3b51d12d0e008eb09acf8c374
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177106"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="114fe-103">Het boekjaar afsluiten</span><span class="sxs-lookup"><span data-stu-id="114fe-103">Close the fiscal year</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="114fe-104">Deze procedure legt de stappen uit in het proces voor jaarafsluiting dat saldi naar een nieuw boekjaar overboekt.</span><span class="sxs-lookup"><span data-stu-id="114fe-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="114fe-105">Parameters voor de jaarafsluiting valideren</span><span class="sxs-lookup"><span data-stu-id="114fe-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="114fe-106">Ga naar **Navigatievenster > Modules > Grootboek > Grootboek instellen > Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="114fe-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="114fe-107">Vouw de sectie **Afsluiting fiscaal jaar** uit.</span><span class="sxs-lookup"><span data-stu-id="114fe-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="114fe-108">Selecteer Ja of Nee voor de optie **Jaareindetransacties verwijderen tijdens overboeking**.</span><span class="sxs-lookup"><span data-stu-id="114fe-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="114fe-109">Als het boekjaar al is afgesloten en jaarafsluiting opnieuw wordt uitgevoerd, wordt deze instelling belangrijk.</span><span class="sxs-lookup"><span data-stu-id="114fe-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="114fe-110">Als de waarde is ingesteld op Ja, wordt het boekstuk voor de vorige jaarafsluiting verwijderd en een nieuw boekstuk aangemaakt voor de beginsaldi voor alle accounts.</span><span class="sxs-lookup"><span data-stu-id="114fe-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="114fe-111">Als de waarde is ingesteld op Nee, wordt het boekstuk behouden en wordt een nieuw boekstuk alleen gemaakt om invoeren aan te passen die na de laatste jaarafsluiting zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="114fe-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="114fe-112">Selecteer Ja of Nee voor de optie **Afsluittransacties tijdens overboeking maken**.</span><span class="sxs-lookup"><span data-stu-id="114fe-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="114fe-113">Als de waarde is ingesteld op Ja, worden twee transacties gemaakt.</span><span class="sxs-lookup"><span data-stu-id="114fe-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="114fe-114">Één boekstuk wordt gemaakt in het boekjaar dat wordt afgesloten, om de saldi van de grootboekrekeningen van W&V op nul in te stellen. Een tweede boekstuk wordt gemaakt in het volgende boekjaar voor de beginsaldi.</span><span class="sxs-lookup"><span data-stu-id="114fe-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="114fe-115">Als de waarde is ingesteld op Nee, wordt één boekstuk gemaakt in het volgende boekjaar voor de beginsaldi.</span><span class="sxs-lookup"><span data-stu-id="114fe-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="114fe-116">Selecteer Ja of Nee voor de optie **Status fiscaal jaar instellen op definitief afgesloten**.</span><span class="sxs-lookup"><span data-stu-id="114fe-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="114fe-117">Als de waarde is ingesteld op Ja, wordt de status van het boekjaar ingesteld op Definitief gesloten.</span><span class="sxs-lookup"><span data-stu-id="114fe-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="114fe-118">Omdat een definitief afgesloten jaar niet kan worden heropend, zou het een best practice zijn om deze optie op Nee in te stellen.</span><span class="sxs-lookup"><span data-stu-id="114fe-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="114fe-119">Selecteer Ja of Nee voor de optie **Boekstuknummer moet worden ingevuld tijdens de jaarafsluiting**.</span><span class="sxs-lookup"><span data-stu-id="114fe-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="114fe-120">Als de waarde is ingesteld Ja, moet een boekstuknummer handmatig in het jaarafsluitingsproces worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="114fe-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="114fe-121">Dit boekstuknummer wordt niet gegenereerd op basis van een nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="114fe-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="114fe-122">Het is een best practice om dit op Ja in te stellen.</span><span class="sxs-lookup"><span data-stu-id="114fe-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="114fe-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="114fe-123">Close the page.</span></span>
8. <span data-ttu-id="114fe-124">Ga naar **Grootboek > Afgesloten periode > Jaarafsluiting**.</span><span class="sxs-lookup"><span data-stu-id="114fe-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="114fe-125">Klik op **Nieuw** om een jaarafsluitingssjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="114fe-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="114fe-126">Een sjabloon kan voor een groep rechtspersonen worden gemaakt waarvoor de jaarafsluiting moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="114fe-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="114fe-127">U kunt deze sjabloon elk jaar opnieuw gebruiken.</span><span class="sxs-lookup"><span data-stu-id="114fe-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="114fe-128">Voer in het veld **Groepsnaam** de naam van de jaarafsluitingssjabloon in.</span><span class="sxs-lookup"><span data-stu-id="114fe-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="114fe-129">Selecteer in het veld **Fiscale kalender** het fiscaal jaar waarvoor de sjabloon wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="114fe-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="114fe-130">Alleen rechtspersonen die hetzelfde boekjaar gebruiken, kunnen samen in de jaarafsluitingssjabloon worden gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="114fe-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="114fe-131">Dit is omdat de jaarafsluiting wordt uitgevoerd door een boekjaar te selecteren in plaats van een datum.</span><span class="sxs-lookup"><span data-stu-id="114fe-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="114fe-132">Klik in het **Actievenster** op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="114fe-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="114fe-133">Klik in de sectie **Rechtspersonen** op **Toevoegen** om de rechtspersonen voor deze sjabloon te selecteren.</span><span class="sxs-lookup"><span data-stu-id="114fe-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="114fe-134">Rechtspersonen kunnen worden toegevoegd door selectie van de rechtspersonen of van een organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="114fe-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="114fe-135">Alleen de rechtspersonen die de organisatiehiërarchie hebben met dezelfde fiscale kalender worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="114fe-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="114fe-136">Selecteer de rechtspersonen of de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="114fe-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="114fe-137">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="114fe-137">Click **OK**.</span></span>
16. <span data-ttu-id="114fe-138">Selecteer Ja of Nee in **Balansdimensie overboeken**.</span><span class="sxs-lookup"><span data-stu-id="114fe-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="114fe-139">Het is een best practice om deze optie voor Balansrekeningen in te stellen op Ja.</span><span class="sxs-lookup"><span data-stu-id="114fe-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="114fe-140">Hierme worden de financiële dimensies op geboekte transacties bewaard, wanneer de beginsaldi worden gemaakt voor de balansrekeningen.</span><span class="sxs-lookup"><span data-stu-id="114fe-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="114fe-141">Voor winst- en verliesrekeningen kunt u ervoor kiezen om de financiële dimensies te bewaren (Alles sluiten) wanneer de saldi worden verplaatst naar Ingehouden winst, of om de financiële dimensies te vervangen door een andere dimensiewaarde (Eén sluiten).</span><span class="sxs-lookup"><span data-stu-id="114fe-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="114fe-142">Als u Eén sluiten kiest, kunt u een specifieke dimensiewaarde definiëren voor elke dimensie of een waarde zelfs leeg laten.</span><span class="sxs-lookup"><span data-stu-id="114fe-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="114fe-143">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="114fe-143">Click **Save**.</span></span>
18. <span data-ttu-id="114fe-144">Start de jaarafsluiting door in het **Actievenster** de optie **Jaarafsluiting uitvoeren** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="114fe-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="114fe-145">De jaarafsluiting wordt voor de geselecteerde sjabloon uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="114fe-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="114fe-146">Selecteer alle rechtspersonen in de sjabloon of een deel daarvan waarvoor de jaarafsluiting moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="114fe-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="114fe-147">Wanneer de jaarafsluiting voor het eerst wordt uitgevoerd, kiezen de meeste organisaties ervoor om de jaarafsluiting voor alle rechtspersonen in de sjabloon uit te voeren, om beginsaldi te krijgen.</span><span class="sxs-lookup"><span data-stu-id="114fe-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="114fe-148">Als daarna nog aanpassende invoeren worden gedaan, kunt u ervoor kiezen de jaarafsluiting alleen uit te voeren voor de rechtspersonen waarvoor correcties zijn aangebracht.</span><span class="sxs-lookup"><span data-stu-id="114fe-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="114fe-149">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="114fe-149">Click **OK**.</span></span>
21. <span data-ttu-id="114fe-150">Selecteer de fiscale kalender waarvoor u de jaarafsluiting wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="114fe-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="114fe-151">Typ een waarde in het veld **Boekstuk**.</span><span class="sxs-lookup"><span data-stu-id="114fe-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="114fe-152">Het is een best practice om het boekjaar in het boekstuknummer op te nemen, om het jaareindeboekstuk vinden dat wordt gemaakt, gemakkelijker te vinden.</span><span class="sxs-lookup"><span data-stu-id="114fe-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="114fe-153">De jaarafsluiting wordt standaard in de batchmodus uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="114fe-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="114fe-154">Het is een best practice om processen met een lange uitvoeringstijd in batchmodus uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="114fe-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="114fe-155">Dit is meestal een dergelijk proces, en daarom wordt standaard de batchmodus geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="114fe-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="114fe-156">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="114fe-156">Click **OK**.</span></span>

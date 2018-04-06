---
title: Toevoegen van projectkosten op inkoopontvangsten
description: In dit onderwerp wordt beschreven hoe toegerekende projectkosten van inkoopontvangsten in Microsoft Dynamics 365 for Finance and Operations kunnen worden getraceerd.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9a74b684e955376b9c3036954f4a6e6628c468f0
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="ca4d9-103">Toevoegen van projectkosten op inkoopontvangsten</span><span class="sxs-lookup"><span data-stu-id="ca4d9-103">Project cost accrual on purchase receipts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ca4d9-104">In dit onderwerp wordt beschreven hoe toegerekende projectkosten van inkoopontvangsten in Microsoft Dynamics 365 for Finance and Operations kunnen worden getraceerd.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="ca4d9-105">Facturen voor een project komen vaak later aan dan de geleverde goederen en diensten, wat een aanzienlijke impact kan hebben op prestatie-indicatoren (KPI's) voor projecten.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="ca4d9-106">Het is belangrijk dat deze transacties zowel in financiële als ook in projectrapporten kunnen worden gevolgd.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="ca4d9-107">Dit wordt geïllustreerd in het volgende voorbeeldscenario.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="ca4d9-108">Contoso Consulting is gestart met een nieuw project voor cloudimplementatie.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="ca4d9-109">Een inkooporder wordt gemaakt een computer aan te schaffen voor het project.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="ca4d9-110">De computer kost EUR 1500 en de installatie kost EUR 150.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="ca4d9-111">De leverancier heeft de computer geleverd en geïnstalleerd, maar de factuur is nog niet aangekomen bij Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="ca4d9-112">De projectmanager wilt de project-kosten van EUR 1650 laten toerekenen voordat de factuur aankomt.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="ca4d9-113">Deze kosten moet ook worden doorgevoerd in de financiële overzichten voor het maandeinde van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="ca4d9-114">Voor rapportagedoeleinden moeten de toegerekende kosten worden vastgelegd op zowel het financiële niveau als ook het projectniveau.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="ca4d9-115">In Finance and Operations kan de financiële update van de productontvangstbon voor het artikel en inkoopcategorieën worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="ca4d9-116">Voor artikelen op de pagina **Parameters van leveranciers** selecteert u de optie **Productontvangstbonnen in grootboek boeken**.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="ca4d9-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="ca4d9-118">Voor aanschaffingscategorieën selecteert u op de pagina **Categoriebeleidsregel** de optie **Inkoopbeleid** en vervolgens **Inkoopkosten samenvoegen voor ontvangst** voor elke aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="ca4d9-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="ca4d9-120">De rekeningen **Inkoopuitgave, niet-gefactureerd** en **Inkoop, toerekening** in **Boekingsinstellingen** worden gebruikt bij het boeken van boekstukken die betrekking hebben op de productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="ca4d9-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="ca4d9-122">Laten we met hetzelfde scenario eens kijken welke invloed het boeken van een productontvangstbon heeft voor het grootboek en projectgegevens.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="ca4d9-123">**Stap 1:** Maak en bevestig een nieuwe inkooporder voor het project, waarmee de aankoop van een computer voor EUR 1500 en installatiediensten voor $150 worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="ca4d9-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="ca4d9-125">Wanneer de inkooporder wordt bevestigd, worden transacties voor de toegezegde kosten gemaakt voor het project.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="ca4d9-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="ca4d9-127">In de transacties voor de toegezegde kosten is het veld **Transactieoorsprong** ingesteld op **Inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="ca4d9-128">Als u een inkooporder maakt en bevestigt, worden hiermee geen transacties voor een project aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="ca4d9-129">**Stap 2:** Goederen en diensten worden geleverd en een productontvangstbon wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="ca4d9-130">Als u een productontvangstbon boekt, wordt hiermee een boekstuk gegenereerd en in het grootboek geboekt.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="ca4d9-131">Het boekstuk debiteert de inkoopuitgave, de niet-gefactureerde rekening, en crediteert de rekening voor inkooptoerekening.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="ca4d9-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="ca4d9-133">Als u een productontvangstbon boekt, worden de boekingsinstellingen voor aanschaffingscategorieën en -producten gebruikt, niet de boekingsinstellingen voor de projectcategorieën.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="ca4d9-134">Deze instelling moet worden afgestemd om correct de financiële invloed van inkooptoerekeningen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="ca4d9-135">U kunt aanschaffingscategorieën toewijzen aan projectcategorieën op de pagina **Aanschaffingscategorie**.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="ca4d9-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="ca4d9-137">**Stap 3:** Maak een conceptleveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="ca4d9-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="ca4d9-138">In Finance and Operations heeft het boeken van een productontvangstbon geen invloed op projectgegevens.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="ca4d9-139">Als workaround kunt u een conceptleveranciersfactuur genereren meteen nadat u de inkoopontvangst hebt geboekt.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="ca4d9-140">Ga naar de pagina **Inkooporder** &gt; **tabblad Factuur** &gt; **Genereren** &gt; **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="ca4d9-141">Hiermee maakt u een in behandeling zijnd factuurdocument waarmee projectgegevens worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="ca4d9-142">Als u een conceptleveranciersfactuur aanmaakt, genereert u hiermee in behandeling zijnde projecttransacties.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="ca4d9-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="ca4d9-144">Op de pagina **Toegezegde kosten** worden records die u in stap 1 hebt gemaakt, gesloten en nieuwe records worden gemaakt om kostentoezeggingen uit de in behandeling zijnde leveranciersfactuur weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="ca4d9-145">Het veld **Oorsprong van transactie** voor de toegezegde kosten wordt ingesteld op **Leveranciersfactuur**.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="ca4d9-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="ca4d9-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="ca4d9-147">De leveranciersfactuur blijft in behandeling, totdat de werkelijke leveranciersfactuur wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="ca4d9-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>





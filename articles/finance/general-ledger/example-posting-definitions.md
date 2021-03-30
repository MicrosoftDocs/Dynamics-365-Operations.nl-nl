---
title: Voorbeelden van boekingsdefinities
description: Dit artikel bevat voorbeelden die laten zien hoe boekdefinities worden gebruikt voor vorderingen van inkooporders en budgettoewijzingen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dbbc727120f5292a3ad94711cf79138b35593bf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235132"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="9138d-103">voorbeelden van boekdefinities</span><span class="sxs-lookup"><span data-stu-id="9138d-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9138d-104">Dit artikel bevat voorbeelden die laten zien hoe boekdefinities worden gebruikt voor vorderingen van inkooporders en budgettoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="9138d-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="9138d-105">Voordat u dit onderwerp leest, moet u vertrouwd zijn met de boekingsdefinities en transactieboekingsdefinities.</span><span class="sxs-lookup"><span data-stu-id="9138d-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="9138d-106">Meer informatie vindt u onder [Boekdefinities](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="9138d-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="9138d-107">De volgende voorbeelden kunnen worden ingesteld op de pagina **Boekdefinities**.</span><span class="sxs-lookup"><span data-stu-id="9138d-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="9138d-108">Elk voorbeeld bevat deze secties:</span><span class="sxs-lookup"><span data-stu-id="9138d-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="9138d-109">Boekdefinitie – Matchcriteria</span><span class="sxs-lookup"><span data-stu-id="9138d-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="9138d-110">Boekingsdefinitie – Gegenereerde vermeldingen</span><span class="sxs-lookup"><span data-stu-id="9138d-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="9138d-111">Transacties met de rekeningen dimensiewaarden en bedragen</span><span class="sxs-lookup"><span data-stu-id="9138d-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="9138d-112">Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd</span><span class="sxs-lookup"><span data-stu-id="9138d-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="9138d-113">Wanneer er een match is tussen de rekeningen en dimensiewaarden in het deelvenster **Criteria voor overeenkomst** voor de boekdefinitie en de rekeningen en dimensiewaarden in de transactie, worden er grootboekboekingen gegenereerd op basis van het deelvenster **Gegenereerde vermeldingen** voor de boekdefinitie.</span><span class="sxs-lookup"><span data-stu-id="9138d-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="9138d-114">Gebruik de pagina **Boekdefinities voor transacties** om een boekdefinitie aan een specifiek transactietype te koppelen.</span><span class="sxs-lookup"><span data-stu-id="9138d-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="9138d-115">Nadat u een boekdefinitie aan een transactietype hebt gekoppeld en **Boekdefinities gebruiken** hebt geselecteerd op de pagina **Grootboekparameters**, moeten alle transacties van het geselecteerde transactietype gebruikmaken van boekdefinities.</span><span class="sxs-lookup"><span data-stu-id="9138d-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="9138d-116">Voorbeeld: Vorderingen van inkooporders</span><span class="sxs-lookup"><span data-stu-id="9138d-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="9138d-117">Wanneer u de verwerking van vorderingen inschakelt door **Vorderingsproces inschakelen** te selecteren op de pagina **Grootboekparameters**, moeten boekdefinities worden gebruikt om vorderingen in het grootboek te registreren voor rekeningen die moeten worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="9138d-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="9138d-118">In de meeste gevallen worden alle onkostenrekeningen op de balans gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="9138d-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="9138d-119">Boekdefinities voor vorderingen worden ingesteld voor de module **Inkoop** op de pagina **Boekdefinities**.</span><span class="sxs-lookup"><span data-stu-id="9138d-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="9138d-120">Daarna kunt u in het gebied **Inkoop** van de pagina **Boekdefinities voor transacties** het transactietype **Inkooporder** selecteren om de boekdefinitie aan inkooporders te koppelen.</span><span class="sxs-lookup"><span data-stu-id="9138d-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="9138d-121">Alle boekstuktransacties voor inkoopordervorderingen moeten in evenwicht zijn (met andere woorden, debet moet gelijk zijn aan credit) in elke unieke dimensie op een boekstuk.</span><span class="sxs-lookup"><span data-stu-id="9138d-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="9138d-122">Boekdefinitie – Matchcriteria</span><span class="sxs-lookup"><span data-stu-id="9138d-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="9138d-123">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="9138d-123">Account structure</span></span>       | <span data-ttu-id="9138d-124">Rekeningnummerovereenkomst</span><span class="sxs-lookup"><span data-stu-id="9138d-124">Match account number</span></span> | <span data-ttu-id="9138d-125">Prioriteit </span><span class="sxs-lookup"><span data-stu-id="9138d-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="9138d-126">Rekeningstructuur - W&V</span><span class="sxs-lookup"><span data-stu-id="9138d-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="9138d-127">1</span><span class="sxs-lookup"><span data-stu-id="9138d-127">1</span></span>        |

<span data-ttu-id="9138d-128"><em>Een lege waarde in het veld \**Vereffeningsrekeningnummer</em>* betekent dat alle overeenkomende rekeningen in de gedefinieerde rekeningstructuur deel uitmaken van de afstemmingsregel.</span><span class="sxs-lookup"><span data-stu-id="9138d-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="9138d-129">Boekingsdefinitie – Gegenereerde vermeldingen</span><span class="sxs-lookup"><span data-stu-id="9138d-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="9138d-130">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="9138d-130">Account structure</span></span> | <span data-ttu-id="9138d-131">Gegenereerd rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="9138d-131">Generated account number</span></span>                    | <span data-ttu-id="9138d-132">Gegenereerd debet/credit</span><span class="sxs-lookup"><span data-stu-id="9138d-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="9138d-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="9138d-133">Balance</span></span>           | <span data-ttu-id="9138d-134">300143 - -(vorderingsrekening)</span><span class="sxs-lookup"><span data-stu-id="9138d-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="9138d-135">Zelfde</span><span class="sxs-lookup"><span data-stu-id="9138d-135">Same</span></span>                   |
| <span data-ttu-id="9138d-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="9138d-136">Balance</span></span>           | <span data-ttu-id="9138d-137">300144 - -(reserveren voor vorderingsrekening)</span><span class="sxs-lookup"><span data-stu-id="9138d-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="9138d-138">Balanceren</span><span class="sxs-lookup"><span data-stu-id="9138d-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="9138d-139">Transacties met de rekeningen dimensiewaarden en bedragen</span><span class="sxs-lookup"><span data-stu-id="9138d-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="9138d-140">De rekeningen en dimensiewaarden zijn afkomstig van de boekhoudingsverdelingen die u invoert voor een inkooporderregel of zijn afkomstig van de rekeningen en dimensies die automatisch worden gegenereerd op basis van de standaardinstellingen voor leveranciers, artikelen, categorieën en dimensiesjablonen.</span><span class="sxs-lookup"><span data-stu-id="9138d-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="9138d-141">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="9138d-141">Account + dimensions</span></span>           | <span data-ttu-id="9138d-142">Debet</span><span class="sxs-lookup"><span data-stu-id="9138d-142">Debit</span></span>  | <span data-ttu-id="9138d-143">Krediet</span><span class="sxs-lookup"><span data-stu-id="9138d-143">Credit</span></span> | <span data-ttu-id="9138d-144">Opmerking</span><span class="sxs-lookup"><span data-stu-id="9138d-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="9138d-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="9138d-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="9138d-146">250,00</span><span class="sxs-lookup"><span data-stu-id="9138d-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="9138d-147">Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd</span><span class="sxs-lookup"><span data-stu-id="9138d-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="9138d-148">Grootboekboekingen worden gemaakt om de vorderingen te registreren.</span><span class="sxs-lookup"><span data-stu-id="9138d-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="9138d-149">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="9138d-149">Account + dimensions</span></span>           | <span data-ttu-id="9138d-150">Debet</span><span class="sxs-lookup"><span data-stu-id="9138d-150">Debit</span></span>  | <span data-ttu-id="9138d-151">Krediet</span><span class="sxs-lookup"><span data-stu-id="9138d-151">Credit</span></span> | <span data-ttu-id="9138d-152">Opmerking</span><span class="sxs-lookup"><span data-stu-id="9138d-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="9138d-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="9138d-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="9138d-154">250,00</span><span class="sxs-lookup"><span data-stu-id="9138d-154">250.00</span></span> |        |         |
| <span data-ttu-id="9138d-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="9138d-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="9138d-156">250,00</span><span class="sxs-lookup"><span data-stu-id="9138d-156">250.00</span></span> |         |

<span data-ttu-id="9138d-157">In dit voorbeeld komt elke rekening die onderdeel is van de Rekeningstructuur - W&V overeen met de criteria van de boekdefinitie.</span><span class="sxs-lookup"><span data-stu-id="9138d-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="9138d-158">Wanneer dus 606500-OU\_1-OU\_3566-Training wordt beoordeeld, worden gegenereerde boekingen gemaakt voor de rekeningen die in het deelvenster **Gegenereerde vermeldingen** voor de boekdefinitie zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="9138d-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="9138d-159">Voorbeeld: Budgettoewijzingen</span><span class="sxs-lookup"><span data-stu-id="9138d-159">Example: Budget appropriations</span></span>
<span data-ttu-id="9138d-160">Wanneer u budgettoewijzingen inschakelt door **Aanwending van budget inschakelen** te selecteren op de pagina **Grootboekparameters**, moeten boekdefinities worden gebruikt om budgetregistervermeldingen te registeren in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="9138d-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="9138d-161">Wanneer een budgetbeheerconfiguratie actief is en is ingeschakeld, kunnen boekdefinities en transactieboekdefinities worden gebruikt om de registratie van toewijzingen, revisies, overboekingen, projecten, vaste activa en prognoseboekingen voor vraag en aanbod in het grootboek te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="9138d-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="9138d-162">U kunt een boekdefinitie voor budgetregisterregels die een budgettype **Oorspronkelijk budget** hebben en waarvoor toewijzingen zijn ingeschakeld, instellen door de module **Budget** te selecteren op de pagina **Boekdefinities**.</span><span class="sxs-lookup"><span data-stu-id="9138d-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="9138d-163">Vervolgens kunt u in het gebied **Budget** van de pagina **Boekdefinities van transacties** budgetcodes gebruiken om de boekdefinitie te koppelen aan budgetregisterregels met een budgettype **Oorspronkelijk budget**.</span><span class="sxs-lookup"><span data-stu-id="9138d-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="9138d-164">Wanneer budgettoewijzingen en boekdefinities zijn ingeschakeld, worden de budgetregisterregels geregistreerd voor budgetbeheer en in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="9138d-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="9138d-165">Boekdefinitie – Matchcriteria</span><span class="sxs-lookup"><span data-stu-id="9138d-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="9138d-166">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="9138d-166">Account structure</span></span>       | <span data-ttu-id="9138d-167">Rekeningnummerovereenkomst</span><span class="sxs-lookup"><span data-stu-id="9138d-167">Match account number</span></span> | <span data-ttu-id="9138d-168">Prioriteit </span><span class="sxs-lookup"><span data-stu-id="9138d-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="9138d-169">Rekeningstructuur - W&V</span><span class="sxs-lookup"><span data-stu-id="9138d-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="9138d-170">1</span><span class="sxs-lookup"><span data-stu-id="9138d-170">1</span></span>        |

<span data-ttu-id="9138d-171"><em>Een lege waarde in het veld \**Vereffeningsrekeningnummer</em>* betekent dat alle overeenkomende rekeningen in de gedefinieerde rekeningstructuur deel uitmaken van de afstemmingsregel.</span><span class="sxs-lookup"><span data-stu-id="9138d-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="9138d-172">Boekingsdefinitie – Gegenereerde vermeldingen</span><span class="sxs-lookup"><span data-stu-id="9138d-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="9138d-173">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="9138d-173">Account structure</span></span> | <span data-ttu-id="9138d-174">Gegenereerd rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="9138d-174">Generated account number</span></span>              | <span data-ttu-id="9138d-175">Gegenereerd debet/credit</span><span class="sxs-lookup"><span data-stu-id="9138d-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="9138d-176">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="9138d-176">Account structure</span></span> | <span data-ttu-id="9138d-177">300145 - -(geschatte opbrengstrekening)</span><span class="sxs-lookup"><span data-stu-id="9138d-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="9138d-178">Zelfde</span><span class="sxs-lookup"><span data-stu-id="9138d-178">Same</span></span>                   |
| <span data-ttu-id="9138d-179">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="9138d-179">Account structure</span></span> | <span data-ttu-id="9138d-180">300146 - -(toewijzingsrekening)</span><span class="sxs-lookup"><span data-stu-id="9138d-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="9138d-181">Balanceren</span><span class="sxs-lookup"><span data-stu-id="9138d-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="9138d-182">Transacties met de rekeningen dimensiewaarden en bedragen</span><span class="sxs-lookup"><span data-stu-id="9138d-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="9138d-183">U voert de rekeningen, dimensiewaarden en bedragen voor de budgetjournaalregel in op de pagina **Budgetregisterpost**.</span><span class="sxs-lookup"><span data-stu-id="9138d-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="9138d-184">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="9138d-184">Account + dimensions</span></span>           | <span data-ttu-id="9138d-185">Debet</span><span class="sxs-lookup"><span data-stu-id="9138d-185">Debit</span></span> | <span data-ttu-id="9138d-186">Krediet</span><span class="sxs-lookup"><span data-stu-id="9138d-186">Credit</span></span> | <span data-ttu-id="9138d-187">Opmerking</span><span class="sxs-lookup"><span data-stu-id="9138d-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="9138d-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="9138d-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="9138d-189">250,00</span><span class="sxs-lookup"><span data-stu-id="9138d-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="9138d-190">Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd</span><span class="sxs-lookup"><span data-stu-id="9138d-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="9138d-191">Gegenereerde grootboekboekingen worden gemaakt om het oorspronkelijke budget in elke dimensie te registreren.</span><span class="sxs-lookup"><span data-stu-id="9138d-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="9138d-192">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="9138d-192">Account + dimensions</span></span>           | <span data-ttu-id="9138d-193">Debet</span><span class="sxs-lookup"><span data-stu-id="9138d-193">Debit</span></span>  | <span data-ttu-id="9138d-194">Krediet</span><span class="sxs-lookup"><span data-stu-id="9138d-194">Credit</span></span> | <span data-ttu-id="9138d-195">Opmerking</span><span class="sxs-lookup"><span data-stu-id="9138d-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="9138d-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="9138d-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="9138d-197">250,00</span><span class="sxs-lookup"><span data-stu-id="9138d-197">250.00</span></span> |         |
| <span data-ttu-id="9138d-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="9138d-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="9138d-199">250,00</span><span class="sxs-lookup"><span data-stu-id="9138d-199">250.00</span></span> |        |         |

<span data-ttu-id="9138d-200">In dit voorbeeld komt elke rekening die onderdeel is van de Rekeningstructuur - W&V overeen met de criteria van de boekdefinitie.</span><span class="sxs-lookup"><span data-stu-id="9138d-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="9138d-201">Daarom worden de gegenereerde grootboekboekingen gemaakt wanneer 606400-OU\_1-OU\_3566-Training wordt beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="9138d-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
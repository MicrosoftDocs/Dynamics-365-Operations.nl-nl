---
title: Boekdefinities
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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5fb08a86639e9a9a79dca5fc1200e73e5870432
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564688"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="acd77-103">voorbeelden van boekdefinities</span><span class="sxs-lookup"><span data-stu-id="acd77-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acd77-104">Dit artikel bevat voorbeelden die laten zien hoe boekdefinities worden gebruikt voor vorderingen van inkooporders en budgettoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="acd77-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="acd77-105">Voordat u dit onderwerp leest, moet u vertrouwd zijn met de boekingsdefinities en transactieboekingsdefinities.</span><span class="sxs-lookup"><span data-stu-id="acd77-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="acd77-106">Meer informatie vindt u onder [Boekdefinities](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="acd77-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="acd77-107">De volgende voorbeelden kunnen worden ingesteld op de pagina **Boekdefinities**.</span><span class="sxs-lookup"><span data-stu-id="acd77-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="acd77-108">Elk voorbeeld bevat deze secties:</span><span class="sxs-lookup"><span data-stu-id="acd77-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="acd77-109">Boekdefinitie – Matchcriteria</span><span class="sxs-lookup"><span data-stu-id="acd77-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="acd77-110">Boekingsdefinitie – Gegenereerde vermeldingen</span><span class="sxs-lookup"><span data-stu-id="acd77-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="acd77-111">Transacties met de rekeningen dimensiewaarden en bedragen</span><span class="sxs-lookup"><span data-stu-id="acd77-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="acd77-112">Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd</span><span class="sxs-lookup"><span data-stu-id="acd77-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="acd77-113">Wanneer er een match is tussen de rekeningen en dimensiewaarden in het deelvenster **Criteria voor overeenkomst** voor de boekdefinitie en de rekeningen en dimensiewaarden in de transactie, worden er grootboekboekingen gegenereerd op basis van het deelvenster **Gegenereerde vermeldingen** voor de boekdefinitie.</span><span class="sxs-lookup"><span data-stu-id="acd77-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="acd77-114">Gebruik de pagina **Boekdefinities voor transacties** om een boekdefinitie aan een specifiek transactietype te koppelen.</span><span class="sxs-lookup"><span data-stu-id="acd77-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="acd77-115">Nadat u een boekdefinitie aan een transactietype hebt gekoppeld en **Boekdefinities gebruiken** hebt geselecteerd op de pagina **Grootboekparameters**, moeten alle transacties van het geselecteerde transactietype gebruikmaken van boekdefinities.</span><span class="sxs-lookup"><span data-stu-id="acd77-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="acd77-116">Voorbeeld: Vorderingen van inkooporders</span><span class="sxs-lookup"><span data-stu-id="acd77-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="acd77-117">Wanneer u de verwerking van vorderingen inschakelt door **Vorderingsproces inschakelen** te selecteren op de pagina **Grootboekparameters**, moeten boekdefinities worden gebruikt om vorderingen in het grootboek te registreren voor rekeningen die moeten worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="acd77-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="acd77-118">In de meeste gevallen worden alle onkostenrekeningen op de balans gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="acd77-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="acd77-119">Boekdefinities voor vorderingen worden ingesteld voor de module **Inkoop** op de pagina **Boekdefinities**.</span><span class="sxs-lookup"><span data-stu-id="acd77-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="acd77-120">Daarna kunt u in het gebied **Inkoop** van de pagina **Boekdefinities voor transacties** het transactietype **Inkooporder** selecteren om de boekdefinitie aan inkooporders te koppelen.</span><span class="sxs-lookup"><span data-stu-id="acd77-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="acd77-121">Alle boekstuktransacties voor inkoopordervorderingen moeten in evenwicht zijn (met andere woorden, debet moet gelijk zijn aan credit) in elke unieke dimensie op een boekstuk.</span><span class="sxs-lookup"><span data-stu-id="acd77-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="acd77-122">Boekdefinitie – Matchcriteria</span><span class="sxs-lookup"><span data-stu-id="acd77-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="acd77-123">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="acd77-123">Account structure</span></span>       | <span data-ttu-id="acd77-124">Rekeningnummerovereenkomst</span><span class="sxs-lookup"><span data-stu-id="acd77-124">Match account number</span></span> | <span data-ttu-id="acd77-125">Prioriteit </span><span class="sxs-lookup"><span data-stu-id="acd77-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="acd77-126">Rekeningstructuur - W&V</span><span class="sxs-lookup"><span data-stu-id="acd77-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="acd77-127">1</span><span class="sxs-lookup"><span data-stu-id="acd77-127">1</span></span>        |

<span data-ttu-id="acd77-128"><em>Een lege waarde in het veld \**Vereffeningsrekeningnummer</em>* betekent dat alle overeenkomende rekeningen in de gedefinieerde rekeningstructuur deel uitmaken van de afstemmingsregel.</span><span class="sxs-lookup"><span data-stu-id="acd77-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="acd77-129">Boekingsdefinitie – Gegenereerde vermeldingen</span><span class="sxs-lookup"><span data-stu-id="acd77-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="acd77-130">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="acd77-130">Account structure</span></span> | <span data-ttu-id="acd77-131">Gegenereerd rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="acd77-131">Generated account number</span></span>                    | <span data-ttu-id="acd77-132">Gegenereerd debet/credit</span><span class="sxs-lookup"><span data-stu-id="acd77-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="acd77-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="acd77-133">Balance</span></span>           | <span data-ttu-id="acd77-134">300143 - -(vorderingsrekening)</span><span class="sxs-lookup"><span data-stu-id="acd77-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="acd77-135">Zelfde</span><span class="sxs-lookup"><span data-stu-id="acd77-135">Same</span></span>                   |
| <span data-ttu-id="acd77-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="acd77-136">Balance</span></span>           | <span data-ttu-id="acd77-137">300144 - -(reserveren voor vorderingsrekening)</span><span class="sxs-lookup"><span data-stu-id="acd77-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="acd77-138">Balanceren</span><span class="sxs-lookup"><span data-stu-id="acd77-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="acd77-139">Transacties met de rekeningen dimensiewaarden en bedragen</span><span class="sxs-lookup"><span data-stu-id="acd77-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="acd77-140">De rekeningen en dimensiewaarden zijn afkomstig van de boekhoudingsverdelingen die u invoert voor een inkooporderregel of zijn afkomstig van de rekeningen en dimensies die automatisch worden gegenereerd op basis van de standaardinstellingen voor leveranciers, artikelen, categorieën en dimensiesjablonen.</span><span class="sxs-lookup"><span data-stu-id="acd77-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="acd77-141">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="acd77-141">Account + dimensions</span></span>           | <span data-ttu-id="acd77-142">Debet</span><span class="sxs-lookup"><span data-stu-id="acd77-142">Debit</span></span>  | <span data-ttu-id="acd77-143">Krediet</span><span class="sxs-lookup"><span data-stu-id="acd77-143">Credit</span></span> | <span data-ttu-id="acd77-144">Opmerking</span><span class="sxs-lookup"><span data-stu-id="acd77-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="acd77-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="acd77-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="acd77-146">250,00</span><span class="sxs-lookup"><span data-stu-id="acd77-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="acd77-147">Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd</span><span class="sxs-lookup"><span data-stu-id="acd77-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="acd77-148">Grootboekboekingen worden gemaakt om de vorderingen te registreren.</span><span class="sxs-lookup"><span data-stu-id="acd77-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="acd77-149">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="acd77-149">Account + dimensions</span></span>           | <span data-ttu-id="acd77-150">Debet</span><span class="sxs-lookup"><span data-stu-id="acd77-150">Debit</span></span>  | <span data-ttu-id="acd77-151">Krediet</span><span class="sxs-lookup"><span data-stu-id="acd77-151">Credit</span></span> | <span data-ttu-id="acd77-152">Opmerking</span><span class="sxs-lookup"><span data-stu-id="acd77-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="acd77-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="acd77-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="acd77-154">250,00</span><span class="sxs-lookup"><span data-stu-id="acd77-154">250.00</span></span> |        |         |
| <span data-ttu-id="acd77-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="acd77-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="acd77-156">250,00</span><span class="sxs-lookup"><span data-stu-id="acd77-156">250.00</span></span> |         |

<span data-ttu-id="acd77-157">In dit voorbeeld komt elke rekening die onderdeel is van de Rekeningstructuur - W&V overeen met de criteria van de boekdefinitie.</span><span class="sxs-lookup"><span data-stu-id="acd77-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="acd77-158">Wanneer dus 606500-OU\_1-OU\_3566-Training wordt beoordeeld, worden gegenereerde boekingen gemaakt voor de rekeningen die in het deelvenster **Gegenereerde vermeldingen** voor de boekdefinitie zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="acd77-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="acd77-159">Voorbeeld: Budgettoewijzingen</span><span class="sxs-lookup"><span data-stu-id="acd77-159">Example: Budget appropriations</span></span>
<span data-ttu-id="acd77-160">Wanneer u budgettoewijzingen inschakelt door **Aanwending van budget inschakelen** te selecteren op de pagina **Grootboekparameters**, moeten boekdefinities worden gebruikt om budgetregistervermeldingen te registeren in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="acd77-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="acd77-161">Wanneer een budgetbeheerconfiguratie actief is en is ingeschakeld, kunnen boekdefinities en transactieboekdefinities worden gebruikt om de registratie van toewijzingen, revisies, overboekingen, projecten, vaste activa en prognoseboekingen voor vraag en aanbod in het grootboek te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="acd77-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="acd77-162">U kunt een boekdefinitie voor budgetregisterregels die een budgettype **Oorspronkelijk budget** hebben en waarvoor toewijzingen zijn ingeschakeld, instellen door de module **Budget** te selecteren op de pagina **Boekdefinities**.</span><span class="sxs-lookup"><span data-stu-id="acd77-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="acd77-163">Vervolgens kunt u in het gebied **Budget** van de pagina **Boekdefinities van transacties** budgetcodes gebruiken om de boekdefinitie te koppelen aan budgetregisterregels met een budgettype **Oorspronkelijk budget**.</span><span class="sxs-lookup"><span data-stu-id="acd77-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="acd77-164">Wanneer budgettoewijzingen en boekdefinities zijn ingeschakeld, worden de budgetregisterregels geregistreerd voor budgetbeheer en in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="acd77-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="acd77-165">Boekdefinitie – Matchcriteria</span><span class="sxs-lookup"><span data-stu-id="acd77-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="acd77-166">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="acd77-166">Account structure</span></span>       | <span data-ttu-id="acd77-167">Rekeningnummerovereenkomst</span><span class="sxs-lookup"><span data-stu-id="acd77-167">Match account number</span></span> | <span data-ttu-id="acd77-168">Prioriteit </span><span class="sxs-lookup"><span data-stu-id="acd77-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="acd77-169">Rekeningstructuur - W&V</span><span class="sxs-lookup"><span data-stu-id="acd77-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="acd77-170">1</span><span class="sxs-lookup"><span data-stu-id="acd77-170">1</span></span>        |

<span data-ttu-id="acd77-171"><em>Een lege waarde in het veld \**Vereffeningsrekeningnummer</em>* betekent dat alle overeenkomende rekeningen in de gedefinieerde rekeningstructuur deel uitmaken van de afstemmingsregel.</span><span class="sxs-lookup"><span data-stu-id="acd77-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="acd77-172">Boekingsdefinitie – Gegenereerde vermeldingen</span><span class="sxs-lookup"><span data-stu-id="acd77-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="acd77-173">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="acd77-173">Account structure</span></span> | <span data-ttu-id="acd77-174">Gegenereerd rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="acd77-174">Generated account number</span></span>              | <span data-ttu-id="acd77-175">Gegenereerd debet/credit</span><span class="sxs-lookup"><span data-stu-id="acd77-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="acd77-176">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="acd77-176">Account structure</span></span> | <span data-ttu-id="acd77-177">300145 - -(geschatte opbrengstrekening)</span><span class="sxs-lookup"><span data-stu-id="acd77-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="acd77-178">Zelfde</span><span class="sxs-lookup"><span data-stu-id="acd77-178">Same</span></span>                   |
| <span data-ttu-id="acd77-179">Rekeningstructuur</span><span class="sxs-lookup"><span data-stu-id="acd77-179">Account structure</span></span> | <span data-ttu-id="acd77-180">300146 - -(toewijzingsrekening)</span><span class="sxs-lookup"><span data-stu-id="acd77-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="acd77-181">Balanceren</span><span class="sxs-lookup"><span data-stu-id="acd77-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="acd77-182">Transacties met de rekeningen dimensiewaarden en bedragen</span><span class="sxs-lookup"><span data-stu-id="acd77-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="acd77-183">U voert de rekeningen, dimensiewaarden en bedragen voor de budgetjournaalregel in op de pagina **Budgetregisterpost**.</span><span class="sxs-lookup"><span data-stu-id="acd77-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="acd77-184">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="acd77-184">Account + dimensions</span></span>           | <span data-ttu-id="acd77-185">Debet</span><span class="sxs-lookup"><span data-stu-id="acd77-185">Debit</span></span> | <span data-ttu-id="acd77-186">Krediet</span><span class="sxs-lookup"><span data-stu-id="acd77-186">Credit</span></span> | <span data-ttu-id="acd77-187">Opmerking</span><span class="sxs-lookup"><span data-stu-id="acd77-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="acd77-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="acd77-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="acd77-189">250,00</span><span class="sxs-lookup"><span data-stu-id="acd77-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="acd77-190">Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd</span><span class="sxs-lookup"><span data-stu-id="acd77-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="acd77-191">Gegenereerde grootboekboekingen worden gemaakt om het oorspronkelijke budget in elke dimensie te registreren.</span><span class="sxs-lookup"><span data-stu-id="acd77-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="acd77-192">Rekening + dimensies</span><span class="sxs-lookup"><span data-stu-id="acd77-192">Account + dimensions</span></span>           | <span data-ttu-id="acd77-193">Debet</span><span class="sxs-lookup"><span data-stu-id="acd77-193">Debit</span></span>  | <span data-ttu-id="acd77-194">Krediet</span><span class="sxs-lookup"><span data-stu-id="acd77-194">Credit</span></span> | <span data-ttu-id="acd77-195">Opmerking</span><span class="sxs-lookup"><span data-stu-id="acd77-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="acd77-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="acd77-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="acd77-197">250,00</span><span class="sxs-lookup"><span data-stu-id="acd77-197">250.00</span></span> |         |
| <span data-ttu-id="acd77-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="acd77-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="acd77-199">250,00</span><span class="sxs-lookup"><span data-stu-id="acd77-199">250.00</span></span> |        |         |

<span data-ttu-id="acd77-200">In dit voorbeeld komt elke rekening die onderdeel is van de Rekeningstructuur - W&V overeen met de criteria van de boekdefinitie.</span><span class="sxs-lookup"><span data-stu-id="acd77-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="acd77-201">Daarom worden de gegenereerde grootboekboekingen gemaakt wanneer 606400-OU\_1-OU\_3566-Training wordt beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="acd77-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






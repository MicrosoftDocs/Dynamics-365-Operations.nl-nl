---
title: Financiële rapporten proefbalans
description: In dit artikel worden de standaardrapporten voor proefbalansen beschreven. Hierin worden ook de bouwstenen beschreven die zijn gekoppeld aan deze rapporten, en hoe u de rapporten kunt aanpassen aan uw zakelijke behoeften.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd500c2880545ccae3cde7e2ead2fc5b83167d32
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595357"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="41fbf-104">Financiële rapporten proefbalans</span><span class="sxs-lookup"><span data-stu-id="41fbf-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41fbf-105">In dit artikel worden de standaardrapporten voor proefbalansen beschreven.</span><span class="sxs-lookup"><span data-stu-id="41fbf-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="41fbf-106">Hierin worden ook de bouwstenen beschreven die zijn gekoppeld aan deze rapporten, en hoe u de rapporten kunt aanpassen aan uw zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="41fbf-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="41fbf-107">Standaardrapporten proefbalans</span><span class="sxs-lookup"><span data-stu-id="41fbf-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="41fbf-108">Drie proefbalansrapporten zijn beschikbaar in financiële rapportage in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="41fbf-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="41fbf-109">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="41fbf-109">Default report</span></span>                                 | <span data-ttu-id="41fbf-110">Functie</span><span class="sxs-lookup"><span data-stu-id="41fbf-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41fbf-111">Gedetailleerde proefbalans - Standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="41fbf-112">Verschaft saldogegevens voor alle rekeningen en bevat debet- en creditsaldi, het nettobedrag van deze saldi samen met de transactiedatum, het boekstuk en de journaalomschrijving.</span><span class="sxs-lookup"><span data-stu-id="41fbf-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="41fbf-113">Overzicht proefbalans – Standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="41fbf-114">Verschaft saldogegevens voor alle rekeningen en bevat openings- en eindsaldi, debet- en creditsaldi samen met het bijbehorende nettoverschil.</span><span class="sxs-lookup"><span data-stu-id="41fbf-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="41fbf-115">Overzicht proefbalansjaar van jaar tot jaar - Standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="41fbf-116">Verschaft saldogegevens voor alle rekeningen en bevat openings- en eindsaldi, debet- en creditsaldi samen met het bijbehorende nettoverschil voor het huidige en het afgelopen jaar.</span><span class="sxs-lookup"><span data-stu-id="41fbf-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="41fbf-117">Bouwstenen</span><span class="sxs-lookup"><span data-stu-id="41fbf-117">Building blocks</span></span>
<span data-ttu-id="41fbf-118">In de financiële rapporten van de proefbalans worden de volgende bouwstenen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="41fbf-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="41fbf-119">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="41fbf-119">Default report</span></span>                                 | <span data-ttu-id="41fbf-120">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="41fbf-120">Row definition</span></span>          | <span data-ttu-id="41fbf-121">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="41fbf-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="41fbf-122">Gedetailleerde proefbalans - Standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="41fbf-123">Proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-123">Trial Balance - Default</span></span> | <span data-ttu-id="41fbf-124">Gedetailleerde proefbalans - Standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="41fbf-125">Overzicht proefbalans – Standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="41fbf-126">Proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-126">Trial Balance - Default</span></span> | <span data-ttu-id="41fbf-127">Samengevatte proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="41fbf-128">Overzicht proefbalansjaar van jaar tot jaar - Standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="41fbf-129">Proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-129">Trial Balance - Default</span></span> | <span data-ttu-id="41fbf-130">Samengevatte proefbalans van jaar tot jaar: standaard</span><span class="sxs-lookup"><span data-stu-id="41fbf-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="41fbf-131">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="41fbf-131">Row definition</span></span>

<span data-ttu-id="41fbf-132">De rijdefinitie, Proefbalans: standaard, bevat één rij die alle hoofdrekeningen bevat.</span><span class="sxs-lookup"><span data-stu-id="41fbf-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="41fbf-133">Zo kan iedereen het rapport genereren zonder wijzigingen te hoeven aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="41fbf-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="41fbf-134">Wanneer u het rapport weergeeft, zoomt u op één rij in om gegevens over elke rekening te bekijken.</span><span class="sxs-lookup"><span data-stu-id="41fbf-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="41fbf-135">U kunt de rijdefinitie wijzigen zodat deze meer details bevat.</span><span class="sxs-lookup"><span data-stu-id="41fbf-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="41fbf-136">Als u de rijdefinitie Proefbalans: standaard wilt wijzigen zodat rijen voor alle accounts worden opgenomen, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="41fbf-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="41fbf-137">Klik in het menu **Bewerken** en klik vervolgens op **Rijen invoegen van dimensies**.</span><span class="sxs-lookup"><span data-stu-id="41fbf-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="41fbf-138">Met de opdracht **Rijen invoegen van dimensies** kunt u kiezen welke dimensies u in uw rijdefinitie wilt hebben.</span><span class="sxs-lookup"><span data-stu-id="41fbf-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="41fbf-139">Voor deze rijdefinitie gaat u **Hoofdrekening** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="41fbf-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="41fbf-140">Zorg ervoor dat **Hoofdrekening** alle en-tekens (&) bevat en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="41fbf-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="41fbf-141">De rijdefinitie bevat nu alle hoofdrekeningen voor uw standaardrechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="41fbf-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="41fbf-142">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="41fbf-142">Column definition</span></span>

<span data-ttu-id="41fbf-143">In elk proefbalansrapport wordt een andere kolomdefinitie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="41fbf-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="41fbf-144">Deze kolomdefinities bevatten verschillende typen kolommen om verschillende detailniveaus en financiële gegevens te verschaffen.</span><span class="sxs-lookup"><span data-stu-id="41fbf-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="41fbf-145">**Gedetailleerde proefbalans: standaardkolomtypen:**</span><span class="sxs-lookup"><span data-stu-id="41fbf-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="41fbf-146">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="41fbf-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="41fbf-147">**ACCT**: rekeningcodes</span><span class="sxs-lookup"><span data-stu-id="41fbf-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="41fbf-148">**ATTR (3)**: kenmerken:</span><span class="sxs-lookup"><span data-stu-id="41fbf-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="41fbf-149">Transactiedatum</span><span class="sxs-lookup"><span data-stu-id="41fbf-149">Transaction Date</span></span>
        -   <span data-ttu-id="41fbf-150">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="41fbf-150">Voucher</span></span>
        -   <span data-ttu-id="41fbf-151">Journaalomschrijving</span><span class="sxs-lookup"><span data-stu-id="41fbf-151">Journal Description</span></span>
    -   <span data-ttu-id="41fbf-152">**FD**: financiële gegevens die alleen debetbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="41fbf-153">**FD**: financiële gegevens die alleen creditbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="41fbf-154">**CALC**: het nettoverschil</span><span class="sxs-lookup"><span data-stu-id="41fbf-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="41fbf-155">**Samengevatte proefbalans: standaardkolomtypen:**</span><span class="sxs-lookup"><span data-stu-id="41fbf-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="41fbf-156">**ACCT**: rekeningcodes</span><span class="sxs-lookup"><span data-stu-id="41fbf-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="41fbf-157">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="41fbf-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="41fbf-158">**ATTR**: een kernmerk:</span><span class="sxs-lookup"><span data-stu-id="41fbf-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="41fbf-159">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="41fbf-159">Voucher</span></span>
    -   <span data-ttu-id="41fbf-160">**FD**: de financiële gegevens van het beginsaldo</span><span class="sxs-lookup"><span data-stu-id="41fbf-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="41fbf-161">**FD**: financiële gegevens die alleen debetbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="41fbf-162">**FD**: financiële gegevens die alleen creditbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="41fbf-163">**CALC**: het nettoverschil</span><span class="sxs-lookup"><span data-stu-id="41fbf-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="41fbf-164">**CALC**: het eindsaldo</span><span class="sxs-lookup"><span data-stu-id="41fbf-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="41fbf-165">**Samengevatte proefbalans van jaar tot jaar: standaard:**</span><span class="sxs-lookup"><span data-stu-id="41fbf-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="41fbf-166">**ACCT**: rekeningcodes</span><span class="sxs-lookup"><span data-stu-id="41fbf-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="41fbf-167">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="41fbf-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="41fbf-168">**ATTR**: een kernmerk</span><span class="sxs-lookup"><span data-stu-id="41fbf-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="41fbf-169">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="41fbf-169">Voucher</span></span>
    -   <span data-ttu-id="41fbf-170">**FD**: de financiële gegevens van het beginsaldo voor het huidige jaar</span><span class="sxs-lookup"><span data-stu-id="41fbf-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="41fbf-171">**FD**: de financiële gegevens die alleen debetbedragen voor het huidige jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="41fbf-172">**FD**: de financiële gegevens die alleen creditbedragen voor het huidige jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="41fbf-173">**CALC**: het nettoverschil</span><span class="sxs-lookup"><span data-stu-id="41fbf-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="41fbf-174">**CALC**: het eindsaldo</span><span class="sxs-lookup"><span data-stu-id="41fbf-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="41fbf-175">**FD**: de financiële gegevens die alleen debetbedragen voor het afgelopen jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="41fbf-176">**FD**: de financiële gegevens die alleen creditbedragen voor het afgelopen jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="41fbf-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="41fbf-177">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="41fbf-177">Additional resources</span></span>
--------

[<span data-ttu-id="41fbf-178">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="41fbf-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="41fbf-179">Financiële rapporten weergeven</span><span class="sxs-lookup"><span data-stu-id="41fbf-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="41fbf-180">Blog met financiële rapportage van Dynamics</span><span class="sxs-lookup"><span data-stu-id="41fbf-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)




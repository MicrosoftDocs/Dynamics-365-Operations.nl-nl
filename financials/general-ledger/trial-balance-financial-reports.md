---
title: "Financiële rapporten proefbalans"
description: In dit artikel worden de standaardrapporten voor proefbalansen beschreven. Hierin worden ook de bouwstenen beschreven die zijn gekoppeld aan deze rapporten, en hoe u de rapporten kunt aanpassen aan uw zakelijke behoeften.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6405599186c8d07ac5ade19d3b7d27ae83b036ff
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="trial-balance-financial-reports"></a><span data-ttu-id="cff77-104">Financiële rapporten proefbalans</span><span class="sxs-lookup"><span data-stu-id="cff77-104">Trial balance financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cff77-105">In dit artikel worden de standaardrapporten voor proefbalansen beschreven.</span><span class="sxs-lookup"><span data-stu-id="cff77-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="cff77-106">Hierin worden ook de bouwstenen beschreven die zijn gekoppeld aan deze rapporten, en hoe u de rapporten kunt aanpassen aan uw zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="cff77-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="cff77-107">Standaardrapporten proefbalans</span><span class="sxs-lookup"><span data-stu-id="cff77-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="cff77-108">Drie proefbalansrapporten zijn beschikbaar in Financiële rapportage in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="cff77-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

| <span data-ttu-id="cff77-109">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="cff77-109">Default report</span></span>                                 | <span data-ttu-id="cff77-110">Functie</span><span class="sxs-lookup"><span data-stu-id="cff77-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cff77-111">Gedetailleerde proefbalans - Standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="cff77-112">Verschaft saldogegevens voor alle rekeningen en bevat debet- en creditsaldi, het nettobedrag van deze saldi samen met de transactiedatum, het boekstuk en de journaalomschrijving.</span><span class="sxs-lookup"><span data-stu-id="cff77-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="cff77-113">Overzicht proefbalans – Standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="cff77-114">Verschaft saldogegevens voor alle rekeningen en bevat openings- en eindsaldi, debet- en creditsaldi samen met het bijbehorende nettoverschil.</span><span class="sxs-lookup"><span data-stu-id="cff77-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="cff77-115">Overzicht proefbalansjaar van jaar tot jaar - Standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="cff77-116">Verschaft saldogegevens voor alle rekeningen en bevat openings- en eindsaldi, debet- en creditsaldi samen met het bijbehorende nettoverschil voor het huidige en het afgelopen jaar.</span><span class="sxs-lookup"><span data-stu-id="cff77-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="cff77-117">Bouwstenen</span><span class="sxs-lookup"><span data-stu-id="cff77-117">Building blocks</span></span>
<span data-ttu-id="cff77-118">In de financiële rapporten van de proefbalans worden de volgende bouwstenen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cff77-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="cff77-119">Standaardrapport</span><span class="sxs-lookup"><span data-stu-id="cff77-119">Default report</span></span>                                 | <span data-ttu-id="cff77-120">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="cff77-120">Row definition</span></span>          | <span data-ttu-id="cff77-121">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="cff77-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="cff77-122">Gedetailleerde proefbalans - Standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="cff77-123">Proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-123">Trial Balance - Default</span></span> | <span data-ttu-id="cff77-124">Gedetailleerde proefbalans - Standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="cff77-125">Overzicht proefbalans – Standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="cff77-126">Proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-126">Trial Balance - Default</span></span> | <span data-ttu-id="cff77-127">Samengevatte proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="cff77-128">Overzicht proefbalansjaar van jaar tot jaar - Standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="cff77-129">Proefbalans: standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-129">Trial Balance - Default</span></span> | <span data-ttu-id="cff77-130">Samengevatte proefbalans van jaar tot jaar: standaard</span><span class="sxs-lookup"><span data-stu-id="cff77-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="cff77-131">Rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="cff77-131">Row definition</span></span>

<span data-ttu-id="cff77-132">De rijdefinitie, Proefbalans: standaard, bevat één rij die alle hoofdrekeningen bevat.</span><span class="sxs-lookup"><span data-stu-id="cff77-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="cff77-133">Zo kan iedereen het rapport genereren zonder wijzigingen te hoeven aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="cff77-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="cff77-134">Wanneer u het rapport weergeeft, zoomt u op één rij in om gegevens over elke rekening te bekijken.</span><span class="sxs-lookup"><span data-stu-id="cff77-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="cff77-135">U kunt de rijdefinitie wijzigen zodat deze meer details bevat.</span><span class="sxs-lookup"><span data-stu-id="cff77-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="cff77-136">Als u de rijdefinitie Proefbalans: standaard wilt wijzigen zodat rijen voor alle accounts worden opgenomen, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="cff77-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="cff77-137">Klik in het menu **Bewerken** en klik vervolgens op **Rijen invoegen van dimensies**.</span><span class="sxs-lookup"><span data-stu-id="cff77-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="cff77-138">Met de opdracht **Rijen invoegen van dimensies** kunt u kiezen welke dimensies u in uw rijdefinitie wilt hebben.</span><span class="sxs-lookup"><span data-stu-id="cff77-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="cff77-139">Voor deze rijdefinitie gaat u **Hoofdrekening** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cff77-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="cff77-140">Zorg ervoor dat **Hoofdrekening** alle en-tekens (&) bevat en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cff77-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="cff77-141">De rijdefinitie bevat nu alle hoofdrekeningen voor uw standaardrechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="cff77-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="cff77-142">Kolomdefinitie</span><span class="sxs-lookup"><span data-stu-id="cff77-142">Column definition</span></span>

<span data-ttu-id="cff77-143">In elk proefbalansrapport wordt een andere kolomdefinitie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cff77-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="cff77-144">Deze kolomdefinities bevatten verschillende typen kolommen om verschillende detailniveaus en financiële gegevens te verschaffen.</span><span class="sxs-lookup"><span data-stu-id="cff77-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="cff77-145">**Gedetailleerde proefbalans: standaardkolomtypen:**</span><span class="sxs-lookup"><span data-stu-id="cff77-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="cff77-146">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="cff77-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="cff77-147">**ACCT**: rekeningcodes</span><span class="sxs-lookup"><span data-stu-id="cff77-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="cff77-148">**ATTR (3)**: kenmerken:</span><span class="sxs-lookup"><span data-stu-id="cff77-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="cff77-149">Transactiedatum</span><span class="sxs-lookup"><span data-stu-id="cff77-149">Transaction Date</span></span>
        -   <span data-ttu-id="cff77-150">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="cff77-150">Voucher</span></span>
        -   <span data-ttu-id="cff77-151">Journaalomschrijving</span><span class="sxs-lookup"><span data-stu-id="cff77-151">Journal Description</span></span>
    -   <span data-ttu-id="cff77-152">**FD**: financiële gegevens die alleen debetbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="cff77-153">**FD**: financiële gegevens die alleen creditbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="cff77-154">**CALC**: het nettoverschil</span><span class="sxs-lookup"><span data-stu-id="cff77-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="cff77-155">**Samengevatte proefbalans: standaardkolomtypen:**</span><span class="sxs-lookup"><span data-stu-id="cff77-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="cff77-156">**ACCT**: rekeningcodes</span><span class="sxs-lookup"><span data-stu-id="cff77-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="cff77-157">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="cff77-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="cff77-158">**ATTR**: een kernmerk:</span><span class="sxs-lookup"><span data-stu-id="cff77-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="cff77-159">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="cff77-159">Voucher</span></span>
    -   <span data-ttu-id="cff77-160">**FD**: de financiële gegevens van het beginsaldo</span><span class="sxs-lookup"><span data-stu-id="cff77-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="cff77-161">**FD**: financiële gegevens die alleen debetbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="cff77-162">**FD**: financiële gegevens die alleen creditbedragen bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="cff77-163">**CALC**: het nettoverschil</span><span class="sxs-lookup"><span data-stu-id="cff77-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="cff77-164">**CALC**: het eindsaldo</span><span class="sxs-lookup"><span data-stu-id="cff77-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="cff77-165">**Samengevatte proefbalans van jaar tot jaar: standaard:**</span><span class="sxs-lookup"><span data-stu-id="cff77-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="cff77-166">**ACCT**: rekeningcodes</span><span class="sxs-lookup"><span data-stu-id="cff77-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="cff77-167">**DESC**: de omschrijving van de rijdefinitie</span><span class="sxs-lookup"><span data-stu-id="cff77-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="cff77-168">**ATTR**: een kernmerk</span><span class="sxs-lookup"><span data-stu-id="cff77-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="cff77-169">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="cff77-169">Voucher</span></span>
    -   <span data-ttu-id="cff77-170">**FD**: de financiële gegevens van het beginsaldo voor het huidige jaar</span><span class="sxs-lookup"><span data-stu-id="cff77-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="cff77-171">**FD**: de financiële gegevens die alleen debetbedragen voor het huidige jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="cff77-172">**FD**: de financiële gegevens die alleen creditbedragen voor het huidige jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="cff77-173">**CALC**: het nettoverschil</span><span class="sxs-lookup"><span data-stu-id="cff77-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="cff77-174">**CALC**: het eindsaldo</span><span class="sxs-lookup"><span data-stu-id="cff77-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="cff77-175">**FD**: de financiële gegevens die alleen debetbedragen voor het afgelopen jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="cff77-176">**FD**: de financiële gegevens die alleen creditbedragen voor het afgelopen jaar bevatten</span><span class="sxs-lookup"><span data-stu-id="cff77-176">**FD** – Financial data that contains only credits for the last year</span></span>

 

<a name="see-also"></a><span data-ttu-id="cff77-177">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cff77-177">See also</span></span>
--------

[<span data-ttu-id="cff77-178">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="cff77-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="cff77-179">Financiële rapporten weergeven</span><span class="sxs-lookup"><span data-stu-id="cff77-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="cff77-180">Blog met financiële rapportage van Dynamics</span><span class="sxs-lookup"><span data-stu-id="cff77-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)





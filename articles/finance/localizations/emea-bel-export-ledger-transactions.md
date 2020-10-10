---
title: Export grootboektransacties
description: Dit onderwerp bevat informatie over het exporteren van grootboekrekeningsaldi naar een ASCII-bestand (tekst zonder opmaak) in CED-indeling voor België.
author: anasyash
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportExtraFieldsBE
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 273103
ms.search.region: Belgium
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.openlocfilehash: 4db6d56d72b9c3e4c9040c791e0cca279f794633
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819998"
---
# <a name="export-ledger-transactions"></a><span data-ttu-id="d07ec-103">Export grootboektransacties</span><span class="sxs-lookup"><span data-stu-id="d07ec-103">Export ledger transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d07ec-104">De functie die in dit onderwerp wordt beschreven, wordt gebruikt om het totaalsaldo van elke grootboekrekening voor een bepaalde periode te exporteren naar een bestand zonder opmaak (ASCII) in CED-indeling.</span><span class="sxs-lookup"><span data-stu-id="d07ec-104">The feature described in this topic is used to export the total balance of each ledger account for a specific period to a plain text (ASCII) file in .CED format.</span></span> <span data-ttu-id="d07ec-105">U kunt het gegenereerde bestand vervolgens importeren in software van derden om een boekhoudingsrapport te maken in overeenstemming met de vereisten die per land/regio gelden.</span><span class="sxs-lookup"><span data-stu-id="d07ec-105">You can then import the generated file into third-party software to create an accounting report according to country/region-specific requirements.</span></span>

<span data-ttu-id="d07ec-106">Deze functionaliteit is beschikbaar voor rechtspersonen die hun primaire adres in België hebben.</span><span class="sxs-lookup"><span data-stu-id="d07ec-106">This functionality is available for legal entities that have their primary address in Belgium.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d07ec-107">Vereisten</span><span class="sxs-lookup"><span data-stu-id="d07ec-107">Prerequisites</span></span>

### <a name="create-posting-journals"></a><span data-ttu-id="d07ec-108">Boekingsjournalen maken</span><span class="sxs-lookup"><span data-stu-id="d07ec-108">Create posting journals</span></span>

1. <span data-ttu-id="d07ec-109">Ga naar **Grootboek** \> **Journaalinstellingen** \> **Boekingsjournalen**.</span><span class="sxs-lookup"><span data-stu-id="d07ec-109">Go to **General ledger** \> **Journal setup** \> **Posting journals**.</span></span>
2. <span data-ttu-id="d07ec-110">Selecteer op de pagina **Grootboekinstellingen** **Maken**.</span><span class="sxs-lookup"><span data-stu-id="d07ec-110">On the **Journal setup** page, select **Create**.</span></span> <span data-ttu-id="d07ec-111">Er worden automatisch boekingsjournalen en bijbehorende nummerreeksen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d07ec-111">Posting journals and corresponding number sequences are automatically created.</span></span>

## <a name="export-ledger-transactions-to-a-plain-text-file-in-ced-format"></a><span data-ttu-id="d07ec-112">Grootboektransacties in CED-indeling naar een bestand met tekst zonder opmaak exporteren</span><span class="sxs-lookup"><span data-stu-id="d07ec-112">Export ledger transactions to a plain text file in CED format</span></span>

1. <span data-ttu-id="d07ec-113">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van ER-configuraties (elektronische rapportage) voor de volgende rapportindeling:</span><span class="sxs-lookup"><span data-stu-id="d07ec-113">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the Shared asset library, download the latest versions of the Electronic reporting (ER) configurations for the following report format:</span></span>

    - <span data-ttu-id="d07ec-114">Exportindeling voor grootboektransacties (BE)</span><span class="sxs-lookup"><span data-stu-id="d07ec-114">Ledger transaction export format (BE)</span></span>

    <span data-ttu-id="d07ec-115">Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](https://docs.microsoft.com/dynamics365/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="d07ec-115">For more information, see [Download Electronic reporting configurations from Lifecycle Services](https://docs.microsoft.com/dynamics365/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

2. <span data-ttu-id="d07ec-116">Ga in Dynamics 365 Finance naar **Grootboek** \> **Periodieke taken** \> **Grootboektransacties exporteren**.</span><span class="sxs-lookup"><span data-stu-id="d07ec-116">In Dynamics 365 Finance, go to **General ledger** \> **Periodic tasks** \> **Export ledger transactions**.</span></span>
3. <span data-ttu-id="d07ec-117">Selecteer in het dialoogvenster **Grootboektransacties in CED-indeling naar een ASCII-bestand exporteren** in het veld **Indelingstoewijzing** de indeling **Exportindeling voor grootboektransacties (BE)** die u zojuist hebt gedownload, en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="d07ec-117">In the **Export ledger transactions to an ASCII file in CED format** dialog box, in the **Format mapping** field, select the **Ledger transaction export format (BE)** format that you just downloaded, and then select **OK**.</span></span>
4. <span data-ttu-id="d07ec-118">Stel in het dialoogvenster **Parameters elektronisch rapport** de volgende velden in.</span><span class="sxs-lookup"><span data-stu-id="d07ec-118">In the **Electronic report parameters** dialog box, set the following fields.</span></span>

| <span data-ttu-id="d07ec-119">**Veld**</span><span class="sxs-lookup"><span data-stu-id="d07ec-119">**Field**</span></span>          | <span data-ttu-id="d07ec-120">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="d07ec-120">**Description**</span></span>                                                             |
|--------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="d07ec-121">Begindatum</span><span class="sxs-lookup"><span data-stu-id="d07ec-121">From date</span></span>          | <span data-ttu-id="d07ec-122">Voer de eerste dag van de aangifteperiode in.</span><span class="sxs-lookup"><span data-stu-id="d07ec-122">Enter the first day of the reporting period.</span></span>                                |
| <span data-ttu-id="d07ec-123">Einddatum</span><span class="sxs-lookup"><span data-stu-id="d07ec-123">To date</span></span>            | <span data-ttu-id="d07ec-124">Voer de laatste dag van de aangifteperiode in.</span><span class="sxs-lookup"><span data-stu-id="d07ec-124">Enter the last day of the reporting period.</span></span>                                 |
| <span data-ttu-id="d07ec-125">Aangifte in euro's</span><span class="sxs-lookup"><span data-stu-id="d07ec-125">Reporting in euros</span></span> | <span data-ttu-id="d07ec-126">Stel deze optie in op **Ja** als het bedrijf een andere valuta dan euro gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d07ec-126">Set this option to **Yes** if the company uses a currency other than euros.</span></span> |

5. <span data-ttu-id="d07ec-127">Selecteer **OK** om het txt-bestand te genereren en te downloaden.</span><span class="sxs-lookup"><span data-stu-id="d07ec-127">Select **OK** to generate and download the .txt file.</span></span>

    <span data-ttu-id="d07ec-128">U boekt bijvoorbeeld de volgende grootboektransacties in het DEMF-bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d07ec-128">For example, you post the following ledger transactions in the DEMF company.</span></span>

| <span data-ttu-id="d07ec-129">**Datum**</span><span class="sxs-lookup"><span data-stu-id="d07ec-129">**Date**</span></span>        | <span data-ttu-id="d07ec-130">**Transactietype**</span><span class="sxs-lookup"><span data-stu-id="d07ec-130">**Transaction type**</span></span> | <span data-ttu-id="d07ec-131">**Hoofdrekening**</span><span class="sxs-lookup"><span data-stu-id="d07ec-131">**Main account**</span></span>          | <span data-ttu-id="d07ec-132">**Tegenrekening**</span><span class="sxs-lookup"><span data-stu-id="d07ec-132">**Offset account**</span></span>        | <span data-ttu-id="d07ec-133">**Nettobedrag**</span><span class="sxs-lookup"><span data-stu-id="d07ec-133">**Amount net**</span></span> | <span data-ttu-id="d07ec-134">**Btw-bedrag**</span><span class="sxs-lookup"><span data-stu-id="d07ec-134">**VAT amount**</span></span> | <span data-ttu-id="d07ec-135">**Btw-code**</span><span class="sxs-lookup"><span data-stu-id="d07ec-135">**Sales tax code**</span></span> |
|-----------------|----------------------|---------------------------|---------------------------|----------------|----------------|--------------------|
| <span data-ttu-id="d07ec-136">1 januari 2020</span><span class="sxs-lookup"><span data-stu-id="d07ec-136">January 1, 2020</span></span> | <span data-ttu-id="d07ec-137">Klantfactuur</span><span class="sxs-lookup"><span data-stu-id="d07ec-137">Customer invoice</span></span>     | <span data-ttu-id="d07ec-138">110110 – Bankrekening in USD</span><span class="sxs-lookup"><span data-stu-id="d07ec-138">110110 – Bank account USD</span></span> |                           | <span data-ttu-id="d07ec-139">1.000</span><span class="sxs-lookup"><span data-stu-id="d07ec-139">1,000</span></span>          | <span data-ttu-id="d07ec-140">190</span><span class="sxs-lookup"><span data-stu-id="d07ec-140">190</span></span>            | <span data-ttu-id="d07ec-141">VAT19</span><span class="sxs-lookup"><span data-stu-id="d07ec-141">VAT19</span></span>              |
| <span data-ttu-id="d07ec-142">1 januari 2020</span><span class="sxs-lookup"><span data-stu-id="d07ec-142">January 1, 2020</span></span> | <span data-ttu-id="d07ec-143">Leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="d07ec-143">Vendor invoice</span></span>       |                           | <span data-ttu-id="d07ec-144">110120 – Bankrekening in CNY</span><span class="sxs-lookup"><span data-stu-id="d07ec-144">110120 – Bank account CNY</span></span> | <span data-ttu-id="d07ec-145">1,095</span><span class="sxs-lookup"><span data-stu-id="d07ec-145">1,095</span></span>          | <span data-ttu-id="d07ec-146">76.65</span><span class="sxs-lookup"><span data-stu-id="d07ec-146">76.65</span></span>          | <span data-ttu-id="d07ec-147">EU7</span><span class="sxs-lookup"><span data-stu-id="d07ec-147">EU7</span></span>                |
| <span data-ttu-id="d07ec-148">1 januari 2020</span><span class="sxs-lookup"><span data-stu-id="d07ec-148">January 1, 2020</span></span> | <span data-ttu-id="d07ec-149">Klantfactuur</span><span class="sxs-lookup"><span data-stu-id="d07ec-149">Customer invoice</span></span>     | <span data-ttu-id="d07ec-150">110115 – Bankrekening in CAD</span><span class="sxs-lookup"><span data-stu-id="d07ec-150">110115 – Bank account CAD</span></span> |                           | <span data-ttu-id="d07ec-151">800</span><span class="sxs-lookup"><span data-stu-id="d07ec-151">800</span></span>            | <span data-ttu-id="d07ec-152">0</span><span class="sxs-lookup"><span data-stu-id="d07ec-152">0</span></span>              | <span data-ttu-id="d07ec-153">EUS</span><span class="sxs-lookup"><span data-stu-id="d07ec-153">EUS</span></span>                |

<span data-ttu-id="d07ec-154">In dit geval bevat het gegenereerde bestand de volgende gegevens.</span><span class="sxs-lookup"><span data-stu-id="d07ec-154">In this case, the file that is generated contains the following data.</span></span>

![Grootboektransactiegegevens](media/1_Export_ledger_transactions.png)

<span data-ttu-id="d07ec-156">Hier volgt een uitleg van de kolommen in dit bestand:</span><span class="sxs-lookup"><span data-stu-id="d07ec-156">Here is an explanation of the columns in this file:</span></span>

- <span data-ttu-id="d07ec-157">In de eerste kolom wordt de grootboekrekeningcode weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d07ec-157">The first column shows the ledger account code.</span></span>
- <span data-ttu-id="d07ec-158">In de tweede kolom wordt het debetsaldo van de grootboekrekening weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d07ec-158">The second column shows the debit balance on the ledger account.</span></span>
- <span data-ttu-id="d07ec-159">In de derde kolom wordt het creditsaldo van de grootboekrekening weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d07ec-159">The third column shows the credit balance on the ledger account.</span></span>
- <span data-ttu-id="d07ec-160">In de vierde kolom wordt de naam van de grootboekrekening weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d07ec-160">The fourth column shows the name of the ledger account.</span></span>

> [!NOTE]
> <span data-ttu-id="d07ec-161">Als u grootboektransacties voor klantfacturen wilt boeken, gaat u naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.</span><span class="sxs-lookup"><span data-stu-id="d07ec-161">To post ledger transactions for customer invoices, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span> <span data-ttu-id="d07ec-162">Voor leveranciersfacturen gaat u naar **Leveranciers** \> **Facturen** \> **Facturenjournaal**.</span><span class="sxs-lookup"><span data-stu-id="d07ec-162">For vendor invoices, go to **Accounts payable** \> **Invoices** \> **Invoice journal**.</span></span>
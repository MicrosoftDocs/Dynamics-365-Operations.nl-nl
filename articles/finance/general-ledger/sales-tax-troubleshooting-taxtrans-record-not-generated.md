---
title: TaxTrans-record is niet gegenereerd
description: Dit onderwerp bevat informatie voor het oplossen van problemen wanneer een TaxTrans-record niet wordt gegenereerd.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018776"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="6c370-103">TaxTrans-record is niet gegenereerd</span><span class="sxs-lookup"><span data-stu-id="6c370-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c370-104">Als u **Geboekte btw** voor een transactie selecteert, maar op de pagina **Geboekte btw** worden geen belastingregels weergegeven of er ontbreekt een belastingregel, is de **TaxTrans**-record mogelijk niet gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="6c370-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="6c370-105">[![Pagina Geboekte btw zonder regelartikelen](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="6c370-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="6c370-106">Volg de stappen in de volgende secties zoals vereist om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="6c370-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="6c370-107">Controleer de btw voordat u een transactie boekt</span><span class="sxs-lookup"><span data-stu-id="6c370-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="6c370-108">Voordat u de transactie boekt, selecteert u op de pagina **Factuur boeken** de **Btw** om de berekening te controleren.</span><span class="sxs-lookup"><span data-stu-id="6c370-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="6c370-109">[![Knop btw op de pagina Factuur boeken](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="6c370-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="6c370-110">Controleer op de pagina **Tijdelijke btw-transacties** het resultaat van de berekening.</span><span class="sxs-lookup"><span data-stu-id="6c370-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="6c370-111">Als er geen belasting is berekend, ga naar [Belasting is niet berekend of belastingbedrag is nul](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="6c370-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="6c370-112">Zoek de TaxTrans-record in alle geboekte btw</span><span class="sxs-lookup"><span data-stu-id="6c370-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="6c370-113">Ga naar **Belasting** \> **Query's en rapporten** \> **Vragen over btw** > **Geboekte btw**.</span><span class="sxs-lookup"><span data-stu-id="6c370-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="6c370-114">Selecteer in de kolomkop **Boekstuk** het filtersymbool om de **TaxTrans**-record te zoeken.</span><span class="sxs-lookup"><span data-stu-id="6c370-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="6c370-115">Als u de btw-records heeft gevonden, controleert u de datum.</span><span class="sxs-lookup"><span data-stu-id="6c370-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="6c370-116">Als de datum verschilt van de datum van de journaalkoptekst, opent u een Microsoft-serviceaanvraag voor extra ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="6c370-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="6c370-117">[![Pagina Geboekte btw](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="6c370-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="6c370-118">Foutopsporing voor het controleren van details</span><span class="sxs-lookup"><span data-stu-id="6c370-118">Debug to check details</span></span>

1. <span data-ttu-id="6c370-119">Voor meer informatie over foutopsporing en te bepalen of **TmpTaxWorkTrans** en **TaxUncommitted** juist zijn gegenereerd, ga naar [Veldwaarde in TaxTrans is onjuist](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="6c370-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="6c370-120">Als **TaxTmpWorkTrans** of **TaxUncommitted** juist zijn gegenereerd, voegt u een onderbrekingspunt toe bij **TaxPost::SaveAndPost()** en **Tax::SaveAndPost** om erachter te komen waarom **TaxTrans** niet is ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="6c370-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="6c370-121">[![Onderbrekingspunten toegevoegd in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="6c370-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="6c370-122">[![Resultaten van toegevoegde onderbrekingspunten](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="6c370-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="6c370-123">Bekijk of er een aanpassing bestaat</span><span class="sxs-lookup"><span data-stu-id="6c370-123">Determine whether customization exists</span></span>

<span data-ttu-id="6c370-124">Als u de stappen in de vorige secties hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat.</span><span class="sxs-lookup"><span data-stu-id="6c370-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="6c370-125">Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="6c370-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

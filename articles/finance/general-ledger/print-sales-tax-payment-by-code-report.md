---
title: Rapport Btw-betaling per code afdrukken
description: Dit onderwerp bevat informatie over de instellingen en acties die vereist zijn om het rapport Btw-betaling per code af te drukken in de valuta van de boekhouding of de btw-code.
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260250"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="d30af-103">Rapport Btw-betaling per code afdrukken</span><span class="sxs-lookup"><span data-stu-id="d30af-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d30af-104">Als u het rapport **Btw-betaling per code** wilt afdrukken, gaat u naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-betaling per code**.</span><span class="sxs-lookup"><span data-stu-id="d30af-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="d30af-105">Standaard worden rapportbedragen gegenereerd in de valuta voor boekhouding van de rechtspersoon voor alle aangiftecodes die zijn ingesteld op de pagina **Btw-aangiftecodes**.</span><span class="sxs-lookup"><span data-stu-id="d30af-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="d30af-106">U kunt dit rapport ook zo genereren dat de btw-betalingsbedragen worden weergegeven in de valuta van de btw-codes voor alle aangiftecodes die aan btw-codes zijn toegewezen op de pagina **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="d30af-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="d30af-107">De functie inschakelen</span><span class="sxs-lookup"><span data-stu-id="d30af-107">Turn on the feature</span></span>

<span data-ttu-id="d30af-108">Schakel in het werkgebied **Functiebeheer** de volgende functie in: **Het rapport btw-betaling per code genereren in de valuta van de btw-code**.</span><span class="sxs-lookup"><span data-stu-id="d30af-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="d30af-109">Het rapport uitvoeren</span><span class="sxs-lookup"><span data-stu-id="d30af-109">Run the report</span></span>

1. <span data-ttu-id="d30af-110">Ga naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-betaling per code**.</span><span class="sxs-lookup"><span data-stu-id="d30af-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="d30af-111">Selecteer in het veld **Rapportvaluta** een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="d30af-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="d30af-112">**Valuta voor boekhouding**: druk de rapportbedragen af in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="d30af-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="d30af-113">**Valuta van btw-code**: druk de rapportbedragen af in de valuta van de btw-codes.</span><span class="sxs-lookup"><span data-stu-id="d30af-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Dialoogvenster Btw-betaling per code](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="d30af-115">In de volgende afbeelding ziet u een voorbeeld van het gegenereerde rapport.</span><span class="sxs-lookup"><span data-stu-id="d30af-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="d30af-116">In het rapport wordt aangegeven dat de aangiftecode **101** de valuta **EUR** gebruikt als het veld **Btw-valuta** wordt ingesteld op **EUR** voor de btw-code waaraan de aangiftecode is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d30af-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Voorbeeld van rapport Btw-betaling per code](media/Sales-tax-payment-by-code-2.png)

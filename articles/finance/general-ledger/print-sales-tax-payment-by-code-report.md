---
title: Rapport Btw-betaling per code afdrukken
description: Dit onderwerp bevat informatie over de instellingen en acties die vereist zijn om het rapport Btw-betaling per code af te drukken in de valuta van de boekhouding of de btw-code.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: 7033999f7258e9ddd1d01620f9ad416e94ef3111
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441973"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="bbe27-103">Rapport Btw-betaling per code afdrukken</span><span class="sxs-lookup"><span data-stu-id="bbe27-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbe27-104">Als u het rapport **Btw-betaling per code** wilt afdrukken, gaat u naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-betaling per code**.</span><span class="sxs-lookup"><span data-stu-id="bbe27-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="bbe27-105">Standaard worden rapportbedragen gegenereerd in de valuta voor boekhouding van de rechtspersoon voor alle aangiftecodes die zijn ingesteld op de pagina **Btw-aangiftecodes**.</span><span class="sxs-lookup"><span data-stu-id="bbe27-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="bbe27-106">U kunt dit rapport ook zo genereren dat de btw-betalingsbedragen worden weergegeven in de valuta van de btw-codes voor alle aangiftecodes die aan btw-codes zijn toegewezen op de pagina **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="bbe27-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="bbe27-107">De functie inschakelen</span><span class="sxs-lookup"><span data-stu-id="bbe27-107">Turn on the feature</span></span>

<span data-ttu-id="bbe27-108">Schakel in het werkgebied **Functiebeheer** de volgende functie in: **Het rapport btw-betaling per code genereren in de valuta van de btw-code**.</span><span class="sxs-lookup"><span data-stu-id="bbe27-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="bbe27-109">Het rapport uitvoeren</span><span class="sxs-lookup"><span data-stu-id="bbe27-109">Run the report</span></span>

1. <span data-ttu-id="bbe27-110">Ga naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-betaling per code**.</span><span class="sxs-lookup"><span data-stu-id="bbe27-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="bbe27-111">Selecteer in het veld **Rapportvaluta** een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="bbe27-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="bbe27-112">**Valuta voor boekhouding**: druk de rapportbedragen af in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="bbe27-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="bbe27-113">**Valuta van btw-code**: druk de rapportbedragen af in de valuta van de btw-codes.</span><span class="sxs-lookup"><span data-stu-id="bbe27-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Dialoogvenster Btw-betaling per code](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="bbe27-115">In de volgende afbeelding ziet u een voorbeeld van het gegenereerde rapport.</span><span class="sxs-lookup"><span data-stu-id="bbe27-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="bbe27-116">In het rapport wordt aangegeven dat de aangiftecode **101** de valuta **EUR** gebruikt als het veld **Btw-valuta** wordt ingesteld op **EUR** voor de btw-code waaraan de aangiftecode is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="bbe27-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Voorbeeld van rapport Btw-betaling per code](media/Sales-tax-payment-by-code-2.png)

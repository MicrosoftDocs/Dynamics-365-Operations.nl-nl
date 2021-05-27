---
title: Certificaatnummers en -datums voor TDS-transacties bijwerken
description: In dit onderwerp wordt uitgelegd hoe u de nummers en datums van het certificaat voor terugvordering kunt bijwerken die zijn geregistreerd voor leverancier-, klant- en grootboekrekeningen voor TDS (belasting ingehouden op bron).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023144"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="c52a8-103">Certificaatnummers en -datums voor TDS-transacties bijwerken</span><span class="sxs-lookup"><span data-stu-id="c52a8-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c52a8-104">In dit onderwerp wordt uitgelegd hoe u de nummers en datums van het certificaat voor terugvordering kunt bijwerken die zijn geregistreerd voor leverancier-, klant- en grootboekrekeningen voor TDS (belasting ingehouden op bron).</span><span class="sxs-lookup"><span data-stu-id="c52a8-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="c52a8-105">U kunt de certificaten voor TDS-transacties weergeven op de pagina **Certificaten voor terugvordering**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="c52a8-106">U kunt de certificaten bijwerken met de pagina **Certificaten bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="c52a8-107">Volg deze stappen om certificaatnummers en -datums voor TDS-transacties bij te werken.</span><span class="sxs-lookup"><span data-stu-id="c52a8-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="c52a8-108">Ga naar **Belasting \> Aangiften \> Bronbelasting \> Certificaat bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="c52a8-109">[![Pagina Certificaat bijwerken](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="c52a8-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="c52a8-110">Selecteer **TDS** op de pagina **Certificaat bijwerken** in de sectie **Selecteren** in het veld **Belastingtype**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="c52a8-111">Selecteer in het veld **Certificaatnummer** het TDS-certificaatnummer van de klant of leverancier.</span><span class="sxs-lookup"><span data-stu-id="c52a8-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c52a8-112">Het veld **Certificaatnummer** bevat alleen TDS-certificaatnummers waar het selectievakje **Afgesloten** voor is gewist op de pagina **Certificaten voor terugvordering**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="c52a8-113">In het veld **Certificaatdatum** wordt de datum van het certificaat weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c52a8-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="c52a8-114">In het veld **Rekeningtype** wordt het type rekening vermeld waar het TDS-certificaatnummer voor wordt ontvangen, en in het veld **Naam** wordt de naam van de rekening vermeld.</span><span class="sxs-lookup"><span data-stu-id="c52a8-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="c52a8-115">Voer in in de velden **Begindatum** en **Einddatum** de begin- en einddatum van de periode in waarvoor u de TDS-transacties wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="c52a8-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="c52a8-116">Selecteer **Gegevens weergeven** om de TDS-transacties weer te geven die tijdens de geselecteerde periode zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="c52a8-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="c52a8-117">Op het tabblad **Overzicht** bevat het raster in het bovenste deelvenster de volgende informatie over elke TDS-transactie die voor de leverancier of klant is geboekt tijdens de geselecteerde periode:</span><span class="sxs-lookup"><span data-stu-id="c52a8-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="c52a8-118">**Boekstuk**: het boekstuknummer van de TDS-transactie.</span><span class="sxs-lookup"><span data-stu-id="c52a8-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="c52a8-119">**Datum**: de vervaldatum van de TDS-transactie.</span><span class="sxs-lookup"><span data-stu-id="c52a8-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="c52a8-120">**Bedrag**: het factuurbedrag waarover de TDS is berekend.</span><span class="sxs-lookup"><span data-stu-id="c52a8-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="c52a8-121">**Belastingbedrag**: het TDS-belastingbedrag dat voor de transactie is berekend.</span><span class="sxs-lookup"><span data-stu-id="c52a8-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="c52a8-122">Als u specifieke TDS-transacties van het bovenste raster naar het onderste raster wilt verplaatsen, selecteert u de transacties en selecteert u **Opnemen**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="c52a8-123">U kunt ook **Alle opnemen** selecteren om alle TDS-transacties van het bovenste raster naar het onderste raster te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="c52a8-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="c52a8-124">Als u specifieke TDS-transacties of alle TDS-transacties van het onderste raster naar het bovenste raster wilt verplaatsen, gebruikt u de knop **Uitsluiten** of **Alle uitsluiten**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="c52a8-125">Selecteer **Bijwerken** om de velden **Certificaatnummer** en **Certificaatdatum** voor TDS-transacties bij te werken in het onderste raster.</span><span class="sxs-lookup"><span data-stu-id="c52a8-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="c52a8-126">Ga naar **Belasting \> Indirecte belasting \> Bronbelasting \> Certificaat voor terugvordering** en selecteer **Opvraag** om de bijgewerkte transactieregels weer te geven met de nieuwe certificaatnummers op de pagina **Certificaattransacties**.</span><span class="sxs-lookup"><span data-stu-id="c52a8-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="c52a8-127">[![Certificaattransacties](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="c52a8-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>

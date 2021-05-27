---
title: Geboekte TDS-betalingen en -transacties weergeven voor een TDS-vereffeningsperiode
description: In dit onderwerp wordt uitgelegd hoe u de TDS-betalingen (belasting ingehouden op bron)en -transacties kunt weergeven die zijn geboekt voor een vereffeningsperiode.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023141"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="ff2d0-103">Geboekte TDS-betalingen en -transacties weergeven voor een TDS-vereffeningsperiode</span><span class="sxs-lookup"><span data-stu-id="ff2d0-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff2d0-104">In dit onderwerp wordt uitgelegd hoe u de TDS-betalingen (belasting ingehouden op bron)en -transacties kunt weergeven die zijn geboekt voor een vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="ff2d0-105">Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Vereffeningsperioden voor bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="ff2d0-106">[![Pagina Vereffeningsperioden voor bronbelasting](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="ff2d0-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="ff2d0-107">Op de pagina **Vereffeningsperioden voor bronbelasting** selecteert u **Bronbelastingbetalingen** om de pagina **Bronbelastingbetalingen** te openen, waar u de TDS-vereffeningen kunt bekijken die voor een bepaalde TDS-vereffeningsperiode zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="ff2d0-108">Op het tabblad **Overzicht** wordt de volgende informatie weergegeven:</span><span class="sxs-lookup"><span data-stu-id="ff2d0-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="ff2d0-109">**Datum**: datum voor vereffening van de btw.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="ff2d0-110">**Boekstuk**: het boekstuknummer van de TDS-vereffeningstransactie.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="ff2d0-111">**Belastingtype**: het belastingtype voor het vereffeningsproces.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="ff2d0-112">**Belastingrekeningnummer (TAN)**: het belastingrekeningnummer van de vereffende TDS-transactie.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="ff2d0-113">**Vereffeningsperiode**: de vereffeningsperiode waarvoor het TDS-vereffeningsproces wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="ff2d0-114">**Begindatum**: de begindatum van de vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="ff2d0-115">**Einddatum**: de einddatum van de vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="ff2d0-116">**Versie van bronbelastingbetaling**: de versie van de bronbelastingbetaling: **Oorspronkelijk**, **Laatste correcties** of **Totaallijst**.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="ff2d0-117">Selecteer **Boekstuk** om de boekstukposten voor de TDS-transactie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="ff2d0-118">Selecteer **Bronbelastingtransacties** om de details weer te geven van de TDS-transacties die zijn vereffend voor een specifieke periode tijdens een vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="ff2d0-119">Selecteer **Boekstuk** om de boekstukposten voor de TDS-transactie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="ff2d0-120">Selecteer **Bronbelastingcomponenten** om TDS weer te geven die per TDS-belastingcomponent is berekend voor een specifieke TDS-belastingcode.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="ff2d0-121">Sluit de pagina **Bronbelastingbetalingen** om terug te keren naar de pagina **Vereffeningsperioden voor bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="ff2d0-122">Selecteer **Bronbelastingtransacties** om de details weer te geven van de TDS-transacties die zijn vereffend voor de vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff2d0-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>

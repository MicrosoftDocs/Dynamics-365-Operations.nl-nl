---
title: Vereffeningsperioden voor bronbelasting voor het TDS-belastingtype instellen
description: In dit onderwerp wordt uitgelegd hoe u vereffeningsperioden in moet stellen voor vereffeningsperioden voor TDS (belasting ingehouden op bron).
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023135"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="bb42d-103">Vereffeningsperioden voor bronbelasting voor het TDS-belastingtype instellen</span><span class="sxs-lookup"><span data-stu-id="bb42d-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb42d-104">In dit onderwerp wordt uitgelegd hoe u vereffeningsperioden in moet stellen voor vereffeningsperioden voor TDS (belasting ingehouden op bron).</span><span class="sxs-lookup"><span data-stu-id="bb42d-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="bb42d-105">Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Vereffeningsperioden voor bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="bb42d-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="bb42d-106">[![Pagina Vereffeningsperioden voor bronbelasting](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="bb42d-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="bb42d-107">Selecteer in het veld **Belastingtype** de optie **TDS** om vereffeningsperioden voor bronbelasting in te stellen voor het belastingtype TDS.</span><span class="sxs-lookup"><span data-stu-id="bb42d-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="bb42d-108">Selecteer **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="bb42d-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="bb42d-109">Voer in het veld **Vereffeningsperiode** een naam in voor de TDS-vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="bb42d-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="bb42d-110">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="bb42d-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="bb42d-111">Selecteer in het veld **Bronbelastingdienst** de TDS-dienst waarvoor u de TDS-vereffeningsperiode definieert.</span><span class="sxs-lookup"><span data-stu-id="bb42d-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="bb42d-112">Selecteer op het sneltabblad **Algemeen** in het veld **Periode-interval** het type periode-interval voor de TDS-vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="bb42d-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="bb42d-113">Geef in het veld **Aantal eenheden** het aantal eenheden op voor het periode-intervaltype.</span><span class="sxs-lookup"><span data-stu-id="bb42d-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="bb42d-114">Selecteer op het sneltabblad **Perioden** in het veld **Begindatum** de begindatum voor de TDS-vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="bb42d-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="bb42d-115">Selecteer in het veld **Einddatum** de einddatum.</span><span class="sxs-lookup"><span data-stu-id="bb42d-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="bb42d-116">Als u een volgende TDS-vereffeningsperiode voor een bestaande periode wilt maken op basis van het periode-interval en de periode-eenheden, selecteert u **Nieuwe periode**.</span><span class="sxs-lookup"><span data-stu-id="bb42d-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="bb42d-117">Als u de details wilt weergeven van de periodieke TDS-vereffening die wordt uitgevoerd voor een specifieke vereffeningsperiode, selecteert u **Bronbelastingbetalingen** om de pagina **Bronbelastingbetaling** te openen.</span><span class="sxs-lookup"><span data-stu-id="bb42d-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb42d-118">Als u het periodieke TDS-vereffeningsproces wilt uitvoeren, gaat u naar **Grootboek \> Periodiek \> Bronbelasting \> Bronbelastingbetaling**.</span><span class="sxs-lookup"><span data-stu-id="bb42d-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="bb42d-119">[![Pagina Bronbelastingbetaling](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="bb42d-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="bb42d-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bb42d-120">Close the page.</span></span>

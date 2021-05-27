---
title: Betalingsschema's met TDS-toewijzing instellen
description: In dit onderwerp wordt uitgelegd hoe u betalingsschema's moet instellen met toewijzing van TDS (belasting ingehouden op bron).
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023156"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="4470b-103">Betalingsschema's met TDS-toewijzing instellen</span><span class="sxs-lookup"><span data-stu-id="4470b-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4470b-104">In dit onderwerp wordt uitgelegd hoe u betalingsschema's moet instellen met toewijzing van TDS (belasting ingehouden op bron).</span><span class="sxs-lookup"><span data-stu-id="4470b-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="4470b-105">Ga naar **Leveranciers \> Betalingsinstelling \> Betalingsschema's**.</span><span class="sxs-lookup"><span data-stu-id="4470b-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="4470b-106">[![Pagina Betalingsschema's](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="4470b-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="4470b-107">Selecteer in het actievenster **Nieuw** om een betalingsschema te maken en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="4470b-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="4470b-108">Selecteer in het veld **Toewijzing** de methode die u wilt gebruiken om de betaling toe te wijzen voor het betalingsschema:</span><span class="sxs-lookup"><span data-stu-id="4470b-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="4470b-109">Totaal</span><span class="sxs-lookup"><span data-stu-id="4470b-109">Total</span></span>
    - <span data-ttu-id="4470b-110">Vast bedrag</span><span class="sxs-lookup"><span data-stu-id="4470b-110">Fixed amount</span></span>
    - <span data-ttu-id="4470b-111">Vaste hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4470b-111">Fixed quantity</span></span>
    - <span data-ttu-id="4470b-112">Opgegeven</span><span class="sxs-lookup"><span data-stu-id="4470b-112">Specified</span></span>

    <span data-ttu-id="4470b-113">In het veld **Bronbelastingtoewijzing** wordt de TDS-toewijzingsmethode voor het betalingsschema getoond.</span><span class="sxs-lookup"><span data-stu-id="4470b-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="4470b-114">Als u **Totaal** selecteert in het veld **Toewijzing**, wordt het veld **Bronbelastingtoewijzing** automatisch ingesteld op **Totaal**.</span><span class="sxs-lookup"><span data-stu-id="4470b-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="4470b-115">Als u **Vast bedrag**, **Vaste hoeveelheid** of **Opgegeven** in het veld **Toewijzing** selecteert, wordt het veld **Bronbelastingtoewijzing** automatisch ingesteld op **Evenredig**.</span><span class="sxs-lookup"><span data-stu-id="4470b-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4470b-116">Als het veld **Bronbelastingtoewijzing** is ingesteld op **Totaal**, worden de betalingstermijnen berekend op basis van het brutobedrag, inclusief het TDS-bedrag.</span><span class="sxs-lookup"><span data-stu-id="4470b-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="4470b-117">Als het veld **Bronbelastingtoewijzing** is ingesteld op **Evenredig**, worden de betalingstermijnen berekend op basis van het nettobedrag, nadat het TDS-bedrag is ingehouden.</span><span class="sxs-lookup"><span data-stu-id="4470b-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="4470b-118">Geef de andere vereiste gegevens op in het formulier en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4470b-118">Enter the other required details, and then close the page.</span></span>

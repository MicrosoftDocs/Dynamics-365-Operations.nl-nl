---
title: Boekstuk is niet gegenereerd
description: Dit onderwerp bevat informatie voor het oplossen van problemen wanneer een boekstuk gegenereerd had moeten worden maar dat niet is gebeurd.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947622"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="542ba-103">Boekstuk is niet gegenereerd</span><span class="sxs-lookup"><span data-stu-id="542ba-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="542ba-104">Als er een boekstuk moet worden gegenereerd maar op de pagina **Boekstuktransacties** wordt geen boekstuk weergegeven, volgt u de stappen in de volgende secties die nodig zijn om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="542ba-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="542ba-105">[![Pagina met boekstuktransacties zonder boekstuk](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="542ba-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="542ba-106">Controleer de toepasbaarheid van de belasting</span><span class="sxs-lookup"><span data-stu-id="542ba-106">Check the tax applicability</span></span>

1. <span data-ttu-id="542ba-107">Ga naar **Belasting** \> **Periodieke taken** \> **Nog niet overgeboekte journaalposten in subadministratie**.</span><span class="sxs-lookup"><span data-stu-id="542ba-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="542ba-108">Als er een journaalrecord is, selecteert u deze en vervolgens selecteert u **Nu overboeken**.</span><span class="sxs-lookup"><span data-stu-id="542ba-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="542ba-109">[![Knop Nu overboeken op de pagina Nog niet overgeboekte journaalposten in subadministratie](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="542ba-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="542ba-110">Open de pagina **Boekstuktransacties** opnieuw om te bekijken of het boekstuk werd gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="542ba-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="542ba-111">Bekijk of er een aanpassing bestaat</span><span class="sxs-lookup"><span data-stu-id="542ba-111">Determine whether customization exists</span></span>

<span data-ttu-id="542ba-112">Als u de stappen in de vorige sectie hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat.</span><span class="sxs-lookup"><span data-stu-id="542ba-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="542ba-113">Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="542ba-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

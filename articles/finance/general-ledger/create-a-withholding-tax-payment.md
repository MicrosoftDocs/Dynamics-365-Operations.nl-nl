---
title: Een betaling voor bronbelasting maken
description: De procedure voor de taak Betaling bronbelasting vereffent bronbelastingsaldi van Leveranciers op bronbelastingrekeningen en boekt ze op de bronbelastingvereffeningsrekening voor een bepaalde periode. Dit onderwerp geeft een overzicht van de stappen voor het instellen van bronbelastingbetaling.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060722"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="79aa8-104">Een betaling voor bronbelasting maken</span><span class="sxs-lookup"><span data-stu-id="79aa8-104">Create a withholding tax payment</span></span>

<span data-ttu-id="79aa8-105">De procedure voor de taak Betaling bronbelasting vereffent bronbelastingsaldi van Leveranciers op bronbelastingrekeningen en boekt ze op de bronbelastingvereffeningsrekening voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="79aa8-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="79aa8-106">Dit onderwerp geeft een overzicht van de stappen voor het instellen van bronbelastingbetaling.</span><span class="sxs-lookup"><span data-stu-id="79aa8-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="79aa8-107">Bij de berekening van bronbelastingbetaling wordt geen rekening gehouden met de tegenrekening voor bronbelasting (van klanten).</span><span class="sxs-lookup"><span data-stu-id="79aa8-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="79aa8-108">Ga naar **Navigatiedeelvenster > Modules > Belasting > Aangiften> Bronbelasting > Bronbelastingbetaling**.</span><span class="sxs-lookup"><span data-stu-id="79aa8-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="79aa8-109">Klik in het veld **Vereffeningsperiode** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="79aa8-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="79aa8-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="79aa8-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="79aa8-111">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="79aa8-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="79aa8-112">Voer in het veld **Transactiedatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="79aa8-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="79aa8-113">Selecteer **Bijwerken** om een boekstuk voor bronbelastingbetaling te boeken op de vereffeningsrekening voor bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="79aa8-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="79aa8-114">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="79aa8-114">Click **OK**.</span></span>

![Parameters voor bronbelastingbetaling](media/withholding-tax-payment.png)

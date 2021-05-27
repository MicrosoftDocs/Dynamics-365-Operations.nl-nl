---
title: De TDS-parameters instellen
description: In dit onderwerp wordt beschreven hoe u parameters in kunt stellen om de functionaliteit TDS (belasting ingehouden op bron) in opgegeven transacties te activeren. Dit is een noodzakelijke stap om de functie voor belasting ingehouden op bron (TDS) te gebruiken.
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023146"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="49c72-104">De TDS-parameters instellen</span><span class="sxs-lookup"><span data-stu-id="49c72-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49c72-105">In dit onderwerp wordt beschreven hoe u parameters in kunt stellen om de functionaliteit TDS (belasting ingehouden op bron) in opgegeven transacties te activeren.</span><span class="sxs-lookup"><span data-stu-id="49c72-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="49c72-106">Dit is een noodzakelijke stap om de functie voor belasting ingehouden op bron (TDS) te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="49c72-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="49c72-107">Ga naar **Grootboek \> Grootboek instellen \> Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="49c72-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="49c72-108">Stel op het tabblad **Directe belastingen** in de sectie **belasting ingehouden op bron** de optie **TDS activeren** in op **Ja** om de TDS-functionaliteit te activeren en de pagina's en velden die hiervoor worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="49c72-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="49c72-109">Stel de optie **Factuuroptie** in op **Ja** om de velden te activeren die worden gebruikt om TDS op factuurniveau te berekenen en in te houden.</span><span class="sxs-lookup"><span data-stu-id="49c72-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="49c72-110">Stel de optie **Betaling** in op **Ja** om de velden te activeren die worden gebruikt om TDS op betalingsniveau te berekenen en in te houden.</span><span class="sxs-lookup"><span data-stu-id="49c72-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="49c72-111">[![Tabblad Directe belastingen](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="49c72-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="49c72-112">Zoek op het tabblad **Nummerreeksen** de rij waarin het veld **Verwijzing** is ingesteld op **Bronbelastingbetaling**.</span><span class="sxs-lookup"><span data-stu-id="49c72-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="49c72-113">Selecteer in het veld **Nummerreekscode** voor de rij de nummerreekscode.</span><span class="sxs-lookup"><span data-stu-id="49c72-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="49c72-114">De nummerreekscode wordt gebruikt om boekstuknummers te genereren voor het periodieke TDS-vereffeningsproces.</span><span class="sxs-lookup"><span data-stu-id="49c72-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="49c72-115">Als u het periodieke TDS-vereffeningsproces wilt uitvoeren, gaat u naar **Belasting \> Aangiften \> Bronbelasting \> Bronbelastingbetaling**.</span><span class="sxs-lookup"><span data-stu-id="49c72-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="49c72-116">[![Tabblad Nummerreeksen](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="49c72-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="49c72-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="49c72-117">Close the page.</span></span>

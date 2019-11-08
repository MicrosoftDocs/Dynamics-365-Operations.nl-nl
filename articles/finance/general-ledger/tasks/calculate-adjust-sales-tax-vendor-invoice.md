---
title: Btw op een leveranciersfactuur berekenen en corrigeren
description: In dit onderwerp wordt uitgelegd hoe u de btw op een leveranciersfactuur in Dynamics 365 Finance aanpast.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68e0df78516875168d977f78adf023887b2362d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186274"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="a432a-103">Btw op een leveranciersfactuur berekenen en corrigeren</span><span class="sxs-lookup"><span data-stu-id="a432a-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a432a-104">In dit onderwerp wordt uitgelegd hoe u de btw op een leveranciersfactuur aanpast.</span><span class="sxs-lookup"><span data-stu-id="a432a-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="a432a-105">Als het oorspronkelijke brondocument verschillende btw-bedragen bevat, zoals berekend, kunt u die bedragen aanpassen voor het boeken.</span><span class="sxs-lookup"><span data-stu-id="a432a-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="a432a-106">Bij deze taak wordt het demobedrijf DEMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a432a-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="a432a-107">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Factuurjournaal**.</span><span class="sxs-lookup"><span data-stu-id="a432a-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="a432a-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a432a-108">Select **New**.</span></span>
3. <span data-ttu-id="a432a-109">Selecteer in het veld **Naam** van de nieuwe rij een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="a432a-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="a432a-110">Selecteer **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a432a-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="a432a-111">Geef in het veld **Rekening** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="a432a-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="a432a-112">Typ een waarde in het veld **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="a432a-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="a432a-113">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="a432a-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="a432a-114">Geef in het veld **Tegenrekening** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="a432a-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="a432a-115">Selecteer **Btw**.</span><span class="sxs-lookup"><span data-stu-id="a432a-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="a432a-116">Voer in het veld **Totaal werkelijk btw-bedrag** een getal in.</span><span class="sxs-lookup"><span data-stu-id="a432a-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="a432a-117">Op het tabblad **Correctie** kunnen de btw-bedragen per btw-code worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="a432a-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="a432a-118">Selecteer **Werkelijke bedragen opnieuw instellen op basis van berekende**.</span><span class="sxs-lookup"><span data-stu-id="a432a-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="a432a-119">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a432a-119">Select **OK**.</span></span>
14. <span data-ttu-id="a432a-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="a432a-120">Select **Save**.</span></span>

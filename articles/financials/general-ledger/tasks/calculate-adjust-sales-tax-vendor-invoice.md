---
title: Btw op een leveranciersfactuur berekenen en corrigeren
description: In dit onderwerp wordt uitgelegd hoe u de btw op een leveranciersfactuur in Dynamics 365 for Finance and Operations aanpast.
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
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862609"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="182a3-103">Btw op een leveranciersfactuur berekenen en corrigeren</span><span class="sxs-lookup"><span data-stu-id="182a3-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="182a3-104">In dit onderwerp wordt uitgelegd hoe u de btw op een leveranciersfactuur in Dynamics 365 for Finance and Operations aanpast.</span><span class="sxs-lookup"><span data-stu-id="182a3-104">This topic explains how to adjust sales tax on a vendor invoice in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="182a3-105">Als het oorspronkelijke brondocument verschillende btw-bedragen bevat, zoals berekend, kunt u die bedragen aanpassen voor het boeken.</span><span class="sxs-lookup"><span data-stu-id="182a3-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="182a3-106">Bij deze taak wordt het demobedrijf DEMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="182a3-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="182a3-107">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Factuurjournaal**.</span><span class="sxs-lookup"><span data-stu-id="182a3-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="182a3-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="182a3-108">Select **New**.</span></span>
3. <span data-ttu-id="182a3-109">Selecteer in het veld **Naam** van de nieuwe rij een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="182a3-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="182a3-110">Selecteer **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="182a3-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="182a3-111">Geef in het veld **Rekening** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="182a3-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="182a3-112">Typ een waarde in het veld **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="182a3-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="182a3-113">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="182a3-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="182a3-114">Geef in het veld **Tegenrekening** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="182a3-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="182a3-115">Selecteer **Btw**.</span><span class="sxs-lookup"><span data-stu-id="182a3-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="182a3-116">Voer in het veld **Totaal werkelijk btw-bedrag** een getal in.</span><span class="sxs-lookup"><span data-stu-id="182a3-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="182a3-117">Op het tabblad **Correctie** kunnen de btw-bedragen per btw-code worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="182a3-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="182a3-118">Selecteer **Werkelijke bedragen opnieuw instellen op basis van berekende**.</span><span class="sxs-lookup"><span data-stu-id="182a3-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="182a3-119">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="182a3-119">Select **OK**.</span></span>
14. <span data-ttu-id="182a3-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="182a3-120">Select **Save**.</span></span>


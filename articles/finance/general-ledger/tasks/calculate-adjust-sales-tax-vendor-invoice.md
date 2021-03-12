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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994710"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="db80f-103">Btw op een leveranciersfactuur berekenen en corrigeren</span><span class="sxs-lookup"><span data-stu-id="db80f-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db80f-104">In dit onderwerp wordt uitgelegd hoe u de btw op een leveranciersfactuur aanpast.</span><span class="sxs-lookup"><span data-stu-id="db80f-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="db80f-105">Als het oorspronkelijke brondocument verschillende btw-bedragen bevat, zoals berekend, kunt u die bedragen aanpassen voor het boeken.</span><span class="sxs-lookup"><span data-stu-id="db80f-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="db80f-106">Bij deze taak wordt het demobedrijf DEMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="db80f-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="db80f-107">Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Factuurjournaal**.</span><span class="sxs-lookup"><span data-stu-id="db80f-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="db80f-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="db80f-108">Select **New**.</span></span>
3. <span data-ttu-id="db80f-109">Selecteer in het veld **Naam** van de nieuwe rij een optie in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="db80f-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="db80f-110">Selecteer **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="db80f-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="db80f-111">Geef in het veld **Rekening** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="db80f-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="db80f-112">Typ een waarde in het veld **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="db80f-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="db80f-113">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="db80f-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="db80f-114">Geef in het veld **Tegenrekening** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="db80f-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="db80f-115">Selecteer **Btw**.</span><span class="sxs-lookup"><span data-stu-id="db80f-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="db80f-116">Voer in het veld **Totaal werkelijk btw-bedrag** een getal in.</span><span class="sxs-lookup"><span data-stu-id="db80f-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="db80f-117">Op het tabblad **Correctie** kunnen de btw-bedragen per btw-code worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="db80f-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="db80f-118">Selecteer **Werkelijke bedragen opnieuw instellen op basis van berekende**.</span><span class="sxs-lookup"><span data-stu-id="db80f-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="db80f-119">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="db80f-119">Select **OK**.</span></span>
14. <span data-ttu-id="db80f-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="db80f-120">Select **Save**.</span></span>


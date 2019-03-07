---
title: Btw op een leveranciersfactuur berekenen en corrigeren
description: Als het oorspronkelijke brondocument verschillende btw-bedragen bevat, zoals berekend, kunt u die bedragen aanpassen voor het boeken.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "308915"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="e1d7d-103">Btw op een leveranciersfactuur berekenen en corrigeren</span><span class="sxs-lookup"><span data-stu-id="e1d7d-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1d7d-104">Als het oorspronkelijke brondocument verschillende btw-bedragen bevat, zoals berekend, kunt u die bedragen aanpassen voor het boeken.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="e1d7d-105">Bij deze taak wordt het demobedrijf DEMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="e1d7d-106">Ga naar Leveranciers > Facturen > Factuurjournaal.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="e1d7d-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-107">Click New.</span></span>
3. <span data-ttu-id="e1d7d-108">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e1d7d-109">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e1d7d-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e1d7d-111">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-111">Click Lines.</span></span>
7. <span data-ttu-id="e1d7d-112">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="e1d7d-113">Geef in het veld Rekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="e1d7d-114">Typ een waarde in het veld Factuur.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="e1d7d-115">Voer een nummer in het veld Credit in.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="e1d7d-116">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="e1d7d-117">Klik op Btw.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-117">Click Sales tax.</span></span>
13. <span data-ttu-id="e1d7d-118">Voer in het veld Totaal werkelijk btw-bedrag een getal in.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="e1d7d-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-119">Click OK.</span></span>
15. <span data-ttu-id="e1d7d-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-120">Click Save.</span></span>
16. <span data-ttu-id="e1d7d-121">Klik op Btw.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-121">Click Sales tax.</span></span>
17. <span data-ttu-id="e1d7d-122">Op het tabblad Correctie kunnen de btw-bedragen per btw-code worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="e1d7d-123">Klik op Werkelijke bedragen opnieuw instellen op basis van berekende.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="e1d7d-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-124">Click OK.</span></span>
20. <span data-ttu-id="e1d7d-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-125">Click Save.</span></span>


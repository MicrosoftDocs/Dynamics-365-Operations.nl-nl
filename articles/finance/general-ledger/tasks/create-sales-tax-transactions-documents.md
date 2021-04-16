---
title: Btw-transacties maken in documenten
description: De btw op documenten wordt berekend door een btw-groep en een btw-groep voor het artikel op documentregels te leveren.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 061949dedde763c188e13c07cec750895cbef175
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836980"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="c4dd1-103">Btw-transacties maken in documenten</span><span class="sxs-lookup"><span data-stu-id="c4dd1-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4dd1-104">De btw op documenten wordt berekend door een btw-groep en een btw-groep voor het artikel op documentregels te leveren.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="c4dd1-105">Deze zijn afkomstig van hoofdgegevens maar kunnen handmatig worden gewijzigd indien nodig.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="c4dd1-106">De berekende btw kan op regel- en documentniveau worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="c4dd1-107">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c4dd1-108">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c4dd1-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-109">Click New.</span></span>
3. <span data-ttu-id="c4dd1-110">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c4dd1-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c4dd1-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c4dd1-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-113">Click OK.</span></span>
7. <span data-ttu-id="c4dd1-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c4dd1-115">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c4dd1-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c4dd1-117">Voer een nummer in het veld Eenheidsprijs in.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="c4dd1-118">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="c4dd1-119">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="c4dd1-120">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="c4dd1-121">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="c4dd1-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="c4dd1-123">Klik op Financiële items.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-123">Click Financials.</span></span>
17. <span data-ttu-id="c4dd1-124">Klik op Btw.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-124">Click Sales tax.</span></span>
18. <span data-ttu-id="c4dd1-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-125">Click OK.</span></span>
19. <span data-ttu-id="c4dd1-126">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-126">Click Add line.</span></span>
20. <span data-ttu-id="c4dd1-127">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="c4dd1-128">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="c4dd1-129">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="c4dd1-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="c4dd1-131">Voer een nummer in het veld Eenheidsprijs in.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="c4dd1-132">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="c4dd1-133">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="c4dd1-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="c4dd1-135">Klik in het actievenster op Verkopen.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="c4dd1-136">Klik op Btw.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-136">Click Sales tax.</span></span>
30. <span data-ttu-id="c4dd1-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
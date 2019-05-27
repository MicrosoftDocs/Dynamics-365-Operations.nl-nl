---
title: Btw-transacties maken in documenten
description: De btw op documenten wordt berekend door een btw-groep en een btw-groep voor het artikel op documentregels te leveren.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02e3ea556da9abefd37ce585086241d1e45aa0fa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571207"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="c0324-103">Btw-transacties maken in documenten</span><span class="sxs-lookup"><span data-stu-id="c0324-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0324-104">De btw op documenten wordt berekend door een btw-groep en een btw-groep voor het artikel op documentregels te leveren.</span><span class="sxs-lookup"><span data-stu-id="c0324-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="c0324-105">Deze zijn afkomstig van hoofdgegevens maar kunnen handmatig worden gewijzigd indien nodig.</span><span class="sxs-lookup"><span data-stu-id="c0324-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="c0324-106">De berekende btw kan op regel- en documentniveau worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="c0324-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="c0324-107">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c0324-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c0324-108">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="c0324-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c0324-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c0324-109">Click New.</span></span>
3. <span data-ttu-id="c0324-110">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c0324-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c0324-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c0324-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c0324-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c0324-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c0324-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0324-113">Click OK.</span></span>
7. <span data-ttu-id="c0324-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c0324-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c0324-115">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c0324-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c0324-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c0324-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c0324-117">Voer een nummer in het veld Eenheidsprijs in.</span><span class="sxs-lookup"><span data-stu-id="c0324-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="c0324-118">Vouw de sectie Regeldetails uit of samen.</span><span class="sxs-lookup"><span data-stu-id="c0324-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="c0324-119">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="c0324-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="c0324-120">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c0324-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="c0324-121">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c0324-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="c0324-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c0324-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="c0324-123">Klik op Financiële items.</span><span class="sxs-lookup"><span data-stu-id="c0324-123">Click Financials.</span></span>
17. <span data-ttu-id="c0324-124">Klik op Btw.</span><span class="sxs-lookup"><span data-stu-id="c0324-124">Click Sales tax.</span></span>
18. <span data-ttu-id="c0324-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0324-125">Click OK.</span></span>
19. <span data-ttu-id="c0324-126">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0324-126">Click Add line.</span></span>
20. <span data-ttu-id="c0324-127">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c0324-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="c0324-128">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c0324-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="c0324-129">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c0324-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="c0324-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c0324-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="c0324-131">Voer een nummer in het veld Eenheidsprijs in.</span><span class="sxs-lookup"><span data-stu-id="c0324-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="c0324-132">Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c0324-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="c0324-133">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c0324-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="c0324-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="c0324-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="c0324-135">Klik in het actievenster op Verkopen.</span><span class="sxs-lookup"><span data-stu-id="c0324-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="c0324-136">Klik op Btw.</span><span class="sxs-lookup"><span data-stu-id="c0324-136">Click Sales tax.</span></span>
30. <span data-ttu-id="c0324-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c0324-137">Click OK.</span></span>


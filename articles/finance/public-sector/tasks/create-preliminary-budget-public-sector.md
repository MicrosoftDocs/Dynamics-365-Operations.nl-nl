---
title: Een voorlopig budget maken voor de openbare sector
description: U kunt voorlopige budgetregisterregels maken voor een specifiek budgetmodel en dimensiewaarden.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22538d58cc3499bd030848699d6c5831dfd8888a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975155"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="19a86-103">Een voorlopig budget maken voor de openbare sector</span><span class="sxs-lookup"><span data-stu-id="19a86-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19a86-104">U kunt voorlopige budgetregisterregels maken voor een specifiek budgetmodel en dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="19a86-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="19a86-105">Nadat het werkelijke budget is goedgekeurd, kunt u oorspronkelijke budgetjournaalregels maken.</span><span class="sxs-lookup"><span data-stu-id="19a86-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="19a86-106">Deze procedure werd gemaakt met de demogegevens van het bedrijf PSUS in de partitie van openbare sector.</span><span class="sxs-lookup"><span data-stu-id="19a86-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="19a86-107">Ga naar Budgettering > Budgetregisterregels.</span><span class="sxs-lookup"><span data-stu-id="19a86-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="19a86-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="19a86-108">Click New.</span></span>
3. <span data-ttu-id="19a86-109">Klik in het veld Budgetmodel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="19a86-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="19a86-110">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="19a86-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="19a86-111">Klik in het veld Budgetcode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="19a86-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="19a86-112">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="19a86-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="19a86-113">Klik in het veld Redencode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="19a86-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="19a86-114">Klik in de lijst op het gewenste record.</span><span class="sxs-lookup"><span data-stu-id="19a86-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="19a86-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="19a86-115">Click Save.</span></span>
10. <span data-ttu-id="19a86-116">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="19a86-116">Click Add line.</span></span>
    * <span data-ttu-id="19a86-117">Optioneel: als u een andere datum wilt dan de datum in de koptekst, voert een nieuwe datum in.</span><span class="sxs-lookup"><span data-stu-id="19a86-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="19a86-118">Deze datum bepaalt de boekperiode waarvoor het budget wordt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="19a86-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="19a86-119">Wanneer u de taakbegeleiding bekijkt en andere velden wilt invullen, klikt u boven aan de pagina op Ontgrendelen.</span><span class="sxs-lookup"><span data-stu-id="19a86-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="19a86-120">Klik in het veld Rekeningstructuur op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="19a86-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="19a86-121">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="19a86-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="19a86-122">Geef in het veld Dimensiewaarden de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="19a86-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="19a86-123">Typ een getal in het veld Bedrag.</span><span class="sxs-lookup"><span data-stu-id="19a86-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="19a86-124">U kunt ook een bedragtype invoeren.</span><span class="sxs-lookup"><span data-stu-id="19a86-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="19a86-125">Klik in het veld Valuta op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="19a86-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="19a86-126">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="19a86-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="19a86-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="19a86-127">Click Save.</span></span>
18. <span data-ttu-id="19a86-128">Klik op Budgetsaldi bijwerken.</span><span class="sxs-lookup"><span data-stu-id="19a86-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="19a86-129">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="19a86-129">Click Update.</span></span>
    * <span data-ttu-id="19a86-130">Om de resultaten van de update te zien, klikt u op de blauwe balk op Berichtdetails.</span><span class="sxs-lookup"><span data-stu-id="19a86-130">To see the results of the update, click Message details on the blue bar.</span></span>  


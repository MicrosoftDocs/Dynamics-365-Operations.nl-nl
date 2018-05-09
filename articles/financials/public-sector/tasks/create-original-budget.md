--- 
title: Een oorspronkelijk budget maken en de voorlopige budgetposten in de openbare sector terugboeken
description: Wanneer u een oorspronkelijke budgetregel maakt en het budgetmodel en de dimensiewaarden gebruikt die voorlopige budgetbedragen bevatten, kunnen voorlopige budgetbedragen worden omgekeerd.
author: twheeloc
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dc315a53e420049689828cce375630a1adf5d843
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="create-an-original-budget-and-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="24f88-103">Een oorspronkelijk budget maken en de voorlopige budgetposten in de openbare sector terugboeken</span><span class="sxs-lookup"><span data-stu-id="24f88-103">Create an original budget and reverse preliminary budget entries in the public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24f88-104">Wanneer u een oorspronkelijke budgetregel maakt en het budgetmodel en de dimensiewaarden gebruikt die voorlopige budgetbedragen bevatten, kunnen voorlopige budgetbedragen worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="24f88-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="24f88-105">Deze procedure werd gemaakt met de demogegevens van het bedrijf PSUS in de partitie van openbare sector.</span><span class="sxs-lookup"><span data-stu-id="24f88-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="24f88-106">Ga naar Budgettering > Budgetregisterregels.</span><span class="sxs-lookup"><span data-stu-id="24f88-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="24f88-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="24f88-107">Click New.</span></span>
3. <span data-ttu-id="24f88-108">Klik in het veld Budgetmodel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="24f88-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="24f88-109">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="24f88-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="24f88-110">Klik in het veld Budgetcode op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="24f88-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="24f88-111">Klik in de lijst op Oorspronkelijke budget.</span><span class="sxs-lookup"><span data-stu-id="24f88-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="24f88-112">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="24f88-112">Click Save.</span></span>
8. <span data-ttu-id="24f88-113">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="24f88-113">Click Add line.</span></span>
9. <span data-ttu-id="24f88-114">Optioneel: als u een andere datum wilt dan de datum in de koptekst, voert een nieuwe datum in.</span><span class="sxs-lookup"><span data-stu-id="24f88-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="24f88-115">Deze datum bepaalt de boekperiode waarvoor het budget wordt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="24f88-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="24f88-116">Klik in het veld Rekeningstructuur op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="24f88-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="24f88-117">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="24f88-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="24f88-118">Geef in het veld Dimensiewaarden de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="24f88-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="24f88-119">Typ een getal in het veld Bedrag.</span><span class="sxs-lookup"><span data-stu-id="24f88-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="24f88-120">Klik in het veld Valuta op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="24f88-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="24f88-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="24f88-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="24f88-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="24f88-122">Click Save.</span></span>
17. <span data-ttu-id="24f88-123">Klik op Budgetsaldi bijwerken.</span><span class="sxs-lookup"><span data-stu-id="24f88-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="24f88-124">Optioneel: u kunt de optie Voorlopig budget omkeren selecteren.</span><span class="sxs-lookup"><span data-stu-id="24f88-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="24f88-125">U kunt alle voorlopige budgetregels omkeren of alleen de voorlopige budgetregels met de budgetcode die u opgeeft.</span><span class="sxs-lookup"><span data-stu-id="24f88-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="24f88-126">Om optionele selecties te maken, klikt u boven aan de pagina op het pictogram Ontgrendelen.</span><span class="sxs-lookup"><span data-stu-id="24f88-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="24f88-127">Klik op Bijwerken.</span><span class="sxs-lookup"><span data-stu-id="24f88-127">Click Update.</span></span>



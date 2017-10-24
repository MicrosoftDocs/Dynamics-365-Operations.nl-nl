--- 
title: Bronbelasting instellen
description: Bronbelasting is belasting op leveranciers waarbij geen btw-transacties worden gemaakt.
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc4c0745235052cb4145bc7083fef1a88c8bb5c9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="839ae-103">Bronbelasting instellen</span><span class="sxs-lookup"><span data-stu-id="839ae-103">Set up withholding tax</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="839ae-104">Bronbelasting is belasting op leveranciers waarbij geen btw-transacties worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="839ae-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="839ae-105">Bronbelasting die is berekend over betalingen van leveranciers is een schuld.</span><span class="sxs-lookup"><span data-stu-id="839ae-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="839ae-106">Daarom zijn alleen balansrekeningen of schuldenrekeningen geldige rekeningen voor het boeken van bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="839ae-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="839ae-107">Deze taakbegeleiding toont hoe u bronbelasting instelt.</span><span class="sxs-lookup"><span data-stu-id="839ae-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="839ae-108">Ga naar Belasting > Indirecte belastingen > Bronbelasting > Bronbelastingcodes.</span><span class="sxs-lookup"><span data-stu-id="839ae-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="839ae-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="839ae-109">Click New.</span></span>
3. <span data-ttu-id="839ae-110">Typ een waarde in het veld Bronbelastingcode.</span><span class="sxs-lookup"><span data-stu-id="839ae-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="839ae-111">Voer in het veld Bronbelastingnaam de naam van de bronbelastingcode in.</span><span class="sxs-lookup"><span data-stu-id="839ae-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="839ae-112">Selecteer in het veld Hoofdrekening de hoofdrekening voor het boeken van de bronbelastingschuld.</span><span class="sxs-lookup"><span data-stu-id="839ae-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="839ae-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="839ae-113">Click Save.</span></span>
7. <span data-ttu-id="839ae-114">Klik op Waarden.</span><span class="sxs-lookup"><span data-stu-id="839ae-114">Click Values.</span></span>
8. <span data-ttu-id="839ae-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="839ae-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="839ae-116">Voer in het veld Waarde een percentage in dat voor de berekening van de bronbelasting wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="839ae-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="839ae-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="839ae-117">Click Save.</span></span>
11. <span data-ttu-id="839ae-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="839ae-118">Close the page.</span></span>
12. <span data-ttu-id="839ae-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="839ae-119">Click Save.</span></span>
13. <span data-ttu-id="839ae-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="839ae-120">Close the page.</span></span>
14. <span data-ttu-id="839ae-121">Ga naar Belasting > Indirecte belastingen > Bronbelasting > Bronbelastinggroepen.</span><span class="sxs-lookup"><span data-stu-id="839ae-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="839ae-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="839ae-122">Click New.</span></span>
16. <span data-ttu-id="839ae-123">Voer in het veld Bronbelastinggroep de id van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="839ae-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="839ae-124">Voer in het veld Beschrijving de naam van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="839ae-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="839ae-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="839ae-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="839ae-126">Selecteer de bronbelastingcode in het veld Bronbelastingcode.</span><span class="sxs-lookup"><span data-stu-id="839ae-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="839ae-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="839ae-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="839ae-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="839ae-128">Click Save.</span></span>



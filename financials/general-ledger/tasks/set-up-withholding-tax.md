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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc4c0745235052cb4145bc7083fef1a88c8bb5c9
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="56092-103">Bronbelasting instellen</span><span class="sxs-lookup"><span data-stu-id="56092-103">Set up withholding tax</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56092-104">Bronbelasting is belasting op leveranciers waarbij geen btw-transacties worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="56092-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="56092-105">Bronbelasting die is berekend over betalingen van leveranciers is een schuld.</span><span class="sxs-lookup"><span data-stu-id="56092-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="56092-106">Daarom zijn alleen balansrekeningen of schuldenrekeningen geldige rekeningen voor het boeken van bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="56092-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="56092-107">Deze taakbegeleiding toont hoe u bronbelasting instelt.</span><span class="sxs-lookup"><span data-stu-id="56092-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="56092-108">Ga naar Belasting > Indirecte belastingen > Bronbelasting > Bronbelastingcodes.</span><span class="sxs-lookup"><span data-stu-id="56092-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="56092-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="56092-109">Click New.</span></span>
3. <span data-ttu-id="56092-110">Typ een waarde in het veld Bronbelastingcode.</span><span class="sxs-lookup"><span data-stu-id="56092-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="56092-111">Voer in het veld Bronbelastingnaam de naam van de bronbelastingcode in.</span><span class="sxs-lookup"><span data-stu-id="56092-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="56092-112">Selecteer in het veld Hoofdrekening de hoofdrekening voor het boeken van de bronbelastingschuld.</span><span class="sxs-lookup"><span data-stu-id="56092-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="56092-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="56092-113">Click Save.</span></span>
7. <span data-ttu-id="56092-114">Klik op Waarden.</span><span class="sxs-lookup"><span data-stu-id="56092-114">Click Values.</span></span>
8. <span data-ttu-id="56092-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="56092-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="56092-116">Voer in het veld Waarde een percentage in dat voor de berekening van de bronbelasting wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="56092-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="56092-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="56092-117">Click Save.</span></span>
11. <span data-ttu-id="56092-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="56092-118">Close the page.</span></span>
12. <span data-ttu-id="56092-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="56092-119">Click Save.</span></span>
13. <span data-ttu-id="56092-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="56092-120">Close the page.</span></span>
14. <span data-ttu-id="56092-121">Ga naar Belasting > Indirecte belastingen > Bronbelasting > Bronbelastinggroepen.</span><span class="sxs-lookup"><span data-stu-id="56092-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="56092-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="56092-122">Click New.</span></span>
16. <span data-ttu-id="56092-123">Voer in het veld Bronbelastinggroep de id van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="56092-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="56092-124">Voer in het veld Beschrijving de naam van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="56092-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="56092-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="56092-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="56092-126">Selecteer de bronbelastingcode in het veld Bronbelastingcode.</span><span class="sxs-lookup"><span data-stu-id="56092-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="56092-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="56092-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="56092-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="56092-128">Click Save.</span></span>



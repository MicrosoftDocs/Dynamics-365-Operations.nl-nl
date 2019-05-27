---
title: Bronbelasting instellen
description: Bronbelasting is belasting op leveranciers waarbij geen btw-transacties worden gemaakt.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562783"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="84b50-103">Bronbelasting instellen</span><span class="sxs-lookup"><span data-stu-id="84b50-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84b50-104">Bronbelasting is belasting op leveranciers waarbij geen btw-transacties worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="84b50-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="84b50-105">Bronbelasting die is berekend over betalingen van leveranciers is een schuld.</span><span class="sxs-lookup"><span data-stu-id="84b50-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="84b50-106">Daarom zijn alleen balansrekeningen of schuldenrekeningen geldige rekeningen voor het boeken van bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="84b50-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="84b50-107">Deze taakbegeleiding toont hoe u bronbelasting instelt.</span><span class="sxs-lookup"><span data-stu-id="84b50-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="84b50-108">Ga naar Belasting > Indirecte belastingen > Bronbelasting > Bronbelastingcodes.</span><span class="sxs-lookup"><span data-stu-id="84b50-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="84b50-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="84b50-109">Click New.</span></span>
3. <span data-ttu-id="84b50-110">Typ een waarde in het veld Bronbelastingcode.</span><span class="sxs-lookup"><span data-stu-id="84b50-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="84b50-111">Voer in het veld Bronbelastingnaam de naam van de bronbelastingcode in.</span><span class="sxs-lookup"><span data-stu-id="84b50-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="84b50-112">Selecteer in het veld Hoofdrekening de hoofdrekening voor het boeken van de bronbelastingschuld.</span><span class="sxs-lookup"><span data-stu-id="84b50-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="84b50-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="84b50-113">Click Save.</span></span>
7. <span data-ttu-id="84b50-114">Klik op Waarden.</span><span class="sxs-lookup"><span data-stu-id="84b50-114">Click Values.</span></span>
8. <span data-ttu-id="84b50-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="84b50-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="84b50-116">Voer in het veld Waarde een percentage in dat voor de berekening van de bronbelasting wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="84b50-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="84b50-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="84b50-117">Click Save.</span></span>
11. <span data-ttu-id="84b50-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="84b50-118">Close the page.</span></span>
12. <span data-ttu-id="84b50-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="84b50-119">Click Save.</span></span>
13. <span data-ttu-id="84b50-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="84b50-120">Close the page.</span></span>
14. <span data-ttu-id="84b50-121">Ga naar Belasting > Indirecte belastingen > Bronbelasting > Bronbelastinggroepen.</span><span class="sxs-lookup"><span data-stu-id="84b50-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="84b50-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="84b50-122">Click New.</span></span>
16. <span data-ttu-id="84b50-123">Voer in het veld Bronbelastinggroep de id van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="84b50-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="84b50-124">Voer in het veld Beschrijving de naam van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="84b50-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="84b50-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="84b50-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="84b50-126">Selecteer de bronbelastingcode in het veld Bronbelastingcode.</span><span class="sxs-lookup"><span data-stu-id="84b50-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="84b50-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="84b50-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="84b50-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="84b50-128">Click Save.</span></span>


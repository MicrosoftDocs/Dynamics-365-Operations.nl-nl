---
title: Bronbelasting instellen
description: In dit onderwerp wordt uitgelegd hoe bronbelasting instelt.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185952"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="e3cb7-103">Bronbelasting instellen</span><span class="sxs-lookup"><span data-stu-id="e3cb7-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3cb7-104">In dit onderwerp wordt uitgelegd hoe bronbelasting instelt.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="e3cb7-105">*Bronbelasting* is belasting op leveranciers waarbij geen btw-transacties worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="e3cb7-106">Bronbelasting die is berekend over betalingen van leveranciers is een schuld.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="e3cb7-107">Daarom zijn alleen balansrekeningen of schuldenrekeningen geldige rekeningen voor het boeken van bronbelasting.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="e3cb7-108">Deze taakbegeleiding toont hoe u bronbelasting instelt.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="e3cb7-109">Ga naar **Navigatievenster > Modules > Belasting > Indirecte belastingen> Bronbelasting > Bronbelastingscodes**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="e3cb7-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-110">Select **New**.</span></span>
3. <span data-ttu-id="e3cb7-111">Typ een waarde in het veld **Bronbelastingcode**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="e3cb7-112">Voer in het veld **Bronbelastingnaam** de naam van de bronbelastingcode in.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="e3cb7-113">Selecteer in het veld **Hoofdrekening** de hoofdrekening voor het boeken van de bronbelastingschuld.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="e3cb7-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-114">Select **Save**.</span></span>
7. <span data-ttu-id="e3cb7-115">Selecteer **Waarden** en markeer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="e3cb7-116">Voer in het veld **Waarde** een percentage in dat voor de berekening van de bronbelasting wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="e3cb7-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-117">Select **Save**.</span></span>
10. <span data-ttu-id="e3cb7-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-118">Close the page.</span></span>
11. <span data-ttu-id="e3cb7-119">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-119">Select **Save**.</span></span>
12. <span data-ttu-id="e3cb7-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-120">Close the page.</span></span>
13. <span data-ttu-id="e3cb7-121">Ga naar **Navigatievenster > Modules > Belasting > Indirecte belastingen> Bronbelasting > Bronbelastinggroepen**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="e3cb7-122">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-122">Select **New**.</span></span>
15. <span data-ttu-id="e3cb7-123">Voer in het veld **Bronbelastinggroep** de id van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="e3cb7-124">Voer in het veld **Beschrijving** de naam van de bronbelastinggroep in.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="e3cb7-125">Selecteer de bronbelastingcode in het veld **Bronbelastingcode**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="e3cb7-126">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-126">Select **Save**.</span></span>
19. <span data-ttu-id="e3cb7-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e3cb7-127">Close the page.</span></span>

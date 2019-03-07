---
title: " RegeIs en parameters instellen voor het cross-docken en klantlevering"
description: Deze procedure demonstreert de stappen om aanvullingsregels te maken.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a22756279ba316a7efd4d09c48c55e8cc98ba29d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "366323"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="f5192-103"> RegeIs en parameters instellen voor het cross-docken en klantlevering</span><span class="sxs-lookup"><span data-stu-id="f5192-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f5192-104">Deze procedure demonstreert de stappen om aanvullingsregels te maken.</span><span class="sxs-lookup"><span data-stu-id="f5192-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="f5192-105">Aanvullingsregels kunnen worden gebruikt om te bepalen hoe producten worden gedistribueerd naar winkels wanneer cross-docking en klantlevering worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f5192-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="f5192-106">Aanvullingsregels kunnen worden ingesteld voor winkels of winkelgroepen.</span><span class="sxs-lookup"><span data-stu-id="f5192-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="f5192-107">Het gewicht dat voor elke regel is gedefinieerd in een regel, bepaalt hoe de hoeveelheden van producten worden gedistribueerd tussen de winkels wanneer aanvullingsregels worden gebruikt als de distributiemethode voor cross-docking of klantlevering.</span><span class="sxs-lookup"><span data-stu-id="f5192-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="f5192-108">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="f5192-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="f5192-109">Ga naar Aanvullingsregels.</span><span class="sxs-lookup"><span data-stu-id="f5192-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="f5192-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f5192-110">Click New.</span></span>
3. <span data-ttu-id="f5192-111">Typ een waarde in het veld Aanvullingsregel.</span><span class="sxs-lookup"><span data-stu-id="f5192-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="f5192-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="f5192-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f5192-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f5192-113">Click Save.</span></span>
6. <span data-ttu-id="f5192-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f5192-114">Click Add.</span></span>
7. <span data-ttu-id="f5192-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5192-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f5192-116">U kunt Aanvullingshiërarchie of Kanaal kiezen voor het type.</span><span class="sxs-lookup"><span data-stu-id="f5192-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="f5192-117">De waarde bepaalt of de selectie in Naam een hiërarchie van kanalen of een specifiek kanaal is.</span><span class="sxs-lookup"><span data-stu-id="f5192-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="f5192-118">Voor dit voorbeeld laat u het als Aanvullingshiërarchie ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f5192-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="f5192-119">Selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f5192-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="f5192-120">De standaardgewichtwaarde wordt gevuld vanuit het gewicht dat is gedefinieerd in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="f5192-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="f5192-121">Dit gewicht kan voor de aanvullingsregel worden gebruikt of u kunt een nieuw gewicht in het veld Gewicht invoeren.</span><span class="sxs-lookup"><span data-stu-id="f5192-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="f5192-122">Voer een getal in het veld Gewicht in.</span><span class="sxs-lookup"><span data-stu-id="f5192-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="f5192-123">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f5192-123">Click Add.</span></span>
11. <span data-ttu-id="f5192-124">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f5192-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="f5192-125">Selecteer 'Kanaal' in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="f5192-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="f5192-126">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f5192-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="f5192-127">Voer een getal in het veld Gewicht in.</span><span class="sxs-lookup"><span data-stu-id="f5192-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="f5192-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f5192-128">Click Save.</span></span>


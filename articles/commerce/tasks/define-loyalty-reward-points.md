---
title: " Beloningspunten voor loyaliteit definiëren"
description: Deze procedure doorloopt het definiëren van loyaliteitsbeloningspunten.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9557b25af0fba6429d34564e1a3e158b6258698a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022119"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="26852-103"> Beloningspunten voor loyaliteit definiëren</span><span class="sxs-lookup"><span data-stu-id="26852-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="26852-104">Deze procedure doorloopt het definiëren van loyaliteitsbeloningspunten.</span><span class="sxs-lookup"><span data-stu-id="26852-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="26852-105">U moet loyaliteitsbeloningspunten instellen voordat u een loyaliteitsprogramma instelt.</span><span class="sxs-lookup"><span data-stu-id="26852-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="26852-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="26852-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="26852-107">Ga naar Retail en Commerce > Klanten > Loyaliteit > Beloningspunten voor loyaliteit.</span><span class="sxs-lookup"><span data-stu-id="26852-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="26852-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="26852-108">Click New.</span></span>
3. <span data-ttu-id="26852-109">Typ een waarde in het veld Beloningspunt-id.</span><span class="sxs-lookup"><span data-stu-id="26852-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="26852-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="26852-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="26852-111">Selecteer een optie in het veld Type beloningspunt.</span><span class="sxs-lookup"><span data-stu-id="26852-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="26852-112">Selecteer Hoeveelheid als u wilt dat de beloningspunten worden afgerond op het dichtstbijzijnde gehele getal.</span><span class="sxs-lookup"><span data-stu-id="26852-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="26852-113">Selecteer Bedrag als u wilt dat de beloningspunten worden afgerond volgens de valuta-afrondingsregels.</span><span class="sxs-lookup"><span data-stu-id="26852-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="26852-114">Als u Hoeveelheid selecteert, slaat u de volgende stap van deze procedure over.</span><span class="sxs-lookup"><span data-stu-id="26852-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="26852-115">Typ een waarde in het veld Valuta.</span><span class="sxs-lookup"><span data-stu-id="26852-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="26852-116">Voor beloningspunten van het type Bedrag hebben alle uitgegeven punten de geselecteerde valuta.</span><span class="sxs-lookup"><span data-stu-id="26852-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="26852-117">Voor beloningspunten van het type Hoeveelheid is dit veld niet van toepassing. Sla deze stap dan over.</span><span class="sxs-lookup"><span data-stu-id="26852-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="26852-118">Schakel het selectievakje Inwisselbaar in of uit.</span><span class="sxs-lookup"><span data-stu-id="26852-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="26852-119">Voer een getal in het veld Positie inwisselen in.</span><span class="sxs-lookup"><span data-stu-id="26852-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="26852-120">Positie inwisselen wordt gebruikt wanneer twee of meer inwisselbare beloningspunten kunnen worden gebruikt om voor producten te betalen.</span><span class="sxs-lookup"><span data-stu-id="26852-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="26852-121">Als de twee beloningspunten dezelfde inwisselpositie hebben, wordt het punt gebruikt dat het kleinste aantal punten nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="26852-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="26852-122">Voer een getal in het veld Waarde vervaltijd in.</span><span class="sxs-lookup"><span data-stu-id="26852-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="26852-123">De beloningspunten vervallen na het opgegeven aantal dagen, maanden of jaren nadat de punten zijn uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="26852-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="26852-124">Een waarde van '0' betekent dat de beloningspunten nooit vervallen.</span><span class="sxs-lookup"><span data-stu-id="26852-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="26852-125">Selecteer een optie in het veld Eenheid vervaltijd.</span><span class="sxs-lookup"><span data-stu-id="26852-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="26852-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="26852-126">Click Save.</span></span>

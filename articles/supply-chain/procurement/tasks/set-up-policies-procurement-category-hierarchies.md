--- 
title: "Beleid instellen voor categoriehiërarchieën voor aanschaffing"
description: Gebruik deze procedure voor het instellen van regels voor het bestellen van producten in een categorie.
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="c58d7-103">Beleid instellen voor categoriehiërarchieën voor aanschaffing</span><span class="sxs-lookup"><span data-stu-id="c58d7-103">Set up policies for procurement category hierarchies</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c58d7-104">Gebruik deze procedure voor het instellen van regels voor het bestellen van producten in een categorie.</span><span class="sxs-lookup"><span data-stu-id="c58d7-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="c58d7-105">De regels worden gedefinieerd voor een specifiek inkoopbeleid.</span><span class="sxs-lookup"><span data-stu-id="c58d7-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="c58d7-106">De regel voor categorietoegang bepaalt tot welke aanschaffingscategorieën werknemers toegang hebben bij het maken van een inkoopopdracht.</span><span class="sxs-lookup"><span data-stu-id="c58d7-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="c58d7-107">Wanneer een inkoopopdracht wordt gemaakt, worden het inkoopbeleid en de regel voor categorietoegang die moeten worden toegepast bepaald door de rechtspersoon en de operationele eenheid waartoe de werknemer behoort.</span><span class="sxs-lookup"><span data-stu-id="c58d7-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="c58d7-108">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="c58d7-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="c58d7-109">Deze taak wordt meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="c58d7-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="c58d7-110">Het inkoopbeleid zoeken</span><span class="sxs-lookup"><span data-stu-id="c58d7-110">Find the procurement policy</span></span>
1. <span data-ttu-id="c58d7-111">Ga naar Inkoopbeheer > Instellingen > Beleid > Inkoopbeleid.</span><span class="sxs-lookup"><span data-stu-id="c58d7-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="c58d7-112">Klik op de koppeling in het beleid Aanschaffingsbeleid USMF.</span><span class="sxs-lookup"><span data-stu-id="c58d7-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="c58d7-113">Dit is het beleid waaraan u een regel wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c58d7-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="c58d7-114">Dit moet een actief beleid zijn.</span><span class="sxs-lookup"><span data-stu-id="c58d7-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="c58d7-115">Een categorietoegangsregel maken</span><span class="sxs-lookup"><span data-stu-id="c58d7-115">Create a category access rule</span></span>
1. <span data-ttu-id="c58d7-116">Selecteer de beleidsregel voor categorietoegang.</span><span class="sxs-lookup"><span data-stu-id="c58d7-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="c58d7-117">Als de knop Beleidsregel maken grijs wordt weergegeven, komt dat doordat er al een actieve beleidsregel voor categorietoegang is.</span><span class="sxs-lookup"><span data-stu-id="c58d7-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="c58d7-118">Schakel de velden Ingangsdatum en Vervaldatum in om te bepalen welke dat is, selecteer deze vervolgens en klik op Beleidsregel deactiveren.</span><span class="sxs-lookup"><span data-stu-id="c58d7-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="c58d7-119">Als de knop Beleidsregel maken beschikbaar is, hoeft u niets te doen.</span><span class="sxs-lookup"><span data-stu-id="c58d7-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="c58d7-120">Klik op Beleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="c58d7-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="c58d7-121">Typ in het veld Begindatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="c58d7-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="c58d7-122">De tijd mag niet overlappen met een andere regel die al actief is.</span><span class="sxs-lookup"><span data-stu-id="c58d7-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="c58d7-123">Selecteer een categorie waarop de regel van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="c58d7-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="c58d7-124">Maak een notitie van welke categorie dit is. Deze informatie hebt u later nodig.</span><span class="sxs-lookup"><span data-stu-id="c58d7-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="c58d7-125">Wanneer u een categorie selecteert, worden alle bovenliggende categorieën eveneens toegevoegd aan de lijst Geselecteerde categorieën.</span><span class="sxs-lookup"><span data-stu-id="c58d7-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="c58d7-126">Als u wilt dat de regel geldt voor alle subcategorieën van de geselecteerde categorie, schakelt u het selectievakje Subcategorieën opnemen in.</span><span class="sxs-lookup"><span data-stu-id="c58d7-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="c58d7-127">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c58d7-127">Click Add.</span></span>
    * <span data-ttu-id="c58d7-128">Als u de optie Bovenliggende regel opnemen wilt instellen op Ja, wordt de beleidsregel die u definieert voor een bovenliggende categorie ook toegewezen aan de onderliggende categorieën als er geen beleidsregel is gedefinieerd voor de onderliggende categorieën.</span><span class="sxs-lookup"><span data-stu-id="c58d7-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="c58d7-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="c58d7-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="c58d7-130">Een categoriebeleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="c58d7-130">Create a category policy rule</span></span>
1. <span data-ttu-id="c58d7-131">Beleidsregel voor categorietoegang selecteren</span><span class="sxs-lookup"><span data-stu-id="c58d7-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="c58d7-132">Als de knop Beleidsregel grijs wordt weergegeven, selecteert u de actieve beleidsregel en klikt u vervolgens op Beleidsregel deactiveren.</span><span class="sxs-lookup"><span data-stu-id="c58d7-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="c58d7-133">Klik op Beleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="c58d7-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="c58d7-134">Typ in het veld Begindatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="c58d7-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="c58d7-135">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c58d7-135">Click Add.</span></span>
5. <span data-ttu-id="c58d7-136">Selecteer dezelfde categorie als u voor de toegangsregel voor categorie hebt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c58d7-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="c58d7-137">Selecteer een optie in het veld Leverancier selecteren.</span><span class="sxs-lookup"><span data-stu-id="c58d7-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="c58d7-138">Selecteer een regel om te bepalen welk type leveranciers kan worden geselecteerd voor de categorie bij het maken van bestelopdrachten.</span><span class="sxs-lookup"><span data-stu-id="c58d7-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="c58d7-139">Klik op Sluiten.</span><span class="sxs-lookup"><span data-stu-id="c58d7-139">Click Close.</span></span>
    * <span data-ttu-id="c58d7-140">De beleidsregels die u hebt gedefinieerd zijn voor bestelopdrachten van het type Verbruik.</span><span class="sxs-lookup"><span data-stu-id="c58d7-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="c58d7-141">Als u beleid wilt definiëren voor bestelopdrachten van het type Aanvulling, maakt u een regel voor het type beleidsregel genaamd "Toegangsbeleidsregel voor aanvullingscategorie".</span><span class="sxs-lookup"><span data-stu-id="c58d7-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  



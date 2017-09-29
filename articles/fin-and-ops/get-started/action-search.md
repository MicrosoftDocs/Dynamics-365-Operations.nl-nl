---
title: Actiezoekopdracht
description: In dit artikel wordt de zoekfunctionaliteit voor acties in Microsoft Dynamics 365 for Finance and Operations beschreven. Met een actiezoekopdracht kunt u zoeken naar acties op een pagina en deze uitvoeren.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 9b9bb0acc6f0dc1722c916f133eed766ffdd4cc8
ms.contentlocale: nl-nl
ms.lasthandoff: 06/29/2017


---

# <a name="action-search"></a><span data-ttu-id="a779e-104">Actiezoekopdracht</span><span class="sxs-lookup"><span data-stu-id="a779e-104">Action search</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a779e-105">In dit artikel wordt de zoekfunctionaliteit voor acties in Microsoft Dynamics 365 for Finance and Operations beschreven.</span><span class="sxs-lookup"><span data-stu-id="a779e-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a779e-106">Met een actiezoekopdracht kunt u zoeken naar acties op een pagina en deze uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a779e-106">Action search will help you find and run actions on a page.</span></span>

<a name="introduction"></a><span data-ttu-id="a779e-107">Introductie</span><span class="sxs-lookup"><span data-stu-id="a779e-107">Introduction</span></span>
------------

<span data-ttu-id="a779e-108">Pagina's in Microsoft Dynamics 365 for Finance and Operations bevatten voornamelijk opdrachten in actiedeelvensters, zowel in het standaardactievenster dat boven aan de pagina wordt weergegeven als op de werkbalken die in verschillende gedeelten van de pagina worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a779e-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="a779e-109">In eerdere versies kon u met de functie Tips toetsen snel een knop in een actievenster openen door op de Alt-toets en vervolgens op een reeks letters te drukken.</span><span class="sxs-lookup"><span data-stu-id="a779e-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span> 

<span data-ttu-id="a779e-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) In de huidige versie van Finance and Operations zijn Tips toetsen echter niet meer beschikbaar en zijn deze vervangen door de zoekfunctie voor acties.</span><span class="sxs-lookup"><span data-stu-id="a779e-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="a779e-111">Met deze nieuwe functie kunt u snel zoeken en een knop uitvoeren van elk weergegeven actievenster.</span><span class="sxs-lookup"><span data-stu-id="a779e-111">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="a779e-112">Actiezoekopdrachten gebruiken</span><span class="sxs-lookup"><span data-stu-id="a779e-112">Using action search</span></span>
<span data-ttu-id="a779e-113">Om de functie van het actiezoekfunctie te gebruiken, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="a779e-113">To use the action search feature, follow these steps.</span></span>

1.  <span data-ttu-id="a779e-114">Op het actievenster, klikt u in het veld **actiezoekopdracht**.</span><span class="sxs-lookup"><span data-stu-id="a779e-114">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="a779e-115">(Het **actiezoekopdracht**-veld bevat een vergrootglaspictogram.)</span><span class="sxs-lookup"><span data-stu-id="a779e-115">(The **action search** field contains a magnifying glass icon.)</span></span>
2.  <span data-ttu-id="a779e-116">Typ de hele of een deel van de naam van de knop die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a779e-116">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="a779e-117">U kunt ook zoeken met behulp van woorden van het "pad" van de knop.</span><span class="sxs-lookup"><span data-stu-id="a779e-117">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="a779e-118">(Zie de volgende sectie van dit artikel voor meer informatie.) Een knop wordt normaal gesproken boven aan de lijst met resultaten weergegeven nadat u twee tot vier tekens hebt getypt.</span><span class="sxs-lookup"><span data-stu-id="a779e-118">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3.  <span data-ttu-id="a779e-119">Zoek en start de knop in de resultatenlijst (met de muis of het toetsenbord).</span><span class="sxs-lookup"><span data-stu-id="a779e-119">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="a779e-120">Nadat de knop is uitgevoerd, keert de focus terug naar uw de laatste positie op de pagina, zodat u door kunt werken.</span><span class="sxs-lookup"><span data-stu-id="a779e-120">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span> 

<span data-ttu-id="a779e-121">[![actiezoekopdracht-veld](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="a779e-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="a779e-122">U kunt actiezoekopdrachten ook starten door Ctrl+/ of Alt+Q in te drukken.</span><span class="sxs-lookup"><span data-stu-id="a779e-122">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="a779e-123">Druk opnieuw op de toetsenbordsneltoets om de focus terug te plaatsen naar uw laatste positie op de pagina.</span><span class="sxs-lookup"><span data-stu-id="a779e-123">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="a779e-124">De resultatenlijst begrijpen</span><span class="sxs-lookup"><span data-stu-id="a779e-124">Understanding the results list</span></span>
<span data-ttu-id="a779e-125">Vaak moet u in Finance and Operations zowel de locatie als de context van een knop weten om het doel van die knop volledig te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="a779e-125">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="a779e-126">Daarom wordt er aanvullende informatie weergegeven voor elk item in de lijst met resultaten, zodat u precies begrijpt welke knoppen in de lijst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a779e-126">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="a779e-127">In het bijzonder wordt het 'pad' van de knop weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a779e-127">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="a779e-128">Dit pad kan de labels van de volgende UI-elementen bevatten, indien dit relevant is:</span><span class="sxs-lookup"><span data-stu-id="a779e-128">This path might include the labels of the following UI elements, as relevant:</span></span>

-   <span data-ttu-id="a779e-129">Tabblad actievenster</span><span class="sxs-lookup"><span data-stu-id="a779e-129">Action Pane tab</span></span>
-   <span data-ttu-id="a779e-130">Knopgroep</span><span class="sxs-lookup"><span data-stu-id="a779e-130">Button group</span></span>
-   <span data-ttu-id="a779e-131">Menuknop (als de knop in een menuknop is)</span><span class="sxs-lookup"><span data-stu-id="a779e-131">Menu button (if the button is inside a menu button)</span></span>
-   <span data-ttu-id="a779e-132">Menuscheidingsteken (als de knop in een benoemde groep in een menuknop is)</span><span class="sxs-lookup"><span data-stu-id="a779e-132">Menu separator (if the button is inside a named group inside a menu button)</span></span>
-   <span data-ttu-id="a779e-133">Groep of tabblad op de pagina (bijvoorbeeld de naam van een sneltabblad)</span><span class="sxs-lookup"><span data-stu-id="a779e-133">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="a779e-134">U hebt bijvoorbeeld **tot** in het **actiezoek**-veld getypt en bekijkt nu de resultatenlijst.</span><span class="sxs-lookup"><span data-stu-id="a779e-134">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="a779e-135">Het eerste item, voor een knop met de naam **Totalen**, wordt gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="a779e-135">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="a779e-136">Een knoppad van **Verkooporder** &gt; **Weergave** wordt ook weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a779e-136">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="a779e-137">Het gedeelte **Verkooporder** van het pad komt overeen met het tabblad **Verkooporder** in het actievenster en het gedeelte **Weergave** van het pad komt overeen met de groep **Weergave** op dat tabblad.</span><span class="sxs-lookup"><span data-stu-id="a779e-137">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab.</span></span> <span data-ttu-id="a779e-138">Evenzo geeft het pad van de knop **Totale korting** (**Verkopen** &gt; **Berekenen**) aan dat deze knop zich bevindt in de groep **Berekenen** op het tabblad **Verkopen** van het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a779e-138">Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="a779e-139">Daarom kunt u aan de hand van deze informatie precies bepalen welke knop wordt geactiveerd door de actiezoekopdracht (als u die knop selecteert in de resultatenlijst).</span><span class="sxs-lookup"><span data-stu-id="a779e-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span> 

<span data-ttu-id="a779e-140">[![actiezoekopdracht-veld-met-gegevens](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="a779e-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span> 

<span data-ttu-id="a779e-141">In het vorige voorbeeld, werden de resultaten van de actiezoekopdracht van het standaard actievenster bovenaan een pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a779e-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="a779e-142">De actiezoekopdracht geeft echter ook resultaten weer van zichtbare werkbalken die zich op andere plaatsen op de pagina bevinden.</span><span class="sxs-lookup"><span data-stu-id="a779e-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="a779e-143">U zoekt bijvoorbeeld naar de knop **Voorhanden voorraad** die zich bevindt op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="a779e-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a779e-144">In dit geval geeft het pad van de knop in de lijst met resultaten (**Verkooporderregels** &gt; **Voorraad** &gt; **Weergave**) aan dat deze knop zich bevindt onder de kop **Weergave** op de menuknop **Voorraad** op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="a779e-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span> 

<span data-ttu-id="a779e-145">[![voorhanden-voorraad](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="a779e-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="a779e-146">Actiezoekopdracht vergeleken met navigatiezoekopdracht</span><span class="sxs-lookup"><span data-stu-id="a779e-146">Action search vs. Navigation search</span></span>
<span data-ttu-id="a779e-147">Actiezoekopdrachten zijn bedoeld om acties op een pagina te zoeken en uit te voeren, maar is er een apart zoekmechanisme voor het zoeken en navigeren naar pagina's in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a779e-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="a779e-148">Zie het artikel [Navigatiezoekfunctie](navigation-search.md) voor meer informatie over deze functie.</span><span class="sxs-lookup"><span data-stu-id="a779e-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>





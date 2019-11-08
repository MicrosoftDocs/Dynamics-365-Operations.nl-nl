---
title: Typen kritieke eigenschappen van activa
description: In het onderwerp wordt uitgelegd hoe u typen kritieke eigenschappen van activa maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f96fcc7ebb8928c6d6b17b30465ad1625d9b5be4
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571065"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="59bdc-103">Typen kritieke eigenschappen van activa</span><span class="sxs-lookup"><span data-stu-id="59bdc-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="59bdc-104">In het onderwerp wordt uitgelegd hoe u typen kritieke eigenschappen van activa maakt in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="59bdc-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="59bdc-105">Kritieke eigenschappen van activa zijn gerelateerd aan activa en worden overgebracht naar werkorders.</span><span class="sxs-lookup"><span data-stu-id="59bdc-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="59bdc-106">Zij kunnen niet worden gewijzigd in een werkorder.</span><span class="sxs-lookup"><span data-stu-id="59bdc-106">It can't be changed on a work order.</span></span> <span data-ttu-id="59bdc-107">Kritieke eigenschappen van activa worden gebruikt voor het berekenen van kritieke eigenschappen van een werkorder tijdens de planning van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="59bdc-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="59bdc-108">Met andere woorden, zij worden gebruikt om te berekenen in hoeverre een onderhoudstaak voor een activum van invloed is op het productieschema en de productiviteit in uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="59bdc-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="59bdc-109">Zie [Parameters voor activabeheer](../setup-for-objects/enterprise-asset-management-parameters.md) voor meer informatie over de instellingen die zijn gerelateerd aan de berekening van beoordelingsscores voor de planning van werkorders.</span><span class="sxs-lookup"><span data-stu-id="59bdc-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="59bdc-110">Als u kritieke eigenschappen wilt instellen, maakt u eerst de typen kritieke eigenschappen die moeten worden gebruikt in de activa-instellingen.</span><span class="sxs-lookup"><span data-stu-id="59bdc-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="59bdc-111">Vervolgens stelt u kritieke eigenschappen van activa in.</span><span class="sxs-lookup"><span data-stu-id="59bdc-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="59bdc-112">Typen kritieke eigenschappen instellen</span><span class="sxs-lookup"><span data-stu-id="59bdc-112">Set up criticality types</span></span>

1. <span data-ttu-id="59bdc-113">Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Typen kritieke eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="59bdc-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="59bdc-114">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="59bdc-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="59bdc-115">Voer in het veld **Kritieke eigenschappen** een getal in dat de kritieke eigenschappen aangeeft.</span><span class="sxs-lookup"><span data-stu-id="59bdc-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="59bdc-116">Voer in het veld **Naam** een naam voor het type kritieke eigenschappen in.</span><span class="sxs-lookup"><span data-stu-id="59bdc-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="59bdc-117">Voer in het veld **Factor** een factor in.</span><span class="sxs-lookup"><span data-stu-id="59bdc-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="59bdc-118">Deze factor wordt gebruikt tijdens de berekening van de werkorderplanning om de record voor kritieke eigenschappen te bepalen die moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="59bdc-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="59bdc-119">(Er wordt altijd gebruikgemaakt van de record met de hoogste factor.) Deze instelling is relevant als, zoals wordt weergegeven in de volgende afbeelding, regels voor kritieke eigenschappen worden gemaakt met dezelfde waarde voor kritieke eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="59bdc-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Pagina Typen kritieke eigenschappen](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="59bdc-121">Kritieke eigenschappen van activa instellen</span><span class="sxs-lookup"><span data-stu-id="59bdc-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="59bdc-122">Selecteer **Activabeheer** \> **Instellingen** \> **Kritieke eigenschappen van activa**.</span><span class="sxs-lookup"><span data-stu-id="59bdc-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="59bdc-123">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="59bdc-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="59bdc-124">Afhankelijk van het vereiste detailniveau voor kritieke eigenschappen van activa moet u relevante selecties maken in de velden **Functionele locatie**, **Activatype**, **Fabrikant**, **Model**, **Activum**, **Categorie van taaktype**, **Taaktype**, **Variant van taaktype** en **Taakbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="59bdc-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="59bdc-125">Wanneer de kritieke eigenschappen van een activum zijn geselecteerd, doorloopt Activabeheer alle records voor kritieke eigenschappen van activa om te controleren op een mogelijke overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="59bdc-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="59bdc-126">De meest specifieke combinatie wordt altijd als eerste gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="59bdc-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="59bdc-127">Met andere woorden, Activabeheer controleert eerst **Taakbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="59bdc-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="59bdc-128">Als er geen overeenkomst wordt gevonden, wordt **Variant van taaktype** gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="59bdc-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="59bdc-129">Als er geen overeenkomst wordt gevonden, wordt **Taaktype** gecontroleerd, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="59bdc-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="59bdc-130">Zoals u zien in de lay-out van de pagina, betekent dit gedrag dat Activabeheer elke record van rechts naar links controleert op overeenkomst om de meest specifieke combinatie te vinden.</span><span class="sxs-lookup"><span data-stu-id="59bdc-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="59bdc-131">Als er geen overeenkomst wordt gevonden, wordt de 'standaardrecord' zonder selecties gebruikt.</span><span class="sxs-lookup"><span data-stu-id="59bdc-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="59bdc-132">Selecteer in het veld **Kritieke eigenschappen** een van de waarden voor kritieke eigenschappen die u in de vorige procedure hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="59bdc-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="59bdc-133">Opmerkingen over de instelling van kritieke eigenschappen</span><span class="sxs-lookup"><span data-stu-id="59bdc-133">Notes about criticality setup</span></span>

- <span data-ttu-id="59bdc-134">Als u de kritieke eigenschappen van een activum in deze instellingen wijzigt nadat u deze al hebt gebruikt op een werkorder, worden de kritieke eigenschappen van de werkorder niet dienovereenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="59bdc-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="59bdc-135">De kritieke eigenschappen van een werkorder worden telkens opnieuw berekend wanneer een werkorderregel wordt toegevoegd aan of verwijderd uit de werkorder.</span><span class="sxs-lookup"><span data-stu-id="59bdc-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="59bdc-136">Als een werkorder meerdere werkordertaken bevat, wordt voor de werkorder altijd gebruikgemaakt van de hoogste kritieke eigenschappen, volgens het veld **Factor** op de pagina **Typen kritieke eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="59bdc-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="59bdc-137">Over het algemeen kunnen kritieke eigenschappen van activa veranderen gedurende een periode.</span><span class="sxs-lookup"><span data-stu-id="59bdc-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="59bdc-138">Kritieke eigenschappen kunnen worden beïnvloed door de aanschaf van nieuwe apparatuur, verbouwingen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="59bdc-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="59bdc-139">Overweeg om de kritieke eigenschappen van uw activa op regelmatige tijdstippen opnieuw te evalueren (bijvoorbeeld één keer per jaar of om het andere jaar) om ervoor te zorgen dat uw definities voor kritieke eigenschappen overeenkomen met uw huidige productie-instellingen.</span><span class="sxs-lookup"><span data-stu-id="59bdc-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>

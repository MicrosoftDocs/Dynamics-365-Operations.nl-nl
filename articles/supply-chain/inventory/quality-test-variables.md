---
title: Testvariabelen voor kwaliteitsbeheer
description: In dit onderwerp wordt beschreven hoe u testvariabelen maakt die kunnen worden gebruikt voor het kwalitatief testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956609"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="603b0-103">Testvariabelen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="603b0-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="603b0-104">In dit onderwerp wordt beschreven hoe u testvariabelen maakt die kunnen worden gebruikt voor het kwalitatief testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="603b0-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="603b0-105">U moet een testvariabele en de bijbehorende uitkomsten (resultaten) definiëren voor elke kwalitatieve test die is gedefinieerd op de pagina **Tests**.</span><span class="sxs-lookup"><span data-stu-id="603b0-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="603b0-106">(Voor kwalitatieve tests wordt het veld **Type** op de pagina **Tests** ingesteld op *Optie*.)</span><span class="sxs-lookup"><span data-stu-id="603b0-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="603b0-107">U gebruikt de pagina **Testvariabelen** om de mogelijke resultaten in te stellen, te bewerken en weer te geven voor een testvariabele die aan een kwalitatieve test is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="603b0-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="603b0-108">Voor elk resultaat kunt u de uitslagstatus *Goedgekeurd* of *Afgekeurd* toewijzen om aan te geven of de test is geslaagd of mislukt wanneer dat resultaat als testresultaat wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="603b0-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="603b0-109">U gebruikt de pagina **Testgroepen** om een testvariabele en een standaarduitkomst toe te wijzen aan een afzonderlijke kwalitatieve test.</span><span class="sxs-lookup"><span data-stu-id="603b0-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="603b0-110">Voor elke testvariabele is het raadzaam om minimaal twee resultaten te definiëren: een resultaat met de uitslagstatus *Goedgekeurd* en een resultaat met de uitslagstatus *Afgekeurd*.</span><span class="sxs-lookup"><span data-stu-id="603b0-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="603b0-111">Er is geen limiet voor het totale aantal variabelen of resultaten dat kan worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="603b0-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="603b0-112">Daarnaast kunnen voor meerdere tests dezelfde testvariabelen worden gebruikt om resultaten vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="603b0-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="603b0-113">Voorbeelden van testvariabelen</span><span class="sxs-lookup"><span data-stu-id="603b0-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="603b0-114">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="603b0-114">Example 1</span></span>

<span data-ttu-id="603b0-115">Een productiebedrijf voert twee tests uit op gefabriceerde materialen.</span><span class="sxs-lookup"><span data-stu-id="603b0-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="603b0-116">In de ene test is het pH-niveau aan een kleurstrook gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="603b0-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="603b0-117">Acceptabele pH-niveaus hebben lichtere kleuren en niet-acceptabele pH-niveaus hebben donkerder kleuren.</span><span class="sxs-lookup"><span data-stu-id="603b0-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="603b0-118">In een andere test worden meerdere visuele inspecties uitgevoerd en kwaliteitsmedewerkers maken gebruik van hun oordeel om te bepalen of het artikel al dan niet door de visuele inspectie komt.</span><span class="sxs-lookup"><span data-stu-id="603b0-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="603b0-119">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="603b0-119">Example 2</span></span>

<span data-ttu-id="603b0-120">Een productiebedrijf dat koekjes produceert, maakt gebruik van een inspectietest voor het eindproduct.</span><span class="sxs-lookup"><span data-stu-id="603b0-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="603b0-121">Deze inspectietest omvat verschillende variabelen.</span><span class="sxs-lookup"><span data-stu-id="603b0-121">This inspection test has several variables.</span></span> <span data-ttu-id="603b0-122">Een van deze variabelen is Smaak met de mogelijke resultaten Goed en Slecht.</span><span class="sxs-lookup"><span data-stu-id="603b0-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="603b0-123">Een tweede variabele is Kleur met als mogelijke resultaten Te donker, Te licht en Correct.</span><span class="sxs-lookup"><span data-stu-id="603b0-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="603b0-124">Een testvariabele maken</span><span class="sxs-lookup"><span data-stu-id="603b0-124">Create a test variable</span></span>

<span data-ttu-id="603b0-125">Volg deze stappen om een testvariabele te maken.</span><span class="sxs-lookup"><span data-stu-id="603b0-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="603b0-126">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Testvariabelen**.</span><span class="sxs-lookup"><span data-stu-id="603b0-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="603b0-127">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="603b0-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="603b0-128">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="603b0-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="603b0-129">**Variabele**: voer een unieke id of naam voor de variabele in.</span><span class="sxs-lookup"><span data-stu-id="603b0-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="603b0-130">**Beschrijving**: voer een gedetailleerde beschrijving voor de variabele in.</span><span class="sxs-lookup"><span data-stu-id="603b0-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="603b0-131">Selecteer, terwijl de nieuwe rij nog steeds is geselecteerd, de optie **Resultaten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="603b0-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="603b0-132">Selecteer op de pagina **Resultaten van testvariabelen** in het actievenster de optie **Nieuw** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="603b0-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="603b0-133">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="603b0-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="603b0-134">**Resultaat**: voer een unieke id of naam voor het resultaat in.</span><span class="sxs-lookup"><span data-stu-id="603b0-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="603b0-135">**Beschrijving**: voer een gedetailleerde beschrijving voor het resultaat in.</span><span class="sxs-lookup"><span data-stu-id="603b0-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="603b0-136">**Resultaat**: selecteer *Goedgekeurd* of *Afgekeurd* om aan te geven of de test is geslaagd of mislukt wanneer het resultaat als testresultaat wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="603b0-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="603b0-137">Herhaal de vorige stap voor elk extra resultaat.</span><span class="sxs-lookup"><span data-stu-id="603b0-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="603b0-138">Zorg ervoor dat ten minste één uitkomst de uitslagstatus *Goedgekeurd* heeft en ten minste één resultaat de uitslagstatus *Afgekeurd*.</span><span class="sxs-lookup"><span data-stu-id="603b0-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="603b0-139">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="603b0-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="603b0-140">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="603b0-140">Additional resources</span></span>

- [<span data-ttu-id="603b0-141">Testinstrumenten voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="603b0-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="603b0-142">Kwaliteitsbeheertests</span><span class="sxs-lookup"><span data-stu-id="603b0-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="603b0-143">Testgroepen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="603b0-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

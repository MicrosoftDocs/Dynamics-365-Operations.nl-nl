---
title: Kwaliteitsbeheertests
description: In dit onderwerp wordt beschreven hoe u tests maakt die kunnen worden gebruikt voor kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021679"
---
# <a name="quality-management-tests"></a><span data-ttu-id="15ab7-103">Kwaliteitsbeheertests</span><span class="sxs-lookup"><span data-stu-id="15ab7-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15ab7-104">In dit onderwerp wordt beschreven hoe u tests maakt die kunnen worden gebruikt voor kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="15ab7-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="15ab7-105">U gebruikt de pagina **Tests** om de afzonderlijke tests definiëren en bekijken aan de hand waarvan wordt bepaald of uw producten voldoen aan de kwaliteitsspecificaties.</span><span class="sxs-lookup"><span data-stu-id="15ab7-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="15ab7-106">U kunt een of meer afzonderlijke tests toewijzen aan een testgroep.</span><span class="sxs-lookup"><span data-stu-id="15ab7-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="15ab7-107">In dit geval geeft u ook testspecifieke informatie op, zoals de aanvaardbare meetwaarden.</span><span class="sxs-lookup"><span data-stu-id="15ab7-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="15ab7-108">Meetwaarden worden gebruikt voor kwantitatieve tests.</span><span class="sxs-lookup"><span data-stu-id="15ab7-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="15ab7-109">Voor kwalitatieve tests worden testvariabelen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="15ab7-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="15ab7-110">Voor kwantitatieve tests wordt het veld **Type** ingesteld op *Geheel getal* of *Breuk*.</span><span class="sxs-lookup"><span data-stu-id="15ab7-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="15ab7-111">Er is ook een maateenheid opgegeven.</span><span class="sxs-lookup"><span data-stu-id="15ab7-111">A unit of measure is also specified.</span></span> <span data-ttu-id="15ab7-112">Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen.</span><span class="sxs-lookup"><span data-stu-id="15ab7-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="15ab7-113">Voor kwalitatieve tests wordt het veld **Type** ingesteld op *Optie*.</span><span class="sxs-lookup"><span data-stu-id="15ab7-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="15ab7-114">Voor kwalitatieve tests is aanvullende informatie nodig over de testvariabele die wordt gemeten en de vaste opties.</span><span class="sxs-lookup"><span data-stu-id="15ab7-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="15ab7-115">Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen volgens een uitkomst.</span><span class="sxs-lookup"><span data-stu-id="15ab7-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="15ab7-116">U kunt een testinstrument ook toewijzen aan een test.</span><span class="sxs-lookup"><span data-stu-id="15ab7-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="15ab7-117">Testinstrumenten zijn echter niet vereist voor het maken en gebruiken van tests met kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="15ab7-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="15ab7-118">Zie [Testinstrumenten voor kwaliteitsbeheer](quality-test-instruments.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="15ab7-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="15ab7-119">U kunt ook een eenheid voor een test opgeven om de maateenheid aan te geven waarin de testresultaten worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="15ab7-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="15ab7-120">Een test voor temperatuur kan bijvoorbeeld de eenheid voor graden Fahrenheit of Celsius bevatten.</span><span class="sxs-lookup"><span data-stu-id="15ab7-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="15ab7-121">Voorbeeld van een test</span><span class="sxs-lookup"><span data-stu-id="15ab7-121">Example of a test</span></span>

<span data-ttu-id="15ab7-122">Een productiebedrijf voert twee tests uit op ingekocht materiaal: een kwantitatieve test op de kwaliteit van het materiaal en een kwalitatieve test op beschadigde verpakking.</span><span class="sxs-lookup"><span data-stu-id="15ab7-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="15ab7-123">Het bedrijf definieert aanvullende gegevens voor de kwalitatieve test om de testvariabele (bijvoorbeeld beschadigde verpakking) en het bijbehorende resultaat te definiëren.</span><span class="sxs-lookup"><span data-stu-id="15ab7-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="15ab7-124">Het bedrijf maakt gebruikt van de pagina **Testgroepen** om de twee tests toe te wijzen aan een testgroep en om specifieke informatie voor de tests op te geven.</span><span class="sxs-lookup"><span data-stu-id="15ab7-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="15ab7-125">De testgroep wordt toegewezen aan een kwaliteitsorder, zodat het bedrijf de testresultaten van de twee tests kan rapporteren.</span><span class="sxs-lookup"><span data-stu-id="15ab7-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="15ab7-126">Een test maken</span><span class="sxs-lookup"><span data-stu-id="15ab7-126">Create a test</span></span>

<span data-ttu-id="15ab7-127">Volg deze stappen om een test te maken.</span><span class="sxs-lookup"><span data-stu-id="15ab7-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="15ab7-128">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Tests**.</span><span class="sxs-lookup"><span data-stu-id="15ab7-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="15ab7-129">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="15ab7-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="15ab7-130">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="15ab7-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="15ab7-131">**Test**: voer een unieke id of naam op voor de test in.</span><span class="sxs-lookup"><span data-stu-id="15ab7-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="15ab7-132">**Beschrijving**: voer een gedetailleerde beschrijving voor de test in.</span><span class="sxs-lookup"><span data-stu-id="15ab7-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="15ab7-133">**Type**: selecteer het type resultaten dat door de test wordt geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="15ab7-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="15ab7-134">Selecteer voor kwantitatieve tests *Breuk* of *Geheel getal*.</span><span class="sxs-lookup"><span data-stu-id="15ab7-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="15ab7-135">Selecteer voor kwalitatieve tests *Optie*.</span><span class="sxs-lookup"><span data-stu-id="15ab7-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="15ab7-136">**Testinstrument**: selecteer een [testinstrument](quality-test-instruments.md) dat moet worden gebruikt voor de test.</span><span class="sxs-lookup"><span data-stu-id="15ab7-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="15ab7-137">**Eenheid**: als u *Breuk* of *Geheel getal* hebt geselecteerd in het veld **Type** (dat wil zeggen, als de test een kwantitatieve test is), selecteert u de maateenheid waarin de testresultaten moeten worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="15ab7-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="15ab7-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="15ab7-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="15ab7-139">Nadat u een test hebt opgeslaan, kunt u het veld **Type** in het raster niet meer bewerken.</span><span class="sxs-lookup"><span data-stu-id="15ab7-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="15ab7-140">Als u het type testresultaten moet wijzigen dat wordt vastgelegd voor een test, selecteert u **Type kwaliteitstest wijzigen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="15ab7-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="15ab7-141">Stel in het dialoogvenster **Type kwaliteitstest wijzigen** het veld **Nieuw type** in op het gewenste type en selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="15ab7-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15ab7-142">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="15ab7-142">Additional resources</span></span>

- [<span data-ttu-id="15ab7-143">Testinstrumenten voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="15ab7-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="15ab7-144">Testgroepen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="15ab7-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="15ab7-145">Testvariabelen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="15ab7-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="15ab7-146">Kwaliteitskoppelingen</span><span class="sxs-lookup"><span data-stu-id="15ab7-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

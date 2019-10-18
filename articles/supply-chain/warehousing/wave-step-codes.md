---
title: Wave-stapcodes
description: Dit onderwerp biedt een overzicht van wave-stapcodes en hoe deze worden gebruikt.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992352"
---
# <a name="wave-step-codes"></a><span data-ttu-id="c5661-103">Wave-stapcodes</span><span class="sxs-lookup"><span data-stu-id="c5661-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="c5661-104">Wave-stapcodes</span><span class="sxs-lookup"><span data-stu-id="c5661-104">About wave step codes</span></span>

<span data-ttu-id="c5661-105">Wave-stapcodes zijn codes die gebruikers kunnen instellen en gebruiken om specifieke instanties van wave-methoden aan een bijbehorende sjabloon te koppelen.</span><span class="sxs-lookup"><span data-stu-id="c5661-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="c5661-106">De sjablonen bevatten sjablonen voor aanvulling, containers, afdrukken van etiketten, belasting bouwen en sorteren.</span><span class="sxs-lookup"><span data-stu-id="c5661-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="c5661-107">Wanneer er geen wave-stapcodes worden gebruikt, moeten gebruikers vrije tekst invoeren om naar een bepaalde sjabloon te verwijzen vanuit het wave-methode-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="c5661-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="c5661-108">Vrije tekst is gevoelig voor fouten, omdat gebruikers ervoor moeten zorgen dat de tekst met de wave-stap die zij toevoegen voor een specifieke wave-stapmethode in een wave-sjabloon exact overeenkomt met de tekst van de wave-stap in de doelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="c5661-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="c5661-109">Wave-stapcodes voor een specifiek wave-staptype worden ingesteld op een afzonderlijke pagina.</span><span class="sxs-lookup"><span data-stu-id="c5661-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="c5661-110">Voor elke wave-stapmethode-instantie in een wave-sjabloon waarvoor een wave-stapcode moet worden gebruikt, moet de wave-stapcode worden geselecteerd in een vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="c5661-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="c5661-111">De selectie in een vervolgkeuzelijst vervangt vrije tekstinvoer en vermindert het risico en de impact van de menselijke fout.</span><span class="sxs-lookup"><span data-stu-id="c5661-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="c5661-112">Met instellingscodes wordt een wave-stapmethode in een wave-sjabloon gekoppeld aan een doelsjabloon voor de methode.</span><span class="sxs-lookup"><span data-stu-id="c5661-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="c5661-113">Het gebruik van de wave-stapcode is optioneel en de opname is per rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="c5661-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="c5661-114">Als een bepaalde rechtspersoon de functie gebruikt, worden alle bestaande wave-stapcodes in die rechtspersoon dus bijgewerkt naar de nieuwe structuur.</span><span class="sxs-lookup"><span data-stu-id="c5661-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="c5661-115">Demo instellen</span><span class="sxs-lookup"><span data-stu-id="c5661-115">Setup demo</span></span> 

<span data-ttu-id="c5661-116">Voor deze demo moeten demogegevens worden geïnstalleerd en moet u het **USMF**-voorbeeld-gegevensbedrijf gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c5661-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="c5661-117">Wave-stapcodes inschakelen</span><span class="sxs-lookup"><span data-stu-id="c5661-117">Enable wave step codes</span></span>

<span data-ttu-id="c5661-118">Voer de volgende stappen uit om de functie wave-stapcodes in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="c5661-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="c5661-119">Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="c5661-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="c5661-120">Stel op het tabblad **Algemeen** op het sneltabblad **Wave-goedkeuring** de optie **Wave-stapcodes inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c5661-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="c5661-121">Alle bestaande vrije teksten uit de Wave-stap worden bijgewerkt naar de nieuwe structuur.</span><span class="sxs-lookup"><span data-stu-id="c5661-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="c5661-122">Nadat deze upgrade voor een rechts persoon is voltooid, is de optie **Wave-stapcodes** inschakelen niet meer beschikbaar op de pagina **Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="c5661-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="c5661-123">Validaties worden uitgevoerd tijdens de upgrade en als de upgrade mislukt, wordt een foutbericht weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="c5661-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="c5661-124">Een upgrade kan mislukken vanwege de volgende conflicten:</span><span class="sxs-lookup"><span data-stu-id="c5661-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="c5661-125">Er zijn dubbele wave-stapteksten beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="c5661-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="c5661-126">Aanpassingen bestaan.</span><span class="sxs-lookup"><span data-stu-id="c5661-126">Customizations exist.</span></span>
- <span data-ttu-id="c5661-127">Een wave-stapvrije tekst die is gekoppeld aan een instantie van de wave-stapmethode komt niet overeen met het verwachte sjabloontype.</span><span class="sxs-lookup"><span data-stu-id="c5661-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="c5661-128">Nadat u de conflicten die tijdens de validaties zijn geïdentificeerd hebt opgelost, kunt u het upgradeproces opnieuw uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c5661-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="c5661-129">Wanneer de upgrade slaagt, wordt de pagina met **Wave-stapcodes** (**Magazijnbeheer \> Instellingen \> Waves \> Wave-stapcodes**) weer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="c5661-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="c5661-130">Op deze pagina worden de wave-stapcodes weergegeven die zijn bijgewerkt toen de functie voor wave-stapcodes werd ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c5661-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="c5661-131">Nieuwe wave-stapcodes maken</span><span class="sxs-lookup"><span data-stu-id="c5661-131">Create new wave step codes</span></span>

<span data-ttu-id="c5661-132">U kunt de pagina **Wave-stapcodes** gebruiken om Wave-stapcodes te maken en te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c5661-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="c5661-133">Elke nieuwe wave-stapcode en de bijbehorende ID moeten uniek zijn binnen alle wave-staptypen en moeten worden gedefinieerd voor een specifiek wave-staptype.</span><span class="sxs-lookup"><span data-stu-id="c5661-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="c5661-134">Wave-stapcodes toepassen</span><span class="sxs-lookup"><span data-stu-id="c5661-134">Apply wave step codes</span></span>

<span data-ttu-id="c5661-135">Nadat u de juiste wave-stapcodes hebt gedefinieerd, kunnen deze worden toegepast op de wave-procesmethoden.</span><span class="sxs-lookup"><span data-stu-id="c5661-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="c5661-136">Ga naar de gewenste doelsjabloon om wave-stapcodes toe te passen.</span><span class="sxs-lookup"><span data-stu-id="c5661-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="c5661-137">Dit zijn de doelsjablonen waaraan de wave-stapcodes zijn toegewezen om naar toe te wijzen:</span><span class="sxs-lookup"><span data-stu-id="c5661-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="c5661-138">**Aanvullingssjablonen:** Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen</span><span class="sxs-lookup"><span data-stu-id="c5661-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="c5661-139">**Sjablonen voor lading samenstellen:** Magazijnbeheer \> Instellingen \> Lading \> Sjablonen voor lading samenstellen</span><span class="sxs-lookup"><span data-stu-id="c5661-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="c5661-140">**Sorteersjablonen:** Magazijnbeheer \> Instellingen \> Verpakking \> Uitgaande Sorteersjablonen</span><span class="sxs-lookup"><span data-stu-id="c5661-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="c5661-141">**Sjablonen voor containervorming:** Magazijnbeheer \> Instellingen \> Containers \> Sjablonen voor containerbouw</span><span class="sxs-lookup"><span data-stu-id="c5661-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="c5661-142">**Sjablonen om etiketten af te drukken:** Magazijnbeheer \> Instellingen \> Documentroutering \> Wave-labelsjablonen</span><span class="sxs-lookup"><span data-stu-id="c5661-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="c5661-143">De sjablonen in deze lijst worden toegepast wanneer er wordt verwezen vanuit een wave-procesmethode die is geselecteerd in een wave-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="c5661-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="c5661-144">Wanneer de wave-stapcode van een wave-procesmethode in een wave-sjabloon overeenkomt met de wave-stapcode in een van de sjabloontypen, wordt de sjabloon toegepast.</span><span class="sxs-lookup"><span data-stu-id="c5661-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="c5661-145">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="c5661-145">Sample scenario</span></span>

<span data-ttu-id="c5661-146">Met de volgende procedure kunt u garanderen dat de aanvullingssjabloon die u hebt gemaakt voor de wave- sjabloon wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="c5661-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="c5661-147">Ga naar **Magazijnbeheer \> Instellingen \> Waves \> Wave-stapcodes** en maak een wave-stapcode for het type **Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="c5661-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="c5661-148">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen** en maak een aanvullingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="c5661-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="c5661-149">Selecteer in het aanvullingssjabloon de wave-stapcode die u voor het type **Aanvulling** hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c5661-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="c5661-150">Ga naar **Magazijnbeheer \> Instellingen \> Waves \> Wave-sjablonen** en selecteer de wave-sjabloon die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c5661-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="c5661-151">Selecteer in de sjabloon op het sneltabblad **Methoden** de methode **Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="c5661-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="c5661-152">Selecteer in het veld **Wave-stapcode** de wave-stapcode die u voor de aanvullingssjabloon hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c5661-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

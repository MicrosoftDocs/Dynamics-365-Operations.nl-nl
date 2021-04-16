---
title: Wave-stapcodes
description: Dit onderwerp biedt een overzicht van wave-stapcodes en hoe deze worden gebruikt.
author: josaw1
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f44d500d58dffb37b27d230b0633336eb87996a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838053"
---
# <a name="wave-step-codes"></a><span data-ttu-id="58320-103">Wave-stapcodes</span><span class="sxs-lookup"><span data-stu-id="58320-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58320-104">Wave-stapcodes zijn codes die gebruikers kunnen instellen en gebruiken om specifieke instanties van wave-methoden aan een bijbehorende sjabloon te koppelen.</span><span class="sxs-lookup"><span data-stu-id="58320-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="58320-105">De sjablonen bevatten sjablonen voor aanvulling, containers, afdrukken van etiketten, belasting bouwen en sorteren.</span><span class="sxs-lookup"><span data-stu-id="58320-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="58320-106">Wanneer er geen wave-stapcodes worden gebruikt, moeten gebruikers vrije tekst invoeren om naar een bepaalde sjabloon te verwijzen vanuit het wave-methode-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="58320-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="58320-107">Vrije tekst is gevoelig voor fouten, omdat gebruikers ervoor moeten zorgen dat de tekst met de wave-stap die zij toevoegen voor een specifieke wave-stapmethode in een wave-sjabloon exact overeenkomt met de tekst van de wave-stap in de doelsjabloon.</span><span class="sxs-lookup"><span data-stu-id="58320-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="58320-108">Wave-stapcodes voor een specifiek wave-staptype worden ingesteld op een afzonderlijke pagina.</span><span class="sxs-lookup"><span data-stu-id="58320-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="58320-109">Voor elke wave-stapmethode-instantie in een wave-sjabloon waarvoor een wave-stapcode moet worden gebruikt, moet de wave-stapcode worden geselecteerd in een vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="58320-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="58320-110">De selectie in een vervolgkeuzelijst vervangt vrije tekstinvoer en vermindert het risico en de impact van de menselijke fout.</span><span class="sxs-lookup"><span data-stu-id="58320-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="58320-111">Met instellingscodes wordt een wave-stapmethode in een wave-sjabloon gekoppeld aan een doelsjabloon voor de methode.</span><span class="sxs-lookup"><span data-stu-id="58320-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="58320-112">Het gebruik van de functie voor wave-stapcodes is optioneel.</span><span class="sxs-lookup"><span data-stu-id="58320-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="58320-113">Het is organisatiebreed ingeschakeld voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="58320-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="58320-114">Demo instellen</span><span class="sxs-lookup"><span data-stu-id="58320-114">Setup demo</span></span> 

<span data-ttu-id="58320-115">Voor deze demo moeten demogegevens worden geïnstalleerd en moet u het **USMF**-voorbeeld-gegevensbedrijf gebruiken.</span><span class="sxs-lookup"><span data-stu-id="58320-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="58320-116">Wave-stapcodes inschakelen</span><span class="sxs-lookup"><span data-stu-id="58320-116">Enable wave step codes</span></span>

<span data-ttu-id="58320-117">Voer de volgende stappen uit om de functie wave-stapcodes in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="58320-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="58320-118">Ga naar **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="58320-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="58320-119">Schakel de functie **Organisatiebrede wave-stapcode inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="58320-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="58320-120">Alle bestaande vrije teksten uit de wave-stap in alle rechtspersonen worden bijgewerkt naar de nieuwe structuur.</span><span class="sxs-lookup"><span data-stu-id="58320-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="58320-121">Nadat deze upgrade voor alle rechtspersonen is voltooid, wordt de functie ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="58320-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="58320-122">Als de functie niet kan worden ingeschakeld voor een of meer rechtspersonen, wordt de functie voor geen enkele rechtspersoon ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="58320-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="58320-123">Tijdens het inschakelen worden validaties uitgevoerd tijdens de gegevensupgrade.</span><span class="sxs-lookup"><span data-stu-id="58320-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="58320-124">Als de upgrade mislukt, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="58320-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="58320-125">Een upgrade kan mislukken vanwege de volgende conflicten:</span><span class="sxs-lookup"><span data-stu-id="58320-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="58320-126">Er zijn dubbele wave-stapteksten beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="58320-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="58320-127">Aanpassingen bestaan.</span><span class="sxs-lookup"><span data-stu-id="58320-127">Customizations exist.</span></span>
- <span data-ttu-id="58320-128">Een wave-stapvrije tekst die is gekoppeld aan een instantie van de wave-stapmethode komt niet overeen met het verwachte sjabloontype.</span><span class="sxs-lookup"><span data-stu-id="58320-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="58320-129">Nadat u de conflicten die tijdens de validaties zijn geïdentificeerd hebt opgelost, kunt u de functie opnieuw proberen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="58320-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="58320-130">Wanneer de functie is ingeschakeld, wordt de pagina met **wave-stapcodes** (**Magazijnbeheer \> Instellingen \> Waves \> Wave-stapcodes**) weer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="58320-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="58320-131">Op deze pagina worden de wave-stapcodes weergegeven die zijn bijgewerkt toen de functie voor organisatiebrede wave-stapcodes werd ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="58320-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="58320-132">Nieuwe wave-stapcodes maken</span><span class="sxs-lookup"><span data-stu-id="58320-132">Create new wave step codes</span></span>

<span data-ttu-id="58320-133">U kunt de pagina **Wave-stapcodes** gebruiken om Wave-stapcodes te maken en te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="58320-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="58320-134">Elke nieuwe wave-stapcode en de bijbehorende ID moeten uniek zijn binnen alle wave-staptypen en moeten worden gedefinieerd voor een specifiek wave-staptype.</span><span class="sxs-lookup"><span data-stu-id="58320-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="58320-135">Wave-stapcodes toepassen</span><span class="sxs-lookup"><span data-stu-id="58320-135">Apply wave step codes</span></span>

<span data-ttu-id="58320-136">Nadat u de juiste wave-stapcodes hebt gedefinieerd, kunnen deze worden toegepast op de wave-procesmethoden.</span><span class="sxs-lookup"><span data-stu-id="58320-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="58320-137">Ga naar de gewenste doelsjabloon om wave-stapcodes toe te passen.</span><span class="sxs-lookup"><span data-stu-id="58320-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="58320-138">Dit zijn de doelsjablonen waaraan de wave-stapcodes zijn toegewezen om naar toe te wijzen:</span><span class="sxs-lookup"><span data-stu-id="58320-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="58320-139">**Aanvullingssjablonen:** Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen</span><span class="sxs-lookup"><span data-stu-id="58320-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="58320-140">**Sjablonen voor lading samenstellen:** Magazijnbeheer \> Instellingen \> Lading \> Sjablonen voor lading samenstellen</span><span class="sxs-lookup"><span data-stu-id="58320-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="58320-141">**Sorteersjablonen:** Magazijnbeheer \> Instellingen \> Verpakking \> Uitgaande Sorteersjablonen</span><span class="sxs-lookup"><span data-stu-id="58320-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="58320-142">**Sjablonen voor containervorming:** Magazijnbeheer \> Instellingen \> Containers \> Sjablonen voor containerbouw</span><span class="sxs-lookup"><span data-stu-id="58320-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="58320-143">**Sjablonen om etiketten af te drukken:** Magazijnbeheer \> Instellingen \> Documentroutering \> Wave-labelsjablonen</span><span class="sxs-lookup"><span data-stu-id="58320-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="58320-144">De sjablonen in deze lijst worden toegepast wanneer er wordt verwezen vanuit een wave-procesmethode die is geselecteerd in een wave-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="58320-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="58320-145">Wanneer de wave-stapcode van een wave-procesmethode in een wave-sjabloon overeenkomt met de wave-stapcode in een van de sjabloontypen, wordt de sjabloon toegepast.</span><span class="sxs-lookup"><span data-stu-id="58320-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="58320-146">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="58320-146">Sample scenario</span></span>

<span data-ttu-id="58320-147">Met de volgende procedure kunt u garanderen dat de aanvullingssjabloon die u hebt gemaakt voor de wave- sjabloon wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="58320-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="58320-148">Ga naar **Magazijnbeheer \> Instellingen \> Waves \> Wave-stapcodes** en maak een wave-stapcode for het type **Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="58320-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="58320-149">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen** en maak een aanvullingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="58320-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="58320-150">Selecteer in het aanvullingssjabloon de wave-stapcode die u voor het type **Aanvulling** hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="58320-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="58320-151">Ga naar **Magazijnbeheer \> Instellingen \> Waves \> Wave-sjablonen** en selecteer de wave-sjabloon die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="58320-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="58320-152">Selecteer in de sjabloon op het sneltabblad **Methoden** de methode **Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="58320-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="58320-153">Selecteer in het veld **Wave-stapcode** de wave-stapcode die u voor de aanvullingssjabloon hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="58320-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="58320-154">U voert deze stappen uit voor elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="58320-154">You perform these steps for each legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
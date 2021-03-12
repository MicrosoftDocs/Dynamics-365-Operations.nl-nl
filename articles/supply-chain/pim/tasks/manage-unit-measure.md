---
title: Maateenheid beheren
description: Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71b478ca294719c20af9de16c27139aeca36bf07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992290"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="bc3f3-103">Maateenheid beheren</span><span class="sxs-lookup"><span data-stu-id="bc3f3-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc3f3-104">Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="bc3f3-105">U kunt deze procedure doorlopen met demogegevens of uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="bc3f3-106">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven productonderhoud**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="bc3f3-107">Klik op **Eenheden**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="bc3f3-108">Een maateenheid maken</span><span class="sxs-lookup"><span data-stu-id="bc3f3-108">Create a unit of measure</span></span>
1. <span data-ttu-id="bc3f3-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-109">Click **New**.</span></span>
2. <span data-ttu-id="bc3f3-110">Typ een waarde in het veld **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="bc3f3-111">Voer de id of het symbool in dat moet worden gebruikt om te verwijzen naar de maateenheid.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="bc3f3-112">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="bc3f3-113">Voer een beschrijvende naam in voor de maateenheid in de systeemtaal.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="bc3f3-114">Selecteer een optie in het veld **Eenheidsklasse**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="bc3f3-115">De eenheidsklasse definieert van welke logische groepering, zoals oppervlakte, massa of hoeveelheid, de maateenheid deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="bc3f3-116">Voer een getal in het veld **Decimale precisie** in.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="bc3f3-117">Geef het aantal decimalen op waarop de omgerekende maateenheid wordt afgerond bij voltooiing van een berekening met de maateenheid.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="bc3f3-118">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="bc3f3-119">Eenheidsvertalingen definiëren</span><span class="sxs-lookup"><span data-stu-id="bc3f3-119">Define unit translations</span></span>
1. <span data-ttu-id="bc3f3-120">Ga naar het **actievenster** en klik op **Eenheidsteksten**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="bc3f3-121">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-121">Click **New**.</span></span> <span data-ttu-id="bc3f3-122">Gebruik eenheidstekst om een vertaling van de id of een symbool te maken waarmee de maateenheid wordt aangeduid voor gebruik op externe documenten in klant- of leverancierspecifieke talen.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="bc3f3-123">Typ of selecteer een waarde in het veld **Taal**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="bc3f3-124">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="bc3f3-125">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-125">Click **Save**.</span></span>
6. <span data-ttu-id="bc3f3-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-126">Close the page.</span></span>
7. <span data-ttu-id="bc3f3-127">Ga naar het **actievenster** en klik op **Vertaalde eenheidsbeschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="bc3f3-128">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-128">Click **New**.</span></span> <span data-ttu-id="bc3f3-129">Definieer taalspecifieke beschrijvingen voor de maateenheid.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="bc3f3-130">Typ of selecteer een waarde in het veld **Taal**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="bc3f3-131">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="bc3f3-132">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-132">Click **Save**.</span></span>
12. <span data-ttu-id="bc3f3-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="bc3f3-134">Regels voor eenheidsconversie definiëren</span><span class="sxs-lookup"><span data-stu-id="bc3f3-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="bc3f3-135">Ga naar het **actievenster** en klik op **Eenheidsconversies**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="bc3f3-136">Definieer regels om de maateenheid te converteren van en naar andere maateenheden in de geselecteerde eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="bc3f3-137">Klik op **Nieuw** om het uitklapdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="bc3f3-138">Voer een getal in het veld **Factor** in.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="bc3f3-139">Conversiefactor tussen Van eenheid en Naar eenheid.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="bc3f3-140">De omrekeningsfactor van centimeter naar meter is 100, aangezien er 100 centimeters in 1 meter gaan.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="bc3f3-141">Typ of selecteer een waarde in het veld **Naar eenheid**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="bc3f3-142">Selecteer een optie in het veld **Afronding**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="bc3f3-143">Definieer hoe de geconverteerde waarde moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="bc3f3-144">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-144">Click **OK**.</span></span>
7. <span data-ttu-id="bc3f3-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bc3f3-145">Close the page.</span></span>


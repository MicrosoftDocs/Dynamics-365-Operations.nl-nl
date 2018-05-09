--- 
title: Maateenheid beheren
description: "Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8524e006bbebe9600deb231f05d6df8fb3f33092
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="72340-103">Maateenheid beheren</span><span class="sxs-lookup"><span data-stu-id="72340-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72340-104">Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren.</span><span class="sxs-lookup"><span data-stu-id="72340-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="72340-105">U kunt deze procedure doorlopen met demogegevens of uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="72340-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="72340-106">Ga naar Vrijgegeven productonderhoud.</span><span class="sxs-lookup"><span data-stu-id="72340-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="72340-107">Klik op Eenheden.</span><span class="sxs-lookup"><span data-stu-id="72340-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="72340-108">Een maateenheid maken</span><span class="sxs-lookup"><span data-stu-id="72340-108">Create a unit of measure</span></span>
1. <span data-ttu-id="72340-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="72340-109">Click New.</span></span>
2. <span data-ttu-id="72340-110">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="72340-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="72340-111">Voer de id of het symbool in dat moet worden gebruikt om te verwijzen naar de maateenheid.</span><span class="sxs-lookup"><span data-stu-id="72340-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="72340-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="72340-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="72340-113">Voer een beschrijvende naam in voor de maateenheid in de systeemtaal.</span><span class="sxs-lookup"><span data-stu-id="72340-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="72340-114">Selecteer een optie in het veld Eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="72340-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="72340-115">De eenheidsklasse definieert van welke logische groepering, zoals oppervlakte, massa of hoeveelheid, de maateenheid deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="72340-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="72340-116">Voer een getal in het veld Decimale precisie in.</span><span class="sxs-lookup"><span data-stu-id="72340-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="72340-117">Geef het aantal decimalen op waarop de omgerekende maateenheid wordt afgerond bij voltooiing van een berekening met de maateenheid.</span><span class="sxs-lookup"><span data-stu-id="72340-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="72340-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="72340-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="72340-119">Eenheidsvertalingen definiëren</span><span class="sxs-lookup"><span data-stu-id="72340-119">Define unit translations</span></span>
1. <span data-ttu-id="72340-120">Klik op Eenheidsteksten.</span><span class="sxs-lookup"><span data-stu-id="72340-120">Click Unit texts.</span></span>
2. <span data-ttu-id="72340-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="72340-121">Click New.</span></span>
    * <span data-ttu-id="72340-122">Gebruik eenheidstekst om een vertaling van de id of een symbool te maken waarmee de maateenheid wordt aangeduid voor gebruik op externe documenten in klant- of leverancierspecifieke talen.</span><span class="sxs-lookup"><span data-stu-id="72340-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="72340-123">Typ of selecteer een waarde in het veld Waarde.</span><span class="sxs-lookup"><span data-stu-id="72340-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="72340-124">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="72340-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="72340-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="72340-125">Click Save.</span></span>
6. <span data-ttu-id="72340-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="72340-126">Close the page.</span></span>
7. <span data-ttu-id="72340-127">Klik op Omschrijvingen van vertaalde eenheden.</span><span class="sxs-lookup"><span data-stu-id="72340-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="72340-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="72340-128">Click New.</span></span>
    * <span data-ttu-id="72340-129">Definieer taalspecifieke beschrijvingen voor de maateenheid.</span><span class="sxs-lookup"><span data-stu-id="72340-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="72340-130">Typ of selecteer een waarde in het veld Waarde.</span><span class="sxs-lookup"><span data-stu-id="72340-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="72340-131">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="72340-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="72340-132">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="72340-132">Click Save.</span></span>
12. <span data-ttu-id="72340-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="72340-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="72340-134">Regels voor eenheidsconversie definiëren</span><span class="sxs-lookup"><span data-stu-id="72340-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="72340-135">Klik op Eenheidsconversies.</span><span class="sxs-lookup"><span data-stu-id="72340-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="72340-136">Definieer regels om de maateenheid te converteren van en naar andere maateenheden in de geselecteerde eenheidsklasse.</span><span class="sxs-lookup"><span data-stu-id="72340-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="72340-137">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="72340-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="72340-138">Voer een getal in het veld Factor in.</span><span class="sxs-lookup"><span data-stu-id="72340-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="72340-139">Conversiefactor tussen Van eenheid en Naar eenheid.</span><span class="sxs-lookup"><span data-stu-id="72340-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="72340-140">De omrekeningsfactor van centimeter naar meter is 100, aangezien er 100 centimeters in 1 meter gaan.</span><span class="sxs-lookup"><span data-stu-id="72340-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="72340-141">Typ of selecteer een waarde in het veld Naar eenheid.</span><span class="sxs-lookup"><span data-stu-id="72340-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="72340-142">Selecteer een optie in het veld Afronding.</span><span class="sxs-lookup"><span data-stu-id="72340-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="72340-143">Definieer hoe de geconverteerde waarde moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="72340-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="72340-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="72340-144">Click OK.</span></span>
7. <span data-ttu-id="72340-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="72340-145">Close the page.</span></span>



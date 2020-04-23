---
title: Vooraf gedefinieerde productvarianten maken
description: Deze procedure begeleidt u bij het maken van productvarianten voor een productmodel met behulp van de combinaties van productdimensies.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e35e0745a37aac3e833919eea7933015bbef45c8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203682"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="09d1b-103">Vooraf gedefinieerde productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="09d1b-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09d1b-104">Deze procedure begeleidt u bij het maken van productvarianten voor een productmodel met behulp van de combinaties van productdimensies.</span><span class="sxs-lookup"><span data-stu-id="09d1b-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="09d1b-105">Het demobedrijf dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="09d1b-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="09d1b-106">Een productmodel maken</span><span class="sxs-lookup"><span data-stu-id="09d1b-106">Create a product master</span></span>
1. <span data-ttu-id="09d1b-107">Ga naar Productgegevensbeheer > Producten > Productmodellen.</span><span class="sxs-lookup"><span data-stu-id="09d1b-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="09d1b-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="09d1b-108">Click New.</span></span>
3. <span data-ttu-id="09d1b-109">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="09d1b-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="09d1b-110">Handmatig invoeren van een productnummer is alleen verplicht als er geen nummerreeks is ingesteld voor het productnummerveld.</span><span class="sxs-lookup"><span data-stu-id="09d1b-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="09d1b-111">Met andere woorden: sla de stap over als een nummerreeks voor het veld is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="09d1b-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="09d1b-112">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="09d1b-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="09d1b-113">Typ of selecteer een waarde in het veld Productdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="09d1b-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="09d1b-114">Selecteer de productdimensiegroep SizeCol (Grootte en Kleur).</span><span class="sxs-lookup"><span data-stu-id="09d1b-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="09d1b-115">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="09d1b-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="09d1b-116">Productdimensies toevoegen</span><span class="sxs-lookup"><span data-stu-id="09d1b-116">Add product dimensions</span></span>
1. <span data-ttu-id="09d1b-117">Klik op Productdimensies.</span><span class="sxs-lookup"><span data-stu-id="09d1b-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="09d1b-118">Dit voorbeeld toont hoe productdimensies handmatig worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="09d1b-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="09d1b-119">U kunt er ook voor kiezen een grootte, kleur of een stijlgroep te selecteren die de productdimensiewaarden bevat die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="09d1b-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="09d1b-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="09d1b-120">Click New.</span></span>
3. <span data-ttu-id="09d1b-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="09d1b-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="09d1b-122">Typ of selecteer een waarde in het veld Grootte.</span><span class="sxs-lookup"><span data-stu-id="09d1b-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="09d1b-123">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="09d1b-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="09d1b-124">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="09d1b-124">Click New.</span></span>
7. <span data-ttu-id="09d1b-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="09d1b-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="09d1b-126">Typ of selecteer een waarde in het veld Grootte.</span><span class="sxs-lookup"><span data-stu-id="09d1b-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="09d1b-127">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="09d1b-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="09d1b-128">Klik op het tabblad Kleuren.</span><span class="sxs-lookup"><span data-stu-id="09d1b-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="09d1b-129">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="09d1b-129">Click New.</span></span>
12. <span data-ttu-id="09d1b-130">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="09d1b-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="09d1b-131">Typ of selecteer een waarde in het veld Kleur.</span><span class="sxs-lookup"><span data-stu-id="09d1b-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="09d1b-132">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="09d1b-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="09d1b-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="09d1b-133">Click New.</span></span>
16. <span data-ttu-id="09d1b-134">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="09d1b-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="09d1b-135">Typ of selecteer een waarde in het veld Kleur.</span><span class="sxs-lookup"><span data-stu-id="09d1b-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="09d1b-136">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="09d1b-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="09d1b-137">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="09d1b-137">Click Save.</span></span>
20. <span data-ttu-id="09d1b-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="09d1b-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="09d1b-139">Productvarianten genereren</span><span class="sxs-lookup"><span data-stu-id="09d1b-139">Generate product variants</span></span>
1. <span data-ttu-id="09d1b-140">Klik op Productvarianten.</span><span class="sxs-lookup"><span data-stu-id="09d1b-140">Click Product variants.</span></span>
2. <span data-ttu-id="09d1b-141">Klik op Variantsuggesties.</span><span class="sxs-lookup"><span data-stu-id="09d1b-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="09d1b-142">Klik op Alles selecteren.</span><span class="sxs-lookup"><span data-stu-id="09d1b-142">Click Select all.</span></span>
    * <span data-ttu-id="09d1b-143">In dit voorbeeld worden alle mogelijke varianten geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="09d1b-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="09d1b-144">Als alleen een subset van de mogelijke productdimensiecombinaties wordt gebruikt om varianten te maken, kunt u de afzonderlijke items selecteren.</span><span class="sxs-lookup"><span data-stu-id="09d1b-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="09d1b-145">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="09d1b-145">Click Create.</span></span>
    * <span data-ttu-id="09d1b-146">U kunt omschrijvingen voor al uw varianten genereren op basis van de combinatie van productdimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="09d1b-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="09d1b-147">De omschrijvingen zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="09d1b-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="09d1b-148">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="09d1b-148">Click Save.</span></span>


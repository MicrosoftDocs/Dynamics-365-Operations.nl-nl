--- 
title: Een route voor een productmodel onderhouden
description: Het uitvoeren van deze procedure vereist dat er een productconfiguratiemodel is.
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 3f6bacc54664c32a7d42f2befc51c420e29ada56
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="2321c-103">Een route voor een productmodel onderhouden</span><span class="sxs-lookup"><span data-stu-id="2321c-103">Maintain a route for a product model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2321c-104">Het uitvoeren van deze procedure vereist dat er een productconfiguratiemodel is.</span><span class="sxs-lookup"><span data-stu-id="2321c-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="2321c-105">Deze procedure gebruikt het model Geavanceerde luidspreker in het demobedrijf USMF om u door het proces te begeleiden.</span><span class="sxs-lookup"><span data-stu-id="2321c-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="2321c-106">Een routebewerking toevoegen</span><span class="sxs-lookup"><span data-stu-id="2321c-106">Add a route operation</span></span>
1. <span data-ttu-id="2321c-107">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="2321c-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="2321c-108">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="2321c-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="2321c-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="2321c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2321c-110">Selecteer het model Geavanceerde luidspreker voor deze oefening.</span><span class="sxs-lookup"><span data-stu-id="2321c-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="2321c-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2321c-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2321c-112">Vouw de sectie Routebewerkingen uit.</span><span class="sxs-lookup"><span data-stu-id="2321c-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="2321c-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2321c-113">Click Add.</span></span>
7. <span data-ttu-id="2321c-114">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="2321c-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="2321c-115">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="2321c-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="2321c-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="2321c-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="2321c-117">Routebewerkingsdetails opgeven</span><span class="sxs-lookup"><span data-stu-id="2321c-117">Enter route operation details</span></span>
1. <span data-ttu-id="2321c-118">Klik op Routebewerkingsdetails.</span><span class="sxs-lookup"><span data-stu-id="2321c-118">Click Route operation details.</span></span>
2. <span data-ttu-id="2321c-119">Typ of selecteer een waarde in het veld Bewerking.</span><span class="sxs-lookup"><span data-stu-id="2321c-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="2321c-120">Voer in het veld Bewerkingsnummer</span><span class="sxs-lookup"><span data-stu-id="2321c-120">In the Oper.</span></span> <span data-ttu-id="2321c-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="2321c-121">No.</span></span> <span data-ttu-id="2321c-122">een getal in.</span><span class="sxs-lookup"><span data-stu-id="2321c-122">field, enter a number.</span></span>
    * <span data-ttu-id="2321c-123">Bewerkingsnummers bepalen de routevolgorde.</span><span class="sxs-lookup"><span data-stu-id="2321c-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="2321c-124">Elke eigenschap voor een routebewerking kan een statische waarde krijgen of aan een kenmerk worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="2321c-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="2321c-125">De toewijzing aan een kenmerk zorgt ervoor dat de waarde wordt ingesteld als onderdeel van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="2321c-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="2321c-126">Typ of selecteer een waarde in het veld Routegroep.</span><span class="sxs-lookup"><span data-stu-id="2321c-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="2321c-127">De routegroep bepaalt essentieel gedrag voor kostprijsberekening, verbruik en instelling.</span><span class="sxs-lookup"><span data-stu-id="2321c-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="2321c-128">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="2321c-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="2321c-129">Klik op het tabblad Tijden.</span><span class="sxs-lookup"><span data-stu-id="2321c-129">Click the Times tab.</span></span>
7. <span data-ttu-id="2321c-130">Voer in het veld Verwerkingshoeveelheid</span><span class="sxs-lookup"><span data-stu-id="2321c-130">In the Process qty.</span></span> <span data-ttu-id="2321c-131">een getal in.</span><span class="sxs-lookup"><span data-stu-id="2321c-131">field, enter a number.</span></span>
    * <span data-ttu-id="2321c-132">Bepaal hoeveel in één bewerking wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="2321c-132">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="2321c-133">Voer in het veld Uren/tijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="2321c-133">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="2321c-134">Geef de duurverhouding op.</span><span class="sxs-lookup"><span data-stu-id="2321c-134">Enter the time ratio.</span></span>  
9. <span data-ttu-id="2321c-135">Schakel het selectievakje Instellen in.</span><span class="sxs-lookup"><span data-stu-id="2321c-135">Select the Set check box.</span></span>
10. <span data-ttu-id="2321c-136">Voer een getal in het veld Uitvoeringstijd in.</span><span class="sxs-lookup"><span data-stu-id="2321c-136">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="2321c-137">Bepaal de verwerkingstijd voor de hoeveelheid die u hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="2321c-137">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="2321c-138">Klik op het tabblad Bronbehoeften.</span><span class="sxs-lookup"><span data-stu-id="2321c-138">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="2321c-139">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2321c-139">Click Add.</span></span>
13. <span data-ttu-id="2321c-140">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2321c-140">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="2321c-141">Selecteer een optie in het veld Vereiste.</span><span class="sxs-lookup"><span data-stu-id="2321c-141">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="2321c-142">Bepaal of u specifieke bronnen of capaciteiten wilt opgeven die ze moet bezitten.</span><span class="sxs-lookup"><span data-stu-id="2321c-142">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="2321c-143">Typ of selecteer een waarde in het veld Vereiste.</span><span class="sxs-lookup"><span data-stu-id="2321c-143">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="2321c-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2321c-144">Click OK.</span></span>



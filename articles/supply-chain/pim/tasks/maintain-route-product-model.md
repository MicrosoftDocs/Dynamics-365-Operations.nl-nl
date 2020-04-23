---
title: Route voor een productmodel onderhouden
description: Het uitvoeren van deze procedure vereist dat er een productconfiguratiemodel is.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24419cb9bad4b4344fe23789750387de6cca3796
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203507"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="e754c-103">Route voor een productmodel onderhouden</span><span class="sxs-lookup"><span data-stu-id="e754c-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e754c-104">Het uitvoeren van deze procedure vereist dat er een productconfiguratiemodel is.</span><span class="sxs-lookup"><span data-stu-id="e754c-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="e754c-105">Deze procedure gebruikt het model Geavanceerde luidspreker in het demobedrijf USMF om u door het proces te begeleiden.</span><span class="sxs-lookup"><span data-stu-id="e754c-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="e754c-106">Een routebewerking toevoegen</span><span class="sxs-lookup"><span data-stu-id="e754c-106">Add a route operation</span></span>
1. <span data-ttu-id="e754c-107">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="e754c-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e754c-108">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="e754c-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="e754c-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e754c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e754c-110">Selecteer het model Geavanceerde luidspreker voor deze oefening.</span><span class="sxs-lookup"><span data-stu-id="e754c-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="e754c-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e754c-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e754c-112">Vouw de sectie Routebewerkingen uit.</span><span class="sxs-lookup"><span data-stu-id="e754c-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="e754c-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e754c-113">Click Add.</span></span>
7. <span data-ttu-id="e754c-114">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e754c-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="e754c-115">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="e754c-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="e754c-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e754c-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="e754c-117">Routebewerkingsdetails opgeven</span><span class="sxs-lookup"><span data-stu-id="e754c-117">Enter route operation details</span></span>
1. <span data-ttu-id="e754c-118">Klik op Routebewerkingsdetails.</span><span class="sxs-lookup"><span data-stu-id="e754c-118">Click Route operation details.</span></span>
2. <span data-ttu-id="e754c-119">Typ of selecteer een waarde in het veld Bewerking.</span><span class="sxs-lookup"><span data-stu-id="e754c-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="e754c-120">Voer in het veld Bewerkingsnummer</span><span class="sxs-lookup"><span data-stu-id="e754c-120">In the Oper.</span></span> <span data-ttu-id="e754c-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="e754c-121">No.</span></span> <span data-ttu-id="e754c-122">een getal in.</span><span class="sxs-lookup"><span data-stu-id="e754c-122">field, enter a number.</span></span>
    * <span data-ttu-id="e754c-123">Bewerkingsnummers bepalen de routevolgorde.</span><span class="sxs-lookup"><span data-stu-id="e754c-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="e754c-124">Elke eigenschap voor een routebewerking kan een statische waarde krijgen of aan een kenmerk worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e754c-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="e754c-125">De toewijzing aan een kenmerk zorgt ervoor dat de waarde wordt ingesteld als onderdeel van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="e754c-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="e754c-126">Typ of selecteer een waarde in het veld Routegroep.</span><span class="sxs-lookup"><span data-stu-id="e754c-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="e754c-127">De routegroep bepaalt essentieel gedrag voor kostprijsberekening, verbruik en instelling.</span><span class="sxs-lookup"><span data-stu-id="e754c-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="e754c-128">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="e754c-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="e754c-129">Klik op het tabblad Tijden.</span><span class="sxs-lookup"><span data-stu-id="e754c-129">Click the Times tab.</span></span>
7. <span data-ttu-id="e754c-130">Voer in het veld Verwerkingshoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="e754c-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="e754c-131">Bepaal hoeveel in één bewerking wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e754c-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="e754c-132">Voer in het veld Uren/tijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="e754c-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="e754c-133">Geef de duurverhouding op.</span><span class="sxs-lookup"><span data-stu-id="e754c-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="e754c-134">Schakel het selectievakje Instellen in.</span><span class="sxs-lookup"><span data-stu-id="e754c-134">Select the Set check box.</span></span>
10. <span data-ttu-id="e754c-135">Voer een getal in het veld Uitvoeringstijd in.</span><span class="sxs-lookup"><span data-stu-id="e754c-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="e754c-136">Bepaal de verwerkingstijd voor de hoeveelheid die u hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e754c-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="e754c-137">Klik op het tabblad Bronbehoeften.</span><span class="sxs-lookup"><span data-stu-id="e754c-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="e754c-138">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e754c-138">Click Add.</span></span>
13. <span data-ttu-id="e754c-139">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e754c-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e754c-140">Selecteer een optie in het veld Vereiste.</span><span class="sxs-lookup"><span data-stu-id="e754c-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="e754c-141">Bepaal of u specifieke bronnen of capaciteiten wilt opgeven die ze moet bezitten.</span><span class="sxs-lookup"><span data-stu-id="e754c-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="e754c-142">Typ of selecteer een waarde in het veld Vereiste.</span><span class="sxs-lookup"><span data-stu-id="e754c-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="e754c-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e754c-143">Click OK.</span></span>


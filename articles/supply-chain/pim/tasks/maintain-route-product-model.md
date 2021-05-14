---
title: Route voor een productmodel onderhouden
description: Het uitvoeren van deze procedure vereist dat er een productconfiguratiemodel is.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921260"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="419ab-103">Route voor een productmodel onderhouden</span><span class="sxs-lookup"><span data-stu-id="419ab-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="419ab-104">Het uitvoeren van deze procedure vereist dat er een productconfiguratiemodel is.</span><span class="sxs-lookup"><span data-stu-id="419ab-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="419ab-105">Deze procedure gebruikt het model Geavanceerde luidspreker in het demobedrijf USMF om u door het proces te begeleiden.</span><span class="sxs-lookup"><span data-stu-id="419ab-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="419ab-106">Een routebewerking toevoegen</span><span class="sxs-lookup"><span data-stu-id="419ab-106">Add a route operation</span></span>

1. <span data-ttu-id="419ab-107">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="419ab-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="419ab-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="419ab-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="419ab-109">Selecteer het model Geavanceerde luidspreker voor deze oefening.</span><span class="sxs-lookup"><span data-stu-id="419ab-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="419ab-110">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="419ab-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="419ab-111">Vouw de sectie **Routebewerkingen** uit.</span><span class="sxs-lookup"><span data-stu-id="419ab-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="419ab-112">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="419ab-112">Select **Add**.</span></span>
1. <span data-ttu-id="419ab-113">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="419ab-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="419ab-114">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="419ab-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="419ab-115">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="419ab-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="419ab-116">Routebewerkingsdetails opgeven</span><span class="sxs-lookup"><span data-stu-id="419ab-116">Enter route operation details</span></span>

1. <span data-ttu-id="419ab-117">Klik op **Routebewerkingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="419ab-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="419ab-118">Typ of selecteer een waarde in het veld **Bewerking**.</span><span class="sxs-lookup"><span data-stu-id="419ab-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="419ab-119">Voer in het veld **Bewerkingsnummer**</span><span class="sxs-lookup"><span data-stu-id="419ab-119">In the **Oper. No.**</span></span> <span data-ttu-id="419ab-120">een getal in.</span><span class="sxs-lookup"><span data-stu-id="419ab-120">field, enter a number.</span></span>
    * <span data-ttu-id="419ab-121">Bewerkingsnummers bepalen de routevolgorde.</span><span class="sxs-lookup"><span data-stu-id="419ab-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="419ab-122">Elke eigenschap voor een routebewerking kan een statische waarde krijgen of aan een kenmerk worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="419ab-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="419ab-123">De toewijzing aan een kenmerk zorgt ervoor dat de waarde wordt ingesteld als onderdeel van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="419ab-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="419ab-124">Typ of selecteer een waarde in het veld **Routegroep**.</span><span class="sxs-lookup"><span data-stu-id="419ab-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="419ab-125">De routegroep bepaalt essentieel gedrag voor kostprijsberekening, verbruik en instelling.</span><span class="sxs-lookup"><span data-stu-id="419ab-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="419ab-126">Selecteer het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="419ab-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="419ab-127">Selecteer het tabblad **Tijden**.</span><span class="sxs-lookup"><span data-stu-id="419ab-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="419ab-128">Voer in het veld **Verwerkingshoeveelheid** een getal in.</span><span class="sxs-lookup"><span data-stu-id="419ab-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="419ab-129">Bepaal hoeveel in één bewerking wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="419ab-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="419ab-130">Voer in het veld **Uren/tijd** een getal in.</span><span class="sxs-lookup"><span data-stu-id="419ab-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="419ab-131">Geef de duurverhouding op.</span><span class="sxs-lookup"><span data-stu-id="419ab-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="419ab-132">Schakel het selectievakje **Instellen** in.</span><span class="sxs-lookup"><span data-stu-id="419ab-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="419ab-133">Voer een getal in het veld **Uitvoeringstijd** in.</span><span class="sxs-lookup"><span data-stu-id="419ab-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="419ab-134">Bepaal de verwerkingstijd voor de hoeveelheid die u hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="419ab-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="419ab-135">Selecteer het tabblad **Resourcevereisten**.</span><span class="sxs-lookup"><span data-stu-id="419ab-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="419ab-136">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="419ab-136">Select **Add**.</span></span>
1. <span data-ttu-id="419ab-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="419ab-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="419ab-138">Selecteer een optie in het veld **Type behoefte**.</span><span class="sxs-lookup"><span data-stu-id="419ab-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="419ab-139">Bepaal of u specifieke bronnen of capaciteiten wilt opgeven die ze moet bezitten.</span><span class="sxs-lookup"><span data-stu-id="419ab-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="419ab-140">Typ of selecteer een waarde in het veld **Behoefte**.</span><span class="sxs-lookup"><span data-stu-id="419ab-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="419ab-141">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="419ab-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
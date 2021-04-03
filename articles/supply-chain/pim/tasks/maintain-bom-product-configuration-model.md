---
title: Stuklijst voor een productconfiguratiemodel onderhouden
description: Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12eb2d8fcdae5d60efa19e5443a01ab9bd104267
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258798"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="6a74e-103">Stuklijst voor een productconfiguratiemodel onderhouden</span><span class="sxs-lookup"><span data-stu-id="6a74e-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a74e-104">Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="6a74e-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="6a74e-105">Het model Geavanceerde luidspreker in het demobedrijf USMF wordt gebruikt voor het maken van deze procedure.</span><span class="sxs-lookup"><span data-stu-id="6a74e-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="6a74e-106">Een stuklijstregel toevoegen</span><span class="sxs-lookup"><span data-stu-id="6a74e-106">Add a BOM line</span></span>
1. <span data-ttu-id="6a74e-107">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="6a74e-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="6a74e-108">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="6a74e-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="6a74e-109">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6a74e-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6a74e-110">Selecteer de Geavanceerde luidspreker voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="6a74e-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="6a74e-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6a74e-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6a74e-112">Vouw de sectie Stuklijstregels uit.</span><span class="sxs-lookup"><span data-stu-id="6a74e-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="6a74e-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6a74e-113">Click Add.</span></span>
7. <span data-ttu-id="6a74e-114">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6a74e-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="6a74e-115">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="6a74e-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="6a74e-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6a74e-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="6a74e-117">Regeldetails van stuklijst toevoegen</span><span class="sxs-lookup"><span data-stu-id="6a74e-117">Add BOM line details</span></span>
1. <span data-ttu-id="6a74e-118">Klik op Regeldetails van stuklijst.</span><span class="sxs-lookup"><span data-stu-id="6a74e-118">Click BOM line details.</span></span>
2. <span data-ttu-id="6a74e-119">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="6a74e-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6a74e-120">Zo kunt u bijvoorbeeld het artikel M0055 selecteren.</span><span class="sxs-lookup"><span data-stu-id="6a74e-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="6a74e-121">Voor elke regeleigenschap van de stuklijst kunt u selecteren of deze een vaste waarde heeft of aan een kenmerk is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="6a74e-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="6a74e-122">Schakel het selectievakje Instellen in.</span><span class="sxs-lookup"><span data-stu-id="6a74e-122">Select the Set check box.</span></span>
4. <span data-ttu-id="6a74e-123">Selecteer Ja in het veld Berekening.</span><span class="sxs-lookup"><span data-stu-id="6a74e-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="6a74e-124">Het instellen van de eigenschap Berekening op Ja zorgt ervoor dat de stuklijstregel in kostenberekeningen wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="6a74e-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="6a74e-125">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="6a74e-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="6a74e-126">Schakel het selectievakje Instellen in.</span><span class="sxs-lookup"><span data-stu-id="6a74e-126">Select the Set check box.</span></span>
7. <span data-ttu-id="6a74e-127">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="6a74e-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6a74e-128">Het hoeveelheidsveld bepaalt hoeveel van het artikel in de stuklijst wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="6a74e-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="6a74e-129">Dit moet een duidelijke kandidaat zijn voor een kenmerktoewijzing.</span><span class="sxs-lookup"><span data-stu-id="6a74e-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="6a74e-130">Klik op het tabblad Dimensies.</span><span class="sxs-lookup"><span data-stu-id="6a74e-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="6a74e-131">Controleer of een van de productdimensies actief is en daardoor een waarde of kenmerk moeten toegewezen krijgen.</span><span class="sxs-lookup"><span data-stu-id="6a74e-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="6a74e-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6a74e-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Stuklijst voor een productconfiguratiemodel onderhouden
description: Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921312"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="16039-103">Stuklijst voor een productconfiguratiemodel onderhouden</span><span class="sxs-lookup"><span data-stu-id="16039-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16039-104">Het uitvoeren van deze procedure vereist een bestaand productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="16039-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="16039-105">Het model Geavanceerde luidspreker in het demobedrijf USMF wordt gebruikt voor het maken van deze procedure.</span><span class="sxs-lookup"><span data-stu-id="16039-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="16039-106">Een stuklijstregel toevoegen</span><span class="sxs-lookup"><span data-stu-id="16039-106">Add a BOM line</span></span>

1. <span data-ttu-id="16039-107">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="16039-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="16039-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="16039-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="16039-109">Selecteer de Geavanceerde luidspreker voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="16039-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="16039-110">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="16039-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="16039-111">Vouw de sectie **Stuklijstregels** uit.</span><span class="sxs-lookup"><span data-stu-id="16039-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="16039-112">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="16039-112">Select **Add**.</span></span>
1. <span data-ttu-id="16039-113">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="16039-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="16039-114">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="16039-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="16039-115">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="16039-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="16039-116">Regeldetails van stuklijst toevoegen</span><span class="sxs-lookup"><span data-stu-id="16039-116">Add BOM line details</span></span>

1. <span data-ttu-id="16039-117">Selecteer **Details van stuklijstregel**.</span><span class="sxs-lookup"><span data-stu-id="16039-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="16039-118">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="16039-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="16039-119">Zo kunt u bijvoorbeeld het artikel M0055 selecteren.</span><span class="sxs-lookup"><span data-stu-id="16039-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="16039-120">Voor elke regeleigenschap van de stuklijst kunt u selecteren of deze een vaste waarde heeft of aan een kenmerk is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="16039-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="16039-121">Schakel het selectievakje **Instellen** in.</span><span class="sxs-lookup"><span data-stu-id="16039-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="16039-122">Selecteer *Ja* in het veld **Berekening**.</span><span class="sxs-lookup"><span data-stu-id="16039-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="16039-123">Als u de eigenschap **Berekening** instelt op *Ja*, wordt de stuklijstregel in kostenberekeningen opgenomen.</span><span class="sxs-lookup"><span data-stu-id="16039-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="16039-124">Selecteer het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="16039-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="16039-125">Schakel het selectievakje **Instellen** in.</span><span class="sxs-lookup"><span data-stu-id="16039-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="16039-126">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="16039-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="16039-127">Het hoeveelheidsveld bepaalt hoeveel van het artikel in de stuklijst wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="16039-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="16039-128">Dit moet een duidelijke kandidaat zijn voor een kenmerktoewijzing.</span><span class="sxs-lookup"><span data-stu-id="16039-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="16039-129">Selecteer het tabblad **Dimensie**.</span><span class="sxs-lookup"><span data-stu-id="16039-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="16039-130">Controleer of een van de productdimensies actief is en daardoor een waarde of kenmerk moeten toegewezen krijgen.</span><span class="sxs-lookup"><span data-stu-id="16039-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="16039-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="16039-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
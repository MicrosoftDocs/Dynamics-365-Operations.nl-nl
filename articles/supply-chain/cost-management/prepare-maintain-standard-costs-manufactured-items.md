---
title: Voorbereiding van het onderhoud van standaardkosten voor gefabriceerde artikelen
description: Dit onderwerp beschrijft de stappen voor het voorbereiden van het beheer van kosten voor gefabriceerde artikelen.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbd7344f3d542cbd46e3568d8a7911ab4ab53b17
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "350614"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="d2c42-103">Voorbereiding van het onderhoud van standaardkosten voor gefabriceerde artikelen</span><span class="sxs-lookup"><span data-stu-id="d2c42-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2c42-104">Dit onderwerp beschrijft de stappen voor het voorbereiden van het beheer van kosten voor gefabriceerde artikelen.</span><span class="sxs-lookup"><span data-stu-id="d2c42-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="d2c42-105">De stappen voor gefabriceerde artikelen verschillen enigszins van de stappen voor ingekochte artikelen.</span><span class="sxs-lookup"><span data-stu-id="d2c42-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="d2c42-106">Beleidsregels die aan gefabriceerde artikelen zijn toegewezen, kunnen gevolgen hebben voor de kostprijsberekeningen voor de bovenliggende gefabriceerde artikelen.</span><span class="sxs-lookup"><span data-stu-id="d2c42-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="d2c42-107">Voer de volgende stappen uit om kosten voor gefabriceerde artikelen te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="d2c42-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="d2c42-108">Wijs een artikelmodelgroep toe aan het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="d2c42-109">Met de artikelmodelgroep wordt aangegeven dat standaardkosten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d2c42-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="d2c42-110">Wijs een artikelgroep toe aan het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="d2c42-111">De artikelgroep bevat grootboekrekeningen die van toepassing zijn op het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="d2c42-112">De grootboekrekeningen voor een gefabriceerd artikel dat een standaardkostenvoorraadmodel heeft, omvatten verschillende productieafwijkingen, de kostenwijzigingsafwijking en de herwaardering van de voorraadkosten.</span><span class="sxs-lookup"><span data-stu-id="d2c42-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="d2c42-113">Wijs de voorraadmaateenheid toe aan het artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="d2c42-114">De kosten van het artikel worden altijd uitgedrukt in de voorraadmaateenheid van het artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="d2c42-115">Wijs geen kostengroep aan het gefabriceerde artikel toe, tenzij het artikel als ingekocht artikel wordt beschouwd.</span><span class="sxs-lookup"><span data-stu-id="d2c42-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="d2c42-116">Wijs een stuklijstberekeningsgroep toe aan het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="d2c42-117">De stuklijstberekeningsgroep van het artikel definieert waarschuwingsvoorwaarden die van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="d2c42-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="d2c42-118">Op die manier kunnen, wanneer een stuklijstberekening wordt uitgevoerd, waarschuwingsberichten worden gegenereerd over mogelijke oorzaken van berekeningsfouten.</span><span class="sxs-lookup"><span data-stu-id="d2c42-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="d2c42-119">Een waarschuwingsbericht kan bijvoorbeeld aangeven wanneer er geen actieve stuklijst of route bestaat.</span><span class="sxs-lookup"><span data-stu-id="d2c42-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="d2c42-120">De stuklijstberekeningsgroep bevat een beleid voor het stoppen van een explosie, dat aangeeft wanneer een gefabriceerd artikel als ingekocht artikel moet worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="d2c42-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="d2c42-121">Als het gefabriceerde artikel constante kosten heeft, wijst u er een standaardorderhoeveelheid aan toe.</span><span class="sxs-lookup"><span data-stu-id="d2c42-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="d2c42-122">De standaardorderhoeveelheid is een boekhoudpartijgrootte voor het afschrijven van constante kosten.</span><span class="sxs-lookup"><span data-stu-id="d2c42-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="d2c42-123">Voorbeelden van constante kosten zijn instellingstijden in routebewerkingen en een constante onderdeelhoeveelheid in de stuklijst.</span><span class="sxs-lookup"><span data-stu-id="d2c42-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="d2c42-124">Definieer de stuklijst voor het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="d2c42-125">Er kunnen een of meer stuklijstversies worden gedefinieerd voor het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="d2c42-126">Verifieer dat de gewenste versies zijn gemarkeerd als goedgekeurd en actief, en dat ze de gewenste ingangsdatums hebben.</span><span class="sxs-lookup"><span data-stu-id="d2c42-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="d2c42-127">De stuklijstversie kan het hele bedrijf of een specifieke locatie beslaan.</span><span class="sxs-lookup"><span data-stu-id="d2c42-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="d2c42-128">Definieer de route voor het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="d2c42-129">Er kunnen een of meer routeversies worden gedefinieerd voor het gefabriceerde artikel.</span><span class="sxs-lookup"><span data-stu-id="d2c42-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="d2c42-130">Verifieer dat de gewenste versies zijn gemarkeerd als goedgekeurd en actief, en dat ze de gewenste ingangsdatums hebben.</span><span class="sxs-lookup"><span data-stu-id="d2c42-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="d2c42-131">De routeversie moet locatiespecifiek zijn.</span><span class="sxs-lookup"><span data-stu-id="d2c42-131">The route version must be site-specific.</span></span>

<span data-ttu-id="d2c42-132">Als u routegegevens wilt gebruiken voor kostprijsberekening, zijn er extra voorbereidende stappen vereist.</span><span class="sxs-lookup"><span data-stu-id="d2c42-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="d2c42-133">Zo moeten de kostencategorieën die aan routebewerkingen zijn toegewezen, juist en volledig zijn.</span><span class="sxs-lookup"><span data-stu-id="d2c42-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="d2c42-134">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="d2c42-134">Related topics</span></span>
--------

[<span data-ttu-id="d2c42-135">Constante kosten voor een gefabriceerd artikel afschrijven</span><span class="sxs-lookup"><span data-stu-id="d2c42-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="d2c42-136">Producten instellen die kunnen worden geproduceerd of kunnen worden aangeschaft</span><span class="sxs-lookup"><span data-stu-id="d2c42-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)


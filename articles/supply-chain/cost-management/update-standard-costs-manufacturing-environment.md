---
title: Standaardkosten in een productieomgeving bijwerken
description: Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een productieomgeving.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: a381f68e58fd6c2c567125482b72592aa40df636
ms.contentlocale: nl-nl
ms.lasthandoff: 10/13/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="87cd5-103">Standaardkosten in een productieomgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="87cd5-103">Update standard costs in a manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="87cd5-104">Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een productieomgeving.</span><span class="sxs-lookup"><span data-stu-id="87cd5-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="87cd5-105">Updates kunnen nieuwe artikelen, kostencategorieën of berekeningsformules voor indirecte kosten reflecteren.</span><span class="sxs-lookup"><span data-stu-id="87cd5-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="87cd5-106">Ze kunnen ook correcties en wijzigingen in kosten aangeven.</span><span class="sxs-lookup"><span data-stu-id="87cd5-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="87cd5-107">Het type update bepaalt welke stappen u moet uitvoeren om standaardkosten bij te werken, zoals in de volgende gevallen wordt geïllustreerd:</span><span class="sxs-lookup"><span data-stu-id="87cd5-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="87cd5-108">Voer verwachte wijzigingen in standaardkosten voor ingekochte artikelen in en wijzig vervolgens de status van de artikelkostprijsregistraties naar **Actief** op de toepasselijke datum.</span><span class="sxs-lookup"><span data-stu-id="87cd5-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="87cd5-109">Bereken echter niet opnieuw de kosten van gefabriceerde artikelen die de ingekochte artikelen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="87cd5-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="87cd5-110">Voer standaardkosten voor een nieuw, ingekocht artikel in, maar bereken niet opnieuw de kosten van gefabriceerde artikelen die een stuklijstversie hebben die het nieuwe ingekochte artikel als onderdeel bevat.</span><span class="sxs-lookup"><span data-stu-id="87cd5-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="87cd5-111">Corrigeer of wijzig de kosten van een ingekocht artikel, of wijzig de kostengroep die aan een ingekocht artikel is toegewezen, en bereken de kosten voor alle gefabriceerde artikelen die een stuklijstversie hebben die het ingekochte artikel als onderdeel bevat.</span><span class="sxs-lookup"><span data-stu-id="87cd5-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="87cd5-112">Wijzig de kosten voor een kostencategorie, en bereken de kosten voor alle gefabriceerde artikelen die een routeversie hebben die routebewerkingen bevat die de kostencategorie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="87cd5-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="87cd5-113">Wijzig de kostencategorieën die zijn toegewezen aan routing-bewerkingen of de kostengroep die aan de kostencategorieën toegewezen is.</span><span class="sxs-lookup"><span data-stu-id="87cd5-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="87cd5-114">Bereken vervolgens de kosten voor alle gefabriceerde artikelen die een routeversie hebben die routebewerkingen bevat die de kostencategorie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="87cd5-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="87cd5-115">Wijzig een berekeningsformule voor indirecte kosten, en bereken de kosten voor alle gefabriceerde artikelen waarvoor de wijziging gevolgen heeft.</span><span class="sxs-lookup"><span data-stu-id="87cd5-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="87cd5-116">Wijzig een productiesite voor een gefabriceerd artikel of voeg een site toe, en bereken de productiekosten van het artikel voor de site.</span><span class="sxs-lookup"><span data-stu-id="87cd5-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="87cd5-117">Bereken de kosten voor een gefabriceerd artikel (opnieuw), en herbereken de kosten voor alle gefabriceerde artikelen die een stuklijstversie hebben die het gefabriceerde artikel als onderdeel bevat.</span><span class="sxs-lookup"><span data-stu-id="87cd5-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="87cd5-118">Bereken kosten voor een nieuw gefabriceerd artikel op basis van de gedefinieerde, goedgekeurde en actieve stuklijst- en route-informatie.</span><span class="sxs-lookup"><span data-stu-id="87cd5-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="87cd5-119">In alle gevallen dient u nauwkeurig te overwegen hoe de standaardkosten moeten worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="87cd5-119">Each case requires careful consideration about how to update standard costs.</span></span>





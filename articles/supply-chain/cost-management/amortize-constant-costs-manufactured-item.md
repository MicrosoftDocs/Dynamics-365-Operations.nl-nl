---
title: Constante kosten voor een gefabriceerd artikel afschrijven
description: De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: AndersGirke
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 5a8c08b97f6500ea8de22fed28e790b6f9a1b3db
ms.contentlocale: nl-nl
ms.lasthandoff: 10/13/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="ef68a-103">Constante kosten voor een gefabriceerd artikel afschrijven</span><span class="sxs-lookup"><span data-stu-id="ef68a-103">Amortize constant costs for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef68a-104">De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben.</span><span class="sxs-lookup"><span data-stu-id="ef68a-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="ef68a-105">Het concept van de partijgrootte voor kostprijsberekening wordt gebruikt om deze constante kosten af te schrijven via de berekende kosten van een gefabriceerd artikel.</span><span class="sxs-lookup"><span data-stu-id="ef68a-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="ef68a-106">Dit concept heeft verschillende synoniemen, waaronder partijgrootte voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="ef68a-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="ef68a-107">Het concept van het afschrijven van constante kosten heeft ook verschillende synoniemen, waaronder proportionele constante kosten.</span><span class="sxs-lookup"><span data-stu-id="ef68a-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="ef68a-108">De hoeveelheid van de partijgrootte voor kostprijsberekening wordt gebruikt in een stuklijstberekening.</span><span class="sxs-lookup"><span data-stu-id="ef68a-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="ef68a-109">De hoeveelheid is afhankelijk van de manier waarop u de stuklijstberekening initieert en uitvoert, zoals wordt geïllustreerd door het volgende:</span><span class="sxs-lookup"><span data-stu-id="ef68a-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="ef68a-110">Standaardberekeningshoeveelheid in stuklijstberekening van een artikel - De standaardorderhoeveelheid voor voorraad van het artikel fungeert als partijgrootte voor boekhouding, maar de standaardwaarde kan een grotere hoeveelheid zijn om het veelvoud van de orderhoeveelheid van het artikel aan te geven.</span><span class="sxs-lookup"><span data-stu-id="ef68a-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="ef68a-111">De standaardorderhoeveelheid en veelvoud van het artikel kunnen in de standaardorderinstellingen of locatiespecifieke orderinstellingen worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="ef68a-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="ef68a-112">Opgegeven berekeningshoeveelheid in de stuklijstberekening van een artikel - De opgegeven berekeningshoeveelheid dient als de partijgrootte voor kostprijsberekening voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="ef68a-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="ef68a-113">De berekeningshoeveelheid gebruikt de standaardorderhoeveelheid van het artikel, maar de standaardwaarde kan handmatig worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="ef68a-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="ef68a-114">De opgegeven berekeningshoeveelheid representeert de partijgrootte voor kostprijsberekening voor het opgegeven artikel en voor gefabriceerde onderdelen met het stuklijstregeltype Productie.</span><span class="sxs-lookup"><span data-stu-id="ef68a-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="ef68a-115">Dat komt omdat ervan wordt uitgegaan dat het onderdeel wordt gefabriceerd in de exacte hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="ef68a-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="ef68a-116">De partijgrootte voor kostprijsberekening voor andere gefabriceerde onderdelen met het stuklijstregeltype Artikel geeft de standaardorderhoeveelheid weer.</span><span class="sxs-lookup"><span data-stu-id="ef68a-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="ef68a-117">Opgegeven Maken naar order-berekeningshoeveelheid in de stuklijstberekening van een artikel - De opgegeven berekeningshoeveelheid dient als de partijgrootte voor kostprijsberekening voor het artikel en de bijbehorende gefabriceerde artikelen wanneer stuklijstberekeningen een Maken naar order-explosiemodus gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ef68a-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="ef68a-118">Er wordt uitgegaan van de veronderstelling dat de gefabriceerde onderdelen in de exacte hoeveelheid worden gemaakt, net als een gefabriceerd onderdeel met het stuklijstregeltype Productie.</span><span class="sxs-lookup"><span data-stu-id="ef68a-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="ef68a-119">Opgegeven berekeningshoeveelheid in een orderspecifieke stuklijstberekening - Een orderspecifieke stuklijstberekening kan worden uitgevoerd voor een regelartikel op een verkooporder, verkoopofferte of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="ef68a-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="ef68a-120">De opgegeven berekeningshoeveelheid gebruikt de hoeveelheid van het oorspronkelijke regelartikel, maar de standaardhoeveelheid kan worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="ef68a-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="ef68a-121">U kunt selecteren of u wilt dat de orderspecifieke stuklijstberekening een Maken naar order-explosiemodus of een explosiemodus voor meerdere niveaus gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ef68a-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="ef68a-122">Het berekende bedrag van de afgeschreven constante kosten van een gefabriceerd artikel wordt toeslagen genoemd.</span><span class="sxs-lookup"><span data-stu-id="ef68a-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>







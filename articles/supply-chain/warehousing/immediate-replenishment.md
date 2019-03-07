---
title: Directe aanvulling
description: In dit onderwerp wordt beschreven hoe u directe aanvulling kunt gebruiken voor het aanvullen van voorraad wanneer met een richtlijn van de locatie voorraad niet kan worden toegewezen.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ab1f06951d5daceaf002b2cc23236dd818457985
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "348590"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="3f838-103">Directe aanvulling</span><span class="sxs-lookup"><span data-stu-id="3f838-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f838-104">Met directe aanvulling kunt u de voorraad meteen aanvullen wanneer met een richtlijn van de locatie voorraad niet kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="3f838-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="3f838-105">De aanvulling is gebaseerd op één regel in de instellingen van de locatie-instructie.</span><span class="sxs-lookup"><span data-stu-id="3f838-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="3f838-106">Aanvulling van die eenheid vindt onmiddellijk plaats als voorraad niet voorhanden is in de maateenheid die is opgegeven in die regel.</span><span class="sxs-lookup"><span data-stu-id="3f838-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="3f838-107">Directe aanvulling biedt een alternatief voor de methode waarbij de toewijzing van de voorraad is gebaseerd op meer regels in de locatie-instructie en waar de vraag aan het einde van de toewijzing wordt opgeteld en aangevuld in de maateenheid die is opgegeven door de laatste regel van de locatie-instructie.</span><span class="sxs-lookup"><span data-stu-id="3f838-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="3f838-108">De voordelen van onmiddellijke aanvulling zijn dat de aanvulling kan worden beperkt door specifieke eenheden en de hoeveelheid kan worden doorgestuurd naar specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="3f838-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="3f838-109">Bedrijfsscenario</span><span class="sxs-lookup"><span data-stu-id="3f838-109">Business scenario</span></span>

<span data-ttu-id="3f838-110">U hebt bijvoorbeeld een magazijn met afzonderlijke orderverzamelgebieden voor de maateenheden 'doos' en 'stuk'.</span><span class="sxs-lookup"><span data-stu-id="3f838-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="3f838-111">U wilt de orderverzamelprocedure optimaliseren door zoveel mogelijk dozen te verzamelen en daarna de resterende hoeveelheid die kleiner is dan een doos te verzamelen in het gebied 'stuk'.</span><span class="sxs-lookup"><span data-stu-id="3f838-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="3f838-112">In dit geval kunt u directe aanvulling gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3f838-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="3f838-113">In de locatie-instructie kunt u directe aanvulling instellen voor dozen zodat aanvulling op vraag wordt gebruikt zodra er een tekort is aan dozen die kunnen worden verzameld voor de vraaghoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="3f838-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="3f838-114">Op deze manier optimaliseert u het orderverzamelproces en omvat de orderverzameling zoveel mogelijk dozen.</span><span class="sxs-lookup"><span data-stu-id="3f838-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="3f838-115">Directe aanvulling zorgt voor aanvulling van de dozen en de vraag wordt niet doorgegeven, zodat de hoeveelheden worden verzameld in de maateenheid 'stuk'.</span><span class="sxs-lookup"><span data-stu-id="3f838-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="3f838-116">Met andere woorden, alleen de hoeveelheden die moeten worden verzameld in de maateenheid 'stuk' (dat wil zeggen hoeveelheden die kleiner zijn dan een doos) worden verzameld uit het gebied 'stuk'.</span><span class="sxs-lookup"><span data-stu-id="3f838-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="3f838-117">Als er een tekort optreedt in het gebied 'doos', kunt u zo veel mogelijk dozen buiten de totale vraag ophalen.</span><span class="sxs-lookup"><span data-stu-id="3f838-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="3f838-118">De resterende hoeveelheden wordt vervolgens worden opgehaald uit het gebied 'stuk'.</span><span class="sxs-lookup"><span data-stu-id="3f838-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="3f838-119">Waar van toepassing</span><span class="sxs-lookup"><span data-stu-id="3f838-119">Where it applies</span></span>

<span data-ttu-id="3f838-120">Directe aanvulling wordt gebruikt tijdens het uitvoeren van een wave als toewijzing mislukt voor een locatie-instructieregel waarvoor een aanvullingssjabloon is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="3f838-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="3f838-121">Directe aanvulling instellen</span><span class="sxs-lookup"><span data-stu-id="3f838-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="3f838-122">Ga naar **Magazijnbeheer** \> **Instellen** \> **Locatie-instructies** en selecteer vervolgens op het tabblad **Regels** in de lijst **Sjabloon voor directe aanvulling** een aanvullingssjabloon voor de wavevraag.</span><span class="sxs-lookup"><span data-stu-id="3f838-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="3f838-123">De aanvullingssjabloon wordt toegepast als de locatie-instructieregel een specifieke maateenheid niet kan toewijzen.</span><span class="sxs-lookup"><span data-stu-id="3f838-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="3f838-124">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="3f838-124">Troubleshooting</span></span>

<span data-ttu-id="3f838-125">Als directe aanvulling wordt geselecteerd voor een locatie-instructieregel, maar geen aanvullingswerk wordt gegenereerd als u vraagaanvullingssjablonen voor die locatie-instructieregel gebruikt, moeten twee mogelijke oorzaken worden onderzocht:</span><span class="sxs-lookup"><span data-stu-id="3f838-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="3f838-126">Zorg ervoor dat de toegepaste vraagaanvullingssjabloon is ingesteld om de juiste locatiesjablonen en werksjablonen te gebruiken van het type **Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="3f838-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="3f838-127">Zorg ervoor dat er voldoende voorhanden voorraad beschikbaar is op de locaties waar de vraagaanvullingssjabloon naar voorhanden voorraad voor aanvulling zoekt.</span><span class="sxs-lookup"><span data-stu-id="3f838-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>

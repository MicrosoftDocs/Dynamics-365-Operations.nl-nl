---
title: Zonemodel voor Transportbeheer
description: In dit onderwerp wordt uitgelegd u met Transportbeheer geografische locaties in zones kunt verdelen.
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425910"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="078ae-103">Zonemodel voor Transportbeheer</span><span class="sxs-lookup"><span data-stu-id="078ae-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="078ae-104">Met Transportbeheer kunt u geografische locaties in zones verdelen.</span><span class="sxs-lookup"><span data-stu-id="078ae-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="078ae-105">Het verdelen van locaties in zones kan helpen bij het volgende:</span><span class="sxs-lookup"><span data-stu-id="078ae-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="078ae-106">**Vereenvoudigen van transportprijzen**: zones waarvoor prijzen gelden kan eenvoudiger zijn dan afzonderlijke, op locatie gebaseerde prijzen, vooral wanneer transportlocaties verspreid zijn.</span><span class="sxs-lookup"><span data-stu-id="078ae-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="078ae-107">**Ladingplanning optimaliseren**: door ladingen per zone te consolideren.</span><span class="sxs-lookup"><span data-stu-id="078ae-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="078ae-108">**Routeplanning optimaliseren**: door specifieke routeplannen toe te wijzen aan specifieke zones.</span><span class="sxs-lookup"><span data-stu-id="078ae-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="078ae-109">U definieert zones op basis van de waarden in metagegevensvelden (zoals land, postcodebereik of vervoerdersservice) die elke zone kwalificeren.</span><span class="sxs-lookup"><span data-stu-id="078ae-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="078ae-110">Zonedefinities zijn niet vereist als uw transportprijzen niet met een zoneconcept werken.</span><span class="sxs-lookup"><span data-stu-id="078ae-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>

---
title: Geïntegreerde locaties en magazijnen
description: In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Common Data Service beschreven.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770978"
---
# <a name="integrated-sites-and-warehouses"></a>Geïntegreerde locaties en magazijnen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Common Data Service beschreven. Operationele locaties en magazijnen zijn gangbare concepten in een Supply Chain Management-toepassing. Ze worden gebruikt om de toeleveringsketen van uw bedrijf te modelleren.

## <a name="templates"></a>Sjablonen

Dankzij de integratie met Common Data Service zijn deze concepten en alle bijbehorende informatie beschikbaar in Common Data Service met behulp van de entiteiten voor locatie- en magazijngegevens in de volgende tabel.

Finance and Operations-apps | Andere Dynamics 365-apps | Beschrijving
--------------------------|---------------------------|---
Sites | msdyn_operationalsites | 
Magazijnen | msdyn_warehouses | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]


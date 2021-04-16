---
title: Geïntegreerde locaties en magazijnen
description: In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Dataverse beschreven.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750661"
---
# <a name="integrated-sites-and-warehouses"></a>Geïntegreerde locaties en magazijnen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Dataverse beschreven. Operationele locaties en magazijnen zijn gangbare concepten in een Supply Chain Management-toepassing. Ze worden gebruikt om de toeleveringsketen van uw bedrijf te modelleren.

## <a name="templates"></a>Sjablonen

Dankzij de integratie met Dataverse zijn deze concepten en alle bijbehorende informatie beschikbaar in Dataverse met behulp van de tabellen voor locatie- en magazijngegevens in de volgende tabel.

Finance and Operations-apps | Andere Dynamics 365-apps | Beschrijving
--------------------------|---------------------------|---
Sites | msdyn_operationalsites | 
Magazijnen | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
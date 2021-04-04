---
title: Geïntegreerde locaties en magazijnen
description: In dit onderwerp wordt de integratie van locatie- en magazijngegevens tussen Finance and Operations en Dataverse beschreven.
author: t-benebo
manager: AnnBe
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
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560356"
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
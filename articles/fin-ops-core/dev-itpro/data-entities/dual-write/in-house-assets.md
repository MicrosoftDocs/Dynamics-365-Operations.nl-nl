---
title: Interne activa voor onderhoudsbeurten
description: In dit onderwerp wordt beschreven hoe u met Microsoft Dynamics 365 Field Service zowel klantactiva als in-house activa kunt onderhouden.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941409"
---
# <a name="in-house-assets-for-servicing"></a>Interne activa voor onderhoudsbeurten

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service is ontworpen voor het onderhouden van klantactiva. Activabeheer voor Dynamics 365 Supply Chain Management is ontworpen om interne activa te onderhouden. Dankzij de integratie van deze twee apps kunt u Field Service gebruiken om zowel klantactiva als interne activa te onderhouden. U kunt de activa ook classificeren, op basis van functionele locatie of hiërarchie, en het onderhoud op een gedetailleerd niveau bijhouden.

Zie [Dynamics 365 Field Service en Supply Chain Management integreren](/dynamics365/field-service/supply-chain-field-service-integration) voor meer informatie.

## <a name="templates"></a>Sjablonen

Interne activa omvatten een verzameling basistabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| Finance and Operations-apps | Modelgestuurde apps in Dynamics 365 | Omschrijving |
|-----------------------------|-----------------------------------|-------------|
| Levenscyclusmodellen van activa voor activabeheer | msdyn\_assetlifecyclemodels | |
| Statussen van levenscyclus van activa voor activabeheer | msdyn\_assetlifecyclestates | |
| Activa voor activabeheer | msdyn\_customerassets | |
| Activatypen voor activabeheer | msdyn\_customerassetcategories | |
| Levenscyclusmodellen voor functionele locaties voor activabeheer | msdyn\_functionallocationlifecyclemodels | |
| Levenscyclusstatussen voor functionele locaties voor activabeheer | msdyn\_functionallocationlifecyclestates | |
| Functionele locaties voor activabeheer | msdyn\_functionallocations | |
| Functionele locatietypen voor activabeheer | msdyn\_functionallocationtypes | |
| Fabrikanten voor activabeheer | msdyn\_manufacturers | |
| Modellen voor activabeheer | msdyn\_models | |
| Garantie voor activabeheer | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
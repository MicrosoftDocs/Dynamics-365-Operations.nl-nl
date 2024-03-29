---
title: Interne activa voor onderhoudsbeurten
description: In dit artikel wordt beschreven hoe u met Microsoft Dynamics 365 Field Service zowel klantactiva als interne activa kunt onderhouden.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289245"
---
# <a name="in-house-assets-for-servicing"></a>Interne activa voor onderhoudsbeurten

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service is ontworpen voor het onderhouden van klantactiva. Activabeheer voor Dynamics 365 Supply Chain Management is ontworpen om interne activa te onderhouden. Dankzij de integratie van deze twee apps kunt u Field Service gebruiken om zowel klantactiva als interne activa te onderhouden. U kunt de activa ook classificeren, op basis van functionele locatie of hiërarchie, en het onderhoud op een gedetailleerd niveau bijhouden.

Zie [Dynamics 365 Field Service en Supply Chain Management integreren](/dynamics365/field-service/supply-chain-field-service-integration) voor meer informatie.

## <a name="templates"></a>Sjablonen

Interne activa omvatten een verzameling basistabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| Finance and Operations-apps | Customer Engagement-apps | Beschrijving |
|-----------------------------|-----------------------------------|-------------|
[Levenscyclusmodellen van activa voor activabeheer](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Statussen van levenscyclus van activa voor activabeheer](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Activatypen voor activabeheer](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Activa voor activabeheer](mapping-reference.md#125) | msdyn_customerassets | |
[Levenscyclusmodellen voor functionele locaties voor activabeheer](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Levenscyclusstatussen voor functionele locaties voor activabeheer](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Functionele locatietypen voor activabeheer](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Functionele locaties voor activabeheer](mapping-reference.md#136) | msdyn_functionallocations | |
[Fabrikanten voor activabeheer](mapping-reference.md#153) | msdyn_manufacturers | |
[Modellen voor activabeheer](mapping-reference.md#154) | msdyn_models | |
[Garantie voor activabeheer](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

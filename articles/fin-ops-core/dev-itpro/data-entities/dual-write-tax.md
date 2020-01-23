---
title: Geïntegreerde belasting
description: In dit onderwerp wordt de integratie van belastinggegevens tussen Finance and Operations en Common Data Service beschreven.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853854"
---
# <a name="integrated-tax"></a>Geïntegreerde belasting

[!include [banner](../includes/banner.md)]

Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting. Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.

## <a name="templates"></a>Sjablonen

Belastinggegevens omvatten een verzameling entiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

Finance en Operations   | Andere Dynamics 365-apps
-------------------------|---------------------------------
Belastingcodes                  | msdyn\_taxcodes.md
Belastinggroepen               | msdyn\_taxgroups.md
Btw-artikelengroepen          | msdyn\_taxitemgroups.md
Belastingvrijstellingen           | msdyn\_taxexemptcodes.md
Belastingdienst          | msdyn\_taxauthorities.md
Bronbelastingcodes      | msdyn\_withholdingtaxcodes.md
Bronbelastinggroepen   | msdyn\_withholdingtaxgroups.md
Grootboekrekeningsgroep voor belasting | msdyn\_taxpostinggroups  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]


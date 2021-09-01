---
title: Geïntegreerde belasting
description: In dit onderwerp wordt de integratie van btw-gegevens tussen Finance and Operations en Dataverse beschreven.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7e76294944196670ed4b02ebf785c1bed7b5106f73d4b66a15a19c9a4235cbf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738547"
---
# <a name="integrated-tax"></a>Geïntegreerde belasting

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting. Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.

## <a name="templates"></a>Sjablonen

Belastinggegevens omvatten een verzameling tabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| Finance and Operations-apps | Customer Engagement-apps | Beschrijving |
|-----------------------------|-----------------------------------|-------------|
[Btw-groep voor artikel](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Btw-dienst](mapping-reference.md#193) | msdyn_taxauthorities | |
[Entiteit btw-vrijstellingscode voor CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Btw-groepen](mapping-reference.md#195) | msdyn_taxgroups | |
[Groepen van boekingen in btw-grootboek V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Bronbelastingcodes](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Bronbelastinggroepen](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

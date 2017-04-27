---
title: Verschillende leden van kostenelementdimensies toewijzen aan een gemeenschappelijke reeks dimensieleden
description: Door verschillende kostenelementendimensieleden aan een gemeenschappelijke set kostenelementendimensieleden toe te wijzen, kunt u gegevens samenvoegen in een gemeenschappelijke indeling ten behoeve van analyse.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Verschillende leden van kostenelementdimensies toewijzen aan een gemeenschappelijke reeks dimensieleden

Door verschillende kostenelementendimensieleden aan een gemeenschappelijke set kostenelementendimensieleden toe te wijzen, kunt u gegevens samenvoegen in een gemeenschappelijke indeling ten behoeve van analyse.

Als uw bedrijf wereldwijd actief is en de wettelijke boekhoudvereisten naleeft, maakt u mogelijk gebruik van meerdere rekeningschema's. Wanneer u kostenelementendimensieleden uit verschillende rekeningschema's importeert, kan het resultaat een wirwar van rekeningen zijn. Maar deze rekeningen kunnen dezelfde aard hebben, en u wilt misschien de kosten voor deze rekeningen analyseren en toewijzen met behulp van een gemeenschappelijke indeling.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Kostenelementdimensieleden toewijzen aan een gemeenschappelijke indeling
In het volgende voorbeeld wordt getoond hoe u als kostencontroller een nieuwe kostenelementendimensie aanmaakt in Kostprijsboekhouding. Deze dimensie wijst kostenelementendimensieleden van het Amerikaanse rekeningschemastructuur en de Franse rekeningschemastructuur toe aan een gemeenschappelijke set kostenelementdimensieleden. U kunt vervolgens met de gemeenschappelijke set kostenelementendimensieleden kostengegevens van de twee rechtspersonen analyseren in een kostprijsboekhoudinggrootboek.

| Bron: Amerikaans rekeningschema                                          | Bron: Frans rekeningschema                                          | Nieuwe gemeenschappelijke set kostenelementendimensieleden                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Geïmporteerde kostenelementendimensieleden van het Amerikaanse rekeningschema. | Geïmporteerde kostenelementendimensieleden van het Franse rekeningschema. | Toewijzing van de Franse en Amerikaanse kostenelementendimensieleden aan een gemeenschappelijke set |
| 5001: Verkoop                                                           | 5001: Verkoop en advertenties                                               | 5000: Verkoop en advertenties                                             |
| 5030: Advertenties                                                     | 6390: Voorraadinkoop\*                                                    | 7000: Schoonmaakkosten                                                 |
| 7001: Schoonmaakkosten                                               | 7001: Reiskosten                                                      | 7001: Reiskosten                                                   |

\*Het Franse kostenelementdimensielid Voorraadinkoop is niet toegewezen.

## <a name="currency-conversion"></a>Valutaomrekening
De verschillende rekeningschema's die u gebruikt zijn mogelijk ingesteld voor verschillende valuta's. Specificeer in dit geval een valutaomrekening, zodat de kostengegevens worden verwerkt met de juiste valuta zoals is gedefinieerd in het kostenboekhoudingsgrootboek waarin de kostenelementdimensieleden worden gebruikt. In het voorafgaande voorbeeld geldt dat als Amerikaanse dollars (USD) worden gebruikt in het kostprijsboekhoudinggrootboek, u een valutaomrekening moet maken van USD naar euro's (EUR) om transacties voor de toegewezen kostenelementdimensieleden te kunnen verwerken.

## <a name="update-mappings-at-any-time"></a>Toewijzingen op elk gewenst moment bijwerken
U kunt de toewijzingsdefinities voor een kostenelementendimensie op elk gewenst moment bijwerken. Omdat de toewijzingen niet beïnvloed worden door de datum, worden wijzigingen toegepast bij de volgende keer dat u kostentransacties verwerkt of kostenberekeningen uitvoert.



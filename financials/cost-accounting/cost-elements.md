---
title: Dimensies van kostenelement
description: Kostenelementdimensies zijn een van de kernpijlers in Kostprijsboekhouding en worden gebruikt om te categoriseren en te traceren waar kosten heen stromen.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c06f4f636a58ac8068415b1291bd8668e7a977d5
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="cost-element-dimensions"></a>Dimensies van kostenelement

[!include[banner](../includes/banner.md)]


Kostenelementdimensies zijn een van de kernpijlers in Kostprijsboekhouding en worden gebruikt om te categoriseren en te traceren waar kosten heen stromen. 

Een kostenelement correspondeert met een kostenrelevant artikel in het rekeningschema. Dit kan in principe elk type element zijn op het laagste niveau in een bedrijf, waar kosten heen kunnen stromen. Kostenelementen als concept kunnen variëren van grootboekrekeningen tot alle kostenrelevante resources. Momenteel biedt Kostprijsboekhouding ondersteuning voor grootboekrekeningen.

## <a name="two-types-of-cost-elements"></a>Twee typen kostenelementen
Er zijn twee typen kostenelementen: primaire kostenelementen en secundaire kostenelementen. In de volgende tabel worden de verschillen tussen de twee typen beschreven.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Primaire kostenelementen</strong></td>
<td><strong>Secundaire kostenelementen</strong></td>
</tr>
<tr class="even">
<td>De primaire kostenelementen vertegenwoordigen de stroom van kosten van financiële boekhouding naar kostprijsboekhouding. De kostenelementenstructuur correspondeert met de winst- verliesrekeningstructuur in het grootboek, waar een kostenelement kan corresponderen met een hoofdrekening. Niet alle hoofdrekeningen hoeven als kostenelementen te zijn vertegenwoordigd, afhankelijk van de behoeften van het bedrijf. Voorbeelden van primaire kostenelementen zijn onder meer:
<ul>
<li>Kosten van verkochte goederen</li>
<li>Indirecte materiaalkosten</li>
<li>Personeelskosten</li>
<li>Energiekosten</li>
</ul></td>
<td>De secundaire kostenelementen vertegenwoordigen de interne stroom van kosten, omdat deze kosten alleen in Kostenprijsboekhouding worden gemaakt en gebruikt. Deze worden gebruikt om te borgen dat de oorsprong van kosten getraceerd kan worden. Deze kostenelementen worden gebruikt in kostentoewijzingen en overheadberekeningen. Voorbeelden van secundaire kostenelementen zijn onder meer:
<ul>
<li>Productiekosten</li>
<li>Overheadkosten voor productie, materiaal, en marketing</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Dimensies van kostenelementen en dimensieleden van kostenelementen.
Kostenelementen worden ook aangeduid als *kostenelementendimensies*. De individuele dimensiewaarden staan bekend als *kostenelementdimensieleden*. Stel dat u een rekeningschemastructuur hebt, die de basis voor de wettelijk voorgeschreven rapportage vormt. Deze structuur wordt gebruikt als de kostenelementendimensie. De rekeningen, die de primaire kostenelementen vormen, zijn vertegenwoordigd als de kostenelementendimensieleden in Kostprijsboekhouding. In de onderstaande schermopname ziet u een voorbeeld van Hoofdrekeningen als de kostenelementdimensie met de werkelijke hoofdrekeningen als kostenelementdimensieleden. 

[![dimensies-kostenelement](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Kostenelementdimensieleden importeren door middel van gegevensconnectors
Om gemakkelijker leden van kostenelementdimensies te kunnen configureren in Kostenprijsboekhouding, kunt u met vooraf gemaakte gegevensconnectors of zelf samengestelde connectors de primaire kostenelementen ophalen vanuit een of meer bronsystemen.

## <a name="implementation-considerations"></a>Implementatieoverwegingen
Omdat kostenelementen het laagste niveau van kostendetails vertegenwoordigen, moet u ervoor zorgen dat alle kostenelementen die zijn vereist om de managementrapporten aan maken, zijn opgenomen wanneer u de kostenelementenstructuur implementeert. Het kan lastig zijn om een gepast aantal kostenelementen voor kostenbeheer te bepalen. Als u duizenden kostenelementen hebt, kan moeilijk zijn om elk kostenelement te beheersen. Eventueel kunt u kostenelementen groeperen en kostenbeheer uitvoeren op een samengevoegd niveau.





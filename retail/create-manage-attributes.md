---
title: Attributen maken en beheren
description: In dit artikel worden kenmerken in Microsoft Dynamics 365 for Operations beschreven. De attributen laten u een product en zijn kenmerken beschrijven via de gebruiker gedefinieerde velden.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: eaee0edb4822a386c8781d9929999cea326f0a40
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="create-and-manage-attributes"></a>Attributen maken en beheren

[!include[banner](includes/banner.md)]


In dit artikel worden kenmerken in Microsoft Dynamics 365 for Operations beschreven. De attributen laten u een product en zijn kenmerken beschrijven via de gebruiker gedefinieerde velden.

De attributen laten u een product en zijn kenmerken beschrijven via de gebruiker gedefinieerde velden. Bijvoorbeeld, U kunt de geheugengrootte van het product en de harde schijf capaciteit opgeven, en aangeven of het product Energy star-conform is. De attributen kunnen met verschillende kleinhandelsentiteiten zoals productcategorieën en kleinhandelskanalen zijn gekoppeld, en de standaardwaarden kunnen voor hen zijn ingesteld. De producten erven hun kenmerken en standaardwaarden voor die kenmerken wanneer ze gekoppeld zijn met productcategorieën of kleinhandelskanalen. De standaardwaarden kunnen op het niveau van het afzonderlijke product, op het kleinhandelskanaalniveau, of in een kleinhandelscatalogus worden overschreven.

#### <a name="examples"></a>Voorbeelden

| Categorie   | Kenmerk                | Toegestane waarden          | Standaardwaarde |
|------------|--------------------------|-----------------------------|---------------|
| Tv en Video | Merk                    | Alle geldige Merk waarde       | Geen          |
| Tv         | Schermgrootte              | 20"–80"                     | Geen          |
| Tv         | Verticale resolutie      | 480i, 720p, 1080i, or 1080p | 1080p         |
| Tv         | Schermvernieuwingsfrequentie      | 60hz, 120hz of 240hz       | 60hz          |
| Tv         | HDMI-ingang              | 0–10                        | 3             |
| Tv         | DVI-ingang               | 0–10                        | 1             |
| Tv         | Composiet-ingang         | 0–10                        | 2             |
| Tv         | Component-ingang         | 0–10                        | 1             |
| LCD        | 3D Ready                 | Ja of Nee                   | Ja           |
| LCD        | 3D Enabled               | Ja of Nee                   | Nee            |
| Plasma     | Operationele Temperaturen van      | 32–110 graden              | 32            |
| Plasma     | Operationele Temperaturen tot        | 32–110 graden              | 100           |
| Projectie | De Garantie van de projectiebuis | 6, 12, of 18 maanden         | 12            |
| Projectie | # van Projectiebuizen    | 1–5                         | 3             |


## <a name="attribute-type"></a>Type kenmerk
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Kenmerken zijn gebaseerd op kenmerktypen. Het kenmerktype geeft het gegevenstype aan dat kan worden ingevoerd voor een specifiek kenmerk. Momenteel worden in Microsoft Dynamics 365 for Operations de volgende kenmerktypen ondersteund:

-   **Valuta** - Dit kenmerktype ondersteunt valutawaarden. Het kan begrensd zijn (oftewel kan het een waardebereik ondersteunen), of kan worden opengelaten.
-   **DateTime** - Dit kenmerktype ondersteunt datum en tijdwaarden. Het kan begrensd zijn (oftewel kan het een waardebereik ondersteunen), of het kan worden opengelaten.
-   **Decimaal** - Dit kenmerktype ondersteunt numerieke waarden die decimalen zijn. Het kan ook maateenheden ondersteunen. Het kan begrensd zijn (oftewel kan het een waardebereik ondersteunen), of het kan worden opengelaten.
-   **Heel getal** - Dit kenmerktype ondersteunt numerieke waarden. Het kan ook maateenheden ondersteunen. Het kan begrensd zijn (oftewel kan het een waardebereik ondersteunen), of het kan worden opengelaten.
-   **Tekst** - Dit kenmerktype ondersteunt tekst waarden. Het kan ook een vooraf bepaalde set van mogelijke waarden (opsomming) ondersteunen.
-   **Booleaans**: dit type kenmerk ondersteunt binaire waarden (**waar**/**onwaar**).
-   **Verwijzing**.

## <a name="attribute"></a>Kenmerk
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) Naast de naam, beschrijvende naam, omschrijving en Help-tekst kunnen een of meer van de volgende gegevenstypen worden vastgelegd voor een kenmerk:

-   Standaardwaarde
-   Kenmerkmetagegevens, zoals metagegevens die aangeven of het kenmerk kan worden gezocht, geraffineerd of gesorteerd worden.

## <a name="attribute-group"></a>Kenmerkgroep
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Nadat kenmerken zijn gedefinieerd, kunnen ze in kenmerkgroepen worden gegroepeerd. De kenmerkgroepen geven groeperingen van individuele kenmerken, en kunnen van worden toegewezen aan kleinhandelscategorieën of kleinhandelskanalen.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Toewijzen van kenmerkgroepen aan kleinhandelscategorieën
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Een of meer kenmerkgroepen kunnen worden gekoppeld aan categorieknooppunten in de productcategoriehiërarchie voor de detailhandel. Wanneer producten zijn gecategoriseerd, erven zij de kenmerken die zijn opgenomen in de kenmerkgroepen.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Toewijzen van kenmerkgroepen aan kleinhandelswinkels
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Een of meer kenmerkgroepen kunnen worden gekoppeld aan een of meer detailhandelswinkels in de hiërarchie voor detailhandelswinkels. Wanneer producten zijn verrijkt voor specifieke kleinhandelswinkels, erven zij de kenmerken die zijn opgenomen in de kenmerkgroepen.

## <a name="overriding-attribute-values"></a>Overschrijven van kenmerkwaarden
### <a name="at-the-product-level"></a>Op het productniveau

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) De standaardwaarden van kenmerken kunnen worden overschreven op productniveau (oftewel voor afzonderlijke producten).

### <a name="in-a-retail-catalog"></a>In een kleinhandelcatalogus

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) De standaardwaarden van kenmerken kunnen worden overschreven voor afzonderlijke producten in specifieke catalogi die gericht zijn op specifieke detailhandelskanalen.

### <a name="at-the-retail-channel-level"></a>Op het detailhandelkanaalniveau

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) De standaardwaarden van kenmerken kunnen worden overschreven voor afzonderlijke producten in specifieke catalogi die gericht zijn op specifieke detailhandelskanalen.





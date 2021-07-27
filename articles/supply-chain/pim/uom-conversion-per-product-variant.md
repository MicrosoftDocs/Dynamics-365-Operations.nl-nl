---
title: Conversie van maateenheid per productvariant
description: In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten. Het bevat een voorbeeld van de instellingen.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 03c9406d295fb0dbd22e8072c2695dbef419b706
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353535"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Conversie van maateenheid per productvariant

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor verschillende productvarianten.

In plaats van meerdere afzonderlijke producten te maken die moeten worden onderhouden, kunt u productvarianten gebruiken om variaties te maken van een enkel product. Een productvariant kan bijvoorbeeld een t-shirt van een bepaalde maat en kleur zijn.

Voorheen konden eenheidconversies alleen in het productmodel worden ingesteld. Daarom hadden alle productvarianten dezelfde regels voor eenheidsomrekening. Wanneer echter de functie *Maateenheid omrekeningen voor productvarianten* is ingeschakeld, en uw t-shirts in dozen wordt verkocht en het aantal t-shirts dan kan worden verpakt in een doos hafhankelijk is van de maat van de t-shirts. kunt u nu eenheidsomrekeningen instellen tussen de verschillende shirtmaten en de dozen die voor de verpakking worden gebruikt.

## <a name="turn-on-the-feature-in-your-system"></a>De functie inschakelen in uw systeem

Als deze functie nog niet in uw systeem wordt weergegeven, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Maateenheid omrekeningen voor productvarianten* in.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Een product voor eenheidconversie per variant instellen

Productvarianten kunnen alleen worden gemaakt voor producten die productmodellen zijn. Zie [Een productmodel maken](tasks/create-product-master.md) voor meer informatie. De functie *Maateenheid omrekeningen voor productvarianten* is niet beschikbaar voor producten die zijn ingesteld voor catch-weight-processen.

Voer de volgende stappen uit om een productmodel te configureren voor ondersteuning van eenheidsomrekening per variant.

1. Ga naar **Productgegevensbeheer \> Producten \> Productmodellen**.
1. Maak of open een productmodel om naar de pagina **Productgegevens** te gaan.
1. Stel de optie **Maateenheidconversies inschakelen** in op *Ja*.
1. Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Eenheidsomrekeningen**.
1. De pagina **Eenheidsomrekeningen** wordt geopend. Selecteer een van de volgende tabbladen:

    - **Omrekeningen binnen klasse**: selecteer dit tabblad om te converteren tussen eenheden die tot dezelfde eenheidsklasse behoren.
    - **Omrekeningen tussen klassen**: selecteer dit tabblad om te converteren tussen eenheden die tot verschillende eenheidsklassen behoren.

1. Selecteer **Nieuw** om een nieuwe eenheidsomrekening toe te voegen.
1. Stel het veld **Conversie maken voor** in op een van de volgende waarden:

    - **Product**: als u deze waarde selecteert, kunt u een eenheidconversie instellen voor het productmodel. Deze eenheidsomrekening wordt gebruikt als terugval voor alle productvarianten waarvoor geen eenheidsomrekening is gedefinieerd.
    - **Productvariant**: als u deze waarde selecteert, kunt u een eenheidconversie instellen voor een specifieke productvariant. Gebruik het veld **Productvariant** om de variant te selecteren.

    ![Een nieuwe eenheidsomrekening toevoegen.](media/uom-new-conversion.png "Een nieuwe eenheidsomrekening toevoegen")

1. Gebruik de andere velden die zijn opgegeven om de eenheidsomrekening in te stellen.
1. Selecteer **OK** om de nieuwe eenheidsomrekening op te slaan.

> [!TIP]
> U kunt de pagina **Eenheidsomrekeningen** voor een product of een productvariant openen vanaf een van de volgende pagina's:
> 
> - Productgegevens
> - Details van vrijgegeven producten
> - Vrijgegeven productvarianten

## <a name="example-scenario"></a>Voorbeeldscenario

In dit scenario verkoopt een bedrijf t-shirts in de maten small, medium, large en extra large. Het t-shirt is gedefinieerd als een product en de verschillende maten zijn gedefinieerd als varianten van dat product. De shirts worden in dozen verpakt. Voor de maten small, medium en large passen er vijf shirts in elke doos. Voor de maat extra large is er echter ruimte voor slechts vier shirts in elke doos.

Het bedrijf wil de verschillende varianten van de t-shirts in de eenheid *Stuks* bijhouden, maar verkoopt de t-shirts in de eenheid *Dozen*. Voor de maten small, medium en large luidt de omrekening tussen de voorraadeenheid en de verkoopeenheid 1 doos = 5 stuks. Voor de maat extra large is de omrekening 1 doos = 4 stuks.

1. Ga naar de pagina **Details van vrijgegeven producten** voor het product **T-shirt** en open de pagina **Eenheidsomrekening**.
1. Stel op de pagina **Eenheidsomrekeningen** de volgende eenheidsomrekening in voor de productvariant **Extra large**.

    | Veld                 | Instelling                 |
    |-----------------------|-------------------------|
    | Conversie maken voor | Productvariant         |
    | Productvariant       | T-Shirt : : Extra large : : |
    | Van eenheid             | Dozen                   |
    | Factor                | 4                       |
    | Naar eenheid               | Stuks                  |

1. Aangezien de productvarianten **Small**, **Medium** en **Large** allemaal dezelfde eenheidsomrekening hebben tussen de eenheden *Doos* en *Stuks*, kunt u hiervoor de volgende eenheidsomrekening definiëren in het productmodel.

    | Veld                 | Instelling |
    |-----------------------|---------|
    | Conversie maken voor | Artikel |
    | Artikel               | T-shirt |
    | Van eenheid             | Dozen   |
    | Factor                | 5       |
    | Naar eenheid               | Stuks  |

## <a name="using-excel-to-update-the-unit-conversions"></a>De eenheidconversies bijwerken met Excel

Als een product veel productvarianten met verschillende eenheidsomrekeningen heeft, is het een goed idee om de eenheidsomrekeningen naar een Microsoft Excel-werkmap te exporteren, deze bij te werken en ze vervolgens terug te publiceren naar Dynamics 365 Supply Chain Management.

Als u eenheidsomrekeningen naar Excel wilt exporteren, selecteert u op de pagina **Eenheidsomrekeningen** in het actievenster de optie **Openen in Microsoft Office**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Maateenheden beheren](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
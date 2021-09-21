---
title: Varianten genereren voor technische producten
description: In dit onderwerp wordt beschreven hoe u varianten voor technische producten genereert
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4e2133263f4bee09a3365236601e0d2fdd08a7ae
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471831"
---
# <a name="generate-variants-for-engineering-products"></a>Varianten genereren voor technische producten

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u varianten voor technische producten genereert.

## <a name="turn-on-variant-generation-for-engineering-products"></a>Varianten genereren voor technische producten inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *beheer technische wijzigingen*
- **Naam eigenschap:** *Varianten genereren voor technische producten*

> [!IMPORTANT]
> De functie *Varianten genereren voor technische producten* is alleen zichtbaar in het systeem nadat u de configuratiesleutel *Engineering Change Management* hebt ingeschakeld. Raadpleeg [Overzicht van technisch wijzigingsbeheer](product-engineering-overview.md) voor instructies.

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Een of meer nieuwe varianten van een technisch product genereren

U kunt een of meer nieuwe varianten van een product maken zonder gegevens van een bestaand product te kopiëren. Dit is handig wanneer u meerdere productvarianten tegelijk moet maken.

De volgende procedure geeft een voorbeeld van het maken van verschillende varianten die de kleurdimensie bevatten.

1. Open de pagina **Vrijgegeven producten** (ga bijvoorbeeld naar **Beheer voor technische wijzigingen \> Algemeen \> Vrijgegeven producten**).
1. Selecteer **Technisch product** in de groep **Nieuw** op het tabblad **Product** in het actievenster.
1. Het dialoogvenster **Nieuw product** wordt geopend. Selecteer de juiste **Technische categorie**.
1. Als uw geselecteerde technische categorie variantdimensies bevat, kunt u nu waarden voor die dimensies instellen. Als de categorie bijvoorbeeld een dimensie **Kleur** heeft, kunt u deze instellen op *Blauw*.
1. Maak zo nodig andere instellingen. Selecteer **OK** om het product te maken.
1. Het product en de blauwe V-1-variant worden gemaakt en het nieuwe product wordt nu geopend.
1. Voeg indien nodig een stuklijst en een route aan de variant toe.
1. Ga naar het actievenster en open het tabblad **Product**. Selecteer **Productdimensies** in de groep **Productmodel**.
1. De pagina **Productdimensies** wordt geopend. Deze pagina bevat een tabblad voor elke beschikbare dimensie. Voeg op elk tabblad een rij toe voor elke waarde die u voor elke relevante dimensie zult ondersteunen. (In dit voorbeeld kunt u rijen toevoegen aan het tabblad **Kleur** voor *Wit*, *Geel* en *Groen*).
1. Sluit de pagina en selecteer vervolgens **Vrijgegeven productvarianten**. Merk op dat de eerste variant die u hebt aangemaakt (blauwe V-1) verschijnt.
1. Selecteer in het actiepaneel op het tabblad **Productvariant** **Variantsuggesties**.
1. Volg in het dialoogvenster **Variantsuggesties** een van deze stappen:

    - Boven aan het dialoogvenster is er een gedeelte voor elke beschikbare dimensie. Schakel voor elke dimensie het selectievakje in voor elke waarde waarvoor u een variant suggestie wilt genereren en selecteer vervolgens **Voorstellen** op de werkbalk. Relevante suggesties worden toegevoegd aan het gedeelte **Voorgestelde varianten**.
    - Selecteer **Alles voorstellen** op de werkbalk om variantsuggesties te genereren voor alle beschikbare combinaties van dimensiewaarden. De suggesties worden toegevoegd aan het gedeelte **Voorgestelde varianten**.

1. Schakel in het gedeelte **Voorgestelde varianten** het selectievakje in voor elke variant die u wilt aanmaken. Selecteer vervolgens **Aanmaken** om de geselecteerde varianten te genereren en vrij te geven aan het technische bedrijf. De volgende voorwaarden zijn van toepassing:

    - Geen van de gemaakte varianten heeft een stuklijst of route.
    - De kenmerken voor deze varianten worden standaard uit de technische categorie gekopieerd en niet van de vorige variant.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Een variant genereren als kopie van een andere productvariant

U kunt een variant van een product maken op basis van een andere productvariant. De stuklijst en route van de bronproductvariant worden naar de nieuwe variant gekopieerd. Dit kan handig zijn voor discrete productieproducten waar het handig kan zijn om de stuklijst te maken op basis van een begin stuklijst en de wijzigingen van de vorige variant bij te houden. Voor traceerbaarheid registreert het systeem welke variant is gekopieerd om een nieuwe kopie te maken.

De volgende procedure geeft een voorbeeld van het maken van een nieuwe variant die de kleurdimensie bevat door een kopie van een bestaande variant te maken

1. Open de pagina **Vrijgegeven producten** (ga bijvoorbeeld naar **Beheer voor technische wijzigingen \> Algemeen \> Vrijgegeven producten**).
1. Selecteer **Technisch product** in de groep **Nieuw** op het tabblad **Product** in het actievenster.
1. Het dialoogvenster **Nieuw product** wordt geopend. Selecteer de juiste **Technische categorie**.
1. Als uw geselecteerde technische categorie variantdimensies bevat, kunt u nu waarden voor die dimensies instellen. Als de categorie bijvoorbeeld een dimensie **Kleur** heeft, kunt u deze instellen op *Blauw*.)
1. Maak zo nodig andere instellingen. Selecteer **OK** om het product te maken.
1. Het product en de blauwe V-1-variant worden gemaakt en het nieuwe product wordt nu geopend.
1. Voeg indien nodig een stuklijst en een route aan de variant toe.
1. Voeg indien nodig kenmerken aan de productvariant toe.
1. Voeg de blauwe V-1 productvariant toe aan een order voor een technische wijziging.
1. Stel **Impact** in op *Nieuwe variant*.
1. Selecteer de nieuwe kleurwaarde (bijvoorbeeld *Wit*). De volgende voorwaarden gelden: 
    - De nieuwe variant heeft een stuklijst en route die van de vorige variant zijn gekopieerd.
    - De nieuwe variant heeft de kenmerken die van de vorige variant zijn gekopieerd.
1. Keur de gewijzigde order goed.
1. verwerk de gewijzigde order. Nadat de order is verwerkt, wordt de V-1-variant gemaakt en vrijgegeven aan het technische bedrijf.

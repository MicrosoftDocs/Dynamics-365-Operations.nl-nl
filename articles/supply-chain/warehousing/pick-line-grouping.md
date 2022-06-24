---
title: Orderverzamelregels groeperen
description: Dit artikel bevat een overzicht van de groepering van orderverzamelregels.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: f9e6cbf0f520f0f30c01cefba03689e9c119f2cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890620"
---
# <a name="pick-line-grouping"></a>Orderverzamelregels groeperen

[!include [banner](../includes/banner.md)]

Bij het groeperen van orderverzamelregels kunnen meerdere werkregels met hetzelfde artikel en dezelfde locatie worden gecombineerd in één orderverzameling die voor de gebruiker wordt weergegeven op het mobiele apparaat. Op deze manier kunnen magazijnmedewerkers de meest efficiënte instructies ontvangen, maar wordt tegelijkertijd de vereiste scheiding van werkregels in het systeem gehandhaafd (bijvoorbeeld voor verschillende containers, orders enzovoort).

## <a name="turn-on-the-pick-line-grouping-feature"></a>De functie Orderverzamelregels groeperen inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en de functie desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Orderverzamelregels groeperen*

## <a name="set-up-pick-line-grouping"></a>De groepering van orderverzamelregels instellen

### <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Naam menuopdracht** *Orderverzameling voor verkoopgroepsregels* in.
1. Voer in het veld **Titel** *Orderverzameling voor verkoopgroepsregel* in. Deze titel wordt weergegeven in het menu van het mobiele apparaat.
1. Selecteer **Werk** in het veld *Modus*.
1. Stel de optie **Bestaand werk gebruiken** in op *Ja*.
1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - Selecteer **Door gebruiker bestuurd** in het veld *Bestuurd door*.
    - Stel de optie **Nummerplaat maken** in op *Ja*.
    - Stel de optie **Groep verzamelen** in op *Ja*.
    - Accepteer de standaardwaarden voor de overige opties.

1. Voer de volgende stappen uit om de geldige werkklassen voor de menuopdracht voor mobiele apparaten te configureren:

    1. Selecteer **Nieuw** op het sneltabblad **Werkklassen**.
    2. In het veld **Werkklasse-id** kunt u *Verkoop* of *VO verzamelen* selecteren, afhankelijk van het magazijn dat u gebruikt. Selecteer voor dit scenario *VO verzamelen*.

        Het veld **Werkordertype** wordt automatisch ingesteld op *Verkooporders*.

### <a name="set-up-a-mobile-device-menu"></a>Een menu van een mobiel apparaat instellen

Voer deze stappen uit om de menuopdracht die u zojuist hebt gemaakt, toe te voegen aan het menu **Uitgaand**.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer **Bewerken** in het actievenster.
1. In het lijstvenster worden alle bestaande menu's van het mobiele apparaat weergegeven. Selecteer *Uitgaand* in de lijst.
1. Zoek en selecteer in de lijst **Beschikbare menu's en menuopdrachten** de menuopdracht *Orderverzameling voor verkoopgroepsregel* die u zojuist hebt gemaakt.
1. Selecteer de pijlknop naar rechts om de menuopdracht *Orderverzameling voor verkoopgroepsregel* te verplaatsen naar de lijst **Menustructuur**.
1. Gebruik de pijlknoppen omhoog en omlaag om de menuopdracht naar de gewenste positie in de menustructuur te verplaatsen.
1. Selecteer **Opslaan** in het actievenster.

### <a name="set-up-a-work-template"></a>Een werksjabloon instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Selecteer *Verkooporders* in het veld **Werkordertype**.
1. Zoek en selecteer in het raster **Overzicht** de werksjabloon die met deze functie moet worden gebruikt. Selecteer voor dit scenario de sjabloon *51 orderverzamelen voor klaarzetten*.
1. Selecteer **Query bewerken** in het actievenster.
1. Selecteer in het dialoogvenster Query-editor op het tabblad **Sorteren** de optie **Toevoegen** en stel vervolgens de volgende waarden voor de nieuwe rij in:

    - Selecteer **Tijdelijke werktransacties** in de kolom *Tabel*.
    - Selecteer **Tijdelijke werktransacties** in de kolom *Afgeleide tabel*.
    - Selecteer **Artikelnummer** in de kolom *Veld*.
    - Selecteer **Oplopend** in de kolom *Zoekrichting*.

1. Selecteer **OK** om het dialoogvenster te sluiten en uw selectie op te slaan.
1. Het volgende bericht wordt weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?' Selecteer **Ja** om door te gaan.

> [!IMPORTANT]
> De groepering van orderverzamelregels werkt alleen als de werkregels zijn gesorteerd op artikel-id. Als regels met dezelfde artikels niet na elkaar worden geordend, worden ze niet gegroepeerd.

## <a name="example"></a>Voorbeeld

### <a name="create-picking-work"></a>Orderverzamelingswerk maken

Voordat u de groepering van orderverzamelregels kunt instellen, moet u in aanmerking komend uitgaand werk maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder te maken.
1. Selecteer *US-004* in het veld **Klantrekening**.
1. Selecteer op het sneltabblad **Algemeen** magazijn **51** in het veld *Magazijn*.
1. Selecteer **OK**.
1. Voeg op het sneltabblad **Verkooporderregels** de volgende zes regels toe:

    - **Regel 1:** selecteer in het veld **Artikelnummer** de optie *M9200*. Typ **3** in het veld *Hoeveelheid*.
    - **Regel 2:** selecteer in het veld **Artikelnummer** de optie *M9201*. Typ **3** in het veld *Hoeveelheid*.
    - **Regel 3:** selecteer in het veld **Artikelnummer** de optie *M9202*. Typ **2** in het veld *Hoeveelheid*.
    - **Regel 4:** selecteer in het veld **Artikelnummer** de optie *M9200*. Typ **1** in het veld *Hoeveelheid*.
    - **Regel 5:** selecteer in het veld **Artikelnummer** de optie *M9200*. Typ **3** in het veld *Hoeveelheid*.
    - **Regel 6:** selecteer in het veld **Artikelnummer** de optie *M9202*. Typ **7** in het veld *Hoeveelheid*.

    Hier is een overzicht van de totale aantallen voor elk artikel:

    - **Artikel M9200:** *7* stuks
    - **Artikel M9201:** *3* stuks
    - **Artikel M9202:** *9* stuks

1. Voordat u de orders aan het magazijn vrijgeeft, moet u ervoor zorgen dat de picklocaties voldoende voorraad hebben voor alle artikelen op alle orders. Controleer de instelling **Locatie-instructie** om te bepalen welke orderverzamellocaties worden gebruikt voor het verzamelen van verkooporders. Als u de Demonstratiegegevensomgeving van Contoso voor magazijn *51* gebruikt, bevestigt u dat er beschikbare voorraad is.

    U moet nu de voorraad voor elke regel reserveren.

1. Selecteer op het sneltabblad **Verkooporderregels** een van de regels die moeten worden gereserveerd.
1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om de reservering toe te passen. Sluit de pagina vervolgens.
1. Herhaal stap 8 tot en met 10 voor de overige regels die moeten worden gereserveerd.

    U moet nu de verkooporder aan het magazijn vrijgeven.

1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    U ontvangt een bericht waarin wordt bericht dat er een zending en een wave zijn gemaakt en dat de wave is verzonden om te worden uitgevoerd in een batch.

    Wanneer de wave en alle taken verderop in de stroom zijn voltooid, wordt een werk-id gemaakt voor werk met zes regels. De regels worden gesorteerd op artikelnummer.

1. Ga naar **Magazijnbeheer \> Werk \> Alle werkzaamheden** om het gemaakte werk weer te geven. Noteer de waarde van de **Werk-id** omdat u deze in de volgende procedure nodig hebt.

### <a name="initiate-picking-from-the-mobile-device"></a>Order verzamelen starten vanaf het mobiele apparaat

1. Meld u aan bij het mobiele apparaat als een gebruiker met instellingen voor magazijn *51*.
1. Selecteer op het mobiele apparaat het menu dat de nieuwe menuoptie voor mobiele apparaten bevat. Selecteer voor dit scenario **Uitgaand**.
1. Selecteer de menuopdracht **Orderverzameling voor verkoopgroepsregels** en initieer de orderverzameling.
1. Voer de waarde van de **werk-ID** in die u in de vorige procedure hebt genoteerd.

    U ziet een verzamelstap waarin alle orderverzamelregels voor artikel *M9200* worden gegroepeerd, en u moet een instructie ontvangen om van elk artikel *M9200* *7* te verzamelen.

    > [!IMPORTANT]
    > Op het mobiele apparaat is de orderverzameling voor de drie verzamelwerkregels samengevoegd in één verzamelstap voor de gebruiker.

1. Bevestig de verzamelstap.
1. Ga naar de werkpagina voor de werk-id. U ziet dan dat alle drie de orderverzamelregels voor artikel *M9200* tegelijkertijd zijn gesloten.
1. Ga terug naar het mobiele apparaat en ga verder met verzamelen. Werkregel 4 voor artikel *M9201* moet worden weergegeven. Aangezien de order slechts één werkregel heeft, hoeft er niets te worden samengevoegd.
1. Bevestig de verzamelstap.
1. Met de laatste orderverzamelstap op het mobiele apparaat worden de laatste twee orderverzamelregels uit de werkorder samengevoegd.
1. Voltooi de orderverzamelstap voor *9* stuks van artikel *M9202*.
1. Bevestig de wegzetstap en eventuele extra verzamel-/wegzetparen om het werk te voltooien.

> [!IMPORTANT]
>
> - Werkregels kunnen alleen worden gegroepeerd als ze op volgorde zijn.
> - De volgende functionaliteit wordt niet ondersteund:
>
>   - Catch weight-artikelen.
>
>    Als er catch weight-artikelen voor het werk aanwezig zijn, wordt een foutbericht weergegeven voordat u begint te kiezen.
>
>   - Orderverzameling
>   - Werkregels met onvoltooid aanvullingswerk
>   - Meerverzameling
>   - Kort orderverzamelen met artikelhertoewijzing


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
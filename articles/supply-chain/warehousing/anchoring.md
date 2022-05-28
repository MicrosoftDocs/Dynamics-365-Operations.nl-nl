---
title: Verankering
description: In dit onderwerp wordt uitgelegd hoe een verankering gebruikt en inschakelt.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 26a7bf60912ff1e8a23305e9331d520fe8d65727
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676490"
---
# <a name="anchoring"></a>Verankering

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het proces van verankering. Het beschrijft de vereiste configuratie en de logica die wordt uitgevoerd wanneer een magazijnmedewerker de klaarzetlocatie of de laadlocatie wijzigt.

Met de verankeringsfunctie kunt u de klaarzetlocatie of laadlocatie overschrijven. Alle openstaande ladingen worden vervolgens doorgestuurd naar de nieuwe klaarzetlocatie of laadlocatie die u opgeeft.

Deze functie kan werknemers efficiënter maken wanneer ze goederen verzenden. Hieronder volgen een aantal voorbeelden:

- Een werknemer die artikelen voor order 1 in een klaarzetlocatie bij Dok 1 moet zetten, maar dat niet kan omdat een vorige lading de locatie niet heeft vrijgemaakt. In plaats van te wachten totdat de klaarzetlocatie Dok 1 beschikbaar komt, besluit de werknemer de klaarzetlocatie voor Dok 2 te gebruiken. In dat geval negeert de werknemer de voorgestelde klaarzetlocatie. De neerzetlocatie voor alle resterende artikelen voor het werk wordt dan bijgewerkt naar de klaarzetlocatie Dok 2.
- Als een werknemer meerdere taken moet uitvoeren voor dezelfde levering, kan deze er zeker van zijn dat alle neergezette artikelen op dezelfde plaats worden verzameld. Daarom is er minder tijd nodig om de artikelen in de truck te laden.

U configureert verankering voor menuopties van mobiele apparaten met de optie **Verankeren**. Als u deze optie instelt op *Ja*, selecteert, kunt in het veld **Verankeren volgens** opgeven of u wilt verankeren op zending of lading. Als u het veld **Verankeren volgens** instelt op *Zending*, worden de volgende openstaande wegzetlocaties gewijzigd in de nieuwe locatie voor die zending. Als u het veld instelt op *Laden*, worden de volgende openstaande wegzetlocaties gewijzigd in de nieuwe locatie voor die lading.

> [!IMPORTANT]
> De volgende open wegzetlocatie wordt alleen gewijzigd op de werkregels die worden gegenereerd vanuit dezelfde werksjabloonregel. Met andere woorden, het systeem verankert de neerzetregels die afkomstig zijn van dezelfde werksjabloonregel.

Dit onderwerp biedt een scenario dat laat zien hoe verankering werkt. Tijdens het scenario maakt u een set verkooporders en geeft u deze set vrij naar het magazijn. Vervolgens overschrijft u de voorgestelde klaarzetlocatie en controleert u of alle resterende neerzetwerkzaamheden zijn overgeplaatst naar de nieuwe locatie.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Vereiste voor scenario: demonstratiegegevens beschikbaar maken

Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op *USMF* voordat u begint.

## <a name="scenario-setup"></a>Scenario instellen

Voordat u het voorbeeldscenario doorwerkt, moet u Verankeren inschakelen voor de relevante menuopdracht op uw mobiele apparaat.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Een menuopdracht voor een mobiel apparaat instellen om verankering in te schakelen

Volg deze stappen om verankering in te schakelen voor een menu-item van een mobiel apparaat.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het lijstdeelvenster de record met de naam *Orderverzamelen*. Als er geen record bestaat met deze naam, maakt u deze record. De volgende waarden voor de record bevestigen of instellen:

    - **Naam menuopdracht:** *Orderverzamelen*
    - **Titel:** *Orderverzamelen*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Ja*
    - **Bestuurd door:** *Door gebruiker bestuurd*
    - **Verankeren:** *Ja*

        Deze instelling zorgt ervoor dat het systeem meerdere werkorderregels verankert bij het verzamelen van verkoop.

    - **Verankeren volgens:** *Lading*

        Deze instelling zorgt ervoor dat het systeem verankert per lading.

    - **Doelnummerplaat overschrijven:** *Ja*
    - **Doelnummerplaat overschrijven tijdens wegzetten:** *Ja*
    - **Werk door gebruiker vergrendeld houden:** *Ja*
    - **Oververzamelen toestaan:** *Ja*

### <a name="set-up-a-work-template-to-enable-staging"></a>Een werksjabloon instellen om klaarzetten in te stellen

Volg deze stappen om een werksjabloon te configureren om klaarzetten in te schakelen. Deze configuratie ondersteunt het scenario waarin een werknemer artikelen voor een order op een klaarzetlocatie plaatst.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Selecteer *Verkooporders* in het veld **Werkordertype**.
1. Selecteer in het raster de werksjabloon **61 SO Stage**.
1. Zorg er in het gedeelte **Werksjabloondetails** voor dat de volgende regels bestaan en zijn geconfigureerd zoals hier wordt weergegeven:

    - Regel 1:

        - **Werktype:** *Orderverzamelen*
        - **Verplicht:** geselecteerd (= *Ja*)
        - **Werkklasse-id:** *VO verzamelen*

    - Regel 2:

        - **Werktype:** *Wegzetten*
        - **Verplicht:** geselecteerd (= *Ja*)
        - **Instructiecode:** *Klaarzetten*
        - **Werkklasse-id:** *VO verzamelen*

    - Regel 3:

        - **Werktype:** *Orderverzamelen*
        - **Verplicht:** geselecteerd (= *Ja*)
        - **Werken stoppen:** *Ja*
        - **Werkklasse-id:** *SO laden*

    - Regel 4:

        - **Werktype:** *Wegzetten*
        - **Verplicht:** geselecteerd (= *Ja*)
        - **Richtlijncode:** *Laaddeur*
        - **Werkklasse-id:** *SO laden*

1. Selecteer in het actievenster de optie **Query bewerken** om de Power Query-editor te openen.
1. Controleer of op het tabblad **Bereik** de volgende twee regels aanwezig zijn:

    - **Tabel:** *Tijdelijke werktransacties*
    - **Afgeleide tabel:** *Tijdelijke werktransacties*
    - **Veld:** *Magazijn*
    - **Criteria:** *61*

1. Controleer of op het tabblad **Sortering** de volgende twee regels aanwezig zijn:

    - **Tabel:** *Tijdelijke werktransacties*
    - **Afgeleide tabel:** *Tijdelijke werktransacties*
    - **Veld:** *Zending-id*
    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om de instellingen toe te passen en de query-editor te sluiten. Accepteer de wijzigingen als u hier om wordt gevraagd.
1. Selecteer **Opsplitsingen voor werkkoptekst** in het actievenster.
1. Schakel op de regel waarvoor het veld **Veldnaam** is ingesteld op *Zending-id* het selectievakje **Groeperen op dit veld** in.

### <a name="set-up-license-plates-locations-and-inventory"></a>Nummerplaten, locaties en voorraad instellen

Voordat u verkooporders en zendingen maakt, moet u ervoor zorgen dat de vereiste locaties, nummerplaten en voorraad aanwezig zijn.

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Nummerplaten** en maak twee nummerplaten:

    - MyLP1
    - MyLP2

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**, en maak de volgende locaties als deze nog niet aanwezig zijn.

    | Magazijn | Locatie   | Locatieprofiel-id | Zone-id   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | VERDIEPING     |
    | 61        | 06A01R3S1B | PICK-06             | VERDIEPING     |
    | 61        | STAGE01    | STAGE               | *(Leeg)* |
    | 61        | STAGE02    | STAGE               | *(Leeg)* |
    | 61        | STAGE03    | STAGE               | *(Leeg)* |
    | 61        | STAGE04    | STAGE               | *(Leeg)* |

1. Controleer of de volgende voorraad beschikbaar is. Als u de voorraad moet corrigeren, kunt u handmatige verplaatsingen maken en aanvulling of elke andere stroom gebruiken.

    | artikelnummer | Hoeveelheid | Magazijn | Locatie   | Nummerplaat |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Vraag maken

Voordat u de functionaliteit verankering kunt uitproberen, moet u een bepaalde vraag maken. Voor dit scenario maakt u drie verkooporders voor dezelfde klant.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om de eerste verkooporder te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *61*

1. Selecteer **OK**.
1. De nieuwe verkooporder wordt geopend. Deze bevat een lege rij in het sneltabblad **Verkooporderregels**. Stel de volgende waarden in voor deze regel:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *1*

1. Op de werkbalk, selecteer **Regel toevoegen** om een tweede verkooporderregel toe te voegen en stel hiervoor de volgende waarden in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *1*

1. Volg deze stappen voor elke verkoopregel op de order om de voorraad te reserveren:

    1. Selecteer een verkooporderregel in het sneltabblad **Verkooporderregels**.
    1. Selecteer op de werkbalk **Voorraad \> Reservering**.
    1. Ga naar de pagina **Reservering** en selecteer de optie **Partij reserveren** en sluit de pagina vervolgens.
    1. Selecteer **Opslaan** in het actievenster.

1. Herhaal stap 2 tot en met 6 om een tweede verkooporder te maken. Stel de volgende waarden in:

    - In het dialoogvenster **Verkooporder maken**:

        - **Klantrekening:** *US-001*
        - **Magazijn:** *61*

    - Op verkooporderregel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *2*

    - Op verkooporderregel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *2*

1. Herhaal stap 7 om elke regel op verkooporder 2 te reserveren.
1. Herhaal stap 2 tot en met 6 om een derde verkooporder te maken. Stel de volgende waarden in:

    - In het dialoogvenster **Verkooporder maken**:

        - **Klantrekening:** *US-001*
        - **Magazijn:** *61*

    - Op verkooporderregel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *3*

    - Op verkooporderregel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *3*

1. Herhaal stap 7 om elke regel op verkooporder 3 te reserveren.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>De workbench voor ladingplanning gebruiken om een lading te maken en vrij te geven naar het magazijn

Voer de deze stappen uit om een lading te maken voor de orders die u voor dit scenario hebt gemaakt en vervolgens vrij te geven naar het magazijn.

1. Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.
1. Op het tabblad **Verkoopregels** kunt u alle verkooporderregels zoeken en selecteren voor verkooporder 1 en verkooporder 2.
1. Selecteer in het actievenster op het tabblad **Vraag en aanbod** in de groep **Toevoegen** de optie **Aan nieuwe lading**.
1. Selecteer in het dialoogvenster **Ladingsjabloon toewijzen** in het veld **Ladingsjabloon-id** een ladingssjabloon, zoals *Standaardladingssjabloon*.
1. Selecteer **OK** om het dialoogvenster te sluiten.
1. In de sectie **Ladingen** zoekt en selecteert u de lading die u hebt gemaakt.
1. Selecteer **Vrijgeven \> Vrijgeven aan magazijn** op de werkbalk.
1. Selecteer **OK** in het dialoogvenster **Lading vrijgeven aan magazijn** om de geselecteerde lading vrij te geven aan het magazijn.
1. Ga naar **Magazijnbeheer \> Werk \> Alle werkzaamheden** om het gemaakte werk weer te geven. U moet twee nieuwe werk-id's zoeken, één voor elke zending. Elke werk-id heeft verzamel- en neerzetregels die voorraad brengen van de verzamellocaties naar de klaarzetlocatie en van de klaarzetlocatie naar de laaddeur. Noteer de waarde van de **Werk-id** omdat u deze in de volgende procedure nodig hebt voor de eerste zending.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Verkooporder verzamelen naar de klaarzetlocatie voor de eerste zending

1. Meld u aan bij de mobiele app Warehouse Management als werknemer in magazijn *61*. (In de standaard demogegevens kunt u zich aanmelden aan met _61_ als gebruikers-id en _1_ als wachtwoord.)
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer **Orderverzamelen** in het menu **Uitgaand**.
1. Selecteer het veld **Id** en voer de werk-id in van de eerste zending.
1. Bevestig uw invoer.
1. Voer in het veld **NP** een nummerplaatnummer in voor het eerste artikel (*MyLP1*).
1. Bevestig uw invoer.
1. Voer in het veld **Doel-NP** een nummer in (het doelnummer hoeft nog niet te bestaan).

    U gaat alle regels verzamelen die van de verwerkte wave op dezelfde doelnummerplaat zijn gemaakt.

1. Bevestig uw invoer.
1. Voer in het veld **NP** een nummerplaatnummer in voor het tweede artikel (*MyLP2*).
1. Bevestig uw invoer.

    Stel dat werknemers de order hebben verzameld, maar als ze op de klaarzetlocatie komen die in het werk is opgegeven, zien ze dat de ruimte al is bezet. De werknemer kan echter zien dat er een andere locatie in de buurt beschikbaar is (*STAGE03*). Daarom vragen ze een wijziging van de klaarzetlocatie aan. Aangezien de verankeringsfunctie is ingeschakeld, wordt de klaarzetlocatie voor dit en alle gerelateerde werk automatisch bijgewerkt.

1. Selecteer **Overschrijven locatie** om de voorgestelde klaarzetlocatie te overschrijven.
1. Geef in het veld **Werkuitzonderingen** op *Klaarzetlaan gewijzigd*.
1. Geef in het veld **Locatie** een nieuwe klaarzetlocatie op (*STAGE03*).
1. Bevestig uw invoer. U ziet de melding "Werk voltooid".
1. Ga naar **Magazijnbeheer \> Werk \> Alle werk**.
1. Open de werk-id voor de eerste zending. Controleer of de klaarzetlocatie is bijgewerkt naar de nieuwe locatie (*STAGE03*) die is gedefinieerd met het mobiele apparaat.
1. Open de werk-id voor de tweede zending. Controleer of de klaarzetlocatie is bijgewerkt naar een nieuwe klaarzetlocatie (*STAGE03*) vanwege de verankeringsinstellingen.

> [!NOTE]
> De locatie van alle resterende openstaande werkregels met dezelfde klaarzetlocatie en die zijn gegenereerd op basis van dezelfde werksjabloonregel, wordt naar de nieuwe locatie bijgewerkt.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Gebruik de workbench voor ladingplanning om de nieuwe verkooporder aan de bestaande lading toe te voegen

Volg deze stappen om een order toe te voegen aan de lading en deze vervolgens vrij te geven aan het magazijn.

1. Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.
1. Op het tabblad **Verkoopregels** kunt u alle verkooporderregels zoeken en selecteren voor verkooporder 3.
1. Selecteer in het actievenster op het tabblad **Vraag en aanbod** in de groep **Toevoegen** de optie **Aan nieuwe lading** om de geselecteerde orderregels aan een bestaande lading toe te voegen.
1. Selecteer **OK** om het dialoogvenster te sluiten.
1. In de sectie **Ladingen** zoekt en selecteert u de lading die u in de vorige stappen hebt gemaakt.
1. Selecteer **Vrijgeven \> Vrijgeven aan magazijn**.
1. Selecteer **OK** in het dialoogvenster **Lading vrijgeven aan magazijn** om de geselecteerde lading vrij te geven aan het magazijn.
1. Ga naar **Magazijnbeheer \> Werk \> Alle werkzaamheden** om het gemaakte werk weer te geven. Noteer de waarde van de **Werk-id** omdat u deze in de volgende procedure nodig hebt.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Verkooporder verzamelen naar de klaarzetlocatie voor de derde zending

1. Meld u aan bij de mobiele app als een medewerker in magazijn *61*.
1. Selecteer **Uitgaand** in het hoofdmenu.
1. Selecteer **Orderverzamelen** in het menu **Uitgaand**.
1. Selecteer het veld **Id** en voer de werk-id in van de derde zending.
1. Bevestig uw invoer.
1. Voer in het veld **NP** een nummerplaatnummer in voor het eerste artikel (*MyLP1*).
1. Bevestig uw invoer.
1. Voer in het veld **Doel-NP** een nummer in (het doelnummer hoeft nog niet te bestaan).
1. Bevestig uw invoer.
1. Voer in het veld **NP** een nummerplaatnummer in voor het tweede artikel (*MyLP2*).
1. Bevestig uw invoer.

    Stel dat net als bij de eerste lading dat de werknemer ziet dat de opgegeven klaarzetlocatie niet beschikbaar is. Daarom willen ze een andere klaarzetlocatie gebruiken (*STAGE04*).

1. Selecteer **Overschrijven locatie** om de voorgestelde klaarzetlocatie te overschrijven.
1. Geef in het veld **Werkuitzonderingen** op *Klaarzetlaan gewijzigd*.
1. Geef in het veld **Locatie** een nieuwe klaarzetlocatie op (*STAGE04*).
1. Bevestig uw invoer. U ziet de melding "Werk voltooid".
1. Ga naar **Magazijnbeheer \> Werk \> Alle werk**.
1. Open de werk-id voor de eerste zending. Controleer of de klaarzetlocatie niet is bijgewerkt naar de nieuwe klaarzetlocatie (*STAGE04*), omdat de resterende openstaande wegzetregel niet overeenkomt met de werksjabloonregel van de voltooide wegzetregel.
1. Open de werk-id voor de tweede zending. Controleer of de klaarzetlocatie niet is bijgewerkt naar de nieuwe klaarzetlocatie (*STAGE04*), omdat de klaarzetlocatie niet overeenkomt met de klaarzetlocatie van de voltooide wegzetregel. Met andere woorden de voltooide wegzetwerkregel en de resterende openstaande werkregel hebben verschillende klaarzetlocaties. In dit geval worden alleen regels met dezelfde klaarzetlocatie bijgewerkt.
1. Open de werk-id voor de derde zending. Controleer of de klaarzetlocatie is bijgewerkt naar de nieuwe klaarzetlocatie (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

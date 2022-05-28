---
title: Oververzamelen voor verkooporders en overboekingsorders
description: In dit onderwerp wordt uitgelegd hoe u meer- of oververzameling van orders voor verkoop- en overboekingsorders kunt inschakelen.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 52a4225efa88a7b9303dd611d5652f59da1612a4
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678403"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Oververzamelen voor verkooporders en overboekingsorders

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft een scenario weer dat laat zien hoe u een bepaalde werknemer of alle werknemers meer kunt laten verzamelen. Met het meerverzamelingsproces kunnen op gecontroleerde wijze meerdere artikelen worden verzameld tijdens het verzamelen.

Meerverzamelen in magazijnen is een eenvoudig concept. Werknemers kunnen door het systeem meer artikelen verzamelen dan voor een order zijn opgegeven. Er wordt echter nog steeds rekening gehouden met de meerleveringslimiet die is ingesteld op het regelniveau voor de overboekings- of verkooporder. Als die limiet wordt overschreden, meldt de Warehouse Management-app aan de medewerkers dat ze de meerleveringslimiet overschrijden.

De functie voor meerverzameling zorgt voor minder onderhoud en helpt bovendien bij flexibel instellen. U kunt een of meer menuopdrachtens van een mobiel apparaat definiëren en het meerverzamelen inschakelen voor slechts enkele items. U kunt ook voorkomen dat geselecteerde werknemers te veel verkooporders en/of overboekingsorders verzamelen zonder dat u de menuopdrachtens hoeft te wijzigen. In plaats daarvan kunt u een of beide capaciteiten in de relevante werknemerinstellingen uitschakelen.

De functie voor het meerverzamelen van artikelen kan werknemers helpen tijd en moeite te besparen bij het verzamelen en verzenden van artikelen. Werknemers kunnen door deze functie bijvoorbeeld de volgende taken uitvoeren:

- Verlies compenseren tijdens het verzamelen of verzenden.
- Uitpakken van bepaalde verpakkingsmateriaal voorkomen tijdens orderverzameling.
- Compensatie van artikelschade tijdens het transport.
- Een afwijking in de hoeveelheid of maateenheid verzenden.
- Breuk van hoeveelheden op nummerplaten minimaliseren.
- Vermijden van materiaalverlies en schaarste van dure materialen.
- De verzamelde hoeveelheid meten na het verzamelen (bijvoorbeeld via wegen van vrachtwagen).

> [!IMPORTANT]
> De functie voor oververzamelen is alleen van toepassing op het verzamelen en verwerken van verkooporders en overboekingsorders. Aanvulling biedt geen ondersteuning voor te oververzamelen. Wanneer aanvullingswerkzaamheden worden uitgevoerd, mogen gebruikers niet oververzamelen.

Dit onderwerp bespreekt een scenario waarin wordt uitgelegd hoe de functie voor oververzamelen wordt ingesteld en gebruikt.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Vereiste voor scenario: demonstratiegegevens beschikbaar maken

Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op *USMF* voordat u begint.

## <a name="scenario-setup"></a>Scenario instellen

Voordat u het voorbeeldscenario doorwerkt, moet u oververzamelen inschakelen voor de relevante werknemer en de relevante menuopdracht.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Een werknemer instellen voor oververzamelen

Hier is de algemene procedure voor het configureren van een werknemer voor het afzonderlijk oververzamelen voor verkooporders en overboekingsorders. Deze configuratie bepaalt welke orderpickers kunnen meerverzamelen en of die medewerkers dat kunnen doen voor zowel overboekings- als verkooporders.

1. Ga naar **Magazijnbeheer \> Instellen \> Medewerker**.
1. Selecteer in het lijstvenster **Julia Funderburk**.
1. Selecteer op het sneltabblad **Gebruikers** de rij met de volgende waarden. Als er geen bestaande rij is met deze waarden, maakt u deze rij.

    - **Gebruikers-id:** *24*
    - **Gebruikersnaam:** *WH 24*
    - **Standaardmagazijn:** *24*
    - **Menunaam:** *Hoofd*

1. Stel op het sneltabblad **Werk** de volgende waarden in voor gebruiker *24* als deze nog niet zijn ingesteld:

    - **Oververzamelen van verkooporders toestaan:** *Ja*
    - **Oververzamelen van overboekingsorders toestaan:** *Ja*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Een menuopdracht voor een mobiel apparaat instellen op oververzamelen

Hier is de algemene procedure voor het configureren van een menuopdracht van een mobiele apparaat om het oververzamelen van orders in te stellen. Afhankelijk van uw bedrijfvereisten voor het machtigingsniveau van de medewerker die het menu voor mobiele apparaten gebruikt, kunnen sommige parameters in- of uitgeschakeld zijn.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het lijstdeelvenster de record met de naam *Orderverzamelen*. Als er geen record bestaat met deze naam, maakt u deze record. De volgende waarden voor de record bevestigen of instellen:

    - **Naam menuopdracht:** *Orderverzamelen*
    - **Titel:** *Orderverzamelen*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Ja*
    - **Bestuurd door:** *Door gebruiker bestuurd*
    - **Doelnummerplaat overschrijven:** *Ja*
    - **Doelnummerplaat overschrijven tijdens wegzetten:** *Ja*
    - **Werk door gebruiker vergrendeld houden:** *Ja*
    - **Oververzamelen toestaan:** *Ja*

> [!IMPORTANT]
> Nadat de relevante parameters voor zowel de medewerker als de menuopdracht van het mobiele apparaat zijn ingeschakeld, kan oververzamelen alleen worden verwerkt via het mobiele apparaat.

## <a name="example-scenario"></a>Voorbeeldscenario

Wanneer de vereisten, werknemerinstellingen en menuopdrachtinstellingen zijn ingesteld, kunt u met de functie werken.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Een verkooporder maken voor meerlevering

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** voor het maken van een nieuwe verkooporder.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *24*

1. Selecteer **OK**.
1. De nieuwe verkooporder wordt geopend. Voeg op het sneltabblad **Verkooporderregels** een regel toe met de volgende instellingen:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *10*

1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Meerlevering** in op *10*.
1. Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.
1. Sluit de pagina **Reservering**.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

Als de vrijgave is voltooid, ontvangt u een informatieve melding waarin de wave- en ladings-id's worden vermeld die zijn gemaakt.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Haal de werk-ID en het nummerplaatnummer voor de nieuwe order op

Wanneer u de verkooporder naar het magazijn hebt vrijgegeven, moet er een nieuwe werk-ID zijn gemaakt met één orderpickregel. Voer de volgende stappen uit om de toewijzingen van werk-ID's en nummerplaten te vinden.

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Zoek in raster **Overzicht** de kolom **Ordernummer** voor de verkooporder die u zojuist hebt gemaakt. Noteer voor die verkooporder de bijbehorende werk-ID.
1. Selecteer de rij voor de nieuwe verkooporder om gerelateerde informatie weer te geven in het raster **Regels**. Noteer de locatie waar het artikel wordt verzameld.
1. Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden voorraad**.
1. Selecteer in het actievenster de optie **Dimensies**.
1. Controleer of in het dialoogvenster **Weergave van dimensies** de selectievakjes **Nummerplaat**, **Magazijn** en **Artikelnummer** zijn ingeschakeld en selecteer **OK**.
1. Stel in het deelvenster **Filter** de volgende filters in:

    - **Artikelnummer** – **is één van** – *A0001*
    - **Magazijn** – **begint met** – *24*

1. Selecteer **Toepassing**.
1. Noteer de weergegeven waarden voor **Nummerplaat**.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Oververzamel de order met de Warehouse Management-app

1. Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker in magazijn *24*.
1. Ga naar **Uitgaand \> Orderverzamelen**.
1. Voer in het veld **Werk-ID of nummerplaat scannen** de werk-ID in die voor de verkooporder is gemaakt.
1. Selecteer **OK** (symbool voor vinkje).
1. Selecteer **Oververzamelen**.
1. Stel het veld **Verzamelhoeveelheid** in op *14*.
1. Selecteer **OK** (symbool voor vinkje).

    Op de pagina **Oververzamelen** ontvangt u het volgende bericht: "De meerlevering van de regel is 40,00 procent, maar de toegestane meerlevering is slechts 10,00 procent." Dit bericht geeft aan dat de ingevoerde verzamelhoeveelheid de limiet voor meerlevering overschrijdt. De meerleveringslimiet voor de verkooporderregel is 10 procent. Daarom kunt u voor een opgegeven hoeveelheid van 10 niet meer dan 1 extra ophalen, voor een totale verzamelhoeveelheid van 11.

1. Stel het veld **Verzamelhoeveelheid** in op *11*.
1. Selecteer **OK** (symbool voor vinkje).
1. Voer in het veld **Nummerplaat** de nummerplaat in die u in de vorige sectie hebt genoteerd.
1. Voer in het veld **Doelnummerplaat** de ID van de doelnummerplaat in. U ziet dat de orderverzamellocatie (*VLOER-001*), artikel (*A0001*) en hoeveelheid (*11 stuks*) worden weergegeven.
1. Selecteer **OK** (symbool voor vinkje).
1. Bekijk de informatie op de pagina **Verkooporders: wegzetten**. Het veld **Loc** moet aangeven dat de verzamelde artikelen naar de *LAADDEUR*-locatie gaan.
1. Selecteer **OK** (symbool voor vinkje).

Op de pagina **Een werk-id/nummerplaat-id scannen** ontvangt u het bericht "Werk voltooid". Dit bericht geeft aan dat de werk-ID van de verkooporder is voltooid en dat de meerverzamelde hoeveelheid de limiet van meer dan 10 procent niet overschrijdt.

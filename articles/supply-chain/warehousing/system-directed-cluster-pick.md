---
title: Door systeem gestuurde clusterverzameling
description: In dit onderwerp vindt u een overzicht van door het systeem gestuurde clusterverzameling in Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: cc634b82a64b7774abc1538e034f1b8289176f4e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831141"
---
# <a name="system-directed-cluster-picking"></a>Door systeem gestuurde clusterverzameling

[!include [banner](../includes/banner.md)]

Clusterverzameling is een proces voor stuksverzameling waarmee u artikelen voor meerdere orders tegelijk kunt kiezen door ze te clusteren in verzamelclusters. U hoeft de orderverzamellocatie in dat geval slechts één keer te bezoeken. Deze functionaliteit wordt meestal gebruikt bij het verzamelen van kleine orders of aantallen die kleiner zijn dan aanvraaghoeveelheden.

Wanneer door het systeem gestuurde clusterverzameling is ingesteld, u werkkopteksten in clusters verzamelen, op basis van een door het systeem gegenereerd cluster. Orders worden in clusters verzameld tot het aantal posities dat is opgegeven in het clusterprofiel. Daarom kunt u meerdere orders op hetzelfde moment verzamelen zonder handmatig een cluster te hoeven maken.

Door het systeem gestuurde clusterverzameling biedt een alternatief voor het handmatig maken van clusters, waarbij een clusterprofiel wordt gebruikt om een cluster te maken. Er moeten verschillende instellingsregels in het clusterprofiel worden gedefinieerd voordat dit profiel wordt gebruikt:

- **Aantal posities** komt overeen met het aantal orders dat in een cluster wordt geplaatst. Daarom komt het overeen met het aantal totes.
- **Cluster opsplitsen** bepaalt wanneer het cluster moet worden opgesplitst.
- **Cluster-id maken** bepaalt of de cluster-id wordt gegenereerd door het systeem of ingevoerd door de gebruiker.
- **Verificatietype sorteren** bepaalt of positieverificatie vereist is.

Een nieuw menu-item voor mobiele apparaten wordt gebruikt voor door het systeem gestuurde clusterverzameling. De **clusterprofiel-id** moet worden opgegeven voor de geselecteerde optie **Bestuurd door**. Bovendien kunnen met de door het systeem gestuurde werkreeksquery's orders worden gegroepeerd op basis van bedrijfsspecifieke criteria. Daarom kunt u de toewijzing van werkorders verder optimaliseren door aangepaste sorteercriteria op te geven met de door het systeem gestuurde werkreeksquery's.

Wanneer de door het systeem gestuurde clusterverzameling is ingeschakeld, krijgen magazijnmedewerkers een cluster voorgeschoteld waarin orderverzamelorders vooraf zijn toegewezen aan clusterposities. Daarom kunnen medewerkers beginnen met het verzamelen van een artikel voor meerdere werkorders door slechts één keer naar de orderverzamellocatie te gaan. Het orderverzamelproces voor door het systeem gestuurde clusterverzameling is hetzelfde als het proces voor door de gebruiker gestuurde clusterverzameling.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>De functie Door systeem gestuurde clusterverzameling inschakelen

Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem. Beheerders kunnen gebruikmaken van de pagina voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen. Hier ziet u de functie als:

- **Module** - Magazijnbeheer
- **Functienaam** - Door systeem gestuurde clusterverzameling

Voor deze functie moet ook een afhankelijke functie worden ingeschakeld. De afhankelijke functie is:

- **Module** - Magazijnbeheer
- **Functienaam** - Organisatiebrede, door het systeem gestuurde werkvolgorde

## <a name="set-up-system-directed-cluster-picking"></a>Door systeem gestuurde clusterverzameling instellen

### <a name="create-cluster-profiles"></a>Clusterprofielen maken

Clusterprofielen bepalen hoe het systeem elk cluster maakt. Als verschillende clusters vereist zijn, moet voor elk menu-item van het mobiele apparaat een ander clusterprofiel worden gemaakt.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Clusterprofielen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Profiel-id van cluster** de tekst **2 positie** in.
4. Voer in het veld **Naam** de tekst **2 positie** in.
5. Voer de volgende informatie in op het sneltabblad **Algemeen**:

    - **Cluster-id maken**: selecteer **Ja**. Met deze optie bepaalt u of de cluster-id automatisch wordt gemaakt door het systeem of dat de gebruiker deze maakt bij het begin van het orderverzamelen. 
    - **Posities activeren**: selecteer **Ja**. Met deze optie bepaalt u of de positienamen automatisch worden gegenereerd op basis van de instellingen voor positienamen. Als deze optie is ingesteld op **Nee**, wordt de nummerplaat-id gebruikt voor de positie.
    - **Aantal posities:** selecteer **2**. Dit veld bepaalt het maximum aantal posities dat het cluster kan hebben (het maximum aantal vakken, totes, enzovoort).
    - **Positienaam**: selecteer **Numeriek** zodat posities worden benoemd op basis van doorlopende nummers. Als u **Alfabetisch** selecteert, worden de posities in alfabetische volgorde benoemd.
    - **Cluster opsplitsen bij**: selecteer **Wegzetten**. Dit veld bepaalt wanneer het cluster wordt opgesplitst. 
    - **Verificatietype sorteren**: selecteer **Positie scannen**. Met dit veld bepaalt u of de stap voor wegzetten naar positie wordt geverifieerd.
        
6. Op het sneltabblad **Clustersortering** kunt u sorteercriteria definiëren door een nieuwe regel te maken en de volgende velden informatie op te geven:

    - **Volgnummer**: selecteer **1**. Dit veld bepaalt de volgorde waarop het systeem sorteert. Er wordt automatisch een waarde ingevoerd, maar u kunt desgewenst wijzigen.
    - **Veldnaam:** voer **WMSLocationId** in. Met dit veld bepaalt u welk veld door de regel wordt gebruikt voor sorteercriteria.
    - **Sorteren:** selecteer **Oplopend**. Met dit veld bepaalt u of de sortering in oplopende of aflopende volgorde wordt uitgevoerd.

### <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken

Ga als volgt te werk als u een nieuw menu-item voor mobiele apparaten wilt maken voor door het systeem gestuurde clusterverzameling en de clusterprofiel-id aan het menu-item van het mobiele apparaat wilt koppelen.

1. Ga naar **Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw**.
1. Voer in de koptekstsectie de volgende informatie in:
    - **Menuoptie**: SD-cluster
    - **Titel**: SD-cluster
    - **Modus**: Werk
    - **Bestaand werk gebruiken**: Ja

1. Voer de volgende informatie in op het sneltabblad **Algemeen**:
    - **Gestuurd door:** Door systeem gestuurde clusterverzameling
    - **Nummerplaat maken**: Ja
    - **Clusterprofiel-id:** 2 positie

1. Stel op het sneltabblad **Werkklassen** de geldige werkklasse voor deze menuopdracht voor mobiel apparaten in door de volgende velden in te stellen:
    - **Werkklasse-id**: Verkoop
    - **Werkordertype**: Verkooporders

1. Selecteer in het actievenster **Menuopties voor mobiel apparaat** de optie **Door het systeem gestuurde werkreeksquery's** en voer deze stappen uit om een nieuwe systeemgestuurde werkreeksquery op te geven:
    - Selecteer **Nieuw** in het actievenster.
    - **Volgnummer:** 1
    - **Omschrijving:** Werkprioriteit – Werk-id

1. Selecteer **Query bewerken** in het actievenster.
1. Selecteer het tabblad **Sortering**.
1. Selecteer **Toevoegen** om een nieuwe regel toe te voegen en voer vervolgens het volgende in:
    - **Tabel**: Werk
    - **Afgeleide tabel:** Werk
    - **Veld**: Werkprioriteit
    - **Zoekrichting:** Oplopend
1. Selecteer **Toevoegen** om een tweede regel toe te voegen en voer vervolgens het volgende in:
    - **Tabel**: Werk
    - **Afgeleide tabel:** Werk
    - **Veld:** Werk-id
    - **Zoekrichting:** Oplopend

1. Het systeem sorteert werk-id's nu in het cluster, eerst op werkprioriteit en vervolgens op werk-id.

### <a name="set-up-a-mobile-device-menu"></a>Een menu van een mobiel apparaat instellen

1. Ga naar **Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat**.
1. Voeg de menuoptie **SD-cluster** die u net hebt gemaakt toe aan een menu Mobiel apparaat.
1. Selecteer het menu **Uitgaand**.
1. Selecteer **Bewerken** in het actievenster.
1. Blader tot u **SD-cluster** hebt gevonden.
1. Selecteer **SD-cluster**. De pijl die naar de lijst **Menustructuur** wijst, wordt ingeschakeld.
1. Selecteer de **pijlknop** om het menu-item **SD-cluster** te verplaatsen naar de menustructuur **Uitgaand**.
1. Selecteer **SD-cluster** in de lijst **Menustructuur** en selecteer vervolgens de **pijl-omhoog** of **pijl-omlaag** om de menuopdracht naar de gewenste positie in het menu voor mobiele apparaten te verplaatsen.

## <a name="scenario"></a>Scenario's

### <a name="create-picking-work"></a>Orderverzamelingswerk maken

Voordat u door het systeem gestuurde clusterverzameling kunt instellen, moet u in aanmerking komend uitgaand werk maken. Met het clusterprofiel dat u eerder hebt gemaakt, worden twee clusterposities opgegeven. Daarom moet u ten minste twee werk-id's maken. In dit scenario maakt u twee verkooporders, reserveert u voorraad, geeft u de verkooporders vrij naar het magazijn en verwerkt u de wave vervolgens handmatig.

1. Ga naar **Verkoop en marketing > Verkooporders > Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster om de eerste verkooporder te maken.
    - Het menu **Verkooporder maken** wordt geopend. Hierin voert u de volgende gegevens in:
        - Op het sneltabblad **Klant** voert u **Klantrekening** - **US-004** in.
        - Op het sneltabblad **Algemeen** voert u **Magazijn** - **62** in.
        - Selecteer **OK** om het menu te sluiten en de verkooporder te maken.
    - Selecteer op het sneltabblad **Verkooporderregels** de optie **Regel toevoegen** als niet automatisch een nieuwe regel wordt toegevoegd en voer het volgende in:
        - **Artikelnummer** - A0001
        - **Hoeveelheid** - 1
        - Selecteer **Regel toevoegen** om een tweede regel toe te voegen.
        - **Artikelnummer** - A0002
        - **Hoeveelheid** - 3
    - Reserveer voorraad voor de beide regels die u zojuist hebt gemaakt.
        - Selecteer **Regel 1**.
        - Selecteer in het actievenster **Verkooporderregels** de optie **Voorraad** en selecteer vervolgens **Reservering** in de lijst.
        - In het formulier **Reservering** selecteert u **Partij reserveren** om de voorraad te reserveren.
        - Sluit het formulier **Reservering** wanneer de reservering is voltooid.
        - Herhaal deze stappen om voorraad voor **regel 2** te reserveren.
1. Selecteer **Nieuw** in het actievenster om de tweede verkooporder te maken.
    - Het menu **Verkooporder maken** wordt geopend. Hierin voert u de volgende gegevens in:
        - Op het sneltabblad **Klant** voert u **Klantrekening** - **US-005** in.
        - Op het sneltabblad **Algemeen** voert u **Magazijn** - **62** in.
        - Selecteer **OK** om het menu te sluiten en de verkooporder te maken.
    - Selecteer op het sneltabblad **Verkooporderregels** de optie **Regel toevoegen** als niet automatisch een nieuwe regel wordt toegevoegd en voer de volgende gegevens in:
        - **Artikelnummer** - A0001
        - **Hoeveelheid** - 4
        - Selecteer **Regel toevoegen** om een tweede regel toe te voegen.
        - **Artikelnummer** - A0002
        - **Hoeveelheid** - 2
    - Reserveer voorraad voor beide regels die u zojuist hebt gemaakt.
        - Selecteer **Regel 1**.
        - Selecteer in het actievenster **Verkooporderregels** de optie **Voorraad** en selecteer vervolgens **Reservering** in de lijst.
        - In het formulier **Reservering** selecteert u **Partij reserveren** om de voorraad te reserveren.
        - Sluit het formulier **Reservering** wanneer de reservering is voltooid.
        - Herhaal deze stappen om voorraad voor **regel 2** te reserveren.
    - Sluit de verkooporder en keer terug naar de lijstpagina **Alle verkooporders**.
1. Zoek de twee verkooporders die u zojuist hebt gemaakt (mogelijk moet u de pagina vernieuwen). Selecteer in de tabel beide verkooporders door het vinkje te gebruiken.
    - Selecteer in het actievenster **Alle verkooporders** het tabblad **Magazijn**.
    - Selecteer in de groep **Acties** de optie **Vrijgave naar magazijn** om beide verkooporders naar het magazijn vrij te geven.
1. Wanneer het proces voor vrijgave naar het magazijn is voltooid, wordt er een informatiebericht weergegeven.
    - Voor elke verkooporder worden verzendingen gemaakt.
    - Er wordt een wave gemaakt en beide zendingen worden aan de wave toegewezen. Noteer de **wave-id**.
1. Ga naar **Magazijnbeheer > Uitgaande waves > Zendingwaves > Alle waves**.
    - Zoek in de lijst **Alle waves** de **wave-id** die u in de vorige stap hebt gemaakt en selecteer deze.
    - Selecteer het tabblad **Wave** in het actievenster.
    - Selecteer in de groep **Wave** de optie **Verwerken** om de wave te verwerken en **werk** te maken.
    - Informatieve berichten worden gegenereerd wanneer de verwerking is voltooid, om aan te geven dat er werk is gemaakt en de wave is geboekt.
1. **Optioneel**: ga naar **Magazijnbeheer > Werk > Werkdetails** om het gemaakte werk weer te geven. Er worden twee verschillende werk-id's gemaakt. Elke werk-id heeft twee orderverzamelregels.

### <a name="run-the-mobile-device-flow"></a>De stroom voor mobiele apparaten uitvoeren

1. Meld u aan bij het mobiele apparaat voor een gebruiker in magazijn **62**.
1. Selecteer **Uitgaand** in het **hoofdmenu**.
1. Selecteer **SD-cluster** in het menu **Uitgaand** om de orderverzameling te starten.
    - Er wordt een cluster gemaakt en de twee werk-id's die u eerder hebt gemaakt, worden gekoppeld. Als u meer dan twee werk-id's hebt gemaakt, worden alleen de eerste twee toegevoegd aan het cluster. U ziet dat de werk-id's in oplopende volgorde worden toegevoegd aan het cluster, zoals u hebt opgegeven in de query-instellingen.

    > [!NOTE]
    > Het nieuwe cluster wordt alleen automatisch gemaakt als er eerder voldoende extra werk-id's zijn gemaakt. Anders wordt het volgende bericht weergegeven: Er is niet genoeg werk gevonden voor het cluster.

    - Nadat u het menu selecteert, wordt het eerste orderverzamelscherm weergegeven. Het systeem verzamelt alle overeenkomende orderverzamelregels van de twee werk-id's en instrueert u om één keer naar de orderverzamellocatie te gaan, zodat u aan beide orders voldoen met behulp van één orderverzameling. Dit proces wordt op dezelfde manier uitgevoerd als het proces voor door de gebruiker gestuurde clusterverzameling.

1. Bevestig de eerste orderverzamellocatie en het artikel door **OK** te selecteren.
    - Het aantal van de orderverzameling is het totaal van het artikel dat wordt weergegeven op de verkooporders in het cluster.
1. Voer de positienaam (numeriek of alfabetisch) in om te bevestigen dat de artikelhoeveelheid die voor de positie is verzameld, op de juiste positie is geplaatst.
1. Herhaal dit proces totdat alle artikelhoeveelheden zijn verzameld en op de juiste positie zijn geplaatst.
1. De laatste stap die u op het mobiele apparaat uitvoert, is het cluster op de uiteindelijke locatie **wegzetten**. Selecteer **OK**.
    - Wanneer de wegzetbewerking wordt bevestigd, wordt het cluster gesloten en opgesplitst, op basis van de waarde die u hebt ingesteld voor het veld **Cluster opsplitsen bij** in het clusterprofiel. Werk-id's worden ook gesloten.
1. Op het mobiele apparaat wordt aangegeven dat het cluster is voltooid.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
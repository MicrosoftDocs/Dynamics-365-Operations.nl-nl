---
title: Automatische vrijgave van zending voor cross-docken
description: In dit artikel wordt een strategie voor cross-docken beschreven waarmee u automatisch een vraagorder kunt vrijgeven aan het magazijn wanneer de productieorder die de vraaghoeveelheid levert is gereedgemeld, zodat de hoeveelheid rechtstreeks vanuit de locatie voor productie-uitvoer naar de uitgaande locatie kan worden verplaatst.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c7199f5a5a401e627bb5fac9dece3950900e5f97
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067906"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Automatische vrijgave van zending voor cross-docken

[!include [banner](../includes/banner.md)]

In dit artikel wordt een strategie voor cross-docken beschreven waarmee u automatisch een vraagorder kunt vrijgeven aan het magazijn wanneer de productieorder die de vraaghoeveelheid levert is gereedgemeld. Op deze manier wordt de hoeveelheid die nodig is voor het uitvoeren van de vraagorder rechtstreeks vanuit de locatie voor productie-uitvoer naar de uitgaande locatie wordt verplaatst.

Cross-docken is een magazijnverwerkingsstroom waarbij de hoeveelheid die nodig is om een uitgaande order te vervullen direct naar de outbound dock of het faseringsgebied voor de order wordt gestuurd vanaf de locatie waar de inkomende order is ontvangen. (De inkomende order kan een inkooporder, een overboekingsorder of een productieorder zijn.) Hoewel de functie voor geavanceerd cross-docken alle leverings- en vraagorders ondersteunt en vereist dat de uitgaande vraag moet worden vrijgegeven voordat de cross-dockmogelijkheid wordt geïdentificeerd, heeft de functie voor het automatisch vrijgeven van zendingen deze kenmerken:

- Het ondersteunt alleen productieorders als aanbod en alleen verkooporders en overboekingsorders als vraag.
- De bewerking voor cross-docken kan ook worden gestart als de vraagorder niet is vrijgegeven aan het magazijn voordat de ontvangstbevestiging is geregistreerd (dat wil zeggen voordat de productie is gereedgemeld).

Deze functionaliteit voor cross-docken heeft twee voordelen:

- Met de magazijnbewerkingen kunt u de stap van het wegzetten van hoeveelheden gereedgemelde goederen in het normale opslaggebied van het magazijn overslaan, als deze hoeveelheden simpelweg opnieuw zullen worden opgehaald om de uitgaande order te vervullen. In plaats daarvan kunnen de hoeveelheden eenmalig worden verplaatst van de uitvoerlocatie naar een verpakkings-/verzendlocatie. Op deze manier helpt de functionaliteit om het aantal keren dat voorraad wordt verwerkt tot een minimum te beperken, waardoor maximale tijds- en ruimtebesparingen op de werkvloer in het magazijn mogelijk worden.
- De magazijnbewerkingen kunnen de vrijgave van verkooporders en overboekingsorders naar het magazijn uitstellen tot de uitvoer van eindproducten voor de bijbehorende productieorder is gereedgemeld. Dit voordeel is vooral relevant in productieomgevingen voor maken naar order, waar de doorlooptijden van de productie gewoonlijk langer zijn dan de levertijden in productieomgevingen voor maken naar voorraad.

## <a name="prerequisites"></a>Vereisten

| Vereiste | Beschrijving |
|---|---|
| Item | Het artikel moet ingeschakeld zijn voor magazijnbeheerprocessen (WMS).<p>**Opmerking:** Catch weight-artikelen kunnen niet worden opgenomen in de processen voor cross-docken.</p> |
| Magazijn | Het magazijn moet ingeschakeld zijn voor magazijnbeheerprocessen (WMS). |
| Sjablonen voor cross-docken | Er moet ten minste één sjabloon voor cross-docken die gebruikmaakt van het vrijgavebeleid voor de vraag **Bij ontvangst van levering** worden ingesteld voor een bepaald magazijn. |
| Werkklasse | Er moet een werkklasse-id voor cross-docken worden gemaakt voor het werkordertype **Cross-docken**. |
| Werksjablonen | Werksjablonen van het werkordertype **Cross-docken** zijn vereist voor het maken van verzamel- en wegzetwerk voor cross-docken. |
| Locatie-instructies | De locatie-instructies werkordertype **Cross-docken** zijn vereist om weggezet werk te begeleiden op de locaties waar verkooporderhoeveelheden worden verpakt en verzonden. |
| Markering tussen een vraagorder en een productieorder | Het magazijnsysteem kan de automatische vrijgave van verzending van de uitgaande order alleen activeren en werk voor cross-docken maken vanaf de uitvoerlocatie bij de actie gereedmelding als verkooporders en overboekingsorders zijn gereserveerd en gemarkeerd voor een productieorder. |

## <a name="example-cross-docking-flow"></a>Voorbeeld van cross-dockstroom

Een standaard cross-dockstroom bestaat uit de volgende hoofdstappen.

1. Een aannemer van verkooporders maakt een verkooporder voor een product dat op order wordt gemaakt. Normaal gesproken is de gevraagde hoeveelheid niet op voorraad beschikbaar en moet eerst worden geproduceerd.
2. De opsteller van verkooporders maakt rechtstreeks een productieorder vanuit de verkooporderregel. Op deze manier reserveert de opsteller van verkooporders de hoeveelheid van de verkooporder en zet deze af tegen de productieorderhoeveelheid. 

    Een productieplanner kan ook specificeren dat de markering moet worden bijgewerkt wanneer geplande orders worden gefiatteerd.

3. De productieorder doorloopt de volgende stappen:

    1. Een productieplanner raamt de productieorder en geeft deze vrij. (De raming omvat de reservering van grondstoffen en de vrijgave omvat de vrijgave naar een magazijn.)
    2. Een magazijnmedewerker begint met het verzamelen van grondstoffen van de opslaglocatie naar de invoerlocatie naar de productie en voltooit deze op basis van de hoeveelheid verzameld werk voor productie.
    3. Een werkvloeroperator start de productieorder.
    4. Bij de laatste bewerking gebruikt een machineoperator het mobiele apparaat om de productieorder gereed te melden.

4. Het systeem gebruikt de instellingen om de cross-dockartikelen te identificeren voor de twee gekoppelde orders en voert vervolgens deze taken uit:

    1. Automatisch vrijgeven van de gekoppelde verkooporder naar een magazijn om een zending te maken.
    2. Automatisch cross-dockwerk maken met instructies voor het verzamelen van de eindproducten van de uitvoerlocatie en het verplaatsen hiervan naar de uitgaande locatie die door de locatie-instructies voor cross-docken is toegewezen aan de verkooporder.
    3. Een machineoperator om het cross-docken van werk onmiddellijk te voltooien nadat de productieorder is gereedgemeld.

5. Nadat de werkzaamheden voor cross-docken zijn voltooid en de hoeveelheden op het voertuig zijn geladen, wordt de verkoopzending bevestigd door een uitgaande magazijnplanner.

## <a name="example-scenario"></a>Voorbeeldscenario

Voor deze scenario moeten demogegevens worden geïnstalleerd en moet u het **USMF**-voorbeeld-gegevensbedrijf gebruiken.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Cross-docken instellen waarbij de functie voor automatische vrijgave van een zending wordt gebruikt

#### <a name="cross-docking-template"></a>Sjabloon voor cross-docken

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Werk** \> **Sjablonen voor cross-docken**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Volgnummer** de waarde **1** in.
4. Voer in het veld **Id van sjabloon voor cross-docken** een naam in, zoals **XDock\_RAF**.
5. Selecteer in het veld **Beleid voor vraagvrijgave** de optie **Bij ontvangst van levering**.
6. Voer in het veld **Magazijn** het nummer in van het magazijn waarin u het cross-dockproces wilt instellen. Selecteer voor dit voorbeeld de waarde **51**.

    > [!NOTE]
    > Zodra u **Bij ontvangst van levering** selecteert als beleid voor vraagvrijgave voor de sjabloon, zijn alle andere velden op de pagina niet langer beschikbaar. Ook kunt u geen leveringsbronnen definiëren. Dit probleem treedt op omdat cross-docken waarbij de functie voor automatische vrijgave van zendingen wordt gebruikt alleen productieorders als leveringsbronnen ondersteunt en vereist is dat er een markering bestaat tussen verkooporders en productieorders. Als u **Voor ontvangst van levering** selecteert als beleid voor vraagvrijgave, zijn de velden op de tabbladen **Planning** en **Leveringsbronnen** beschikbaar en kunnen deze worden bewerkt.

#### <a name="work-classes"></a>Werkklassen

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Werkk** \> **Werkklassen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Werkklasse-id** een naam in, zoals **CrossDock**.
4. Selecteer **Cross-docken** in het veld **Werkordertype**.

Als u de typen locaties wilt beperken waar gereed product kan worden weggezet waarop cross-docken is toegepast, kunt u een of meer geldige locatietypen opgeven.

#### <a name="work-templates"></a>Werksjablonen

1. Ga naar **Magazijnbeheert** \> **Instellen** \> **Werk** \> **Werksjablonen**.
2. Selecteer **Cross-docken** in het veld **Werkordertype**.
3. Selecteer **Nieuw**.
4. Voer in het veld **Volgnummer** de waarde **1** in.
5. Voer in het veld **Werksjabloon** een naam in, zoals **CrossDock\_51**.
6. Selecteer **Opslaan**.
7. Selecteer in de sectie **Werksjabloongegevens** de optie **Nieuw**.
8. Selecteer **Orderverzamelen** voor de nieuwe regel in het veld **Werktype**. Selecteer **CrossDock** in het veld **Werkklasse-id**.
9. Selecteer **Nieuw**.
10. Selecteer **Wegzetten** voor de nieuwe regel in het veld **Werktype**. Selecteer **CrossDock** in het veld **Werkklasse-id**.

#### <a name="location-directives"></a>Locatie-instructies

Voor een standaard wegzetproces voor eindproducten is een locatie-instructie **Wegzetten** vereist om de verplaatsing van verzamelde productiehoeveelheden naar een normale opslagruimte te begeleiden. Evenzo moet u een locatie-instructie voor **Wegzetten** bij cross-docken instellen om aan te geven dat het werk de voltooide hoeveelheid moet wegzetten naar een toegewezen uitgaande locatie die de verzending van de bijbehorende verkooporder verzorgt.

Bij cross-docken hoeft u, net als bij het normaal wegzetten van eindproducten, geen locatie-instructie op te stellen voor de actie voor het verzamelen van werk, omdat de uitvoerlocatie is opgegeven. Bovendien wordt deze uitvoerlocatie naar verwachting ingesteld als de standaarduitvoerlocatie voor een van de resourcegerelateerde records (dat we zeggen de resource, resourcegroepsrelatie of resourcegroep) of als standaardlocatie voor eindproducten voor een magazijn.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Locatie-instructies**.
2. Selecteer **Cross-docken** in het veld **Werkordertype**.
3. Selecteer **Nieuw**.
4. Voer in het veld **Volgnummer** de waarde **1** in.
5. Voer in het veld **Naam** een naam in, zoals **Baydoor**.
6. Selecteer **Wegzetten** in het veld **Werktype**.
7. Selecteer **5** in het veld **Locatie**.
8. Selecteer **51** in het veld **Magazijn**.
9. Selecteer **Nieuw** op het sneltabblad **Regels**.
10. Voer in het veld **Tot hoeveelheid** de maximale hoeveelheid van het bereik in, bijvoorbeeld **1000000**.
11. Selecteer **Opslaan**.
12. Selecteer **Nieuw** op het sneltabblad **Acties voor locatie-instructies**.
13. Voer in het veld **Naam** een naam in, zoals **Baydoor**.
14. Selecteer **Opslaan**.
15. U kunt de standaardqueryfunctie gebruiken om wegzetlocaties te beperken tot een of meer specifieke locaties. Selecteer **Query bewerken** en selecteer **51** als criterium voor het veld **Magazijn** in de tabel **Locaties**.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Eindproducten cross-docken naar de uitgaande locatie

Voer de volgende stappen uit om de hoeveelheid gereed product te cross-docken naar de uitgaande locatie van de bijbehorende verkooporder.

1. Ga naar **Verkoop en marketing** \> **Verkooporders** \> **Alle verkooporders**.
2. Selecteer **Nieuw**.
3. Selecteer voor de verkooporderkop klantrekening **US-001** en een magazijn dat is ingesteld voor cross-docken via de functie voor automatische vrijgave van zendingen.
4. Voeg een regel toe voor een eindproduct en voer **10** in als hoeveelheid.
5. Selecteer in de sectie **Verkooporderregels** de optie **Product en voorraad** \> **Productieorder**
6. Controleer het dialoogvenster **Productieorder maken** de standaardwaarden en selecteer vervolgens **Maken**. Er wordt een nieuwe productieorder gemaakt en aan de verkooporder gekoppeld (dat wil zeggen gereserveerd en gemarkeerd).
7. Optioneel: Wijzig de waarde van het veld **Hoeveelheid** zodat deze meer is dan de waarde die nodig is om de verkooporder te vervullen. Wanneer de productiehoeveelheid wordt gereedgemeld, wordt in het systeem werk voor cross-docken gemaakt voor de gemarkeerde hoeveelheid en wegzetwerk voor de resterende hoeveelheid, volgens de gebruikelijke procedure voor verwerking van het wegzetten van eindproducten.

    Zoals eerder vermeld, moet er een markering bestaan tussen de verkooporder en de productieorder. Anders werkt het cross-docken niet. Een markering kan op meerdere manieren worden gemaakt:

    - Het systeem kan in de volgende situaties automatisch de markering maken:

        - De productieorder wordt handmatig rechtstreeks vanuit de verkooporderregel gemaakt (zie stap 6).
        - Geplande productieorders worden gefiatteerd en het veld **Markering bijwerken** wordt ingesteld op **Standaard**.

    - De gebruiker kan handmatig de markering maken door de pagina **Markering** te openen vanuit de gevraagde orderregel.

    > [!NOTE]
    > Een markering kan niet handmatig worden gemaakt voor artikelen die zijn ingesteld om standaard en gewogen gemiddelde te gebruiken als voorraadmodellen.

8. Selecteer op de pagina **Productieorder** in het actievenster, op het tabblad **Productieorder** in de groep **Proces** de optie **Raming** en selecteer vervolgens **OK**. De order wordt geraamd en de hoeveelheid van de grondstof wordt gereserveerd voor de productie.
9. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Vrijgave** en selecteer vervolgens **OK**. Er wordt verzamelwerk in het magazijn gemaakt voor de grondstoffen.
10. Open en controleer het werk. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Algemeen** de optie **Werkgegevens**. Noteer de werk-id.
11. Meld u aan bij de mobiele app Magazijnbeheer om werkzaamheden uit te voeren in magazijn 51.
12. Ga naar **Productie** \> **Productieverzamelen**.
13. Voer de werk-id in om de orderverzameling van grondstoffen te starten en te voltooien. 

    Nadat het werk is gereedgemeld, is de hoeveelheid grondstoffen beschikbaar op de productie-invoerlocatie (**005** in USMF-demogegevens) en kan de uitvoering van de productieorder beginnen.

14. Selecteer op de pagina **Productieorder** in het actievenster, op het tabblad **Productieorder** in de groep **Proces** de optie **Starten** en selecteer vervolgens **OK**.
15. Ga in de app naar **Productie** \> **RAF en wegzetten**.
16. Voer in het veld **Prod-id** het productieordernummer en andere verplichte gegevens in en klik vervolgens op **OK**.

De volgende gebeurtenissen vinden nu plaats:

- De vrijgave van een magazijn wordt geactiveerd voor de gekoppelde verkooporder.
- Op basis van de vrijgave wordt het werk voor verzenden en cross-docken gemaakt. Dit werk geeft de magazijnoperator opdracht om de hoeveelheden te verzamelen die nodig zijn om de verkooporderregel te vervullen en deze te plaatsen op de uitgaande locatie die is opgegeven in de locatie-instructie voor cross-docken.
- Als de hoeveelheid van de productieorder groter is dan de hoeveelheid die nodig is voor de verkooporder, wordt normaal wegzetwerk gemaakt. Dit werk geeft de magazijnoperator opdracht om de hoeveelheid gereed product te kiezen die achterblijft na cross-docken en deze naar normale opslag te verplaatsen op basis van de locatie-instructie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
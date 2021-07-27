---
title: Overboekingsorders maken via de app voor magazijnbeheer
description: In dit onderwerp wordt beschreven hoe u overboekingsorders kunt maken en verwerken via de mobiele app Magazijnbeheer
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: fe5983d40033c0cd15674815067eaa969e97d38b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343620"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>overboekingsorders maken vanuit de magazijnapp

[!include [banner](../includes/banner.md)]

Met deze functie kunnen magazijnmedewerkers overboekingsorders rechtstreeks vanuit de mobiele app Magazijnbeheer maken en verwerken. De medewerker begint met het selecteren van het doelmagazijn en kan vervolgens met de app een of meer nummerplaten scannen om de nummerplaten aan de overboekingsorder toe te voegen. Wanneer de magazijnmedewerker **Order voltooien** selecteert, worden met een batchtaak de vereiste overboekingsorder en orderregels gemaakt op basis van de voorhanden voorraad die voor deze nummerplaten is geregistreerd.

## <a name="enable-the-create-transfer-orders-from-the-warehouse-app-feature"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>De functie voor het maken van overboekingsorders inschakelen via de functie van de app voor magazijnbeheer

Voordat u deze functie kunt gebruiken, moet u deze functie en de bijbehorende vereisten in uw systeem inschakelen. Beheerders kunnen gebruikmaken van de pagina voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen.

1. Schakel eerst de functie [Gebeurtenissen van de app voor magazijnbeheer verwerken](warehouse-app-events.md) in. Deze wordt in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) weergegeven als:
    - **Module** - Magazijnbeheer
    - **Functienaam**: gebeurtenissen van de app voor magazijnbeheer verwerken
1. Schakel vervolgens de functie *Overboekingsorders maken via de app voor magazijnbeheer* in. Deze wordt weergegeven als:
    - **Module** - Magazijnbeheer
    - **Functienaam**: Overboekingsorders maken en verwerken via de app voor magazijnbeheer
1. Als u de verwerking van uitgaande verzendingen wilt automatiseren, moet u ook de functie [Uitgaande verzendingen bevestigen op basis van batchtaken](confirm-outbound-shipments-from-batch-jobs.md) inschakelen. Deze functie wordt weergegeven als:
    - **Module** - Magazijnbeheer
    - **Functienaam**: Uitgaande verzendingen bevestigen op basis van batchtaken

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Een menuoptie voor een mobiel apparaat instellen om overboekingsorders te maken

Hier volgen algemene richtlijnen voor het instellen van een menuoptie voor mobiele apparaten waarmee u een overboekingsorder kunt maken. Afhankelijk van uw zakelijke vereisten voor het automatiseringsniveau dat moet worden ingesteld wanneer gebruikers overboekingsorders vanaf de werkvloer maken, worden verschillende configuraties ingeschakeld. In het scenario in dit document wordt één dergelijke configuratie beschreven.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** om een nieuwe menuoptie toe te voegen. Voer vervolgens de volgende instellingen in om aan de slag te gaan:

    - **Naam menuoptie**: wijs een naam toe zoals deze moet worden weergegeven in Supply Chain Management.
    - **Titel**: wijs een menunaam toe, zoals deze moet worden gepresenteerd aan de medewerkers in de mobiele app Magazijnbeheer.
    - **Modus**: stel de modus in op *Indirect* (met deze menuoptie wordt geen werk gemaakt).
    - **Activiteitscode**: stel deze waarde in op *Overboekingsorder op basis van nummerplaten maken* zodat de magazijnmedewerkers een overboekingsorder op basis van een of meer gescande nummerplaten kunnen maken.

1. Gebruik de instelling **Beleid voor het maken van overboekingsorderregels** om te bepalen hoe overboekingsorderregels door deze menuoptie worden gemaakt. De regels worden gemaakt/bijgewerkt op basis van de voorhanden voorraad die is geregistreerd voor de gescande nummerplaten. Kies een van de volgende waarden:

    - **Geen reservering**: de overboekingsorderregels worden niet gereserveerd.
    - **Nummerplaatgeleid met regelreservering**: de overboekingsorderregels worden gereserveerd en gebruiken de optie van de strategie Nummerplaatgeleid, waarmee de relevante aan de orderregels gekoppelde nummerplaat-ID´s worden opgeslagen. Gevonden nummerplaat-ID's kunnen daarom worden gebruikt als onderdeel van het proces voor het maken van werk voor overboekingsorderregels.

1. Gebruik de instelling **Beleid voor uitgaande verzendingen** om zo nodig meer automatisering toe te voegen aan het verzendproces voor uitgaande overboekingsorders. Wanneer een medewerker de knop **Order voltooien** selecteert, wordt de gebeurtenis *Order voltooien* van de app voor magazijnbeheer gemaakt, waarmee de waarde die u hier kiest wordt opgeslagen in het veld **Beleid voor uitgaande verzendingen** voor elke regel in de huidige overboekingsorder. Wanneer de gebeurtenissenwachtrij later wordt verwerkt door een batchtaak om de overboekingsorder te maken, kan de waarde die in dit veld is opgeslagen, worden gelezen door de batchtaak en kan daarmee dus worden bepaald hoe die taak elke regel verwerkt. Kies een van de volgende opties:

    - **Geen**: er vindt geen automatische verwerking plaats.
    - **Vrijgeven aan magazijn**: hiermee wordt het vrijgaveproces voor magazijnen geautomatiseerd.
    - **Verzenden bevestigen**: hiermee wordt het proces voor bevestiging van verzending geautomatiseerd.
    - **Vrijgeven en verzending bevestigen**: hiermee worden de processen voor vrijgave aan magazijn en bevestiging van verzending geautomatiseerd.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>De menuoptie voor mobiele apparaten aan een menu toevoegen

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**
1. Selecteer **Bewerken**.
1. Selecteer een bestaand menu na selectie van de nieuwe menuoptie onder **Beschikbare menu's en menuopties**. Voeg de menuoptie toe door de pijl naar rechts te selecteren.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Een overboekingsorder maken op basis van nummerplaten

De mobiele app Magazijnbeheer heeft een eenvoudig proces voor het maken van overboekingsorders op basis van nummerplaten. Hiervoor doet de medewerker het volgende met de mobiele app Magazijnbeheer:

1. Maak de overboekingsorder en bepaal het doelmagazijn.
1. Bepaal elke nummerplaat die moet worden verzonden.
1. Selecteer **Order voltooien**.

>[!NOTE]
> Het is mogelijk dat meerdere medewerkers nummerplaten toewijzen die zijn bedoeld voor dezelfde overboekingsorder door de knop **Overboekingsorder selecteren** te gebruiken om een bestaand, niet-verwerkt overboekingsordernummer te selecteren in de gebeurtenissenwachtrij van de app voor magazijnbeheer. Zie [Informatie opvragen over gebeurtenissen van de app voor magazijnbeheer](#inquire-the-warehouse-app-events) voor informatie over het vinden van waarden van overboekingsordernummers.

## <a name="example-scenario"></a>Voorbeeldscenario

Dit scenario biedt een overzicht van het proces voor het ophalen van overboekingsorders die zijn gemaakt en automatisch worden verwerkt op basis van de voorhanden voorraad die voor de geselecteerde nummerplaten is geregistreerd.

Als u dit scenario wilt doorlopen met de voorgestelde waarden, moet u in een systeem werken waarop demogegevens zijn geïnstalleerd en moet u de rechtspersoon *USMF* selecteren voordat u begint.

In dit scenario wordt ervan uitgegaan dat u zowel de mogelijkheid [overboekingsorders maken en verwerken via de functie van de app voor magazijnbeheer](#enable-create-transfer-order-from-warehouse-app) als de mogelijkheid [Verwerking van gebeurtenissen van de app voor magazijnbeheer](warehouse-app-events.md) hebt ingeschakeld.

U moet niet alleen het proces voor het maken van overboekingsorders instellen in de menuopties voor mobiele apparaten, maar er moeten ook aanvullende sjablonen, locatie-instructies en batchtaken worden ingesteld en ingeschakeld.

### <a name="example-scenario-blueprint"></a>Blauwdruk van voorbeeldscenario

U bent een detailhandelaar en hebt meerdere nummerplaten, die elk een combinatie van artikelen bevatten die op een specifieke locatie in een van uw magazijnen zijn geplaatst (*Magazijn 51*). U wilt het proces inschakelen waarmee medewerkers een overboekingsorder kunnen maken voor een ander magazijn (*Magazijn 61*) voor een verzameling gescande nummerplaten. De overboekingsorder wordt automatisch verzonden/bijgewerkt als de laatste nummerplaat voor de order is geïdentificeerd.

![Voorbeeld van automatisch proces van overboekingsorders.](media/create-transfer-order-from-app-example.png "Voorbeeld van automatisch proces van overboekingsorders")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Een menuoptie voor mobiel apparaten instellen om overboekingsorders te maken

In deze sectie wordt uitgelegd hoe u een nieuwe menuoptie voor mobiele apparaten instelt voor het maken van overboekingsorders. Stel de **Modus** in op *Indirect* en de **Activiteitscode** op *overboekingsorder maken op basis van nummerplaten*.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw**.
1. Voer in het veld **Naam menuoptie** de naam *overboekingsorder maken* in.
1. Voer in het veld **Titel** de beschrijving *overboekingsorder maken* in.
1. Selecteer *Indirect* in het veld **Modus**.
1. Selecteer bij **Activiteitscode** de optie *Overboekingsorder maken op basis van nummerplaten*
1. Selecteer bij **Beleid voor het maken van orderregels** de optie *Nummerplaatgeleid met regelreservering*.
1. Selecteer bij **Beleid voor uitgaande verzendingen** de optie *Vrijgeven en bevestigen van verzending*.
1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer **Bewerken**.
1. Selecteer het bestaande menu **Voorraad** en selecteer vervolgens de nieuwe menuoptie onder **Beschikbare menu's en menuopties**. Voeg de menuoptie toe aan het menu **Voorraad** door de pijl naar rechts te selecteren.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Werksjablonen instellen voor het automatisch verwerken en verdelen van werk per gevonden nummerplaat

In deze sectie wordt uitgelegd hoe u een werksjabloon inschakelt om het werk dat door de sjabloon is gemaakt wanneer een wave wordt vrijgegeven, automatisch te verwerken.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Selecteer *Werkordertype* in het veld **Transferuitgifte**.
1. Selecteer **Nieuw** om een nieuwe werksjabloon te maken.
1. Voer in het veld **Werksjabloon** *51 NP automatisch verwerken* in.
1. Voer in het veld **Omschrijving werksjabloon** *51 NP automatisch verwerken* in.
1. Schakel het selectievakje **Automatisch verwerken** in. U moet deze optie selecteren om alle automatiseringsstappen te kunnen verwerken.
1. In de demogegevens bestaat er al een werksjabloon *51 transfer*. Bewerk het veld **Volgnummer** zodat de nieuwe werksjabloon een lager volgnummer heeft dan de bestaande werksjabloon *51 transfer*.
1. Selecteer **Opslaan** op de werkbalk om het sneltabblad **Werksjabloongegevens** in te schakelen.
1. Selecteer op het sneltabblad **Werksjabloongegevens** **Nieuw** op de werkbalk. U voegt twee regels toe.
1. Selecteer **Verzamelen** in het veld *Werktype*.
1. Selecteer *TransfOut* in het veld **Werkklasse-id**.
1. Selecteer op de werkbalk **Werksjabloongegevens** de optie **Nieuw**.
1. Selecteer *Wegzetten* in het veld **Werktype**.
1. Selecteer *TransfOut* in het veld **Werkklasse-id**.
1. Selecteer **Opslaan** om het veld **Instructiecode** in te schakelen.
1. Selecteer op de regel *Plaatsen* van **Werktype** de **Instructiecode** *Laaddeur*. Zorg ervoor dat deze nieuwe werksjabloon het laagste **Volgnummer** krijgt.
1. Selecteer op de werkbalk **Query bewerken** om de query-editor te openen.
1. Selecteer **Toevoegen** op het tabblad **Bereik**.
1. Op de regel die is toegevoegd in **Veld** selecteert u *Magazijn*.
1. Selecteer in het veld **Criteria** *51*.
1. Selecteer het tabblad **Sorteren**.
1. Selecteer **Toevoegen** en stel **Veld** in op *Gevonden nummerplaat-ID*. Als u dit veld selecteert, wordt de werkbalkknop **Opsplitsingen voor werkkoptekst** ingeschakeld.
1. Selecteer **OK** gevolgd door **Ja** om de groepering opnieuw in te stellen en terug te keren naar de pagina **Werksjablonen**.
1. Selecteer **Opsplitsingen voor werkkoptekst** en schakel **Dit veld groeperen** in voor **Gevonden nummerplaat-ID**. Sluit vervolgens af.

> [!NOTE]
> Niet alle instellingen kunnen automatisch worden verwerkt, bijvoorbeeld catch weight-artikelen en het gebruik van gecombineerde traceringsdimensies.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Locatie-instructies instellen voor de nummerplaatgeleide strategie

In deze sectie wordt uitgelegd hoe u een proces instelt voor het verzamelen van locatie-instructies voor gebruik van de strategie **Nummerplaatgeleid**.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatie-instructies**.
1. Selecteer **Bewerken**.
1. Selecteer in de koptekst van de navigatielijst het **Werkordertype** *Transferuitgifte*.
1. Selecteer in de navigatielijst de bestaande locatie-instructie **51 te verzamelen**.
1. Schakel op het sneltabblad **Regels** het selectievakje **Splitsen toestaan** in.
1. Selecteer op het sneltabblad **Acties locatie-instructie** **Nieuw** om een nieuwe actieregel toe te voegen.
1. Voer in het veld **Naam** *Nummerplaatgeleid* in.
1. Selecteer in het veld **Strategie** *Nummerplaatgeleid*. Voor deze actie is het laagste volgnummer vereist.
1. Selecteer **Opslaan** op de werkbalk.
1. Selecteer het paginapictogram **Vernieuwen** op de werkbalk.
1. Selecteer op het sneltabblad **Acties locatie-instructie** de regel *Te verzamelen*.
1. Selecteer op de werkbalk **Acties locatie-instructie** **Omlaag** om het volgnummer te wijzigen zodat het hoger is dan het volgnummer voor de zojuist gemaakte actie *Nummerplaatgeleid*.

> [!NOTE]
> De nummerplaatgeleide strategie probeert orderverzamelingswerk te reserveren en te maken voor de locaties die de gevraagde nummerplaten bevatten die aan de overboekingsorderregels zijn gekoppeld. Als dit niet mogelijk is en u nog steeds orderverzamelingswerk wilt maken, moet u echter terugvallen op een andere strategie voor locatie-instructieacties en misschien ook zoeken naar voorraad in een ander gebied van het magazijn, afhankelijk van de vereisten van uw bedrijfsproces.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Een batchtaak instellen om gebeurtenissen van de app voor magazijnbeheer te verwerken

In deze sectie wordt uitgelegd hoe u een geplande batchtaak instelt voor de verwerking van gebeurtenissen van de app voor magazijnbeheer.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Gebeurtenissen in app voor magazijnbeheer verwerken**.
2. Schakel in het dialoogvenster **Batchverwerking** in onder de sectie **Uitvoeren op achtergrond**.
3. Selecteer **Terugkeerpatroon** en stel de batchtaak in die moet worden verwerkt op basis van het interval dat nodig is voor uw bedrijf.
4. Selecteer **OK** om terug te gaan naar het hoofddialoogvenster.
5. Selecteer **OK** in het hoofddialoogvenster om de taak aan de batchwachtrij toe te voegen.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Een batchtaak instellen om overboekingsorders automatisch vrij te geven

In deze sectie wordt uitgelegd hoe u een geplande batchtaak instelt om de overboekingsorders vrij te geven die zijn gemarkeerd als 'gereed voor vrijgave'.

1. Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Automatische vrijgave van overboekingsorders**.
1. Vouw in het dialoogvenster de sectie **Op te nemen records** uit.
1. Selecteer **Filter** onder de sectie **Op te nemen records**.
1. Selecteer op de querypagina **WHSTransferAutoRTWQuery** op het tabblad **Bereik** **Toevoegen** om een nieuwe regel aan de query toe te voegen.
1. Selecteer in het veld **Tabel** van de nieuwe regel het vervolgkeuzemenu en selecteer de tabel **Overboekingsorderregel vrijgeven aan magazijn**.
1. Selecteer in het vervolgkeuzemenu **Veld** **Beleid voor uitgaande verzendingen**.
1. Selecteer in het veld **Criteria** de optie **Vrijgeven en bevestigen van verzending**.
1. Selecteer *51* op de regel waar **Veld** is ingesteld op *Vanuit magazijn* in het veld **Criteria**.
1. Selecteer **OK** om terug te gaan naar het hoofddialoogvenster.
1. Vouw de sectie **Uitvoeren op achtergrond** uit om batchverwerking in te stellen.
1. Schakel **Batchverwerking** onder de sectie **Uitvoeren op achtergrond** in.
1. Selecteer **Terugkeerpatroon** en stel de batchtaak in die moet worden verwerkt op basis van het interval dat nodig is voor uw bedrijf.
1. Selecteer **OK** om terug te gaan naar het hoofddialoogvenster.
1. Selecteer **OK** in het hoofddialoogvenster om de batchtaak aan de batchwachtrij toe te voegen.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>De batchtaak Uitgaande verzending verwerken instellen

In deze sectie wordt uitgelegd hoe u een geplande batch taak instelt voor het uitvoeren van de bevestiging van de uitgaande verzending voor ladingen die gereed zijn voor verzending en die zijn gerelateerd aan overboekingsorderregels die gereed zijn om te worden verzonden.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Uitgaande zendingen verwerken**.
1. Vouw de sectie **Op te nemen records** uit.
1. Selecteer **Filter**.
1. Selecteer in de query **WHSLoadShipConfirm** het tabblad **Joins**.
1. Vouw de tabelhiërarchie uit zodat **Ladingen** en **Gegevens lading** worden uitgevouwen.
1. Selecteer de tabel **Gegevens lading**.
1. Selecteer de knop **Tabeljoin toevoegen**.
1. In de lijst met tabelrelaties in de kolom **Relatie** filtert u op of zoekt u naar *Overboekingsorderregels (verwijzing)*.
1. Focus op de tabelrelatie in de lijst en druk vervolgens op de knop **Selecteren**.
1. Selecteer de tabel **Overboekingsorderregels**.
1. Selecteer de knop **Tabeljoin toevoegen**.
1. In de lijst met tabelrelaties filtert u in de kolom **Relatie** op of zoekt u naar *Extra velden voorraadtransfer (record-ID)*.
1. Focus op de tabelrelatie in de lijst en druk vervolgens op de knop **Selecteren**.
1. Selecteer het tabblad **Bereik**.
1. In de querytabellen voor **Bereik** stelt u drie bereiken met querycriteria in. Selecteer de knop **Toevoegen** om een regel toe te voegen.
1. Voeg een bereik voor de tabel **Ladingen** toe. Stel **Veld** in op *Status lading* en stel **Criteria** in op *Geladen*.
1. Voeg een ander bereik toe voor de tabel **Extra velden transfervoorraad**. Stel **Veld** in op *Beleid voor uitgaande verzendingen* en stel **Criteria** in op *Vrijgeven en bevestigen van verzending*.
1. Voeg een ander bereik toe voor de tabel **Gegevens lading**. Stel **Veld** in op *Verwijzing* en stel **Criteria** in op *Verzending overboekingsorder*.
1. Selecteer **OK** om terug te gaan naar het hoofddialoogvenster.
1. Vouw de sectie **Op de achtergrond uitvoeren** uit.
1. Schakel **Batchverwerking** in.
1. Selecteer **Terugkeerpatroon** en stel de batchtaak in die moet worden verwerkt op basis van het interval dat nodig is voor uw bedrijf.
1. Selecteer **OK** om terug te gaan naar het hoofddialoogvenster.
1. Selecteer **OK** in het hoofddialoogvenster om de batchtaak aan de batchwachtrij toe te voegen.

> [!NOTE]
> Zie voor meer informatie [Uitgaande verzendingen bevestigen op basis van batchtaken](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Het voorbeeld verwerken voor 'Overboekingsorder maken vanuit de app voor magazijnbeheer'

### <a name="add-on-hand-on-a-license-plate"></a>Voorhanden voorraad aan een nummerplaat toevoegen

Als beginpunt voor dit scenario moet u een nummerplaat hebben die fysieke voorhanden voorraad bevat.

| Artikel | Magazijn | Voorraadstatus | Locatie | Nummerplaat | Hoeveelheid |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Beschikbaar | NP-010 | NP10 | 1 |
| A0002 | 51 | Beschikbaar | NP-010 | NP10 | 2 |

Voeg hoeveelheden van fysieke voorhanden voorraad toe met behulp van de volgende waarden:

> [!NOTE]
> U moet de nummerplaat maken en locaties gebruiken waarmee u gecombineerde artikelen kunt overbrengen, zoals NP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>overboekingsorders maken en verwerken vanuit de magazijnapp

1. Open de app en meld u aan als gebruiker *51*. Het magazijn van de huidige gebruiker is 51.
1. Selecteer de menuoptie **Overboekingsorder maken** van de menulocatie die u tijdens het instellen hebt toegevoegd.
1. Start het maken van een overboekingsorder door het doelmagazijn in te voeren (Naar magazijn) en voer in het veld **Magazijn** *61* in. De nieuwe overboekingsorders gaat vanuit het huidige magazijn 51 (Van magazijn) naar het doelmagazijn *61*.
1. Selecteer **OK**.
1. Scan een nummerplaat-ID in het veld **Nummerplaat**. Voer de nummerplaat van de voorraad in die in een eerdere stap is toegevoegd, *NP10*.
1. Selecteer **OK**.
1. Selecteer de menuknop en selecteer vervolgens **Order voltooien** om het maken van de overboekingsorders met de app voor magazijnbeheer te voltooien.

Voor het genoemde voorbeeld zijn twee **Gebeurtenissen van de app voor magazijnbeheer** (*Overboekingsorders maken* en *Overboekingsorders voltooien*) gebruikt.

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Informatie opvragen over gebeurtenissen van de app voor magazijnbeheer

U kunt de gebeurtenissenwachtrij en gebeurtenisberichten die zijn gegenereerd door de mobiele app Magazijnbeheer weergeven door naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer** te gaan.

De berichten van de gebeurtenis *Overboekingsorder maken* ontvangen de status *Wachten*, wat betekent dat de batchtaak **Gebeurtenissen van de app voor magazijnbeheer verwerken** de gebeurtenisberichten niet ophaalt en verwerkt. Zodra de status van het gebeurtenisbericht verandert in *In wachtrij*, worden de gebeurtenissen met de batchtaak verwerkt. Dit gebeurt op hetzelfde moment als het maken van de gebeurtenis *Overboekingsorder voltooien* (wanneer een medewerker de knop **Order voltooien** in de mobiele app Magazijnbeheer selecteert). Wanneer de berichten van de gebeurtenis *Overboekingsorder maken* zijn verwerkt, wordt de status gewijzigd in *Voltooid* of *Mislukt*. Wanneer de status van *Overboekingsorder voltooien* wordt gewijzigd in *Voltooid*, worden alle gerelateerde gebeurtenissen uit de wachtrij verwijderd.

Omdat de **Gebeurtenissen van de app voor magazijnbeheer** voor het maken van gegevens van overboekingsorders niet worden verwerkt door de batchtaak voordat de berichten zijn gewijzigd in de status *In wachtrij*, moet u de aangevraagde overboekingsordernummers opzoeken als onderdeel van het veld **ID**. Het veld **ID** bevindt zich in de koptekst van de pagina **Gebeurtenissen van de app voor magazijnbeheer**.

Als onderdeel van de verwerking van magazijngebeurtenissen kan het maken van de overboekingsorderregel mislukken. In dit geval wordt de status van het gebeurtenisbericht gewijzigd in *Mislukt* en kunt u de informatie van **Batchlogboek** gebruiken om te weten te komen waarom het is mislukt en hoe u actie kunt ondernemen om eventuele problemen op te lossen.

Veelvoorkomende problemen kunnen betrekking hebben op het ontbreken van instellingen voor het proces, zoals een ontbrekend transitmagazijn voor de gebeurtenis *Overboekingsorder maken*. In een dergelijk voorbeeld voegt u een transitmagazijn toe aan het verzendmagazijn en gebruikt u de optie **Opnieuw instellen** om de status te wijzigen voor alle gebeurtenisberichten van de app voor magazijnbeheer van *Mislukt* in *In wachtrij*. Dit betekent dat de batchtaak de gebeurtenisberichten opnieuw verwerkt na de correctie van de instellingsgegevens.

Binnen productieomgevingen zijn de uitzonderingen meer procesgerelateerd, zoals in geval van een aangevraagde nummerplaat die leeg is tijdens de verwerking van de batchtaak waardoor er geen overboekingsorderregels worden gemaakt. Dit mislukte gebeurtenisbericht kan worden verwijderd met de optie **Verwijderen** of u kunt de benodigde fysieke voorhanden voorraad toevoegen op de nummerplaat en de optie **Opnieuw instellen** gebruiken voor alle gerelateerde gebeurtenisberichten.

Zie [Verwerking van de gebeurtenis van de app voor magazijnbeheer](warehouse-app-events.md) voor meer informatie.

### <a name="follow-up-on-the-example-scenario-processing"></a>De verwerking van het voorbeeldscenario vervolgen

Tijdens dit scenario is het volgende gebeurd:

1. Met de mobiele app Magazijnbeheer hebt u een menuoptie geselecteerd waarbij de activiteitscode **Overboekingsorder maken op basis van een nummerplaat** wordt gebruikt.
1. De app heeft u gevraagd het doelmagazijn voor de overboekingsorder te selecteren. Het bronmagazijn is altijd het magazijn waarbij u momenteel als medewerker bent aangemeld.
1. Bij de selectie van het doelmagazijn heeft het systeem een ID-nummer voor de komende overboekingsorder gereserveerd (op basis van de nummerreeks van de overboekingsorder die in uw systeem is gedefinieerd), maar de overboekingsorder is nog niet gemaakt.
1. Toen u de nummerplaat *NP10* scande met de voorhanden voorraad die naar het nieuwe magazijn moet worden verplaatst, is er een **Gebeurtenis van de app voor magazijnbeheer** toegevoegd aan de gebeurtenissenwachtrij om later te worden verwerkt. De magazijngebeurtenis bevatte berichtgegevens over de scan, inclusief het bedoelde overboekingsordernummer.
1. In de mobiele app Magazijnbeheer is er toen de knop **Order voltooien** is geselecteerd, een nieuwe gebeurtenis van de app voor magazijnbeheer **Overboekingsorder voltooien** gemaakt en is met de gerelateerde bestaande gebeurtenis **Overboekingsorder maken** de status gewijzigd in **In wachtrij**.
1. In de backend heeft de batchtaak **Gebeurtenissen van de app voor magazijnbeheer verwerken** de gebeurtenis **In wachtrij** opgehaald en de voorhanden voorraad verzameld die gerelateerd is aan de gescande nummerplaat. Op basis van de voorhanden voorraad zijn de werkelijke overboekingsorderregel en de gekoppelde regels gemaakt. Met de taak is ook het veld **Beleid voor uitgaande verzendingen** voor de overboekingsorder ingevuld met de waarde op basis van de geconfigureerde optie *Vrijgeven en bevestigen van verzending* en is de nummerplaat gekoppeld voor de regels voor de strategie **Nummerplaatgeleid**.
1. Op basis van de waarde in het veld **Beleid voor uitgaande verzendingen** van de overboekingsorderregel heeft de query van de batchtaak **Automatische vrijgave van overboekingsorders** nu geresulteerd in de vrijgave van de overboekingsorder aan het verzendmagazijn. En dankzij de instelling van de gebruikte **Wavesjabloon**, **Werksjabloon** en **Locatie-instructies** is het werk automatisch verwerkt en is **Status lading** gewijzigd in *Geladen*.
1. De batchtaak **Uitgaande verzendingen verwerken** wordt uitgevoerd voor de lading, wat erin resulteert dat de overboekingsorder wordt verzonden en de Advance Shipment Notice (ASN) wordt gegenereerd.
1. De timing van al deze gebeurtenissen is afhankelijk van de instellingen bij **Terugkeerpatroon** voor de gemaakte batchtaken.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="mobile-device-menu-item-setup"></a>Instelling van de menuoptie voor mobiele apparaten

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Waarom kan ik "Overboekingsorder maken op basis van nummerplaat" niet zien in de vervolgkeuzelijst voor werkactiviteit van de menuoptie?

De functie *Overboekingsorders maken en verwerken via de app voor magazijnbeheer* moet worden ingeschakeld. Zie [De functie voor het maken van overboekingsorders via de app voor magazijnbeheer inschakelen](#enable-create-transfer-order-from-warehouse-app) voor meer informatie.

### <a name="warehouse-management-mobile-app-processes"></a>Processen van de mobiele app Magazijnbeheer

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Waarom zie ik de menuknop "Order voltooien" niet?

Er moet ten minste één nummerplaat aan de overboekingsorder zijn toegewezen.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Kunnen meerdere gebruikers van de mobiele app Magazijnbeheer tegelijkertijd nummerplaten aan dezelfde overboekingsorder toevoegen?

Ja, meerdere magazijnmedewerkers kunnen nummerplaten in dezelfde overboekingsorder scannen.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Kan dezelfde nummerplaat aan verschillende overboekingsorder worden toegevoegd?

Nee, een nummerplaat kan aan slechts aan één overboekingsorder tegelijk worden toegevoegd.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Kan ik nadat ik de knop "Order voltooien" heb geselecteerd, meerdere nummerplaten voor die overboekingsorder toevoegen?

Nee, u kunt geen aanvullende nummerplaten toevoegen aan een overboekingsorder met de gebeurtenis van de app voor magazijnbeheer **Overboekingsorder voltooien**.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Hoe kan ik bestaande overboekingsorders vinden die moeten worden gebruikt via de knop "Overboekingsorder selecteren" in de mobiele app Magazijnbeheer, als de order nog niet is gemaakt in het backend-systeem?

Op dit moment kunt u geen overboekingsorders opzoeken in de app, maar u kunt de overboekingsordernummers vinden op de pagina **Gebeurtenissen van de app voor magazijnbeheer**. Zie [Informatie opvragen over de gebeurtenissen van de app voor magazijnbeheer](#inquire-the-warehouse-app-events) voor meer informatie.

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Kan ik handmatig het overboekingsordernummer selecteren dat moet worden gebruikt vanuit de mobiele app Magazijnbeheer?

Alleen automatisch gegenereerde overboekingsordernummers via nummerreeksen worden ondersteund.

### <a name="background-processing"></a>Achtergrondverwerking

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Hoe moet ik records opschonen in mijn wachtrijberichttabellen voor de gebeurtenissen van de app voor magazijnbeheer?

U kunt dit weergeven en beheren op de pagina **Gebeurtenissen van de app voor magazijnbeheer**. Zie [Informatie opvragen over de gebeurtenissen van de app voor magazijnbeheer](#inquire-the-warehouse-app-events) voor meer informatie.

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Waarom is de "Ontvangstdatum" van de overboekingsorder niet bijgewerkt in overeenstemming met de instelling van "Controle van leveringsdatum"?

De overboekingsorders worden gemaakt zonder gebruik te maken van de mogelijkheden van **Controle leveringsdatum**.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Kan ik een nummerplaat gebruiken die een fysieke negatieve voorhanden voorraad heeft?

Deze functie ondersteunt alleen positieve fysieke voorhanden hoeveelheden die op nummerplaatniveau aanwezig zijn, maar u kunt fysieke negatieve voorhanden hoeveelheden hebben op hogere magazijn- en voorraadstatusniveaus bij het toewijzen van nummerplaten aan transferorders.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
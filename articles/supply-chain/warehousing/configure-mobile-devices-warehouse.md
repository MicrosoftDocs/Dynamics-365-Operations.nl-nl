---
title: Mobiele apparaten instellen voor magazijnwerk
description: In dit onderwerp wordt beschreven hoe u de menu-items configureert die magazijnmedewerkers gebruiken om werk op een mobiel apparaat uit te voeren.
author: MarkusFogelberg
manager: tfehr
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6a3330b0123605d4c7b86cedcb8bc95b3cf6de8
ms.sourcegitcommit: a52a789044ca66c6771224a6cf0be8749bc99e5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2020
ms.locfileid: "3837258"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Mobiele apparaten instellen voor magazijnwerk

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de menu-items configureert die magazijnmedewerkers gebruiken om werk op een mobiel apparaat uit te voeren.

> [!NOTE]
> Dit onderwerp is van toepassing op functies in Magazijnbeheer. Het geldt niet voor functies in Voorraadbeheer. De menuopties die in de menu's op een mobiel apparaat in een magazijn worden weergegeven worden geconfigureerd op de pagina **Menuopties voor mobiel apparaat**. Omdat de menuopties op verschillende menu's kunnen worden geplaatst, is het gemakkelijk om menustructuren te configureren zodat alleen specifieke typen werk aan specifieke gebruikers worden beschikbaar gesteld. U kunt de menuopties configureren om de volgende taken uit te voeren:

-   Een query verwerken of een activiteit uitvoeren, zoals een label afdrukken, nummerplaatnummers genereren, een productieorder starten of snel informatie over artikelen op een locatie opzoeken.
-   Maken het werk dat door een ander proces wordt uitgevoerd. Bijvoorbeeld, door het ontvangen van een artikel voor een inkooporder kan weggezet werk worden gemaakt voor een andere werknemer.
-   Werk uitvoeren dat door een ander proces (bestaand werk) is gemaakt, zoals weggezet werk dat is gemaakt bij het ontvangen van een artikel voor een inkooporder.

Als u een menuopdracht voor een activiteit of query wilt maken, stelt u het veld **Modus** in op **Indirect**. Een lijst met opties voor **Activiteitscode** worden vervolgens beschikbaar, zodat u het type query of de activiteit kunt selecteren waarvoor de menuopdracht is bedoeld. Als u een menuopdracht voor het genereren van magazijnwerk wilt maken, stelt u het veld **Modus** in op **Werk**. Een lijst met opties voor **Proces van werkaanmaak** wordt vervolgens beschikbaar. Als u een menuoptie wilt maken om het bestaande magazijnwerk te verwerken, stelt u het veld **Modus** in op **Werk** en stelt u vervolgens de optie **Bestaand werk gebruiken** in op **Ja**. 

> [!NOTE]
> Er kunnen aanvullende velden voor menuopdrachten beschikbaar zijn. Dit hangt af van de modus die u selecteert voor de menuopdracht en of de menuopdracht wordt gebruikt om bestaand werk uit te voeren. Zie voor informatie over de aanvullende veldselecties de sectie "Extra opties voor menuopdrachten" verderop in dit artikel.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Menuopties configureren voor activiteiten en query's
Als het veld **Modus** voor een menuoptie is ingesteld op **Indirect**, kunt u een menuoptie maken om een algemene activiteit of query uit te voeren die geen werk maakt. Voorbeelden zijn onder andere het opnieuw afdrukken van nummerplaatlabels en een query over de artikelen op een locatie. De volgende tabel bevat een lijst met beschikbare opties.

| Optie                      | Beschrijving                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Geen                        | Deze standaardwaarde schakelt geen activiteit of query in.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Informatie                       | Bekijk informatie over het systeem, zoals het versienummer, de magazijn-ID en de werknemer die momenteel is aangemeld.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Magazijn wijzigen            | Wijzig het magazijn waarbij een werknemer is aangemeld.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Locatieonderzoek            | Informatie weergeven over alle artikelen en hoeveelheden voor een locatie.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Nummerplaatonderzoek       | Geef de hoeveelheid artikelen op een nummerplaat en de locatie van de nummerplaat weer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Productieorder beginnen      | Een productieorder beginnen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Productie-uitval            | Voer de hoeveelheid uitval in die tijdens productie voor elke stuklijstregel is gemaakt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Laatste pallet van productie      | Geef aan dat de laatste pallet met artikelen voor een productieorder is geproduceerd en dat de status van de productieorder moet worden bijgewerkt naar **Gereedgemeld**. De status van de grondstoffen die niet tijdens de productie zijn verbruikt wordt teruggewijzigd van **Verzameld** naar **In bestelling** en de artikelen kunnen worden geretourneerd naar de voorraad.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Artikelonderzoek                | Scan een artikel om te bepalen waar in het magazijn het is. De query retourneert alle locaties en hoeveelheden voor het gescande artikel.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Etiket opnieuw afdrukken               | Een nummerplaatlabel opnieuw afdrukken.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Nummerplaat-build         | Maak een bovenliggende nummerplaat door meerdere nummerplaten in dezelfde locatie te combineren. Deze optie is handig als u meerdere nummerplaten tegelijk verplaatst. Nadat de bovenliggende nummerplaat wordt verplaatst, moet u een nummerplaatpauze uitvoeren voordat u artikelen van elke nummerplaat kunt verzamelen. <p></p>**Tip:** Om een bovenliggende nummerplaat te verplaatsen, moet u een mobiel apparaat gebruiken dat wordt geconfigureerd om werk voor verplaatsingen te maken.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Nummerplaat onderbreken         | Een nummerplaat maken zodat u de artikelen van nummerplaten kunt verzamelen die in de build zijn.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Inchecken chauffeur             | Als u Transportbeheer gebruikt, registreert u de aankomst van een chauffeur door de uitgaande laad-id, afspraak-id of zendings-id te scannen. Voor deze optie moet een lading worden toegewezen aan de afspraak en moet de status van de lading **Geladen** zijn.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Uitchecken chauffeur            | Registeer dat een chauffeur zijn of haar afspraak heeft voltooid.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| De cache van de nummerreeks legen | Verwijderen nummerreeksnummers van de nummerreekscache. Deze activiteit wordt gewoonlijk uitgevoerd door een systeembeheerder om cachingsproblemen op te lossen bij gebruik van mobiele apparaten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Batchbeschikking wijzigen    | Sta een werknemer toe om een batchbeschikkingscode voor een artikel en een batch op te geven. Deze selectie werkt de beschikkingscode bij die voor de batch is opgegeven.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Geopende werklijst weergeven      | Geef een lijst met beschikbaar werk weer aan een specifieke gebruiker. De gebruiker kan vervolgens uit te voeren werk selecteren en wordt hier naartoe geleid. Deze lijst is bedoeld voor weergave op tabletapparaten met een schermgrootte van 7 inch of meer. Wanneer u deze optie selecteert, komen de menuopties **Query bewerken** en **Veldenlijst** beschikbaar. Op de pagina **Query bewerken** kunt u criteria instellen voor het werk dat in de lijst wordt weergegeven. Op de pagina **Veldenlijst** kunt u selecteren welke velden in de werklijst worden weergegeven. Zo kunt u bijvoorbeeld het aantal velden beperken dat wordt weergegeven zodat de gebruiker sneller het meest passende werkitem kan selecteren. Op het sneltabblad **Algemeen** in het veld **Records per pagina** kunt u tevens selecteren hoeveel werkrecords per pagina worden weergegeven. Als de optie **Toestaan dat gebruikers kunnen filteren op type werktransactie** is geselecteerd, bevat de werklijst een besturingselement **Werk filteren** waarmee de gebruiker kan filteren op transactietype. In de werklijst krijgen gebruikers alleen werk te zien waarvoor zij toegangsmachtiging hebben. U moet ervoor zorgen dat gebruikers machtiging voor een of meer gebruikergeleide menuopties hebben die de specifieke werkklassetypen ondersteunen waartoe zij toegang moeten hebben. De machtigingen worden geverifieerd wanneer de gebruiker probeert om werk van de lijst uit te voeren. |

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Menuopties configureren om het werk voor een andere werknemer of proces te maken
U kunt een menuoptie instellen die het werk voor een andere werknemer zal maken nadat een eerste actie is uitgevoerd op het mobiele apparaat. Wanneer bijvoorbeeld de ene werknemer een mobiel apparaat gebruikt om een artikel te ontvangen, wordt weggezet werk gemaakt voor een andere werknemer. Als u een menuoptie wilt instellen dat werk maakt, gaat u naar de pagina **Menuopties voor mobiel apparaat** en selecteert u **Werk** in het veld **Modus**. In de volgende tabel, worden de opties in het veld **Proces van werkaanmaak** geordend op type werkorder.

<table>
<tbody>
<tr>
<th>Werkordertype</th>
<th>Optie</th>
<th>Beschrijving</th>
</tr>
<tr>
<td rowspan="8">Inkooporder</td>
<td>Ontvangen van inkooporderregel</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel door het inkoopordernummer en het inkooporderregelnummer te gebruiken en maak weggezet werk voor een andere werknemer.</td>
</tr>
<tr>
<td>Ontvangen van inkooporderregel en wegzetten</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel door het inkoopordernummer en het inkooporderregelnummer te gebruiken en zet de artikelen weg. Dezelfde werknemer voert beide acties uit.</td>
</tr>
<tr>
<td>Ontvangen van inkooporderartikel</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel voor een inkooporder door het inkoopordernummer en artikelnummer te registreren en maak weggezet werk voor een andere werknemer.</td>
</tr>
<tr>
<td>Ontvangen en wegzetten van inkooporderartikel</td>
<td>Registreer de ontvangst van een hoeveelheid voor een inkooporder door het inkooporderregelnummer en artikelnummer te registreren en zet het artikel weg. Dezelfde werknemer voert beide acties uit.</td>
</tr>
<tr>
<td>Ontvangen van nummerplaat</td>
<td>Ontvang een binnenkomende advance shipping notice (ASN) met behulp van een nummerplaat-id.</td>
</tr>
<tr>
<td>Ontvangen en wegzetten van nummerplaat</td>
<td>Ontvang een binnenkomende advance shipping notice (ASN) en zet deze weg met behulp van een nummerplaat-id.</td>
</tr>
<tr>
<td>Artikelontvangst laden</td>
<td>Registreer de ontvangst van een hoeveelheid van een lading door de lading-id te gebruiken en maak weggezet werk voor een andere werknemer. Het artikelnummer en de productdimensies komen overeen met het ontvangstbewijs op de inkooporderregels.</td>
</tr>
<tr>
<td>Ontvangen en wegzetten van artikel laden</td>
<td>Registreer de ontvangst van een belasting door de belastings-ID te gebruiken en zet de artikelen weg. Het artikelnummer en de productdimensies komen overeen met het ontvangstbewijs op de inkooporderregels. Dezelfde werknemer voert beide acties uit.</td>
</tr>
<tr>
<td rowspan="2">Retourorder</td>
<td>Ontvangen van retourorder</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel door het RMA-nummer te registreren en maak weggezet werk voor een andere werknemer.</td>
</tr>
<tr>
<td>Ontvangen en wegzetten van retourorder</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel door het RMA-nummer te registreren, en zet de artikelen weg. Dezelfde werknemer voert beide acties uit.</td>
</tr>
<tr>
<td rowspan="6">Transferorder</td>
<td>Ontvangen overboekingorder-artikel</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel en maak weggezet werk voor een andere werknemer.

<strong>Opmerking:</strong> Gebruik deze optie alleen als de artikelen zijn verzonden van een magazijn dat niet voor de processen magazijnbeheer is ingeschakeld.</td>
</tr>
<tr>
<td>Ontvangen en wegzetten van artikel voor overboekingorder</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel, en zet de artikelen weg. Dezelfde werknemer voert beide acties uit.

<strong>Opmerking:</strong> Gebruik deze optie alleen als de artikelen zijn verzonden van een magazijn dat niet voor de processen magazijnbeheer is ingeschakeld.</td>
</tr>
<tr>
<td>Ontvangen overboekingorderregel</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel en maak weggezet werk voor een andere werknemer.</td>
</tr>
<tr>
<td>Transferorderregel ontvangen en wegzetten</td>
<td>Registreer de ontvangst van een hoeveelheid van een artikel, en zet de artikelen weg. Dezelfde werknemer voert beide acties uit.</td>
</tr>
<tr>
<td>Ontvangen van nummerplaat</td>
<td>Ontvang een binnenkomende advance shipping notice (ASN) met behulp van een nummerplaat-id.</td>
</tr>
<tr>
<td>Ontvangen en wegzetten van nummerplaat</td>
<td>Ontvang een binnenkomende advance shipping notice (ASN) en zet deze weg met behulp van een nummerplaat-id.</td>
</tr>
<tr>
<td rowspan="4">Productie</td>
<td>Rapporteren als gereed</td>
<td>Registreer een hoeveelheid van een voltooid artikel dat is voltooid voor een productie en maak weggezet werk voor een andere werknemer. De hoeveelheid kan enkele of alle hoeveelheid zijn die voor productie is gepland.</td>
</tr>
<tr>
<td>Rapporteren als voltooid en wegzetten</td>
<td>Registreer een hoeveelheid van een voltooid artikel dat voor een productie is voltooid en zet de artikelen weg. De hoeveelheid kan enkele of alle hoeveelheid zijn die voor productie is gepland. Dezelfde werknemer voert beide acties uit.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Geef aan dat een Kanban is voltooid en maak weggezet werk voor een andere werknemer.</td>
</tr>
<tr>
<td>Kanban wegzetten</td>
<td>Geef aan dat een Kanban is voltooid en zet de artikelen weg. Dezelfde werknemer voert beide acties uit.</td>
</tr>
<tr>
<td rowspan="5">Voorraad</td>
<td>Mutatie</td>
<td>Registreren dat de artikelen van een locatie zijn naar een andere verplaatst. De werknemer geeft de locatie van de artikelen aan die zijn verplaatst en waarheen ze zijn verplaatst.</td>
</tr>
<tr>
<td>Quarantaine</td>
<td>Wijzig de status van de voorhanden voorraad voor een nummerplaat of een locatie om ontbrekende of beschadigde voorraadartikelen niet beschikbaar te maken.</td>
</tr>
<tr>
<td>Mutatie door sjabloon</td>
<td>Artikelen verplaatsen van een locatie naar een andere op een halfautomatische manier. De werknemer selecteert de locatie om artikelen van te verplaatsen, en het systeem gebruikt de locatierichtlijn om te bepalen waar de artikelen naartoe moeten worden verplaatst.</td>
</tr>
<tr>
<td>Magazijntransfer</td>
<td>Registreren dat de artikelen van een magazijn naar een andere zijn overgebracht. Deze optie vereist dat de werknemer toestemming moet krijgen om werk uit te voeren in beide magazijnen.

<strong>Opmerking:</strong> Deze menuoptie vereist een standaard voorraadoverboekingsjournaal waarbij het veld <strong>Boekstuk</strong> is ingesteld op <strong>Boeken</strong>.</td>
</tr>
<tr>
<td>Nummerplaatlading</td>
<td>Gebruik deze optie wanneer u uw magazijn voor het eerst instelt. Scan alle nummerplaten op alle locaties in het magazijn. De locaties moeten op nummerplaat worden gecontroleerd. U kunt deze optie niet gebruiken als <strong>Serienummer</strong> of <strong>Batchnummer</strong> boven <strong>Locatie</strong> staat in de voorraadreserveringshiërarchie.</td>
</tr>
<tr>
<td rowspan="3">Cyclus tellen</td>
<td>Correctie-invoer</td>
<td>Verhoog de hoeveelheid van de artikelen in voorraad. Geef de locatie, de nummerplaat, het artikel, de hoeveelheid, de maateenheid, en de status op.</td>
</tr>
<tr>
<td>Correctie-uitvoer</td>
<td>Verminder de hoeveelheid van de artikelen in voorraad. Geef de locatie, de nummerplaat, het artikel, de hoeveelheid, de maateenheid, en de status van de voorraad op.</td>
</tr>
<tr>
<td>Plaatscyclustelling</td>
<td>Start een telling voor een locatie op. De werknemer moet alle artikelen in de locatie tellen. Wanneer het resultaat van een telling lager zijn dan de verwachte hoeveelheid is, wordt de ontbrekende hoeveelheid beschouwd als verlies.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Menuopties configureren om bestaand werk te verwerken
Naast het instellen van menuopties om magazijnwerk te maken, kunt u menuopties instellen voor het verwerken van werk dat al is gemaakt. Stel het veld **Modus** in op **Werk** en selecteer de optie **Bestaand werk gebruiken**. Sommige aanvullende opties komen dan beschikbaar op het tabblad **Algemeen**. U kunt de toegang tot menuoptie regelen door een of meer werkklassen toe te wijzen op het sneltabblad **Werkklasse**. De werkklassen bepalen het werk dat de menuoptie kan verwerken. De werkklasse kan ook worden gebruikt om toegang te verlenen tot specifieke gebruikersrollen of tot afzonderlijke verwerking voor verschillende soorten bewerkingen. In de volgende tabel wordt beschreven welke opties beschikbaar zijn. De optie kan worden gekozen onder het veld **Bestuurd door** op de pagina **Menuopties voor mobiel apparaat**. 

<table>




<thead>
<tr class="header">
<th>Optie</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Geen</td>
<td>Deze standaardwaarde verwerkt geen werk.</td>
</tr>
<tr class="even">
<td>Door systeem bestuurd</td>
<td>Met Supply Chain Management wordt bepaald welk type werk wordt toegewezen aan een medewerker en wordt de volgorde bepaald waarin de medewerker het werk uitvoert. Wanneer u deze optie selecteert, kunt u klikken op <strong>Door systeem bestuurd werk</strong> in het actievenster om de pagina <strong>Door systeem bestuurde sorteervolgorde</strong> te openen waarop u sorteercriteria voor het werk kunt instellen. Met de sorteercriteria wordt de volgorde bepaald waarin de werknemer het werk uitvoert. U kunt zoveel criteria toevoegen als u nodig hebt.</td>
</tr>
<tr class="odd">
<td>Door gebruiker bestuurd</td>
<td>De werknemer selecteert het uit te voeren werk en de volgorde waarin dit wordt uitgevoerd.</td>
</tr>
<tr class="even">
<td>Gebruikergroepering</td>
<td>De werknemer groepeert handmatig het werk. Deze optie is bijvoorbeeld handig als een werknemer meerdere artikelen op een locatie tegelijk kan verzamelen. Wanneer de werknemer klaar is met het verzamelen van alle vereiste artikelen, kan hij of zij de artikelen wegzetten.</td>
</tr>
<tr class="odd">
<td>Systeemgroepering</td>
<td>Supply Chain Management groepeert werk voor de medewerker, gebaseerd op een opgegeven veld. Bijvoorbeeld, wordt het verzamelen van het werk gegroepeerd wanneer een werknemer een zendings-ID, belastings-ID, of elke waarde die elke werkeenheid kan koppelen scant. Als u deze optie selecteert, zijn de volgende velden vereist:
<ul>
<li><strong>Systeemgroeperingsveld</strong> – Selecteer het veld dat de werknemer scant om het werk te groeperen.</li>
<li><strong>Systeemgroeperingslabel</strong> – Voer de tekst in om de werknemer te instrueren over wat te scannen om het werk te groeperen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Gevalideerd door gebruiker bestuurd</td>
<td>De werknemer selecteert het werk om uit te voeren wanneer het werk aan een grotere entiteit, zoals een belasting of een verzending is gekoppeld. De werknemer bepaalt de volgorde waarin de artikelen worden verzameld. Als u deze optie selecteert, zijn de volgende velden vereist:
<ul>
<li><strong>Gevalideerd door gebruiker bestuurd veld</strong> – Selecteer het veld dat de werknemer scant om het werk te groeperen.</li>
<li><strong>Gevalideerd door gebruikersbestuurd etiket</strong> – Voer de tekst in die de werknemer instrueert over wat te scannen wanneer de orderverzameling van het werk door het systeem is gegroepeerd.</li>
</ul>
Deze optie is bijvoorbeeld handig wanneer meerdere pallets voor een lading worden klaargezet. Als u het veld <strong>LoadId</strong> selecteert in het veld <strong>Gevalideerd door gebruiker bestuurd veld</strong>, kan de werknemer elke pallet selecteren die aan de lading is gekoppeld. De medewerker ontvangt een foutmelding als hij of zij een artikel scant dat niet aan de lading is gekoppeld.</td>
</tr>
<tr class="odd">
<td>Orderverzamelen van cluster</td>
<td>De werknemer groepeert werk in clusters. Clusters stellen werknemers in staat om artikelen van één locatie te verzamelen voor meerdere werkorders tegelijk.</td>
</tr>
<tr class="even">
<td>Groepering van cyclustelling</td>
<td>De werknemer selecteert een zone, werkgroep of locatie, en Supply Chain Management wijst werk toe op basis van de selectie. Als u deze optie selecteert, kunt u ook klikken op <strong>Cyclustelling</strong> in het actievenster om extra informatie weer te geven. Daarnaast kunt u opgeven hoe vaak de werknemer de telling moet uitvoeren als een verschil is gevonden.</td>
</tr>
 <tr class="odd">
<td>Transportlading</td>
<td>Met deze functie kunnen verschillende magazijnmedewerkers voorraad laden uit dezelfde of verschillende ladingen op dezelfde vrachtwagen, met ladingen die volledig of gedeeltelijk worden verzonden.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Extra menuoptieopties
Extra menuopties zijn beschikbaar op de pagina **Menuopties voor mobiel apparaat**. De opties verschillen, afhankelijk van het proces waarvoor u de menuoptie configureert. 

Deze opties worden in de onderstaande tabel beschreven.

<table>




<thead>
<tr class="header">
<th>Veld</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Splitsing van werk toestaan</td>
<td>Selecteer deze optie om gebruikers artikelen voor een werkorder in meer dan één doelnummerplaat te laten plaatsen. Deze optie is bijvoorbeeld handig als een doelnummerplaat vol is en de werknemer de resterende artikelen aan een andere nummerplaat moet toevoegen. De werknemer kan klikken op <strong>Volledig</strong> om aan te geven dat de nummerplaat volledig is en is gestopt met het ontvangen van orderverzameling het werk. De gezette locatie voor de verzamelde artikelen wordt vervolgens weergegeven, en het orderverzameling werk dat al is voltooid wordt verplaatst naar een nieuw werkorder. Het resterende werk voor de orderverzameling voor de doelnummerplaat blijft op het oorspronkelijke werkorder.</td>
</tr>
<tr class="even">
<td>Verankering</td>
<td>Selecteer deze optie om werknemers toe te staan om een locatie op te geven die de voorgestelde klaarzet- of laadlocatie overschrijft. Alle resterende weggezet werk wordt naar de nieuwe locatie gevoerd. Deze optie is bijvoorbeeld handig wanneer een werknemer die artikelen voor order 1 in een klaarzetlocatie bij Dok 1 moet zetten, maar dat niet kan omdat een vorige lading de locatie niet heeft vrijgemaakt. In plaats van te wachten totdat de klaarzetlocatie Dok 1 beschikbaar komt, kan de werknemer besluiten de klaarzetlocatie voor Dok 2 te gebruiken. In dat geval negeert de werknemer de voorgestelde klaarzetlocatie. De neerzetlocatie voor alle resterende artikelen voor de werkorder wordt dan bijgewerkt naar de klaarzetlocatie Dok 2. Als u deze optie selecteert, moet u het veld <strong>Verankeren volgens</strong> instellen.</td>
</tr>
<tr class="odd">
<td>Verankeren volgens</td>
<td>Als u verankeren gebruikt, moet u opgeven of u volgens zending of volgens lading wilt verankeren.</td>
</tr>
<tr class="even">
<td>Auditsjabloon-id</td>
<td>Selecteer de sjabloon van het werkcontrole die het werkproces voor dit menuoptie zal onderbreken zodat een andere bewerking kan worden uitgevoerd. Als deze menuoptie bijvoorbeeld bestemd is voor binnenkomend werk, kan de controlesjabloon vereisen dat de werknemer de temperatuur in de leveringscontainer controleert. Het punt waarop het proces wordt onderbroken wordt opgegeven in de controlesjabloon. Dit punt kan bijvoorbeeld zijn als werk wordt gestart of voltooid, of als de status hiervan verandert.</td>
</tr>
<tr class="odd">
<td>Profiel-id van cluster</td>
<td>Selecteer het clusterprofiel om voor clusterverzamelen te gebruiken. Het clusterprofiel bevat instellingen zoals of om clusters automatisch te maken, de namen van posities en het aantal werkeenheden dat ze kunnen worden toegewezen, wanneer clusters in afzonderlijke eenheden te breken, en of de verificatie wordt vereist. Dit veld is alleen beschikbaar als <strong>Orderverzamelen van cluster</strong> is geselecteerd in het veld <strong>Bestuurd door</strong>.</td>
</tr>
<tr class="even">
<td>De totale artikelhoeveelheid eerst tellen</td>
<td>Selecteer deze optie om van een werknemer te vereisen dat deze eerst de totale hoeveelheid telt tijdens een telling. Als een verschil wordt gevonden, moet de werknemer aanvullende informatie geven, zoals het nummerplaatnummer, batchnummer en serienummers.</td>
</tr>
<tr class="odd">
<td>Verplaatsing maken</td>
<td>Selecteer deze optie om een werknemer in staat te stellen werk voor een verplaatsing te maken zonder dat de werknemer dit werk onmiddellijk uitvoert. Deze optie is bijvoorbeeld handig als een kwaliteitscontrole is voltooid, en de inspecteur wil dat het artikel van het kwaliteitscontrolegebied worden verplaatst.</td>
</tr>
<tr class="even">
<td>Instructiecode</td>
<td>Om een specifieke locatierichtlijn wilt gebruiken, selecteer de richtlijncode die de locatierichtlijn is gekoppeld. Dit veld is beschikbaar als u het werk maakt en het werkaanmaakproces <strong>Mutatie door sjabloon</strong> is.</td>
</tr>
<tr class="odd">
<td>Drempels voor cyclustelling uitschakelen</td>
<td>Selecteer deze optie om de drempels van de cyclustelling te negeren. Als u deze optie selecteert, wordt het werk van de cyclustelling niet gemaakt wanneer de drempelwaarden worden overschreden.</td>
</tr>
<tr class="even">
<td>Batchbeschikkingscode weergeven</td>
<td>Selecteer deze optie als u batchbeschikkingscodes wilt weergeven. Stel, u kunt batchbeschikkingscodes weergeven wanneer u een batch geretourneerde ontvangt. Werknemers kunnen dan de status of de kwaliteit van een batch beoordelen en de gewenste code selecteren. De regels van de batchbeschikkingscode definiëren of de batch voor andere magazijnprocessen beschikbaar is. Als u deze optie niet selecteert, wordt een van de volgende batchbeschikkingscodes gebruikt:
<ul>
<li>Als u een nieuw batchnummer ontvangt, wordt de standaardbatchbeschikkingscode die in de artikelmodelgroep is opgegeven gebruikt.</li>
<li>De batchbeschikkingscode die al aan de batch is toegewezen wordt gebruikt.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Beschikkingscode weergeven</td>
<td>Selecteer deze optie om beschikkingscodes weer te geven. Zo kunt u bijvoorbeeld beschikkingscodes weergeven wanneer u een geretourneerde artikelen ontvangt. Werknemers kunnen dan de status of de kwaliteit van de artikelen beoordelen en de gewenste code selecteren. De regels van de beschikkingscode definiëren of de artikelen voor andere magazijnprocessen beschikbaar zijn.</td>
</tr>
<tr class="even">
<td>Voorraadstatus weergeven</td>
<td>Selecteer deze optie als u de status van artikelen op voorraad wilt weergeven. Deze optie is beschikbaar voor alle menuopties die het bestaande werk, behalve het cyclus tellen gebruiken.</td>
</tr>
<tr class="odd">
<td>Samenvatting van orderverzamelscherm weergeven</td>
<td>Selecteer deze optie om een overzicht weer te geven van orderverzamelingswerk voor de geselecteerde werkorder. Het overzicht weergegeven tot de eerste werkregel wordt verwerkt voor het werkorder.</td>
</tr>
<tr class="even">
<td>Nummerplaat maken</td>
<td>Selecteer deze optie om een uniek nummerplaatnummer te genereren op basis van de nummerreeksselectie. Zo kunt u bijvoorbeeld een nummerplaatnummer instellen voor artikelen die voor inkooporders worden ontvangen.</td>
</tr>
<tr class="odd">
<td>Opslag voor groep</td>
<td>Selecteer deze optie om weggezet werk te groeperen. Deze optie is beschikbaar als het werk is gegroepeerd door de werknemer of door Supply Chain Management. Wanneer de werknemer alle orderverzameltaken in de groep heeft afgerond, wordt wegzet-werk gemaakt voor dezelfde groep.</td>
</tr>
<tr class="even">
<td>Voorraadcorrectietypen</td>
<td>Selecteer het voorraadcorrectietype dat het voorraadteljournaal bepaalt dat wordt gebruikt om de correctie te boeken, en of om reserveringen te verwijderen. Dit veld is alleen beschikbaar voor de werkaanmaakprocessen <strong>Correctie-invoer</strong> of <strong>Correctie-uitvoer</strong>.</td>
</tr>
<tr class="odd">
<td>Batchnummer overschrijven</td>
<td>Selecteer deze optie selectievakje om werknemers die een hoeveelheid als gereed voor een productieorder rapporteren toe te staan om een batchnummer in te voeren dat verschilt van het batchnummer dat aan de productieorder wordt toegewezen.</td>
</tr>
<tr class="even">
<td>Doelnummerplaat overschrijven</td>
<td>Selecteer deze optie om werknemers toe te staan om een specifiek doelnummerplaatnummer op te geven dat afwijkt van de voorgestelde doelnummerplaat. Gebruik deze optie wanneer de eerste order een voor het werkorder voor de volledige hoeveelheid van een artikel op een nummerplaat is. Deze optie is bijvoorbeeld handig als u een pallet opnieuw gebruikt.</td>
</tr>
<tr class="odd">
<td>Verzamelen en inpakken</td>
<td>Selecteer deze optie om werknemers toe te staan om werk voor een verkooporder of lading te combineren in één werkeenheid. Een werknemer kan alleen werk uitvoeren voor de verkooporder of de lading. Deze optie is bijvoorbeeld handig wanneer u een hoeveelheid voor een verkooporder moet verhogen na de lading, zending en er werk voor de verkooporder is gemaakt. Deze optie is alleen beschikbaar wanneer de menuoptie het bestaande werk gebruikt, en het werk wordt uitgevoerd door de gebruiker of het systeem.</td>
</tr>
<tr class="even">
<td>Oudste batch verzamelen</td>
<td>Geef aan of de werknemer de oudste batch in een locatie eerst moet verzamelen. De volgende opties zijn beschikbaar:
<ul>
<li><strong>Geen</strong> – De werknemer kan elke batch in de locatie selecteren. De werknemer ontvangt geen bericht.</li>
<li><strong>Waarschuwing</strong>: de medewerker kan elke batch in de locatie verzamelen, maar hij of zij ontvangt een waarschuwingsbericht als een batch niet de oudste batch is.</li>
<li><strong>Forceren</strong> – De werknemer moet de oudste batch in de locatie verzamelen. De medewerker ontvangt een foutbericht als een batch niet de oudste batch is. <strong>Opmerking:</strong> Deze optie is alleen relevant als <strong>Batchnummer</strong> lager is dan <strong>Locatie</strong> in de reserveringhiërarchie die aan het artikel is toegewezen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Etiket afdrukken</td>
<td>Selecteer deze optie om werknemers toe te staan nummerplaatlabels af te drukken.</td>
</tr>
<tr class="even">
<td>Systeemgroeperingsveld</td>
<td>Selecteer het veld dat bepaalt hoe in Supply Chain Management orderverzamelingswerk voor werknemers wordt gegroepeerd. Bijvoorbeeld, als u het veld <strong>ShipmentId</strong> selecteert, scant de werknemer de zendings-ID om orderverzameling werk te groeperen. Alle werk voor de zending wordt vervolgens toegewezen aan de werknemer. Dit veld vereist dat u een menuoptie maakt om bestaand werk te gebruiken dat door het systeem is gegroepeerd. U moet tevens tekst invoeren in het veld <strong>Systeemgroeperingslabel</strong> om de werknemer te instrueren over wat te scannen.</td>
</tr>
<tr class="odd">
<td>Systeemgroeperingslabel</td>
<td>Voer de tekst in die de werknemer instrueert over wat te scannen wanneer orderverzamelingswerk door Supply Chain Management wordt gegroepeerd. Als u bijvoorbeeld het veld <strong>ShipmentId</strong> gebruikt voor het verzamelen van werk per zending, kunt u <strong>Zendings-id</strong> in het veld invoeren. Dit veld vereist dat u een menuoptie maakt om bestaand werk te gebruiken dat door het systeem is gegroepeerd. U moet ook het veld selecteren waarop moet worden gegroepeerd in het veld <strong>Systeemgroeperingsveld</strong>.</td>
</tr>
<tr class="even">
<td>Standaardgegevens gebruiken</td>
<td>Selecteer deze optie om de knop <strong>Standaardgegevens</strong> in het Actievenster in te schakelen, waar u velden kunt selecteren voor gegevens die een werknemer meestal in zijn of haar dagelijks werk nodig heeft. Deze optie is bijvoorbeeld handig als een werknemer vaak artikelen van dezelfde locatie orderverzamelt. U kunt het veld <strong>Van locatie</strong> selecteren om standaard de locatie weer te geven.</td>
</tr>
<tr class="odd">
<td>Gevalideerd door gebruiker bestuurd veld</td>
<td>Selecteer het veld dat de werknemer scant om het werk te groeperen. Als u bijvoorbeeld <strong>LoadId</strong> selecteert, kan een werknemer elk werk orderverzamelen dat aan een geselecteerde belasting is gekoppeld. U moet tevens tekst invoeren in het veld <strong>Gevalideerd door gebruikersbestuurd etiket</strong> om de werknemer te instrueren over wat te scannen.</td>
</tr>
<tr class="even">
<td>Gevalideerd door gebruikersbestuurd etiket</td>
<td>Voer de tekst in die de werknemer instrueert over wat te scannen wanneer de orderverzameling van het werk door een gevalideerd door gebruiker gestuurd veld is gegroepeerd. Bijvoorbeeld, als u het veld <strong>LoadId</strong> gebruikt voor het verzamelen van het werk voor belasting te groeperen, kunt u <strong>belastings-ID</strong> in het veld invoeren.</td>
</tr>
<tr class="odd">
<td>Code werksjabloon</td>
<td>Selecteer het werksjabloon die het werk voor een proces maken zal. Als u bijvoorbeeld een artikel voor een inkooporder ontvangt, wordt het weggezette werk gegenereerd op basis van de werksjabloon Als u niet een werksjabloon selecteert, zal Supply Chain Management een sjabloon toewijzen op basis van zoekcriteria. Zie voor meer informatie over werksjablonen het onderwerp <a href="control-warehouse-location-directives.md">Magazijnwerk beheren met werksjablonen en locatierichtlijnen</a>.</td>
<tr class="even">
<td>Lijst met werkregels weergeven</td>
<td>Selecteer een optie voor de manier waarop medewerkers de regels voor het momenteel geselecteerde orderverzamelingswerk kunnen weergeven en gebruiken. Zie <a href="pick-line-overview.md">Een menuoptie voor een mobiel apparaat instellen om een overzicht van orderverzamelregels te bieden</a> voor meer informatie over deze optie.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Vereisen dat werknemers het product, de locatie of de hoeveelheid bevestigen bij het verzamelen van artikelen
U kunt werkbevestigingen instellen waarbij een werknemer een mobiel apparaat moet gebruiken om de locatie of de hoeveelheid te registreren bij het uitvoeren van werk in het magazijn. Werkbevestigingen helpen garanderen dat de werknemer zich op de juiste locatie bevindt of de juiste hoeveelheid artikelen verwerkt. U kunt Supply Chain Management ook inschakelen om de registratie van de medewerker automatisch te bevestigen. Als u automatische bevestiging inschakelt, kunt u niet ook bevestigingen voor locatie of hoeveelheid vereisen. Werkbevestigingen bevatten tevens producten en productvarianten. Bovendien kunt u bevestigingen registreren met een streepjescode te scannen. Om producten en productvarianten te bevestigen, moet u een ID voor het product of de productvariant invoeren. Deze id kan een product-id, id voor het zoeken van producten, externe id, GTIN of streepjescode zijn. Nadat u invoert de ID of de streepjescode scant, worden de dimensies voor de productvariant weergegeven op het mobiele apparaat. 

In de volgende tabel worden de verschillende werktypen beschreven waarbij u werkbevestigingen kunt gebruiken.

| Optie                 | Beschrijving                                                                |
|------------------------|----------------------------------------------------------------------------|
| Verzamelen                   | Vereis bevestiging bij het verzamelen van artikelen.                                |
| Wegzetten                    | Vereis bevestiging bij het wegzetten van artikelen op een locatie.                     |
| Tellen               | Vereis bevestiging tijdens cyclus telling.                                |
| Correcties            | Vereis bevestiging bij het aanpassen van voorraadhoeveelheden.               |
| Aangepast                 | Vereis bevestiging voor aangepast werk.                                      |
| Quarantaine             | Vereis bevestiging bij het verplaatsen van artikelen naar quarantaine.                   |
| Nummerplaat maken | Vereis bevestiging bij het consolideren van artikelen voor het maken van een nummerplaat. |
| Afdrukken                  | Vereis bevestiging bij het afdrukken van nummerplaatlabels.                |
| Statuswijziging          | Vereis bevestiging bij het wijzigen van de status van voorraad.              |

**Opmerking:** U kunt productbevestiging alleen vereisen voor werktypen voor verzamelen en wegzetten.

<a name="additional-resources"></a>Aanvullende bronnen
--------

[Een menuopdracht van mobiel apparaat instellen voor het voltooien van werkzaamheden van het type Inkooporder](tasks/set-up-mobile-device-menu.md)

[Een menuopdracht voor een mobiel apparaat instellen om de ontvangen artikelen te registreren](tasks/set-up-mobile-device-menu-item-register-received-items.md)

[Voorraadstatussen](../inventory/inventory-statuses.md)



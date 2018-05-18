---
title: Ploegen- en kasladebeheer
description: "In dit artikel wordt beschreven hoe u de twee typen ploegen voor detailhandelverkooppunten (POS) kunt instellen en gebruiken: gedeelde en zelfstandige. Gedeelde ploegen kunnen worden gebruikt door meerdere gebruikers op meerdere plaatsen terwijl zelfstandige ploegen kunnen worden gebruikt door slechts één werknemer tegelijk."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: nl-nl
ms.lasthandoff: 03/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Ploegen- en kasladebeheer

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u de twee typen ploegen voor detailhandelverkooppunten (POS) kunt instellen en gebruiken: gedeelde en zelfstandige. Gedeelde ploegen kunnen worden gebruikt door meerdere gebruikers op meerdere plaatsen terwijl zelfstandige ploegen kunnen worden gebruikt door slechts één werknemer tegelijk.

Er zijn twee typen ploegen voor detailhandelverkooppunten: zelfstandige en gedeelde. Zelfstandige ploegen kunnen door slechts één werknemer tegelijk worden gebruikt. Gedeelde ploegen kunnen worden gebruikt door meerdere gebruikers op meerdere plaatsen. Hierdoor creëren zij in feite één ploeg voor meerdere werknemers in een winkel.

## <a name="standalone-shifts"></a>Zelfstandige ploegen
Zelfstandige ploegen worden gebruikt in een traditioneel scenario met vaste POS, waarin geld voor elk POS-kassa afzonderlijk wordt afgestemd. In een supermarkt, bijvoorbeeld, zijn er meestal verschillende vaste POS-kassa's en wordt een kassamedewerker toegewezen aan elke kassa. In dit geval maakt elke kassa waarschijnlijk gebruik van een zelfstandige ploeg en is de kassamedewerker verantwoordelijk voor de kassa of de fysieke contanten in die kassa. Een zelfstandige ploeg omvat alle activiteiten op die kassa tijdens de ploegendienst van de kassamedewerker. Activiteiten kunnen het openingsbedrag dat wordt gestort in de kassa omvatten, alle verwijderingen en toevoegingen van contanten via bewerkingen als bankstortingen en wisselgeldinvoer, en de kascontrole aan het einde van de werktijd.

### <a name="set-up-a-stand-alone-shift"></a>Een zelfstandige ploeg instellen

Een zelfstandige ploeg wordt aangewezen op het niveau van de kassalade. In deze procedure wordt uitgelegd hoe u een zelfstandige ploeg kunt instellen op een POS-kassa.

1.  Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**.
2.  Selecteer het hardwareprofiel dat moet worden gebruikt voor de zelfstandige ploeg.
3.  Bevestig op het sneltabblad **Lade** dat de optie **Gedeelde ploeglade** is ingesteld op **Nee**.
4.  Klik op **Opslaan**.
5.  Klik op **Retail** &gt; **Kanaalinstelling** &gt; **POS-instellingen** &gt; **Kassa's**.
6.  Selecteer de kassa waarvoor een zelfstandige ploeg is vereist en klik vervolgens op **Bewerken**.
7.  Selecteer in het veld **Hardwareprofiel** het hardwareprofiel dat u in stap 2 hebt geselecteerd.
8.  Klik op **Opslaan**.
9.  Klik op **Retail** &gt; **IT detailhandel** &gt; **Distributieplanning**.
10. Selecteer de distributieplanning **1090** en klik vervolgens op **Nu uitvoeren** om wijzigingen in het POS te synchroniseren.

### <a name="use-a-stand-alone-shift"></a>Een zelfstandige ploeg gebruiken

1.  Meld u aan bij het POS.
2.  Als er geen ploeg geopend is, selecteert u **Een nieuwe ploeg openen**.
3.  Ga naar de bewerking **Beginbedrag declareren** en geef de hoeveelheid contanten op die aan de kassa wordt toegevoegd aan het begin van de werkdag.
4.  Voer een aantal transacties uit.
5.  Selecteer aan het einde van de dag **Kas controleren** om de hoeveelheid contant geld dat in de kassalade blijft aan te geven.
6.  Voer de hoeveelheid contant geld in en klik vervolgens op **Opslaan** om de kascontrole op te slaan.
7.  Selecteer **Ploeg sluiten** om de ploeg te sluiten.

**Opmerking:** andere activiteiten zijn beschikbaar tijdens de ploeg, afhankelijk van de bedrijfsprocessen die aanwezig zijn. De bewerkingen **Kluisstorting**, **Bankstorting** en **Kascontrole** kunnen worden gebruikt voor het verwijderen van geld uit de kassa gedurende de dag of voordat de ploeg wordt gesloten. Als nog maar weinig geld in een kassa zit, kan de bewerking **Wisselgeldinvoer** worden gebruikt om geld toe te voegen aan de kassa.

## <a name="shared-shifts"></a>Gedeelde ploegen
Een gedeelde ploeg wordt gebruikt in een omgeving waarin meerdere kassamedewerkers een kassalade of een reeks kassalades delen gedurende de werkdag. Een gedeelde ploeg wordt meestal gebruikt in mobiele POS-omgevingen. In een mobiele omgeving is elke kassamedewerker niet toegewezen aan en verantwoordelijk is voor een enkele kassalade. In plaats daarvan moeten alle kassamedewerkers een verkoop kunnen afhandelen en geld kunnen toevoegen aan de kassalade die zich het dichtst bij hen bevindt. In dit scenario worden de kassalades die worden gedeeld door kassamedewerkers opgenomen in een gedeelde ploeg. Alle kassalades in een gedeelde ploeg zijn opgenomen in de dezelfde ploeg ten behoeve van de activiteiten die betrekking hebben op kasbeheer voor die ploeg. Daarom moet het beginbedrag van de ploeg het totaal van alle geld in alle kassalades omvatten die zijn opgenomen in de gedeelde ploeg. Op vergelijkbare wijze is de kascontrole het totaal van alle geld in alle kassalades die zijn opgenomen in de gedeelde ploeg. **Opmerking:** In elke winkel kan telkens slechts één gedeelde shift tegelijk zijn geopend. Gedeelde ploegen en zelfstandige ploegen kunnen worden gebruikt in dezelfde winkel.

### <a name="set-up-a-shared-shift"></a>Een gedeelde ploeg instellen

1.  Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**.
2.  Selecteer het hardwareprofiel dat moet worden gebruikt voor de gedeelde ploeg.
3.  Stel op het sneltabblad **Lade** de optie **Gedeelde ploeglade** in op **Ja**.
4.  Klik op **Opslaan**.
5.  Klik op **Retail** &gt; **Kanaalinstelling** &gt; **POS-instellingen** &gt; **Kassa's**.
6.  Selecteer de kassa waarvoor een gedeelde ploeg is vereist en klik vervolgens op **Bewerken**.
7.  Selecteer in het veld **Hardwareprofiel** het hardwareprofiel dat u in stap 2 hebt geselecteerd.
8.  Klik op **Opslaan**.
9.  Klik op **Retail** &gt; **IT detailhandel** &gt; **Distributieplanning**.
10. Selecteer de distributieplanning **1090** en klik vervolgens op **Nu uitvoeren** om wijzigingen in het POS te synchroniseren.

### <a name="use-a-shared-shift"></a>Een gedeelde ploeg gebruiken

1.  Meld u aan bij het POS.
2.  Als de POS nog niet met een hardwarestation is verbonden, selecteert u **Niet-ladebewerking** en selecteert u vervolgens de bewerking **Hardwarestation selecteren** om een hardwarestation actief te maken voor de gedeelde ploeg. Deze stap is alleen vereist de eerste keer dat een kassa wordt toegevoegd aan een gedeelde ploegomgeving.
3.  Meld u af bij het POS en vervolgens opnieuw aan.
4.  Selecteer **Een nieuwe ploeg maken**.
5.  Selecteer **Beginbedrag declareren**.
6.  Voer het beginbedrag van alle kassalades in de winkel in die deel uitmaken van de gedeelde ploeg en klik vervolgens op **Opslaan**.
    -   Als u een deel van het beginbedrag wilt toevoegen aan elke opeenvolgende kassalade, gebruikt u de bewerking **Hardwarestation selecteren** om het hardwarestation actief te maken.
    -   U kunt een kassa toevoegen aan een specifieke kassalade door de bewerking **Lade openen** te gebruiken.
    -   Ga door totdat alle kassalades in de gedeelde ploeg hun deel van het beginbedrag bevatten.

7.  Aan het einde van de dag, opent u elke kassalade en verwijdert u het contante geld.
8.  Nadat u het contante geld hebt verwijderd uit de laatste kassalade, telt u alle geld uit alle kassalades.
9.  Gebruik de bewerking **Kas controleren** om het totale bedrag aan contant geld van alle kassalades die zijn opgenomen in de gedeelde ploeg aan te geven.
10. Gebruik de bewerking **Ploeg sluiten** om de gedeelde ploeg te sluiten.

## <a name="shift-operations"></a>Bewerkingen voor ploegen
U kunt verschillende acties ondernemen om de status van een ploegendienst te wijzigen of om het geldbedrag in de lade te verhogen of te verlagen. De onderstaande sectie beschrijft deze bewerkingen voor ploegen in Dynamics 365 for Retail Modern POS and Cloud POS.

**Ploeg openen**

POS vereist dat een gebruiker een actieve, open ploeg heeft voor het uitvoeren van bewerkingen die resulteren in een financiële transactie, zoals een verkoop, retour of klant.  

Bij het aanmelden bij het POS wordt eerst gecontroleerd of de gebruiker een actieve ploeg heeft in de huidige kassa. Als dit niet het geval is, kan de gebruiker een nieuwe ploeg openen, een bestaande ploeg hervatten of verdergaan met aanmelden voor de modus 'niet-ladebewerkingen', afhankelijk van de configuratie van het systeem en de machtigingen.

**Beginbedrag declareren**

Deze bewerking is vaak de eerste actie voor een net geopende ploeg. Gebruikers geven het beginbedrag in de lade op voor de ploeg. Dit is belangrijk omdat dit bedrag wordt gebruikt bij de berekening van overschot/tekort bij het afsluiten van een ploegendienst.

**Wisselgeldinvoer**

Wisselgeldinvoer zijn niet-verkooptransacties die worden uitgevoerd in een actieve ploeg. Hierdoor wordt het bedrag aan contant geld in de lade verhoogd. Een algemeen voorbeeld van wisselgeldinvoer is het aanvullen van het kleingeld in de lade wanneer dit bijna op is.

**Wisselgeld verwijderen**

Wisselgeld verwijderen is een niet-verkooptransactie die wordt uitgevoerd in een actieve ploeg. Hierdoor wordt het bedrag aan contant geld in de lade verlaagd. Dit wordt meestal gebruikt in combinatie met wisselgeldinvoer in een andere ploegendienst. Bijvoorbeeld: als kassa 1 weinig wisselgeld heeft, kan de gebruiker op kassa 2 wisselgeld verwijderen om het ladebedrag te verlagen. De gebruiker op kassa 1 voert vervolgens een wisselgeldinvoer uit om het bedrag te verhogen.

**Ploeg uitstellen**

Gebruikers kunnen hun actieve ploeg opschorten om de huidige kassa vrij te maken voor een andere gebruiker, of hun dienst verplaatsen naar een andere kassa (vaak een 'zwevende kassa' genoemd). 

Het opschorten van de dienst voorkomt eventuele nieuwe transacties of wijzigingen tot de dienst wordt hervat.

**Ploeg hervatten**

Met deze bewerking kan een gebruiker een eerder opgeschorte dienst hervatten op een kassa die nog geen actieve ploeg heeft.

**Kascontrole**

Kascontrole is een actie die de gebruiker uitvoert om het totale geldbedrag op te geven dat zich op dat moment in de lade bevindt, meestal voordat de dienst wordt gesloten. Deze waarde wordt vergeleken met de verwachte dienst voor het berekenen van het overschot/tekort.

**Kluisstorting**

Kluisstortingen kunnen op elk gewenst moment tijdens een actieve dienst worden uitgevoerd. Bij deze bewerking wordt geld uit de kassalade gehaald en overgeboekt naar een beter beveiligde locatie zoals een kluis in de achterruimte. Het totale bedrag voor de kluisstortingen wordt wel opgenomen in de diensttotalen, maar hoeft niet te worden geteld als onderdeel van de kascontrole.

**Bankstorting**

Net als kluisstortingen worden ook bankstortingen uitgevoerd bij actieve diensten. Bij deze bewerking wordt geld uit de dienst verwijderd ter voorbereiding van de bankstorting.

**Ploeg blind sluiten**

Een blind gesloten ploeg is een ploegendienst die niet langer actief is, maar niet volledig is afgesloten. Blind gesloten ploegen kunnen net als een opgeschorte dienst niet worden voortgezet, maar procedures zoals het declareren van startbedragen en kascontroles kunnen op een later tijdstip worden uitgevoerd of vanuit een andere kassa.

Blind gesloten ploegen worden vaak gebruikt voor het vrijmaken van een kassa voor een nieuwe gebruiker of ploeg, zonder dat deze ploeg eerst volledig wordt geteld, afgestemd en gesloten. 

**Ploeg sluiten**

Door deze bewerking worden vervolgens totalen en overschotten/tekorten berekend. Vervolgens wordt de actieve of blind gesloten dienst beëindigd. Gesloten diensten kunnen niet worden hervat of gewijzigd.  

**Ploegen beheren**

Met deze bewerking kunnen gebruikers alle actieve, opgeschorte en blind gesloten diensten voor de winkel weergeven. Afhankelijk van hun machtigingen kunnen gebruikers hun definitieve afsluitingsprocedures uitvoeren zoals kascontrole en ploegen sluiten voor blind gesloten ploegen. Met deze bewerking kunnen gebruikers ook ongeldige ploegen weergeven en verwijderen in het zeldzame geval dat een ploeg een onjuiste status heeft na het afwisselen tussen de modi offline en online. Deze ongeldige ploegen bevatten niet alle financiële informatie of transactiegegevens die nodig zijn voor de afstemming. 


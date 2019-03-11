---
title: Ploeg- en kasladebeheer
description: In dit onderwerp wordt uitgelegd hoe u ploegen gebruikt in detailhandelverkooppunten.
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 7ad3c3fd17e88f364be12c122e2f5c155b7b9064
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "313009"
---
# <a name="shift-and-cash-drawer-management"></a>Ploeg- en kasladebeheer

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u ploegen gebruikt in detailhandelverkooppunten.

In Microsoft Dynamics 365 for Retail wordt met de term *ploeg* de verzameling van POS-transactiegegevens en -activiteiten tussen twee tijdstippen bedoeld. Voor elke ploeg wordt de verwachte hoeveelheid geld vergeleken met het bedrag dat is geteld en gedeclareerd.

Doorgaans worden ploegen geopend aan het begin van een werkdag. Op dat moment declareert de gebruiker het beginbedrag, oftewel het bedrag dat zich in de kassalade bevindt. Verkooptransacties worden vervolgens uitgevoerd gedurende de dag. Ten slotte wordt aan het einde van de dag het kassabedrag geteld en worden de eindbedragen gedeclareerd. De ploeg wordt gesloten en er wordt een Z-rapport gegenereerd. In het Z-rapport wordt aangegeven of er een overschot of tekort is.

## <a name="typical-shift-scenarios"></a>Normale ploegscenario's

Retail biedt verschillende configuratieopties en POS-bewerkingen ter ondersteuning van een breed scala aan zakelijke eindedagprocessen voor het POS. In deze sectie worden enkele veelvoorkomende ploegscenario's beschreven.

### <a name="fixed-till"></a>Vaste geldlade

Van oudsher werd dit scenario het meest gebruikt. En ook nu nog wordt het vaak gebruikt. In een ploeg met een vaste geldlade zijn de ploeg en de geldlade gekoppeld aan een bepaalde kassa. Geldlades worden niet van de ene naar de andere kassa meegenomen. Een ploeg van het type Vaste geldlade kan door één gebruiker worden gebruikt of worden gedeeld met meerdere gebruikers. Ploegen van het type Vaste geldlade vereisen geen speciale configuratie.

### <a name="floating-till"></a>Zwevende geldlade

In een ploeg van het type Zwevende geldlade kunnen de ploeg en kassalade van de ene kassa naar de andere worden meegenomen. Hoewel voor een kassa slechts één actieve ploeg per kassalade kan bestaan, kunnen ploegen wel worden opgeschort en later op een andere kassa worden hervat.

Stel dat een winkel twee kassa's heeft. Beide kassa's worden aan het begin van de dag geopend wanneer de kassamedewerker een nieuwe ploeg opent en het beginbedrag opgeeft. Wanneer een kassamedewerker pauze wil nemen, schort hij of zij zijn of haar ploeg op en neemt hij of zij de geldlade uit de kassa. Deze kassa wordt zo beschikbaar voor andere kassamedewerkers. Een andere kassamedewerker kan zich nu aanmelden en zijn of haar ploeg openen op de kassa. Als de pauze van de eerste kassamedewerker voorbij is, kan deze zijn of haar ploeg hervatten zodra een van de andere kassa's beschikbaar wordt. Ploegen van het type Zwevende geldlade vereisen geen speciale machtiging.

### <a name="single-user"></a>Eén gebruiker

Veel detailhandelaren geven er de voorkeur aan om slechts één gebruiker per ploeg toe te staan, om de hoogste mate van aansprakelijkheid voor het contante geld in de kassalade te garanderen. Als slechts één gebruiker de kassa mag gebruiken die is gekoppeld aan een ploeg, kan die gebruiker geheel verantwoordelijk worden gesteld voor eventuele verschillen. Als meer dan één gebruiker een ploeg gebruikt, is het moeilijk om te bepalen wie een fout heeft gemaakt of wie mogelijk probeert te stelen uit de geldlade.

### <a name="multiple-users"></a>Meerdere gebruikers

Sommige detailhandelaren zijn bereid om de mate van aansprakelijkheid die ploegen met één gebruiker bieden, op te offeren om meerdere gebruikers per ploeg toe te staan. Deze benadering is gebruikelijk als er meer gebruikers dan beschikbare kassa's zijn en flexibiliteit en snelheid belangrijker zijn dan het risico van verlies. Het is ook gebruikelijk wanneer winkelmanagers niet hun eigen ploegen hebben, maar wel de ploegen van hun kassamedewerkers kunnen gebruiken. Een gebruiker moet over de POS-machtiging **Aanmelding meerdere ploegen toestaan** beschikken om zich te kunnen aanmelden bij en gebruik te maken van een ploeg die is geopend door een andere gebruiker.

### <a name="shared-shift"></a>Gedeelde ploeg

In de configuratie Gedeelde ploeg kan één ploeg meerdere kassa's, kassalades en gebruikers omvatten. Een gedeelde ploeg heeft één beginbedrag en één eindbedrag voor alle kassalades. Gedeelde ploegen zijn vooral handig wanneer mobiele apparaten worden gebruikt. In dit scenario is niet voor elke kassa een aparte geldlade gereserveerd. In plaats daarvan kunnen alle kassa's één kassalade delen.

Als u gedeelde ploegen in een winkel wilt gebruiken, moet de kassalade worden geconfigureerd als een gedeelde kassalade via **Retail \> Afzetkanaalinstellingen \> POS-instellingen \> POS-profielen \> Hardwareprofielen \> Lade**. Gebruikers hebben bovendien een of beide machtigingen voor gedeelde ploegen nodig (Beheer van gedeelde ploeg toestaan en Gebruik van gedeelde ploeg toestaan).

> [!NOTE]
> In een winkel kan altijd slechts één gedeelde ploeg tegelijk geopend zijn. Gedeelde ploegen en zelfstandige ploegen kunnen worden gebruikt in dezelfde winkel.

## <a name="shift-and-drawer-operations"></a>Ploeg- en kassaladebeheer

U kunt verschillende acties ondernemen om de status van een ploeg te wijzigen of het geldbedrag in de kassalade te verhogen of te verlagen. Deze sectie beschrijft deze ploegbewerkingen voor Microsoft Dynamics 365 for Retail Modern POS en Cloud POS.

### <a name="open-shift"></a>Ploeg openen

Het POS vereist dat een gebruiker een actieve, open ploeg heeft voor het uitvoeren van bewerkingen die resulteren in een financiële transactie, zoals een verkoop, retour of klantorder.

Wanneer een gebruiker zich bij het POS aanmeldt, wordt eerst gecontroleerd of er voor de huidige kassa een actieve ploeg beschikbaar is voor die gebruiker. Als dit niet het geval is, kan de gebruiker een nieuwe ploeg openen, een bestaande ploeg hervatten of zich aanmelden in een niet-lademodus, afhankelijk van de configuratie van het systeem en de machtigingen van de gebruiker.

### <a name="declare-start-amount"></a>Beginbedrag declareren

Deze bewerking is vaak de eerste bewerking voor een net geopende ploeg. Voor deze bewerking geven gebruikers het beginbedrag in de kassalade op voor de ploeg. Deze bewerking is belangrijk omdat voor het berekenen van het overschot of tekort bij het sluiten van een ploeg rekening moet worden gehouden met het beginbedrag.

### <a name="float-entry"></a>Wisselgeldinvoer

*Wisselgeldinvoer* bestaat uit niet-verkooptransacties die worden uitgevoerd in een actieve ploeg om het bedrag aan contant geld in de kassalade te verhogen. Een typisch voorbeeld van wisselgeldinvoer is een transactie om het kleingeld in de lade aan te vullen wanneer dit bijna op is.

### <a name="tender-removal"></a>Wisselgeld verwijderen

*Wisselgeld verwijderen* is een niet-verkooptransactie die wordt uitgevoerd in een actieve ploeg. Hierdoor wordt het bedrag aan contant geld in de kassalade verlaagd. Deze bewerking wordt meestal gebruikt in combinatie met wisselgeldinvoer in een andere ploeg. Als kassa 1 weinig wisselgeld bevat, kan de gebruiker op kassa 2 bijvoorbeeld wisselgeld verwijderen om het bedrag in zijn of haar kassalade te verlagen. De gebruiker op de kassa 1 registreert nu een wisselgeldinvoer om het bedrag in zijn of haar kassalade te verhogen.

### <a name="suspend-shift"></a>Ploeg uitstellen

Gebruikers kunnen hun actieve ploeg opschorten om de huidige kassa vrij te maken voor een andere gebruiker of hun ploeg te verplaatsen naar een andere kassa (in dit geval wordt de ploeg vaak een ploeg van het type Zwevende geldlade genoemd).

Wanneer een ploeg wordt opgeschort, kunnen er pas weer nieuwe transacties of wijzigingen worden uitgevoerd als de ploeg wordt hervat.

### <a name="resume-shift"></a>Ploeg hervatten

Met deze bewerking kunnen gebruikers een eerder opgeschorte ploeg hervatten op een kassa die nog geen actieve ploeg heeft.

### <a name="tender-declaration"></a>Kascontrole

Deze bewerking wordt uitgevoerd om het totale geldbedrag op te geven dat zich momenteel in de kassalade bevindt. Gebruikers voeren deze bewerking meestal uit voordat ze een ploeg afsluiten. Het opgegeven bedrag wordt vergeleken met het verwachte bedrag voor de ploeg om het overschot/tekort te berekenen.

### <a name="safe-drop"></a>Kluisstorting

Kluisstortingen kunnen op elk gewenst moment tijdens een actieve ploeg worden uitgevoerd. Bij deze bewerking wordt geld uit de kassalade gehaald en overgeboekt naar een beter beveiligde locatie, zoals een kluis in de achterruimte. Het totale geregistreerde bedrag voor kluisstortingen wordt wel opgenomen in de ploegtotalen, maar hoeft niet te worden geteld als onderdeel van de kascontrole.

### <a name="bank-drop"></a>Bankstorting

Net als kluisstortingen worden bankstortingen uitgevoerd bij actieve ploegen. Bij deze bewerking wordt geld uit de dienst verwijderd ter voorbereiding van de bankstorting.

### <a name="blind-close-shift"></a>Ploeg blind sluiten

*Blind gesloten ploegen* zijn niet meer actief, maar zijn niet volledig gesloten. In tegenstelling tot opgeschorte ploegen kunnen blind gesloten ploegen niet worden hervat. Bewerkingen zoals Beginbedrag declareren en Kascontrole kunnen echter later of vanaf een andere kassa worden uitgevoerd.

Blind gesloten ploegen worden vaak gebruikt om een kassa voor een nieuwe gebruiker of ploeg vrij te maken zonder dat deze ploeg eerst volledig moet wordt geteld, afgestemd en gesloten.

### <a name="close-shift"></a>Ploeg sluiten

Met deze bewerking worden vervolgens totalen en overschotten/tekorten berekend. Daarna wordt de actieve of blind gesloten ploeg beëindigd. Afhankelijk van de machtigingen van de gebruiker, wordt ook een Z-rapport afgedrukt voor de ploeg. Gesloten ploegen kunnen niet worden hervat of gewijzigd.

### <a name="print-x"></a>X afdrukken

Met deze bewerking wordt een X-rapport voor de huidige actieve ploeg gegenereerd en afgedrukt.

### <a name="reprint-z"></a>Z opnieuw afdrukken

Met deze bewerking wordt het laatste Z-rapport dat door het systeem werd gegenereerd toen een ploeg werd gesloten opnieuw afgedrukt.

### <a name="manage-shifts"></a>Ploegen beheren

Met deze bewerking kunnen gebruikers alle actieve, opgeschorte en blind gesloten ploegen voor de winkel weergeven. Afhankelijk van hun machtigingen, kunnen gebruikers hun definitieve afsluitingsprocedures, zoals Kascontrole en Ploeg sluiten, uitvoeren voor blind gesloten ploegen. Met deze bewerking kunnen gebruikers ongeldige ploegen weergeven en verwijderen in het zeldzame geval dat een ploeg een onjuiste status heeft na het schakelen tussen offline- en onlinemodi. Deze ongeldige ploegen bevatten geen financiële informatie of transactiegegevens die vereist zijn voor de afstemming.

## <a name="shift-and-drawer-permissions"></a>Ploeg- en kassalademachtigingen

De volgende POS-machtigingen hebben invloed op wat een gebruiker wel en niet kan doen in verschillende situaties:

- **Blind sluiten toestaan**
- **X-rapport afdrukken toestaan**
- **Afdrukken van Z-rapport toestaan**
- **Kascontrole toestaan**
- **Aangifte van wisselgeld toestaan**
- **Lade openen zonder verkoop**
- **Aanmelding meerdere ploegen toestaan**: met deze machtiging kan de gebruiker zich aanmelden en een ploeg gebruiken die door een andere gebruiker is geopend. Gebruikers die deze machtiging niet hebben, kunnen zich alleen aanmelden bij en gebruikmaken van de ploegen die zij hebben geopend.
- **Beheer van gedeelde ploeg toestaan**: gebruikers moeten deze machtiging hebben om een gedeelde ploeg te openen of te sluiten.
- **Gebruik van gedeelde ploeg toestaan**: gebruikers moeten deze machtiging hebben om zich aan te melden bij en gebruik te maken van een gedeelde ploeg.

## <a name="back-office-end-of-day-considerations"></a>Overwegingen voor einde dag backoffice

De manier waarop ploegen en de afstemming van kassalades worden gebruikt in het POS wijkt af van de manier waarop transactiegegevens tijdens de berekening van het overzicht worden samengevat. Het is belangrijk dat u dit verschil begrijpt. Afhankelijk van uw configuratie en bedrijfsprocessen, kunnen de ploeggegevens in het POS (het Z-rapport) en een berekend overzicht in de backoffice verschillende resultaten opleveren. Dit hoeft niet te betekenen dat de ploeggegevens of het berekende overzicht onjuist zijn of dat er een probleem met de gegevens is. Het betekent alleen dat de opgegeven parameters mogelijke extra of minder transacties bevatten of dat de transacties anders zijn samengevat.

Hoewel elke detailhandelaar andere bedrijfsvereisten heeft, raden we u aan uw systeem op de volgende manier in te stellen om situaties te voorkomen waarin zich verschillen van dit type voordoen:

Ga naar **Retail \> Afzetkanalen \> Detailhandelwinkels \> Alle detailhandelwinkels \> Overzicht/afsluiting** en stel voor elke winkel de velden **Overzichtsmethode** en **Afsluitingsmethode** in op **Ploeg**.

Met deze instelling zorgt u ervoor dat backoffice-overzichten dezelfde transacties als ploegen bevatten in het POS en dat de gegevens worden samengevat op basis van die ploegen.

Zie [Winkelconfiguraties voor detailhandeloverzichten](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements) voor meer informatie over overzichten en afsluitingsmethoden.

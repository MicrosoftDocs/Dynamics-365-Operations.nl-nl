---
title: Gegevens die worden gebruikt in stuklijstberekeningen met standaardkosten
description: Berekeningen van stuklijsten (BOM) gebruiken gegevens uit verschillende bronnen om de standaardkosten van een geproduceerd artikel te berekenen. De bronnen bevatten informatie over de artikelen, routering van facturen, formules voor de berekening van indirecte kosten en de versie van de kostprijsberekening.
author: JennySong-SH
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aad47abd72876da67dc6cb2602893281a5b270eb
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676210"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>Gegevens die worden gebruikt in stuklijstberekeningen met standaardkosten

[!include [banner](../includes/banner.md)]

Berekeningen van stuklijsten (BOM) gebruiken gegevens uit verschillende bronnen om de standaardkosten van een geproduceerd artikel te berekenen. De bronnen bevatten informatie over de artikelen, routering van facturen, formules voor de berekening van indirecte kosten en de versie van de kostprijsberekening.

De volgende gegevens van een ingekocht artikel worden gebruikt bij een stuklijstberekening voor standaardkosten:
-   Kosten - De kosten van een aangekocht artikel worden bijgehouden als sitespecifieke kostenrecords in een kostprijsberekeningsversie voor standaardkosten. Elke kostprijsrecords heeft een ingangsdatum, en de berekeningsdatum van de BOM bepaalt welke kostenrecord wordt gebruikt. De stuklijstberekening van een met een toekomstige berekeningsdatum kan bijvoorbeeld een kostenrecord gebruiken met een status in behandeling en een toekomstige ingangsdatum.
-   Kostengroep. De kostengroep die aan een ingekocht artikel is toegewezen, levert de basis voor de kostensegmentatie in de berekende kosten van een gefabriceerd artikel.
-   Dankzij waarschuwingsvoorwaarden die zijn ingesloten in de berekeningsgroep voor de stuklijst van het item, kunnen de stuklijstberekeningen potentiële problemen herkennen. Dit kan zijn als het gekochte artikel nul kosten heeft, een hoeveelheid nul heeft in een stuklijst of een verouderde kostenrecord. U kunt deze waarschuwingsvoorwaarden overschrijven wanneer u een stuklijstberekening start.

De volgende gegevens van een gefabriceerd artikel worden gebruikt bij een stuklijstberekening voor standaardkosten:
-   Standaardorderhoeveelheid voor voorraad - De standaardorderhoeveelheid voor voorraad is de standaard partijgrootte voor het afschrijven van constante kosten in een stuklijstberekening. De boekhoudkundige partijgrootte weerspiegelt ook het bestelveelvoud indien dit is opgegeven.
-   Dankzij waarschuwingsvoorwaarden die zijn ingesloten in de berekeningsgroep voor de stuklijst van het item, kunnen de stuklijstberekeningen potentiële problemen herkennen. Het geproduceerd artikel beschikt bijvoorbeeld niet over een stuklijst of route. U kunt deze waarschuwingsvoorwaarden overschrijven wanneer u een stuklijstberekening start.

De volgende stuklijstgegevens worden gebruikt bij een stuklijstberekening voor standaardkosten:
-   Stuklijstversie - De stuklijstversie die is toegewezen aan een geproduceerd artikel heeft geldigheidsdata en de status goedgekeurd en actief. De factuurversie kan specifiek zijn voor het hele bedrijf of site en kan optioneel breekpunten voor hoeveelheden bevatten.
-   Artikelhoeveelheid stuklijst - Een onderdeel waar meestal een variabele hoeveelheid vereist is, maar dit kan ook een constante zijn. De onderdeelhoeveelheid wordt meestal aangegeven voor de productie van een bovenliggend artikel, maar kan worden uitgedrukt per 100 of 1000 voor de decimale nauwkeurigheid. Het aantal onderdelen kan ook worden berekend op basis van metingen.
-   Uitval stuklijstartikel. Een onderdeel kan een variabele of een constante hoeveelheid voor geplande uitval hebben.
-   Geldige datums stuklijstartikel. Een onderdeel kan een geldige begin- en einddatum hebben.
-   Type stuklijstartikel van productie - De partijgrootte van de kostprijsberekening voor het afschrijven van constante kosten weerspiegelt de hoeveelheid van de stuklijstberekening en een explosiemodus voor het maken van orders, omdat er bij de stuklijstberekening vanuit wordt gegaan dat het gefabriceerde onderdeel in exact dezelfde hoeveelheid en niet in de standaardbestelhoeveelheid zal worden gefabriceerd.
-   Substuklijst voor een gefabriceerd onderdeel. Een gefabriceerd onderdeel kan optioneel een opgegeven stuklijstversie hebben die in plaats van de huidige actieve stuklijstversie van het artikel in een stuklijstberekening moet worden gebruikt.
-   Subroute voor een gefabriceerd onderdeel. Een gefabriceerd onderdeel kan optioneel een opgegeven routeversie hebben die in plaats van de huidige actieve routeversie van het artikel in een stuklijstberekening moet worden gebruikt.
-   Bewerkingsnummer en de invloed van uitvalpercentages - Het bewerkingsnummer is gekoppeld aan een specifieke bewerking en bewerkingen kunnen een uitvalpercentage hebben. Door deze koppeling kunnen stuklijstberekeningen rekening houden met uitvalpercentages cumulatieve uitvalpercentages over meerdere bewerkingen op de vereiste hoeveelheid van het onderdeel.
-   Stuklijstregelartikel in kostenberekeningen negeren. Een onderdeel kan worden genegeerd bij stuklijstberekeningen.

De informatiebron voor bedrijfsactiveiten gebruikt bij een standaard stuklijstberekening omvat:
-   Uurtarief - De uurkosten die worden gekoppeld aan een bron voor bedrijfsactiviteiten worden uitgedrukt als kostencategorieën die zijn toegewezen om de tijd en doorlooptijd in te stellen. Deze kostencategorieën moeten worden geïdentificeerd voor resourcegroepen en bronnen voor bedrijfsactiviteiten. De uurkosten die zijn gekoppeld aan een kostencategorie kunnen sitespecifiek zijn of gelden voor het hele bedrijf.
-   Per eenheid kosten - In sommige productieomgevingen worden kosten voor bronnen voor bedrijfsactiviteiten toegewezen per eenheid of output, die wordt uitgedrukt als een andere kostencategorie voor hoeveelheid. De hoeveelheidsgerelateerde kosten kunnen bijvoorbeeld stuktarieven voor arbeidsuren weerspiegelen of een verffabrikant kan bijvoorbeeld kosten voor bronnen voor bedrijfsactiviteiten toewijzen per geproduceerde gallon.
-   Informatie van bronnen voor bedrijfsactiviteiten bij routeringbewerkingen overschrijven - De resource-informatie over de kostencategorieën wordt overgenomen door bewerkingen, waarbij deze kunnen worden overschreven. Stuklijstberekeningen gebruiken de kostencategorie-informatie die is opgegeven bij routebewerkingen.
-   Kostengroep voor een kostencategorie - De kostengroep die aan een kostencategorie is toegewezen, levert de basis voor de kostensegmentatie in de berekende kosten van een gefabriceerd artikel. Verschillende groepen kunnen bijvoorbeeld worden gebruikt om de berekende kosten te segmenteren die zijn gekoppeld aan machines en arbeid of aan instellings- en doorlooptijd.

De volgende routegegevens worden gebruikt bij een stuklijstberekening voor standaardkosten:
-   Routeversie - De routeversie die is toegewezen aan een geproduceerd artikel heeft geldigheidsdata en de status goedgekeurd en actief. De routeversie moet specifiek zijn voor de site en kan optioneel breekpunten voor hoeveelheden bevatten.
-   Routering bewerkingstijd - De tijd voor de runtime en insteltijd kan worden ingesteld. De uurtijd wordt meestal aangegeven voor de productie van een bovenliggend artikel, maar kan worden uitgedrukt per 100 of 1000 voor de decimale nauwkeurigheid.
-   Routering bewerkingstijd voor secundaire bronnen - Een secundaire bron heeft hetzelfde bewerkingsnummer als de primaire bron en dezelfde routering bewerkingstijd. Een bewerking kan bijvoorbeeld een computer als primaire bron vereisen en arbeidskosten en hulpmiddelen als secundaire bronnen.
-   Routeringsbewerking uitvalpercentage - stuklijstberekeningen houden rekening met uitvalpercentages en cumulatieve uitvalpercentages over meerdere bewerkingen. Dit geldt voor de vereiste tijd voor routeringbewerkingen en de vereiste hoeveelheid voor onderdelen die zijn gekoppeld aan de bewerkingsnummers.
-   Kostencategorieën voor een routeringbewerking - Informatie van bronnen voor bedrijfsactiviteiten over kostencategorieën wordt overgenomen door bewerkingen, waarbij deze kan worden overschreven. Stuklijstberekeningen gebruiken de kostencategorie-informatie die is opgegeven bij routebewerkingen.

De volgende gegevens productieoverhead worden gebruikt bij een stuklijstberekening voor standaardkosten:
-   Toeslag. Een formule voor het berekenen van toeslagen geeft een percentage van een waarde weer, bijvoorbeeld 100 procent, die aan een specifieke kostengroep, zoals arbeid, is gekoppeld.
-   Tarief. Een formule voor het berekenen van tarieven geeft een bedrag per eenheid weer, bijvoorbeeld 10,00 euro per uur, dat aan een specifieke kostengroep, zoals arbeid, is gekoppeld.
-   Op tijd gebaseerde overhead versus op materiaal gebaseerde overhead. De productieoverhead kan worden gekoppeld aan routeringsbewerkingen of materialen.

De volgende kostprijsberekeningsversiegegevens worden gebruikt bij een stuklijstberekening voor standaardkosten:
-   Type kostprijsberekening - De kostprijsberekeningsversie moet standaard kosten bevatten. Er gelden diverse beperkingen voor stuklijstberekeningen met standaardkosten. Deze beperkingen bepalen bijvoorbeeld dat diverse toeslagen moeten worden opgenomen in de kostprijs en dat de explosiemodus van de stuklijstberekening op één niveau moet gebeuren.
-   Voorgeschreven terugvalprincipe - De kostprijsberekeningsversie kan het gebruik van een terugvalprincipe opleggen, zoals gebruik van een opgegeven kostprijsberekeningsversie van de actieve kostenrecords. Het voorgeschreven terugvalprincipe geldt meestal voor een kostprijsberekeningsversie die de incrementele updates in een aanpak van kostenupdates met twee versies vertegenwoordigt.
-   Blokkeringsvlag voor hangende kosten. Een blokkeringsvlag kan de stuklijstberekening van de hangende kosten voor gefabriceerde artikelen tegenhouden.
-   Opgegeven begindatum. De opgegeven begindatum fungeert als de standaardberekeningsdatum voor alle stuklijstberekeningen waarbij de kostprijsberekeningsversie is betrokken.
-   Opgegeven locatie. Een opgegeven locatie zorgt ervoor dat de stuklijstberekeningen maar voor een enkele locatie worden uitgevoerd.
-   De inhoud van de kostprijsberekeningsversie moet kosten bevatten. De inhoud moet inclusief kosten zijn en kan eventueel verkoopprijzen bevatten om de adviesverkoopprijzen voor gefabriceerde artikelen te berekenen.

Verschillende informatiebronnen kunnen worden opgegeven bij het initiëren van een stuklijstberekening. Dit omvat de site, de berekeningsdatum van en de kostprijsberekeningsversie.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
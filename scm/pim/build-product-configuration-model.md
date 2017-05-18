---
title: Een productconfiguratiemodel maken
description: De noodzaak om producten te configureren om aan speciale vereisten te voldoen, wordt de regel eerder dan de uitzondering, zowel in business-to-business- als business-to-consumer-relaties.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ac5ed00006b93e1aa63ea9032d0898d073af3f62
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="build-a-product-configuration-model"></a>Een productconfiguratiemodel maken

[!include[banner](../includes/banner.md)]


De noodzaak om producten te configureren om aan speciale vereisten te voldoen, wordt de regel eerder dan de uitzondering, zowel in business-to-business- als business-to-consumer-relaties.

Een fabrikant die configureren-op-bestelling-scenario's ondersteunt, kan beter inspelen op behoeften van de klant. Bovendien kan de fabrikant, door halffabrikaten op te slaan in de vorm van algemene onderdelen in plaats van eindproducten, het kapitaal verkleinen dat vast zit in voorraad.  

Een geslaagde verplaatsing van een vervaardiging-naar-voorraadinstelling naar een configureren-op-bestelling instelling vereist zorgvuldige analyse van de productstructuren, identificatie van productfamilies en componentisering. Om het aantal onderdelen te verlagen en het aantal goederen te minimaliseren die in uitvoering zijn, is het zeer belangrijk dat u de productinterfacen begrijpt, en dat u ontwerpt voor herbruikbaarheid.  

Er zijn verschillende modelleringsprincipes voor productconfiguratie, zoals op regels gebaseerd, op dimensies gebaseerd en op beperkingen gebaseerd modelleren. Uit onderzoek blijkt dat de op beperkingen gebaseerde methodologie het aantal coderegels in modellen met ongeveer 50 procent kan verminderen door het gebruik van andere modelleringsprincipes. Daarom kan deze methodologie de totale kosten van eigendom (TCO) drukken. Door over te stappen vanuit een op regels gebaseerd model dat is gebaseerd op X++-code, op een model dat op beperkingen is gebaseerd, hebt u geen ontwikkelaarslicentie meer nodig om productmodellen te onderhouden.

## <a name="product-configuration"></a>Productconfiguratie
De industrialisatieperiode heeft geleid tot grote verwezenlijkingen in de productie van hoogwaardige en functierijke producten tegen betaalbare prijzen. De schaaleconomieën hebben het voor de meeste mensen in de geïndustrialiseerde wereld mogelijk gemaakt auto's, tv's, huishoudapparaten en andere goederen te kopen die de meesten van ons nodig vinden in het dagelijks leven.  

Als meerdere producten basisproducten zijn geworden, is de noodzaak ontstaan om er onderscheid tussen te maken. Het directe antwoord van fabrikanten op deze uitdaging is geweest om varianten van elk product te maken, zodat de klanten meerdere alternatieve hebben. Deze strategie heeft tot toegenomen prognose-uitdagingen geleid en tevens tot een verhoging van voorraadkosten en onverkochte producten die verouderd raken.  

Door een configureren-op-bestelling filosofie te hanteren kunnen fabrikanten aan klantvraag naar unieke producten voldoen en tegelijkertijd verouderde voorraadartikelen elimineren. Wanneer een vervaardiging-naar-voorraadfilosofie wordt gewijzigd naar een configureren-op-bestellingfilosofie, is van de directe uitdagingen die zich voordoet dat de vereiste voor korte levertijden moet worden gebalanceerd met lage voorraadniveaus.  

De sleutel tot succes moet u deze hier productportfolio zorgvuldig analyseren, en gebruikspatronen in zowel productfuncties als processen zoeken. Het algemene doel is componenten identificeren die kunnen worden gefabriceerd met dezelfde apparatuur in alle varianten kunnen worden gebruikt.  

De nieuwe Productconfiguratie-functieset bevat een gebruikersinterface (UI) die een visueel overzicht geeft van de productconfiguratiemodelstructuur, en een complete beperkingsyntaxis die niet hoeft te worden gecompileerd. Daarom kunnen bedrijven die een configuratiepraktijk willen ondersteunen gemakkelijker aan de slag gaan. Zoals in de volgende secties wordt uitgelegd, heeft een productontwerper geen ondersteuning meer nodig van een ontwikkelaar om een productconfguratiemodel te maken, te testen en vrij te geven aan de verkooporganisatie.

## <a name="building-a-product-configuration-model"></a>Een productconfiguratiemodel maken
Er zijn verschillende benaderingen die een gebruiker kan kiezen bij het maken van een productconfiguratiemodel. Een optie is om een opeenvolgende stroom te volgen door eerst alle verwijzingsgegevens te maken, zoals productmodellen, verschillende producten, en operationele bronnen en deze vervolgens bij te voegen als componenten, stuklijstregels, routebewerkingen en andere elementen van het productconfiguratiemodel. Als alternatief kunt u een meer iteratieve aanpak selecteren door eerst het model te maken en vervolgens verwijzingsgegevens toe te voegen wanneer dat nodig is.

### <a name="components"></a>Onderdelen

Een productconfiguratiemodel bestaat uit een of meerdere onderdelen die door subcomponentrelaties verbonden zijn. De onderdelen worden eenmaal gedefinieerd en kunnen vervolgens vaak worden gebruikt in een of meer productconfiguratiemodellen. De componenten zijn de belangrijkste bouwstenen van een productconfiguratiemodel, en vrijwel alle informatie over het model is eraan gerelateerd.

### <a name="attributes"></a>Kenmerken

Elke component heeft een of meer kenmerken die de eigenschappen ervan identificeren. De kenmerken zijn wat gebruikers tijdens het configuratieproces kiezen. Kenmerken bepalen relaties tussen en binnen componenten door middel van opname in beperkingen of berekeningen. Via voorwaarden die op stuklijstregels worden toegepast, kunnen de kenmerken worden gebruikt om te bepalen uit welke fysieke onderdelen het geconfigureerde product moet bestaan. Bovendien kan een kenmerk de eigenschap van een stuklijstregel bepalen door middel van een toewijzingsmechanisme. Vergelijkbare functionaliteit er bestaat voor routebewerkingen voor zowel opname als eigenschapsinstellingen.

### <a name="expression-constraints"></a>Expressiebeperkingen

Het gebruik van een op beperkingen gebaseerd productconfiguratiemodel betekent dat bepaalde beperkingen bestaan wanneer de gebruiker de waarden voor de diverse kenmerken selecteert. Deze beperkingen kunnen als expressiebeperkingen worden uitgevoerd door de Optimization Modeling Language (OML) te gebruiken. Als alternatief kan een beperking worden geïmplementeerd in de vorm van een tabelbeperking.

### <a name="table-constraints"></a>Tabelbeperkingen

Tabelbeperkingen kunnen door de gebruiker of door het systeem zijn gedefinieerd.  

Een door de gebruiker gedefinieerde tabelbeperking wordt gemaakt door de gebruiker. De gebruiker selecteert een combinatie van kenmerktypen om de kolommen van de tabel weer te geven, en voert vervolgens waarden uit de domeinen van het geselecteerde kenmerktype in om de rijen in de tabelbeperking te vormen.  

Een door het systeem gedefinieerde tabelbeperking wordt gedefinieerd door te selecteren welke Microsoft Dynamics 365 for Operations-tabel als referentie wordt gebruikt, en vervolgens velden in deze tabel te selecteren om de kolommen te vormen in de beperking. De rijen van de tabelbeperking zijn de rijen van de Dynamics 365 for Operations-tabel die aanwezig zijn tijdens de configuratie.  

Een tabelbeperking wordt opgenomen in een model voor productconfiguratie door naar de definitie van de tabelbeperking te verwijzen en de betreffende kenmerken in het model toe te wijzen aan de kolommen in de tabelbeperking.

### <a name="calculations"></a>Berekeningen

Berekeningen vertegenwoordigen een mechanisme om rekenkundige bewerkingen uit te voeren in een configuratiemodel. Bijvoorbeeld, een berekening kan de lengte van een specifiek stuk grondstof bepalen of de verwerkingstijd voor een oppoetsbewerking. Berekeningen zijn noodzakelijk en stellen de waarde in voor een doelkenmerk nadat alle kenmerkwaarden die in de berekeningsexpressie opgenomen zijn, beschikbaar worden.

### <a name="subcomponents"></a>Subonderdelen

Subonderdelen vertegenwoordigen de knooppunten van de structuur van het productconfiguratiemodel. Voor elke subcomponentrelatie moet een verwijzing worden opgegeven voor een productmodel waarvan de technologie voor variantconfiguratie is ingesteld op op beperkingen gebaseerde configuratie.

### <a name="user-requirements"></a>Gebruikersvereisten

Een gebruikersvereiste heeft alle elementen van een subonderdeel. Het enige verschil dat een gebruikersvereiste niet gebonden aan een productmodel. Het praktische effect van dit verschil is dat de stuklijstregels of routebewerking die in de context van een gebruikersvereiste worden gedefinieerd in de bovenliggende route of de componentstuklijststructuur worden samengevouwen. Dit gedrag lijkt op het gedrag van een phantom-stuklijst.

### <a name="bom-lines"></a>Stuklijstregels

Stuklijstregels worden opgenomen om de productiestuklijst voor elke component te identificeren. Een stuklijstregel moet verwijzen naar een artikel en alle artikeleigenschappen kunnen op een vaste waarde worden ingesteld of aan een kenmerk worden toegewezen.

### <a name="route-operations"></a>Routebewerkingen

De routebewerkingen zijn opgenomen om de productieroute te identificeren. Een routebewerking moet verwijzen naar een gedefinieerde bewerking en alle bewerkingseigenschappen kunnen op een vaste waarde worden ingesteld. Alle eigenschappen, behalve bronbehoeften kunnen aan een kenmerk in plaats van een waarde worden toegewezen.

## <a name="validating-and-testing-a-product-configuration-model"></a>Een productconfiguratiemodel valideren en testen
De validatie van een productconfiguratiemodel kan op meerdere niveaus in het model plaatsvinden en kan daarom verschillende bereiken beslaan. Het laagste niveau is voor één expressiebeperking. In dit geval wordt de validatie gewoonlijk uitgevoerd door de productontwerper om te verifiëren dat de syntaxis van een expressie correct is.  

Op dezelfde manier kan een voorwaarde voor een stuklijstregel een routebewerking in isolatie worden gevalideerd.  

De validatie kan ook worden uitgevoerd voor een door de gebruiker gedefinieerde tabelbeperking. In dit geval kan de gebruiker controleren of de waarden die voor elk veld zijn ingevoerd, binnen het domein van de corresponderende kenmerktypen vallen.  

Tot slot kan validatie worden uitgevoerd voor een compleet productconfiguratiemodel om te controleren of de volledige syntaxis klopt en of alle naam- en modelleringsconventies zijn gerespecteerd.

### <a name="testing"></a>Testen

Testen van een model is vergelijkbaar met de uitvoering van een werkelijke configuratiesessie. De gebruiker kan de configuratiepagina's doorlopen en controleren of de modelstructuur het configuratieproces ondersteunt. De gebruiker kan controleren of de kenmerkwaarden correct zijn en of de kenmerkomschrijvingen de gebruiker ondersteunen bij het selecteren van de juiste waarden. Ten slotte probeert het systeem, nadat een testsessie is voltooid, de stuklijst te maken en de route die correspondeert met de geselecteerde kenmerkwaarden, en toont het systeem een foutbericht als er iets misgaat.

### <a name="the-configuration-page"></a>De configuratiepagina

Om tussen componenten te navigeren, klikt u op **Volgende**, of op een onderdeel in de productconfiguratiemodelstructuur om het te selecteren.

## <a name="finalizing-a-model-for-configuration"></a>Een model voor configuratie voltooien
Wanneer een productconfiguratiemodel gereed is voor gebruik in configureren-op-bestellingscenario's, moet een versie worden gemaakt. Er zijn echter meerdere opties die de modelleringservaring kunnen uitbreiden.

### <a name="user-interface"></a>Gebruikersinterface

Het configuratie-gebruikersinterface kan worden gewijzigd door kenmerkgroepen in een of meerdere subcomponenten te introduceren. Dergelijke groepering kan de relaties tussen specifieke kenmerken markeren en de configuratiegebruiker helpen om het gebied van het product identificeren waarop momenteel gefocust wordt.

### <a name="templates"></a>Sjablonen

Een of meerdere configuratiesjablonen kunnen worden gemaakt om het configuratieproces te versnellen. Als alternatief kunnen sjablonen worden gemaakt om specifieke kenmerkcombinaties te promoten, zoals wanneer een verkoopcampagne is gericht op een specifieke set productfuncties.

### <a name="translations"></a>Taalteksten

Als het product in verschillende landen/regio's wordt verkocht, kunnen vertalingen worden gemaakt voor tekst die in de configuratie-UI wordt weergegeven. Deze tekst bevat niet alleen de naam en omschrijvingsvelden, maar ook de waarden van de kenmerktekst.

### <a name="versions"></a>Versies

De laatste stap en belangrijkste in het voltooiingsproces is een versie voor het model te maken. De versie geeft de relatie aan tussen het productmodel, dat kan worden geselecteerd voor configuratie op een order of een offerteregel, en het productconfiguratiemodel. Een versie moet zijn goedgekeurd en geactiveerd voordat deze kan worden gebruikt in een configuratiesessie.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Een productconfiguratiemodel uitbreiden met de API
Een specifieke toepassingsprogrammeringsinterface (API) is geïmplementeerd, zodat partners en anderen die een ontwikkelaarslicentie hebben, de mogelijkheden van een productconfiguratiemodel kunnen uitbreiden. Het belangrijkste doel is een mechanisme te bepalen waarmee partners en de klanten die de bestaande Product Builder gebruiken, de code die in Product Builder-modellen is ingesloten kunnen migreren naar de API. Op deze manier kunnen ze de modellen van Product Builder naar een productconfiguratie migreren. Nieuwe partners en klanten kunnen echter ook profiteren van het gebruik van de API om nieuwe productconfiguratiemodellen uit te breiden.

### <a name="pcadaptor-class"></a>PCAdaptor-klasse

De API wordt uitgevoerd via een set van **PCAdaptor**-klassen die de gegevensstructuur van de productconfiguratiemodellen beschikbaar maken. Een exemplaar van de klasse **PCAdaptor** moet worden gemaakt voor elk model dat wordt uitgebreid. Nadat een configuratiesessie is voltooid, wordt gecontroleerd op een exemplaar van deze klasse en wordt deze uitgevoerd wanneer deze wordt gevonden.  

Het volgende stroomdiagram toont de processtroom van een catalogus.  

[![Stroomdiagram](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Stroomdiagram productconfiguratie-API

## <a name="product-configuration"></a>Productconfiguratie
De productconfiguratie kan worden uitgevoerd van de volgende locaties:

-   Verkooporderregel
-   Verkoopofferteregel
-   Inkooporderregel
-   Productieorderregel
-   Artikelbehoefteregel (project)

Het doel van de configuratie is een aparte variant van het product te maken die voldoet aan de eisen van de klant. Een unieke configuratie-id wordt gemaakt voor elke nieuwe configuratie. Deze id schakelt het bijhouden via voorraad in.

### <a name="multiple-sites-and-intercompany"></a>Meerdere sites en intercompany

Als de configuratie op een locatie of zelfs een bedrijf wordt uitgevoerd dat verschilt van de locatie of het bedrijf waar productie optreedt, worden de stuklijst en de route gemaakt voor en geplaatst op de locatie van de leverancier in het leverende bedrijf. De productvariant wordt in alle bedrijven zijn vrijgegeven die aan de leveringsketen deelnemen.





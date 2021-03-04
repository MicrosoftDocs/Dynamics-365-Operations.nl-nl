---
title: Wat is nieuw of gewijzigd in Dynamics AX 7.0 (februari 2016)
description: In dit artikel worden de functies beschreven die in Microsoft Dynamics AX 7.0 nieuw of gewijzigd zijn. Deze versie bevat zowel platform- als toepassingsfuncties en werd uitgebracht in februari 2016.
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d72eaa28cfe3d114d2ab48cb1e477074a8bf739
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693253"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Wat is nieuw of gewijzigd in Dynamics AX 7.0 (februari 2016)

[!include [banner](../includes/banner.md)]

In dit artikel worden de functies beschreven die in Microsoft Dynamics AX 7.0 nieuw of gewijzigd zijn. Deze versie bevat zowel platform- als toepassingsfuncties en werd uitgebracht in februari 2016.

## <a name="cost-management"></a>Kostenbeheer

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Krijg snel een overzicht van de voorraadbalans, de OHW-voorraadbalans (onderhanden werk) en wat de voorraadmutaties voor de geselecteerde boekperiode zijn.</td>
<td>Niet van toepassing</td>
<td>De werkruimte <strong>Kostenadministratie</strong> bevat een gedeelte waarin het voorraadoverzicht of OHW-voorraadoverzicht voor de geselecteerde boekperiode wordt getoond. Het overzicht is gebaseerd op een gegevenssetcache die standaard om de 24 uur wordt bijgewerkt. De gegevenssetcache kan worden geconfigureerd zodat gebruikers deze handmatig kunnen bijwerken voor de realtime rapportage. De kaart <strong>Status van gegevensvernieuwing</strong> in de werkruimte <strong>Kostenadministratie</strong> laat zien wanneer de cache voor het laatst is bijgewerkt.</td>
<td>Kostencontrollers willen graag weten of de toename of de voorraadbalans of OHW-voorraadbalans in de loop van de tijd toe- of afneemt. Door operationele gebeurtenissen in het overzicht te classificeren, kan de kostencontroller zien welke kant het met de voorraad opgaat. Als de voorraad of OHW-voorraad wordt gewaardeerd op standaardkosten, kan de algemene geregistreerde afwijking eveneens worden bekeken.</td>
</tr>
<tr>
<td>Gebruik de module <strong>Kostenbeheer</strong>.</td>
<td>Niet van toepassing</td>
<td>Kostenbeheer wordt geïntroduceerd als domeingebied. De kostengerelateerde configuratie en inzicht waren verspreid over Voorraadbeheer, Productiebeheer en Leveranciers.</td>
<td>Omdat alle taken die verband houden met kostenbeheer in een module zijn gecentraliseerd, wordt het eenvoudiger voor kostencontrollers om het systeem te onderhouden.</td>
</tr>
<tr>
<td>De boekingstypen die verband houden met voorraadboekhouding en productieboekhouding zijn bijgewerkt.</td>
<td>De labels in de formulieren <strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong> en <strong>ProductionGroup</strong> zijn niet altijd afgestemd met de <strong>LedgerPostingType</strong>-labels die daadwerkelijk worden gebruikt. Het is niet makkelijk om de terminologie te begrijpen die in de labels wordt gebruikt.</td>
<td>De labels zijn bijgewerkt, zodat de labels op de formulieren <strong>InventPosting</strong>, <strong>Resource</strong> <strong>ResourceGroup</strong> en <strong>ProductionGroup</strong> nu overeenkomen met de daadwerkelijke labels op <strong>LedgerPostingType</strong>. De namen van alle labels zijn ook gewijzigd, zodat ze overeenkomen met de operationele gebeurtenissen. Houd er rekenening mee dat de daadwerkelijke logica van het boeken niet is gewijzigd.</td>
<td>Is het eenvoudiger om het systeem te configureren, omdat de labels gerelateerd zijn aan de nieuwe operationele gebeurtenissen die dit boekingstype gebruiken.</td>
</tr>
<tr>
<td>Inkoopprijs, kosten of verkoopprijs im- of exporteren vanuit Microsoft Excel naar of vanuit een kostprijsberekeningsversie.</td>
<td>U kunt niet correct prijzen of kosten in een kostprijsberekeningsversie importeren, omdat het gegevensmodel een InventDim-ID vereist.</td>
<td>De introductie van de gegevensentiteiten maakt het mogelijk om een import-/exportfunctie implementeren. Met deze functie kunnen gebruikers prijzen of kosten in een kostprijsberekeningsversie importeren/exporteren.
<ul>
<li>Een complete lijst importeren van de inkoopprijzen van het volgende jaar, die van de afdeling Inkoop is verkregen.</li>
<li>Verzend kosten en standaardverkoopprijzen van het hoofdkantoor naar een of meerdere verkoopbedrijven in één bewerking.</li>
</ul></td>
<td>Het kan de kostencontrollers een aanzienlijke hoeveelheid tijd besparen wanneer ze het systeem onderhouden, met name als zij vooraf bepaalde kosten voor het volgende boekjaar moeten onderhouden.</td>
</tr>
<tr>
<td>Snel een overzicht krijgen van de voorraadbalans en de gemiddelde eenheidskosten van een kostenobject.</td>
<td>De gebruiker moet het voorhanden formulier openen en de voorraaddimensies selecteren die het kostenobject weergeven. Daarom moet de gebruiker weten welke voorraaddimensies zijn gemarkeerd voor financiële voorraad voor het betreffende product.</td>
<td>Een nieuwe pagina <strong>Kostenobject</strong> is geïntroduceerd. Standaard toont deze pagina alle kostenobjecten die aan het product zijn gerelateerd. De pagina toont de huidige voorraadhoeveelheid, de waarde, en de gemiddelde eenheidskosten per kostenobject.</td>
<td>Dit reduceert de complexiteit en maakt het eenvoudiger om een kostencontroller te zijn.</td>
</tr>
<tr>
<td>Gebruik de nieuwe pagina <strong>Kosteninvoer</strong> tijdens het voorraadbeheer.</td>
<td>Het kan gecompliceerd zijn om voorraadbeheer uit te voeren op geregistreerde voorraadtransacties en bijbehorende vereffeningen, omdat dezelfde transacties fysiek of financieel van aard kunnen zijn.</td>
<td>De pagina <strong>Kosteninvoer</strong> pagina biedt een nieuwe manier om voorraadtransacties weer te geven.
<ul>
<li>Transacties worden in chronologische volgorde weergeven.</li>
<li>Alleen transacties die bijdragen tot kosten zijn opgenomen.</li>
<li>Er is geen concept van fysieke kosten of financiële kosten.</li>
<li>Er is geen concept van fysieke of financiële hoeveelheden.</li>
<li>De kosten worden incrementeel opgeteld.</li>
</ul></td>
<td>Dit kan kostencontrollers veel tijd besparen, wanneer ze voorraadbeheer op transactieniveau moet uitvoeren.</td>
</tr>
<tr>
<td>Gebruik het nieuwe dialoogvenster <strong>OHW-overzicht productie</strong> om een overzichtsweergave te bekijken van gecumuleerde kosten voor een specifiek product.</td>
<td>Niet van toepassing</td>
<td>Het OHW-overzicht geeft een samengevatte OHW-balans van de specifieke productieorder, gegroepeerd in passende kostprijsclassificaties. Een diagram toont in chronologische volgorde hoe de operationele boekingen uitwerken op de OHW-balans.</td>
<td>Dit kan kostencontrollers veel tijd besparen, wanneer ze moet weten wat de actuele OHW-balans op een specifieke productieorder is of hoeveel materiaal voor de order is verbruikt.</td>
</tr>
<tr>
<td>De functie Kostenvergelijking weergeven gebruiken, die is geïntroduceerd voor productieorders. Met deze functie wordt het eenvoudiger om kosten te vergelijken die aan een productieorder zijn gekoppeld.</td>
<td>De gebruiker kan alleen geraamde kosten en gerealiseerde kosten vergelijken. De vergelijking kan op het laagste niveau worden uitgevoerd.</td>
<td>De kostenvergelijkingsfunctie geeft kostencontrollers de mogelijkheid om de volgende gegevens te vergelijken:
<ul>
<li>Actieve kosten met Geraamde kosten = Planningsafwijking</li>
<li>Geraamde kosten met Gerealiseerde kosten = Productieafwijking</li>
<li>Planningsafwijking + Productieafwijking = Totale afwijking</li>
</ul>
Deze functie werkt onafhankelijk van kostprijsberekeningmethodes die aan het geproduceerde artikel zijn toegewezen. Standaard toont een grafiek de kostprijsvergelijking op kostengroeptype. De grafiek biedt gebruikers de mogelijkheid om in te zoomen op meer gedetailleerde niveaus.</td>
<td>Hiermee kunnen kostencontrollers of productiemanagers analyseren waar de productieafwijkingen vandaan komen, en wat de oorzaak ervan is.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Ontwikkelaar

| Wat kunt u doen? | Dynamics AX 2012 | Dynamics AX 7.0 | Waarom is dit belangrijk? |
|------------------|------------------|-----------------|------------------------|
| Webgebaseerde oplossingen in de cloud maken, die vanaf veel apparaten toegankelijk zijn. | Niet beschikbaar | De huidige versie van Dynamics AX is gebaseerd op een nieuw webclient en een clientframework. | Hiermee kunt u uw eindgebruikers zeer geavanceerde oplossingen aanbieden. |
| Ontwikkel uw oplossingen met Microsoft Visual Studio. | Microsoft MorphX is de belangrijkste ontwikkelomgeving, maar een deel van de ontwikkeling wordt uitgevoerd in Visual Studio. | Visual Studio is de enige ontwikkelomgeving. | Hiermee worden de vertrouwde Dynamics AX 2012-concepten bewaard en naadloos aangepast aan het framework en de paradigma's van Visual Studio. Het maakt standaardinteroperabiliteit met andere talen en projecten van .NET mogelijk. |
| Compileer Common Intermediate Language (CIL) voor alle functies. | X++ is gecompileerd naar p-code. | De gloednieuwe X++-compiler genereert CIL voor alle functies. CIL is dezelfde IL (intermediate language) die door andere op .NET-gebaseerde talen wordt gebruikt. | CIL is sneller, kan efficiënt verwijzen naar klassen in beheerde Dynamic Link Libraries (DLL's) en kan worden uitgevoerd op een uitgebreide reeks van .NET-hulpprogramma's. |
| Rapporten en visualisaties voor business intelligence (BI) integreren in de Microsoft Dynamics AX-client. | Niet beschikbaar | Zeer intuïtieve en vloeiende visualisaties maken. | Het biedt inzicht voor besluitvorming dat is gebaseerd op BI. |
| Integreren met Microsoft Office. | Niet beschikbaar | Nieuwe mogelijkheden zijn onder meer de app Excel-gegevensconnector,, de pagina **Werkmapontwerper**, export-API en Documentbeheer. | U kunt productiviteitsoplossingen voor uw eindgebruikers maken. |
| Automatiseer het bouwen, testen en implementeren. | Gedeeltelijk beschikbaar | De ontwikkelaartopologie uitrollen met de Developer-VM en de Build-VM. Configureer automatisch de Build-VM voor detectie, bouw modules vanuit Visual Studio Online (VSO) en voer tests uit. Compilatie en verwijzingen van C\# en X++-modules wordt ondersteund. | Dit vergroot de productiviteit van ontwikkelaars door kosten en arbeid voor testen en validering te reduceren. |
| Aanpassen met overlayering en extensies. | Extensies zijn niet beschikbaar. | De huidige versie van Dynamics AX heeft een nieuw aanpassingsmodel. | U kunt van broncode en metagegevens van modelelementen aanpassen, die Microsoft of externe partners van Microsoft leveren. |
| Stel nieuwe besturingselementen en UI-elementen samen met X++ en een modern webframework. | Aaangepaste besturingselementen zijn afhankelijk van externe frameworks, zoals Microsoft ActiveX en Windows Presentation Foundation (WPF). | Het is eenvoudiger om besturingselementen in de huidige versie te maken. Het X++-framework kan voor toepassingsgedrag en bedrijfslogica worden gebruikt, en een client op basis van HTML/JavaScript maakt moderne visualisaties mogelijk. | Uw besturingselementen kunnen zijn ontworpen met hetzelfde uiterlijk en gedrag als de kant-en-klare besturingselementen van Dynamics AX. |
| Beoordeel en stem prestaties af met nieuwe functies. | PerfSDK, Data Expansion Toolkit, de webapp Trace Parser en PerfTimer zijn niet beschikbaar. | PerfSDK, Data Expansion Toolkit, de webapp Trace Parser en PerfTimer zijn nieuw. | Met de software-ontwikkelingkit (SDK) kunt u alle kritieke bedrijfsprocessen voor prestaties testen en valideren in een testuitvoeringen met één of (indien van toepassing) meerdere gebruikers. Met de Data Expansion Toolkit kunt u alle prestatietests correct uitvouwen, waarvoor hoofdgegevens en transactiegegevens correct moeten zijn uitgevouwen. De Trace Parser kunt u een prestatietest met een enkele gebruiker of uitvoeringen met meerdere gebruikers valideren. Met PerfTimer kunt u zien of bepaalde vragen of methodeaanroepen leiden tot prestatieproblemen. Daarom hoeft u geen trace uit te voeren en deze tot in detail analyseren. |
| Bijwerkbare weergave tonen door OData te gebruiken. | Niet beschikbaar | De huidige versie van Dynamics AX introduceert een openbaar OData-service-eindpunt dat toegang tot Dynamics AX-gegevens mogelijk maakt, op consistente wijze en voor een breed bereik van clients. | Uw oplossingen kunnen interageren met RESTful-services, gegevens op een detecteerbare manier delen en brede integratie mogelijk maken door middel van het HTTP-stackprotocol. |
| Zet de Business Connector in om scenario's voor bedrijfslogica en ondersteuningintegratie op te stellen. | De Business Connector is beschikbaar om X++-code aan te roepen vanuit beheerde code. Het wordt aangeraden om de bedrijfsconnector alleen te gebruiken om bedrijfslogica op te stellen in C\#, maar niet voor integratiescenario's. | De Business Connector wordt niet meer ondersteund. In de behoefte om scenario's aan te maken wordt voorzien doordat X++ in de beheerde code is gecompileerd. Daarom is interop eenvoudiger. In integratiescenario's wordt voorzien door middel van OData. | U kunt de Business Connector in de toekomst niet meer gebruiken. |
| Kies de schaal (het aantal decimalen) voor de echte databasevelden en uitgebreide gegevenstypes (EDT's). | Schaal 16 is de standaardschaal en kan niet door de ontwikkelaar worden gewijzigd. | EDT's en velden hebben nu een eigenschap 'schaal´, die op afzonderlijke velden en EDT's kan worden toegepast. De standaardwaarde is ingesteld op 6 in plaats van 16. | De prestaties met NCCI-tabellen (ondersteuning in geheugen in SQL) zijn vele malen sneller wanneer een kleinere schaal wordt gebruikt. Pas de schaal aan op uw gebruik van de afzonderlijke velden. |

## <a name="financial-management"></a>Financieel beheer

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rekeningstructuren exporteren naar Microsoft Excel.</td>
<td>Niet beschikbaar</td>
<td>U kunt nu een rekeningstructuur selecteren en deze naar Excel exporteren.</td>
<td>Veel klanten hebben gevraagd om de mogelijkheid om rekeningstructuren naar Excel te exporteren voor makkelijker filteren.</td>
</tr>
<tr>
<td>Geef op een enkele pagina grootboeken en geavanceerde regelstructuren weer die aan een rekeningstructuur zijn gekoppeld.</td>
<td> De gebruiker moet naar meerdere formulieren navigeren om het grootboek en de rekeningstructuur te zien die worden gebruikt.</td>
<td>Feitenblokken zijn toegevoegd aan de rekeningstructuurpagina.</td>
<td>Toegang tot belangrijke informatie is eenvoudiger wanneer de rekeningstructuren worden gedefinieerd en bewerkt.</td>
</tr>
<tr>
<td>Op een enkele pagina grootboeken weergeven die aan een rekeningschema zijn gekoppeld.</td>
<td>De gebruiker moet naar elk bedrijf navigeren en het grootboekformulier openen om het rekeningschema te zien dat toegewezen is aan het grootboek.</td>
<td>Feitenblokken zijn toegevoegd aan de pagina <strong>Rekeningschema</strong>.</td>
<td> Toegang tot belangrijke informatie is eenvoudiger wanneer een rekeningschema is gedefinieerd en toegewezen.</td>
</tr>
<tr>
<td>Geef correcties op het afsluitwerkblad en afsluittransacties weer in afzonderlijke kolommen op de lijstpagina <strong>Proefbalans</strong>.</td>
<td>De gebruiker ziet beide transactietypen in één kolom.</td>
<td>Een extra parameter is toegevoegd aan de lijstpagina <strong>Proefbalans</strong>.</td>
<td>Dit maakt beknoptere analyse van gegevens mogelijk en is in sommige landen/regio's ook vereist voor verplichte rapportage.</td>
</tr>
<tr>
<td>Gebruik de nieuwe pagina <strong>Globale algemene journalen</strong>.</td>
<td>Niet beschikbaar</td>
<td>Nieuwe pagina <strong>Globale algemene journalen</strong> voor het invoeren van algemene journalen. Rechten voor deze pagina worden toegevoegd aan de rol <strong>Accountant</strong>.</td>
<td>Maakt het mogelijk voor een gedeelde service-accountant om dagboeken voor verschillende bedrijven in te voeren zonder het formulier te hoeven verlaten of naar een andere bedrijfscontext te hoeven overschakelen.</td>
</tr> 
<tr>
<td>Gebruik de nieuwe pagina <strong>Boekhoudingsbronverkenner</strong>.</td>
<td>Beschikbaar vanaf Dynamics AX 2012 R3-CU10.</td>
<td>Nieuwe pagina <strong>Boekhoudingsbronverkenner</strong> en acties om daar naartoe te gaan vanaf de lijspagina <strong>Proefbalans</strong> en de pagina <strong>Boekstuktransacties</strong>.</td>
<td>Maakt het mogelijk de meest gedetailleerde informatie te bekijken over de bron voor een proefbalans of een journaalregel in het grootboek voor ad hoc analyse.</td>
</tr>
<tr>
<td>Voeg extra boekingslagen toe.</td>
<td>Het toevoegen van extra boekingslagen was een activiteit voor ontwikkelaars.</td>
<td>Nu zijn er tien boekingslagen beschikbaar.</td>
<td>De meeste klanten voegen extra boekingslagen toe.</td>
</tr>
<tr>
<td>Gebruik de optie Verwant boekstuk.</td>
<td>Niet beschikbaar</td>
<td>De optie Verwant boekstuk is beschikbaar voor gebruikers die het boekstuk in het tegenbedrijf zien bij het boeken van intercompany-transacties. Vanuit de verwante boekstukken kunnen gebruikers op de details klikken en snel naar het boekstuk van het tegenbedrijf gaan.</td>
<td>Bij het boeken van intercompany-transacties hadden gebruikers geen zicht op het boekstuk dat werd geboekt in het tegenbedrijf en konden zij dit niet traceren.</td>
</tr>
<tr>
<td>Groot aantal financiële perioden afsluiten</td>
<td>Niet beschikbaar</td>
<td>Gebruikers kunnen de toegang tot de module bijwerken en de status van de periode wijzigen voor meerdere bedrijven tegelijk.</td>
<td>Vóór de beschikbaarheid van de functie moesten gebruikers wijzigen bij welk bedrijf ze waren aangemeld, naar het formulier Grootboekkalender gaan en handmatig de toegang tot de module en periodestatus bijwerken.</td>
</tr>
<tr>
<td>Wisselkoersen worden geleverd door Oanda.</td>
<td>Het configureren van de wisselkoersprovider voor het importeren van wisselkoersen vanuit Oanda was een activiteit voor ontwikkelaars.</td>
<td>Als gebruikers een sleutel voor Oanda hebben, kunnen zij deze invoeren bij het configureren van de wisselkoersprovider.</td>
<td>Gebruikers kunnen gebruikmaken van de standaardfunctionaliteit door volgens schema wisselkoersen van Oanda te laten importeren.</td>
</tr>
<tr>
<td>Filter financiële rapporten (Management Reporter) op basis van dimensies, kenmerken, datums en scenario's.</td>
<td> Al het filteren van Management Reporter-rapporten wordt afgehandeld via het ontwerp van het rapport. Als bijvoorbeeld een gebruiker die weergavebevoegdheden heeft een rapport voor een andere datum wil weergeven, moet een rapportontwerper de wijziging doorvoeren.</td>
<td>Rapportopties zijn toegevoegd, zodat verschillende filters kunnen worden toegepast wanneer een gebruiker een rapport weergeeft. Een nieuw rapport wordt dan gegenereerd op basis van die filters.</td>
<td>De consumenten van financiële rapporten kunnen verschillende filters voor dimensies, datums, kenmerken, en scenario's toepassen zonder dat het rapportontwerp moet worden aangepast.</td>
</tr>
<tr>
<td>Bekijk financiële rapporten (Management Reporter) binnen de Microsoft Dynamics AX-client.</td>
<td>Een afzonderlijke webclient werd gebruikt om Management Reporter-rapporten weer te geven.</td>
<td>Alle financiële rapporten kunnen in de Dynamics AX-client worden geopend. De gebruiker selecteert een rapport om weer te geven en het rapport wordt geopend in de client.</td>
<td>U kunt financiële rapporten nu bekijken zonder daarvoor een andere client/toepassing te openen.</td>
</tr>
<tr>
<td>Financiële rapporten (Management Reporter) van de Microsoft Dynamics AX-client afdrukken.</td>
<td>Bij het afdrukken van een rapport werden de afdrukopties van de browser gebruikt voor afdrukken en werd alleen afgedrukt wat gebruikers op het scherm kunnen zien.</td>
<td>De gebruiker kan het detailniveau en de pagina-instelling voor een rapport kiezen via de optie Afdrukken in het financiële rapport in de Dynamics AX-client.</td>
<td>Afgedrukte rapporten worden afgedrukt op de manier die gebruikers verwachten in plaats van dat een webpagina wordt afgedrukt.</td>
</tr><tr>
<td>Analyseer financiële gegevens met het Power BI-inhoudpakket 'Financiële prestaties controleren'.</td>
<td>Niet beschikbaar</td>
<td>Selecteer in PowerBI.com <strong>Get Data</strong> en selecteer vervolgens het inhoudpakket <strong>Dynamics AX - Financial performance</strong>. Voer de URL voor uw Dynamics AX-eindpunt in om uw gegevens in het dashboard te bekijken.</td>
<td>Met drie tot vier muisklikken kunnen organisaties een Power BI-dashboard met belangrijke financiële gegevens uitrollen. De inhoud kan door de organisatie worden gepersonaliseerd.</td>
</tr>
<tr>
<td>Afsluitingsprocessen voor financiële periodes volgen</td>
<td>Niet beschikbaar</td>
<td>De afsluitingssjablonen en -plannen kunnen worden gemaakt met de Financiële periode afsluiten configuratie. Met de werkruimte <strong>Financiële periode afsluiten</strong> kan de voortgang van afsluitingsplannen voor meerdere bedrijven worden gevolgd.</td>
<td>Deze werkruimte maakt handmatige systemen voor het definiëren, plannen en communiceren van afsluitingsactiviteiten overbodig. Zo kunt u het aantal dagen voor afsluiting reduceren.</td>
</tr>
<tr>
<td>Vergelijk budgetgegevens met werkelijke cijfers en stel grootboekprognoses op met de werkruimte <strong>Grootboekbudgetten en prognoses</strong> en aanvullende queryformulieren.</td>
<td>Niet beschikbaar</td>
<td> Toegang tot de werkruimte gaat via Dynamics AX-dashboard. Deze bevat koppelingen naar verschillende nieuwe querypagina's: <strong>Overzicht werkelijke waarden versus budget</strong>, <strong>Overzicht statistieken voor budgetbeheer</strong>, <strong>Budgetregisterposten</strong> en <strong>Budgetplannen</strong>.</td>
<td>Nieuwe querypagina's geven eenvoudig toegang tot budgetgegevens. De werkruimte combineert alle taken voor beheer en monitoring van het budget in één plaats, waardoor budgetmanagers of boekhoudmanagers gemakkelijker kunnen werken.</td>
</tr>
<tr>
<td>Maak indelingen voor budgetplannen en prognoses.</td>
<td>Het document <strong>Budgetplan</strong> wordt weergegeven als lijst van regels met ingangsdatums en bedragen voor combinaties van financiële dimensies. De gebruiker moet Excel-sjablonen maken en gebruiken om de gegevens van budgetplannnen in een draaitabel weer te geven.</td>
<td>Een onbeperkt aantal indelingen is beschikbaar voor budgetplannen en prognoses. U kunt geselecteerde financiële dimensies, door de gebruiker gedefinieerde kolommen en andere rijkenmerken (zoals opmerkingen, projecten, en activa) in de indeling combineren. Gebruikers kunnen meteen overschakelen tussen indelingen voor het document van het budgetplan en gegevens bewerken door elke geselecteerde indeling te gebruiken. De configuratie van budgetplanning is vereenvoudigd door scenariobeperkingen te schrappen en indelingen te gebruiken om te bepalen welke gegevens in elke fase van het document met het budgetplan kunnen worden bekeken en bewerkt.</td>
<td>Het geeft de flexibiliteit om budgetplannen te maken en te bewerken met zowel Excel als de Dynamics AX-client. Sjablonen voor Excel-werkmappen kunnen worden gegenereerd door de configuratie voor budgetplanindeling.</td>
</tr>
<tr>
<td>Druk het rapport <strong>Leveranciersfactuurtransacties</strong> af door informatie van het rapport <strong>Gedetailleerde vervaldagenlijst</strong> te gebruiken, dat de dagen na vervaldatum bevat.</td>
<td>U moet twee verschillende rapporten afdrukken: <strong>Gedetailleerde vervaldagenlijst</strong> en <strong>Leveranciersfactuurtransacties</strong>.</td>
<td>De informatie voor de rapporten is geconsolideerd in het rapport <strong>Leveranciersfactuurtransacties</strong>. Het rapport <strong>Gedetailleerde vervaldagenlijst</strong> is afgeschaft.</td>
<td>Hierdoor vervalt de noodzaak om twee afzonderlijke maar gerelateerde rapporten af te drukken.</td>
</tr>
<tr>
<td>Direct wettelijk verplichte rapporten genereren in PDF-indeling.</td>
<td>U moet eerst een wettelijk verplicht rapport in een bepaalde indeling genereren en het vervolgens exporteren naar PDF-indeling.</td>
<td>De PDF-indeling is de standaardindeling voor wettelijk voorgeschreven rapporten.</td>
<td>Het biedt een standaardvertoningservaring op zowel de computermonitor als papieren afdrukken.</td>
</tr>
<tr>
<td>Het proces voor btw-vereffening uitvoeren als een batchproces.</td>
<td>Niet beschikbaar</td>
<td>Op de pagina <strong>Btw-vereffeningsperiode</strong> kunt u opgeven dat het vereffeningsproces moet worden uitgevoerd in de batchmodus.</td>
<td>Voor perioden die veel belastingtransacties hebben, kan het vereffeningsproces tijdrovend zijn en is het mogelijk beter om het proces op de achtergrond uit te voeren als batchproces.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Stichting

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Krijg overal en altijd toegang tot de client.</td>
<td>De AX 2012-desktopclient biedt een volledige set formulieren, maar het kan alleen worden uitgevoerd op computers met Microsoft Windows en moet daarop worden geïnstalleerd. Terminal Server wordt vaak gebruikt met de desktopclient voor toegang in een draadloos netwerk (WAN). De Enterprise Portal-webclient biedt een kleinere set formulieren.</td>
<td>De twee AX 2012-clients zijn vervangen door een enkele, op standaarden gebaseerde webclient die de volledige functionaliteit van de desktopclient biedt samen met het bereik van de Enterprise Portal-client.</td>
<td>Hiermee wordt voorkomen dat ontwikkelingsarbeid moet worden verdeeld over twee UI-platforms. Door gebruik van standaardwebinterfaces is Terminal Server overbodig.</td>
</tr>
<tr>
<td>Productief werken met de nieuwe Taakrecorder.</td>
<td>De Taakrecorder in AX 2012 vereist rechtstreekss toegang tot een AOS-computer (Application Object Server) en uitgebreide bevoegdheden, en biedt geen opties voor bewerken.</td>
<td>De nieuwe Taakrecorder kan rechtstreeks vanuit de webclient worden gebruikt. Toegang tot de Taakrecorder vereist geen beheerdersbevoegdheid. De geregistreerde stappen kunnen live worden weergegeven terwijl u registreert, nieuwe opties voor bewerken zijn ingevoerd en het Taakrecorder ondersteunt meer scenario's naast de bestaande scenario's van de modelleertool voor bedrijfsprocessen.</td>
<td>De nieuwe Taakrecorder biedt een gestroomlijnde ervaring en ontsluit nieuwe mogelijkheden in Dynamics AX. Enkele van deze mogelijkheden zijn nu al beschikbaar, en meer zullen in de toekomst volgen.</td>
</tr>
<tr>
<td>Help gebruikers hun toekomstige werk met werkruimten beter te begrijpen.</td>
<td>Rollencentrums bieden een overzicht met informatie die betrekking heeft op de taakfunctie van een gebruiker in het bedrijf of de organisatie.</td>
<td>Werkruimten zijn een nieuw concept in Dynamics AX die zijn bedoeld ter vervanging van rollencentrums als de belangrijkste manier om naar taken en specifieke pagina's te navigeren. Zij bieden een overzicht van één pagina van een bedrijfsactiviteit en helpen gebruikers de huidige status, de verwachte werklast en de prestaties van het proces of de gebruiker te begrijpen. Werkruimten zijn meer gedetailleerd dan AX 2012-rollencentrums en een gebruiker kan toegang hebben tot meerdere werkruimten.</td>
<td>Werkruimten zijn bedoeld ter verhoging van de gebruikersproductiviteit. Ontwikkelaars moeten een werkruimte maken voor elke belangrijke activiteit die in het product wordt ondersteund. Een oud rollencentrum van AX 2012 wordt meestal vervangen door meerdere werkruimten in de huidige versie van Dynamics AX.</td>
</tr>
<tr>
<td>Maak formulieren die reageren op de browserviewport- of apparaatgrootte.</td>
<td>In AX 2012 lag de opmaak van de formulierinhoud strak vast aan de hand van kolommen en werd de totale hoogte/breedte van het formulier voornamelijk bepaald op basis van de besturingselementen op het formulier.</td>
<td>Met de overschakeling naar het web in de meest recente Dynamics AX zijn de afmetingen van het formulier nu gebaseerd op de grootte van de viewport van de browser of het apparaat. Besturingselementen en de parameters van de lay-out zijn gewijzigd of toegevoegd om beter te kunnen reageren op de wijzigingen in de grootte van de viewport.</td>
<td>Formulierinhoud moet beter reageren om optimaal gebruik te maken van de beschikbare hoogte/breedte van de browser of het apparaat. Het realiseren van dit reactievermogen vereist mogelijk wijzigingen in de manier waarop een formulier is vormgegeven.</td>
</tr>
<tr>
<td>Gebruik patronen voor een verbeterde formulierontwikkeling.</td>
<td>Er waren formuliersjablonen beschikbaar als uitgangspunt voor het ontwikkelen van formulieren in AX 2012 op basis van een formulierstijl. Formulierstijl controleren is een optionele module die informatie verstrekt over hoe een formulier afwijkt van de overeenkomstige sjabloon.</td>
<td>In de huidige versie van Dynamics AX zijn formulierpatronen geïntroduceerd. Formulierpatronen vormen een combinatie van formuliersjablonen en Formulierstijl controleren die nauw zijn geïntegreerd in het ontwikkelingsproces. Er zijn patronen gedefinieerd op het formulierniveau (zoals AX 2012) en er zijn nu subpatronen beschikbaar op het niveau van de groep en de tabblad.</td>
<td>Formulieren die aan patronen voldoen hebben tal van voordelen zoals een consistentere gebruikersinterface, eenvoudigere ontwikkeling, een gemakkelijker pad voor formulierupgrades en meer vertrouwen in de flexibiliteit an de formulierlay-out.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Help

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Gebruik begeleide procedurele Help (taakbegeleidingen) en concepuele onderwerpen door op <strong>Help</strong> te klikken.</td>
<td>Het Help-systeem van AX 2012 wijst de weg naar HTML-onderwerpen die op een lokale webserver zijn opgeslagen. Klanten en partners kunnen hun eigen Help maken.</td>
<td>Het Help-systeem in de huidige versie van AX geeft taakbegeleidingen weer die zijn opgeslagen in de BPM van Microsoft Dynamics Lifecycle Services (LCS). Het Help-systeem geeft ook onderwerpen van de MicrosoftDocs-site weer. Zie <a href="help-overview.md" data-raw-source="[Help system](help-overview.md)">Help-systeem</a> en <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides (February 2016)](new-task-guides-available-february-2016.md)">Nieuwe taakbegeleidingen (februari 2016)</a> voor meer informatie.</td>
<td>De taakbegeleidingen bieden een interactieve geleide ervaring die u door de stappen van een taak of een bedrijfsproces leidt. U kunt de taakbegeleidingen die Microsoft biedt downloaden en aanpassen. Het onderwerp biedt een snellere en flexibelere manier om productdocumentatie te maken, leveren en bijwerken. Zo helpt het te garanderen dat u toegang tot de meest recente technische informatie hebt.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Human Capital-beheer

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vaardigheden en certificaten doorgeven aan cursusdeelnemers na afloop van de cursus.</td>
<td>Dit is een handmatig proces.</td>
<td>Als een cursus is voltooid, wordt een nieuwe optie beschikbaar om de records van een deelnemer bij te werken met de nieuwe vaardigheden en de certificaten.</td>
<td>Dit is een nieuwe en efficiënte manier om werknemerrecords bij te werken.</td>
</tr>
<tr>
<td>Snel het dienstverband controleren.</td>
<td>Dit is een handmatig proces.</td>
<td>Uw HR-afdeling kan dienstverbanden snel controleren door een werkruimte of de werknemerpagina te gebruiken.</td>
<td>Uw HR-afdeling moet niet meer meerdere pagina's openen om de begindatum, de manager, de maanden in de functie en compensatiegegevens te controleren.</td>
</tr>
<tr>
<td>Werknemers informatie in het systeem laten weergeven, bijwerken en verwijderen.</td>
<td>Beschikbaar, maar met beperkte mogelijkheden voor weergeven en bijwerken.</td>
<td>Deze functie is ingeschakeld en laat werknemers en contractanten een breed bereik van persoonlijke gegevens weergeven. Desgewenst kan een workflow worden gebruikt wanneer de gegevens worden gemaakt, bijgewerkt of verwijderd.</td>
<td>Het geeft werknemers controle over hun eigen gegevens, of dat nu het bijwerken van adres- of contactgegevens, het solliciteren op een functie, het invullen van een vragenlijst of, het bijwerken van hun foto omvat. Wanneer een workflow is ingeschakeld, kan de informatie door een goedkeurder worden gecontroleerd of automatisch worden goedgekeurd, op basis van uw bedrijfsprocessen.</td>
</tr>
<tr>
<td>Managers gegevens van werknemers laten weergeven of bewerken.</td>
<td>Beschikbaar, maar met beperkte mogelijkheden voor weergeven en bijwerken.</td>
<td>Afhankelijk van de configuratie-instellingen beveiliging kunnen managers werknemerinformatie weergeven of bewerken.</td>
<td>Hiermee hebben managers toegang tot belangrijke gegevens van de werknemers, zodat zij betere beslissingen kunnen nemen over toewijzing van bronnen, prestaties en werknemerontwikkeling.</td>
</tr>
<tr>
<td>Profiteer van de selfservice-functionaliteit voor managers.</td>
<td>Niet beschikbaar</td>
<td>Managers kunnen nu verzoeken indienen voor nieuwe werknemers (werknemers en contractanten), overplaatsing en ontslag (beëindiging van dienstverband). Managers kunnen ook verzoeken om een nieuwe positie, verlenging van de duur van een positie of positiewijzigingen.</td>
<td>Deze scenario's waren eerder alleen beschikbaar voor Human Resources. Het inschakelen van deze scenario's biedt krachtige hulpprogramma's voor managers in een organisatie. Optionele werkstromen kunnen worden ingeschakeld om het vereiste niveau van evaluatie en goedkeuring te bieden.</td>
</tr>
<tr>
<td>De resultaten van compensatieverwerking bekijken.</td>
<td>De resultaten zijn alleen beschikbaar op het moment van verwerking.</td>
<td>De resultaten van de compensatieverwerking kunnen nu op elk moment worden geopend nadat het proces is uitgevoerd.</td>
<td>Het bevat een uitstekende audit van het proces en het resultaat van het proces. Het biedt ook een uitgebreide weergave van de gegevens voordat de werknemerrecords worden bijgewerkt.</td>
</tr>
<tr>
<td>De resultaten van vergoedingenverwerking bekijken.</td>
<td>De resultaten zijn alleen beschikbaar op het moment van verwerking.</td>
<td>De resultaten van de vergoedingenverwerking kunnen nu op elk moment worden geopend nadat het proces is uitgevoerd.</td>
<td>Het biedt een uitgebreide weergave van de gegevens die door inschrijving op vergoedingen en kostenwijzigingen worden bijgewerkt.</td>
</tr>
<tr>
<td>Wijzigingen in de tijdlijn van de ingangsdatum weergeven.</td>
<td>Niet beschikbaar</td>
<td>Deze vergelijkingstool is beschikbaar voor werknemers, posities en functies. Het biedt een uitgebreide weergave van wijzigingen tussen verschillende versies van een record.</td>
<td>Hiermee bespaart u tijd wanneer u wijzigingen weergeeft die in de loop der tijd zijn doorgevoerd in records van werknemers, posities en functies. Zo kunt u snel twee versies van een record vergelijken, of alle records, in de loop van de tijd.</td>
</tr>
<tr>
<td>Werknemers weergeven op bedrijf.</td>
<td>Dit is een handmatig proces dat met filteren wordt uitgevoerd.</td>
<td>Lijsten van werknemers en contractanten worden automatisch gefilterd op het bedrijf waarbij u bent aangemeld.</td>
<td>Het biedt een gefilterde weergave van werknemers die in het aangemelde bedrijf in dienst zijn. Voor een ongefilterde weergave van alle werknemers en contractanten is de werknemerlijst nog beschikbaar. In de huidige versie van Dynamics AX wijzigt het systeem niet het bedrijf op basis van de werknemer die in de lijst is geselecteerd.</td>
</tr>
<tr>
<td>De lijst van cursusdeelnemers bijwerken.</td>
<td>Niet beschikbaar</td>
<td>Cursusdeelnemers kunnen uit de deelnemerslijst worden verwijderd.</td>
<td>Het biedt een gemakkelijke manier om cursusdeelnemers bij te werken die zich per ongeluk hebben aangemeld.</td>
</tr>
<tr>
<td>Compensatiegebeurtenissen in een groep beheren.</td>
<td>Niet beschikbaar</td>
<td>Deze functie stroomlijnt de verwerking van compensatiewijzigingen voor werknemers.</td>
<td>Het biedt een eenvoudig, gestroomlijnd proces voor het bijwerken van werknemerrecords door middel van de compensatiewerkruimte en de bijbehorende pagina's.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Voorraadbeheer

Geen nieuwe functies zijn toegevoegd.

## <a name="localization"></a>Lokalisatie

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Elektronische documenten configureren en genereren om aan de wettelijke vereisten in verschillende landen/regio's te voldoen.</td>
<td>De elektronische documenten zijn in code vastgelegd in X++ of als Extensible Stylesheet Language Transformaties (XSLT's). Eventuele indelingscorrecties vereisen ontwikkelingsarbeid. De toegang tot gegevens en opmaak zijn niet geïsoleerd. Een aangepaste indelingsplaatsing vereist een nieuw Microsoft Dynamics AX-hotfixpakket om de bestaande indeling te overschrijven. Eigen aanpassingen van de indelingen moeten handmatig worden overgezet naar de broncode van een nieuw Microsoft Dynamics AX-hotfixpakket.</td>
<td>Elektronische rapportage (ER) is een nieuw hulpmiddel om elektronische documenten te configureren en te genereren die zijn bedoeld voor bedrijfsgebruikers in plaats van ontwikkelaars. Met ER kunt u gegevensmodellen opstellen die domeinspecifiek zijn en onafhankelijk van de Microsoft Dynamics AX-database als gegevensbronnen voor documentindelingen. Een bedrijfsgebruiker kan de indelingen configureren op basis van deze domeinspecifieke gegevensmodellen (bijvoorbeeld, voor betalingen, Intrastat-aangiften of belastingaangiften). De gebruiker configureert de indelingen met eenvoudige visuele tools die lijken op Excel. ER ondersteunt momenteel het genereren van elektronische documenten in de indelingen tekst, XML en Excel. Deze documenten kunnen tegelijkertijd worden gegenereerd en in zipbestanden worden verpakt. De gegevensmodellen en indelingen ondersteunen versiebeheer. De indelingsversies kunnen geldigheidsperioden hebben. Elk versie van een gegevensmodel of indeling wordt opgeslagen in een afzonderlijke configuratie en via LCS gedistribueerd naar partners en klanten. Partners en klanten kunnen Microsoft-gegevensmodellen en -indelingen aanpassen, of hun eigen maken. ER slaat configuratiewijzigingen van partners en klanten op als delta's van de Microsoft-configuraties, wat upgrades naar nieuwe versies van Microsoft-configuraties vereenvoudigt. Door LCS te gebruiken, kunnen partners hun configuraties van gegevensmodellen en indelingen ook met andere klanten en partners delen, die deze kunnen aanpassen en verspreiden. De delta-aanpassing en eenvoudige upgrade worden ondersteund door de gehele aanpassingsketen.</td>
<td>ER vereenvoudigt het maken, onderhouden, en upgraden van elektronische documentindelingen waarmee u kunt voldoen aan wettelijke vereisten in verschillende landen/regio's. ER maakt het proces om elektronische documentindelingen te maken of te wijzigen sneller en eenvoudiger. Deze wijzigingen kunnen worden doorgevoerd door bedrijfsgebruikers in plaats van ontwikkelaars. ER maakt het voor klanten en partners sneller en gemakkelijker om hun indelingsaanpassingen naar nieuwe versies van indelingen te upgraden, die door Microsoft of andere partners worden vrijgegeven. ER biedt een gemeenschappelijke manier (door LCS) voor Microsoft en partners om elektronische documentconfiguraties te verspreiden naar andere klanten en partners. ER maakt het ook voor partners en klanten eenvoudiger om elektronische documentindelingen voor hun specifieke bedrijfsbehoeften aan te passen, bij te werken en te verspreiden.</td>
</tr>
<tr>
<td>(MEX) De Mexicaanse wettelijk verplichte rapporten voor VAT (btw) genereren.</td>
<td>U moet de rapporten <strong>BTW omzet en inkopen</strong> genereren met de functionaliteit voor niet-gerealiseerde btw, zodat gebruikers transacties kunnen identificeren die tot de gerealiseerde en niet-gerealiseerde secties behoren op basis van de status.</td>
<td>De rapporten <strong>BTW omzet en inkopen</strong> zijn gewijzigd en wegen nu de voorwaardelijke belastingfunctie alleen mee door specifieke vereffeningsperioden te gebruiken voor de definitie van codes voor niet-gerealiseerd en gerealiseerde btw.</td>
<td>Wijzigingen in de configuratie van btw-codes zijn vereist voordat gebruikers deze rapporten correct kunnen genereren. Een voorwaardelijke btw-functie is vereist, en de gebruiker moet afzonderlijke vereffeningsperioden configureren, zowel niet-gerealiseerd als gerealiseerd, om de transacties in de gerelateerde sectiegebieden te identificeren.</td>
</tr>
<tr>
<td>(JPN) Het Japanse document voor aangifte van versnelde afschrijving van vaste assets beheren.</td>
<td>Niet beschikbaar</td>
<td>De belangrijkste aangiftegegevens worden centraal opgeslagen in één document voor beter beheer.</td>
<td>Conformiteit van documenten en het beheersgemak helpen problemen tijdens audits en andere controles reduceren.</td>
</tr>
<tr>
<td>(JPN) JBA-tekens op de bankrekening verifiëren.</td>
<td>Niet beschikbaar</td>
<td>U kunt verifiëren of de kana-velden voor de naam alleen de tekens bevatten die de JBA-bankindeling toestaat.</td>
<td>Dit helpt onderbrekingen voor gebruikers tijdens het genereren van betalingsbestanden vanwege ongeldige tekens te verminderen.</td>
</tr>
<tr>
<td>(JPN) Het Japanse afrondingsverschil voor vaste activa aan het einde van het fiscale jaar inlopen.</td>
<td>Niet beschikbaar</td>
<td>Op de pagina <strong>Vaste-activaparameters</strong> kunt u kiezen om in te lopen aan het einde van de boekperiode of van het fiscale jaar.</td>
<td>Het biedt meer flexibiliteit voor aansluiting aan lokale praktijken.</td>
</tr>
<tr>
<td>(JPN) De Japanse Toegevoegde tabellen voor aangifte van vennootschapsbelasting reeks 16 genereren tegen een aggregatiebedrag op hooftypen van vaste assets.</td>
<td>Niet beschikbaar</td>
<td>Voor de waardemodellen van vaste activa kunt u kiezen om samen te vatten op hoofdtype. Standaard wordt deze functionaliteit gebruikt voor nieuwe vaste activa.</td>
<td>Voor grote bedrijven die duizenden vaste activa hebben, verlagen de samengevatte rapporten aanzienlijk de grootte van het rapport dat wordt gegenereerd.</td>
</tr>
<tr>
<td>(JPN) De reservering voor speciale afschrijving starten vanaf het volgende boekjaar voor vaste activa in Japan.</td>
<td>Niet beschikbaar</td>
<td>Op de waardemodellen van vaste activa die een geschikte buitengewone-afschrijvingsprofiel hebben, kunt u kiezen om de toewijzing te starten vanaf de volgende boekperiode of het volgende boekjaar.</td>
<td>Het biedt meer flexibiliteit voor aansluiting aan lokale praktijken.</td>
</tr>
<tr>
<td>(JPN) Een Japans verbruiksbelastingrapport generen dat de herziene belastingtarieven bevat.</td>
<td>De verbruikbelastingrapportage is beschikbaar voor een belastingtarief van 5 procent.</td>
<td>De verbruikbelastingrapportage bevat een onderdeel voor het herziene btw-tarief (bijvoorbeeld, 8 procent).</td>
<td>De indeling is onlangs aangekondigd door de overheid.</td>
</tr>
<tr>
<td>(EU) Afrondingsinstellingen configureren voor EU-verkooplijst.</td>
<td>Afrondingsinstellingen voor de EU-verkooplijstrapportage voor verschillende landen zijn hard gecodeerd in X ++ of Extensible Stylesheet Language Transformations (XSLT's).</td>
<td>Afrondingsinstellingen worden toegevoegd aan parameters voor buitenlandse handel. Kunt u afrondingsprecisie, afrondingsmethode, uitvoerprecisie en gedrag voor bedragen die kleiner zijn dan de afrondingsprecisie configureren.</td>
<td>Hiermee wordt de configuratie van de EU-verkooplijstrapportage gelijkgeschakeld en vereenvoudigd. Aanpassing van afrondingsinstellingen vereist niet langer ontwikkelingsinspanningen.</td>
</tr>
<tr>
<td>(EU) Toepasbaarheidsregels voor verlegging configureren.</td>
<td>Toepasbaarheidsregels voor verlegging zijn hard gecodeerd voor het binnenlandse verleggingsscenario. De toepasbaarheidsdrempel kan worden ingesteld per artikelgroep. De functionaliteit is alleen beschikbaar voor Groot-Brittannië.</td>
<td>U kunt toepasbaarheidsregels voor verlegging per documenttype (inkoop-/verkooporder, leveranciersfactuur, factuur met vrije tekst enz.) configureren en een verleggingsgroep die artikelen, artikelgroepen en inkoop-/verkoopcategorieën combineert. De toepasbaarheidregels hebben een specifieke ingangsdatum. U kunt ook afzonderlijke btw-codes in btw-groepen markeren van zover van toepassing voor verlegging. Het verkoopfactuurrapport wordt aangepast om details van de toegepaste verlegging weer te geven. De functionaliteit is beschikbaar voor alle Europese landen/regio's.</td>
<td>Deze wijziging verenigt de configuratie van de toepasbaarheidsregels voor verlegging en ondersteunt het aannemen van binnenlandse voorschriften voor verlegging door Europese landen.</td>
</tr>
<tr>
<td>(DE) Het Duitse auditfile - GDPdUGoBD genereren</td>
<td>Gebruikers kunnen de definitie instellen van tabellen met financiële gegevens die moeten worden geëxporteerd in een indeling die wordt geaccepteerd door Duitse accountants en autoriteiten.</td>
<td>De functie is geïmplementeerd als een configuratie voor elektronische rapportage. Deze functionaliteit is beschikbaar voor Duitsland en Oostenrijk.</td>
<td>Deze wijziging geeft de gebruiker veel meer mogelijkheden bij gegevensopmaak, transformaties en biedt ook alle voordelen die afkomstig zijn van het levenscyclusbeheer van de configuratie van elektronische rapportage, zoals eenvoudige uitwisseling van configuraties, versiebeheer enz.</td>
</tr>
<tr>
<td>(FR) Rapport met saldilijst voor groepstotaalrekeningen.</td>
<td>Het rapport met de saldilijst voor groepstotaalrekeningen is geïmplementeerd als SSRS-rapport (LedgerAccountSum_FR).</td>
<td>Het rapport met de saldilijst voor groepstotaalrekeningen is geïmplementeerd als rapport in Management Reporter dat beschikbaar is in de map met gelokaliseerde financiële rapporten van de LCS-activabibliotheek.</td>
<td>Hierdoor krijgen gebruikers alle voordelen en vrijheid in aanpassingen geboden door het gebruik van financiële rapporten in Management Reporter.</td>
</tr>
<tr>
<td>(EU) Betalingsadvies, bijbehorende notitie en beheerrapporten voor betalingen.</td>
<td>Al deze rapporten zijn geïmplementeerd en SSRS-rapporten.</td>
<td>Deze rapporten zijn geïmplementeerd als OpenXML-sjablonen voor gebruik in Microsoft Excell.</td>
<td>Configuraties voor elektronische betaling bevatten instellingen en sjablonen voor betalingsbestandsindelingen. Hierdoor krijgen gebruikers alle voordelen en vrijheid in rapportaanpassingen geboden door het gebruik van Elektronische rapportage.</td>
</tr>
<tr>
<td>(EU) Afrondingsinstellingen configureren voor Intrastat.</td>
<td>Afrondingsinstellingen voor de Intrastat-verkooplijstrapportage voor verschillende landen/regio's zijn hard gecodeerd in X++ of in Extensible Stylesheet Language Transformations (XSLT's).</td>
<td>Afrondingsinstellingen worden toegevoegd aan parameters voor buitenlandse handel. Kunt u afrondingsprecisie, afrondingsmethode, uitvoerprecisie en gedrag voor bedragen die kleiner zijn dan de afrondingsprecisie configureren.</td>
<td>Hiermee wordt de configuratie van de Intrastat-rapportage gelijkgeschakeld en vereenvoudigd. Aanpassing van afrondingsinstellingen vereist niet langer ontwikkelingsinspanningen.</td>
</tr>
<tr>
<td>(EU) Insteling van Intrastat-basisproductcodes in categoriehiërarchieën.</td>
u<td>Intrastat-basisproductcodes vormen een aparte lijst. Hoewel er een categoriehiërarchie van het type Basisproductcode is, kunnen deze basisproductcodes als standaard worden gebruikt in Retail HQent en verkoopcategorieën.</td>
<td>Aparte lijst met Intrastat-basisproductcodes zijn samengevoegd met de producthiërarchie van het type Basisproductcode.</td>
<td>Dit verenigt de aanpak voor het toewijzen van basisproductcodes aan vrijgegeven producten en categorieën in verkoop- en inkoopdocumenten.</td>
</tr>
<tr>
<td>(EU) Rapportage van hoeveelheid in aanvullende eenheden voor Intrastat via het gebruik van de instelling voor eenheidsconversie.</td>
<td>Intrastat-basisproductcode heeft een tekstveld voor het identificeren van aanvullende eenheden en de kaart <strong>Product</strong> heeft een veld voor het identificeren van de hoeveelheid extra eenheden in kilogrammen.</td>
<td>Aanvullende eenheden voor Intrastat-basisproductcode worden gekozen uit de lijst met eenheden. Het aantal aanvullende eenheden wordt berekend via instellingen voor eenheidsconversie.</td>
<td>Dit verenigt aanpak voor herberekening van transactie-eenheden naar extra eenheden.</td>
</tr>
<tr>
<td>(EU) Wijs standaardtransportmethode toe aan leveringsmethode.</td>
<td>Niet beschikbaar</td>
<td>Een veld voor de standaardtransportmethode is toegevoegd aan de leveringsmethode.</td>
<td>Dit vereenvoudigt de voorbereiding van de Intrastat-rapportage.</td>
</tr>
<tr>
<td>(EU) Geef aan dat vrijgegeven product niet moet worden gerapporteerd in Intrastat.</td>
<td>Niet beschikbaar</td>
<td>Een optie voor het uitsluiten van het artikel uit de Intrastat-rapportage wordt toegevoegd aan het vrijgegeven product.</td>
<td>Dit vereenvoudigt de voorbereiding van de Intrastat-rapportage.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Productie

| Wat kunt u doen? | Dynamics AX 2012 |
|------------------|------------------|
| Voer een controle van de materiaalbeschikbaarheid uit voor productieorders op een aparte pagina, die wordt geopend vanuit de werkruimte **Productievloerbeheer**. | Niet beschikbaar |
| Voortgang starten en rapporteren voor productietaken met de nieuwe pagina **Taakkaartapparaat**. | Het formulier **Taakregistratie** is voornamelijk bedoeld voor grote terminalschermen, en de UI wordt meestal bediend via muiskliks. |

## <a name="master-planning-and-forecasting"></a>Hoofdplanning en prognoses

| Wat kunt u doen? | Dynamics AX 2012 | Dynamics AX 7.0 | Waarom is dit belangrijk? |
|------------------|------------------|-----------------|------------------------|
| Waarschuw de gebruiker als een verkooporder of productieorder niet op de geplande datum gereed is voor levering. | De waarschuwingen die worden gemaakt door de hoofdplanning worden *vertragingsberichten* (futures messages) genoemd. Een *Futures* is een contract tussen twee partijen om een activum te kopen of te verkopen voor een prijs die vandaag is vastgesteld (de *futuresprijs*), maar waarvoor levering en betaling op een toekomstig tijdstip plaatsvinden (de *leveringsdatum*). | *Vertragingsberichten* en *Vertragingsdatums* worden nu respectievelijk *berekende vertragingen* en *vertragingsdatums* genoemd. | De terminologie die in AX 2012 werd gebruikt, is onnauwkeurig en leidde tot onjuiste vertalingen. |
| Krijg snel inzicht in de status van een hoofdplanning, urgente geplande orders en geplande orders die vertragingen opleveren. | De informatie is beschikbaar, maar is verspreid over meerdere formulieren. | De werkruimte **Hoofdplanning** biedt in één oogopslag informatie over wanneer de laatste hoofdplanning is voltooid, of er fouten zijn opgetreden, welke urgent geplande orders er zijn en welke geplande orders vertragingen opleveren. | U profiteert van het overzicht dat de werkruimte biedt. Relevante informatie wordt samengebracht om de hoofdplanning te leiden en productiviteit te vergroten. |
| Vraagprognoses bijwerken met Excel. | Niet beschikbaar | U kunt profiteren van naadloze integratie met Excel wanneer u vraagprognoses invoert, updates uitvoert en vraagprognoses verwijdert. | Dit helpt efficiëntie en de productiviteit te verhogen. |
| Raam de toekomstige vraag en stel vraagprognoses op, aan de hand van historische transactiegegevens. | In Microsoft Dynamics AX 2012 R3 worden de prognosemodellen in Microsoft SQL Server Analysis Service gebruikt voor het maken van de vraagprognosevoorspellingen. | Raam de toekomstige vraag dankzij de kracht en uitbreidbaarheid van een Microsoft Azure-cloudservice voor Machine Learning. Het is gemakkelijk in het gebruik en breidt de prognosemodellen in Machine Learning uit om te voldoen aan de behoeften van klanten. De service voert modelselectie op basis van best match uit en biedt Key Performance Indicators (KPI's) die kunnen worden gebruikt om de prognosenauwkeurigheid te berekenen. | Genereer nauwkeurigere prognoses met de Machine Learning-technieken. |
| De orderdatum en -hoeveelheid optimaliseren, op basis van een visueel overzicht van verwante acties uit de uitvoering van de hoofdplanning. | De grafiek voor overzicht van acties is beschikbaar maar geeft alle verwante acties weer. Wanneer de acties worden toegepast, verdwijnen ze onmiddellijk uit de weergave. | De actiegrafiek bevat een beter overzicht. Het bevat opties waarmee u alleen toegepaste acties en direct verwante acties kunt weergeven. Wanneer de acties worden toegepast, worden ze lichter gekleurd maar nog steeds weergegeven. Daarmee behoudt u het overzicht. Aanvullende informatie wordt toegevoegd aan de actiegrafiek om de gegevens op één pagina weer te geven. | U ondervindt productiviteitsverbetering, omdat u zich alleen op de relevante acties hoeft te richten. |

## <a name="procurement-and-sourcing"></a>Inkoopbeheer

| Wat kunt u doen? | Dynamics AX 2012 | Dynamics AX 7.0 | Waarom is dit belangrijk? |
|------------------|------------------|-----------------|------------------------|
| Gebruik de werkruimte **Voorbereiding van inkooporder** om snel inzicht te krijgen in de status van inkooporders die worden voorbereid. | Niet ondersteund | De werkruimte **Voorbereiding van inkooporder** biedt een overzicht van orders vanaf de tijd dat ze als concept worden gemaakt en getraceerd, door de statussen van de workflowgoedkeuring tot het moment van bevestiging. | Uw inkoopafdeling hoeft niet meer gegevens van meerdere pagina's op te vragen, maar profiteert nu van het overzicht dat de werkruimte biedt. |
| Gebruik de werkruimte **Ontvangst en opvolging van inkooporders** om snel inzicht te krijgen in inkooporders die in afwachting van ontvangst zijn, om te helpen met het opvolgen. | Niet ondersteund | De werkruimte **Ontvangst en opvolging van inkooporders** geeft een overzicht van bevestigde inkooporders die in afwachting zijn van ontvangsten of verzendingen. De werkruimte bevat lijsten met uitstaande of in behandeling zijnde ontvangsten, die helpen bij pro-actieve controle opvolging door de leverancier. De werkruimte bevat ook lijsten met inkooporders waarvoor de aankomstregistratie in het magazijn is gebeurd, wat helpt waarborgen dat de ontvangst is geboekt. Retouren voor inkooporders die nog niet zijn verzonden, zijn ook beschikbaar voor controle. | Uw inkoopafdeling profiteert van het overzicht dat de werkruimte biedt. Relevante informatie wordt samengebracht om opvolging te leiden en productiviteit te vergroten. |
| Verzend inkooporders ter bevestiging naar een leveranciersportal die wordt uitgevoerd in de Dynamics AX-client. De leverancier deze laten bevestigen of afwijzen. | Niet ondersteund | De leveranciersportalinterface laat leveranciers inkooporders ontvangen voor bevestiging of afwijzing. Het biedt ook de leverancier een overzicht van alle bevestigde inkooporders voor een account. De inkoper kan een inkooporder verzenden en bevestiging van de leverancier verzoeken. De leverancier moet een geregistreerde Microsoft Azure Active Directory (Azure AD)-gebruiker in Dynamics AX zijn, een contactpersoon voor de leverancier en een specifieke beveiligingsrol hebben. | Uw inkoopafdeling profiteert van minder papierwerk het handmatig volgen van antwoorden op inkooporders, aangezien deze rechtstreeks het systeem in worden gestuurd. Dankzij één bron voor de feiten kunnen minder misverstanden ontstaan tussen klant en leverancier. |

## <a name="projects"></a>Projecten

| Wat kunt u doen? | Dynamics AX 2012 | Dynamics AX 7.0 | Waarom is dit belangrijk? |
|------------------|------------------|-----------------|------------------------|
| Werknemers boeken als resources voor projecten. | Net zoals hulpbronnen worden werknemers direct geboekt op projecten naast de hulpbronnen. | De tabel Werkplaats, waarin bronnen voor fabricage en productie worden opgeslagen, kan nu worden gebruikt om werknemers te boeken als resources op een project. | Wanneer u projecten boekt, hoeft u alleen bronnen te boeken. |

## <a name="retail-sales-marketing-and-customer-service"></a>Detailhandelverkoop, marketing en klantenservice

### <a name="retail-hq"></a>Retail HQ

Microsoft Azure gehoste Retail HQ biedt gecentraliseerd beheer van en volledige zichtbaarheid in alle aspecten van commerciële handelingen door middel van een webclient.

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Merchandising-activiteiten uitvoeren.</td>
<td>Gebruikers moeten meerdere formulieren openen om deze gegevens te beheren:
<ul>
<li>Categoriebeheer</li>
<li>Productbeheer</li>
<li>Afzetkanaalproductkenmerken</li>
<li>Assortimenten</li>
<li>Catalogusbeheer</li>
<li>Kits</li>
<li>Prijzen &amp; kortingen</li>
</ul></td>
<td>De werkruimte <strong>Categorie- en productbeheer</strong> maakt de volgende functionaliteit mogelijk:
<ul>
<li>Assortimentsbeheer.</li>
<li>Levenscyclustracering van het assortiment.</li>
<li>Beheer van vrijgegeven producten.</li>
</ul>
De werkruimte <strong>Beheer van prijzen en kortingen</strong> maakt de volgende functionaliteit mogelijk:
<ul>
<li>Prijs- en kortingbeheer voor een bepaald kanaal en een bepaalde categorie.</li>
<li>Beheer van categorieprijsregels.</li>
<li>Prijs- en kortingprioriteiten, waarmee u prioriteiten kunt toewijzen aan prijsgroepen en kortingen, zodat u de volgorde kunt controleren waarin ze worden toegepast.</li>
<li>Beheer van aansluiting en cataloguskorting.</li>
</ul>
De werkruimte <strong>Catalogusbeheer</strong> maakt de volgende functionaliteit mogelijk:
<ul>
<li>Overzicht van actieve catalogi.</li>
<li>Cataloguslevenscyclus bijhouden in één locatie.</li>
</ul></td>
<td><ul>
<li>Werkruimten verbeteren de efficiëntie en productiviteit van werknemers, door deze centraal de taken en acties te laten beheren die zijn gekoppeld aan de merchandisingrol.</li>
<li>De functie prijs- en kortingsprioriteit geeft klanten meer controle over hoe prijzen en kortingen worden gebruikt. De functie maakt ook nieuwe scenario's mogelijk waarin de hogere winkelprijzen standaardprijzen overhalen.</li>
</ul></td>
</tr>
<tr>
<td>Implementatie van en activiteiten in detailhandelkanalen beheren.</td>
<td>De gebruiker moet meerdere formulieren openen om de volgende taken uit te voeren:
<ul>
<li>Nieuwe kanalen en gerelateerde entiteiten maken en configureren.</li>
<li>Dagelijkse winkelactiviteiten beheren.</li>
<li>Detailhandelstransacties verwerken in Microsoft Dynamics AX, overzichten van detailhandel genereren en bijwerken van Microsoft Dynamics AX-voorraad en financiële gegevens.</li>
</ul>
</td>
<td>In de werkruimte <strong>Afzetkanaalimplementatie</strong> kunt u de volgende taken uitvoeren:
<ul>
<li>Nieuwe kanalen en gerelateerde entiteiten maken.</li>
<li>De voortgang van detailhandelconfiguraties volgen.</li>
<li>De vereiste stappen uitvoeren om een taak te voltooien, of informatie te leveren om de taak te voltooien.</li>
<li>De status weergeven van apparaten, en rechtstreeks de installatie van Retail Modern POS (MPOS) in winkels valideren en downloaden.</li>
<li>Alle gerelateerde pagina's openen.</li>
</ul>
<strong>In de werkruimte Beheer van detailhandelwinkel</strong> kunt u de volgende taken uitvoeren:
<ul>
<li>Werknemers en de machtigingen voor het verkooppunt (POS) van de werknemers beheren.</li>
<li>De werktijdstatus voor een bepaalde winkel of groep van winkels volgen.</li>
<li>Rechtstreeks de programma-installatie van MPOS in winkels valideren en downloaden.</li>
<li>Rapporten afdrukken en gerelateerde pagina's openen.</li>
</ul>
<strong>In de werkruimte Financiën van detailhandelwinkel</strong> kunt u de volgende taken uitvoeren:
<ul>
<li>Overzichten maken, berekenen en boeken voor een specifiek kanaal.</li>
<li>Batchtaken plannen om voorraad bij te werken en overzichten te berekenen en te boeken.</li>
<li>Openstaande overzichten volgen.</li>
<li>De werktijdstatus voor een bepaalde winkel of groep van winkels volgen.</li>
<li>Rapporten afdrukken en snel alle gerelateerde pagina's openen.</li>
</ul></td>
<td>Werkruimten verbeteren de efficiëntie en productiviteit van werknemers, door deze centraal de taken en acties te laten beheren die zijn gekoppeld aan kanaalimplementatie, winkelbeheer en financiële gegevens.</td>
</tr>
<tr>
<td>IT-activiteiten voor detailhandel beheren.</td>
<td>De gebruiker moet meerdere formulieren openen.</td>
<td>De werkruimte <strong>IT detailhandel</strong> maakt query's voor Commerce Data Exchange mogelijk in één plaats voor een bepaald kanaal, zodat u de volgende taken kunt uitvoeren:
<ul>
<li>Sessies downloaden</li>
<li>Sessies uploaden</li>
<li>Mislukte sessies volgen en deze opnieuw initiëren of uitvoeren</li>
<li>Komende taken weergeven of uitvoeren</li>
</ul></td>
<td>Werkruimten verbeteren de efficiëntie en productiviteit van werknemers, door deze centraal de taken en acties te laten beheren die zijn gekoppeld aan activiteiten voor detailhandel-IT.</td>
</tr>
<tr>
<td>Importeer/exporteer gegevens door gegevensentiteiten te gebruiken.</td>
<td>AX 2012 ondersteunt standaard de migratie van het Microsoft Dynamics Retail Management System (RMS) door het raamwerk voor gegevensimport/-export.</td>
<td>De gegevensentiteiten voor de detailhandel zijn uitgebreid en ondersteunen alle hoofdgegevens en referentiegegevens die verband houden met de detailhandel. Er is ook verbeterde ondersteuning voor gegevensentiteiten in de gehele Dynamics AX-oplossing.</td>
<td>Gegevensentiteiten stellen klanten in staat gegevens te importeren en te exporteren op basis van metagegevens. OData-entiteiten laten klanten ook met Dynamics AX integreren met software van derden.</td>
</tr>
<tr>
<td>Intelligente analyse uitvoeren door gebruik van BI-rapporten van Dynamics Microsoft AX en de POS-client.</td>
<td>Meer dan 25 backofficerapporten en vijf kanaalrapporten zijn beschikbaar.</td>
<td>Meer dan 30 backofficerapporten en tien kanaalrapporten zijn beschikbaar.</td>
<td>Met deze rapporten kunnen klanten beschikken over meer BI om trends te voorspellen, inzichten te genereren en continu met maximale prestaties te werken.</td>
</tr>
<tr>
<td>Verkoopgegevens van detailhandelkanalen analyseren door middel van het Power BI-inhoudpakket Monitor Retail Channel Performance.</td>
<td>Niet beschikbaar</td>
<td>Selecteer op PowerBI.com <strong>Get Data</strong> en selecteer vervolgens het inhoudpakket <strong>Dynamics AX - Retail Channel performance</strong>. Voer de URL voor uw Dynamics AX-eindpunt in om uw gegevens in het dashboard te bekijken.</td>
<td>Met drie tot vier muisklikken kunnen organisaties een Power BI-dashboard met belangrijke financiële gegevens uitrollen. De inhoud kan door de organisatie worden gepersonaliseerd. Daarnaast kunnen gebruikers dashboardtegels van Power BI in hun gepersonaliseerde werkruimten in Dynamics AX integreren, zodat zij analytische informatie in een oogopslag kunnen overzien.</td>
</tr>
<tr>
<td>Consumentenmachtigingen configureren.</td>
<td>Niet beschikbaar</td>
<td>Klanten kunnen kiezen of POS-activiteiten beschikbaar zijn voor klanten. Retail Server gebruikt machtigingen voor API-aanroepen (Application Programming Interface).</td>
<td>Dit biedt de mogelijkheid om machtigingen op consumentenniveau te configureren.</td>
</tr>
<tr>
<td>Entiteitconfiguraties beheren en valideren.</td>
<td>Niet beschikbaar</td>
<td>De functie configuratiebeheer en -validatie en biedt de volgende functionaliteit:
<ul>
<li>Configuratiegegevens in bulk uploaden</li>
<li>Bedrijfsentiteit valideren</li>
</ul></td>
<td>Het biedt de mogelijkheid om de configuratie automatisch te laden en de status en de mate van compleetheid van de configuratie voor de verschillende configuratie-elementen te valideren.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Retail-hardwarestation

| Wat kunt u doen? | Dynamics AX 2012 | Dynamics AX 7.0 | Waarom is dit belangrijk? |
|------------------|------------------|-----------------|------------------------|
| POS-apparaten verbinding laten maken met randapparaten zoals printers, kassa-laden of betalingapparaten. | Het MPOS-hardwareprofiel wordt gebruikt om de apparaten te specificeren die worden gebruikt. | Een toegevoegd hardwareprofiel ondersteunt meer verschillende hardware op de verschillende stations. Een nieuw hardwarestationprofiel ondersteunt een unieke terminal-ID voor elk hardwarestation wanneer elektronische betalingstransacties (EFT) worden verwerkt. EFT-ondersteuning is geïntegreerd in het hardwarestation om de betrokkenheid van MPOS bij verwerking van EFT-betalingen te verminderen. | Dit biedt meer flexibiliteit voor implementaties. Het biedt ook verbeterde beveiliging en verminderde blootstelling aan creditcardgegevens. |

### <a name="retail-server-and-data-management"></a>Retail Server en gegevensbeheer

Met Retail Server en gegevensbeheer kunt klanten en bedrijven een shoppingervaring creëren over meerdere kanalen zoals online, in-store en de callcenters.

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Verbinding maken met een van commerce runtime-database (CRT), die zakelijke gegevens voor het kanaal opslaat door CRT-services te gebruiken.</td>
<td>OData V3 wordt ondersteund.</td>
<td>OData V4 wordt ondersteund.</td>
<td>Dit helpt de klant om up-to-date te blijven met OData-normen. Het creëert ook een ervaring over meerdere afzetkanalen door integratie van verkoop in de kanalen in winkels en op mobiele apparatuur en online.</td>
</tr>
<tr>
<td>Detailhandelservices ondersteunen als een set van diensten die gehost kan worden.</td>
<td>De E-commerce-API wordt niet ondersteund via Retail Server.</td>
<td>De E-commerce-API nu is beschikbaar via Retail Server om online scenario's te ondersteunen.</td>
<td>Het biedt gehoste en schaalbare e-commerceservices aan, die kunnen worden gebruikt met externe online winkels.</td>
</tr>
<tr>
<td>Verplaatsen van gegevens tussen de Microsoft Dynamics AX-back-office en -kanalen met Commerce Data Exchange.</td>
<td>Commerce Data Exchange is een systeem dat de gegevensoverdracht tussen Microsoft Dynamics AX en detailhandelkanalen, zoals onlinewinkels of fysieke winkels. Zie <a href="https://technet.microsoft.com/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a> voor meer informatie.</td>
<td>Er is functionele pariteit met Microsoft Dynamics AX 2012 CU8. Houd echter rekening met het volgende:
<ul>
<li>Commerce Data Exchange is opnieuw ontworpen voor de cloud.</li>
<li>De Async-service maakt gebruik van rechtstreekse databasetoegang tot de database van het afzetkanaal.</li>
<li>Commerce Data Exchange: Real-time Service wordt gehost als een Microsoft Dynamics AX aangepaste service.</li>
<li>MPOS beheert synchronisatie tussen offlinedatabases en Retail Server.</li>
</ul></td>
<td>Commerce Data Exchange is opnieuw ontworpen voor het cloudplatform. Het beheert nog steeds het overzetten van gegevens tussen Microsoft Dynamics AX en afzetkanalen voor detailhandel, zoals online winkels of fysieke winkels.</td>
</tr>
<tr>
<td>Verwerking van semi-geïntegreerde plug en play-betalingen tussen afzetkanalen ondersteunen door de betaling-SDK te gebruiken.</td>
<td>AX 2012 biedt de volgende functionaliteit:
<ul>
<li>Ondersteuning voor alle kanalen: POS, e-commerce en callcenter.</li>
<li>Ondersteuning voor transacties met of zonder kaart (´card present´ of ´card not present´).</li>
<li>Pagina voor het accepteren van betalingen.</li>
<li>Randapparatuurondersteuning voor LS5300 EN MX925 als voorbeeldcode in de Retail SDK.</li>
</ul></td>
<td>De huidige versie van Dynamics AX ondersteunt alle bestaande functies uit Microsoft Dynamics AX Retail 2012 voor creditcards/betaalpassen en vier nieuwe verbeteringen.</td>
<td>Hiermee kan de klant betaaltransacties met creditcards of betaalpassen verwerken.</td>
</tr>
<tr>
<td>Apparaten activeren met behulp van een Microsoft-account (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Niet beschikbaar</td>
<td>De volgende functionaliteit is beschikbaar:
<ul>
<li>Verbeterde beveiliging door Azure AD-gebaseerde activering voor de cloud.</li>
<li>Verbeterde beveiliging voor tokenbeheer.</li>
<li>Betere betrouwbaarheid, probleemoplossing en verzending van foutberichten tijdens de activering</li>
<li>Vereenvoudigde IT-beheertaken die verband houden met activering.</li>
<li>Risicomodel herzien en beveiligingsrisico's opgelost.</li>
</ul></td>
<td>Het biedt de volgende voordelen:
<ul>
<li>De beveiliging is verbeterd met Azure AD en apparaattoken/ID (RS-aanroepen die een token, gebruiker-specifieke appopslag gebruiken).</li>
<li>Het stopt onbevoegd extern gebruik van MPOS (fysiek apparaat).</li>
<li>Het volgt MPOS-apparaten voor PCI-conformiteitsdoeleinden.</li>
<li>Het wijst fysieke apparaten toe aan een bedrijfsentiteit (registreren) door een apparaattoken te gebruiken.</li>
<li>Het initialiseert instellingen voor soepele MPOS-functionaliteit (nummerreeksen en hardwareprofielen) als eerste contactpunt van MPOS.</li>
<li>Het rapporteert apparaatinformatie vanaf het hoofdkantoor.</li>
</ul></td>
</tr>
<tr>
<td>Rijke mediainhoud beheren voor creatie en indienen met Media Gallery.</td>
<td>Niet beschikbaar</td>
<td><ul>
<li>Ondersteun het uploaden, weergeven, beheren en verwijderen van afbeeldingen in Media Gallery voor zowel extern gehoste als ook Retail-gehoste afbeeldingen.</li>
<li>Ondersteun het uploaden en weergeven van afbeelding vanaf entiteitpagina's (,<strong>Producten</strong>, <strong>Catalogi</strong> enzovoorts) door een afbeelding in de galerie te koppelen en een afbeelding vanaf het bureaublad te uploaden.</li>
<li>Afbeeldingen optimaliseren voor miniaturen, aangepaste grootte, en originele grootte.</li>
<li>Entiteiten in bulk koppelen door een sjabloon en achtergrondtaken voor bulkkoppeling te gebruiken.</li>
<li>Microsoft Excel-integratie overschrijft de beperking van de kenmerkgroep voor naamgevingsconventies en voorgedefinieerde paden.</li>
<li>Offline afbeeldingen ondersteunen en afbeeldingen beveiligen voor persoonsgegevensinhoud, zoals afbeeldingen van werknemers en klanten die op Retail worden gehost.</li>
</ul></td>
<td><ul>
<li>Dit is een oplossing voor problemen rondom extern gehoste afbeeldingen, zodat u niet steeds heen en weer hoeft te gaan maar deze in één locatie kunt beheren.</li>
<li>Het biedt krachtig inhoudsbeheer via Media Gallery voor geüploade en extern gehoste afbeeldingen, en biedt ook een filterfunctie om u te helpen afbeeldingen te zoeken.</li>
<li>Het laat u eenvoudig bulkkoppelingen aanmaken tussen extern gehoste afbeeldingen en entiteiten, zoals producten en catalogi.</li>
<li>Het ondersteunt Retail-gehoste opslag voor afbeeldingen en Excel-integratie voor eenvoudig updaten.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Rijke ervaring voor klanten

Retail biedt meeslepende mobiele ervaringen overal, altijd en op elk apparaat. Deze functionaliteit maakt betere shopping- en winkelervaringen mogelijk in alle afzetkanalen.

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Producten zoeken, browsen, opzoeken of scannen producten, producten toevoegen aan een winkelwagen, betaling accepteren en uitchecken door een intuïtieve, aanraking-vriendelijke, rijke en meeslepende gebruikerservaring op MPOS te gebruiken.</td>
<td>AX 2012 biedt de volgende functies:
<ul>
<li>Verkopen, retouren en ongeldig maken van transacties uitvoeren.</li>
<li>Klantorders aanmaken, aanpassen en ophalen.</li>
<li>Activiteiten voor ploegen en lades uitvoeren.</li>
<li>Orders ophalen en ontvangen en voorraadtellingen uitvoeren.</li>
<li>In-store rapporten weergeven.</li>
</ul></td>
<td>Functionele pariteit met AX 2012 MPOS wordt geboden. Dit bevat de volgende functionaliteit:
<ul>
<li>Opzoeken van klanten in meerdere winkels/afzetkanalen.</li>
<li>De mogelijkheid om klantorders te maken zonder toegang tot Real-time Service.</li>
<li>Verbeterde werkstromen, statussen en foutberichten voor apparaatactivering.</li>
<li>Verbeteringen in uitbreidbaarheid, zoals pre-posttriggers en activiteitondersteuning voor betere aanpassingsmogelijkheden.</li>
</ul></td>
<td>Verkoopmedewerkers kunnen verkooptransacties en klantorders verwerken en dagelijkse activiteiten en voorraadbeheer uitvoeren door mobiele apparatuur overal in de winkel te gebruiken.</td>
</tr>
<tr>
<td>POS starten als een web-app via Cloud POS.</td>
<td>Niet beschikbaar</td>
<td>Functionele pariteit met MPOS wordt geboden. Dit bevat de volgende functionaliteit:
<ul>
<li>Apparaatactivering door AAD te gebruiken</li>
<li>Ontwerp met responsieve indeling</li>
<li>Ondersteuning voor de browsers Edge, Internet Explorer en Chrome.</li>
</ul></td>
<td>Het bevat een web-app POS die functionaliteit biedt die compatibel is met MPOS en zonder implementatiekosten kan worden gebruikt op verschillende platforms en browsers.</td>
</tr>
<tr>
<td>Integreren met contentmanagementsystemen om een website voor e-Commerce met meerdere kanalen te maken.</td>
<td>Microsoft SharePoint en winkels van externe partijen worden ondersteund.</td>
<td>Een platform voor e-Commerce wordt aangeboden dat winkels van derden ondersteunt. Het platform bevat de volgende functies:
<ul>
<li>Een uitgebreide consumenten-API.</li>
<li>Verificatie-integratie met alle externe providers van OpenID.</li>
<li>Betalingsintegratie.</li>
</ul></td>
<td>Klanten hebben nu de flexibiliteit om het contentmanagementsysteem van hun keuze te gebruiken.</td>
</tr>
<tr>
<td>Klanten aanspreken via postordercatalogi en activiteiten stroomlijnen door snelle orderinvoer, sales met assistentie en afhandeling door Call Center te gebruiken.</td>
<td><ul>
<li>Callcenterafzetkanaal</li>
<li>Postordercatalogi</li>
<li>Snelle orderinvoer en bijgestane verkoop</li>
<li>Verbeterde orderafhandeling</li>
<li>Klantenservice</li>
<li>Geïntegreerde prijsstelling en promoties/kortingen</li>
</ul></td>
<td>Functionele pariteit met de oplossing Call Center van AX 2012 wordt geboden, met uitzondering van prijsoverschrijvingen.</td>
<td>Callcenters zijn een type detailhandelafzetkanaal waarin werknemers orders van klanten over de telefoon kunnen aannemen en verkooporders maken.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Hoofdzaken van commerce

Een op detailhandel en commerce gerichte configuratieoptie helpt bij het stroomlijnen van retailspecifieke implementaties.

| Wat kunt u doen? | Dynamics AX 2012 | Dynamics AX 7.0 | Waarom is dit belangrijk? |
|------------------|------------------|-----------------|------------------------|
| Het dashboard Hoofdzaken van commerce gebruiken. | Een gebiedspagina met koppelingen naar menu-items is beschikbaar. | Het dashboard Hoofdzaken van commerce bevat koppelingen naar veelvoorkomende taken, inclusief koppelingen naar werkruimten, het webbesturingselement Power BI, favorieten, recente pagina's en actuele werkitems. | Het verbeterde dashboard laat werknemers beter werken, door hen efficiënter te maken en een flexibel beginpunt te bieden voor elke detailhandelspecifieke taak. |
| Gegevensentiteiten gebruiken voor toegang tot rekeningwijzigingen. | Rekeningwijzigingen worden geëxporteerd naar een map op het bestandssysteem. | Rekeningwijzigingen zijn toegankelijk via gegevensentiteiten. | Deze functie geeft meer flexibiliteit bij het verplaatsen van gegevens tussen verschillende systemen. Deze functie kan door OData-toepassingen worden uitgebreid. |
| Cloud-POS en MPOS gebruiken. | Alleen Enterprise POS (EPOS) wordt standaard na installatie ondersteund. | MPOS en Cloud-POS vervangen de EPOS-client. Het e-Commerce-afzetkanaal is standaard ook toegevoegd aan Hoofdzaken van commerce. | Deze functie maakt sterkere ondersteuning van het kant-en-klare kanaal mogelijk met snel implementeerbare POS-clients. |
| Implementeer en onderhoud een tweelagige architectuur. | Het raamwerk voor gegevensimport/-export biedt de mogelijkheid om gegevens tussen AX 2012 en systemen van derden te verplaatsen. | Gegevensentiteiten gemaakt om ondersteuning voor architectuur op twee lagen te verbeteren. | Gegevensentiteiten en OData-toepassingen bevatten een abstractielaag om scenario's op twee lagen eenvoudiger te kunnen uitvoeren en onderhouden. |
| Formulieren vereenvoudigen. | Aangepaste code is vereist om de UI te vereenvoudigen. | Uitbreidingen voor formulieren en menu's bieden gestandaardiseerde mogelijkheden voor vereenvoudiging van de UI. | Deze functie voorziet in een snellere en eenvoudiger manier om formulieren te verfijnen op basis van de vereisten van de detailhandelaar. |

### <a name="pos-task-recorder"></a>POS-taakregistratie

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Taakhandleidingen en documenten voor Modern POS maken en delen.</td>
<td>Niet beschikbaar</td>
<td>De MPOS-taakregistratie ondersteunt de volgende functies:
<ul>
<li>Taakregistraties maken voor verschillende taken die in MPOS worden uitgevoerd.</li>
<li>Genereer een document dat stappen en schermopnamen bevat, en deze koppelen aan een knooppunt in het bedrijfsprocesmodel.</li>
</ul></td>
<td>Partners en onafhankelijke softwareaanbieders (ISV's) kunnen MPOS aanpassen en ondersteuningsdocumentatie leveren om de gebruikers te trainen.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Uitbreidbaarheid

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ondersteun uitbreidbare en eenvoudig te implementeren Retail-onderdelen in HQ, Call Center, e-Commerce en POS.</td>
<td>De componenten kunnen worden uitgebreid door middel van de Retail-SDK. Capaciteiten voor verpakking en implementatie worden niet ondersteund.</td>
<td>Uitbreidings-hooks zijn verbeter in de verschillende componenten voor betere ondersteuning van isolatie en onderhoudsvriendelijkheid van de code. Enkele van de beschikbare functies zijn:
<ul>
<li>Workflow, activiteit en bewerking.</li>
<li>Pre-triggers en post-triggers waarmee u gemakkelijk een workflow kunt verlengen.</li>
<li>Triggers voor toepassingen en bewerkingen.</li>
</ul>
Daarnaast is een raamwerk beschikbaar waarmee u deze componenten kunt maken en verpakken door MSBuild te gebruiken, en uw aanpassing vervolgens naadloos kunt implementeren via Microsoft Dynamics Lifecycle Services (LCS).</td>
<td>Detailhandelaren hebben zeer specifieke vereisten die zijn gebaseerd op verticalen en geografieën van hun activiteiten. Door een eenvoudig een uitbreidbaar platform te bieden, maken we mogelijk om dit te gebruiken voor de verschillende verticalen en markten. Omdat Retail ook een zeer gedistribueerde architectuur heeft, vergroot de mogelijkheid om voor naadloze implementatie de productiviteit aanzienlijk.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Levenscyclusbeheer

Lifecycle Services (LCS) biedt een set van services die klanten en partners kunnen gebruiken om de levenscyclus van het systeem te beheren van aanmeding tot en met dagelijkse activiteiten.

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Het programma beheren via services voor cloudimplementatie.</td>
<td>Niet beschikbaar</td>
<td>De volgende topologieën kunnen naar de cloud worden geïmplementeerd:
<ul>
<li>Retail 1-doostopologie voor proeven.</li>
<li>Retail multi-box topologie voor hoge beschikbaarheid.</li>
<li>Ontwikkelaartopologie met de Retail-SDK.</li>
</ul>
Er is een betere 'low-touch' installatie van clientcomponenten via selfservice-installatie:
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Ondersteuning voor upload en distributie van aangepaste pakketten door selfservice-installatie.</li>
</ul></td>
<td>De services voor cloudimplementatie bieden de volgende voordelen:
<ul>
<li>Aanzienlijk minder implementatiearbeid en complexiteit voor Retail HQ-onderdelen.</li>
<li>Native implementatie naar de Microsoft Azure openbare cloud.</li>
<li>Betere selfservice-installatie van in-store onderdelen voor eenvoudiger en meer intuïtieve configuratie</li>
</ul></td>
</tr>
<tr>
<td>De status van het systeem controleren en fouten en problemen diagnostiseren.</td>
<td>Deze functionaliteit vereist <a href="https://www.microsoft.com/download/details.aspx?id=42636">System Center 2012 Management Pack voor Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Monitoring en diagnostiek voor Retail-componenten is nu beschikbaar via het dashboard <strong>Operationeel Inzicht</strong> in LCS.</td>
<td>Het dashboard <strong>Operationeel Inzicht</strong> is een op cloud gebaseerde monitoringportal, dat installatie van de System Center Operations Manager-infrastructuur (SCOM) overbodig maakt.</td>
</tr>
<tr>
<td>Retail Hardware Station en apparaten via selfservice maken, configureren, downloaden en installeren.</td>
<td>Door de installatieverpakkingstool en de Enterprise Portal te gebruiken, kunnen gebruikers een geautomatiseerde installatie en configuratie van alle onderdelen uitvoeren die op een specifieke computer worden vereist, op basis van een gedefinieerde topologie.</td>
<td>Omdat er slechts twee installatiepakketten zijn, een voor de MPOS-client en de andere voor de Retail Hardware Station-component, reduceert selfservice het werk dat op alle niveaus is vereist om deze clientcomponenten te installeren.</td>
<td>Selfservice is bedoeld om vereisten te minimaliseren en het gemakkelijker te maken voor een gebruiker om een installatie uit te voeren.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Verkoop

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Snel een overzicht krijgen van leveringsalternatieven wanneer u orders belooft aan klanten.</td>
<td>Wanneer er beperkingen van de productbeschikbaarheid zijn en de door de klant verzochte leveringsdatum voor een of meer producten op de order niet kan worden gehaald, wordt de taak voor levering van de order een uitdaging. Om alternatieven te vinden die problemen op het gebied van beschikbaarheid en leveringstijden kunnen compenseren, zodat u de leveringsdatum van de klant kunt halen, of om klanten een leveringsoplossing te bieden die zij kunnen accepteren en vertrouwen, moet de orderverwerker mogelijk meerdere formulieren openen, die elk slechts een subset van de vereiste informatie bevatten. Specifieker geeft een formulier de voorhanden hoeveelheden op verschillende locaties weer, terwijl een ander formulier voorhanden hoeveelheden in de intercompany-instellingen weergeeft, een derde formulier de gebruiker de vroegst beschikbare datum voor één locatie/variant laat berekenen en een vierde formulier de aanbodorders toont. Daarom voelen gebruikers zich niet zeker dat ze alle relevante opties hebben overwogen, maar in plaats daarvan simpelweg een onmiddellijke maar suboptimale oplossing hebben gekozen. Gebruikers voelen zich ook niet effectief, aangezien zich veel onderbrekingen voordoen tijdens de workflow voor orderbelofte bij het openen en sluiten van meerdere pagina's en het combineren van de inzichten en opties.</td>
<td>Op basis van de bestaande algoritmen voor berekening van de leveringsdatum, biedt de pagina <strong>Alternatieven voor levering </strong>een nieuwe gebruikerservaring voor orderbelofte:
<ul>
<li>Hier worden relevante gegevens van meerdere formulieren in één ruimte gecombineerd.</li>
<li>Het biedt kant-en-klare alternatieve leveringspakketten, zoals een combinatie van site/warehousing/variant/vervoerswijze, op basis van het criterium voor de snelste levering (eerste beschikbare datum) waaruit de gebruiker kan kiezen.</li>
<li>De gebruiker kan opties selecteren in de simulatie-interface en deze overbrengen naar de verkooporderregel.</li>
</ul></td>
<td>Bedrijven die streven naar uitstekende klantenservice en een strategie voor voorraadoptimalisatie willen realiseren, moeten in staat zijn om orders op betrouwbare en concurrerende wijze te beloven. De eigen bedrijven van hun klanten vereisen immers dat de producten op tijd beschikbaar zijn. De taakpagina <strong>Alternatieven voor levering</strong> maakt de taak voor orderbelofte sneller, eenvoudiger en meer systematisch door de beste alternatieve datums voor orderlevering te bepalen en aan te bevelen in één interactieve plaats.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Servicebeheer

Geen nieuwe functies zijn toegevoegd.

## <a name="transportation-management"></a>Transportbeheer

Geen nieuwe functies zijn toegevoegd.

## <a name="travel-and-expense"></a>Reis- en onkosten

Geen nieuwe functies zijn toegevoegd.

## <a name="warehouse-management"></a>Magazijnbeheer

| Wat kunt u doen? | Dynamics AX 2012 | Dynamics AX 7.0 | Waarom is dit belangrijk? |
|------------------|------------------|-----------------|------------------------|
| Download, installeer en configureer de Magazijn-portal voor mobiele apparaten. | U kunt de portal downloaden, installeren en configureren tijdens het installatieproces van Microsoft Dynamics AX, door een standaardsetup. Het is ontworpen voor zelfgestuurde implementatie en configuratie on-premises. | U kunt een zelfstandig installatieprogramma downloaden via een menu-item in Magazijnbeheer. Het is ontworpen voor zelfgestuurde implementatie en configuratie on-premises. | Wanneer u de functionaliteit voor gebruik van mobiele apparaten opzet, moet u de magazijnportal voor mobiele apparaten lokaal installeren en configureren en een verbinding opzetten met het Dynamics AX-programma in de cloud. |

## <a name="additional-resources"></a>Aanvullende bronnen

[Nieuwe of gewijzigde functies op de startpagina van Finance and Operations](whats-new-changed.md)

[Nieuwe taakbegeleidingen (februari 2016)](new-task-guides-available-february-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
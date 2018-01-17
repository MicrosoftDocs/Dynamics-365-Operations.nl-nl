---
title: Overzicht kwaliteitsbeheer
description: In dit onderwerp wordt beschreven hoe u kwaliteitsbeheer in Microsoft Dynamics 365 for Finance and Operations kunt gebruiken om de productkwaliteit in uw keten van toeleveranciers te verbeteren.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8961d1c62167192fcf32d17c2941b8813ea0629
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="quality-management-overview"></a>Overzicht kwaliteitsbeheer

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u kwaliteitsbeheer in Microsoft Dynamics 365 for Finance and Operations kunt gebruiken om de productkwaliteit in uw keten van toeleveranciers te verbeteren.

Kwaliteitsbeheer kan u helpen keerpunttijden te beheren wanneer u te maken hebt met niet-overeenkomende producten, ongeacht hun punt van oorsprong. Omdat typen diagnoses aan correctierapportage zijn gekoppeld, kan Microsoft Dynamics 365 for Finance and Operations taken plannen om problemen te corrigeren en te voorkomen dat deze worden herhaald.

Naast functionaliteit voor het beheer van non-conformiteit omvat het kwaliteitsbeheer functionaliteit voor het bijhouden van problemen op probleemtype (ook interne problemen) en om oplossingen als kortetermijn- of langetermijnoplossingen te identificeren. De statistieken over Key Performance Indicators (KPI´s) bieden inzicht in de geschiedenis van eerdere niet-conformeringsproblemen en de oplossingen die zijn gebruikt om ze te corrigeren. U kunt de historische gegevens gebruiken om de efficiëntie van eerdere kwaliteitsmetingen te controleren en passende stappen voor de toekomst te definiëren.

Wanneer u een kwaliteitskoppeling opzet, kan Finance and Operations kwaliteitsorders genereren voor verschillende bedrijfsprocessen, gebeurtenissen en voorwaarden. De kwaliteitskoppeling kan betrekking hebben op een specifiek artikel, een specifieke groep artikelen of alle artikelen.

## <a name="examples-of-the-use-of-quality-management"></a>Voorbeelden van het gebruik van kwaliteitsbeheer
Kwaliteitsbeheer is flexibel en kan op verschillende manieren worden geïmplementeerd om aan de vereisten van specifieke niveaus van toeleveringsactiviteiten te voldoen. In de volgende voorbeelden worden mogelijke toepassingen van deze functies beschreven:

-   Start automatisch een kwaliteitscontroleproces, op basis van vooraf gedefinieerde criteria (bij magazijnregistratie van een inkooporder van een specifieke leverancier).
-   Blokkeer voorraad tijdens inspectie om te voorkomen dat niet-goedgekeurde voorraad wordt gebruikt (volledig blokkeren van inkooporderhoeveelheden).
-   Gebruik artikelbemonstering als onderdeel van een kwaliteitskoppeling om te definiëren hoeveel fysieke actuele voorraad moet worden geïnspecteerd. Bemonstering kan betrekking hebben op een vaste hoeveelheid of een percentage.
-   Maak kwaliteitsorders voor gedeeltelijke ontvangsten. Als u een kwaliteitsorder wilt maken die is gebaseerd op de hoeveelheid die fysiek is ontvangen met een order, moet u het selectievakje **Per bijgewerkte hoeveelheid** op het formulier **Artikelbemonstering** inschakelen.
-   Maak testtypen die minimum-, maximum- en doeltestwaarden bevatten en voer vergelijkende kwalitatieve en kwantitatieve testen met vooraf gedefinieerde validatieresultaten uit.
-   Geef een acceptabel kwaliteitsniveau op om kwaliteitsmetingstoleranties te beheren.
-   Geef op welke resources een inspectiebewerking nodig hebben, zoals een testgebied en testinstrumenten.

## <a name="working-with-quality-associations"></a>Werken met kwaliteitskoppelingen
Bedrijfsprocessen die gebruikmaken van een kwaliteitskoppeling, kunnen betrekking hebben op verschillende brondocumenten, zoals inkooporders, verkooporders of productieorders.

Elk kwaliteitskoppelingsrecord definieert de set met testen, het aanvaardbare kwaliteitsniveau en het bemonsteringsplan dat van toepassing is op de gegenereerde kwaliteitsorders. U moet een kwaliteitskoppelingsrecord definiëren voor elke variatie in een bedrijfsproces. U kunt bijvoorbeeld een kwaliteitskoppeling opzetten die een kwaliteitsorder genereert wanneer een productontvangstbon voor een inkooporder wordt bijgewerkt. Afhankelijk van de instelling van het uitvoeringsplan, kan het activerende proces zelf worden geblokkeerd terwijl er een kwaliteitsorder geopend is of kunnen volgende processen, zoals de facturering van inkooporders, worden geblokkeerd.

**Opmerking:** wanneer er kwaliteitsorders open staan, wordt de uitgave van voorraadhoeveelheden die zijn opgegeven in kwaliteitsorder automatisch geblokkeerd. Afhankelijk van de instelling **Volledig blokkeren** op de pagina **Artikelbemonsteringen**, is de hoeveelheid de hoeveelheid op de kwaliteit op de brondocumentregel.

De kwaliteitskoppeling identificeert voor een opgegeven bedrijfsproces de gebeurtenis en de omstandigheden waarin een kwaliteitsorder wordt gegenereerd. De voorwaarden kunnen specifiek voor een site of een rechtspersoon zijn. Een kwaliteitsorder waarvoor destructieve testen worden uitgevoerd, kan alleen worden gegenereerd als er voorraad voor de gebeurtenis voorhanden is.

In de volgende voorbeelden ziet u hoe een kwaliteitskoppelingsrecord wordt gedefinieerd voor de verschillen in elk bedrijfsproces. Voor elk voorbeeld worden in de volgende tabel de gebeurtenissen en voorwaarden samengevat die door een kwaliteitskoppelingsrecord zijn gedefinieerd.

<table>
<tbody>
<tr>
<th>Verwijzingstype</th>
<th>Gebeurtenistype</th>
<th>Uitvoering</th>
<th>Gebeurtenisblokkering</th>
<th>Documentverwijzing</th>
</tr>
<tr>
<td>Voorraad</td>
<td>Niet van toepassing</td>
<td>Niet van toepassing</td>
<td>Geen</td>
<td>Alle</td>
</tr>
<tr>
<td rowspan="7">Verkoop</td>
<td rowspan="4">Verzamelproces is gepland</td>
<td rowspan="4">Vóór</td>
<td>Geen</td>
<td rowspan="22">Specifieke id, Groep of alleen Alle</td>
</tr>
<tr>
<td>Verzamelproces</td>
</tr>
<tr>
<td>Pakbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="3">Pakbon</td>
<td rowspan="3">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Pakbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="15">Inkoop</td>
<td rowspan="7">Ontvangstlijst</td>
<td rowspan="4">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Ontvangstlijst</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="3">Na</td>
<td>Geen</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="3">Registratie</td>
<td rowspan="3">Niet van toepassing</td>
<td>Geen</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="5">Productontvangstbon</td>
<td rowspan="3">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="2">Na</td>
<td>Geen</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="8">Productie</td>
<td rowspan="3">Registratie</td>
<td rowspan="3">Niet van toepassing</td>
<td>Geen</td>
<td rowspan="12">Alle</td>
</tr>
<tr>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="5">Rapporteren als gereed</td>
<td rowspan="3">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="2">Na</td>
<td>Geen</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="4">Quarantaine</td>
<td rowspan="3">Rapporteren als gereed</td>
<td rowspan="2">Vóór</td>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td>Na</td>
<td>Beëindigen</td>
</tr>
<tr>
<td>Beëindigen</td>
<td>Vóór</td>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="3">Routebewerking</td>
<td rowspan="3">Rapporteren als gereed</td>
<td rowspan="2">Vóór</td>
<td>Geen</td>
<td rowspan="3">Specifieke id, Groep of Alle, en Resourcespecifiek, Groep of Alle</td>
</tr>
<tr>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Na</td>
<td>Geen</td>
</tr>
<tr>
<td rowspan="3">Productie van coproducten</td>
<td>Registratie</td>
<td>Niet van toepassing</td>
<td rowspan="3">Geen</td>
<td rowspan="3">Alle</td>
</tr>
<tr>
<td rowspan="2">Rapporteren als gereed</td>
<td>Vóór</td>
</tr>
<tr>
<td>Na</td>
</tr>
</tbody>
</table>

De volgende tabel bevat meer informatie over de manier waarop kwaliteitsorders kunnen worden gegenereerd voor specifieke typen processen.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Procestypen</th>
<th>Wanneer automatisch kwaliteitsorders kunnen worden gegenereerd</th>
<th>Wanneer kwaliteitsorders kunnen worden gegenereerd als destructieve testen vereist zijn</th>
<th>Informatie over voorwaarden</th>
<th>Handmatig informatie genereren</th>
</tr>
<tr>
<td>Inkooporder</td>
<td>Vóór of nadat een ontvangstlijst of productontvangstbon voor het ontvangen materiaal wordt geboekt</td>
<td>Nadat de productontvangstbon voor het ontvangen materiaal is geboekt, aangezien het materiaal beschikbaar dient te zijn voor destructieve testen</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een inkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Quarantaineorder</td>
<td>Vóór of nadat de quarantaineorder is gerapporteerd als voltooid of beëindigd</td>
<td>Kwaliteitsorders waarvoor destructieve testen vereist zijn, kunnen niet worden gegenereerd. Er wordt verondersteld dat de functie voor quarantaineorders de rangschikking verwerkt van het materiaal dat wordt vernietigd.</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een quarantaineorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Verkooporder</td>
<td>Vóór een gepland orderverzamelproces of pakbonupdate voor de artikelen die worden verzonden</td>
<td>Bij elke stap</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde klant of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een verkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Productieorder</td>
<td>Vóór of nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</td>
<td>Nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een productieorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Productieorder met een routebewerking</td>
<td>Voor of nadat het rapport voor een bewerking wordt voltooid</td>
<td>Nadat de rapportageproductie voor de laatste bewerking wordt voltooid</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde bron voor bedrijfsactiviteiten of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een routebewerking verwijst, kan gebruikmaken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Voorraad</td>
<td>Er kan niet automatisch een kwaliteitsorder worden gegenereerd voor een transactie in een voorraadjournaal of voor overdrachtordertransacties.</td>
<td></td>
<td></td>
<td>Er dient handmatig een kwaliteitsorder te worden gemaakt voor de voorraadhoeveelheid van een artikel. Fysieke voorhanden voorraad is vereist.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Kwaliteitsbeheerpagina's
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Pagina</th>
<th>Beschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kwaliteitskoppelingen</td>
<td>Zie de vorige secties van dit artikel.</td>
<td>Met een kwaliteitskoppeling worden de volgende gegevens gedefinieerd voor een gegenereerde kwaliteitsorder:
<ul>
<li>De transactiegebeurtenis</li>
<li>De tests die op de artikelen moeten worden uitgevoerd</li>
<li>Het acceptabele kwaliteitsniveau</li>
<li>Het bemonsteringsplan</li>
</ul>
U moet een kwaliteitskoppeling opgeven voor elke afwijking in een bedrijfsproces waarvoor automatisch kwaliteitsorders moeten worden gegenereerd. Er kan bijvoorbeeld een kwaliteitsorder worden gegenereerd in de bedrijfsprocessen voor inkooporders, quarantaineorders, verkooporders en productieorders.</td>
</tr>
<tr class="even">
<td>Tests</td>
<td>Met deze pagina kunt u de afzonderlijke tests definiëren en bekijken aan de hand waarvan wordt bepaald of uw producten voldoen aan de kwaliteitsspecificaties. U kunt een of meer afzonderlijke tests toewijzen aan een testgroep. In dit geval geeft u ook testspecifieke informatie op, zoals de aanvaardbare meetwaarden. Meetwaarden worden gebruikt voor kwantitatieve tests en testvariabelen worden gebruikt voor kwalitatieve tests.
<ul>
<li>Een kwantitatieve test is van het testtype <strong>Geheel getal</strong> of <strong>Breuk</strong> en heeft ook een bepaalde maateenheid. Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen.</li>
<li>Het testtype van een kwalitatieve test is <strong>Optie</strong>. Voor kwalitatieve tests is aanvullende informatie nodig over de testvariabele die wordt gemeten en de vaste opties. Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen volgens een uitkomst.</li>
</ul></td>
<td>Een productiebedrijf voert twee tests uit op ingekocht materiaal: een kwantitatieve test op de kwaliteit van het materiaal en een kwalitatieve test op beschadigde verpakking. Het bedrijf definieert aanvullende gegevens voor de kwalitatieve test om de testvariabele (beschadigde verpakking) en de bijbehorende uitkomst te bepalen. Het bedrijf maakt gebruikt van de pagina <strong>Testgroepen</strong> om de twee tests toe te wijzen aan een testgroep en om specifieke informatie voor de tests op te geven. De testgroep wordt toegewezen aan een kwaliteitsorder, zodat het bedrijf kan rapporteren over de testresultaten van de twee tests.</td>
</tr>
<tr class="odd">
<td>Testgroepen</td>
<td>Gebruik deze pagina voor het instellen, bewerken en weergeven van testgroepen en de afzonderlijke tests die zijn toegewezen aan een testgroep. In het bovenste deelvenster worden testgroepen weergegeven en in het onderste deelvenster worden de tests weergegeven die aan een geselecteerde testgroep zijn toegewezen. U wijst beleid toe aan een testgroep, zoals een bemonsteringsplan, een acceptabel kwaliteitsniveau en of een destructieve test moet worden uitgevoerd. Wanneer u een afzonderlijke test aan een testgroep toewijst, definieert u extra informatie, zoals de volgorde, datums en geldigheidsdatums. Voor een kwantitatieve test omvatten de gedefinieerde gegevens ook de acceptabele meetwaarden. Voor een kwalitatieve test omvatten de gegevens de testvariabele en standaarduitkomst. De testgroep die aan een kwaliteitsorder is toegewezen, bepaalt de standaardverzameling aan tests die moeten worden uitgevoerd op het opgegeven artikel. U kunt echter ook tests toevoegen aan en verwijderen of wijzigen in de kwaliteitsorder. De testresultaten worden vastgelegd voor elke test in een kwaliteitsorder.</td>
<td>Een productiebedrijf stelt een testgroep in voor elke wijziging van in de kwaliteitsrichtlijnen van het bedrijf. De verschillende testgroepen vertegenwoordigen de verschillen in de bemonsteringsplannen, de verzameling tests die moet worden uitgevoerd, de AQL en andere factoren. Voor kwantitatieve tests zijn er ook verschillen in de acceptabele meetwaarden. Het bedrijf dwingt zijn kwaliteitsrichtlijnen af door op de pagina <strong>Kwaliteitskoppelingen</strong> een testgroep toe te wijzen aan elke regel voor het automatisch genereren van kwaliteitsorders en een testgroep toe te wijzen aan handmatig gemaakte kwaliteitsorders.</td>
</tr>
<tr class="even">
<td>Artikelkwaliteitsgroepen</td>
<td>Gebruik deze pagina om de artikelen die aan een kwaliteitsgroep zijn toegewezen of de kwaliteitsgroepen die aan een artikel zijn toegewezen, in te stellen, te bewerken en weer te geven. Een kwaliteitsgroep bevat algemene testvereisten voor artikelen. Wanneer u de testvereisten hebt gedefinieerd op de pagina <strong>Testgroepen</strong>, kunt u de regels voor het automatisch genereren van kwaliteitsorders definiëren. Om het proces te vereenvoudigen, definieert u geen regels voor afzonderlijke artikelen. In plaats daarvan definieert u regels voor een kwaliteitsgroep op de pagina <strong>Kwaliteitskoppelingen</strong>. U kunt de pagina <strong>Artikelkwaliteitsgroepen</strong> ook gebruiken voor een bepaalde kwaliteitsgroep om relevante artikelen aan die groep toe te wijzen. U kunt de pagina <strong>Artikelkwaliteitsgroepen</strong> ook gebruiken voor een bepaald artikel om relevante kwaliteitsgroepen aan dat artikel toe te wijzen.</td>
<td>Een bedrijf dat artikelen vervaardigt koopt verschillende grondstoffen in waarvoor testvereisten gelden voor een op handen zijnde inspectie. Het bedrijf definieert een kwaliteitsgroep en wijst de artikelnummers die aan de grondstoffen zijn gekoppeld, aan deze groep toe. Later koopt het bedrijf een nieuw grondstoftype in waarop dezelfde testvereisten van toepassing zijn. In plaats van nieuwe testvereisten voor de nieuwe grondstof in te stellen, voegt het bedrijf het artikelnummer voor de nieuwe grondstof aan de bestaande kwaliteitsgroep toe. Hetzelfde productiebedrijf produceert tevens artikelen met dezelfde productietestvereisten en stuurt artikelen met dezelfde vereisten door voor tests die worden uitgevoerd voordat er een verzending plaatsvindt. Het bedrijf definieert twee extra kwaliteitsgroepen en wijst de relevante artikelnummers aan elke groep toe.</td>
</tr>
<tr class="odd">
<td>Testvariabelen</td>
<td>Gebruik deze pagina om de variabelen te definiëren die aan een kwalitatieve test zijn gekoppeld. Voor elke variabele definieert u genummerde uitkomsten die de mogelijke opties vertegenwoordigen. U definieert tests op de pagina <strong>Tests</strong>. Voor kwalitatieve tests moet u het testtype instellen op <strong>Optie</strong>. Gebruik de pagina <strong>Testgroepen</strong> om een testvariabele aan een afzonderlijke test toe te wijzen.</td>
<td>Een productiebedrijf dat koekjes produceert, maakt gebruik van een inspectietest voor het eindproduct. Deze inspectietest omvat verschillende variabelen. Een van deze variabelen is Smaak met de mogelijke uitkomsten Goed en Slecht. Een tweede variabele is Kleur met als mogelijke uitkomsten Te donker, Te licht en Correct.</td>
</tr>
<tr class="even">
<td>Uitkomsten van testvariabele</td>
<td>Gebruik deze pagina om de mogelijke testresultaten in te stellen, te bewerken en weer te geven voor een testvariabele die aan een kwaliteitstest is gekoppeld. Voor elke uitkomst wijst u de status <strong>Gehaald</strong> of <strong>Mislukt</strong> toe. U moet een variabele en de bijbehorende uitkomsten instellen voor elke kwaliteitstest die is ingesteld op de pagina <strong>Tests</strong>. (Voor kwalitatieve tests wordt het testtype ingesteld op <strong>Optie</strong> op de pagina <strong>Tests</strong>.) Gebruik de pagina <strong>Testgroepen</strong> om een testvariabele en de standaarduitkomst toe te wijzen aan een afzonderlijke kwaliteitstest.</td>
<td>Een productiebedrijf dat koekjes produceert, maakt gebruik van een inspectietest voor het eindproduct. Deze inspectietest omvat verschillende variabelen. Een van deze variabelen is Smaak met de mogelijke uitkomsten Goed en Slecht. Een tweede variabele is Kleur met als mogelijke uitkomsten Te donker, Te licht en Correct. Aan elke uitkomst wordt de status <strong>Gehaald</strong> of <strong>Mislukt</strong> toegewezen. De inspecteur rapporteert gedurende de inspectietest voor elke variabele de testresultaten door een van de uitkomsten te selecteren.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Zie ook
--------

[Processen voor kwaliteitsbeheer](quality-management-processes.md)

[Niet-conformeringsbeheer inschakelen](enable-nonconformance-management.md)


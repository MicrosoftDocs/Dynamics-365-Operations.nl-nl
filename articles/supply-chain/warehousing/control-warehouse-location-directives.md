---
title: Magazijnwerk beheren met werksjablonen en locatierichtlijnen
description: In dit onderwerp wordt beschreven hoe werksjablonen en locatie-instructies kunnen worden gebruikt om te bepalen hoe en waar werk wordt uitgevoerd in het magazijn.
author: perlynne
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4645cf36201aa1b87c22ba4dbfb1b8d8117f425a
ms.sourcegitcommit: fb7d0efd97754f1ae0b5aa765d0eeb3f57b8078f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3028023"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Magazijnwerk beheren met werksjablonen en locatierichtlijnen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe werksjablonen en locatie-instructies kunnen worden gebruikt om te bepalen hoe en waar werk wordt uitgevoerd in het magazijn.

De instructies die werknemers ontvangen op een mobiel apparaat worden gedefinieerd door de werksjablonen die u in Dynamics 365 Supply Chain Management hebt ingesteld om de verschillende magazijnprocessen en de functies te definiëren. Werksjablonen bepalen hoe het werk voor elk magazijnproces wordt uitgevoerd. Door een locatierichtlijn te koppelen aan werksjablonen kunt u helpen garanderen dat werk plaatsvindt in specifieke gebieden van de magazijnen.

## <a name="work-templates"></a>Werksjablonen
Op de pagina **Werksjablonen** kunt u de werkbewerkingen definiëren die in het magazijn moet worden uitgevoerd. Doorgaans bestaan de bewerkingen van het magazijnwerk uit een tweetal acties: een magazijnwerknemer verzameld voorhanden voorraad in één locatie en brengt de voorraad vervolgens naar een andere locatie. 

Werksjablonen bestaan uit een koptekst en bijbehorende regels. Elke werksjabloon is voor een specifiek *werkordertype* Veel typen werkorders worden gekoppeld aan brondocumenten, zoals inkoop- of verkooporders. Andere werkordertypen vertegenwoordigen echter aparte magazijnprocessen, zoals cyclustelling. Met *werkgroep-id's* kunt u werk in groepen organiseren. 

De instellingen in de definitie van het werkkoptekst kunnen worden gebruikt om te bepalen wanneer een nieuw werkstuk moet worden gemaakt. U kunt bijvoorbeeld een maximaal aantal verzamelregels en een maximale verwachte verzameltijd instellen. Vervolgens, als het werk voor een verzamelproces voor een verkooporder een van die waarden overschrijdt, wordt dat werk opgesplitst in twee werkstukken. 

De werkregels vertegenwoordigen de fysieke taken die zijn vereist om het werk te kunnen verwerken. Voor een uitgaand magazijnproces kan er bijvoorbeeld een werkregel zijn het voor het verzamelen van de artikelen in het magazijn en een andere regel voor het plaatsen van die artikelen in het faseringsgebied. Er kunnen vervolgens een extra regel voor het verzamelen van de artikelen voor het klaarzetten en een andere regel voor het plaatsen van de artikelen in een truck deel uitmaken van het ladingsproces. U kunt een *instructiecode* voor werksjabloonregels instellen. Een richtlijncode is gekoppeld aan een locatierichtlijn en helpt daarom te garanderen dat het magazijnwerk op de juiste locatie in het magazijn wordt verwerkt. 

U kunt een query instellen om te bepalen wanneer een bepaalde werksjabloon wordt gebruikt. U kunt bijvoorbeeld een beperking instellen, zodat een bepaalde sjabloon alleen voor werk kan worden gebruikt in een specifiek magazijn. Als alternatief hebt u mogelijk verschillende sjablonen die worden gebruikt om werk voor uitgaande verkooporderverwerking te maken, afhankelijk van de verkoopoorsprong. Het veld **Volgnummer** wordt gebruikt om de volgorde te definiëren waarin de beschikbare werksjablonen worden beoordeeld. Daarom moet u, als u een zeer specifieke zoekopdracht voor een bepaalde werksjabloon hebt, er een laag volgnummer aan toewijzen. Die Query wordt vervolgens beoordeeld vóór andere, meer algemene query's. 

Om een werkproces te onderbreken of stopen, kunt u de instelling **Werk stoppen** gebruiken op de werkregel. In dat geval wordt de werknemer die het werk uitvoert, niet gevraagd de volgende werkregelstap uit te voeren. Om naar de volgende stap te gaan, moet die werknemer of een andere werknemer het werk opnieuw selecteren. U kunt de taken in een stuk werk ook scheiden door een andere *werkklasse-ID* te gebruiken in de werksjabloonregels.

## <a name="location-directives"></a>Instructielocatie
De locatierichtlijnen zijn regels die verzamelings- en wegzetlocaties identificeren voor voorraadverplaatsing. In een verkoopordertransactie kan een locatierichtlijn bijvoorbeeld bepalen waar de artikelen worden verzameld en waar de verzamelde artikelen worden geplaatst. Locatierichtlijnen bestaan uit een koptekst en gekoppelde regels, en u maakt deze op de pagina **Locatierichtlijnen**. 

Voor de koptekst, moet elke locatierichtlijn zijn gekoppeld aan een *werkordertype* dat het type voorraadtransactie opgeeft waarvoor de richtlijn wordt gebruikt, zoals verkooporders gebruikt, aanvulling, of orderverzameling van grondstoffen. Het *werktype* geeft aan of de locatierichtlijn wordt gebruikt voor het verzamelen van of het plaatsen van het werk, of voor een ander magazijnproces, zoals tellen of voorraadstatuswijzigingen. U moet ook een *locatie* en een *magazijn* opgeven. Een *richtlijncode* die u opgeeft in de koptekst, kan worden gebruikt om de locatierichtlijn aan een of meer werksjablonen te koppelen. 

Net als werksjablonen kunt u een query instellen om te bepalen wanneer een bepaalde locatierichtlijn wordt gebruikt. U kunt bijvoorbeeld opgeven dat wanneer e-commerce de oorsprong van een verkooporder is, is de voorraad moet worden verzameld uit een speciaal gedeelte in het magazijn. Het systeem gebruikt het veld **Volgnummer** om de volgorde te definiëren waarin de beschikbare locatierichtlijnen worden beoordeeld. 

De locatierichtlijnen stellen aanvullende beperkingen in voor de toepassing van regels voor het zoeken van de locatie. U kunt een minimale en maximale hoeveelheid opgeven waarop de richtlijn wordt toegepast en u kunt opgeven dat de richtlijn voor een specifieke voorraadeenheid moet zijn. Als de maateenheid bijvoorbeeld pallets is, kunnen de artikelen in pallets op een bepaalde locatie worden geplaatst. U kunt ook opgeven of de hoeveelheid over meerdere locaties kan worden opgesplitst. Net als de koptekst van de locatierichtlijn heeft elke regel van de locatierichtlijn een volgnummer dat de volgorde bepaalt waarin regels worden beoordeeld. 

De locatierichtlijnen hebben één extra detailniveau: *de acties van de locatierichtlijn*. U kunt meerdere locatierichtlijnacties voor elke regel definiëren. Een volgnummer wordt dus gebruikt om de volgorde te bepalen waarin de acties worden beoordeeld. Op dit niveau kunt u een zoekopdracht instellen om te definiëren hoe de beste locatie in het magazijn kan worden gevonden. U kunt ook vooraf gedefinieerde instellingen voor **Strategie** gebruiken om een optimale locatie te zoeken.

## <a name="location-directives-configuration-details"></a>Configuratiedetails locatie-instructies 

 ### <a name="sequence-number"></a>Volgnummer
 
Dit nummer duidt de volgorde aan waarin een locatie-instructie voor een geselecteerd ordertype wordt verwerkt. Dit kan worden gewijzigd met **Omhoog** en **Omlaag** in het menu.
 
 ### <a name="work-type"></a>Werktype
 
Dit is het type werk dat moet worden uitgevoerd. Het beschikbare type werk is gebaseerd op het type voorraadtransactie dat u in het veld **Werkordertype** hebt geselecteerd.
-   **Wegzetten** - Een werktype **Wegzetten** betekent dat de locatierichtlijn de meest optimale locatie vindt om voorraad te plaatsen of te zoeken die binnenkomt in het systeem, op basis van ontvangsten, productie of voorraadaanpassingen. Het kan ook worden gebruikt om een faseringslocatie voor wegzetten of een laaddeur voor de uiteindelijke verzendlocatie op te geven.
-   **Verzamelen** - Een werktype **Verzamelen** betekent dat het magazijn de meest optimale locatie zoekt om voorraad fysiek van te reserveren (werk maken). De verzameling kan ook worden voltooid (verzamelwerkregel kan worden gesloten) als het werk nog niet is voltooid. De gebruiker kan de fysieke verzameling voltooien. De gebruiker kan vervolgens annuleren vanaf een mobiel apparaat en het werk later voltooien. De werkkoptekst wordt echter gesloten wanneer de laatste plaatsing is voltooid. 
-   **Tellen, Correcties, Aangepast, Wijziging van voorraadstatus, Nummerplaat maken, afdrukken, Statuswijziging, Verpakken naar geneste nummerplaten** - Deze zijn niet bruikbaar in een setup met locatie-instructies. Dit is een opsomming, dus er zijn geen filters verbonden met het type werkorder. 

### <a name="directive-code"></a>Instructiecode

Selecteer de richtlijncode om aan een werksjabloon of het aanvullingssjabloon te associeren. Op het formulier **Instructiecode** kunt u nieuwe codes maken die kunnen worden gebruikt voor verbindingen tussen een aanvullingssjabloon voor een werksjabloon en locatie-instructie. Dit kan ook worden gebruikt om de koppeling tussen een werksjabloonregel en locatie-instructie tot stand te brengen (zoals een laaddeur of faseringslocatie).

Als er code is ingesteld en er werk wordt gegenereerd, wordt de locatie-instructie niet op volgorde doorzocht, maar wordt er op instructiecode gezocht. Dit betekent dat u specifieker kunt opgeven welke locatiesjabloon moet worden gebruikt voor een bepaalde stap in een werksjabloon, zoals de fasering van materialen. 

### <a name="site"></a>Site

Locatie is een verplicht veld omdat de locatie-instructie de locatie en het magazijn waarvoor deze geldig is nodig heeft. 

### <a name="warehouse"></a>Magazijn

Magazijn is een verplicht veld omdat de locatie-instructie de locatie en het magazijn waarvoor deze geldig is nodig heeft.

### <a name="multiple-sku"></a>Meerdere SKU's

Hiermee zijn meerdere voorraadeenheden (SKU's), zoals de laaddeur, toegestaan op een locatie. Als u **Meerdere SKU's** selecteert, wordt de wegzetlocatie opgegeven tijdens het werk (verwacht), maar dit is alleen mogelijk voor het verwerken van meerdere artikelen (als meerdere SKU's moeten worden verzameld en weggezet en niet een afzonderlijke SKU). Als u **Meerdere SKU's** niet selecteert, wordt de wegzetlocatie alleen opgegeven als er slechts één soort SKU moet worden weggezet. Als u beide acties wilt gebruiken, moet u twee regels opgeven, één met Meerdere SKU's ingeschakeld en één met Meerdere SKU's uitgeschakeld. Deze moeten dezelfde structuur en instellingen hebben. Voor wegzetbewerkingen moet u locatie-instructies hebben die identiek zijn, zelfs als u geen onderscheid maakt tussen enkele en meerdere SKU's op de werk-id. Daarnaast moet u instellingen opgeven voor orderverzameling, zelfs als u een order met meerdere artikelen hebt.

### <a name="sequence-number"></a>Volgnummer

Geef op in welke volgorde de locatie-instructieregels moeten worden verwerkt voor het geselecteerde werktype. U kunt de volgorde ook wijzigen indien nodig, via **Omhoog** en **Omlaag**.

### <a name="fromto-quantity"></a>Vanaf hoeveelheid/Tot hoeveelheid

Hiermee kunt u een hoeveelheidsbereik opgeven voor als de volgorde van het middelste raster moet worden geselecteerd. U kunt het bereik voor de hoeveelheid opgeven in de betreffende eenheid.

### <a name="unit"></a>Eenheid

U kunt een minimale en maximale hoeveelheid opgeven waarop de richtlijn wordt toegepast en u kunt opgeven dat de richtlijn voor een specifieke voorraadeenheid moet zijn. Het veld Eenheid op de regel wordt gebruikt voor de evaluatie van de hoeveelheid.

Wanneer wordt gecontroleerd of de locatie-instructieregel van toepassing is, wordt dit gebaseerd op de hoeveelheid in de betreffende eenheid die is opgegeven op de locatie-instructieregel. Elke keer dat een locatie-instructieregel wordt bereikt, wordt geprobeerd de vraageenheid om te zetten in een eenheid die is opgegeven op de regel. Als de maateenheidconversie niet bestaat, wordt doorgegaan naar de volgende regel. 

### <a name="locate-quantity"></a>Hoeveelheid plaatsen

Deze optie wordt alleen gebruikt voor het wegzetten/zoeken van hoeveelheid in het magazijn. Dit is alleen bedoeld voor werk van het type wegzetten. De volgende waarden zijn geldig:

-   **Nummerplaathoeveelheid**: wanneer moet worden gecontroleerd of de hoeveelheid zich in het bereik tussen Vanaf en Tot bevindt, wordt de hoeveelheid op de ontvangen nummerplaat gebruikt.
-   **In eenheden omgezette hoeveelheid**: wanneer moet worden gecontroleerd of de hoeveelheid zich in het bereik tussen Vanaf en Tot bevindt, wordt de in eenheden omgezette hoeveelheid tijdens de specifieke transactie gebruikt.
-   **Resterende hoeveelheid**: wanneer moet worden gecontroleerd of de hoeveelheid zich in het bereik tussen Vanaf en Tot bevindt, wordt de resterende te ontvangen hoeveelheid op de inkooporderregel die wordt ingecheckt gebruikt.
-   **Verwachte hoeveelheid**: wanneer moet worden gecontroleerd of de hoeveelheid zich in het bereik tussen Vanaf en Tot bevindt, wordt de totale hoeveelheid op de inkooporderregel gebruikt, ongeacht wat al is ontvangen.

### <a name="restrict-by-unit"></a>Beperken op eenheid

Hiermee kunt u een specifieke locatie-instructieregel voor een maateenheid of meerdere maateenheden maken. Wanneer u bij het reserveren van hoeveelheid alleen pallets van een specifieke reeks locaties wilt reserveren, wordt die volgorde op basis van de volgorde van het middelste raster beperkt tot PL zodat bij elke hoeveelheid kleiner dan een pallet de volgorde niet wordt geselecteerd. Selecteer **Beperken op eenheid** om de eenheden in te stellen. U kunt de regel ook beperken tot meer dan één eenheid. Dit werkt alleen voor locatie-instructies van het type orderverzameling. 

### <a name="round-up-to-unit"></a>Naar eenheid afronden

Dit veld werkt in combinatie met het veld **Beperken op eenheid**. Als de locatie-instructieregel **Beperken op eenheid** is ingesteld op Vak en u **Naar eenheid afronden** selecteert, geeft u aan dat het gegenereerde werk op basis van orderverzameling van grondstoffen naar boven moet worden afgerond naar een veelvoud van één materiaalverwerkingseenheid (opgegeven in **Beperken op eenheid**). Dit werkt alleen voor orderverzameling van grondstoffen en alleen met locatie-instructies van het type orderverzameling.

### <a name="locate-packing-qty"></a>Zoek verpakkingshoeveelheid

Als een verpakkingshoeveelheid is opgegeven op een verkooporder, transferorder of productieorder, worden alleen locaties met een verpakkingshoeveelheid op de locatie geselecteerd. Dit werkt alleen voor locatie-instructies van het type orderverzameling.

### <a name="allow-split"></a>Splitsing toestaan

Hiermee geeft u op of een locatie-instructie is toegestaan om de ontvangen of gereserveerde hoeveelheid te verdelen over meerdere magazijnlocaties of dat de gehele hoeveelheid zich in één locatie moet bevinden of vanuit één locatie moet worden gereserveerd om werk te maken. 

### <a name="sequence-number"></a>Volgnummer

Dit nummer staat voor de volgorde waarin de locatie-instructie voor het geselecteerde werktype wordt verwerkt. U kunt de volgorde wijzigen, als dat nodig is. Ga echter zorgvuldig te werk met volgnummers, aangezien de verwerking altijd op volgorde wordt uitgevoerd. 

### <a name="name"></a>Naam

Voer een naam in voor de locatie-instructieactie. Wees specifiek wanneer u een naam opgeeft.

### <a name="fixed-location-usage"></a>Gebruik vaste locaties 

-   **Vaste en niet-vaste locaties**: alle locaties komen in aanmerking voor de locatie-instructie.
-   **Alleen vaste locaties voor het product**: alleen vaste locaties voor producten komen in aanmerking voor de locatie-instructie.
-   **Alleen vaste locaties voor de productvariant**: alleen vaste locaties voor productvarianten komen in aanmerking voor de locatie-instructie.

### <a name="allow-negative-inventory"></a>Negatieve voorraad toestaan

Selecteer deze optie om negatieve voorraad op de opgegeven magazijnlocatie in locatie-instructies toe te staan. 

### <a name="batch-enabled"></a>Batch ingeschakeld 

Selecteer deze optie om batchstrategieën voor de artikelen te gebruiken die voor batches kunnen worden ingeschakeld. Als u een regel bereikt waar **Batch ingeschakeld** is ingesteld zonder batchartikel, gaat het proces verder met de volgende actieregel. 

### <a name="strategy"></a>Strategie

-   **Consolideren**: deze optimalisatiestrategie wordt gebruikt om artikelen in een bepaalde locatie te consolideren wanneer vergelijkbare artikelen beschikbaar zijn. Dit werkt alleen voor de locatie-instructie van het type Wegzetten. Algemene instellingen voor wegzetten zijn bedoeld om te consolideren op de eerste actieregel en bij de tweede poging weg te zetten zonder consolidatie. Door goederen te consolideren, wordt orderverzamelen later efficiënter.
-   **Verpakkingshoeveelheid afstemmen**: met deze strategie wordt een locatie gevonden die een nummerplaat bevat met de exact vereiste hoeveelheid. Het kan niet worden gebruikt bij locaties niet met nummerplaten worden beheerd. Deze strategie werkt alleen voor locatie-instructies van het type verzamelwerk.
-   **FEFO-batchreservering**: deze strategie wordt gebruikt wanneer voorraad wordt gevonden door middel van een batchvervaldatum en voor een batchreservering wordt toegewezen. U kunt deze strategie alleen maar voor batch ingeschakelde artikelen gebruiken. Dit werkt alleen voor locatie-instructies van het type verzamelwerk. 
-   **Naar volledige LP afronden**: deze strategie wordt gebruikt om de voorraadhoeveelheid naar boven af te ronden om de hoeveelheid toegewezen nummerplaten (LP) te verzamelen. U kunt deze strategie alleen gebruiken voor het aanvullingstype van de locatie-instructie van het type Verzamelen. 
-   **Lege locatie zonder inkomend werk**: deze strategie wordt gebruikt om blanco locaties te vinden. De locatie wordt beschouwd als leeg als het geen fysieke voorraad en geen verwacht inkomend werk heeft. Deze strategie wordt alleen gebruikt voor een locatie-instructie van het type Wegzetten. 

### <a name="example-of-the-use-of-location-directives"></a>Voorbeeld van het gebruik van locatierichtlijnen

Voor dit voorbeeld kijken we naar een inkooporderproces waar de locatie-instructie vrije capaciteit in een magazijn moet zoeken voor voorraadartikelen die zojuist zijn geregistreerd in het ontvangende dok. Eerst moet u we beschikbare capaciteit in het magazijn vinden door te consolideren met bestaande voorhanden voorraad. Als consolidatie niet mogelijk is, moet u een lege locatie zoeken. 

Voor dit scenario moet u twee locatie-instructieacties definiëren. De eerste actie in de reeks moet de **consolidatie**-strategie gebruiken, de tweede de **Lege locatie met geen inkomend werk**-strategie. Tenzij u een derde actie definieert om een overloopscenario te dekken, zijn er twee resultaten mogelijk wanneer er geen capaciteit meer is in het magazijn: werk kan worden gemaakt zonder dat er locaties worden gedefinieerd of het werkaanmaakproces mislukt. Het resultaat wordt gedefinieerd door de instellingen op de pagina **Fouten bij locatie-instructie**, waar u kunt kiezen om de optie **Werk stoppen bij fout van locatie-instructie** voor elk type werkorder te selecteren.

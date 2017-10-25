---
title: Magazijnwerk beheren met werksjablonen en locatierichtlijnen
description: In dit artikel wordt beschreven hoe werksjablonen en locatierichtlijnen kunnen worden gebruikt om te bepalen hoe en waar werk wordt uitgevoerd in het magazijn.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b32e2d178f9f0307fea4362e5ec99aa67c81ee8
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Magazijnwerk beheren met werksjablonen en locatierichtlijnen

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe werksjablonen en locatierichtlijnen kunnen worden gebruikt om te bepalen hoe en waar werk wordt uitgevoerd in het magazijn.

De instructies die werknemers ontvangen op een mobiel apparaat worden gedefinieerd door de werksjablonen die u in Microsoft Dynamics 365 for Finance and Operations hebt ingesteld om de verschillende magazijnprocessen en de functies te definiëren. Werksjablonen bepalen hoe het werk voor elk magazijnproces wordt uitgevoerd. Door een locatierichtlijn te koppelen aan werksjablonen kunt u helpen garanderen dat werk plaatsvindt in specifieke gebieden van de magazijnen.

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

### <a name="example-of-the-use-of-location-directives"></a>Voorbeeld van het gebruik van locatierichtlijnen

Voor dit voorbeeld kijken we naar een inkooporderproces waar de locatierichtlijn vrije capaciteit in een magazijn moet zoeken voor voorraadartikelen die zojuist zijn geregistreerd in het ontvangende dok. Eerst proberen we beschikbare capaciteit in het magazijn te vinden door te consolideren met bestaande voorhanden voorraad. Als consolidatie niet mogelijk is, willen we een lege locatie zoeken. 

Voor dit scenario moeten er twee locatierichtlijnacties worden gedefinieerd. De eerste actie in de reeks moet de **consolidatie**-strategie gebruiken, de tweede de **Lege locatie met geen inkomend werk**-strategie. Tenzij we een derde actie definiëren om een overloopscenario te dekken, zijn er twee resultaten mogelijk wanneer er geen capaciteit meer is in het magazijn: werk kan worden gemaakt zonder dat er locaties worden gedefinieerd, of het werkaanmaakproces mislukt. Het resultaat wordt gedefinieerd door de instellingen op de pagina **Fouten bij locatie-instructie**, waar u kunt kiezen om de optie **Werk stoppen bij fout van locatie-instructie** voor elk type werkorder te selecteren.




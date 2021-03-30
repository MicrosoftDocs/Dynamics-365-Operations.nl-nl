---
title: Magazijnwerk beheren met werksjablonen en locatierichtlijnen
description: In dit onderwerp wordt beschreven hoe werksjablonen en locatie-instructies kunnen worden gebruikt om te bepalen hoe en waar werk wordt uitgevoerd in het magazijn.
author: perlynne
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f51d30a63cba9e9fa5c8319c8b7d713acea5f19c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214173"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Magazijnwerk beheren met werksjablonen en locatierichtlijnen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe werksjablonen en locatie-instructies kunnen worden gebruikt om te bepalen hoe en waar werk wordt uitgevoerd in het magazijn.

De instructies die werknemers ontvangen op een mobiel apparaat worden gedefinieerd door de werksjablonen die u in Dynamics 365 Supply Chain Management hebt ingesteld om de verschillende magazijnprocessen en de functies te definiëren. Werksjablonen bepalen hoe het werk voor elk magazijnproces wordt uitgevoerd. Door een locatierichtlijn te koppelen aan werksjablonen kunt u helpen garanderen dat werk plaatsvindt in specifieke gebieden van de magazijnen.

## <a name="work-templates"></a>Werksjablonen

Op de pagina **Werksjablonen** kunt u de werkbewerkingen definiëren die in het magazijn moet worden uitgevoerd. Doorgaans bestaan de bewerkingen van het magazijnwerk uit een tweetal acties: een magazijnwerknemer verzameld voorhanden voorraad in één locatie en brengt de voorraad vervolgens naar een andere locatie. 

Werksjablonen bestaan uit een koptekst en bijbehorende regels. Elke werksjabloon is voor een specifiek *werkordertype* Veel typen werkorders worden gekoppeld aan brondocumenten, zoals inkoop- of verkooporders. Andere werkordertypen vertegenwoordigen echter aparte magazijnprocessen, zoals cyclustelling. Met *werkgroep-id's* kunt u werk in groepen organiseren. 

Gebruik de instellingen in de definitie van het werkkoptekst om te bepalen wanneer een nieuw werkstuk moet worden gemaakt. U kunt bijvoorbeeld een maximaal aantal verzamelregels en een maximale verwachte verzameltijd instellen. Vervolgens, als het werk voor een verzamelproces voor een verkooporder een van die waarden overschrijdt, wordt dat werk opgesplitst in twee werkstukken.

Met de knop **Opsplitsingen voor werkkoptekst** definieert u wanneer het systeem nieuwe werkkopteksten moet maken. Als u bijvoorbeeld een werkkoptekst wilt maken voor elk _ordernummer_, selecteert u **Query bewerken** in het actiedeelvenster en voegt u het veld **Ordernummer** toe aan het tabblad **Sorteren** van de query-editor. Velden die worden toegevoegd aan het tabblad **Sorteren** zijn beschikbaar voor selectie als *groeperingsvelden*. Als u groeperingsvelden wilt instellen, selecteert u de optie **Opsplitsingen voor werkkoptekst** in het actiedeelvenster en selecteert u voor elk veld dat u als groeperingsveld wilt gebruiken, het selectievakje in de kolom **Groeperen op dit veld**.

De werkregels vertegenwoordigen de fysieke taken die zijn vereist om het werk te kunnen verwerken. Voor een uitgaand magazijnproces kan er bijvoorbeeld één regel zijn het voor het verzamelen van de artikelen in het magazijn en een andere regel voor het plaatsen van die artikelen in het faseringsgebied. Er kan vervolgens een extra regel worden toegevoegd voor het verzamelen van de artikelen uit de fasering en weer een andere voor het plaatsen van de artikelen in een truck als onderdeel van het ladingsproces. U kunt een *instructiecode* voor werksjabloonregels instellen. Een instructiecode is gekoppeld aan een locatie-instructie en helpt daarom te waarborgen dat het magazijnwerk op de juiste locatie in het magazijn wordt verwerkt.

U kunt een query instellen om te bepalen wanneer een bepaalde werksjabloon wordt gebruikt. U kunt bijvoorbeeld een beperking instellen, zodat een bepaalde sjabloon alleen voor werk kan worden gebruikt in een specifiek magazijn. Als alternatief hebt u mogelijk verschillende sjablonen om werk voor uitgaande verkooporderverwerking te maken, afhankelijk van de verkoopoorsprong. Het veld **Volgnummer** wordt gebruikt om de volgorde te definiëren waarin de beschikbare werksjablonen worden beoordeeld. Daarom moet u, als u een zeer specifieke zoekopdracht voor een bepaalde werksjabloon hebt, er een laag volgnummer aan toewijzen. Die query wordt vervolgens beoordeeld vóór de andere, meer algemene query's.

> [!NOTE]
> Als u wilt voorkomen dat het systeem automatisch *volgnummers* van werksjablonen overschrijft nadat een sjabloon is verwijderd, schakelt u de functie *Volgnummers van werksjabloon bij verwijderen behouden* in bij [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Om een werkproces te onderbreken of stopen, kunt u de instelling **Werk stoppen** gebruiken op de werkregel. In dat geval wordt de werknemer die het werk uitvoert, niet gevraagd de volgende werkregelstap uit te voeren. Om naar de volgende stap te gaan, moet die werknemer of een andere werknemer het werk opnieuw selecteren. U kunt de taken in een stuk werk ook scheiden door een andere *werkklasse-ID* te gebruiken in de werksjabloonregels.

## <a name="location-directives"></a>Instructielocatie

De locatierichtlijnen zijn regels die verzamelings- en wegzetlocaties identificeren voor voorraadverplaatsing. In een verkoopordertransactie kan een locatierichtlijn bijvoorbeeld bepalen waar de artikelen worden verzameld en waar de verzamelde artikelen worden geplaatst. Locatierichtlijnen bestaan uit een koptekst en gekoppelde regels, en u maakt deze op de pagina **Locatierichtlijnen**.

Voor de koptekst, moet elke locatierichtlijn zijn gekoppeld aan een *werkordertype* dat het type voorraadtransactie opgeeft waarvoor de richtlijn wordt gebruikt, zoals verkooporders gebruikt, aanvulling, of orderverzameling van grondstoffen. Het *werktype* geeft aan of de locatierichtlijn wordt gebruikt voor het verzamelen van of het plaatsen van het werk, of voor een ander magazijnproces, zoals tellen of voorraadstatuswijzigingen. U moet ook een *locatie* en een *magazijn* opgeven. Een *richtlijncode* die u opgeeft in de koptekst, kan worden gebruikt om de locatierichtlijn aan een of meer werksjablonen te koppelen. 

Net als werksjablonen kunt u een query instellen om te bepalen wanneer een bepaalde locatierichtlijn wordt gebruikt. U kunt bijvoorbeeld opgeven dat wanneer e-commerce de oorsprong van een verkooporder is, is de voorraad moet worden verzameld uit een speciaal gedeelte in het magazijn. Het systeem gebruikt het veld **Volgnummer** om de volgorde te definiëren waarin de beschikbare locatierichtlijnen worden beoordeeld.

De locatierichtlijnen stellen aanvullende beperkingen in voor de toepassing van regels voor het zoeken van de locatie. U kunt een minimale en maximale hoeveelheid opgeven waarop de richtlijn wordt toegepast en u kunt opgeven dat de richtlijn voor een specifieke voorraadeenheid moet zijn. Als de maateenheid bijvoorbeeld pallets is, kunnen de artikelen in pallets op een bepaalde locatie worden geplaatst. U kunt ook opgeven of de hoeveelheid over meerdere locaties kan worden opgesplitst. Net als de koptekst van de locatierichtlijn heeft elke regel van de locatierichtlijn een volgnummer dat de volgorde bepaalt waarin regels worden beoordeeld.

De locatierichtlijnen hebben één extra detailniveau: *de acties van de locatierichtlijn*. U kunt meerdere locatierichtlijnacties voor elke regel definiëren. Een volgnummer wordt dus gebruikt om de volgorde te bepalen waarin de acties worden beoordeeld. Op dit niveau kunt u een zoekopdracht instellen om te definiëren hoe de beste locatie in het magazijn kan worden gevonden. U kunt ook vooraf gedefinieerde instellingen voor **Strategie** gebruiken om een optimale locatie te zoeken.

Zie [Een locatie-instructie maken](create-location-directive.md) voor meer informatie over het maken en configureren van locatie-instructies.

### <a name="how-location-directives-work"></a>Hoe werken locatie-instructies

De locatie-instructies bepalen *waar* artikelen moeten worden verzameld en *waar* ze moeten worden geplaatst. Het systeem evalueert een locatie-instructie aan de hand van elke werkregel en selecteert vervolgens een locatie op basis van de details van de werkregel. Het systeem zoekt eerst naar alle locatie-instructies die overeenkomen met een bepaalde werkregel (bijvoorbeeld voor het juiste magazijn en overeenkomen met de query). De gevonden instructies worden vervolgens opeenvolgend geëvalueerd.

> [!NOTE]
> Er zijn speciale gevallen waarin de orderverzamellocatie of de neerzetlocatie vooraf is geselecteerd. Tijdens de _inkoopregistratie_ is de eerste verzamelorder bijvoorbeeld altijd afkomstig van de locatie waar de registratie plaatsvindt. Een ander voorbeeld is *voorraadmutatie per sjabloon*, waarbij de magazijnmedewerker de orderverzamellocatie selecteert en alleen de neerzetlocaties worden gevonden via locatie-instructies.

## <a name="additional-resources"></a>Aanvullende bronnen

- Video: [Configuratie van magazijnbeheer: diepgravend](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Help-onderwerp: [Locatie-instructies maken](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Overzicht van Magazijnconfiguratie
description: In dit artikel wordt beschreven hoe u een magazijn configureert. Er wordt aangegeven hoe u een magazijnindeling en magazijnprocessen inschakelt.
author: perlynne
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11554"
- intro-internal
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7643a333c269a7e1976563ff0f10b89c1fb91674
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065177"
---
# <a name="warehouse-configuration-overview"></a>Overzicht van Magazijnconfiguratie

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een magazijn configureert. Er wordt aangegeven hoe u een magazijnindeling en magazijnprocessen inschakelt.

> [!NOTE]
> Dit artikel geldt voor functies in de module voor **Magazijnbeheer**. Het is niet van toepassing op magazijnfuncties in de module **Voorraadbeheer**.

## <a name="warehouse-layout"></a>Magazijnindeling
Met Magazijnbeheerprocessen (WMS) in Supply Chain Management hebt u flexibele manieren om uw magazijnindeling te definiëren voor wisselende behoeften, zodat u optimale magazijnefficiëntie kunt bereiken.

-   U kunt opslaggebieden met hoge prioriteit en lage prioriteit ontwikkelen voor optimale plaatsing van goederen.
-   U kunt uw magazijn in zones verdelen voor verschillende opslagbehoeften, zoals temperatuurvereisten of diverse omzettarieven voor artikelen.
-   U kunt magazijnlocaties op elk niveau (bijvoorbeeld locatie, magazijn, gang, rek, plank en bakpositie) opgeven.
-   U kunt locaties groeperen door de instellingen voor fysieke capaciteitsbeperking te gebruiken.
-   U kunt bepalen hoe de artikelen worden opgeslagen en verzameld, gebaseerd op query-bepaalde regels.

Als u WMS wilt gebruiken in Supply Chain Management, moet u een magazijn maken en het inschakelen voor WMS. Selecteer op de pagina **Magazijnen** de optie **Magazijnbeheerprocessen gebruiken**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Zonegroepen, zones, locatietypen en locaties

Als onderdeel van het proces voor een magazijnindeling moet u de magazijnzonegroepen, zones, locatieprofielen, locatietypen en locaties definiëren.

-   **Zonegroepen**: de logische of fysieke groepering van zones in een magazijn.
-   **Zones**: een logische of fysieke groepering van locaties in een magazijn.
-   **Locatieprofielen**: de logische of fysieke groepering van locaties die hetzelfde magazijnlocatieprocesbeleid (bijvoorbeeld een mix van verschillende artikelnummers die daar kunnen worden opgeslagen en waarvoor dezelfde fysieke capaciteitsbeperkingen gelden) hebben.
-   **Locatietypen**: de logische of fysieke groepering van de magazijnlocaties. U kunt bijvoorbeeld een locatietype voor alle faseringslocaties maken. De verplichte instellingen op de pagina **Parameters voor magazijnbeheer** bevorderen het proces om faseringslocatietypen en het uiteindelijke verzendlocatietype te definiëren.
-   **Locaties**: het laagste locatiegegevensniveau. De locaties worden gebruikt om te traceren waar de voorhanden voorraad wordt opgeslagen en in een magazijn verzameld.

De rechtspersonen die u maakt om uw magazijnindeling te definiëren, worden gebruikt in de query's die u in de werksjablonen instelt om werkorders in het magazijn te sturen. Wanneer u dus de zones, locatietypen, enzovoort selecteert, moet u er dus rekening mee houden hoe de verschillende gebieden in het magazijn voor verschillende processen worden gebruikt. Houd bovendien rekening met factoren zoals de fysieke kenmerken van een specifiek gebied. Er kunnen bijvoorbeeld gebieden zijn waarin u alleen een bepaald type vorkheftruck kunt gebruiken. Of, als uw bedrijf zowel productie als gereed gemelde goederen binnen dezelfde faciliteit heeft, kunt u wellicht één magazijn in Supply Chain Management maken maar hierbij de twee bewerkingen van elkaar scheiden door twee zonegroepen te maken. Geef uw entiteiten beschrijvende namen, zodat het eenvoudig is om te identificeren wanneer u ze in sjabloonquery's gebruikt.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Locatie-opslaglimieten, locatieprofielen en vaste orderverzamellocaties

U moet rekening houden met de fysieke indeling van het magazijn, zowel om opslagcapaciteiten (locatie-opslaglimieten en locatieprofielen) te definiëren en als onderdeel van uw pogingen om optimale magazijnprocessen te bereiken. 

Opslaglimieten van locaties helpen ervoor te zorgen dat geen werk wordt gemaakt om te verzoeken dat voorraad wordt geplaatst op een locatie die niet de fysieke capaciteit voor die voorraad heeft. Als in sommige locaties in een magazijn bijvoorbeeld alleen plaats is voor één pallet per locatie, kunt u de locatie-opslagbeperkingen inschakelen. De waarde van **Hoeveelheid** kan worden ingesteld op **1** en de **Eenheid** kan worden ingesteld op **PL** in een specifieke locatieprofielgroep. 

Als meer geavanceerdere berekeningen vereist zijn om de locatiecapaciteitsbeperkingen te controleren, kunt u de locatieprofielinstellingen gebruiken. In dit geval worden het gewicht en volume in aanmerking genomen bij de capaciteitsberekeningen. 

Om optimale uitgaande processen te bereiken, dient u te bepalen of u orderverzamellocaties en/of verpakkingslocaties wilt gebruiken. Vaak wordt minimum- en maximumaanvulling gebruikt voor aanvullingsprocessen van een bulkgebied naar de vaste verzamellocaties, en meerdere vaste orderverzamellocaties kunnen in hetzelfde magazijn en voor productvarianten worden ingeschakeld. Overweeg de flexibiliteit die u kunt bereiken door aanvullingsoverlooplocaties voor speciale aanvragen, die alleen worden gebruikt voor verwerking van wave-/ladingaanvulling worden gebruikt, in te schakelen.

### <a name="location-setup-wizard"></a>Wizard voor locatie-instelling

Als u de locaties in een magazijn snel wilt maken, kunt u de wizard **Locatie-instelling** gebruiken. Als onderdeel van dit proces kunt u de indeling van de locatienamen eenvoudig beheren.

## <a name="warehouse-processes"></a>Magazijnprocessen
Als onderdeel van de configuratie van het magazijn is het belangrijk dat u magazijnprocessen overeenkomstig de bedrijfsbehoeften inschakelt. De belangrijkste onderdelen die u moet configureren zijn wavesjablonen, werksjablonen, werkgroepen en locatierichtlijnen.

### <a name="wave-templates"></a>Wavesjablonen

Wavesjablonen helpen om het uitgaande proces "wavesjablonen " in te schakelen. Wanneer de orderregels worden vrijgegeven (rechtstreeks uit brondocumenten, via batchtaakprocessen of via ladingen die al zijn gemaakt), wordt de wavesjabloonfunctionaliteit gebruikt. 

U kunt drie typen wave-sjablonen maken: 
-   **Verzending**
-   **Productieorder**
-   **Kanban** 

De parameters worden gebruikt om te bepalen hoe ver het systeem automatisch moet gaan bij de uitgaande werkverwerking. Een wavesjabloon wordt geselecteerd op basis van de volgorde en criteria van het wavesjabloon die zijn opgegeven in het sjabloon. Als een sjabloon bovenaan de volgorde staat, worden de criteria in die sjabloon eerst gecontroleerd. Als aan de criteria kan worden voldaan, wordt de wavesjabloon verwerkt. Anders worden de criteria in het volgende sjabloon gecontroleerd, enzovoort. Daarom is het een goed idee om het sjabloon met de meest specifieke criteria bovenaan de wavesjabloonvolgordelijst te zetten, zodat het eerst wordt verwerkt. U wilt bijvoorbeeld al het werk voor een specifieke vervoerder vandaag verwerken en de verwerking van het werk voor andere voor vervoerders tijdelijk vertragen. In dit geval moet de wavesjabloon die het werk voor die vervoerder selecteert hoger in de volgorde worden weergegeven dan andere sjablonen. Anders wordt het werk voor andere vervoerders mogelijk verwerkt voordat het werk voor die vervoerder is voltooid. 

U moet de waveprocesmethoden in elk wavesjabloon opgeven. Welke methoden beschikbaar zijn, is afhankelijk van het wavesjabloontype.

### <a name="work-templates"></a>Werksjablonen

Werksjabloondefinities spelen een belangrijke rol bij de definitie van werkprocessen voor magazijnbeheer. Ze bepalen welk werk wordt uitgevoerd en hoe het werk wordt uitgevoerd. De sjablonen kunnen ook een richtlijncode bevatten die verwijst naar een locatierichtlijn om te bepalen waar het werk wordt uitgevoerd. Werksjablonen bevatten een query die de criteria voor het werk opgeeft. Elk sjabloon moet ten minste één ophaalbewerking en één neerzetbewerking opnemen om de basis werkbewerking voor het overboeken van voorhanden voorraad van de ene naar de andere locatie te sturen. 

Als meerdere werknemers werk moeten kunnen verwerken voor enkele van uw magazijnbewerkingen, kunt u het concept van *fasering* gebruiken voor de voorraad en de werkuitvoering opdelen in verschillende het werkklassen.

### <a name="work-pools"></a>Werkgroepen

Werkgroepen worden gebruikt om werk in groepen te organiseren. U kunt bijvoorbeeld, een werkpool maken om werk te classificeren dat zich in een bepaalde magazijnlocatie voordoet. Voor alle werktypen, behalve tellen, kunt u een werkgroep toewijzen aan een werksjabloon. Voor cyclustelling kunt u een werkgroep toewijzen op de volgende pagina's:

-   Cyclustelplannen
-   Drempels voor cyclustelling
-   Cyclustellingswerk volgens locatie
-   Cyclustellingswerk volgens artikel

Wanneer u werksjablonen gebruikt om werk te maken, wordt de werkpool automatisch toegewezen aan het werk. 

Werkgroep-id's kunnen ook worden gebruikt om het type werk dat wordt toegewezen aan een bepaalde magazijnwerknemer, te beperken, mits deze functionaliteit is geconfigureerd in het menu-item van het mobiele apparaat.

### <a name="location-directives"></a>Instructielocatie

Zoals de naam al zegt, worden de locatierichtlijnen gebruikt om de werktransacties naar de juiste locaties in het magazijn te sturen. Hiermee wordt dus bepaald waar het verzamelen en wegzetten wordt uitgevoerd. 

Om het gemakkelijker en sneller te maken om de acties te definiëren die zijn gekoppeld aan elke regel van de locatierichtlijn, gebruikt u een van de vooraf gedefinieerde strategieën. U kunt bijvoorbeeld de strategie **Lege locatie met geen inkomend werk** gebruiken om te zoeken naar vrije locaties in een magazijn, of u kunt de strategie **FEFO-batchreservering** gebruiken voor uitgaande verkoopverzameling.

## <a name="additional-resources"></a>Aanvullende resources

[Locaties in een WMS-magazijn configureren](tasks/configure-locations-wms-enabled-warehouse.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
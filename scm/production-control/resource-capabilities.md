---
title: Bronmogelijkheden
description: Dit artikel bevat informatie over resourcemogelijkheden. Een capaciteit (mogelijkheid) is het vermogen van een bron voor bedrijfsactiviteiten om een bepaalde activiteit uit te voeren. In het artikel wordt beschreven hoe mogelijkheden en gerelateerde concepten, zoals vaardigheidsniveau en prioriteit, worden gebruikt om de juiste resources voor een activiteit te selecteren.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4463ca8e11115eb83323716faa4ed6b38937a3e4
ms.lasthandoff: 03/31/2017


---

# <a name="resource-capabilities"></a>Bronmogelijkheden

Dit artikel bevat informatie over resourcemogelijkheden. Een capaciteit (mogelijkheid) is het vermogen van een bron voor bedrijfsactiviteiten om een bepaalde activiteit uit te voeren. In het artikel wordt beschreven hoe mogelijkheden en gerelateerde concepten, zoals vaardigheidsniveau en prioriteit, worden gebruikt om de juiste resources voor een activiteit te selecteren.

Een capaciteit is de mogelijkheid van een bron voor bedrijfsactiviteiten om een bepaalde activiteit uit te voeren. Aan een bron voor bedrijfsactiviteiten kunnen meerdere mogelijkheden worden toegewezen en een mogelijkheid kan aan meerdere bronnen worden toegewezen. U kunt capaciteiten tijdelijk toewijzen aan bronnen door een begindatum en een vervaldatum te definiëren voor de toewijzing van de capaciteit. Wanneer de capaciteit voor een bron verloopt, kan de bron niet worden gepland voor een project of een productie waarvoor die capaciteit is vereist. Een capaciteit die is verlopen, kan worden vernieuwd. U kunt capaciteiten verwijderen, mits deze zich niet in een routerelatie bevinden of deel uitmaken van een productieroute of een actieve productieorder. Wees over het algemeen voorzichtig bij het verwijderen van capaciteiten. Overweeg om in plaats daarvan de vervaldatum aan te passen voor de bronnen die de capaciteit hebben. Capaciteiten kunnen aan allerlei soorten bronnen worden toegewezen: hulpmiddel, leverancier, machine, locatie, faciliteit of human resource.

## <a name="level"></a>Niveau
Meerdere bronnen hebben dezelfde functionele mogelijkheid hebben maar op verschillende vaardigheidsniveaus (bijvoorbeeld, sterkte, verwerkingssnelheid, of nauwkeurigheid). Daarom kunt u, als u een capaciteit aan een resource toewijst, een waarde **Niveau** opgeven. Het niveau is een eenvoudige numerieke waarde. Als u opgeeft dat een mogelijkheid een bronbehoefte voor een productieroute is, kunt u ook een waarde voor **Benodigd minimumniveau** voor die mogelijkheid opgeven. De planningsengine selecteert vervolgens alleen resources die de vereiste capaciteit hebben op een niveau dat gelijk is aan of hoger is dan het minimumniveau dat in de bronbehoefte is opgegeven.

## <a name="priority"></a>Prioriteit
De bronnen voor bedrijfsactiviteiten die hebben dezelfde mogelijkheden hebben kunnen een prioriteit worden toegewezen. Klik, als meerdere resources capaciteiten die voldoen aan de planningsbehoeften op het vereiste niveau hebben en vrije capaciteit, de planningsengine kunt kiezen uit deze bronnen. Als **prioriteit** is geselecteerd in de **selectie van primaire resource** op de **planning parameters** pagina, de resource met de hoogste prioriteit (de laagste numerieke waarde in de **prioriteit** veld) is geselecteerd tijdens het plannen van eerste.

## <a name="resource-requirements"></a>Resourcevereisten
Wanneer u bronbehoeften definieert voor een productieroute, kunt u een of meer capaciteiten als behoeften opgeven. Tijdens productieplanning worden de capaciteiten die zijn gedefinieerd in de bronvereisten in de routebewerking, vergeleken met de capaciteiten die zijn gedefinieerd voor de bronnen. Bronnen met de capaciteiten die voldoen aan de behoeften, worden geselecteerd. Als meerdere resources dezelfde functionele mogelijkheden maar andere vaardigheden (zoals kracht, verwerkingssnelheid of nauwkeurigheid) hebben, kunt u meerdere capaciteiten definiëren of het capaciteitsniveau gebruiken om het vermogen van de bron te kwalificeren. Dit is een voorbeeld:

-   In een route is de verwerkingstijd voor boren ingesteld op 10 eenheden, maar de behoefte zelf is gedefinieerd als Boren.
-   U hebt twee machines voor inzoomen, M1 en M2.
-   De boorcapaciteit is toegewezen aan beide bronnen, de machines M1 en de machine M2.
-   De machine M1 kan 2 eenheden per uur boren en de machine M2 kan 11 eenheden per uur boren.

In dit voorbeeld kunnen beide machines worden geselecteerd door de planningsengine omdat beide voldoen aan de basiscapaciteitsvereiste (boren). De machine M1 kan echter slechts twee eenheden per uur boren. Omdat dit tarief veel lager is dan de 10 eenheden per uur die zijn opgegeven voor de route, leidt de M1-machine tot productieproblemen als deze wordt geselecteerd. Er zijn twee manieren om dit probleem op te lossen en ervoor te zorgen dat in plaats daarvan de machine M2 wordt geselecteerd:

-   Maak twee afzonderlijke capaciteiten: Boren op lage snelheid en Boren op hoge snelheid. Definieer boren met lage snelheid als boren met een boorprocestijd van 1 tot 9 eenheden per uur. Definieer boren met hoge snelheid als boren met een boorprocestijd van 10 tot 19 eenheden per uur. Wijs vervolgens machine M1 de trage boren mogelijkheid, en machine M2 de capaciteit van de snelle boren toewijzen. Ten slotte wijzigen in de vereiste resource mogelijkheid op de route Boren op hoge snelheid. De planningsengine zal in dat geval de juiste machine (M2) selecteren.
-   Gebruik het capaciteitsniveau om de capaciteit 'Boren' te kwalificeren die aan de boringsmachines is toegewezen. Opgeven of de machine M1 de mogelijkheid Boren op een niveau van 2.0 heeft en dat de machine M2 de mogelijkheid boren heeft op een niveau van 11.0. Vervolgens kunt u opgeven dat 10.0 is het minimale niveau dat is vereist voor het boren mogelijkheid met betrekking tot de route. De planningsengine bepaalt vervolgens dat alleen machine M2 voldoet aan de bronbehoeften.

## <a name="competencies-for-human-resources"></a>Competenties voor human resources
Als u bronnen voor bedrijfsactiviteiten van het type **Human resources** hebt die aan werknemers in Human resources zijn gekoppeld, kunt u uit de competenties van werknemers ook voordeel halen wanneer u de bronbehoeften voor een productieroute definieert. Met andere woorden, kunt u ook vereisten voor specifieke vaardigheden, cursussen, certificaten of functies opgeven. De planningsengine kan vervolgens resources selecteren die aan werknemers worden gekoppeld, en de selectie wordt gebaseerd op de competenties van die werknemers. De competenties worden ingesteld in Human resources, niet op de pagina **Bronmogelijkheden**. Wanneer u vaardigheden, cursussen, certificaten of functies als bronbehoeften definieert, moet u de HRM-functionaliteit gebruiken en koppelt elke bron van de **Human resources** type aan een bijbehorende werknemer. Als u de HRM-functionaliteit niet gebruikt, u kunt capaciteiten definiëren op het **Bronmogelijkheden** pagina die lijken op of een kopie van de competenties van Human resources. De pagina **Bronmogelijkheden** bevat echter niet de functionaliteit die vereist is om vaardigheden, cursussen, certificeringen of functies te onderhouden.



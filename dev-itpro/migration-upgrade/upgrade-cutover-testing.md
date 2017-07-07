---
title: Testen van de upgrade-cutover
description: In dit onderwerp wordt uitgelegd hoe u de taken test die plaatsvinden nadat u AX 2012 hebt uitgeschakeld, maar voordat u Dynamics 365 for Finance and Operations, Enterprise edition, inschakelt.
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: nl-nl
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Testen van de upgrade-cutover

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Cutover* is de term die wordt gebruikt voor het uiteindelijke proces om een nieuw systeem live te krijgen. Dit cutover-proces bestaat uit de taken die plaatsvinden nadat Microsoft Dynamics AX 2012 is uitgeschakeld, maar voordat u Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, inschakelt. Het doel van het testen van de upgrade-cutover is om het cutover-proces te oefenen, zodat alles soepel verloopt voor iedereen die betrokken is bij de werkelijke cutover voor het live gaan.

Er zijn twee belangrijke werkstromen tijdens een cutover:

- **Technische werkstroom**: deze workstream omvat de procedure voor uitvoering van de gegevensupgrade. Uw bedrijf legt een limiet op voor de toegestane lengte van de uitvaltijd. Tijdens deze uitvaltijd zijn AX 2012 en Finance and Operations beide niet beschikbaar. Deze werkstroom moet mogelijk de procedure voor gegevensupgrade tunen, zodat u kunt voldoen aan downtime-limiet van het bedrijf.
- **Functionele werkstroom**: deze werkstroom omvat de configuratietaken die worden uitgevoerd nadat de gegevensupgrade is voltooid. Al deze taken moeten worden gedocumenteerd en gekwantificeerd en een resource moet worden toegewezen, omdat de functionele werkstroom en de technische werkstroom beide binnen de voorgeschreven downtime-limiet moeten passen.

In de volgende afbeelding ziet u het volledige cutover-proces om live te gaan, zoals dit wordt uitgevoerd in een productieomgeving.

![Cutover-proces](./media/cutover_1.png)

Dit cutover-proces verschilt op de volgende punten van een eenvoudige gegevensupgrade in de sandbox-omgeving:

- De AX 2012-database wordt niet gekopieerd, maar er wordt alleen een back-up van gemaakt, waarna de oorspronkelijke database wordt gewijzigd. Deze benadering werkt sneller en de back-up biedt mogelijkheid voor een rollback, als dit vereist is.
- Omdat de productieomgeving voor Finance and Operations toegangsbeperkingen kent, worden de taken die eerder zijn uitgevoerd op het sandbox-exemplaar van Application Object Server (AOS) nu uitgevoerd door het Microsoft DSE-team. Deze taken omvatten het downloaden en importeren van het bacpac-bestand en het uitvoeren van het pakket MajorversionDataUpgrade.zip.
- We hebben de volgende taken toegevoegd:

    - Voer een 'smoke test' uit.
    - Taken voor instellen van de toepassing uitvoeren. Dit kan een omvangrijke stap zijn, afhankelijk van de gebruikte functionaliteit. Tijdens deze stap configureert het functionele team nieuwe functionaliteit in de toepassing, zodat dit kan worden gebruikt in het bijgewerkte systeem.
    - Gebruikers weer toegang geven. Waarschuw de gebruikers dat de upgrade is voltooid en dat ze het systeem weer kunnen gebruiken.

## <a name="technical-workstream"></a>Technische werkstroom

Bij de technische werkstroom zijn verschillende leden van het technische team betrokken: de databasebeheerder (DBA), de AX 2012-systeembeheerder, serverbeheerders en ontwikkelaars die vertrouwd zijn met AX 2012 en Finance and Operations. In dit onderwerp wordt uitgelegd welke rollen betrokken zijn bij welke taken.

Tijdens het cutover-testen is het technische team gericht op het testen van prestaties en betrouwbaarheid van de gegevensupgrade, om ervoor te zorgen dat deze voldoet aan de downtime-limiet van het bedrijf. Bij dit proces zijn veel elementen van hardware en software betrokken. Sommige van deze elementen bevinden zich op locatie, terwijl anderen zich in de Microsoft-cloud bevinden. Daarnaast zijn er veel elementen van aangepaste toepassingscode en standaardcode betrokken. Het resultaat van deze tests moet zijn dat men vertrouwen heeft in het cutover-proces voor uw omgeving.

### <a name="turn-off-the-ax-2012-aos-instances"></a>De AX 2012 AOS-exemplaren uitschakelen

Bij deze taak zijn de AX 2012-systeembeheerder en de serverbeheerders betrokken.

De volgende gebieden moeten worden gevalideerd:

- **Batchtaken die worden uitgevoerd op het moment van cutover**: een langlopende batchtaak die al is gestart voor uitvoering voorkomt dat het systeem kan worden afgestopt. Plan dit vooruit, zodat u de AOS-exemplaren op het gewenste moment kunt stoppen. U moet wellicht batches zo plannen dat ze zijn voltooid voordat u AX 2012 uitschakelt.
- **Geïntegreerde systemen**: u hebt mogelijk andere systemen die zijn geïntegreerd in de AX 2012-omgeving. U moet rekening houden met deze systemen in uw plan voor het uitschakelen van AX 2012. U moet de geïntegreerde systemen misschien uitschakelen enige tijd voordat u AX 2012 zelf uitschakelt, zodat eventuele resterende lopende transacties kunnen worden afgerond. De vereisten voor geïntegreerde systemen lopen van bedrijf tot bedrijf aanzienlijk uiteen. Uw team van experts moet daarom voor dit scenario afzonderlijk plannen opstellen.

### <a name="create-a-backup-of-the-ax-2012-database"></a>Maak een back-up van de AX 2012-database.

Bij deze taak is de DBA betrokken. De back-up wordt gebruikt als een rollback vereist is. Hij wordt ook gebruikt als referentiepunt die gedurende enige tijd wordt bewaard en de status van het systeem weergeeft op het moment dat de cutover plaatsvond.

De volgende gebieden moeten worden gevalideerd:

- Verkrijg een concreet tijdsverloop voor het back-upproces.
- Pas de gebruikte back-upopties aan, zoals gecomprimeerd of niet-gecomprimeer, zodat u de back-up binnen zo kort mogelijke tijd kunt afronden.

### <a name="export-the-database-to-bacpac"></a>De database exporteren naar bacpac

Bij deze taak is de DBA betrokken. De uitvoer van deze taak is het exportbestand dat voor het nieuwe systeem worden geüpload naar Microsoft Azure.

De volgende gebieden moeten worden gevalideerd:

- Verkrijg een concreet tijdsverloop voor het back-upproces.
- Optimaliseer het exportproces om de snelst mogelijke ervaring te garanderen. Voor optimalisatie moeten mogelijk de volgende taken worden uitgevoerd:

    - Meten van systeembronnen tijdens de export, zoals CPU, schijf-i/o en geheugen.
    - Als u resourceproblemen vindt, stelt u een plan op om deze op te vangen. Meestal lost u deze problemen op door meer van de vereiste bronnen in te zetten.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Het bacpac-bestand uploaden naar Azure-opslag

Bij deze taak is de DBA of de serverbeheerder betrokken. Het Bacpac-bestand wordt tijdens deze taak verplaatst naar Azure.

De volgende gebieden moeten worden gevalideerd:

- Selecteer de machine die wordt gebruikt voor de upload en zorg ervoor dat de tool Azure Storage explorere is geconfigureerd en klaar voor gebruik.
- Verkrijg een concreet tijdsverloop voor het uploadproces door dit meerdere keren te meten. De uploadtijden variëren, afhankelijk van de snelheid van uw internetverbinding en de geografische locatie van het Azure-datacenter ten opzichte van uw locatie.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>Het bacpac-bestand downloaden en importeren in de Azure SQL-database

Wanneer deze taak tijdens de go-live plaatsvindt, wordt hij uitgevoerd door het Microsoft DSE-team. Tijdens de cutover-test is hierbij echter de DBA betrokken. Het resultaat van deze taak is het exportbestand dat voor het nieuwe systeem worden geüpload naar Azure.

De volgende gebieden moeten worden gevalideerd:

- Verkrijg een concreet tijdsverloop voor het importproces.
- Optimaliseer het exportproces om de snelst mogelijke ervaring te garanderen. Voor optimalisatie moeten mogelijk de volgende taken worden uitgevoerd:

    - Meet de beschikbare systeembronnen tijdens de export. Hieronder vindt u enkele voorbeelden:

        - **Op de AOS-computer:** CPU, schijf-i/o en geheugen
        - **Op het Azure SQL Database-exemplaar:** doorvoer van SQL Database (DTU). U kunt de DTU in Azure SQL in de gaten houden vanuit Microsoft SQL Server Management Studio op het AOS-systeem in de systeemweergave sys.dm_resource_stats.

    - Als u resourceproblemen vindt, stelt u een plan op om deze op te vangen. Meestal lost u deze problemen op door meer van de vereiste bronnen in te zetten. Omdat deze computer wordt gehost door Microsoft, moet u een aanvraag indienen bij Microsoft voor het vergroten van resources als u merkt dat deze een knelpunt kunnen vormen.

### <a name="run-the-majorversiondataupgradezip-package"></a>Het pakket MajorVersionDataUpgrade.zip uitvoeren

Wanneer deze taak tijdens de go-live plaatsvindt, wordt hij uitgevoerd door het Microsoft DSE-team. Tijdens de cutover-test zijn hierbij echter de ontwikkelaars betrokken. Tijdens deze taak wordt de oude databasestructuur omgezet naar de structuur van het nieuwe systeem.

Het databasesynchronisatieproces wordt uitgevoerd als onderdeel van deze taak. Databasesynchronisatie kan aanzienlijke tijd duren in sommige situaties, zoals wanneer een gegroepeerde index op een tabel is gewijzigd, omdat deze bewerking in SQL veel resources vraagt.

Het wordt sterk aangeraden om eerst uw proces voor analyse en foutopsporing uit te voeren in een ontwikkelomgeving. In de sandboxomgeving zijn de opties voor foutopsporing en analyse meer beperkt. De bedoeling van de cutover-test is dat er weinig of geen problemen overblijven die moeten worden opgelost bij de werkelijke cutover.

De volgende gebieden moeten worden gevalideerd:

- Verkrijg een concreet tijdsverloop voor het importproces.
- Optimaliseer het proces om de snelst mogelijke ervaring te garanderen. Voor optimalisatie moeten mogelijk de volgende taken worden uitgevoerd:

    - De prestaties van afzonderlijke upgradescripts monitoren via de tabel ReleaseUpdateScriptsExecution.
    - Scripts aanpassen om prestaties te optimaliseren. Deze taak vereist mogelijk dat u de X++-code van een script aanpast om deze te optimaliseren voor uw gegevensset.
    - Azure SQL DTU monitoren door middel van Microsoft Dynamics Lifecycle Services monitoring of de weergave sys.dm_resources_stats systeem in Management Studio. Als de resources maximaal worden gebruikt, moet u wellicht een hoger databaseniveau aanvragen bij Microsoft DSE-team.

### <a name="roll-back-to-ax-2012"></a>Terugdraaien naar AX 2012

Het doel van deze taak is om de database te herstellen met behulp van de back-up die is gemaakt toen AX 2012 werd uitgeschakeld, en daarna AX 2012 weer in te schakelen. De toestand van geïntegreerde systemen moet wellicht ook worden hersteld. Omdat elk bedrijf weer werkt met andere geïntegreerde systemen, moet u dit scenario afzonderlijk plannen op basis van uw specifieke situatie. Hoewel het onwaarschijnlijk is dat u de upgrade moet terugdraaien, is het belangrijk dat u een geteste procedure hebt voor het geval dat er iets misloopt.

## <a name="functional-workstream"></a>Functionele werkstroom

Nadat de gegevensupgrade moeten diverse configuratietaken worden uitgevoerd in de nieuwe omgeving. Het doel van deze werkstroom is om alle configuratietaken te documenteren en te kwantificeren en een resource toe te wijzen aan elke taak, om te garanderen dat deze taken samen met de technische workstream kunnen worden uitgevoerd gedurende het downtime-venster.

Functionele taken omvatten meestal het wijzigen van de waarden van bepaalde systeemparameters of andere configuratiegegevens. Deze taken worden geïdentificeerd in de volledige functionele testdoorloop, wat losstaat van het cutover-testen. Wanneer een taak van dit type wordt geïdentificeerd, moet deze worden geëvalueerd samen met de functionele resource en uw ontwikkelaar.

Grotere veranderingen kunnen inhouden dat een nieuw aangepaste script voor gegevensupgrade wordt geschreven om de gegevens bij te werken tijdens de gegevensupgrade. De functionele resource kan echter handmatig kleinere wijzigingen uitvoeren via het nieuwe systeem na de gegevensupgrade.

Grotere veranderingen waarvoor nieuwe gegevensupgradescripts worden opgesteld, moeten worden getest. Dit houdt in dat u het pakket MajorVersionDataUpgrade.zip enkele keren zult moeten herhalen. Het is belangrijk dat u de kosten van het hernieuwd uitvoeren van het pakket afweegt tegen de kosten van het handmatig invoeren van gegevens.

Voor elke handmatige wijziging moet een taak worden toegevoegd aan het document met het cutover-plan. Deze taak moet de volgende gegevens bevatten:

-   Wat de taak is en wat er moet gebeuren.
-   Wie de taak uitvoert.
-   Hoe lang de taak duurt.


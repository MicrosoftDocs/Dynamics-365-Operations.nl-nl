---
title: Wavetoewijzing
description: In dit onderwerp wordt beschreven hoe u de stap voor wavetoewijzing instelt, inclusief hoe u parallelle verwerking hiervoor inschakelt.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: feee33a7d4ea3f0d9c4d671210293a28aac14f61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823162"
---
# <a name="wave-allocation"></a>Wavetoewijzing

[!include [banner](../includes/banner.md)]

Waveverwerking kan tijdrovend zijn en het grootste deel van de verwerkingstijd wordt besteed aan de toewijzingsstap en aan de stap voor het maken van werk.

Het is nu mogelijk om elk van deze stappen parallel uit te voeren, wat de prestaties van de waveverwerking kan verbeteren en een grotere doorvoer van waves in hetzelfde magazijn mogelijk kan maken. In dit onderwerp wordt uitgelegd hoe u wavetoewijzingsmethode instelt zodat deze parallel wordt uitgevoerd. Zie [Het maken van werk tijdens wave plannen](configure-wave-schedule-work-creation.md) voor meer informatie over hoe het maken van werk parallel kan worden uitgevoerd.

Voorheen kon slechts één wave tegelijk in een magazijn worden toegewezen. Deze beperking is verwijderd en vervangen door een nieuwe beperking die alleen het artikel en de dimensies boven de locatie in de reserveringshiërarchie vergrendelt. Afmetingen boven de locatie bevatten altijd productafmetingen. Als een artikel bijvoorbeeld is geconfigureerd met *Kleur*, kunnen varianten voor *Rood*, *Blauw* en *Geel* elk parallel worden verwerkt.

Dit betekent dat als hetzelfde artikel met dezelfde dimensies boven de locatie door één wave wordt toegewezen, andere waves moeten wachten om een vergrendeling van hetzelfde artikel en dezelfde dimensies te verkrijgen. Als de vergrendeling niet tijdig kan worden verkregen, treedt er een fout op en mislukt de waveverwerking.

Als u parallelle verwerking wilt gebruiken, moet de wave in batch worden uitgevoerd.

## <a name="performance-improvements"></a>Prestatieverbeteringen

De prestatievoordelen van parallelle verwerking vallen uiteen in twee categorieën:

- **Verbeterde doorvoer**: de doorvoer van waves zal doorgaans verbeteren, zelfs als parallelle verwerking niet is geconfigureerd, vooral voor scenario's waarbij er geen overlapping van artikelen binnen de waves is.
- **Verbetering van de toewijzing voor een enkele wave**: testen op klantgegevens heeft een prestatieverbetering van bijna 50% laten zien na overschakeling op parallelle toewijzing. De parallelle verwerking wordt uitgevoerd op artikelen en dimensies boven de locatie, dus de verbeteringen zijn afhankelijk van het aantal verschillende artikelen dat een wave bevat, de beschikbare infrastructuur en de duur van de toewijzing versus de duur van de werkcreatie.

## <a name="configure-parallel-allocation"></a>Parallelle toewijzing configureren

### <a name="warehouse-management-parameters"></a>Parameters voor magazijnbeheer

Als u parallelle toewijzingsverwerking wilt gebruiken, gaat u naar **Magazijnbeheer > Instellen > Parameters voor magazijnbeheer**, opent u het tabblad **Waveverwerking** en maakt u de volgende instellingen:

- **Batchgroep voor waveverwerking**: selecteer de batchgroep die bij de eerste verwerking van de waves moet worden gebruikt. De daaropvolgende verwerking van toewijzing kan worden uitgevoerd met behulp van verschillende batchgroepen.
- **Waves in batch verwerken**: stel dit in op *Ja* om parallelle verwerking te gebruiken.
- **Wachten op vergrendeling (ms)**: voer de tijd, uitgedrukt in milliseconden, in die een toewijzingsstap moet wachten op een systeemresource die door een andere toewijzingsstap wordt vergrendeld. Nadat deze tijd is verstreken, wordt de golf niet verwerkt en wordt er een foutbericht weergegeven. We raden u aan ten minste een paar seconden toe te staan om de toewijzing van één logische eenheid te voltooien.

Zie [Magazijnparameters voor golfverwerking](wave-warehouse-parameters.md) voor informatie over deze en andere opties voor waveverwerking op de pagina **Parameters voor magazijnbeheer**.

## <a name="wave-process-methods"></a>Methoden voor verwerking van waves

Parallelle verwerking instellen:

1. Ga naar **Magazijnbeheer > Instellen > Waves > Methoden voor verwerking van waves**.
1. Selecteer de methode `allocateWave` in het raster.
1. Selecteer **Taakconfiguratie** in het actievenster.
1. De pagina **Taakconfiguratie van de wave-postmethode** wordt geopend. Dit raster biedt een overzicht van elk magazijn waar u de methode `allocateWave` hebt geconfigureerd. Parallelle verwerking wordt alleen gebruikt voor magazijnen die worden vermeld. Gebruik de knoppen in het actievenster om indien nodig magazijnen aan het raster toe te voegen of te verwijderen. 
1. Maak voor elk magazijn de volgende instellingen:
    - **Maximumaantal batchtaken**: geef het aantal batchtaken op dat moet worden gebruikt voor de toewijzing voor het geselecteerde magazijn. Het optimale aantal batchtaken is afhankelijk van de beschikbare infrastructuur en welke andere batchtaken op de server worden verwerkt. Tests uitgevoerd op een omgeving met vier kernen die was gereserveerd voor waveverwerking toonden aan dat het gebruik van acht taken goede resultaten opleverde.
    - **Batchgroep voor waveverwerking**: specifieke batchgroepen kunnen worden gebruikt voor verschillende magazijnen om de toewijzingsverwerking per magazijn te kunnen uitschalen.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Parallellisatie tussen alle rechtspersonen in- of uitschakelen

We raden u aan de methode `allocateWave` parallel in te stellen voor alle rechtspersonen, omdat dit helpt om de prestaties van de waveverwerking te verbeteren. Vanaf Supply Chain Management versie 10.0.17 is de functie *Wave-parallelisatie voor methode Wave toewijzen* standaard ingeschakeld voor alle nieuwe en bijgewerkte installaties en kan deze niet opnieuw worden uitgeschakeld. Nadat u deze functie hebt inschakeld, treedt het volgende op:

- De methode `allocateWave` wordt bijgewerkt met een taakconfiguratie-instelling waarmee u de pagina **Wave-procesmethoden** kunt gebruiken om het aantal taken te definiëren dat tegelijkertijd wordt uitgevoerd, equivalent aan het aantal parallelle processen. Als gevolg hiervan wordt de tijd die wordt gebruikt voor de stap voor wavetoewijzing (die meestal 30% tot 60% van de totale verwerkingstijd bedraagt) verminderd met een factor die ongeveer gelijk is aan het aantal taken. Het is ook mogelijk om te selecteren welke batch wordt toegewezen om deze taken te verwerken. Het is belangrijk op te merken dat al uw rechtspersonen worden geconfigureerd om waves in batch te verwerken. Voor de magazijnen die al zijn geconfigureerd om waves in batch te verwerken en voor de magazijnen die al zijn geconfigureerd om de methode `allocateWave` parallel te gebruiken, wordt de bestaande configuratie bewaard.
- Standaard worden alle nieuwe rechtspersonen geconfigureerd om waves in batch te verwerken. Voor alle nieuwe magazijnen waarop de optie **Magazijnbeheerprocessen** is ingeschakeld, is de methode `allocateWave` geconfigureerd om standaard parallel te worden uitgevoerd.
- Op de pagina **Parameters voor magazijnbeheer** is **Waves verwerken in batch** ingesteld op *Ja* en **Wacht op vergrendeling (ms)** op een standaardoptie van 15 seconden. Dit betekent dat alle waves in batch worden uitgevoerd. Wanneer een wave wordt uitgevoerd, moeten het artikel en de afmetingen boven de locatie in de toewijzingsstap worden vergrendeld. Wanneer een andere taak voor waveverwerking dezelfde vergrendeling probeert te verkrijgen voor de identieke record, wordt deze geblokkeerd totdat het huidige proces is voltooid. Met de instellingen **Wachten op vergrendeling (ms)** wordt de maximale tijd vastgesteld waarop het systeem wacht voordat de vergrendeling wordt losgelaten.

Voor parallelle toewijzingsverwerking moet de waveverwerking in batch worden uitgevoerd. Daarom vermindert u uw waveverwerkingsprestaties als u de instelling **Waves verwerken in batch** uitschakelt, vooral als waveverwerking een parallel proces gebruikt zoals gedefinieerd door de taakconfiguratie voor de relevante wavemethoden.

Indien nodig kunt u elk van de standaard gemaakte instellingen ongedaan maken wanneer de functie *Wave-parallelisatie voor methode Wave toewijzen* automatisch is ingeschakeld voor uw exemplaar. Hiervoor gaat u als volgt te werk:

- Ga naar **Magazijnbeheer \> Instellen \> Parameters voor magazijnbeheer**. Pas op het tabblad **Golfverwerking** de gewenste waarden toe voor **Waves verwerken in batch** en **Wachten op vergrendeling (ms)**.
- Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**. Selecteer de methode `allocateWave`. Selecteer **Taakconfiguratie** in het actievenster om een pagina te openen met een overzicht van elk magazijn waar de methode parallel moet worden uitgevoerd. Wijzig of verwijder het aantal batchtaken en de toegewezen wavegroep voor elk vermeld magazijn indien nodig.

## <a name="troubleshooting"></a>Problemen oplossen

### <a name="troubleshoot-using-the-infolog"></a>Problemen oplossen met het infologboek

Omdat het batchframework wordt gebruikt, worden fouten die optreden tijdens de waveverwerking vastgelegd als onderdeel van de infologboeken voor batchtaken. Ga als volgt te werk om de batchtaken met betrekking tot een wave te lezen:

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave die u wilt inspecteren.
1. Open in het actievenster het tabblad **Wave** en selecteer in de groep **Wave** de optie **Batchtaken**.

Waveverwerking is zelfcorrigerend, dus elke fout die tijdens de verwerking wordt gedetecteerd, moet worden gemeld met behulp van het infologboek.

Een typische fout met betrekking tot parallelle verwerking kan zijn dat twee waves tegelijkertijd hetzelfde artikel proberen toe te wijzen en één niet voltooit, zodat de andere wave niet in staat is om binnen de opgegeven tijd een vergrendeling te verkrijgen. Als deze situatie zich voordoet, bevat het logboek voor batchtaken informatie waarin staat dat de vergrendeling voor het artikel niet kan worden verkregen, in welk geval de wave die is mislukt opnieuw moet worden verwerkt.

Omdat de verwerking parallel plaatsvindt, moeten gegevens in verschillende tabellen worden bijgehouden om de status van de verwerking bij te houden. Dit betekent dat de logboeken voor de batchtaken fouten kunnen bevatten, zoals fouten door dubbele sleutels.

De fouten uit de batchtaken maken ook deel uit van het logboek voor batchtaken. De belangrijkste informatie bevindt zich meestal onderaan.

In zeldzame gevallen, bijvoorbeeld als de SQL-verbinding is beëindigd, is het mogelijk dat de waveverwerking eindigt in een inconsistente status waarin de batchverwerking lijkt te worden uitgevoerd, maar de verwerking wordt gestopt. De wave kan dit soort fouten niet aan, dus vindt een poging om mislukte waves op te ruimen plaats wanneer de volgende wave wordt uitgevoerd. Als de huidige wave zich in een inconsistente toestand bevindt, voert u de volgende stappen uit:

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave die u moet opschonen.
1. Open in het actievenster het tabblad **Wave** en selecteer in de groep **Wave** de optie **Wavegegevens opschonen**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Problemen oplossen met het voortgangslogboek van de wave

Als de optie **Voortgangslogboek voor waves maken** is ingeschakeld op de pagina **Parameters voor magazijnbeheer**, wordt elke keer dat de toewijzing voor een artikel en de bijbehorende dimensies begint en eindigt, een logboekrecord gemaakt. U moet dit logboek alleen inschakelen wanneer u het nodig hebt, bijvoorbeeld tijdens de eerste tests of voor het oplossen van problemen. Wanneer deze optie is ingeschakeld, kunt u het logboek bekijken door de volgende stappen uit te voeren:

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer de wave die u wilt inspecteren.
1. Open in het actievenster het tabblad **Wave** en selecteer in de groep **Wave** de optie **Voortgang**.

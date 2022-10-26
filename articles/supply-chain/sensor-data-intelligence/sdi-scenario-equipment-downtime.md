---
title: Het scenario machinestatus
description: In dit artikel wordt het scenario machinestatus beschreven, waarmee u sensorgegevens kunt gebruiken om de beschikbaarheid van uw apparatuur te controleren.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 30fdfb898384aea4c1f8cb2f36f9e104cd316f90
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689634"
---
# <a name="the-machine-status-scenario"></a>Het scenario machinestatus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

In dit artikel wordt het scenario *machinestatus* beschreven, waarmee u sensorgegevens kunt gebruiken om de beschikbaarheid van uw apparatuur te controleren. Als u een sensor instelt om een signaal te verzenden wanneer een productietaak op een machine uitvoer produceert maar binnen een opgegeven interval geen sensorsignaal wordt ontvangen, wordt een melding weergegeven op het dashboard van de supervisor.

## <a name="scenario-dependencies"></a>Afhankelijkheden voor dit scenario

Het scenario *machinestatus* heeft de volgende afhankelijkheden:

- Een melding kan alleen worden geactiveerd als een productietaak wordt uitgevoerd op een toegewezen machine.
- Er moet een signaal voor een *onderdeel uit* naar de IoT-hub worden verzonden.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Demogegevens voorbereiden voor het scenario machinestatus

Als u een demonstratiesysteem wilt gebruiken om het scenario *machinestatus* te testen, gebruikt u een systeem waarop de [demonstratiegegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd, selecteert u de rechtspersoon *USMF* (bedrijf) en bereidt u de aanvullende demonstratiegegevens voor, zoals wordt beschreven in deze sectie. U kunt deze sectie overslaan als u uw eigen sensoren en gegevens gebruikt.

### <a name="set-up-a-sensor-simulator"></a>Een sensorsimulator instellen

Als u dit scenario wilt uitproberen zonder een fysieke sensor te gebruiken, kunt u een simulator instellen om de vereiste signalen te genereren. Meer informatie over dit onderwerp vindt u in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Controleren of resource 3118 wordt gebruikt voor product P0111

Een productieorder wordt gepland en vrijgegeven. Daarom wordt een productietaak vrijgegeven voor resource *3118* (*Foam cutting machine*). Volg deze stappen om te controleren of resource *3118* wordt gebruikt voor product *P0111* in uw demonstratiegegevens.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer het product waarvan het veld **Artikelnummer** is ingesteld op *P0111*.
1. Selecteer in het actievenster op het tabblad **Technicus** in de groep **Weergave** de optie **Route**.
1. Selecteer op de pagina **Route**, op het tabblad **Overzicht** onderaan de pagina, de regel waarop het veld **Bewerkingsnr.** is ingesteld op *30*.
1. Ga naar het tabblad **Resourcevereisten** onderaan de pagina en controleer of dat resource *3118* (*Foam cutting machine*) is gekoppeld aan de bewerking.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Een productieorder voor het product P0111 maken en deze vrijgeven

Volg deze stappen om een productieorder voor product *P0111* te maken en vrij te geven.

1. Ga naar **Productiebeheer \> Productieorders \> Alle productieorders**.
1. Ga naar de pagina **Alle productieorders** en selecteer in het actievenster de optie **Nieuwe batchorder**.
1. Stel in het dialoogvenster **Batch maken** de volgende waarden in:

    - **Artikelnummer:** *P0111*
    - **Hoeveelheid:** *10*

1. Selecteer **Maken** om de order te maken en terug te keren naar de pagina **Alle productieorders**.
1. Gebruik het veld **Filter** om te zoeken naar productieorders waarbij het veld **Artikelnummer** is ingesteld op *P0111*. Zoek en selecteer vervolgens de productieorder die u zojuist hebt gemaakt.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Raming**.
1. Selecteer in het dialoogvenster **Raming** **OK** om de raming uit te voeren.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Vrijgave**.
1. Noteer het nummer van de batchorder die u hebt gemaakt, die u ziet in het dialoogvenster **Vrijgave**.
1. Selecteer **OK** om de order vrij te geven.

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>De uitvoeringsinterface voor de werkvloer configureren

U gebruikt de interface voor de uitvoering van de productievloer om de taak te starten die in de vorige sectie is gepland en vrijgegeven voor artikelnummer *P0111*. Volg deze stappen om de uitvoeringsinterface voor de werkvloer te configureren.

1. Ga naar **Productiebeheer \> Productie-uitvoering \> Uitvoering werkvloer**.
1. Als u de interface nog niet eerder hebt ingesteld, wordt een aanmeldingspagina geopend. Voer uw referenties in.
1. Selecteer op de welkomstpagina **Configureren** om de wizard **Apparaat configureren** te starten.
1. Selecteer op de pagina **Apparaat configureren - stap 1 - Configuratie selecteren** de configuratie *Standaard*.
1. Selecteer **Volgende**.
1. Stel op de pagina **Apparaat configureren - stap 2 - Het gebied voor de productievloer definiëren** het veld **Resource** in op *3118*.
1. Selecteer **OK**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>De zoekoptie inschakelen voor de uitvoeringsinterface voor de werkvloer

U kunt de productietaak voor de productieorder die eerder is vrijgegeven gemakkelijker vinden door de volgende stappen uit te voeren, om de zoekoptie in de interface voor het uitvoeren van de werkvloer in te schakelen.

1. Ga naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Uitvoering werkvloer configureren**.
1. Selecteer de configuratie *Standaard*.
1. Selecteer **Bewerken** in het actievenster.
1. Stel op het sneltabblad **Algemeen** de optie **Zoeken inschakelen** in op *Ja*.
1. Sluit de pagina.

### <a name="start-the-first-job-in-the-batch-order"></a>De eerste taak in de batchorder starten

Volg deze stappen om de taak te starten die is gepland voor resource *3118*.

1. Ga naar **Productiebeheer \> Productie-uitvoering \> Uitvoering werkvloer**.
1. Typ **123** in het veld *Badge-ID*. Selecteer vervolgens **Aanmelden**.
1. Als u wordt gevraagd om een reden voor afwezigheid, selecteert u een van de kaarten voor afwezigheid en selecteert u vervolgens **OK**.
1. Voer in het veld **Zoeken** het batchordernummer in dat u eerder hebt genoteerd. Selecteer vervolgens de toets **Terug**.
1. Selecteer de order en selecteer **Taak beginnen**.
1. Selecteer in het dialoogvenster **Taak beginnen** de knop **Starten**.

## <a name="set-up-the-machine-status-scenario"></a>Het scenario machinestatus instellen

Volg deze stappen om het scenario *machinestatus* in te stellen Supply Chain Management.

1. Ga naar **Productiebeheer \> Instellingen \> Sensor Data Intelligence \> Scenario's**.
1. Selecteer in het vak van het scenario **machinestatus** de optie **Configureren** om de configuratiewizard voor dit scenario te openen.
1. Selecteer op de pagina **Sensoren** de optie **Nieuw** om een sensor toe te voegen aan het raster. Stel er daarna de volgende velden voor in:

    - **Sensor-ID**: voer de id in van de sensor die u gebruikt Als u de Raspberry Pi Azure IoT Online Simulator gebruikt en deze hebt ingesteld zoals beschreven in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md), voer dan *Machinestatus* op.
    - **Beschrijving van de sensor**: voer een beschrijving van de sensor in.

1. Herhaal nu de vorige stap voor elke extra sensor die u wilt toevoegen. U kunt later op elk moment terug komen en meer sensoren toevoegen.
1. Selecteer **Volgende**.
1. Selecteer op de pagina **Toewijzing van bedrijfsrecord** in de sectie **Sensoren** de record voor een van de sensoren die u zojuist hebt toegevoegd.
1. Selecteer in het gedeelte **Toewijzing van bedrijfsrecord** de optie **Nieuw** om een rij aan het raster toe te voegen.
1. Stel in de nieuwe rij het veld **Bedrijfsrecord** in op de resource die u wilt bewaken met de geselecteerde sensor. Als u gebruik maakt van de demogegevens die u eerder in dit artikel hebt gemaakt, stelt u dit veld in op *3118, Foam cutting machine*.
1. Selecteer **Volgende**.
1. Definieer op de pagina **Drempel machinestatus** hoe lang het systeem na het laatste signaal *onderdeel uit* een machinestatusmelding moet verzenden. Er zijn twee manieren om de drempelwaarde te definiëren:

    - **Standaarddrempel (minuten)**: stel dit veld in om de standaarddrempel te definiëren. De waarde geldt vervolgens voor alle resources waarbij het veld **Drempel om niet-reagerende machine te bepalen (minuten)** is ingesteld op twee minuten of minder. De minimumwaarde is *2* (minuten).
    - **Drempel om niet-reagerende machine te bepalen (minuten)**: voer in dit veld een overschrijvingswaarde in voor elke resource in het raster waar u niet de standaarddrempelwaarde voor wilt gebruiken. Resources die zijn ingesteld op een drempel van twee minuten of minder gebruiken in plaats daarvan de **Standaarddrempel ( minuten)**.

    > [!NOTE]
    > Normaal gesproken gebruikt u een *onderdeel uit*-signaal om de machinestatus te controleren. Controleer daarom of de drempel voor elke machineresource langer is dan de machine nodig heeft om een onderdeel te produceren.

1. Selecteer **Volgende**.
1. Selecteer op de pagina **Sensors activeren** in het raster de sensor die u toegevoegd hebt en selecteer vervolgens **Activeren**. Voor elke geactiveerde sensor in het raster wordt een vinkje weergegeven in de kolom **Actief**.
1. Selecteer **Voltooien**.

## <a name="work-with-the-machine-status-scenario"></a>Werken met het scenario machinestatus

Nadat u de sensoren hebt geïnstalleerd en het scenario hebt geconfigureerd, kunt u gebeurtenissen voor machinestatus bekijken in Supply Chain Management. In deze sectie wordt beschreven waar en hoe u deze informatie kunt weergeven.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Gegevens voor machinestatus weergeven op de pagina Resourcestatus

Op de pagina **Resourcestatus** kunnen supervisors een tijdlijn controleren van het *onderdeel uit*-signaal dat wordt ontvangen van de sensoren die zijn toegekend aan elke machineresource. Volg deze stappen om de tijdlijn te configureren:

1. Ga naar **Productiebeheer \> Productieregistratie \> Resourcestatus**.
1. Stel in het dialoogvenster **Configureren** de volgende velden in:

    - **Resource**: selecteer de resources die u wilt bewaken. Als u met de demonstratiegegevens werkt, selecteert u *3118*.
    - **Tijdreeks 1**: selecteer de record (metrische sleutel) met de volgende notatie voor de naam: *MachineReportingStatus:&lt;Sensor&gt;*
    - **Weergavenaam**: voer hier *Onderdeel uit-signaal* in.

In de volgende afbeelding ziet u een voorbeeld van gegevens over de machinestatus op de pagina **Resourcestatus** tijdens normaal bedrijf.

![Gegevens voor machinestatus op de pagina Resourcestatus tijdens normaal bedrijf.](media/sdi-resource-status-downtime-up.png "Gegevens voor machinestatus op de pagina Resourcestatus tijdens normaal bedrijf")

In de volgende afbeelding ziet u een voorbeeld van gegevens over de machinestatus wanneer uitvaltijd wordt gedetecteerd.

![Gegevens voor de machinestatus op de pagina Resourcestatus wanneer uitvaltijd is gedetecteerd.](media/sdi-resource-status-downtime-down.png "Gegevens voor de machinestatus op de pagina Resourcestatus wanneer uitvaltijd is gedetecteerd")

### <a name="view-machine-status-on-the-notifications-page"></a>De machinestatus weergeven op de pagina Meldingen

Op de pagina **Meldingen** kunnen supervisors de meldingen weergeven die worden gegenereerd wanneer er te veel tijd is verstreken sinds de sensor voor de laatste keer een *onderdeel uit*-signaal heeft geleverd. Elke melding geeft een overzicht van de productietaak die wordt beïnvloed door de uitval en geeft de optie om de beïnvloede taak opnieuw toe te kennen aan een andere resource.

Om de pagina **Meldingen** te openen, gaat u naar **Productiebeheer \> Query's en rapporten \> Sensor Data Intelligence \> Meldingen**.

In de volgende afbeelding ziet u een voorbeeld van een melding voor machinestatus.

![Voorbeeld van een melding voor machinestatus.](media/sdi-resource-status-downtime-notification.png "Voorbeeld van een melding voor machinestatus")

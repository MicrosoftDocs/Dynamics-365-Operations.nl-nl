---
title: Het scenario activumonderhoud
description: In dit artikel wordt het scenario activumonderhoud beschreven, waarmee u deze gegevens kunt gebruiken om tellerrecords te maken die het gebruik van een machineactivum bijhouden.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ff3944b987314a688a5829b05f8627479e3e79ed
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428303"
---
# <a name="the-asset-maintenance-scenario"></a>Het scenario activumonderhoud

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

In het scenario *activumonderhoud* kunt u sensorgegevens gebruiken om tellerrecords te maken. Tellerrecords volgen het gebruik van machineactiva en worden gebruikt als invoer om het onderhoudsschema voor machineactiva te genereren.

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Demogegevens voorbereiden voor het scenario activumonderhoud

Als u een demonstratiesysteem wilt gebruiken om het scenario *activumonderhoud* te testen, gebruikt u een systeem waarop de [demonstratiegegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd, selecteert u de rechtspersoon *USMF* (bedrijf) en bereidt u de aanvullende demonstratiegegevens voor, zoals wordt beschreven in deze sectie. U kunt deze sectie overslaan als u uw eigen sensoren en gegevens gebruikt.

In deze sectie stelt u het activum *AK-101, Air knife* in de demogegevens in als voorbeeld. U ziet dan hoe het aanstaande onderhoudswerk kan worden voorspeld op basis van sensorsignalen om het aantal uren te meten dat het luchtmes heeft gewerkt. U stelt ook een onderhoudsplan op waarin het luchtmes om de 10.000 uur moet worden onderhouden.

### <a name="set-up-a-sensor-simulator"></a>Een sensorsimulator instellen

Als u dit scenario wilt uitproberen zonder een fysieke sensor te gebruiken, kunt u een simulator instellen om de vereiste signalen te genereren. Meer informatie over dit onderwerp vindt u in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Een activumteller maken om productie-uren bij te houden

Volg deze stappen om een activumteller te maken om productie-uren bij te houden.

1. Ga naar **Activabeheer \> Instellingen \> Activatypen \> Tellers**.
1. Selecteer in het actievenster **Nieuw** om een teller te maken.
1. Stel in de koptekst de volgende waarden in:

    - **Teller:** *ProductieUur*
    - **Naam:** *Productie-uren*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Eenheid:** *uur*
    - **Bijwerken:** *Handmatig*
    - **Totaal samengevoegd:** *Som*

1. Selecteer op het sneltabblad **Activumtypen** de optie **Regel toevoegen**.
1. Stel op de nieuwe regel het veld **Activumtypen** in op *Air knife*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Een onderhoudsplan maken voor het activum

Volg deze stappen om een onderhoudsplan te maken voor het activum.

1. Ga naar **Activabeheer \> Instellingen \> Preventief onderhoud \> Onderhoudsplan**.
1. Selecteer in het actievenster **Nieuw** om een onderhoudsplan te maken.
1. Stel in de koptekst de volgende waarden in:

    - **Onderhoudsplan:** *Luchtmes*
    - **Naam:** *Plan voor luchtmessen*

1. Stel op het sneltabblad **Details** de volgende waarden in:

    - **Plandatum:** selecteer de datum van vandaag.
    - **Actief:** *Ja*

1. Ga naar het sneltabblad **Regels** en selecteer **Regel voor activumteller toevoegen** om een regel toe te voegen aan het raster. Stel vervolgens de volgende waarden in:

    - **Werkorderomschrijving:** *Onderhoud voor luchtmessen*
    - **Onderhoudstaaktype:** *Preventief*
    - **Intervaltype:** *Herhaald vanaf laatste werkorder*
    - **Periodefrequentie:** *10000*
    - **Teller:** *ProductieUur*

## <a name="set-up-the-asset-maintenance-scenario"></a>Het scenario activumonderhoud instellen

Volg deze stappen om het scenario *activumonderhoud* in te stellen Supply Chain Management.

1. Ga naar **Activumbeheer \> Instellingen \> Sensor Data Intelligence \> Scenario's**.
1. Selecteer in het vak van het scenario **activumonderhoud** de optie **Configureren** om de configuratiewizard voor dit scenario te openen.
1. Selecteer op de pagina **Sensoren** de optie **Nieuw** om een sensor toe te voegen aan het raster. Stel er daarna de volgende velden voor in:

    - **Sensor-ID**: voer de id in van de sensor die u gebruikt Als u de Raspberry Pi Azure IoT Online Simulator gebruikt en deze hebt ingesteld zoals beschreven in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md), voer dan *Activumonderhoud* op.
    - **Beschrijving van de sensor**: voer een beschrijving van de sensor in.

1. Herhaal nu de vorige stap voor elke extra sensor die u wilt toevoegen. U kunt later op elk moment terug komen en meer sensoren toevoegen.
1. Selecteer **Volgende**.
1. Selecteer op de pagina **Toewijzing van bedrijfsrecord** in de sectie **Sensoren** de record voor een van de sensoren die u zojuist hebt toegevoegd.
1. Selecteer in het gedeelte **Toewijzing van bedrijfsrecord** de optie **Nieuw** om een rij aan het raster toe te voegen.
1. In de nieuwe rij moet het veld **Type bedrijfsrecord** automatisch zijn ingesteld op *Assets(EntAssetObjectTable)*. Stel het veld **Bedrijfsrecord** in op de resource die u wilt bewaken met de geselecteerde sensor. Als u gebruik maakt van de demogegevens die u eerder in dit artikel hebt gemaakt, stelt u dit in op *AK-101, AK-101 luchtmes voor regel 1*.
1. Direct nadat u een type bedrijfsrecord hebt geselecteerd voor de rij die u in de vorige stap hebt toegevoegd, wordt automatisch een tweede rij aan het raster toegevoegd. In deze rij moet het veld **Type bedrijfsrecord** zijn ingesteld op *Tellers(EntAssetCounterType)*. Stel het veld **Bedrijfsrecord** in op de activumteller die u wilt bijwerken aan de hand van signalen van de geselecteerde sensor. Als u gebruik maakt van de demogegevens die u eerder in dit artikel hebt gemaakt, stelt u dit in op *ProductieUur, Productie-uren*.
1. Selecteer **Volgende**.
1. Selecteer op de pagina **Sensors activeren** in het raster de sensor die u toegevoegd hebt en selecteer vervolgens **Activeren**. Voor elke geactiveerde sensor in het raster wordt een vinkje weergegeven in de kolom **Actief**.
1. Selecteer **Voltooien**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Werken met het scenario activumonderhoud

### <a name="view-counter-values"></a>De tellerwaarde weergeven

Nadat de gegevens zijn voorbereid en het scenario *activumonderhoud* is geconfigureerd en geactiveerd, kunt u zien hoe records voor een activumteller worden ingevoegd op basis van deze gegevens.

1. Ga naar **Activabeheer \> Activa \> Alle activa**.
1. Zoek en selecteer het activum dat u wilt controleren. Als u gebruik maakt van de demogegevens die u eerder in dit artikel hebt gemaakt, selecteert u *AK-101*.
1. Selecteer in het actievenster op het tabblad **Activum** in de groep **Preventief** de optie **Tellers** om de pagina voor tellerrecords te openen voor het activum *AK-101*.

### <a name="generate-maintenance-work-orders"></a>Onderhoudswerkorders genereren

Nadat u het scenario *activumonderhoud* hebt ingeschakeld en het onderhoudsplan hebt ingesteld, kunt u het onderhoudsschema uitvoeren om onderhoudswerkorders te genereren. Zie voor meer informatie over hoe u werkt met preventie onderhoud het onderwerp [Overzicht van preventief onderhoud](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).

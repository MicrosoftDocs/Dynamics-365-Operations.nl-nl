---
title: Een gesimuleerde sensor instellen voor tests
description: In dit artikel wordt beschreven hoe u een simulator kunt instellen om Sensor Data Intelligence te testen, zonder fysieke sensoren te installeren.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc8bd020a53214abab28ec51ffc6d6be74979932
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643971"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Een gesimuleerde sensor instellen voor tests

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Als u Sensor Data Intelligence wilt testen zonder fysieke sensoren te installeren, kunt u door middel van de service *Raspberry PI Azure IoT Online Simulator* sensorsignalen emuleren en deze zenden naar uw IoT-oplossing op Microsoft Azure. Meer informatie over de simulator vindt u in [Raspberry Pi online simulator verbinden met Azure IoT-hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Video-instructies

De volgende video laat zien hoe u een gesimuleerde sensor kunt instellen voor testen. De resterende secties in dit artikel bieden dezelfde instructies in tekstvorm.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Een apparaat maken in de Azure IoT-hub

U moet eerst een apparaat configureren om de sensorsignalen naar de Azure IoT-hub te verifiëren.

1. Ga in Azure naar de lijst met resources voor de resourcegroep die u hebt gemaakt voor gebruik met Sensor Data Intelligence. Meer informatie over dit onderwerp vindt u in [Een IoT-oplossing implementeren op Azure](sdi-deploy-iot-solution-on-azure.md).
1. Zoek in de resourcelijst de record waar het veld **Type** is ingesteld op *IoT-hub*. Selecteer in de kolom **Naam** de naam om de pagina met gegevens van de bron te openen.
1. Selecteer **Apparaten** in het navigatievenster aan de linkerkant.
1. Selecteer op de pagina **Apparaten** de optie **Apparaat toevoegen**.
1. Stel op de pagina **Een apparaat maken** de volgende velden in:

    - **Apparaat-ID**: voer een naam in voor het nieuwe apparaat (bijvoorbeeld *Mijn IoT-apparaat*).
    - **Verificatietype**: selecteer *Symmetrische sleutels*.
    - **Sleutels automatisch genereren**: schakel dit selectievakje in.
    - **Dit apparaat verbinden met een IoT-hub**: selecteer *inschakelen*.

1. Selecteer **Opslaan** om naar de pagina **Apparaten** terug te gaan.
1. Zoek het nieuwe apparaat in de lijst. Selecteer in de kolom **Apparaat-ID** de naam om de pagina met gegevens van de het apparaat te openen. Als het nieuwe apparaat niet in de lijst wordt weergegeven, vernieuwt u de pagina.
1. Kopieer de waarde in het veld **Primaire verbindingsreeks** (bijvoorbeeld door te klikken op de knop **Kopiëren naar klembord**). U hebt deze waarde later nodig wanneer u de Raspberry Pi IoT-simulator instelt om de sensorsignalen te kunnen emuleren. U kunt het daarom nu even in een tekstbestand plakken.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>De Azure-verbindingsreeks toevoegen aan de Raspberry Pi IoT-simulator

Volg deze stappen om de verbindingsreeks van het apparaat in de Azure IoT-hub toe te voegen aan het script in de Raspberry-service.

1. Open de [Raspberry Pi IoT-simulator](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Zoek in het code-editorvenster de regel met de volgende opdracht.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Vervang de helptekst, inclusief de haakjes, door de waarde van de **Primaire verbindingsreeks** die u in de vorige sectie hebt gekopieerd. Het resultaat moet lijken op het volgende voorbeeld.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Sensor-id's en -waarden toevoegen aan de nettolading in de Raspberry Pi IoT-simulator

U moet nu de Raspberry Pi IoT-simulator configureren met gesimuleerde sensoren en de waarden die deze als nettoladingen zullen verzenden.

- Zoek in de code-editor van de Raspberry Pi IoT-simulator de `getMessage`-functie en bewerk deze zodat deze overeenkomt met de volgende code. (De sensoren worden ingesteld in de `cb()`-regels.)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > De sensor-ID's die zijn gedefinieerd in de code-editor voor de Raspberry Pi IoT-simulator moeten identiek zijn aan de sensor-ID's die u later specificeert voor de scenario's in Supply Chain Management. In de voorgaande voorbeeldcode worden sensor-ID's gebruikt die leesbaar zijn voor mensen. In een reëel scenario zijn de sensor-ID's echter GUID-waarden (Globally Unique Identifiers) die door de fabrikant worden geleverd. De door mensen leesbare sensor-ID's die in deze voorbeeldcode worden gebruikt, worden ook gebruikt in de voorbeelden in [Het scenario productkwaliteit](sdi-scenario-product-quality.md), [Het scenario activumonderhoud](sdi-scenario-asset-maintenance.md), [Het scenario productievertragingen](sdi-scenario-production-delays.md) en [Het scenario machinestatus](sdi-scenario-equipment-downtime.md). Gebruik deze code daarom als u ook die scenario's wilt uitvoeren.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Het interval voor het verzenden van sensorsignalen bewerken

U moet nu het interval instellen waarmee de berichten van de Raspberry Pi IoT-simulator de geëmuleerde sensorsignalering moeten verzenden.

1. Zoek de volgende functieaanroep in de code-editor van de Raspberry Pi IoT-simulator.

    `setInterval(sendMessage, 2000);`

2. Standaard verzendt de Raspberry Pi IoT-simulator elke 2000 milliseconden (2 seconden) een sensorsignaal. U kunt deze waarde naar wens aanpassen.

## <a name="run-the-raspberry-pi-iot-simulator"></a>De Raspberry Pi IoT-simulator uitvoeren

- Selecteer **Uitvoeren** om de simulator te starten en te beginnen met het verzenden van gesimuleerde sensorgegevens.

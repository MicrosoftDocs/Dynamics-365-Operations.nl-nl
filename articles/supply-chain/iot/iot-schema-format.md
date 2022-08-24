---
title: Schema-indelingen voor berichten van IoT-hub
description: In dit artikel wordt uitgelegd hoe u een berichtschema moet ontwerpen dat u in IoT-intelligentie kunt gebruiken.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6d133d520ce0a1dccb2575e352f63e6ceb2bd3f
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228627"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Schema-indelingen voor berichten van IoT-hub

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

In dit artikel wordt uitgelegd hoe u een berichtschema moet ontwerpen dat u in IoT-intelligentie kunt gebruiken.

## <a name="message-requirements"></a>Berichtvereisten

De volgende regels zijn van toepassing op het controleren van berichten in IoT-intelligence:

+ Berichtschema's moeten de JSON-indeling (JavaScript Object Notation) hebben.
+ Een UNIX-**tijdstempel** eigenschap, waarbij de waarde wordt uitgedrukt in milliseconden (ms), moet aanwezig zijn in het bericht van de Microsoft Azure IoT-hub.
+ Een bericht wordt alleen bijgehouden als het alle eigenschappen bevat die in de scenario-instellingen zijn gedefinieerd. Als u bijvoorbeeld de eigenschappen **id**, **tijdstempel** en **waarde** definieert, wordt het volgende bericht gecontroleerd.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Dit bericht wordt niet gecontroleerd omdat de eigenschap **waarde** ontbreekt.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT-Intelligentie negeert eigenschappen in het bericht die niet in de scenarioconfiguratie zijn gedefinieerd. Als u bijvoorbeeld de eigenschappen **id**, **tijdstempel** en **waarde** definieert, controleert IoT-intelligentie alle volgende berichten.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT-intelligentie negeert berichten die niet overeenkomen met de criteria voor de scenarioconfiguratie.
+ U kunt meerdere typen berichtschema's definiëren en gebruiken.
+ Niet elk type berichtschema hoeft te worden gedefinieerd. Alleen schema's die worden gebruikt voor de IoT-intelligentiescenario's moeten worden gedefinieerd.

## <a name="id-value-pair-schema"></a>Schema van het id-waardepaar

Een id-waardepaar is een algemeen patroon voor berichtschema's voor IoT-intelligence. Door een id-waardepaar te gebruiken zorgt u ervoor dat uw berichtschema in alle scenario's hetzelfde is. Hier wordt bijvoorbeeld een bericht weergegeven voor het scenario **Apparatuuruitvaltijd** of het scenario **Productievertragingen**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Hier wordt een bericht weergegeven voor het scenario **Productkwaliteit**.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Beide voorgaande berichten bevatten de eigenschappen **id** en **waarde**. De **id**-waarden kunnen tijdens het instellen van een scenario in de tabel **Waarden voor signaalgegevens** worden toegewezen. Voor het scenario **Apparatuuruitval** wijst u de waarde **IoTInt.Machine1225.PartOut** toe. Voor het scenario **Productkwaliteit** wijst u de waarde **IoTInt.Machine1225.Temperature** toe.

Zie [Documentatie voor Azure IoT-hub](/azure/iot-hub/) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
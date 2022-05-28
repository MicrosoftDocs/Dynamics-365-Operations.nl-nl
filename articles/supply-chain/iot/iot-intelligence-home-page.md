---
title: Startpagina van IoT-intelligentie
description: Dit onderwerp bevat koppelingen naar informatie over IoT-intelligentie.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2386d71fde8196304fde846cbff4cd45d1edc834
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674416"
---
# <a name="iot-intelligence-home-page"></a>Startpagina van IoT-intelligentie

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Deze functie is momenteel alleen beschikbaar in de volgende landen en regio's:
>
> - VS (Verenigde Staten van Amerika)
> - EU (Europese Unie)
> - AU (Australië)
> - CA (Canada)
> - VK (Verenigd Koninkrijk)

IoT-intelligentie is een invoegvoeging voor Microsoft Dynamics 365 Supply Chain Management. Met de invoegtoepassing worden IoT-signalen (Internet of Things) geïntegreerd met gegevens in Supply Chain Management om bruikbare inzichten te krijgen.

IoT ondersteunt de volgende scenario's:

- **Productievertragingen**: in dit scenario wordt de werkelijke cyclusduur vergeleken met de geplande cyclusduur. Supply Chain Management stelt u op de hoogte wanneer de productie niet op schema ligt, zodat u kunt ingrijpen om de operationele efficiëntie te maximaliseren en ordervertragingen te voorkomen.
- **Apparatuuruitval**: in dit scenario wordt de gemeten uptime vergeleken met door de gebruiker gedefinieerde parameters. Supply Chain Management stelt u op de hoogte wanneer een drempel voor uitval wordt overschreden, zodat u actie kunt ondernemen en bijvoorbeeld een productiewerkorder opnieuw kunt plannen of een onderhoudswerkorder kunt maken.
- **Productkwaliteit:**: in dit scenario worden sensormetingen, zoals vocht en temperatuur, vergeleken met door de gebruiker gedefinieerde kwaliteitsmetingen. Supply Chain Management stelt u op de hoogte wanneer zich een afwijking voordoet, zodat u kunt ingrijpen om de kwaliteitsstandaarden te behouden en verlies te minimaliseren.

De onderstaande afbeelding toont de interactie tussen Azure IoT-hub, IoT-intelligentie en Supply Chain Management.

![IoT-hub, IoT-intelligentie en Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Tracering en onderhoud

- [Scenario's controleren in Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Een scenario uitschakelen](iot-scenario-setup.md#disable-a-scenario)
- [Een actief IoT-intelligentie-scenario wijzigen](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Simulatieopties](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
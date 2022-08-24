---
title: IoT-intelligentie controleren en beheren
description: In dit artikel wordt uitgelegd hoe u IoT-intelligentie kunt controleren en beheren.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f1804e8b9cfa407f6549dc146df17338c4d51572
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228854"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT-intelligentie controleren en beheren

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

In dit artikel wordt uitgelegd hoe u IoT-intelligentie kunt controleren en beheren.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Controlescenario's in Microsoft Dynamics 365 Supply Chain Management

U kunt de IoT-intelligentie-verwerking vanaf verschillende locaties controleren:

+ **Modules \> Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Meldingen** – De lijst met niet-opgeloste meldingen weergeven.
+ **Modules \> Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Afgesloten meldingen** – De lijst bekijken met meldingen die zijn opgelost of afgewezen.
+ **Modules \> Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Metrische sleutels** – Bekijk de metrische sleutels voor de tijdreeksdiagrammen **Resourcestatus**.
+ **Modules \> Productiebeheer \> Productieregistratie \> Resource status** – Houd specifieke metrische gegevens bij met behulp van het dialoogvenster **Configureren**. Als een scenario een uitzondering detecteert, worden de details van de uitzondering weergegeven in een melding.
+ **Werkgebieden \> Productiebeheer \> Meldingen** – Bekijk de lijst met niet-opgeloste meldingen.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Een actief IoT-intelligentie-scenario wijzigen

Wanneer een scenario wordt uitgevoerd, kunt u de volgende wijzigingen aanbrengen:

+ Voeg nieuwe definities voor sensorschema's toe.
+ Selecteer nieuwe waarden voor signaalgegevens.
+ Annuleer de selectie van bestaande waarden voor signaalgegevens.
+ Voeg nieuwe waarden voor signaalgegevens toe en wijs deze toe.
+ Werk drempelwaarden bij.

Wanneer een scenario wordt uitgevoerd, zijn de volgende wijzigingen niet toegestaan:

+ Schemadefinities die momenteel worden gebruikt in een ingeschakeld scenario verwijderen of wijzigen.
+ De geselecteerde schemapaden voor het ingeschakelde scenario wijzigen.

## <a name="simulation-options"></a>Simulatieopties

U kunt de signalen van fabrieksmachines simuleren. Voor meer informatie wordt verwezen naar deze artikelen.

+ [IoT DevKit AZ3166 verbinden met Azure IoT-hub](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi online simulator verbinden met Azure IoT-hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

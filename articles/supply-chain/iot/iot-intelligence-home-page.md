---
title: Startpagina van IoT-intelligentie
description: Dit onderwerp bevat koppelingen naar informatie over IoT-intelligentie.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782676"
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

+ **Productievertragingen**: in dit scenario wordt de werkelijke cyclusduur vergeleken met de geplande cyclusduur. Supply Chain Management stelt u op de hoogte wanneer de productie niet op schema ligt, zodat u kunt ingrijpen om de operationele efficiëntie te maximaliseren en ordervertragingen te voorkomen.
+ **Apparatuuruitval**: in dit scenario wordt de gemeten uptime vergeleken met door de gebruiker gedefinieerde parameters. Supply Chain Management stelt u op de hoogte wanneer een drempel voor uitval wordt overschreden, zodat u actie kunt ondernemen en bijvoorbeeld een productiewerkorder opnieuw kunt plannen of een onderhoudswerkorder kunt maken.
+ **Productkwaliteit:**: in dit scenario worden sensormetingen, zoals vocht en temperatuur, vergeleken met door de gebruiker gedefinieerde kwaliteitsmetingen. Supply Chain Management stelt u op de hoogte wanneer zich een afwijking voordoet, zodat u kunt ingrijpen om de kwaliteitsstandaarden te behouden en verlies te minimaliseren.

De onderstaande afbeelding toont de interactie tussen Azure IoT-hub, IoT-intelligentie en Supply Chain Management.

![IoT-hub, IoT-intelligentie en Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Instelling

U kunt IoT-intelligentie instellen en configureren zonder code te schrijven. Hier volgen de basisstappen.

1. [Azure-bronnen instellen](iot-azure-setup.md): maak een IoT-hub, een Redis-cache en een sleutelkluis die toegankelijk is vanuit Supply Chain Management.
2. [Indelingen voor berichtschema's voor IoT-hub](iot-schema-format.md): configureer uw apparaten om berichten naar IoT-hub te verzenden en om de JSON-berichtenindeling (JavaScript Object Notation) te definiëren.
3. Schakel in Functiebeheer de functie IoT-intelligentie in. 
4. [Installeer de invoegtoepassing IoT-intelligentie in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md): installeer de invoegtoepassing in LCS en configureer de Azure-geheimen.
5. [Metrische gegevens instellen](iot-metrics-setup.md): stel metrische gegevens in Supply Chain Management in.
6. [Scenario-instellingen](iot-scenario-setup.md): stel de scenario's in Supply Chain Management in.

## <a name="tracking-and-maintenance"></a>Tracering en onderhoud

+ [Scenario's controleren in Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Een scenario uitschakelen](iot-scenario-setup.md#disable-a-scenario)
+ [De invoegtoepassing verwijderen](iot-lcs-setup.md#uninstall-addin)
+ [Een actief IoT-intelligentie-scenario wijzigen](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Simulatieopties](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
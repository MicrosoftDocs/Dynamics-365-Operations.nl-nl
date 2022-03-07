---
title: Metrische gegevens instellen voor IoT-intelligentie
description: In dit onderwerp wordt uitgelegd hoe u metrische gegeven voor IoT-intelligentie instelt.
author: robinarh
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f623e49422dfb238415ae450fd0ab354b68c38b
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651965"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>Metrische gegevens instellen voor IoT-intelligentie

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Metrische gegevens configureren

Als u de tijdreeksdiagrammen van uw berichten in Microsoft Dynamics 365 Supply Chain Management wilt weergeven, moet u de metrische gegevens instellen aan de hand van de volgende stappen.

1. Kopieer de verbindingsreeks voor de Redis-cache:

    1. Ga in de Azure-portal naar de Redis-cache.
    2. Ga naar **Instellingen** \> **Toegangssleutels**.
    3. Kopieer de waarde in het veld **Primaire verbindingsreeks**.

2. Ga in Supply Chain Management naar **Productiebeheer \> Instellingen \> IoT-intelligentie \> Scenarioparameters**.
3. Plak op de pagina **Scenarioparameters** op het tabblad **Tijdreeks** in het veld **Verbindingsreeks metrische Redis-opslag** de verbindingsreeks die u eerder hebt gekopieerd. Met deze stap kunnen de metrische gegevens van Azure IoT worden gevisualiseerd in Supply Chain Management. Wanneer u de waarde in het veld plakt, wordt deze weergegeven als **\*\*\*\*\*\***.

    > [!NOTE]
    > Telkens wanneer u een van de verbindingsreeks van de Redis-cache bijwerkt, moet u ook dit veld bijwerken.

4. Ga naar **Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Metrische sleutels**.
5. Selecteer **Bijwerken** op de pagina **Metrische sleutels**.
6. In het dialoogvenster **Metrische sleutels bijwerken** ziet u dat **Uitvoeren op de achtergrond** is geselecteerd in het veld. Selecteer **OK**.

Alle metrische sleutels in de Redis-cache worden opgehaald en toegevoegd aan de lijst **Metrische sleutels**. Metrische waarden worden pas weergegeven wanneer u [de scenario's hebt ingeschakeld](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>De tijdreeks voor resourcestatus configureren

Volg deze stappen om de tijdreeks **Resourcestatus** te configureren.

1. Ga in Supply Chain Management naar **Productiebeheer \>, Productieregistratie \> Resourcestatus**.
2. Selecteer op de pagina **Resourcestatus** de optie **Configureren**.
2. Selecteer in het dialoogvenster **Configureren** in de lijst **Resource** een artikel dat u wilt controleren.
3. Klik op de knop **Bewerken** voor **Tijdreeks 1**.
4. Selecteer in het dialoogvenster **Tijdreeks selecteren** metrische gegevens in het raster. (U kunt ook de koppeling **Metrische sleutels bijwerken** selecteren om de metrische sleutels vanuit dit dialoogvenster bij te werken.)
5. Selecteer **OK** om terug te gaan naar het dialoogvenster **Configureren**.
6. Voer een weergavenaam in.
7. Selecteer een tijdsbestek in het veld **Gegevens weergeven van**.
8. Selecteer **OK**.

Het diagram wordt weergegeven.

## <a name="delete-a-metric-key"></a>Een metrische sleutel verwijderen

1. Ga in Supply Chain Management naar **Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Metrische sleutels**.
2. Selecteer op de pagina **Metrische sleutels** de metrische sleutel die u wilt verwijderen.
3. Selecteer **Verwijderen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
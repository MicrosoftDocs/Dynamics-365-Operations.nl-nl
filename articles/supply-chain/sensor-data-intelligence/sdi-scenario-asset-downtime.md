---
title: Het scenario activumuitvaltijd
description: In dit artikel wordt het scenario activumuitvaltijd beschreven, waarmee u sensorgegevens kunt gebruiken om de beschikbaarheid van uw activa te controleren.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689424"
---
# <a name="the-asset-downtime-scenario"></a>Het scenario activumuitvaltijd

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

In het scenario activumuitvaltijd wordt een record voor uitvaltijd voor onderhoud gegenereerd, als geen signaal wordt ontvangen met een gedefinieerde tijdsdrempel na ontvangst van het laatste signaal. Het scenario vereist dat u uw machine uitrust met een sensor die periodiek een signaal verzendt naar uw Azure IoT-hub zolang de machine actief is, maar geen signaal verzendt wanneer de machine niet actief is.

## <a name="set-up-the-asset-downtime-scenario"></a>Het scenario activumuitvaltijd instellen

Volg deze stappen om het scenario *activumuitvaltijd* in te stellen Supply Chain Management.

1. Ga naar **Activumbeheer \> Instellingen \> Sensor Data Intelligence \> Scenario's** om de pagina **Scenario's** te openen.
2. Selecteer in het vak van het scenario **activumuitvaltijd** de optie **Configureren** om de configuratiewizard voor dit scenario te openen.
3. Selecteer op de pagina **Sensoren** de optie **Nieuw** om een sensor toe te voegen aan het raster. Stel er daarna de volgende velden voor in:

    - **Sensor-ID**: voer de id in van de sensor die u gebruikt Als u de Raspberry PI Azure IoT Online Simulator gebruikt en deze hebt ingesteld zoals beschreven in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md), voer dan *ActivumUitvaltijd* op.
    - **Beschrijving van de sensor**: voer een beschrijving van de sensor in.

4. Herhaal nu de vorige stap voor elke extra sensor die u wilt toevoegen. U kunt later op elk moment terug komen en meer sensoren toevoegen.
5. Selecteer **Volgende**.
6. Selecteer op de pagina **Toewijzing van bedrijfsrecord** in de sectie **Sensoren** de record voor een van de sensoren die u zojuist hebt toegevoegd.
7. Selecteer in het gedeelte **Toewijzing van bedrijfsrecord** de optie **Nieuw** om een rij aan het raster toe te voegen.
8. Stel in de nieuwe rij het veld **Bedrijfsrecord** in op de resource die u wilt bewaken met de geselecteerde sensor. Als u de demonstratiegegevens gebruikt, selecteert u *AK-101, Luchtmes* voor regel 1.
9. Selecteer **Volgende**.
10. Definieer op de pagina **Drempel activumuitvaltijd** hoe lang het systeem moet wachten voordat er een melding voor uitval van een activum wordt gegeven. Er zijn twee manieren om de drempelwaarde te definiëren:

    - **Standaarddrempel (minuten)**: stel dit veld in om de standaarddrempel te definiëren. Deze waarde geldt voor alle resources waarbij het veld **Meldingsdrempel (minuten)** is ingesteld op twee minuten of minder. De minimumwaarde is *2* (minuten).
    - **Drempel om niet-reagerende machine te bepalen (minuten)**: voer in dit veld een overschrijvingswaarde in voor elke resource in het raster waar u niet de standaarddrempelwaarde voor wilt gebruiken. Resources die zijn ingesteld op een drempel van twee minuten of minder gebruiken in plaats daarvan de **Standaarddrempel ( minuten)**.
11. Selecteer **Volgende**.
12. Selecteer op de pagina **Sensors activeren** in het raster de sensor die u geconfigureerd hebt en selecteer vervolgens **Activeren**. Voor elke geactiveerde sensor in het raster wordt een vinkje weergegeven in de kolom **Actief**.
13. Selecteer **Voltooien**.

## <a name="work-with-the-asset-downtime-scenario"></a>Werken met het scenario activumuitvaltijd

Als er geen sensorsignaal wordt ontvangen van een activum binnen de drempel die is gedefinieerd in de scenarioconfiguratie, wordt een record voor uitvaltijd voor onderhoud gemaakt voor dat activum. Managers moeten de uitvaltijdrecords regelmatig controleren (bijvoorbeeld één keer tijdens elke dienst) en de juiste redencodes en eindtijden toepassen voor elke uitvaltijdregistratie. Volg deze stappen om de records voor uitvaltijd voor onderhoud voor een activum te bekijken:

1. Ga naar **Activabeheer > Activa > Alle activa**.
2. Zoek en selecteer het activum dat u wilt controleren. Als u met de demonstratiegegevens werkt, selecteert u *AK-101*.
3. Open in het actievenster het tabblad **Activum**. Ga naar de groep **Werkorder** en selecteer **Uitvaltijd voor onderhoud** om de pagina met onderhoudsuitvaltijdsrecords voor het geselecteerde activum te openen.

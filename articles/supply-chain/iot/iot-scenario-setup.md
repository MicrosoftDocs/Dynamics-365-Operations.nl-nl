---
title: Scenario-instelling voor IoT-intelligentie
description: In dit onderwerp wordt uitgelegd hoe u scenario's configureert voor IoT-intelligentie in Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1deaa2130b63272da39a42315c6a1bc4b7ccb8a
ms.sourcegitcommit: 8adc65e26d78e229271eb427659a87ee5f371319
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814054"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Scenario-instelling voor IoT-intelligentie

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u scenario's configureert voor IoT-intelligentie in Microsoft Dynamics 365 Supply Chain Management. Voordat u de scenario's kunt instellen, moet u [Microsoft Dynamics Lifecycle Services (LCS) instellen](iot-lcs-setup.md).

In dit onderwerp configureert u het scenario **Apparatuuruitval** om een melding te genereren in Supply Chain Management wanneer een machine uitvalt. Het onderwerp laat ook zien hoe u het scenario **Productkwaliteit** zo kunt configureren dat er een melding wordt gegenereerd als een kenmerk van een artikel buiten een opgegeven bereik valt en hoe u het scenario **Productievertragingen** zo configureert dat er een melding wordt gegenereerd als de productiedoorvoer onder een drempelwaarde valt.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Het scenario Apparatuuruitval configureren in Supply Chain Management

Het scenario **Apparatuuruitval** wijst een **PartOut**-signaal toe aan een waarschuwingsdrempel voor een machine. De machine wordt alleen gecontroleerd als deze wordt geselecteerd voor het scenario en wordt ingesteld op **Uitvoering** in Supply Chain Management. Als de tijd sinds het laatst ontvangen **PartOut**-signaal voor de machine langer is dan de waarschuwingsdrempel, wordt er een melding **Machine uitgevallen** geactiveerd. Als de machine nog steeds actief is, wordt bij ontvangst van het volgende **PartOut**-signaal een melding **Machine actief** geactiveerd. Als een machine gedurende 30 minuten uitgeschakeld blijft, wordt er een nieuwe melding **Machine uitgevallen** geactiveerd.

Het scenario **Apparatuuruitval** heeft de volgende afhankelijkheden:

+ Er kan alleen een waarschuwing worden geactiveerd als een productieorder wordt uitgevoerd op een toegewezen machine.
+ Er moet een signaal dat overeenkomt met een **PartOut**-signaal voor een toegewezen machine met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.
+ Een Unix-eigenschap **tijdstempel**, waarbij de waarde wordt uitgedrukt in milliseconden (ms), moet aanwezig zijn in het Azure IoT Hub-bericht.

Volg deze stappen om het scenario te configureren.

1. Meld u aan bij Supply Chain Management.
2. Schakel de functievlag voor IoT-intelligentie in. Zie [Overzicht van functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) voor meer informatie.
3. Configureer de metrische gegevens. Zie [Metrische gegevens configureren](iot-metrics-setup.md#configure-metrics) voor meer informatie.
4. Ga naar **Productiebeheer \> Instellingen \> IoT-intelligentie- \> Scenariobeheer**.
6. Selecteer op de tegel **Apparatuuruitval** de optie **Configureren** om de configuratiewizard te openen.

   De eerste pagina in de wizard is de pagina **Schemadefinitie voor apparatuursensor**. Op deze pagina kunt u het schema instellen in Supply Chain Management, zodat dit overeenkomt met de JSON-indeling (JavaScript Object Notation) van de IoT Hub-berichten. Er kunnen meerdere berichtschema's worden gedefinieerd. Zie [Schema-indelingen voor IoT Hub-berichten](iot-schema-format.md) voor meer informatie. In dit voorbeeld bevat de berichtlading een batch berichten met de volgende indeling.

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Voeg een regel toe aan de tabel en stel de volgende waarden in:

    1. Stel het veld **Schemanaam** in op **Id**.
    2. Stel het veld **Schemapad** in op **/payload\[\*\]/id**.
    3. Stel het veld **Beschrijving** in op **Bericht-id**.

8. Voeg nog een regel toe aan de tabel en stel de volgende waarden in:

    1. Stel het veld **Schemanaam** in op **Timestamp**.
    2. Stel het veld **Schemapad** in op **/payload\[\*\]/timestamp**.
    3. Stel het veld **Beschrijving** in op **Tijdstempel bericht**.

9. Voeg nog een regel toe aan de tabel en stel de volgende waarden in:

    1. Stel het veld **Schemanaam** in op **Waarde**.
    2. Stel het veld **Schemapad** in op **/payload\[\*\]/value**.
    3. Stel het veld **Beschrijving** in op **Waarde bericht**.

    > [!NOTE]
    > U hoeft niet alle eigenschappen in het bericht te definiëren. Definieer alleen de eigenschappen die u nodig hebt. In de voorgaande stappen hebt u geen rij gemaakt voor **Basistijdstempel**. Het pad van **Basistijdstempel** zou **/timestamp** zijn.

10. Selecteer **Volgende** om naar de pagina **Schematoewijzing van apparatuursensor** te gaan.
11. Stel in de rij voor **Resource-id apparatuur** de **schemanaam** in op **Id**.
12. Stel in de rij voor **UTC-tijd** de **schemanaam** in op **Tijdstempel**.
13. Stel in de rij voor **Door onderdeel geproduceerd signaal** de **schemanaam** in op **Waarde**.
14. Selecteer **Volgende** om naar de pagina **Configuratie resource-id apparatuur** te gaan.
15. Volg deze stappen om de waarden in het IoT Hub-bericht toe te wijzen aan de resources van Supply Chain Management:

    1. Voeg in de tabel **Waarden voor signaalgegevens** een nieuwe rij toe. Voer in het veld **Waarde** de waarde **IoTInt.Machine1225.PartOut** in. Deze waarde is afkomstig van de JSON-eigenschap **id** in het IoT Hub-bericht.
    2. Selecteer **Opslaan**.
    3. Selecteer in de tabel **Toewijzing van zakelijke records** de optie **Nieuw**. Een se standaardwaarde voor het veld **Type zakelijke record** wordt automatisch ingevuld en u hoeft deze niet te wijzigen.
    4. Selecteer in het veld **Zakelijke record** de Supply Chain Management-machineresource van waaruit deze signaalwaarde wordt verzonden.
    5. Selecteer **Opslaan**.
    6. Herhaal deze stappen om een nieuwe zakelijke record toe te voegen voor **Machine1226**. U kunt meerdere waarden voor signaalgegevens toewijzen aan een enkele record in Supply Chain Management.

16. Gebruik de kolom **Geselecteerd** om te kiezen welke machines u wilt verwerken. U hoeft niet alle signaalwaarden te definiëren en u hoeft niet alle machines te selecteren.
17. Selecteer **Volgende** om naar de pagina **Configuratie van door onderdeel geproduceerd signaal** te gaan.
18. Voeg in de tabel **Waarden voor signaalgegevens** een rij toe en stel het veld **Waarde** in op **Waar**. Deze waarde is afkomstig van de JSON-eigenschap **value** in het IoT Hub-bericht. U kunt zoveel waarden toevoegen als u nodig hebt voor het scenario.
19. Selecteer **Opslaan**.
20. Selecteer **Volgende** om naar de pagina **Drempel voor apparatuuruitval** te gaan. De vermelde computers zijn de machines waaraan eerder signaalwaarden zijn toegewezen. Op deze pagina definieert u een drempel waarmee u kunt bepalen of een machine is uitgevallen. Als u bijvoorbeeld de drempel instelt op **10**, wordt door Supply Chain Management een melding gegenereerd als er gedurende 10 minuten geen **PartOut**-signaal van een machine binnenkomt.
21. Selecteer **Volgende** om naar de pagina **Scenario inschakelen** te gaan. Stel de optie om het scenario in te schakelen in.
22. Selecteer **Voltooien**.

De scenario-instelling is nu voltooid. IoT-intelligentie start automatisch met het verwerken van de IoT Hub-berichten.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Het scenario Productkwaliteit configureren in Supply Chain Management

Het scenario **Productkwaliteit** genereert een melding als een kenmerk van een artikel buiten een opgegeven bereik valt. Een sensor verzendt bijvoorbeeld het gewicht van elk artikel naar IoT Hub. In Supply Chain Management wordt een melding gegenereerd als het artikel te zwaar of te licht is.

Het scenario **Productkwaliteit** heeft de volgende afhankelijkheden:

+ Er kan alleen een waarschuwing worden gegenereerd als een productieorder wordt uitgevoerd op een toegewezen machine en een product met een toegewezen batchkenmerk produceert.
+ Er moet een signaal dat overeenkomt met het batchkenmerk met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.
+ Een Unix-eigenschap **tijdstempel**, waarbij de waarde wordt uitgedrukt in milliseconden (ms), moet aanwezig zijn in het Azure IoT Hub-bericht.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Het scenario Productievertragingen configureren in Supply Chain Management

Het scenario **Productievertraging** genereert een melding als de productiedoorvoer onder een drempelwaarde daalt. In dit scenario wordt een **PartOut**-signaal naar de IoT-hub verzonden voor elk geproduceerd artikel. In Supply Chain Management wordt de ordervertraging berekend op basis van de geplande duur van de productieorder, het aantal artikelen dat moet worden geproduceerd, hoe lang de taak actief is en hoeveel **PartOut**-signalen zijn ontvangen. Er wordt een vertragingsmelding gegenereerd als het aantal **PartOut**-signalen voor de taak onder de drempelwaarde daalt.

Het scenario **Productievertragingen** heeft de volgende afhankelijkheden:

+ Er kan alleen een waarschuwing worden geactiveerd als een productieorder wordt uitgevoerd op een toegewezen machine.
+ Er moet een signaal dat overeenkomt met een **PartOut**-signaal voor een toegewezen machine met een unieke eigenschapsnaam naar de Azure IoT-hub worden verzonden.
+ Een Unix-eigenschap **tijdstempel**, waarbij de waarde wordt uitgedrukt in milliseconden (ms), moet aanwezig zijn in het Azure IoT Hub-bericht.

## <a name="disable-a-scenario"></a>Een scenario uitschakelen

Voer de volgende stappen uit om een scenario uit te schakelen.

1. Ga in Supply Chain Management naar **Productiebeheer \> Instellingen \> IoT-intelligentie \> Scenariobeheer**.
2. Selecteer **Configureren** op de tegel voor het scenario.
3. Selecteer **Volgende** om naar de laatste wizardpagina te gaan.
4. Stel de optie om het scenario uit te schakelen in.

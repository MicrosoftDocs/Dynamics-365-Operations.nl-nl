---
title: Scenario-instelling voor IoT-intelligentie
description: In dit onderwerp wordt beschreven hoe u een scenario kunt configureren in Supply Chain Management voor IoT-intelligentie.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597163"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Scenario-instelling voor IoT-intelligentie

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een scenario kunt configureren in Supply Chain Management voor IoT-intelligentie. Voordat u de scenario's kunt instellen, moet u [LCS instellen](iot-lcs-setup.md).

In dit onderwerp configureert u het scenario **Apparatuuruitval** om een melding te genereren in Supply Chain Management wanneer een machine uitvalt.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Het scenario **Apparatuuruitval** configureren in Supply Chain Management

Het scenario **Apparatuuruitval** wijst een PartOut-signaal toe aan een waarschuwingsdrempel voor een machine. De machine wordt alleen gecontroleerd als de machine is geselecteerd voor het scenario en is ingesteld op uitvoering in Supply Chain Management. Als de tijd sinds het laatst ontvangen PartOut-signaal voor de machine langer is dan de waarschuwingsdrempel, wordt er een melding **Machine uitgevallen** geactiveerd. Als de machine nog steeds actief is, wordt bij ontvangst van het volgende **PartOut**-signaal een melding **Machine actief** geactiveerd. Als een machine gedurende 30 minuten uitgeschakeld blijft, wordt er een nieuwe melding **Machine uitgevallen** geactiveerd.

Het scenario **Apparatuuruitval** heeft de volgende afhankelijkheden:

+ Er moet een productieorder worden uitgevoerd op een toegewezen machine om een waarschuwing te kunnen activeren.
+ Er moet een signaal dat overeenkomt met een PartOut-signaal voor een toegewezen machine met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.
+ Er moet een Unix-eigenschap tijdstempel milliseconden aanwezig zijn in het IoT-hub-bericht.

Volg deze stappen om het scenario te configureren:

1. Meld u aan bij Supply Chain Management.
2. Schakel de functievlag voor IoT-intelligentie in. Zie [Overzicht van functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.
3. Configureer de metrische gegevens. Zie [Metrische gegevens configureren](iot-metrics-setup.md#configure-metrics) voor meer informatie.
4. Navigeer naar **Productiebeheer**.
5. Navigeer naar **Instellingen \> IoT-intelligentie \> Scenariobeheer**.
6. Klik op **Configureren** op de tegel **Apparatuuruitval**. De configuratiewizard wordt gestart met de pagina **Schemadefinitie voor apparatuursensor**. Het doel hier is het instellen van het schema in Supply Chain Management, zodat dit overeenkomt met de JSON-indeling van de IoT-berichten. Er kunnen meerdere berichtschema's worden gedefinieerd. Zie [Indelingen voor berichtschema's voor IoT-hub](iot-schema-format.md) voor meer informatie. In dit voorbeeld bevat de berichtlading een batch berichten met de volgende indeling:

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

7. Voeg een rij toe aan de tabel.

    1. Stel de **schemanaam** in op **Id**.
    2. Stel het **schemapad** in op **/payload[\*]/id**.
    3. Stel de **beschrijving** in op **Bericht-id**.

8. Voeg een rij toe aan de tabel.

    1. Stel de **schemanaam** in op **Timestamp**.
    2. Stel het **schemapad** in op **/payload[\*]/timestamp**.
    3. Stel de **beschrijving** in op **Tijdstempel bericht**.

9. Voeg een rij toe aan de tabel.

    1. Stel de **schemanaam** in op **Waarde**.
    2. Stel het **schemapad** in op **/payload[\*]/value**.
    3. Stel de **beschrijving** in op **Waarde bericht**.

    U hoeft niet alle eigenschappen in het bericht te definiëren, maar alleen de eigenschappen die u nodig hebt. In dit voorbeeld hebt u geen rij gemaakt voor **Basistijdstempel**. Het pad voor **Basistijdstempel** zou **/timestamp** zijn.
  
10. Klik op **Volgende** om naar de pagina **Schematoewijzing van apparatuursensor** te gaan.
11. Stel in de rij voor **Resource-id apparatuur** de **schemanaam** in op **ID**. De geldige waarden worden weergegeven in een vervolgkeuzelijst.
12. Stel in de rij voor **UTC-tijd** de **schemanaam** in op **Tijdstempel**. De geldige waarden worden weergegeven in een vervolgkeuzelijst.
13. Stel in de rij voor **Door onderdeel geproduceerd signaal** de **schemanaam** in op **Waarde**. De geldige waarden worden weergegeven in een vervolgkeuzelijst.
14. Klik op **Volgende** voor de pagina **Configuratie resource-id apparatuur**.
15. In deze stap wijst u de berichtwaarden van de IoT-hub toe aan de resources van Supply Chain Management.

    1. Voeg in de tabel **Waarden voor signaalgegevens** een nieuwe rij toe en voer **IoTInt. Machine1225. PartOut** in de kolom **Waarde** in. De waarde **IoTInt.Machine1225.PartOut** is afkomstig van de JSON-eigenschap **id** in het IoT-hub-bericht.
    2. Klik op **Opslaan**.
    3. Klik in de tabel **Toewijzing van zakelijke records** op **Nieuw**. De standaardwaarde voor **Type zakelijke record** wordt automatisch ingevuld en u hoeft deze niet te wijzigen.
    4. Selecteer in de kolom **Zakelijke record** de Supply Chain Management-machineresource van waaruit deze signaalwaarde wordt verzonden.
    5. Klik op **Opslaan**.
    6. Herhaal deze stappen en voeg een nieuwe zakelijke record toe voor **Machine1226**. U kunt meerdere waarden voor signaalgegevens toewijzen aan een enkele record in Supply Chain Management.

16. Gebruik de kolom **Geselecteerd** om te kiezen welke machines u wilt verwerken. U hoeft niet alle signaalwaarden te definiëren en u hoeft niet alle machines te selecteren.
17. Klik op **Volgende** om naar de pagina **Configuratie van door onderdeel geproduceerd signaal** te gaan.
18. Voeg in de tabel **Waarden voor signaalgegevens** een rij toe en stel **Waarde** in op **Waar**. De waarde **Waar** is afkomstig van de JSON_eigenschap **value** in het IoT-hub-bericht. U kunt zoveel waarden toevoegen als u nodig hebt voor het scenario.
19. Klik op **Opslaan**.
20. Klik op **Volgende** om naar de pagina **Drempel voor apparatuuruitval** te gaan. De vermelde computers zijn de machines waaraan eerder signaalwaarden zijn toegewezen. In deze stap definieert u een drempel waarmee u kunt bepalen of een machine is uitgevallen. Als u bijvoorbeeld de drempel instelt op 10, wordt er door Supply Chain Management een melding gegenereerd als er gedurende 10 minuten geen bericht voor onderdeeluitval van een machine binnenkomt.
21. Klik op **Volgende** om naar de pagina **Scenario inschakelen** te gaan. Schakel de schuifregelaar in om het scenario in te schakelen.
22. Klik op **Voltooien**.

De scenario-instelling is voltooid. IoT-intelligentie start automatisch met het verwerken van de IoT-hub-berichten.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Het scenario **Productkwaliteit** configureren in Supply Chain Management

Het scenario **Productkwaliteit** genereert een melding als een kenmerk van een artikel buiten een opgegeven bereik valt. Een sensor kan bijvoorbeeld het gewicht van elk artikel naar IoT-hub verzenden. In Supply Chain Management wordt een melding gegenereerd als het artikel te zwaar of te licht is.

Het scenario heeft de volgende afhankelijkheden:

+ Een productieorder moet worden uitgevoerd op een toegewezen machine en een product met een toegewezen batchkenmerk produceren om een waarschuwing te activeren.
+ Er moet een signaal dat overeenkomt met het batchkenmerk met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.
+ Er moet een Unix-eigenschap tijdstempel milliseconden aanwezig zijn in het IoT-hub-bericht.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Het scenario **Productievertragingen** configureren in Supply Chain Management

Het scenario **Productievertraging** genereert een melding als de productiedoorvoer onder een drempelwaarde daalt. In dit scenario wordt een **PartOut**-signaal naar de IoT-hub verzonden voor elk geproduceerd artikel. In Supply Chain Management wordt de ordervertraging berekend op basis van de duur van de geplande productieorder, het aantal artikelen dat moet worden geproduceerd, hoe lang de taak actief is en hoeveel **PartOut**-signalen zijn ontvangen. Er wordt een vertragingsmelding gegenereerd als het aantal **PartOut**-signalen voor de taak onder de drempelwaarde van de verwachte waarde daalt.

Het scenario heeft de volgende afhankelijkheden:

+ Er moet een productieorder worden uitgevoerd op een toegewezen machine om een waarschuwing te kunnen activeren.
+ Er moet een signaal dat overeenkomt met een PartOut-signaal voor een toegewezen machine met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.
+ Er moet een Unix-eigenschap tijdstempel milliseconden aanwezig zijn in het IoT-hub-bericht.

## <a name="how-to-disable-a-scenario"></a>Een scenario uitschakelen

Voer de volgende stappen uit om een scenario uit te schakelen:

1. Navigeer in Supply Chain Management naar **Productiebeheer \> Instellingen \> IoT-intelligentie \> Scenariobeheer**.
2. Klik op **Configureren** in het scenario.
3. Klik op **Volgende** om naar het laatste tabblad van de wizard te gaan.
4. Schakel de schuifregelaar in om het scenario uit te schakelen.

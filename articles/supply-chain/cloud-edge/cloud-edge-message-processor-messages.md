---
title: Berichten van berichtenverwerker
description: Dit onderwerp biedt informatie over de functie Berichten van berichtenverwerker voor de workloads van schaaleenheden.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 76a3cc316da322c7997072c00780f2fc133bfd2a02274b1e53f5cd06cfb1277e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748854"
---
# <a name="message-processor-messages"></a>Berichten van berichtenverwerker

[!include [banner](../includes/banner.md)]

Berichten van berichtenverwerker worden gebruikt wanner u cloud- en randschaaleenheden gebruikt voor [productieworkloads](cloud-edge-workload-manufacturing.md) en [magazijnbeheerworkloads](cloud-edge-workload-warehousing.md).

Er wordt een grote hoeveelheid gegevens uitgewisseld tussen de implementatieomgevingen van de hub en de schaaleenheid om deze te synchroniseren, maar slechts enkele van deze gegevensuitwisselingen worden verwerkt door de *berichtenverwerker*. U kunt de berichten die worden verwerkt door de berichtenverwerker weergeven door te gaan naar **Systeembeheer > Berichtverwerker > Berichten van berichtenverwerker**.

## <a name="message-grid-columns-and-filters"></a>Kolommen en filters in het berichtenraster

Met de velden boven aan de pagina **Berichten van berichtenverwerker** kunt u specifieke berichten vinden die u zoekt. De meeste filters komen overeen met de kolomkoppen in het berichtenraster. De volgende filters en kolomkoppen zijn beschikbaar:

- **Berichttype**: geeft het type bericht op.
- **Berichtenwachtrij**: Hiermee wordt de naam opgegeven van de wachtrij waarin het bericht moet worden verwerkt. De volgende wachtrijen zijn beschikbaar:
  - *Schaaleenheid naar hub*
  - *Schaaleenheid voor uitvoering van hub naar magazijn*
  - *Schaaleenheid voor uitvoering van hub naar productie*
- **Berichtstatus**: Geeft de status van het bericht op. De volgende statuswaarden bestaan:
  - *In de wachtrij*: het bericht is gereed voor verwerking door de berichtenverwerker.
  - *Verwerkt*: het bericht is verwerkt door de berichtenverwerker.
  - *Geannuleerd*: het bericht is verwerkt, maar de verwerking is mislukt.
- **Berichtinhoud**: Dit filter biedt de mogelijkheid voor een zoekopdracht in de volledige tekst van de berichtinhoud. (De inhoud van het bericht wordt niet in het raster getoond.) Het filter verwerkt de meeste speciale symbolen (zoals '-') als spaties en alle spatietekens als booleaanse OR-operators. Dit betekent dat als u bijvoorbeeld naar een specifieke `journalid`-waarde zoekt die gelijk is aan 'USMF-123456', het systeem alle berichten vindt met 'USMF' of '123456', wat een lange lijst kan zijn. Het is daarom beter om alleen '123456' in te voeren, omdat dat meer specifieke resultaten oplevert.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Voorbeeld berichttype: Financiële update voorraadcorrectie aanvragen

Het **berichttype** *Financiële update voorraadcorrectie aanvragen* wordt bijvoorbeeld gebruikt om een tellingsjournaal te maken en te boeken op de hub, wanneer een medewerker met behulp van de magazijnapp [een voorraadcorrectie registreert](cloud-edge-warehouse-inventory-adjustment.md) voor een workload voor magazijnbeheer van de schaaleenheid. Omdat dit specifieke proces afkomstig is van een schaaleenheid, wordt in het veld **Berichtenwachtrij** de waarde *Schaaleenheid naar hub* getoond.

Voor dit berichttype registreert een schaaleenheidworkload het bericht als onderdeel van een voorraadcorrectiebewerking in een magazijn-app. De berichtgegevens worden vervolgens doorgegeven naar de hub als onderdeel van hetzelfde proces dat wordt gebruikt voor de [Commerce Data Exchange-architectuur](../../commerce/commerce-architecture.md). De **berichtstatus** wordt bijgewerkt naar *In de wachtrij*. De berichtenverwerker probeert vervolgens het bericht te verwerken en werkt **berichtstatus** bij naar *Verwerkt* of *Geannuleerd*, al naar gelang de uitkomst van de verwerking.

## <a name="view-the-message-log-message-content-and-details"></a>Het berichtenlogboek, de berichtinhoud en details weergeven

U kunt gedetailleerde informatie over een bericht vinden door het te selecteren in het raster en vervolgens de tabbladen **Logboek** of **Berichtinhoud** te openen onder het berichtenraster, waar alle verwerkingsgebeurtenis worden weergegeven.

De **Berichtinhoud** is afhankelijk van het **Berichttype** en heeft daarom een andere tekstlengte. Een typische tekst uit de berichtinhoud begint met een **{** en eindigt met een **}**, waartussen veldnamen staan zoals `journalId` gevolgd door een **:** en een waarde zoals *USMF-123456*.

De werkbalk op het tabblad **Logboek** bevat de volgende knoppen:

- **Logboek**: Geeft de verwerkingsresultaten weer. Dit is vooral nuttig om te zien wat de redenen voor een verwerkingsfout zijn voor berichten waarvan het **Verwerkingsresultaat** *Mislukt* is.
- **Bundel**: Meerdere bewerkingen voor berichtverwerking kunnen worden uitgevoerd als onderdeel van hetzelfde batchproces. Selecteer deze knop als u deze gedetailleerde gegevens wilt weergeven. U kunt bijvoorbeeld zien of er afhankelijkheden zijn die vereisen dat het systeem bepaalde berichten in een specifieke volgorde verwerkt.

## <a name="message-processor-batch-job"></a>De batchtaak Berichtenverwerker

Wanneer u een cloud- en edge-implementatie hebt, wordt de batchtaak *Berichtenverwerker* automatisch aangeroepen wanneer een nieuw bericht wordt gemaakt voor verwerking. U zou daarom deze taak niet handmatig hoeven te plannen.

U kunt de batchtaak zo nodig openen door te gaan naar **Systeembeheer > Berichtverwerker > Berichtenverwerker**.

## <a name="manually-process-or-cancel-a-message"></a>Een bericht handmatig verwerken of annuleren

Zo nodig kunt u een bericht handmatig verwerken of annuleren, afhankelijk van de huidige status. Selecteer hiervoor het bericht in het raster en selecteer **Verwerken** of **Annuleren** in het actievenster.

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Zakelijke gebeurtenissen instellen om waarschuwingen te leveren voor mislukte verwerkingsresultaten

Niet alleen kunt u, om berichten te vinden waarvan de verwerking is mislukt, filteren op de **Geannuleerd** in het veld *Berichtstatus*. U kunt ook [zakelijke gebeurtenissen](../../fin-ops-core/dev-itpro/business-events/home-page.md) op de hub instellen om u te waarschuwen dat de verwerking van berichten is mislukt. Om dit te doen, activeert u de zakelijke gebeurtenis met de naam *Berichtverwerker-bericht verwerkt* op de pagina **Catalogus met zakelijke gebeurtenissen** (**Systeembeheer > Instellingen > Zakelijke gebeurtenissen > Catalogus met zakelijke gebeurtenissen**).

Als onderdeel van het activeringsproces wordt u gevraagd om op te geven of de gebeurtenis specifiek is voor een rechtspersoon of voor alle rechtspersonen en om een **Eindpuntnaam** op te geven, die u eerst moet definiëren.

>[!NOTE]
> Als **Als zich een zakelijke gebeurtenis voordoet** is ingesteld op *Microsoft Power Automate* (in plaats van bijvoorbeeld *HTTPS*), wordt de **eindpuntnaam** automatisch gemaakt in Supply Chain Management op basis van de *Microsoft Power Automate*-configuratie.

### <a name="microsoft-power-automate-example"></a>Voorbeeld met Microsoft Power Automate

In dit voorbeeld wordt **Als zich een zakelijke gebeurtenis voordoet** gebruikt met *Microsoft Power Automate*; e-mails met InfoLog-berichten en hyperlinks worden verzonden om de pagina **Berichten van berichtenverwerker** te openen voor een specifiek mislukt bericht op de implementatie van de hub. Zo nodig kunt u extra logica toevoegen om de meldingen parallel te verzenden via verschillende kanalen en de ontvangers aan te sturen op basis van de gebeurtenisgegevens.

1. Maak in [Power Automate](https://preview.flow.microsoft.com) een nieuwe automatische cloudstroom voor de flowtrigger **Als zich een zakelijke gebeurtenis voordoet - Fin & Ops-app (Dynamics 365)** gevolgd door de stappen **JSON parseren** en **Een e-mail verzenden**, zoals in de volgende afbeelding wordt weergegeven.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Met Power Automate geautomatiseerde cloudstroom.":::

1. In de stap **Als zich een zakelijke gebeurtenis voordoet** kunt u het **Exemplaar** van de hub zoeken of invoeren, met daarna de **Categorie** en de **Zakelijke gebeurtenis** *Bericht van berichtenverwerker verwerkt*, zoals in de volgende afbeelding wordt weergegeven.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Stap Als zich een zakelijke gebeurtenis voordoet in Power Automate.":::

1. Voer voor de stap **JSON parseren** een **Schema** in dat de uitgebreide velden definieert. U kunt de optie *Schema downloaden* op de pagina **Catalogus met zakelijke gebeurtenissen** in Supply Chain Management gebruiken of u kunt beginnen door de voorbeeldtekst voor een schema te plakken. Deze voorbeeldtekst vindt u na de volgende afbeelding.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Stap JSON parseren in Power Automate.":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. In de stap **Een e-mail verzenden** kunt u de afzonderlijke velden selecteren of beginnen door het voorbeeld van het e-mailbericht te plakken in het veld **Hoofdtekst**. Dit voorbeeld vindt u na de volgende afbeelding.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Stap Een e-mail verzenden in Power Automate.":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Wanneer u de zakelijke gebeurtenis opslaat, wordt deze automatisch geactiveerd en is hij klaar om te worden gebruikt als onderdeel van Supply Chain Management.

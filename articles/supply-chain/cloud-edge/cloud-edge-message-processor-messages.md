---
title: Berichten van berichtenverwerker
description: Dit onderwerp biedt informatie over de functie Berichten van berichtenverwerker voor de workloads van schaaleenheden.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b1428e2e657e653874d4ec07605932a32bd803b2
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938245"
---
# <a name="message-processor-messages"></a><span data-ttu-id="bfecb-103">Berichten van berichtenverwerker</span><span class="sxs-lookup"><span data-stu-id="bfecb-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bfecb-104">Berichten van berichtenverwerker worden gebruikt wanner u cloud- en randschaaleenheden gebruikt voor [productieworkloads](cloud-edge-workload-manufacturing.md) en [magazijnbeheerworkloads](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="bfecb-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="bfecb-105">Er wordt een grote hoeveelheid gegevens uitgewisseld tussen de implementatieomgevingen van de hub en de schaaleenheid om deze te synchroniseren, maar slechts enkele van deze gegevensuitwisselingen worden verwerkt door de *berichtenverwerker*.</span><span class="sxs-lookup"><span data-stu-id="bfecb-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="bfecb-106">U kunt de berichten die worden verwerkt door de berichtenverwerker weergeven door te gaan naar **Systeembeheer > Berichtverwerker > Berichten van berichtenverwerker**.</span><span class="sxs-lookup"><span data-stu-id="bfecb-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="bfecb-107">Kolommen en filters in het berichtenraster</span><span class="sxs-lookup"><span data-stu-id="bfecb-107">Message grid columns and filters</span></span>

<span data-ttu-id="bfecb-108">Met de velden boven aan de pagina **Berichten van berichtenverwerker** kunt u specifieke berichten vinden die u zoekt.</span><span class="sxs-lookup"><span data-stu-id="bfecb-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="bfecb-109">De meeste filters komen overeen met de kolomkoppen in het berichtenraster.</span><span class="sxs-lookup"><span data-stu-id="bfecb-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="bfecb-110">De volgende filters en kolomkoppen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="bfecb-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="bfecb-111">**Berichttype**: geeft het type bericht op.</span><span class="sxs-lookup"><span data-stu-id="bfecb-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="bfecb-112">**Berichtenwachtrij**: Hiermee wordt de naam opgegeven van de wachtrij waarin het bericht moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="bfecb-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="bfecb-113">De volgende wachtrijen zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="bfecb-113">The following queues are provided:</span></span>
  - <span data-ttu-id="bfecb-114">*Schaaleenheid naar hub*</span><span class="sxs-lookup"><span data-stu-id="bfecb-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="bfecb-115">*Schaaleenheid voor uitvoering van hub naar magazijn*</span><span class="sxs-lookup"><span data-stu-id="bfecb-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="bfecb-116">*Schaaleenheid voor uitvoering van hub naar productie*</span><span class="sxs-lookup"><span data-stu-id="bfecb-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="bfecb-117">**Berichtstatus**: Geeft de status van het bericht op.</span><span class="sxs-lookup"><span data-stu-id="bfecb-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="bfecb-118">De volgende statuswaarden bestaan:</span><span class="sxs-lookup"><span data-stu-id="bfecb-118">The following states exists:</span></span>
  - <span data-ttu-id="bfecb-119">*In de wachtrij*: het bericht is gereed voor verwerking door de berichtenverwerker.</span><span class="sxs-lookup"><span data-stu-id="bfecb-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="bfecb-120">*Verwerkt*: het bericht is verwerkt door de berichtenverwerker.</span><span class="sxs-lookup"><span data-stu-id="bfecb-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="bfecb-121">*Geannuleerd*: het bericht is verwerkt, maar de verwerking is mislukt.</span><span class="sxs-lookup"><span data-stu-id="bfecb-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="bfecb-122">**Berichtinhoud**: Dit filter biedt de mogelijkheid voor een zoekopdracht in de volledige tekst van de berichtinhoud.</span><span class="sxs-lookup"><span data-stu-id="bfecb-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="bfecb-123">(De inhoud van het bericht wordt niet in het raster getoond.) Het filter verwerkt de meeste speciale symbolen (zoals '-') als spaties en alle spatietekens als booleaanse OR-operators.</span><span class="sxs-lookup"><span data-stu-id="bfecb-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="bfecb-124">Dit betekent dat als u bijvoorbeeld naar een specifieke `journalid`-waarde zoekt die gelijk is aan 'USMF-123456', het systeem alle berichten vindt met 'USMF' of '123456', wat een lange lijst kan zijn.</span><span class="sxs-lookup"><span data-stu-id="bfecb-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="bfecb-125">Het is daarom beter om alleen '123456' in te voeren, omdat dat meer specifieke resultaten oplevert.</span><span class="sxs-lookup"><span data-stu-id="bfecb-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="bfecb-126">Voorbeeld berichttype: Financiële update voorraadcorrectie aanvragen</span><span class="sxs-lookup"><span data-stu-id="bfecb-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="bfecb-127">Het **berichttype** *Financiële update voorraadcorrectie aanvragen* wordt bijvoorbeeld gebruikt om een tellingsjournaal te maken en te boeken op de hub, wanneer een medewerker met behulp van de magazijnapp [een voorraadcorrectie registreert](cloud-edge-warehouse-inventory-adjustment.md) voor een workload voor magazijnbeheer van de schaaleenheid.</span><span class="sxs-lookup"><span data-stu-id="bfecb-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="bfecb-128">Omdat dit specifieke proces afkomstig is van een schaaleenheid, wordt in het veld **Berichtenwachtrij** de waarde *Schaaleenheid naar hub* getoond.</span><span class="sxs-lookup"><span data-stu-id="bfecb-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="bfecb-129">Voor dit berichttype registreert een schaaleenheidworkload het bericht als onderdeel van een voorraadcorrectiebewerking in een magazijn-app.</span><span class="sxs-lookup"><span data-stu-id="bfecb-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="bfecb-130">De berichtgegevens worden vervolgens doorgegeven naar de hub als onderdeel van hetzelfde proces dat wordt gebruikt voor de [Commerce Data Exchange-architectuur](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="bfecb-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="bfecb-131">De **berichtstatus** wordt bijgewerkt naar *In de wachtrij*.</span><span class="sxs-lookup"><span data-stu-id="bfecb-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="bfecb-132">De berichtenverwerker probeert vervolgens het bericht te verwerken en werkt **berichtstatus** bij naar *Verwerkt* of *Geannuleerd*, al naar gelang de uitkomst van de verwerking.</span><span class="sxs-lookup"><span data-stu-id="bfecb-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="bfecb-133">Het berichtenlogboek, de berichtinhoud en details weergeven</span><span class="sxs-lookup"><span data-stu-id="bfecb-133">View the message log, message content, and details</span></span>

<span data-ttu-id="bfecb-134">U kunt gedetailleerde informatie over een bericht vinden door het te selecteren in het raster en vervolgens de tabbladen **Logboek** of **Berichtinhoud** te openen onder het berichtenraster, waar alle verwerkingsgebeurtenis worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bfecb-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="bfecb-135">De **Berichtinhoud** is afhankelijk van het **Berichttype** en heeft daarom een andere tekstlengte.</span><span class="sxs-lookup"><span data-stu-id="bfecb-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="bfecb-136">Een typische tekst uit de berichtinhoud begint met een **{** en eindigt met een **}**, waartussen veldnamen staan zoals `journalId` gevolgd door een **:** en een waarde zoals *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="bfecb-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="bfecb-137">De werkbalk op het tabblad **Logboek** bevat de volgende knoppen:</span><span class="sxs-lookup"><span data-stu-id="bfecb-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="bfecb-138">**Logboek**: Geeft de verwerkingsresultaten weer.</span><span class="sxs-lookup"><span data-stu-id="bfecb-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="bfecb-139">Dit is vooral nuttig om te zien wat de redenen voor een verwerkingsfout zijn voor berichten waarvan het **Verwerkingsresultaat** *Mislukt* is.</span><span class="sxs-lookup"><span data-stu-id="bfecb-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="bfecb-140">**Bundel**: Meerdere bewerkingen voor berichtverwerking kunnen worden uitgevoerd als onderdeel van hetzelfde batchproces.</span><span class="sxs-lookup"><span data-stu-id="bfecb-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="bfecb-141">Selecteer deze knop als u deze gedetailleerde gegevens wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="bfecb-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="bfecb-142">U kunt bijvoorbeeld zien of er afhankelijkheden zijn die vereisen dat het systeem bepaalde berichten in een specifieke volgorde verwerkt.</span><span class="sxs-lookup"><span data-stu-id="bfecb-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="bfecb-143">De batchtaak Berichtenverwerker</span><span class="sxs-lookup"><span data-stu-id="bfecb-143">Message processor batch job</span></span>

<span data-ttu-id="bfecb-144">Wanneer u een cloud- en edge-implementatie hebt, wordt de batchtaak *Berichtenverwerker* automatisch aangeroepen wanneer een nieuw bericht wordt gemaakt voor verwerking. U zou daarom deze taak niet handmatig hoeven te plannen.</span><span class="sxs-lookup"><span data-stu-id="bfecb-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="bfecb-145">U kunt de batchtaak zo nodig openen door te gaan naar **Systeembeheer > Berichtverwerker > Berichtenverwerker**.</span><span class="sxs-lookup"><span data-stu-id="bfecb-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="bfecb-146">Een bericht handmatig verwerken of annuleren</span><span class="sxs-lookup"><span data-stu-id="bfecb-146">Manually process or cancel a message</span></span>

<span data-ttu-id="bfecb-147">Zo nodig kunt u een bericht handmatig verwerken of annuleren, afhankelijk van de huidige status.</span><span class="sxs-lookup"><span data-stu-id="bfecb-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="bfecb-148">Selecteer hiervoor het bericht in het raster en selecteer **Verwerken** of **Annuleren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="bfecb-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="bfecb-149">Zakelijke gebeurtenissen instellen om waarschuwingen te leveren voor mislukte verwerkingsresultaten</span><span class="sxs-lookup"><span data-stu-id="bfecb-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="bfecb-150">Niet alleen kunt u, om berichten te vinden waarvan de verwerking is mislukt, filteren op de **Geannuleerd** in het veld *Berichtstatus*. U kunt ook [zakelijke gebeurtenissen](../../fin-ops-core/dev-itpro/business-events/home-page.md) op de hub instellen om u te waarschuwen dat de verwerking van berichten is mislukt.</span><span class="sxs-lookup"><span data-stu-id="bfecb-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="bfecb-151">Om dit te doen, activeert u de zakelijke gebeurtenis met de naam *Berichtverwerker-bericht verwerkt* op de pagina **Catalogus met zakelijke gebeurtenissen** (**Systeembeheer > Instellingen > Zakelijke gebeurtenissen > Catalogus met zakelijke gebeurtenissen**).</span><span class="sxs-lookup"><span data-stu-id="bfecb-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="bfecb-152">Als onderdeel van het activeringsproces wordt u gevraagd om op te geven of de gebeurtenis specifiek is voor een rechtspersoon of voor alle rechtspersonen en om een **Eindpuntnaam** op te geven, die u eerst moet definiëren.</span><span class="sxs-lookup"><span data-stu-id="bfecb-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="bfecb-153">Als **Als zich een zakelijke gebeurtenis voordoet** is ingesteld op *Microsoft Power Automate* (in plaats van bijvoorbeeld *HTTPS*), wordt de **eindpuntnaam** automatisch gemaakt in Supply Chain Management op basis van de *Microsoft Power Automate*-configuratie.</span><span class="sxs-lookup"><span data-stu-id="bfecb-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="bfecb-154">Voorbeeld met Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="bfecb-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="bfecb-155">In dit voorbeeld wordt **Als zich een zakelijke gebeurtenis voordoet** gebruikt met *Microsoft Power Automate*; e-mails met InfoLog-berichten en hyperlinks worden verzonden om de pagina **Berichten van berichtenverwerker** te openen voor een specifiek mislukt bericht op de implementatie van de hub.</span><span class="sxs-lookup"><span data-stu-id="bfecb-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="bfecb-156">Zo nodig kunt u extra logica toevoegen om de meldingen parallel te verzenden via verschillende kanalen en de ontvangers aan te sturen op basis van de gebeurtenisgegevens.</span><span class="sxs-lookup"><span data-stu-id="bfecb-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="bfecb-157">Maak in [Power Automate](https://preview.flow.microsoft.com) een nieuwe automatische cloudstroom voor de flowtrigger **Als zich een zakelijke gebeurtenis voordoet - Fin & Ops-app (Dynamics 365)** gevolgd door de stappen **JSON parseren** en **Een e-mail verzenden**, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bfecb-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Met Power Automate geautomatiseerde cloudstroom":::

1. <span data-ttu-id="bfecb-159">In de stap **Als zich een zakelijke gebeurtenis voordoet** kunt u het **Exemplaar** van de hub zoeken of invoeren, met daarna de **Categorie** en de **Zakelijke gebeurtenis** *Bericht van berichtenverwerker verwerkt*, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bfecb-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Stap Als zich een zakelijke gebeurtenis voordoet in Power Automate":::

1. <span data-ttu-id="bfecb-161">Voer voor de stap **JSON parseren** een **Schema** in dat de uitgebreide velden definieert.</span><span class="sxs-lookup"><span data-stu-id="bfecb-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="bfecb-162">U kunt de optie *Schema downloaden* op de pagina **Catalogus met zakelijke gebeurtenissen** in Supply Chain Management gebruiken of u kunt beginnen door de voorbeeldtekst voor een schema te plakken.</span><span class="sxs-lookup"><span data-stu-id="bfecb-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="bfecb-163">Deze voorbeeldtekst vindt u na de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="bfecb-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Stap JSON parseren in Power Automate":::

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

1. <span data-ttu-id="bfecb-165">In de stap **Een e-mail verzenden** kunt u de afzonderlijke velden selecteren of beginnen door het voorbeeld van het e-mailbericht te plakken in het veld **Hoofdtekst**.</span><span class="sxs-lookup"><span data-stu-id="bfecb-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="bfecb-166">Dit voorbeeld vindt u na de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="bfecb-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Stap Een e-mail verzenden in Power Automate":::

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

1. <span data-ttu-id="bfecb-168">Wanneer u de zakelijke gebeurtenis opslaat, wordt deze automatisch geactiveerd en is hij klaar om te worden gebruikt als onderdeel van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bfecb-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>

---
title: Scenario-instelling voor IoT-intelligentie
description: In dit onderwerp wordt beschreven hoe u een scenario kunt configureren in Supply Chain Management voor IoT-intelligentie.
author: robinarh
manager: AnnBe
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
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386502"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="97b1f-103">Scenario-instelling voor IoT-intelligentie</span><span class="sxs-lookup"><span data-stu-id="97b1f-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97b1f-104">In dit onderwerp wordt beschreven hoe u een scenario kunt configureren in Supply Chain Management voor IoT-intelligentie.</span><span class="sxs-lookup"><span data-stu-id="97b1f-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="97b1f-105">Voordat u de scenario's kunt instellen, moet u [LCS instellen](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="97b1f-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="97b1f-106">In dit onderwerp configureert u het scenario **Apparatuuruitval** om een melding te genereren in Supply Chain Management wanneer een machine uitvalt.</span><span class="sxs-lookup"><span data-stu-id="97b1f-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="97b1f-107">Het scenario **Apparatuuruitval** configureren in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="97b1f-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="97b1f-108">Het scenario **Apparatuuruitval** wijst een PartOut-signaal toe aan een waarschuwingsdrempel voor een machine.</span><span class="sxs-lookup"><span data-stu-id="97b1f-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="97b1f-109">De machine wordt alleen gecontroleerd als de machine is geselecteerd voor het scenario en is ingesteld op uitvoering in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="97b1f-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="97b1f-110">Als de tijd sinds het laatst ontvangen PartOut-signaal voor de machine langer is dan de waarschuwingsdrempel, wordt er een melding **Machine uitgevallen** geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="97b1f-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="97b1f-111">Als de machine nog steeds actief is, wordt bij ontvangst van het volgende **PartOut**-signaal een melding **Machine actief** geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="97b1f-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="97b1f-112">Als een machine gedurende 30 minuten uitgeschakeld blijft, wordt er een nieuwe melding **Machine uitgevallen** geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="97b1f-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="97b1f-113">Het scenario **Apparatuuruitval** heeft de volgende afhankelijkheden:</span><span class="sxs-lookup"><span data-stu-id="97b1f-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="97b1f-114">Er moet een productieorder worden uitgevoerd op een toegewezen machine om een waarschuwing te kunnen activeren.</span><span class="sxs-lookup"><span data-stu-id="97b1f-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="97b1f-115">Er moet een signaal dat overeenkomt met een PartOut-signaal voor een toegewezen machine met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="97b1f-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="97b1f-116">Er moet een Unix-eigenschap tijdstempel milliseconden aanwezig zijn in het IoT-hub-bericht.</span><span class="sxs-lookup"><span data-stu-id="97b1f-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="97b1f-117">Volg deze stappen om het scenario te configureren:</span><span class="sxs-lookup"><span data-stu-id="97b1f-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="97b1f-118">Meld u aan bij Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="97b1f-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="97b1f-119">Schakel de functievlag voor IoT-intelligentie in.</span><span class="sxs-lookup"><span data-stu-id="97b1f-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="97b1f-120">Zie [Overzicht van functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="97b1f-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="97b1f-121">Configureer de metrische gegevens.</span><span class="sxs-lookup"><span data-stu-id="97b1f-121">Configure the metrics.</span></span> <span data-ttu-id="97b1f-122">Zie [Metrische gegevens configureren](iot-metrics-setup.md#configure-metrics) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="97b1f-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="97b1f-123">Navigeer naar **Productiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="97b1f-124">Navigeer naar **Instellingen \> IoT-intelligentie \> Scenariobeheer**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="97b1f-125">Klik op **Configureren** op de tegel **Apparatuuruitval**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="97b1f-126">De configuratiewizard wordt gestart met de pagina **Schemadefinitie voor apparatuursensor**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="97b1f-127">Het doel hier is het instellen van het schema in Supply Chain Management, zodat dit overeenkomt met de JSON-indeling van de IoT-berichten.</span><span class="sxs-lookup"><span data-stu-id="97b1f-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="97b1f-128">Er kunnen meerdere berichtschema's worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="97b1f-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="97b1f-129">Zie [Indelingen voor berichtschema's voor IoT-hub](iot-schema-format.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="97b1f-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="97b1f-130">In dit voorbeeld bevat de berichtlading een batch berichten met de volgende indeling:</span><span class="sxs-lookup"><span data-stu-id="97b1f-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="97b1f-131">Voeg een rij toe aan de tabel.</span><span class="sxs-lookup"><span data-stu-id="97b1f-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="97b1f-132">Stel de **schemanaam** in op **Id**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="97b1f-133">Stel het **schemapad** in op **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="97b1f-134">Stel de **beschrijving** in op **Bericht-id**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="97b1f-135">Voeg een rij toe aan de tabel.</span><span class="sxs-lookup"><span data-stu-id="97b1f-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="97b1f-136">Stel de **schemanaam** in op **Timestamp**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="97b1f-137">Stel het **schemapad** in op **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="97b1f-138">Stel de **beschrijving** in op **Tijdstempel bericht**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="97b1f-139">Voeg een rij toe aan de tabel.</span><span class="sxs-lookup"><span data-stu-id="97b1f-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="97b1f-140">Stel de **schemanaam** in op **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="97b1f-141">Stel het **schemapad** in op **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="97b1f-142">Stel de **beschrijving** in op **Waarde bericht**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="97b1f-143">U hoeft niet alle eigenschappen in het bericht te definiëren, maar alleen de eigenschappen die u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="97b1f-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="97b1f-144">In dit voorbeeld hebt u geen rij gemaakt voor **Basistijdstempel**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="97b1f-145">Het pad voor **Basistijdstempel** zou **/timestamp** zijn.</span><span class="sxs-lookup"><span data-stu-id="97b1f-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="97b1f-146">Klik op **Volgende** om naar de pagina **Schematoewijzing van apparatuursensor** te gaan.</span><span class="sxs-lookup"><span data-stu-id="97b1f-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="97b1f-147">Stel in de rij voor **Resource-id apparatuur** de **schemanaam** in op **ID**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="97b1f-148">De geldige waarden worden weergegeven in een vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="97b1f-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="97b1f-149">Stel in de rij voor **UTC-tijd** de **schemanaam** in op **Tijdstempel**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="97b1f-150">De geldige waarden worden weergegeven in een vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="97b1f-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="97b1f-151">Stel in de rij voor **Door onderdeel geproduceerd signaal** de **schemanaam** in op **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="97b1f-152">De geldige waarden worden weergegeven in een vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="97b1f-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="97b1f-153">Klik op **Volgende** voor de pagina **Configuratie resource-id apparatuur**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="97b1f-154">In deze stap wijst u de berichtwaarden van de IoT-hub toe aan de resources van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="97b1f-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="97b1f-155">Voeg in de tabel **Waarden voor signaalgegevens** een nieuwe rij toe en voer **IoTInt. Machine1225. PartOut** in de kolom **Waarde** in.</span><span class="sxs-lookup"><span data-stu-id="97b1f-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="97b1f-156">De waarde **IoTInt.Machine1225.PartOut** is afkomstig van de JSON-eigenschap **id** in het IoT-hub-bericht.</span><span class="sxs-lookup"><span data-stu-id="97b1f-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="97b1f-157">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-157">Click **Save**.</span></span>
    3. <span data-ttu-id="97b1f-158">Klik in de tabel **Toewijzing van zakelijke records** op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="97b1f-159">De standaardwaarde voor **Type zakelijke record** wordt automatisch ingevuld en u hoeft deze niet te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="97b1f-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="97b1f-160">Selecteer in de kolom **Zakelijke record** de Supply Chain Management-machineresource van waaruit deze signaalwaarde wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="97b1f-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="97b1f-161">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-161">Click **Save**.</span></span>
    6. <span data-ttu-id="97b1f-162">Herhaal deze stappen en voeg een nieuwe zakelijke record toe voor **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="97b1f-163">U kunt meerdere waarden voor signaalgegevens toewijzen aan een enkele record in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="97b1f-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="97b1f-164">Gebruik de kolom **Geselecteerd** om te kiezen welke machines u wilt verwerken.</span><span class="sxs-lookup"><span data-stu-id="97b1f-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="97b1f-165">U hoeft niet alle signaalwaarden te definiëren en u hoeft niet alle machines te selecteren.</span><span class="sxs-lookup"><span data-stu-id="97b1f-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="97b1f-166">Klik op **Volgende** om naar de pagina **Configuratie van door onderdeel geproduceerd signaal** te gaan.</span><span class="sxs-lookup"><span data-stu-id="97b1f-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="97b1f-167">Voeg in de tabel **Waarden voor signaalgegevens** een rij toe en stel **Waarde** in op **Waar**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="97b1f-168">De waarde **Waar** is afkomstig van de JSON_eigenschap **value** in het IoT-hub-bericht.</span><span class="sxs-lookup"><span data-stu-id="97b1f-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="97b1f-169">U kunt zoveel waarden toevoegen als u nodig hebt voor het scenario.</span><span class="sxs-lookup"><span data-stu-id="97b1f-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="97b1f-170">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-170">Click **Save**.</span></span>
20. <span data-ttu-id="97b1f-171">Klik op **Volgende** om naar de pagina **Drempel voor apparatuuruitval** te gaan.</span><span class="sxs-lookup"><span data-stu-id="97b1f-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="97b1f-172">De vermelde computers zijn de machines waaraan eerder signaalwaarden zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="97b1f-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="97b1f-173">In deze stap definieert u een drempel waarmee u kunt bepalen of een machine is uitgevallen.</span><span class="sxs-lookup"><span data-stu-id="97b1f-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="97b1f-174">Als u bijvoorbeeld de drempel instelt op 10, wordt er door Supply Chain Management een melding gegenereerd als er gedurende 10 minuten geen bericht voor onderdeeluitval van een machine binnenkomt.</span><span class="sxs-lookup"><span data-stu-id="97b1f-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="97b1f-175">Klik op **Volgende** om naar de pagina **Scenario inschakelen** te gaan.</span><span class="sxs-lookup"><span data-stu-id="97b1f-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="97b1f-176">Schakel de schuifregelaar in om het scenario in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="97b1f-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="97b1f-177">Klik op **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-177">Click **Finish**.</span></span>

<span data-ttu-id="97b1f-178">De scenario-instelling is voltooid.</span><span class="sxs-lookup"><span data-stu-id="97b1f-178">The scenario setup is complete.</span></span> <span data-ttu-id="97b1f-179">IoT-intelligentie start automatisch met het verwerken van de IoT-hub-berichten.</span><span class="sxs-lookup"><span data-stu-id="97b1f-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="97b1f-180">Het scenario **Productkwaliteit** configureren in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="97b1f-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="97b1f-181">Het scenario **Productkwaliteit** genereert een melding als een kenmerk van een artikel buiten een opgegeven bereik valt.</span><span class="sxs-lookup"><span data-stu-id="97b1f-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="97b1f-182">Een sensor kan bijvoorbeeld het gewicht van elk artikel naar IoT-hub verzenden.</span><span class="sxs-lookup"><span data-stu-id="97b1f-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="97b1f-183">In Supply Chain Management wordt een melding gegenereerd als het artikel te zwaar of te licht is.</span><span class="sxs-lookup"><span data-stu-id="97b1f-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="97b1f-184">Het scenario heeft de volgende afhankelijkheden:</span><span class="sxs-lookup"><span data-stu-id="97b1f-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="97b1f-185">Een productieorder moet worden uitgevoerd op een toegewezen machine en een product met een toegewezen batchkenmerk produceren om een waarschuwing te activeren.</span><span class="sxs-lookup"><span data-stu-id="97b1f-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="97b1f-186">Er moet een signaal dat overeenkomt met het batchkenmerk met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="97b1f-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="97b1f-187">Er moet een Unix-eigenschap tijdstempel milliseconden aanwezig zijn in het IoT-hub-bericht.</span><span class="sxs-lookup"><span data-stu-id="97b1f-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="97b1f-188">Het scenario **Productievertragingen** configureren in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="97b1f-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="97b1f-189">Het scenario **Productievertraging** genereert een melding als de productiedoorvoer onder een drempelwaarde daalt.</span><span class="sxs-lookup"><span data-stu-id="97b1f-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="97b1f-190">In dit scenario wordt een **PartOut**-signaal naar de IoT-hub verzonden voor elk geproduceerd artikel.</span><span class="sxs-lookup"><span data-stu-id="97b1f-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="97b1f-191">In Supply Chain Management wordt de ordervertraging berekend op basis van de duur van de geplande productieorder, het aantal artikelen dat moet worden geproduceerd, hoe lang de taak actief is en hoeveel **PartOut**-signalen zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="97b1f-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="97b1f-192">Er wordt een vertragingsmelding gegenereerd als het aantal **PartOut**-signalen voor de taak onder de drempelwaarde van de verwachte waarde daalt.</span><span class="sxs-lookup"><span data-stu-id="97b1f-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="97b1f-193">Het scenario heeft de volgende afhankelijkheden:</span><span class="sxs-lookup"><span data-stu-id="97b1f-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="97b1f-194">Er moet een productieorder worden uitgevoerd op een toegewezen machine om een waarschuwing te kunnen activeren.</span><span class="sxs-lookup"><span data-stu-id="97b1f-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="97b1f-195">Er moet een signaal dat overeenkomt met een PartOut-signaal voor een toegewezen machine met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="97b1f-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="97b1f-196">Er moet een Unix-eigenschap tijdstempel milliseconden aanwezig zijn in het IoT-hub-bericht.</span><span class="sxs-lookup"><span data-stu-id="97b1f-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="97b1f-197">Een scenario uitschakelen</span><span class="sxs-lookup"><span data-stu-id="97b1f-197">How to disable a scenario</span></span>

<span data-ttu-id="97b1f-198">Voer de volgende stappen uit om een scenario uit te schakelen:</span><span class="sxs-lookup"><span data-stu-id="97b1f-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="97b1f-199">Navigeer in Supply Chain Management naar **Productiebeheer \> Instellingen \> IoT-intelligentie \> Scenariobeheer**.</span><span class="sxs-lookup"><span data-stu-id="97b1f-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="97b1f-200">Klik op **Configureren** in het scenario.</span><span class="sxs-lookup"><span data-stu-id="97b1f-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="97b1f-201">Klik op **Volgende** om naar het laatste tabblad van de wizard te gaan.</span><span class="sxs-lookup"><span data-stu-id="97b1f-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="97b1f-202">Schakel de schuifregelaar in om het scenario uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="97b1f-202">Toggle the slider to disable the scenario.</span></span>

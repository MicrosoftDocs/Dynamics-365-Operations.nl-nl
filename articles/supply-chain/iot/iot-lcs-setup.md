---
title: De invoegtoepassing IoT-intelligentie installeren in LCS
description: In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS).
author: tonyafehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89d2f53a761085949885c987d664654c3423524b
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645072"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>De invoegtoepassing IoT-intelligentie installeren in LCS

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS). Invoegtoepassingen kunnen niet worden geïnstalleerd in een demo-/proefomgeving. Voordat u de invoeg toepassing kunt installeren, moet u [de Azure-resources maken](iot-azure-setup.md).

U kunt IoT-intelligentie instellen en configureren zonder code te schrijven. Hier volgen de basisstappen.

1. [Azure-bronnen instellen](iot-azure-setup.md): maak een IoT-hub, een Redis-cache en een sleutelkluis die toegankelijk is vanuit Supply Chain Management.
2. [Indelingen voor berichtschema's voor IoT-hub](iot-schema-format.md): configureer uw apparaten om berichten naar IoT-hub te verzenden en om de JSON-berichtenindeling (JavaScript Object Notation) te definiëren.
3. Schakel in Functiebeheer de functie IoT-intelligentie in.
4. Installeer de invoegtoepassing IoT-intelligentie in Microsoft Dynamics Lifecycle Services (LCS): installeer de invoegtoepassing in LCS en configureer de Azure-geheimen (zoals beschreven in dit onderwerp).
5. [Metrische gegevens instellen](iot-metrics-setup.md): stel metrische gegevens in Supply Chain Management in.
6. [Scenario-instellingen](iot-scenario-setup.md): stel de scenario's in Supply Chain Management in.

## <a name="set-up-the-lcs-environment"></a>De LCS-omgeving instellen

1. Open LCS en ga naar uw Microsoft Dynamics 365 Supply Chain Management-omgeving.
2. Schuif naar de sectie **Invoegtoepassingen voor omgeving**.
3. Selecteer **Een nieuwe invoegtoepassing installeren** om de lijst met invoegtoepassingen weer te geven die zijn ingeschakeld voor de omgeving.
4. Selecteer in het dialoogvenster **Een invoegtoepassing selecteren voor installatie** de optie **IoT-intelligentie**.
5. Geef in het dialoogvenster **Invoegtoepassing instellen** de details op van uw IOT-hub en Redis-cache. U kunt de vereiste waarden vinden in de sleutelkluis die u hebt gemaakt in [Azure-resources maken](iot-azure-setup.md).

    + **Tenant-id**: ga in de Azure-portal naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **Directory-id**. Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.
    + **URI van sleutelkluis voor eindpunt dat compatibel is met IoT Event hub**: ga naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **DNS-naam**. Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.
    + **Geheime naam van eindpunt dat compatibel is met IoT Event hub**: ga naar de sleutelkluis, selecteer in het linkernavigatiedeelvenster de optie **Geheimen** en kopieer de naam van het geheim waar de verbindingsreeks van de Event hub voor de IoT-hub is opgeslagen. Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.
    + **URI van sleutelkluis voor Redis-cache**: ga naar de sleutelkluis en selecteer vervolgens in het linkernavigatiedeelvenster de optie **Overzicht** en kopieer de waarde voor **DNS-naam**. Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.
    + **Geheime naam van eindpunt voor Redis-cache**: ga naar de sleutelkluis, selecteer in het linkernavigatiedeelvenster de optie **Geheimen** en kopieer de naam van het geheim waar de verbindingsreeks voor de Redis-cache is opgeslagen. Plak die waarde in het dialoogvenster **Invoegtoepassing instellen**.

6. Schakel het selectievakje in om de voorwaarden te accepteren.
7. Selecteer **Installeren**.
8. Er verschijnt een berichtvenster met de mededeling dat de invoegtoepassing is geactiveerd voor installatie. Selecteer **OK**.

LCS-instelling is nu voltooid. De volgende stap is het [instellen van de scenario's](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>De invoegtoepassing verwijderen

1. [Schakel de scenario's uit](iot-scenario-setup.md#disable-a-scenario) in Supply Chain Management.
2. Ga in LCS naar de details van uw Supply Chain Management-omgeving.
3. Schuif naar de sectie **Invoegtoepassingen voor omgeving**.
4. Selecteer **Verwijderen** voor de invoegtoepassing IoT-intelligentie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
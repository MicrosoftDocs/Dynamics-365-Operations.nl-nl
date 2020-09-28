---
title: De invoegtoepassing IoT-intelligentie installeren in LCS
description: In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
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
ms.openlocfilehash: ae6b36c40d2f2f9e5266dfb3e2d1cbbb57755222
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803086"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>De invoegtoepassing IoT-intelligentie installeren in LCS

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de invoegtoepassing IoT-intelligentie kunt installeren in Microsoft Dynamics Lifecycle Services (LCS). Invoegtoepassingen kunnen niet worden geïnstalleerd in een demo-/proefomgeving. Voordat u de invoeg toepassing kunt installeren, moet u [de Azure-resources maken](iot-azure-setup.md).

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

1. [Schakel de scenario's uit](iot-scenario-setup.md#how-to-disable-a-scenario) in Supply Chain Management.
2. Ga in LCS naar de details van uw Supply Chain Management-omgeving.
3. Schuif naar de sectie **Invoegtoepassingen voor omgeving**.
4. Selecteer **Verwijderen** voor de invoegtoepassing IoT-intelligentie.

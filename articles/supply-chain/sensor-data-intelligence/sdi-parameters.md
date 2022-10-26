---
title: Parameters van Sensor Data Intelligence
description: Dit artikel biedt informatie over configuratie-instellingen die beschikbaar zijn op de pagina Parameters van Sensor Data Intelligence.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689368"
---
# <a name="sensor-data-intelligence-parameters"></a>Parameters van Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

De pagina **Parameters van Sensor Data Intelligence** bevat diverse instellingen die u kunt gebruiken om de functie te configureren. Deze instellingen omvatten verbindingsparameters voor Azure en een parameter voor de levensduur van waarschuwingsberichten die naar gebruikers worden verzonden als reactie op sensorgegevens.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Verbindingsgegevens voor uw Azure IoT-oplossing lezen en wijzigen

Meestal stelt u uw Azure IoT-oplossing in en koppelt u deze met Microsoft Dynamics 365 Supply Chain Management via de pagina **Azure-resources implementeren en verbinden**, waar u door beide procedures wordt geleid. Meer informatie over dit onderwerp vindt u in [Een IoT-oplossing implementeren op Azure](sdi-deploy-iot-solution-on-azure.md). U kunt de verbindingsdetails op elk moment weergeven en bewerken in Supply Chain Management door deze stappen uit te voeren.

1. Ga naar **Systeembeheer \> Instellingen \> Sensor Data Intelligence \> Parameters van Sensor Data Intelligence**.
1. Voer op het tabblad **Tijdreeks** in het veld **Verbindingsreeks voor metrische opslag (Redis)** de waarde voor **Primaire verbindingsreeks (StackExchange.Redis)** in voor de Azure IoT-oplossing waarmee u verbinding wilt maken. Hoe u deze waarde vindt, wordt uitgelegd in [Een IoT-oplossing implementeren op Azure](sdi-deploy-iot-solution-on-azure.md).
1. Voer op het tabblad **Integraties** in het veld **Client-ID van Azure AD-toepassing** de **client-ID**-waarde in voor de Azure IoT-oplossing waarmee u verbinding wilt maken. Hoe u deze waarde vindt, wordt uitgelegd in [Een IoT-oplossing implementeren op Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>De levensduur van waarschuwingsberichten instellen

Telkens wanneer Sensor Data Intelligence detecteert dat er een situatie is die aandacht van de gebruiker behoeft, wordt een melding naar de relevante gebruiker gestuurd. Om te voorkomen dat deze meldingen zich ophopen in het systeem, moet u instellen dat deze na een paar dagen verlopen.

1. Ga naar **Systeembeheer \> Instellingen \> Sensor Data Intelligence \> Parameters van Sensor Data Intelligence**.
1. Voer op het tabblad **Meldingen** in het veld **Dagen dat melding actief is** het aantal dagen dat een melding moet worden bewaard. Nadat de opgegeven tijd is verstreken, wordt de melding verwijderd.

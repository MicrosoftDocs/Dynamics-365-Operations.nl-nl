---
title: Azure-resources instellen voor IoT-intelligentie
description: In dit onderwerp wordt uitgelegd hoe u de Microsoft Azure-resources maakt en configureert die u nodig hebt voor IoT-intelligentie.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b605f283bc53c1c5b87ad88d4f19aeba9737e00563290413f3cb75b4e20dbbde
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774868"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Azure-resources instellen voor IoT-intelligentie

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de Microsoft Azure-resources maakt en configureert die u nodig hebt voor IoT-intelligentie.

## <a name="create-azure-resources"></a>Azure-resources maken

Voer de volgende stappen uit om een IoT-hub, een Redis-cache en een sleutelkluis te maken die toegankelijk zijn voor Microsoft Dynamics 365 Supply Chain Management.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Controleren of de app-id voor de Microsoft Dynamics ERP Microservices first-party app in uw tenant is opgenomen

Ga als volgt te werk om te controleren of de app-id voor de Microsoft Dynamics ERP Microservices first-party app in uw tenant is opgenomen.

1. Meld u aan bij de Azure-portal op <https://portal.azure.com>.
2. Ga naar **Azure Active Directory**.
3. Ga naar **ondernemingstoepassingen**.
4. Selecteer in het veld **Toepassingstype** de optie **Microsoft-toepassingen**.
5. Voer in het zoekveld **Microsoft Dynamics ERP Microservices** in.
6. Controleer of **Microsoft Dynamics ERP Microservices** in de lijst staat. Andere toepassingen hebben vergelijkbare namen. Let er daarom op dat u de juiste toepassing zoekt. De app-id is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Als de toepassing niet in de lijst staat, moet u deze aan uw tenant toevoegen:

    1. Selecteer in de Azure-portal op de werkbalk de knop om Azure Cloud Shell te openen.
    2. Voer de opdracht **install-module AzureAD** uit. Voer **Y** in om de module te installeren.
    3. Voer de opdracht **Get-InstalledModule-name "AzureAD"** uit om te controleren of de module is geïnstalleerd.
    4. Voer de opdracht **Connect-AzureAD-confirm** uit om de verificatie uit te voeren.
    5. Voer de opdracht **New-AzureADServicePrincipal-AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** uit.

    U kunt nu stap 1 tot en met 6 herhalen om te controleren of de app-id zich in uw tenant bevindt.

### <a name="create-a-key-vault-resource"></a>Een sleutelkluisresource maken

Volg deze stappen om een sleutelkluisresource te maken.

1. Maak of zoek een resourcegroep in de Azure-portal.
2. Selecteer **Toevoegen**.
3. Voer op de pagina **Nieuw** in het zoekveld de term **sleutelkluis** in. Selecteer vervolgens **Maken**.
4. Voer op de pagina **Sleutelkluis maken** in het veld **Naam sleutelkluis** een naam in.
5. Controleer de standaardwaarden en selecteer vervolgens **Controleren + maken**.
6. Selecteer **Maken**.

De sleutelkluis wordt op de achtergrond gemaakt.

### <a name="create-an-iot-hub-resource"></a>Een IoT-hub-resource maken

Volg deze stappen om een IoT-hub-resource te maken.

1. Maak of zoek een resourcegroep.
2. Selecteer **Toevoegen**.
3. Voer op de pagina **Nieuw** in het zoekveld de term **IoT-hub** in. Selecteer vervolgens **Maken**.
4. Voer vervolgens in het veld **Naam IoT-hub** een naam in.
5. Controleer de standaardwaarden en selecteer vervolgens **Controleren + maken**.
6. Selecteer **Maken**.

De IoT-hub wordt op de achtergrond gemaakt.

> [!NOTE]
> We raden u aan om slechts één IoT-hub-resource per omgeving te maken.

### <a name="create-a-redis-cache-resource"></a>Een Redis-cacheresource maken

Volg deze stappen om een Redis-cacheresource te maken.

1. Maak of zoek een resourcegroep.
2. Selecteer **Toevoegen**.
3. Voer op de pagina **Nieuw** in het zoekveld de term **Azure-cache voor Redis** in. Selecteer vervolgens **Maken**.
4. Voer in het veld **DNS-naam** een naam in.
5. Controleer de standaardwaarden en selecteer vervolgens **Maken**.

De Redis-cache wordt op de achtergrond gemaakt.

> [!NOTE]
> We raden u aan om slechts één Redis-cache per omgeving te maken.

Alle resources zijn nu gemaakt.

## <a name="configure-the-azure-resources"></a>De Azure-resources configureren

### <a name="configure-the-iot-hub"></a>De IoT-hub configureren

Volg deze stappen om de IoT-hub te configureren.

1. Selecteer de IoT-hub-resource in uw resources.
2. Selecteer **Ingebouwde eindpunten** in het navigatievenster aan de linkerkant.
3. Plak onder **Consumentengroepen** de volgende consumentengroepen. Deze consumentengroepen komen overeen met de kant-en-klare scenario's.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>De sleutelkluis configureren

Ga als volgt te werk om de sleutelkluis te configureren.

1. Selecteer de sleutelkluisresource in uw resources.
2. Selecteer **Toegangsbeleid** in het navigatievenster aan de linkerkant.
3. Selecteer **Een toegangsbeleid toevoegen**.
4. Selecteer op de pagina **Toegangsbeleid toevoegen** in het veld **Geheime machtigingen** de optie **Ophalen** en **Lijst**.
5. Klik op **Principal selecteren**.
6. Zoek in het dialoogvenster **Principal** de optie **Microsoft Dynamics ERP Microservices** en selecteer deze. Selecteer vervolgens **Selecteren**.
7. Selecteer **Toevoegen**.
8. Selecteer **Opslaan**.

De app heeft nu toegang tot de geheimen in de sleutelkluis.

### <a name="save-the-iot-hub-connection-string-secret"></a>Het geheim voor de IoT-hub-verbindingsreeks opslaan

Voer de volgende stappen uit om het geheim voor de IoT-hub-verbindingsreeks op te slaan:

1. Selecteer de IoT-hub-resource in uw resources.
2. Selecteer **Ingebouwde eindpunten** in het navigatievenster aan de linkerkant.
3. Kopieer de waarde in het veld **Eindpunt dat compatibel is met Event hub**.
4. Ga naar de sleutelkluisresource.
5. Selecteer **Geheimen** in het navigatievenster aan de linkerkant.
6. Selecteer **Genereren/Importeren**.
7. Voer in het veld **Naam** een naam in.
8. Plak in het veld **Waarde** de eindpuntwaarde die u eerder hebt gekopieerd.
9. Selecteer **Maken**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Het geheim voor de Redis-cacheverbindingsreeks opslaan

Voer de volgende stappen uit om het geheim voor de Redis-cacheverbindingsreeks op te slaan:

1. Selecteer de Redis-cacheresource in uw resources.
2. Selecteer **Toegangssleutels**.
3. Kopieer de waarde in het veld **Primaire verbindingsreeks**.
4. Ga naar de sleutelkluisresource.
5. Selecteer **Geheimen** in het navigatievenster aan de linkerkant.
6. Selecteer **Genereren/Importeren**.
7. Voer in het veld **Naam** een naam in.
8. Plak in het veld **Waarde** de verbindingstekenreeks die u eerder hebt gekopieerd.
9. Selecteer **Maken**.

> [!NOTE]
> Telkens wanneer u een van de verbindingsreeksen bijwerkt, moet u ook de geheime waarden bijwerken.

U bent nu klaar met het inrichten van de vereiste Azure-resources. De volgende stap is het [installeren van de invoegtoepassing IoT-intelligentie in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

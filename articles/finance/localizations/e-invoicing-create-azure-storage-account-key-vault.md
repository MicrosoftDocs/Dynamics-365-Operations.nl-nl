---
title: Een Azure-opslagaccount en een sleutelkluis maken
description: In dit onderwerp wordt uitgelegd hoe u een Azure-opslagaccount en een sleutelkluis maakt.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104224"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Een Azure-opslagaccount en een sleutelkluis maken

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Vereisten

Voordat u de stappen in dit onderwerp kunt voltooien, moet u controleren of de volgende zijn uitgevoerd:

- Maak een sleutelkluis-resource in Azure. Zie [Over Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview) voor meer informatie.
- Maak een Azure-opslagaccount (Blob-opslag). Zie [Azure-opslagaccount onderhouden](https://docs.microsoft.com/azure/storage/blobs/) voor meer informatie.

## <a name="overview"></a>Overzicht

In dit onderwerp voert u twee belangrijke stappen uit:

- Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen.
- Stel de sleutelkluis in om de URI van het opslagaccount op te slaan.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen

1. Open het opslagaccount dat u wilt gebruiken met de invoegtoepassing voor elektronische facturering.
2. Ga naar **Blob-service** \> **Containers** en maak een nieuwe container.
3. Voer een naam in voor de container en stel het veld **Openbaar toegangsniveau** in op **Privé (geen anonieme toegang)**.
4. Open de container en ga naar **instellingen \> Toegangsbeleid**.
5. Selecteer **Beleid toevoegen** om een opgeslagen toegangsbeleid toe te voegen.
6. Stel de velden **ID** en **Machtigingen** naar wens in. In het veld **Machtigingen** moet u alle machtigingen selecteren.

    ![Machtiging voor Blob-opslag verlenen](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Voer de begin- en vervaldatum in. De vervaldatum moet in de toekomst liggen.
8. Selecteer **OK** om het beleid op te slaan en sla uw wijzigingen vervolgens op in de container.
9. Ga terug naar het opslagaccount en open **Opslagverkenner (Preview)**.
10. Klik met de rechtermuisknop op de container en selecteer **Shared Access Signature ophalen**.
11. Kopieer in het dialoogvenster **Shared Access Signature** de waarde in het veld **URI** en sla deze op. Deze waarde wordt in de volgende procedure gebruikt en wordt de *Shared Access Signature-URI* genoemd.

    ![De URI-waarde selecteren en kopiëren](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Stel de sleutelkluis in om de URI van het opslagaccount op te slaan

1. Open de sleutelkluis die u wilt gebruiken met de invoegtoepassing voor elektronische facturering.
2. Ga naar **instellingen** \> **Geheimen** en selecteer **Genereren/importeren** om een nieuw geheim te maken.
3. Selecteer op de pagina **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.
4. Voer de naam van het geheim in. Deze naam wordt gebruikt tijdens de installatie van de service in Regulatory Configuration Service (RCS) en wordt de *geheime naam van de sleutelkluis* genoemd.
5. Selecteer in het veld **Waarde** de **Shared Access Signature URI** en selecteer **Maken**.
6. Stel het toegangsbeleid in om de invoegtoepassing voor elektronische facturering het juiste niveau van beveiligde toegang te verlenen tot het geheim dat u hebt gemaakt. Ga naar **Instellingen \> Toegangsbeleid** en selecteer **Toegangsbeleid toevoegen**.
7. Stel de geheime machtigingen voor de bewerkingen **Get** en **List** in.

    ![Toegang tot de service verlenen](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Stel de certificaatmachtigingen voor de bewerkingen **Get** en **List** in.

    ![Certificaatmachtiging verlenen](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Selecteer in het veld **Principal** de principal door **Invoegtoepassing voor elektronische facturering** toe te voegen.
10. Selecteer **Toevoegen** en selecteer **Sleutelkluiswijzigingen opslaan**.
11. Kopieer op de pagina **Overzicht** de **DNS-naam**-waarde voor de sleutelkluis. Deze waarde wordt gebruikt tijdens de installatie van de service in RCS en wordt de *sleutel-kluis-URI* genoemd.

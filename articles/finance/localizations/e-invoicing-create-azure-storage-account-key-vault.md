---
title: Een Azure-opslagaccount en een sleutelkluis aanmaken
description: In dit onderwerp wordt uitgelegd hoe u een Azure-opslagaccount en een sleutelkluis maakt.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463837"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Een Azure-opslagaccount en een sleutelkluis maken

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Vereisten

Voordat u de stappen in dit onderwerp kunt voltooien, moet u controleren of de volgende zijn uitgevoerd:

- Maak een sleutelkluis-resource in Azure. Zie [Over Azure Key Vault](/azure/key-vault/general/overview) voor meer informatie.
- Maak een Azure-opslagaccount (Blob-opslag). Zie [Azure-opslagaccount onderhouden](/azure/storage/blobs/) voor meer informatie.

## <a name="overview"></a>Overzicht

In dit onderwerp voert u twee belangrijke stappen uit:

- Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen.
- Stel de sleutelkluis in om de URI van het opslagaccount op te slaan.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen

1. Open het opslagaccount dat u wilt gebruiken met Elektronische facturering.
2. Ga naar **Gegevensopslag** > **Containers** en maak een nieuwe container aan.
3. Voer een naam in voor de container en stel het veld **Openbaar toegangsniveau** in op **Privé (geen anonieme toegang)**.
4. Open de container en ga naar **Instellingen** > **Toegangsbeleid**.
5. Selecteer **Beleid toevoegen** om een opgeslagen toegangsbeleid toe te voegen.
6. Stel de velden **ID** en **Machtigingen** naar wens in. In het veld **Machtigingen** moet u alle machtigingen selecteren.

    ![Machtiging voor Blob-opslag verlenen.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Voer de begin- en vervaldatum in. De vervaldatum moet in de toekomst liggen.
8. Selecteer **OK** om het beleid op te slaan en sla uw wijzigingen vervolgens op in de container.
9. Ga naar **Instellingen** > **Gedeelde toegangstokens** en stel de veldwaarden in. 
10. Voer de begin- en einddatum in. De einddatum moet in de toekomst liggen.
11. Selecteer in het veld **Machtigingen** de volgende machtigingen: **Lezen**, **Toevoegen**, **Aanmaken**, **Schrijven**, **Verwijderen** en **Opsommen**. 
12. Selecteer **HET SAS-token en de URL genereren**.
13. Kopieer de waarde en sla deze op in het veld **Blob SAS-URL**. Deze waarde wordt in de volgende procedure gebruikt en wordt de *Shared Access Signature-URI* genoemd.

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Stel de sleutelkluis in om de URI van het opslagaccount op te slaan

1. Open de sleutelkluis die u wilt gebruiken met Elektronische facturering.
2. Ga naar **instellingen** \> **Geheimen** en selecteer **Genereren/importeren** om een nieuw geheim te maken.
3. Selecteer op de pagina **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.
4. Voer de naam van het geheim in. Deze naam wordt gebruikt tijdens de installatie van de service in Regulatory Configuration Service (RCS) en wordt de *geheime naam van de sleutelkluis* genoemd.
5. Geef in het veld **Waarde** de URI voor de Shared Acess Signature op die u hebt gekopieerd in de vorige procedure en selecteer Vervolgens **Aanmaken**.
6. Stel het toegangsbeleid in om Elektronische facturering het juiste niveau van beveiligde toegang te verlenen tot het geheim dat u hebt gemaakt. Ga naar **Instellingen \> Toegangsbeleid** en selecteer **Toegangsbeleid toevoegen**.
7. Stel de geheime machtigingen voor de bewerkingen **Get** en **List** in.

    ![Toegang tot de service verlenen.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Stel de certificaatmachtigingen voor de bewerkingen **Get** en **List** in.

    ![Certificaatmachtiging verlenen.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Selecteer **Geen geselecteerd** in het veld **Principal selecteren**.
10. Selecteer in het dialoogvenster **Principal** de principal door **e-Factureringsservice** toe te voegen.
11. Selecteer **Toevoegen** en vervolgens **Opslaan**.
12. Kopieer op de pagina **Overzicht** de **DNS-naam**-waarde voor de sleutelkluis. Deze waarde wordt gebruikt tijdens de installatie van de service in RCS en wordt de *sleutel-kluis-URI* genoemd.

> [!NOTE]
> Als u extra beveiliging wilt op het opslagaccount, kunt u de Azure Defender for Storage configureren.
> 
> Meer informatie over dit onderwerp vindt u in [Inleiding op Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

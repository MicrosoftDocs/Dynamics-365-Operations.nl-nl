---
title: Power BI inschakelen voor Algemene voorraadboekhouding
description: In dit onderwerp wordt beschreven hoe u deze functie Microsoft Power BIkunt inschakelen voor Algemene voorraadboekhouding.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8be486409d60cc4927599816e30e1e4ab21a312a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669764"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Power BI inschakelen voor Algemene voorraadboekhouding

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

U kunt tegels, dashboards en rapporten vastzetten vanuit uw [PowerBI.com](https://powerbi.com/)-account naar uw Microsoft Dynamics 365-toepassingswerkruimte.

## <a name="prerequisites"></a>Vereisten

Aan de volgende vereisten moet zijn voldaan voordat u Power BI-rapportage kunt inschakelen:

- U moet een systeembeheerder zijn in de toepassing Dynamics 365.
- U moet over een [PowerBI.com](https://powerbi.com/)-account beschikken.
- U moet ten minste één dashboard en één rapport in uw Power BI-account hebben.
- U moet een beheerder zijn voor uw Azure AD-account (Azure Active Directory).
- Het Azure AD-domein moet hetzelfde domein zijn dat u hebt gebruikt voor uw [PowerBI.com](https://powerbi.com/)-account.

## <a name="setup"></a>Instelling

Volg deze stappen voor het instellen van de Power BI-integratie.

1. Meld u aan bij [Microsoft Dynamics LCS (LifeCycle Services)](https://lcs.dynamics.com/Logon/Index).
1. Ga naar de **Bibliotheek voor gedeelde activa**, selecteer een **Power BI-rapportmodel** als het activatype en download het pakket **Global Inventory Accounting** (Algemene voorraadboekhouding). 
1. Meld u aan bij [PowerBI.com](https://app.powerbi.com/) en ga als volgt te werk om het rapportbestand **Algemene voorraadboekhouding** van Power BI te uploaden:

    1. Selecteer **Nieuw**.
    1. Selecteer **Een bestand uploaden**.
    1. Selecteer het Power BI-rapportbestand **Algemene voorraadboekhouding**.

1. Configureer het Power BI-rapportbestand **Algemene voorraadboekhouding** als volgt:

    1. Ga naar **Mijn werkruimte**, zoek de gegevensset voor Algemene voorraadboekhouding en selecteer vervolgens **Instellingen** in het menu **Opties**.
    1. Vouw in **Instellingen voor Algemene voorraadboekhouding** de optie **Parameters** uit en werk alle parameters waar nodig bij. Controleer met name de volgende instellingen:
        1. Overschrijf de standaardwaarden voor **Dataverse-URL** door de waarden onder **Power Platform-omgevingsdetails** in LCS (in de sectie **Power Platform-integratie**).
        1. Overschrijf de standaardwaarden voor **Omgevings-id** door de waarden onder **Omgevingsdetails** in LCS (in de sectie **Omgeving beheren**).
        1. Selecteer de koppeling **Referenties bewerken** naast het label **CDS** in de sectie **Gegevensbronreferenties**. Meld u vervolgens aan bij uw Dataverse-account met de verificatiemethode **OAuth2**.
    1. Controleer of de Power BI-rapporten in **Mijn werkruimte \> Rapporten \> Algemene voorraadboekhouding** nu correct werken en inhoud van uw systeem weergeven.

1. Registreer de toepassing zoals beschreven in [Integratie van PowerBI.com configureren ](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Integreer het Power BI-rapportbestand **Algemene voorraadboekhouding** als volgt in Dynamics 365 Supply Chain Management:

    1. Ga naar **Systeembeheer \> Instellingen \> Configuratie PowerBI.com**.
    1. Selecteer **Bewerken**.
    1. Selecteer **Integratie PowerBI.com inschakelen**.
    1. Voer in het veld **Toepassings-id** de volgende id in:
    1. Voer in het veld **Toepassingssleutel** de volgende sleutel in:
    1. Selecteer **Opslaan**.

1. Vernieuw de pagina zodat het dialoogvenster voor aanmelding bij Power BI wordt weergegeven.
1. Selecteer op het tabblad **Opties** de optie **Rapportcatalogus openen** en selecteer vervolgens het Power BI--rapportbestand **Algemene voorraadboekhouding** dat u eerder hebt geüpload.
1. Vernieuw de pagina. Als het goed is, ziet u dat uw rapport is toegevoegd.
1. Selecteer onder **Power BI-rapporten** de koppeling **Algemene voorraadboekhouding**.

Zie [Integratie van PowerBI.com configureren](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md) voor meer informatie.

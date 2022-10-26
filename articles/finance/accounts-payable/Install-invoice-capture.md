---
title: De oplossing Invoice Capture installeren
description: Dit artikel biedt informatie over het installeren van de oplossing Invoice Capture en de integratie hiervan met Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691174"
---
# <a name="install-the-invoice-capture-solution"></a>De oplossing Invoice Capture installeren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Als u de oplossing in een beperkte preview hebt geïnstalleerd, moet u de oude oplossing verwijderen voordat u doorgaat.

## <a name="prerequisites"></a>Vereisten

Voordat u de oplossing Invoice Capture kunt installeren, moet u de volgende vereisten uitvoeren:

1. Registreer een toepassing en voeg een clientgeheim toe aan Microsoft Azure Active Directory (Azure AD) onder uw Azure-abonnement. Zie [Een webtoepassing registreren met ADD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad) voor meer informatie.

    > [!NOTE]
    > Zorg ervoor dat u de waarden voor **Client-id van toepassing**, **Clientgeheim** en **Tenant-id** noteert, omdat u ze later nodig hebt.

2. Registreer de toepassing Azure in een Dynamics 365 Finance-omgeving. Zie [Uw externe toepassing registreren](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application) voor meer informatie.

## <a name="install-and-set-up-the-solution"></a>De oplossing installeren en instellen

Als u de oplossing Invoice Capture wilt installeren, gaat u naar AppSource en selecteert u de koppeling voor de preview-versie van [Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Als de installatie is voltooid, is de oplossing geïnstalleerd in de geselecteerde omgeving in Power Apps.

Volg deze stappen om de instellingen te voltooien.

1. Download de [assistentoplossing](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) om de volgende details in te stellen:

    - De communicatie tussen Microsoft Power Platform en de Finance-omgeving
    - De verbindingsverwijzing voor Dataverse en Office 365 Outlook die door het kanaal wordt gebruikt

2. Ga in Power Apps naar uw omgeving en selecteer **Oplossing importeren**.
3. Selecteer **Bladeren**, selecteer het assistentoplossingspakket dat u hebt gedownload en selecteer vervolgens **Volgende**.
4. Selecteer **Volgende**.
5. Wijs een bestaande verbinding toe of maak een nieuwe verbinding door **Nieuwe verbinding** te selecteren.
6. Nadat het pakket is geïmporteerd, opent u **Dynamics 365 Invoice Capture – Installation Tools**.
7. Voer de cloudstroom uit om de verbinding in te stellen tussen de oplossing Invoice Capture in Microsoft Power Platform en Finance.
8. Selecteer **Uitvoeren** en geef de volgende parameters op:

    - **URL voor Dynamics 365 Finance**: de URL van de Finance-omgeving waarmee u wilt integreren.
    - **Tenant-id**: de tenant-id voor de Finance-omgeving.
    - **Client-id**: de Azure-toepassings-id die is geregistreerd.
    - **Clientgeheim**: het clientgeheim dat is gegenereerd voor de Azure-toepassing.

---
title: Aan de slag met Algemene voorraadboekhouding (Global Inventory Accounting)
description: In dit onderwerp wordt beschreven hoe u aan de slag gaat met Algemene voorraadboekhouding.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88f1e9ef8c8b2aa494c44ea3b33713adc470eb96
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384792"
---
# <a name="get-started-with-global-inventory-accounting"></a>Aan de slag met Algemene voorraadboekhouding (Global Inventory Accounting)

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Met Algemene voorraadboekhouding kunt u meerdere voorraadboekingen uitvoeren in de grootboeken voor Algemene voorraadboekhouding die u hebt ingesteld. U moet elk grootboek voor Algemene voorraadboekhouding aan een *conventie* koppelen. Een conventie is een verzameling van de volgende typen boekhoudbeleidsregels:

- Kostenobject
- Basis van invoermeting
- Veronderstelling van kostenstroom
- Kostenelement

> [!NOTE]
> Zelfs nadat u Algemene voorraadboekhouding hebt ingeschakeld, kunt u nog gewoon voorraadboekhouding uitvoeren in Microsoft Dynamics 365 Supply Chain Management.

Algemene voorraadboekhouding is een invoegtoepassing. Om de functies beschikbaar te maken, moet u deze installeren vanuit Microsoft Dynamics Lifecycle Services (LCS). U kunt ervoor kiezen om deze te evalueren in een testomgeving voordat u ze voor productie-omgevingen inschakelt.

Algemene voorraadboekhouding ondersteunt momenteel niet alle kostenbeheerfuncties die in Supply Chain Management zijn ingebouwd. Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is, voldoet aan uw behoeften.

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>Procedure voor het ophalen van de preview van Algemene voorraadboekhouding

> [!IMPORTANT]
> Als u Algemene voorraadboekhouding wilt gebruiken, moet u een omgeving met hoge beschikbaarheid voor LCS hebben (niet in een OneBox-omgeving). Daarnaast moet u Supply Chain Management versie 10.0.19 of hoger uitvoeren.

Als u zich wilt aanmelden voor de preview van Algemene voorraadboekhouding, verzendt u uw LCS-omgevings-id per e-mail naar het [team voor Algemene voorraadboekhouding](mailto:GlobalInvAccount@microsoft.com). Nadat u bent goedgekeurd voor het programma, verzendt het team u een opvolgings-e-mail met de bètasleutel voor Algemene voorraadboekhouding en uw service-eindpunten. Nadat u de bètasleutel hebt ontvangen, kunt u [de invoegtoepassing installeren](#install).

## <a name="licensing"></a>Licenties

Algemene voorraadboekhouding wordt samengevoegd met de standaardfuncties van kostenbeheer die beschikbaar zijn voor Supply Chain Management. U hoeft geen extra licentie aan te schaffen voor het gebruik van Algemene voorraadboekhouding.

## <a name="prerequisites"></a>Vereisten

### <a name="set-up-microsoft-power-platform-integration"></a>Microsoft Power Platform-integratie instellen

Voordat u de functionaliteit van de invoegtoepassing kunt inschakelen, moet u deze als volgt integreren in Microsoft Power Platform.

1. Open de LCS-omgeving waar u de service wilt toevoegen.
1. Ga naar **Volledige details**.
1. Selecteer **Instellingen** in de sectie **Power Platform**-integratie.
1. Schakel het selectievakje **Power Platformomgeving instellen** in het dialoogvenster in en selecteer **Instellingen**. Het instellen duurt doorgaans tussen de 60 en 90 minuten.
1. Nadat de instelling van de Microsoft Power Platform-omgeving is voltooid, wordt op de pagina de naam van uw omgeving weergegeven. Verder wordt in de sectie **Power Platform-integratie** de melding 'De instelling van de Power Platform-omgeving is voltooid' weergegeven. Voor Algemene voorraadboekhouding is geen toepassing voor twee keer wegschrijven vereist.

Zie [Inschakelen na de implementatie van de omgeving](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy) voor meer informatie.

### <a name="set-up-dataverse"></a>Dataverse instellen

Voer, voordat u Dataverse instelt, de volgende stappen uit om de serviceprincipes voor Algemene voorraadboekhouding toe te voegen aan uw tenant.

1. Installeer Azure AD-module voor Windows PowerShell v2, zoals beschreven in [Azure Active Directory PowerShell for Graph installeren](/powershell/azure/active-directory/install-adv2).
1. Voer de volgende PowerShell-opdracht uit.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Maak vervolgens met de volgende stappen toepassingsgebruikers voor Algemene voorraadboekhouding in Dataverse.

1. Open de URL van uw Dataverse-omgeving.
1. Ga naar **Geavanceerde instellingen \> Systeem \> \> Gebruikers** en maak een toepassingsgebruiker. Gebruik het veld **Weergeven** om de paginaweergave te wijzigen in *Toepassingsgebruikers*.
1. Selecteer **Nieuw**.
1. Stel het veld **Toepassings-ID** in op *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Selecteer **Rol toewijzen** en selecteer vervolgens *Systeembeheerder*. Als er een rol is met de naam *Common Data Service-gebruiker*, selecteert u ook deze rol.
1. Herhaal de voorgaande stappen, maar stel het veld **Toepassings-id** in op *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Zie [Een toepassingsgebruiker maken](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user) voor meer informatie.

Als de standaardtaal van uw Dataverse-installatie niet Engels is, volgt u deze stappen.

1. Ga naar **Geavanceerde instelling \> Beheer \> Talen**.
1. Selecteer *Engels* (*LanguageCode=1033*) en selecteer vervolgens **Toepassen**.

## <a name="install-the-add-in"></a><a name="install"></a>De invoegtoepassing installeren

Voer deze stappen uit om de invoegtoepassing te installeren zodat u Algemene voorraadboekhouding kunt gebruiken.

1. [Registreer u](#sign-up) voor de preview van Algemene voorraadboekhouding.
1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index).
1. Ga naar **Beheer van previewfuncties**.
1. Selecteer het plusteken (**+**).
1. Voer in het veld **Code** uw bètasleutel voor de invoegtoepassing Algemene voorraadboekhouding in. (U zou uw bètasleutel per e-mail moeten hebben ontvangen toen u zich registreerde.)
1. Selecteer **Deblokkeren**.
1. Open de LCS-omgeving waar u de service wilt toevoegen.
1. Ga naar **Volledige details**.
1. Ga naar **Power Platform-integratie** en selecteer **Instelling**.
1. Schakel het selectievakje **Power Platformomgeving instellen** in het dialoogvenster in en selecteer **Instellingen**. Het instellen duurt doorgaans tussen de 60 en 90 minuten.
1. Nadat u de Microsoft Power Platform-omgeving hebt ingesteld, selecteert u op het sneltabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
1. Selecteer **Global Inventory Accounting** (Algemene voorraadboekhouding).
1. Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.
1. Selecteer **Installeren**.
1. Op het sneltabblad **Invoegtoepassingen voor omgeving** ziet u dat Algemene voorraadboekhouding wordt geïnstalleerd. Na enkele minuten verandert de status van *Bezig met installeren* in *Geïnstalleerd*. (Mogelijk moet u de pagina vernieuwen om deze wijziging te zien.) Op dat moment is Algemene voorraadboekhouding klaar voor gebruik.

## <a name="set-up-the-integration"></a>De integratie instellen

Volg deze stappen om de integratie in te stellen tussen Global Inventory Accounting en Supply Chain Management.

1. Meld u aan bij Supply Chain Management.
1. Ga naar **Systeembeheer \> Functiebeheer**.
1. Selecteer **Controleren op updates**.
1. Zoek op het tabblad **Alle** naar de functie genaamd *(Preview) Algemene voorraadboekhouding*.
1. Selecteer **Nu inschakelen**.
1. Ga naar voor **Algemene voorraadboekhouding \> Instellen \> Parameters algemene voorraadboekhouding \> Integratieparameters**.
1. In de velden **Dataservice-eindpunt** en **Eindpunt voor algemene voorraadboekhouding** voert u de URL's in uit de e-mail die het team van Global Inventory Accounting heeft verzonden toen u zich hebt geregistreerd voor de preview.

Global Inventory Accounting is nu klaar voor gebruik.

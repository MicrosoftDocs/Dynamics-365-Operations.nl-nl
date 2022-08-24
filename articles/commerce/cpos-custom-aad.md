---
title: CPOS configureren om een aangepaste Azure AD-app te gebruiken
description: In dit artikel wordt uitgelegd hoe u Cloud POS (CPOS) configureert om een aangepaste Azure Active Directory (Azure AD)-app te gebruiken.
author: boycez
ms.date: 08/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: baa0c3da25308345037b5dd1b4c5907d6213e7f7
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/03/2022
ms.locfileid: "9222965"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>CPOS configureren om een aangepaste Azure AD-app te gebruiken

[!include [banner](includes/banner.md)]

Standaard wijst Cloud POS (CPOS) in Microsoft Dynamics 365 Commerce naar een geregistreerde eigen Microsoft-app in Azure Active Directory (Azure AD). Daarom kunt u CPOS gebruiken zonder wijzigingen aan te brengen in Azure AD. U wilt uw exemplaar van CPOS echter misschien naar een aangepaste Azure AD-app laten wijzen die u beheert. In dit artikel wordt uitgelegd hoe u CPOS configureert om een aangepaste Azure AD-app te gebruiken.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Een aangepaste Retail Server-app instellen in Azure AD

Voer de volgende stappen uit om een aangepaste Retail Server-app in Azure AD te maken en configureren.

1. Meld u aan bij het [Azure Active Directory-beheercentrum](https://aad.portal.azure.com) met een willekeurige Azure AD-gebruikersaccount. De gebruikersaccount hoeft geen beheerdermachtigingen te hebben.
1. Selecteer **Azure Active Directory**.
1. Selecteer **App-registraties** en selecteer vervolgens **Nieuwe registratie** om het dialoogvenster **Een toepassing registreren** te openen.
1. Stel de volgende velden in:

    - **Naam**: voer een eigen naam in voor de app. Voer bijvoorbeeld **Aangepaste Retail Server** in.
    - **Ondersteunde accounttypen**: selecteer de standaardoptie **Alleen accounts in deze organisatiemap (alleen Microsoft - enkele tenant)** geselecteerd.
    - **Omleidings-URI**: dit is een optioneel veld. Laat dit leeg.
    - **Servicestructuur-id**: dit is een optioneel veld. Laat dit leeg.
    
1. Selecteer **Registreren**. De configuratiepagina voor de nieuwe geregistreerde app wordt weergegeven.
1. In de sectie **Overzicht \> Essentials** selecteert u **Een URI voor de toepassings-id toevoegen** en vervolgens selecteert u **Instellen** naast **URI van toepassings-id**. Maak een notitie van de voorgestelde waarde en selecteer **Opslaan** om die waarde te accepteren. 
1. Selecteer **Bereik toevoegen** en stel daarna de volgende velden in:

    - **Bereiknaam**: voer een aangpaste naam in voor het bereik. Voer bijvoorbeeld **Legacy.Access.Full** in .
    - **Wie kan toestemming geven**: geef op of zowel beheerders als gebruikers of alleen beheerders toestemming kunnen geven op basis van het beveiligingsbeleid van uw organisatie.
    - **Weergavenaam van beheerderstoestemming**: geef een weergavenaam op. Voer bijvoorbeeld **Toegang tot Retail Server** in.
    - **Beschrijving van beheerderstoestemming**: voer een beschrijving in. Voer bijvoorbeeld **Geeft toegang tot Retail Server** in.

1. Selecteer **Bereik toevoegen** om het aanmaakproces van het bereik te voltooien.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Een aangepaste CPOS-app instellen in Azure AD

Voer de volgende stappen uit om een aangepaste CPOS-app in Azure AD te maken en configureren.

1. Meld u aan bij het [Azure Active Directory-beheercentrum](https://aad.portal.azure.com) met een willekeurige Azure AD-gebruikersaccount. De gebruikersaccount hoeft geen beheerdermachtigingen te hebben.
1. Selecteer **Azure Active Directory**.
1. Selecteer **App-registraties** en selecteer vervolgens **Nieuwe registratie** om het dialoogvenster **Een toepassing registreren** te openen.
1. Stel de volgende velden in:

    - **Naam**: voer een naam voor de app in. Voer bijvoorbeeld **Aangepaste Cloud POS** in.
    - **Ondersteunde accounttypen**: selecteer de standaardoptie **Alleen accounts in deze organisatiemap (alleen Microsoft - enkele tenant)** geselecteerd.
    - **Omleidings-URI**: selecteer **Toepassing met één pagina** in de vervolgkeuzelijst en voer uw CPOS -URI in.
    - **Servicestructuur-id**: dit is een optioneel veld. Laat dit leeg.

1. Selecteer **Registreren**. De configuratiepagina voor de nieuwe geregistreerde app wordt weergegeven.
1. Stel in de sectie **Manifest** de parameters **oauth2AllooauthwIdTokenImplicitFlow** en **oauth2AllowImplicitFlow** in op **waar** en selecteer **Opslaan**.
1. Volg deze stappen in de sectie **Tokenconfiguratie** om twee claims toe te voegen:

    - Selecteer **Optionele claim toevoegen**. Stel het veld **Tokentype** in op **Id** en selecteer vervolgens de **sid**-claim. Selecteer **Toevoegen**.
    - Selecteer **Optionele claim toevoegen**. Stel het veld **Tokentype** in op **Toegang** en selecteer vervolgens de **sid**-claim. Selecteer **Toevoegen**.

1. Selecteer in de sectie **API-machtigingen** de optie **Een machtiging toevoegen**.
1. Zoek op het tabblad **API's die in mijn organisatie worden gebruikt** naar de Retail Server-app die u hebt gemaakt in de sectie [Een aangepaste Retail Server-app instellen in Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad). Selecteer vervolgens **Machtigingen toevoegen**.
1. Noteer in de sectie **Overzicht** de waarde uit het veld **Id van toepassing (client)**.

## <a name="update-the-cpos-configuration-file"></a>Het CPOS-configuratiebestand bijwerken

Open het bestand config.json van CPOS en werk het op de volgende manier bij.

1. Vervang de sleutelwaarde **AADClientId** door de waarde van **Id van toepassing (client)** van de aangepaste CPOS-app die u hebt gemaakt in de sectie [Een aangepaste CPOS-app in Azure AD instellen](#set-up-a-custom-cpos-app-in-azure-ad).
1. Vervang de sleutelwaarde **AADRetailServerResourceId** door de waarde van **URI van toepassings-id** van de aangepaste Retail Server-app die u hebt gemaakt in de sectie [Een aangepaste Retail Server-app in Azure AD instellen](#set-up-a-custom-retail-server-app-in-azure-ad).

CPOS gebruikt beide parameters wanneer het aanvragen verzendt naar Azure AD om een beveiligingstoken te verkrijgen.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Instellingen voor identiteitsproviders bijwerken in Commerce headquarters

Vervolgens moet u instellingen voor identiteitsproviders bijwerken in Commerce headquarters.

1. Open in Commerce headquarters de pagina **Gedeelde Commerce-parameters**.
1. Selecteer op het tabblad **Identiteitsproviders** in de sectie **Identiteitsproviders** de rij waar het veld **Type** is ingesteld op **Azure Active Directory** en het veld **Uitgever** wijst naar uw Azure AD-tenant. Met deze instelling wordt gemeld dat u werkt met onderliggende rasters die de gegevens bevatten met betrekking tot de identiteitsprovider die overeenkomt met uw Azure AD-tenant.
1. Selecteer in de sectie **Relying party´s** de optie **Toevoegen** om een rij toe te voegen.
1. Stel de volgende velden in:

    - **ClientId**: voer de waarde in van **Id van toepassing (client)** van de aangepaste CPOS-app die u hebt gemaakt in de sectie [Een aangepaste CPOS-app in Azure AD instellen](#set-up-a-custom-cpos-app-in-azure-ad).
    - **Type**: selecteer **Openbaar**.
    - **UserType**: selecteer **Medewerker**.

1. Selecteer de rij die u hebt toegevoegd. In de sectie **Serverresource-id's** onder de sectie **Relying party´s** worden de Retail Server-app-id's weergegeven die toegankelijk zijn via de app die u hebt geselecteerd in het raster **Relying party´s**.
1. Selecteer in de sectie **Serverresource-id's** de optie **Toevoegen** om een rij toe te voegen.
1. Voer in het veld **Serverresource-id** de waarde in van **URI van toepassings-id** van de aangepaste Retail Server-app die u hebt gemaakt in de sectie [Een aangepaste Retail Server-app in Azure AD instellen](#set-up-a-custom-retail-server-app-in-azure-ad).

    > [!IMPORTANT]
    > Alle velden die in de voorgaande stappen worden genoemd, zijn hoofdlettergevoelig. De waarden die u moet invoeren, moeten exact overeenkomen met de waarden die zijn geconfigureerd in het Azure AD-beheercentrum.

1. Ga naar **Retail en commerce IT \> Distributieplanning** en voer taak **1110** (**Algemene configuratie**) uit.

U kunt nu CPOS-apparaten activeren met uw eigen Azure AD-app.

## <a name="additional-resources"></a>Aanvullende bronnen

[POS (point-of-sale)-activering van apparaten](dev-itpro/retail-device-activation.md)

[Activeringsaccounts beheren en apparaten valideren](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

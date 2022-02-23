---
title: Aangepaste pagina's voor gebruikersaanmeldingen instellen
description: In dit onderwerp wordt beschreven hoe u aangepaste pagina's maakt in Microsoft Dynamics 365 Commerce voor het verwerken van aangepaste aanmeldingen voor gebruikers van B2C-tenants (business-to-consumers) met Azure Active Directory (Azure AD).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a55da9683c43ac75109fd256e481b02a4d565914
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970073"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Aangepaste pagina's voor gebruikersaanmeldingen instellen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u aangepaste pagina's maakt in Microsoft Dynamics 365 Commerce voor het verwerken van aangepaste aanmeldingen voor gebruikers van B2C-tenants (business-to-consumers) met Azure Active Directory (Azure AD).

## <a name="overview"></a>Overzicht

Als u aangepaste pagina's wilt gebruiken die zijn gemaakt in Dynamics 365 Commerce waarin de aanmeldingsgegevens van gebruikers worden afgehandeld, moet u het Azure AD-beleid instellen waarnaar wordt verwezen in de Commerce-omgeving. U kunt Azure AD B2C-beleidsregels configureren voor 'Registreren en aanmelden', 'Profiel bewerken' en 'Wachtwoord opnieuw instellen' met behulp van de Azure AD B2C-toepassing. Vervolgens kan worden verwezen naar de namen van de Azure AD B2C-tenant en het beleid tijdens het inrichtingsproces dat voor de Commerce-omgeving wordt uitgevoerd met Microsoft Dynamics Lifecycle Services (LCS).

U kunt de aangepaste Commerce-pagina's maken met behulp van de modules voor registreren, aanmelden, accountprofiel bewerken of wachtwoord opnieuw instellen. De pagina-URL's die voor deze aangepaste pagina's worden gepubliceerd, moeten vervolgens worden opgenomen in de Azure AD B2C-beleidsconfiguraties in de Azure-portal.

## <a name="set-up-b2c-policies"></a>B2C-beleid instellen

Nadat u uw Azure AD B2C-tenant hebt ingesteld en deze aan uw Commerce-omgeving hebt gekoppeld, gaat u naar de pagina **Azure AD B2C** in de Azure-portal en selecteert u in het menu **Beleid** de optie **Gebruikersstromen (beleid)**.

![Gebruikersstromen (beleid), opdracht in het menu](./media/B2C_CustomPage_PoliciesMenu.png)

U kunt nu de aanmeldingsstromen configureren voor 'Registreren en aanmelden', 'Profiel bewerken' en 'Wachtwoord opnieuw instellen'.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Het beleid voor 'Registreren en aanmelden' configureren

Voer de volgende stappen uit om het beleid voor 'Registreren en aanmelden' te configureren.

1. Selecteer **Nieuwe gebruikersstroom** en vervolgens op het tabblad **Aanbevolen** het beleid **Registreren en aanmelden**.
1. Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_SignInSignUp**).
1. Selecteer in de sectie **Identiteitsproviders** de identiteitsproviders die u voor het beleid wilt gebruiken. U moet minimaal **E-mailaanmelding** selecteren.
1. Schakel in de kolom **Kenmerk verzamelen** de selectievakjes in voor **E-mailadres**, **Voornaam** en **Achternaam**.
1. Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Identiteitsprovider**, **Achternaam** en **Object-id van de gebruiker**.

    ![Geselecteerde kenmerken en claims](./media/B2C_SignInSignUp_Attributes.png)

1. Selecteer **OK** om het beleid te maken.
1. Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.
1. Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.

    ![Eigenschappenpagina voor het nieuwe beleid](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> In de Commerce-omgeving wordt verwezen naar de volledig beleidsnaam. (Het voorvoegsel **B2C\_1\_** wordt opgenomen in de verwijzing.) De naam van beleid kan niet worden gewijzigd nadat dit zijn gemaakt. Als u een bestaand beleid vervangt voor uw Commerce-omgeving, kunt u het oorspronkelijke beleid verwijderen en een nieuw beleid met dezelfde naam maken. Als de omgeving al is ingericht, kunt u de nieuwe beleidsnaam indienen via een serviceaanvraag.

U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt. Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.

### <a name="configure-the-profile-editing-policy"></a>Het beleid voor het 'Profiel bewerken' configureren

Ga als volgt te werk om het beleid voor 'Profiel bewerken' te configureren.

1. Selecteer **Nieuwe gebruikersstroom** en vervolgens op het tabblad **Aanbevolen** het beleid **Profiel bewerken**.
1. Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_EditProfile**).
1. Selecteer in de sectie **Identiteitsproviders** de identiteitsproviders die u voor het beleid wilt gebruiken. U moet minimaal een **Aanmelding voor een lokaal account** selecteren.
1. Schakel in de kolom **Kenmerk verzamelen** de selectievakjes in voor **E-mailadressen** en **Achternaam**.
1. Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Identiteitsprovider**, **Achternaam** en **Object-id van de gebruiker**.
1. Selecteer **OK** om het beleid te maken.
1. Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.
1. Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.

U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt. Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.

### <a name="configure-the-password-reset-policy"></a>Het beleid voor 'Wachtwoord opnieuw instellen' configureren

Ga als volgt te werk om het beleid voor 'Wachtwoord opnieuw instellen' te configureren.

1. Selecteer **Nieuwe gebruikersstroom** en vervolgens op het tabblad **Preview** het beleid **Wachtwoord opnieuw instellen v1.1**.

    ![Beleid voor Wachtwoord opnieuw instellen v1.1 geselecteerd op het tabblad Preview](./media/B2C_ForgetPassword_Menu.png)

1. Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_ForgetPassword**).
1. Selecteer in de sectie **Identiteitsproviders** de optie **Wachtwoord via e-mailadres opnieuw instellen**.
1. Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Achternaam** en **Object-id van de gebruiker**.

    ![Geselecteerde claims](./media/B2C_ForgetPassword_Attributes.png)

1. Selecteer **OK** om het beleid te maken.
1. Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.
1. Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.

U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt. Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.

## <a name="build-the-custom-pages"></a>Aangepaste pagina's maken

Ga als volgt te werk om de aangepaste pagina's te maken voor het verwerken van gebruikersaanmeldingen.

1. Ga in de Commerce-ontwerpfunctie naar uw site.
1. Maak de volgende vijf sjablonen en vijf pagina's:

    - Een sjabloon **Aanmelden** en een pagina waarop de aanmeldingsmodule wordt gebruikt.
    - Een sjabloon **Registreren** en een pagina waarop de registratiemodule wordt gebruikt.
    - Een sjabloon **Wachtwoord opnieuw instellen** en een pagina waarop de module Wachtwoord opnieuw instellen wordt gebruikt.
    - Een sjabloon **Verificatie voor wachtwoord opnieuw instellen** en een pagina waarop de verificatiemodule voor Wachtwoord opnieuw instellen wordt gebruikt.
    - Een sjabloon **Profiel bewerken** en een pagina waarop de module Accountprofiel bewerken wordt gebruikt

Volg de volgende richtlijnen wanneer u de pagina's bouwt:

- Gebruik voor elke pagina of module de indeling en de stijl die het best aansluiten bij uw zakelijke vereisten.
- Publiceer alle pagina's en URL's die moeten worden gebruikt in de Azure AD B2C-configuratie.
- Nadat de pagina's en URL's zijn gepubliceerd, verzamelt u de URL's die moeten worden gebruikt voor de Azure AD B2C-beleidsconfiguraties. Het achtervoegsel **?preloadscripts=true** wordt toegevoegd aan elke URL wanneer deze wordt gebruikt.

> [!IMPORTANT]
> Gebruik universele kop- en voetteksten met relatieve koppelingen niet opnieuw. Aangezien deze pagina's in het Azure AD B2C-domein worden gehost wanneer ze worden gebruikt, moeten alleen absolute URL's worden gebruikt voor alle koppelingen.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C-beleid configureren met aangepaste paginagegevens 

Ga in de Azure-portal terug naar de pagina **Azure AD B2C** en selecteer in het menu **Beleid** de optie **Gebruikersstromen (beleid)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Het beleid 'Registreren en aanmelden' bijwerken met aangepaste paginagegevens

Volg deze stappen om het beleid 'Registreren en aanmelden' bij te werken met aangepaste paginagegevens.

1. Selecteer In het beleid voor **Registreren en aanmelden** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.
1. Selecteer de indeling voor **Gecombineerde pagina voor Registreren en aanmelden**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige aanmeldings-URL in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/sign-in?preloadscripts=true`` in.
1. Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.
1. Selecteer de indeling **Lokale accountaanmeldingspagina**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige aanmeldings-URL in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/sign-up?preloadscripts=true`` in.
1. Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.
1. Voer de volgende stappen uit in de sectie **Gebruikerskenmerken**:

    1. Selecteer **Nee** in het veld **Verificatie vereist** voor de kenmerken **E-mailadres**, **Voornaam** en **Achternaam**.
    1. Selecteer **Nee** in het veld **Optioneel** voor de kenmerken **Voornaam** en **Achternaam**.

    ![Configuratie van het beleid voor lokale accountaanmeldingspagina](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Het beleid 'Profiel bewerken' bijwerken met aangepaste paginagegevens

Volg deze stappen om het beleid 'Profiel bewerken' bij te werken met aangepaste paginagegevens.

1. Selecteer In het beleid voor **Profiel bewerken** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.
1. Selecteer de indeling voor de **pagina Profiel bewerken**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige URL voor profielbewerking in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/profile-edit?preloadscripts=true`` in.
1. Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.
1. Voer de volgende stappen uit in de sectie **Gebruikerskenmerken**:

    1. Selecteer **Nee** in het veld **Verificatie vereist** voor de kenmerken **E-mailadres** en **Voornaam**.
    1. Selecteer **Nee** in het veld **Optioneel** voor de kenmerken **Voornaam** en **Achternaam**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Het beleid 'Wachtwoord opnieuw instellen' bijwerken met aangepaste paginagegevens

Volg deze stappen om het beleid 'Wachtwoord opnieuw instellen' bij te werken met aangepaste paginagegevens.

1. Selecteer In het beleid voor **Wachtwoord opnieuw instellen** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.
1. Selecteer de indeling voor de **pagina Nieuw wachtwoord**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige URL voor het opnieuw instellen van het wachtwoord in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/passwordreset?preloadscripts=true`` in.
1. Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.
1. Selecteer de indeling voor de **pagina Accountverificatie**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige URL voor verificatie voor het opnieuw instellen van het wachtwoord in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/passwordreset-verification?preloadscripts=true`` in.
1. Selecteer in het veld **Versie van pagina-indeling (Preview)** **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Standaard tekstreeksen aanpassen voor labels en omschrijvingen

In de modulebibliotheek worden aanmeldingsmodules vooraf ingevuld met standaard tekstreeksen voor de labels en omschrijvingen. U kunt deze reeksen aanpassen in de Software Development Kit (SDK) door de waarden in het global.json-bestand voor de logboekmodule bij te werken.

De standaardtekst voor de koppeling voor vergeten wachtwoord is bijvoorbeeld **Vergeten wachtwoord?**. Hieronder ziet u deze standaardtekst op de aanmeldingspagina.

![Standaardtekst van de koppeling voor vergeten wachtwoord op de aanmeldingspagina](./media/B2C_SignUp_ModuleFace.png)

In het bestand global.json voor de aanmeldingsmodule van de modulebibliotheek kunt u de tekst echter wijzigen in **Wachtwoord vergeten?**, zoals u in de volgende afbeelding kunt zien.

![Bijgewerkte koppelingstekst in het bestand global.json van het aanmeldingsmodule](./media/B2C_CustomizingStringsForModule.png)

Nadat u het bestand Global.json hebt bijgewerkt en uw wijzigingen hebt gepubliceerd, wordt de tekst van de nieuwe koppeling weergegeven in de aanmeldingsmodule in Commerce en op de live aanmeldingspagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[robots.txt-bestanden beheren](manage-robots-txt-files.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)

[Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-B2C-tenants.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)

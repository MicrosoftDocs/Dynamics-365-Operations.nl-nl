---
title: Aangepaste pagina's voor gebruikersaanmeldingen instellen
description: In dit onderwerp wordt beschreven hoe u aangepaste pagina's maakt in Microsoft Dynamics 365 Commerce voor het verwerken van aangepaste aanmeldingen voor gebruikers van B2C-tenants (business-to-consumers) met Azure Active Directory (Azure AD).
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d4a1c2f45d77c3ff9a7bb4dffaf12d877dc04e69
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936775"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Aangepaste pagina's voor gebruikersaanmeldingen instellen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u aangepaste pagina's maakt in Microsoft Dynamics 365 Commerce voor het verwerken van aangepaste aanmeldingen voor gebruikers van B2C-tenants (business-to-consumers) met Azure Active Directory (Azure AD).

Als u aangepaste pagina's wilt gebruiken die zijn gemaakt in Dynamics 365 Commerce waarin de aanmeldingsgegevens van gebruikers worden afgehandeld, moet u het Azure AD-beleid instellen waarnaar wordt verwezen in de Commerce-omgeving. U kunt Azure AD B2C-beleidsregels configureren voor 'Registreren en aanmelden', 'Profiel bewerken' en 'Wachtwoord opnieuw instellen' met behulp van de Azure AD B2C-toepassing. Vervolgens kan worden verwezen naar de namen van de Azure AD B2C-tenant en het beleid tijdens het inrichtingsproces dat voor de Commerce-omgeving wordt uitgevoerd met Microsoft Dynamics Lifecycle Services (LCS).

U kunt de aangepaste Commerce-pagina's maken met de modules voor registreren, aanmelden, accountprofiel bewerken of wachtwoord opnieuw instellen, of met algemene AAD-modules. De pagina-URL's die voor deze aangepaste pagina's worden gepubliceerd, moeten vervolgens worden opgenomen in de Azure AD B2C-beleidsconfiguraties in de Azure-portal.

> [!WARNING] 
> Azure AD B2C stelt voor 1 augustus 2021 oude (legacy) gebruikersstromen buiten gebruik. Daarom moet u de migratie van uw gebruikersstromen naar de nieuwe aanbevolen versie gaan plannen. De nieuwe versie biedt functiepariteit en nieuwe functies. Zie [Gebruikersstromen in Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview) voor meer informatie.

>De modulebibliotheek voor Commerce versie 10.0.15 of hoger moet worden gebruikt met de aanbevolen B2C-gebruikersstromen. De standaardpagina's voor gebruikersbeleid die in Azure AD B2C worden aangeboden, kunnen ook worden gebruikt en toegevoegd aan achtergrondafbeeldingen, logo's en achtergrondkleurwijzigingen met betrekking tot het huismerk van bedrijven. Hoewel beperkter in ontwerpmogelijkheden, bieden de standaard gebruikersbeleidspagina's Azure AD B2C-beleidsfunctionaliteit zonder speciale aangepaste pagina's te maken en te configureren. 

## <a name="set-up-b2c-policies"></a>B2C-beleid instellen

Nadat u uw Azure AD B2C-tenant hebt ingesteld en deze aan uw Commerce-omgeving hebt gekoppeld, gaat u naar de pagina **Azure AD B2C** in de Azure-portal en selecteert u in het menu **Beleid** de optie **Gebruikersstromen (beleid)**.

![Gebruikersstromen (beleid), opdracht in het menu](./media/B2C_CustomPage_PoliciesMenu.png)

U kunt nu de aanmeldingsstromen configureren voor 'Registreren en aanmelden', 'Profiel bewerken' en 'Wachtwoord opnieuw instellen'.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Het beleid voor 'Registreren en aanmelden' configureren

Voer de volgende stappen uit om het beleid voor 'Registreren en aanmelden' te configureren.

1. Selecteer **Nieuwe gebruikersstroom**, selecteer **Registreren en aanmelden** en selecteer vervolgens het tabblad **Aanbevolen** en **Maken**.
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

1. Selecteer **Nieuwe gebruikersstroom**, selecteer **Profiel bewerken** en selecteer vervolgens het tabblad **Aanbevolen** en **Maken**.
1. Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_EditProfile**).
1. Selecteer in de sectie **Identiteitsproviders** de identiteitsproviders die u voor het beleid wilt gebruiken. U moet minimaal een **Aanmelding voor een lokaal account** selecteren.
1. Schakel in de kolom **Kenmerk verzamelen** de selectievakjes in voor **Voornaam** en **Achternaam**.
1. Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Identiteitsprovider**, **Achternaam** en **Object-id van de gebruiker**.
1. Selecteer **OK** om het beleid te maken.
1. Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.
1. Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.

U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt. Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.

### <a name="configure-the-password-reset-policy"></a>Het beleid voor 'Wachtwoord opnieuw instellen' configureren

Ga als volgt te werk om het beleid voor 'Wachtwoord opnieuw instellen' te configureren.

1. Selecteer **Nieuwe gebruikersstroom** en selecteer vervolgens de optie **Wachtwoord opnieuw instellen** en kies het tabblad **Aanbevolen** en klik op **Maken**.
1. Voer een naam in voor het beleid (bijvoorbeeld **B2C\_1\_ForgetPassword**).
1. Selecteer in de sectie **Identiteitsproviders** de optie **Wachtwoord via e-mailadres opnieuw instellen**.
1. Schakel in de kolom **Claim terugsturen** de selectievakjes in voor **E-mailadressen**, **Voornaam**, **Achternaam** en **Object-id van de gebruiker**.
1. Selecteer **OK** om het beleid te maken.
1. Dubbelklik op de nieuwe beleidsnaam en selecteer vervolgens **Eigenschappen** in het navigatievenster.
1. Stel de optie **Pagina-indeling afdwingen met JavaScript inschakelen (preview)** in op **Aan**.

U keert terug naar dit beleid om de instellingen te voltooien nadat u de aangepaste pagina's hebt gemaakt. Sluit het beleid voor nu af om terug te keren naar de pagina **Gebruikersstromen (beleid)** in de Azure-portal.

## <a name="build-the-custom-pages"></a>Aangepaste pagina's maken

Speciale Azure AD-modules zijn opgenomen in Commerce om aangepaste pagina's te bouwen voor Azure AD B2C-gebruikersbeleid. Pagina's kunnen speciaal voor de lay-out van elke gebruikersbeleidspagina worden gebouwd met behulp van de belangrijkste Azure AD B2C-modules die hieronder worden beschreven. Als alternatief kan de module **AAD Generic** worden gebruikt voor alle pagina-indelingen en -beleidsregels in Azure AD B2C (zelfs voor pagina-indelingsopties binnen beleid dat hieronder niet wordt vermeld). 

- Paginaspecifieke Azure AD-modules zijn gebonden aan gegevensinvoeritems die door Azure AD B2C worden gerenderd. Deze modules geven u meer controle over de positionering van de elementen op uw pagina's. Er moeten echter mogelijk meer pagina's en module-extensies worden gebouwd om rekening te houden met verschillen die verder gaan dan de onderstaande standaardinstellingen.
- De module **AAD Generic** maakt het "div"-element voor Azure AD B2C om alle elementen in de pagina-indeling van het gebruikersbeleid weer te geven, waardoor de B2C-functies van de pagina flexibeler worden, maar u minder controle hebt over de positionering en styling (hoewel CSS kan worden gebruikt om het uiterlijk van uw site aan te passen).

U kunt een enkele pagina maken met de module **AAD Generic** en deze gebruiken voor al uw gebruikersbeleidspagina's of specifieke pagina's uitbouwen met behulp van de afzonderlijke Azure AD-modules voor aanmelding, registratie, profielbewerking, wachtwoordherstel en verificatie van wachtwoordherstel. U kunt ook een mix van beide gebruiken, met behulp van de specifieke Azure AD-pagina's voor de pagina-indelingen die hieronder worden vermeld en de algemene AAD-modulepagina voor resterende pagina-indelingen binnen deze of andere pagina's met gebruikersbeleid.

Lees [Pagina's en modules voor identiteitsbeheer](identity-mgmt-modules.md) voor meer informatie over Azure AD-modules die bij de modulebibliotheek worden geleverd.

Ga als volgt te werk om de aangepaste pagina's met specifieke identiteitsmodules te maken voor het verwerken van gebruikersaanmeldingen.

1. Ga naar uw site in Commerce Site Builder.
1. Bouw de volgende vijf sjablonen en pagina's (indien nog niet aanwezig op uw site):
    - Een sjabloon **Aanmelden** en een pagina waarop de aanmeldingsmodule wordt gebruikt.
    - Een sjabloon **Registreren** en een pagina waarop de registratiemodule wordt gebruikt.
    - Een sjabloon **Wachtwoord opnieuw instellen** en een pagina waarop de module Wachtwoord opnieuw instellen wordt gebruikt.
    - Een sjabloon **Verificatie voor wachtwoord opnieuw instellen** en een pagina waarop de verificatiemodule voor Wachtwoord opnieuw instellen wordt gebruikt.
    - Een sjabloon **Profiel bewerken** en een pagina waarop de module Accountprofiel bewerken wordt gebruikt.

Volg de volgende richtlijnen wanneer u de pagina's bouwt:

- Gebruik voor elke pagina of module de indeling en de stijl die het best aansluiten bij uw zakelijke vereisten.
- Publiceer alle pagina's en URL's die moeten worden gebruikt in de Azure AD B2C-configuratie.
- Nadat de pagina's en URL's zijn gepubliceerd, verzamelt u de URL's die moeten worden gebruikt voor de Azure AD B2C-beleidsconfiguraties. Het achtervoegsel **?preloadscripts=true** wordt toegevoegd aan elke URL wanneer deze wordt gebruikt.

> [!IMPORTANT]
> Pagina's waarnaar in Azure AD B2C moet worden verwezen, worden rechtstreeks vanuit het domein van de Azure AD B2C-tenant bediend. Gebruik universele kop- en voetteksten met relatieve koppelingen niet opnieuw. Aangezien deze pagina's in het Azure AD B2C-domein worden gehost wanneer ze worden gebruikt, moeten alleen absolute URL's worden gebruikt voor alle koppelingen. Het wordt aanbevolen om een specifieke header- en voettekst te maken met absolute URL's voor uw aan Azure AD gerelateerde aangepaste pagina's, waarbij alle Commerce-specifieke modules waarvoor verbinding met Retail Server vereist is, zijn verwijderd. De favorieten, zoekbalk, aanmeldingskoppeling en winkelwagenmodules mogen bijvoorbeeld niet worden opgenomen in pagina's die worden gebruikt in Azure AD B2C-gebruikersstromen.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C-beleid configureren met aangepaste paginagegevens 

Ga in de Azure-portal terug naar de pagina **Azure AD B2C** en selecteer in het menu **Beleid** de optie **Gebruikersstromen (beleid)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Het beleid 'Registreren en aanmelden' bijwerken met aangepaste paginagegevens

Volg deze stappen om het beleid 'Registreren en aanmelden' bij te werken met aangepaste paginagegevens.

1. Selecteer In het beleid voor **Registreren en aanmelden** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.
1. Selecteer de indeling voor **Gecombineerde pagina voor Registreren en aanmelden**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige aanmeldings-URL in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/sign-in?preloadscripts=true`` in.
1. Selecteer in het veld **Pagina-indelingsversie** de versie **2.1.0** of hoger (modulebibliotheek voor Commerce versie 10.0.15 of hoger vereist).
1. Selecteer **Opslaan**.
1. Selecteer de indeling **Lokale accountaanmeldingspagina**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige aanmeldings-URL in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/sign-up?preloadscripts=true`` in.
1. Selecteer in het veld **Pagina-indelingsversie** de versie **2.1.0** of hoger (modulebibliotheek voor Commerce versie 10.0.15 of hoger vereist).
1. Voer de volgende stappen uit in de sectie **Gebruikerskenmerken**:
    1. Selecteer voor de kenmerken **Voornaam** en **Achternaam** de optie **Nee** in de kolom **Vereist verificatie**.
    1. Voor het kenmerk **E-mailadres** wordt aanbevolen om de standaardwaarde **Ja** geselecteerd te laten in de kolom **Vereist verificatie**. Deze optie zorgt ervoor dat gebruikers die zich aanmelden met een bepaald e-mailadres verifiëren dat ze eigenaar zijn van het e-mailadres.
    1. Selecteer **Nee** in de kolom **Optioneel** voor de kenmerken **E-mailadres**, **Voornaam** en **Achternaam**.
1. Selecteer **Opslaan**.

    ![Configuratie van het beleid voor lokale accountaanmeldingspagina](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Het beleid 'Profiel bewerken' bijwerken met aangepaste paginagegevens

Volg deze stappen om het beleid 'Profiel bewerken' bij te werken met aangepaste paginagegevens.

1. Selecteer In het beleid voor **Profiel bewerken** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.
1. Selecteer de indeling voor de **pagina Profiel bewerken** (mogelijk moet u naar beneden scrollen langs andere indelingsopties, afhankelijk van uw scherm).
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige URL voor profielbewerking in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/profile-edit?preloadscripts=true`` in.
1. Selecteer voor **Versie van pagina-indeling** de versie **2.1.0** of hoger (vereist modulebibliotheek voor Commerce versie 10.0.15 of hoger).
1. Voer de volgende stappen uit in de sectie **Gebruikerskenmerken**:
    1. Selecteer **Nee** in de kolom **Optioneel** voor de kenmerken **Voornaam** en **Achternaam**.
    1. Selecteer voor de kenmerken **Voornaam** en **Achternaam** de optie **Nee** in de kolom **Vereist verificatie**.
1. Selecteer **Opslaan**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Het beleid 'Wachtwoord opnieuw instellen' bijwerken met aangepaste paginagegevens

Volg deze stappen om het beleid 'Wachtwoord opnieuw instellen' bij te werken met aangepaste paginagegevens.

1. Selecteer In het beleid voor **Wachtwoord opnieuw instellen** dat u eerder hebt geconfigureerd, de optie **Pagina-indelingen** in het navigatievenster.
1. Selecteer de indeling voor **pagina Wachtwoord vergeten**.
1. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
1. Voer in het veld **Aangepaste pagina-URI** de volledige URL voor verificatie voor het opnieuw instellen van het wachtwoord in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/password-reset-verification?preloadscripts=true`` in.
1. Selecteer in het veld **Pagina-indelingsversie** de versie **2.1.0** of hoger (modulebibliotheek voor Commerce versie 10.0.15 of hoger vereist).
2. Selecteer **Opslaan**.
3. Selecteer de indeling voor de **pagina Wachtwoord wijzigen**.
4. Stel de optie **Aangepaste paginainhoud gebruiken** in op **Ja**.
5. Voer in het veld **Aangepaste pagina-URI** de volledige URL voor het opnieuw instellen van het wachtwoord in. Neem het achtervoegsel **?preloadscripts=true** op. Voer bijvoorbeeld ``www.<my domain>.com/password-reset?preloadscripts=true`` in.
6. Selecteer in het veld **Pagina-indelingsversie** de versie **2.1.0** of hoger (modulebibliotheek voor Commerce versie 10.0.15 of hoger vereist).
7. Selecteer **Opslaan**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Standaard tekstreeksen aanpassen voor labels en omschrijvingen

In de modulebibliotheek worden aanmeldingsmodules vooraf ingevuld met standaard tekstreeksen voor de labels en omschrijvingen. U kunt de tekenreeksen aanpassen in het eigenschappenvenster van de module waaraan u werkt. Voor extra tekenreeksen op de pagina (zoals de koppelingstekst **Wachtwoord vergeten?** of de aanroep **Een account maken** voor actietekst) moet u de Commerce Software Development Kit (SDK) gebruiken en de waarden in het bestand global.json bijwerken voor de aanmeldingsmodule.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
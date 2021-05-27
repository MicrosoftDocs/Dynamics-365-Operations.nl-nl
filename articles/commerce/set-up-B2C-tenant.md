---
title: Een B2C-tenant instellen in Commerce
description: In dit onderwerp wordt beschreven hoe u uw B2C-tenants (business-to-consumers) in Azure Active Directory (Azure AD) instelt voor de verificatie van sitegebruikers in Dynamics 365 Commerce.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 84b3a3630d3809c05f87242784207c3c4af160ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018575"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Een B2C-tenant instellen in Commerce

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u uw B2C-tenants (business-to-consumers) in Azure Active Directory (Azure AD) instelt voor de verificatie van sitegebruikers in Dynamics 365 Commerce.

Dynamics 365 Commerce gebruikt Azure AD B2C om gebruikersreferenties en verificatiestromen te ondersteunen. Een gebruiker kan zich registreren en aanmelden, en vervolgens zijn/haar wachtwoord opnieuw instellen via deze stromen. Azure AD B2C slaat gevoelige gebruikersverificatiegegevens op, zoals de gebruikersnaam en het wachtwoord. In de gebruikersrecord in de B2C-tenant wordt een record voor een lokale B2C-account of een record voor een B2C-provider van sociale identiteiten opgeslagen. Deze B2C-records verwijzen weer naar de klantrecord in de Commerce-omgeving.

> [!WARNING] 
> Azure AD B2C stelt voor 1 augustus 2021 oude (legacy) gebruikersstromen buiten gebruik. Daarom moet u de migratie van uw gebruikersstromen naar de nieuwe aanbevolen versie gaan plannen. De nieuwe versie biedt functiepariteit en nieuwe functies. De modulebibliotheek voor Commerce versie 10.0.15 of hoger moet worden gebruikt met de aanbevolen B2C-gebruikersstromen. Zie [Gebruikersstromen in Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview) voor meer informatie.
 
 > [!NOTE]
 > Commerce-evaluatieomgevingen worden geleverd met een vooraf geladen Azure AD B2C-tenant voor demonstratiedoeleinden. Het laden van uw eigen Azure AD B2C-tenant met behulp van de onderstaande stappen is niet vereist voor evaluatieomgevingen.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Een AAD B2C-tenant maken of een koppeling met een bestaande AAD B2C-tenant instellen in de Azure-portal

1. Meld u aan bij de [Azure-portal](https://portal.azure.com/).
1. Selecteer **Een resource maken** in het menu van Azure Portal. Gebruik het abonnement en de map die met uw Commerce-omgeving worden verbonden.

    ![Een resource maken in Azure Portal](./media/B2CImage_1.png)

1. Ga naar **Identiteit \> Azure Active Directory B2C**.
1. Op de pagina **Nieuwe B2C-tenant maken of koppelen aan bestaande tenant maken** gebruikt u een van de volgende opties die het beste aansluit bij de behoeften van uw bedrijf:

    - **Een nieuwe Azure AD B2C-tenant maken**: gebruik deze optie om een nieuwe AAD B2C-tenant te maken.
        1. Selecteer **Een nieuwe Azure AD B2C-tenant maken**.
        1. Voer onder **Naam van organisatie** de naam van de organisatie in.
        1. Voer bij **Oorspronkelijke domeinnaam** de oorspronkelijke domeinnaam in.
        1. Selecteer het land of de regio bij **Land of regio**.
        1. Selecteer **Maken** om de tenant te maken.

     ![Een nieuwe Azure AD-tenant maken](./media/B2CImage_2.png)

     - **Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**: gebruik deze optie als u al een Azure AD B2C-tenant hebt waarmee u een koppeling tot stand wilt brengen.
        1. Selecteer **Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**.
        1. Selecteer bij **Azure AD B2C-tenant** de geschikte B2C-tenant. Als het bericht Geen B2C-tenants gevonden die in aanmerking komen wordt weergegeven in het selectievak, beschikt u niet over een bestaande B2C-tenant die in aanmerking komt en moet u een nieuwe maken.
        1. Selecteer **Nieuwe maken** voor **Resourcegroep**. Voer een **naam** in voor de resourcegroep die de tenant moet bevatten, selecteer **de locatie de resourcegroep** en selecteer vervolgens **Maken**.

    ![Een bestaande Azure AD B2C-tenant koppelen aan een Azure-abonnement](./media/B2CImage_3.png)

1. Zodra de nieuwe Azure AD B2C-map is gemaakt (dit kan even duren), wordt een koppeling naar de nieuwe map weergegeven op het dashboard. Met deze koppeling wordt u naar de pagina Welkom bij Azure Active Directory B2C geleid.

    ![Koppeling naar nieuwe AAD-map](./media/B2CImage_4.png)

> [!NOTE]
> Als u meerdere abonnementen hebt in uw Azure-account of als u de B2C-tenant hebt ingesteld zonder deze aan een actief abonnement te koppelen, kunt u via een banner **Problemen oplossen** de tenant aan een abonnement koppelen. Selecteer het probleemoplossingsbericht en volg de instructies om het probleem met het abonnement op te lossen.

In de volgende afbeelding ziet u een voorbeeld van een Azure AD B2C-banner **Problemen oplossen**.

![Waarschuwing met de melding dat voor de map geen actief abonnement bestaat](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>De B2C-toepassing maken

Nadat de B2C-tenant is gemaakt, maakt u een B2C-toepassing in uw nieuwe Azure AD B2C-tenant om te communiceren met Commerce.

Ga als volgt te werk om de B2C-toepassing te maken:

1. Selecteer in de Azure-portal de optie **App-registraties** en selecteer vervolgens **Nieuwe registratie**.
1. Voer onder **Naam** de naam in die u aan deze Azure AD B2C-toepassing wilt geven.
1. Selecteer onder **Ondersteunde accounttypen** de optie **Accounts in een identiteitsprovider of organisatiemap (voor het verifiëren van gebruikers met gebruikersstromen)**.
1. Voer voor **Omleidings-URI** uw speciale antwoord-URL's in als type **Web**. Zie [Antwoord-URL's](#reply-urls) hieronder voor informatie over antwoord-URL's en hoe u deze kunt opmaken.
1. Selecteer voor **Machtigingen** de optie **Beheerdersmachtigingen verlenen voor de machtigingen openid en offline_access**.
1. Selecteer **Registreren**.
1. Selecteer de nieuw gemaakte toepassing en navigeer naar het menu **Verificatie**. Hier kunt u indien nodig (nu of later) extra **Omleidings-URI's** toevoegen. Ga verder met de volgende stap als dit momenteel niet nodig is.
1. Selecteer onder **Impliciete toekenning** zowel **Toegangstokens** als **Id-tokens** om ze in te schakelen voor de toepassing. Selecteer **Opslaan**.
1. Ga naar het menu **Overzicht** van de Azure-portal en kopieer de **Toepassings(client)-id**. Noteer deze id voor latere installatiestappen (hiernaar wordt later verwezen als de **client-GUID**).

Zie [De nieuwe ervaring App-registraties voor Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide) voor meer informatie over App-registraties in Azure AD B2C

### <a name="reply-urls"></a>Antwoord-URL's

Antwoord-URL's zijn belangrijk omdat ze een toegestane lijst van de retourdomeinen leveren wanneer uw site Azure AD B2C aanroept om een gebruiker te verifiëren. Hierdoor kan de geverifieerde gebruiker worden geretourneerd naar het domein waarbij ze zich aanmelden (uw sitedomein). 

In het **Antwoord-URL** in het scherm **Azure AD B2C -Toepassingen \> Nieuwe toepassing** moet u afzonderlijke regels toevoegen voor uw sitedomein en (zodra uw omgeving is ingericht) de door Commerce gegenereerde URL. Deze URL's moeten altijd een geldige URL-indeling gebruiken en mogen alleen basis-URL's (geen navolgende slashes of paden) zijn. De tekenreeks ``/_msdyn365/authresp`` moet vervolgens worden toegevoegd aan de basis-URL's, zoals in de volgende voorbeelden.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Het domein moet volledig overeenkomen met het e-commercedomein. Als u meerdere domeinen hebt, moet u deze URL toevoegen voor elk domein toevoegen.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Beleid voor gebruikersstromen maken

Gebruikersstromen zijn de beleidsregels die Azure AD B2C gebruikt om veilige gebruikerservaringen voor registeren, aanmelden, profielbewerkingen en vergeten wachtwoorden te bieden. Dynamics 365 Commerce gebruikt deze stromen om de beleidsacties uit te voeren om te communiceren met de Azure AD B2C-tenant. Wanneer een gebruiker met dit beleid communiceert, wordt deze omgeleid naar de Azure AD B2C-tenant om de acties uit te voeren.

Azure AD B2C biedt drie algemene typen gebruikersstromen:
- Registreren en aanmelden
- Profiel bewerken
- Wachtwoord opnieuw instellen

U kunt ervoor kiezen om de standaardgebruikersstromen van Azure AD te gebruiken. Vervolgens wordt er een pagina weergegeven die wordt gehost door AAD B2C. U kunt ook een HTML-pagina maken om het uiterlijk van deze gebruikersstroomervaringen te bepalen. 

Zie [Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md) als u de gebruikersbeleidspagina's wilt aanpassen met pagina's die zijn gebouwd in Dynamics 365 Commerce. Zie voor aanvullende informatie [De interface met gebruikerservaringen in Azure Active Directory B2C aanpassen](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Een gebruikersstroombeleid voor registreren en aanmelden maken

Voer de volgende stappen uit om een gebruikersstroombeleid voor registreren en aanmelden te maken.

1. Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.
1. Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.
1. Selecteer het beleid **Registreren en aanmelden** en selecteer vervolgens de versie **Aanbevolen**.
1. Voer een beleidsnaam in onder **Naam**. Deze naam wordt vervolgens weer gegeven met een voorvoegsel dat wordt toegewezen door de portal (bijvoorbeeld B2C_1_).
1. Schakel onder **Identiteitsproviders** het desbetreffende selectievakje in.
1. Selecteer de juiste keuze voor uw bedrijf onder **Meervoudige verificatie**. 
1. Selecteer onder **Gebruikerskenmerken en claims** opties om kenmerken te verzamelen of claims naar wens te retourneren. Voor Commerce zijn de volgende standaardopties vereist:

    | **Kenmerk verzamelen** | **Claim retourneren** |
    | ---------------------- | ----------------- |
    | E-mailadres          | E-mailadressen   |
    | Voornaam             | Voornaam        |
    |                        | Identiteitsprovider |
    | Achternaam                | Achternaam           |
    |                        | De object-id van de gebruiker  |

1. Selecteer **Maken**.

De volgende afbeelding is een voorbeeld van de gebruikersstroom voor registreren en aanmelden voor Azure AD B2C.

![Beleidsinstellingen voor registreren en aanmelden](./media/B2CImage_11.png)

In de volgende afbeelding ziet de optie **Gebruikersstroom uitvoeren** in de in de gebruikers stroom voor registreren en aanmelden in Azure AD B2C.

![De optie Gebruikersstroom uitvoeren in de beleidsstroom](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Een beleid voor de gebruikersstroom voor het bewerken van profielen maken

Voer de volgende stappen uit om een gebruikersstroombeleid voor het bewerken van profielen te maken.

1. Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.
1. Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.
1. Selecteer **Profielen bewerken** en selecteer vervolgens de versie **Aanbevolen**.
1. Voer onder **Naam** de gebruikersstroom voor het bewerken van profielen in. Deze naam wordt vervolgens weer gegeven met een voorvoegsel dat wordt toegewezen door de portal (bijvoorbeeld B2C_1_).
1. Selecteer onder **Identiteitsproviders** de optie **Aanmelden voor e-mail**.
1. Schakel onder **Gebruikerskenmerken** de volgende selectievakjes in:
    - **E-mailadressen** (alleen **Claim retourneren**)
    - **Voornaam** (**Kenmerk verzamelen** en **Claim retourneren**)
    - **Identiteitsprovider** (alleen **Claim retourneren**)
    - **Achternaam** (**Kenmerk verzamelen** en **Claim retourneren**)
    - **De object-id van de gebruiker** (alleen **Claim retourneren**)
1. Selecteer **Maken**.

In de volgende afbeelding ziet u een voorbeeld van de gebruikersstroom voor het bewerken van profielen in Azure AD B2C.

![De gebruikersstroom voor het bewerken van profielen maken](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Een beleid voor de gebruikersstroom voor het opnieuw instellen van wachtwoorden maken

Voer de volgende stappen uit om een gebruikersstroombeleid voor het opnieuw instellen van wachtwoorden te maken.

1. Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.
1. Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.
1. Selecteer **Wachtwoord opnieuw instellen** en selecteer vervolgens de versie **Aanbevolen**.
1. Voer onder **Naam** een naam in voor de gebruikersstroom voor het opnieuw instellen van wachtwoorden.
1. Selecteer onder **Identiteitsproviders** de optie **Wachtwoord via e-mailadres opnieuw instellen**.
1. Selecteer **Maken**.
1. Schakel onder **Toepassingsclaims** de volgende selectievakjes in:
    - **E-mailadressen**
    - **Voornaam**
    - **Achternaam**
    - **De object-id van de gebruiker**
1. Selecteer **Maken**.

De volgende afbeelding geeft aan waar het **wachtwoord via het e-mailadres opnieuw moet worden ingesteld** in de gebruikersstroom voor het opnieuw instellen van wachtwoorden in Azure AD B2C.

![Wachtwoord opnieuw instellen via e-mailadres instellen in het beleid Wachtwoord opnieuw instellen](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a>Providers van sociale identiteiten toevoegen (optioneel)

Providers van sociale identiteiten stellen gebruikers in staat hun sociale accounts te gebruiken voor verificatie. Het toevoegen van verificatie via providers van sociale identiteiten is optioneel in Dynamics 365 Commerce. 

Als geen verificatie via de provider van sociale identiteiten wordt toegevoegd, zijn de standaardprofielen voor Azure AD B2C de hoofdprofielen voor uw gebruikers. Gebruikers selecteren hun eigen gebruikersnaam (hun gewenste e-mailadres) en stellen een wachtwoord in. Azure AD B2C verifieert gebruikers rechtstreeks. 

Als verificatie via de provider van sociale identiteiten wordt toegevoegd en een gebruiker een van de aangeboden providers van sociale identiteiten kiest, wordt er nog steeds een entiteit gemaakt in de Azure AD B2C-tenant. Azure AD B2C verifieert vervolgens de referenties van de gebruiker met de provider van sociale identiteiten.

> [!NOTE]
> Er wordt een record van de aanmelding via de identiteitsprovider gemaakt in de B2C-Tenant, maar in een andere indeling dan lokale accounts, aangezien de externe provider van de sociale identiteiten wordt aangeroepen voor verificatie. De gebruiker kan hetzelfde e-mailadres gebruiken voor providers van sociale identiteiten, wat inhoudt dat de e-mailgebruikersnaam die voor verificatie wordt gebruikt mogelijk niet uniek is voor de tenant. Azure AD B2C dwingt alleen af dat gebruikers een uniek e-mailadres hebben op lokale B2C-accounts.

Voordat u een provider van sociale identiteiten voor verificatie kunt toevoegen, moet u naar de portal van de identiteitsprovider gaan en een toepassing van de identiteitsprovider instellen, zoals aangegeven in de documentatie van Azure AD B2C. Hieronder vindt u een lijst met koppelingen naar de documentatie.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Eén tenant)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-account](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Een provider van sociale identiteiten toevoegen en instellen

Voer de volgende stappen uit om een provider van sociale identiteiten toe te voegen en in te stellen.  

1. Navigeer in de Azure-portal naar **Identiteitsproviders**.
1. Selecteer **Toevoegen**. Het scherm **Identiteitsprovider toevoegen** wordt weergegeven.
1. Voer onder **Naam** de naam in die voor gebruikers moet worden weergegeven in uw aanmeldingsscherm.
1. Selecteer onder **Type identiteitsprovider** een identiteitsprovider in de lijst.
1. Selecteer **OK**.
1. Selecteer **Deze identiteitsprovider instellen** voor toegang tot het scherm **De provider van identiteiten instellen**.
1. Voer onder **Client-id** de client-id in die u hebt opgehaald uit de toepassingsinstellingen van de identiteitsprovider.
1. Voer onder **Clientgeheim** het clientgeheim in dat u hebt opgehaald uit de toepassingsinstellingen van de identiteitsprovider.
1. Gebruikersstroom voor beleid voor registreren en aanmelden koppelen:
1. Ga naar **Azure AD B2C - Gebruikersstromen (beleid) \> {uw beleid voor registreren en aanmelden} \> Identiteitsproviders**.
1. Als u het beleid voor gebruikersstromen voor registreren/aanmelden wilt bijvoegen, selecteert u de identiteitsproviders die u hebt ingesteld voor uw account. Als u deze wilt testen, selecteert u **Gebruikersstroom uitvoeren** voor elke identiteitsprovider. Op een nieuw tabblad wordt de aanmeldingspagina weergegeven met het selectievakje voor de nieuwe identiteitsprovider.

In de volgende afbeelding ziet u voorbeelden van de schermen **Identiteitsprovider toevoegen** en **De provider van identiteiten instellen** in Azure AD B2C.

![Een provider van sociale identiteiten toevoegen aan uw toepassing](./media/B2CImage_14.png)

De volgende afbeelding toont een voorbeeld van hoe u identiteitsproviders selecteert op de pagina Azure AD B2C-pagina **Identiteitsproviders**.

![De providers van sociale identiteiten selecteren die u wilt inschakelen voor uw beleid](./media/B2CImage_16.png)

In de volgende afbeelding ziet u een voorbeeld van een standaardscherm voor aanmelding waarin een knop voor aanmelding via de provider van de sociale identiteit wordt weergegeven.

> [!NOTE]
> Als u de aangepaste pagina's gebruikt die in Commerce zijn gebouwd voor uw gebruikersstromen, moeten de knoppen voor sociale identiteitsproviders worden toegevoegd met behulp van de uitbreidbaarheidsfuncties van de bibliotheek van de module Commerce. Bovendien kunnen URL- of configuratietekenreeksen in sommige gevallen hoofdlettergevoelig zijn bij het instellen van uw toepassingen bij een specifieke sociale identiteitsprovider. Raadpleeg de verbindingsinstructies van uw sociale identiteitsprovider voor meer informatie.
 
![Voorbeeld van standaardaanmeldingsscherm met knop voor aanmelding via provider van sociale identiteiten](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce Headquarters bijwerken met de nieuwe Azure AD B2C-informatie

Als de bovenstaande Azure AD B2C-inrichtingsstappen zijn voltooid, moet de Azure AD B2C-toepassing in uw Dynamics 365 Commerce-omgeving zijn geregistreerd.

Voer de volgende stappen uit Headquarters bij te werken met de nieuwe Azure AD B2C-informatie.

1. Ga in Commerce naar **Gedeelde Commerce-parameters** en selecteer **Identiteitsproviders** in het linkermenu.
1. Onder **Identiteitsproviders** doet u het volgende:
    1. Voer in het vak **Uitgever** de URL van de uitgevende identiteitsprovider in. Zie [Uitgevers-URL ophalen](#obtain-issuer-url) om de uitgevers-URL te vinden.
    1. Typ in het vak **Naam** een naam voor de uitgeversrecord.
    1. Voer in het vak **Type** de tekst **Azure AD B2C (id_token)** in.
1. Doe het volgende onder **Relying Party's** terwijl het bovenstaande item voor B2C-identiteitsproviders is geselecteerd:
    1. Voer in het vak **ClientID** de id van uw B2C-toepassing in. U vindt deze in het vak **Toepassings-id** op de eigenschappenpagina van de B2C-toepassing.
    1. Typ **Openbaar** in het vak **Type**.
    1. Typ **Klant** in het vak **Gebruikerstype**.
1. Selecteer **Opslaan** in het actievenster.
1. Zoek in het Commerce-zoekvak naar **Distributieplanning**.
1. Selecteer in het linkernavigatiemenu van de pagina **Distributieplanningen** de taak **1110 Algemene configuratie**.
1. Selecteer **Nu uitvoeren** in het actievenster.

### <a name="obtain-issuer-url"></a>Uitgevers-URL ophalen

Voer de volgende stappen uit om de uitgevers-URL van de identiteitsprovider te krijgen.
1. Navigeer op de Azure AD B2C-pagina van de Azure-portal naar uw gebruikersstroom **Registreren en aanmelden**.
1. Selecteer **Pagina-indelingen** in het linkernavigatiemenu, selecteer onder **Indelingsnaam** de optie **Gecombineerde pagina voor Registreren en aanmelden** en selecteer vervolgens **Gebruikersstroom uitvoeren**.
1. Zorg ervoor dat uw toepassing is ingesteld op de hierboven gemaakte Azure AD B2C-toepassing en selecteer vervolgens de koppeling onder de header **Gebruikersstroom uitvoeren** die ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` bevat.
1. Er wordt een metagegevenspagina weergegeven op het tabblad van uw browser. Kopieer de URL van de uitgever van de identiteitsprovider (de waarde voor **'uitgever'**).
   - Voorbeeld: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**OF**: voer de volgende stappen uit om handmatig dezelfde URL voor metagegevens te maken.

1. Maak metagegevensadres-URL met de volgende indeling met uw B2C-tenant en -beleid: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Voorbeeld: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Voer de metagegevensadres-URL in een browseradresbalk in.
1. Kopieer in de metagegevens de uitgevers-URL van de identiteitsprovider (de waarde voor **"issuer"**).
    - Voorbeeld: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Uw B2C-tenant configureren in Commerce Site Builder

Nadat de installatie van uw Azure AD B2C-tenant is voltooid, moet u de B2C-tenant configureren in Commerce Site Builder. Configuratiestappen zijn onder andere het verzamelen van B2C-toepassingsgegevens van de Azure-portal, het invoeren van die B2C-toepassingsgegevens in Site Builder en vervolgens het koppelen van de B2C-toepassing aan uw site en kanaal.

### <a name="collect-the-required-application-information"></a>De vereiste toepassingsgegevens verzamelen

Voer de volgende stappen uit om de vereiste toepassingsgegevens te verzamelen.

1. Ga in de Azure-portal naar **Start \> Azure AD B2C - Toepassingen**.
1. Selecteer de gewenste toepassing en selecteer in het linkernavigatievenster **Eigenschappen** om de toepassingsgegevens op te halen.
1. Verzamel in het vak **Toepassings-id** de toepassings-id van de B2C-toepassing die in de B2C-tenant is gemaakt. Deze wordt later ingevoerd als **client-GUID** in Site Builder.
1. Verzamel de antwoord-URL onder **Antwoord-URL**.
1. Ga naar **Start \> Azure AD B2C – Gebruikersstromen (beleid)** en verzamel vervolgens de namen van elk gebruikersstroombeleid.

In de volgende afbeelding ziet u een voorbeeld van de pagina **Azure AD B2C - Toepassingen**.

![Naar de B2C-toepassing navigeren binnen uw tenant](./media/B2CImage_19.png)

In de volgende afbeelding ziet u een voorbeeld van de pagina **Eigenschappen** van een toepassing in Azure AD B2C. 

![De toepassings-id uit de eigenschappen van de B2C-toepassing kopiëren](./media/B2CImage_21.png)

De volgende afbeelding toont een voorbeeld van een beleid voor gebruikersstromen op de pagina **Azure AD B2C – Gebruikersstromen (beleid)**.

![De namen van elke B2C-beleidsstroom verzamelen](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>De toepassingsgegevens van de AAD B2C-tenant invoeren in Commerce

U moet gegevens van de Azure AD B2C-tenant invoeren in Commerce Site Builder voordat u de B2C-tenant aan uw site(s) koppelt.

Ga als volgt te werk om uw toepassingsgegevens voor AAD B2C-tenants toe te voegen aan Commerce.

1. Meld u aan als beheerder van Commerce Site Builder voor uw omgeving.
1. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** om deze uit te vouwen.
1. Selecteer **B2C-instellingen** onder **Tenantinstellingen**. 
1. Selecteer **Beheren** in het hoofdvenster naast **B2C-toepassingen**. (Als uw tenant wordt weergegeven in de lijst met B2C-toepassingen, was deze al toegevoegd door een beheerder. Controleer of de items in stap 6 hieronder overeenkomen met de B2C-toepassing.)
1. Selecteer **B2C-toepassing toevoegen**.
1. Voer de volgende vereiste items in het weergegeven formulier in met waarden uit uw B2C-tenant en -toepassing. Velden die niet vereist zijn (zonder sterretje) kunnen leeg worden gelaten.

    - **Toepassingsnaam**: de naam voor uw B2C-toepassing, bijvoorbeeld Fabrikam B2C.
    - **Tenantnaam**: de naam van uw B2C-tenant (gebruik bijvoorbeeld "fabrikam" als het domein wordt weergegeven als "fabrikam.onmicrosoft.com" voor de B2C-tenant). 
    - **Id beleid voor vergeten wachtwoorden**: de id van het beleid voor de gebruikersstroom voor vergeten wachtwoorden, bijvoorbeeld B2C_1_PasswordReset.
    - **Beleids-id voor aanmelden registreren**: de beleids-id voor registreren en aanmelden, bijvoorbeeld B2C_1_signup_signin.
    - **Client-GUID**: de B2C-toepassings-id, bijvoorbeeld '22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6'.
    - **Profielbeleid-id bewerken**: de beleids-id voor het bewerken van gebruikersprofielen, bijvoorbeeld B2C_1A_ProfileEdit.

1. Selecteer **OK**. De naam van de B2C-toepassing wordt nu weergegeven in de lijst.
1. Klik op **Opslaan** om uw wijzigingen op te slaan.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>De B2C-toepassing koppelen aan uw site en kanaal

> [!WARNING]
> Als uw site al is gekoppeld aan een B2C-toepassing, worden bij het overschakelen naar een andere B2C-toepassing de huidige referenties verwijderd voor gebruikers die zich al hebben aangemeld in deze omgeving. Na wijziging zijn de referenties die aan de momenteel toegewezen B2C-toepassing zijn gekoppeld niet beschikbaar voor gebruikers. 
> 
> Werk de B2C-toepassing alleen bij als u de B2C-toepassing voor het kanaal voor de eerste keer instelt of als u wilt dat gebruikers zich opnieuw moeten aanmelden met nieuwe referenties voor dit kanaal met de nieuwe B2C-toepassing. Wees voorzichtig bij het koppelen van kanalen aan B2C-toepassingen en benoem toepassingen duidelijk. Als een kanaal niet is gekoppeld aan een B2C-toepassing in de onderstaande stappen, worden gebruikers die zich bij dat kanaal voor uw site aanmelden, in de B2C-toepassing ingevoerd als **standaard** in de lijst met B2C-toepassingen onder **Tenantinstellingen \> B2C-instellingen**.

Ga als volgt te werk om de B2C-toepassing te koppelen aan uw site en kanaal.

1. Ga naar de site in Commerce Site Builder.
1. Selecteer in het linkernavigatievenster de optie **Site-instellingen** om deze uit te vouwen.
1. Selecteer **Kanalen** onder **Site-instellingen**.
1. Selecteer uw kanaal in het hoofdvenster onder **Kanalen**.
1. Selecteer in het deelvenster voor kanaaleigenschappen aan de rechterkant de naam van de B2C-toepassing in de vervolgkeuzelijst **B2C-toepassing selecteren**.
1. Selecteer **Sluiten** en selecteer vervolgens **Opslaan en publiceren**.

## <a name="additional-b2c-information"></a>Aanvullende B2C-gegevens

### <a name="customer-migration"></a>Klantmigratie

Als u overweegt om klantrecords te migreren van een eerder platform van een identiteitsprovider, kunt u met het team van Dynamics 365 Commerce samenwerken om uw klantmigratiebehoeften te bekijken.

Zie [Gebruikers migreren naar Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration) voor aanvullende Azure AD B2C-documentatie over klantmigratie.

### <a name="custom-policies"></a>Aangepast beleid

Zie voor aanvullende informatie over het aanpassen van Azure AD B2C-interacties en beleidsstromen die verdergaan dan wat wordt aangeboden op basis van B2C-standaardbeleid [Aangepaste beleid in Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Secundaire beheerder

U kunt een optionele, secundaire beheerdersaccount toevoegen in de sectie **Gebruikers** van uw B2C-tenant. Dit kan een directe account of een algemene account zijn. Als u een account wilt delen tussen teamresources, kan ook een algemene account worden gemaakt. Vanwege de gevoeligheid van de gegevens die zijn opgeslagen in Azure AD B2C, moet een gemeenschappelijke account nauwkeurig worden gemonitord volgens de beveiligingsprocedures van uw bedrijf.

## <a name="additional-resources"></a>Aanvullende bronnen

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[robots.txt-bestanden beheren](manage-robots-txt-files.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

[Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-B2C-tenants.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
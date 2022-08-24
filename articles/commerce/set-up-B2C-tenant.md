---
title: Een B2C-tenant instellen in Commerce
description: In dit artikel wordt beschreven hoe u uw B2C-tenants (business-to-consumers) in Azure Active Directory (Azure AD) instelt voor de verificatie van sitegebruikers in Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 0b41d61c388e3723e3c30fa4dc0ae0055ffb1842
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271845"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Een B2C-tenant instellen in Commerce

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u uw B2C-tenants (business-to-consumers) in Azure Active Directory (Azure AD) instelt voor de verificatie van sitegebruikers in Dynamics 365 Commerce.

Dynamics 365 Commerce gebruikt Azure AD B2C om gebruikersreferenties en verificatiestromen te ondersteunen. Een gebruiker kan zich registreren en aanmelden, en vervolgens zijn/haar wachtwoord opnieuw instellen via deze stromen. Azure AD B2C slaat gevoelige gebruikersverificatiegegevens op, zoals de gebruikersnaam en het wachtwoord. In de gebruikersrecord in de B2C-tenant wordt een record voor een lokale B2C-account of een record voor een B2C-provider van sociale identiteiten opgeslagen. Deze B2C-records verwijzen weer naar de klantrecord in de Commerce-omgeving.

> [!WARNING] 
> Azure AD B2C stelt voor 1 augustus 2021 oude (legacy) gebruikersstromen buiten gebruik. Daarom moet u de migratie van uw gebruikersstromen naar de nieuwe aanbevolen versie gaan plannen. De nieuwe versie biedt functiepariteit en nieuwe functies. De modulebibliotheek voor Commerce versie 10.0.15 of hoger moet worden gebruikt met de aanbevolen B2C-gebruikersstromen. Zie [Gebruikersstromen in Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview) voor meer informatie.
 
 > [!NOTE]
 > Commerce-evaluatieomgevingen worden geleverd met een vooraf geladen Azure AD B2C-tenant voor demonstratiedoeleinden. Het laden van uw eigen Azure AD B2C-tenant met behulp van de onderstaande stappen is niet vereist voor evaluatieomgevingen.

> [!TIP]
> U kunt uw sitegebruikers nog verder beschermen en de beveiliging van uw Azure AD B2C-tenants verbeteren met Azure AD Identity Protection en Conditional Access. Voor meer informatie over de beschikbare mogelijkheden voor Azure AD B2C Premium P1- en Premium P2-p2-tenants: zie [Identity Protection en Conditional Access voor Azure AD B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview)

## <a name="dynamics-environment-prerequisites"></a>Dynamics-omgevingsvereisten

Voordat u begint, moet u ervoor zorgen dat uw Dynamics 365 Commerce-omgeving en e-commercekanaal correct zijn geconfigureerd door aan het volgende te voldoen.

- Stel de POS-bewerkingen **AllowAnonymousAccess** waarde in op "1" in Commerce headquarters:
    1. Naar **POS-bewerkingen** gaan.
    1. Klik met de rechtermuisknop in het raster en klik vervolgens op **Aanpassen**.
    1. Selecteer **Veld toevoegen**.
    1. Selecteer in de lijst met beschikbare kolommen de kolom **AllowNymousAccess** om deze toe te voegen.
    1. Selecteer **Bijwerken**.
    1. Wijzig **AllowNymousAccess** voor de bewerking **612** "Klant toevoegen" naar 1.
    1. Voer de taak **1090 (Kassa's)** uit.
- Stel het **handmatige** kenmerk van de nummerreeksklantrekening in op **Nee** in Commerce headquarters:
    1. Ga naar **Retail en Commerce \> Instelling van Headquarters \> Parameters \> klantenparameters**.
    1. Selecteer **Nummerreeksen**.
    1. Dubbelklik in de rij **Klantaccount** op de waarde **Nummerreekscode**.
    1. Stel in het sneltabblad **Algemeen** van de nummerreeks **Handmatig** in op **Nee**.

Na implementatie van uw Dynamics 365 Commerce-omgeving is het ook aan te raden om [seed data](enable-configure-retail-functionality.md) te initialiseren in de omgeving.

## <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal

In deze sectie wordt het maken of koppelen van een Azure AD B2C-tenant voor gebruik op uw Commerce-site behandeld. Zie [Zelfstudie: Een Azure Active Directory B2C-tenant maken](/azure/active-directory-b2c/tutorial-create-tenant) voor meer informatie.

1. Meld u aan bij de [Azure-portal](https://portal.azure.com/).
1. Selecteer **Een resource maken** in het menu van Azure Portal. Gebruik het abonnement en de map die met uw Commerce-omgeving worden verbonden.

    ![Een resource maken in Azure Portal.](./media/B2CImage_1.png)

1. Ga naar **Identiteit \> Azure Active Directory B2C**.
1. Op de pagina **Nieuwe B2C-tenant maken of koppelen aan bestaande tenant maken** gebruikt u een van de volgende opties die het beste aansluit bij de behoeften van uw bedrijf:

    - **Een nieuwe Azure AD B2C-tenant maken**: gebruik deze optie om een nieuwe Azure AD B2C-tenant te maken.
        1. Selecteer **Een nieuwe Azure AD B2C-tenant maken**.
        1. Voer onder **Naam van organisatie** de naam van de organisatie in.
        1. Voer bij **Oorspronkelijke domeinnaam** de oorspronkelijke domeinnaam in.
        1. Selecteer het land of de regio bij **Land of regio**.
        1. Selecteer **Maken** om de tenant te maken.

     ![Een nieuwe Azure AD-tenant maken.](./media/B2CImage_2.png)

     - **Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**: gebruik deze optie als u al een Azure AD B2C-tenant hebt waarmee u een koppeling tot stand wilt brengen.
        1. Selecteer **Een bestaande Azure AD B2C-tenant koppelen aan mijn Azure-abonnement**.
        1. Selecteer bij **Azure AD B2C-tenant** de geschikte B2C-tenant. Als het bericht Geen B2C-tenants gevonden die in aanmerking komen wordt weergegeven in het selectievak, beschikt u niet over een bestaande B2C-tenant die in aanmerking komt en moet u een nieuwe maken.
        1. Selecteer **Nieuwe maken** voor **Resourcegroep**. Voer een **naam** in voor de resourcegroep die de tenant moet bevatten, selecteer **de locatie de resourcegroep** en selecteer vervolgens **Maken**.

    ![Een bestaande Azure AD B2C-tenant koppelen aan een Azure-abonnement.](./media/B2CImage_3.png)

1. Zodra de nieuwe Azure AD B2C-map is gemaakt (dit kan even duren), wordt een koppeling naar de nieuwe map weergegeven op het dashboard. Met deze koppeling wordt u naar de pagina Welkom bij Azure Active Directory B2C geleid.

    ![Koppeling naar nieuwe Azure AD-directory](./media/B2CImage_4.png)

> [!NOTE]
> Als u meerdere abonnementen hebt in uw Azure-account of als u de B2C-tenant hebt ingesteld zonder deze aan een actief abonnement te koppelen, kunt u via een banner **Problemen oplossen** de tenant aan een abonnement koppelen. Selecteer het probleemoplossingsbericht en volg de instructies om het probleem met het abonnement op te lossen.

In de volgende afbeelding ziet u een voorbeeld van een Azure AD B2C-banner **Problemen oplossen**.

![Waarschuwing met de melding dat voor de map geen actief abonnement bestaat.](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>De B2C-toepassing maken

Nadat de B2C-tenant is gemaakt, maakt u een B2C-toepassing in uw nieuwe Azure AD B2C-tenant om te communiceren met Commerce.

Ga als volgt te werk om de B2C-toepassing te maken:

1. Selecteer in de Azure-portal de optie **App-registraties** en selecteer vervolgens **Nieuwe registratie**.
1. Voer onder **Naam** de naam in die u aan deze Azure AD B2C-toepassing wilt geven.
1. Selecteer onder **Ondersteunde accounttypen** de optie **Accounts in een identiteitsprovider of organisatiemap (voor het verifiëren van gebruikers met gebruikersstromen)**.
1. Voer voor **Omleidings-URI** uw speciale antwoord-URL's in als type **Web**. Zie [Antwoord-URL's](#reply-urls) hieronder voor informatie over antwoord-URL's en hoe u deze kunt opmaken. Er moet een omleidings-URI/antwoord-URL worden ingevoerd om omleidingen van Azure AD B2C terug naar uw site in te schakelen wanneer een gebruiker verifieert. De antwoord-URL kan tijdens het registratieproces worden toegevoegd of later worden toegevoegd door de koppeling **Omleidings-URI toevoegen** te selecteren in het menu **Overzicht** in de sectie **Overzicht** van de B2C-toepassing.
1. Selecteer voor **Machtigingen** de optie **Beheerdersmachtigingen verlenen voor de machtigingen openid en offline_access**.
1. Selecteer **Registreren**.
1. Selecteer de nieuw gemaakte toepassing en navigeer naar het menu **Verificatie**. 
1. Als een antwoord-URL is ingevoerd, selecteert u onder **Impliciete toekenning en hybride stromen** de opties **Toegangstokens** en **ID-tokens** om deze voor de toepassing in te schakelen en selecteert u **Opslaan**. Als een antwoord-URL niet is ingevoerd tijdens de registratie, kunt u deze ook op deze pagina toevoegen door **Een platform toevoegen** te selecteren, **Web** te selecteren, en vervolgens de omleidings-URI van de toepassing in te voeren. De sectie **Impliciete toekenning en hybride stromen** is vervolgens beschikbaar voor het selecteren van zowel **Toegangstokens** als **ID-tokens**.
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

U kunt ervoor kiezen om de standaardgebruikersstromen van Azure AD te gebruiken. Vervolgens wordt er een pagina weergegeven die wordt gehost door Azure AD B2C. U kunt ook een HTML-pagina maken om het uiterlijk van deze gebruikersstroomervaringen te bepalen. 

Zie [Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md) als u de gebruikersbeleidspagina's wilt aanpassen met pagina's die zijn gebouwd in Dynamics 365 Commerce. Zie voor aanvullende informatie [De interface met gebruikerservaringen in Azure Active Directory B2C aanpassen](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Een gebruikersstroombeleid voor registreren en aanmelden maken

Voer de volgende stappen uit om een gebruikersstroombeleid voor registreren en aanmelden te maken.

1. Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.
1. Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.
1. Selecteer het beleid **Registreren en aanmelden** en selecteer vervolgens de versie **Aanbevolen**.
1. Voer een beleidsnaam in onder **Naam**. Deze naam wordt vervolgens weer gegeven met een voorvoegsel dat wordt toegewezen door de portal (bijvoorbeeld B2C_1_).
1. Selecteer onder **Identiteitsproviders** in de sectie **Lokale accounts** de optie **E-mailaanmelding**. E-mailverificatie wordt gebruikt in de meeste algemene scenario's voor Commerce. Als u ook de verificatie via providers van sociale identiteiten gebruikt, kunt u deze op dit moment ook selecteren.
1. Selecteer de juiste keuze voor uw bedrijf onder **Meervoudige verificatie**. 
1. Selecteer onder **Gebruikerskenmerken en claims** opties om kenmerken te verzamelen of claims naar wens te retourneren. Selecteer **Meer weergeven...** om de volledige lijst met kenmerken en claimopties te bekijken. Voor Commerce zijn de volgende standaardopties vereist:

    | **Kenmerk verzamelen** | **Claim retourneren** |
    | ---------------------- | ----------------- |
    | E-mailadres          | E-mailadressen   |
    | Voornaam             | Voornaam        |
    |                        | Identiteitsprovider |
    | Achternaam                | Achternaam           |
    |                        | De object-id van de gebruiker  |

1. Selecteer **Maken**.

De volgende afbeelding is een voorbeeld van de gebruikersstroom voor registreren en aanmelden voor Azure AD B2C.

![Beleidsinstellingen voor registreren en aanmelden.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Een beleid voor de gebruikersstroom voor het bewerken van profielen maken

Voer de volgende stappen uit om een gebruikersstroombeleid voor het bewerken van profielen te maken.

1. Selecteer **Gebruikersstromen (beleid)** in het linkernavigatievenster van de Azure-portal.
1. Selecteer op de pagina **Azure AD B2C - Gebruikersstromen (beleid)** de optie **Nieuwe gebruikersstroom**.
1. Selecteer **Profielen bewerken** en selecteer vervolgens de versie **Aanbevolen**.
1. Voer onder **Naam** de gebruikersstroom voor het bewerken van profielen in. Deze naam wordt vervolgens weer gegeven met een voorvoegsel dat wordt toegewezen door de portal (bijvoorbeeld B2C_1_).
1. Selecteer onder **Identiteitsproviders** in het gedeelte **Lokale accounts** de optie **E-mailaanmelding**.
1. Schakel onder **Gebruikerskenmerken** de volgende selectievakjes in:
    
    | **Kenmerk verzamelen** | **Claim retourneren** |
    | ---------------------- | ----------------- |
    |                        | E-mailadressen   |
    | Voornaam             | Voornaam        |
    |                        | Identiteitsprovider |
    | Achternaam                | Achternaam           |
    |                        | De object-id van de gebruiker  |
    
1. Selecteer **Maken**.

In de volgende afbeelding ziet u een voorbeeld van de gebruikersstroom voor het bewerken van profielen in Azure AD B2C.

![Voorbeeld van de gebruikersstroom voor het bewerken van Azure AD B2C-profielen](./media/B2CImage_12.png)

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

![Een provider van sociale identiteiten toevoegen aan uw toepassing.](./media/B2CImage_14.png)

De volgende afbeelding toont een voorbeeld van hoe u identiteitsproviders selecteert op de pagina Azure AD B2C-pagina **Identiteitsproviders**.

![De providers van sociale identiteiten selecteren die u wilt inschakelen voor uw beleid.](./media/B2CImage_16.png)

In de volgende afbeelding ziet u een voorbeeld van een standaardscherm voor aanmelding waarin een knop voor aanmelding via de provider van de sociale identiteit wordt weergegeven.

> [!NOTE]
> Als u de aangepaste pagina's gebruikt die in Commerce zijn gebouwd voor uw gebruikersstromen, moeten de knoppen voor sociale identiteitsproviders worden toegevoegd met behulp van de uitbreidbaarheidsfuncties van de bibliotheek van de module Commerce. Bovendien kunnen URL- of configuratietekenreeksen in sommige gevallen hoofdlettergevoelig zijn bij het instellen van uw toepassingen bij een specifieke sociale identiteitsprovider. Raadpleeg de verbindingsinstructies van uw sociale identiteitsprovider voor meer informatie.
 
![Voorbeeld van standaardaanmeldingsscherm met knop voor aanmelding via provider van sociale identiteiten.](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce Headquarters bijwerken met de nieuwe Azure AD B2C-informatie

Als de bovenstaande Azure AD B2C-inrichtingsstappen zijn voltooid, moet de Azure AD B2C-toepassing in uw Dynamics 365 Commerce-omgeving zijn geregistreerd.

Voer de volgende stappen uit Headquarters bij te werken met de nieuwe Azure AD B2C-informatie.

1. Ga in Commerce naar **Gedeelde Commerce-parameters** en selecteer **Identiteitsproviders** in het linkermenu.
1. Onder **Identiteitsproviders** doet u het volgende:
    1. Voer in het vak **Uitgever** de tekenreeks van de uitgevende identiteitsprovider in. Zie [Tekenreeks van uitgever verkrijgen voor het instellen van Headquarters](#obtain-issuer-string-for-headquarters-setup) hieronder voor de tekenreeks van uw uitgever.
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

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Tekenreeks van uitgever verkrijgen voor het instellen van Headquarters

Voer de volgende stappen uit om de uitgeverstekenreeks van de identiteitsprovider te krijgen.

1. Navigeer op de Azure AD B2C-pagina van de Azure-portal naar uw gebruikersstroom **Registreren en aanmelden**.
1. Selecteer **Pagina-indelingen** in het linkernavigatiemenu, selecteer onder **Indelingsnaam** de optie **Gecombineerde pagina voor Registreren en aanmelden** en selecteer vervolgens **Gebruikersstroom uitvoeren**.
1. Zorg ervoor dat uw toepassing is ingesteld op de hierboven gemaakte Azure AD B2C-toepassing en selecteer vervolgens de gebruikersstroomkoppeling onder de header **Gebruikersstroom uitvoeren** die ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` bevat. (Selecteer niet **Gebruikersstroom uitvoeren**.) Er wordt een nieuw tabblad geopend met metagegevens voor het beleid om de tekenreeks van de uitgever te verzamelen.
1. Kopieer op de metagegevenspagina die in uw browsertabblad wordt weergegeven de tekenreeks van de uitgever van de identiteitsprovider (de waarde voor **Uitgever** die begint met "https://" en eindigt op "/v2.0/") die lijkt op het volgende voorbeeld.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
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

1. Ga in de Azure-portal naar **Start \> Azure AD B2C - App-registraties**.
1. Selecteer uw toepassing en selecteer in het linkernavigatievenster **Overzicht** om de toepassingsgegevens op te halen.
1. Verzamel in het vak **Id van toepassing (client)** de toepassings-id van de B2C-toepassing die in uw B2C-tenant is gemaakt. Deze wordt later ingevoerd als **client-GUID** in Site Builder.
1. Selecteer **Omleidings-URI´s** en verzamel de antwoord-URL die voor uw site wordt weergegeven (de antwoord-URL die is ingevoerd bij de setup).
1. Ga naar **Start \> Azure AD B2C – Gebruikersstromen** en verzamel vervolgens de volledige namen van elk gebruikersstroombeleid.

In de volgende afbeelding ziet u een voorbeeld van de overzichtspagina **Azure AD B2C - App-registraties**.

![Overzichtspagina Azure AD B2C - App-registraties met de id van toepassing (client) gemarkeerd](./media/ClientGUID_Application_AzurePortal.png)

De volgende afbeelding toont een voorbeeld van een beleid voor gebruikersstromen op de pagina **Azure AD B2C – Gebruikersstromen (beleid)**.

![De namen van elke B2C-beleidsstroom verzamelen.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>De toepassingsgegevens van de Azure AD B2C-tenant invoeren in Commerce

U moet gegevens van de Azure AD B2C-tenant invoeren in Commerce Site Builder voordat u de B2C-tenant aan uw site(s) koppelt.

Ga als volgt te werk om uw toepassingsgegevens voor Azure AD B2C-tenants toe te voegen aan Commerce.

1. Meld u aan als beheerder van Commerce Site Builder voor uw omgeving.
1. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** om deze uit te vouwen.
1. Selecteer onder **Tenantinstellingen** **Instellingen voor siteverificatie**. 
1. Selecteer **Beheren** in het hoofdvenster naast **Profielen voor siteverificatie**. (Als uw tenant wordt weergegeven in de lijst met siteverificatieprofielen, was deze al toegevoegd door een beheerder. Controleer of de items in stap 6 hieronder overeenkomen met de bedoelde B2C-instellingen. Er kan ook een nieuw profiel worden gemaakt met vergelijkbare Azure AD B2C-tenants of toepassingen om kleine verschillen te verantwoorden, zoals verschillende gebruikersbeleids-id's).
1. Selecteer **Siteverificatieprofiel toevoegen**.
1. Voer de volgende vereiste items in het weergegeven formulier in met waarden uit uw B2C-tenant en -toepassing. Velden die niet vereist zijn (zonder sterretje) kunnen leeg worden gelaten.

    - **Toepassingsnaam**: de naam voor uw B2C-toepassing, bijvoorbeeld Fabrikam B2C.
    - **Tenantnaam**: de naam van uw B2C-tenant (gebruik bijvoorbeeld "fabrikam" als het domein wordt weergegeven als "fabrikam.onmicrosoft.com" voor de B2C-tenant). 
    - **Id beleid voor vergeten wachtwoorden**: de id van het beleid voor de gebruikersstroom voor vergeten wachtwoorden, bijvoorbeeld B2C_1_PasswordReset.
    - **Beleids-id voor aanmelden registreren**: de beleids-id voor registreren en aanmelden, bijvoorbeeld B2C_1_signup_signin.
    - **Client-GUID**: de B2C-toepassings-id, bijvoorbeeld '22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6'.
    - **Profielbeleid-id bewerken**: de beleids-id voor het bewerken van gebruikersprofielen, bijvoorbeeld B2C_1A_ProfileEdit.

1. Selecteer **OK**. De naam van de B2C-toepassing wordt nu weergegeven in de lijst.
1. Klik op **Opslaan** om uw wijzigingen op te slaan.

Het optionele veld **Aangepast domein voor aanmelding** mag alleen worden gebruikt als u een aangepast domein instelt voor de Azure AD B2C-tenant. Zie [Aanvullende B2C-informatie](#additional-b2c-information) voor meer informatie en overwegingen over het gebruik van het veld **Aangepast domein voor aanmelding**.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>De B2C-toepassing koppelen aan uw site en kanaal

> [!WARNING]
> - Als uw site al is gekoppeld aan een B2C-toepassing, worden bij het overschakelen naar een andere B2C-toepassing de huidige referenties verwijderd voor gebruikers die zich al hebben aangemeld in deze omgeving. Na wijziging zijn de referenties die aan de momenteel toegewezen B2C-toepassing zijn gekoppeld niet beschikbaar voor gebruikers. 
> - Werk de B2C-toepassing alleen bij als u de B2C-toepassing voor het kanaal voor de eerste keer instelt of als u wilt dat gebruikers zich opnieuw moeten aanmelden met nieuwe referenties voor dit kanaal met de nieuwe B2C-toepassing. Wees voorzichtig bij het koppelen van kanalen aan B2C-toepassingen en benoem toepassingen duidelijk. Als een kanaal niet is gekoppeld aan een B2C-toepassing in de onderstaande stappen, worden gebruikers die zich bij dat kanaal voor uw site aanmelden, in de B2C-toepassing ingevoerd als **standaard** in de lijst met B2C-toepassingen onder **Tenantinstellingen \> B2C-instellingen**.

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

### <a name="set-up-a-custom-sign-in-domain"></a>Een aangepast aanmeldingsdomein instellen

Met Azure AD B2C kunt u een aangepast aanmeldingsdomein instellen voor de Azure AD B2C-tenant. Zie [Aangepaste domeinen voor Azure Active Directory B2C inschakelen](/azure/active-directory-b2c/custom-domain) voor instructies. 

Als u een aangepast aanmeldingsdomein gebruikt, moet het domein worden ingevoerd in Commerce Site Builder.

Voer de volgende stappen uit om een aangepast domein voor aanmelding in Site Builder in te voeren.

1. Selecteer Sites wisselen in de rechterbovenhoek van de Site Builder en vervolgens **Sites beheren**.
1. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen \> Instellingen voor siteverificatie**.
1. Selecteer **Beheren** in de sectie **Profielen voor siteverificatie**.
1. Selecteer in het flyoutmenu aan de rechterkant de knop **Bewerken** (potloodsymbool) naast het siteverificatieprofiel voor wie u een aangepast domein wilt invoeren.
1. Voer in het dialoogvenster **Siteverificatieprofiel bewerken** onder **Aangepast domein voor aanmelding** uw aangepaste aanmeldingsdomein in (bijvoorbeeld 'login.fabrikam.com').

> [!WARNING]
> Wanneer u een aangepast domein voor de Azure AD B2C-tenant bijwerkt, heeft de wijziging invloed op de uitgeverdetails van de tenant voor het gegenereerde token. De uitgeverdetails omvatten vervolgens het aangepaste domein in plaats van het standaarddomein dat door Azure AD B2C wordt geleverd. Een andere **Uitgeverconfiguratie** in Commerce Headquarters (**Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde handelparameters \> Identiteitsproviders**) wijzigt de interactie van het systeem met sitegebruikers, waardoor mogelijk een nieuwe klantrecord wordt gemaakt als een gebruiker wordt geverifieerd met de nieuwe uitgever. Eventuele wijzigingen in het aangepaste domein moeten grondig worden getest voordat u overschakelt naar het aangepaste domein in een live Azure AD B2C-omgeving.

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

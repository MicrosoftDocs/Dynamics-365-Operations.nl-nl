---
title: Beleid voor gebruikersstromen maken
description: In dit artikel wordt beschreven hoe u beleid voor gebruikersstromen maakt in de Microsoft Azure-portal.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785253"
---
# <a name="create-user-flow-policies"></a>Beleid voor gebruikersstromen maken

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u beleid voor gebruikersstromen maakt in de Microsoft Azure-portal.

Gebruikersstromen zijn de beleidsregels die Azure Active Directory (Azure AD) voor B2C gebruikt om veilige gebruikerservaringen voor registeren, aanmelden, profielbewerkingen en vergeten wachtwoorden te bieden. Dynamics 365 Commerce gebruikt deze stromen om de beleidsacties uit te voeren om te communiceren met de Azure AD B2C-tenant. Wanneer een gebruiker met dit beleid communiceert, wordt deze omgeleid naar de Azure AD B2C-tenant om de acties uit te voeren.

Azure AD B2C biedt drie algemene typen gebruikersstromen:
- Registreren en aanmelden
- Profiel bewerken
- Wachtwoord opnieuw instellen

U kunt ervoor kiezen om de standaardgebruikersstromen van Azure AD te gebruiken. Vervolgens wordt er een pagina weergegeven die wordt gehost door Azure AD B2C. U kunt ook een HTML-pagina maken om het uiterlijk van deze gebruikersstroomervaringen te bepalen. 

Zie [Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md) als u de gebruikersbeleidspagina's wilt aanpassen met pagina's die zijn gebouwd in Dynamics 365 Commerce. Zie voor meer informatie [De interface met gebruikerservaringen in Azure Active Directory B2C aanpassen](/azure/active-directory-b2c/tutorial-customize-ui).

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

## <a name="next-steps"></a>Volgende stappen

Als u wilt doorgaan met het instellen van een B2C-tenant in Commerce, gaat u verder met [Providers van sociale identiteiten toevoegen](add-social-identity-providers.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md)

[De B2C-toepassing maken](create-b2c-app.md)

[Providers van sociale identiteiten toevoegen (optioneel)](add-social-identity-providers.md)

[Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md)

[Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Aanvullende B2C-gegevens](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

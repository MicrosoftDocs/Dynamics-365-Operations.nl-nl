---
title: Providers van sociale identiteiten toevoegen
description: In dit artikel wordt beschreven hoe u providers van sociale identiteiten toevoegt in de Microsoft Azure-portal.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785242"
---
# <a name="add-social-identity-providers"></a>Providers van sociale identiteiten toevoegen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u providers van sociale identiteiten toevoegt in de Microsoft Azure-portal.

Providers van sociale identiteiten stellen gebruikers in staat hun sociale accounts te gebruiken voor verificatie. Het toevoegen van verificatie via providers van sociale identiteiten is optioneel in Dynamics 365 Commerce. 

Als geen verificatie via de provider van sociale identiteiten wordt toegevoegd, zijn de standaard B2C-profielen van Azure Active Directory (Azure AD) de hoofdprofielen voor uw gebruikers. Gebruikers selecteren hun eigen gebruikersnaam (hun gewenste e-mailadres) en stellen een wachtwoord in. Azure AD B2C verifieert gebruikers rechtstreeks. 

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

> [!NOTE]
> Het toevoegen van providers van sociale identiteiten is een optionele stap bij het instellen van een B2C-tenants in Microsoft Dynamics 365 Commerce.

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
1. Als u het beleid voor gebruikersstromen voor registreren/aanmelden wilt bijvoegen, selecteert u de identiteitsproviders die u hebt ingesteld voor uw account. Als u de stromen wilt testen, selecteert u **Gebruikersstroom uitvoeren** voor elke identiteitsprovider. Op een nieuw tabblad wordt de aanmeldingspagina weergegeven met het selectievakje voor de nieuwe identiteitsprovider.

In de volgende afbeelding ziet u voorbeelden van de schermen **Identiteitsprovider toevoegen** en **De provider van identiteiten instellen** in Azure AD B2C.

![Een provider van sociale identiteiten toevoegen aan uw toepassing.](./media/B2CImage_14.png)

De volgende afbeelding toont een voorbeeld van hoe u identiteitsproviders selecteert op de pagina Azure AD B2C-pagina **Identiteitsproviders**.

![De providers van sociale identiteiten selecteren die u wilt inschakelen voor uw beleid.](./media/B2CImage_16.png)

In de volgende afbeelding ziet u een voorbeeld van een standaardscherm voor aanmelding waarin een knop voor aanmelding via de provider van de sociale identiteit wordt weergegeven.

> [!NOTE]
> Als u de aangepaste pagina's gebruikt die in Commerce zijn gebouwd voor uw gebruikersstromen, moeten de knoppen voor sociale identiteitsproviders worden toegevoegd met behulp van de uitbreidbaarheidsfuncties van de bibliotheek van de module Commerce. Bovendien kunnen URL- of configuratietekenreeksen in sommige gevallen hoofdlettergevoelig zijn bij het instellen van uw toepassingen bij een specifieke sociale identiteitsprovider. Raadpleeg de verbindingsinstructies van uw sociale identiteitsprovider voor meer informatie.
 
![Voorbeeld van standaardaanmeldingsscherm met knop voor aanmelding via provider van sociale identiteiten.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Volgende stappen

Als u wilt doorgaan met het instellen van een B2C-tenant in Commerce, gaat u verder naar [Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md)

[De B2C-toepassing maken](create-b2c-app.md)

[Beleid voor gebruikersstromen maken](create-user-flow-policies.md)

[Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md)

[Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Aanvullende B2C-gegevens](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

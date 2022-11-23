---
title: Uw B2C-tenant configureren in Commerce Site Builder
description: In dit artikel wordt beschreven hoe u uw B2C-tenants (business-to-consumers) configureert in de site builder van Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785262"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Uw B2C-tenant configureren in Commerce Site Builder

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u uw B2C-tenants (business-to-consumers) configureert in de site builder van Microsoft Dynamics 365 Commerce.

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

Het optionele veld **Aangepast domein voor aanmelding** mag alleen worden gebruikt als u een aangepast domein instelt voor de Azure AD B2C-tenant. Zie [Aanvullende B2C-informatie](additional-b2c-info.md) voor meer informatie en overwegingen over het gebruik van het veld **Aangepast domein voor aanmelding**.

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

## <a name="next-steps"></a>Volgende stappen

Als u wilt doorgaan met het instellen van een B2C-tenant in Commerce, gaat u verder met [Aanvullende B2C-gegevens](additional-b2c-info.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md)

[De B2C-toepassing maken](create-b2c-app.md)

[Beleid voor gebruikersstromen maken](create-user-flow-policies.md)

[Providers van sociale identiteiten toevoegen (optioneel)](add-social-identity-providers.md)

[Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md)

[Aanvullende B2C-gegevens](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

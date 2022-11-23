---
title: Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie
description: In dit artikel wordt beschreven hoe u Microsoft Dynamics 365 Commerce headquarters bijwerkt met over nieuwe Azure Active Directory (Azure AD) B2C-gegevens.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785263"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u Microsoft Dynamics 365 Commerce headquarters bijwerkt met over nieuwe Azure Active Directory (Azure AD) B2C-gegevens.

Als de bovenstaande Azure AD B2C-inrichtingsstappen zijn voltooid, moet de Azure AD B2C-toepassing in uw Dynamics 365 Commerce-omgeving zijn geregistreerd.

Voer de volgende stappen uit Headquarters bij te werken met de nieuwe Azure AD B2C-informatie.

1. Ga in Commerce naar **Gedeelde Commerce-parameters** en selecteer **Identiteitsproviders** in het linkermenu.
1. Onder **Identiteitsproviders** doet u het volgende:
    1. Voer in het vak **Uitgever** de tekenreeks van de uitgevende identiteitsprovider in. Zie [Tekenreeks van uitgever verkrijgen voor het instellen van Headquarters](#obtain-issuer-string-for-headquarters-setup) hieronder voor de tekenreeks van uw uitgever.
    1. Typ in het vak **Naam** een naam voor de uitgeversrecord.
    1. Voer in het vak **Type** de tekst **Azure AD B2C (id_token)** in.
1. Doe het volgende onder **Relying Party's** terwijl het bovenstaande item voor B2C-identiteitsproviders is geselecteerd:
    1. Voer in het vak **ClientID** uw B2C-toepassings-id in, die u kunt vinden in het vak **Toepassings-id** van de eigenschappenpagina van uw B2C-toepassing.
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

## <a name="next-steps"></a>Volgende stappen

Als u wilt doorgaan met het instellen van een B2C-tenant in Commerce, gaat u verder met [Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md)

[De B2C-toepassing maken](create-b2c-app.md)

[Beleid voor gebruikersstromen maken](create-user-flow-policies.md)

[Providers van sociale identiteiten toevoegen (optioneel)](add-social-identity-providers.md)

[Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Aanvullende B2C-gegevens](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

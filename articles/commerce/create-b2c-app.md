---
title: Een B2C-toepassing maken
description: In dit artikel wordt beschreven hoe u een B2C-toepassing (business-to-consumer) maakt in de Microsoft Azure-portal.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785243"
---
# <a name="create-a-b2c-application"></a>Een B2C-toepassing maken

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een B2C-toepassing (business-to-consumer) maakt in de Microsoft Azure-portal.

Nadat uw B2C-tenant is gemaakt, maakt u een B2C-toepassing in uw nieuwe Azure Active Directory (Azure AD)-tenant om te communiceren met Commerce.

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

## <a name="next-steps"></a>Volgende stappen

Als u wilt doorgaan met het instellen van een B2C-tenant in Commerce, gaat u verder met [Beleid voor gebruikersstromen maken](create-user-flow-policies.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md)

[Beleid voor gebruikersstromen maken](create-user-flow-policies.md)

[Providers van sociale identiteiten toevoegen (optioneel)](add-social-identity-providers.md)

[Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md)

[Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Aanvullende B2C-gegevens](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

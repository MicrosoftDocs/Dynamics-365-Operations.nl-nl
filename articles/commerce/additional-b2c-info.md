---
title: Aanvullende B2C-gegevens
description: Dit artikel biedt extra informatie over het instellen van uw B2C-tenants (business-to-consumer) in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785235"
---
# <a name="additional-b2c-information"></a>Aanvullende B2C-gegevens

[!include [banner](includes/banner.md)]

Dit artikel biedt extra informatie over het instellen van uw B2C-tenants (business-to-consumer) in Microsoft Dynamics 365 Commerce.

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
> Wanneer u een aangepast domein voor de Azure AD B2C-tenant bijwerkt, heeft de wijziging invloed op de uitgeverdetails van de tenant voor het gegenereerde token. De uitgeverdetails omvatten vervolgens het aangepaste domein in plaats van het standaarddomein dat door Azure AD B2C wordt geleverd. Een andere **Uitgeverconfiguratie** in Commerce headquarters (**Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde handelparameters \> Identiteitsproviders**) wijzigt de interactie van het systeem met sitegebruikers, waardoor mogelijk een nieuwe klantrecord wordt gemaakt als een gebruiker wordt geverifieerd met de nieuwe uitgever. Eventuele wijzigingen in het aangepaste domein moeten grondig worden getest voordat u overschakelt naar het aangepaste domein in een live Azure AD B2C-omgeving.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md)

[De B2C-toepassing maken](create-b2c-app.md)

[Beleid voor gebruikersstromen maken](create-user-flow-policies.md)

[Providers van sociale identiteiten toevoegen (optioneel)](add-social-identity-providers.md)

[Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md)

[Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

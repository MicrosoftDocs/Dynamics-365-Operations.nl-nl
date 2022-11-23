---
title: Een B2C-tenant instellen in Commerce
description: In dit artikel wordt beschreven hoe u uw B2C-tenants (business-to-consumers) in Azure Active Directory (Azure AD) instelt voor de verificatie van sitegebruikers in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785122"
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

## <a name="next-steps"></a>Volgende stappen

Als u wilt doorgaan met het instellen van een B2C-tenant in Commerce, gaat u naar [Een Azure AD B2C-tenant maken of een koppeling met een bestaande B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Een Azure AD B2C-tenant maken of een koppeling met een bestaande Azure AD B2C-tenant instellen in de Azure-portal](create-link-aad-b2c-tenant.md)

[De B2C-toepassing maken](create-b2c-app.md)

[Beleid voor gebruikersstromen maken](create-user-flow-policies.md)

[Providers van sociale identiteiten toevoegen (optioneel)](add-social-identity-providers.md)

[Commerce headquarters bijwerken met de nieuwe Azure AD B2C-informatie](update-hq-aad-b2c-info.md)

[Uw B2C-tenant configureren in Commerce Site Builder](config-b2c-tenant-site-builder.md)

[Aanvullende B2C-gegevens](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

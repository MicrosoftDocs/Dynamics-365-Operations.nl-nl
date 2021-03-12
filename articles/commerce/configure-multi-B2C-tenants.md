---
title: Meerdere B2C-tenants configureren in een Commerce-omgeving
description: In dit onderwerp wordt beschreven wanneer en hoe u meerdere Microsoft Azure Active Directory (Azure AD) B2C-tenants (Business-to-consumers) per kanaal instelt voor gebruikersverificatie in een specifieke Dynamics 365 Commerce-omgeving.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a1af453349d69ef94d725e138a898c73ea052fa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997595"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Meerdere B2C-tenants configureren in een Commerce-omgeving

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wanneer en hoe u meerdere Microsoft Azure Active Directory (Azure AD) B2C-tenants (Business-to-consumers) per kanaal instelt voor gebruikersverificatie in een specifieke Dynamics 365 Commerce-omgeving.

## <a name="overview"></a>Overzicht

Dynamics 365 Commerce gebruikt de Azure AD-B2C-cloudidentiteitsservice om gebruikersreferenties en verificatiestromen te ondersteunen. Gebruikers kunnen de verificatiestromen gebruiken om te registreren, om zich aan te melden en hun wachtwoord opnieuw in te stellen. Azure AD B2C slaat gevoelige gebruikersverificatiegegevens op, zoals de gebruikersnaam en het wachtwoord. De gebruikersrecord is uniek voor elke B2C-tenant en gebruikt de referenties voor de gebruikersnaam (e-mailadres) of de referentie van de sociale identiteitsprovider.

In de meeste gevallen wordt één Azure AD-B2C-tenant gebruikt in een Commerce-omgeving. Commerce-klanten kunnen vervolgens meerdere sites maken en publiceren in dezelfde Commerce-omgeving, en dezelfde klantreferenties worden op deze sites gebruikt. Als de sites in de omgeving echter moeten worden behandeld als verschillende merken en als afzonderlijke bedrijven worden weergegeven aan gebruikers, kan een B2C-tenant worden geconfigureerd voor het kanaal dat wordt gebruikt voor de site-/merkscheiding.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Overwegingen bij het instellen van meerdere B2C-tenants per kanaal

Wanneer elk kanaal of elke site wordt behandeld als een afzonderlijk bedrijf, is de beste optie met betrekking tot de gebruikersverificatiestromen in Commerce het gebruik van afzonderlijke rechtspersonen. Als u echter elk kanaal/elke site in dezelfde omgeving en rechtspersoon wilt bewaren, maar voor elke site afzonderlijke gebruikersverificatie wilt, is het belangrijk dat u de volgende punten in overweging neemt voordat u verdergaat:

- Gebruikers krijgen hun eigen referenties voor elk kanaal/elke site.

    Dezelfde persoon kan twee afzonderlijke accounts per kanaal/locatie hebben, omdat elk account een unieke vermelding in een afzonderlijke B2C-tenant is.

- In de Microsoft Dynamics-omgeving worden afzonderlijke klantrecords geretourneerd voor algemene zoekopdrachten voor records.

    Als een gebruiker hetzelfde e-mailadres gebruikt voor verschillende kanalen/site, worden algemene zoekopdrachten voor klanten resultaten voor elk kanaal/elke site geretourneerd. (Er wordt een kanaalindicator weergegeven.)

- U kunt het adresboek gebruiken om gebruikers te groeperen, zodat deze per kanaal kunnen worden bijgehouden.
- Het aantal klantrecords per kanaal kan toenemen en deze verhoging kan de prestaties van de algemene zoekopdrachten voor klanten beïnvloeden.
- B2C-tenants moeten zorgvuldig aan een kanaal worden toegewezen om situaties te helpen voorkomen waarin klanten zich aanmelden voor een onjuiste tenant. Anders kan er sprake zijn van verwarring of traceringsproblemen.

In de volgende afbeelding ziet u meerdere B2C-tenants in een Commerce-omgeving.

![Meerdere B2C-tenants in een Commerce-omgeving](media/MultiB2C_In_Environment.png)

Als u besluit dat voor uw bedrijf verschillende B2C-tenants per kanaal in dezelfde Commerce-omgeving vereist zijn, voert u de procedures in de volgende secties uit om deze functie aan te vragen.

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>Aanvragen om B2C per kanaal om te schakelen in uw omgeving

Als u op dit moment wilt dat afzonderlijke B2C-tenantsper kanaal beschikbaar zijn in dezelfde Commerce-omgeving, moet u een aanvraag indienen bij Dynamics 365 Commerce. Zie [Ondersteuning krijgen voor Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) voor meer informatie of bespreek dit probleem met uw contactpersoon voor Commerce-oplossingen.

## <a name="configure-b2c-tenants-in-your-environment"></a>B2C-tenants configureren in uw omgeving

Voer de relevante procedures in deze sectie uit om B2C-tenants in uw omgeving te configureren.

### <a name="add-an-azure-ad-b2c-tenant"></a>Een Azure AD-B2C-tenant toevoegen

Voer deze stappen uit om een Azure AD-B2C-tenant toe te voegen aan uw omgeving.

1. Meld u aan bij Commerce Site Builder voor uw omgeving als systeembeheerder. U moet systeembeheerder zijn voor de Commerce-omgeving om Azure AD-B2C-tenants te configureren.
1. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** om deze uit te vouwen.
1. Selecteer **B2C-instellingen** en selecteer vervolgens **Beheren**.
1. Selecteer **B2C-toepassing toevoegen** en voer de volgende informatie in:

    - **Toepassingsnaam**: voer de naam in die moet worden gebruikt voor de toepassing in de context van het beheer in Commerce. U wordt aangeraden de naam van de toepassing te gebruiken die u hebt gekozen bij het instellen van de Azure AD-B2C-toepassing in de Azure Portal. Op deze manier kunt u de verwarring beperken wanneer u B2C-tenants beheert in Commerce.
    - **Tenantnaam**: voer de B2C-tenantnaam in zoals deze wordt weergegeven in de Azure Portal.
    - **Id beleid voor vergeten wachtwoorden**: voer de beleids-id in (de naam van het beleid in de Azure Portal).
    - **Beleids-id voor aanmelden registreren**: voer de beleids-id in (de naam van het beleid in de Azure Portal).
    - **GUID van client**: voer de id van de Azure AD-B2C-tenant in zoals deze wordt weer gegeven in de Azure Portal (niet de toepassings-id voor de B2C-tenant).
    - **Profielbeleid-id bewerken.**: voer de beleids-id in (de naam van het beleid in de Azure Portal).

1. Wanneer u klaar bent met het invoeren van deze gegevens, selecteert u **OK** om de wijzigingen op te slaan.

> [!NOTE]
> U moet velden zoals **Bereik**, **Niet-interactieve beleids-id**, **Niet-interactieve client-id**, **Aangepast domein voor aanmelding** en **Beleids-id voor aanmelden** leeg laten tenzij het Dynamics 365 Commerce-team aangeeft dat u deze moet instellen.
Uw nieuwe Azure AD-B2C-tenant moet nu worden weergegeven in de lijst onder **B2C-toepassingen beheren**.

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Een Azure AD-B2C-tenant beheren of verwijderen

1. Meld u aan bij Commerce Site Builder voor uw omgeving als systeembeheerder. U moet systeembeheerder zijn voor de Commerce-omgeving om Azure AD-B2C-tenants te configureren.
1. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** om deze uit te vouwen.
1. Selecteer **B2C-instellingen** en selecteer vervolgens **Beheren**.
1. Als u een B2C-tenant wilt bewerken, selecteert u het potloodsymbool ernaast. Als u een B2C-tenant wilt verwijderen, selecteert u het prullenbaksymbool ernaast.
1. Selecteer **Opslaan** en **Publiceren** om uw wijzigingen te activeren.

> [!WARNING]
> Wanneer een B2C-tenant is geconfigureerd voor een live/gepubliceerde site, hebben gebruikers zich mogelijk aangemeld via accounts die aanwezig zijn in de tenant. Als u een geconfigureerde tenant verwijdert uit het menu **Tenant-instellingen \> B2C-tenant**, verwijdert u de koppeling van die B2C-tenant van sites die zijn gekoppeld aan kanalen van de tenant. In dit geval kunnen uw gebruikers zich niet meer aanmelden bij hun accounts. Wees daarom zeer voorzichtig wanneer u een geconfigureerde tenant verwijdert.
>
> Wanneer een geconfigureerde tenant wordt verwijderd, blijven de B2C-tenant en -records behouden, maar wordt de Commerce-systeemconfiguratie van die tenant gewijzigd of verwijderd. Gebruikers die zich aanmelden bij de site, maken een nieuwe accountrecord in de standaard- of nieuw gekoppelde B2C-tenant die is geconfigureerd voor het kanaal van de site.
## <a name="configure-your-channel-with-a-b2c-tenant"></a>Uw kanaal met een B2C-tenant configureren

1. Meld u aan bij Commerce Site Builder voor uw omgeving als systeembeheerder. U moet systeembeheerder zijn voor de Commerce-omgeving om Azure AD-B2C-tenants te configureren.
1. Selecteer in het linkernavigatievenster de optie **Site-instellingen** om deze uit te vouwen.
1. Selecteer **Kanalen** en selecteer vervolgens het kanaal dat u wilt configureren.
1. Selecteer in het deelvenster met eigenschappen aan de rechterkant in het veld **B2C-toepassing selecteren** de geconfigureerde Azure AD-B2C-tenant die voor dit kanaal moet worden gebruikt.
1. Selecteer op de opdrachtbalk de optie **Opslaan en publiceren** om de nieuwe of bijgewerkte configuratie door te voeren.

> [!WARNING]
> Als u de B2C-toepassing wijzigt die aan het kanaal is toegewezen, verwijdert u de huidige verwijzingen die zijn gemaakt voor alle gebruikers die zich al bij de omgeving hebben aangemeld. In dit geval zijn de referenties die aan de momenteel toegewezen B2C-toepassing zijn gekoppeld, niet beschikbaar voor gebruikers. Wijzig daarom de configuratie van een Azure AD-B2C-kanaal alleen als u het kanaal voor de eerste keer instelt en er geen gebruikers zijn die zich hebben kunnen aanmelden. Anders moeten gebruikers zich mogelijk opnieuw registreren om een record in de nieuwe Azure AD-B2C-tenant te maken.
## <a name="additional-resources"></a>Aanvullende bronnen

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[robots.txt-bestanden beheren](manage-robots-txt-files.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)

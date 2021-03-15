---
title: Overzicht van E-commerce
description: Dit onderwerp biedt een overzicht van de ondersteuning voor E-commerce-pagina's in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae220e98acbda99255beefea598d973dbaa22368
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997542"
---
# <a name="e-commerce-site-overview"></a>Overzicht van E-commerce

[!include [banner](includes/banner.md)]

Dit onderwerp biedt een overzicht van de ondersteuning voor E-commerce-pagina's in Microsoft Dynamics 365 Commerce. Het bevat informatie over de manier waarop e-commerce-online winkels worden geïnitialiseerd en beheerd in Dynamics 365 Commerce. Daarnaast vindt u hier koppelingen naar meer informatie over online winkels en informatie over het instellen en configureren van een e-commercepagina. Hoewel in dit onderwerp veel van de basisprincipes worden behandeld, is dit niet van toepassing op alles wat is vereist voor het instellen van een e-commercepagina voor productie. Meer geavanceerde onderwerpen vindt u in de Dynamics 365 Commerce-documentatie.

## <a name="online-store-channel"></a>Online winkelkanaal

Voordat u uw site kunt maken in Dynamics 365 Commerce, moet er minimaal één online kanaal zijn ingesteld. Zie [een online kanaal instellen](channel-setup-online.md) voor meer informatie. 

In Dynamics 365 Commerce gebruikt u een online kanaal om de producten, prijzen, talen, betaalmethoden, leveringsmethoden, verwerkingscentra en andere aspecten van de online ervaring vast te stellen die beschikbaar moeten zijn voor uw klanten.

Er hoeft slechts één online kanaal te worden ingesteld voordat u aan de slag kunt gaan met Dynamics 365 Commerce. Een enkele e-commerce-site kan echter de online ervaring voor meerdere online winkels bieden. Als meerdere online winkels bijvoorbeeld zijn ingesteld ter ondersteuning van verschillende geografische regio's, kan één set e-commercepagina's worden gebruikt om de unieke ervaringen te bieden die door elke winkel worden gedefinieerd. Zie [Een online-site koppelen aan een kanaal](associate-site-online-store.md) voor meer informatie over het configureren van een site voor de ondersteuning van meerdere online winkels.

Nadat een online winkel is ingesteld, kan deze worden gekoppeld aan de Dynamics 365 Commerce-site die als uw online winkel zal fungeren. Zie [Online winkels instellen](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores) voor meer informatie over online winkels en hoe u deze instelt.

## <a name="deploy-a-new-e-commerce-tenant"></a>Een nieuwe e-commerce-tenant implementeren

Tijdens de initialisatie van een e-commercepagina wordt u gevraagd een domeinnaam op te geven. Zie [Uw domeinnaam configureren](configure-your-domain-name.md) en [Domeinen in Dynamics 365 Commerce](domains-commerce.md) voor meer informatie over domeinen in Commerce. Als u een nieuwe e-commerce-tenant wilt implementeren met behulp van [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), volgt u de stappen in [Implementatie van een nieuwe e-commerce-tenant](deploy-ecommerce-site.md). Nadat uw e-commerce-tenant is ingesteld in LCS wordt er een koppeling naar een Commerce site builder geleverd. U kunt vervolgens Commerce site builder gebruiken om uw e-commercepagina's te initialiseren en te configureren.

## <a name="initialize-your-e-commerce-site"></a>Uw e-commercepagina initialiseren

Wanneer u Commerce site builder start vanuit LCS verschijnt de pagina **Pagina's**. Deze pagina bevat twee vooraf geconfigureerde sites, **standaard** en **fabrikam**, zoals wordt weergegeven in de volgende afbeelding.

![Pagina's van Commerce site builder](media/e-commerce-site-01.png)

Wanneer u een van deze sites selecteert, wordt u gevraagd een domeinnaam, een standaard online winkelkanaal, een ondersteunde taal voor het geselecteerde kanaal en een pad te selecteren. Als er slechts één kanaal wordt gebruikt, kunt u het pad leeg laten. Meer online winkelkanalen of -talen kunnen later worden geconfigureerd in Commerce site builder. Voor elk extra kanaal of elke taal is een uniek pad nodig. U hebt bijvoorbeeld twee online kanalen die aan één pagina zijn gekoppeld, en de domeinnaam voor de site is `www.fabrikam.com`. In dit geval kan het pad voor het ene kanaal de standaardwaarde zijn zonder pad (`https://www.fabrikam.com`) en kan het tweede kanaal worden ingesteld op een nieuw pad, zoals **site2**, dat de URL `https://www.fabrikam.com/site2` heeft. In de volgende afbeelding ziet u een voorbeeld van een dialoogvenster voor het initialiseren van sites in Commerce site builder.

![Het dialoogvenster site-initialisatie in Commerce site builder](media/e-commerce-site-02.png)

De pagina **Sites** bevat ook een knop **Nieuwe site**. Het dialoogvenster dat wordt weergegeven wanneer u deze knop kiest, lijkt op het dialoogvenster site-initialisatie, maar wordt gebruikt om een nieuwe site te maken. Nieuwe locaties zijn leeg. Ze bevatten niet dezelfde standaardsjablonen, fragmenten, pagina's en afbeeldingen die bij de **standaard-** en **fabrikam**-sites worden geleverd. Indien nodig kunt u een ondersteuningsticket openen om aan te vragen dat een kopie van de standaardinhoud wordt toegevoegd aan een nieuwe lege site. Zie voor meer informatie [Een e-commerce-site maken](create-ecommerce-site.md).

Nadat een nieuwe site is geïnitialiseerd, wordt de **start**-pagina voor Commerce Site Builder weergegeven. Deze pagina bevat koppelingen naar algemene acties en informatie over richtlijnen, zoals wordt weergegeven in het voorbeeld in de volgende afbeelding.

![Koppelingen op de startpagina in Commerce site builder](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Online winkelkanalen wijzigen of online winkelkanalen toevoegen aan een e-commerce site

Nadat u een e-commercesite hebt gemaakt, kunt u het kanaal waaraan het is gekoppeld wijzigen door de stappen uit te voeren in [Een e-commercesite aan een online kanaal koppelen](associate-site-online-store.md). In het voorbeeld in de volgende afbeelding ziet u hoe een operationeel eenheidsnummer (OUN) van een kanaal kan worden gewijzigd op de pagina **Kanalen** (**Site-instellingen \> Kanalen**). Nadat u een wijziging hebt aangebracht, selecteert u **Opslaan en publiceren**. Op deze manier zorgt u ervoor dat de wijziging wordt gepubliceerd.

![Kanaalpagina's van Commerce site builder](media/e-commerce-site-04.png)

U kunt nieuwe kanalen toevoegen door **Een kanaal toevoegen** te selecteren. Als u nieuwe talen aan een kanaal wilt toevoegen, selecteert u het kanaal en selecteert u **Een landinstelling toevoegen** in het kanaaldialoogvenster dat wordt weergegeven. Voordat u landinstellingen kunt weergeven in het dialoogvenster, moeten deze vooraf worden geconfigureerd voor het online winkelkanaal in Commerce Headquarters.

![Kanaaldialoogvenster in Commerce site builder](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Een Azure B2C-tenant instellen

Dynamics 365 Commerce gebruikt Azure Active Directory (Azure AD) B2C om gebruikersreferenties en verificatiestromen te ondersteunen. Zie [Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md), [Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md) en [Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-b2c-tenants.md) voor meer informatie over het instellen van de Azure B2C-tenant.

## <a name="overview-of-the-default-site-pages"></a>Overzicht van de standaard sitepagina's

De **standaard** en **fabrikam**-sites bevatten vooraf geconfigureerde sjablonen, fragmenten en pagina's om u te helpen aan de slag te gaan. Zie de volgende onderwerpen voor meer informatie:

- [Overzicht introductiepagina](quick-tour-home-page.md)
- [Overzicht van pagina met productgegevens](quick-tour-pdp.md)
- [Overzicht van pagina's met winkelwagen en kassa](quick-tour-cart-checkout.md)
- [Overzicht van pagina's voor rekeningbeheer](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Site-instellingen beheren

Zie de volgende onderwerpen voor informatie over het beheren van uw site-instellingen:

- [e-Commerce-gebruikers en -rollen beheren](manage-ecommerce-users-roles.md)
- [Overwegingen bij SEO (Search Engine Optimization) voor uw site](/search-engine-optimization-considerations.md)
- [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md)
- [Een thema voor de site selecteren](select-site-theme.md)

## <a name="manage-site-content"></a>Site-inhoud beheren

Zie de volgende onderwerpen voor informatie over het beheren van uw site-inhoud:

- [Woordenlijst voor paginamodellen](page-elements-overview.md)
- [Statussen en levenscyclus van document](document-states-overview.md)
- [Sjablonen en indeling](templates-layouts-overview.md)
- [Werken met fragmenten](work-with-fragments.md)
- [Werken met modules](work-with-modules.md)
- [Overzicht van digitaal activabeheer](dam-overview.md)
- [Overzicht van modulebibliotheek](starter-kit-overview.md)

## <a name="additional-resources"></a>Aanvullende bronnen

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een nieuwe e-commerce-site implementeren](deploy-ecommerce-site.md)

[Een online-site koppelen aan een kanaal](associate-site-online-store.md)

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
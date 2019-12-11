---
title: Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen
description: In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb757672fffb56892837c066d552773908dd1ec1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696963"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.

## <a name="overview"></a>Overzicht

Wanneer u een e-commerce-omgeving instelt in Dynamics 365 Commerce, kunt u deze configureren om met uw CDN-service te werken. 

Het aangepaste domein kan tijdens het inrichtingsproces voor uw e-commerce-omgeving worden ingeschakeld. U kunt ook een serviceaanvraag gebruiken om deze in te stellen nadat het inrichtingsproces is voltooid. Het inrichtingsproces voor de e-commerce-omgeving genereert een hostnaam die aan de omgeving wordt gekoppeld. Deze hostnaam heeft de volgende indeling, waarbij *e-commerce-tenant-name* de naam van uw omgeving is:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

De hostnaam of het eindpunt dat tijdens het inrichtingsproces wordt gegenereerd, ondersteunt alleen een Secure Sockets Layer-certificaat (SSL) voor \*.commerce.dynamics.com. SSL wordt niet ondersteund voor aangepaste domeinen. Daarom moet u SSL beëindigen voor aangepaste domeinen in uw CDN en verkeer doorsturen van de CDN naar de hostnaam of het eindpunt dat door Commerce wordt gegenereerd. 

Bovendien worden de *statische* onderdelen (Javascript- of \[CSS\]-bestanden (Cascading Style Sheets)) van Commerce verzonden vanaf het eindpunt dat door Commerce wordt gegenereerd (\*.commerce.dynamics.com). De statische onderdelen kunnen alleen in de cache worden geplaatst, als de hostnaam of het eindpunt dat door Commerce gegenereerd wordt, achter het CDN wordt geplaatst.

## <a name="set-up-ssl"></a>SSL instellen

Om ervoor te zorgen dat de SSL-configuratie wordt ingesteld en dat de statische onderdelen in de cache worden opgeslagen, moet u uw CDN zo configureren dat dit is gekoppeld aan de hostnaam die door Commerce wordt gegenereerd voor uw omgeving. U moet ook het volgende patroon in cache opslaan, alleen voor statische onderdelen: 

/\_msdyn365/\_scnr/\*

Nadat u uw Commerce-omgeving hebt ingericht met het aangepaste domein dat is opgegeven of nadat u het aangepaste domein voor uw omgeving hebt opgegeven met behulp van een serviceaanvraag, wijst u uw aangepaste domein toe aan de hostnaam of het eindpunt dat door Commerce is gegenereerd.

Zoals eerder is vermeld, ondersteunt de gegenereerde hostnaam of het eindpunt alleen een SSL-certificaat voor \*.commerce.dynamics.com. SSL wordt niet ondersteund voor aangepaste domeinen.

## <a name="cdn-services"></a>CDN-services

Een CDN-service kan met een Commerce-omgeving worden gebruikt. Hieronder vindt u twee voorbeelden:

- **Microsoft Azure Front Door Service**: de Azure CDN-oplossing. Meer informatie over de Azure Front Door Service vindt u in [Documentatie bij Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator**: zie voor meer informatie [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN-instellingen

Het CDN-installatieproces bestaat uit de volgende algemene stappen:

1. Een front-endhost toevoegen.
1. Een back-endgroep configureren.
1. Regels voor routering en caching instellen.

### <a name="add-a-front-end-host"></a>Een front-endhost toevoegen

U kunt elke CDN-service gebruiken, maar voor het voorbeeld in dit onderwerp wordt de Azure Front Door Service gebruikt. 

Voor informatie over het instellen van de Azure Front Door Service raadpleegt u [Beknopte gids voor Front Door Service voor een algemene webtoepassing met hoge beschikbaarheid](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Een back-endgroep configureren in Azure Front Door Service

Volg deze stappen om een back-endgroep te configureren in Azure Front Door Service.

1. Voeg **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** toe aan een back-endgroep als een aangepaste host met een lege koptekst voor de back-endhost.
1. Voer onder **Statusprobes** in het veld **Pad** **/keepalive** in.
1. Voer in het veld **Intervallen (seconden)** **255** in.
1. Laat de standaardwaarden staan onder **Taakverdeling**.

In de volgende afbeelding ziet u het dialoogvenster **Een backend-groep toevoegen** in de Azure Front Door Service.

![Het dialoogvenster Een backend-groep toevoegen](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Regels in de Azure Front Door Service instellen

Voer de volgende stappen uit om een routeringsregel in te stellen in de Azure Front Door Service.

1. Voeg een routeringregel toe.
1. Voer in het veld **Naam** de tekst **standaard** in.
1. Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.
1. Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.
1. Voer onder **Af te stemmen patronen** in het bovenste veld **/\*** in.
1. Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.
1. Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.
1. Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**. 
1. Stel de optie **URL herschrijven** in op **Uitgeschakeld**.
1. Stel de optie **Caching** in op **Uitgeschakeld**.

Voer de volgende stappen uit om een cachingregel in te stellen in de Azure Front Door Service.

1. Voeg een cachingregel toe.
1. Voer in het veld **Naam** de tekst **statics** in.
1. Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.
1. Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.
1. Voer onder **Af te stemmen patronen** in het bovenste veld **/\_msdyn365/\_scnr/\*** in.
1. Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.
1. Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.
1. Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**.
1. Stel de optie **URL herschrijven** in op **Uitgeschakeld**.
1. Stel de optie **Caching** in op **Uitgeschakeld**.
1. Selecteer in het veld **Cachegedrag queryreeks** de optie **Elke unieke URL in cache plaatsen**.
1. Selecteer de optie **Ingeschakeld** in de veldgroep **Dynamische compressie**.

In de volgende afbeelding ziet u het dialoogvenster **Een regel toevoegen** in de Azure Front Door Service.

![Het dialoogvenster Regel toevoegen](./media/CDN_CachingRule.png)

Nadat deze eerste configuratie is geïmplementeerd, moet u uw aangepaste domein toevoegen aan de configuratie voor de Azure Front Door Service. Als u het aangepaste domein wilt toevoegen (bijvoorbeeld `www.fabrikam.com`), moet u een canonieke naam (CNAME) voor het domein configureren.

In de volgende afbeelding ziet u het dialoogvenster **CNAME-configuratie** in de Azure Front Door Service.

![Dialoogvenster CNAME-configuratie](./media/CNAME_Configuration.png)

> [!NOTE]
> Als het domein dat u gaat gebruiken al actief en live is, neemt u contact op met de ondersteuning om dit domein als test in te schakelen met de Azure Front Door Service.

U kunt de Azure Front Door Service gebruiken om het certificaat te beheren of u kunt uw eigen certificaat voor het aangepaste domein gebruiken.

In de volgende afbeelding ziet u het dialoogvenster **Aangepast domein HTTPS** in de Azure Front Door Service.

![Dialoogvenster Aangepast domein HTTPS](./media/Custom_Domain_HTTPS.png)

Uw CDN is nu correct geconfigureerd voor gebruik met uw Commerce-site.

## <a name="additional-resources"></a>Aanvullende resources

[Online winkeloverzicht](online-store-overview.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een nieuwe e-commerce-site implementeren](deploy-ecommerce-site.md)

[Een online-site koppelen aan een kanaal](associate-site-online-store.md)

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

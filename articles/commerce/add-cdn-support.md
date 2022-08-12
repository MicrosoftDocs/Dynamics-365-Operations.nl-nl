---
title: Ondersteuning voor een CDN (netwerk voor contentlevering) toevoegen
description: In dit artikel wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2177eeb6497269d580d2baea87ebb4fcd395223b
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069663"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Ondersteuning voor een CDN (netwerk voor contentlevering) toevoegen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een CDN (Content Delivery Network) toevoegt aan uw Microsoft Dynamics 365 Commerce-omgeving.

Wanneer u een e-commerce-omgeving instelt in Dynamics 365 Commerce, kunt u deze configureren om met uw CDN-service te werken. 

Het aangepaste domein kan tijdens het inrichtingsproces voor uw e-commerce-omgeving worden ingeschakeld. U kunt ook een serviceaanvraag gebruiken om deze in te stellen nadat het inrichtingsproces is voltooid. Het inrichtingsproces voor de e-commerce-omgeving genereert een hostnaam die aan de omgeving wordt gekoppeld. Deze hostnaam heeft de volgende indeling, waarbij \<*e-commerce-tenant-name*\> de naam van uw omgeving is:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

De hostnaam of het eindpunt dat tijdens het inrichtingsproces wordt gegenereerd, ondersteunt alleen een Secure Sockets Layer-certificaat (SSL) voor \*.commerce.dynamics.com. SSL wordt niet ondersteund voor aangepaste domeinen. Daarom moet u SSL beëindigen voor aangepaste domeinen in uw CDN en verkeer doorsturen van de CDN naar de hostnaam of het eindpunt dat door Commerce wordt gegenereerd. 

Bovendien worden de *statische* onderdelen (Javascript- of \[CSS\]-bestanden (Cascading Style Sheets)) van Commerce verzonden vanaf het eindpunt dat door Commerce wordt gegenereerd (\*.commerce.dynamics.com). De statische onderdelen kunnen alleen in de cache worden geplaatst, als de hostnaam of het eindpunt dat door Commerce gegenereerd wordt, achter het CDN wordt geplaatst.

## <a name="set-up-ssl"></a>SSL instellen

Nadat u uw Commerce-omgeving hebt ingericht met het aangepaste domein dat is opgegeven of nadat u het aangepaste domein voor uw omgeving hebt opgegeven met behulp van een serviceaanvraag, moet u de DNS-wijzigingen samen met het onboardingteam voor Commerce plannen.

Zoals eerder is vermeld, ondersteunt de gegenereerde hostnaam of het eindpunt alleen een SSL-certificaat voor \*.commerce.dynamics.com. SSL wordt niet ondersteund voor aangepaste domeinen.

## <a name="cdn-services"></a>CDN-services

Een CDN-service kan met een Commerce-omgeving worden gebruikt. Hieronder vindt u twee voorbeelden:

- **Microsoft Azure Front Door Service**: de Azure CDN-oplossing. Meer informatie over de Azure Front Door Service vindt u in [Documentatie bij Azure Front Door Service](/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator**: zie voor meer informatie [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN-instellingen

Het CDN-installatieproces bestaat uit de volgende algemene stappen:

1. Een front-endhost toevoegen.
1. Een back-endgroep configureren.
1. Stel regels voor doorsturen in.

### <a name="add-a-front-end-host"></a>Een front-endhost toevoegen

U kunt elke CDN-service gebruiken, maar voor het voorbeeld in dit artikel wordt de Azure Front Door Service gebruikt. 

Voor informatie over het instellen van de Azure Front Door Service raadpleegt u [Beknopte gids voor Front Door Service voor een algemene webtoepassing met hoge beschikbaarheid](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Een back-endpool configureren in Azure Front Door Service

Volg deze stappen om een back-endpool te configureren in Azure Front Door Service.

1. Voeg **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** toe aan een back-endgroep als een aangepaste host met een koptekst voor de back-endhost die hetzelfde is als **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.
1. Laat de standaardwaarden staan onder **Taakverdeling**.
1. Schakel statuscontroles voor de back-endgroep uit.

In de volgende afbeelding ziet u het dialoogvenster **Een back-end toevoegen** in de Azure Front Door Service met de naam van de back-endhost ingevuld.

![Het dialoogvenster Een backend-groep toevoegen.](./media/CDN_BackendPool.png)

In de volgende afbeelding ziet u het dialoogvenster **Een back-endgroep toevoegen** in de Azure Front Door Service met de standaardwaarden voor taakverdeling.

![Dialoogvenster Een back-endgroep toevoegen (vervolg).](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Zorg ervoor dat u **Statusprobes** uitschakelt bij het instellen van uw eigen Azure Front Door Service voor Commerce.


### <a name="set-up-rules-in-azure-front-door-service"></a>Regels in de Azure Front Door Service instellen

Voer de volgende stappen uit om een regel voor doorsturen in te stellen in de Azure Front Door Service.

1. Voeg een regel voor doorsturen toe.
1. Voer in het veld **Naam** de tekst **standaard** in.
1. Selecteer **HTTP en HTTPS** in het veld **Geaccepteerd protocol**.
1. Voer in het veld **Frontend hosts** **dynamics-ecom-tenant-name.azurefd.net** in.
1. Voer onder **Af te stemmen patronen** in het bovenste veld **/\*** in.
1. Stel onder **Routedetails** de optie **Routetype** in op **Doorsturen**.
1. Selecteer in het veld **Back-endgroep** de optie **ecom-backend**.
1. Selecteer in de veldgroep **Protocol voor doorsturen** de optie **Afstemmen op aanvraag**. 
1. Stel de optie **URL herschrijven** in op **Uitgeschakeld**.
1. Stel de optie **Caching** in op **Uitgeschakeld**.


> [!WARNING]
> Als het domein dat u gaat gebruiken al actief en live is, maakt u een ondersteuningsticket vanuit de tegel **Ondersteuning** in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) om hulp te krijgen bij uw volgende stappen. Zie [Ondersteuning krijgen voor apps voor financiën en bedrijfsactiviteiten of Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) voor meer informatie.

Als uw domein nieuw is en geen reeds bestaand live domein is, kunt u uw aangepaste domein toevoegen aan de configuratie voor de Azure Front Door Service. Hierdoor wordt webverkeer via het Azure Front Door-exemplaar naar uw site geleid. Als u het aangepaste domein wilt toevoegen (bijvoorbeeld `www.fabrikam.com`), moet u een canonieke naam (CNAME) voor het domein configureren.

In de volgende afbeelding ziet u het dialoogvenster **CNAME-configuratie** in de Azure Front Door Service.

![Dialoogvenster CNAME-configuratie.](./media/CNAME_Configuration.png)

U kunt de Azure Front Door Service gebruiken om het certificaat te beheren of u kunt uw eigen certificaat voor het aangepaste domein gebruiken.

In de volgende afbeelding ziet u het dialoogvenster **Aangepast domein HTTPS** in de Azure Front Door Service.

![Dialoogvenster Aangepast domein HTTPS.](./media/Custom_Domain_HTTPS.png)

Zie voor gedetailleerde instructies voor het toevoegen van een aangepast domein aan uw Azure Front Door [Een aangepast domein toevoegen aan uw Front Door](/azure/frontdoor/front-door-custom-domain).

Uw CDN is nu correct geconfigureerd voor gebruik met uw Commerce-site.

## <a name="additional-resources"></a>Aanvullende bronnen

[Implementatieopties voor netwerk voor contentlevering](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

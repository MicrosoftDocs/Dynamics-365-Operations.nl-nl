---
title: Domeinen in Dynamics 365 Commerce
description: In dit artikel wordt beschreven hoe domeinen worden verwerkt in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f1a2de7984aad7d291b8a4dc68f5690d57ebe6cc
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750675"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domeinen in Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe domeinen worden verwerkt in Microsoft Dynamics 365 Commerce.

Domeinen zijn webadressen die worden gebruikt om te navigeren naar Dynamics 365 Commerce-sites in een webbrowser. U beheert het beheer van uw domein met een gekozen DNS-provider (Domain Name Server). In Dynamics 365 Commerce Site Builder wordt naar domeinen verwezen om te coördineren hoe een site wordt geopend wanneer deze wordt gepubliceerd. In dit artikel wordt beschreven hoe domeinen worden verwerkt en gebruikt in de levenscyclus van de ontwikkeling en lancering van de Commerce-site.

> [!NOTE]
> Vanaf 6 mei 2022 worden alle omgevingen gemaakt in Dynamics 365 Commerce ingericht met het domein `.dynamics365commerce.ms`, dat het eerdere patroon vervangt van `.commerce.dynamics.com` vervangt. Bestaande omgevingen ingericht met het domein `.commerce.dynamics.com` blijven werken.

## <a name="provisioning-and-supported-host-names"></a>Inrichten en ondersteunde hostnamen

Wanneer u een e-commerce-omgeving inricht in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), wordt het vak **Ondersteunde hostnamen** in het inrichtingsscherm voor e-Commerce gebruikt om domeinen in te voeren die aan de geïmplementeerde Commerce-omgeving worden gekoppeld. Deze domeinen zijn de voor klanten zichtbare DNS-namen (Domain Name Server) waar e-Commerce-websites worden gehost. Als u tijdens deze fase een domein invoert, wordt er niet begonnen met het omleiden van verkeer voor het domein naar Dynamics 365 Commerce. Verkeer voor een domein wordt alleen naar het Commerce-eindpunt gerouteerd wanneer de DNS CNAME-record wordt bijgewerkt om het Commerce-eindpunt te gebruiken met het domein.

> [!NOTE]
> U kunt meerdere domeinen invoeren in het vak **Ondersteunde hostnamen** door deze met puntkomma's van elkaar te scheiden.

De volgende afbeelding toont het inrichtingsscherm voor e-Commerce van LCS met het vak **Ondersteunde hostnamen** gemarkeerd. 

![Inrichtingsscherm voor e-Commerce van LCS met het vak **Ondersteunde hostnamen** gemarkeerd.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

U kunt een serviceverzoek maken om extra domeinen aan een omgeving toe te voegen als het inrichten al heeft plaatsgevonden. Als u een serviceaanvraag wilt maken in LCS, gaat u in uw omgeving naar **Ondersteuning \> Ondersteuningsproblemen** en selecteert u **Een incident indienen**.

## <a name="commerce-generated-urls"></a>Door Commerce gegenereerde URL's

Bij het inrichten van een Dynamics 365 Commerce e-Commerce-omgeving genereert Commerce een URL die het werkadres van de omgeving is. Naar deze URL wordt verwezen in de koppeling naar de e-Commerce-site die wordt weergegeven in LCS nadat de omgeving is ingericht. Een door Commerce gegenereerde URL heeft de indeling `https://<e-commerce tenant name>.dynamics365commerce.ms`, waarbij de tenantnaam van e-Commerce de naam is die is ingevoerd in LCS voor de Commerce-omgeving.

U kunt ook hostnamen van productiesites in een sandbox-omgeving gebruiken. Deze optie is ideaal wanneer u een site van een sandbox-omgeving naar productie wilt kopiëren.

## <a name="site-setup"></a>Instellingen voor site

Nadat uw e-Commerce-omgeving is ingericht, moet u de site instellen in Commerce Site Builder om uw site te koppelen aan de werkende URL.

Wanneer u voor het eerst een site instelt in Site Builder, wordt het dialoogvenster **Uw site instellen** weergegeven.

In de volgende afbeelding wordt het dialoogvenster **Uw site instellen weergegeven** voor een site met de naam 'default' wanneer u de site voor het eerst opent in Site Builder.

![Het dialoogvenster **Uw site instellen**.](./media/Domains_SetupyoursiteScreen.png)

In het vak **Een domein selecteren** kunt u een van de ondersteunde hostnamen voor uw site koppelen in LCS aan uw site koppelen in Site Builder.

U kunt het vak **Pad** leeg laten of u kunt een extra padreeks toevoegen die wordt weergegeven in uw werkende URL. Als u het vak **Pad** leeg laat, wordt de door Commerce gegenereerde basis-URL gekoppeld aan de site die wordt ingesteld in Site Builder. Paden moeten uniek zijn voor elk paar van site en domein. Binnen de geselecteerde site en het geselecteerde domein kan slechts één site in de omgeving het lege pad gebruiken of aan een unieke padreeks worden gekoppeld. Elke tekenreeks die tijdens het instellen van de site aan het veld **Pad** wordt toegevoegd, wordt een subpad van de door Commerce gegenereerde basis-URL die wordt gebruikt om toegang te krijgen tot de site in een webbrowser.

> [!NOTE]
> Het pad wordt ook wel het **afstemmingspad** genoemd wanneer een kanaal wordt toegevoegd in de configuratiesectie **Site-instellingen \> Kanalen** van Site Builder.

Als u bijvoorbeeld in Site Builder een site met de naam fabrikam in een e-Commerce-tenant met de naam xyz hebt en als u de site instelt met een leeg pad, kunt u de gepubliceerde site-inhoud in een webbrowser openen door rechtstreeks naar de door Commerce gegenereerde basis-URL te gaan:

`https://xyz.dynamics365commerce.ms`

Als u tijdens de installatie van dezelfde site een pad naar fabrikam hebt toegevoegd, kunt u de gepubliceerde site-inhoud ook in een webbrowser openen met behulp van de volgende URL:

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>Pagina's en URL's

Nadat de site is ingesteld met een pad, worden alle URL's die zijn gekoppeld aan pagina's in Site Builder samengesteld op de werkende URL (de door Commerce gegenereerde URL of de door Commerce gegenereerde URL plus het pad) voor de site. Wanneer u een nieuwe URL maakt in Site Builder (**URL's /> +Nieuw**) door een pagina te selecteren in de lijst in het dialoogvenster **Nieuwe URL** en het URL-pad voor die pagina te typen, wordt die URL aan de geselecteerde pagina gekoppeld. De waarde van het URL-pad wordt vervolgens toegevoegd aan de werkende URL van de site om toegang te krijgen tot de pagina en wordt aangeduid als `./<URL path>` in de URL-lijst van de pagina **URL's** in Site Builder.

In de volgende afbeelding ziet u het dialoogvenster **Nieuwe URL** in Site Builder met een voorbeeld van een URL-pad. 

![Het dialoogvenster **Nieuwe URL** in Site Builder.](./media/Domains_PageSetup2a.png)

In de volgende afbeelding ziet u de pagina **URL's** in Site Builder met een voorbeeld van een URL in de lijst.

![De optie Gebruikersstroom uitvoeren in de beleidsstroom.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domeinen in Site Builder

De ondersteunde waarden voor hostnamen zijn beschikbaar om te worden gekoppeld als een domein bij het instellen van een site. Wanneer u een ondersteunde hostnaamwaarde als domein selecteert, ziet u dat in Site Builder naar het gekozen domein wordt verwezen. Dit domein is alleen een verwijzing in de Commerce-omgeving. Live verkeer voor dat domein wordt nog niet doorgestuurd naar Dynamics 365 Commerce.

Wanneer u met sites werkt in Site Builder en u twee locaties met twee verschillende domeinen hebt ingesteld, kunt u het kenmerk **?domain=** toevoegen aan uw werkende URL om toegang te krijgen tot de gepubliceerde site-inhoud in een browser.

Stel dat de omgeving xyz is ingericht en er twee sites zijn gemaakt en gekoppeld in Site Builder: een met het domein `www.fabrikam.com` en de andere met het domein `www.constoso.com`. Elke site is ingesteld met een leeg pad. Deze twee sites kunnen dan als volgt worden geopend in een webbrowser met behulp van het kenmerk **?domain=**
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

Wanneer geen domeinquerytekenreeks is opgegeven in een omgeving met meerdere domeinen, gebruikt Commerce het eerste domein dat u hebt opgegeven. Als het pad fabrikam bijvoorbeeld als eerste is opgegeven tijdens het instellen van de site, kan `https://xyz.dynamics365commerce.ms` worden gebruikt om toegang te krijgen tot de gepubliceerde site-inhoudssite voor `www.fabrikam.com`.

U kunt ook aangepaste domeinen toevoegen. Selecteer om dit te doen op de pagina Commerce-beheer van uw omgeving voor het project onder de subkop **e-Commerce** de optie **+ Aangepast domein toevoegen**. De schuifregelaar toont de bestaande aangepaste domeinen en biedt de optie om een nieuw aangepast domein toe te voegen.

## <a name="update-which-commerce-scale-unit-is-used"></a>Bijwerken welke Commerce Scale Unit wordt gebruikt

De CSU (Commerce Scale Unit) die door Commerce wordt gebruikt, wordt meestal geselecteerd wanneer een omgeving voor het eerst wordt gemaakt. Met Commerce kunt u wijzigen welk CSU-exemplaar in uw omgeving wordt gebruikt, zodat u uw architectuur beter kunt onderhouden via de selfservicefunctionaliteit en minder vaak contact hoeft op te nemen met de ondersteuning. Als u het CSU-exemplaar wilt bijwerken, gaat u naar de pagina Commerce-beheer van uw omgeving voor het project en selecteert u **Scale Unit bijwerken**. Gebruik de schuifregelaar **Nieuwe Commerce Scale Unit** om een nieuw CSU-exemplaar te selecteren in de lijst met CSU's die beschikbaar zijn voor uw omgeving.

## <a name="traffic-forwarding-in-production"></a>Verkeer doorsturen in productie

U kunt meerdere domeinen simuleren met behulp van parameters voor domeinquerytekenreeksen op het eindpunt commerce.dynamics.com zelf. Wanneer u live moet gaan in productie, moet u het verkeer voor uw aangepaste domein echter doorsturen naar het eindpunt `<e-commerce tenant name>.dynamics365commerce.ms`.

Het eindpunt `<e-commerce tenant name>.dynamics365commerce.ms` ondersteunt geen aangepaste SSL's (Secure Sockets Layers), dus u moet aangepaste domeinen instellen met behulp van een Front Door Service of een CDN (Content Delivery Network). 

Als u aangepaste domeinen wilt instellen met een Front Door Service of CDN, hebt u twee mogelijkheden:

- Stel een Front Door Service, zoals Azure Front Door, in voor het verwerken van front-end verkeer en om verbinding te maken met uw Commerce-omgeving. Hiermee beschikt u over meer controle over domein- en certificaatbeheer en een meer gedetailleerd beveiligingsbeleid.

- Gebruik het door Commerce geleverde exemplaar van Azure Front Door. Dit vereist coördinatie met het Dynamics 365 Commerce-team voor domeinverificatie en het verkrijgen van SSL-certificaten voor uw productiedomein.

> [!NOTE]
> Als u een externe CDN- of front door-service gebruikt, moet u ervoor zorgen dat de aanvraag wordt aangeboden op het Commerce-platform met de door Commerce opgegeven hostnaam, maar met de XFH-header (X-Forwarded-Host) \<custom-domain\>. Als het Commerce-eindpunt bijvoorbeeld `xyz.dynamics365commerce.ms` is en het aangepaste domein is `www.fabrikam.com`, moet de hostheader van de forwarded request `xyz.dynamics365commerce.ms` zijn en moet de XFH-koptekst `www.fabrikam.com`.

Zie [Ondersteuning voor een CDN (netwerk voor contentlevering) toevoegen](add-cdn-support.md) voor informatie over het rechtstreeks instellen van een CDN-service.

Als u het door Commerce geleverde Azure Front Door-exemplaar wilt gebruiken, moet u een serviceaanvraag voor assistentie voor CDN-installatie van het Commerce-team voor onboarding maken. 

- U moet de naam van uw bedrijf, het productiedomein, de omgevings-id en de naam van de e-Commerce-tenant voor productie opgeven. 
- U moet bevestigen of deze serviceaanvraag voor een bestaand domein (wordt gebruikt voor een actieve site) of een nieuw domein is. 
- Voor een nieuw domein kunt u de domeinverificatie en het SSL-certificaat in één stap ontvangen. 
- Voor een domein van een bestaande website moet een proces van meerdere stappen worden uitgevoerd om de domeinverificatie en het SSL-certificaat in te stellen. Voor dit proces geldt een SLA van 7 werkdagen voor een domein om live te gaan, omdat hierin meerdere opeenvolgende stappen zijn opgenomen.

Als u een serviceaanvraag wilt maken in LCS, gaat u in uw omgeving naar **Ondersteuning \> Ondersteuningsproblemen** en selecteert u **Een incident indienen**.

> [!NOTE]
> Aangepaste domeinen met SSL worden alleen ondersteund in productieomgevingen. Gebruik voor niet-productieomgevingen, zoals sandbox- en UAT-omgevingen, de door Commerce gegenereerde URL om toegang te krijgen tot gepubliceerde inhoud in een webbrowser.

## <a name="ssl-certificate-process"></a>SSL-certificaatproces

Wanneer een serviceaanvraag wordt ingediend, coördineert het Commerce-team de volgende stappen met u.

Voor nieuwe domeinen:
- Het Commerce-team stelt het Azure Front Door-exemplaar (door Commerce gehost) in.
- Het Commerce-team levert vervolgens de CNAME-record om naar uw aangepaste domein te verwijzen.
- Nadat de CNAME-record is bijgewerkt, kan het door Commerce gehoste Azure Front Door-exemplaar het eigendom van het domein verifiëren en het SSL-certificaat verkrijgen.

Voor bestaande/actieve domeinen:
- Het Commerce-team geeft u de opdracht om een CNAME-record `afdverify.<custom-domain>` toe te voegen om aan uw domein-DNS-provider te leveren.
- Vervolgens voegt het Commerce-team het domein toe aan het Azure Front Door-exemplaar en biedt dit team aanvullende DNS-TXT-records die aan de DNS voor het domein moeten worden toegevoegd.
- Nadat de TXT-records zijn voltooid, voltooit het Commerce-team de Azure Front Door-updates voor het domein waarin het SSL-certificaat wordt ingesteld.

## <a name="apex-domains"></a>Apex-domeinen

Het door Commerce geleverde Azure Front Door-exemplaar ondersteunt geen Apex-domeinen (hoofddomeinen die geen subdomeinen bevatten). Apex-domeinen vereisen dat een IP-adres wordt omgezet en het Azure Front Door-exemplaar alleen met virtuele eindpunten bestaat. Als u een Apex-domein wilt gebruiken, hebt u de volgende mogelijkheden:

- **Optie 1** - gebruik uw DNS-provider om het apex-domein om te leiden naar een www-domein. fabrikam.com leidt bijvoorbeeld om naar `www.fabrikam.com` waarbij `www.fabrikam.com` de CNAME-record is die verwijst naar het Commerce gehoste Azure Front Door-exemplaar.

- **Optie 2** : Als uw DNS-provider ALIAS-records ondersteunt, kunt u het apex-domein laten verwijzen naar het Azure Front Door-eindpunt. Dit zorgt ervoor dat de IP-wijziging door het eindpunt wordt weergegeven. U moet het Azure Front Door-exemplaar zelf hosten.
  
- **Optie 3** : als uw DNS-provider ALIAS-records niet ondersteunt, moet u uw DNS-provider wijzigen in Azure DNS en zowel Azure DNS als het Azure Front Door-exemplaar zelf hosten.

> [!NOTE]
> Als u Azure Front Door gebruikt, moet u ook een Azure DNS instellen in hetzelfde abonnement. Het apex-domein dat op Azure DNS wordt gehost, kan naar uw Azure Front Door verwijzen als een aliasrecord. Dit is de enige tijdelijke oplossing, aangezien apex-domeinen altijd naar een IP-adres moeten verwijzen.
  
Als u vragen hebt over Apex-domeinen, kunt u contact opnemen met [Microsoft Support](https://support.microsoft.com/).

  ## <a name="additional-resources"></a>Aanvullende bronnen

  [Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

  [Een online winkelafzetkanaal instellen](./channel-setup-online.md)

  [Een e-commerce-site maken](create-ecommerce-site.md)

  [Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

  [robots.txt-bestanden beheren](manage-robots-txt-files.md)

  [URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

  [Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)

  [Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

  [Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-B2C-tenants.md)

  [Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

  [Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

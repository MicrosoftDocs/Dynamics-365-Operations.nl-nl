---
title: Conformiteit van cookie
description: In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.
author: BrianShook
ms.date: 03/10/2022
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
ms.openlocfilehash: 2efb866d513ba90630b0397c1ca144c92d40719c
ms.sourcegitcommit: 4645278a4b4a38dcb18fdfb49ce2e276eabb59de
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/11/2022
ms.locfileid: "8403142"
---
# <a name="cookie-compliance"></a>Conformiteit van cookie

[!include [banner](includes/banner.md)]

In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.

Privacy is een belangrijke factor wanneer trackingtechnologieën worden gebruikt die invloed hebben op e-Commerce-klanten. Vanwege normen voor privacycompliance, zoals de AVG (Algemene Verordening Gegevensbescherming) in de EU (Europese Unie), moeten elektronische privacyrichtlijnen worden overwogen voor elke site die nu actief is. Omdat veel e-Commerce-sites standaard wereldwijd toegankelijk zijn, is het belangrijk dat u de compliancenormen voor uw e-Commerce-site controleert.

Bezoek het [Microsoft Vertrouwenscentrum](https://www.microsoft.com/trust-center) voor meer informatie over de basisbeginselen die Microsoft gebruikt voor cookiecompliance. Op die site vindt u ook meer informatie over de compliancegebieden en privacy.

In de volgende tabel wordt de huidige verwijzingslijst van cookies weergegeven die door Dynamics 365 Commerce-sites zijn geplaatst.

| Cookienaam                               | Gebruik                                                        | Levensduur |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Cookies                             | Microsoft Azure Active Directory (Azure AD)-verificatiecookies opslaan voor eenmalige aanmelding (SSO). Hiermee wordt gecodeerde informatie over gebruikers opgeslagen (naam, achternaam, e-mail). | Sessie |
| \_msdyn365___cart_                           | Winkelwagen-id wordt gebruikt om lijst met producten op te halen die aan het winkelwagenexemplaar zijn toegevoegd. | Sessie |
| \_msdyn365___checkout_cart_                           | Winkelwagen-id voor kassa wordt gebruikt om lijst met producten op te halen die aan het winkelwagenexemplaar voor kassa zijn toegevoegd. | Sessie |
| \_msdyn365___ucc_                            | Toestemming bijhouden voor cookienaleving.                          | 1 jaar |
| ai_session                                  | Detecteert in hoeveel sessies met gebruikersactiviteit bepaalde pagina's en functies van de app zijn opgenomen. | 30 minuten |
| ai_user                                     | Detecteert hoeveel mensen de app en de bijbehorende functies hebben gebruikt. Gebruikers worden geteld met behulp van anonieme id's. | 1 jaar |
| b2cru                                       | De omleidings-URL wordt dynamisch opgeslagen.                              | Sessie |
| JSESSIONID                                  | Wordt gebruikt door betalingsconnector Adyen om gebruikerssessie op te slaan.       | Sessie |
| OpenIdConnect.nonce.&#42;                       | Authenticatie                                               | 11 minuten |
| x-ms-cpim-cache:.&#42;                          | Wordt gebruikt voor het onderhouden van de aanvraagstatus.                      | Sessie |
| x-ms-cpim-csrf                              | CRSF-token (aanvraagvervalsing op meerdere sites) wordt gebruikt voor de CRSF-beveiliging.     | Sessie |
| x-ms-cpim-dc                                | Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren. | Sessie |
| x-ms-cpim-rc.&#42;                              | Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren. | Sessie |
| x-ms-cpim-slice                             | Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren. | Sessie |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Wordt gebruikt voor het onderhouden van de SSO-sessie.                        | Sessie |
| x-ms-cpim-trans                             | Wordt gebruikt voor het traceren van transacties (het aantal geopende tabbladen dat wordt geverifieerd tegen een Business-to-consumer-site (B2C)), inclusief de huidige transactie. | Sessie |
| \_msdyn365___muid_                            | Wordt gebruikt als experimenteren is geactiveerd voor de omgeving. Wordt gebruikt als gebruikers-id voor experimenteerdoeleinden. | 1 jaar |
| \_msdyn365___exp_                             | Wordt gebruikt als experimenteren is geactiveerd voor de omgeving. Wordt gebruikt voor het meten van de prestaties voor de taakverdeling.         | 1 uur |
| d365mkt                                       | Wordt gebruikt als detectie op basis van locaties om het IP-adres van een gebruiker voor winkellocatie-suggesties bij te houden is ingeschakeld in Commerce Site Builder bij **Site-instellingen \> Algemeen \> Detectie van winkels op basis van de locatie inschakelen**.      | 1 uur |
| \_msdyn365___tuid_                           | Wordt alleen gebruikt als experimenten voor een omgeving zijn geactiveerd; er wordt een GUID gegenereerd die als een gebruikers-id moet fungeren. De waarde wordt gewijzigd als de aanmeldingsstatus van een gebruiker verandert.      | 1 jaar |
| \_msdyn365___aud_0                          | Hiermee worden segmentwaarden opgeslagen die worden gebruikt voor geolocaties en deze worden alleen gebruikt als geolocaties zijn geconfigureerd voor een pagina die of fragment dat is aangevraagd door een sitegebruiker. Het koekje wordt alleen geplaatst wanneer de segmentwaarden afkomstig zijn van een externe segmentatieprovider.      | 7 dagen |
| \_msdyn365___aud_1                           | Hiermee worden segmentwaarden opgeslagen die worden gebruikt voor geolocaties en deze worden alleen gebruikt als geolocaties zijn geconfigureerd voor een pagina die of fragment dat is aangevraagd door een sitegebruiker. Het koekje wordt alleen geplaatst wanneer de segmentwaarden afkomstig zijn van een externe segmentatieprovider.      | 7 dagen |
| \_msdyn365___aud_2                           | Hiermee worden segmentwaarden opgeslagen die worden gebruikt voor geolocaties en deze worden alleen gebruikt als geolocaties zijn geconfigureerd voor een pagina die of fragment dat is aangevraagd door een sitegebruiker. Het koekje wordt alleen geplaatst wanneer de segmentwaarden afkomstig zijn van een externe segmentatieprovider.      | 7 dagen |
| d365gi                                       | In deze cookie worden gegevens over de geografische locatie opgeslagen wanneer er een Geolocation-service van een derde partij wordt gebruikt.      | 1 dag |

Als een sitegebruiker een koppeling voor social media op een site selecteert, worden de cookies in de volgende tabel ook in de browser bijgehouden.


| Domein                      | Cookie               | Beschrijving                                                  | Bron                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Id-synchronisatie van LinkedIn-advertenties                                      | LinkedIn-feed en Insight-label                                |
| .linkedin.com               | li_sugr                  | Browser-id                                           | LinkedIn Insight Tag als IP-adres niet in een opgegeven land/regio is |
| .linkedin.com               | BizographicsOptOut       | Bepaalt de afmeldstatus voor tracering van derden.              | Besturingselementen voor LinkedIn-gast en pagina's voor afmelden bedrijfstak           |
| .linkedin.com               | \_guid                    | Browser-id voor Google Ads.                            | LinkedIn-feed                                                |
| .linkedin.com               | li_oatml                 | Indirecte lid-id voor conversietracering, retargeting en analyses. | LinkedIn Ads en Insight-labels                                |
| Verschillende first-party domeinen | li_fat_id                | Indirecte lid-id voor conversietracering, retargeting en analyses. | LinkedIn Ads en Insight-labels                                |
| .adsymptotic.com            | U                        | Browser-id                                           | LinkedIn Insight Tag als IP-adres niet in een opgegeven land/regio is |
| .linkedin.com                | bcookie                  | Cookie browser-id                                            | Aanvragen voor LinkedIn                                         |
| .linkedin.com                | bscookie                 | Veilige browsercookie                                        | Aanvragen voor LinkedIn                                         |
| .linkedin.com               | lang                     | Hiermee stelt u standaard landinstelling en taal in.                                 | Aanvragen voor LinkedIn                                         |
| .linkedin.com                | lidc                     | Gebruikt voor routering.                                             | Aanvragen voor LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Cookie voor Adobe Audience Manager                                                     | Instellen voor synchronisatie van id                                              |
| .linkedin.com               | \_ga                      | Google Analytics-cookie                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analytics-cookie                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analytics-cookie                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Cookie bevat de gebruikers-id van de momenteel aangemelde gebruiker.  |   Facebook                                                           |
| .facebook.com               | datr                     | Gebruikt om de webbrowser aan te geven die wordt gebruikt om verbinding te maken met Facebook, onafhankelijk van de aangemelde gebruiker. | Facebook                                                             |
| .facebook.com               | wd                       | Slaat de dimensies van het browservenster op en wordt gebruikt door Facebook om de weergave van de pagina te optimaliseren. | Facebook                                                             |
| .facebook.com               | xs                       | Een nummer met twee cijfers dat het sessienummer aangeeft. Het tweede deel van de waarde is een sessiegeheim. |  Facebook                                                            |
| .facebook.com               | fr                       | Bevat een unieke browser en gebruikers-id, gebruikt voor doelgerichte reclame. |  Facebook                                                            |
| .facebook.com               | sb                       | Gebruikt om Facebook-suggesties voor vrienden te verbeteren.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Cookie bevat de gebruikers-id van de momenteel aangemelde gebruiker.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Cookie bevat de gebruikers-id van de momenteel aangemelde gebruiker.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Cookie bevat pagina's wanneer de gebruiker op de knop Pinterest klikt.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Cookie bevat pagina's wanneer de gebruiker op de knop Pinterest klikt.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Bevat een gebruikers-id en de tijdstempel op het moment dat de cookie werd gemaakt. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Cookie bevat pagina's wanneer de gebruiker op de knop Pinterest klikt.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Cookie bevat pagina's wanneer de gebruiker op de knop Pinterest klikt.      | Pinterest                                                             |
| .pinterest.com              | Lokale opslag            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Servicemedewerkers          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Cookietoestemming van sitegebruiker op een e-commerce-site 

Als een functie of module van een e-commerce-site een niet-essentiële cookie gebruikt, moet de toestemming van de sitegebruiker worden verkregen voordat de cookie wordt gevolgd. Als u wilt dat sitegebruikers cookietoestemming op de e-commerce-site, moet een auteur van een site een cookietoestemmingsmodule toevoegen en configureren in de koptekstmodule van de pagina om ervoor te zorgen dat de toestemming wordt gevraagd en ontvangen. Toestemming van de sitegebruiker moet worden verleend voordat een functie of module met een niet-essentiële cookie kan worden weergegeven op een sitepagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Toegankelijksfuncties en -voorzieningen](accessibility.md)

[Conformiteitsoverzicht](compliance-overview.md)

[Een pagina met het privacybeleid toevoegen](add-privacy-page.md)

[Gebruikers-id's vervangen die zijn gekoppeld aan wijzigingen in bijgehouden inhoud](replace-IDs-tracked-changes.md)

[Cookietoestemmingsmodule](cookie-consent-module.md) 
 
[Koptekstmodule](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

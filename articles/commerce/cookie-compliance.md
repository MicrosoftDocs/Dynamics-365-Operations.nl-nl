---
title: Conformiteit van cookie
description: In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.
author: BrianShook
ms.date: 05/21/2021
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
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088382"
---
# <a name="cookie-compliance"></a>Conformiteit van cookie

[!include [banner](includes/banner.md)]

In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.

Privacy is een belangrijke factor wanneer trackingtechnologieën worden gebruikt die invloed hebben op e-Commerce-klanten. Vanwege normen voor privacycompliance, zoals de AVG (Algemene Verordening Gegevensbescherming) in de EU (Europese Unie), moeten elektronische privacyrichtlijnen worden overwogen voor elke site die nu actief is. Omdat veel e-Commerce-sites standaard wereldwijd toegankelijk zijn, is het belangrijk dat u de compliancenormen voor uw e-Commerce-site controleert.

Bezoek het [Microsoft Vertrouwenscentrum](https://www.microsoft.com/trust-center) voor meer informatie over de basisbeginselen die Microsoft gebruikt voor cookiecompliance. Op die site vindt u ook meer informatie over de compliancegebieden en privacy.

In de volgende tabel wordt de huidige verwijzingslijst van cookies weergegeven die door Dynamics 365 Commerce-sites zijn geplaatst.

| Cookienaam                               | Gebruik                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Microsoft Azure Active Directory (Azure AD)-verificatiecookies opslaan voor eenmalige aanmelding (SSO). Hiermee wordt gecodeerde informatie over gebruikers opgeslagen (naam, achternaam, e-mail). |
| &#95;msdyn365___cart&#95;                           | Winkelwagen-id wordt gebruikt om lijst met producten op te halen die aan het winkelwagenexemplaar zijn toegevoegd. |
| &#95;msdyn365___ucc&#95;                            | Toestemming bijhouden voor cookienaleving.                          |
| ai_session                                  | Detecteert in hoeveel sessies met gebruikersactiviteit bepaalde pagina's en functies van de app zijn opgenomen. |
| ai_user                                     | Detecteert hoeveel mensen de app en de bijbehorende functies hebben gebruikt. Gebruikers worden geteld met behulp van anonieme id's. |
| b2cru                                       | De omleidings-URL wordt dynamisch opgeslagen.                              |
| JSESSIONID                                  | Wordt gebruikt door betalingsconnector Adyen om gebruikerssessie op te slaan.       |
| OpenIdConnect.nonce.&#42;                       | Authenticatie                                               |
| x-ms-cpim-cache:.&#42;                          | Wordt gebruikt voor het onderhouden van de aanvraagstatus.                      |
| x-ms-cpim-csrf                              | CRSF-token (aanvraagvervalsing op meerdere sites) wordt gebruikt voor de CRSF-beveiliging.     |
| x-ms-cpim-dc                                | Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren. |
| x-ms-cpim-rc.&#42;                              | Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren. |
| x-ms-cpim-slice                             | Wordt gebruikt om aanvragen naar het toepasselijke serverexemplaar voor productieverificatie te routeren. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Wordt gebruikt voor het onderhouden van de SSO-sessie.                        |
| x-ms-cpim-trans                             | Wordt gebruikt voor het traceren van transacties (het aantal geopende tabbladen dat wordt geverifieerd tegen een Business-to-consumer-site (B2C)), inclusief de huidige transactie. |
| \_msdyn365___muid_                            | Wordt gebruikt als Experimenten is geactiveerd voor de omgeving. wordt gebruikt als userId voor experimentdoeleinden. |
| \_msdyn365___exp_                             | Wordt gebruikt als Experimenten is geactiveerd voor de omgeving; wordt gebruikt voor het meten van de prestaties voor de taakverdeling.         |
| d365mkt                                       | Wordt gebruikt als detectie op basis van locaties om het IP-adres van een gebruiker voor winkellocatie-suggesties bij te houden is ingeschakeld in Commerce Site Builder bij **Site-instellingen > Algemeen > Detectie van winkels op basis van de locatie inschakelen**.      |

Als een sitegebruiker een koppeling voor social media op een site selecteert, worden de cookies in de volgende tabel ook in de browser bijgehouden.


| Domein                      | Cookie               | Beschrijving                                                  | Bron                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Id-synchronisatie van LinkedIn-advertenties                                      | LinkedIn-feed en Insight-label                                |
| .linkedin.com               | li_sugr                  | Browser-id                                           | LinkedIn Insight-label als IP-adres niet in een opgegeven land/regio is |
| .linkedin.com               | BizographicsOptOut       | Bepaalt de afmeldstatus voor tracering van derden.              | Besturingselementen voor LinkedIn-gast en pagina's voor afmelden bedrijfstak           |
| .linkedin.com               | \_guid                    | Browser-id voor Google Ads.                            | LinkedIn-feed                                                |
| .linkedin.com               | li_oatml                 | Indirecte lid-id voor conversietracering, retargeting en analyses. | LinkedIn Ads en Insight-labels                                |
| Verschillende first-party domeinen | li_fat_id                | Indirecte lid-id voor conversietracering, retargeting en analyses. | LinkedIn Ads en Insight-labels                                |
| .adsymptotic.com            | U                        | Browser-id                                           | LinkedIn Insight-label als IP-adres niet in een opgegeven land/regio is |
| .linkedin.com                | bcookie                  | Cookie browser-id                                            | Aanvragen voor LinkedIn                                         |
| .linkedin.com                | bscookie                 | Veilige browsercookie                                        | Aanvragen voor LinkedIn                                         |
| .linkedin.com               | lang                     | Hiermee stelt u standaard landinstelling en taal in.                                 | Aanvragen voor LinkedIn                                         |
| .linkedin.com                | lidc                     | Gebruikt voor routering.                                             | Aanvragen voor LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Adobe-cookie voor doelgroepbeheer                                                     | Instellen voor synchronisatie van id                                              |
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


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Cookietoestemming van sitegebruiker op een e-Commerce-site 

Als een functie of module van een e-Commerce-site een niet-essentiële cookie gebruikt, moet de toestemming van de sitegebruiker worden verkregen voordat de cookie wordt gevolgd. Als u wilt dat sitegebruikers cookietoestemming op de e-Commerce-site, moet een auteur van een site een cookietoestemmingsmodule toevoegen en configureren in de koptekstmodule van de pagina om ervoor te zorgen dat de toestemming wordt gevraagd en ontvangen. Toestemming van de sitegebruiker moet worden verleend voordat een functie of module met een niet-essentiële cookie kan worden weergegeven op een sitepagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Toegankelijksfuncties en -voorzieningen](accessibility.md)

[Conformiteitsoverzicht](compliance-overview.md)

[Een pagina met het privacybeleid toevoegen](add-privacy-page.md)

[Gebruikers-id's vervangen die zijn gekoppeld aan wijzigingen in bijgehouden inhoud](replace-IDs-tracked-changes.md)

[Cookietoestemmingsmodule](cookie-consent-module.md) 
 
[Koptekstmodule](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

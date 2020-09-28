---
title: Conformiteit van cookie
description: In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761316"
---
# <a name="cookie-compliance"></a>Conformiteit van cookie

[!include [banner](includes/banner.md)]

In dit onderwerp worden overwegingen voor compliance op het gebied van cookies en het standaardbeleid in Microsoft Dynamics 365 Commerce beschreven.

## <a name="overview"></a>Overzicht

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

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Cookietoestemming van sitegebruiker op een e-Commerce-site 

Als een functie of module van een e-Commerce-site een niet-essentiële cookie gebruikt, moet de toestemming van de sitegebruiker worden verkregen voordat de cookie wordt gevolgd. Als u wilt dat sitegebruikers cookietoestemming op de e-Commerce-site, moet een auteur van een site een cookietoestemmingsmodule toevoegen en configureren in de koptekstmodule van de pagina om ervoor te zorgen dat de toestemming wordt gevraagd en ontvangen. Toestemming van de sitegebruiker moet worden verleend voordat een functie of module met een niet-essentiële cookie kan worden weergegeven op een sitepagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Toegankelijksfuncties en -voorzieningen](accessibility.md)

[Conformiteitsoverzicht](compliance-overview.md)

[Een pagina met het privacybeleid toevoegen](add-privacy-page.md)

[Gebruikers-id's vervangen die zijn gekoppeld aan wijzigingen in bijgehouden inhoud](replace-IDs-tracked-changes.md)

[Cookietoestemmingsmodule](cookie-consent-module.md) 
 
[Koptekstmodule](author-header-module.md)

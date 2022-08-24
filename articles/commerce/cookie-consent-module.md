---
title: Module voor cookietoestemming
description: In dit artikel wordt beschreven wat cookietoestemmingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 8ca4cc1ffcf8229589591dce6e4666b78bba3890
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276261"
---
# <a name="cookie-consent-module"></a>Module voor cookietoestemming

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat cookietoestemmingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

In de cookietoestemmingsmodule wordt aan sitegebruikers gevraagd expliciet cookies toe te staan voor alle functies of modules die browsercookies bijhouden. De toestemming is vereist wanneer een sitegebruiker de site voor het eerst bezoekt in een nieuwe browsersessie. Wanneer toestemming wordt ontvangen, wordt deze getraceerd en wordt de sitegebruiker niet nogmaals om toestemming gevraagd. Zie [Conformiteit van cookie](cookie-compliance.md) voor meer informatie.

Als de cookietoestemming niet is ontvangen van de sitegebruiker, worden de functies of modules waarvoor cookietoestemming vereist is niet weergegeven op de pagina. Voor de kassamodule, de module voor sociaal delen en de functie voor de voorkeurswinkel is bijvoorbeeld cookietoestemming vereist en deze worden niet weergegeven als de gebruiker geen toestemming heeft gekregen. 

Een cookietoestemmingsmodule kan worden geconfigureerd in het koptekstfragment van een pagina, zodat deze kan worden afgedwongen wanneer de pagina wordt geladen. De cookietoestemmingsmodule moet een duidelijk bericht bevatten waarin de sitegebruiker wordt geïnformeerd over het gebruik van cookies op de site en een koppeling naar de privacypagina van de site moet bieden.

In de volgende afbeelding ziet u een voorbeeld van een cookietoestemmingsbericht met een koppeling naar de pagina met het privacybeleid van de site in de koptekst van een sitepagina.
![Voorbeeld van een cookietoestemmingsmodule.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Eigenschappen van cookietoestemmingsmodule

| Naam van eigenschap.             | Waarde                 | Beschrijving |
|---------------------------|-----------------------|-------------|
| RTF                  | RTF | Hiermee geeft u een RTF-bericht op voor sitegebruikers dat de site gebruikmaakt van browsercookies en dat gebruikers het gebruik van cookies moeten accepteren om toegang te krijgen tot een volledig functionele site. |
| Koppelingen | URL | U kunt een of meer koppelingen toevoegen aan de privacypagina van een site die de typen cookies beschrijft die op de site worden bijgehouden. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Een cookietoestemmingsmodule toevoegen aan sitepagina's

Als u een cookietoestemmingsmodule efficiënt wilt toevoegen aan meerdere sitepagina's, kan deze worden toegevoegd aan een koptekstfragment van een gedeelde pagina. Als het koptekstfragment aan alle sitepagina's is toegevoegd, wordt automatisch een cookietoestemmingsmelding weergegeven wanneer een sitegebruiker voor het eerst naar sitepagina gaat.

Zie [Koptekstmodule](author-header-module.md) voor meer informatie over koptekstfragmenten en modules.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Koptekstmodule](author-header-module.md) 

[Conformiteit van cookie](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

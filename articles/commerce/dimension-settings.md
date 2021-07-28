---
title: Weergave-instellingen voor productdimensies toepassen
description: In dit onderwerp worden de weergave-instellingen voor productdimensies besproken en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d6854c11822e07ff06426b7a35eac86cdc0e9b06
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356897"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Weergave-instellingen voor productdimensies toepassen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp worden de weergave-instellingen voor productdimensies besproken en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce ondersteunt het gebruik van grootte-, stijl- en kleurdimensies om productvarianten te onderscheiden. Dimensies worden meestal weergegeven als tekstwaarden, zoals 'Klein', 'Normaal' en 'Groot' voor grootte, en 'Zwart' en 'Bruin' voor kleuren. Als een product echter veel variaties ondersteunt, kan het moeilijk zijn om door productvarianten te bladeren omdat er meerdere selecties vereist zijn om de afbeelding voor elke variant weer te geven. Om het gemakkelijker te maken om door productvarianten te bladeren, kunnen in de versie 10.0.20 van Commerce afbeeldingen en hexadecimale (hex) codes worden gebruikt om dimensies weer te geven als stalen.

In Commerce Site Builder worden dimensie-instellingen gedefinieerd via **Site-instellingen \> Extensies \> Dimensie-instellingen**. In de volgende afbeelding ziet u een voorbeeld van dimensie-instellingen in Site Builder.

![Voorbeeld van site-instellingen in Commerce Site Builder.](./dev-itpro/media/swatch_site_settings.PNG)

Er zijn twee dimensie-instellingen beschikbaar:

- **Dimensies die als afbeelding moeten worden weergegeven**: opgeven welke dimensies als stalen moeten worden weergegeven op pagina's met e-commercesite's, zoals productdetailpagina's (PDP's) en lijstpagina's met zoekresultaten. Elke combinatie van kleur-, grootte- en stijldimensies kan als een staal worden weergegeven. Als een dimensie wordt geselecteerd voor weergave als een staal, wordt met de rendering van de Commerce-module gezocht naar een beschikbare configuratie van een hexcodestaal. Als er geen hexcode is geconfigureerd, wordt via de systeemlogica naar een configuratie van een staal op basis van een afbeeldings-URL gezocht. Als noch een hexcode noch een afbeeldings-URL is geconfigureerd, wordt tekst weergegeven.

    De onderstaande afbeelding toont een voorbeeld waarin een PDP op een e-commercesite kleur- en groottestalen bevat. In dit voorbeeld wordt een hexcode geconfigureerd voor de kleurdimensie. Daarom worden stalen als kleuren weergegeven. Voor de groottedimensie worden echter noch hexcodes noch afbeeldings-URL´s geconfigureerd. Daarom wordt tekst weergegeven.

    ![Voorbeeld van de kleurdimensie die als stalen op een pagina met productdetails voor e-commerce wordt weergegeven.](./dev-itpro/media/swatch_pdp.png)

- **Dimensies die op een productkaart moeten worden weergegeven** – opgeven welke dimensies moeten worden weergegeven op productkaarten die worden weergegeven in lijsten en op lijstpagina's. Voordat een dimensie op een productkaart kan worden weergegeven, moet deze instelling voor die dimensie zijn ingeschakeld. De instelling **Dimensies die als afbeelding moeten worden weergegeven** moet ook worden ingeschakeld. Het gedrag van staalselectie op productkaarten is geoptimaliseerd voor de kleurdimensie. Voor andere dimensies is mogelijk een weergave-extensie vereist voor het aanpassen van het gedrag van staalselectie.

    De onderstaande afbeelding toont een voorbeeld waarbij een lijstpagina op een e-commercesite productkaarten bevat die kleurstalen bevatten.

    ![Voorbeeld van de kleurdimensie die als stalen op een lijstpagina voor e-commerce wordt weergegeven.](./dev-itpro/media/swatch_searchresults.PNG)

Zie [Productdimensiewaarden configureren zodat deze als stalen worden weergegeven](./dev-itpro/dimensions-swatch.md) voor informatie over het configureren van productdimensies zodat deze worden weergegeven als stalen op sitepagina´s.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module voor zoekresultaten](search-result-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Productdimensiewaarden configureren die als stalen moeten worden weergegeven](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

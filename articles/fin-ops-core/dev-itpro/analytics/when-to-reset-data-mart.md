---
title: Veelgestelde vragen over opnieuw instellen van een datamart
description: Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart.
author: jinniew
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 53f45f469c39f9e389763aa0daed658e5a62d377
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119507"
---
# <a name="data-mart-resets-faq"></a>Veelgestelde vragen over opnieuw instellen van een datamart

Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart. Het opnieuw instellen van de datamart kan een tijdrovend proces zijn en is, afhankelijk van de omstandigheden, mogelijk niet de oplossing die nodig is. Daarom bevat dit onderwerp informatie over omstandigheden waarin opnieuw instellen van een datamart kan helpen en omstandigheden waarin het opnieuw instellen van de datamart waarschijnlijk niet helpt.

## <a name="what-is-a-data-mart-reset"></a>Wat houdt opnieuw instellen van een datamart in?

Met opnieuw instellen van een datamart worden de integratietaken uitgeschakeld, alle datamart-gegevens verwijderd en de integratie opnieuw ingeschakeld.

Om te zorgen dat oude gegevens niet zijn ingevoegd, kan opnieuw instellen van een datamart alleen worden gestart nadat bestaande taken zijn voltooid. Als u probeert een datamart opnieuw in te stellen voordat alle taken zijn voltooid, ontvangt u mogelijk een bericht, bijvoorbeeld: 'De datamart-reset kan niet worden verwerkt vanwege een actieve taak. Probeer het later opnieuw.'

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Wanneer moet ik een datamart opnieuw instellen?

Als er een of meer van de volgende uitspraken van toepassing zijn op uw situatie, kan opnieuw instellen van een datamart voor uw organisatie zin hebben:

- **De toepassingsdatabase is teruggezet**
- **U hebt een ondersteuningsticket geopend**: een ondersteuningstechnicus heeft u opdracht gegeven om de datamart opnieuw in te stellen als onderdeel van een probleemoplossingsstap.
- **Hoog percentage verouderde records**: verouderde records zijn op zichzelf geen reden om de datamart opnieuw in te stellen. Hoge percentages verlopen gegevens kunnen de algehele prestaties van het genereren en integreren van rapporten beïnvloeden en leiden tot extra databaseruimtegebruik. We raden u aan om een datamartreset te voltooien om de verouderde gegevens te verwijderen wanneer de datamart meer dan 80% aan verlopen gegevens bevat.
 
> [!NOTE]
> Het proces van het opnieuw instellen van een datamart wordt beïnvloed door het aantal grootboek- en budgettransacties in uw database. Afhankelijk van het aantal transacties in het systeem kan een reset van de datamart binnen een paar minuten worden uitgevoerd. Het kan echter ook tot vier uur in beslag nemen. Als het opnieuw instellen echter meer dan vier uur duurt, raden we u aan contact op te nemen met Ondersteuning.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Wanneer kunt u een datamart beter niet opnieuw instellen?

Hierna volgen enkele omstandigheden waarin het niet raadzaam is om een datamart opnieuw in te stellen:

- U ondervindt prestatieproblemen met betrekking tot gegevensintegraties.
- Er is sprake van een terugkerend resetpatroon om een van de volgende redenen:

    - **Ontbrekende of onverwachte gegevens in het rapport**: als u ziet dat er gegevens ontbreken, opent u een ondersteuningticket bij Microsoft om de rapportindeling en mogelijke problemen met gegevenssynchronisatie te bekijken.
    - **Vastgelopen integratie**
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Als ik de datamart opnieuw instel, raak ik dan rapporten kwijt die ik al heb ontworpen?

Nee. Uw rapporten worden opgeslagen in SQL-tabellen die niet worden beïnvloed door opnieuw instellen van de datamart. Als u zich zorgen maakt over het kwijtraken van rapporten die u hebt ontworpen, kunt u een back-up maken van de ontwerpen die u niet kwijt wilt raken. Als u een back-up van de ontwerpen wilt maken, opent u Report Designer en gaat u naar **Bedrijf \> Bedrijven \> Bouwstenen \> Exporteren**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Moeten alle gebruikers het systeem afsluiten voordat ik de datamart opnieuw kan instellen?

Nee. Gebruikers kunnen in het systeem blijven werken tijdens het opnieuw instellen van een datamart. Ze hebben echter geen toegang tot rapporten die met Financial Reporter zijn gemaakt totdat het instellen van de datamart is voltooid.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

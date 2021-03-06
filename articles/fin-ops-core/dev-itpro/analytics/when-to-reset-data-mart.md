---
title: Veelgestelde vragen over opnieuw instellen van een datamart
description: Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266604"
---
# <a name="data-mart-resets-faq"></a>Veelgestelde vragen over opnieuw instellen van een datamart

Dit onderwerp biedt antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart. Het opnieuw instellen van de datamart kan een tijdrovend proces zijn en is, afhankelijk van de omstandigheden, mogelijk niet de oplossing die nodig is. Daarom bevat dit onderwerp informatie over omstandigheden waarin opnieuw instellen van een datamart kan helpen en omstandigheden waarin het opnieuw instellen van de datamart waarschijnlijk niet helpt.

## <a name="what-is-a-data-mart-reset"></a>Wat houdt opnieuw instellen van een datamart in?

Met opnieuw instellen van een datamart worden de integratietaken uitgeschakeld, alle datamart-gegevens verwijderd en de integratie opnieuw ingeschakeld.

Om te zorgen dat oude gegevens niet zijn ingevoegd, kan opnieuw instellen van een datamart alleen worden gestart nadat bestaande taken zijn voltooid. Als u probeert een datamart opnieuw in te stellen voordat alle taken zijn voltooid, ontvangt u mogelijk een bericht, bijvoorbeeld: 'De datamart-reset kan niet worden verwerkt vanwege een actieve taak. Probeer het later opnieuw.'

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Wanneer moet ik een datamart opnieuw instellen?

Als er een of meer van de volgende uitspraken van toepassing zijn op uw situatie, kan opnieuw instellen van een datamart voor uw organisatie zin hebben:

- De toepassingsdatabase is teruggezet.
- U hebt een ondersteuningsticket geopend en een ondersteuningstechnicus heeft u opdracht gegeven om de datamart opnieuw in te stellen als onderdeel van een probleemoplossingsstap.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Wanneer kunt u een datamart beter niet opnieuw instellen?

Hierna volgen enkele omstandigheden waarin het niet raadzaam is om een datamart opnieuw in te stellen:

- U ondervindt prestatieproblemen die betrekking hebben op gegevenssynchronisatie.
- Er is sprake van een terugkerend resetpatroon om een van de volgende redenen:

    - **Ontbrekende gegevens**: als u ziet dat er gegevens ontbreken, opent u een ondersteuningticket bij Microsoft om de rapportindeling en mogelijke problemen met gegevenssynchronisatie te bekijken.
    - **Vastgelopen integratie**
    - **Verouderde records**: verouderde records zijn op zichzelf geen reden om de datamart opnieuw in te stellen. Als u een grote gegevensset hebt, zal het even duren deze opnieuw in te stellen, maar is het niet waarschijnlijk dat dit iets oplevert.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Als ik de datamart opnieuw instel, raak ik dan rapporten kwijt die ik al heb ontworpen?

Nee. Uw rapporten worden opgeslagen in SQL-tabellen die niet worden beïnvloed door opnieuw instellen van de datamart. Als u zich zorgen maakt over het kwijtraken van rapporten die u hebt ontworpen, kunt u een back-up maken van de ontwerpen die u niet kwijt wilt raken. Als u een back-up van de ontwerpen wilt maken, opent u Report Designer en gaat u naar **Bedrijf \> Bedrijven \> Bouwstenen \> Exporteren**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Moeten alle gebruikers het systeem afsluiten voordat ik de datamart opnieuw kan instellen?

Nee. Gebruikers kunnen in het systeem blijven werken tijdens het opnieuw instellen van een datamart. Ze hebben echter geen toegang tot rapporten die met Financial Reporter zijn gemaakt totdat het instellen van de datamart is voltooid.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

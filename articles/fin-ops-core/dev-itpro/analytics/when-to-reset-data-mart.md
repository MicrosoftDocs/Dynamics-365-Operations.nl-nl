---
title: Veelgestelde vragen over opnieuw instellen van een datamart
description: Dit artikel bevat antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.search.form: ''
ms.openlocfilehash: 949bf64fefe2dc70541eb5a94518d6b9fe1d3eb8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289871"
---
# <a name="data-mart-resets-faq"></a>Veelgestelde vragen over opnieuw instellen van een datamart

Dit artikel bevat antwoorden op een aantal veelgestelde vragen over het opnieuw instellen (reset) van een datamart. Het opnieuw instellen van de datamart kan een tijdrovend proces zijn en is, afhankelijk van de omstandigheden, mogelijk niet de oplossing die nodig is. Daarom bevat dit artikel informatie over omstandigheden waarin opnieuw instellen van een datamart kan helpen en omstandigheden waarin het opnieuw instellen van de datamart waarschijnlijk niet helpt.

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
- Uw integratie met Financial Reporter is niet ingeschakeld. 

    - Dit betekent dat grootboekgegevens niet meer worden gesynchroniseerd met uw datamart voor Financial Reporting. Uw Financial Reporter ontvangt mogelijk geen actuele cijfers voor uw financiële rapporten. Dit gebeurt meestal als u Financial Reporter lange tijd niet hebt gebruikt.
    - U wordt gevraagd om integratie in te schakelen door de datamart-functie opnieuw in te stellen. U kunt doorgaan door **Ja** te selecteren. U kunt de datamart ook later opnieuw instellen. Nadat integratie is ingeschakeld, worden uw grootboekgegevens opnieuw gesynchroniseerd in Financial Reporter. 
- Er is sprake van een terugkerend resetpatroon om een van de volgende redenen:

    - **Ontbrekende of onverwachte gegevens in het rapport**: als u ziet dat er gegevens ontbreken, opent u een ondersteuningticket bij Microsoft om de rapportindeling en mogelijke problemen met gegevenssynchronisatie te bekijken.
    - **Vastgelopen integratie**: als u ziet dat de integratiestatus is vastgelopen, kan dit te wijten zijn aan een groot transactievolume in het systeem. Deze status lost zichzelf op. Als u echter ziet dat de integratiestatus meer dan vier uur vastloopt, opent u een ondersteuningsticket bij Microsoft. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Als ik de datamart opnieuw instel, raak ik dan rapporten kwijt die ik al heb ontworpen?

Nee. Uw rapporten worden opgeslagen in SQL-tabellen die niet worden beïnvloed door opnieuw instellen van de datamart. Als u zich zorgen maakt over het kwijtraken van rapporten die u hebt ontworpen, kunt u een back-up maken van de ontwerpen die u niet kwijt wilt raken. Als u een back-up van de ontwerpen wilt maken, opent u Report Designer en gaat u naar **Bedrijf \> Bedrijven \> Bouwstenen \> Exporteren**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Moeten alle gebruikers het systeem afsluiten voordat ik de datamart opnieuw kan instellen?

Nee. Gebruikers kunnen in het systeem blijven werken tijdens het opnieuw instellen van een datamart. Ze hebben echter geen toegang tot rapporten die met Financial Reporter zijn gemaakt totdat het instellen van de datamart is voltooid.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

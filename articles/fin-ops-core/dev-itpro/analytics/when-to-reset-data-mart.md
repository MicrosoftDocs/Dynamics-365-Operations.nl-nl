---
title: Wanneer moet een datamart opnieuw worden ingesteld
description: In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.
author: jinniew
ms.date: 05/06/2021
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
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988987"
---
# <a name="when-to-reset-a-data-mart"></a>Wanneer moet een datamart opnieuw worden ingesteld

Het opnieuw instellen van een datamart kan tijdrovend zijn. Afhankelijk van de omstandigheden is deze reset-actie mogelijk niet de oplossing die nodig is. In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Wanneer moet ik een datamart opnieuw instellen?
Houd rekening met de volgende vragen voordat u een datamart opnieuw instelt. Als u een of meer vragen met ja beantwoordt, kan dat erop wijzen dat uw organisatie baat kan hebben van het opnieuw instellen van de datamart.

- Is de toepassingsdatabase teruggezet?
- Als u een ondersteuningsincident hebt geopend en een ondersteuningstechnicus heeft u opdracht gegeven om de datamart opnieuw in te stellen als onderdeel van een probleemoplossingsstap?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Wanneer kunt u een datamart beter niet opnieuw instellen?
Er zijn omstandigheden waarin het niet wordt aangeraden een datamart opnieuw in te stellen. Deze omstandigheden zijn: 

- U ondervindt prestatieproblemen die betrekking hebben op gegevenssynchronisatie. 
- Als er sprake is van een terugkerend resetpatroon vanwege een van de volgende redenen: 
  - **Ontbrekende gegevens** 
  - **Vastgelopen integratie** 
  - **Verouderde records**: verouderde records zijn op zichzelf geen reden om de datamart opnieuw in te stellen. Als u een grote gegevensset hebt, zal het even duren deze opnieuw in te stellen, maar is het niet waarschijnlijk dat dit iets oplevert.
 
## <a name="what-is-a-data-mart-reset"></a>Wat houdt opnieuw instellen van een datamart in?
- Een reset wordt alleen gestart wanneer bestaande taken zijn voltooid. Op deze manier zorgt u ervoor dat er geen oude gegevens worden ingevoegd. Op dit punt wordt er mogelijk een bericht weergegeven met de tekst "De datamart-reset kan niet worden verwerkt vanwege een actieve taak. Probeer het later opnieuw.”
- Met de reset worden de integratietaken uitgeschakeld en worden alle datamartgegevens verwijderd. De integratie wordt opnieuw ingeschakeld.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Als ik de datamart opnieuw instel, raak ik dan rapporten kwijt die ik al heb ontworpen? 
Nee, uw rapporten worden opgeslagen in SQL-tabellen die niet worden beïnvloed door opnieuw instellen van de datamart. Als u zich zorgen maakt over het kwijtraken van rapporten die u hebt ontworpen, kunt u een back-up maken van de ontwerpen die u niet kwijt wilt raken. Als u een back-up wilt maken, opent u Report Designer en gaat u naar **Bedrijf > Bedrijven > Bouwstenen > Exporteren**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Moeten alle gebruikers het systeem afsluiten om de datamart opnieuw in te stellen?
Nee, gebruikers kunnen in het systeem blijven werken tijdens het opnieuw instellen van de datamart. Ze hebben echter geen toegang tot rapporten die met Financial Reporter zijn gemaakt totdat de datamart opnieuw is ingesteld. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

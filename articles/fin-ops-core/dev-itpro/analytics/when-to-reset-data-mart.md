---
title: Wanneer moet een datamart opnieuw worden ingesteld
description: In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71324d4aa2d20dd6ae4729412a017d130ab0144f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563724"
---
# <a name="when-to-reset-a-data-mart"></a>Wanneer moet een datamart opnieuw worden ingesteld

Het opnieuw instellen van een datamart kan tijdrovend zijn. Afhankelijk van de omstandigheden is deze reset-actie mogelijk niet de oplossing die nodig is. In dit onderwerp worden de omstandigheden vermeld die kunnen worden verbeterd door het opnieuw instellen van een datamart en omstandigheden waarin het resetten van uw datamart waarschijnlijk niet helpt.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Wanneer moet een datamart opnieuw worden ingesteld?
Houd rekening met de volgende vragen voordat u een datamart opnieuw instelt. Als u een of meer vragen met ja beantwoordt, kan dat erop wijzen dat uw organisatie baat kan hebben van het opnieuw instellen van de datamart.

- De toepassingsdatabase is opnieuw ingesteld, maar de database van de datamart niet.
- U ziet onjuiste gegevens voor een boekhoudperiode. Dit is dus niet het resultaat van een probleem met het rapportontwerp.
- U ziet onjuiste gegevens voor een boekhoudperiode en records worden weergegeven onder Integratiepogingen op de pagina **Integratiestatus** in Report Designer (start Report Designer en selecteer **Extra > Integratiestatus**).
- U hebt een ondersteuningsincident geopend en een ondersteuningstechnicus heeft u opdracht gegeven om de datamart opnieuw in te stellen als onderdeel van een probleemoplossingsstap.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Wanneer kunt u een datamart beter niet opnieuw instellen?
Er zijn omstandigheden waarin het niet wordt aangeraden een datamart opnieuw in te stellen. Deze omstandigheden zijn: 

- Omstandigheden waarvoor de reden niet in dit onderwerp wordt weergegeven.
- U ondervindt prestatieproblemen die zijn gekoppeld aan gegevenssynchronisatie. Hierbij helpt het opnieuw instellen van de datamart waarschijnlijk niet.
- Als er sprake is van een terugkerend resetpatroon vanwege een van de volgende redenen: 
  - **Ontbrekende gegevens**: elimineer eerst problemen met rapportontwerp en timing van gegevenssynchronisatie. U ziet bijvoorbeeld dat het feitenoverzicht niet is uitgevoerd omdat er ontbrekende gegevens zijn geboekt.
  - **Vastgelopen integratie**: als de integratie langzaam is of lijkt te zijn vastgelopen, wordt het probleem waarschijnlijk niet opgelost door de datamart opnieuw in te stellen.
  - **Pogingen om opnieuw in te stellen zijn mislukt**: als een aantal pogingen is gedaan om een reset te voltooien en deze niet zijn gelukt vanwege ontbrekende gegevens, is het raadzaam een ondersteuningsincident te openen en samen met een ondersteuningstechnicus de situatie te analyseren voordat u de datamart opnieuw probeert in te stellen.
  - **Verouderde records**: verouderde records zijn op zichzelf geen reden om de datamart opnieuw in te stellen. Als u een grote gegevensset hebt, zal het even duren deze opnieuw in te stellen, maar is het niet waarschijnlijk dat dit iets oplevert.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Wat een datamart-reset niet doet  
- Een reset wordt alleen gestart wanneer bestaande taken zijn voltooid. Op deze manier zorgt u ervoor dat er geen oude gegevens worden ingevoegd. Op dit punt wordt er mogelijk een bericht weergegeven met de tekst "De datamart-reset kan niet worden verwerkt vanwege een actieve taak. Probeer het later opnieuw.”
- Met de reset worden de integratietaken uitgeschakeld en worden alle datamartgegevens verwijderd. De integratie wordt opnieuw ingeschakeld.

> [!NOTE]
> De volgende punten geven twee zaken aan die met een datamart-reset *niet* gebeuren. <br>
> - Met resets worden rapportontwerpen niet gewist. <br>
> - Met resets worden bedrijfs- of gebruikersgegevens niet gewist, tenzij u dat hebt aangegeven.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
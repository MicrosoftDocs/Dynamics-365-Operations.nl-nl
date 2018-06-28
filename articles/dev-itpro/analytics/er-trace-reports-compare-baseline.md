---
title: Gegenereerde rapportresultaten traceren en vergelijken met basislijnwaarden
description: Dit onderwerp biedt informatie over hoe u de resultaten van gegenereerde ER-rapporten kunt vergelijken met basislijnrapportwaarden.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Gegenereerde rapportresultaten traceren en vergelijken met basislijnwaarden

[!include[banner](../includes/banner.md)]

U kunt de resultaten van ER-indelingen traceren die uitgaande elektronische documenten genereren. Wanneer het genereren van tracering is ingeschakeld (ER-gebruikersparameter **Uitvoeren in foutoplossingsmodus**), wordt een nieuwe tracerecord gegenereerd in het uitvoeringslogboek met ER-indeling, elke keer dat een ER-rapport wordt uitgevoerd. De volgende gegevens worden opgeslagen in elke trace die wordt gegenereerd:

- Alle waarschuwingen die zijn gegenereerd door validatieregels
- Alle fouten die zijn gegenereerd door validatieregels 
- Alle gegenereerde bestanden die zijn opgeslagen als bijlagen van de traceringsrecord

U kunt afzonderlijke basislijntoepassingsbestanden voor een bepaalde ER-indeling opslaan. Bestanden worden als basislijnbestanden beschouwd wanneer ze de verwachte resultaten beschrijven van rapporten die worden uitgevoerd. Als een basislijnbestand beschikbaar is voor een ER-indeling die werd uitgevoerd terwijl het genereren van tracering was ingeschakeld, slaat de trace, naast de gegevens die reeds eerder zijn vermeld, het resultaat op van de vergelijking van het gegenereerde elektronische document met het basislijnbestand. Met één klik kunt u ook het gegenereerde elektronische document en het basislijnbestand in een enkel zip-bestand krijgen. Vervolgens kunt u een gedetailleerde vergelijking uitvoeren met behulp van een extern hulpprogramma zoals Windiff.

U kunt de tracering evalueren om te analyseren of de elektronische documenten die worden gegenereerd, de verwachte inhoud bevatten. U kunt deze evaluatie uitvoeren in een UAT-omgeving (User Acceptance Testing) wanneer de codebasis is gewijzigd (bijvoorbeeld wanneer u bent gemigreerd naar een nieuw exemplaar van de toepassing, hotfixpakketten hebt geïnstalleerd of codewijzigingen hebt geïmplementeerd). Op deze manier kunt u ervoor zorgen dat de evaluatie geen invloed heeft op de uitvoering van ER-rapporten die worden gebruikt. Voor veel ER-rapporten kan de evaluatie plaatsvinden in de modus zonder toezicht.

Voor meer informatie over deze functie speelt u de taakbegeleiders **ER-rapporten genereren en resultaten vergelijken (deel 1)** en **ER-rapporten genereren en resultaten vergelijken (deel 2)** af, die deel uitmaken van het bedrijfsproces **7.5.4.3 IT-services en -oplossingen testen ( 10679)** en kunnen worden gedownload uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684). Deze taakrichtlijnen begeleiden u bij het proces van het configureren van het ER-raamwerk om basislijnbestanden te gebruiken om gegenereerde elektronische documenten te evalueren.


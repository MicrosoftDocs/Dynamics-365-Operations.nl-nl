---
title: RegeIs en parameters instellen voor het cross-docken en klantlevering
description: Deze procedure demonstreert de stappen om aanvullingsregels te maken.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc5404e5eb1679659604a6268fa09519a7a4282e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003712"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a>RegeIs en parameters instellen voor het cross-docken en klantlevering

[!include [banner](../includes/banner.md)]

Deze procedure demonstreert de stappen om aanvullingsregels te maken. Aanvullingsregels kunnen worden gebruikt om te bepalen hoe producten worden gedistribueerd naar winkels wanneer cross-docking en klantlevering worden gebruikt. Aanvullingsregels kunnen worden ingesteld voor winkels of winkelgroepen. Het gewicht dat voor elke regel is gedefinieerd in een regel, bepaalt hoe de hoeveelheden van producten worden gedistribueerd tussen de winkels wanneer aanvullingsregels worden gebruikt als de distributiemethode voor cross-docking of klantlevering. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Aanvullingsregels.
2. Klik op Nieuw.
3. Typ een waarde in het veld Aanvullingsregel.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Opslaan.
6. Klik op Toevoegen.
7. Markeer in de lijst de geselecteerde rij.
    * U kunt Aanvullingshiërarchie of Kanaal kiezen voor het type. De waarde bepaalt of de selectie in Naam een hiërarchie van kanalen of een specifiek kanaal is.  Voor dit voorbeeld laat u het als Aanvullingshiërarchie ingesteld.  
8. Selecteer een waarde in het veld Naam.
    * De standaardgewichtwaarde wordt gevuld vanuit het gewicht dat is gedefinieerd in het magazijn.  Dit gewicht kan voor de aanvullingsregel worden gebruikt of u kunt een nieuw gewicht in het veld Gewicht invoeren.  
9. Voer een getal in het veld Gewicht in.
10. Klik op Toevoegen.
11. Markeer in de lijst de geselecteerde rij.
12. Selecteer 'Kanaal' in het veld Type.
13. Typ of selecteer een waarde in het veld Naam.
14. Voer een getal in het veld Gewicht in.
15. Klik op Opslaan.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
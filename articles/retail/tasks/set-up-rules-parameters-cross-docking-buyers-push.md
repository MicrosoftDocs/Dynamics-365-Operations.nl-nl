---
title: " RegeIs en parameters instellen voor het cross-docken en klantlevering"
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a22756279ba316a7efd4d09c48c55e8cc98ba29d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "366323"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> RegeIs en parameters instellen voor het cross-docken en klantlevering

[!include[task guide banner](../includes/task-guide-banner.md)]

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


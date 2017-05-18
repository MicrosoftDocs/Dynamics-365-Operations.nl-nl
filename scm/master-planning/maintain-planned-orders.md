---
title: Geplande orders onderhouden
description: Dit artikel bevat informatie over het beheer van geplande orders. Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: df3b7d285e2aa4c3e1fc102b821c30bdc7c9fb83
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="maintain-planned-orders"></a>Geplande orders onderhouden

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie over het beheer van geplande orders. Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.

U kunt geplande orders vanuit de werkruimte **Hoofdplanning**, de lijst **Geplande order** of de lijsten **Geplande productieorders**, **Geplande inkooporders** en **Geplande overboeking** beheren. U kunt het veld **Status** gebruiken om uw voortgang bij te houden. De volgende waarden worden gebruikt:

-   Wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben de geplande orders de status **Niet-verwerkt**.
-   Wanneer u besluit een geplande order niet te fiatteren, kunt u die order de status **Voltooid** geven.
-   Wanneer u besluit een geplande order te fiatteren, geeft u die order de status **Goedgekeurd**. Deze status geeft aan dat u ermee akkoord gaat dat de geplande order wordt gefiatteerd, maar de order is nog niet gefiatteerd.

**Opmerking:** Een goedgekeurde, geplande order wordt in de huidige status overgeboekt naar de volgende berekening in de hoofdplanning. U kunt geplande orders fiatteren door te klikken op **Fiatteren**. De volgende geplande orders kunnen worden gefiatteerd:

-   De geplande order die is geselecteerd.
-   Meerdere geplande orders.
-   Geplande orders die door een explosie vanaf de pagina **Explosie** zijn gegenereerd. Klik op **Geplande orders**, selecteer de geplande order en klik op **Fiatteren**.

Wanneer een geplande order wordt gefiatteerd, wordt die order naar de ordersectie van de relevante module verplaatst. **Opmerking:** U kunt met de rechtermuisknop op een geplande order met een bepaalde status klikken en vervolgens op geplande orders met dezelfde status filteren. Dit is een handige functionaliteit die u kunt gebruiken wanneer u bijvoorbeeld alle geplande orders met de status **Goedgekeurd** wilt filteren zodat u ze kunt fiatteren.

<a name="see-also"></a>Zie ook
--------

[Hoofdplannen](master-plans.md)





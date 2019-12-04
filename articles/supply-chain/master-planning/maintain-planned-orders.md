---
title: Geplande orders onderhouden
description: Dit onderwerp bevat informatie over het beheer van geplande orders. Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813771"
---
# <a name="maintain-planned-orders"></a>Geplande orders onderhouden

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over het beheer van geplande orders. Het beschrijft hoe u de status van geplande orders kunt bijwerken en fiatteren en hoe u kunt filteren voor geplande orders die dezelfde status als een geselecteerde geplande order hebben.

U kunt geplande orders vanuit de werkruimte **Hoofdplanning**, de lijst **Geplande order** of de lijsten **Geplande productieorders**, **Geplande inkooporders** en **Geplande overboeking** beheren. 

## <a name="planned-order-status"></a>Status van geplande order
U kunt het veld **Status** gebruiken om uw voortgang bij te houden. De volgende waarden worden gebruikt:

-   Wanneer geplande orders door de hoofdplanning worden gegenereerd, hebben de geplande orders de status **Niet-verwerkt**.
-   Wanneer u besluit een geplande order niet te fiatteren, kunt u die order de status **Voltooid** geven.
-   Als u een geplande order wilt fiatteren, kunt u de status wijzigen in **Goedgekeurd**. Geplande orders met de status **Goedgekeurd** worden geëerbiedigd door de hoofdplanning. Ze worden dus niet gewijzigd of verwijderd tijdens een latere hoofdplanningsuitvoering. 

## <a name="firming-planned-orders"></a>Geplande orders fiatteren 
Door geplande orders te fiatteren, worden echte orders gemaakt. Dit worden ook wel *vrijgegeven* of *openstaande orders* genoemd. Wanneer een geplande order wordt gefiatteerd, wordt die order naar de ordersectie van de relevante module verplaatst.

Op de pagina **Geplande orders** kunt u twee opties voor fiatteren selecteren:

-   **Fiatteren**: hiermee kunt u een of meer geselecteerde geplande orders fiatteren.
-   **Alles fiatteren**: hiermee kunt u alle geplande orders in het filter fiatteren. Als u **Alles fiatteren** gebruikt, hoeft u de geplande order niet te selecteren. Alle geplande orders in het filter worden gefiatteerd. Deze optie kan handig zijn als u een groot aantal geplande orders wilt fiatteren.

> [!NOTE]
> U kunt een gefiatteerde geplande order volgen via **Fiatteringshistorie** onder **formulier Geplande orders > Weergeven > Fiatteringshistorie**.

## <a name="parallelize-firming"></a>Fiattering parallel uitvoeren
Als u meerdere orders tegelijk wilt fiatteren, kunt u de uitvoeringstijd of prestaties verbeteren door de uitvoering parallel te laten verlopen. Deze optie is beschikbaar wanneer u meerdere geplande orders fiatteert met **Fiatteren** of **Alles fiatteren**. De volgende parameters zijn beschikbaar:

-   **Parallel fiatteren**: als **Ja** is ingesteld, wordt het fiatteringsproces uitgevoerd parallel met het aantal threads dat is gedefinieerd in **Aantal threads**.
-   **Aantal threads** : hiermee bepaalt u het aantal threads waarmee het fiatterinigsproces parallel moet worden uitgevoerd. De parameter wordt alleen weergegeven als **Parallel fiatteren** is ingesteld op **Ja**.


<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht van Hoofdplannen](master-plans.md)




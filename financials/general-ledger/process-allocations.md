---
title: Toewijzingen verwerken
description: Dit artikel bevat informatie over toewijzingen, de opties voor verwerking hiervan in Microsoft Dynamics 365 for Operations en de wijze waarop u deze kunt gebruiken in budgetplanningen. Toewijzingen worden gebruikt om bedragen over meerdere combinaties van grootboekrekeningen te verdelen. Hiermee kunt u ervoor zorgen dat uitgaven en opbrengsten in de boekhouding aan het juiste object worden doorberekend.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f66414beeacafdbbe3b6f7bcba8481096636e025
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="process-allocations"></a>Toewijzingen verwerken

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie over toewijzingen, de opties voor verwerking hiervan in Microsoft Dynamics 365 for Operations en de wijze waarop u deze kunt gebruiken in budgetplanningen. Toewijzingen worden gebruikt om bedragen over meerdere combinaties van grootboekrekeningen te verdelen. Hiermee kunt u ervoor zorgen dat uitgaven en opbrengsten in de boekhouding aan het juiste object worden doorberekend.

Microsoft Dynamics 365 for Operations biedt de volgende mogelijkheden om dit proces te ondersteunen:

-   Handmatig toewijzen van transactiebedragen door de actie Splitsen in boekhoudingsverdelingen te gebruiken of door standaardsjablonen van financiële dimensies toe te passen op een document. Zie [Boekhoudingsverdelingen](../accounts-payable/accounting-distributions.md) voor meer informatie.
-   Automatisch toewijzen van transactiebedragen op basis van toewijzingstermijnen die zijn gedefinieerd in de afzonderlijke hoofdrekening. Toewijzingsjournaalregels worden gegenereerd voor elk journaal op basis van het percentage en de doelgrootboekrekening wanneer een journaalregel voldoet aan de criteria die als brongrootboekrekening zijn gedefinieerd.
-   Automatisch toewijzen van grootboeksaldi of vaste bedragen op basis van grootboektoewijzingsregels. De grootboektoewijzingsregels worden verwerkt op periodieke basis met toewijzingsjournalen. 

###  <a name="allocations-in-budget-planning"></a>Toewijzingen in budgetplanning

Grootboektoewijzingsregels kunnen worden gebruikt voor budgetplannen. Als u toewijzingsregels voor het grootboek gebruikt in budgetplanning, werken de toewijzingsregels op dezelfde manier als in het grootboek, alleen komen de bron- en doelgegevens uit het budgetplan. U kunt handmatig toewijzingsregels voor het grootboek selecteren voor budgetplanning. U kunt ook een toewijzingsschema gebruiken dat als onderdeel van een werkstroomproces werkt.

> [!NOTE]
> U kunt geen intercompany-toewijzingsregels voor het grootboek gebruiken voor budgetplanning.







---
title: Toewijzingen verwerken
description: Dit artikel bevat informatie over toewijzingen, de opties voor verwerking hiervan in Microsoft Dynamics 365 Finance en de manier waarop u deze kunt gebruiken in budgetplanningen. Toewijzingen worden gebruikt om bedragen over meerdere combinaties van grootboekrekeningen te verdelen. Hiermee kunt u ervoor zorgen dat uitgaven en opbrengsten in de boekhouding aan het juiste object worden doorberekend.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0629b32d39f4d74ec37eebe92b92e0b186b5fce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877978"
---
# <a name="process-allocations"></a>Toewijzingen verwerken

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over toewijzingen, de opties voor verwerking hiervan en de wijze waarop u deze kunt gebruiken in budgetplanningen. Toewijzingen worden gebruikt om bedragen over meerdere combinaties van grootboekrekeningen te verdelen. Hiermee kunt u ervoor zorgen dat uitgaven en opbrengsten in de boekhouding aan het juiste object worden doorberekend.

De volgende mogelijkheden ondersteunen dit proces:

-   Handmatig toewijzen van transactiebedragen door de actie Splitsen in boekhoudingsverdelingen te gebruiken of door standaardsjablonen van financiële dimensies toe te passen op een document. Zie [Boekhoudingsverdelingen](../accounts-payable/accounting-distributions.md) voor meer informatie.
-   Automatisch toewijzen van transactiebedragen op basis van toewijzingstermijnen die zijn gedefinieerd in de afzonderlijke hoofdrekening. Toewijzingsjournaalregels worden gegenereerd voor elk journaal op basis van het percentage en de doelgrootboekrekening wanneer een journaalregel voldoet aan de criteria die als brongrootboekrekening zijn gedefinieerd. Zie voor meer informatie [Toewijzingstermijnen voor hoofdaccounts](../general-ledger/main-account-allocation-terms.md)
-   Automatisch toewijzen van grootboeksaldi of vaste bedragen op basis van grootboektoewijzingsregels. De grootboektoewijzingsregels worden verwerkt op periodieke basis met toewijzingsjournalen. Zie voor meer informatie [Toewijzingsregels](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Toewijzingen in budgetplanning

Grootboektoewijzingsregels kunnen worden gebruikt voor budgetplannen. Als u toewijzingsregels voor het grootboek gebruikt in budgetplanning, werken de toewijzingsregels op dezelfde manier als in het grootboek, alleen komen de bron- en doelgegevens uit het budgetplan. U kunt handmatig toewijzingsregels voor het grootboek selecteren voor budgetplanning. U kunt ook een toewijzingsschema gebruiken dat als onderdeel van een werkstroomproces werkt.

> [!NOTE]
> U kunt geen intercompany-toewijzingsregels voor het grootboek gebruiken voor budgetplanning.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

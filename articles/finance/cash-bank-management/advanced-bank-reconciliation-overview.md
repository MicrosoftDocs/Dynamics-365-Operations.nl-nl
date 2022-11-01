---
title: Overzicht van geavanceerde bankafstemming
description: In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven. Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.
author: angelad116
ms.date: 10/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 677a032ce77fbe57393c85235a1c64dba3958f2d
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715144"
---
# <a name="advanced-bank-reconciliation-overview"></a>Overzicht van geavanceerde bankafstemming

[!include [banner](../includes/banner.md)]

In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven. Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.

Met de functie voor geavanceerde bankafstemming kunt u bankafschriften importeren. Het geïmporteerde bankafschrift kan vervolgens automatisch in banktransacties worden afgestemd. Hier vindt u de stappen in de geavanceerde bankafstemmingsstroom.

1.  Stel de import van een bankafschrift in.
    -   Importeer bankafschriften via het gegevensentiteitsraamwerk.
    -   Drie typische bankafschriftindelingen zijn ingebouwd: ISO20022, BAI2 en MT940.
    -   De functionaliteit kan naar iedere indeling worden uitgebreid.

2.  Stel een nummerreeks in die moet worden gebruikt voor geavanceerde bankafstemming en definieer de afstemmingsregels voor bankafstemming.
    -   Een afstemmingsregel is een reeks criteria die worden gebruikt om regels van bankafschriften en Microsoft Dynamics 365 Finance-banktransactieregels te filteren tijdens het afstemmingsproces. Afhankelijk van uw bedrijfspraktijk kunt u meerdere afstemmingsregels instellen om uw afstemmingsproces te automatiseren en te optimaliseren.

3.  Stem bankafschriften af met de banktransacties van Finance.
    -   Voer automatische afstemming en het maken van afstemmingsjournalen uit.
    -   Geef bankafschriften en banktransacties van Finance naast elkaar weer.
    -   Boek banktransacties van Finance automatisch als deze op een bankafschrift worden weergegeven, maar niet in de Finance-app.
    -   Genereer een afstemmingsafschrift.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

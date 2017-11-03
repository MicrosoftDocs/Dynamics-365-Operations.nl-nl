---
title: Overzicht van geavanceerde bankafstemming
description: In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven. Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33150777222faa97af7488c59ab13cb0fb9e8e2c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="advanced-bank-reconciliation-overview"></a>Overzicht van geavanceerde bankafstemming

[!include[banner](../includes/banner.md)]


In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven. Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.

Met de functie voor geavanceerde bankafstemming kunt u bankafschriften importeren. Het geïmporteerde bankafschrift kan vervolgens automatisch in banktransacties worden afgestemd. Hier vindt u de stappen in de geavanceerde bankafstemmingsstroom.

1.  Stel de import van een bankafschrift in.
    -   Importeer bankafschriften via het gegevensentiteitsraamwerk.
    -   Drie typische bankafschriftindelingen zijn ingebouwd: ISO20022, BAI2 en MT940.
    -   De functionaliteit kan naar iedere indeling worden uitgebreid.

2.  Stel een nummerreeks in die moet worden gebruikt voor geavanceerde bankafstemming en definieer de afstemmingsregels voor bankafstemming.
    -   Een afstemmingsregel is een reeks criteria die worden gebruikt om regels van bankafschriften en banktransactieregels van Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition te filteren tijdens het afstemmingsproces. Afhankelijk van uw bedrijfspraktijk kunt u meerdere afstemmingsregels instellen om uw afstemmingsproces te automatiseren en te optimaliseren.

3.  Stem bankafschriften af met de banktransacties van Finance and Operations.
    -   Voer automatische afstemming en het maken van afstemmingsjournalen uit.
    -   Geef bankafschriften en banktransacties van Finance and Operations naast elkaar weer.
    -   Boek banktransacties van Finance and Operations automatisch als deze op een bankafschrift worden weergegeven, maar niet in Finance and Operations.
    -   Genereer een afstemmingsafschrift.







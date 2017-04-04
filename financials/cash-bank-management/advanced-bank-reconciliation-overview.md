---
title: Overzicht van geavanceerde bankafstemming
description: In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven. Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Overzicht van geavanceerde bankafstemming

In dit artikel wordt de stroom voor het geavanceerde bankafstemmingsproces beschreven. Met de geavanceerde bankafstemmingsfunctie kunt u bankafschriften importeren die automatisch kunnen worden afgestemd vanuit banktransacties.

Met de functie voor geavanceerde bankafstemming kunt u bankafschriften importeren. Het geïmporteerde bankafschrift kan vervolgens automatisch in banktransacties worden afgestemd. Hier vindt u de stappen in de geavanceerde bankafstemmingsstroom.

1.  Stel de import van een bankafschrift in.
    -   Importeer bankafschriften via het gegevensentiteitsraamwerk.
    -   Drie typische bankafschriftindelingen zijn ingebouwd: ISO20022, BAI2 en MT940.
    -   De functionaliteit kan naar iedere indeling worden uitgebreid.

2.  Stel een nummerreeks in die moet worden gebruikt voor geavanceerde bankafstemming en definieer de afstemmingsregels voor bankafstemming.
    -   Afstemmingsregel voor bankafstemming is een reeks criteria die worden gebruikt voor het filteren van regels van bankafschriften en Microsoft Dynamics 365 op transactieregels van de bank bewerkingen tijdens het afstemmingsproces. U kunt meer dan één overeenkomende regel automatiseren en optimaliseren van uw afstemmingsproces instellen, afhankelijk van uw zakelijke verkeer.

3.  Bankafschriften afstemmen met Dynamics 365 voor bewerkingen banktransacties.
    -   Voer automatische afstemming en het maken van afstemmingsjournalen uit.
    -   Bankafschriften bekijken en Dynamics 365 voor bewerkingen banktransacties naast elkaar.
    -   Automatisch Dynamics 365 voor bewerkingen banktransacties boeken als ze worden weergegeven op een bankafschrift maar worden niet in Dynamics 365 voor bewerkingen weergegeven.
    -   Genereer een afstemmingsafschrift.





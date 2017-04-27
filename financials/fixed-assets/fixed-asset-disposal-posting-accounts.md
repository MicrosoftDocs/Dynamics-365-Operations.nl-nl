---
title: Boekingsrekeningen voor afboeking van vaste activa
description: In dit artikel wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het afboeken van activa.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 670a67de2287fa5d0be29463f6f456b27fd88000
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a>Boekingsrekeningen voor afboeking van vaste activa

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het afboeken van activa.

Selecteer op de pagina Boekingsprofielen voor vaste activa, op het sneltabblad Grootboekrekeningen, de optie Verkoop/afstoting en Afstoting - uitval voor het instellen van boekingen naar het grootboek.

Voor beide transactietypen wordt de grootboekrekening gecrediteerd voor de afboekwaarde van het vaste activum. Het debetbedrag wordt naar een tegenrekening geboekt, die bijvoorbeeld een bankrekening kan zijn. Als een vast activum aan een klant wordt verkocht, wordt de klantrekening in plaats van de tegenrekening gebruikt.

Klik op Afstoting en klik vervolgens op Verkoop of Uitval, en stel vervolgens gedetailleerde rekeningen in om de nettoboekwaarde van het vaste activum om te keren. U kunt ook informatie invoeren in de velden Waarde boeken en Verkoopwaarde op de pagina Afstotingsparameters. 

Door de afboekingstransactie voor een activum in een groep met lage waarden, wordt de nettoboekwaarde van de groep met lage waarden alleen verminderd met het afgeboekte bedrag. Wanneer de verkoop van een activum echter de nettoboekwaarde van de groep met lage waarden overschrijdt, wordt de nettoboekwaarde verlaagd tot nul.







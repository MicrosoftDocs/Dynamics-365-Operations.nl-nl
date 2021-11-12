---
title: Boekingsrekeningen voor afboeking van vaste activa
description: In dit onderwerp wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het afboeken van activa.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c82cb8b82f2cc8424675f76c68613a2b5aa76745
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675513"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Boekingsrekeningen voor afboeking van vaste activa

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u grootboekboekingsrekeningen als u activa afboekt.

Als u grootboekboekingsrekeningen wilt instellen die moeten worden gebruikt wanneer u een activum afboekt, selecteert u **Verkoop -afstoting** en **Afstoting - uitval** op het sneltabblad **Grootboekrekeningen** op de pagina **Boekingsprofielen vaste activa**.

Voor beide transactietypen (afstoten van een activum door verkoop of uitval), wordt de grootboekrekening gecrediteerd voor de afboekwaarde van het vaste activum. Het debetbedrag wordt naar een tegenrekening geboekt, bijvoorbeeld een bankrekening. Als een vast activum aan een klant wordt verkocht, wordt de klantrekening in plaats van de tegenrekening gebruikt. Zie [Een vast activum als uitval afboeken](dispose-of-a-fixed-asset-as-scrap.md) voor meer informatie.

Klik op **Afstoting** en klik vervolgens op **Verkoop** of **Uitval** en stel vervolgens gedetailleerde rekeningen in om de nettoboekwaarde van het vaste activum om te keren. U kunt ook informatie invoeren in de velden **Waarde boeken** en **Op basis van verkoopwaarde** op de pagina **Afstotingsparameters**. 

Door de afboekingstransactie voor een activum in een groep met lage waarden, wordt de nettoboekwaarde van de groep met lage waarden alleen verminderd met het afgeboekte bedrag. Wanneer de verkoop van een activum echter de nettoboekwaarde van de groep met lage waarden overschrijdt, wordt de nettoboekwaarde verlaagd tot nul.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

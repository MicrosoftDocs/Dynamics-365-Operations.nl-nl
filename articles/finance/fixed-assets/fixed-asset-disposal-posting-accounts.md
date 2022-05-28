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
ms.reviewer: kfend
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8501bbb0fc47fb52e100d9086054db4831dae178
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720246"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Boekingsrekeningen voor afboeking van vaste activa

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u grootboekboekingsrekeningen als u activa afboekt.

Als u grootboekboekingsrekeningen wilt instellen die moeten worden gebruikt wanneer u een activum afboekt, selecteert u **Verkoop -afstoting** en **Afstoting - uitval** op het sneltabblad **Grootboekrekeningen** op de pagina **Boekingsprofielen vaste activa**.

Voor beide transactietypen (afstoten van een activum door verkoop of uitval), wordt de grootboekrekening gecrediteerd voor de afboekwaarde van het vaste activum. Het debetbedrag wordt naar een tegenrekening geboekt, bijvoorbeeld een bankrekening. Als een vast activum aan een klant wordt verkocht, wordt de klantrekening in plaats van de tegenrekening gebruikt. Zie [Een vast activum als uitval afboeken](dispose-of-a-fixed-asset-as-scrap.md) voor meer informatie.

Klik op **Afstoting** en klik vervolgens op **Verkoop** of **Uitval** en stel vervolgens gedetailleerde rekeningen in om de nettoboekwaarde van het vaste activum om te keren. U kunt ook informatie invoeren in de velden **Waarde boeken** en **Op basis van verkoopwaarde** op de pagina **Afstotingsparameters**. 

Door de afboekingstransactie voor een activum in een groep met lage waarden, wordt de nettoboekwaarde van de groep met lage waarden alleen verminderd met het afgeboekte bedrag. Wanneer de verkoop van een activum echter de nettoboekwaarde van de groep met lage waarden overschrijdt, wordt de nettoboekwaarde verlaagd tot nul.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

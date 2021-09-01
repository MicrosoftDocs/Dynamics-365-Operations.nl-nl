---
title: Een artikel kan geen stuklijst of formule hebben
description: Wanneer u een order probeert te valideren, wordt er tijdens het valideren van het artikel een foutbericht weergegeven. In die formule staat dat het artikel geen stuklijst of formule mag hebben.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730101"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Een artikel kan geen stuklijst of formule hebben

Foutcode: PRO2614

## <a name="symptoms"></a>Symptomen

Wanneer u een order probeert te valideren, wordt tijdens het valideren van het artikel het volgende foutbericht weergegeven:

> Artikel kan geen stuklijst of formule hebben

## <a name="resolution"></a>Oplossing

Artikelen met een stuklijst of formule moeten van het type *Planningsartikel*, *Stuklijst* of *formule* zijn. Als u het type van een artikel wilt wijzigen, volgt u deze stappen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het relevante product.
1. Op het sneltabblad **Technicus** stelt u het veld **Productietype** in op *Planningsartikel*, *Stuklijst* of *formule*.

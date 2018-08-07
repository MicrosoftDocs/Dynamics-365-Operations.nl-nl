---
title: Evenwichtige journalen voor interunit-boekhouding
description: "Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina."
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5b1d788ebd5617a1d3f1c8ca36f5ae3c29b534c5
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>Evenwichtige journalen voor interunit-boekhouding

[!include [banner](../includes/banner.md)]

Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina. 

Als boekingen niet in evenwicht zijn op het niveau van de financiële dimensiewaarden, worden automatisch extra boekingen gemaakt om het journaal automatisch in evenwicht te brengen. Deze boekingen gebruiken de boekingstypen **Inter-unit - debet** en **Inter-unit - credit** op de pagina **Rekeningen voor automatische transacties** om de hoofdrekening te bepalen. Bijvoorbeeld, Bedrijfseenheid, het tweede segment van de grootboekrekening, wordt geselecteerd als de financiële tegendimensie en de volgende boekingsregels staan op het punt om te worden gemaakt.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

In dit geval worden de volgende saldi gedefinieerd:

-   Voor Bedrijfseenheid MSP = 100,00 CR
-   Voor Bedrijfseenheid MSP = 100,00 DR

Daarom worden de volgende posten automatisch gemaakt om het journaal op het niveau van de financiële dimensiewaarden in evenwicht te brengen.

|                                   |           |
|-----------------------------------|-----------|
| (Inter-unit debet) – MSP – OU\_256 | 100,00 DR |
| (Inter-unit credit) – NY – OU\_249 | 100,00 CR |







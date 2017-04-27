---
title: Evenwichtige journalen voor interunit-boekhouding
description: "Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8b6fda79222905b0df211a0b944aca9e4dc76850
ms.lasthandoff: 03/31/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>Evenwichtige journalen voor interunit-boekhouding

[!include[banner](../includes/banner.md)]


Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina. 

Als boekingen niet in evenwicht zijn op het niveau van de financiële dimensiewaarden, worden automatisch extra boekingen gemaakt om het journaal automatisch in evenwicht te brengen. Deze boekingen gebruiken de boekingstypen **Inter-unit - debet** en** Inter-unit - credit** op de pagina **Rekeningen voor automatische transacties** om de hoofdrekening te bepalen. Bijvoorbeeld, Vestiging, het tweede segment van de grootboekrekening, wordt geselecteerd als de financiële tegendimensie en de volgende boekingsregels staan op het punt om te worden gemaakt.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

In dit geval worden de volgende saldi gedefinieerd:

-   Voor Vestiging MSP = 100,00 CR
-   Voor Vestiging NY = 100,00 DR

Daarom worden de volgende posten automatisch gemaakt om het journaal op het niveau van de financiële dimensiewaarden in evenwicht te brengen.

|                                   |           |
|-----------------------------------|-----------|
| (Inter-unit debet) – MSP – OU\_256 | 100,00 DR |
| (Inter-unit credit) – NY – OU\_249 | 100,00 CR |







---
title: Evenwichtige journalen voor interunit-boekhouding
description: Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a926adcc631ec286f37796713466eb0144494c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818387"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Evenwichtige journalen voor interunit-boekhouding

[!include [banner](../includes/banner.md)]

Dit artikel laat zien hoe een journaal automatisch wordt gesaldeerd wanneer een financiële tegendimensie wordt geselecteerd op de Grootboekpagina. 

Als boekingen niet in evenwicht zijn op het niveau van de financiële dimensiewaarden, worden automatisch extra boekingen gemaakt om het journaal automatisch in evenwicht te brengen. Deze boekingen gebruiken de boekingstypen **Inter-unit - debet** en **Inter-unit - credit** op de pagina **Rekeningen voor automatische transacties** om de hoofdrekening te bepalen. Bijvoorbeeld, Bedrijfseenheid, het tweede segment van de grootboekrekening, wordt geselecteerd als de financiële tegendimensie en de volgende boekingsregels staan op het punt om te worden gemaakt.

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

In dit geval worden de volgende saldi gedefinieerd:

-   Voor Bedrijfseenheid MSP = 100,00 CR
-   Voor Bedrijfseenheid MSP = 100,00 DR

Daarom worden de volgende posten automatisch gemaakt om het journaal op het niveau van de financiële dimensiewaarden in evenwicht te brengen.

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| (Inter-unit debet) – MSP – OU\_256 | 100,00 DR |
| (Inter-unit credit) – NY – OU\_249 | 100,00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
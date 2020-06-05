---
title: Auditfile (XML Auditfile Financieel, XAF)
description: In dit onderwerp wordt uitgelegd hoe u het auditfile (XML Auditfile Financieel, XAF) voor rechtspersonen kunt instellen en genereren in Nederland.
author: liza-golub
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxEvatParameters_NL
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Finance
ms.search.region: Netherlands
ms.author: elgolu
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dfaa9f4b59e27629bc0ec022100deac05cd34d7
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346318"
---
# <a name="audit-file-xml-auditfile-financieel-xaf"></a>Auditfile (XML Auditfile Financieel, XAF)

[!include [banner](../../includes/banner.md)]

Deze functionaliteit is beschikbaar voor rechtspersonen waarvan het primaire adres in Nederland is.

In dit onderwerp wordt uitgelegd hoe u ER-configuraties voor het auditfile importeert en hoe u het auditfile (XML Auditfile Financieel, XAF) voor rechtspersonen in Nederland genereert.

## <a name="import-and-set-up-er-configurations"></a>ER-configuraties importeren en instellen

Als u Microsoft Dynamics 365 Finance wilt voorbereiden op het genereren van het auditfile, moet u de volgende ER-configuraties importeren.

| Nummer | Naam van ER-configuratie         | Type                                 | Omschrijving |
|--------|-------------------------------|--------------------------------------|-------------|
| 1      | Model van auditfile              | Model                                | Een model voor het auditfile voor Nederland. |
| 2      | Auditfile (NL)               | Indeling (exporteren)                   | ER-indeling voor XML Auditfile Financieel, XAF. |

## <a name="generate-the-audit-file"></a>Het auditfile genereren

Met de stappen in deze procedure wordt uitgelegd hoe u het auditfile (XML Auditfile Financieel, XAF) gebruikt.

1. Ga naar **Grootboek** > **Periodieke taken** > **Auditfile**.
2. Voer een datum in het veld **Begindatum** in. Typ of selecteer bijvoorbeeld 01/11/2020.
3. Voer een datum in het veld **Einddatum** in. Typ of selecteer bijvoorbeeld 30/11/2020.
4. Typ of selecteer **Auditfile (NL)** een waarde in het veld **Indelingstoewijzing**.
5. Selecteer **OK**.

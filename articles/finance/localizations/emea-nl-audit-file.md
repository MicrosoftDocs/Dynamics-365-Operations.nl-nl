---
title: Auditfile (XML Auditfile Financieel, XAF)
description: In dit onderwerp wordt uitgelegd hoe u de auditfile voor rechtspersonen in Nederland kunt instellen en genereren.
author: liza-golub
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxEvatParameters_NL
audience: Application User
ms.reviewer: kfend
ms.search.region: Netherlands
ms.author: elgolu
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32aa934e8ed997795081b6addba74a275e44e11c
ms.sourcegitcommit: 66dd0268aea4e1353f7efd74e226de24fa56f56c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/16/2021
ms.locfileid: "5612917"
---
# <a name="audit-file-xml-auditfile-financieel-xaf"></a>Auditfile (XML Auditfile Financieel, XAF)

[!include [banner](../../includes/banner.md)]

Deze functionaliteit is beschikbaar voor rechtspersonen waarvan het primaire adres in Nederland is.

In dit onderwerp wordt uitgelegd hoe u ER-configuraties voor de auditfile importeert en vervolgens de auditfile voor rechtspersonen in Nederland genereert.

## <a name="import-and-set-up-er-configurations"></a>ER-configuraties importeren en instellen

Als u Microsoft Dynamics 365 Finance wilt voorbereiden op het genereren van het auditfile, moet u de volgende ER-configuraties importeren.

| Nummer | Naam van ER-configuratie         | Type                                 | Omschrijving |
|--------|-------------------------------|--------------------------------------|-------------|
| 1      | Model van auditfile              | Model                                | Een model voor het auditfile voor Nederland. |
| 2      | Auditfile (NL)               | Indeling (exporteren)                   | ER-indeling voor XML Auditfile Financieel, XAF. |

## <a name="generate-the-audit-file"></a>Het auditfile genereren

Met de stappen in deze procedure wordt uitgelegd hoe u de auditfile gebruikt.

1. Ga naar **Grootboek** > **Periodieke taken** > **Auditfile**.
2. Voer een datum in het veld **Begindatum** in. 
3. Voer een datum in het veld **Einddatum** in. 
4. Typ **Auditfile (NL)** in het veld **Indelingstoewijzing**.
5. Selecteer **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
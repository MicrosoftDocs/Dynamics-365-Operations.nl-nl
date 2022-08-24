---
title: Auditfile (XML Auditfile Financieel, XAF)
description: In dit artikel wordt uitgelegd hoe u de auditfile voor rechtspersonen in Nederland kunt instellen en genereren.
author: AdamTrukawka
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Netherlands
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: TaxEvatParameters_NL
ms.openlocfilehash: 6168be17a1447d2e243e90cb9e92c073684968fc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282407"
---
# <a name="audit-file-xml-auditfile-financieel-xaf"></a>Auditfile (XML Auditfile Financieel, XAF)

[!include [banner](../../includes/banner.md)]

Deze functionaliteit is beschikbaar voor rechtspersonen waarvan het primaire adres in Nederland is.

In dit artikel wordt uitgelegd hoe u ER-configuraties voor de auditfile importeert en vervolgens de auditfile voor rechtspersonen in Nederland genereert.

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

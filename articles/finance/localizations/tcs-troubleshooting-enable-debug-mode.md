---
title: Foutopsporingsmodus inschakelen in de service voor belastingberekening
description: In dit artikel wordt uitgelegd hoe u de foutopsporingsmodus inschakelt in de belastingberekeningsservice om problemen te onderzoeken.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 38ef8c51d52de6b8f748330d0697e860d75233bf
ms.sourcegitcommit: 43cf54d057eccd07a71bb48e2fcf858d043a9669
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/04/2022
ms.locfileid: "9620893"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>Foutopsporingsmodus inschakelen in de service voor belastingberekening

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de foutopsporingsmodus inschakelt in de belastingberekeningsservice om problemen te onderzoeken.

1. Voeg aan de URL van de Application Object Server (AOS) de tekt **&debug=vs%2CconfirmExit&** toe en vernieuw de pagina.
2. Als u **btw** selecteert om de btw te berekenen, wordt een tekstbestand met de naam **TaxServiceTroubleshootingLog.txt** vastgelegd op de server **C:\AXWeb_SMBShare\temporary-file\\{%session%}\\**. Het bestand **TaxServiceTroubleshootingLog.txt** bevat **TaxableDocument** en de berekeningsparameter. Deze resultaten worden geretourneerd door de belastingservice en uitzonderingsinformatie voor probleemoplossing.

## <a name="sample"></a>Voorbeeld

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

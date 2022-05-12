---
title: Kan geen overeenkomend resultaat vinden
description: In dit onderwerp wordt uitgelegd hoe u het probleem met de fout "Kan geen overeenkomend resultaat vinden" in de service voor belastingberekening oplost.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: c1a343b0b74645d40b0a2582749968cc0a56afd7
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645391"
---
# <a name="no-matching-result-could-be-found"></a>Kan geen overeenkomend resultaat vinden

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de probleemoplossingsstappen toegelicht die u kunt uitvoeren als u een fout "Kan geen overeenkomend resultaat vinden" in de service voor belastingberekening krijgt.

## <a name="symptom"></a>Symptoom

Het volgende foutbericht wordt weergegeven: "Koptekst/regels - 1, Belastinggroep, kan geen overeenkomend resultaat vinden."

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Oorzaak

Het probleem treedt op wanneer de functieconfiguratie in de Regulatory Configuration Service (RCS) onjuist is.

## <a name="troubleshoot"></a>Problemen oplossen

1. Download het probleemoplossingsbestand. Meer informatie vindt u in [Foutopsporingsmodus voor probleemoplossing inschakelen](tcs-troubleshooting-enable-debug-mode.md).
2. Vergelijk de invoer van de belastingserviceberekening met de functieconfiguratie om het probleem met de instellingen op te lossen.

    In het volgende voorbeeld ziet u de invoer voor de belastingserviceberekening.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    In de volgende tabel wordt de toepasbaarheid van de belastinggroep in RCS vermeld.

    | Header.Bedrijfsproces | Lines.Bedrijfseenheid | Header.Verzenden vanaf postcode | Btw-groep |
    |-------------------------|---------------------|---------------------------|-----------|
    | Journaal                 |                     |                           | Groep A   |
    | Sales                   |                     | 30160                     | Groep B   |

    Volgens de invoer van de belastingserviceberekening is de waarde voor **Bedrijfsproces** in de koptekst **Verkoop**, en de waarde voor **Verzenden vanaf postcode** in de koptekst is **30159**. Deze invoer is gebaseerd op de instelling van toepasbaarheidsregels in RCS. Omdat er geen overeenkomende regel is, treedt de fout op.

    > [!NOTE]
    > Als de waarde in de toepasbaarheidsregel leeg is, is de regel van toepassing op elke waarde.

## <a name="mitigation"></a>Risicobeperking

Volg deze stappen om de fout op te lossen.

1. Ga in RCS naar **Globaliseringsfuncties** \> **Belastingberekening**.
2. Maak een nieuwe versie van de functie.
3. Voeg een regel toe voor de bijbehorende informatie.

    | Header.Bedrijfsproces | Lines.Bedrijfseenheid | Header.Verzenden vanaf postcode| Btw-groep |
    |-------------------------|---------------------|--------------------------|-----------|
    | Journaal                 |                     |                          | Groep A   |
    | Sales                   |                     | 30160                    | Groep B   |
    | Sales                   |                     | 30159                    | Groep B   |

4. Publiceer de versie van de instelfunctie.
5. Ga in Microsoft Dynamics 365 Finance naar **Belastingen** \> **Instellingen** \> **Belastingconfiguratie** \> **Parameters voor belastingberekening** en selecteer de nieuwe versie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

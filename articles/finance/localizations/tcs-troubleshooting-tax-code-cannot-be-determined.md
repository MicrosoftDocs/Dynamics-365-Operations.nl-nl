---
title: Belastingcode kan niet worden bepaald
description: In dit artikel wordt uitgelegd hoe u de fout "Belastingcode kan niet worden bepaald" van de Belastingberekeningsservice oplost.
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
ms.openlocfilehash: 6a74724de38cf362900277ab9addc8e6894f7689
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877854"
---
# <a name="tax-code-cannot-be-determined"></a>Belastingcode kan niet worden bepaald

[!include [banner](../includes/banner.md)]

In dit artikel worden de probleemoplossingsstappen toegelicht die u kunt uitvoeren als u een fout "Belastingcode kan niet worden bepaald" in de service voor belastingberekening krijgt.

## <a name="symptom"></a>Symptoom

Het volgende foutbericht wordt weergegeven: "Koptekst/regels - 1, Belastingcode kan niet worden bepaald." U kunt de fout ook vinden in het probleemoplossingsbestand, zoals getoond in het volgende voorbeeld. Meer informatie vindt u in [Foutopsporingsmodus voor probleemoplossing inschakelen](tcs-troubleshooting-enable-debug-mode.md).

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
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
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

Het probleem treedt waarschijnlijk op omdat de belastinggroep en de belastinggroep van het artikel niet overlappen.

## <a name="troubleshoot"></a>Problemen oplossen

Volg deze stappen om het probleem op te lossen.

1. Controleer in het probleemoplossingsbestand of de belastinggroep en de artikelbelastinggroep zijn bepaald. Als de waarden voor **Belastinggroep** en **Artikelbelastinggroep** leeg zijn, zijn de belastinggroep en de belastinggroep voor het artikel nog niet bepaald. Als deze zijn bepaald, zijn de resultaten mogelijk onjuist.

    Hier volgt een voorbeeld van een probleemoplossingsbestand.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
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

2. Controleer of de optie **Btw-overschrijving** op het tabblad **Instellingen** van de verkooporderregeldetails is ingeschakeld.

    - Als deze is ingeschakeld, worden belastingcodes bepaald door de waarden voor **Belastinggroep** en de **Artikelbelastinggroep** die u op de transactieregel invoert. Controleer of deze waarden correct zijn ingevoerd.
    - Als deze niet is ingeschakeld, controleert u of correcte waarden zijn ingesteld voor de velden **Toepasbaarheid van belastinggroep** en **Artikelbelastinggroep**. Meer informatie vindt u in [Kan geen overeenkomend resultaat vinden](tcs-troubleshooting-no-matching-result.md).

3. Als de belastinggroep en de artikelbelastinggroep correct zijn bepaald, moet u bepalen of deze groepen elkaar overlappen.

    1. Ga in RCS naar **Belastingfuncties** \> **Belastingcodes en -groepen** \> **Belastinggroep**.

        | Line.Belastinggroep | Belastingcodes |
        |----------------|-----------|
        | Groep A        | V         |

    2. Ga naar **Belastingfuncties** \> **Belastingcodes en -groepen** \> **Artikelbelastinggroep**.

        | Line.Artikelbelastinggroep | Belastingcodes |
        |---------------------|-----------|
        | Groep B             | B         |

    Als de belastinggroep en de artikelbelastinggroep elkaar niet overlappen, wordt de belastingcode niet bepaald.

## <a name="mitigation"></a>Risicobeperking

1. Doorloop alle stappen in het gedeelte [Probleemoplossing](#troubleshoot) van dit artikel en stel de configuratie in zoals vereist. Als de belastinggroep en de artikelbelastinggroep niet juist zijn bepaald, raadpleeg dan [Kan geen overeenkomend resultaat vinden](tcs-troubleshooting-no-matching-result.md).
2. Als er geen overlap is voor de belastinggroep en de artikelbelastinggroep, maakt u een nieuwe functieversie in RCS en herstelt u de configuratie.

    - Ga naar **Belastingfuncties** \> **Belastingcodes en -groepen** > **Artikelbelastinggroep**.

        | Line.Artikelbelastinggroep | Btw-codes |
        |---------------------|-----------|
        | Groep B             | A;B       |

    De belastingcode wordt bepaald als **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

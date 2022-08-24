---
title: De belastinginstellingen van Service voor belastingberekening synchroniseren met Dynamics 365 Finance
description: In dit artikel wordt uitgelegd hoe u hoofdgegevens van de Service voor belastingberekening synchroniseert met Microsoft Dynamics 365 Finance.
author: EricWangChen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.custom: intro-internal
ms.search.form: TaxIntegration, TaxServiceParameters
ms.openlocfilehash: 315f2b27a64906ca0fc404d704d0b170dbfa48c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283848"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>De belastinginstellingen van Service voor belastingberekening synchroniseren met Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u hoofdgegevens van de Service voor belastingberekening synchroniseert met Microsoft Dynamics 365 Finance.

Nadat u de vereiste instellingsstappen in [Aan de slag met belastingberekening](global-get-started-with-tax-calculation-service.md) hebt voltooid, worden de volgende instellingsgegevens uit de Service voor belastingberekening automatisch gesynchroniseerd naar Finance.

## <a name="sales-tax-code"></a>Btw-code

| Service voor belastingberekening           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Belastingcode                          | Btw-code                      |
| Description                       | Name                                |
| Gebruikersinvoer                        | Vereffeningsperiode                   |
| Gebruikersinvoer                        | Groep boekingen in grootboek                |
| Gebruikersinvoer                        | Btw-valuta                  |
| Er wordt een negatief belastingtarief geconfigureerd | Negatief btw-percentage toestaan |

## <a name="tax-value"></a>Belastingbedrag

| Service voor belastingberekening | Finance                   |
| ----------------------- | ------------------------- |
| Van transactiedatum   | Begindatum                 |
| T/m transactiedatum     | Einddatum                   |
| Minimumbedrag          | Ondergrens             |
| Maximumbedrag          | Bovengrens             |
| Belastingtarief                | Waarde                     |
| Niet-aftrekbaar tarief     | Niet-aftrekbaar percentage |

## <a name="tax-limits"></a>Belastinglimieten

| Service voor belastingberekening | Finance           |
| ----------------------- | ----------------- |
| Van transactiedatum   | Begindatum         |
| T/m transactiedatum     | Einddatum           |
| Minimaal belastingbedrag      | Minimale btw |
| Maximaal belastingbedrag      | Maximale btw |

## <a name="sales-tax-group"></a>Btw-groep

| Service voor belastingberekening                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Belastinggroep                                       | Btw-groep                            |
| Belastingcodes onder deze belastinggroep                  | Btw-codes onder deze btw-groep |
| De belastingcode is gemarkeerd als **Vrijgesteld**         | Vrijstelling                                     |
| De belastingcode is gemarkeerd als **Vrijgesteld**         | Vrijstellingscode                                |
| De belastingcode is gemarkeerd als **Terugboeking**. | Terugboeking                             |
| De belastingcode is gemarkeerd als **Gebruiksbelasting**        | Gebruiksbelasting                                    |

## <a name="item-sales-tax-group"></a>Btw-groep voor artikel

| Service voor belastingberekening             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Artikelbelastinggroep                      | Btw-groep voor artikel                            |
| Belastingcodes onder deze artikelbelastinggroep | Btw-codes onder deze btw-groep voor artikelen |

Ga na de synchronisatie verder met het onderhouden van de resterende parameters in Finance voor boekings- en rapportagedoeleinden.

> [!NOTE]
> Synchronisatie van de belastinginstellingen uit Finance met de Service voor belastingberekening wordt niet ondersteund. Maak voor een bestaande Finance-omgeving eerst de belastinginstellingen in de Service voor belastingberekening. Synchroniseer vervolgens de instellingsgegevens weer met de Finance-omgeving.

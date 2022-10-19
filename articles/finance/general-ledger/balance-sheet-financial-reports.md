---
title: Financiële rapporten balans
description: In dit artikel worden de standaardrapporten voor balansen beschreven. Hierin worden ook de bouwstenen beschreven die aan deze rapporten zijn gekoppeld.
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643818"
---
# <a name="balance-sheet-financial-reports"></a>Financiële rapporten balans

[!include [banner](../includes/banner.md)]

In dit artikel worden de standaardrapporten voor balansen beschreven. Hierin worden ook de bouwstenen beschreven die aan deze rapporten zijn gekoppeld. 

## <a name="default-balance-sheet-reports"></a>Standaardbalansrapporten

Er zijn twee standaardbalansrapporten. In één rapport zijn de secties gestapeld. In het andere rapport worden de secties naast elkaar weergegeven.

| Standaardrapport                       | Functie                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| Balans – Standaard              | Bevat een weergave van de financiële positie van de organisatie voor het jaar.                    |
| Balans en Inkomensoverzicht naast elkaar - Standaard | Bevat een weergave naast elkaar van de financiële positie van de organisatie voor het jaar. |

## <a name="building-blocks"></a>Bouwstenen
In de financiële rapporten van de balans worden de volgende bouwstenen gebruikt.

| Standaardrapport                       | Rijdefinitie                       | Kolomdefinitie             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Balans: standaard              | Balans: standaard              | Jaar tot heden en afwijking: standaard    |
| Balans en Inkomensoverzicht naast elkaar - Standaard | Balans en Inkomensoverzicht naast elkaar - Standaard | Kolom Jaar tot heden: standaard |

### <a name="row-definition"></a>Rijdefinitie

De rijdefinities voor beide balansrapporten bevatten secties voor elk onderdeel van een traditionele balans. Het rapport waarin secties naast elkaar worden weergegeven, bevat een kolomeinde, zodat de passiva en het eigen vermogen van de eigenaar naast activa worden weergegeven. De dimensie Categorie van hoofdrekening wordt gebruikt om beide rijdefinities te maken. Zo kan iedereen de rapporten genereren zonder wijzigingen te hoeven aanbrengen.

### <a name="column-definition"></a>Kolomdefinitie

De kolomdefinities bevatten verschillende typen kolommen om verschillende detailniveaus en financiële gegevens te verschaffen.

-   **Jaar tot heden en afwijking: standaardkolomtypen:**
    -   **DESC**: de omschrijving van de rijdefinitie
    -   **FD**: financiële gegevens voor jaar tot heden voor het huidige jaar
    -   **FD**: financiële gegevens voor jaar tot heden voor het afgelopen jaar
    -   **CALC**: de afwijking na aftrek van afgelopen jaar van dit jaar

<!-- -->

-   **Kolom Jaar tot heden: standaard:**
    -   **DESC**: de omschrijving van de rijdefinitie
    -   **FD**: financiële gegevens voor jaar tot heden voor het huidige jaar



## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Financiële rapportage](financial-reporting-getting-started.md)

[Financiële rapporten weergeven](view-financial-reports.md)

[Blog met financiële rapportage van Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

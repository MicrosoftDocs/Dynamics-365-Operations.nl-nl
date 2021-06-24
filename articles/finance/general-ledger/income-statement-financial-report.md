---
title: Financieel rapport inkomensoverzicht
description: In dit artikel wordt het standaardrapport voor inkomensoverzichten beschreven. In dit artikel worden ook de bouwstenen beschreven die aan dit rapport zijn gekoppeld.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ab5e7a2675705cc2265b7f894d9b12d4465aea1
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187815"
---
# <a name="income-statement-financial-report"></a>Financieel rapport inkomensoverzicht

[!include [banner](../includes/banner.md)]

In dit artikel wordt het standaardrapport voor inkomensoverzichten beschreven. In dit artikel worden ook de bouwstenen beschreven die aan dit rapport zijn gekoppeld. 

## <a name="default-income-statement-report"></a>Standaardrapport inkomensoverzicht

| Standaardrapport             | Functie                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Inkomensoverzicht – Standaard | Biedt een weergave van de winstgevendheid van de organisatie voor de huidige periode en ook voor het jaar tot heden. |

## <a name="building-blocks"></a>Bouwstenen
In het financiële rapport van het inkomensoverzicht worden de volgende bouwstenen gebruikt.

| Standaardrapport             | Rijdefinitie                     | Kolomdefinitie          |
|----------------------------|------------------------------------|----------------------------|
| Inkomensoverzicht: standaard | Samengevat inkomensoverzicht: standaard | Periodiek en jaar tot heden: standaard |

### <a name="row-definition"></a>Rijdefinitie

De rijdefinitie, Samengevat inkomensoverzicht: standaard, bevat een sectie voor elk onderdeel van een traditioneel inkomensoverzicht. De dimensie Categorie van hoofdrekening wordt gebruikt om deze rijdefinitie te maken. Zo kan iedereen het rapport genereren zonder wijzigingen te hoeven aanbrengen.

### <a name="column-definition"></a>Kolomdefinitie

De kolomdefinities bevatten verschillende typen kolommen om verschillende detailniveaus en financiële gegevens te verschaffen.

-   **Periodiek en jaar tot heden: standaardkolomtypen:**
    -   **DESC**: de omschrijving van de rijdefinitie
    -   **FD**: financiële gegevens voor de huidige periode
    -   **FD**: financiële gegevens voor jaar tot heden



## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Financiële rapportage](financial-reporting-getting-started.md)

[Financiële rapporten weergeven](view-financial-reports.md)

[Blog met financiële rapportage van Dynamics](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
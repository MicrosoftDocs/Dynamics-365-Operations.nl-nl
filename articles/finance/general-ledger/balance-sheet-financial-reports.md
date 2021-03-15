---
title: Financiële rapporten balans
description: In dit artikel worden de standaardrapporten voor balansen beschreven. Hierin worden ook de bouwstenen beschreven die aan deze rapporten zijn gekoppeld.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d249172c2bc4241a47502b57f2ac20b29111eeba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985007"
---
# <a name="balance-sheet-financial-reports"></a>Financiële rapporten balans

[!include [banner](../includes/banner.md)]

In dit artikel worden de standaardrapporten voor balansen beschreven. Hierin worden ook de bouwstenen beschreven die aan deze rapporten zijn gekoppeld. 

<a name="default-balance-sheet-reports"></a>Standaardbalansrapporten
-----------------------------

Er zijn twee standaardbalansrapporten. In één rapport zijn de secties gestapeld. In het andere rapport worden de secties naast elkaar weergegeven.

| Standaardrapport                       | Functie                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Balans – Standaard              | Bevat een weergave van de financiële positie van de organisatie voor het jaar.                                                                 |
| Balans naast elkaar - Standaard | Bevat een weergave van de financiële positie van de organisatie voor het jaar. Activa en passiva en het eigen vermogen van de aandeelhouder worden naast elkaar weergegeven. |

## <a name="building-blocks"></a>Bouwstenen
In de financiële rapporten van de balans worden de volgende bouwstenen gebruikt.

| Standaardrapport                       | Rijdefinitie                       | Kolomdefinitie             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Balans: standaard              | Balans: standaard              | Jaar tot heden en afwijking: standaard    |
| Balans naast elkaar - Standaard | Balans naast elkaar - Standaard | Kolom Jaar tot heden: standaard |

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



<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht van Financiële rapportage](financial-reporting-getting-started.md)

[Financiële rapporten weergeven](view-financial-reports.md)

[Blog met financiële rapportage van Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
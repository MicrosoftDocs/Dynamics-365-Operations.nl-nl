---
title: "Financiële rapporten balans"
description: In dit artikel beschrijft de standaardrapporten voor balansen. Hierin worden ook de bouwstenen die aan deze rapporten gekoppeld zijn.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 664d32c2bfecb50e24fd48a66ab5b34cef6c09a3
ms.lasthandoff: 03/31/2017


---

# <a name="balance-sheet-financial-reports"></a>Financiële rapporten balans

In dit artikel beschrijft de standaardrapporten voor balansen. Hierin worden ook de bouwstenen die aan deze rapporten gekoppeld zijn. 

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

 

<a name="see-also"></a>Zie ook
--------

[Financial reporting](financial-reporting-getting-started.md)

[View financial reports](view-financial-reports.md)

[Dynamics-Blog voor financiële rapportage](http://blogs.msdn.com/b/dynamics_financial_reporting/)



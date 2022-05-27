---
title: Beschikbare budgetfondsen
description: Dit onderwerp introduceert de functie voor beschikbare budgetfondsen en biedt informatie die u kan helpen bij het configureren van budgetbeheer om het beheer van de financiële middelen van uw organisatie te optimaliseren.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 1e7b2bf7ef7bd1bca6db27371f87dfddcdceef89
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710244"
---
# <a name="budget-funds-available"></a>Beschikbare budgetfondsen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dit onderwerp introduceert de functie voor beschikbare budgetfondsen en biedt informatie die u kan helpen bij het configureren van budgetbeheer om het beheer van de financiële middelen van uw organisatie te optimaliseren.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Verbeterde berekeningsfunctie voor beschikbare budgetfondsen

Met de functie **Alleen bedragen bijhouden in de berekeningsfunctie voor beschikbare budgetfondsen** kunt u de onderliggende budgetbeheertabellen voor documenttypen en -staten bijhouden op basis van de instellingen op de pagina **Parameters voor budgetbeheer definiëren**.

Voor sommige configuratieopties voor budgetbeheer moeten specifieke instellingen worden geconfigureerd om de functie correct te kunnen gebruiken. Deze opties worden in- of uitgeschakeld op het tabblad **Beschikbare budgetfondsen** van de pagina **Parameters voor budgetbeheer definiëren**. De volgende tabel toont de instellingen die vereist zijn voor de functie voor beschikbare budgetfondsen.

| Als deze optie is geselecteerd | Moet deze optie ook zijn geselecteerd |
| ------------------------- | -------------------------------- |
| Budgetreserveringen voor voorvorderingen | Budgetreserveringen voor vorderingen *en* werkelijke uitgaven |
| Budgetreserveringen voor vorderingen | Werkelijke uitgaven |
| Budgetreserveringen voor vorderingen met documenten van het type Opdracht tot inkoop | Budgetreserveringen voor voorvorderingen |

Deze functie is alleen van invloed op nieuwe documenten. Bedragen voor bestaande documenten worden bijgehouden en weergegeven wanneer statistieken voor budgetbeheer worden opgevraagd tot een instelling voor beschikbare budgetfondsen wordt gewijzigd en de nieuwe budgetbeheerconfiguratie is geactiveerd. Op dat moment worden budgettraceringsgegevens verwijderd voor documenten die uit de berekening voor beschikbare budgetfondsen zijn verwijderd.

We raden u aan de optie **Niet-geboekte werkelijke uitgaven** uitgeschakeld te laten. Als u deze optie selecteert, wordt een tijdrovende berekening van budgetbeheer uitgevoerd op niet-geboekte documenten, zoals leveranciersfacturen die in behandeling zijn.

---
title: Tijd toewijzen aan taken in een takenbundel
description: In Productie-uitvoering kunt u taken bundelen. U kunt meerdere taken tegelijk starten op de pagina Taaklijst.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a5204288ce3eaabb605f136ea788d235f408f349
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Tijd toewijzen aan taken in een takenbundel

[!include[banner](../includes/banner.md)]


In Productie-uitvoering kunt u taken bundelen. U kunt meerdere taken tegelijk starten op de pagina Taaklijst.

Als u taken bundelt, moet u definiëren hoe de totale geregistreerde tijd voor de taken moet worden toegewezen aan elke taak. U definieert de toewijzing door een van de volgende opties te selecteren in het veld **Bundeltype** op de pagina **Toewijzingssleutels**:

-   **Raming** – De tijd wordt over de taken verdeeld op basis van de geraamde tijd voor de taken.
-   **Taken** – De tijd wordt verdeeld op basis van het totale aantal gebundelde taken en de hoeveelheid tijd die is besteed aan het voltooien van alle taken.
-   **Nettotijd** – De tijd wordt evenredig verdeeld over de taken die op een gegeven moment in de bundel zijn opgenomen.
-   **Realtime** – Werkelijke taaktijd die is toegewezen. De kosten kunnen worden berekend op basis van de daadwerkelijke salariskosten. **Opmerking:** De toewijzingssleutel **Realtime** is alleen beschikbaar als uw bedrijf de salarisfunctie in Tijd en aanwezigheid gebruikt.

De volgende voorbeelden laten de resultaten van de verschillende toewijzingssleutels zien.

## <a name="example-scenario"></a>Voorbeeldscenario
Drie taken in de taakwachtrij moten worden voltooid. U start de eerste taak en vervolgens, terwijl deze wordt uitgevoerd, start u de tweede en de derde taak. Er is dus sprake van een bundel van drie taken. De volgende tabel bevat de geschatte productietijd voor elke taak.

| Taak   | Productietijd |
|-------|-----------------|
| Taak 1 | 1 uur          |
| Taak 2 | 3 uur         |
| Taak 3 | 4 uur         |
| Totaal | 8 uur         |

In de volgende tabel ziet u de werkelijke werkuren die aan elke taak worden besteed.

| Taak    | Begintijd | Eindtijd | Bundeltijd |
|--------|------------|----------|-------------|
| Taak 1  | 09.00      | 11:00:00    | 2 uur     |
| Taak 2  | 10:00:00      | 13:00:00    | 3 uur     |
| Taak 3  | 10:00:00      | 15.00    | 5 uur     |
| Bundel | 09.00      | 15.00    | 6 uur     |

De volgende secties beschrijft de resultaten van de berekende tijd voor elke toewijzingssleutel.

## <a name="estimation-allocation-key"></a>Toewijzingssleutel Raming
De volgende tabel illustreert de formule voor de berekening van de toegewezen tijd. Hier volgt de formule: Tijd per taak = Totale bundeltijd × (Geraamde taaktijd ÷ Totaal geraamde tijd)

| Functie   | Formule           | Toegewezen tijd |
|-------|-------------------|----------------|
| Taak 1 | 6 × (1 ÷ 8) uur | 0,75 uur      |
| Taak 2 | 6 × (3 ÷ 8) uur | 2,25 uur     |
| Taak 3 | 6 × (4 ÷ 8) uur | 3,00 uur     |

## <a name="jobs-allocation-key"></a>Toewijzingssleutel Taken
De volgende tabel illustreert de formule voor de berekening van de toegewezen tijd. Hier volgt de formule: Tijd per taak = Totale bundeltijd ÷ Aantal taken

| Functie   | Formule | Toegewezen tijd |
|-------|---------|----------------|
| Taak 1 | 6 ÷ 3   | 2 uur        |
| Taak 2 | 6 ÷ 3   | 2 uur        |
| Taak 3 | 6 ÷ 3   | 2 uur        |

## <a name="net-time-allocation-key"></a>Toewijzingssleutel Nettotijd
De volgende tabel illustreert de formule voor de berekening van de toegewezen tijd. Hier volgt de formule: Berekende tijd per rapportage = Bundeltijd ÷ Aantal taken

|                              | 09:00–10:00 (1 uur) | 10:00–11:00 (1 uur) | 11:00–13:00 (2 uur) | 13:00–15:00 (2 uur) | Toegewezen tijd |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Het aantal taken in de bundel | 1                    | 3                    | 2                     | 1                     | Niet van toepassing |
| Taak 1                        | 1 ÷ 1 = 1 uur       | 1 ÷ 3 = 0,33 uur    | Niet van toepassing        | Niet van toepassing        | 1,33 uur     |
| Taak 2                        | Niet van toepassing       | 1 ÷ 3 = 0,33 uur    | 2 ÷ 2 = 1 uur        | Niet van toepassing        | 1,33 uur     |
| Taak 3                        | Niet van toepassing       | 1 ÷ 3 = 0,33 uur    | 2 ÷ 2 = 1 uur        | 2 ÷ 1 = 2 uur       | 3,33 uur     |

## <a name="real-time-allocation-key"></a>Toewijzingssleutel Feitelijke tijd
Als u wilt dat de productiekosten worden berekend op basis van de werkelijke kosten, moet u de optie **Kostencategorie** op de pagina **Productieorderstandaarden** uitschakelen. De volgende tabel illustreert de formule voor de berekening van de toegewezen tijd. Hier volgt de formule: Feitelijke tijd per taak = Feitelijke tijd in bundel

| Functie   | Werkelijke tijd |
|-------|-------------|
| Taak 1 | 2 uur     |
| Taak 2 | 3 uur     |
| Taak 3 | 5 uur     |

Stel dat de drie taken door een werknemer worden uitgevoerd voor een uurprijs van EUR 12,00. Bij de tijd die aan de taak wordt gespendeerd, worden geen premies of toeslagen voor overuren toegekend. De werknemer heeft in totaal zes uur aan deze gebundelde taken gewerkt. De salariskosten zijn dan 6 × EUR 12,00 = EUR 72,00. Wanneer u de toewijzing Realtime gebruikt, worden de kosten per uur herberekend met de factor uit de formule voor Nettotijd. De feitelijke tijd die aan elke taak werd gespendeerd, wordt vervolgens overgeboekt, samen met de gecorrigeerde kostprijs per uur. In het voorbeeld werden 6 uren gespendeerd, hoewel 10 uren waren toegewezen. De volgende tabel illustreert de formule voor de berekening van de kosten. Hier volgt de formule: Kosten per uur = (Totale bundeltijd per taak (Nettotijd) ÷ Feitelijke tijd per taak)) × Standaardkostprijs per uur

| Functie   | Berekening van gecorrigeerde kosten per uur | Gecorrigeerde kosten per uur | Toegewezen tijd | Totale kosten taak |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Taak 1 | (1,33 ÷ 2) × EUR 12,00                 | 8,00 USD                | 2 uur        | 16,00 USD         |
| Taak 2 | (1,33 ÷ 3) × EUR 12,00                 | 5,33 USD                | 3 uur        | 16,00 USD         |
| Taak 3 | (3,33 ÷ 5) × EUR 12,00                 | 8,00 USD                | 5 uur        | 40,00 USD         |

De gecorrigeerde kosten per uur en de taaktijd worden geboekt in een productiejournaal. **Opmerking:** Als u de optie **Kostencategorie** op het tabblad **Algemeen** op de pagina **Productieorderstandaarden** selecteert, wordt de werkelijke tijd voor elke taak overgeboekt naar een productiejournaal, waarbij de kosten worden toegepast op de kostencategorie van de specifieke taak.





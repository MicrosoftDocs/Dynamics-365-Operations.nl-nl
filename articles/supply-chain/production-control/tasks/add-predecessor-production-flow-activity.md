---
title: Een voorafgaande taak toevoegen aan een productiestroomactiviteit
description: In een productiestroomversie moeten alle activiteiten worden gerangschikt.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 346dca110fde9ff7600f3e4606529c27289dfc97
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838770"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Een voorafgaande taak toevoegen aan een productiestroomactiviteit

[!include [task guide banner](../../includes/task-guide-banner.md)]

In een productiestroomversie moeten alle activiteiten worden gerangschikt. Een activiteit kan een of meerdere voorafgaande taken of opvolgende taken hebben. 

Deze procedure laat zien hoe u een voorafgaande taak aan een activiteit koppelt. 

Voor deze taak hebt u een productiestroom nodig met de Conceptversie waaraan minimaal twee activiteiten kunnen worden gekoppeld. 

Zie voor meer informatie de whitepaper "Production flows and activities in lean manufacturing".


## <a name="find-the-production-flow-and-version"></a>De productiestroom en versie vinden
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik op Activiteiten.

## <a name="select-an-activity-and-add-a-predecessor"></a>Een activiteit selecteren en een voorafgaande taak toevoegen
1. Zoek en selecteer de gewenste record in de lijst.
2. Klik op Voorafgaande taak toevoegen.
3. Typ of selecteer een waarde in het veld Activiteit.
4. Voer in het veld Cyclusduurverhouding een nummer in.
    * De standaard cyclusduurverhouding van een activiteitrelatie is 1. Hierbij wordt ervan uitgegaan dat beide activiteiten op dezelfde snelheid of takttijd worden uitgevoerd. Als de voorafgaande taak met een hoger tempo (lagere takttijd) wordt uitgevoerd, moet de verhouding lager zijn dan 1. Als de voorafgaande taak met een langzamer tempo (hogere takttijd) wordt uitgevoerd, is de cyclusduurverhouding groter is dan 1.  
5. Klik op OK.


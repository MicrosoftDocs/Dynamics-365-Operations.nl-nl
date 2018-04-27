--- 
title: Een voorafgaande taak toevoegen aan een productiestroomactiviteit
description: In een productiestroomversie moeten alle activiteiten worden gerangschikt.
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Een voorafgaande taak toevoegen aan een productiestroomactiviteit

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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



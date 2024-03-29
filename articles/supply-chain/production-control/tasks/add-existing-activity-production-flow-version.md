---
title: Een bestaande activiteit toevoegen aan een productiestroomversie
description: Bij het maken van nieuwe versies van productiestromen, kunt u kiezen om activiteiten die voor de oudere versies zijn gemaakt, aan de nieuwe versie toe te voegen.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f73274c6e102df3007793e027587793d87c4f83
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579299"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Een bestaande activiteit toevoegen aan een productiestroomversie

[!include [banner](../../includes/banner.md)]

Bij het maken van nieuwe versies van productiestromen, kunt u kiezen om activiteiten die voor de oudere versies zijn gemaakt, aan de nieuwe versie toe te voegen. Deze procedure laat zien hoe een nieuwe versie voor een bestaande productiestroom wordt gemaakt, zonder de activiteiten te kopiëren. In de volgende stap wordt een bestaande activiteit toegevoegd aan de nieuwe versie. 

Deze taak vereist dat er al een productiestroom met versie en activiteiten is gemaakt.


## <a name="create-a-new-production-flow-version"></a>Een nieuwe productiestroomversie maken
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op Bewerken.
5. Markeer in de lijst de geselecteerde rij.
6. Voer in het veld Vervaldatum een datum en tijd in.
    * Let op dat voordat u een nieuwe productiestroomversie maakt, u de vervaldatum en -tijd van de actieve versie moet controleren. De nieuwe versie wordt gemaakt met een ingangsdatum, die aan de vervaldatum van de geselecteerde versie is gekoppeld.  
7. Klik op Toevoegen.
8. Selecteer Nee in het veld Kopiëren uit versie.
    * Selecteer Nee om met een lege versie te starten als de meeste activiteiten van de gekopieerde versie door nieuwe activiteiten worden vervangen. Voeg de onveranderde activiteiten handmatig toe aan het formulier Bestaande functie toevoegen in de activiteit.  
9. Selecteer Nee in het veld Dubbele kanbanregels.
    * Wanneer de activiteiten niet naar de nieuwe versie worden gekopieerd, is het niet mogelijk om de kanbanregels op het moment van aanmaken van de nieuwe versie te kopiëren.   In plaats daarvan gebruikt u de functie om later een vervangende kanban te maken in het kanbanregelformulier om kanbanregels van de oude productiestroomversie te vervangen door kanbanregels met de activiteiten van de nieuwe versie.  
10. Klik op OK.
11. Zoek en selecteer de gewenste record in de lijst.

## <a name="add-an-existing-activity"></a>Een bestaande activiteit toevoegen
1. Klik op Activiteiten.
2. Klik op Bestaand toevoegen om het dialoogvenster voor beëindiging te openen.
    * Zoek en selecteer een bestaande activiteit die moet worden toegevoegd aan de nieuwe productiestroomversie.  Merk op dat de lijst alle activiteiten weergeeft die voor deze productiestroom zijn gemaakt voor alle vorige versies van de stroom.  
3. Typ of selecteer een waarde in het veld Activiteit.
4. Klik op OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
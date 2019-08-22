---
title: Kanbanschemagroepen definiëren
description: Kanbanschemagroepen zijn gedefinieerd om producten te groeperen en te onderscheiden in kanbanplanning.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0cb17c68abbc4979a65e33c50450be575df3d93
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836259"
---
# <a name="define-lean-schedule-groups"></a>Kanbanschemagroepen definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kanbanschemagroepen zijn gedefinieerd om producten te groeperen en te onderscheiden in kanbanplanning. Het groeperen kan als algemene koppeling per bedrijf of specifiek voor een werkcel worden uitgevoerd. Elke groep heeft een kleurencode voor grafische indicatie in de lijstpagina van kanbanplanning. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="define-lean-scheduling-group"></a>Kanbanschemagroep definiëren
1. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanschemagroepen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Planningsgroep.
    * Een planningsgroep kan worden gedefinieerd als globale groep of specifiek voor een werkcel. In dit eenvoudige voorbeeld definiëren we een globale groep en blijft de werkcel leeg. De instellingen van deze groep zijn van toepassing op alle werkcellen die geen specifieke planningsgroepen hebben.  
4. Selecteer een kleur uit de kleurselectie.
    * De kleuren worden gebruikt om de taken te markeren in de lijstpagina van de kanbanplanning of het bord van het kanbanproces.  
5. Markeer in de lijst de geselecteerde rij.
6. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="associate-product"></a>Product koppelen
1. Een specifiek product koppelen
    * Er zijn twee manieren om producten aan lean planningsgroepen te koppelen: als een specifiek product (type artikelrelatie = Artikel) of als onderdeel van een artikeltoewijzingssleutel (type artikelrelatie = groep).    
2. Selecteer Artikel in het veld Type artikelrelatie.
3. Typ een waarde in het veld Artikelnummer.
4. Typ een nummer in het veld Doorvoerverhouding.
    * De standaarddoorvoerverhouding is 1, wat wil dat zeggen dat de gerelateerde producten precies de capaciteit verbruiken die is opgegeven in de procesactiviteiten van de productiestromen. Doorvoerverhouding > 1 bepaalt een hoger resourceverbruik, doorvoerverhouding < 1 definieert een lager resourceverbruik. De verhouding wordt gebruikt in de kostprijsberekening en in de berekening van het kanbantaakverbruik.  

## <a name="associate-item-allocation-key"></a>Artikeltoewijzingssleutel koppelen
1. Een artikeltoewijzingssleutel koppelen
    * Voeg een koppeling toe aan een artikeltoewijzingssleutel door het type artikelrelatie Groep te gebruiken.   Voor dit proces hebt u nodig een alllocationsleutel hebt een artikeltoewijzingssleutel nodig die in uw gegevens wordt gedefinieerd.  
2. Selecteer Groep in het veld Type artikelrelatie.
3. Klik in het veld Artikeltoewijzingssleutel op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.


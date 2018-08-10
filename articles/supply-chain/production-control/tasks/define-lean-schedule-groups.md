--- 
title: "Kanbanschemagroepen definiëren"
description: Kanbanschemagroepen zijn gedefinieerd om producten te groeperen en te onderscheiden in kanbanplanning.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e07fa270b47be3527c572dc53ca30a7bcde5ba6
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

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
    * Voeg een koppeling toe aan een artikeltoewijzingssleutel door het type artikelrelatie Groep te gebruiken.   Voor dit proces moet u een artikeltoewijzingssleutel voor prognoses in uw gegevens hebben gedefinieerd.  
2. Selecteer Groep in het veld Type artikelrelatie.
3. Klik in het veld Artikeltoewijzingssleutel op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.



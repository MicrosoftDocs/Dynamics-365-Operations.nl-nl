--- 
title: Compensatierasters instellen
description: Compensatierasters worden gebruikt om de salarisstructuren voor plannen voor vaste compensatie weer te geven of te onderhouden.
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 33a95e4366dc352f28202155be7fc0b8f4c99e4a
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-compensation-grids"></a>Compensatierasters instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Compensatierasters worden gebruikt om de salarisstructuren voor plannen voor vaste compensatie weer te geven of te onderhouden. Compensatierasters kunnen worden gedeeld over meerdere plannen of worden gekopieerd bij het maken van een nieuw compensatieplan.  Voordat u een compensatieraster maakt, moet u de Niveaus en Referentiepunten instellen. In dit voorbeeld wordt een nieuw Cijfertype van compensatieraster gemaakt met demogegevens voor de Niveaus en Referentiepunten. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Information over het compensatieraster instellen
1. Ga naar Human resources > Compensatie > Vaste compensatie > Compensatierasters.
2. Klik op Nieuw.
3. Typ een waarde in het veld Raster.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer een optie in het veld Type.
6. Typ of selecteer een waarde in het veld Referentie-instelling.
7. Typ of selecteer een waarde in het veld Valuta.
8. Typ een waarde in het veld Valuta.
9. Voer een datum in het veld Begindatum in.

## <a name="add-levels-to-the-compensation-structure"></a>Niveaus toevoegen aan de compensatiestructuur
1. Klik op Compensatiestructuur.
2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld Niveau.
4. Klik op Nieuw.
5. Markeer in de lijst de geselecteerde rij.
6. Typ of selecteer een waarde in het veld Niveau.
7. Klik op Nieuw.
8. Markeer in de lijst de geselecteerde rij.
9. Typ of selecteer een waarde in het veld Niveau.
10. Klik op Nieuw.
11. Markeer in de lijst de geselecteerde rij.
12. Typ of selecteer een waarde in het veld Niveau.
13. Klik op Nieuw.
14. Markeer in de lijst de geselecteerde rij.
15. Typ of selecteer een waarde in het veld Niveau.

## <a name="fill-in-the-compensation-structure-with-values"></a>De compensatiestructuur vullen met waarden
1. Markeer in de lijst de geselecteerde rij.
    * Op dit moment kunnen de compensatiewaarden handmatig in elk veld in de tabel worden ingevoerd, of kunt u de functie Groepsgewijs wijzigen gebruiken om eenvoudig meerdere velden in te vullen en basisberekeningen uit te voeren.  
2. Klik op Groepsgewijs wijzigen.
    * Voor dit raster passen we eerst de waarde voor het middelpunt van eerste vlak toe op alle velden in de tabel. Dit wordt de basis voor de compensatiematrix.  
3. Selecteer een optie in het veld Correctietype.
4. U moet een getal invoeren in het veld Aanpassingsbedrag.
5. Selecteer of deselecteer alle rijen in de lijst.
6. Klik op Toepassen op raster.
    * Nu gebruiken we de functie Groepsgewijs wijzigen om de bedragen in elk volgend niveau te verhogen met een bepaald percentage of bedrag. In dit voorbeeld krijgt elk cijfer een afstand van 12,5% tussen hun middelpunten.  
7. Selecteer een optie in het veld Correctietype.
8. U moet een getal invoeren in het veld Aanpassingsbedrag.
9. Zoek en selecteer het gewenste record in de lijst.
10. Zoek en selecteer het gewenste record in de lijst.
11. Zoek en selecteer het gewenste record in de lijst.
12. Zoek en selecteer het gewenste record in de lijst.
13. Klik op Toepassen op raster.
14. Zoek en selecteer het gewenste record in de lijst.
15. Zoek en selecteer het gewenste record in de lijst.
16. Zoek en selecteer het gewenste record in de lijst.
17. Klik op Toepassen op raster.
18. Zoek en selecteer het gewenste record in de lijst.
19. Zoek en selecteer het gewenste record in de lijst.
20. Klik op Toepassen op raster.
21. Zoek en selecteer de gewenste record in de lijst.
22. Klik op Toepassen op raster.
    * Nu gebruiken we de functie Groepsgewijs wijzigen om de minimum- en maximumreferentiepunten voor elk niveau te corrigeren. Dit voorbeeld gebruikt een afstand van 50% zodat het minimumreferentiepunt met -20% worden gecorrigeerd en het maximumreferentiepunt met +20% wordt aangepast.  
23. U moet een getal invoeren in het veld Aanpassingsbedrag.
24. Typ of selecteer een waarde in het veld Referentiepunt.
25. Selecteer of deselecteer alle rijen in de lijst.
26. Klik op Toepassen op raster.
27. U moet een getal invoeren in het veld Aanpassingsbedrag.
28. Typ of selecteer een waarde in het veld Referentiepunt.
29. Selecteer of deselecteer alle rijen in de lijst.
30. Klik op Toepassen op raster.



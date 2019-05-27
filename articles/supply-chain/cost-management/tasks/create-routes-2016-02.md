---
title: Routes maken (uitsluitend februari 2016)
description: Deze taak is gericht op het maken van de productieroutes voor een eindproduct en een halffabricaat.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63ad2cc0c41a5931750dffbfc64bc7ce965a1da4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563199"
---
# <a name="create-routes-february-2016-only"></a>Routes maken (uitsluitend februari 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taak is gericht op het maken van de productieroutes voor een eindproduct en een halffabricaat. Dit is de vijfde taak in de reeks stuklijstberekeningen. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.


## <a name="create-a-route-for-a-semi-finished-product"></a>Een route voor een halffabricaat maken
1. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer het artikelnummer Stuklijst_2.  
3. Klik op Technicus in het actievenster.
4. Klik op Route.
5. Klik op Nieuw.
6. Klik op Route en routeversie.
7. Typ een waarde in het veld Omschrijving.
    * Typ voor dit voorbeeld ROUTE_2.  
8. Typ of selecteer een waarde in het veld Locatie.
    * Typ of selecteer voor dit voorbeeld Locatie 1.  
9. Klik op OK.
10. Klik op Nieuw.
11. Typ of selecteer een waarde in het veld Bewerking.
    * Selecteer voor dit voorbeeld Assembleren.  
12. Voer een getal in het veld Uitvoeringstijd in.
    * Typ bijvoorbeeld 1. Uitvoeringstijden maken vaak deel uit van de prijs die voor een artikel wordt berekend.  
13. Typ of selecteer een waarde in het veld Routegroep.
    * Selecteer voor dit voorbeeld 'Std'.  
14. Klik op het tabblad Instellingen.
15. Typ of selecteer een waarde in het veld Instelcategorie.
    * Selecteer voor dit voorbeeld Assembleren.  
16. Klik op het tabblad Tijden.
17. Voer in het veld Insteltijd een getal in.
    * Typ voor dit voorbeeld 1. Insteltijden maken vaak deel uit van de prijs die voor een artikel wordt berekend.  
18. Klik in het actievenster op Routeversie.
19. Klik op Goedkeuren.
20. Selecteer Ja bij de vraag Wilt u ook de route goedkeuren?.
21. Klik op OK.
22. Klik in het actievenster op Routeversie.
23. Klik op Activeren.
24. Sluit de pagina.
25. Sluit de pagina.

## <a name="create-a-route-for-a-finished-product"></a>Een route voor een eindproduct maken
1. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer het artikelnummer Stuklijst_1.  
2. Klik op Technicus in het actievenster.
3. Klik op Route.
4. Klik op Nieuw.
5. Klik op Route en routeversie.
6. Typ een waarde in het veld Omschrijving.
    * Typ voor dit voorbeeld ROUTE_1.  
7. Typ of selecteer een waarde in het veld Locatie.
    * Typ of selecteer voor dit voorbeeld Locatie 1.  
8. Klik op OK.
9. Klik op Nieuw.
10. Typ of selecteer een waarde in het veld Bewerking.
    * Selecteer voor dit voorbeeld Verpakken.  
11. Voer een getal in het veld Uitvoeringstijd in.
    * Typ voor dit voorbeeld 1.  
12. Typ of selecteer een waarde in het veld Routegroep.
    * Selecteer voor dit voorbeeld 'Std'.  
13. Klik op het tabblad Instellingen.
14. Typ of selecteer een waarde in het veld Instelcategorie.
    * Selecteer voor dit voorbeeld Verpakken.  
15. Klik op het tabblad Tijden.
16. Voer in het veld Insteltijd een getal in.
    * Typ voor dit voorbeeld 1.  
17. Klik in het actievenster op Routeversie.
18. Klik op Goedkeuren.
19. Klik op OK.
20. Klik in het actievenster op Routeversie.
21. Klik op Activeren.
22. Sluit de pagina.
23. Sluit de pagina.

## <a name="enable-automatic-consumption-of-setup-time"></a>Automatisch verbruik van de insteltijd inschakelen
1. Ga naar Productiebeheer > Instellingen > Routes > Routegroepen.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer in de lijst 'Std'.  
3. Klik op Bewerken.
4. Selecteer Ja in het veld Insteltijd.
    * Insteltijden maken vaak deel uit van de prijs die voor een artikel wordt berekend.  
5. Klik op Opslaan.
6. Sluit de pagina.


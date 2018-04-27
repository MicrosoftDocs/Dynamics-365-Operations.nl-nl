--- 
title: De indeling uitvoeren voor tellen en totaliseren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e3569e48bcc063b2423a60038732e8e53dbea2cb
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="run-the-format-to-do-counting-and-summing"></a>De indeling uitvoeren voor tellen en totaliseren

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 3: Berekeningen gebruiken om de uitvoer te maken)".

Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Test deze configuratie voor het genereren van de Intrastat-rapporten
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.
3. Vouw in de structuur 'Intrastat-model' uit.
4. Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.
5. Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.
6. Klik in het actievenster op Configuraties.
7. Klik op Gebruikersparameters.
8. Selecteer Ja in het veld Uitvoeringsinstellingen.
9. Klik op OK.
10. Klik op Bewerken.
11. Selecteer Ja in het veld Concept uitvoeren.
12. Klik op Opslaan.
13. Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.
14. Vouw de sectie Elektronische rapportage uit.
15. Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.
16. Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.
17. Klik op Opslaan.
18. Sluit de pagina.
19. Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.
20. Klik op Uitvoer.
21. Klik op Rapport.
    * Voer het proces uit om het Intrastat-rapport te genereren.  
22. Stel in het veld Begindatum de datum in op "2000-01-01".
    * Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.  
23. Stel in het veld Einddatum de datum in op "2022-12-31".
    * Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.  
24. Selecteer Ontvangsten in het veld Richting.
25. Selecteer Ja in het veld Bestand maken.
26. Klik op OK.
    * Controleer de gemaakte uitvoer met de overzichtsregels aan het einde.  
27. Klik op Nieuw.
28. Markeer in de lijst de geselecteerde rij.
29. Selecteer Verzendingen in het veld Richting.
30. Typ of selecteer een waarde in het veld Artikelnummer.
31. Typ of selecteer een waarde in het veld Basisproduct.
32. Stel Gewicht in op 10.
33. Stel Factuurbedrag in op 10000.
34. Stel Statistisch bedrag in op 10000.
35. Klik op Uitvoer.
36. Klik op Rapport.
37. Selecteer Verzendingen in het veld Richting.
38. Klik op OK.
    * Controleer de gemaakte uitvoer met de overzichtsregels aan het einde. Let op dat dit in vergelijking met de eerste uitvoering is gewijzigd.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Voer deze configuratie uit in foutoplossingsmodus uit om de verzamelde tel- en totaalgegevens te controleren
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Intrastat-model' uit.
3. Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.
4. Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.
5. Klik in het actievenster op Configuraties.
6. Klik op Gebruikersparameters.
7. Selecteer Ja in het veld Uitvoeren in foutoplossingsmodus.
8. Klik op OK.
9. Sluit de pagina.
10. Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.
11. Klik op Uitvoer.
12. Klik op Rapport.
13. Klik op OK.
14. Sluit de pagina.
15. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
16. Vouw in de structuur 'Intrastat-model' uit.
17. Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.
18. Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.
19. Klik op Foutopsporingslogboeken.
    * Merk op dat er een record met een foutopsporingslogboek is gemaakt voor het uitvoeringsproces van de geselecteerde configuratie.  
20. Klik op Koppelen.
21. Klik op Openen.
    * Controleer het gemaakte XML-bestand dat de tellings- en totaliseringsgegevens bevat die tijdens de uitvoering van de geselecteerde configuratie zijn verzameld.  



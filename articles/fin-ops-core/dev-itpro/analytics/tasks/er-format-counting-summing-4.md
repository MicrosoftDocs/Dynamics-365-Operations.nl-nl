---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 4: Indeling uitvoeren)'
description: In dit artikel wordt beschreven hoe u een indeling voor elektronische rapportage configureert voor tellen en totaliseren op basis van de gegevens van de reeds gegenereerde tekstuitvoer. (Deel 4)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
ms.openlocfilehash: 7610e71346b57a7e624424418b22b40e51f9bb95
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290599"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a>ER Indeling configureren voor tellen en totaliseren (deel 4: Indeling uitvoeren)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen in de procedure ER Indeling configureren voor tellen en totaliseren (Deel 3: Berekeningen gebruiken om de uitvoer te maken) uit.

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

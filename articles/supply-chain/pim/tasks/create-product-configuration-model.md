--- 
title: Een productconfiguratiemodel maken
description: Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert.
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: d494a20ba6f1f9c33a3935779b4bd3a8eefce26a
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---
# <a name="create-a-product-configuration-model"></a>Een productconfiguratiemodel maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-product-model"></a>Een productmodel maken
1. Klik op Definitie van productvariantmodel.
2. Klik op Productconfiguratiemodellen.
3. Klik op Nieuw.
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Omschrijving.
6. Selecteer een optie in het veld Oplossingsstrategie.
    * De oplossingsstrategie bepaalt hoe de beperkingen in een op beperkingen gebaseerd productconfiguratiemodel worden verwerkt. Deze selectie kan een invloed hebben op de prestaties van het productconfiguratiemodel.  
7. Typ een waarde in het veld Naam.
    * Het hoofdcomponent vertegenwoordigt het productconfiguratiemodel, maar kan ook in andere productmodellen worden gebruikt.  
8. Klik op OK.
9. Selecteer een optie in het veld Configuraties opnieuw gebruiken.
    * Als de parameter Configuraties opnieuw gebruiken op Ja is ingesteld, controleert het systeem identieke configuraties na elke sessie en elk hergebruik van de configuratie als een exacte overeenkomst wordt gevonden.  

## <a name="add-attributes"></a>Kenmerken toevoegen
1. Vouw de sectie Kenmerken uit.
2. Klik op Toevoegen.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Oplossingsnaam.
    * De oplossingsnaam wordt gebruikt door oplosser van beperkingen van de productconfiguratie. Deze mag geen spaties of speciale tekens bevatten, behalve _ (onderstrepingsteken).  
6. Typ een waarde in het veld Omschrijving.
    * De omschrijvingstekst wordt aan de gebruiker van de configuratie weergegeven en kan daarom fungeren als hulp bij het selecteren van de juiste kenmerkwaarde.  
7. Typ of selecteer een waarde in het veld Kenmerktype.
    * Het kenmerktype bepaalt welke waarden beschikbaar zijn voor het kenmerk.  
8. Schakel het selectievakje Opnemen in hergebruik in.
    * Deze optie is alleen beschikbaar als de optie Configuraties opnieuw gebruiken is geselecteerd. Als het selectievakje van het kenmerk wordt ingeschakeld, wordt met dit kenmerk rekening gehouden wanneer het systeem naar een exacte overeenkomst zoekt.  

## <a name="add-subcomponents"></a>Subonderdelen toevoegen
1. Vouw de sectie Subonderdelen uit.
2. Klik op Toevoegen.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld Naam.
5. Typ een waarde in het veld Oplossingsnaam.
6. Typ een waarde in het veld Omschrijving.
7. Typ of selecteer een waarde in het veld Onderdeel.
    * Elke subonderdeel moet naar een componentdefinitie verwijzen. Dit ontwerp ondersteunt herbruikbare onderdelen en zorgt ervoor dat een onderdeel, als het is gedefinieerd, in veel productmodellen kan worden gebruikt.  
8. Klik op Opslaan.
9. Klik op Regeldetails van stuklijst.
    * Met het formulier Regeldetails van stuklijst kan de gebruiker de vereiste eigenschappen voor het subonderdeel selecteren. Elke eigenschap kan een vaste waarde krijgen of aan een kenmerk worden toegewezen. De toewijzing aan een kenmerk zorgt ervoor dat de regeleigenschap van de stuklijst verschillende waarden krijgt, afhankelijk van de geselecteerde configuratie.  
10. Typ of selecteer een waarde in het veld Artikelnummer.
    * Elke subonderdeel vertegenwoordigt een configureerbaar productmodel met op beperkingen gebaseerde configuratietechnologie. De verwijzing wordt gemaakt door het artikelnummer.  
11. Schakel het selectievakje Instellen in.
12. Selecteer Ja in het veld Berekening.
    * Het instellen van de berekeningsoptie zorgt ervoor dat het product wordt opgenomen bij de uitvoering van een kostenberekening voor het product.  
13. Klik op het tabblad Instellingen.
14. Schakel het selectievakje Instellen in.
15. Voer in het veld Hoeveelheid een getal in.
    * Het hoeveelheidsveld bepaalt hoeveel van dit product wordt verbruikt in het geconfigureerde product.  
16. Schakel het selectievakje Instellen in.
17. Voer in het veld Per reeks een getal in.
18. Klik op OK.



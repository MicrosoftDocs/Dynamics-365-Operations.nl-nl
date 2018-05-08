--- 
title: Salaris-/compensatiestructuur en -plannen ontwikkelen
description: Deze taakbegeleiding doorloopt het proces voor het maken van een vastecompensatieplan en het mogelijk maken dat werknemers worden geregistreerd in het plan via geschiktheidsregels.
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d2a4a0b2bf2d33530dedc7ce3974ee558d063878
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="develop-salarycompensation-structure-and-plans"></a>Salaris-/compensatiestructuur en -plannen ontwikkelen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding doorloopt het proces voor het maken van een vastecompensatieplan en het mogelijk maken dat werknemers worden geregistreerd in het plan via geschiktheidsregels. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF en de taak is bedoeld voor de Manager compensatie en vergoedingen.


## <a name="create-fixed-compensation-plan"></a>Vastecompensatieplan maken
1. Klik op Compensatiebeheer.
2. Klik op Vastecompensatieplannen.
3. Klik op Nieuw.
4. Typ een waarde in het veld Plan.
5. Typ een waarde in het veld Omschrijving.
6. Voer een datum in het veld Begindatum in.
7. Selecteer in het veld Type of het vastecompensatieplan van het type schaal, schijf of stap is.
8. Het selectievakje Aanbeveling toegestaan fungeert als standaardwaarde voor eventuele acties die aan dit plan in een procesgebeurtenis worden toegevoegd.  Met Aanbeveling toegestaan kunt u het berekende richtlijnbedrag overschrijven bij het verwerken van de compensatie.
9. Met Tolerantie voor buiten bereik kunt u opgeven hoe u compensatiebedragen wilt verwerken die buiten het opgegeven bereik van de compensatiestructuur voor het opgegeven niveau vallen.  Met Tolerantie voor buiten bereik of Geen kunt u elk compensatiebedrag gebruiken.  Een zachte tolerantie waarschuwt de gebruiker als het compensatiebedrag minder is dan het minimumreferentiepuntbedrag voor dat niveau of groter dan het maximumbedrag voor dat niveau. De gebruiker kan de waarschuwing negeren en verdergaan.  Een harde tolerantie genereert een fout als de compensatie van een werknemer ligt buiten de minimum- en maximumreferentiepunten voor het niveau en wordt de compensatie automatisch aangepast om binnen het bereik te vallen.
10. Het veld Huurregel wordt gebruikt wanneer een gebeurtenis van de compensatieverwerking wordt uitgevoerd om de compensatie van een werknemer te berekenen.  Een huurregel Percentage berekent een verhoging die evenredig is voor de duur dat de werknemer in dienst is in de cyclus.
11. Typ een waarde in het veld Valuta.
12. Typ of selecteer een waarde in het veld Conversie van loontarief.
13. Vouw de sectie Bereikgebruiksmatrix uit.
    * Voeg desgewenst bereikgebruikrecords toe om werknemers sneller naar hun middelpunt toe te krijgen en ze af te remmen voor het bereiken van het maximum van hun bereik.  
14. Op dit punt moet u het vastecompensatieplan opslaan om de knop Compensatie instellen te activeren en door te gaan met het definiëren van de compensatiestructuur voor het plan.  Klik op Opslaan.
15. Klik op Compensatie instellen.
    * Er zijn drie manieren om een compensatiestructuur te maken. 1: Maak een geheel nieuwe structuur door een set referentiepunten te selecteren en de niveaus toe te voegen om uw eigen structuur te maken. 2: Kopieer een compensatiestructuur van een bestaand plan als beginpunt en wijzig deze voor het nieuwe plan. 3: Selecteer een bestaand compensatieraster. Als het compensatieraster al door een ander plan wordt gebruikt, worden eventuele wijzigingen in het raster ook doorgevoerd in het andere plan.  
16. Schakel het selectievakje Nieuwe matrix maken op basis van bestaande compensatiematrix in.
17. Typ of selecteer een waarde in het veld Uit raster kopiëren.
    * Desgewenst kunt u de naam van het nieuwe compensatieraster wijzigen dat als een kopie van het geselecteerde raster wordt gemaakt.  
18. Klik op OK.
19. Klik op Groepsgewijs wijzigen.
    * Door de massawijziging kunt u de bedragen van de compensatiematrix onderhouden door een percentage of een vlakke bedragverhoging toe te passen op één of meerdere niveaus en/of referentiepunten.  
20. U moet een getal invoeren in het veld Aanpassingsbedrag.
21. Selecteer of deselecteer alle rijen in de lijst.
22. Klik op Toepassen op raster.
23. Sluit de pagina.
    * Zodra een compensatiestructuur is gemaakt of geselecteerd, kunt u selecteren welke referentiepunten als een controlepunt moet worden gebruikt voor het vastecompensatieplan.  Het controlepunt wordt gebruikt om de comparatio van een werknemer te berekenen.  
24. Typ of selecteer een waarde in het veld Controlepunt.
25. Sluit de pagina.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Maak een geschiktheidsregel voor het nieuwe vastecompensatieplan
    * Het nieuwe vastecompensatieplan kan niet aan een werknemer worden toegewezen tot geschiktheidsregels voor het plan zijn gedefinieerd.  
1. Klik op Geschiktheidsregels.
2. Klik op Nieuw.
3. Typ een waarde in het veld Geschiktheid.
4. Typ een waarde in het veld Omschrijving.
5. Voer een datum in het veld Begindatum in.
    * Geschiktheidsregels worden voor zowel vaste- als variabele-compensatieplannen gebruikt.  Selecteer in het veld Type voor welk type plan deze reeks geschiktheidsregels is.  
6. Typ of selecteer een waarde in het veld Plan.
    * Selecteer de criteria waaraan een werknemer moet voldoen om in aanmerking te komen voor het compensatieplan. De criteria kunnen zijn: Afdeling, Vakbond, Locatie (Compensatieregio), Taak, Functie, Taaktype of Compensatieniveau. De werknemer moet aan alle criteria voldoen om in aanmerking te komen voor het compensatieplan. Als er geen criteria bestaan, komen alle werknemers in aanmerking voor het compensatieplan. Als een werknemer niet voldoet aan de criteria die in de regel voor geschiktheid worden opgegeven, of er geen regel voor geschiktheid voor een compensatieplan is opgegeven, wordt het compensatieplan niet in de zoekopdracht bij het maken van een vaste-compensatierecord voor een werknemer weergegeven.  
7. Sluit de pagina.
8. Sluit de pagina.



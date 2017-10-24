--- 
title: Een min./max. aanvullingsproces instellen
description: Deze procedure laat zien hoe u een nieuw aanvullingsproces instelt waarin de strategie van min./max. aanvulling wordt gebruikt.
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>Een min./max. aanvullingsproces instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een nieuw aanvullingsproces instelt waarin de strategie van min./max. aanvulling wordt gebruikt. Wanneer de voorraad onder het minimumniveau valt, wordt werk gemaakt om de locatie aan te vullen. De procedure laat ook zien hoe u vaste orderverzamellocaties kunt gebruiken om herbevoorrading mogelijk te maken zelfs als de voorraad onder het minimumniveau valt, en hoe het aanvullingsproces regelmatig kan worden uitgevoerd met een batchtaak. Deze taken worden meestal uitgevoerd door een magazijnmanager. U kunt deze procedure in het demobedrijf USMF uitvoeren met behulp van de voorbeeldwaarden in de notities of kunt de procedure op uw eigen gegevens uitvoeren. Als u uw eigen gegevens gebruikt, moet u ervoor zorgen dat u een magazijn hebt dat voor de magazijnbeheerprocessen is ingeschakeld.


## <a name="create-a-fixed-picking-location"></a>Een vaste orderverzamellocatie maken
1. Ga naar Magazijnbeheer > Instellingen > Magazijn > Vaste locaties.
    * Dit is een optionele taak voor min./max. aanvulling, maar als u vaste orderverzamellocatie gebruikt, kan de voorraad zelfs worden aangevuld als deze onder het minimumniveau valt, omdat het systeem kan bepalen welke artikelen moeten worden aangevuld, zelfs als er geen meer zijn.  
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Artikelnummer.
    * Als u USMF gebruikt, kunt u artikel A0001 selecteren.  
4. Typ of selecteer een waarde in het veld Locatie.
    * Als u USMF gebruikt, kunt u Vestiging 2 selecteren.  
5. Typ of selecteer een waarde in het veld Magazijn.
    * Als u USMF gebruikt, kunt u magazijn 24 selecteren.  
6. Typ of selecteer een waarde in het veld Locatie.
    * Als u USMF gebruikt, kunt u CP-003 selecteren.  
7. Sluit de pagina.

## <a name="create-a-replenishment-location-directive"></a>Een aanvullingslocatierichtlijn maken
1. Ga naar Magazijnbeheer > Instellingen > Instructielocatie.
    * Locatierichtlijnen worden gebruikt om te bepalen waar artikelen in het aanvullingsproces moeten worden verzameld.  
2. Selecteer 'Aanvulling' in het veld Werkordertype.
3. Klik op Nieuw.
4. Typ een waarde in het veld Naam.
5. Selecteer 'Verzamelen' in het veld Werktype.
6. Typ of selecteer een waarde in het veld Locatie.
    * Als u USMF gebruikt, kunt u Vestiging 2 selecteren.  
7. Typ of selecteer een waarde in het veld Magazijn.
    * Als u USMF gebruikt, kunt u magazijn 24 selecteren.  
8. Klik op Opslaan.
9. Klik op Nieuw.
10. Markeer in de lijst de geselecteerde rij.
11. Voer een getal in het veld Tot hoeveelheid in.
    * U kunt dit bijvoorbeeld instellen op 9999.  
12. Schakel het selectievakje Splitsen toestaan in.
    * Als u deze optie selecteert, kunnen tijdens het maken van werk werkregelhoeveelheden worden opgesplitst verspreid over meerdere locaties.  
13. Klik op Opslaan.
14. Klik op Nieuw.
15. Markeer in de lijst de geselecteerde rij.
16. Typ een waarde in het veld Naam.
17. Klik op Opslaan.
18. Klik op Query bewerken.
    * U kunt deze query bewerken om beperkingen toe te voegen op basis waarvan voorraad in het aanvullingsproces kan worden geselecteerd. Het kan bijvoorbeeld zijn dat alleen voorraad van het bulkgebied van het magazijn mag worden gebruikt.  
19. Klik op OK.
20. Sluit de pagina.

## <a name="create-a-replenishment-work-template"></a>Een aanvullingswerksjabloon maken
1. Ga naar Magazijnbeheer > Instellingen > Werk > Werksjablonen.
    * De werksjabloon wordt gebruikt als richtlijn voor het systeem om te bepalen hoe min./max. aanvullingswerk moet worden gemaakt. Als minimum moet er een werksjabloonregel voor verzamelen en neerzetten zijn. De werksjabloon geeft aan dat het ongeldig is totdat alle vereiste informatie is ingevuld.  
2. Selecteer 'Aanvulling' in het veld Werkordertype.
3. Klik op Nieuw.
4. Typ een waarde in het veld Werksjabloon.
5. Klik op Opslaan.
6. Klik op Nieuw.
7. Selecteer 'Verzamelen' in het veld Werktype.
8. Typ of selecteer een waarde in het veld Werkklasse-id.
    * Dit moet een werkklasse gerelateerd aan aanvulling zijn. Als u USMF gebruikt, selecteert u Aanvullen.  
9. Klik op Nieuw.
10. Markeer in de lijst de geselecteerde rij.
11. Selecteer 'Wegzetten' in het veld Werktype.
12. Typ of selecteer een waarde in het veld Werkklasse-id.
13. Klik op Opslaan.
14. Sluit de pagina.

## <a name="create-a-new-replenishment-template"></a>Een nieuwe aanvullingssjabloon maken
1. Ga naar Magazijnbeheer > Instellingen > Aanvulling > Aanvullingssjablonen.
    * De aanvullingssjabloon wordt gebruikt om de artikelen en hoeveelheden en de aan te vullen locatie te definiëren.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Aanvullingssjabloon.
    * Geef de sjabloon een naam om aan te geven dat deze bestemd is voor min./max. aanvulling.  
4. Typ een waarde in het veld Omschrijving.
5. Schakel het selectievakje Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan in.
    * Als u deze optie selecteert, kunnen met wavevraagaanvulling hoeveelheden worden verbruikt die zijn gerelateerd aan min./max. aanvulling. Dit kan bijvoorbeeld nuttig zijn als het min./max. aanvullingswerk niet onmiddellijk wordt verwerkt om te voorkomen dat onnodig vraagaanvullingswerk wordt gemaakt.  
6. Klik op Nieuw.
7. Voer een getal in het veld Volgnummer in.
8. Typ een waarde in het veld Omschrijving.
9. Markeer in de lijst de geselecteerde rij.
10. Typ of selecteer een waarde in het veld Aanvullingseenheid.
    * Selecteer bijvoorbeeld stuks. Deze instelling moet worden opgegeven. Met deze instelling kunt u een andere maateenheid opgeven voor aanvullingswerk in vergelijking met de eenheid die is opgegeven voor de minimale en maximale voorraadniveaus in deze sjabloon.  
11. Typ of selecteer een waarde in het veld Werksjabloon.
    * Kies de werksjabloon die u eerder hebt gemaakt.  
12. Voer een getal in het veld Minimumhoeveelheid in.
    * Selecteer de minimumhoeveelheid die de aanvulling moet activeren. Stel dit bijvoorbeeld in op 50. Het is mogelijk om deze instelling op nul te laten staan, als u een vaste locatie aanvult en de optie Lege vaste locaties aanvullen is ingesteld op Ja. Het wordt ook aanbevolen de optie Alleen vaste locaties aanvullen te selecteren om prestatieredenen.  
13. Voer een getal in het veld Maximumhoeveelheid in.
    * Stel dit bijvoorbeeld in op 100.  
14. Typ of selecteer een waarde in het veld Eenheid.
    * Wijs de eenheid voor de minimale en maximale hoeveelheden toe. Stel dit bijvoorbeeld in op stuks.  
15. Schakel het selectievakje Lege vaste locaties aanvullen in.
    * Schakel dit selectievakje in om vaste locaties aan te vullen wanneer ze leeg zijn. Anders worden alleen de locaties aangevuld waar er een hoeveelheid voorhanden is.  
16. Schakel het selectievakje Alleen vaste locaties aanvullen in.
17. Klik op Producten selecteren.
    * Dit is de plaats om te bepalen welke producten moeten worden aangevuld. Als de optie Vaste orderverzamellocatie is ingeschakeld, moet u ook de locaties in deze query definiëren. Er zijn zowel variantspecifieke query's als productspecifieke query's beschikbaar.  
18. Selecteer de rij Artikelen.
19. Typ een waarde in het veld Criteria.
    * Selecteer de artikelen die op de vaste locaties moeten worden aangevuld. Typ bijvoorbeeld A* om alle artikelnummers te selecteren die met A beginnen.  
20. Klik op Toevoegen.
    * Voeg de locatie-entiteit (tenzij deze al bestaat) toe om het aanvullingswerk te kunnen beperken tot de vaste orderverzamellocaties binnen een specifiek gebied van het magazijn.  
21. Markeer in de lijst de geselecteerde rij.
22. Stel het veld Tabel in op Locaties.
23. Selecteer Locatieprofiel-ID in het veld Veld.
24. Typ of selecteer een waarde in het veld Criteria.
25. Klik op OK.
26. Sluit de pagina.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Het aanvullingsproces instellen op uitvoering als een batchtaak
1. Ga naar Magazijnbeheer > Aanvulling > Aanvullingen.
    * Op de pagina Aanvullingen kunt u instellen dat een aanvulling als een batchtaak wordt uitgevoerd of dat deze handmatig moet worden gestart.  
2. Klik op Filter.
3. Markeer in de lijst de geselecteerde rij.
4. Typ of selecteer een waarde in het veld Criteria.
5. Klik op OK.
6. Vouw de sectie Op de achtergrond uitvoeren uit.
7. Stel de optie Batchverwerking in op Ja.
8. Klik op Terugkeerpatroon.
9. Selecteer de optie Geen einddatum.
10. Stel het terugkeerpatroon in.
    * Selecteer bijvoorbeeld Dagen.  
11. Klik op OK.
12. Klik op OK.



--- 
title: Een menuopdracht voor een mobiel apparaat instellen voor het voltooien van werk in een inkooporder
description: Deze procedure laat zien hoe u een menuopdracht Mobiel apparaat instelt.
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b80c258d6a779a8fc5bb6c846abd3af7e69d5e06
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a>Een menuopdracht voor een mobiel apparaat instellen voor het voltooien van werk in een inkooporder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een menuopdracht Mobiel apparaat instelt. In dit voorbeeld, wordt de menuopdracht gebruikt voor het uitvoeren van werkzaamheden van het type Inkooporder. De werkklasse die aan de menuopdracht is gekoppeld, bepaalt welk werk geldig is. U kunt deze begeleiding gebruiken in het demobedrijf USMF. Doorgaans wordt deze procedure uitgevoerd door een magazijnbeheerder.


## <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken
1. Ga naar Menuopdrachten voor mobiel apparaat.
2. Klik op Nieuw.
3. Typ een waarde in het veld Menuoptie.
    * Voer een unieke waarde in. Zo kunt u bijvoorbeeld IO-verplaatsing typen. Onthoud de waarde. Deze zult u later nodig hebben.  
4. Typ een waarde in het veld Titel.
    * Dit is de titel die wordt weergegeven op het mobiele apparaat. Zo kunt u bijvoorbeeld IO verplaatsen typen.  
5. Selecteer 'Werk' in het veld Modus.
6. Selecteer Ja in het veld Bestaand werk gebruiken.
    * Dit menu-item op het mobiele apparaat wordt gebruikt voor het uitvoeren van bestaand werk. Daarom moet u deze waarde instellen op Ja.  
    * Het veld Voorraadstatus weergeven bepaalt of de voorraadstatus van de beschikbare voorraad wordt weergegeven aan de magazijnmedewerker op het mobiele apparaat.  
7. Selecteer 'Systeemgroepering' in het veld Bestuurd door.
    * Wanneer u iets selecteert in het veld Bestuurd door, worden extra velden weergegeven in de sectie Algemeen op deze pagina. De velden die worden weergegeven zijn afhankelijk van wat u hebt geselecteerd. Als u Systeemgroepering selecteert, worden twee nieuwe velden toegevoegd. Deze worden hieronder nader uitgelegd.  
8. Typ 'WorkPoolId' in het veld Systeemgroepering.
    * Wanneer magazijnmedewerkers dit menu-item openen, worden zij gevraagd een werkgroep-id te scannen. Alle werkorders met deze werkgroep-id en open werkorderregels met een van de werkklassen die zijn toegevoegd aan dit menu-item toegevoegd, worden aan de gebruiker getoond.  
9. Typ een waarde in het veld Systeemgroeperingslabel.
    * Dit is de tekst die wordt weergegeven voor de gebruiker van het mobiele apparaat. Zo kunt u bijvoorbeeld Werkgroep typen.  
10. Selecteer Ja in het veld Nummerplaat overschrijven tijdens wegzetten.
    * Met deze optie kunnen magazijnmedewerkers de doelnummerplaat overschrijven als artikelen op een locatie worden geplaatst die moet worden gecontroleerd op nummerplaat.  
11. Selecteer Ja in het veld Opslag voor groep.
    * Als de zetregels op de werkorder dezelfde locatie delen, ontvangt de gebruiker één gecombineerde wegzetinstructie voor alle regels.  
    * Auditsjabloon-id: met een werkauditsjabloon kunt u opgeven dat het werkproces voor een menu-item moet worden onderbroken zodat een andere bewerking kan worden uitgevoerd. Als bijvoorbeeld dit menu-item bestemd is voor binnenkomend werk, vereist de auditsjabloon mogelijk dat de werknemer de temperatuur controleert. Het tijdstip waarop het proces wordt onderbroken is opgegeven op de controlesjabloon en kan zijn, bijvoorbeeld, wanneer het werk wordt gestart of voltooid, of als de status verandert.  
12. Vouw de werkklassensectie uit.
13. Klik op Nieuw.
14. Typ 'Inkoop' in het veld Werkklasse-id.
    * De werkgroep beperkt het werk waarvoor het menu-item kan worden gebruikt. In dit geval wordt het gebruikt voor open orderregels die de werkklasse-id Inkoop hebben.  
15. Klik op Opslaan.

## <a name="set-up-work-confirmation"></a>Werkbevestiging instellen
1. Klik op Werkbevestigingsinstellingen.
2. Selecteer 'Verzamelen' in het veld Werktype.
3. Schakel het selectievakje Automatisch bevestigen in.
    * De werkinstructie met werktype Verzamelen wordt automatisch bevestigd. Deze instructie wordt niet aan de gebruiker gepresenteerd.  
4. Klik op Nieuw.
5. Selecteer 'Wegzetten' in het veld Werktype.
6. Schakel het selectievakje Bevestiging van locatie in.
    * De magazijnmedewerker wordt gevraagd een bevestigingsscan van de locatie uit te voeren bij het neerzetten van het artikel.  
7. Klik op Opslaan.
8. Sluit de pagina.
9. Sluit de pagina.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>De menuopdracht toevoegen aan het menu van een mobiel apparaat
1. Ga naar Menu voor mobiel apparaat.
2. Klik op Bewerken.
3. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Naam met een waarde van 'inkomend'.
    * U wilt het menu vinden dat u gebruikt voor binnenkomende menu-items. In USMF heet dit Inkomend.  
4. Selecteer een waarde in de structuur.
5. Klik op de pijl naar rechts.
6. Klik op Opslaan.
7. Sluit de pagina.



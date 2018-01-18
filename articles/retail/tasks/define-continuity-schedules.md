--- 
title: " Continuïteitsplanningen definiëren"
description: "In dit onderwerp worden de stappen besproken voor het instellen van een continuïteitsprogramma (ook wel aangeduid als terugkerende orders."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f99b3b71e46aae1e510cc24efe2f99f1a258fa1
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="define-continuity-schedules"></a> Continuïteitsplanningen definiëren

[!include[task guide banner](../includes/task-guide-banner.md)]

In dit onderwerp worden de stappen besproken voor het instellen van een continuïteitsprogramma (ook wel aangeduid als terugkerende orders. In dit onderwerp wordt het demobedrijf USRT gebruikt.


## <a name="create-continuity-program"></a>Een continuïteitsprogramma maken
1. Ga naar Detailhandel en commerce > Continuïteit > Continuïteitsprogramma's.
2. Klik op Nieuw.
3. Typ in het veld Plannings-ID de ID van de continuïteitsplanning.
4. Selecteer in het veld Orderbegin de waarde 'Eerste gebeurtenis'.
    * Als een klant een nieuwe order voor het continuïteitsprogramma plaatst, zijn er twee opties waarvoor product wordt verzonden: 1. De eerste gebeurtenis: het eerste product in het continuïteitsprogramma wordt verzonden.  2. De huidige gebeurtenis: het eerste product in het continuïteitsprogramma wordt verzonden. 2: Huidige gebeurtenis: het huidige product wordt verzonden. Bijvoorbeeld: in de derde maand van het programma ontvangt de klant het derde product uit het programma.  
5. Selecteer 'Ja' om te laten vragen om de begindatum van de order.
6. Klik op Regel toevoegen.
7. Typ in het veld Artikelnummer het artikelnummer van het eerste product ('0013').
8. Typ 'CP'.
9. Voer de datum in waarop het eerste product beschikbaar is om te worden besteld.
10. Klik op Regel toevoegen.
11. Typ '0014' in het veld Artikelnummer.
12. Wis de waarde in het veld Datumintervalcode.
    * Wis voor deze procedure het datuminterval. U stelt de datum in als incrementele datum vanaf de begindatum van het eerste artikel.  
13. Hier voert u het interval in waarmee de producten worden verzonden. Typ '30'.
    * Voor een maandelijks programma moet u 30 dagen invoeren als het interval.  
14. Klik op Regel toevoegen.
15. Typ '0015' in het veld Artikelnummer.
16. Typ 'Beëindigen'.
17. Klik op Opslaan.

## <a name="assign-to-continuity-item"></a>Aan continuïteitsartikel toewijzen
1. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
2. Selecteer artikel '0016'.
    * Voor deze procedure selecteert u artikelnummer 0016. Normaal gesproken hebt u een vrijgegeven product gemaakt waarop extra bedrijfslogica voor continuïteit wordt toegepast, wanneer het in het callcenter wordt geplaatst op een verkooporder.  
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik op Bewerken.
5. Vouw de sectie Verkopen uit of samen.
6. Hier voert u het continuïteitsprogramma in dat dit artikel vertegenwoordigt. Voer de plannings-ID in die u eerder hebt gemaakt.
    * Wanneer dit artikel wordt verkocht in een callcenter, wordt de extra bedrijfslogica toegepast van het geselecteerde continuïteitsprogramma.  
7. Klik op Opslaan.



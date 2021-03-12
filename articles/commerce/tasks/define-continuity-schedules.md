---
title: " Continuïteitsplanningen definiëren"
description: In dit onderwerp worden de stappen besproken voor het instellen van een continuïteitsprogramma (ook wel aangeduid als terugkerende orders).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 37c4022cb2f2acf567437c821946ad452ba8f37c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972325"
---
# <a name="define-continuity-schedules"></a> Continuïteitsplanningen definiëren

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de stappen besproken voor het instellen van een continuïteitsprogramma (ook wel aangeduid als terugkerende orders). In dit onderwerp wordt het demobedrijf USRT gebruikt.


## <a name="create-continuity-program"></a>Een continuïteitsprogramma maken
1. Ga naar Retail en Commerce > Continuïteit > Continuïteitsprogramma's.
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


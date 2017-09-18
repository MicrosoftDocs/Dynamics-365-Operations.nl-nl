--- 
title: Een vast activum splitsen
description: "Deze taakbegeleiding splitst een percentage van één activumboek op naar een nieuw activumboek."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5aea1aab9f6b084bd0c5bd2119639bff3555bb8a
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="split-a-fixed-asset"></a>Een vast activum splitsen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding splitst een percentage van één activumboek op naar een nieuw activumboek.  Het gebruikt de accountantsrol en USMF-demogegevens.


## <a name="create-a-new-fixed-asset"></a>Nieuwe vaste activa maken
1. Ga naar Vaste activa > Vaste activa > Vaste activa.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Groep vaste activa.
4. Noteer het vaste-activanummer om het later in het splitsingsproces te gebruiken.
5. Typ een waarde in het veld Naam.
6. Het formulier sluiten.

## <a name="split-a-fixed-asset"></a>Een vast activum splitsen
1. Zoek en selecteer in de lijst het vaste activum om te splitsen.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
3. Klik op Boeken.
    * Selecteer het boek dat u wilt opsplitsen naar het nieuwe activum.  
4. Klik op Functies.
5. Klik op Vaste activa splitsen.
6. Typ of selecteer een waarde in het veld Naar vaste activa.
7. Klik in het veld Boeken op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Voer in het veld Transactiedatum een datum in.
9. Voer een getal in het veld Percentage in.
10. Typ of selecteer een waarde in het veld Journaalnaam.
11. Klik op OK.

## <a name="post-the-journal-transaction"></a>De journaaltransactie boeken
1. Ga naar Vaste activa > Journaalboekingen > Vaste-activajournaal.
2. Selecteer in de lijst het journaal dat met het splitsingsproces is gemaakt.
3. Klik op Regels.
    * Controleer de gemaakte journaalregels.  Een bijboekingscorrectietransactie wordt gemaakt voor het oorspronkelijke activum om de waarde te verlagen door het percentage dat is opgegeven tijdens het opsplitsingsproces.  Een bijboekingstransactie wordt gemaakt voor het nieuwe activum voor hetzelfde bedrag.  
4. Klik op Boeken.


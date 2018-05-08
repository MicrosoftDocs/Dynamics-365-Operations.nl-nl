--- 
title: Een kostengedragsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Kostengedrag is de classificatie van kosten als vast of variabel.
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 392cb83ceb8612a2e73cc54bb2d8d40c62a6b7b6
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Een kostengedragsbeleid maken en toewijzen aan een kostenbeheereenheid

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kostengedrag is de classificatie van kosten als vast of variabel. Een beleid en de bijbehorende regels moeten worden toegewezen aan een kostenbeheereenheid wil het beleid van kracht worden. Gebruik deze procedure om een beleid te maken en het vervolgens toe te wijzen aan een kostenbeheereenheid.


## <a name="create-a-cost-behavior-hierarchy"></a>Een kostengedraghiërarchie maken
1. Ga naar Kostprijsboekhouding > Dimensies > Dimensiehiërarchieën.
2. Klik op Nieuw.
3. Klik op Maken.
4. Typ in het veld Naam van dimensiehiërarchie 'Kostengedraghiërarchie'.
5. Typ of selecteer een waarde in het veld Dimensie.
    * Selecteer Kostenelementen.  
6. Klik op Opslaan.
7. Klik op Hiërarchie weergeven.
8. Klik op Nieuw.
9. Typ een waarde in het veld Naam knooppunt.
    * Voer Vaste kosten in.  
10. Selecteer in de structuur 'Kostengedraghiërarchie'.
11. Klik op Nieuw.
12. Typ een waarde in het veld Naam knooppunt.
    * Voer Variabele kosten in.  
13. Klik op Opslaan.
14. Selecteer in de structuur 'Kostengedraghiërarchie\Vaste kosten'.
15. Klik op Nieuw.
16. Markeer in de lijst de geselecteerde rij.
17. Typ of selecteer een waarde in het veld Van dimensielid.
    * Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.  
18. Typ of selecteer een waarde in het veld Tot dimensielid.
    * Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.  
19. Selecteer in de structuur 'Kostengedraghiërarchie\Variabele kosten'.
20. Klik op Nieuw.
21. Markeer in de lijst de geselecteerde rij.
22. Typ of selecteer een waarde in het veld Van dimensielid.
    * Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.  
23. Typ of selecteer een waarde in het veld Tot dimensielid.
    * Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.  
24. Klik op Opslaan.

## <a name="create-the-policy-and-rules"></a>Het beleid en regels maken
1. Ga naar Kostprijsboekhouding > Beleid > Kostengedragbeleidslijnen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Beleid.
4. Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.
    * Selecteer de beleidshiërarchie die u zojuist hebt gemaakt.  
5. Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.
    * Selecteer Organisatie.  
6. Klik op Opslaan.
7. Klik op Nieuw.
8. Markeer in de lijst de geselecteerde rij.
9. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.
    * Vouw de hiërarchie uit om Variabele kosten te selecteren.  
10. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
    * Standaard is het variabele percentage 100 procent.  
11. Klik op Beleidstoewijzingen voor kostenbeheereenheid.
12. Klik op Nieuw.
13. Markeer in de lijst de geselecteerde rij.
14. Typ een datum in het veld Geldig vanaf boekhouddatum.
    * De regels zijn datumregels en een regel kan vervallen door een gebruiker of door het systeem, als een nieuwere versie wordt gemaakt.  
15. Typ of selecteer een waarde in het veld Kostenbeheer.
16. Klik op Opslaan.



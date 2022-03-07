---
title: Een kostengedragsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Kostengedrag is de classificatie van kosten als vast of variabel.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58f888a373af33832c24518fbb5483c3de2d1a58
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208698"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Een kostengedragsbeleid maken en toewijzen aan een kostenbeheereenheid

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
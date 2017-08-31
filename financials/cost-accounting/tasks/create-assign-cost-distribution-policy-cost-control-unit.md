--- 
title: Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Kostenverdelingsregels worden gebruikt om kosten te verdelen die financieel zijn geteld in een collectieve kostenplaats.
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 492e4a94ec0caef8c51a691043a1ffb9e6a04758
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kostenverdelingsregels worden gebruikt om kosten te verdelen die financieel zijn geteld in een collectieve kostenplaats. De kostenaccountant zorgt dat de kosten worden gedistribueerd naar de kostencentra, op basis van de geselecteerde toewijzingsgrondslag. Een beleid en de bijbehorende regels worden toegewezen aan een kostenbeheereenheid. Deze taakbegeleider gebruikt een voorbeeld om te laten zien hoe u een beleid voor distributie van kosten en de bijbehorende regels maakt.


## <a name="create-a-policy"></a>Een beleid maken
1. Ga naar Kostprijsboekhouding > Beleid > Kostenverdelingsbeleid.
2. Klik op Nieuw.
3. Typ een waarde in het veld Beleid.
4. Typ een waarde in het veld Omschrijving.
5. Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.
    * Selecteer Organisatie.  
6. Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.
    * Selecteer CDS P/L.  
7. Typ of selecteer een waarde in het veld Statistische dimensie.
    * Selecteer Statistische elementen.  
8. Klik op Opslaan.

## <a name="create-rules-for-the-policy"></a>Regels voor het beleid maken
1. Klik op Nieuw.
2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
    * Vouw de sectie te selecteren hiërarchie 094 uit.  
4. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.
    * Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605110 Reiniging.  
5. Selecteer een optie in het veld Kostengedrag.
    * Selecteer Vaste kosten  
6. Typ of selecteer een waarde in het veld Toewijzingsgrondslag.
7. Klik op Nieuw.
8. Markeer in de lijst de geselecteerde rij.
9. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
    * Vouw de sectie te selecteren hiërarchie 094 uit.  
10. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.
    * Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605150 Huur.  
11. Selecteer een optie in het veld Kostengedrag.
    * Selecteer Vaste kosten  
12. Typ of selecteer een waarde in het veld Toewijzingsgrondslag.
13. Klik op Opslaan.

## <a name="assign-rules-to-a-cost-control-unit"></a>Regels aan een kostenbeheereenheid toewijzen
1. Klik op Beleidstoewijzingen voor kostenbeheereenheid.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een datum in het veld Geldig vanaf boekhouddatum.
    * Selecteer 1 september in het geldige boekjaar.  
5. Typ of selecteer een waarde in het veld Kostenbeheer.
6. Klik op Opslaan.



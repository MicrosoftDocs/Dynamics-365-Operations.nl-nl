--- 
title: Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid.
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid. Deze registratie gebruikt het USP2-demogegevensbedrijf.


## <a name="create-a-policy"></a>Een beleid maken
1. Ga naar Kostprijsboekhouding > Beleid > Beleidslijnen voor kostprijstoewijzing.
2. Klik op Nieuw.
3. Typ een waarde in het veld Beleid.
4. Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.
    * Selecteer Organisatie.  
5. Typ of selecteer een waarde in het veld Statistische dimensie.
6. Klik op Opslaan.

## <a name="create-allocation-rules"></a>Toewijzingsregels maken
1. Klik op Nieuw.
2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
4. Selecteer 'Totaal' in het veld Kostengedrag.
5. Typ of selecteer een waarde in het veld Toewijzingsgrondslag.
6. Klik op Nieuw.
7. Markeer in de lijst de geselecteerde rij.
8. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
9. Selecteer 'Totaal' in het veld Kostengedrag.
10. Typ of selecteer een waarde in het veld Toewijzingsgrondslag.
11. Klik op Nieuw.
12. Markeer in de lijst de geselecteerde rij.
13. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
14. Selecteer 'Totaal' in het veld Kostengedrag.
15. Typ of selecteer een waarde in het veld Toewijzingsgrondslag.
    * Ga door totdat u alle regels hebt gemaakt.  
16. Klik op Opslaan.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Het beleid toewijzen aan een kostenbeheereenheid
1. Klik op Beleidstoewijzingen voor kostenbeheereenheid.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een datum in het veld Geldig vanaf boekhouddatum.
    * De regels zijn datumregels. Een gebruiker of het systeem kan de regels laten vervallen wanneer een nieuwere versie wordt gemaakt.  
5. Typ of selecteer een waarde in het veld Kostenbeheer.
6. Klik op Opslaan.



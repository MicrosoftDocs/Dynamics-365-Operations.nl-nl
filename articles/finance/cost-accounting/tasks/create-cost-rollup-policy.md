---
title: Beleid voor totalisering van kosten maken
description: Deze procedure laat zien hoe u een beleid voor het totaliseren van kosten maakt en regels voor het beleid maakt.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50a50dc359dc4c2741ac4d280a9f97c6a7f2c259
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810009"
---
# <a name="create-a-cost-rollup-policy"></a>Beleid voor totalisering van kosten maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een beleid voor het totaliseren van kosten maakt en regels voor het beleid maakt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.


## <a name="create-a-policy"></a>Een beleid maken
1. Ga naar Kostprijsboekhouding > Beleid > Beleidslijnen voor totalisering van kosten.
2. Klik op Nieuw.
3. Typ een waarde in het veld Beleid.
4. Typ een waarde in het veld Omschrijving.
5. Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.
    * Selecteer Kosten totaliseren CC.  
6. Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.
    * Selecteer Kosten totaliseren CC.  
7. Klik op Opslaan.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Regels maken voor het beleid voor totalisering van kosten
1. Klik op Nieuw.
2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
    * Selecteer 007.  
4. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.
    * Selecteer Kosten totaliseren CE.  
5. Typ of selecteer een waarde in het veld Secundair kostenelement.
    * Wijs voor dit voorbeeld het secundaire kostenelement CC-007 toe aan de kostenplaats.  
6. Klik op Nieuw.
7. Markeer in de lijst de geselecteerde rij.
8. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
    * Selecteer 008.  
9. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.
    * Selecteer Kosten totaliseren CE.  
10. Typ of selecteer een waarde in het veld Secundair kostenelement.
    * Wijs voor dit voorbeeld het secundaire kostenelement CC-008 toe aan de kostenplaats.  
11. Klik op Nieuw.
12. Markeer in de lijst de geselecteerde rij.
13. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.
    * Selecteer 009.  
14. Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.
    * Selecteer Kosten totaliseren CE.  
15. Typ of selecteer een waarde in het veld Secundair kostenelement.
    * Wijs voor dit voorbeeld het secundaire kostenelement CC-009 toe aan de kostenplaats.  
    * Ga door totdat alle kostenplaatsen zijn toegewezen aan de overeenkomstige secundaire kostenelementen.  
16. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Kostenverdelingsregels worden gebruikt om kosten te verdelen die financieel zijn geteld in een collectieve kostenplaats.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: CAMCostDistributionRule
ms.openlocfilehash: 23adea279cad3fcf69cc6926d6f8dee485150221
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272393"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

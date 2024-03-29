---
title: Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid.
author: twheeloc
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5082f4e80958ddb1e4a79bfe46df4a621f10fc40
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734242"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid

[!include [banner](../../includes/banner.md)]

Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid. Deze registratie gebruikt het USP2-demogegevensbedrijf.


## <a name="create-a-policy"></a>Een beleid maken
1. Ga naar **Kostprijsboekhouding > Beleid > Beleidslijnen voor kostprijstoewijzing**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Beleidsnaam**.
4. Typ of selecteer een waarde in het veld **Dimensiehiërarchie van een kostenobject**.
    * Selecteer Organisatie.  
5. Typ of selecteer een waarde in het veld **Statistische dimensie**.
6. Klik op **Opslaan**.

## <a name="create-allocation-rules"></a>Toewijzingsregels maken
1. Klik op **Nieuw**.
2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld **Dimensiehiërarchieknooppunt van een kostenobject**.
4. Selecteer 'Totaal' in het veld **Kostengedrag**.
5. Typ of selecteer een waarde in het veld **Toewijzingsgrondslag**.
6. Klik op **Nieuw**.
7. Markeer in de lijst de geselecteerde rij.
8. Typ of selecteer een waarde in het veld **Dimensiehiërarchieknooppunt van een kostenobject**.
9. Selecteer 'Totaal' in het veld **Kostengedrag**.
10. Typ of selecteer een waarde in het veld **Toewijzingsgrondslag**.
11. Klik op **Nieuw**.
12. Markeer in de lijst de geselecteerde rij.
13. Typ of selecteer een waarde in het veld **Dimensiehiërarchieknooppunt van een kostenobject**.
14. Selecteer 'Totaal' in het veld **Kostengedrag**.
15. Typ of selecteer een waarde in het veld **Toewijzingsgrondslag**.
    * Ga door totdat u alle regels hebt gemaakt.  
16. Klik op **Opslaan**.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Het beleid toewijzen aan een kostenbeheereenheid
1. Klik op **Beleidstoewijzingen voor kostenbeheereenheid**.
2. Klik op **Nieuw**.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een datum in het veld **Geldig vanaf boekhouddatum**.
    * De regels zijn datumregels. Een gebruiker of het systeem kan de regels laten vervallen wanneer een nieuwere versie wordt gemaakt.  
5. Typ of selecteer een waarde in het veld **Kostenbeheer**.
6. Klik op **Opslaan**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

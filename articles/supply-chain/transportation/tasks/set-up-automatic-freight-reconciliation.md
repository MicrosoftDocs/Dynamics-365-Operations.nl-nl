--- 
title: Automatische vrachtafstemming instellen
description: Deze procedure laat zien hoe u gegevens instelt voor automatische vrachtafstemming.
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 61b795d52d4d2586db7f42a976790ee8608e179b
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>Automatische vrachtafstemming instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u gegevens instelt voor automatische vrachtafstemming. Dit wordt gewoonlijk uitgevoerd door een magazijnmanager. U kunt deze procedure gebruiken in het demobedrijf USMF.


## <a name="set-up-the-freight-bill-type"></a>Stel het vrachtfactuurtype in
1. Ga naar Transportbeheer > Instellen > Vrachtafstemming > Type vrachtfactuur.
    * Het type vrachtrekening bepaalt hoe de vrachtrekeningen en vervoerderfacturen moeten worden afgestemd.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Vrachtfactuur.
4. Typ in het veld Engine-assembly 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.
    * Dit is de standaardcodebibliotheek voor de afstemmingsengine Transportbeheer.  
5. Typ in het veld Engineklasse 'Microsoft.Dynamics.Ax.Tms.dll'.
    * Dit is de standaardklasse voor de afstemmingsengine Transportbeheer.  
6. Klik op Nieuw.
7. Kies in het veld Omschrijving de waarde die moet overeenkomen op de vrachtrekening en de vervoerderfactuur.  
8. Selecteer Ja in het veld Overeenkomst vereist.
    * Als u dit veld instelt op Ja, betekent dit dat de geselecteerde waarde in het veld Omschrijving overeen moet komen met de vrachtfactuur en de vervoerderfactuur. Als u dit instelt op Nee, kan het veld in een van deze leeg zijn.  
9. Klik op Opslaan.

## <a name="set-up-the-freight-bill-type-assignment"></a>Stel de toewijzing van het vrachtfactuurtype in
1. Sluit de pagina.
2. Ga naar Transportbeheer > Instellen > Vrachtafstemming > Type toewijzingen van vrachtfractuur.
    * De toewijzing van de vrachtrekening wordt gebruikt om op te geven welk type vrachtrekening voor een bepaalde vervoerder wordt gebruikt.   
3. Klik op Nieuw.
4. Typ of selecteer een waarde in het veld Modus.
5. Typ of selecteer een waarde in het veld Vervoerder.
6. Selecteer in het veld Type vrachtfactuur het type vrachtfactuur dat u eerder hebt gemaakt.
7. Sluit de pagina.

## <a name="set-up-the-audit-master"></a>Stel het controlemodel in
1. Ga naar Transportbeheer > Instellen > Vrachtafstemming > Controlemodel.
    * Het controlemodel bepaalt de tolerantielimieten voor automatische vrachtafstemming. Het specificeert met hoeveel de monetaire bedragen op de vrachtrekening en de vervoerderfactuur kunnen verschillen en toch nog afstemming toestaan. Het bepaalt ook hoe om verschillen worden verwerkt.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Controlemodel-id.
4. Selecteer in het veld Vervoerder dezelfde vervoerder als eerder.
5. Selecteer in het veld Type vrachtfactuur het type vrachtfactuur dat u eerder hebt gemaakt.
6. Vouw de sectie Tolerantie uit.
7. Typ een getal in het veld Minimumtolerantie.
8. Typ een getal in het veld Maximumtolerantie.
9. Vouw de sectie Resultaat uit.
10. Typ of selecteer een waarde in het veld Redencode voor overbetaling.
    * Als de monetaire bedragen op de vrachtrekening en de vervoerderfactuur verschillen, geven de redencodes voor overbetaling en onderbetaling de rekeningen aan waarop het verschil moet worden geregistreerd, zolang het verschil binnen de tolerantieniveaus is.  
11. Typ of selecteer een waarde in het veld Redencode voor onderbetaling.
12. Sluit de pagina.


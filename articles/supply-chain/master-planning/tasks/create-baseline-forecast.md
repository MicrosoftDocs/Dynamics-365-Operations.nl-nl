---
title: Een basislijnprognose maken
description: Een productieplanner kan een basislijnprognose maken of door prognosemodellen voor de tijdreeks te gebruiken of door de historische vraag naar de prognose te kopiëren.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85d687c0c21112f815bb5cf28b0af5501d299c12
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148119"
---
# <a name="create-a-baseline-forecast"></a>Een basislijnprognose maken

[!include [banner](../../includes/banner.md)]

Een productieplanner kan een basislijnprognose maken of door prognosemodellen voor de tijdreeks te gebruiken of door de historische vraag naar de prognose te kopiëren. Deze procedure laat zien hoe u de historische vraag kopieert om een basislijnprognose te maken voor alle producten met één artikeltoewijzingssleutel. 


## <a name="set-up-an-item-allocation-key"></a>Een artikeltoewijzingssleutel instellen
1. Ga naar Hoofdplanning > Instellingen > Intercompany-planningsgroepen.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld Naam met een waarde van "10".
    * Vraagprognose uitvoeren voor verschillende rechtspersonen. Daarom moet u alle bedrijven instellen waarvoor u prognoses wilt genereren in één intercompany-planningsgroep.  
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik op Artikeltoewijzingssleutels.
    * Selecteer alle artikeltoewijzingssleutels waarvoor u prognoses wilt maken.  
5. Markeer in de lijst de geselecteerde rij.
    * Selecteer de artikeltoewijzingssleutel D_Aloc.  
6. Klik op >.
7. Sluit de pagina.
8. Sluit de pagina.

## <a name="set-up-the-demand-forecasting-paramters"></a>De parameters voor vraagprognose instellen
1. Ga naar Hoofdplanning > Instellingen > Vraagprognose > Parameters voor vraagprognose.
2. Vouw de sectie Parameters van prognosealgoritme uit.
3. Selecteer in het veld Strategie voor aanmaken van vraagprognose de optie Kopieer over historische vraag.
4. Klik op Opslaan.

## <a name="create-a-baseline-forecast"></a>Een basislijnprognose maken
1. Ga naar Hoofdplanning > Prognose > Vraagprognose > Statistische basislijnprognose maken.
2. Voer een datum in het veld Begindatum in.
    * Als u verkooporders hebt die vanaf 1 januari 2015 beginnen, voert u deze datum in. Als dat niet zo is, voert u de vroegste datum van uw verkooporders in.  
3. Voer een datum in het veld Einddatum in.
    * Voer de laatste datum van uw verkooporders in, bijvoorbeeld 31-03-2015.  
4. Voer een datum in het veld Begindatum in.
    * Voer '01-04-2015' in. Deze datum wordt automatisch berekend als begindatum van de volgende prognoseverzameling.  
5. Breid de sectie Op te nemen records uit.
6. Klik op Filter.
7. Markeer in de lijst de geselecteerde rij.
    * Markeer de rij waarbj Veld = intercompany-planningsgroep.  
8. Typ een waarde in het veld Criteria.
    * Typ de intercompany-planningsgroep, bijvoorbeeld 10, die u in de eerste taak hebt gebruikt.  
9. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de rij waarbij Veld = Artikeltoewijzingssleutel.  
10. Typ een waarde in het veld Criteria.
11. Klik op OK.
12. Vouw de sectie Geavanceerde parameters uit.
13. Selecteer Maand in het veld Prognoseverzameling.
14. Voer "3" in het veld Prognoseperiode in.
15. Voer 1 in het veld Blokkering van de tijdlimiet in.
16. Klik op OK.

## <a name="visualize-the-demand-forecast"></a>De vraagprognose visualiseren
1. Ga naar Hoofdplanning > Prognose > Vraagprognose > Gecorrigeerde vraagprognose.
2. Selecteer in de tabel met de samengestelde weergave de cel in rij 1, kolom 2. Dit is de tweede maand waarvoor u een prognose hebt gemaakt.
3. Stel QtyCell in op "400".
    * Voer in de cel een afwijkend aantal in dan was geraamd, bijvoorbeeld 400.  
4. U hebt een handmatige correctie van de prognose uitgevoerd. Zie de grafische indicatie in de volgende stap.
5. Klik op Regeldetails voor prognose.
    * Op deze pagina kunt u de nauwkeurigheidswaarden, de historische vraag en de prognose weergeven. U kunt ook wijzigingen aanbrengen in de prognose.  


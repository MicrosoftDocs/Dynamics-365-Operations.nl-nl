---
title: Een hoofdplanningsuitvoering controleren
description: De productieplanner wil zien of er een hoofdplanning wordt uitgevoerd.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845108"
---
# <a name="monitor-a-master-planning-run"></a>Een hoofdplanningsuitvoering controleren

[!include [task guide banner](../../includes/task-guide-banner.md)]

De productieplanner wil zien of er een hoofdplanning wordt uitgevoerd. Gebruik het demobedrijf USMF om deze procedure te voltooien.


## <a name="run-master-planning"></a>Hoofdplanning uitvoeren
1. Klik op Hoofdplanning.
    * U vindt dit in het standaarddashboard.  
2. Typ of selecteer een waarde in het veld Plan.
    * Voorbeeld: StaticPlan  
3. Klik op Uitvoeren.
4. Selecteer Ja in het veld Verwerkingstijd traceren.
    * Als het veld al is geselecteerd, slaat u deze stap over.  
5. Voer een getal in het veld Aantal threads in.
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Markeer in de lijst de geselecteerde rij.
    * Markeer de rij waarin Veld = Artikelnummer.  
9. Typ of selecteer een waarde in het veld Criteria.
    * Voorbeeld: T0001  
10. Klik op OK.
11. Klik op OK.

## <a name="monitor-the-master-planning-run"></a>De hoofdplanningsuitvoering controleren
1. Klik op Historie.
2. Klik op Query's.
3. Klik op Duur procestaak.
4. Zoek en selecteer de gewenste record in de lijst.
    * Voor elk artikel kunt u een overzicht krijgen van de tijd die de voltooiing van elke planningsstap in beslag nam.  


---
title: Uitgaande geplande intercompany-vraag weergeven
description: Dit onderwerp biedt een procedure die laat zien hoe u uitgaande geplande intercompany-vraag weergeeft.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39f2c1ad6fa6f282d9e281e4d1ed9483d45f096a
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469386"
---
# <a name="view-outbound-planned-intercompany-demand"></a>Uitgaande geplande intercompany-vraag weergeven

[!include [banner](../../includes/banner.md)]

Deze procedure beschrijft hoe u alle geplande orders kunt weergeven die door een intercompany-leverancier worden vervuld. Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.

1. Selecteer **Hoofdplanning**.
2. Typ of selecteer een waarde in het veld **Plannen**.
    * Selecteer in het veld **Plan** de optie plan *10*.  
3. Selecteer *Uitvoeren*.
4. Voer een getal in het veld **Aantal threads** in.
    * Dit vertegenwoordigt het aantal parallelle threads dat voor de hoofdplanning moet worden gebruikt.  
5. Selecteer **OK**.
    * Dit kan enige tijd duren.  
6. Selecteer **Geplande intercompany-vraag**.
7. Selecteer **Uitgaande geplande intercompany-vraag**.
    * Deze pagina biedt een overzicht van alle geplande vraag die door een interne toeleverancier wordt vervuld.  
8. Vouw de sectie **Details van upstream vraag** uit.
    * In deze sectie ziet u de details voor de wijze waarop de vraag wordt vervuld. U moet mogelijk wachten totdat de hoofdplanning is uitgevoerd in het toeleveringsbedrijf, voordat u hier aanvullende informatie kunt zien.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

--- 
title: Een intercompany-plan maken
description: Deze procedure laat zien hoe u een intercompany-plan maakt.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7c7f466add55fb9a24c3fb8f1f92df712a8622e3
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-intercompany-plan"></a>Een intercompany-plan maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een intercompany-plan maakt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Intercompany-planningsgroep instellen 
1. Ga naar Intercompany-planningsgroepen.
    * Hoofdplanning > Instellingen > Intercompany-planningsgroepen  
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld Naam met een waarde van "10".
3. Markeer in de lijst de geselecteerde rij.
4. Klik op Verwijderen.
    * Deze stap is nodig om het maken van de intercompany-planning in te korten.   Intercompany-planning voert hoofdplanning uit in alle bedrijven in een planningsgroep, te beginnen met de laagste schemareeks.  
5. Klik op Ja.
6. Sluit de pagina.

## <a name="create-an-intercompany-plan"></a>Een intercompany-plan maken
1. Klik op Intercompany-hoofdplanning.
    * Dit is in het Hoofdplanningwerkgebied.  
2. Klik in het veld Intercompany-planningsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer Intercompany-planningsgroep 10.  
4. Typ 2 in het veld Aantal intercompany-planningsherhalingen.
    * Intercompany-planningsgroep 10 heeft twee leden. Om de vertragingen van het bronbedrijf (USMF) door te voeren naar het klantbedrijf (DEMF), moet u intercompany in beide bedrijven twee keer uitvoeren. De eerste herhaling voert de vraag door en geeft de vertragingen in het bronbedrijf (USMF) aan. Bij de tweede herhaling worden de vertragingen van de USMF naar DEMF doorgevoerd.  
5. Selecteer een optie in het veld Eerste iteratie.
6. Selecteer Opnieuw genereren in het veld Eerste iteratie.
7. Selecteer Opnieuw genereren in het veld Volgende iteraties.
8. Voer een getal in het veld Aantal threads in.
    * Dit geeft het aantal parallelle threads aan dat voor planning wordt gebruikt.  
9. Klik op OK.

## <a name="view-the-result-of-the-plan"></a>Het resultaat van het plan weergeven
1. Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Klik op de koppeling voor StaticPlan. U moet in het bedrijf USMF zijn.  
3. Klik op Geplande orders.



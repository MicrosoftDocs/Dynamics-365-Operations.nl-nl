---
title: Een intercompany-plan maken
description: Deze procedure laat zien hoe u een intercompany-plan maakt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7fe8d155b39190f6c0ee1ee310a5edd2400623c
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916709"
---
# <a name="create-an-intercompany-plan"></a>Een intercompany-plan maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een intercompany-plan maakt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Intercompany-planningsgroep instellen 
1. Ga in het **navigatievenster** naar **Modules > Hoofdplanning > Instellingen > Intercompany-planningsgroepen**. 
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld Naam met een waarde van "10".
3. Markeer in de lijst de geselecteerde rij.
4. Klik op **Verwijderen**. Deze stap is nodig om het maken van de intercompany-planning in te korten.   Intercompany-planning voert hoofdplanning uit in alle bedrijven in een planningsgroep, te beginnen met de laagste schemareeks.  
5. Klik op **Ja**.
6. Sluit de pagina.

## <a name="create-an-intercompany-plan"></a>Een intercompany-plan maken
1. Ga in het **navigatievenster** naar **Modules > Hoofdplanning > Werkgebieden > Hoofdplanning**.
2. Klik op **Intercompany-hoofdplanning**.  
3. Klik in het veld **Intercompany-planningsgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij. Selecteer Intercompany-planningsgroep 10.  
5. Typ 2 in het veld **Aantal intercompany-planningsherhalingen**. Intercompany-planningsgroep 10 heeft twee leden. Om de vertragingen van het bronbedrijf (USMF) door te voeren naar het klantbedrijf (DEMF), moet u intercompany in beide bedrijven twee keer uitvoeren. De eerste herhaling voert de vraag door en geeft de vertragingen in het bronbedrijf (USMF) aan. Bij de tweede herhaling worden de vertragingen van de USMF naar DEMF doorgevoerd.  
6. Selecteer Opnieuw genereren in het veld **Eerste iteratie**.
7. Selecteer Opnieuw genereren in het veld **Volgende iteraties**.
8. Voer een getal in het veld **Aantal threads** in. Dit geeft het aantal parallelle threads aan dat voor planning wordt gebruikt.  
9. Klik op **OK**.

## <a name="view-the-result-of-the-plan"></a>Het resultaat van het plan weergeven
1. Klik in het veld **Plan** op de vervolgkeuzeknop om de zoekopdracht te openen.
2. Klik in de lijst op de koppeling in de geselecteerde rij. Klik op de koppeling voor StaticPlan. U moet in het bedrijf USMF zijn.  
3. Klik op **Geplande orders**.


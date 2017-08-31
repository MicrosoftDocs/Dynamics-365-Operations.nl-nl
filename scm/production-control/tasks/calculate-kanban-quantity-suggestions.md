--- 
title: Suggesties voor kanbanhoeveelheid berekenen
description: Deze procedure is gericht op optimaliseren van de kanbangrootte en -hoeveelheden voor een specifieke kanbanregel door gebruik te maken van de berekening van de kanbanhoeveelheid.
author: ChristianRytt
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 7416e0407892281377b69a7a3b19e61f46220709
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="calculate-kanban-quantity-suggestions"></a>Suggesties voor kanbanhoeveelheid berekenen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht op optimaliseren van de kanbangrootte en -hoeveelheden voor een specifieke kanbanregel door gebruik te maken van de berekening van de kanbanhoeveelheid. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de waardestroombeheerder. Het is een vereiste dat u de procedure Een beleid voor berekening van de kanbanhoeveelheid toevoegen aan een kanbanregel hebt uitgevoerd.


## <a name="create-a-kanban-quantity-calculation"></a>Een berekening van een kanbanhoeveelheid maken
1. Ga naar Productiebeheer > Periodieke taken > Berekening kanbanhoeveelheid > Kanbanhoeveelheid berekenen.
2. Klik op Nieuw.
3. Typ "Speaker2016" in het veld Naam.
4. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer het beleid dat u hebt gemaakt in de procedure Een beleid voor berekening van de kanbanhoeveelheid toevoegen aan een kanbanregel. Bijvoorbeeld Speaker2016.  
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Stel in het veld "Regel actief vanaf datum" de datum en tijd in op "2012-12-17T08:00:00".
    * Deze datum dient als basis om te bepalen welke vaste kanbanregels in de kanbanberekening worden opgenomen.  
7. Stel in het veld "Begindatum behaalde vraagperiode" de datum en tijd in op "2012-11-17T09:00:00".
    * De datum vanaf wanneer voorbije aanvraagtransacties worden opgenomen om de kanbanhoeveelheid te berekenen.  
8. Stel in het veld "Einddatum behaalde vraagperiode" de datum en tijd in op "2012-12-17T07:59:59".
    * De datum tot wanneer voorbije transacties worden opgenomen om de kanbanhoeveelheid te berekenen.  
9. Stel in het veld "Begindatum vraagperiode" de datum en tijd in op "2012-12-17T08:00:00".
    * De datum vanaf wanneer huidige vraagtransacties worden opgenomen om de kanbanhoeveelheid te berekenen.  
10. Stel in het veld "Einddatum vraagperiode" de datum en tijd in op "2013-01-16T07:59:59".
    * De datum tot wanneer huidige vraagtransacties worden opgenomen om de kanbanhoeveelheid te berekenen.  

## <a name="generate-kanban-quantity-proposal"></a>Voorstel voor kanbanhoeveelheid genereren
1. Klik op Opslaan.
2. Klik op Genereren.
    * Hiermee wordt een voorstelregel voor de kanbanhoeveelheid gegenereerd voor kanbanregel 000020.  

## <a name="run-kanban-quantity-calculation"></a>Berekening van kanbanhoeveelheid uitvoeren
1. Klik op Berekenen.
    * Hiermee wordt het voorstel voor de kanbanhoeveelheid berekend.  
2. Klik op OK.
3. Markeer in de lijst de geselecteerde rij.
    * De voorgestelde kanbanhoeveelheid is 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Producthoeveelheid wijzigen en opnieuw berekenen
1. Stel Producthoeveelheid in op "5".
2. Klik op Berekenen.
3. Klik op OK.
    * Merk op dat bij een kanbanhoeveelheid van 5, het voorstel wordt gewijzigd in een kanbanhoeveelheid van 4.  
    * Dit wordt veroorzaakt door het feit dat er bij een lagere producthoeveelheid meer kanbans nodig zijn om aan de vraag te voldoen.  

## <a name="update-kanban-rule"></a>Kanbanregel bijwerken
1. Voer in het veld Datum regel van kracht een datum en tijd in.
    * Stel de datum bij "Regel actief vanaf datum" in op een datum in de toekomst. Bijvoorbeeld, vandaag + één jaar.  
2. Klik op Bijwerken.
3. Klik op OK.
4. Sluit de pagina.

## <a name="validate-change-on-kanban-rule"></a>Wijziging op kanbanregel valideren
1. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer de kanbanregel die in de vorige deeltaak is gemaakt. Dit moet de eerste kanbanregel in de lijst zijn die is gesorteerd op nummer.  
3. Schakel de uitbreiding van de sectie Details om.
    * Let op de ingangsdatum, die betekent dat deze regel niet vóór deze datum wordt geactiveerd.  
4. Schakel de uitbreiding van de sectie Hoeveelheden om.
    * Merk op dit de standaardhoeveelheid is die u bij de berekening van de kanbanhoeveelheid hebt ingevoerd.  
    * Merk op dit de vaste kanbanhoeveelheid van 4 is van de berekening van de kanbanhoeveelheid.  
5. Klik op het tabblad Lijstpaneel.



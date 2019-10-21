---
title: EUR-00011 Genereren van het rapport ICL-lijst.
description: Deze procedure begeleidt u bij het genereren van het rapport van de EU-verkooplijst.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7038af3977797a0be2523f2414800400757b7007
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183815"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a>EUR-00011 Genereren van het rapport ICL-lijst.

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure begeleidt u bij het genereren van het rapport van de EU-verkooplijst. Dit omvat het overboeken van intracommunautaire handelstransacties naar de EU-verkooplijst en het uitvoeren van het rapport. Deze procedure omvat ook het maken van een intracommunautair handelstransactie voor demodoeleinden. Raadpleeg voor meer informatie over EU-verkooplijstrapportage, met inbegrip van vereisten, de Help.

Deze procedure is van toepassing op alle Europese landen/regio's. De procedure werd gemaakt met de demogegevens van het bedrijf DEMF en dus Duitsland als voorbeeld voor land/regio. De procedure maakt ook gebruik van Portugal als voorbeeld van EU-land/-regio. Voordat u deze procedure kunt uitvoeren, moet u het rapporteren van de EU-verkooplijst configureren.

Deze procedure is alleen bedoeld voor accountants.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>Een intracommunautaire verkooptransactie voor demodoeleinden maken
1. Ga naar Klanten > Orders > Alle verkooporders.
2. Klik op Nieuw.
3. Typ 'PRT-001' in het veld Klantrekening.
4. Klik op OK.
5. Typ in het veld Artikelnummer de waarde 'D0001'.
6. Vouw de sectie Regeldetails uit.
7. Klik op het tabblad Instellingen.
8. Typ 'VOL' in het veld Btw-groep voor artikel.
9. Klik op Regel toevoegen.
10. Typ in het veld Artikelnummer de waarde 'D0003'.
11. Typ 'ROOD' in het veld Btw-groep voor artikel.
12. Klik op Opslaan.
13. Klik in het actievenster op Factuur.
14. Klik op Factuur.
15. Vouw de sectie Parameters uit.
16. Selecteer in het veld Hoeveelheid de optie 'Alle'.
17. Vouw de sectie Instellingen uit.
18. Stel de datum in het veld Factuurdatum in op '01/11/2016'.
19. Klik op OK.
20. Klik op OK.

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>Intracommunautaire handelstransacties naar de EU-verkooplijst overboeken
1. Ga naar Belasting > Aangiften > Buitenlandse handel > ICL-lijst.
2. Klik op Overbrengen.
3. Selecteer Ja in het veld Artikel om artikeltransacties over te boeken.
4. Selecteer Ja in het veld Service om servicetransacties over te boeken.
    * U kunt ook extra filters op intracommunautair handelstransacties opgeven voor overboeking.  
5. Klik op Overbrengen.
    * Controleer of de intracommunautaire verkooptransactie goed is overgeboekt naar de EU-verkooplijst.  

## <a name="generate-the-eu-sales-list-report"></a>Het rapport van de EU-verkooplijst genereren
1. Klik op Rapportage.
2. Selecteer 'Maandelijks' in het veld Aangifteperiode.
3. Stel in het veld Begindatum de datum in op '01/01/2016'.
4. Selecteer Ja in het veld Bestand maken.
5. Selecteer Ja in het veld Rapport maken.
6. Typ 'EUSalesList' in het veld Bestandsnaam.
7. Typ 'EUSalesList' in het veld Bestandsnaam van rapport.
8. Typ '123' in het veld Registratie-id van EU-verkooplijst.
    * Dit veld is alleen beschikbaar voor Duitsland.  
    * U kunt ook extra filters op intracommunautair handelstransacties opgeven om in het rapport op te nemen.  
9. Klik op OK.
    * Controleer of de pop-upvensters worden weergegeven om te bevestigen dat het bestand en het controlerapport worden gedownload.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>Regels van EU-verkooplijst markeren als Gerapporteerd
1. Klik op Markeren.
2. Klik op Markeren als gerapporteerd.
3. Selecteer in de lijst de rij voor het veld Factuurnummer.
4. Typ '01/01/2016..01/31/2016' in het veld Criteria.
5. Selecteer in de lijst de rij voor het veld Rapportagestatus.
6. Selecteer 'Opgenomen' in het veld Criteria.
    * U kunt ook extra filters op intracommunautair handelstransacties opgeven om te markeren als Gerapporteerd.  
7. Klik op OK.
8. Selecteer 'Gerapporteerd' in het veld Selectie.

## <a name="mark-eu-sales-list-lines-as-closed"></a>Regels van EU-verkooplijst markeren als Afgesloten
1. Klik op Markeren.
2. Klik op Markeren als afgesloten.
3. Markeer in de lijst de rij voor het veld Factuurnummer.
4. Typ '01/01/2016..01/31/2016' in het veld Criteria.
5. Markeer in de lijst de rij voor het veld Rapportagestatus.
6. Selecteer 'Gerapporteerd' in het veld Criteria.
    * U kunt ook extra filters op intracommunautair handelstransacties opgeven om te markeren als Afgesloten.  
7. Klik op OK.
8. Selecteer 'Afgesloten' in het veld Selectie.


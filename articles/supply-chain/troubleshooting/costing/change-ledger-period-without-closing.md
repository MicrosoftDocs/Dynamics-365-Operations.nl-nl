---
title: Waarschuwingen of foutberichten over het wijzigen van de status van een grootboekperiode zonder de voorraad af te sluiten
description: Waarschuwingen of foutberichten over het wijzigen van de status van een grootboekperiode zonder de voorraad af te sluiten
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475998"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Waarschuwingen of foutberichten over het wijzigen van de status van een grootboekperiode zonder de voorraad af te sluiten

Microsoft heeft de volgende validaties geïntroduceerd om problemen te voorkomen die worden veroorzaakt door een onjuist periode-eindeproces in verband met kostprijsberekening. Als u een van de volgende foutberichten ontvangt, raadpleegt u [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) voor meer informatie over het oplossen van deze problemen.

- U staat op het punt een herberekening uit te voeren met datum %1 (10-02-2019). De laatste geregistreerde herberekening is in een vorige periode uitgevoerd met datum %2 (20-01-2019). Geen uitvoerbewerking geregistreerd van voorraadafsluiting met datum overeenkomend met datum %3 (31-01-2019) overeenkomend met een periode-einde. Vergeet niet om een voorraadafsluiting uit te voeren ingaande %3 (31-01-2019) overeenkomend met het periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd.

- U staat op het punt de status van grootboekperiode %1 te wijzigen in %2. Geen uitvoerbewerking geregistreerd van voorraadafsluiting met datum overeenkomend met datum %3 overeenkomend met een periode-einde. Voer een voorraadafsluiting uit ingaande %3 overeenkomend met het periode-einde voordat u de status wijzigt. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd. Gemeld door rechtspersoon %4. Nu is het informatief, maar voortaan is het verplicht om deze actie uit te voeren.

- De rekeningstructuur %1 is gewijzigd. Een of meer hoofdrekeningen %2 bestaan niet meer. Deze hoofdrekeningen zijn vereist voor de %3 met datum %4. Voeg deze hoofdrekeningen toe aan de rekeningstructuur %1 voordat u de taak %3 kunt hervatten. Nu is het informatief, maar voortaan is het verplicht om deze actie uit te voeren.

- U staat op het punt een voorraadafsluiting uit te voeren met datum %1 (31-01-2019). Geen uitvoerbewerking geregistreerd van kostprijsberekening via terugwaarts afboeken met datum %2 (31-01-2019) overeenkomend met een periode-einde. Vergeet niet een kostprijsberekening via terugwaarts afboeken uit te voeren met datum %3 (31-01-2019) overeenkomend met een periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd.

- U staat op het punt een kostprijsberekening voor terugwaarts afboeken uit te voeren met datum %1 (28-02-2019). De laatste geregistreerde kostprijsberekening voor terugwaarts afboeken is in een vorige periode uitgevoerd met datum %2 (31-01-2019). Geen uitvoerbewerking geregistreerd van voorraadafsluiting met datum %3 (31-01-2019) overeenkomend met een periode-einde.

Vergeet niet om een voorraadafsluiting uit te voeren ingaande %3 (31-01-2019) overeenkomend met een periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat de voorraadafsluiting is uitgevoerd.
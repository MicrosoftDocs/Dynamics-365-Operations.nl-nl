---
title: Problemen met kostenbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met kostenbeheer.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4425888"
---
# <a name="troubleshoot-cost-management"></a>Problemen met kostenbeheer oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met kostenbeheer.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Functionele hiaten tussen de voorraadwaardenrapporten/naar ouderdom gerangschikte voorraadrapporten en de opslagversies hiervan

Met de functies [Opslag naar ouderdom gerangschikt voorraadrapport](inventory-aging-report-storage.md) en [Rapport opslag van voorraadwaarden](inventory-value-report-storage.md) voor Supply Chain Management kunnen grote hoeveelheden voorraadtransacties worden weergegeven. In elk geval worden de rapportresultaten opgeslagen om te kunnen bekijken en exporteren, in tegenstelling tot de versies van deze rapporten die niet worden opgeslagen. Sommige functies in de niet-opgeslagen versies van deze rapporten bestaan echter niet in de opgeslagen versies. In de volgende subsecties vindt u een beknopt overzicht van de verschillen en oplossingen.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Opslagrapporten bevatten geen subtotalen, zelfs niet als deze zijn ingeschakeld in de rapportindeling

Subtotalen kunnen problemen veroorzaken wanneer het resultaat wordt geëxporteerd, vooral als gebruikers de recordvolgorde wijzigen.

Als u de subtotalen wilt controleren, kunt u het resultaat exporteren naar Microsoft Excel. Ook kunt u, als u subtotalen binnen Supply Chain Management wilt controleren, [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de functies *Nieuw rasterbesturingselement* en *(Preview) Groeperen in rasters* in te schakelen. Dit biedt een veel flexibelere manier om het subtotaal voor een groep per kolom te bekijken. Zie [Rastermogelijkheden](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md) voor meer informatie.

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Rapport opslag van voorraadwaarden biedt geen ondersteuning voor gegevens over grootboekrekeningen

U kunt de proefbalans uitvoeren om het voorraadrekeningensaldo op te halen en te vergelijken met het rapport **Opslag van voorraadwaarden**.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Er worden waarschuwingen of foutberichten weergegeven wanneer u de status van een grootboekperiode wijzigt zonder de voorraad af te sluiten

Microsoft heeft de volgende validaties geïntroduceerd om problemen te voorkomen die worden veroorzaakt door een onjuist periode-eindeproces in verband met kostprijsberekening. Als u een van de volgende foutberichten ontvangt, raadpleegt u [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) voor meer informatie over het oplossen van deze problemen.

- U staat op het punt een herberekening uit te voeren met datum %1 (10-02-2019). De laatste geregistreerde herberekening is in een vorige periode uitgevoerd met datum %2 (20-01-2019). Geen uitvoerbewerking geregistreerd van voorraadafsluiting met datum overeenkomend met datum %3 (31-01-2019) overeenkomend met een periode-einde. Vergeet niet om een voorraadafsluiting uit te voeren ingaande %3 (31-01-2019) overeenkomend met het periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd.

- U staat op het punt de status van grootboekperiode %1 te wijzigen in %2. Geen uitvoerbewerking geregistreerd van voorraadafsluiting met datum overeenkomend met datum %3 overeenkomend met een periode-einde. Voer een voorraadafsluiting uit ingaande %3 overeenkomend met het periode-einde voordat u de status wijzigt. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd. Gemeld door rechtspersoon %4. Nu is het informatief, maar voortaan is het verplicht om deze actie uit te voeren.

- De rekeningstructuur %1 is gewijzigd. Een of meer hoofdrekeningen %2 bestaan niet meer. Deze hoofdrekeningen zijn vereist voor de %3 met datum %4. Voeg deze hoofdrekeningen toe aan de rekeningstructuur %1 voordat u de taak %3 kunt hervatten. Nu is het informatief, maar voortaan is het verplicht om deze actie uit te voeren.

- U staat op het punt een voorraadafsluiting uit te voeren met datum %1 (31-01-2019). Geen uitvoerbewerking geregistreerd van kostprijsberekening via terugwaarts afboeken met datum %2 (31-01-2019) overeenkomend met een periode-einde. Vergeet niet een kostprijsberekening via terugwaarts afboeken uit te voeren met datum %3 (31-01-2019) overeenkomend met een periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat dit is uitgevoerd.

- U staat op het punt een kostprijsberekening voor terugwaarts afboeken uit te voeren met datum %1 (28-02-2019). De laatste geregistreerde kostprijsberekening voor terugwaarts afboeken is in een vorige periode uitgevoerd met datum %2 (31-01-2019). Geen uitvoerbewerking geregistreerd van voorraadafsluiting met datum %3 (31-01-2019) overeenkomend met een periode-einde.
Vergeet niet om een voorraadafsluiting uit te voeren ingaande %3 (31-01-2019) overeenkomend met een periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in journaal of grootboek totdat de voorraadafsluiting is uitgevoerd.

## <a name="inventory-aging-report-discrepancies"></a>Verschillen in naar ouderdom gerangschikt voorraadrapport

In het **Naar ouderdom gerangschikt voorraadrapport** worden verschillende waarden weergegeven wanneer ze worden weergegeven in verschillende opslagdimensies (zoals locatie of magazijn). Zie [Voorbeelden en logica voor naar ouderdom gerangschikt voorraadrapport](inventory-aging-report.md) voor informatie de rapportlogica.
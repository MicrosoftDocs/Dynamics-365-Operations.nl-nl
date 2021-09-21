---
title: Functionele hiaten tussen de voorraadwaarderapporten/naar ouderdom gerangschikte voorraadrapporten en de opslagversies hiervan
description: Functionele hiaten tussen de voorraadwaarderapporten/naar ouderdom gerangschikte voorraadrapporten en de opslagversies hiervan
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476036"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Functionele hiaten tussen de voorraadwaarderapporten/naar ouderdom gerangschikte voorraadrapporten en de opslagversies hiervan

Met de functies [Opslag naar ouderdom gerangschikt voorraadrapport](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md) en [Rapport opslag van voorraadwaarden](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) voor Supply Chain Management kunnen grote hoeveelheden voorraadtransacties worden weergegeven. In elk geval worden de rapportresultaten opgeslagen om te kunnen bekijken en exporteren, in tegenstelling tot de versies van deze rapporten die niet worden opgeslagen. Sommige functies in de niet-opgeslagen versies van deze rapporten bestaan echter niet in de opgeslagen versies. In de volgende subsecties vindt u een beknopt overzicht van de verschillen en oplossingen.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Opslagrapporten bevatten geen subtotalen, zelfs niet als deze zijn ingeschakeld in de rapportindeling

Subtotalen kunnen problemen veroorzaken wanneer het resultaat wordt geëxporteerd, vooral als gebruikers de recordvolgorde wijzigen.

Als u de subtotalen wilt controleren, kunt u het resultaat exporteren naar Microsoft Excel. Ook kunt u, als u subtotalen binnen Supply Chain Management wilt controleren, [Functiebeheer](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de functies *Nieuw rasterbesturingselement* en *Groeperen in rasters* in te schakelen. Dit biedt een veel flexibelere manier om het subtotaal voor een groep per kolom te bekijken. Zie [Rastermogelijkheden](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md) voor meer informatie.

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Rapport opslag van voorraadwaarden biedt geen ondersteuning voor gegevens over grootboekrekeningen

U kunt de proefbalans uitvoeren om het voorraadrekeningensaldo op te halen en te vergelijken met het rapport **Opslag van voorraadwaarden**.

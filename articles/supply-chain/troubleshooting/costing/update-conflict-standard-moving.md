---
title: Updateconflict wanneer de voorraadwaarderingsmethode standaardkosten of zwevend gemiddelde is
description: Updateconflict opgetreden wanneer de voorraadwaarderingsmethode standaardkosten of zwevend gemiddelde is
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
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476042"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Updateconflict opgetreden wanneer de voorraadwaarderingsmethode standaardkosten of zwevend gemiddelde is

## <a name="symptoms"></a>Symptomen

Wanneer u documenten, zoals voorraadjournalen, inkooporderfacturen of verkooporderfacturen, gelijktijdig voor schaalbaarheid en prestaties boekt, wordt er mogelijk een foutbericht weergegeven over een updateconflict en worden sommige documenten mogelijk niet geboekt. Dit probleem kan optreden wanneer de voorraadwaarderingsmethode *Standaardkosten* of *Zwevend gemiddelde* is Beide methoden zijn permanente kostprijsmethoden. Dit wil zeggen dat de uiteindelijke kosten worden bepaald tijdens het boeken.

Als u de methode *Zwevend gemiddelde* gebruikt, lijkt het foutbericht op dit voorbeeld:

> Voorraadwaarde xx,xx wordt niet verwacht na de berekening van proportionele onkosten

Als u de methode *Standaardkosten* gebruikt, lijkt het foutbericht op dit voorbeeld:

> De standaardkosten komen niet overeen met de financiële voorraadwaarde na het bijwerken. Waarde = xx,xx, Hoeveelheid = yy,yy, Standaardkosten = zz,zz

## <a name="workaround"></a>Tijdelijke oplossing

Voordat Microsoft met een oplossing voor het probleem komt, moet u overwegen de volgende oplossingen te gebruiken om deze fouten te voorkomen of te verminderen:

- De mislukte documenten opnieuw boeken.
- Documenten met minder regels maken.
- Decimale waarden in de standaardkosten vermijden. Probeer de standaardkosten te definiëren zodat het veld **Prijshoeveelheid** wordt ingesteld op *1*. Als u een waarde voor de **Prijshoeveelheid** van meer dan *1* moet opgeven, moet u proberen het aantal decimalen in de standaardkosten per eenheid te minimaliseren. (In de ideale situatie moeten er minder dan twee decimalen zijn.) Vermijd bijvoorbeeld standaardkosteninstellingen zoals **Prijs** = *10* en **Prijshoeveelheid** = *3* te definiëren, omdat hiermee standaardkosten per eenheid van 3,333333 worden geproduceerd (waarbij de decimale waarde wordt herhaald).
- Probeer in de meeste documenten te voorkomen dat er meerdere regels zijn met dezelfde combinatie van product- en financiële voorraaddimensies.
- De mate van parallellisatie verminderen. (In dit geval kan het systeem sneller worden, omdat er minder updateconflicten zijn en er minder nieuwe pogingen worden ondernomen.)

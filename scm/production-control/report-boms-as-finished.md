---
title: Rapport gereedmelden van stuklijsten
description: Dit artikel bevat informatie over het gereedmelden van stuklijsten.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 318c88f88277a8300b1fcda5056a9a92c9a81eae
ms.lasthandoff: 03/31/2017


---

# <a name="report-boms-as-finished"></a>Rapport gereedmelden van stuklijsten

Dit artikel bevat informatie over het gereedmelden van stuklijsten.

De pagina's **Gereedmelden** en **Maximale gereedmelding** worden gebruikt om stuklijsten (BOMs) te melden als zijnde gereed. Conceptueel is het proces voor een stuklijst als voltooid rapporteren hetzelfde als het proces voor gereedmelden van een productieorder. Dit proces kan worden gebruikt in bijvoorbeeld eenvoudige processen voor maken en kitting, waar de geavanceerdere mogelijkheden van productieorders niet zijn vereist. Met de pagina **Gereedmelden** kunt u meerdere stuklijsten in een batch gereedmelden. De **Max. gereedmelden** pagina kunt u slechts één stuklijst gereedmelden tegelijk. De **gereedmelden** pagina is beschikbaar vanuit een menu-item in Voorraadbeheer en beide pagina's beschikbaar zijn als een menu-items op de **vrijgegeven producten** pagina.

## <a name="report-as-finished-page"></a>Pagina Gereedmelden
Als u de pagina **Gereedmelden ** van een vrijgegeven product opent, suggereert de pagina dat u de standaardhoeveelheid van de standaardvoorraad gereedmeldt. Standaard wordt de actieve stuklijstversie weergegeven, maar u kunt de stuklijstversie wijzigen als er andere goedgekeurde versies zijn. Op de pagina kunt u ook registraties verwijderen en nieuwe records voor vrijgegeven producten maken, die moeten worden gereedgemeld. Om een query te gebruiken om producten te selecteren, klikt u op het menu-item **Selecteren**. U kunt handmatig rapportage bevestigen als voltooid voor de geselecteerde producten door te klikken op **OK**. U kunt ook instellen dat het proces wordt uitgevoerd in een batch. Wanneer het proces Gereedmelden is bevestigd, genereert het systeem een stuklijstjournaal waarin het boeken naar de voorraad is verwerkt. Dit journaal bestaat uit één regelartikel voor het eindproduct en een regelartikel voor elke stuklijstregel. U kunt controleren of het journaal automatisch wordt geboekt of wordt opengelaten voor aanvullende correcties.

## <a name="max-report-as-finished-page"></a>Max. Rapport als voltooide pagina
Op de pagina **Maximale gereedmelding** geeft elke stuklijstregel het aantal stuks van het product aan dat kan worden gereedgemeld. Deze berekening wordt gebaseerd op de beschikbare voorhanden materiële voorraad van elke materiaalregel. In het volgende voorbeeld verbruikt een stuk van het artikelnummer FG twee stuks van grondstof RM10 en een stuk van grondstof RM20. Omdat er maar 10 stuks van RM10 voorradig zijn, bedraagt de maximale hoeveelheid van FG die kan worden gereedgemeld vijf stuks. Deze waarde wordt weergegeven in het veld **Maximale gereedmelding**.

| Niveau | Artikelnummer | Hoeveelheid | Voorhanden | Max. Rapporteren als gereed |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Stuklijsten met meerdere niveaus
Wanneer een stuklijst meerdere niveaus heeft, kunt u bepalen hoe de materialen worden verantwoord op alle niveaus door het veld **Explosie** te gebruiken. Dit veld is zowel beschikbaar op de pagina **Gereedmelden** als op de pagina **Maximale gereedmelding**. De volgende opties zijn beschikbaar:

-   **Nooit**: onderliggende stuklijsten worden niet geëxplodeerd bij een materiaaltekort.
-   **Altijd**: alle onderliggende stuklijsten worden geheel geëxplodeerd. Dit betekent dat eventuele vrije voorhanden voorraad voor halfvoltooide componentartikelen niet wordt gebruikt.
-   **Tekort**: onderliggende stuklijsten worden alleen geëxplodeerd als de gehele hoeveelheid van het gewenste materiaal niet beschikbaar is.

### <a name="example"></a>Voorbeeld

In dit voorbeeld zijn drie stuks van het eindproduct (artikelnummer FG) gereed om worden gereedgemeld. Er is een stuklijst op twee niveaus, zoals hier weergegeven.

| Niveau | Artikelnummer | Hoeveelheid stuklijstregel | Voorhanden |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

De volgende tabellen tonen hoe de instelling van het veld **Explosie** de wijze beïnvloedt waarop de journaalregels van de stuklijst worden gegenereerd. **Explosie: Nooit**

| Niveau | Artikelnummer | Hoeveelheid |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -3       |

Als de voorgaande tabel staat, alleen artikelnummer COMP wordt beschouwd als in het journaal in mindering gebracht. Artikelnummer RM, dat deel van COMP uitmaakt, aan de journaalregel is niet geëxplodeerd en de twee stuks van de voorhanden voorraad van COMP niet worden beschouwd. **Explosie: Altijd**

| Niveau | Artikelnummer | Hoeveelheid |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

In dit geval wordt het artikelnummer COMP geëxplodeerd in zijn grondstof, artikelnummer RM. De twee voorhanden stuks COMP worden niet meegenomen in de te verbruiken hoeveelheid RM. **Explosie: Tekort**

| Niveau | Artikelnummer | Hoeveelheid |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

In dit geval worden de twee voorhanden stuks van artikelnummer COMP meegenomen. Echter, omdat drie stuks van artikelnummer FG vereist zijn, is één stuk van artikelnummer RM ook vereist om het aanvullende ene stuk van COMP te maken.



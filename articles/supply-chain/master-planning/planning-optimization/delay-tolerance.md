---
title: Vertragingstolerantie (negatieve dagen)
description: Dit artikel bevat informatie over de berekening van vertragingstolerantie en over het effect ervan op het maken van geplande orders in Planningsoptimalisatie.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4bd6042f9dd33ba15773b251911e965cb870c5aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865116"
---
# <a name="delay-tolerance-negative-days"></a>Vertragingstolerantie (negatieve dagen)

[!include [banner](../../includes/banner.md)]

Door de functionaliteit voor vertragingstolerantie kan in Planningsoptimalisatie rekening worden houden met de waarde voor **Negatieve dagen** die is ingesteld voor behoefteplanningsgroepen. Deze wordt gebruikt om de vertragingstolerantieperiode te verlengen die wordt toegepast tijdens de hoofdplanning. Op deze manier voorkomt u dat u nieuwe aanvulorders maakt als het bestaande aanbod na korte tijd aan de vraag kan voldoen. Het doel van de functionaliteit is te bepalen of het zin heeft om een nieuwe aanvulorder voor een bepaalde vraag te maken.

## <a name="turn-on-the-feature-in-your-system"></a>De functie inschakelen in uw systeem

Als u de functionaliteit voor vertragingstolerantie beschikbaar wilt maken in uw systeem, gaat u naar [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Negatieve dagen voor Planningsoptimalisatie* in.

## <a name="delay-tolerance-in-planning-optimization"></a>Vertragingstolerantie in Planningsoptimalisatie

Vertragingstolerantie is het aantal dagen na de levertijd die u wilt wachten voordat u nieuwe aanvulling bestelt wanneer een bestaand aanbod al is gepland. Vertragingstolerantie wordt gedefinieerd met behulp van kalenderdagen, niet werkdagen.

Wanneer de vertragingstolerantie wordt berekend bij de hoofdplanning, wordt rekening gehouden met de instelling **Negatieve dagen**. U kunt de **Negatieve dagen**-waarde opgeven op de pagina **Behoefteplanningsgroepen** of de pagina **Artikelbehoefteplanning**.

De berekening van de vertragingstolerantie wordt door het systeem aan de *vroegste aanvullingsdatum* gekoppeld. Dit is gelijk aan de datum van vandaag plus de levertijd. De vertragingstolerantie wordt berekend met behulp van de volgende formule, waarbij *max()* het grootste aantal waarden heeft gevonden:

*max(Vroegste aanvullingsdatum, Vervaldatum vraag)* – *Vervaldatum vraag* + *Negatieve dagen*

Met deze formule wordt gegarandeerd dat er door de hoofdplanning geen nieuwe aanvulorders worden gemaakt wanneer er voldoende aanbod bestaat tijdens de productlevertijd.

> [!NOTE]
> Bij de berekening van vertragingstolerantie in Planningsoptimalisatie wordt altijd de dynamische, berekening van negatieve dagen gebruikt op basis van de ingebouwde hoofdplanning. De instelling **Dynamische, negatieve dagen gebruiken** op de pagina **Parameters hoofdplanning** heeft geen effect op dit gedrag.

Als het bestaande aanbod een uitgestelde vraag geeft die kleiner is dan of gelijk is aan de berekende vertragingstolerantie, zorgt Planningsoptimalisatie ervoor dat het bestaande aanbod aan de vraag wordt gekoppeld. In sommige gevallen is het beter de vraag uit te stellen dan te eindigen met een overaanbod.

In de volgende subsecties staan voorbeelden die laten zien welke vertragingstolerantie van invloed is op het maken van geplande orders in Planningsoptimalisatie.

### <a name="example-1"></a>Voorbeeld 1

Een product heeft de volgende configuratie:

- **Levertijd:** *10*
- **Negatieve dagen:** *2*

De volgende vraag en aanbod bestaan voor het product:

- **Vraag voor vandaag:** een verkooporder voor een hoeveelheid van 10
- **Aanbod in 12 dagen:** een inkooporder voor een hoeveelheid van 10

Het bestaande aanbod kan binnen 12 dagen de vraag dekken en deze periode is gelijk aan de vertragingstolerantie. Wanneer de hoofdplanning wordt uitgevoerd, worden er dus geen geplande orders gemaakt.

### <a name="example-2"></a>Voorbeeld 2

Een product heeft de volgende configuratie:

- **Levertijd:** *10*
- **Negatieve dagen:** *0*

De volgende vraag en aanbod bestaan voor het product:

- **Vraag voor vandaag:** een verkooporder voor een hoeveelheid van 10
- **Aanbod in 12 dagen:** een inkooporder voor een hoeveelheid van 10

Bestaand aanbod kan de vraag pas na twaalf 12 dekken. De vertragingstolerantie is echter 10 dagen. Wanneer de hoofdplanning wordt uitgevoerd, wordt daarom een geplande order gemaakt voor een hoeveelheid van 10.

### <a name="example-3"></a>Voorbeeld 3

Een product heeft de volgende configuratie:

- **Levertijd:** *10*
- **Negatieve dagen:** *2*

De volgende vraag en aanbod bestaan voor het product:

- **Vraag in 11 dagen:** een verkooporder voor een hoeveelheid van 10
- **Aanbod in 14 dagen:** een inkooporder voor een hoeveelheid van 10

Bestaand aanbod kan de vraag pas na drie dagen dekken. De vertragingstolerantie is echter twee dagen. (In dit geval omvat de vertragingstolerantie alleen de twee negatieve dagen. De vraagdatum wordt niet opgenomen omdat deze na de levertijd van het product is.) Wanneer de hoofdplanning wordt uitgevoerd, wordt een geplande order gemaakt voor een hoeveelheid van 10.

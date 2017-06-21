---
title: Updates voor standaardkosten beheren
description: "Updates van standaardkostengegevens kunnen worden beheerd met twee verschillende benaderingen: de benadering met één versie en de benadering met twee versies."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d1d498b1a843415e106c90330dd661b78bc2865e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="manage-standard-cost-updates"></a>Updates voor standaardkosten beheren

[!include[banner](../includes/banner.md)]


Updates van standaardkostengegevens kunnen worden beheerd met twee verschillende benaderingen: de benadering met één versie en de benadering met twee versies. 

Bij de benadering met één versie wordt één kostprijsberekeningsversie gebruikt die alle kostenregistraties bevat. Deze registraties omvatten de oorspronkelijke koten en alle kostenupdates.
Bij de methode met twee versies wordt één versie gebruikt die registraties van de oorspronkelijke kosten bevat en een tweede versie die registraties alle van kostenupdates bevat. Het belangrijkste voordeel van de methode met twee versies is de duidelijke afbakening en tracering van kostenupdates in een aparte kostprijsberekeningsversie, zonder dat dit gevolgen heeft voor de oorspronkelijke kostprijsberekeningsversie. De methode met twee versies kan worden gebruikt om meerdere incrementele updates te identificeren, waarbij elke incrementele update een aparte kostprijsberekeningsversie heeft die de incrementele kostenrecords bevat. **Voorbeeld** Het volgende voorbeeld illustreert hoe de methoden met één versie en met twee versies kunnen worden gebruikt voor het bijwerken van standaardkosten in een productieomgeving. Bijvoorbeeld updates die nieuwe artikelen of foutcorrecties weerspiegelen. Ga ervanuit dat één kostprijsberekeningsversie de standaardkosten voor het huidige jaar voorstelt. De id voor deze versie is 2016-STD. Versie 2016-STD bevat de huidige actieve kosten voor alle artikelen. Bovendien bevat ze alle route-gerelateerde kostencategorieën en overheadberekeningsformules die aan het begin van het jaar 2016 bekend waren. 2016-STD is de oorspronkelijke kostprijsberekeningsversie.
-   **Methode met één versie voor updates van kostengegevens** − In de methode met één versie, bevat de oorspronkelijke kostprijsberekeningsversie 2016-STD alle kostenregistraties. Kostenupdates worden in 2016-STD vastgelegd en de status ervan wordt ingesteld op “In behandeling.” De kosten in behandeling kunnen handmatig worden ingevoerd voor nieuw ingekochte artikelen of ze kunnen worden berekend voor een gefabriceerd artikel om correcties weer te geven. Wanneer de methode met één versie wordt gebruikt, vereisen de stuklijstberekeningen geen terugvalgegevensbron omdat alle actieve kosten in de kostprijsberekeningsversie zijn opgenomen. Nadat de kosten in behandeling actief worden, bevat de oorspronkelijke kostprijsberekeningsversie 2016-STD opnieuw alle huidige actieve kosten.
-   **Methode met twee versies voor updates van kostengegevens** − De methode met twee versies vereist een extra kostprijsberekeningsversie die alleen de kostenupdates bevat. De id voor deze versie is 2016-STD-WIJZIGINGEN. De kostenupdates worden geregistreerd in 2016 STD-WIJZIGINGEN vastgelegd en hun status wordt ingesteld op “In behandeling”. Bij de methode met twee kostprijsberekeningsversies vereisen de stuklijstberekeningen van kosten in behandeling voor gefabriceerde artikelen een terugvalgegevensbron. Dit is zo omdat de extra kostprijsberekeningsversie 2016-STD-WIJZIGINGEN alleen een subset van kostengegevens bevat. De terugval kan worden uitgedrukt als de actieve kosten, of als de opgegeven kostprijsberekeningsversie 2016-STD, omdat beide de bron van kostengegevens identificeren wanneer die niet bestaat in 2016-STD-WIJZIGINGEN. Nadat de kosten in behandeling zijn geactiveerd, zal de kostprijsberekeningsversie 2016-STD-WIJZIGINGEN de huidige actieve kosten bevatten die de updates reflecteren, terwijl de oorspronkelijke kostprijsberekeningsversie 2016-STD ongewijzigd blijft. Wanneer de methode met twee versies wordt gebruikt, moet blokkeerbeleid voor de oorspronkelijke kostprijsberekeningsversie worden ingesteld om updates te voorkomen. De extra kostprijsberekeningsversie moet precies hetzelfde blokkeringsbeleid hebben als de oorspronkelijke kostprijsberekeningsversie, met uitzondering van de opgegeven begindatum en het selectieve gebruik van blokkeringsbeleid om updates toe te staan. De opgegeven begindatum moet bij elke batch wijzigingen worden bijgewerkt om de geplande activeringsdatum te reflecteren.

In het voorgaande voorbeeld werd één extra kostprijsberekeningsversie gebruikt om updates tijdens het jaar 2016 te beheren. Er kan meer dan een extra kostprijsberekeningsversie worden gebruikt, bijvoorbeeld een aparte versie voor elke batch met updates. Wanneer meer dan één extra kostprijsberekening wordt gebruikt, dan moet de terugval worden uitgedrukt als de actieve kosten, omdat de actieve kosten over meerdere kostprijsberekeningsversies zijn verdeeld.







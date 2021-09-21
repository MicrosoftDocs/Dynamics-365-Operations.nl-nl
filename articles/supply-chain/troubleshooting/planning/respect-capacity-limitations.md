---
title: In Hoofdplanning is meer gepland dan de beschikbare capaciteit
description: De capaciteitsbeperkingen worden niet door de hoofdplanning in acht genomen en er wordt meer dan de beschikbare capaciteit gepland.
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476026"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>In Hoofdplanning is meer gepland dan de beschikbare capaciteit

## <a name="symptoms"></a>Symptomen

De capaciteitsbeperkingen worden niet door de hoofdplanning in acht genomen en er wordt meer dan de beschikbare capaciteit gepland.

Wanneer u bewerkingsplanning gebruikt waarbij er sprake is van een eindige capaciteit en waar in de route een combinatie van vereisten voor zowel een resourcegroep als afzonderlijke resources is opgegeven, is er een kleine kans op overboeking door de manier waarop het algoritme de validatie van capaciteitsconflicten valideert. Deze overboeking kan optreden wanneer u helpers gebruikt om de hoofdplanning uit te voeren. Dit wordt waarschijnlijk veroorzaakt door een groot aantal taken met een relatief korte runtime.

## <a name="resolution"></a>Oplossing

Als het van essentieel belang is dat er geen overboekingen plaatsvinden voor de bewerkingsplanning, kunt u het planningsgedeelte van de hoofdplanning met afzonderlijke threads maken door de optie **Nauwkeurige eindige capaciteit voor bewerkingsplanning** in te schakelen op de pagina **Parameters hoofdplanning**. Deze optie is niet standaard beschikbaar. U moet dit handmatig aan de pagina toevoegen met behulp van de functies voor persoonlijke instellingen. Wanneer u deze optie gebruikt, wordt de planning langzamer uitgevoerd vanwege het gebrek aan parallelle verwerking.

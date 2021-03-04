---
title: Voorraadlocaties
description: Voorraadlocaties worden met basale magazijnen (WMS I) gebruikt om te bepalen waar artikelen worden opgeslagen en waar artikelen uit worden verzameld in een WMS I-magazijn.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 490f510ca0a5522d7bc892733ff066ebc65bcd24
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425850"
---
# <a name="inventory-locations"></a>Voorraadlocaties

[!include [banner](../includes/banner.md)]

Voorraadlocaties worden met basale magazijnen (WMS I) gebruikt om te bepalen waar artikelen worden opgeslagen en waar artikelen uit worden verzameld in een WMS I-magazijn.

Dit onderwerp geldt voor functies in de module voor Voorraadbeheer. Het geldt niet voor functies in de module Magazijnbeheer.

De term locatie verwijst naar de plaats waar artikelen worden opgeslagen en opgehaald.

Voor elke locatie kan ook de plaats worden opgegeven waar het artikel wordt ingevoegd. Standaard zijn deze gelijk. Meestal worden artikelen aan dezelfde kant van de locatie ingevoegd en opgehaald, maar niet altijd. Zo worden artikelen in opslagrekken aan de ene kant in de rekken geplaatst en aan de andere kant uit de rekken gehaald. De belangrijkste invoer is een locatienaam, die meestal door de coördinaten ervan wordt gedefinieerd: magazijn, gang, rek, plank en bak. Deze naam of id kan op de pagina Voorraadlocaties handmatig worden ingevoerd of worden gegenereerd op basis van de coördinaten van de locatie, bijvoorbeeld 01-02-03-4 voor gang 1, rek 2, plank 3, bak 4.
Locatie-eigenschappen

Een locatie heeft de volgende kenmerken:
-   Grootte (hoogte, breedte, diepte, en dus volume)
-   Magazijn, gang, rek, plank en bakpositie
-   Locatietype (bulklocatie, orderverzamellocatie, inbound dock, outbound dock, productieinvoerlocatie, inspectielocatie, of kanbansupermarkt)

Met controletekst kan in onlinesystemen worden gecontroleerd of de operator de juiste locatie voor een bepaald artikel heeft geselecteerd. Deze controletekst kan handmatig of standaard door het systeem worden gemaakt.

## <a name="sort-codes"></a>Sorteercodes
Met sorteercodes kunt u de afhandeling van orderverzamelregels optimaliseren. Deze regels bevatten de gegevens die nodig zijn om artikelen uit de voorraad op te halen zoals de volgorde waarin de orders worden verzameld. Sorteercodes kunnen worden opgegeven met de gang en de andere coördinaten, of handmatig voor de locatie worden toegewezen.

## <a name="blocked-locations"></a>Geblokkeerde locaties
Soms wilt u wellicht aangeven dat een locatie gedurende een bepaalde tijd is geblokkeerd, bijvoorbeeld om reparaties mogelijk te maken. Op andere momenten wilt u mogelijk aangeven dat alleen de invoer of alleen de uitvoer is geblokkeerd.

## <a name="tree-structure"></a>Boomstructuur

Op de pagina Voorraadlocaties kunt u de magazijnindeling bekijken in een boomstructuur in een bepaalde weergave-indeling op basis van de coördinaten van voorraadlocaties.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Voorraadlocaties onderhouden via het formulier voor magazijnbeheer

Het is mogelijk om locaties van het ene magazijn naar het andere te kopiëren en locaties via een wizard te maken. Voordat u de wizard uitvoert, moet u ervoor zorgen dat u de standaardlocatienamen hebt gedefinieerd op de pagina Magazijn.



<a name="additional-resources"></a>Aanvullende resources
--------

[Een nieuwe magazijnindeling maken](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
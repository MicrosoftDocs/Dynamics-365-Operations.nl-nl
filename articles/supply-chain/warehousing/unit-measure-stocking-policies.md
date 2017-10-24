---
title: Maateenheid en opslagbeleid
description: Dit artikel beschrijft hoe de standaardeenheden, eenheidsvolgorden, en eenheidsomrekeningen worden gebruikt in magazijnprocessen.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80bd5978ffe137e48da3f5eac6c75ad0f5e2f06a
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# Maateenheid en opslagbeleid

[!include[banner](../includes/banner.md)]


Dit artikel beschrijft hoe de standaardeenheden, eenheidsvolgorden, en eenheidsomrekeningen worden gebruikt in magazijnprocessen.

Eenheidsvolgordegroepen bepalen de volgorde van eenheden die in magazijnbewerkingen kunnen worden gebruikt. Deze worden gemaakt op de pagina **Volgordegroepen eenheid**. De volgorde laat de relatie tussen de verschillende eenheden zien. Zo slaat u bijvoorbeeld pallets op die dozen bevatten die individuele artikelen bevatten. In dit geval, moet u de drie verschillende eenheden en de logische volgorde van de lagen opgeven. Met eenheidsvolgordegroepen kunt u de beleidsregels definiëren voor groepering van nummerplaten en de standaardeenheden die voor verschillende magazijnprocessen moeten worden gebruikt. Dit artikel is zowel van toepassing op de geavanceerde magazijnoplossing die in Magazijnbeheer beschikbaar als op de meer elementaire magazijnoplossing die beschikbaar is in Voorraadbeheer.

## Eenheidvolgordegroepen voor vrijgegeven producten
Als u vrijgegeven producten wilt gebruiken in processen voor magazijnwerk, moet hieraan een eenheidvolgordegroep worden toegewezen. Als u een product valideert dat aan een opslagdimensiegroep is gekoppeld, en de optie **HMagazijnbeheerprocessen gebruiken** voor de voorraaddimensiegroep is ingesteld op **Ja**, ontvangt u een foutbericht als geen id voor een eenheidvolgordegroep is gedefinieerd voor het product. Als de eenheidvolgordegroep die u gebruikt meerdere regels (en daarmee meerdere eenheden) bevat, moet u een eenheidsomrekening tussen de eenheden instellen. U voltooit deze instellingen op de pagina **Eenheidsconversies**. De kleinste eenheid in een volgordegroep die u aan een artikel koppelt met een vrijgegeven product moet overeenstemmen met de voorraadeenheid die voor het overeenkomstige product is gedefinieerd. De voorraadeenheid is de eenheid die voor basisberekeningen van de voorhanden voorraad wordt gebruikt. U kunt ook maateenheidsconversies voor productvarianten van productmodellen instellen door de optie **Maateenheidconversies inschakelen** te gebruiken.

## Nummerplaatgroepering
U kunt opgeven of ontvangstbewijzen van minder dan of meer dan een specifieke eenheid moeten worden gegroepeerd in een nummerplaat of opgedeeld in een nummerplaat voor elke eenheid. U kunt dit gedrag instellen door de optie **Nummerplaatgroepering** op het tabblad **Regeldetails** van de pagina **Volgordegroepen eenheid** te gebruiken. Als u de nummerplaatgroepering wilt gebruiken bij het verwerken van werk met een mobiel apparaat, moet u de optie **Nummerplaatgroepering** in de menuoptie **Mobiel apparaat**. Als u bijvoorbeeld een mobiel apparaat gebruikt om een artikel te registreren dat is gekoppeld aan een eenheidvolgordegroep die twee regels bevat. De eerste regel is voor stuks, en de optie **Nummerplaatgroepering** is ingesteld op **Ja**. De tweede regel is voor de eenheid Pallet, en de optie **Nummerplaatgroepering** is ingesteld op **Nee**. In dit geval kan het systeem automatisch het splitsen en maken van 100 stuks nummerplaten beheren.

## Eenheden voor cyclustelling
U kunt bepalen welke eenheden als onderdeel van de levenscyclus moeten worden gebruikt door de optie **Eenheid voor cyclustelling gebruiken** te selecteren op de pagina **Volgordegroepen eenheid**. U kunt maximaal vier eenheden selecteren in de volgordegroep. Als u meer dan vier eenheden selecteert, worden de extra eenheden niet weergegeven op het mobiele apparaat.

## Standaardeenheden voor ontvangstprocessen via mobiel apparaat
U kunt de standaardeenheden instellen die voor het ontvangen van processen op mobiele apparaten moeten worden gebruikt, door de opties **Standaardeenheid voor inkoop en overboeking** en **Standaardeenheid voor productie** in te schakelen op de pagina **Volgordegroepen eenheid**. Zo kunt u bijvoorbeeld opgeven dat, standaard, het systeem Pallethoeveelheden moet gebruiken wanneer de inkooporder voor voorhanden voorraad wordt ontvangen met een mobiel apparaat, maar dat de voorraadeenheid Stuks moet zijn. U kunt de conversie voor het aantal stuks dat elke pallet bevat bepalen door een eenheidsomrekening te definiëren, zoals 100 stuks = 1 pallet.

## Standaard orderinstellingen
Als onderdeel van het maken van vrijgegeven producten, moet u standaardeenheden voor inkoop, verkoop, en voorraad selecteren om de verschillende orders te verwerken. U kunt de standaardeenheden en de hoeveelheden voor de diverse brondocumenten instellen door gebruik te maken van de pagina's **Standaard orderinstellingen** en **Vestigingspecifieke orderinstellingen**. U kunt deze pagina's openen vanaf de pagina **Vrijgegeven producten**.





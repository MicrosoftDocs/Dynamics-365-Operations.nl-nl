---
title: Planning met negatieve voorhanden hoeveelheden
description: In dit artikel wordt uitgelegd hoe negatieve voorhanden hoeveelheden worden verwerkt.
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b4fc8b37fd800e3b4652513f150f9806bf1d5d67
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741117"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planning met negatieve voorhanden hoeveelheden

[!include [banner](../../includes/banner.md)]

Als in het systeem een negatieve cumulatieve hoeveelheid voorhanden voorraad wordt weergegeven, behandelt de planningsengine de hoeveelheid als 0 (nul) om te voorkomen dat er te veel voorraad wordt geleverd. Deze functionaliteit werkt als volgt:

1. Met de hoofdplanning worden voorhanden hoeveelheden op het laagste niveau van de behoefteplanningsdimensies samengevoegd. (Als *locatie* bijvoorbeeld geen behoefteplanningsdimensie is, worden in de hoofdplanning de voorhanden hoeveelheden geaggregeerd op het niveau *magazijn*.)
1. Als de totale voorhanden voorraad op het laagste niveau van de behoefteplanningsdimensies negatief is, wordt er in het systeem van uitgegaan dat de voorhanden voorraad in werkelijkheid 0 (nul) is.

> [!IMPORTANT]
> De nauwkeurigheid van het planningssysteem is afhankelijk van de invoergegevens. Als de invoergegevens onjuist zijn, geven negatieve voorhanden records aan dat de voorraadinformatie in Microsoft Dynamics 365 Supply Chain Management niet meer synchroon loopt met de echte wereld. Daarom bevat het planningsresultaat fouten. Om een nauwkeurig planningsresultaat te krijgen, moet u het aantal records beperken dat een negatieve voorhanden hoeveelheid weergeeft.

## <a name="example-1"></a>Voorbeeld 1

Magazijn 13 wordt op de volgende manier geconfigureerd:

- **Behoefteplanningscode:** Min./Max.
- **Minimum:** 15 stuks (st)
- **Maximum:** 25 st.

Het laagste niveau van behoefteplanningsdimensies is *magazijn* en de volgende voorhanden hoeveelheden worden geregistreerd op het niveau *locatie*:

- **Vestiging 1, magazijn 13, locatie 1:** 20 st.
- **Vestiging 1, magazijn 13, locatie 2:** &minus;8 st.

Daarom is de gecumuleerde voorhanden hoeveelheid voor magazijn 13 12 st. (= 20 st. &minus; 8 st.).

In dit geval gebruikt de planningsengine een cumulatieve voorhanden hoeveelheid van 12 st. voor magazijn 13.

Het resultaat is een geplande order van 13 st. (= 25 st. &minus; 12 st.) om magazijn 13 opnieuw te vullen op basis van 12 st. tot 25 st.

## <a name="example-2"></a>Voorbeeld 2

Magazijn 13 wordt op de volgende manier geconfigureerd:

- **Behoefteplanningscode:** Min./Max.
- **Minimum:** 15 st.
- **Maximum:** 25 st.

Het laagste niveau van behoefteplanningsdimensies is *magazijn* en de volgende voorhanden hoeveelheden worden geregistreerd op het niveau *locatie*:

- **Vestiging 1, magazijn 13, locatie 1:** 4 st.
- **Vestiging 1, magazijn 13, locatie 2:** &minus;8 st.

Daarom is de gecumuleerde voorhanden hoeveelheid voor magazijn 13 &minus;4 st. (= 4 st. &minus; 8 st.). Dat wil zeggen dat de voorraad minder dan 0 (nul) is.

In dit geval gaat de planningsengine ervan uit dat de voorhanden hoeveelheid voor magazijn 13 0 st. bedraagt. in plaats van &minus;4 st.

Het resultaat is een geplande order van 25 st. (= 25 st. &minus; 0 st.) om magazijn 13 opnieuw te vullen op basis van 0 st. tot 25 st.

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Planning bij reservering tegen negatieve voorhanden voorraad

Als u de voorraad aanpast terwijl er fysieke reserveringen bestaan, kunt u een situatie veroorzaken waarin een order fysiek wordt gereserveerd tegen negatieve voorraad. Omdat er in dit geval sprake is van een fysieke reservering, moet u voorraad aangeleverd krijgen om de gereserveerde hoeveelheid te kunnen dekken. Dat vereist dus aanvulling. Er wordt dus een geplande order gemaakt om de hoeveelheid aan te vullen die niet kon worden gedekt door de bestaande voorraad of het wordt gedekt met een bestaande order voor het artikel.

Dit wordt geïllustreerd in het volgende voorbeeldscenario.

### <a name="example"></a>Voorbeeld

Het systeem wordt als volgt geconfigureerd:

- Product *FG* bestaat en heeft *10* st. voorhanden voorraad.
- Met de productconfiguratie is fysieke negatieve voorraad mogelijk.
- Er bestaat een verkooporder voor een hoeveelheid *van 10* st. van product *FG*.
- De verkooporderhoeveelheid wordt fysiek gereserveerd tegen de bestaande voorraad.

Vervolgens past u de hoeveelheid van product *FG* aan, zodat de voorhanden voorraad 5 wordt. Aangezien de voorhanden productvoorraad 5 is, wordt de hoeveelheid op de verkooporder nu gereserveerd op de hoeveelheid die niet voorhanden is (dit zou vergelijkbaar zijn als voorhanden voorraad 0 zou zijn, waarbij de verkooporder gereserveerd wordt op negatieve voorraad). Als u nu de hoofdplanning uitvoert, wordt er echter geen geplande order van 5 voor *FG* gemaakt om de verkooporder te leveren. Dit komt doordat de hoofdplanning altijd bestaande voorraad wordt gebruikt of een nieuwe geplande order wordt gemaakt om de fysieke reservering te leveren.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

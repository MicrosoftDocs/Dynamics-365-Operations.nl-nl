---
title: Planning met negatieve voorhanden hoeveelheden
description: In dit onderwerp wordt uitgelegd hoe negatieve voorhanden voorraad wordt verwerkt wanneer u planningsoptimalisatie gebruikt.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425414"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planning met negatieve voorhanden hoeveelheden

[!include [banner](../../includes/banner.md)]

Als in het systeem een negatieve cumulatieve hoeveelheid voorhanden voorraad wordt weergegeven, behandelt de planningsengine de hoeveelheid als 0 (nul) om te voorkomen dat er te veel voorraad wordt geleverd. Deze functionaliteit werkt als volgt:

1. Met de functie voor planningsoptimalisatie worden voorhanden hoeveelheden op het laagste niveau van de behoefteplanningsdimensies samengevoegd. (Als *locatie* bijvoorbeeld geen behoefteplanningsdimensie is, worden in planningsoptimalisatie de voorhanden hoeveelheden geaggregeerd op het niveau *magazijn*.)
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

## <a name="related-resources"></a>Gerelateerde bronnen

[Overzicht van Planningsoptimalisatie](planning-optimization-overview.md)

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Een planningstaak annuleren](cancel-planning-job.md)

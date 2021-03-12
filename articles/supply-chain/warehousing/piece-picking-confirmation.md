---
title: Bevestiging door stuksverzameling
description: In dit onderwerp wordt beschreven hoe u bevestiging voor stuksverzameling instelt en toepast vanaf een mobiel apparaat.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66903d142ecb7228e4fdec56dbd45472acbdeb69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989638"
---
# <a name="piece-picking-confirmation"></a>Bevestiging door stuksverzameling

[!include [banner](../includes/banner.md)]

Met stuksverzameling kunt u elk stuk in uw voorraad bevestigen via picking- of tellingswerk op een mobiel apparaat. Voor orderverzameling kunt u de hoeveelheid werk die moet worden verwerkt, bevestigen tot en met de hoeveelheid die is opgegeven op het werk dat moet worden gepickt. Voor tellingswerk kunt u de voorraad scannen die u telt en de totale hoeveelheid bijhouden.

Wanneer u stuksverzameling inschakelt, wordt productbevestiging automatisch ingeschakeld. Voor verzameling van het type werk wordt een maximum aantal stuks ingeschakeld. Zo kunt u een maximum instellen voor het aantal delen dat tijdens het werk moet worden bevestigd. De maximumhoeveelheid is gebaseerd op de huidige werkeenheid die wordt verwerkt. Werk van het type telling staat geen maximum toe.

U kunt ook de hoeveelheid en eenheid (maateenheid) gebruiken, die is gekoppeld aan een gescande streepjescode. Dit functioneert voor ontvangst op inkomende stromen, inclusief gecombineerde nummerplaatontvangst, inkooporderartikel, transferorderartikel en ladingsitem. Het functioneert ook voor stuksverzameling waarbij het scannen van de streepjescode de hoeveelheid toevoegt aan het totale aantal bevestigde stuks, met conversie tussen de maateenheid in de streepjescode en de werkeenheid. Als bij het tellen van de maateenheid in de streepjescode wordt bevestigd dat de hoeveelheid is toegestaan voor het tellen van de nummerreeksgroep, wordt de hoeveelheid wordt toegevoegd aan het totale aantal.

## <a name="where-it-applies"></a>Waar van toepassing

Stuksverzameling werkt voor alle tellingswerk en voor de eerste verzameling voor elke soort werk. Stuksverzameling is niet van toepassing als het artikel wordt gecontroleerd door serienummers, of als het een productieverzameling of kanbanverzameling is van een nummerplaatlocatie en het artikel is ingesteld op klaarzetten.

## <a name="set-up-piece-picking"></a>Stuksverzameling instellen

1.  Open op een menu-item voor mobiele apparaten het instellingsformulier voor werkbevestiging : Magazijnbeheer > **Magazijnbeheer** > **Instellingen** > **Mobiel apparaat** > **Menuopties voor mobiel apparaat**. 
2. Open in de menuoptie voor het mobiele apparaat de Werkbevestigingsinstellingen.

De volgende opties worden beschikbaar voor selectie, wanneer het type werk verzameling of telling is.


|           Optie           |                                                                            Omschrijving                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bevestiging van orderverzameling | Beschikbaar voor werktypen verzamelen en tellen. Productbevestiging wordt automatisch ingeschakeld. Hiermee kunt u elk stuk van de voorraad vanaf het mobiele apparaat bevestigen. |
|  Maximumaantal stuks  |                   Beschikbaar voor verzamelingswerk, als bevestiging voor stuksverzamelen is ingeschakeld. Stelt een limiet in op het aantal onderdelen dat u moet bevestigen.                   |


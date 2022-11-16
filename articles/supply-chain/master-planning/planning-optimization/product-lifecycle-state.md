---
title: Producten met specifieke levenscyclusstatussen uitsluiten
description: In dit artikel wordt uitgelegd hoe u producten uitsluit op basis van hun levenscyclusstatus.
author: t-benebo
ms.date: 11/13/2020
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
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 647e2cf4f14dbdfc3e7f04f43dcbd7115f19e8dc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740760"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Producten met specifieke levenscyclusstatussen uitsluiten

[!include [banner](../../includes/banner.md)]

Vrijgegeven producten en vrijgegeven productversies bevatten een veld **Levenscyclusstatus van het product**. Met dit veld kunt u onder andere bepalen welke producten in de hoofdplanning worden opgenomen. U kunt de levenscyclusstatussen naar wens toevoegen, verwijderen en bewerken door naar **Productgegevensbeheer \> Instellingen \> Levenscyclusstatus van het product** te gaan. Stel voor elke levenscyclusstatus de optie **Is actief voor planning** op *Ja* als producten met die status moeten worden opgenomen in de hoofdplanning. Wanneer de optie is ingesteld op *Nee*, worden de gekoppelde producten en varianten uitgesloten van alle hoofdplanningen en alle berekeningen op stuklijstniveau.

Vrijgegeven producten en varianten waarbij het veld **Levenscyclusstatus van het product** leeg is gelaten, worden verwerkt alsof ze een levenscyclusstatus hebben waarbij de optie **Is actief voor planning** is ingesteld op *Ja*. Met andere woorden, deze worden opgenomen in de hoofdplanning.

> [!NOTE]
> Om onnodige aanbodvoorstellen te voorkomen, raden we u aan om alle verouderde vrijgegeven producten en varianten te koppelen aan de productlevenscyclusstatus waarvoor de optie **Is actief voor planning** is ingesteld op *Nee*. Deze aanpak is met name belangrijk wanneer u werkt met product configuratievarianten die niet herbruikbaar zijn, omdat u hiermee afval kunt voorkomen.

## <a name="related-resources"></a>Gerelateerde bronnen

Zie [Overzicht van Levenscyclusstatus van producten](../../pim/product-lifecycle.md) voor meer informatie over levenscyclusstatussen van producten.

Voor gedetailleerde informatie, waaronder stappen voor het gebruik van productlevenscyclusstatussen om producten uit te sluiten van de hoofdplanning en berekeningen op stuklijstniveau, gaat u naar [Een status voor de productlevenscyclus maken om producten uit te sluiten van Hoofdplanning](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
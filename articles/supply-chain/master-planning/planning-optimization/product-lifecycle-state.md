---
title: Producten met specifieke levenscyclusstatussen uitsluiten
description: In dit onderwerp wordt uitgelegd hoe u producten opneemt op basis van de levenscyclusstatus wanneer de functie Planningsoptimalisatie wordt gebruikt.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1e0c734db763ffa69e2d6540a07d5fa04c22ea1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227812"
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
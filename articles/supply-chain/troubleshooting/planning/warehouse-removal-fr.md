---
title: U kunt de dimensie voor magazijnvraagprognose niet verwijderen uit prognoseregels
description: U kunt de dimensie voor magazijnvraagprognose niet verwijderen uit prognoseregels.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741208"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>U kunt de dimensie voor magazijnvraagprognose niet verwijderen uit prognoseregels

KB-nummer: 4614408

## <a name="symptoms"></a>Symptomen

Dit probleem treedt op wanneer de dimensie **Magazijn** niet is toegewezen op het tabblad **Prognosedimensies** van de pagina **Vraagprognoseparameter**. De kolom **Magazijn** wordt echter weergegeven op de pagina **Vraagprognose** (**Hoofdplanning \> Prognose \> Handmatige prognose-entiteit \> Vraagprognoseregels**).

## <a name="resolution"></a>Oplossing

De instellingen op het tabblad **Prognosedimenssie** van de pagina **Vraagprognoseparameter** hebben geen invloed op de pagina **Vraagprognose**. Ze bepalen de basislijnprognose die wordt gegenereerd en weergegeven in de gecorrigeerde vraagprognose. Ze hebben echter geen controle over de dimensies die vereist zijn voor de 'echte' vraagprognose. Door de records toe te staan die worden weergegeven op de pagina **Gecorrigeerde vraagprognose**, kunt u ze converteren naar 'echte' prognosegegevens voor een prognosemodel. Dat model kan vervolgens worden gebruikt voor de hoofdplanning.

Op de pagina **Vraagprognose** maken de dimensies voor de 'echte' prognose die wordt weergegeven op de vraagprognoseregels deel uit van de voorraaddimensies. (Dit gedrag lijkt op het gedrag van verkooporderregels.) Als uw systeem niet is ingesteld om **Magazijn** te gebruiken als verplichte voorraaddimensie, kunt u de pagina aanpassen om de kolom te verbergen.

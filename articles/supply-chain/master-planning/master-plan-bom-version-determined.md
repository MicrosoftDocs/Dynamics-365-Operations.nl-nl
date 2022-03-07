---
title: De stuklijstversie bepalen
description: Als voor een artikel tijdens een vraagexplosie een standaardordertype is ingesteld op Productie, wordt een geldige stuklijstversie gezocht op basis van de locatie.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370091eed4ee050031d5d135aa7b1d8d0fe82491
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570964"
---
# <a name="determine-the-bom-version"></a>De stuklijstversie bepalen

[!include [banner](../includes/banner.md)]

Als voor een artikel tijdens een vraagexplosie een standaardordertype is ingesteld op Productie, wordt een geldige stuklijstversie gezocht op basis van de locatie. 

De locatiedimensie is altijd bekend en wordt vermeld op de vraagtransactie. Het bepalen van de te gebruiken stuklijstversie gaat als volgt in zijn werk:

-   Als voor het artikel een stuklijstversie is gedefinieerd op de vraaglocatie, wordt deze locatiespecifieke stuklijst gebruikt.
-   Als voor een artikel op de vraaglocatie geen locatiespecifieke stuklijstversie is gedefinieerd, wordt een algemene stuklijst gebruikt. Op een algemene stuklijst wordt geen locatie vermeld, want deze is geldig voor meerdere locaties. Als er een algemene stuklijst bestaat, wordt deze gebruikt.
-   Als er geen algemene stuklijstversie bestaat, wordt de vraagexplosie op dit moment gestopt.

Een geldige stuklijstversie, of deze nu locatiespecifiek of algemeen is, moet voldoen aan de vereiste criteria voor datum en hoeveelheid.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
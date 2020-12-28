---
title: De stuklijstversie bepalen
description: Als voor een artikel tijdens een vraagexplosie een standaardordertype is ingesteld op Productie, wordt een geldige stuklijstversie gezocht op basis van de locatie.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 766c857cca603f84bb7fcef2c7eea3bc76620c19
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425682"
---
# <a name="determine-the-bom-version"></a>De stuklijstversie bepalen

[!include [banner](../includes/banner.md)]

Als voor een artikel tijdens een vraagexplosie een standaardordertype is ingesteld op Productie, wordt een geldige stuklijstversie gezocht op basis van de locatie. 

De locatiedimensie is altijd bekend en wordt vermeld op de vraagtransactie. Het bepalen van de te gebruiken stuklijstversie gaat als volgt in zijn werk:

-   Als voor het artikel een stuklijstversie is gedefinieerd op de vraaglocatie, wordt deze locatiespecifieke stuklijst gebruikt.
-   Als voor een artikel op de vraaglocatie geen locatiespecifieke stuklijstversie is gedefinieerd, wordt een algemene stuklijst gebruikt. Op een algemene stuklijst wordt geen locatie vermeld, want deze is geldig voor meerdere locaties. Als er een algemene stuklijst bestaat, wordt deze gebruikt.
-   Als er geen algemene stuklijstversie bestaat, wordt de vraagexplosie op dit moment gestopt.

Een geldige stuklijstversie, of deze nu locatiespecifiek of algemeen is, moet voldoen aan de vereiste criteria voor datum en hoeveelheid.






---
title: Hoofdplanning en de functionaliteit voor meerdere locaties
description: In de hoofdplanning wordt rekening gehouden met de instellingen van de locatie- en magazijnvoorraaddimensies.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d45cc1e69696fbc22078d0f1cd7f089fd322b440
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="master-planning-and-multisite-functionality"></a>Hoofdplanning en de functionaliteit voor meerdere locaties

[!include[banner](../includes/banner.md)]


In de hoofdplanning wordt rekening gehouden met de instellingen van de locatie- en magazijnvoorraaddimensies. 

De locatiedimensie is verplicht en u kunt de magazijndimensie als verplicht instellen.

Als een dimensie verplicht is, moet u een dimensiewaarde invoeren voor alle voorraadtransacties. Daarom zijn bij de hoofdplanning de locatie en het magazijn voor de eerste vraag bekend. Daarnaast is de locatiedimensie consistent, zodat de locatiewaarde niet wordt gewijzigd tijdens de explosie van de vraag op lager niveau.

Als het magazijn niet wordt ingesteld op verplicht, is dit mogelijk niet bekend voor de eerste vraag. Via het planningsprogramma moet worden bepaald welk magazijn moet worden gebruikt op basis van de instellingen die zijn gedefinieerd voor het artikel, afzonderlijke magazijnen en de gegevens van de orderregel.

In de volgende onderwerpen wordt beschreven hoe het planningsprogramma werkt als er verschillende instellingen zijn gedefinieerd om het magazijn te bepalen dat moet worden gebruikt.

[Hoofdplanning - locatie en magazijnbehoefte, magazijn verplicht](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatiebehoefte, magazijn verplicht](master-plan-site-coverage-warehouse-mandatory.md)

[Hoofdplanning - locatie- en magazijnbehoefte, magazijn niet verplicht](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hoofdplanning - locatiebehoefte, magazijn niet verplicht](master-plan-site-coverage-warehouse-not-mandatory.md)

[Hoofdplanning - hoe de stuklijstversie wordt bepaald](master-plan-bom-version-determined.md)




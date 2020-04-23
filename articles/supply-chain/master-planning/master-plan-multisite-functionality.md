---
title: Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties
description: In de hoofdplanning wordt rekening gehouden met de instellingen van de locatie- en magazijnvoorraaddimensies.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b26ff5c2f580c30113b82302bbad744bbf285ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213717"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties

[!include [banner](../includes/banner.md)]

In de hoofdplanning wordt rekening gehouden met de instellingen van de locatie- en magazijnvoorraaddimensies. 

De locatiedimensie is verplicht en u kunt de magazijndimensie als verplicht instellen.

Als een dimensie verplicht is, moet u een dimensiewaarde invoeren voor alle voorraadtransacties. Daarom zijn bij de hoofdplanning de locatie en het magazijn voor de eerste vraag bekend. Daarnaast is de locatiedimensie consistent, zodat de locatiewaarde niet wordt gewijzigd tijdens de explosie van de vraag op lager niveau.

Als het magazijn niet wordt ingesteld op verplicht, is dit mogelijk niet bekend voor de eerste vraag. Via het planningsprogramma moet worden bepaald welk magazijn moet worden gebruikt op basis van de instellingen die zijn gedefinieerd voor het artikel, afzonderlijke magazijnen en de gegevens van de orderregel.

In de volgende onderwerpen wordt beschreven hoe het planningsprogramma werkt als er verschillende instellingen zijn gedefinieerd om het magazijn te bepalen dat moet worden gebruikt.

[Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hoofdplanning voor locatiebehoefte, magazijn verplicht](master-plan-site-coverage-warehouse-mandatory.md)

[Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hoofdplanning voor locatiebehoefte, magazijn niet verplicht](master-plan-site-coverage-warehouse-not-mandatory.md)

[De stuklijstversie bepalen](master-plan-bom-version-determined.md)




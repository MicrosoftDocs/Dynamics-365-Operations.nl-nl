---
title: Activa en werkorders
description: In dit onderwerp worden activa en werkorders in Activabeheer beschreven.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783176"
---
# <a name="assets-and-work-orders"></a>Activa en werkorders

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In dit onderwerp worden activa en werkorders in Activabeheer beschreven. Activa en werkorders zijn de centrale onderdelen van Activabeheer. Een *activum* is een machine of een machineonderdeel dat continu onderhoud en service vereist. Activa kunnen worden gemaakt in een hiërarchische structuur en kunnen worden gerelateerd aan functionele locaties. Onderhoudstaken kunnen worden gepland op alle niveaus in de activastructuur.

Voor elk activum worden verschillende gegevens, zoals productinformatie en activaspecificatie, en vereiste onderhoudsplannen ingesteld. In de volgende afbeelding ziet u een overzicht van activagegevens en de koppeling van activa op taaktypen. Rode tekst wordt gebruikt voor voorbeelden die overname en afhankelijkheden aangeven.

![Figuur 1](media/05-overview-image.png)

Elke werkorder heeft een werkordertype, zoals preventief onderhoud, correctief onderhoud of inspectie. De werkorder bevat een of meer werkordertaken. Elke werkordertaak definieert een taak die moet worden uitgevoerd voor een activum en een gerelateerd taaktype. Voorbeelden van gerelateerde taaktypen zijn 10.000 km, 50.000 km, 1 jaar revisie en veiligheidsinspectie. Eén werkorder kan aan meerdere activa zijn gerelateerd.

In de volgende afbeelding wordt een overzicht gegeven van de belangrijkste gegevens in een werkorder.

![Figuur 2](media/06-overview-image.png)

Een werkorder kan worden gerelateerd aan een andere werkorder en taaktypen kunnen opvolgende taken bevatten die een werkorder maken. Over het algemeen zijn er geen afhankelijkheden tussen werkorders. Daarom kunnen ze de levenscyclusstatus voor werkorders wijzigen en onafhankelijk van elkaar worden gepland.

Werkorders kunnen op verschillende manieren worden gemaakt die gerelateerd zijn aan correctief, preventief of reactief onderhoud. U kunt werkorders ook handmatig maken. In de volgende afbeelding wordt een overzicht weergegeven van het proces voor het automatisch of handmatig maken van werkorders.

![Figuur 3](media/07-overview-image.png)

Verschillende stappen moeten worden voltooid wanneer u een onderhoudstaak voor een werkorder wilt plannen en uitvoeren. In de volgende afbeelding wordt een overzicht gegeven van de verwerking van een werkorder.

![Figuur 4](media/08-overview-image.png)

> [!NOTE]
> In het algemeen geldt dat, wanneer u in Microsoft Dynamics 365 for Finance and Operations en de module **Activabeheer** werkt, u **Nieuw** selecteert om een nieuwe record te maken, **Bewerken** selecteert om een bestaande record bij te werken en **Opslaan** selecteert om nieuwe of bewerkte gegevens op te slaan.

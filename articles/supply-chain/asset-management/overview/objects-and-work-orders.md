---
title: Activa en werkorders
description: In dit onderwerp worden activa en werkorders in Activabeheer beschreven.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2500a695fcffe0d60ac13b1b74cda4322b0e14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425485"
---
# <a name="assets-and-work-orders"></a>Activa en werkorders

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp worden activa en werkorders in Activabeheer beschreven. Activa en werkorders zijn de centrale onderdelen van Activabeheer. Een *activum* is een machine of een machineonderdeel dat continu onderhoud en service vereist. Activa kunnen worden gemaakt in een hiërarchische structuur en kunnen worden gerelateerd aan functionele locaties. Onderhoudstaken kunnen worden gepland op alle niveaus in de activastructuur.

Voor elk activum worden verschillende gegevens, zoals productinformatie en activaspecificatie, en vereiste onderhoudsplannen ingesteld. In de volgende afbeelding ziet u een overzicht van activagegevens en de koppeling van activa op taaktypen. Rode tekst wordt gebruikt voor voorbeelden die overname en afhankelijkheden aangeven.

![Diagram met de activagegevens die zijn gerelateerd aan taaktypen](media/05-overview-image.png)

Elke werkorder heeft een werkordertype, zoals preventief onderhoud, correctief onderhoud of inspectie. De werkorder bevat een of meer werkordertaken. Elke werkordertaak definieert een taak die moet worden uitgevoerd voor een activum en een gerelateerd taaktype. Voorbeelden van gerelateerde taaktypen zijn 10.000 km, 50.000 km, 1 jaar revisie en veiligheidsinspectie. Eén werkorder kan aan meerdere activa zijn gerelateerd.

In de volgende afbeelding wordt een overzicht gegeven van de belangrijkste gegevens in een werkorder.

![Diagram waarin de belangrijkste gegevens in een werkorder worden weergegeven](media/06-overview-image.png)

Een werkorder kan worden gerelateerd aan een andere werkorder en taaktypen kunnen opvolgende taken bevatten die een werkorder maken. Over het algemeen zijn er geen afhankelijkheden tussen werkorders. Daarom kunnen ze de levenscyclusstatus voor werkorders wijzigen en onafhankelijk van elkaar worden gepland.

Werkorders kunnen op verschillende manieren worden gemaakt die gerelateerd zijn aan correctief, preventief of reactief onderhoud. U kunt werkorders ook handmatig maken. In de volgende afbeelding wordt een overzicht weergegeven van het proces voor het automatisch of handmatig maken van werkorders.

![Diagram waarin het automatisch of handmatig maken van werkorders wordt weergegeven](media/07-overview-image.png)

Verschillende stappen moeten worden voltooid wanneer u een onderhoudstaak voor een werkorder wilt plannen en uitvoeren. In de volgende afbeelding wordt een overzicht gegeven van de verwerking van een werkorder.

![Diagram met een overzicht van de verwerking van een werkorder](media/08-overview-image.png)

> [!NOTE]
> In het algemeen geldt dat, wanneer u in Dynamics 365 Supply Chain Management en de module **Activabeheer** werkt, u **Nieuw** selecteert om een nieuwe record te maken, **Bewerken** selecteert om een bestaande record bij te werken en **Opslaan** selecteert om nieuwe of bewerkte gegevens op te slaan.

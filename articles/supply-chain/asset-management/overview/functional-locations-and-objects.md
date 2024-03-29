---
title: Functionele locaties en activa
description: In dit artikel worden de functionele locaties en activa in Activabeheer beschreven. Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8d155b8bbf981408f6f15e914fc3bb1da25c9c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111071"
---
# <a name="functional-locations-and-assets"></a>Functionele locaties en activa

[!include [banner](../../includes/banner.md)]

 

In dit artikel worden de functionele locaties en activa in Activabeheer beschreven. Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Overzicht

Activabeheer is naadloos geïntegreerd met verschillende modules in andere apps voor financiën en bedrijfsactiviteiten. In de volgende afbeelding ziet u de interfaces met andere modules.

![Diagram waarin wordt getoond hoe Activabeheer samenwerkt met andere modules.](media/01-overview-image.png)

Met Activabeheer kunt u alle taken efficiënt beheren en uitvoeren die betrekking hebben op het beheren en onderhouden van allerlei soorten apparatuur in uw bedrijf. Deze apparatuur omvat machines, productieapparatuur en voertuigen. Activabeheer ondersteunt ook oplossingen in tal van industrieën.

In de volgende afbeelding ziet u een overzicht van de hoofdfunctionaliteit die wordt gedekt door Activabeheer.

![Diagram met de hoofdfunctionaliteit in Activabeheer.](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Functionele locaties en activa

Functionele locaties worden gebruikt om activa op locaties te beheren. Dit beheer omvat het volgen van de activakosten op functionele locaties. Functionele locaties zijn hiërarchisch gestructureerd en locaties kunnen sublocaties hebben. De structuur van functionele locaties is statisch. Met andere woorden locaties kunnen niet van plaats veranderen. Activa kunnen op functionele locaties worden geïnstalleerd en kunnen, indien nodig, later op andere functionele locaties worden geïnstalleerd.

Activakosten volgen altijd de locatie van het activum. Met andere woorden, als u een activum op een nieuwe functionele locatie installeert, gebruikt het activum automatisch de financiële dimensies die samenhangen met de nieuwe functionele locatie. Daarom zijn de activakosten altijd gerelateerd aan de functionele locatie waarop het activum momenteel is geïnstalleerd. Deze automatische afhandeling van financiële dimensies helpt garanderen dat alle kosten worden bijgehouden wanneer uw bedrijf projectcontrole en rapportage op functionele locaties doet.

De manier waarop u uw hiërarchie van functionele locaties bouwt, is afhankelijk van de vereisten van uw bedrijf voor het onderhouden van interne apparatuur of het onderhoud van klantapparatuur. In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op geografische locaties.

![Diagram met functionele locaties op basis van geografische locaties.](media/03-overview-image.png)

In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op klanten.

![Diagram met functionele locaties op basis van klanten.](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

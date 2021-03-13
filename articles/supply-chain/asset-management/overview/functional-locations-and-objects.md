---
title: Functionele locaties en activa
description: In dit onderwerp worden de functionele locaties en activa in Activabeheer beschreven. Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Dynamics 365 Supply Chain Management.
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
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f93a68f19b0b952eb2964b404bb957865c625cd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018041"
---
# <a name="functional-locations-and-assets"></a>Functionele locaties en activa

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp worden de functionele locaties en activa in Activabeheer beschreven. Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Overzicht

Activabeheer integreert naadloos met verschillende modules in andere Finance and Operations-apps. In de volgende afbeelding ziet u de interfaces met andere modules.

![Diagram waarin wordt getoond hoe Activabeheer samenwerkt met andere modules](media/01-overview-image.png)

Met Activabeheer kunt u alle taken efficiënt beheren en uitvoeren die betrekking hebben op het beheren en onderhouden van allerlei soorten apparatuur in uw bedrijf. Deze apparatuur omvat machines, productieapparatuur en voertuigen. Activabeheer ondersteunt ook oplossingen in tal van industrieën.

In de volgende afbeelding ziet u een overzicht van de hoofdfunctionaliteit die wordt gedekt door Activabeheer.

![Diagram met de hoofdfunctionaliteit in Activabeheer](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Functionele locaties en activa

Functionele locaties worden gebruikt om activa op locaties te beheren. Dit beheer omvat het volgen van de activakosten op functionele locaties. Functionele locaties zijn hiërarchisch gestructureerd en locaties kunnen sublocaties hebben. De structuur van functionele locaties is statisch. Met andere woorden locaties kunnen niet van plaats veranderen. Activa kunnen op functionele locaties worden geïnstalleerd en kunnen, indien nodig, later op andere functionele locaties worden geïnstalleerd.

Activakosten volgen altijd de locatie van het activum. Met andere woorden, als u een activum op een nieuwe functionele locatie installeert, gebruikt het activum automatisch de financiële dimensies die samenhangen met de nieuwe functionele locatie. Daarom zijn de activakosten altijd gerelateerd aan de functionele locatie waarop het activum momenteel is geïnstalleerd. Deze automatische afhandeling van financiële dimensies helpt garanderen dat alle kosten worden bijgehouden wanneer uw bedrijf projectcontrole en rapportage op functionele locaties doet.

De manier waarop u uw hiërarchie van functionele locaties bouwt, is afhankelijk van de vereisten van uw bedrijf voor het onderhouden van interne apparatuur of het onderhoud van klantapparatuur. In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op geografische locaties.

![Diagram met functionele locaties op basis van geografische locaties](media/03-overview-image.png)

In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op klanten.

![Diagram met functionele locaties op basis van klanten](media/04-overview-image.png)

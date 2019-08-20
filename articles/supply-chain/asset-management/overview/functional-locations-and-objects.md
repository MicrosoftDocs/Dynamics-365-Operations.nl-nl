---
title: Functionele locaties en activa
description: In dit onderwerp worden de functionele locaties en activa in Activabeheer beschreven. Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: 351e27dfbbd5227a9642f14a48afe194c447a0f3
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783194"
---
# <a name="functional-locations-and-assets"></a>Functionele locaties en activa

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In dit onderwerp worden de functionele locaties en activa in Activabeheer beschreven. Activabeheer is een geavanceerde module voor het beheren van activa en onderhoudstaken in Microsoft Dynamics 365 for Finance and Operations.

## <a name="overview"></a>Overzicht

Activabeheer is naadloos geïntegreerd met verschillende modules in Finance and Operations. In de volgende afbeelding ziet u de interfaces met andere modules.

![Figuur 1](media/01-overview-image.png)

Met Activabeheer kunt u alle taken efficiënt beheren en uitvoeren die betrekking hebben op het beheren en onderhouden van allerlei soorten apparatuur in uw bedrijf. Deze apparatuur omvat machines, productieapparatuur en voertuigen. Activabeheer ondersteunt ook oplossingen in tal van industrieën.

In de volgende afbeelding ziet u een overzicht van de hoofdfunctionaliteit die wordt gedekt door Activabeheer.

![Figuur 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Functionele locaties en activa

Functionele locaties worden gebruikt om activa op locaties te beheren. Dit beheer omvat het volgen van de activakosten op functionele locaties. Functionele locaties zijn hiërarchisch gestructureerd en locaties kunnen sublocaties hebben. De structuur van functionele locaties is statisch. Met andere woorden locaties kunnen niet van plaats veranderen. Activa kunnen op functionele locaties worden geïnstalleerd en kunnen, indien nodig, later op andere functionele locaties worden geïnstalleerd.

Activakosten volgen altijd de locatie van het activum. Met andere woorden, als u een activum op een nieuwe functionele locatie installeert, gebruikt het activum automatisch de financiële dimensies die samenhangen met de nieuwe functionele locatie. Daarom zijn de activakosten altijd gerelateerd aan de functionele locatie waarop het activum momenteel is geïnstalleerd. Deze automatische afhandeling van financiële dimensies helpt garanderen dat alle kosten worden bijgehouden wanneer uw bedrijf projectcontrole en rapportage op functionele locaties doet.

De manier waarop u uw hiërarchie van functionele locaties bouwt, is afhankelijk van de vereisten van uw bedrijf voor het onderhouden van interne apparatuur of het onderhoud van klantapparatuur. In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op geografische locaties.

![Figuur 3](media/03-overview-image.png)

In de volgende afbeelding ziet u een voorbeeld van functionele locaties die zijn gebaseerd op klanten.

![Figuur 4](media/04-overview-image.png)

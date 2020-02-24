---
title: Carrouselmodule
description: In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025776"
---
# <a name="carousel-module"></a>Carrouselmodule


[!include [banner](includes/banner.md)]

In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotieartikelen (met afbeeldingen) in een draaiende carrouselbanner waar klanten doorheen kunnen bladeren. Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.

U kunt inhoudsblokmodules in een carrouselmodule toevoegen. De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Voorbeelden van carrouselmodules in e-commerce

- Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.
- Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.
- Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.

## <a name="carousel-module-properties"></a>Eigenschappen van carrouselmodules

| Naam van eigenschap.             | Waarde                 | Beschrijving |
|---------------------------|-----------------------|-------------|
| Automatisch afspelen                  | **True** of **False** | Als de waarde is ingesteld op **True**, vindt de overgang tussen items binnen de carrousel automatisch plaats. Als de waarde is ingesteld op **False**, vindt er geen overgang plaats tenzij de klant het toetsenbord of de muis gebruikt om van het ene naar het volgende item te gaan. |
| Interval voor diaovergang | Een waarde in seconden    | Het interval voor overgangen tussen items. |
| Overgangstype           | **Verschuiven** of **Vervagen** | Het overgangseffect tussen artikelen. |
| Carrouselflipper verbergen     | **True** of **False** | Als de waarde is ingesteld op **True**, worden de carrouselflipper en reeksindicator verborgen. |
| Sluiten van carrousel toestaan    | **True** of **False** | Als de waarde is ingesteld op **True**, kunnen gebruikers de carrousel sluiten. |

## <a name="add-a-carousel-module-to-a-page"></a>Een carrouselmodule toevoegen aan een pagina

Voer de volgende stappen uit om een carrouselmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **Carrouselsjabloon**.
1. Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.
1. Check de sjabloon in en publiceer deze. 
1. Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe. 
1. Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Scherm vullen**.
1. Voeg onder **Paginaoverzicht** een carrouselmodule aan de containermodule toe.
1. Voeg aan de carrouselmodule een inhoudsblokmodule toe. Stel de eigenschappen van de inhoudsblokmodule in door **Koptekst**, **Koppeling**, **Indeling** en andere eigenschappen op te geven.
1. U kunt nog een inhoudsblokmodule toevoegen en configureren.
1. Stel zo nodig aanvullende eigenschappen in voor de carrouselmodule.
1. Sla de pagina op en bekijk een voorbeeld. Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule). U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.
1. Voltooi het bewerken van de pagina en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Promospandoekmodule](add-alert.md)

[Tekstblokmodule](add-content-rich-block.md)

[Inhoudsblokmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)

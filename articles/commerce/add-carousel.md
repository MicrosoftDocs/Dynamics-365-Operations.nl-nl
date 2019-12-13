---
title: Carrouselmodule
description: In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785232"
---
# <a name="carousel-module"></a>Carrouselmodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotiepunten in een carrousel waarin klanten kunnen bladeren. Het is een speciale containermodule waarin andere modules worden gehost. Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.

U kunt held- en functiemodules toevoegen binnen een carrouselmodule. De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Voorbeelden van carrouselmodules in e-commerce

- Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.
- Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.
- Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.

## <a name="carousel-module-properties"></a>Eigenschappen van carrouselmodules

| Naam van eigenschap.             | Waarde                                | Beschrijving |
|---------------------------|--------------------------------------|-------------|
| Automatisch afspelen                  | **True** of **False**                | Als de waarde is ingesteld op **True**, vindt de overgang tussen items binnen de carrousel automatisch plaats. Als de waarde is ingesteld op **False**, vindt er geen overgang plaats tenzij de klant het toetsenbord of de muis gebruikt om van het ene naar het volgende item te gaan. |
| Interval voor diaovergang | Een waarde in seconden                   | Het interval voor overgangen tussen items. |
| Overgangsanimatie      | **Verschuiven** of **Vervagen**                | Het overgangseffect. |
| Breedte                     | **Passen in container** of **Scherm vullen** | Als de waarde wordt ingesteld op **Passen in container**, zijn de items in de carrousel beperkt tot de breedte van de carrousel. Als de waarde is ingesteld op **Scherm vullen**, zijn de items niet beperkt tot de breedte van de carrousel voor de plaatsing van inhoud, maar gebruiken ze de modus Volledig scherm. U kunt de waarde wijzigen om de gewenste indeling te bereiken. |

## <a name="add-a-carousel-module-to-a-page"></a>Een carrouselmodule toevoegen aan een pagina

Voer de volgende stappen uit om een carrouselmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **Carrouselsjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een carrouselmodule toe.
1. Voeg een heldmodule toe aan de carrouselmodule.
1. Voeg een functiemodule toe aan de carrouselmodule.
1. Check de sjabloon in en publiceer deze. 
1. Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een carrouselmodule toe.
1. Stel de eigenschap **Breedte** van de carrouselmodule in op **Scherm vullen**. 
1. Stel de eigenschap **Overgangsanimatie** in op **Verschuiven**.
1. Voeg een heldmodule toe aan de carrouselmodule.
1. Voeg in de heldmodule een afbeelding en een koptekst toe en selecteer vervolgens **Opslaan**.
1. Voeg een functiemodule toe aan de carrouselmodule.
1. Voeg in de functiemodule een afbeelding, een kop en een alineatekst toe.
1. Sla de pagina op en bekijk een voorbeeld. Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule). U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.
1. Check de pagina in en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Waarschuwingsmodule](add-alert.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Module voor het plaatsen van inhoud](add-content-placement-modules.md)

[Functiemodule](add-feature-module.md)

[Heldmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)

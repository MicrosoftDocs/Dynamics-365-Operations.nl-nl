---
title: Carrouselmodule
description: In dit artikel worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b99fea773f18c65b73ea3f519705d3043820cfd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865002"
---
# <a name="carousel-module"></a>Carrouselmodule

[!include [banner](includes/banner.md)]

In dit artikel worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotieartikelen (met afbeeldingen) in een draaiende carrouselbanner waar klanten doorheen kunnen bladeren. Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.

U kunt inhoudsblokmodules in een carrouselmodule toevoegen. De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Voorbeelden van carrouselmodules in e-commerce

- Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.
- Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.
- Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.

De volgende afbeelding toont een voorbeeld van een carrouselmodule die wordt gebruikt op een introductiepagina. Deze carrouselmodule bevat meerdere inhoudsblokitems.

![Voorbeeld van een carrouselmodule.](./media/Hero.PNG)

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

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Carrouselsjabloon** in en selecteer vervolgens **OK**.
1. Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.  
1. Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe. 
1. Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Scherm vullen**.
1. Voeg onder **Paginaoverzicht** een carrouselmodule aan de containermodule toe.
1. Voeg aan de carrouselmodule een inhoudsblokmodule toe. Stel de eigenschappen van de inhoudsblokmodule in door **Koptekst**, **Koppeling**, **Indeling** en andere eigenschappen op te geven.
1. U kunt nog een inhoudsblokmodule toevoegen en configureren.
1. Stel zo nodig aanvullende eigenschappen in voor de carrouselmodule.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule). U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Promotiebanner-module](add-alert.md)

[Text Block-module](add-content-rich-block.md)

[Inhoudsblokkenmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

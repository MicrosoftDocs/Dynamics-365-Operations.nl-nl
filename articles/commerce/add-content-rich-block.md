---
title: Tekstblokmodule
description: In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7dbeb8785641960cc2680335436aea10775759d3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797762"
---
# <a name="text-block-module"></a>Text Block-module

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Een tekstblokmodule is een module die wordt gebruikt om tekstuele inhoud toe te voegen. Deze inhoud kan informatief of promotioneel zijn.

Tekstblokmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst. Ze zijn zelfstandige modules die niet afhankelijk is van andere paginacontext of andere modules.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Voorbeelden van tekstblokmodules in e-Commerce

Tekstblokmodules kunnen op de volgende manieren worden gebruikt:

* Voor het presenteren van productfuncties op een pagina met productgegevens.
* Voor informatieve doeleinden op elke willekeurige pagina. Ze kunnen bijvoorbeeld de voordelen van loyaliteitsprogramma's toelichten, verzend- en retourbeleid beschrijven, veelgestelde vragen beantwoorden of informatie over het bedrijf invullen.
* Aangepaste berichten toevoegen aan een pagina met productgegevens. (bijvoorbeeld "gratis verzending voor bestellingen boven $50").
* Voor disclaimers en contactgegevens op pagina's met productdetails, winkelwagens, kassa en andere pagina's (bijvoorbeeld "verzending en retouren vallen onder het winkelbeleid").

De volgende afbeelding toont een voorbeeld van een tekstblokmodule die wordt gebruikt op een introductiepagina.

![Voorbeeld van een tekstblokmodule](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Eigenschappen van tekstblokmodule

| Naam van eigenschap.     | Waarde                                            | Omschrijving |
|-------------------|--------------------------------------------------|-------------|
| RTF         | RTF                                        | Alineatekst. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst. |
| Naam van aangepaste klasse | Een naam voor een CSS-klasse (trapsgewijs opmaakmodel)        | De naam van een aangepaste CSS-klasse die een ontwikkelaar biedt om deze module te formatteren. De klassenaam moet worden gedefinieerd in het themapakket. |
| Lettergrootte         | **Klein**, **Normaal**, **Groot** of **X-Large** | De lettergrootte van de inhoud. |

## <a name="add-a-text-block-module-to-a-page"></a>Een tekstblokmodule toevoegen aan een pagina

Voer de volgende stappen uit om een tekstblokmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Inhoudsjabloon** in.
1. Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** de **Inhoudsjabloon**. Voer onder **Paginanaam** **Inhoudpagina** in en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Tekstblok** en selecteer vervolgens **OK**. 
1. Voeg in het eigenschappenvenster van de tekstblokmodule tekst toe aan het veld **RTF**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Promotiebanner-module](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsblokkenmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
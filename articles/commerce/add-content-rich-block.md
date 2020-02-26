---
title: Tekstblokmodule
description: In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025592"
---
# <a name="text-block-module"></a>Tekstblokmodule


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een tekstblokmodule is een module die wordt gebruikt om tekstuele inhoud toe te voegen. Deze inhoud kan informatief of promotioneel zijn.

Tekstblokmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst. Ze zijn zelfstandige modules die niet afhankelijk is van andere paginacontext of andere modules.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Voorbeelden van tekstblokmodules in e-Commerce

Tekstblokmodules kunnen op de volgende manieren worden gebruikt:

* Voor het presenteren van productfuncties op een pagina met productgegevens.
* Voor informatieve doeleinden op elke willekeurige pagina. Ze kunnen bijvoorbeeld de voordelen van loyaliteitsprogramma's toelichten, verzend- en retourbeleid beschrijven, veelgestelde vragen beantwoorden of informatie over het bedrijf invullen.
* Aangepaste berichten toevoegen aan een pagina met productgegevens. (bijvoorbeeld "gratis verzending voor bestellingen boven $50").
* Voor disclaimers en contactgegevens op pagina's met productdetails, winkelwagens, kassa en andere pagina's (bijvoorbeeld "verzending en retouren vallen onder het winkelbeleid").

## <a name="text-block-module-properties"></a>Eigenschappen van tekstblokmodule

| Naam van eigenschap.     | Value                                            | Beschrijving |
|-------------------|--------------------------------------------------|-------------|
| RTF         | RTF                                        | Alineatekst. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst. |
| Naam van aangepaste klasse | Een naam voor een CSS-klasse (trapsgewijs opmaakmodel)        | De naam van een aangepaste CSS-klasse die een ontwikkelaar biedt om deze module te formatteren. De klassenaam moet worden gedefinieerd in het themapakket. |
| Lettergrootte         | **Klein**, **Normaal**, **Groot** of **X-Large** | De lettergrootte van de inhoud. |

## <a name="add-a-text-block-module-to-a-page"></a>Een tekstblokmodule toevoegen aan een pagina

Voer de volgende stappen uit om een tekstblokmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **Inhoudsjabloon**. 
1. Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.
1. Voltooi het bewerken van de sjabloon en publiceer deze.
1. Gebruik de inhoudsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Inhoudpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.
1. Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.
1. Voeg een tekstblokmodule toe aan de containermodule. 
1. Voeg in het eigenschappenvenster van de tekstblokmodule tekst toe aan het veld **RTF**.
1. Voltooi het bewerken van de pagina en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Promospandoekmodule](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsblokmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)


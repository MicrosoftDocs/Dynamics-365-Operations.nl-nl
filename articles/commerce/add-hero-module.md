---
title: Heldmodule
description: In dit onderwerp wordt beschreven wat heldmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785381"
---
# <a name="hero-module"></a>Heldmodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat heldmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een heldmodule wordt gebruikt voor de marketing van producten of promoties via een combinatie van afbeeldingen en tekst. Een detailhandelaar kan bijvoorbeeld een heldmodule toevoegen aan de startpagina van een e-commerce-site om een nieuw product te promoten en de aandacht van klanten te trekken.

Een heldmodule wordt gestuurd door gegevens uit het Content Management System (CMS). Het is een zelfstandige module die niet afhankelijk is van andere modules op de pagina. Een heldmodule kan op elke sitepagina worden geplaatst waar een detailhandelaar iets wil verhandelen of promoten (bijvoorbeeld producten, verkoop of functies).

## <a name="examples-of-hero-module-in-e-commerce"></a>Voorbeelden van heldmodules in e-commerce

- U kunt een heldmodule gebruiken op de startpagina van een e-commerce-site om promoties en nieuwe producten te markeren.
- U kunt een heldmodule op een pagina met productgegevens gebruiken om productinformatie te presenteren.
- Er kunnen meerdere heldmodules in een carrouselmodule worden geplaatst om meerdere producten of promoties te markeren.

## <a name="hero-module-properties"></a>Eigenschappen van heldmodule

| Naam van eigenschap.  | Waarden | Beschrijving |
|----------------|--------|-------------|
| Afbeelding          | Afbeeldingbestand | Een afbeelding kan worden gebruikt voor de presentatie van een product of promotie. Een afbeelding kan naar de afbeeldingengalerie worden geüpload, of er kan een bestaande afbeelding worden gebruikt. |
| Koptekst        | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Elke heldmodule kan een koptekst hebben. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |
| Alinea      | Alineatekst | Heldmodules ondersteunen alineatekst in RTF-indeling. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst en hyperlinks. Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast. |
| Koppeling           | Koppelingstekst, koppelings-URL, het label Accessible Rich internet Applications (ARIA) en **Koppeling in nieuw tabblad openen** | Heldmodules ondersteunen een of meer koppelingen met oproep tot actie. Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist. ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen. U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad. |
| Tekstplaatsing | **Linksboven**, **rechtsboven**, **middenboven**, **linksonder**, **rechtsonder**, **middenonder**, **midden links**, **midden rechts** of **midden rechts** | Met deze eigenschap wordt de positie van de afbeelding ten opzichte van de tekst bepaald. Als bijvoorbeeld **Rechts** is geselecteerd, wordt de afbeelding rechts van de tekst weergegeven. |
| Tekstthema     | **Licht** of **donker** | Er kan een kleurenschema worden gedefinieerd voor de tekst op basis van de achtergrondafbeelding. Als de afbeelding bijvoorbeeld een donkere achtergrond heeft, kan een licht thema worden toegepast om de tekst beter zichtbaar te maken en om te voldoen aan de kleurcontrastverhoudingen voor toegankelijkheidsdoeleinden. |
| Kleurovergang       | **True** of **False** | Er kan een kleurverloop op de afbeelding worden toegepast om te voldoen aan de kleurcontrastverhouding voor toegankelijkheidsdoeleinden. |

## <a name="add-a-hero-module-to-a-new-page"></a>Een heldmodule toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een heldmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en maak een paginasjabloon met de naam **heldsjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een heldmodule toe.
1. Check de sjabloon in en publiceer deze.
1. Gebruik de heldsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Heldpagina** te maken.
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** onder **Modules selecteren** een heldmodule en selecteer vervolgens **OK.**
1. Selecteer in de overzichtsstructuur aan de linkerkant de heldmodule.
1. Selecteer **Een afbeelding toevoegen** in het eigenschappenvenster aan de rechterkant. Selecteer vervolgens een bestaande afbeelding of upload een nieuwe afbeelding.
1. Selecteer **Koptekst**.
1. Voeg in het dialoogvenster **Koptekst** de koptekst toe, selecteer het kopniveau en selecteer vervolgens **OK**.
1. Voeg onder **RTF-indeling** de gewenste tekst toe.
1. Selecteer **Actiekoppeling toevoegen**.
1. Voeg in het dialoogvenster **Actiekoppeling** de koppelingstekst, een koppelings-URL en een ARIA-label voor de koppeling toe en selecteer vervolgens **OK**.
1. Sla de pagina op en bekijk uw wijzigingen.
1. Check de pagina in en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Waarschuwingsmodule](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Module voor het plaatsen van inhoud](add-content-placement-modules.md)

[Functiemodule](add-feature-module.md)

[Videospelermodule](add-video-player.md)

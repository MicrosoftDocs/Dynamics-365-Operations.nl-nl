---
title: Tegellijstmodule
description: In dit artikel wordt beschreven wat tegellijstmodules zijn en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 204465df80e490c8f3f4dc5aca04cb43cd853515
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284625"
---
# <a name="tile-list-module"></a>Tegellijstmodule

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat tegellijstmodules zijn en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Een tegellijstmodule is een verzameling tegels in een carrousel. Deze wordt gebruikt om productcategorieën of productmerken op de markt te brengen via afbeeldingen en tekst. Een detailhandelaar kan bijvoorbeeld een tegellijstmodule toevoegen aan de startpagina van een e-commercesite om alle best verkopende categorieën te promoten.

Een tegellijstmodule wordt gestuurd door gegevens uit het Content Management System (CMS). Dit is niet afhankelijk van andere modules of gegevens uit Commerce Headquarters. De tegellijstmodule kan aan elke sitepagina worden toegevoegd waar een detailhandelaar iets wil verhandelen of promoten (bijvoorbeeld producten, categorieën of merken).

In de volgende afbeelding ziet u een voorbeeld van een tegellijstmodule en tegelmodules op de startpagina van Adventure Works.

![Voorbeeld van een tegellijstmodule en tegelmodules op de startpagina van Adventure Works](./media/Tile_list.PNG)

> [!IMPORTANT]
> De tegellijstmodule is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.20.
> Een voorbeeld van de tegellijstmodule is opgenomen in het Adventure Works-thema.

## <a name="tile-list-modules-and-themes"></a>Tegellijstmodules en thema's

De tegellijstmodule kan verschillende indelingen en stijlen ondersteunen op basis van een thema. In het Adventure Works-thema bieden tegels bijvoorbeeld een animatie-effect wanneer sitegebruikers de aanwijzer erop plaatsen. Elk thema kan extra eigenschappen bevatten voor de tegellijst en tegelmodules. Themaontwikkelaars kan tevens extra indelingen bouwen voor de tegellijst en tegelmodules.

## <a name="tile-list-module-properties"></a>Eigenschappen van tegellijstmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Koptekst       | Koptekst en tag van koptekst | Een koptekst voor de tegellijstmodule. |

## <a name="tile-module-properties"></a>Eigenschappen van tegelmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Afbeelding         | Afbeeldingbestand | Een afbeelding kan worden gebruikt voor de presentatie van een product of categorie. De afbeelding kan worden geüpload naar de Mediabibliotheek in Commerce Site Builder of er kan een bestaande afbeelding worden gebruikt. |
| Koptekst       | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Standaard wordt het koptekstlabel **H2** gebruikt voor de koptekst, maar het label kan desgewenst worden gewijzigd voor toegankelijkheidsvereisten. |
| Alinea     | Alineatekst | De module ondersteunt alineatekst in RTF-indeling. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals hyperlinks en vetgedrukte, onderstreepte en cursieve tekst. Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast. |
| Koppeling          | Koppelingstekst, koppelings-URL, het label Accessible Rich internet Applications (ARIA) en **Koppeling in nieuw tabblad openen** | Modules ondersteunen een of meer koppelingen met oproep tot actie. Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist. ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen. U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad. |
| Tegelkoppeling     | Koppelingstekst, koppelings-URL, ARIA-label en kiezer **Koppeling in nieuw tabblad openen** | Met deze eigenschap kunt u een koppeling naar een oproep tot actie definiëren. Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist. ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen. U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad.|
| Pictogram          | Afbeelding | Naast een product- of categorieafbeelding kan een pictogramsymbool worden toegevoegd. Het pictogramsymbool wordt boven de afbeelding van het product of de categorie weergegeven. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Een tegellijstmodule toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een tegellijstmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en open de marketingsjabloon voor de startpagina van uw site (of maak een nieuwe marketingsjabloon).
1. Selecteer in het vak **Hoofdonderdeel** van de standaardpagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Tegellijst** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en open de startpagina van de site (of maak een nieuwe startpagina met de marketingsjabloon).
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Tegellijst** en selecteer vervolgens **OK**.
1. Voeg een koptekst toe in het eigenschappenvenster van de tegellijstmodule.
1. Selecteer in het vak **Tegellijst** de knop met het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Tegelmodule** en selecteer vervolgens **OK**.
1. Voeg in het eigenschappenvenster van de tegelmodule een afbeelding, een koptkes en een pictogramsymbool toe.
1. Voeg waar nodig extra tegelmodules toe en configureer deze.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Adventure Works-thema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

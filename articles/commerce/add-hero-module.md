---
title: Inhoudsblokmodule
description: In dit artikel wordt beschreven wat inhoudsblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: dc6d728f49befd0c156340379dba05f592ca7919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276995"
---
# <a name="content-block-module"></a>Inhoudsblokmodule

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat inhoudsblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Een inhoudsblokmodule wordt gebruikt voor de marketing van producten of promoties via een combinatie van afbeeldingen en tekst. Zo kan een detailhandelaar een inhoudsblokmodule toevoegen aan de startpagina van een e-Commerce-site om een nieuw product te promoten en de aandacht van klanten te trekken.

Een inhoudsblokmodule wordt gestuurd door gegevens uit het Content Management System (CMS). Het is een zelfstandige module die niet afhankelijk is van andere modules op de pagina. Een inhoudsblokmodule kan op elke sitepagina worden geplaatst waar een detailhandelaar iets wil verhandelen of promoten (bijvoorbeeld producten, verkoop of functies).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Voorbeelden van inhoudsblokmodules in e-Commerce

- U kunt een inhoudsblokmodule gebruiken op de startpagina van een e-Commerce-site om promoties en nieuwe producten te markeren.
- U kunt een inhoudsblokmodule op een pagina met productgegevens gebruiken om productinformatie te presenteren.
- Er kunnen meerdere inhoudsblokmodules in een carrouselmodule worden geplaatst om meerdere producten of promoties te markeren.

## <a name="content-block-modules-and-themes"></a>Inhoudsblokmodules en thema's

Inhoudsblokmodules kunnen verschillende indelingen en stijlen ondersteunen op basis van een thema. Het Fabrikam-thema ondersteunt bijvoorbeeld drie opmaakvarianten van een inhoudsblokmodule: hero, functie en tegel. De hero-indeling toont een afbeelding op de achtergrond met tekst eroverheen. De functie-indeling toont een afbeelding en tekst naast elkaar. Met de tegelindeling kunnen meerdere inhoudsblokken in een tegelindeling worden weergegeven.

Bovendien kan het thema verschillende eigenschappen voor elke indeling tonen. Een themaontwikkelaar kan met de inhoudsblokmodule meer stijlen maken.

In de volgende afbeelding ziet u een voorbeeld van een inhoudsblokmodule met een hero-indeling.

![Voorbeeld van een heldmodule.](./media/Hero.PNG)

In de volgende afbeelding ziet u een voorbeeld van een inhoudsblokmodule met een functie-indeling.

![Voorbeelden van functiemodules.](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Eigenschappen van inhoudsblokmodules

| Naam van eigenschap.  | Waarden | Beschrijving |
|----------------|--------|-------------|
| Afbeelding          | Afbeeldingbestand | Een afbeelding kan worden gebruikt voor de presentatie van een product of promotie. Een afbeelding kan naar de afbeeldingengalerie worden geüpload, of er kan een bestaande afbeelding worden gebruikt. |
| Koptekst        | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Elke heldmodule kan een koptekst hebben. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |
| Alinea      | Alineatekst | Heldmodules ondersteunen alineatekst in RTF-indeling. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst en hyperlinks. Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast. |
| Koppeling           | Koppelingstekst, koppelings-URL, het label Accessible Rich internet Applications (ARIA) en **Koppeling in nieuw tabblad openen** | Heldmodules ondersteunen een of meer koppelingen met oproep tot actie. Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist. ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen. U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Eigenschappen van inhoudsblokmodules, weergegeven door het Fabrikam-thema 

| Naam van eigenschap.  | Waarden | Beschrijving |
|----------------|--------|-------------|
| Tekstplaatsing | **Links**, **Rechts**, **Midden** | Met deze eigenschap wordt de positie van de tekst in de afbeelding bepaald. Deze is alleen van toepassing op de hero-indeling. |
| Tekstthema     | **Licht** of **donker** | Er kan een kleurenschema worden gedefinieerd voor de tekst op basis van de achtergrondafbeelding. Als de afbeelding bijvoorbeeld een donkere achtergrond heeft, kan een licht thema worden toegepast om de tekst beter zichtbaar te maken en om te voldoen aan de kleurcontrastverhoudingen voor toegankelijkheidsdoeleinden. Deze is alleen van toepassing op de hero-indeling.|
| Plaatsing van afbeelding       | **Links**, **Rechts** | Deze eigenschap geeft aan of de afbeelding links of rechts van de tekst moet staan. Deze is alleen van toepassing op de functie-indeling.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Een inhoudsblokmodule toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een heldmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en maak een paginasjabloon met de naam **Inhoudsbloksjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een heldmodule toe.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Gebruik de hero-sjabloon die u zojuist hebt gemaakt om een pagina met de naam **Inhoudsblokpagina** te maken.
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de heldmodule en selecteer vervolgens **OK**.
1. Selecteer in de overzichtsstructuur aan de linkerkant de inhoudsblokmodule.
1. Selecteer **Een afbeelding toevoegen** in het eigenschappenvenster aan de rechterkant. Selecteer vervolgens een bestaande afbeelding of upload een nieuwe afbeelding.
1. Selecteer **Koptekst**.
1. Voeg in het dialoogvenster **Koptekst** de koptekst toe, selecteer het kopniveau en selecteer vervolgens **OK**.
1. Voeg onder **RTF-indeling** de gewenste tekst toe.
1. Selecteer **Koppeling toevoegen**.
1. Voeg in het dialoogvenster **Koppeling** de koppelingstekst, een koppelings-URL en een ARIA-label voor de koppeling toe en selecteer vervolgens **OK**.
1. Selecteer de **Hero**-indeling.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Promotiebanner-module](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Text Block-module](add-content-rich-block.md)

[Videospelermodule](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

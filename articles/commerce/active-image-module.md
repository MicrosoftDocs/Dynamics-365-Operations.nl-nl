---
title: Module voor actieve afbeeldingen
description: In dit onderwerp wordt beschreven wat modules voor actieve afbeeldingen zijn en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 36b7d6dea87c7f309c07608794d443a0ae19be211847d2cddcad95f2d933a8db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716903"
---
# <a name="active-image-module"></a>Module voor actieve afbeeldingen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat modules voor actieve afbeeldingen zijn en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Een module voor actieve afbeeldingen kan worden gebruikt om productlabels in een afbeelding in te voegen. Gebruikers van de e-Commercesite kunnen vervolgens de aanwijzer boven de labels plaatsen om een voorbeeld van producten weer te geven die in de afbeelding worden weergegeven. De voorbeelden worden weergegeven in pop-upvensters. Als u een pop-upvenster voor een voorbeeld selecteert, kunnen gebruikers rechtstreeks naar de pagina met productdetails (PDP) voor het bijbehorende product gaan.

De labels worden gedefinieerd met behulp van X- en Y-coördinaten in de afbeelding. Elk gelabeld punt moet worden geconfigureerd met de product-id van het product dat in de afbeelding wordt weergegeven.

In de volgende afbeelding ziet u een voorbeeld van een pop-upvenster met een voorbeeld van een hero-afbeelding op de startpagina van Adventure Works.

![Voorbeeld van een pop-upvenster voor een voorbeeld in een module voor actieve afbeeldingen](./media/Active_image.PNG)

> [!IMPORTANT]
> - De module voor actieve afbeeldingen is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.20.
> - Een voorbeeld van de module voor actieve afbeeldingen is opgenomen in het Adventure Works-thema.

## <a name="active-image-module-properties"></a>Eigenschappen van module voor actieve afbeeldingen

| Naam van eigenschap.      | Waarden | Beschrijving |
|--------------------|--------|-------------|
| Afbeelding              | Afbeeldingbestand | Een afbeelding kan worden gebruikt voor de presentatie van een of meer producten. De afbeelding kan worden geüpload naar de Mediabibliotheek in Commerce Site Builder of er kan een bestaande afbeelding worden gebruikt. |
| Breedte              | Aantal pixels | Met deze eigenschap wordt de breedte van de afbeelding bepaald. De actieve coördinaten worden berekend op basis van de breedte van de afbeelding.|
| Actieve coördinaten | X- en Y-coördinaten en een product-id-nummer | Elke actieve afbeeldingsmatrix bestaat uit X- en Y-coördinaten en een product-id-nummer.|
| Koptekst            | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Standaard wordt het koptekstlabel **H2** gebruikt voor de koptekst, maar het label kan desgewenst worden gewijzigd voor toegankelijkheidsvereisten. |
| Alinea          | Alineatekst | De module ondersteunt alineatekst in RTF-indeling. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals hyperlinks en vetgedrukte, onderstreepte en cursieve tekst. Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast. |
| Koppeling               | Koppelingstekst, koppelings-URL, label Accessible Rich internet Applications (ARIA) en selectie **Koppeling in nieuw tabblad openen** | De module ondersteunt een of meer koppelingen met oproep tot actie. Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist. ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen. U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad. |
| Subtekst           | Koptekst, tekst en koppelingen | Er kan extra context voor de afbeelding worden toegevoegd, zoals een auteurs- of ontwerpernaam, of koppelingen naar persoonlijke blogs.|
| Tekstthema         | **Licht** of **donker** | Met deze eigenschap kan een gebruiker de tekst instellen op licht of donker, op basis van de achtergrondafbeelding. Deze is beschikbaar als thema-extensie in het thema van Adventure Works. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Een module voor actieve afbeeldingen toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een module voor actieve afbeeldingen aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en open de marketingsjabloon voor de startpagina van uw site (of maak een nieuwe marketingsjabloon).
1. Selecteer in het vak **Hoofdonderdeel** van de standaardpagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Actieve afbeelding** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en open de startpagina van de site (of maak een nieuwe startpagina met de marketingsjabloon).
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Actieve afbeelding** en selecteer vervolgens **OK**.
1. Voeg in het eigenschappenvenster van de module voor actieve afbeeldingen een afbeelding toe en stel de breedte van het canvas in op de grootte van de afbeelding.
1. Stel de X- en Y-coördinaten in en voeg het toepasselijke product-id-nummer toe.
1. Voeg waar nodig extra modules voor actieve afbeeldingen toe en configureer deze.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Adventure Works-thema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

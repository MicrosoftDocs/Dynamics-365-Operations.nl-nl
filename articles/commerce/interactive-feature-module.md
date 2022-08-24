---
title: Module voor interactieve functies
description: In dit artikel worden modules voor interactieve functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 7922ae892d75099ca22df55a7237cf57cfa45cc7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284709"
---
# <a name="interactive-feature-module"></a>Module voor interactieve functies

[!include [banner](includes/banner.md)]

In dit artikel worden modules voor interactieve functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Microsoft Dynamics 365 Commerce.

Modules voor interactieve functies zijn modules die kunnen worden gebruikt om meerdere productcategorieën of productmerken op de markt te brengen door een combinatie van afbeeldingen en tekst te gebruiken. Een detailhandelaar kan bijvoorbeeld een module voor interactieve functies toevoegen aan de startpagina van een e-commercesite om alle best verkopende categorieën te promoten. De module voor interactieve functies lijkt op de tegellijstmodule, maar heeft een andere indeling en andere interactiefuncties.

Elke module voor interactieve functies is een verzameling modules met interactieve functie-items. Elke module met functie-items wordt aangestuurd door gegevens uit het Content Management System (CMS). Dit is niet afhankelijk van andere modules of gegevens uit Commerce Headquarters. De module voor interactieve functies kan aan elke sitepagina worden toegevoegd waar een detailhandelaar iets wil verhandelen of promoten (bijvoorbeeld producten, categorieën of merken).

> [!IMPORTANT]
> - De module voor interactive functies is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.20.
> - Een voorbeeld van de module voor interactieve functies is opgenomen in het Adventure Works-thema.

In de volgende afbeelding ziet u een voorbeeld van een module voor interactieve functies op de startpagina van Adventure Works.

![Voorbeeld van een module voor interactieve functies op de startpagina van Adventure Works](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Module voor interactieve functies en thema's

De module voor interactieve functies kan verschillende indelingen en stijlen ondersteunen op basis van een thema. In het Adventure Works-thema heeft de module voor interactieve functies bijvoorbeeld een indeling met twee kolommen die interactieve effecten laat zien wanneer een sitegebruiker de aanwijzer over elk item beweegt. De module voor interactieve functies is geoptimaliseerd voor een even aantal afbeeldingen in een indeling met twee kolommen.

## <a name="interactive-feature-module-properties"></a>Eigenschappen van module voor interactieve functies

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Koptekst       | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Een koptekst voor de module voor interactieve functies. |

## <a name="interactive-feature-item-module-properties"></a>Eigenschappen van module voor interactieve functie-items

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Afbeelding         | Afbeeldingbestand | Een afbeelding die een product of categorie vertegenwoordigt. De afbeelding kan worden geüpload naar de Mediabibliotheek in Commerce Site Builder of er kan een bestaande afbeelding worden gebruikt. |
| Koptekst       | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Standaard wordt het koptekstlabel **H2** gebruikt voor de koptekst, maar het label kan desgewenst worden gewijzigd voor toegankelijkheidsvereisten. |
| Alinea     | Alineatekst | De module ondersteunt alineatekst in RTF-indeling. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals hyperlinks en vetgedrukte, onderstreepte en cursieve tekst. Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast. |
| Koppeling          | Koppelingstekst, koppelings-URL, label Accessible Rich internet Applications (ARIA) en selectie **Koppeling in nieuw tabblad openen** | De module ondersteunt een of meer koppelingen met oproep tot actie. Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist. ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen. U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Een module voor interactieve functies toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een module voor interactieve functies toe te voegen aan een nieuwe pagina en de vereiste eigenschappen in te stellen in Commerce Site Builder.

1. Ga naar **Sjablonen** en open de marketingsjabloon voor de startpagina van uw site (of maak een nieuwe marketingsjabloon).
1. Selecteer in het vak **Hoofdonderdeel** van de standaardpagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Interactieve functie** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en open de startpagina van de site (of maak een nieuwe startpagina met de marketingsjabloon).
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** onder **Modules selecteren** de module **Interactieve functie** en selecteer vervolgens **OK**.
1. Voeg een koptekst toe in het eigenschappenvenster van de module voor interactieve functies.
1. Selecteer in het vak **Interactieve functies** de knop met het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Interactief functie-item** en selecteer vervolgens **OK**.
1. Voeg een afbeelding, een koptekst, een alineatekst en een URL toe in het eigenschappenvenster van de module voor interactieve functie-items.
1. Voeg waar nodig extra modules voor interactieve functie-items toe en configureer deze.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Adventure Works-thema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

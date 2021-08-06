---
title: Afbeeldingslijstmodule
description: In dit onderwerp wordt beschreven wat afbeeldingslijstmodules zijn en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b7e070bfe562bb1a28b10d4632725b53a090cda4
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638825"
---
# <a name="image-list-module"></a>Afbeeldingslijstmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat afbeeldingslijstmodules zijn en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

De afbeeldingslijstmodule kan worden gebruikt om eenvoudig een verzameling (matrix) van afbeeldingen aan sitepagina's toe te voegen. Elke afbeelding in de matrix kan worden geconfigureerd met alineatekst en koppelings-URL's. De afbeeldingslijstmodule is het meest geschikt voor het weergeven van merklogo's of een lijst met logo's.

> [!IMPORTANT]
> - De afbeeldingslijstmodule is beschikbaar in de modulebibliotheek van Commerce vanaf Dynamics 365 Commerce versie 10.0.20.
> - Een voorbeeld van de afbeeldingslijstmodule is opgenomen in het Adventure Works-thema.

De onderstaande afbeelding toont een voorbeeld waarin in een afbeeldingslijstmodule een lijst met tekst met logo's op een B2C-sitepagina (Business-to-Consumer) van Adventure Works wordt weergegeven.

![Voorbeeld van een afbeeldingslijstmodule met een lijst met tekst met logo's](./media/Image_list.PNG)

De onderstaande afbeelding toont een voorbeeld waarin in een afbeeldingslijstmodule merklogo's op een B2B-sitepagina (Business-to-Business) van Adventure Works wordt weergegeven.

![Voorbeeld van een afbeeldingslijstmodule met merklogo's](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Eigenschappen van afbeeldingslijstmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Koptekst       | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Een koptekst voor de afbeeldingslijstmodule. |
| Afbeeldingslijst    | Afbeeldingen, tekst en URL's | Elk item in de matrix is een afbeelding die wordt aangevuld met alineatekst en een URL. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Een afbeeldingslijstmodule toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een afbeeldingslijstmodule toe te voegen aan een nieuwe pagina en de vereiste eigenschappen in te stellen in Commerce Site Builder.

1. Ga naar **Sjablonen** en open de marketingsjabloon voor de startpagina van uw site (of maak een nieuwe marketingsjabloon).
1. Selecteer in het vak **Hoofdonderdeel** van de standaardpagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Afbeeldingslijst** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en open de startpagina van de site (of maak een nieuwe startpagina met de marketingsjabloon).
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Afbeeldingslijst** en selecteer vervolgens **OK**.
1. Voeg in het eigenschapvenster voor de afbeeldingslijstmodule een koptekst toe (bijvoorbeeld **Onze merken**).
1. Voeg een afbeeldingslijstitem toe en geef een afbeelding, alineatekst en een omleidings-URL op.
1. Voeg waar nodig extra modules voor afbeeldingslijstitems toe en configureer deze.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Adventure Works-thema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Module Container
description: In dit onderwerp worden containermodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43017cbb76c38eed6951a9e87c763cf919c3bd93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206410"
---
# <a name="container-module"></a>Containermodule

[!include [banner](includes/banner.md)]

In dit onderwerp worden containermodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Een container module is een module waarin andere modules worden gehost. Het primaire doel van een containermodule is het definiëren van de indeling van de modules die de container bevat, door de ingestelde eigenschappen. Deze modules kunnen bijvoorbeeld naast elkaar worden weergegeven in een indeling met twee kolommen, drie kolommen, vier kolommen of zes kolommen. Ze kunnen ook worden beperkt tot de breedte van de container of ze kunnen het scherm vullen. Er kan een koptekst aan elke containermodule worden toegevoegd.

Drie containermodules worden ondersteund: container, container met 2 vakken en container met 3 vakken. Modules van elk type kunnen in deze containers worden geplaatst. 

> [!NOTE] 
> Het is raadzaam om modules altijd in een containermodule te plaatsen, zodat deze kunnen worden beperkt tot de breedte van de container.

## <a name="examples-of-container-modules-in-e-commerce"></a>Voorbeelden van containermodules in e-commerce

- Een auteur van een site wil een indeling met drie kolommen, waarbij drie modules naast elkaar worden weergegeven. Daarom gebruikt de auteur van de site een containermodule met een container van het type met 3 vakken.
- Een auteur van een site wil een indeling met zes kolommen, waarbij zes modules naast elkaar worden weergegeven. Daarom gebruikt de auteur van de site een container van het type met zes kolommen.
- Een auteur van een site wil een module op een pagina plaatsen, maar wil niet dat deze schermvullend is. Daarom voegt de auteur van de site de module toe aan een containermodule en wordt de eigenschap **Breedte** van de containeringesteld op **Passend in container**.

De volgende afbeelding toont een voorbeeld van een containermodule die een carrouselmodule bevat in Commerce Site Builder. In dit voor beeld wordt de eigenschap **Breedte** van de containermodule ingesteld op **Scherm vullen**.

![Voorbeeld van een containermodule](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Eigenschappen van containermodule

| Naam van eigenschap.     | Waarden | Omschrijving |
|-------------------|--------|-------------|
| Koptekst           | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Er kan een optionele koptekst voor de container worden opgegeven. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |
| Breedte             | **Passen in container** of **Scherm vullen** | Als de waarde wordt ingesteld op **Passen in container** (de standaardwaarde), zijn de modules in de container beperkt tot de breedte van de container. Als de waarde is ingesteld op **Scherm vullen**, zijn de modules niet beperkt tot de breedte van de container maar kunnen ze het scherm vullen. |
| Aantal kolommen | **1**, **2**, **3**, **4**, **6** of **12** | Met deze eigenschap wordt het aantal kolommen in de container bepaald. Een container kan maximaal 12 kolommen bevatten. |

## <a name="container-with-2-slots"></a>Container met 2 ruimten

De container van het type met 2 vakken is geoptimaliseerd voor een indeling met twee kolommen. Dit type container heeft twee vakken die naast elkaar kunnen worden weergegeven in de modules in de container.

U kunt aanvullende eigenschappen gebruiken om de indeling te optimaliseren voor verschillende viewports (mobiele apparaten, tablets, computers, enzovoort). Voor elke viewport kan de breedte van elke kolom worden gedefinieerd. De volgende instellingen voor de kolombreedte zijn beschikbaar:

- **75%/25%**: de eerste module heeft een kolombreedte van 75 procent en de tweede module heeft een kolombreedte van 25 procent. Er is ook een optie van **25%/75%** beschikbaar.
- **50%/50%**: beide modules hebben dezelfde kolombreedte.
- **67%/33%**: de eerste module heeft een kolombreedte van 67 procent en de tweede module heeft een kolombreedte van 33 procent. Er is ook een optie van **33%/67%** beschikbaar.
- **100%**: beide modules hebben een volledige kolombreedte. Daarom worden de modules verticaal gestapeld in één kolom. Hoewel deze indeling met één kolom in strijd is met de container van het type met 2 vakken, kan het handig zijn voor sommige viewports (bijvoorbeeld voor kleine mobiele apparaten).

### <a name="container-with-2-slots-properties"></a>Eigenschappen van container met 2 vakken

| Naam van eigenschap.                   | Waarden | Beschrijving |
|---------------------------------|--------|-------------|
| Koptekst                         | Koptekst en tag van koptekst | Er kan een optionele koptekst voor de container worden opgegeven. |
| Configuratie voor extra kleine viewport | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** of **100%** | Met deze eigenschap wordt de indeling gedefinieerd voor extra kleine viewports. |
| Configuratie voor kleine viewport   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** of **100%** | Met deze eigenschap wordt de indeling gedefinieerd voor kleine viewports, zoals mobiele apparaten. |
| Configuratie voor middelgrote viewport  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** of **100%** | Met deze eigenschap wordt de indeling gedefinieerd voor middelgrote viewports, zoals tablets. |
| Configuratie voor grote viewport   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** of **100%** | Met deze eigenschap wordt de indeling gedefinieerd voor grote viewports, zoals computers. |

## <a name="container-with-3-slots"></a>Container met 3 ruimten

De container met het moduletype met 3 vakken is geoptimaliseerd voor een indeling met drie kolommen.

U kunt aanvullende eigenschappen gebruiken om de indeling van verschillende viewports te optimaliseren. Voor elke viewport kan de breedte van elke kolom worden gedefinieerd. De volgende instellingen voor de kolombreedte zijn beschikbaar:

- **33%/33%/33%**: alle drie modules hebben dezelfde kolombreedte.
- **50%/25%/25%**: de eerste module heeft een kolombreedte van 50 procent en elk van de resterende twee modules heeft een kolombreedte van 25 procent. De opties **25%/50%/25%** en **25%/25%/50%** zijn ook beschikbaar.
- **16%/16%/67%**: de eerste twee modules hebben elk een kolombreedte van 16 procent en de derde module heeft een kolombreedte van 67 procent. De opties **16%/67%/16%** en **67%/16%/16%** zijn ook beschikbaar.

### <a name="container-with-3-slots-properties"></a>Eigenschappen van container met 3 vakken

| Naam van eigenschap.                   | Waarden | Beschrijving |
|---------------------------------|--------|-------------|
| Koptekst                         | Koptekst en tag van koptekst | Er kan een optionele koptekst voor de container worden toegevoegd. |
| Configuratie voor extra kleine viewport | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** of **67%/16%/16%** | Met deze eigenschap wordt de indeling gedefinieerd voor extra kleine viewports. |
| Configuratie voor kleine viewport   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** of **67%/16%/16%** | Met deze eigenschap wordt de indeling gedefinieerd voor kleine viewports, zoals mobiele apparaten. |
| Configuratie voor middelgrote viewport  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** of **67%/16%/16%** | Met deze eigenschap wordt de indeling gedefinieerd voor middelgrote viewports, zoals tablets. |
| Configuratie voor grote viewport   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** of **67%/16%/16%** | Met deze eigenschap wordt de indeling gedefinieerd voor grote viewports, zoals computers. |

## <a name="add-a-container-module-to-a-page"></a>Een containermodule toevoegen aan een pagina

Voer de volgende stappen uit om een containerspelermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Containersjabloon** in en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren. 
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** de sjabloon van de videospeler die u hebt gemaakt. Voer onder **Paginanaam** **Containerpagina** in en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster voor de containermodule de eigenschap **Aantal kolommen** in op **1** en de eigenschap **Breedte** op **Container vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Inhoudsblok** en selecteer vervolgens **OK**.
1. Configureer in het eigenschappenvenster voor de inhoudsblokmodule de kop, de afbeelding en de indeling.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Er moet een functiemodule worden weergegeven die past binnen de breedte van de containermodule.
1. Wijzig in het eigenschappenvenster voor de containermodule de waarde van de eigenschap **Aantal kolommen** in **3**.
1. Voeg twee extra inhoudsblokmodules toe aan de containermodule en configureer deze.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Er worden nu drie inhoudsblokmodules naast elkaar weergegeven.
1. Nadat u de gewenste indeling hebt gemaakt, selecteert u **Bewerken voltooien** om de pagina in te checken en vervolgens **Publiceren** om deze te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Accordeonmodule](add-accordion.md)

[Tabbladmodule](add-tab.md)

[Carrouselmodule](add-carousel.md)

[Text Block-module](add-content-rich-block.md)

[Module met vakje voor kopen](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Betalingsmodule](add-checkout-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
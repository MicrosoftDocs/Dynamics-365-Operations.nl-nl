---
title: Module Container
description: In dit onderwerp wordt beschreven wat containermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697055"
---
# <a name="container-module"></a>Module Container

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat containermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een container module is een module waarin andere modules worden gehost. Dit is de meest algemene container die wordt gebruikt in Dynamics 365 Commerce. Het primaire doel van een containermodule is het definiëren van de indeling van de opgenomen modules, door de ingestelde eigenschappen. Deze modules kunnen bijvoorbeeld naast elkaar worden weergegeven in een indeling met twee kolommen, drie kolommen, vier kolommen of zes kolommen. Ze kunnen ook worden beperkt tot de breedte van de container of ze kunnen het scherm vullen. Er kan een koptekst aan elke containermodule worden toegevoegd.

Er zijn drie standaardtypen containermodules: container, container met 2 vakken en container met 3 vakken. Modules van elk moduletype kunnen in deze containers worden geplaatst. Er zijn ook speciale typen containermodules, zoals carrousel, uitgebreid blokinhoud, inhoudplaatsing, winkelwagen, kassa, koopvak, koptekst en voettekst. Deze containers hebben specifieke doeleinden en kunnen alleen specifieke ondersteunde moduletypen opnemen.

Het is raadzaam om modules in een container te plaatsen, zodat deze kunnen worden beperkt tot de breedte van de container.

## <a name="examples-of-container-modules-in-e-commerce"></a>Voorbeelden van containermodules in e-commerce

- Een auteur van een site wil een indeling met drie kolommen, waarbij drie modules naast elkaar worden weergegeven. Daarom gebruikt de auteur van de site een containermodule met een container van het type met 3 vakken.
- Een auteur van een site wil een indeling met zes kolommen, waarbij zes modules naast elkaar worden weergegeven. Daarom gebruikt de auteur van de site een container van het type met zes kolommen.
- Een auteur van een site wil een module op een pagina plaatsen, maar wil niet dat deze schermvullend is. Daarom voegt de auteur van de site de module toe aan een containermodule en wordt de eigenschap **Breedte** van de containeringesteld op **Passend in container**.

## <a name="container-module-properties"></a>Eigenschappen van containermodule

| Naam van eigenschap.     | Waarden | Beschrijving |
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

1. Maak een paginasjabloon met de naam **containersjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een containermodule toe.
1. Voeg in de containermodule een functiemodule toe.
1. Check de sjabloon in en publiceer deze.
1. Gebruik de containersjabloon die u zojuist hebt gemaakt om een pagina met de naam **containerpagina** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.
1. Stel in het eigenschappenvenster voor de containermodule de eigenschap **Aantal kolommen** in op **1** en de eigenschap **Breedte** op **Passen in container**.
1. Voeg in de containermodule een functiemodule toe.
1. Configureer een koptekst in het eigenschappenvenster voor de functiemodule.
1. Sla de pagina op en bekijk een voorbeeld. Er moet een functiemodule worden weergegeven die past binnen de breedte van de containermodule.
1. Wijzig in het eigenschappenvenster voor de containermodule de waarde voor de eigenschap **Aantal kolommen** in **3**.
1. Voeg nog twee functiemodules toe aan de containermodule.
1. Sla de pagina op en bekijk een voorbeeld. Er worden nu drie functiemodules naast elkaar worden weergegeven.
1. Nadat u de gewenste indeling hebt verkregen, checkt u de pagina in en publiceert u deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Module voor het plaatsen van inhoud](add-content-placement-modules.md)

[Module voor vakje voor kopen](add-buy-box.md)

[Module Winkelwagen](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)

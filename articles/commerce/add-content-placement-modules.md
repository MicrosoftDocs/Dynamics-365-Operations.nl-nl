---
title: Module voor het plaatsen van inhoud
description: In dit onderwerp worden modules voor het plaatsen van inhoud of inhoudsitems beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785295"
---
# <a name="content-placement-module"></a>Module voor het plaatsen van inhoud

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp worden modules voor het plaatsen van inhoud of inhoudsitems beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een module voor het plaatsen van inhoud is een speciale container waarin andere modules in een specifieke indeling kunnen worden geplaatst. Modules voor plaatsing van inhoud ondersteunen de volgende typen modules als onderliggende modules: item voor inhoudplaatsing, welkomstitem voor account, item voor accountorders, item voor verlanglijst van account en items voor accountprofiel.

Met modules voor plaatsing van inhoud worden gegevens afgeleid uit de onderliggende modules die ze ondersteunen. Daarom kunnen modules voor het plaatsen van inhoud op verschillende manieren worden gebruikt, afhankelijk van de modules die eraan zijn toegevoegd.

Voor de modules voor het plaatsen van inhoud worden zowel afbeeldingen als tekst gebruikt om acties, beleid en productfuncties te presenteren. U kunt bijvoorbeeld een module voor het plaatsen van inhoud op een startpagina gebruiken om winkelbeleid of verzendgegevens weer te geven. Modules voor het plaatsen van inhoud worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst. Ze kunnen echter alleen worden gebruikt binnen een module voor de plaatsing van inhoud.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Voorbeelden van modules voor het plaatsen van inhoud in e-commerce

* Modules voor het plaatsen van specifieke inhouditems kunnen op een startpagina of marketingpagina's worden gebruikt om productfuncties, promoties, winkelinformatie en andere informatie te presenteren via afbeeldingen en tekst.
* Modules voor het plaatsen van inhoudsitems kunnen op de pagina's met productgegevens worden gebruikt om productfuncties te presenteren.
* Modules voor plaatsing van inhoud met een welkomstitem of orders voor het account kunnen worden gebruikt op accountbeheerpagina's.

## <a name="content-placement-module-properties"></a>Eigenschappen van modules voor het plaatsen van inhoud

| Naam van eigenschap. | Waarde | Beschrijving |
|---------------|-------|-------------|
| Breedte         | **Passen in container** of **Scherm vullen** | Als de waarde op **Passen in container** wordt ingesteld, worden de items binnen de module voor het plaatsen van inhoud beperkt tot de breedte van de module. Als de waarde is ingesteld op **Scherm vullen**, zijn de items niet beperkt tot de breedte van de module voor de plaatsing van inhoud, maar gebruiken ze de modus Volledig scherm. |

## <a name="content-placement-item-module-properties"></a>Eigenschappen van modules voor het plaatsen van inhoudsitems

| Naam van eigenschap. | Waarde | Beschrijving |
|---------------|-------|-------------|
| Koptekst       | Koptekst en tags voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Elke module voor plaatsing van inhoudsitems kan een koptekst hebben. De eigenschap **Koptekst** ondersteunt labels voor kopteksten. Standaard wordt het koptekstlabel **H2** gebruikt, maar dit kan desgewenst worden gewijzigd voor toegankelijkheidsvereisten. |
| Alinea     | Alineatekst | Modules voor het plaatsen inhoudsitems ondersteunen alineatekst in RTF-indeling. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst en hyperlinks. Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast. |
| Afbeelding         | Afbeeldingbestand | Er kan een afbeelding aan de tekst worden gekoppeld. |
| Koppeling          | URL van koppeling en koppelingstekst | U kunt een koppeling toevoegen aan de tekst om gebruikers om te leiden naar een specifieke pagina. |
| Tegelgrootte     | Een getal tussen **1** en **12** | Voor elk item voor inhoudsplaatsing wordt met deze eigenschap het aantal vakken gedefinieerd dat de inhoud van het item moet invullen. De maximum grootte van de module voor het plaatsen van inhoud is 12 vakken. Als de totale grootte van de tegel voor de eerste *n* items in de module voor inhoudplaatsing meer dan 12 vakken bevat, worden de items verplaatst naar de volgende rij. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Een module voor het plaatsen van inhoud met inhoudsitems toevoegen op een pagina

Voer de volgende stappen uit om een module voor het plaatsen van inhoud met inhoudsitems toe te voegen aan een nieuwe pagina en de vereiste eigenschappen in te stellen.

1. Maak een paginasjabloon met de naam **sjabloon voor het plaatsen van inhoud**.
1. Voeg in het **hoofdvak** van de standaardpagina een module voor het plaatsen van inhoud toe.
1. Voeg in de module voor het plaatsen van inhoud een module toe voor inhoudsitems.
1. Check de sjabloon in en publiceer deze.
1. Gebruik de sjabloon voor het plaatsen van inhoud die u zojuist hebt gemaakt om een pagina met de naam **Pagina voor het plaatsen van inhoud** te maken.
1. Voeg in het **hoofdvak** van de nieuwe pagina een module voor het plaatsen van inhoud toe.
1. Voeg in de module voor het plaatsen van inhoud een module toe voor inhoudsitems.
1. Selecteer een afbeelding in het eigenschappenvenster voor de module voor plaatsing van inhoudsitems. Voeg vervolgens een kop, een alinea en een koppeling toe, stel de URL van de koppeling in en stel de grootte van de tegel in op **6**.
1. Herhaal stap 7 en 8 om nog een module voor plaatsing van inhoudsitems met dezelfde tegelgrootte toe te voegen.
1. Sla de pagina op en bekijk een voorbeeld. U ziet nu twee inhoudplaatsingitems die naast elkaar worden weergegeven. U kunt de eigenschap voor de **Tegelgrootte** van elke module voor de plaatsing van inhoudsitems aanpassen of meer modules toevoegen om de gewenste indeling te bereiken.
1. Check de pagina in en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Waarschuwingsmodule](add-alert.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Functiemodule](add-feature-module.md)

[Heldmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)

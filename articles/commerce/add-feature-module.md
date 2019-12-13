---
title: Functiemodule
description: In dit onderwerp worden modules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785278"
---
# <a name="feature-module"></a>Functiemodule 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp worden modules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een functiemodule wordt gebruikt voor de marketing van producten of promoties via een combinatie van afbeeldingen en tekst. Een detailhandelaar kan bijvoorbeeld een functiemodule aan een pagina met productgegevens toevoegen om de functies van het product te markeren.

Een functiemodule wordt gestuurd door gegevens uit het Content Management System (CMS). Het is een zelfstandige module die niet afhankelijk is van andere modules op de pagina. Een functiemodule kan op elke sitepagina worden geplaatst waar een detailhandelaar iets wil verhandelen of promoten (bijvoorbeeld producten, verkoop of functies).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Voorbeelden van functiemodules in e-commerce

Een functiemodule kan op de volgende pagina's worden gebruikt:

- Een pagina met productgegevens om productfuncties te presenteren
- De startpagina om producten te promoten
- Een categoriepagina om een categorie met producten te markeren

## <a name="feature-module-properties"></a>Eigenschappen van functiemodule

| Naam van eigenschap.     | Waarden | Beschrijving |
|-------------------|--------|-------------|
| Afbeelding             | Afbeeldingbestand | Een afbeelding kan worden gebruikt voor marketing van het product of de promotie. Een afbeelding kan naar de afbeeldingengalerie worden geüpload, of er kan een bestaande afbeelding worden gebruikt. |
| Koptekst           | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | Elke functiemodule kan een koptekst hebben. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |
| Alinea         | Alineatekst | Functiemodules ondersteunen alineatekst in RTF-indeling. Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst en hyperlinks. Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast. |
| Koppeling              | Koppelingstekst, koppelings-URL, het label Accessible Rich internet Applications (ARIA) en **Koppeling in nieuw tabblad openen** | Functiemodules ondersteunen een of meer koppelingen met oproep tot actie. Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist. ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen. U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad. |
| Plaatsing van afbeelding   | **Rechts**, **Links**, **Boven** of **Onder** | Met deze eigenschap wordt de positie van de afbeelding ten opzichte van de tekst bepaald. Als bijvoorbeeld **Rechts** is geselecteerd, wordt de afbeelding rechts van de tekst weergegeven. |
| Grootte afbeeldingskolom | Een waarde tussen **1** en **12** | Met deze eigenschap wordt de grootte van de afbeelding ten opzichte van de tekst bepaald. De grootte wordt uitgedrukt als een aantal kolommen op de pagina. Een pagina bevat 12 kolommen. De afbeelding en tekst hebben standaard dezelfde grootte (zes kolommen elk). De grootte kan echter zo nodig worden aangepast. |

## <a name="add-a-feature-module-to-a-new-page"></a>Een functiemodule toevoegen aan een nieuwe pagina 

Voer de volgende stappen uit om een functiemodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en maak een paginasjabloon met de naam **functiesjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een functiemodule toe.
1. Check de sjabloon in en publiceer deze.
1. Gebruik de functiesjabloon die u zojuist hebt gemaakt om een pagina met de naam **functiepagina** te maken.
1. Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** onder **Modules selecteren** een functiemodule en selecteer vervolgens **OK.**
1. Selecteer in de overzichtsstructuur aan de linkerkant de functiemodule.
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

[Heldmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)

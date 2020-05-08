---
title: Promospandoekmodule
description: In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269769"
---
# <a name="promo-banner-module"></a>Promospandoekmodule


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Promobannermodules worden gebruikt om inline informatie op een pagina weer te geven. Ze kunnen worden gebruikt om promoties op alle pagina's van een e-commerce-site weer te geven. 

Promobannermodules ondersteunen een tekstbericht en een koppeling. Als er meerdere berichten aan een promobannermodule worden toegevoegd, verandert deze in een draaiende carrouselbanner waarmee klanten door alle berichten kunnen bladeren. 

Promobannermodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Gebruiksvoorbeelden van promotiebanners in e-Commerce

Promobanners kunnen in de koptekst van een site worden gebruikt om promoties of berichten voor de hele site weer te geven, zoals in de volgende voorbeelden.

"Jaarlijkse uitverkoop eindigt over 10 dagen"

"Grote besparingen bij terug naar school. Winkel nu."

## <a name="promo-banner-module-properties"></a>Eigenschappen van promobannermodules

| Naam van eigenschap.             | Value                              | Beschrijving |
|---------------------------|------------------------------------|-------------|
| Bannerberichten           | Tekst en koppelingen                     | Een matrix met tekst en koppelingen. |
| Automatisch afspelen                  | **True** of **False**              | Een waarde die aangeeft of berichten automatisch worden doorlopen als er meerdere berichten zijn geconfigureerd. |
| Interval voor diaovergang | Een aantal milliseconden (ms)      | Het interval voor het doorlopen van berichten. |
| Negeren toestaan             | **True** of **False**              | Als de waarde is ingesteld op **True**, kunnen klanten de waarschuwing sluiten. |
| Carrouselflipper weergeven     | **True** of **False**              | Een waarde die aangeeft of de carrouselflippers moeten worden weergegeven, zodat klanten handmatig meerdere banneritems kunnen doorlopen. |
| Tekstuitlijning            | **Rechts**, **Links** of **Midden** | De tekstuitlijning in de promobannermodule. |
| Koppeling                      | Een URL                              | Een URL voor een optionele koppeling. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Een promobannermodule toevoegen aan een pagina 

Voer de volgende stappen uit om een promobannermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Selecteer **Nieuw** om een paginasjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Sjabloon voor promobanner** in en selecteer vervolgens **OK**.
1. Voeg onder **Paginaoverzicht** een **Standaardpagina**module aan de **Hoofd**sleuf toe. 
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren. 
1. Gebruik de sjabloon die u zojuist hebt gemaakt om een pagina met de naam **Promobannerpagina** te maken. 
1. Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe. 
1. Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Container vullen**.
1. Voeg onder **Paginaoverzicht** een promobannermodule aan de containermodule toe.
1. Voeg in de instellingen voor de bannermodule een of meer bannerberichten toe. Elk bericht kan tekst bevatten met een koppeling. U kunt de andere eigenschappen bewerken als u de module verder wilt aanpassen.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken. Bovenaan de pagina wordt een waarschuwing weergegeven die de tekst toont die u hebt toegevoegd.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren. 

> [!NOTE]
> Een promobanner wordt meestal gebruikt in de sleuf van een paginakoptekst of een sleuf van een subkoptekst.


## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Carrouselmodule](add-carousel.md)

[Tekstblokmodule](add-content-rich-block.md)

[Inhoudsblokmodule](add-hero-module.md)

[Videospelermodule](add-video-player.md)

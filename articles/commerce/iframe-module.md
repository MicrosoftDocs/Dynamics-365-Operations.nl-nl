---
title: Iframe-module
description: In dit onderwerp wordt beschreven wat de iframe-module is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665391"
---
# <a name="iframe-module"></a>Iframe-module

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat de iframe-module is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een iframe-module biedt een iframe (inline frame) dat de host is van externe inhoud op een site. Het kan bijvoorbeeld worden gebruikt om een YouTube-video of PDF-bestandsviewer te hosten op een sitepagina. 

Voor een iframe-module is een doel-URL vereist. Vervolgens wordt de inhoud van de doelpagina binnen een HTML **iframe**-element gehost. Externe URL's moeten worden vermeld in de toegestane lijst volgens de CSP-instructies (Content Security Policy) van de site. Voor iframe-inhoud moeten URL's worden toegestaan met behulp van de instructie **frame-ancestor**. Zie voor meer informatie [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md).

> [!NOTE]
> De iframe-module is beschikbaar in de Dynamics 365 Commerce versie 10.0.13.

De volgende afbeelding laat voorbeelden van iframe-modules zien waarin externe video's op sitepagina's worden weergegeven.

![Voorbeeld van iframe-modules met externe video's](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Eigenschappen van iframe-module

| Naam van eigenschap.             | Waarde                 | Omschrijving |
|---------------------------|-----------------------|-------------|
| Kop | Tekst | De koptekst voor de module. |
| Doel-URL | URL | De URL die wordt gehost in de module. |
| Hoogte | Getal of percentage | De hoogte van de module, in pixels of als een percentage. De waarde **100** wordt bijvoorbeeld behandeld als een aantal pixels en de waarde **100%** wordt beschouwd als een percentage. |
| Aria-label | Tekst | Een toegankelijk ARIA-label (Accessible Rich internet Applications) kan worden gedefinieerd voor toegankelijkheidsdoeleinden. |

## <a name="add-an-iframe-module-to-a-page"></a>Een iframe-module toevoegen aan een pagina

Voer de volgende stappen uit om een iframe-module aan een pagina toe te voegen om een externe video weer te geven.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Marketingsjabloon** in en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** de sjabloon **Marketingsjabloon**. Voer onder **Paginanaam** **Marketingpagina** in en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster van de module de **Breedte** in op **Container vullen**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **iframe**-module en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster van de module de waarde van de **Doel-URL** in op een externe URL voor een video.
1. Stel zo nodig andere eigenschappen, zoals **koptekst** en **Hoogte** in.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar de marketingpagina op uw site. U ziet dat de video wordt weergegeven in de iframe-module.
 
## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md)

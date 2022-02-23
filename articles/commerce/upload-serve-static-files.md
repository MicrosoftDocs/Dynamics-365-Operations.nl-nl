---
title: Statische bestanden uploaden en verwerken
description: In dit onderwerp wordt beschreven hoe u een statisch bestand uploadt in Microsoft Dynamics 365 Commerce Site Builder en hoe u een aangepaste URL en bestandsnaam maakt die u kunt gebruiken om dat bestand aan te vragen.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594955"
---
# <a name="upload-and-serve-static-files"></a>Statische bestanden uploaden en verwerken

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u een statisch bestand uploadt in Microsoft Dynamics 365 Commerce Site Builder en hoe u een aangepaste URL en bestandsnaam maakt die u kunt gebruiken om dat bestand aan te vragen.

Voor sommige connectors van derden moet een bestand worden gehost en vanaf de e-commerce site worden aangeboden. Deze connectors verwachten dat het bestand wordt geretourneerd door verzoeken naar een specifiek callback URL-pad en bestandsnaam. Daarom wordt in dit onderwerp uitgelegd hoe u een statisch bestand kunt uploaden en bedienen met een door de gebruiker te definiëren URL en bestandsnaam op een Dynamics 365 Commerce e-commercesite.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Een site-URL maken die een statisch bestand retourneert

Voer de volgende stappen uit om een site-URL te maken die een statisch bestand retourneert in Commerce site builder.

1. Ga naar de Mediabibliotheek van uw site en upload het bestand dat moet worden geleverd door verzoeken naar de URL die u gaat definiëren. Als u het bestand al hebt geüpload, kunt u deze stap overslaan.
1. Ga naar **URL's** voor uw site.
1. Selecteer **Nieuw \> Nieuwe URL**.
1. Selecteer in het dialoogvenster **Nieuwe URL** de optie **Mediabibliotheekmaterialen**.
1. Voer in het veld **URL-pad** het URL-pad in. Neem de bestandsnaam op in het pad.
1. Selecteer **Volgende**. De Mediabibliotheek wordt geopend en toont alle mediamaterialen van het type **document** dat is geüpload.
1. Selecteer het bestand dat moet worden geleverd voor verzoeken naar de URL die u in stap 5 hebt gedefinieerd.
1. Selecteer **Opslaan**.

Op dit moment bevindt de URL die u hebt gemaakt zich in een conceptstatus. Het bestand waarnaar de URL verwijst, wordt niet geretourneerd totdat u de URL publiceert. Voordat u de URL publiceert, kunt u valideren of de juiste gegevens worden geretourneerd.

## <a name="validate-and-publish-a-url"></a>Een URL valideren en publiceren

Ga als volgt te werk om een URL te valideren voordat u deze publiceert.

1. Ga naar **URL's** voor uw site en selecteer de URL die u wilt bekijken.
2. Selecteer in het deelvenster Eigenschappen rechtsonder via de knop **Bewerken** de juiste URL-koppeling. Er wordt een nieuw browservenster geopend en er wordt een 404-fout weergegeven.
3. Voeg de **?preview=inprogress**-query reeks toe aan de URL (bijvoorbeeld `https://yoursite.com/callback.html?preview=inprogress`) en laad de pagina opnieuw. Het bestand dat u naar de Mediabibliotheek hebt geüpload, moet in het antwoord zijn geretourneerd.

Nadat u de URL hebt gevalideerd, kunt u deze publiceren.

1. Ga naar **URL's** voor uw site en selecteer de URL.
2. Selecteer **Publiceren** in de opdrachtbalk.

## <a name="update-the-file-that-a-url-points-to"></a>Het bestand bijwerken waarnaar een URL verwijst

Nadat een URL is gepubliceerd, kunt u deze bijwerken zodat deze naar een ander bestand verwijst. U kunt de URL ook bijwerken, zodat deze verwijst naar een ander type bron, zoals wordt beschreven in de volgende sectie. U kunt bijvoorbeeld de URL naar een interne pagina of een omleiding verwijzen.

Voer de volgende stappen uit om het bestand bij te werken waarnaar een URL verwijst:

1. Ga naar **URL's** voor uw site en selecteer de URL die u wilt bijwerken.
1. Selecteer **Bewerken** in het eigenschappenvenster aan de rechterkant.
1. Selecteer onder **URL-toewijzing** het vak **Stap 2** en selecteer vervolgens een nieuw document in de Mediabibliotheek.
1. Selecteer **Toepassing**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Het materiaaltype bijwerken waarnaar een URL verwijst

U kunt ook een URL bijwerken zodat deze naar een ander type materiaal (resource) verwijst, zoals een interne pagina of een omleiding.

Voer de volgende stappen uit om het materiaaltype bij te werken waarnaar een URL verwijst:

1. Ga naar **URL's** voor uw site en selecteer de URL die u wilt bijwerken.
1. Selecteer **Bewerken** in het eigenschappenvenster aan de rechterkant.
1. Selecteer onder **URL-toewijzing** onder **Stap 1** een ander materiaaltype.
1. Selecteer het vak **Stap 2** en selecteer vervolgens het nieuwe materiaal.
1. Selecteer **Toepassing**.

## <a name="change-the-url-path"></a>Het URL-pad wijzigen

Nadat een URL is gemaakt, kan het pad ervan niet worden gewijzigd. Als u het URL-pad moet wijzigen dat een bestand of een ander type bron bevat, moet u een nieuwe URL maken, deze toewijzen aan het bestaande bestand of een andere bron, en vervolgens de publicatie ongedaan maken en de oude URL verwijderen.

Als u het URL-pad wilt wijzigen, volgt u deze stappen.

1. Als u een nieuwe URL wilt maken en toewijzen aan het bestaande bestand of een andere bron, volgt u de instructies in de sectie [Een site-URL maken die een statisch bestand retourneert](#create-a-site-url-that-returns-a-static-file) eerder in dit onderwerp.
1. Selecteer de nieuwe URL en selecteer **Publiceren** in de opdrachtbalk. De nieuwe URL wordt gepubliceerd.
1. Als u de publicatie van de oude URL ongedaan wilt maken, selecteert u de URL en selecteert u vervolgens **Publicatie ongedaan maken** in de opdrachtbalk. U kunt nu de oude URL verwijderen als u wilt.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van digitaal activabeheer](dam-overview.md)

[Afbeeldingen uploaden](dam-upload-images.md)

[Video's uploaden](dam-upload-video.md)

[Andere bestanden uploaden dan afbeeldingen en video's](dam-upload-files.md)

[Afbeeldingen bijsnijden](dam-crop-images.md)

[Focuspunten van afbeelding aanpassen](dam-custom-focal-point.md)

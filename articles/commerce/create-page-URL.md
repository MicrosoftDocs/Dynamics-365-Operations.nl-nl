---
title: Een pagina-URL maken
description: In dit onderwerp worden de basisconcepten en procedures beschreven voor het maken van een pagina-URL op uw site.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 062a49df93e442dbe402ac9a78244c966958aaa2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965248"
---
# <a name="create-a-page-url"></a>Een pagina-URL maken


[!include [banner](includes/banner.md)]

In dit onderwerp worden de basisconcepten en procedures beschreven voor het maken van een pagina-URL op uw site.

## <a name="overview"></a>Overzicht

De volledige of absolute URL die naar een pagina op uw site verwijst, bestaat uit verschillende onderdelen. De URL `https://www.contoso.com/en-us/contactus` heeft bijvoorbeeld de volgende onderdelen:

- `https://www.contoso.com`: het HTTP-protocol en het domein van de site.
- `/en-us`: het taalpad van de site.
- `/contactus`: de relatieve URL voor de pagina **Contact opnemen**. Een relatieve URL wordt ook wel een *tijdelijke aanduiding* (slug) voor een URL genoemd.

U kunt het domein en het pad naar de optionele taal van de site instellen wanneer u de site instelt. U kunt meer domeinen en taalpaden aan uw site toevoegen via de online winkelpagina in de instellingen van de site.

De URL-slug voor een pagina bestaat als een zelfstandige entiteit in de ontwerpomgeving van de site. Een pagina-URL bestaat uit twee delen: een naam die de URL-slug vertegenwoordigt en een verwijzing naar een pagina op uw site of een externe site. Een pagina-URL kan ook worden geconfigureerd om te fungeren als een omleiding naar een andere pagina op uw site of een externe site.

## <a name="create-a-page-url"></a>Een pagina-URL maken

Er zijn twee manieren om pagina-URL's te maken:

- Automatisch, wanneer u een pagina maakt
- Handmatig, op de pagina **URL's**

### <a name="create-a-page-url-when-you-create-a-page"></a>Een pagina-URL maken wanneer u een pagina maakt

Als u een naam opgeeft in het veld **URL** wanneer u een nieuwe pagina maakt, wordt er automatisch een pagina-URL gemaakt die naar die pagina verwijst op de pagina **URL's**. Nadat u de URL hebt gepubliceerd en de pagina waarnaar deze verwijst, hebben sitegebruikers (uw klanten) toegang tot de pagina die aan de URL is gekoppeld.

> [!NOTE]
> Als u een URL publiceert zonder de pagina te publiceren waarnaar deze verwijst, ontvangen sitegebruikers een 404-fout wanneer ze proberen toegang te krijgen tot de pagina. Als u een pagina publiceert zonder de URL te publiceren die naar deze pagina verwijst, wordt de pagina niet geopend met behulp van een URL.

### <a name="manually-create-a-page-url"></a>Handmatig een pagina-URL maken

Wanneer u nieuwe pagina's maakt, hoeft u geen pagina-URL op te geven. Als u het URL-veld leeg laat, wordt de pagina in een niet-gekoppelde status gemaakt. In dit geval hebben klanten geen toegang tot de pagina, zelfs als deze is gepubliceerd. Als u de pagina toegankelijk wilt maken, moet u de URL handmatig maken en aan de pagina koppelen.

Voer de volgende stappen uit om handmatig de pagina-URL voor een pagina te maken.

1. Selecteer **Nieuw** op de pagina **URL's**.
1. Selecteer de sitepagina waaraan de URL moet worden gekoppeld.
1. Voer de URL-slug in en selecteer vervolgens **OK**.

Op dit moment bevindt de URL zich in een conceptstatus. De URL moet worden gepubliceerd voordat de sitegebruikers toegang kunnen krijgen tot de bijbehorende pagina.

## <a name="update-a-page-url"></a>Een pagina-URL bijwerken

Voer de volgende stappen uit om de doelpagina van een pagina-URL bij te werken.

1. Selecteer op de pagina **URL's** de URL die u wilt bijwerken.
1. Selecteer in het eigenschappenvenster aan de rechterkant de knop met het weglatingsteken (**...**) naast het veld van de doelpagina.
1. Selecteer in het dialoogvenster een andere pagina en selecteer vervolgens **OK**.
1. Sla de URL op en publiceer deze.

## <a name="redirect-a-page-url"></a>Omleiding instellen voor een pagina-URL

Soms wilt u dat uw klanten een andere pagina zien wanneer ze een specifieke URL opvragen. In deze gevallen is de beste en eenvoudigste methode vaak de pagina te wijzigen waarnaar de URL van de pagina verwijst. U kunt echter goede redenen hebben voor het gebruik van HTTP 301- of 3023-omleidingen om aanvragen voor een URL om te leiden naar een andere URL.

Voer de volgende stappen uit om een URL om te leiden naar een andere URL.

1. Selecteer op de pagina **URL's** de URL die u wilt bijwerken.
1. Selecteer in het eigenschappenvenster aan de rechterkant de optie **Omleiden**.
1. Selecteer een bestemming voor de omleiding:

    - Als u naar een andere pagina op uw site wilt verwijzen, selecteert u **Interne URL**, de knop met het weglatingsteken (**...**) en vervolgens de URL waarnaar u wilt omleiden.
    - Als u naar een pagina op een externe site wilt verwijzen, selecteert u **Externe URL** en voert u vervolgens de volledige URL voor die pagina in. Zorg ervoor dat u het protocol opneemt. Voer bijvoorbeeld `https://domain.com/new/page` in. Als de URL al omleidt naar een interne URL, moet u **Selectie wissen** selecteren voordat u een externe URL kunt invoeren.

1. Selecteer een omleidingstype:

    - **Permanente omleiding (301)**: selecteer deze optie wanneer u weet dat de inhoud permanent wordt verplaatst en de vorige URL niet wordt hersteld. In zoekmachines wordt de SEO-waarde (Search Engine Optimization) van de omgeleide URL toegewezen aan de URL waarnaar wordt omgeleid. Ook wordt de record bijgewerkt om de nieuwe URL weer te geven. 
    - **Tijdelijke omleiding (302)**: selecteer deze optie om verkeer om te leiden zonder de zoekmachines bij te werken. Deze benadering wordt meestal gebruikt als de inhoud binnenkort teruggaat naar de vorige URL.

1. Wanneer u klaar bent om de omleiding uit te voeren, moet u de URL opslaan en publiceren.

## <a name="additional-resources"></a>Aanvullende resources

[Sitenavigatie aanpassen](customize-site-navigation.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)

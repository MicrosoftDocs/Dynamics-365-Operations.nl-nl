---
title: Productdimensiewaarden configureren die moeten worden weergegeven als stalen
description: In dit onderwerp wordt beschreven hoe u productdimensiewaarden als stalen kunt configureren in Microsoft Dynamics 365 Commerce Headquarters.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 08564ce7af7412f2501b917b3496942004402611
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117216"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Productdimensiewaarden configureren die moeten worden weergegeven als stalen

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u productdimensiewaarden als stalen kunt configureren in Microsoft Dynamics 365 Commerce Headquarters. Zie [Productdimensies](../../supply-chain/pim/product-dimensions.md) voor meer informatie over productdimensies.

Dynamics 365 Commerce ondersteunt het gebruik van grootte-, stijl- en kleurdimensie om productvarianten voor te stellen. Productdimensies hebben beschrijvende namen die worden weergegeven op productdetailpagina's (PDP´s), zodat productvarianten kunnen worden geselecteerd. Voorbeelden van deze beschrijvende namen zijn "Klein", "Normaal" en "Groot" voor grootte en "Zwart" en "Bruin" voor kleuren. Als een product echter veel variaties ondersteunt, zijn er meerdere selecties vereist om de afbeelding voor elke productvariant weer te geven. Het kan daarom langzaam verlopen en lastig zijn voor klanten om te bladeren door productvarianten en deze te selecteren.

Wanneer dimensies worden weergegeven als stalen in PDP´s, krijgen klanten een visueel voorbeeld van de variaties van een product. Klanten kunnen eenvoudig door een grote verscheidenheid van kleuren en patronen bladeren en snel verschillende combinaties van productvariaties weergeven.

Met de functie Dimensies als stalen weergeven kunnen in Commerce hexadecimale (hex) codes en afbeeldingen worden gebruikt om dimensies als stalen weer te geven. Bovendien kunnen vergelijkbare dimensies, zoals kleuren, worden gegroepeerd op productlijstpagina's. Een klant zoekt bijvoorbeeld naar producten die blauw zijn. Als de verschillende blauwe dimensiewaarden zijn gegroepeerd, worden op de lijstpagina met zoekresultaten producten weergegeven met verschillende tinten blauw. Met dimensiegroepering wordt de productverfijningservaring aanzienlijk verbeterd en kunnen klanten meer producten vinden via één zoekquery voor producten.

> [!NOTE]
> De functie Dimensies als stalen weergeven is beschikbaar vanaf versie 10.0.20 van Dynamics 365 Commerce.

De onderstaande afbeelding toont een voorbeeld waarin kleuren als stalen worden weergegeven in een Commerce PDP.

![Voorbeeld van kleuren die als stalen op een productdetailpagina worden weergegeven](../dev-itpro/media/swatch_pdp.png)

De onderstaande afbeelding toont een voorbeeld waarin kleuren als stalen worden weergegeven op een lijstpagina met zoekresultaten in Commerce.

![Voorbeeld van kleuren die als stalen op een lijstpagina met zoekresultaten worden weergegeven](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>De functie Dimensies als stalen weergeven in Commerce Headquarters

Als u de functie Dimensies als stalen weergeven wilt inschakelen in Commerce Headquarters, gaat u naar **Werkgebieden \> Functiebeheer** en schakelt u de functie **Afbeeldingsondersteuning voor productdimensiewaarden inschakelen** in. Wanneer deze functievlag is ingeschakeld, worden er drie nieuwe velden toegevoegd voor elke dimensie in de betreffende tabellen in Commerce Headquarters: **Hexcode**, **URL** (voor afbeeldingen) en **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Dimensiewaarden configureren in Commerce Headquarters

De functie Dimensies als stalen weergeven wordt ondersteund voor grootte-, stijl- en kleurdimensies. Waarden voor hexcodes en afbeeldings-URL´s voor de betreffende dimensies kunnen in Commerce Headquarters worden opgegeven. Als er geen waarden voor hexcodes en afbeeldings-URL´s worden opgegeven voor een dimensie, wordt de tekst weergegeven van de beschrijvende naam van de dimensie.

De configuratie kan op een van de volgende niveaus worden uitgevoerd:

- **Dimensie**: open in Commerce Headquarters de pagina voor een dimensie door te zoeken naar **Kleur**, **Grootte** of **Stijl**. Op elke pagina staat een raster met de dimensiewaarden. U kunt de waarden voor de weergavevolgorde, hexcodes en afbeeldings-URL´s beheren. In de volgende afbeelding ziet u een voorbeeldconfiguratie van de pagina **Kleuren**.

    ![Voorbeeld van dimensieconfiguratie op de pagina Kleuren](../dev-itpro/media/swatch_Color.PNG)

- **Dimensiegroep**: in Dynamics 365 Commerce kunt u de eigenschap **RefinerGroup** gebruiken om dimensiegroepen te maken. Als er dimensiegroepen zijn gedefinieerd, opent u de betreffende pagina door te zoeken naar **Kleurgroep**, **Formaatgroep** of **Stijlgroep**. Op elke pagina kunt u waarden voor hexcodes, afbeeldings-URL's en verfijningsgroepen beheren. In de volgende afbeelding ziet u een voorbeeldconfiguratie van de pagina **Kleurgroepen**.

    ![Voorbeeld van dimensieconfiguratie op de pagina Kleurgroepen](../dev-itpro/media/swatch_colorGroup.PNG)

- **Productdimensie (tijdens het maken van producten)**: wanneer u een nieuw product maakt, kunt u de pagina **Productdimensies** gebruiken om de dimensiewaarden in te voeren. Voor bestaande producten zijn mogelijk al de velden **Hexcode**, **URL (voor afbeeldingen)** en **RefinerGroup** ingesteld. U kunt de waarden echter zo nodig wijzigen. In de volgende afbeelding ziet u een voorbeeldconfiguratie op de pagina **Productdimensies**.

    ![Voorbeeld van dimensieconfiguratie op de pagina Productdimensies](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Bij het beheren van configuraties van hexcodes en afbeeldings-URL´s wordt hetzelfde patroon gevolgd als dat wordt gebruikt om de weergavevolgorde van dimensies te beheren.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Dimensiewaarden configureren met behulp van hexcodes

Voor de meeste kleurdimensies moet een kleurwaarde voor hexcodes worden opgegeven op dimensiepagina's in Commerce Headquarters. De kleur zwart moet bijvoorbeeld een hexcodewaarde hebben van **#00000**. Wanneer in Commerce een sitepagina wordt weergegeven, wordt de hexcode voorgesteld door een gekleurde staal.

De onderstaande afbeelding toont een voorbeeld waarin kleurdimensies met behulp van hexcodewaarden worden geconfigureerd.

![Voorbeeld van dimensieconfiguratie waarin hexcodes worden gebruikt](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Dimensiewaarden configureren met behulp van afbeeldings-URL´s

Sommige kleurdimensies vertegenwoordigen patronen, geen effen kleuren. Een kleurdimensie kan bijvoorbeeld worden omschreven als 'luipaard'. In deze gevallen kunt u de kleurdimensies effectiever voorstellen met behulp van gepubliceerde afbeeldingen in plaats van hexcodes voor stalen.

U moet elke afbeelding naar Commerce Site Builder uploaden en publiceren. Voer vervolgens de afbeeldings-URL in voor de gepubliceerde afbeelding op de betreffende dimensiepagina's in Commerce Headquarters. Als een dimensie is geselecteerd voor weergave als een staal, maar er geen hexcode is gedefinieerd, wordt er in Commerce een afbeelding opgezocht wanneer de pagina wordt weergegeven. Als het zoeken naar afbeeldingen mislukt, wordt in Commerce de tekst van de beschrijvende naam van de dimensie weergegeven.

In de volgende afbeelding ziet u een voorbeeld waarin afbeeldings-URL´s worden gebruikt voor de configuratie op de pagina **Kleuren**.

![Voorbeeld van dimensieconfiguratie waarin afbeeldings-URL´s worden gebruikt](../dev-itpro/media/swatch_color_urls.PNG)

U kunt een mediasjabloon gebruiken voor het definiëren van afbeeldings-URL's, net als bij product- en categorieafbeeldingen. Wanneer u afbeeldingen uploadt naar Site Builder, moeten bestandsnaamconventies en bestandspaden consistent zijn.

In de volgende afbeelding ziet u een voorbeeld waarin afbeeldings-URL´s worden gebruikt voor de configuratie van een mediasjabloon.

![Voorbeeld van de configuratie van een mediasjabloon](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Dimensiewaarden configureren met behulp van hexcodes en afbeeldings-URL´s

Voor de meeste kleurdimensies kunt u zowel hexcodes als afbeeldings-URL's configureren. Voor terugvallogica voor rendering in Commerce wordt automatisch gezocht naar een hexcode of een afbeeldings-URL om een kleurenstaal weer te geven. Met behulp van zowel hexcodes als afbeeldings-URL's om kleurdimensies te configureren, kunt u afbeeldingsbeheer vereenvoudigen wanneer het aantal kleuren groot is.

In de volgende afbeelding ziet u een voorbeeld waarin zowel hexcodes als afbeeldings-URL´s worden gebruikt voor de configuratie op de pagina **Kleuren**.

![Voorbeeld van dimensieconfiguratie waarin zowel hexcodes als afbeeldings-URL´s worden gebruikt](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Verfijningsgroepen configureren

Wanneer u een hexcode of afbeeldings-URL voor een dimensiewaarde definieert, kunt u ook een waarde opgeven voor het veld **RefinerGroup**. Met dit veld wordt de dimensie gedefinieerd die moet worden gebruikt om vergelijkbare dimensiewaarden in de verfijningservaring te groeperen.

Als de waarden van uw kleurdimensie bijvoorbeeld 'blauw', 'lichtblauw', 'grijsblauw' en 'donkerblauw' zijn, wordt elke waarde aan een andere hexcode of afbeeldings-URL toegevoegd. Daarom wordt elke waarde als een andere kleur weergegeven op PDP´s en productkaarten voor de betreffende producten. Als u al deze kleurdimensiewaarden echter toewijst aan een **RefinerGroup**-waarde van **Blauw**, wordt met een zoekopdracht naar "blauwe" producten een lijstpagina met zoekresultaten gegenereerd voor producten met dimensiekleurwaarden van "blauw", "lichtblauw", "grijsblauw" en "donkerblauw".

Het voorbeeld in de volgende afbeelding toont de relatie tussen de eigenschappen **Kleur** en **RefinerGroup** in Commerce Headquarters.

![Voorbeeld van beheer van verfijningsgroepen](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Afbeeldingen in Commerce Site Builder beheren

Als afbeelding-URL's voor dimensiewaarden worden gebruikt, moeten de bijbehorende afbeeldingen naar Commerce Site Builder worden geüpload. De locatie van elke afbeelding moet overeenkomen met de bestandsnaam en het mappad die voor de afbeelding zijn gedefinieerd in Commerce Headquarters. Afbeeldingsbestanden moeten naar de betreffende categorielocaties in Site Builder worden geüpload. Kleurafbeeldingen moeten bijvoorbeeld worden geüpload naar de categoriemap **Kleur**. Zie [Afbeeldingen uploaden](../dam-upload-images.md) voor meer informatie over het uploaden van afbeeldingen naar Site Builder.

In de volgende afbeelding ziet u een voorbeeld van de plaats waar het dialoogvenster **Bestanden uploaden** wordt gebruikt om afbeeldingen naar de mediabibliotheek van Site Builder te uploaden. De categorieën **Grootte**, **Kleur** en **Stijl** worden gemarkeerd die beschikbaar zijn voor selectie.

![Voorbeeld van afbeeldingsbestandscategorieën tijdens het uploaden naar de mediabibliotheek van Site Builder](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Staalweergave op e-commercesitepagina's inschakelen

Voordat stalen op e-commercesitepagina's kunnen worden weergegeven die dimensieselectie vereisen, zoals PDF's en lijstpagina's, moet u dimensiesite-instellingen configureren in Commerce Headquarters. Zie [Site-instellingen voor dimensies toepassen](../dimension-settings.md) voor meer informatie.

Bovendien moet u de eigenschap **Productkenmerken opnemen in zoekresultaten** inschakelen voor modules van zoekresultaten. Als op uw site aangepaste categoriepagina's worden gebruikt, moet u de modules van de zoekresultaten die op die pagina's worden gebruikt, bijwerken zodat de eigenschap **Productkenmerken opnemen in zoekresultaten** wordt ingeschakeld. Zie [Module voor zoekresultaten](../search-result-module.md) voor meer informatie.

## <a name="display-swatches-in-pos-and-other-channels"></a>Stalen weergeven in POS en andere kanalen

Commerce heeft op dit moment geen standaardimplementatie waarin de weergave van stalen wordt ondersteund in POS (Point of Sale) en andere kanalen. U kunt de functionaliteit voor weergave van stalen echter implementeren als extensie die ervoor zorgt dat kanaal-API's de hexcodes en afbeelding-URL's retourneren die nodig zijn voor het weergeven van stalen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Module voor zoekresultaten](../search-result-module.md)

[Site-instellingen voor dimensies toepassen](../dimension-settings.md)

[Productdimensies](../../supply-chain/pim/product-dimensions.md)

[Afbeelding uploaden](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

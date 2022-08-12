---
title: Dynamische e-commercepagina's maken op basis van URL-parameters
description: In dit artikel wordt beschreven hoe u een Microsoft Dynamics 365 Commerce-e-commercepagina kunt instellen die dynamische inhoud kan aanbieden op basis van URL-parameters.
author: StuHarg
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 83e20d9fc655a474a11521ec61d0b64d30603181
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169125"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Dynamische e-commercepagina's maken op basis van URL-parameters

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een Microsoft Dynamics 365 Commerce-e-commercepagina kunt instellen die dynamische inhoud kan aanbieden op basis van URL-parameters.

Een e-commercepagina kan worden geconfigureerd voor verschillende soorten inhoud, gebaseerd op een segment in het URL-pad. Daarom staat de pagina bekend als een dynamische pagina. Het segment wordt gebruikt als parameter om de pagina-inhoud op te halen. Een pagina gemaakt in Site Builder met de naam **blog\_viewer** wordt bijvoorbeeld toegewezen aan de URL `https://fabrikam.com/blog`. Deze pagina kan vervolgens worden gebruikt om andere inhoud weer te geven, gebaseerd op het laatste segment in het URL-pad. Het laatste segment in de URL `https://fabrikam.com/blog/article-1` is bijvoorbeeld **artikel-1**.

U kunt een parameter-URL-segment ook overschrijven met een Site Builder-pagina. Een pagina gemaakt in Site Builder met de naam **blog\_summary** kan bijvoorbeeld worden toegewezen aan de URL `https://fabrikam.com/blog/about-this-blog`. Wanneer de URL `https://fabrikam.com/blog` wordt aangevraagd met het segment `/about-this-blog` aan het einde, wordt de inhoud van de pagina **blog\_summary** geretourneerd in plaats van dat het segment `/about-this-blog` wordt geïnterpreteerd als parameter die door de pagina `https://fabrikam.com/blog` moet worden gebruikt. 

Wanneer u de namen selecteert voor de parameters die moeten worden doorgegeven aan de dynamische pagina, kan de naam van de dynamische pagina zoals deze in de URL (`/blog` in het bovenstaande voorbeeld) wordt weergegeven, niet worden gebruikt als parameternaam of als subtekenreeks van een parameternaam. 

> [!NOTE]
> De functionaliteit voor het hosten, ophalen en weergeven van dynamische pagina-inhoud is geïmplementeerd met een aangepaste module. Zie [Uitbreidbaarheid van online kanalen](e-commerce-extensibility/overview.md) voor meer informatie.

## <a name="set-up-a-dynamic-e-commerce-page"></a>Een dynamische e-commercepagina instellen

Als u een dynamische e-commercepagina wilt instellen, moet u de dynamische pagina maken, de basis-URL maken en de route naar de dynamische pagina configureren.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>De pagina maken die dynamische inhoud zal aanbieden

Volg de stappen in [Een nieuwe sitepagina toevoegen](add-new-page.md) om een pagina te maken voor dynamische inhoud. Voor de pagina die u maakt, moet een module worden uitgevoerd die gebruikmaakt van het laatste segment in het URL-pad om inhoud op te halen uit een externe gegevensbron. Zie [Uitbreidbaarheid van online kanalen](e-commerce-extensibility/overview.md) voor meer informatie over aangepaste moduleontwikkeling.

### <a name="create-the-base-url-for-the-dynamic-page"></a>De basis-URL voor de dynamische pagina maken

Volg deze stappen om de basis-URL voor de dynamische pagina in Commerce Site Builder te maken.

1. Ga naar **URL's** en selecteer **Nieuw \> Nieuwe URL**.
1. Selecteer in het dialoogvenster **Nieuwe URL maken** de optie **Interne pagina**. Voer onder **URL-pad** het pad in dat zal fungeren als basis voor de dynamische pagina (in dit voorbeeld **/blog**). Selecteer **Volgende**.
1. Selecteer in het dialoogvenster **Een pagina selecteren** de pagina die u als de dynamische pagina hebt gemaakt, en selecteer **Opslaan**.
1. Selecteer **Publiceren**.

### <a name="configure-the-route-to-the-dynamic-page"></a>De route naar de dynamische pagina configureren

Volg deze stappen om de route naar de dynamische pagina in Commerce Site Builder te maken.

1. Ga naar **Site-instellingen \> Extensies**.
1. Selecteer onder **Parameter-URL-paden** de optie **Toevoegen** en voer het URL-pad in dat u hebt ingevoerd toen u de URL hebt gemaakt (in dit voorbeeld **/blog**).
1. Selecteer **Opslaan en publiceren**.

Nadat de route is geconfigureerd, retourneren alle aanvragen naar het pad met de parameter-URL de pagina die aan die URL is gekoppeld. Als er aanvragen zijn die een extra segment bevatten, wordt de bijbehorende pagina geretourneerd en wordt de pagina-inhoud opgehaald door het segment als parameter te gebruiken. `https://fabrikam.com/blog/article-1` retourneert bijvoorbeeld de pagina `https://fabrikam.com/blog`, waarbij de inhoud wordt weergegeven die is opgehaald met de parameter **/article-1**.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Een parameter-URL met een aangepaste pagina overschrijven

Volg deze stappen om een parameter-URL met een aangepaste pagina in Commerce Site Builder te overschrijven.

1. Ga naar **URL's** en selecteer **Nieuw \> Nieuwe URL**.
1. Selecteer in het dialoogvenster **Nieuwe URL maken** de optie **Interne pagina**. Voer onder **URL-pad** het pad in dat het segment bevat dat u wilt overschrijven (in dit voorbeeld **/blog/over-dit-blog**). Selecteer **Volgende**.
1. Selecteer in het dialoogvenster **Een pagina selecteren** de aangepaste pagina en selecteer **Opslaan**.
1. Selecteer **Publiceren**.
1. Als de aangepaste pagina nog niet is gepubliceerd, gaat u naar **Pagina's**, selecteert u de aangepaste pagina en selecteert u **Publiceren**.

Nadat de aangepaste pagina is gepubliceerd, wordt deze gebruikt in plaats van de dynamische pagina met parameterinhoud.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een productpagina verrijken](enrich-product-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)

[Uitbreidbaarheid van online afzetkanaal](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

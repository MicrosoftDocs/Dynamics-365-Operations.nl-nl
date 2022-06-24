---
title: Commerce-catalogi voor B2B-sites maken
description: In dit artikel wordt beschreven hoe u Commerce-catalogi maakt voor B2B-sites (business-to-business) in Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d87b6c64a6038c4518eeec178f9e139ef6f5ae2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848984"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Commerce-catalogi voor B2B-sites maken

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit artikel wordt beschreven hoe u Commerce-productcatalogi maakt voor B2B-sites (business-to-business) in Microsoft Dynamics 365 Commerce. Zie [Veelgestelde vragen over Commercecatalogi voor B2B-sites](catalogs-b2b-sites-FAQ.md) voor antwoorden op veelgestelde vragen over commercecatalogi voor B2B-sites.

> [!NOTE]
> Dit artikel is van toepassing op Dynamics 365 Commerce versie 10.0.27 en hoger.

U kunt detailhandel Commercecatalogi gebruiken voor de identificatie van de producten die u in uw online B2B-winkels wilt aanbieden. Wanneer u een catalogus maakt, identificeert u de online winkels waarin de producten worden aangeboden, voegt u de producten toe die u wilt opnemen en verbetert u het productaanbod door productdetails toe te voegen. U kunt meerdere catalogi maken voor elke online B2B-winkel.

Met commerceproductcatalogi kunt u de volgende gegevens definiëren:

- **Catalogusspecifieke navigatiehiërarchie**: organisaties kunnen een verschillende categoriestructuur maken voor hun specifieke catalogus.
- **Catalogusspecifieke metagegevens voor kenmerken**: kenmerken bevatten details over een product. Door kenmerken toe te wijzen aan een categorie van de navigatiehiërarchie kunt u waarden definiëren voor die kenmerken op het niveau van producten die aan die categorie zijn toegewezen. Organisaties kunnen vervolgens deze taken uitvoeren:

    - Catalogusspecifieke kenmerkwaarden definiëren.
    - De zichtbaarheid van kenmerken op catalogusniveau controleren.
    - De verfijningen selecteren die specifiek zijn voor een afzonderlijke catalogus.

- **Afzetkanalen**: organisaties kunnen meer dan één online B2B-kanaal aan een catalogus koppelen. Volledige ondersteuning voor catalogi is momenteel alleen beschikbaar voor online B2B-winkels.
- **Klanthiërarchieën**: voor een bepaald B2B-kanaal kunnen organisaties een specifieke catalogus beschikbaar maken voor geselecteerde B2B-partners door klanthiërarchieën aan die catalogus te koppelen.
- **Prijsgroepen**: u kunt prijzen en promoties configureren die specifiek zijn voor een bepaalde catalogus. Deze mogelijkheid is de kernreden voor het definiëren van een catalogus voor een B2B-kanaal. Met prijsgroepen voor catalogi kunnen organisaties producten beschikbaar maken voor de gewenste B2B-organisaties en hun voorkeursprijzen en -kortingen toepassen. B2B-klanten die bestellen uit een geconfigureerde catalogus, kunnen profiteren van speciale prijzen en promoties nadat ze zich hebben aangemeld op een Commerce B2B-site. Als u specifieke catalogusprijzen wilt configureren, selecteert u **Prijsgroepen** op het tabblad **Catalogi** om een of meer prijsgroepen te koppelen aan de catalogus. Alle handelsovereenkomsten, prijscorrectiejournalen en geavanceerde kortingen die zijn gekoppeld aan dezelfde prijsgroep worden toegepast wanneer klanten uit die catalogus bestellen. (Geavanceerde kortingen zijn drempel-, hoeveelheids- en combinatiekortingen.) Zie [Prijsgroepen](price-management.md#price-groups) voor meer informatie over prijsgroepen.

> [!NOTE]
> Deze functie is beschikbaar vanaf Dynamics 365 Commerce versie 10.0.27. Als u catalogusspecifieke configuraties zoals de navigatiehiërarchie en klanthiërarchie wilt configureren, opent u in Commerce Headquarters de werkruimte **Functiebeheer** (**Systeembeheer \> Werkruimtes \> Functiebeheer**), schakelt u de functie **Gebruik van meerdere catalogi in detailhandelkanalen inschakelen** in en voert u de taak **1110 CDX** uit.

## <a name="catalog-process-flow"></a>Processtroom catalogus

Het proces van het maken en verwerken van een catalogus heeft vier algemene stappen. Elke stap wordt uitgebreid beschreven in de volgende sectie.

1. **[Configuratie](#configure-the-catalog)**

    - Koppel de navigatiehiërarchie.
    - Geef de ingangs- en vervaldatums op, indien van toepassing.
    - Voeg producten en categorieën toe.
    - Koppel prijsgroepen.
    - Koppel een klanthiërarchie die specifiek is voor uw B2B-organisaties. 
    - Koppel de kenmerkgroep met standaarddimensies voor verfijnen, zoals grootte, stijl en kleur.
    - Stel metagegevens van kenmerken in.

1. **[Validatie](#validate-the-catalog)**: in deze stap worden validatieregels uitgevoerd die specifiek gedrag afdwingen. Hieronder volgen een aantal voorbeelden:

    - Zorg ervoor dat er geen niet-gecategoriseerde producten zijn.
    - Zorg ervoor dat alle artikelen die voor elk kanaal zijn ingedeeld, aan een catalogus zijn gekoppeld.

1. **[Goedkeuring](#approve-the-catalog)**
1. **[Publiceren](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>De catalogus instellen

Met de informatie in deze sectie kunt u uw catalogus instellen.

### <a name="configure-the-catalog"></a>De catalogus configureren

Ga in Commerce Headquarters naar **Retail en Commerce \> Catalogi en assortimenten \> Alle catalogi** om uw catalogus te configureren.

Wanneer u een nieuwe catalogus maakt, moet u deze eerst koppelen aan een of meer kanalen. Alleen artikelen die zijn gekoppeld aan uw geselecteerde kanaal [assortimenten](/dynamics365/unified-operations/retail/assortments) kunnen worden gebruikt bij het maken van de catalogus. Als u de catalogus wilt koppelen aan een of meer kanalen, selecteert u **Toevoegen** op het sneltabblad **Commerce-kanalen** van de pagina **Catalogusinstellingen**.

#### <a name="associate-the-navigation-hierarchy"></a>De navigatiehiërarchie koppelen

Om producten toe te voegen aan een catalogus moet u een navigatiehiërarchie selecteren. De navigatiehiërarchie ondersteunt de categoriestructuur van de catalogus. U moet kiezen uit een van de navigatiehiërarchieën die zijn gekoppeld aan de kanalen die zijn geselecteerd op het sneltabblad **Commerce-kanalen** van de pagina **Catalogusinstellingen**. Als u een standaardnavigatiehiërarchie wilt koppelen aan elk van uw kanalen, gaat u naar **Retail en Commerce \> Afzetkanaalinstellingen \> Afzetkanaalcategorieën en productkenmerken**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Ingangsdatum en vervaldatum opgeven

Als u een ingangsdatum en vervaldatum wilt opgeven voor een catalogus, selecteert u het bovenste knooppunt van de catalogushiërarchie om terug te gaan naar de koptekstweergave van de hoofdcatalogus. Configureer vervolgens op het sneltabblad **Algemeen** de vereiste ingangsdatums en vervaldatums.

#### <a name="add-and-categorize-products"></a>Producten en categorieën toevoegen

Ga in Commerce Headquarters naar **Retail en Commerce \> Catalogi en assortimenten \> Alle catalogi** om producten voor uw catalogus te configureren. Selecteer vervolgens **Producten toevoegen** op het tabblad **Catalogi**.

U kunt ook een knooppunt in de navigatiehiërarchie selecteren. Vervolgens kunt u producten rechtstreeks toevoegen aan een categorie in de catalogus.

#### <a name="associate-price-groups"></a>Prijsgroepen koppelen

Als u catalogusspecifieke prijzen wilt configureren, moet u een of meer prijsgroepen aan de catalogus koppelen. Ga in Commerce Headquarters naar **Retail en Commerce \> Catalogi en assortimenten \> Alle catalogi** om prijsgroepen aan een catalogus te koppelen. Selecteer vervolgens **Prijsgroepen** op het tabblad **Catalogi** onder **Prijzen**. Alle handelsovereenkomsten, prijscorrectiejournalen en geavanceerde kortingen (drempel, hoeveelheid, combinatie) die zijn gekoppeld aan dezelfde prijsgroep worden toegepast wanneer klanten uit de catalogus bestellen.

Zie [Prijsgroepen](price-management.md#price-groups) voor meer informatie over prijsgroepen.

> [!NOTE]
> U kunt geen nieuwe prijsgroep maken vanuit de pagina **Alle catalogi**. In plaats daarvan moet u deze maken via de pagina **Alle prijsgroepen**. U moet deze vervolgens koppelen aan de catalogus op de pagina **Alle catalogi**.

#### <a name="associate-a-customer-hierarchy"></a>Een klanthiërarchie koppelen

Ga in Commerce Headquarters naar **Retail en Commerce \> Catalogi en assortimenten \> Alle catalogi** om klanthiërarchieën te koppelen. Selecteer vervolgens onder **Klanthiërarchie** op het tabblad **Catalogi** **Hiërarchieën toewijzen** om een of meer klanthiërarchieën aan de catalogus te koppelen.

> [!NOTE]
> U kunt geen nieuwe klanthiërarchie maken vanuit de pagina **Alle catalogi**. In plaats daarvan moet u deze maken via de pagina **Klanthiërarchieën**. U moet deze vervolgens koppelen aan de catalogus op de pagina **Alle catalogi**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Koppel de kenmerkgroep met standaarddimensies voor verfijnen, zoals grootte, stijl en kleur

Als u een kenmerkgroep met standaarddimensies voor verfijnen wilt koppelen, zoals grootte, stijl en kleur, gaat u in Commerce Headquarters naar **Retail en Commerce \> Catalogi en assortimenten \> Alle catalogi**. Selecteer vervolgens **Kenmerkgroepen** op het tabblad **Catalogi** onder **Kenmerken**.

#### <a name="set-attribute-metadata"></a>Metagegevens van kenmerken instellen

Ga in Commerce Headquarters naar **Retail en Commerce \> Catalogi en assortimenten \> Alle catalogi** om uw kenmerkmetagegevens te configureren. Selecteer vervolgens **Metagegevens van kenmerken instellen** op het tabblad **Catalogi** onder **Kenmerken**. Als u de kenmerken wilt selecteren die kunnen worden bekeken en opnieuw kunnen worden gedefinieerd, selecteert u een categorie in de bijbehorende catalogusspecifieke navigatiehiërarchie en selecteert u vervolgens een kenmerk onder **Catalogusproductkenmerken**. Selecteer vervolgens **Kenmerk in kanaal weergeven**. Standaard zijn alle weerbare kenmerken ook doorzoekbaar. Als u wilt dat kenmerken kunnen worden verfijnd, selecteert **Kan worden verfijnd**.

### <a name="validate-the-catalog"></a>De catalogus valideren

Voordat een nieuwe catalogus beschikbaar is voor gebruik, moet deze worden gevalideerd en gepubliceerd.

Volg deze stappen om een catalogus te valideren.

1. Selecteer op het tabblad **Catalogi** van de pagina **Alle catalogi** onder **Validatie** de optie **Catalogus valideren** om een validatie uit te voeren. Deze stap is vereist. Hiermee wordt gevalideerd dat de vereiste instelling klopt.
1. Selecteer **Resultaten weergeven** om de details van de validatie te zien. Als er fouten zijn gevonden, moet u de gegevens corrigeren en de validatie opnieuw uitvoeren totdat deze slaagt.

### <a name="approve-the-catalog"></a>De catalogus goedkeuren

Nadat een catalogus is gevalideerd, moet deze worden goedgekeurd.

Voer deze stappen uit om de goedkeuringswerkstroom voor de catalogus te starten.

1. Selecteer **Werkstroom \> Indienen** in het actievenster van de pagina **Alle catalogi**.
1. Ga naar **Retail en Commerce \> Headquarters instellen \> Commerce-werkstromen** om de stappen en gemachtigde gebruikers voor de werkstroom te configureren. De werkstroom definieert de stappen die vereist zijn om de catalogus de status **Goedgekeurd** te geven.

### <a name="publish-the-catalog"></a>De catalogus publiceren

Wanneer een catalogus de status **Goedgekeurd** heeft, kunt u deze publiceren door **Publiceren** te selecteren in het menu **Catalogi**. Nadat de catalogus de status **Gepubliceerd** heeft gekregen, kan deze worden gebruikt bij callcenterorderinvoer en catalogusverzendprocessen. U kunt een catalogus handmatig publiceren of via een batchproces. De ingangsdatum die u hebt gedefinieerd voor de catalogus bepaalt wanneer de producten beschikbaar zijn in de online winkel. De einddatum die u hebt gedefinieerd, bepaalt wanneer de producten worden verwijderd uit de online winkel.

> [!NOTE]
> U kunt een catalogus publiceren met producten met waarschuwingen. Deze producten worden echter niet weergegeven in de online winkel.

## <a name="additional-resources"></a>Aanvullende bronnen

[Impact van uitbreidbaarheid van Commerce-catalogi voor B2B-aanpassingen](catalogs-b2b-sites-dev.md)

[Veelgestelde vragen over Commercecatalogi voor B2B-sites](catalogs-b2b-sites-FAQ.md)

---
title: Productdimensies
description: 'Er zijn vijf productdimensies: kleur, stijl, configuratie, maat en versie. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.'
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 285e9d2d184a899f1ffa502d59a853ba83cda491
ms.sourcegitcommit: 2093c9dc31d1b60b3114085d9cef48fdbbb0ca0d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2021
ms.locfileid: "5118676"
---
# <a name="product-dimensions"></a>Productdimensies

[!include [banner](../includes/banner.md)]

Er zijn vijf productdimensies: kleur, stijl, configuratie, maat en versie. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.

Productdimensies zijn kenmerkend als ze dienen ter identificatie van de variant van een product. U kunt combinaties van productdimensies gebruiken om varianten van het product te definiëren. Als u een productvariant wilt maken, moet u ten minste één productdimensie definiëren voor een productmodel.

## <a name="product-variants"></a>Productvarianten

Productvarianten worden ook artikelen genoemd. Een artikel is een tastbaar product, dat niet hetzelfde is als een service. Het is echter ook mogelijk om een productmodel te definiëren van het servicetype. Met behulp van het servicetype kunt u productvarianten specificeren die services omvatten. U kunt bijvoorbeeld een productmodel opgeven voor advieswerk en productvarianten voor werk dat is uitgevoerd door senior en junior consultants.

## <a name="product-dimensions"></a>Productdimensies

Een productvarianten kan worden gegenereerd op basis van de waarden van de productdimensies.

Productdimensiewaarden voor de dimensies maat, kleur en stijl kunnen op de volgende locaties worden gemaakt:

- Pagina **Maat** (**Productgegevensbeheer \> Instellen \> Dimensie- en variantgroepen \> Maten**)
- Pagina **Kleur** (**Productgegevensbeheer \> Instellen \> Dimensie- en variantgroepen \> Kleuren**)
- Pagina **Stijl** (**Productgegevensbeheer \> Instellen \> Dimensie- en variantgroepen \> Stijlen**)

Waarden voor productdimensies voor de configuratiedimensie worden doorgaans gemaakt met de functie voor productconfiguratie of op dimensies gebaseerde configuratie. 

Productversies worden gewoonlijk gemaakt voor specifieke versies wanneer het product tijdens de levenscyclus wordt ontwikkeld. Productversies worden verderop in dit onderwerp gedetailleerd besproken.

Productdimensies kunnen tevens worden gemaakt en beheerd op de pagina **Productdimensies**, die kan worden geopend vanaf de volgende locaties:

- Ga naar **Productgegevensbeheer \> Producten \> Productmodellen**. Selecteer **Productdimensies** in het actievenster.
- Ga naar **Productgegevensbeheer \> Producten \> Alle producten en productmodellen**. Een productmodel selecteren. Selecteer **Productdimensies** in het actievenster.
- Ga naar **Productgegevensbeheer \> Vrijgegeven producten**. Een productmodel selecteren. Ga naar het actievenster en het tabblad **Product** in de groep **Productmodel**, en selecteer **Productkenmerken**.

Het aantal varianten dat u voor een artikel maakt, wordt beperkt door het aantal mogelijke productdimensiecombinaties.

> [!TIP]
> Wanneer u een product bijvoorbeeld op een orderregel gebruikt, selecteert u de productdimensies om de productvariant waarmee u wilt werken, te identificeren.

## <a name="example"></a>Voorbeeld

Een bedrijf verkoopt spijkerbroeken. Het artikel *Spijkerbroeken* gebruikt de productdimensies Kleur en Maat. De spijkerbroeken worden in drie verschillende kleuren en in zes verschillende maten verkocht. De kleuren zijn blauw, zwart en bruin. De maten zijn XS, S, M, L, XL en XXL. Niet alle maten zijn beschikbaar in alle drie kleuren. Als alle combinaties beschikbaar zijn, zouden er 18 typen spijkerbroeken zijn. In dit voorbeeld worden echter alleen de volgende negen combinaties van productvarianten geproduceerd.

| Kleur | Grootte |
|-------|------|
| Blauw  | XS   |
| Blauw  | Z    |
| Blauw  | M    |
| Zwart | M    |
| Zwart | L    |
| Zwart | XL   |
| Bruin | L    |
| Bruin | XL   |
| Bruin | XXL  |

## <a name="the-version-product-dimension"></a>De productdimensie versie

Versie is een productdimensie die u helpt bij het onderhouden en bijhouden van meerdere versies van een product in de toeleveringsketen. Het bijhouden van versies is essentieel voor het welslagen van fabrikanten die werken met een steeds kortere levenscyclus van producten, verhoogde vereisten voor kwaliteit en betrouwbaarheid en de nadruk op productveiligheid.

Als standaardproductdimensie is versie vergelijkbaar met de bestaande productdimensies (maat, stijl, kleur en configuratie). Daarom kunt u het naast het bijhouden van productversies ook voor andere doeleinden gebruiken.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>De dimensie versie inschakelen

#### <a name="before-you-turn-on-the-version-dimension"></a>Voordat u de dimensie versie inschakelt

Wanneer u de versiedimensie inschakelt, werkt een deel van de functionaliteit mogelijk niet of niet meer naar behoren als u andere oplossingen hebt geïnstalleerd die aanpassingen aan de voorraaddimensies toevoegen. Als u wilt dat de versie dimensie volledig functioneel is, moet u deze oplossingen mogelijk bijwerken zodat ze de versie dimensie in de verwijzingen naar de voorraaddimensies opnemen.

Wanneer u uw oplossingen test op compatibiliteit met de dimensie versie, zoekt u naar de volgende elementen:

1. **Functionaliteit:** de meeste belangrijke aanpassingen die betrekking hebben op de voorraaddimensies moeten worden beoordeeld om er zeker van te zijn dat ze in combinatie met de versiedimensie kunnen werken.
1. **Verwijzingen naar de voorraaddimensies:** zoek naar verwijzingen naar de voorraaddimensies (dat wil zeggen, plaatsen waar expliciet naar de dimensies wordt verwezen). Verwijzingen naar `InventDimId` zouden standaard moeten werken maar zoek naar verwijzingen naar stijl of kleur. Controleer bijvoorbeeld de volgende elementen:

    - API-aanroepen in uitgebreide klassen
    - Alle verwijzingen naar specifieke voorraaddimensies in uitbreidingscode (deze code moet de versiedimensie omvatten samen met de dimensies stijl, kleur en maat).

1. **Verwijzingen naar verouderde API-aanroepen:** in de introductie van de versiedimensie heeft Microsoft geprobeerd API's zoveel mogelijk in gebruik te laten. De paar API's die zijn verouderd, geven een waarschuwing wanneer u de configuratiesleutel **Productdimensie -versie** inschakelt. Oproepen naar deze API moeten in uw uitgebreide oplossingen worden opgelost voordat u de versiedimensie in een productiesysteem inschakelt. Dit zijn de versiespecifieke verouderde versies API's:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Toewijzingen:** als voor toewijzingen de voorraaddimensies worden gebruikt, moet de bijbehorende relatietoewijzing naar deze toewijzingen worden bijgewerkt zodat deze de versiedimensie bevatten. In het uitgebreide model of de tabelextensies zoekt u naar tabellen waarin de velden voorraaddimensies bevatten.
1. **Microsoft Dynamics 365 Commerce-functionaliteit:** nadat de versiedimensie is ingeschakeld, wordt deze overal in de Commerce-specifieke code weergegeven in Dynamics 365 Supply Chain Management. De versiedimensie wordt echter nog niet ondersteund door de Commerce-kanaaldatabase of in de POS- (Point of Sale) of e-Commerce-toepassingen. Deze Commerce-specifieke toepassingen ondersteunen geen gebruikers die voorraad per versiedimensie verkopen/verzenden of retourneren/ontvangen. Bij functies voor het zoeken naar voorraadbeschikbaarheid wordt voorraad niet vastgesteld op basis van versiedimensie in Commerce-apps. Dit gedrag lijkt op het huidige gedrag van de configuratiedimensie overal in Commerce.

#### <a name="turn-on-the-version-dimension"></a>De dimensie versie inschakelen

Voordat u de versiedimensie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Voor deze taak zijn beheerdersmachtigingen vereist.

1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
1. Schakel de functie in met de naam *Productdimensieversie*. (Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.)
1. Zet het systeem in de [Onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
1. Vouw op het tabblad **Configuratiesleutels** de optie **Handel** uit en schakel het selectievakje voor **Productdimensie - versie** in.
1. Schakel de [onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) uit.

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Gebieden waar de versiedimensie niet wordt ondersteund

De versiedimensie wordt niet ondersteund in de volgende gebieden (u kunt deze gebieden nog wel gebruiken, maar u kunt er geen versieproducten (producten waar de versiedimensie wordt gebruikt) aan toevoegen). U kunt bijvoorbeeld geen versieartikel toevoegen aan een leverancierscatalogus. De reden hiervoor is dat er tijdens het toevoegen van producten met de versiedimensie aan deze gebieden een aantal belangrijke wijzigingen kunnen worden aangebracht.

- Maandoverzicht kostenobject
- Overzichtcache van kostenobject
- MCR-verkoopstatistieken per artikel
- Leverancierscatalogi
- EcoResProductDimensionGroupEntity

Bovendien wordt de versiedimensie niet ondersteund door de functies voor het maken en verwerken van orders in Commerce (bijvoorbeeld voor POS-, Call Center- en e-commerce-orders). Er is geen tijdlijn bevestigd waarop Commerce-orders worden uitgebreid om dit te ondersteunen.

### <a name="functional-characteristics-of-the-version-dimension"></a>Functionele kenmerken van de versiedimensie

De versiedimensie werkt net als andere productdimensies. Vanwege de specifieke aard en omdat het de bedoeling is om meerdere versies van een product te onderhouden en bij te houden, gedraagt deze dimensie zich enigszins anders. Hier volgen enkele verschillen en overeenkomsten:

- **Er is geen versiegroep.**

    Hoewel het concept van groepen bestaat voor maat, kleur en stijl (kleurgroep, maatgroep en stijlgroep), bestaat het concept versiegroep niet. Met groepen kunt u de toepasselijke waarden vooraf definiëren, zodat het product bijvoorbeeld alle kleuren in die kleurgroep kan gebruiken wanneer u een kleurgroep toewijst aan een product. Dit concept is niet van toepassing op de versiedimensie, omdat de versies die een product heeft, niet vooraf zijn gedefinieerd wanneer het product wordt gemaakt. In plaats daarvan worden versies gemaakt tijdens de levenscyclus van het product, als dat nodig is. Als de vorm, de passing en de functie van het product echter hetzelfde blijven, maakt u een nieuwe versie in plaats van een nieuw product.

- **De suggesties van productvarianten werken zoals ze dat nu ook doen.**

    Met productvariantsuggesties worden voor alle waarden van de versiedimensie suggesties gedaan, net als voor andere dimensies. Het proces voor het maken en vrijgeven van producten met een versie is hetzelfde als voor producten met andere dimensies. Wanneer u een product met verschillende versies maakt, wordt de eerste versie (v1) gemaakt als productdimensie en worden de varianten vrijgegeven. Wanneer het product wordt gewijzigd en er een nieuwe versie nodig is, wordt de nieuwe versiewaarde (v2) toegevoegd en worden de vereiste varianten vrijgegeven. Er is niet te verwachten dat alle versies (v1, v2 en v3) vooraf worden gemaakt voor het product.

> [!IMPORTANT]
> Als u de versiedimensie inschakelt en gebruikt, werken sommige oplossingen die verwijzen naar de voorraaddimensies mogelijk niet meer naar behoren. Neem contact op met de ISV (Independent Software Vendor) voor de desbetreffende oplossingen om deze problemen te bevestigen en op te lossen. Zie [De versiedimensie inschakelen](#enable-version-dim) voor meer informatie.

---
title: Kenmerken en kenmerkgroepen beheren
description: In dit onderwerp wordt beschreven hoe u kenmerken kunt gebruiken om een product en de bijbehorende karakteristieken door middel van door gebruiker gedefinieerde velden te beschrijven.
author: ashishmsft
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: b3960f0877bdf68dd2f511ad283961b2a92db6a60078e84be55f071a00eae927
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727649"
---
# <a name="manage-attributes-and-attribute-groups"></a>Kenmerken en kenmerkgroepen beheren

[!include [banner](includes/banner.md)]

*Kenmerken* bieden een manier om een product en de bijbehorende kenmerken te beschrijven via door de gebruiker gedefinieerde velden (zoals **Geheugengrootte**, **Capaciteit van vaste schijf**, **Is EnergyStar**, enzovoort). Kenmerken kunnen aan verschillende Commerce-entiteiten, zoals productcategorieën en kanalen, worden gekoppeld, en de standaardwaarden kunnen daarvoor worden ingesteld. Producten nemen vervolgens de kenmerken en standaardwaarden over wanneer ze worden gekoppeld aan de productcategorieën of kanalen. De standaardwaarden kunnen worden overschreven op het afzonderlijke productniveau, op kanaalniveau of in een catalogus.


Een normaal televisieproduct kan bijvoorbeeld de volgende kenmerken hebben.

| Categorie   | Kenmerk                | Toegestane waarden          | Standaardwaarde |
|------------|--------------------------|-----------------------------|---------------|
| Tv en Video | Merk                    | Een geldige merkwaarde       | None          |
| Tv         | Schermgrootte              | 20–80 inch                | None          |
|            | Verticale resolutie      | 480i, 720p, 1080i, or 1080p | 1080p         |
|            | Schermvernieuwingsfrequentie      | 60hz, 120hz of 240hz       | 60hz          |
|            | HDMI-ingang              | 0–10                        | 3             |
|            | DVI-ingang               | 0–10                        | 1             |
|            | Composiet-ingang         | 0–10                        | 2             |
|            | Component-ingang         | 0–10                        | 1             |
| LCD        | 3D Ready                 | Ja of Nee                   | Ja           |
|            | 3D Enabled               | Ja of Nee                   | Nee            |
| Plasma     | Operationele Temperaturen van      | 32–110 graden              | 32            |
|            | Operationele Temperaturen tot        | 32–110 graden              | 100           |
| Projectie | De Garantie van de projectiebuis | 6, 12, of 18 maanden         | 12            |
|            | \# van projectiebuizen   | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Kenmerken en kenmerktypen

Kenmerken zijn gebaseerd op *kenmerktypen*. Het kenmerktype geeft het gegevenstype aan dat kan worden ingevoerd voor een specifiek kenmerk. De volgende kenmerktypen worden ondersteund:

- **Valuta** - Dit kenmerktype ondersteunt een valutawaarde. Het kan begrensd zijn (oftewel kan het een waardebereik ondersteunen), of kan worden opengelaten.
- **DateTime** - Dit kenmerktype ondersteunt een datum- en tijdwaarde. Dit kan worden begrensd of open blijven.
- **Decimaal** - Dit kenmerktype ondersteunt een numerieke waarde die decimalen bevat. Het kan ook een maateenheid ondersteunen. Dit kan worden begrensd of open blijven.
- **Heel getal** - Dit kenmerktype ondersteunt een numerieke waarde. Het kan ook een maateenheid ondersteunen. Dit kan worden begrensd of open blijven.
- **Tekst** - Dit kenmerktype ondersteunt een tekstwaarde. Het kan ook een vooraf bepaalde set van mogelijke waarden (dat wil zeggen een *opsomming*) ondersteunen.
- **Booleaans** - Dit type kenmerk ondersteunt een binaire waarde (**waar** of **onwaar**).
- **Verwijzing** - Dit type verwijst naar de andere kenmerken.

### <a name="set-up-attribute-types"></a>Kenmerktypen instellen

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Productgegevensbeheer** &gt; **Instellen** &gt; **Categorieën en kenmerken** &gt; **Kenmerktypen**.
3. Maak twee kenmerktypen van het type **Tekst**, stel de optie **Vaste lijst** in op **Ja** en voeg een lijst met waarden toe:

    - Geef één kenmerktype de naam **Vorm lens** en voeg de volgende waarden toe: **Ovaal**, **Vierkant** en **Rechthoek**.
    - Geef het andere kenmerktype de naam **Zonnebrilmerk** en voeg de volgende waarden toe: **Ray ban**, **Aviator** en **Oakley**.

![Typen kenmerk.](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Een kenmerk instellen

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Productgegevensbeheer** &gt; **Instellen** &gt; **Categorieën en kenmerken** &gt; **Kenmerken**.
3. Maak een kenmerk met de naam **Lens**.
4. Stel het veld **Kenmerktype** in op **Vorm lens**.

![Kenmerken.](media/Attribute.png)

## <a name="attribute-metadata"></a>Kenmerkmetagegevens

Bij *Metagegevens van het kenmerk* kunt u opties selecteren om op te geven hoe de kenmerken voor elk product moeten werken. U kunt bijvoorbeeld aangeven of kenmerken vereist zijn, kunnen worden gebruikt voor zoekopdrachten en kunnen worden gebruikt als filter in de online winkel.

Voor producten kunnen de instellingen van kenmerkmetagegevens worden overschreven op kanaalniveau. Deze functionaliteit wordt verderop in dit onderwerp besproken.

Zoals u merkt, bevat de pagina **Kenmerken** opties die betrekking hebben op metagegevens. Onder **Metagegevens van kenmerk voor POS** vindt u een optie met de naam **'Kan worden verfijnd'**. Deze is van invloed op de werking van de kenmerkwaarden in het verkooppunt (POS) of de manier waarop het systeem deze kenmerkwaarden verwerkt. Alleen kenmerken waarvoor u de optie **Kan worden verfijnd** instelt op **Ja**, worden weergegeven voor verfijnen of filteren van producten in het POS.

Dit zijn de overige opties voor kenmerkmetagegevens op de pagina **Kenmerken**:

- Zoekbaar
- Ophaalbaar
- Kan worden opgezocht
- Sorteerbaar
- Meerdere waarden toestaan
- Hoofdlettergebruik en indeling negeren
- Volledige overeenkomst

Deze opties waren oorspronkelijk bedoeld voor het verbeteren van de zoekfunctie voor de online winkel. Hoewel Commerce niet een kant-en-klare online winkel omvat, bevat het product wel de eCommerce Publishing Software Development Kit (SDK). Klanten kunnen met deze SDK producten in een zoekindex van hun keuze plaatsen. Hoewel de productgegevens zijn geïmporteerd, moeten klanten nog steeds onderscheid kunnen maken tussen doorzoekbare gegevens en gegevens die worden opgevraagd, enzovoort. In op die manier kunnen ze een optimale index maken en zorgen dat ze alleen kenmerken indexeren die, *naar hun mening*, moeten worden geïndexeerd.

Zie voor informatie over het doel van deze overige opties [Overzicht van het zoekschema in SharePoint Server 2013](/SharePoint/search/search-schema-overview).

## <a name="filter-settings-for-attributes"></a>Filterinstellingen voor kenmerken

Met filterinstellingen voor kenmerken kunt u opgeven hoe de filters voor kenmerken worden weergegeven in het POS. Voor toegang tot de filterinstellingen voor een kenmerk op de pagina **Kenmerken**, selecteert u het kenmerk en vervolgens **Filterinstellingen** in het Actievenster.

De pagina **Voorkeuren van filterweergave** bevat de volgende velden:

- **Naam** - dit veld is standaard ingesteld op de naam van het kenmerk. U kunt de waarde echter wijzigen.
- **Weergaveoptie** - De volgende opties zijn beschikbaar:

    - **Eén waarde** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Boolean**, **valuta**, **decimaal**, **geheel getal** en **tekst**. Met deze optie schakelt u één waarde in voor deze kenmerken in de client ter verfijning.
    - **Meerdere waarden** - Deze optie is beschikbaar voor de volgende kenmerktypen: **valuta**, **decimaal**, **geheel getal** en **tekst**. Met deze optie schakelt u meerdere waarden in voor dit kenmerk in de client ter verfijning.

- **Weergaveregeling** - De volgende opties zijn beschikbaar:

    - **Lijst** - Deze optie is beschikbaar voor alle kenmerktypen.
    - **Bereik** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Valuta**, **Decimaal** en **Geheel getal**.
    - **Schuifregelaar** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Valuta**, **Decimaal** en **Geheel getal**.
    - **Schuifregelaar met staven** - Deze optie is beschikbaar voor de volgende kenmerktypen: **Valuta**, **Decimaal** en **Geheel getal**.

- **Drempelwaarde** - Deze instelling is vereist als u **Bereik** hebt geselecteerd als het type weergaveregeling. U kunt waarden definiëren met behulp van een puntkomma (;) als scheidingsteken.

    Bijvoorbeeld: voor het filter **Zakvolume** kan de drempelwaarde zijn **10; 20; 50; 100; 200; 500; 1000; 5000**. In dit geval toont het POS het volgende bereik. Alle bereiken die geen producten in de resultatenset hebben, worden grijs weergegeven.

    - Minder dan 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 of meer

![Filterinstellingen van kenmerk.](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Kenmerkgroepen

Nadat de kenmerken zijn gedefinieerd, kunnen ze worden toegewezen aan de kenmerkgroepen. Een *kenmerkgroep* wordt gebruikt om de afzonderlijke kenmerken voor een onderdeel of subonderdeel in een productconfiguratiemodel te groeperen. U kunt een kenmerk opnemen in een of meer kenmerkgroepen. Met kenmerkgroepen kunnen gebruikers producten configureren omdat de verschillende selecties zijn gerangschikt in een specifieke context. U kunt kenmerkgroepen toewijzen aan categorieën of kanalen.

U kunt ook standaardwaarden instellen voor kenmerken die zijn opgenomen in een kenmerkgroep. U kunt bijvoorbeeld een kenmerk voor kleur toevoegen aan een kenmerkgroep en **blauw** selecteren als de standaardwaarde van het kenmerk. Wanneer de kenmerkgroep in dit geval wordt toegevoegd aan een product waarin kleur een van de eigenschappen is, wordt **blauw** weergegeven als de standaardkleur voor dat product.

![Kenmerkgroepen.](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Een kenmerkgroep maken

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Productgegevensbeheer** &gt; **Instellen** &gt; **Categorieën en kenmerken** &gt; **Kenmerkgroepen**.
3. Maak een kenmerkgroep met de naam **Modieuze zonnebril**.
4. Voeg de volgende kenmerken toe: **Vorm lens** en **Merk zonnebril**.

### <a name="assign-attribute-groups-to-categories"></a>Kenmerkgroepen toewijzen aan categorieën

Een of meer kenmerkgroepen kunnen worden gekoppeld aan categorieknooppunten in de volgende hiërarchietypen voor categorieën: Commerce-producthiërarchie, hiërarchie van kanaalnavigatiecategorieën en aanvullende productcategoriehiërarchie. Wanneer producten worden gecategoriseerd, erven zij de kenmerken die zijn opgenomen in de kenmerkgroepen.

![Producthiërarchie: productkenmerkgroepen.](media/AGRetailProdHierarchy.PNG)

Volg deze stappen om kenmerkgroepen toe te wijzen aan categorieën in de Commerce-producthiërarchie.

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Retail en Commerce** &gt; **Categorie- en productbeheer** &gt; **Commerce-producthiërarchie**.
3. Selecteer **Navigatiehiërarchie mode**.
4. Selecteer onder **Mannenmode** de categorie **Broek**, klik vervolgens op het sneltabblad **Productkenmerkgroepen** en voeg een kenmerkgroep toe met de naam **Herenriem**.
5. Selecteer de categorie **Modieuze zonnebril** en controleer de nieuwe kenmerken in de kenmerkgroep **Modieuze zonnebril** door **Kenmerken weergeven** te selecteren.

    De kenmerkgroep zou nu de nieuwe kenmerken **Vorm lens** en **Merk zonnebril** moeten weergeven.

6. Selecteer onder **Mannenmode** de categorie **Broek** en controleer de kenmerken voor de kenmerkgroep **Herenriem** door **Kenmerken weergeven** te selecteren.

    De kenmerkgroep zou **Merk herenriem**, **Stof riem** en **Maat riem** moeten weergeven.

> [!NOTE]
> Deze procedure kan ook worden gebruikt om kenmerkgroepen toe te wijzen aan categorieën in de hiërarchie van kanaalnavigatiecategorieën en de aanvullende productcategoriehiërarchie. Gebruik de volgende navigatiepaden in stap 2:
>
> - Retail en Commerce &gt; Categorie- en productbeheer &gt; Categorieën voor afzetkanaalnavigatie
> - Retail en Commerce &gt; Categorie- en productbeheer &gt; Aanvullende productcategorieën

### <a name="assign-attribute-groups-to-stores"></a>Kenmerkgroepen toewijzen aan winkels

Een of meer kenmerkgroepen kunnen worden gekoppeld aan een of meer winkels in de winkelhiërachie. Wanneer producten zijn verrijkt voor specifieke winkels, nemen zij de kenmerken over die zijn opgenomen in de kenmerkgroepen.

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Retail en Commerce** &gt; **Afzetkanaalinstellingen** &gt; **Kanaalcategorieën en productkenmerken**.
3. Kenmerkgroepen toewijzen aan het kanaal Houston:

    1. Selecteer het kanaal **Houston**.
    2. Selecteer op het sneltabblad **Kenmerkgroep** de optie **Toevoegen** en selecteer in het veld **Naam** **SharePointProvisionedproductAttributeGroup**.
    3. Selecteer opnieuw **Toevoegen** en selecteer in het veld **Naam** **Herenriem**.
    4. Selecteer opnieuw **Toevoegen** en selecteer in het veld **Naam** **Modieuze zonnebril**.

        > [!NOTE]
        > Selecteer de optie dat dit kanaal de kenmerkgroepen van het bovenliggende kanaal in de hiërarchie moet erven. Als u de optie **Overnemen** op **Ja** instelt, neemt het onderliggende kanaalknooppunt alle kenmerkgroepen en kenmerken van deze kenmerkgroepen over.

4. De kenmerken inschakelen zodat ze beschikbaar zijn in het kanaal Houston:

    1. Selecteer in het actievenster **Metagegevens van kenmerken instellen**.
    2. Selecteer het categorieknooppunt **Mode** en selecteer vervolgens op het sneltabblad **Afzetkanaalproductkenmerken** **Kenmerk opnemen** voor elk kenmerk.
    3. Selecteer het categorieknooppunt **Mode-accessoires**, selecteer de categorie **Modieuze zonnebril** en selecteer vervolgens op het sneltabblad **Afzetkanaalproductkenmerken** **Kenmerk opnemen** voor elk kenmerk.
    4. Selecteer het categorieknooppunt **Mannenmode**, selecteer de categorie **Broek** en selecteer vervolgens op het sneltabblad **Afzetkanaalproductkenmerken** **Kenmerk opnemen** voor elk kenmerk.

![Afzetkanaalcategorieën en productkenmerken: kenmerkgroepen.](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Overschrijven van kenmerkwaarden

De standaardwaarden van kenmerken kunnen voor afzonderlijke producten worden overschreven op het productniveau. De standaardwaarden kunnen ook worden overschreven voor afzonderlijke producten in specifieke catalogi die gericht zijn op specifieke kanalen.

### <a name="override-the-attribute-values-of-an-individual-product"></a>De waarden van kenmerken van een afzonderlijk product overschrijven

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Retail en Commerce** &gt; **Categorie- en productbeheer** &gt; **Vrijgegeven producten per categorie**.
3. Selecteer het categorieknooppunt **Mode** &gt; **Mode-accessoires** &gt; **Modieuze zonnebril**.
4. Selecteer het vereiste product in het raster. Selecteer vervolgens in het Actievenster het tabblad **Product** in de groep **Instellen** en selecteer **Productkenmerken**.
5. Selecteer een kenmerk in het linkerdeelvenster en werk vervolgens de waarde bij in het rechterdeelvenster.

![Pagina Productdetails: productkenmerkgroepen.](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>De waarden van kenmerken van producten in een catalogus overschrijven

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Retail en Commerce** &gt; **Catalogusbeheer** &gt; **Alle catalogi**.
3. Selecteer de catalogus **Fabrikam Base Catalog**.
4. Selecteer het categorieknooppunt **Mode** &gt; **Mode-accessoires** &gt; **Modieuze zonnebril**.
5. Selecteer op het sneltabblad **Producten** het vereiste product en selecteer vervolgens **Kenmerken** boven het productraster.
6. Werk de waarden van de vereiste kenmerken bij op de volgende sneltabbladen:

    - Gedeelde productmedia
    - Gedeelde productkenmerken
    - Afzetkanaalmedia
    - Afzetkanaalproductkenmerken

    > [!NOTE]
    > Als gedeelde productmedia en gedeelde productkenmerken zijn gemaakt, zijn ze van toepassing op alle producten.

![Kenmerkgroepen van catalogusproducten.](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>De waarden van kenmerken van producten in een kanaal overschrijven

1. Meld u aan bij een backoffice-client als een merchandisingbeheerder.
2. Ga naar **Retail en Commerce** &gt; **Afzetkanaalinstellingen** &gt; **Kanaalcategorieën en productkenmerken**.
3. Selecteer het kanaal **Houston**.
4. Selecteer op het sneltabblad **Producten** het vereiste product en selecteer vervolgens **Kenmerken** boven het productraster.

    > [!NOTE]
    > Als geen producten beschikbaar zijn, voegt u producten toe met **Toevoegen** op het sneltabblad **Producten** en selecteert u vervolgens de vereiste producten in het dialoogvenster **Producten toevoegen**.

5. Werk de waarden van de vereiste kenmerken bij op de volgende sneltabbladen:

    - Gedeelde productmedia
    - Gedeelde productkenmerken
    - Afzetkanaalmedia
    - Afzetkanaalproductkenmerken

    > [!NOTE]
    > Als gedeelde productmedia en gedeelde productkenmerken zijn gemaakt, zijn ze van toepassing op alle producten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
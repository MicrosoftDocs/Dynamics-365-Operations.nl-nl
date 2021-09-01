---
title: Productfilters voor magazijntransacties configureren
description: In dit onderwerp wordt beschreven hoe u productfilters en filtercodes configureert om voorraadartikelen in een magazijn te categoriseren. U kunt ook filters gebruiken om op te geven welke klanten een bepaald artikel kunnen bestellen en welke artikelen bij een bepaalde leverancier kunnen worden gekocht.
author: Mirzaab
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 6302d596245e058ae0c25fbd91333dbf050e21db5b48f6893131ec1a561e046d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768541"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Productfilters voor magazijntransacties configureren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u productfilters en filtercodes configureert om voorraadartikelen in een magazijn te categoriseren. U kunt ook filters gebruiken om op te geven welke klanten een bepaald artikel kunnen bestellen en welke artikelen bij een bepaalde leverancier kunnen worden gekocht.

Bovendien kunt u productfilters instellen en gebruiken om automatisch voorraadartikelen te organiseren in een magazijn en gefilterde artikelen te combineren in filtergroepen. Filters kunnen worden gebruikt om artikelen in categorieën te plaatsen voor verwerkings-, inkoop- en verkoopprocessen. Het kan zijn dat u artikelen wilt groepen of van elkaar wilt scheiden wanneer de manier waarop deze worden verwerkt, is gebaseerd op het gewicht of de verwerkingsbeperkingen. U kunt ook opgeven aan of van welke klanten of leveranciers een artikel kan worden gekocht of verkocht.

## <a name="prerequisites"></a>Vereisten

De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.

| Vereiste | Instructies |
|---|---|
| Voordat u producten gaat configureren op de pagina **Vrijgegeven productdetails**, moet u de magazijnverwerking voor de opslagdimensiegroep van het product inschakelen. | Ga naar **Productgegevensbeheer \> Instellingen \> Dimensie- en variantgroepen \> Opslagdimensiegroepen** en selecteer of maak een opslagdimensiegroep waarbij de optie **Magazijnbeheerprocessen gebruiken** is ingesteld op *Ja*. |
| Als u klantfilters en/of leveranciersfilters gebruikt, moet u het gebruik ervan inschakelen in de parameters voor magazijnbeheer. | Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**. Stel op het tabblad **Productfilters** de optie **Klantfilters inschakelen** en/of de optie **Leveranciersfilters inschakelen** in op *Ja*. |

## <a name="set-up-product-filters"></a>Productfilters instellen

Productfilters bieden maximaal 10 **Filtertitel**-eigenschappen. Dit zijn opsommingswaarden (enum). Deze opsommingswaarden kunnen worden geselecteerd wanneer u een productfilter maakt. De opsommingswaarden *Code 1* tot en met *Code 10* zijn door het systeem gedefinieerd en vertegenwoordigen een specifiek kenmerk of kenmerk van een artikel. *Code 1* kan bijvoorbeeld artikelen met een classificatie voor gevaarlijk materiaal vertegenwoordigen. *Code 2* kan artikelen vertegenwoordigen die alleen leveranciers kunnen inkopen. Productfilters definiëren vervolgens de specifieke waarde voor **Filtercode** die aan een waarde voor **Filtertitel** is gekoppeld.

1. Ga naar **Magazijnbeheer \> Instellingen \> Productfilters \> Productfilters**.
1. Selecteer in het actievenster de optie **Nieuw** om een productfilter toe te voegen aan het raster.
1. Selecteer een waarde in het veld **Filtertitel**.
1. Voer een waarde in het veld **Filtercode** in.

    ![Een productfilter instellen.](media/Product_Filters10.png "Een productfilter instellen")

1. Voer in het veld **Beschrijving** een naam voor de code in. *Code 2* kan bijvoorbeeld leveranciers vertegenwoordigen. U kunt vervolgens een productfilter maken voor een specifieke leverancier of groep leveranciers. Zie de sectie [Filtercodes van leveranciers instellen](#vendor-product-filters) verderop in dit onderwerp voor meer informatie.

    ![Productfilters instellen.](media/Product_Filters.png "Productfilters instellen")

## <a name="set-up-product-filter-groups"></a>Productfiltergroepen instellen

U kunt filtergroepen gebruiken om filtercodes te groeperen. Deze mogelijkheid is handig wanneer de groep wordt gebruikt in een query in een locatierichtlijn en u wilt zoeken naar de groep in plaats van naar een reeks codes. Elke filtergroep is gekoppeld aan een artikelgroep.

> [!IMPORTANT]
> Niet alle productfiltergroepen zijn beschikbaar voor filtercodes die hoger zijn dan *Code 4* (dat wil zeggen *Code 5* tot en met *Code 10*). Hoewel alle productfiltercodes bijvoorbeeld worden toegevoegd voor vrijgegeven producten, wordt de groepering van filtercodes niet bijgewerkt. Dit gedrag wordt mogelijk bijgewerkt in latere versies.

Voer de onderstaande stappen uit om filtergroepen in te stellen.

1. Ga naar **Magazijnbeheer \> Instellen \> Productfilters \> Productfiltergroepen**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in de velden **Groep 1** en **Groep 2** de namen in die worden gebruikt om artikelen te categoriseren.
1. Selecteer op het sneltabblad **Details** de optie **Nieuw** om een regel toe te voegen.
1. Voer in de velden **Begindatum/-tijd** en **Einddatum/-tijd** de begin- en einddatum voor de filtergroep in.
1. Selecteer in het veld **Artikelgroep** de artikelgroep waar het productfilter op moet worden toegepast.
1. Selecteer in de velden **Code 1** tot en met **Code 10** de filtercodes die u in de groep wilt opnemen.

    ![Artikelengroep.](media/ProdFilterGroup.png "Artikelengroep")

> [!NOTE]
> Als u een foutbericht ontvangt wanneer u de pagina sluit, kan een code-installatie ontbreken. Op de pagina **Artikelgroepen** kunt u de codes verplicht maken voor een artikelgroep door de selectievakjes **Filtercode 1 voor artikelgroep toewijzen**, **Filtercode 2 voor artikelgroep toewijzen** enzovoort in te schakelen.

## <a name="set-up-filter-codes-on-item-groups"></a>Filtercodes in artikelgroepen instellen

Door filtercodes in te stellen op een artikelgroep, kunt u de codes maken die vereist zijn voor producten die aan die artikelgroep zijn gekoppeld.

Voer de onderstaande stappen uit om filtercodes in te stellen op artikelgroepen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Voorraad \> Artikelgroepen**.
1. Selecteer in het actievenster **Nieuw** om een artikelgroep te maken.
1. Voer in het veld **Artikelgroep** een naam in.
1. Voer in het veld **Naam** een beschrijving in.
1. Schakel op het sneltabblad **Magazijn** in de sectie **Filter vereist** de selectievakjes in voor de filtercodes die voor producten moeten worden opgegeven die aan de artikelgroep zijn gekoppeld.

    Als u een vrijgegeven product wilt bijwerken, opent u de pagina **Vrijgegeven productdetails** en selecteert u vervolgens **Bewerken** in het actievenster. De filters die aan codes zijn gekoppeld, worden vervolgens beschikbaar op het sneltabblad **Magazijn**.

    ![Artikelengroepen.](media/ItemGroup10.png "Artikelengroepen")

1. Schakel in de sectie **Artikelgroepfilter** de selectievakjes in voor de filters die moeten overeenkomen om de filtergroep de standaardfiltergroep voor een artikel te maken.

    Als bijvoorbeeld de selectievakjes **Filtercode 1 gebruiken** en **Filtercode 2 gebruiken** zijn ingeschakeld, moet zowel filtercode 1 als 2 van het artikel overeenstemmen met de instellingen van de filtergroep voor de artikelgroep voordat de filtergroep kan worden geselecteerd. Wanneer u een nieuw artikel maakt, is de geselecteerde filtergroep de standaardfiltergroep in de velden **Groep 1** en **Groep 2** op het sneltabblad **Magazijn** van de pagina **Vrijgegeven productdetails**.

> [!IMPORTANT]
> Productfiltercodes worden alleen ingeschakeld voor artikelen die geavanceerd magazijnbeheer gebruiken.

## <a name="specify-filter-codes-for-released-products"></a>Filtercodes opgeven voor vrijgegeven producten

Om filtercodes op te geven voor vrijgegeven producten, voert u de volgende stappen uit: U kunt bijvoorbeeld filtercodes gebruiken om schadelijke producten te groeperen die specifieke leveranciers kopen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer in het actievenster **Nieuw** om een product te maken.
1. Voer in het dialoogvenster **Nieuw vrijgegeven product** de gegevens in die nodig zijn om de basis van een nieuw product te maken en selecteer vervolgens **OK**.

    Productfiltercodes worden alleen ingeschakeld als de artikelgroep die aan het product is gekoppeld, is geconfigureerd voor filtercodes.

    Zie [Een nieuw product maken](../pim/tasks/create-new-product.md) voor meer informatie.

1. Selecteer in het sneltabblad **Magazijn** in de sectie **Productfiltercodes** zo nodig filtercodes voor de velden **Code 1** tot en met **Code 10** om filtercodes voor het product op te geven.

## <a name="set-up-generally-available-items"></a>Algemeen beschikbare artikelen instellen

U kunt specifieke voorraadartikelen alleen voor klanten, alleen voor leveranciers, of zowel voor klanten als leveranciers beschikbaar maken.

> [!NOTE]
> Klant- en leveranciersfilters gelden niet voor een artikel dat als algemeen beschikbaar is ingesteld.

Als u algemeen beschikbaar artikelen wilt instellen, voert u de volgende stappen uit.

1. Ga naar **Magazijnbeheer \> Instellingen \> Productfilters \> Algemeen beschikbare producten**.
1. Selecteer in het actievenster **Nieuw** om een record te maken.
1. Selecteer *Klant*, *Leverancier* of *Alle* in het veld **Klant of leverancier** om de artikelen beschikbaar te maken voor klanten, leveranciers of beide.
1. Voer in het veld **Begindatum/-tijd** de datum en tijd in waarop het artikel beschikbaar komt.
1. Selecteer een artikelgroep in het veld **Artikelgroep**.
1. Selecteer in de velden **Code 1** tot en met **Code 10** de filtercodes om de artikelen te beperken die meestal beschikbaar zijn.

    Als u een artikelgroep selecteert, stelt u die artikelgroep in als algemeen beschikbaar. Door filtercodes in deze velden te selecteren, beperkt u de artikelen die beschikbaar zijn.

## <a name="set-up-customer-product-filters"></a>Productfilters voor klanten instellen

U kunt deze optionele procedure gebruiken om artikelen op te geven die voor een klant beschikbaar moeten zijn naast de artikelen die beschikbaar zijn via de filter die is ingesteld op de pagina **Algemeen beschikbare artikelen**. U kunt meerdere filters instellen voor één klant.

Voer de volgende stappen uit om klantfiltercodes in te stellen.

1. Ga naar **Verkoop en marketing \> Klanten \> Alle klanten**.
1. Selecteer een klant.
1. Selecteer in het actievenster op het tabblad **Klant** in de groep **Instellen** de optie **Productfilters**.
1. Selecteer op de pagina **Productfiltercodes** in het actievenster de optie **Nieuw**.
1. Voer in de velden **Begindatum/-tijd** en **Einddatum/-tijd** de begin- en einddatum voor de geselecteerde artikelgroep in.
1. Selecteer een artikelgroep in het veld **Artikelgroep**.
1. Selecteer in de velden **Code 1** tot en met **Code 10** de filtercodes die u wilt gebruiken als criteria om de artikelen te beperken die beschikbaar zijn voor klanten in de geselecteerde artikelgroep. U moet een selectie maken voor elke filtercode die voor de artikelgroep is ingesteld.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Productfilters voor leveranciers instellen

U kunt deze optionele procedure gebruiken om artikelen op te geven die voor een leverancier beschikbaar moeten zijn naast de artikelen die beschikbaar zijn via de filter die is ingesteld op de pagina **Algemeen beschikbare artikelen**. U kunt meerdere filters instellen voor één leverancier.

Als u leverancierfiltercodes wilt instellen, voert u de volgende stappen uit.

1. Ga naar **Inkoop en sourcing \> Leveranciers \> Alle leveranciers**.
1. Selecteer een leverancier.
1. Selecteer in het actievenster op het tabblad **Leverancier** in de groep **Instellen** de optie **Productfilters**.
1. Selecteer op de pagina **Filtercodes** in het actievenster de optie **Nieuw**.
1. Voer in de velden **Begindatum/-tijd** en **Einddatum/-tijd** de begin- en einddatum voor de geselecteerde artikelgroep in.
1. Selecteer een artikelgroep in het veld **Artikelgroep**.
1. Selecteer in de velden **Code 1** tot en met **Code 10** de filtercodes die u wilt gebruiken als criteria om de artikelen te beperken die beschikbaar zijn voor leveranciers in de geselecteerde artikelgroep. U moet een selectie maken voor elke filtercode die voor de artikelgroep is ingesteld.

> [!NOTE]
> De instelling van leveranciersproductfilters is van toepassing op vrijgegeven producten waarbij de processen voor magazijnbeheer zijn ingeschakeld voor de gekoppelde opslagdimensiegroep. De filtercodes worden gebruikt om te bepalen of gebruikers een bepaald artikel bij een bepaalde leverancier kunnen kopen wanneer ze inkooporderregels maken. Microsoft Dynamics 365 Supply Chain Management kan op twee manieren leveranciersgoedkeuring verwerken. Als er een of meer vrijgegeven producten zijn waarin het veld **Controlemethode goedgekeurde leveranciers** is ingesteld op *Alleen waarschuwing* of *Niet toegestaan*, kunnen beide goedkeuringsmethoden voor leveranciers worden ingeschakeld voor deze artikelen. Deze situatie kan problemen veroorzaken wanneer gebruikers inkooporderregels maken.

## <a name="see-also"></a>Zie ook

[Zie het blogbericht WMS-Magazijnfiltercodes voor meer informatie.](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
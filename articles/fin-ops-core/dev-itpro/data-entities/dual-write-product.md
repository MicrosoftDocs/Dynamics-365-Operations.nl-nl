---
title: Geïntegreerde productervaring
description: In dit onderwerp wordt de integratie van productgegevens tussen Finance and Operations-apps en Common Data Service beschreven.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: bcc2c3d2530153a225a94fa0fb3cc990abbf65b4
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769724"
---
# <a name="unified-product-experience"></a>Geïntegreerde productervaring

[!include [banner](../includes/banner.md)]

Wanneer een zakelijk ecosysteem bestaat uit Dynamics 365-toepassingen, zoals Finance, Supply Chain Management en Sales, gebruiken bedrijven deze toepassingen vaak als bron voor productgegevens. Dit komt omdat deze apps een robuuste productinfrastructuur bieden, aangevuld met geavanceerde prijsbegrippen en nauwkeurige voorraadgegevens. Bedrijven die een extern PLM-systeem (Product Lifecycle Management) gebruiken voor de productgegevens, kunnen producten van Finance and Operations-apps doorsturen naar andere Dynamics 365-apps. De geïntegreerde productervaring brengt het geïntegreerde productgegevensmodel over naar Common Data Service, zodat alle gebruikers, inclusief gebruikers van de toepassing Power Platform, kunnen profiteren van de uitgebreide productgegevens die afkomstig zijn van Finance and Operations-apps.

Dit is het productgegevensmodel van Sales.

![Gegevensmodel voor producten in CE](media/dual-write-product-4.jpg)

Dit is het productgegevensmodel uit Finance and Operations-apps.

![Gegevensmodel voor producten in Finance and Operations](media/dual-write-products-5.jpg)

Deze twee productgegevensmodellen zijn geïntegreerd in Common Data Service zoals hieronder weergegeven.

![Gegevensmodel voor producten in Dynamics 365-apps](media/dual-write-products-6.jpg)

De entiteitstoewijzingen voor twee keer wegschrijven voor producten zijn zo ontworpen dat gegevens alleen in één richting stromen, bijna in realtime, tussen Finance and Operations-apps en Common Data Service. De productinfrastructuur is echter open, zodat deze zo nodig bidirectioneel kan worden gemaakt. Hoewel u dit kunt aanpassen, doet u dat op eigen risico, aangezien Microsoft deze aanpak niet aanbeveelt.

## <a name="templates"></a>Sjablonen

Productinformatie bevat alle informatie die betrekking heeft op het product en de definitie ervan, zoals de productdimensies of de tracerings- en opslagdimensies. Zoals in de volgende tabel wordt aangegeven, wordt een verzameling entiteitstoewijzingen gemaakt om producten en gerelateerde informatie te synchroniseren.

Finance en Operations | Andere Dynamics 365-apps | Beschrijving
-----------------------|--------------------------------|---
Vrijgegeven producten V2 | msdyn\_sharedproductdetails | De entiteit **msdyn\_sharedproductdetails** bevat de velden van Finance and Operations-apps die het product definiëren en die de financiële en beheergegevens van het product bevatten. De volgende tabel geeft de toewijzingen weer.
Door Common Data Service vrijgegeven verschillende producten | Product | De entiteit **Product** bevat de velden die het product definiëren. Het bevat afzonderlijke producten (producten met het subtype product) en de productvarianten. De volgende tabel geeft de toewijzingen weer.
Met streepjescode geïdentificeerd productnummer | msdyn\_productbarcodes | Productstreepjescodes worden gebruikt om producten op unieke wijze te identificeren.
Standaard orderinstellingen | msdyn\_productdefaultordersettings
Productspecifieke standaard orderinstellingen | msdyn_productdefaultordersettings
Productdimensiegroepen | msdyn\_productdimensiongroups | De productdimensiegroep bepaalt welke productdimensies het product definiëren. 
Opslagdimensiegroepen | msdyn\_productstoragedimensiongroups | De dimensiegroep voor productopslag geeft de methode aan die wordt gebruikt voor het definiëren van de plaatsing van het product in het magazijn.
Traceringsdimensiegroepen | msdyn\_producttrackingdimensiongroups | De dimensiegroep voor producttracering geeft de methode aan die wordt gebruikt om het product in de voorraad te volgen.
Kleuren | msdyn\_productcolors
Afmetingen | msdyn\_productsizes
Stijlen | msdyn\_productsytles
Configuraties | msdyn\_productconfigurations
Kleuren van productmodellen | msdyn_sharedproductcolors | De entiteit **Gedeelde productkleur** geeft de kleuren aan die een specifiek productmodel kan hebben. Dit concept wordt naar Common Data Service gemigreerd om gegevens consistent te houden.
Afmetingen van productmodellen | msdyn_sharedproductsizes | De entiteit **Gedeelde productmaat** geeft de maten aan die een specifiek productmodel kan hebben. Dit concept wordt naar Common Data Service gemigreerd om gegevens consistent te houden.
Stijlen van productmodellen | msdyn_sharedproductstyles | De entiteit **Gedeelde productstijl** geeft de stijlen aan die een specifiek productmodel kan hebben. Dit concept wordt naar Common Data Service gemigreerd om gegevens consistent te houden.
Configuraties van productmodellen | msdyn_sharedproductconfigurations | De entiteit **Gedeelde productconfiguratie** geeft de configuraties aan die een specifiek productmodel kan hebben. Dit concept wordt naar Common Data Service gemigreerd om gegevens consistent te houden.
Alle producten | msdyn_globalproducts | De entiteit met alle producten bevat alle producten die beschikbaar zijn in Finance and Operations-apps, zowel de vrijgegeven producten als de niet-vrijgegeven producten.
Eenheid | uoms
Eenheidsomrekeningen | msdyn_ unitofmeasureconversions
Productspecifieke conversie van maateenheid | msdyn_productspecificunitofmeasureconversion
Productcategorieën | msdyn_productcategories | Alle productcategorieën en informatie over de structuur en kenmerken van deze producten zijn opgenomen in de entiteit productcategorie. 
Hiërarchieën van productcategorieën | msdyn_productcategoryhierarhies | U gebruikt producthiërarchieën om producten te categoriseren of te groeperen. De categoriehiërarchieën zijn beschikbaar in Common Data Service via de entiteit Productcategoriehiërarchie. 
Hiërarchierollen van productcategorieën | msdyn_productcategoryhierarchies | Producthiërarchieën kunnen worden gebruikt voor verschillende rollen in D365 Finance and Operations. Om te specificeren welke categorie wordt gebruikt in elke rol wordt de entiteit rol van productcategorie gebruikt met de volgende toewijzingen. 
Toewijzingen van productcategorieën | msdyn_productcategoryassignments | Als u een product aan een categorie wilt toewijzen, kunt u de entiteit productcategorietoewijzingen gebruiken.

## <a name="integration-of-products"></a>Integratie van producten

In dit model wordt het product vertegenwoordigd door de combinatie van twee entiteiten in Common Data Service: **Product** en **msdyn\_sharedproductdetails**. Terwijl de eerste entiteit de definitie van een product bevat (de unieke identificatie voor het product, de productnaam en de omschrijving), bevat de tweede entiteit de velden die zijn opgeslagen op productniveau. De combinatie van deze twee entiteiten wordt gebruikt om het product te definiëren volgens het concept van de Stock Keeping Unit (SKU). Elk vrijgegeven product bevat de informatie in de vermelde entiteiten (Product en Gedeelde productgegevens). Als u alle producten wilt bijhouden (vrijgegeven en niet vrijgegeven), wordt de entiteit **Algemene producten** gebruikt. 

Omdat het product als een SKU wordt voorgesteld, kunt u de concepten van afzonderlijke producten, productmodellen en productvarianten op de volgende manier vastleggen in Common Data Service:

- **Producten met subtype product** zijn producten die door zichzelf worden gedefinieerd. Er hoeven geen dimensies te worden gedefinieerd. Een voorbeeld is een specifiek boek. Voor deze producten wordt één record gemaakt in de entiteit **Product** en één record in de entiteit **msdyn\_sharedproductdetails**. Er wordt geen record met een productfamilie gemaakt.
- **Productmodellen** worden gebruikt als algemene producten die de definitie bevatten en regels die het gedrag in bedrijfsprocessen bepalen. Op basis van deze definities kunnen verschillende producten worden gegenereerd die productvarianten worden genoemd. T-shirt is bijvoorbeeld het productmodel dat kleur en maat als dimensies kan hebben. Er kunnen varianten worden vrijgegeven die verschillende combinaties van deze dimensies hebben, zoals een klein blauw T-shirt of een middelgroot groen T-shirt. Bij de integratie wordt één record per variant gemaakt in de producttabel. Deze record bevat de specifieke gegevens over varianten, zoals de verschillende dimensies. De algemene informatie voor het product wordt opgeslagen in de entiteit **msdyn\_sharedproductdetails**. (Deze algemene informatie wordt opgeslagen in het productmodel.) Daarnaast wordt één record met de productfamilie gemaakt per productmodel. De productmodelgegevens worden gesynchroniseerd met Common Data Service zodra het vrijgegeven productmodel wordt gemaakt (maar voordat varianten worden vrijgegeven).
- **Verschillende producten** verwijzen naar alle subtypeproducten van het product en alle productvarianten. 

![Gegevensmodel voor producten](media/dual-write-product.png)

Als de functie voor twee keer wegschrijven is ingeschakeld, worden de apps van Finance and Operations gesynchroniseerd in andere Dynamics 365-apps in de status **Concept**. Ze worden toegevoegd aan de eerste prijslijst met dezelfde valuta. Met andere woorden ze worden toegevoegd aan de eerste prijslijst in een Dynamics 365-app die overeenkomt met de valuta van uw rechtspersoon waar het product wordt vrijgegeven in een Finance and Operations-app. 

Standaard worden producten van Finance and Operations-apps gesynchroniseerd met andere Dynamics 365-app in de status **Concept**. Om het product te synchroniseren met de status **Actief**, zodat u het rechtstreeks in verkooporderoffertes kunt gebruiken, moet u bijvoorbeeld de volgende instelling kiezen: ga naar **Systeem > Beheer > Systeembeheer > Systeeminstellingen > tabblad Verkoop** en selecteer **Producten maken in actieve status = Ja**. 

De synchronisatie van producten gebeurt vanuit Finance and Operations-apps naar Common Data Service. Dit betekent dat de waarden van de velden van de productentiteit weliswaar kunnen worden gewijzigd in Common Data Service, maar dat bij activering van de synchronisatie (wanneer een productveld wordt gewijzigd in een Finance and Operations-app), de waarden in Common Data Service worden overschreven. 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [products](dual-write/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](dual-write/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](dual-write/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Productdimensies 

Productdimensies zijn kenmerken die de variant van een product identificeren. De vier productdimensies (kleur, maat, stijl en configuratie) worden ook toegewezen aan Common Data Service voor het definiëren van de productvarianten. In de volgende afbeelding wordt het gegevensmodel voor de productdimensie Kleur weergegeven. Hetzelfde model wordt toegepast op maten, stijlen en configuraties. 

![Gegevensmodel voor producten](media/dual-write-product-2.PNG)

[!include [product colors](dual-write/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](dual-write/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](dual-write/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](dual-write/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Wanneer een product verschillende productdimensies heeft (een productmodel heeft bijvoorbeeld maat en kleur als productdimensies), wordt elk afzonderlijk product (elke productvariant) gedefinieerd als een combinatie van deze productdimensies. Productnummer B0001 is bijvoorbeeld een XS zwart T-shirt en het productnummer B0002 is een S zwart T-shirt. In dit geval worden de bestaande combinaties van productdimensies gedefinieerd. Het T-shirt in het vorige voorbeeld kan bijvoorbeeld XS en zwart, S en zwart, M en zwart, L en zwart zijn, maar kan niet XL en zwart worden. Met andere woorden de mogelijke productdimensies voor een productmodel worden opgegeven en varianten kunnen worden vrijgegeven op basis van deze waarden.

Voor het bijhouden van de productdimensies die door een productmodel kunnen worden gebruikt, worden de volgende entiteiten gemaakt en in Common Data Service toegewezen voor elke productdimensie. Zie voor meer informatie [Overzicht met productinformatie](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](dual-write/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](dual-write/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](dual-write/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](dual-write/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](dual-write/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standaardorderinstellingen en productspecifieke standaardorderinstellingen

Standaardorderinstellingen definiëren de locatie en het magazijn waaruit de artikelen worden geleverd of waarin ze worden opgeslagen, de minimum-, maximum-, meervoud- en standaardhoeveelheden die voor handel of voorraadbeheer worden gebruikt, de levertijden, de eindevlag, en de methode voor orderbelofte. Deze informatie is beschikbaar in Common Data Service met behulp van de standaardorderinstellingen en de entiteit voor productspecifieke standaardorderinstellingen. Meer informatie over de functionaliteit vindt u in het onderwerp [Standaardorderinstellingen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](dual-write/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](dual-write/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Maateenheid en maateenheidsconversies

De maateenheden en de bijbehorende conversies zijn beschikbaar in Common Data Service conform het gegevensmodel dat in het diagram wordt weergegeven.

![Gegevensmodel voor producten](media/dual-write-product-3.PNG)

Het concept voor maateenheden is geïntegreerd tussen de Finance and Operations-apps en de andere Dynamics 365-apps. Voor elke eenheidsklasse in een Finance and Operations-app wordt een eenhedengroep gemaakt in een Dynamics 365-app, die de eenheden bevat die bij de eenheidsklasse horen. Er wordt ook een standaard basiseenheid voor elke eenhedengroep gemaakt. 

[!include [unit of measure](dual-write/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](dual-write/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product specific unit of measure conversions](dual-write/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Initiële synchronisatie van eenheden bij gegevensafstemming tussen Finance and Operations en Common Data Service

### <a name="initial-synchronization-of-units"></a>Initiële synchronisatie van eenheden

Als twee keer wegschrijven is ingeschakeld, worden eenheden uit Finance and Operations-apps gesynchroniseerd met andere Dynamics 365-apps. De eenhedengroepen die vanuit Finance and Operations-apps worden gesynchroniseerd in Common Data Service hebben een markering ingesteld die aangeeft dat deze extern worden onderhouden.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Overeenkomende eenheden en gegevens uit eenheidsklassen/groepen uit Finance and Operations en andere Dynamics 365-apps

Allereerst is het belangrijk te weten dat de integratiesleutel voor eenheid msdyn_symbol is. Daarom moet deze waarde uniek zijn in Common Data Service of andere Dynamics 365-apps. Omdat in andere Dynamics 365-apps via de combinatie van "Eenhedengroep-id" en "Naam" de uniekheid van een eenheid wordt gedefinieerd, moet u rekening houden met verschillende scenario's voor het afstemmen van eenheidsgegevens tussen Finance and Operations-apps en Common Data Service.

Voor eenheden die overeenkomen met of overlappen in Finance and Operations-apps en andere Dynamics 365-apps:

+ **De eenheid behoort tot een eenhedengroep in andere Dynamics 365-apps die overeenkomt met de bijbehorende eenheidsklasse in Finance and Operations-apps**. In dit geval moet het veld msdyn_symbol in andere Dynamics 365-apps worden ingevuld met het eenheidssymbool uit Finance and Operations-apps. Dus wanneer de gegevens worden afgestemd, wordt de eenhedengroep ingesteld op "Extern onderhouden" in andere Dynamics 365-apps.
+ **De eenheid behoort tot een eenhedengroep in andere Dynamics 365-apps die niet overeenkomen met de bijbehorende eenheidsklasse in Finance and Operations-apps (geen bestaande eenheidsklasse in Finance and Operations-apps voor de eenheidsklasse in andere Dynamics 365-apps).** In dit geval moet een willekeurige tekenreeks worden ingevuld bij msdyn_symbol. Let op: deze waarde moet uniek zijn in andere Dynamics 365-apps.

Voor eenheden en eenheidsklassen in Finance and Operations-apps die niet bestaan in andere Dynamics 365-apps:

Als onderdeel van het dubbel schrijven worden de eenhedengroepen van Finance and Operations-apps en de bijbehorende eenheden gemaakt en gesynchroniseerd in andere Dynamics 365-apps en Common Data Service en wordt de eenhedengroep ingesteld op "Extern onderhouden". Er is geen extra inspanning voor bootstrapping vereist.

Voor eenheden in andere Dynamics 365-apps die niet bestaan in Finance and Operations-apps:

Het veld msdyn_symbol moet worden ingevuld voor alle eenheden. De eenheden kunnen altijd worden gemaakt in Finance and Operations-apps in de bijbehorende eenheidsklasse (indien aanwezig). Als de eenheidsklasse niet bestaat, moet deze eerst worden gemaakt (houd er rekening mee dat u geen eenheidsklasse kunt maken in Finance and Operations-apps behalve via uitbreiding als u de enum uitbreidt) die overeenkomt met de andere eenhedengroep voor Dynamics 365-apps. U kunt vervolgens de eenheid maken. Houd er rekening mee dat het eenheidssymbool in Finance and Operations-apps het msdyn_symbol moet zijn dat eerder is opgegeven in andere Dynamics 365-apps voor de eenheid.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Productbeleid: dimensie-, tracerings- en opslaggroepen

Het productbeleid is een set beleidsregels die wordt gebruikt voor het definiëren van producten en de bijbehorende kenmerken in voorraad. De productdimensiegroep, producttraceringsdimensiegroep en opslagdimensiegroep kunnen deel uitmaken van het productbeleid. 

[!include [product dimension group](dual-write/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](dual-write/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](dual-write/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Producthiërarchieën

[!include [product category hierarchy](dual-write/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](dual-write/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](dual-write/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](dual-write/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Integratiesleutel voor producten 

Voor unieke identificatie van producten tussen Dynamics 365 for Finance and Operations en producten in Common Data Service worden de integratiesleutels gebruikt. Voor producten is **(productnumber)** de unieke sleutel waarmee een product wordt geïdentificeerd in Common Data Service. Het wordt samengesteld door samenvoeging van: **(company, msdyn_productnumber)**. Met **company** wordt de rechtspersoon in Finance and Operations aangegeven en met **msdyn_productnumber** wordt het productnummer aangegeven voor het specifieke product in Finance and Operations. 

Voor een andere gebruiker van Dynamics 365-apps wordt het product in de gebruikersinterface geïdentificeerd met **msdyn_productnumber** (de label van het veld is **Productnummer**). In het productformulier worden zowel het bedrijf als msydn_productnumber weergegeven. Het veld (productNumber), de unieke sleutel voor een product, wordt echter niet weergegeven. 

Houd er rekening mee dat als apps boven op Common Data Service worden gebouwd, speciale aandacht moet worden besteed aan het gebruik van het (productNumber), dat wil zeggen de unieke product-id, als integratiesleutel en niet aan msdyn_productnumber, omdat de laatste waarde niet uniek is. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Initiële synchronisatie van producten en migratie van gegevens van Common Data Service naar Finance and Operations

### <a name="initial-synchronization-of-products"></a>Initiële synchronisatie van producten 

Als twee keer wegschrijven is ingeschakeld, worden producten uit Dynamics 365 Finance and Operations gesynchroniseerd met Common Data Service en andere Dynamics 365-apps. Producten die zijn gemaakt in Common Data Service en andere Dynamics 365-apps vóór twee keer wegschrijven, worden niet bijgewerkt of komen niet overeen met productgegevens uit Finance and Operations.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Overeenkomende productgegevens uit Finance and Operations en andere Dynamics 365-apps

Als dezelfde producten worden bewaard (overlappend/overeenkomend) in Finance and Operations en in Common Data Service en andere Dynamics 365-apps, wordt bij het inschakelen van twee keer wegschrijven de synchronisatie van producten vanuit Finance and Operations uitgevoerd en worden dubbele records weergegeven in Common Data Service voor hetzelfde product.
Als andere Dynamics 365-apps producten hebben die overlappen/overeenkomen met Finance and Operations kan de vorige situatie worden vermeden als de beheerder die twee keer wegschrijven inschakelt bootstrapping uitvoert voor de velden **Bedrijf** (voorbeeld: "USMF") en **msdyn_productnumber** (voorbeeld: "1234:Black:S") voordat de synchronisatie van producten plaatsvindt. Met andere woorden, deze twee velden in het product in Common Data Service moeten worden ingevuld met het desbetreffende bedrijf in Finance and Operations waarmee het product moet worden afgestemd en met het bijbehorende productnummer. 

Wanneer de synchronisatie is ingeschakeld en wordt uitgevoerd, worden de producten van Finance and Operations vervolgens gesynchroniseerd met de overeenkomende producten in Common Data Service en andere Dynamics 365-apps. Dit geld voor zowel verschillende producten als productvarianten. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Migratie van productgegevens vanuit andere Dynamics 365-apps naar Finance and Operations

Als andere Dynamics 365-apps producten hebben die niet aanwezig zijn in Finance and Operations, kan de beheerder eerst **EcoResReleasedproductCreationV2Entity** gebruiken voor het importeren van die producten in Finance and Operations. Vervolgens kunnen de productgegevens uit Finance and Operations en andere Dynamics 365-apps dan worden afgestemd zoals hierboven beschreven. 

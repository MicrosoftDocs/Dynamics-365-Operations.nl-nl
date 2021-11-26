---
title: Uniforme productervaring
description: In dit onderwerp wordt de integratie van productgegevens tussen Finance and Operations-apps en Dataverse beschreven.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 81f49cf08dcd1b4b1c3d71ff286a1f070e65e914
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782327"
---
# <a name="unified-product-experience"></a>Uniforme productervaring

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Wanneer een zakelijk ecosysteem bestaat uit Dynamics 365-toepassingen, zoals Finance, Supply Chain Management en Sales, gebruiken bedrijven deze toepassingen vaak als bron voor productgegevens. Deze apps bieden namelijk een robuuste productinfrastructuur, aangevuld met geavanceerde prijsbegrippen en nauwkeurige voorraadgegevens. Bedrijven die een extern PLM-systeem (Product Lifecycle Management) gebruiken voor de productgegevens, kunnen producten van Finance and Operations-apps doorsturen naar andere Dynamics 365-apps. De geïntegreerde productervaring brengt het geïntegreerde productgegevensmodel over naar Dataverse, zodat alle gebruikers, inclusief Power Platform-gebruikers, kunnen profiteren van de uitgebreide productgegevens die afkomstig zijn van Finance and Operations-apps.

Dit is het productgegevensmodel van Sales.

![Gegevensmodel voor producten in CE.](media/dual-write-product-4.jpg)

Dit is het productgegevensmodel van Finance and Operations-apps.

![Gegevensmodel voor producten in Finance and Operations.](media/dual-write-products-5.jpg)

Deze twee productgegevensmodellen zijn geïntegreerd in Dataverse zoals hieronder weergegeven.

![Gegevensmodel voor producten in Dynamics 365-apps.](media/dual-write-products-6.jpg)

De tabeltoewijzingen voor twee keer wegschrijven voor producten zijn zo ontworpen dat gegevens alleen in één richting stromen, bijna in realtime, tussen Finance and Operations-apps en Dataverse. De productinfrastructuur is echter open, zodat deze zo nodig bidirectioneel kan worden gemaakt. Hoewel u dit kunt aanpassen, doet u dat op eigen risico, aangezien Microsoft deze aanpak niet aanbeveelt.

## <a name="templates"></a>Sjablonen

Productinformatie bevat alle informatie die betrekking heeft op het product en de definitie ervan, zoals de productdimensies of de tracerings- en opslagdimensies. Zoals in de volgende tabel wordt weergegeven, wordt er een verzameling tabeltoewijzingen gemaakt om producten en verwante informatie te synchroniseren.

Finance and Operations-apps | Andere Dynamics 365-apps | Beschrijving
-----------------------|--------------------------------|---
[Alle producten](mapping-reference.md#138) | msdyn_globalproducts | De tabel met alle producten bevat alle producten die beschikbaar zijn in Finance and Operations-apps, zowel de vrijgegeven producten als de niet-vrijgegeven producten.
[Door CDS vrijgegeven verschillende producten](mapping-reference.md#213) | Artikel | De tabel **Product** bevat de kolommen die het product definiëren. Het bevat afzonderlijke producten (producten met het subtype product) en de productvarianten. De volgende tabel geeft de toewijzingen weer.
[Kleuren](mapping-reference.md#170) | msdyn\_productcolors
[Configuraties](mapping-reference.md#171) | msdyn\_productconfigurations
[Standaard orderinstellingen](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Productcategorieën](mapping-reference.md#166) | msdyn_productcategories | Alle productcategorieën en informatie over de structuur en kenmerken van deze producten zijn opgenomen in de productcategorietabel.
[Toewijzingen van productcategorieën](mapping-reference.md#167) | msdyn_productcategoryassignments | Als u een product aan een categorie wilt toewijzen, kunt u de tabel productcategorietoewijzingen gebruiken.
[Hiërarchieën van productcategorieën](mapping-reference.md#168) | msdyn_productcategoryhierarchies | U gebruikt producthiërarchieën voor het categoriseren of groeperen van producten. De categoriehiërarchieën zijn beschikbaar in Dataverse via de tabel Productcategoriehiërarchie.
[Hiërarchierollen van productcategorieën](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Producthiërarchieën kunnen worden gebruikt voor verschillende rollen in D365 Finance and Operations. Hiermee wordt opgegeven welke categorie wordt gebruikt in elke rol waarvoor de tabel voor productcategorierollen wordt gebruikt.
[Standaard orderinstellingen voor product V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Productdimensiegroepen](mapping-reference.md#173) | msdyn\_productdimensiongroups | De productdimensiegroep bepaalt welke productdimensies het product definiëren.
[Kleuren van productmodellen](mapping-reference.md#187) | msdyn_sharedproductcolors | De tabel **Gedeelde productkleur** geeft de kleuren aan die een specifiek productmodel kan hebben. Dit concept wordt naar Dataverse gemigreerd om gegevens consistent te houden.
[Configuraties van productmodellen](mapping-reference.md#188) | msdyn_sharedproductconfigurations | De tabel **Gedeelde productconfiguratie** geeft de configuraties aan die een specifiek productmodel kan hebben. Dit concept wordt naar Dataverse gemigreerd om gegevens consistent te houden.
[Afmetingen van productmodellen](mapping-reference.md#190) | msdyn_sharedproductsizes | De tabel **Gedeelde productmaat** geeft de maten aan die een specifiek productmodel kan hebben. Dit concept wordt naar Dataverse gemigreerd om gegevens consistent te houden.
[Stijlen van productmodellen](mapping-reference.md#191) | msdyn_sharedproductstyles | De tabel **Gedeelde productstijl** geeft de stijlen aan die een specifiek productmodel kan hebben. Dit concept wordt naar Dataverse gemigreerd om gegevens consistent te houden.
[Geïdentificeerde streepjescodes voor productnummer](mapping-reference.md#164) | msdyn\_productbarcodes | Productstreepjescodes worden gebruikt om producten op unieke wijze te identificeren.
[Productspecifieke eenheidsconversies](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Vrijgegeven producten V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | De tabel **msdyn\_sharedproductdetails** bevat de kolommen van Finance and Operations-apps die het product definiëren en die de financiële en beheergegevens van het product bevatten.
[Afmetingen](mapping-reference.md#174) | msdyn\_productsizes
[Opslagdimensiegroepen](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | De dimensiegroep voor productopslag geeft de methode aan die wordt gebruikt voor het definiëren van de plaatsing van het product in het magazijn.
[Stijlen](mapping-reference.md#178) | msdyn\_productsytles
[Traceringsdimensiegroepen](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | De dimensiegroep voor producttracering geeft de methode aan die wordt gebruikt om het product in de voorraad te volgen.
[Eenheden](mapping-reference.md#219) | uoms
[Eenheidsomrekeningen](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Integratie van producten

In dit model wordt het product vertegenwoordigd door de combinatie van twee tabellen in Dataverse: **Product** en **msdyn\_sharedproductdetails**. Terwijl de eerste tabel de definitie van een product bevat (de unieke identificatie voor het product, de productnaam en de omschrijving), bevat de tweede tabel de kolommen die zijn opgeslagen op productniveau. De combinatie van deze twee tabellen wordt gebruikt om het product te definiëren volgens het concept van de Stock Keeping Unit (SKU). Elk vrijgegeven product bevat de informatie in de vermelde tabellen (Product en Gedeelde productgegevens). Als u alle producten wilt bijhouden (vrijgegeven en niet vrijgegeven), wordt de tabel **Algemene producten** gebruikt.

Omdat het product als een SKU wordt voorgesteld, kunt u de concepten van afzonderlijke producten, productmodellen en productvarianten op de volgende manier vastleggen in Dataverse:

- **Producten met subtype product** zijn producten die door zichzelf worden gedefinieerd. Er hoeven geen dimensies te worden gedefinieerd. Een voorbeeld is een specifiek boek. Voor deze producten wordt één rij gemaakt in de tabel **Product** en één rij in de tabel **msdyn\_sharedproductdetails**. Er wordt geen rij met een productfamilie gemaakt.
- **Productmodellen** worden gebruikt als algemene producten die de definitie bevatten en regels die het gedrag in bedrijfsprocessen bepalen. Op basis van deze definities kunnen verschillende producten worden gegenereerd die productvarianten worden genoemd. T-shirt is bijvoorbeeld het productmodel dat kleur en maat als dimensies kan hebben. Er kunnen varianten worden vrijgegeven die verschillende combinaties van deze dimensies hebben, zoals een klein blauw T-shirt of een middelgroot groen T-shirt. Bij de integratie wordt één rij per variant gemaakt in de producttabel. Deze rij bevat de specifieke gegevens over varianten, zoals de verschillende dimensies. De algemene informatie voor het product wordt opgeslagen in de tabel **msdyn\_sharedproductdetails**. (Deze algemene informatie bevindt zich in het productmodel.) De productmodelgegevens worden gesynchroniseerd met Dataverse zodra het vrijgegeven productmodel wordt gemaakt (maar voordat varianten worden vrijgegeven).
- **Verschillende producten** verwijzen naar alle subtypeproducten van het product en alle productvarianten.

![Gegevensmodel voor producten.](media/dual-write-product.png)

Als de functie voor twee keer wegschrijven is ingeschakeld, worden de producten van Finance and Operations gesynchroniseerd in andere Dynamics 365-producten in de status **Concept**. Deze worden toegevoegd aan de eerste prijslijst met dezelfde valuta die wordt gebruikt in de app Customer Engagement alfabetisch gesorteerd op de naam van de prijslijst. Met andere woorden: ze worden toegevoegd aan de eerste prijslijst in een Dynamics 365-app die overeenkomt met de valuta van uw rechtspersoon waar het product wordt vrijgegeven in een Finance and Operations-app. Als er geen prijslijst voor de opgegeven valuta is, wordt automatisch een prijslijst gemaakt en wordt het product eraan toegewezen.

De huidige implementatie van de invoegtoepassingen voor twee keer wegschrijven die de standaardprijslijst aan de eenheid koppelen, zoeken de valuta die aan de app is gekoppeld en zoeken met de Finance and Operations-app naar de eerste prijslijst in de app voor klantbetrokkenheid met behulp van alfabetisch sorteren op de naam van de prijslijst. Als u een standaardprijslijst voor een specifieke valuta wilt instellen wanneer u meerdere prijslijsten voor die valuta hebt, moet u de naam van de prijslijst bijwerken naar een naam die eerder in de alfabetische volgorde voorkomt dan andere prijslijsten voor die valuta. Als er geen prijslijst voor de opgegeven valuta is, wordt een nieuwe aangemaakt.

Standaard worden producten van Finance and Operations-apps gesynchroniseerd met andere Dynamics 365-app in de status **Concept**. Om het product te synchroniseren met de status **Actief**, zodat u het rechtstreeks in verkooporderoffertes kunt gebruiken, moet u bijvoorbeeld de volgende instelling kiezen: ga naar **Systeem > Beheer > Systeembeheer > Systeeminstellingen > tabblad Verkoop** en selecteer **Producten maken in actieve status = Ja**.

Wanneer producten worden gesynchroniseerd, moet u een waarde invoeren voor het veld **Verkoopeenheid** in de Finance and Operations-app, omdat dit een verplicht veld is in Sales.

Het maken van productfamilies vanuit Dynamics 365 Sales wordt niet ondersteund bij de synchronisatie van het tweemaal wegschrijven van producten.

De synchronisatie van producten gebeurt vanuit de Finance and Operations-app naar Dataverse. Dit betekent dat de waarden van de kolommen van de producttabel weliswaar kunnen worden gewijzigd in Dataverse, maar dat bij activering van de synchronisatie (wanneer een productkolom wordt gewijzigd in een Finance and Operations-app), de waarden in Dataverse worden overschreven.

Finance and Operations-apps | Customer Engagement-apps |
---|---
[Door CDS vrijgegeven verschillende producten](mapping-reference.md#213) | Artikel |
[Vrijgegeven producten V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Alle producten](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Productdimensies

Productdimensies zijn kenmerken die de variant van een product identificeren. De vier productdimensies (kleur, maat, stijl en configuratie) worden ook toegewezen aan Dataverse voor het definiëren van de productvarianten. In de volgende afbeelding wordt het gegevensmodel voor de productdimensie Kleur weergegeven. Hetzelfde model wordt toegepast op maten, stijlen en configuraties.

![Gegevensmodel voor productdimensies.](media/dual-write-product-two.png)

Finance and Operations-apps | Customer Engagement-apps |
---|---
[Kleuren](mapping-reference.md#170) | msdyn\_productcolors
[Afmetingen](mapping-reference.md#174) | msdyn\_productsizes
[Stijlen](mapping-reference.md#178) | msdyn\_productsytles
[Configuraties](mapping-reference.md#171) | msdyn\_productconfigurations

Wanneer een product verschillende productdimensies heeft (een productmodel heeft bijvoorbeeld maat en kleur als productdimensies), wordt elk afzonderlijk product (elke productvariant) gedefinieerd als een combinatie van deze productdimensies. Productnummer B0001 is bijvoorbeeld een XS zwart T-shirt en het productnummer B0002 is een S zwart T-shirt. In dit geval worden de bestaande combinaties van productdimensies gedefinieerd. Het T-shirt in het vorige voorbeeld kan bijvoorbeeld XS en zwart, S en zwart, M en zwart, L en zwart zijn, maar kan niet XL en zwart worden. Met andere woorden de mogelijke productdimensies voor een productmodel worden opgegeven en varianten kunnen worden vrijgegeven op basis van deze waarden.

Voor het bijhouden van de productdimensies die door een productmodel kunnen worden gebruikt, worden de volgende tabellen gemaakt en in Dataverse toegewezen voor elke productdimensie. Zie voor meer informatie [Overzicht met productinformatie](../../../../supply-chain/pim/product-information.md).

Finance and Operations-apps | Customer Engagement-apps |
---|---
[Kleuren van productmodellen](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Configuraties van productmodellen](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Afmetingen van productmodellen](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Stijlen van productmodellen](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Geïdentificeerde streepjescodes voor productnummer](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standaardorderinstellingen en productspecifieke standaardorderinstellingen

Standaardorderinstellingen definiëren de locatie en het magazijn waaruit de artikelen worden geleverd of waarin ze worden opgeslagen, de minimum-, maximum-, meervoud- en standaardhoeveelheden die voor handel of voorraadbeheer worden gebruikt, de levertijden, de eindevlag, en de methode voor orderbelofte. Deze informatie is beschikbaar in Dataverse met behulp van de standaardorderinstellingen en de entiteit voor productspecifieke standaardorderinstellingen. Meer informatie over de functionaliteit vindt u in het onderwerp [Standaardorderinstellingen](../../../../supply-chain/production-control/default-order-settings.md).

Finance and Operations-apps | Customer Engagement-apps |
---|---
[Standaard orderinstellingen](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Standaard orderinstellingen voor product V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Maateenheid en maateenheidsconversies

De maateenheden en de bijbehorende conversie zijn beschikbaar in Dataverse conform het gegevensmodel dat in het diagram wordt weergegeven.

![Gegevensmodel voor maateenheid.](media/dual-write-product-three.png)

Het concept voor maateenheden is geïntegreerd tussen de Finance and Operations-apps en de andere Dynamics 365-apps. Voor elke eenheidsklasse in een Finance and Operations-app wordt een eenhedengroep gemaakt in een Dynamics 365-app, die de eenheden bevat die bij de eenheidsklasse horen. Er wordt ook een standaard basiseenheid voor elke eenhedengroep gemaakt.

Finance and Operations-apps | Customer Engagement-apps |
---|---
[Productspecifieke eenheidsconversies](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Eenheden](mapping-reference.md#219) | uoms
[Eenheidsomrekeningen](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Initiële synchronisatie van eenheden bij gegevensafstemming tussen Finance and Operations en Dataverse

### <a name="initial-synchronization-of-units"></a>Initiële synchronisatie van eenheden

Als twee keer wegschrijven is ingeschakeld, worden eenheden uit Finance and Operations-apps gesynchroniseerd met andere Dynamics 365-apps. De eenhedengroepen die vanuit Finance and Operations-apps worden gesynchroniseerd in Dataverse hebben een markering ingesteld die aangeeft dat deze extern worden onderhouden.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Overeenkomende eenheden en gegevens uit eenheidsklassen/groepen uit Finance and Operations en andere Dynamics 365-apps

Allereerst is het belangrijk te weten dat de integratiesleutel voor eenheid msdyn_symbol is. Daarom moet deze waarde uniek zijn in Dataverse of andere Dynamics 365-apps. Omdat in andere Dynamics 365-apps via de combinatie van Eenhedengroep-id en Naam de uniekheid van een eenheid wordt gedefinieerd, moet u rekening houden met verschillende scenario's voor het afstemmen van eenheidsgegevens tussen Finance and Operations-apps en Dataverse.

Voor eenheden die overeenkomen met of overlappen in Finance and Operations-apps en andere Dynamics 365-apps:

+ **De eenheid behoort tot een eenhedengroep in andere Dynamics 365-apps die overeenkomt met de bijbehorende eenheidsklasse in Finance and Operations-apps**. In dit geval moet de kolom msdyn_symbol in andere Dynamics 365-apps worden ingevuld met het eenheidssymbool uit Finance and Operations-apps. Dus wanneer de gegevens worden afgestemd, wordt de eenhedengroep ingesteld op Extern onderhouden in andere Dynamics 365-apps.
+ **De eenheid behoort tot een eenhedengroep in andere Dynamics 365-apps die niet overeenkomen met de bijbehorende eenheidsklasse in Finance and Operations-apps (geen bestaande eenheidsklasse in Finance and Operations-apps voor de eenheidsklasse in andere Dynamics 365-apps).** In dit geval moet een willekeurige tekenreeks worden ingevuld bij msdyn_symbol. Let op: deze waarde moet uniek zijn in andere Dynamics 365-apps.

Voor eenheden en eenheidsklassen in Finance and Operations-apps die niet bestaan in andere Dynamics 365-apps:

Als onderdeel van het twee keer wegschrijven worden de eenhedengroepen uit Finance and Operations-apps en de bijbehorende eenheden gemaakt en gesynchroniseerd in andere Dynamics 365-apps en Dataverse, en wordt de eenhedengroep ingesteld op Extern onderhouden. Er is geen extra inspanning voor bootstrapping vereist.

Voor eenheden in andere Dynamics 365-apps die niet bestaan in Finance and Operations-apps:

De kolom msdyn_symbol moet worden ingevuld voor alle eenheden. De eenheden kunnen altijd worden gemaakt in Finance and Operations-apps in de bijbehorende eenheidsklasse (indien aanwezig). Als de eenheidsklasse niet bestaat, moet deze eerst worden gemaakt (houd er rekening mee dat u geen eenheidsklasse kunt maken in Finance and Operations-apps behalve via uitbreiding als u de enum uitbreidt) die overeenkomt met de andere eenhedengroep voor Dynamics 365-apps. U kunt vervolgens de eenheid maken. Houd er rekening mee dat het eenheidssymbool in Finance and Operations-apps het msdyn_symbol moet zijn dat eerder is opgegeven in andere Dynamics 365-apps voor de eenheid.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Productbeleid: dimensie-, tracerings- en opslaggroepen

Het productbeleid is een set beleidsregels die wordt gebruikt voor het definiëren van producten en de bijbehorende kenmerken in voorraad. De productdimensiegroep, producttraceringsdimensiegroep en opslagdimensiegroep kunnen deel uitmaken van het productbeleid.

Finance and Operations-apps | Customer Engagement-apps |
---|---
[Productdimensiegroepen](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Opslagdimensiegroepen](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Traceringsdimensiegroepen](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Producthiërarchieën

Finance and Operations-apps | Customer Engagement-apps |
---|---
[Toewijzingen van productcategorieën](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Hiërarchieën van productcategorieën](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Hiërarchierollen van productcategorieën](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Integratiesleutel voor producten

Voor unieke identificatie van producten tussen Dynamics 365 for Finance and Operations en producten in Dataverse worden de integratiesleutels gebruikt.
Voor producten is **(productnumber)** de unieke sleutel waarmee een product wordt geïdentificeerd in Dataverse. Het wordt samengesteld door samenvoeging van: **(company, msdyn_productnumber)**. Met **company** wordt de rechtspersoon in Finance and Operations aangegeven en met **msdyn_productnumber** wordt het productnummer aangegeven voor het specifieke product in Finance and Operations.

Voor gebruikers van andere Dynamics 365-apps wordt het product in de gebruikersinterface geïdentificeerd met **msdyn_productnumber** (het label van de kolom is **Productnummer**). In het productformulier worden zowel het bedrijf als msydn_productnumber weergegeven. De kolom (productNumber), de unieke sleutel voor een product, wordt echter niet weergegeven.

Als u apps bouwt op Dataverse, moet u aandacht besteden aan het gebruik van **productnumber** (de unieke product-id) als integratiesleutel. Maak geen gebruik van **msdyn_productnumber**, omdat dit niet uniek is.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Initiële synchronisatie van producten en migratie van gegevens van Dataverse naar Finance and Operations

### <a name="initial-synchronization-of-products"></a>Initiële synchronisatie van producten

Als twee keer wegschrijven is ingeschakeld, worden producten uit Finance and Operations-apps gesynchroniseerd met Dataverse en andere Customer Engagement-apps. Producten die zijn gemaakt in Dataverse en andere Dynamics 365-apps voordat twee keer wegschrijven werd vrijgegeven, worden niet bijgewerkt of komen niet overeen met productgegevens uit Finance and Operations-apps.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Overeenkomende productgegevens uit Finance and Operations en andere Dynamics 365-apps

Als dezelfde producten worden bewaard (overlappend/overeenkomend) in Finance and Operations en in Dataverse en andere Dynamics 365-apps, wordt bij het inschakelen van twee keer wegschrijven de synchronisatie van producten vanuit Finance and Operations uitgevoerd en worden dubbele rijen weergegeven in Dataverse voor hetzelfde product.
Als andere Dynamics 365-apps producten hebben die overlappen/overeenkomen met Finance and Operations kan de vorige situatie worden vermeden als de beheerder die twee keer wegschrijven inschakelt bootstrapping uitvoert voor de kolommen **Bedrijf** (voorbeeld: 'USMF') en **msdyn_productnumber** (voorbeeld: '1234:Black:S') voordat de synchronisatie van producten plaatsvindt. Met andere woorden: deze twee kolommen in het product in Dataverse moeten worden ingevuld met het desbetreffende bedrijf in Finance and Operations waarmee het product moet worden afgestemd en met het bijbehorende productnummer.

Wanneer de synchronisatie is ingeschakeld en wordt uitgevoerd, worden de producten van Finance and Operations vervolgens gesynchroniseerd met de overeenkomende producten in Dataverse en andere Dynamics 365-apps. Dit geld voor zowel verschillende producten als productvarianten.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Migratie van productgegevens vanuit andere Dynamics 365-apps naar Finance and Operations

Als andere Dynamics 365-apps producten hebben die niet aanwezig zijn in Finance and Operations, kan de beheerder eerst **EcoResReleasedProductCreationV2Entity** gebruiken voor het importeren van die producten in Finance and Operations. Vervolgens kunnen de productgegevens uit Finance and Operations en andere Dynamics 365-apps dan worden afgestemd zoals hierboven beschreven.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

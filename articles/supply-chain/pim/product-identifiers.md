---
title: Product-id's
description: Dit onderwerp bevat informatie over de verschillende typen product-id's en hierin wordt uitgelegd hoe u product-id's in de productgegevens kunt toevoegen.
auhor: cvocph
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductEntityIdentifierCode
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: conradv
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: afd542a652abdf6e45c83a6097dc8f0d36efa905
ms.contentlocale: nl-nl
ms.lasthandoff: 03/23/2018

---

# <a name="product-identifiers"></a>Product-id's 

[!INCLUDE [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over de verschillende typen product-id's en hierin wordt uitgelegd hoe u product-id's in de productgegevens kunt toevoegen.

Wanneer u op de werkvloer met producten of in een magazijn in Microsoft Dynamics ERP of Microsoft Dynamics CRM werkt, moet u een goede strategie voor het identificeren van die producten en productvarianten hebben.

## <a name="unique-product-numberproduct-id"></a>Uniek productnummer of unieke product-id

In Microsoft Dynamics 365 for Finance and Operations is de primaire id voor een product het productnummer (de unieke product-id). Het nummer kan automatisch worden gegenereerd op basis van een nummerreeks of handmatig worden gekoppeld aan een product. Voor productvarianten kunnen de nummers worden gedefinieerd via de sjabloon voor de nomenclatuur van producten.

In veel gevallen is het productnummer oorspronkelijk niet gemaakt in Finance and Operations. In plaats daarvan is het gekoppeld aan een product in een systeem voor productlevenscyclusbeheer (PLM) of productgegevensbeheer (PDM). In dit geval kunt u gegevensentiteiten gebruiken om de producten en productvarianten te importeren. Finance and Operations gebruikt de nummers vervolgens voor alle bewerkingen.

Wanneer u Finance and Operations implementeert, moet u extra aandacht aan uw strategie voor productnummers besteden. Een goed nummeringssysteem verbetert de logistieke stromen en kan fouten helpen voorkomen. Een goede product-id bestaat uit maximaal 15 tekens. In het ideale geval bestaat de id uit minder dan 10 tekens en bevat deze niet meer dan vijf classificerende tekens. U kunt ook zoeknamen gebruiken om snelle zoekacties mogelijk te maken. Een zoeknaam is een extra naam die de classificaties van een product vertegenwoordigt.

Wanneer u CDS (Common Data Service) gebruikt, is het productnummer in Finance and Operations ook het productnummer in CDS. Productvarianten worden als aparte producten naar CDS gesynchroniseerd.

## <a name="item-number-and-product-dimensions"></a>Artikelnummer en productdimensies

Het artikelnummer is de product-id die wordt gebruikt door een bepaalde rechtspersoon. In het ideale geval is het artikelnummer gelijk aan het productnummer. Als de nomenclatuur per rechtspersoon afwijkt, wordt het moeilijk om een product in de toeleveringsketen te volgen en worden er belastende extra processen voor opnieuw labelen en verwijzen geïntroduceerd. Voor de comptabiliteit met oudere versies (met Microsoft Dynamics AX 2009 en eerder) hebben we dit model behouden. We raden u echter aan waar mogelijk specifieke id's voor rechtspersonen te verwijderen en in plaats daarvan het unieke productnummer als primaire id te gebruiken.

Bovendien kan een productvariant niet uniek worden geïdentificeerd op basis van een artikelnummer. Hiervoor is altijd de combinatie van een artikelnummer en alle gedefinieerde productdimensies in het productmodel nodig. Deze vereiste kan omslachtig worden en het identificatieproces vertragen. Ook daarom raden we u aan waar mogelijk het unieke productnummer te gebruiken in plaats van het artikelnummer.

Veel pagina's hebben nog het artikelnummer en de productdimensies als de primaire id's. De productnummers kunnen echter worden gebruikt voor zoekopdrachten. Via **Verkoopbeheer en marketing** &gt; **Instellingen** &gt; **Zoeken** &gt; **Zoekparameters** kunt u de zoekopdracht zo wijzigen dat er als primaire zoekstrategie productnummers worden gebruikt in plaats van artikelnummers. Als u de optie **Zoekveld inschakelen om producten te zoeken** instelt op **Ja**, worden in de zoekresultaten niet alleen productmodellen, maar ook productvarianten weergegeven. Zie [Producten en productvarianten zoeken tijdens orderinvoer](search-products-product-variants.md) voor meer informatie.

Daarnaast kunt u ook zoeken en filteren op het productnummer, de productnaam en -omschrijving, en de productdimensie-id's van de productvariant. Als u een variant selecteert, worden het bijbehorende artikelnummer en alle productdimensie-id's geselecteerd. Daarom kunt u de juiste variant gemakkelijker vinden en selecteren. Deze instelling wordt sterk aangeraden als u productvarianten en het unieke productnummer als de primaire id's voor producten gebruikt. De enige uitzondering is mogelijk de mode-industrie, waar de bedrijfsprocessen vaak vereisen dat u het productmodel selecteert voordat u een variant selecteert. U moet deze optie zorgvuldig evalueren voordat u het nummeringssysteem implementeert.

## <a name="product-name-and-description"></a>Productnaam en -omschrijving

De productnaam en -omschrijving zijn de voor mensen leesbare id's van een product en kunnen in veel talen worden beheerd. Standaard worden in de Finance and Operations-client alle productgegevens in de standaardtaal van het bedrijf weergegeven, niet in de taal van de gebruiker. Vertaalde productnamen en -omschrijvingen worden echter gebruikt in alle communicatie met klanten en leveranciers. De vertalingen zijn gebaseerd op de taalcode van de klant- en leveranciersrekeningen.

Voor productvarianten kan de productnaam worden gegenereerd via een sjabloon voor de nomenclatuur van producten. Omdat productnamen niet uniek hoeven te zijn, kunt u meerdere producten met dezelfde naam vinden.

## <a name="product-and-item-search-names"></a>Zoeknamen voor producten en artikelen

Finance and Operations biedt een secundaire zoeknaam voor producten en artikelen (vrijgegeven producten). Deze zoeknaam hoeft niet uniek te zijn en kan worden gewijzigd nadat een product- of productvariant is gemaakt. U wordt aangeraden de zoeknaam te gebruiken om te zoeken naar producten per categorie. Op basis van de zoeknamen kunt u snel zoeken, vooral in verkoop- en inkoopprocessen.

De zoeknaam kan ook een klant- of leveranciersproduct-id of een andere externe product-id bevatten als deze externe id het primaire zoekcriterium voor een product is.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Externe product-id's (klant- en leveranciers-id's)

Voor vrijgegeven producten kunt u de artikelnummers, -namen en -omschrijvingen die de klant of leverancier gebruikt, behouden. Deze worden ook gebruikt in externe documenten, zoals verkooporders, inkooporders, pakbonnen en facturen. In de huidige versie van Finance and Operations worden deze externe verwijzingen niet weergegeven op pagina's voor kernoperaties. Het leveranciersartikelnummer is de enige uitzondering. Dit nummer wordt weergegeven in het dialoogvenster **Productgegevens** als een standaardleverancier is gedefinieerd voor het vrijgegeven product.

U kunt de externe product-id's op vrijgegeven product, vrijgegeven productvariant, klant of klantengroep, of leverancier of leveranciersgroep beheren.

Voer een van de volgende stappen uit op de pagina **Vrijgegeven producten**.

- Selecteer voor klanten op het tabblad **Verkopen** in de groep **Gerelateerde informatie** de optie **Extern-artikelomschrijving**.
- Selecteer voor leveranciers op het tabblad **Inkoop** in de groep **Gerelateerde informatie** de optie **Extern-artikelomschrijving**.

Op de pagina **Extern-artikelomschrijvingen** kunt u het artikelnummer van de klant of leverancier aan een vrijgegeven product koppelen. Deze koppeling moet worden uitgevoerd voor elke rechtspersoon. U kunt de volgende gegevens vastleggen. Helaas zijn de labels enigszins misleidend in de huidige versie van Finance and Operations. Deze labels worden mogelijk gewijzigd in een toekomstige versie.

| Veld | Bijbehorende klantgegevens | Bijbehorende leveranciersgegevens |
|-------|------------------------------------|----------------------------------|
| Nummer van extern artikel | Het artikelnummer van de klant | Het artikelnummer van de leverancier |
| Omschrijving | De naam die de klant aan het artikel koppelt | De naam die de leverancier aan het artikel koppelt |
| Tekst extern artikel | De artikelomschrijving van de klant | De artikelomschrijving van de leverancier |

Als veel klanten of leveranciers hetzelfde artikelnummer gebruiken (zoals in het geval van een inkopersvereniging of een detailhandelgroep), kunt u groepen klanten of leveranciers maken om het beheer van externe productgegevens te vereenvoudigen.

- Voor klantengroepen gaat u naar **Verkoop** &gt; **Instellingen** &gt; **Artikelen** &gt; **Extern-artikelomschrijving** om de groepen en de bijbehorende artikelnummers te maken en te beheren. Als u klanten wilt koppelen aan een groep, gaat u naar **Klanten** &gt; **Klanten** &gt; **Alle klanten** en geeft u op het sneltabblad **Standaardwaarden verkooporders** een waarde op in het veld **Artikel - klantengroep**.
- Voor leveranciersgroepen gaat u naar **Inkoop en sourcing** &gt; **Instellingen** &gt; **Groep extern-artikelomschrijvingen** om de groepen en de bijbehorende artikelnummers te maken en te beheren. Als u leveranciers wilt koppelen aan een groep, gaat u naar **Crediteuren** &gt; **Leveranciers** &gt; **Alle leveranciers** en geeft u op het sneltabblad **Details over inkooporders** een waarde op in het veld **Artikel - Leveranciersgroep**.
 
## <a name="bar-codes"></a>Streepjescodes

Als u een streepjescodescanner wilt gebruiken ter identificatie van producten, moet u voldoen aan de vereisten van de streepjescodescanner die wordt gebruikt. Daarom bevatten streepjescodes doorgaans niet het onbewerkte productnummer, maar een nummer dat specifiek voor de geselecteerde streepjescodetechnologie wordt gegenereerd. U kunt meerdere streepjescodes op streepjescodetype beheren. U kunt zelfs dezelfde streepjescode koppelen aan meerdere producten en vervolgens de werkelijke koppeling selecteren wanneer u een streepjescode scant.

Voordat u streepjescodes definieert, kunt u een of meer streepjescode-instellingen definiëren. Met de streepjescode-instellingen kunt u valideren dat streepjescodes de vereiste richtlijnen volgen en dat ze daarom effectief afgedrukt en gescand kunnen worden. U kunt ook speciale streepjescodes voor bepaalde producthoeveelheden gebruiken.

Wij raden u aan de streepjescode-instellingen te gebruiken om GTIN- (Global Trade Item Number) of EAN-codes (International Article Number) te beheren.

U beheert streepjescodes door op de pagina **Vrijgegeven producten** op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **Streepjescodes** te selecteren.

## <a name="gtin-codes"></a>GTIN-codes

In e-commerce is het van groot belang dat alle partijen een gemeenschappelijke taal spreken en naar producten verwijzen met een gemeenschappelijke set id's. Daarom maken sommige bedrijfstakken gebruik van [GTIN](https://www.gs1.org/id-keys/gtin), een wereldwijd systeem voor artikelnummering dat mogelijk wordt gemaakt door GS1.

In Finance and Operations kunt u GTIN het beste beheren als streepjescode. U kunt GTIN echter ook gebruiken op de pagina **Artikel - GTIN**. U opent deze pagina door op de pagina **Vrijgegeven producten** op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **GTIN-codes** te selecteren. Houd er rekening mee dat GTIN niet als een globaal nummer wordt beheerd. In plaats daarvan wordt het beheerd per rechtspersoon.

In Finance and Operations definieert u verpakkingsvarianten in de magazijnbewerkingen door specifieke maateenheden op te geven. Een artikel kan bijvoorbeeld zijn opgeslagen in stuks, in bundels van zes, in laden van 18 of in volle pallets. Er wordt een bepaalde maateenheid gedefinieerd voor elk van deze verpakkingsvarianten. Aangezien GTIN doorgaans is gerelateerd aan de verpakkingseenheid van een product, kunt u op de pagina **Artikel - GTIN** meerdere GTIN-codes per product en maateenheid beheren. U kunt dezelfde GTIN-code echter niet vaker dan één keer voor verschillende artikelen of varianten van het product van een rechtspersoon gebruiken.

U beheert **GTIN-codes** door op de pagina **Vrijgegeven producten** op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **GTIN** te selecteren.

## <a name="external-codes"></a>Externe codes

In Finance and Operations kunnen voor veel entiteiten externe codes worden gedefinieerd. Zo kunt u externe codes definiëren om producten en vrijgegeven producten te identificeren. Deze externe codes kunnen worden gebruikt om statistische of btw-codes aan vrijgegeven producten en vrijgegeven productvarianten te koppelen. Externe codes worden gedefinieerd op basis van rechtspersoon en het codetype. Ze moeten uniek zijn voor elke rechtspersoon, elk codetype en elke tabelverwijzing.

Helaas is er geen standaardfunctionaliteit waarmee u op externe codes kunt zoeken naar producten.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Gegevensentiteiten die worden gebruikt om product-id's te importeren en exporteren

| Naam entiteit | Id's importeren | Id's exporteren | Opmerkingen |
|-------------|--------------------|--------------------|----------|
| Producten V2 | Productnummer, zoeknaam voor product, productnaam, productomschrijving | Productnummer, zoeknaam voor product, productnaam, productomschrijving | Afhankelijk van de instellingen van de entiteit en de nummerreeks voor het productnummer, kan het productnummer automatisch worden gemaakt op het moment van importeren. |
| Productvarianten | Productnummer, zoeknaam voor product, productnaam, productomschrijving | Productnummer, zoeknaam voor product, productnaam, productomschrijving | Afhankelijk van de sjabloon voor de nomenclatuur van producten, kan het productnummer automatisch worden gemaakt op het moment van importeren. U kunt echter elk uniek productnummer importeren en dat productnummer hoeft niet de structuur van de sjablonen voor de nomenclatuur van producten te volgen. |
| Productvertalingen | Productnaam, productomschrijving | Productnaam, productomschrijving | Deze entiteit overschrijft elke taal. Wanneer de naam of omschrijving van de primaire taal voor een rechtspersoon wordt overschreven, worden de naam en omschrijving van het product zelf gewijzigd. |
| Vrijgegeven producten V2 | Artikelnummer, productnummer, zoeknaam artikel| Artikelnummer, productnummer, zoeknaam artikel, zoeknaam voor product, productnaam | Deze entiteit kan lastig zijn als nummerreeksen worden gebruikt tijdens het maken van nieuwe vrijgegeven producten. Zowel de nummerreeks **Artikelnummer** als de nummerreeks **Productnummer** heeft invloed. De nummerreeks **Artikelnummer** geldt per rechtspersoon terwijl de nummerreeks **Productnummer** globaal geldt. Daarom raden we u niet aan de nummerreeks **Artikelnummer** te gebruiken wanneer u nieuwe vrijgegeven producten implementeert. Wanneer de entiteit wordt gebruikt voor het vrijgeven van een bestaand product, moet het productnummer vanzelfsprekend wel worden vermeld in de entiteit. Zie de sectie Product- en artikelnummerreeksen in dit onderwerp voor meer informatie. |
| Vrijgegeven productvarianten | Artikelnummer, productdimensies, productnummer | Productnummer, zoeknaam voor product, productnaam, productomschrijving, productdimensies | Net als de entiteit **Productvarianten** kan deze entiteit worden gebruikt voor het maken van nieuwe producten die de sjabloon voor de nomenclatuur van producten volgen of hun eigen productnummers voor de variant gebruiken. |
| Extern-artikelomschrijving voor klanten | Artikelnummer van klant, naam van klantartikel, klantomschrijving, klantrekening | Artikelnummer van klant, naam van klantartikel, klantomschrijving, klantrekening | Een groep klanten (bijvoorbeeld een kopersvereniging) kan worden samengevoegd tot één groep met behulp van de entiteit **Klantengroepen voor extern-artikelomschrijving**. |
| Extern-artikelomschrijving voor leveranciers | Artikelnummer van leverancier, naam van leveranciersartikel, omschrijving van leverancier, leverancierrekening | Artikelnummer van leverancier, naam van leveranciersartikel, omschrijving van leverancier, leverancierrekening | Een groep leveranciers (bijvoorbeeld een leveranciersvereniging of een brancheorganisatie) kan worden samengevoegd tot één groep met behulp van de entiteit **Leveranciersgroepen voor extern-artikelomschrijving**. |
| Artikelstreepjescode | Streepjescode | Streepjescode | Tijdens het importeren moet u verwijzen naar streepjescode-instellingen die zijn gedefinieerd in het doelsysteem. De verwijzingen voor de geïmporteerde streepjescode worden gevalideerd op basis van die streepjescode-instellingen en worden geweigerd als de streepjescodes niet aan de vereisten voldoen die in de streepjescode-instellingen zijn gedefinieerd. |
| Externe codes voor vrijgegeven producten | Externe code | Externe code, externe codeklassen, artikelnummer | Externe codes gelden per rechtspersoon. Voor het importeren moet u verwijzen naar een gedefinieerde codeklasse. Importeer de codeklassen met behulp van de entiteit **Externe codeklassen voor vrijgegeven producten**. |
| Externe codes voor vrijgegeven productvarianten | Externe code | Externe code, externe codeklassen, artikelnummer, productdimensies | Externe codes gelden per rechtspersoon. Voor het importeren moet u verwijzen naar een gedefinieerde codeklasse. Importeer de codeklassen met behulp van de entiteit **Externe codeklassen voor vrijgegeven producten**. Deze entiteit verwijst naar productvarianten op basis van het artikelnummer en productdimensies. |
| Externe codes voor vrijgegeven productvarianten per productnummer-id | Externe code | Externe code, externe codeklassen, productnummer | Externe codes gelden per rechtspersoon. Voor het importeren moet u verwijzen naar een gedefinieerde codeklasse. Importeer de codeklassen met behulp van de entiteit **Externe codeklassen voor vrijgegeven producten**. Deze entiteit verwijst naar productvarianten op basis van het productnummer van de variant. (Uit de volgende grote release) |
| GTIN | Niet van toepassing | Niet van toepassing | Er is momenteel geen specifieke entiteit die wordt gebruikt om GTIN-codes te importeren en te exporteren. Wij raden u aan in plaats daarvan de entiteit **Artikelstreepjescode** te gebruiken. |
| Entiteit voor Common Data Service-id voor productentiteit | Niet van toepassing | Artikelnummer, zoeknaam artikel, zoeknaam voor product, leveranciersartikelnummer, klantartikelnummer, externe codes, GTIN-codes, streepjescodes | Met deze entiteit worden alle id's geconsolideerd in één gegevensmodel, zodat één interface kan worden gebruikt om alle id's en hun bijbehorende typen eenvoudig te exporteren. Gebruik de entiteit **Identificatiecodes voor productentiteiten** voor het exporteren van de id-codes en omschrijvingen. Gebruik de entiteit **Identificatiebereik voor productentiteiten** om aanvullende bereikgegevens naar een id te exporteren, zoals de partij, rechtspersoon, hoeveelheid of eenheid. |

### <a name="product-and-item-number-sequences"></a>Product- en artikelnummerreeksen

In Finance and Operations kunt u twee verschillende nummerreeksen definiëren:

- De nummerreeks **Productnummer** voor het globale productnummer
- De nummerreeks **Artikelnummer** voor het artikelnummer per rechtspersoon

> [!NOTE]
> Alleen als u verschillende rechtspersonen uit verschillende bronnen met verschillende nummeringssystemen migreert, moet u het artikelnummer als een afzonderlijke id gebruiken. U moet altijd proberen een product-id te gebruiken die uniek is voor alle rechtspersonen. U moet daarom de optie **Handmatig** op **Ja** instellen voor de nummerreeks **Artikelnummer**. Op deze manier volgt het artikelnummer het productnummer wanneer het wordt gemaakt. Als Finance and Operations niet uw hoofdsysteem is voor nieuwe productnummers, stelt u de optie **Handmatig** in op **Ja** voor de nummerreeksen **Artikelnummer** en **Productnummer**.

Als u werkt met de entiteit **Vrijgegeven product V2** voor het maken van producten, kunnen meerdere instellingen invloed hebben op hoe de nummerreeksen worden gebruikt voor het maken van het productnummer en artikelnummer:

- Instellingen van de nummerreeks **Productnummer**
- Instellingen van de nummerreeks **Artikelnummer**
- De toewijzing van het artikelnummer 
- De toewijzing van het productnummer

De volgende tabel biedt een overzicht van de resultaten van het importeren en handmatig maken bij specifieke combinaties van de instellingen voor nummerreeksen en veldtoewijzing.

| Nummerreeks Productnummer | Nummerreeks Artikelnummer | Toewijzing van het artikelnummer | Toewijzing van het productnummer | Resultaat van entiteitsimport | Resultaat van handmatig maken | Conclusie |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Handmatig = Nee | Handmatig = Nee | Geen toewijzing | Geen toewijzing | Productnummers gebruiken de nummerreeks **Productnummer**. Artikelnummers gebruiken de nummerreeks **Artikelnummer**. | Productnummers gebruiken de nummerreeks **Productnummer**. Artikelnummers gebruiken de nummerreeks **Artikelnummer**. | Deze instellingen kunnen worden gebruikt als u een ander nummer nodig hebt voor producten en artikelen. We raden u echter niet aan verschillende nummers te gebruiken voor artikelen en producten. |
| Handmatig = Nee | Handmatig = Ja | Automatisch genereren | Geen toewijzing | Zowel productnummers als artikelnummers gebruiken de nummerreeks **Artikelnummer**. | Zowel productnummers als artikelnummers gebruiken de nummerreeks **Productnummer**. | Deze instellingen worden niet aanbevolen. Importeren en handmatig maken werken verschillend. |
| Handmatig = Nee | Handmatig = Ja | Geen toewijzing | Geen toewijzing | Zowel productnummers als artikelnummers gebruiken de nummerreeks **Productnummer**. | Zowel productnummers als artikelnummers gebruiken de nummerreeks **Productnummer**. | Deze instellingen worden aanbevolen als producten een consistente automatische nummering moeten hebben, ongeacht of importeren of handmatig maken is gebruikt. |
| Handmatig = Ja | Niet van toepassing | Niet van toepassing | Automatisch genereren | U ontvangt het foutbericht Nummerreeks kan niet worden gevonden. | Op basis van de nummerreeks **Artikelnummer** | Deze instelling wordt niet ondersteund voor importeren. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Productentiteit-id (alle product-id's exporteren)

Het model voor productentiteit-id's is gemaakt om versie 1.0 van CDS te kunnen inrichten met alle id's die worden gebruikt om te verwijzen naar een product. Om deze taak te vereenvoudigen, worden alle id's samengevoegd in één algemene id-tabel, zodat ze kunnen worden geëxporteerd als één model. Houd er rekening mee dat deze versie van CDS het model voor product-id's niet gebruikt. Daarom hebben de entiteit **Entiteit voor Common Data Service-id voor productentiteit** en dit proces een beperkt praktisch nut en worden deze waarschijnlijk gewijzigd in de toekomst.

De tabel met product-id's is een globale tabel die wordt gevuld op basis van alle verwijzingstabellen van de hoofdrechtspersoon via een terugkerende batchtaak. U moet een rechtspersoon en een productcategoriehiërarchie selecteren als de definitie van het bereik van het globale productmodel. Er wordt alleen een globale tabel met product-id's gegenereerd voor producten die voor de geselecteerde rechtspersoon zijn vrijgegeven en producten die deel uitmaken van de producthiërarchie die is geselecteerd voor de rol **Common Data Service** in de productcategoriehiërarchie.

Hierbij wordt ervan uitgegaan dat producthoofdgegevens voornamelijk worden beheerd in één centrale rechtspersoon. (Deze rechtspersoon kan echter wel een virtuele rechtspersoon zijn die alleen wordt gebruikt voor het beheer van globale hoofdgegevens.)

Ga als volgt te werk om de omgeving te configureren.

1. Selecteer de categoriehiërarchie voor CDS. Als op de pagina **Rolkoppelingen categoriehiërarchie** geen hiërarchie is gekoppeld aan de rol **Common Data Service**, moet u een nieuwe koppeling maken. Selecteer de rol **Common Data Service** en koppel vervolgens de categoriehiërarchie die staat voor het productaanbod dat moet worden gesynchroniseerd naar CDS.
2. Selecteer de rechtspersoon voor globale producthoofdgegevens. Selecteer op de pagina **Parameters productgegevensbeheer** op het tabblad **Productkenmerken** het hoofdbedrijf waar de product- en artikel-id's voornamelijk worden beheerd.
3. Definieer de id-codetypen en -codes die moeten worden geëxporteerd. Ga naar **Productgegevensbeheer** &gt; **Instellingen** &gt; **Identificatiecodes voor producten**. Selecteer **Codes genereren** om de typen id-codes te genereren. Een codetypevermelding wordt gegenereerd voor elk type id dat wordt gevonden in de geselecteerde rechtspersoon.

    Voor streepjescodes wordt een codetype gegenereerd voor elke streepjescode-instelling. Voor externe codes wordt een codetype gegenereerd voor elke externe codeklasse.

    U kunt nu de lijst met codetypen beheren. U kunt de code, naam en omschrijving wijzigen. Ook kunt u codetypen verwijderen. Codetypen die u verwijdert, worden niet gebruikt voor het vullen van de globale tabellen met productentiteit-id's.

4. Wanneer u klaar bent met het definiëren van de codetypen voor product-id's, kunt u de id's in de globale tabel maken door de taak **Id's voor productentiteiten maken** op de pagina **Identificatiecodes voor productentiteiten** te starten. U moet deze taak uitvoeren in een batch. Deze taak moet worden ingesteld als een periodieke batchtaak, zodat de tabel wordt gevuld op basis van nieuwe gegevens.

Nu kunt u de gegevensentiteiten **Entiteit voor Common Data Service-id voor productentiteit**, **Record-id voor identificatiecode voor productentiteit** en **Identificatiebereik voor productentiteiten** gebruiken voor het exporteren van de id's voor elk doelsysteem.

## <a name="related-topic"></a>Verwant onderwerp

[Producten en productvarianten zoeken tijdens orderinvoer](search-products-product-variants.md)

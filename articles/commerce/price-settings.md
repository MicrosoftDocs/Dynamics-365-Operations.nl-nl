---
title: Instellingen voor prijzen
description: In dit artikel worden de verschillende instellingen voor prijs- en kortingsbeheer in Microsoft Dynamics 365 Commerce Headquarters beschreven.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 79130e0ef285d6bd5e544f2d6a6368c0393fa7fa
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474037"
---
# <a name="pricing-settings"></a>Instellingen voor prijzen

[!include [banner](../includes/banner.md)]

In dit artikel worden de verschillende instellingen voor prijs- en kortingsbeheer in Microsoft Dynamics 365 Commerce Headquarters beschreven. Met deze instellingen kunnen organisaties het prijsgedrag in hun Commerce-oplossing definiëren om aan specifieke bedrijfsbehoeften te voldoen.

## <a name="company-level-pricing-settings"></a>Prijsinstellingen op bedrijfsniveau

De meeste prijsinstellingen bevinden zich op bedrijfsniveau bij **Commerce-parameters \> Prijzen en kortingen** in Commerce Headquarters.

### <a name="best-price-and-compound-concurrency-control-model"></a>Model voor beste prijs en samengestelde gelijktijdigheidsregeling

Met de instelling **Model voor beste prijs en samengestelde gelijktijdigheidsregeling** wordt bepaald hoe meerdere kortingen worden verwerkt in de modus voor de **beste prijs** of **samengestelde** gelijktijdigheidsmodus. 

Als de parameter is ingesteld op **Beste prijs en samengestelde korting binnen prioriteit; nooit samengestelde korting tussen prioriteiten**, worden alle **samengestelde** kortingen met dezelfde prijsprioriteit samengesteld. Het samengestelde resultaat concurreert vervolgens met alle **beste prijskortingen** met dezelfde prijsprioriteit, de beste prijs wordt toegepast en alle kortingen met een lagere prijsprioriteit worden genegeerd.

Als de parameter is ingesteld op **Beste prijs alleen binnen prioriteit, altijd samengesteld over prioriteiten**, worden alle **samengestelde** kortingen behandeld als **beste prijskortingen**. Binnen een prijsprioriteit kan slechts één korting winnen. Als die ene korting een **beste prijs** of **samengestelde** korting is, wordt deze samengesteld met alle aanvullende **beste prijzen** of **samengestelde** kortingen met een lagere prijsprioriteit.

### <a name="discount-compound-behavior"></a>Gedrag samengestelde korting

Met de instelling **Gedrag samengestelde korting** wordt bepaald hoe meerdere samengestelde kortingen worden berekend door de prijsbepalingsenengine.

Als de parameter wordt ingesteld op **Samengesteld**, wordt één korting op een cumulatieve manier boven op de andere toegepast. Als de korting is ingesteld op **Samengesteld op basis van de oorspronkelijke prijs**, worden alle kortingen onafhankelijk van elkaar behandeld en op dezelfde oorspronkelijke prijs toegepast.

U wilt bijvoorbeeld een samengestelde korting van 10 procent of 20 procent wilt voor een product met een oorspronkelijke prijs van $100. Als u de parameter **Gedrag samengestelde korting** op **Samengesteld** instelt, wordt de uiteindelijke prijs $72 ($ 100 &times; 90% &times; 80%). Als u dit instelt op **Samengesteld op basis van de oorspronkelijke prijs**, wordt de uiteindelijke prijs $70 ($ 100 - 10% - 20%).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Competitie inschakelen tussen exclusieve drempelwaarde en andere periodieke kortingen

Als de parameter **Competitie inschakelen tussen exclusieve drempelwaarde en andere periodieke kortingen** is ingesteld op **Ja**, zorgt de prijsengine ervoor dat exclusieve drempelkortingen concurreren met exclusieve niet-drempelkortingen. Prijsprioriteit blijft van toepassing. Het gedrag van drempelkortingen voor **beste prijs** en **samengesteld** blijft hetzelfde. Met andere woorden, ze concurreren niet met de niet-drempelkortingen.@@

### <a name="manual-line-discount-and-system-discount"></a>Handmatige regelkorting en systeemkorting

Met de instelling **Handmatige regelkorting en systeemkorting** wordt bepaald hoe een handmatige regelkorting en systeemkorting op dezelfde regel worden toegepast door een prijzenengine. De handmatige regelkorting kan boven op de systeemkorting worden gebruikt of kan de systeemkorting vervangen. Wanneer de handmatige regelkorting en systeemkorting worden samengesteld, heeft de berekeningslogica betrekking op de instelling **Gedrag samengestelde korting**. Een handmatige totale korting die van toepassing is op de gehele order heeft geen betrekking op deze instelling.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Artikelen op dezelfde verkoopregel houden voor afronding van kortingsprijs

Soms kan het bedrag van een hoeveelheidskortingsbedrag niet gelijk worden verdeeld door de kwalificerende hoeveelheid (bijvoorbeeld als het kortingsbedrag voor drie ingekochte eenheden $10 is). In deze gevallen bepaalt de instelling **Artikelen op dezelfde verkoopregel houden voor afronding van kortingsprijs** hoe de prijsengine van toepassing is en wordt het kortingsbedrag verdeeld. Als de parameter is ingesteld op **Ja**, wordt het kortingsbedrag als geheel toegepast en wordt het niet gesplitst. Als deze is ingesteld op **Nee**, wordt het kortingsbedrag verdeeld over de kwalificerende hoeveelheid en afgerond. Een kortingsbedrag van bijvoorbeeld een $ 10 voor drie eenheden wordt in $ 3,33 verdeeld voor één eenheid, $ 3,33 voor de tweede eenheid en $ 3,34 voor de derde eenheid.

### <a name="apply-discounts-to-key-in-price-products"></a>Pas kortingen toe op producten met 'ingetoetste prijs'

Met de instelling **Pas kortingen toe op producten met 'ingetoetste prijs'** wordt bepaald of kortingen kunnen worden toegepast samen met 'ingetoetste prijzen' op het POS. De instelling **Prijs intoetsen** in de productconfiguratie bepaalt of en hoe een product de sleutelprijs ondersteunt.

### <a name="apply-discounts-to-price-overrides"></a>Kortingen toepassen op prijsoverschrijvingen

Met de instelling **Kortingen toepassen op prijsoverschrijvingen** wordt bepaald of kortingen samen met prijsoverschrijvingen kunnen worden toegepast.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Kortingen verdelen voor goedkoopste kortingen

Voor combinatiekortingen met het berekeningstype 'minst duur' bepaalt de instelling **Kortingen verdelen voor goedkoopste kortingen** of de korting over regels wordt verdeeld door de prijsengine.

Als de parameter is ingesteld op **Nee**, wordt de korting alleen toegepast op de goedkoopste regels. Voor bijvoorbeeld een combinatiekorting 'bij aankoop van 2, 1 gratis' is het goedkoopste artikel gratis en blijven de andere twee artikelen voor de volledige prijs. In dit geval krijgt een klant die beide artikelen met volledige prijs retourneert, nog steeds het derde artikel gratis. Dit scenario kan leiden tot verlies voor de detailhandelaar.

Als de parameter is ingesteld op **Ja**, wordt de korting door de prijsengine verdeeld over alle toepasselijke regels. Met deze instelling kunt u het verlies op retouren verminderen.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Handmatig meerregelprijzen en -kortingen berekenen

Met de instelling **Handmatig meerregelprijzen en -kortingen berekenen** wordt bepaald of de prijsengine een uitgestelde prijs- en kortingsberekening gebruikt voor de POS-toepassing en het callcenterkanaal. Als de parameter is ingesteld op **Ja**, worden meerregelkortingen (zoals hoeveelheidskortingen, drempelkortingen en combinatiekortingen) niet onmiddellijk berekend door de prijsengine wanneer een verkooporder wordt gemaakt of bewerkt in de POS-toepassing of het kanaal van de callcenter.

> [!NOTE]
> In Commerce versie 10.0.30 en eerder wordt met de instelling **Handmatig meerregelprijzen en -kortingen berekenen** alleen het kanaal van de callcenter berekend. Met de afzonderlijke instelling **Handmatig meerdere artikelkortingen berekenen** in het functionaliteitsprofiel wordt het gedrag van de prijsberekening in de POS-toepassing bepaald. In Commerce versie 10.0.31 worden deze twee instellingen geconsolideerd in één instelling op bedrijfsniveau.

### <a name="retention-period-in-days"></a>Bewaarperiode in dagen

De instelling **Bewaarperiode in dagen** geeft aan hoeveel dagen na de vervaldatum (als een vervaldatum is ingesteld) of de uitschakeldatum (als er geen vervaldatum is ingesteld) een korting systematisch moet worden verwijderd. Als de parameter is ingesteld op **0** (nul), vindt er geen automatische verwijdering plaats.

> [!NOTE]
> In Commerce versie 10.0.30 en eerder heeft deze instelling de naam **Aantal dagen waarna de vervallen kortingen moeten worden verwijderd**.

### <a name="coupon-bar-code"></a>Streepjescode voor coupon

De instelling **Streepjescode voor coupon** bepaalt welke streepjescode wordt gebruikt om streepjescodes voor coupons te genereren. Gebruikers kunnen een van de vooraf gedefinieerde streepjescodes selecteren die zijn geconfigureerd op de pagina **Streepjescode-instellingen**. Zie [Streepjescodes instellen](set-up-bar-codes.md) en [Streepjescodemaskers instellen](set-up-bar-code-masks.md) voor meer informatie over streepjescodes en streepjescodemaskers instellen.

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Couponcode moet handmatig worden toegepast om transacties terug te sturen

De instelling **Couponcode moet handmatig worden toegepast om transacties terug te sturen** is alleen van toepassing op het retourneren van transacties waarin geen verkoopontvangst is opgegeven. Stel de parameter in op **Nee** als couponcodes automatisch moeten worden toegepast op de transactie. Stel dit in op **Ja** als couponcodes handmatig aan de transactie moeten worden toegevoegd.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Verkoopovereenkomsten die zijn ingesteld voor de organisatie gebruiken

Als de parameter **Verkoopovereenkomsten die zijn ingesteld voor de organisatie gebruiken** is ingesteld op **Ja** voor B2B-orders (business-to-business), gebruikt de prijsengine de verkoopovereenkomsten die voor de organisatie in de klanthiërarchie van de gebruiker zijn gedefinieerd, om de contractgebaseerde prijs te bepalen. Als de parameter is ingesteld op **Nee** of als de klanthiërarchie niet is gedefinieerd, zoekt de prijsengine naar verkoopovereenkomsten die voor de gebruiker zijn gedefinieerd om de contractgebaseerde prijs te bepalen. Zie [B2B-zakenpartners beheren via klanthiërarchieën](b2b/partners-customer-hierarchies.md) voor meer informatie over klanthiërarchieën voor B2B en e-commerce.

## <a name="channel-level-pricing-settings"></a>Prijsinstellingen op kanaalniveau

Met de volgende instellingen kunnen organisaties het prijsgedrag in specifieke verkoopkanalen bepalen.

### <a name="enable-order-price-control"></a>Orderprijscontrole inschakelen

De parameter **Orderprijscontrole inschakelen** bevindt zich op het sneltabblad **Algemeen** van de pagina **Callcenterconfiguratie**. Met de instelling wordt bepaald of de prijsengine een beperking afdwingt op de prijsoverschrijvingsbewerking in het kanaal van de callcenter. Dit werkt in combinatie met de instelling **Prijscorrectie toestaan** op productniveau.

Als orderprijscontrole is uitgeschakeld, kan een gebruiker van een callcenter prijswijzigingen aanbrengen op verkoopregels in het callcenterkanaal, ongeacht of de prijscorrectie is toegestaan voor de overeenkomende producten.

Als orderprijscontrole is ingeschakeld, worden alleen producten waarvoor de parameter **Prijscorrectie toestaan** op **Ja** is ingesteld, prijsoverschrijvingen toegestaan in verkooporders van het callcenterkanaal en moet een redencode worden opgegeven op bijbehorende verkoopregels. Een callcentergebruiker kan de verkoopprijs alleen wijzigen tot de waarde van de **Percentage van prijsverhoging** die is gedefinieerd bij **Retail en Commerce \> Afzetkanaalinstellingen \> Instellingen van callcenter \> Machtigingen overschrijven**. Als een prijsoverschrijving dit percentage overschrijdt, moet de gebruiker een aanvraag indienen, die vervolgens wordt verwerkt via een vooraf gedefinieerde Commerce-workflow voor controle en goedkeuring. Zie [Overzicht van werkstroomsysteem](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system) voor meer informatie over het maken van Commerce-werkstromen.

## <a name="product-level-pricing-settings"></a>Prijsinstellingen op productniveau

De volgende instellingen dwingen prijsregels op productniveau af en zijn te vinden op de pagina **Productconfiguratie** van een organisatie.

### <a name="allow-price-adjust"></a>Prijscorrectie toestaan

Als de parameter **Prijscorrectie toestaan** is ingesteld op **Ja**, kan een prijscorrectie worden toegepast op het product in verkooporders voor het callcenterskanaal.

### <a name="key-in-price"></a>Prijs intoetsen

Met de instelling **Prijs intoetsen** wordt bepaald of het intoetsen van een prijs verplicht is wanneer een product wordt toegevoegd aan een verkooptransactie in POS. Daarnaast worden bijbehorende prijswaardebeperkingen gedefinieerd.

### <a name="zero-price-valid"></a>Aanvangsprijs geldig

De instelling **Aanvangsprijs geldig** bepaalt of vooraf gedefinieerde, door het systeem berekende of handmatig gecorrigeerde verkoopprijzen voor een product 0 (nul) kunnen zijn. Stel de parameter in op **Ja** als een prijs van nul is toegestaan. Deze instelling kan ook worden opgegeven op categorieniveau vanuit de handelproducthiërarchie.

### <a name="prevent-all-discounts"></a>Alle kortingen verhinderen

Door de parameter **Alle kortingen verhinderen** op **Ja** in te stellen, kunt u voorkomen dat alle typen kortingen (inclusief handmatige kortingen) op een product worden toegepast. Deze instelling kan ook worden opgegeven op categorieniveau vanuit de handelproducthiërarchie.

> [!NOTE]
> Deze instelling beperkt niet de werking van prijsoverschrijvingen omdat die bewerking de prijs instelt en niet als een korting geldt.

### <a name="prevent-manual-discounts"></a>Handmatige kortingen verhinderen

Door de parameter **Handmatige kortingen verhinderen** op **Ja** in te stellen, kunt u voorkomen dat handmatige regel- of transactiekortingen (inclusief handmatige kortingen) op een product worden toegepast. Alle overige kortingen kunnen nog worden toegepast. Deze instelling kan ook worden opgegeven op categorieniveau vanuit de handelproducthiërarchie.

> [!NOTE]
> Deze instelling beperkt niet de werking van prijsoverschrijvingen omdat die bewerking de prijs instelt en niet als een korting geldt.

### <a name="prevent-retail-discounts"></a>Detailhandelkortingen voorkomen

Als de parameter **Detailhandelkortingen voorkomen** is ingesteld op **Ja**, kunnen de kortingen **eenvoudig**, **hoeveelheid**, **drempel**, **combinatiekorting** en **verzendkorting** niet op een product worden toegepast. Alle overige kortingen (met inbegrip van handmatige kortingen) kunnen nog worden toegepast.

### <a name="prevent-tender-based-discounts"></a>Korting op basis van betalingsmethode voorkomen

Als de parameter **Korting op basis van betalingsmethode voorkomen** is ingesteld op **Ja**, kan een korting **op basis van een betalingsmethoden** niet op een product worden toegepast. Alle overige kortingen (met inbegrip van handmatige kortingen) kunnen nog worden toegepast.

Detailhandelaren kiezen er vaak voor om bepaalde producten, zoals nieuwe artikelen of veelgevraagde artikelen, uit te sluiten van kortingen op basis van het artikel (zoals eenvoudige en hoeveelheidskortingen). Als de klant echter betaalt met de voorkeursbetaalmethode, gelden ze mogelijk nog wel voor kortingen op basis van betalingsmethode. Om dit te realiseren kunnen detailhandelaren de opties **Alle kortingen voorkomen** en **Kortingen op basis van betalingsmethode voorkomen** op **Nee** instellen en de optie **Detailhandelkortingen voorkomen** en **Handmatige kortingen voorkomen** op **Ja**.

## <a name="deprecated-or-removed-settings"></a>Verwijderde of afgeschafte instellingen

De volgende prijsinstellingen zijn verwijderd of gepland voor verwijdering uit Dynamics 365 Commerce.

| Instelling | Reden voor afschaffing of verwijdering | Status van afschaffing of verwijdering |
|---------|-----------------------------------|-------------------------------|
| Verwerking van overlappende kortingen | We hebben deze instelling in Commerce-parameters opgegeven om te bepalen hoe de prijsengine de beste kortingscombinatie zoekt en bepaalt die u wilt toepassen. Met de optie **Beste korting** moeten alle mogelijke kortingscombinaties worden gecombineerd tijdens de prijsberekening. De optie **Beste prestaties** is een geoptimaliseerde optie die een geavanceerd heuristisch algoritme gebruikt en een marginale-waardeclassificatie om de prioriteit te bepalen, te evalueren en tijdig de beste kortingscombinatie te bepalen. De optie **Vereffende berekening** in de codebasis werkt op dezelfde manier als de optie **Beste prestaties**. Daarom is het in wezen een gedupliceerde optie. De prijsengine is bijgewerkt zodat deze alleen **Beste prestaties** als standaardoptie gebruikt. Daarom is deze instelling niet langer van toepassing. | Afgeschaft in de versie 10.0.21 en wordt verwijderd in oktober 2022. |
| Toestaan dat prijscorrecties de productprijs verhogen | Deze instelling was bedoeld om te bepalen of de functie voor prijscorrectie de productprijzen kan verhogen. Als de parameter is uitgeschakeld, kunnen organisaties de functie voor prijscorrectie alleen gebruiken om de eenheidsprijs van een product in te stellen zodat deze lager is dan de basisprijs en de verkoopprijs in de handelsovereenkomst. We hebben deze instelling afgeschaft, omdat de functie voor prijscorrectie is bijgewerkt en standaard tweewegscorrecties (verhoging of verlaging) ondersteunt. | Afgeschaft in de versie 10.0.30 en wordt verwijderd in oktober 2023. |
| Prijzenrapport voor detailhandel inschakelen | Met deze instelling werd bepaald of de functie **Prijsrapport** beschikbaar is voor gebruik in de pagina met de winkelconfiguratie. Deze instelling is afgeschaft, omdat de winkelconfiguratiepagina is bijgewerkt en standaard de functie **Prijsrapport** levert. | Afgeschaft in de versie 10.0.31 en wordt verwijderd in oktober 2023. |
| De datum van vandaag gebruiken om prijzen te berekenen | De prijsengine voor Dynamics 365 Supply Chain Management ondersteunt de prijsberekening op basis van de gewenste verzenddatum of gewenste ontvangstdatum, samen met de huidige datum. De Commerce-prijsengine ondersteunt alleen prijsberekening op basis van de huidige datum. We hebben deze instelling opgenomen voor klanten die gebruik maken van zowel Supply Chain Management- als Commerce-functies, en we raden deze klanten aan dat deze altijd op **Ja** wordt ingesteld, zodat de twee prijsengines kunnen samenwerken. We hebben deze instelling afgeschaft, omdat deze het berekeningsgedrag niet fundamenteel wijzigt en dus overbodig is. | Afgeschaft in de versie 10.0.31 en wordt verwijderd in oktober 2023. |
| Maximumprijs | Met deze instelling in het functionaliteitsprofiel kunnen we bepalen of alleen producten met een verkoopprijs die onder de opgegeven maximumprijs valt, via POS kunnen worden verkocht in specifieke winkels. Deze instelling is afgeschaft vanwege een laag functiegebruik. | Afgeschaft in de versie 10.0.31 en wordt verwijderd in oktober 2023. |
| Kortingen toepassen op eenheidsprijs | Deze instelling was bedoeld om te bepalen of prijzen en kortingen tijdens het berekenen van de prijs worden afgerond op eenheidsprijsniveau of op verkoopregelniveau. We hebben de functie afgeschaft omdat deze niet wordt gebruikt in de huidige codebasis. | Afgeschaft in de versie 10.0.31 en wordt verwijderd in oktober 2023. |
| Handmatig meerdere artikelkortingen berekenen | We hebben deze instelling gebruikt om te bepalen of de prijsengine uitgestelde prijsberekening gebruikt voor het detailhandelwinkelkanaal. Als de parameter is ingesteld op **Ja**, worden meerregelkortingen (zoals hoeveelheidskortingen, drempelkortingen en combinatiekortingen) niet onmiddellijk berekend door de prijsengine wanneer een verkooporder wordt gemaakt of bewerkt in de POS-toepassing. We hebben besloten deze instelling te consolideren met een vergelijkbare instelling in Commerce-parameters voor een omnichannel-controle. | Afgeschaft in de versie 10.0.31 en wordt verwijderd in oktober 2023. |

Zie [Verwijderde of afgeschafte functies in Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md) voor een volledige lijst met verwijderde of afgeschafte functies in Dynamics 365 Commerce.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

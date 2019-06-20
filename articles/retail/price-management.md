---
title: Verkoopprijsbeheer detailhandel
description: Dit onderwerp beschrijft de concepten voor het maken en beheren van verkoopprijzen in Microsoft Dynamics 365 for Retail.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afa553fd0562b306f720f2a30c7f901db7ad1b3a
ms.sourcegitcommit: 0fbfb9b0ab78c804f3931a083028d2ce313d6521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/21/2019
ms.locfileid: "1594065"
---
# <a name="retail-sales-price-management"></a>Verkoopprijsbeheer van detailhandel

[!include [banner](includes/banner.md)]

Dit onderwerp bevat informatie over het proces voor het maken en beheren van verkoopprijzen in Microsoft Dynamics 365 for Retail. Het richt zich op de concepten die betrokken zijn bij dit proces, en op de effecten van de verschillende configuratieopties voor verkoopprijzen.

## <a name="terminology"></a>Terminologie

De volgende termen worden gebruikt in dit onderwerp.

| Voorwaarde | Definitie, gebruik en notities |
|---|---|
| Prijs | Het bedrag voor één eenheid waarvoor een product wordt verkocht in een verkooppunt-client (POS) of op een verkooporder. In dit onderwerp heeft de term *prijs* altijd betrekking op de verkoopprijs niet op de voorraadprijs of de kostprijs. |
| Basisprijs | De prijs die is ingesteld in het veld **Prijs** voor een vrijgegeven product. |
| Handelsovereenkomstprijs | De prijs die is ingesteld voor een product of variant op basis van een handelsovereenkomst van het type **Prijs (verkoop)**. |
| Beste prijs | Wanneer meerdere prijzen of kortingen kunnen worden toegepast op een product, het kleinste prijsbedrag en/of het grootste kortingsbedrag wat leidt tot het laagst mogelijke nettobedrag dat de klant moet betalen. In dit onderwerp wordt het concept van de beste prijs altijd aangeduid als 'de beste prijs.' Deze beste prijs verschilt van en moet niet worden verward met de opsommingswaarde **Beste prijs** voor een gelijktijdigheidsmodus voor korting. |

## <a name="price-groups"></a>Prijsgroepen

Prijsgroepen vormen de kern van het prijzen- en kortingenbeheer in Retail. Prijsgroepen worden gebruikt om prijzen en kortingen toe te wijzen aan detailhandelentiteiten (zoals kanalen, catalogi, aansluitingen en loyaliteitsprogramma's). Aangezien prijsgroepen worden gebruikt voor alle prijzen en kortingen, is het belangrijk dat u plant hoe u ze gebruikt voordat u begint.

Een prijsgroep is in feite alleen een naam, een omschrijving en eventueel een prioriteit voor prijscalculatie. Het belangrijkste punt om te onthouden over prijsgroepen is dat ze worden gebruikt om de veel-op-veel-relaties van kortingen en prijzen met retailentiteiten te beheren.

De volgende afbeelding laat zien hoe prijsgroepen worden gebruikt. In deze afbeelding ziet u dat 'Prijsgroep' letterlijk het middelpunt is van prijzen- en kortingsbeheer. De retailentiteiten die u kunt gebruiken voor het beheren van gedifferentieerde prijzen en kortingen staan aan de linkerkant en de werkelijke prijzen- en kortingsrecords aan de rechterkant.

![Prijsgroepen](./media/PriceGroups.png "Prijsgroepen")

Wanneer u prijsgroepen maakt, moet u niet één prijsgroep gebruiken voor meerdere soorten retailentiteiten. Anders kan het lastig zijn om te bepalen waarom een bepaalde prijs of korting op een transactie wordt toegepast.

Zoals de rode streepjeslijn in de afbeelding laat zien, ondersteunt Retail de basisfunctie van Microsoft Dynamics 365 van prijsgroepen die direct voor een klant zijn ingesteld. In dit geval krijgt u echter alleen verkoopprijshandelsovereenkomsten. Als u klantspecifieke prijzen wilt toepassen, raden wij aan dat u niet prijsgroepen rechtstreeks voor de klant instelt. In plaats daarvan moet u aansluitingen gebruiken.

De volgende secties bevatten meer informatie over de retailentiteiten die u kunt gebruiken om verschillende prijzen in te stellen wanneer prijsgroepen worden gebruikt. De configuratie van prijzen en kortingen voor alle entiteiten is een tweeledig proces. Deze stappen kunnen in een willekeurige volgorde worden uitgevoerd. De logische volgorde is echter om de prijsgroepen eerst in te stellen voor de entiteiten, omdat deze stap waarschijnlijk een eenmalige instelling is die wordt uitgevoerd tijdens de implementatie. Vervolgens kunt u, als prijzen en kortingen zijn gemaakt, de prijsgroepen afzonderlijk instellen voor deze prijzen en kortingen.

### <a name="channels"></a>Afzetkanalen

In de detailhandel is het heel gebruikelijk om verschillende prijzen te hanteren voor verschillende kanalen. De twee primaire factoren die invloed hebben op specifieke kanaalprijzen zijn kosten en voorwaarden van de lokale markt.

- **Kosten** : hoe verder een kanaal van de productbron verwijderd is, hoe meer het kost om een product op te slaan. Verse producten hebben bijvoorbeeld een beperkte houdbaarheid en specifieke productievereisten (bijvoorbeeld een groeiseizoen). In de winter kosten kost sla waarschijnlijk meer in noordelijke klimaten dan in zuidelijke klimaten. Als u de prijzen voor kanalen over een groot geografisch gebied instelt, wilt u waarschijnlijk verschillende prijzen instellen in verschillende kanalen.
- **Lokale marktvoorwaarden**: een winkel die een directe concurrent in de straat heeft, werkt veel prijsgevoeliger dan een winkel die geen directe concurrent in de buurt heeft.

### <a name="affiliations"></a>Aansluitingen

De algemene definitie van een aansluiting is een koppeling naar of de koppeling met een groep. In Retail zijn aansluitingen groepen met klanten. Aansluitingen zijn een flexibelere manier voor klantprijzen en kortingen dan het basisconcept van Microsoft Dynamics 365 voor klantgroepen en kortingsgroepen. In de eerste plaats kan een aansluiting worden gebruikt voor prijzen en kortingen, terwijl bij niet-detailhandelsprijzen voor elk type prijs en korting een andere groep bestaat. Vervolgens kan een klant deel uitmaken van meerdere aansluitingen maar van slechts één niet-detailhandelsprijsgroep van elk type. Ten slotte kunnen aansluitingen zo worden ingesteld dat ze aan een klant zijn gekoppeld, maar dat hoeft niet. Een ad-hoc-aansluiting kan worden gebruikt voor anonieme klanten op het POS. Een typisch voorbeeld van een anonieme aansluitingskorting is een korting voor senioren of studenten waar een klant een korting kan ontvangen door een lidmaatschapskaart te tonen.

Hoewel aansluitingen meestal zijn gekoppeld aan kortingen, kunt u ze ook gebruiken om gedifferentieerde prijzen in te stellen. Wanneer een detailhandelaar bijvoorbeeld aan een werknemer verkoopt, kan de verkoopprijs worden aangepast in plaats van het toepassen van een korting boven op de normale prijs. Ook kan een detailhandelaar die aan particuliere en zakelijke klanten verkoopt, zakelijke klanten betere prijzen bieden, op basis van hun inkoopvolume. Aansluitingen maken beide scenario's mogelijk.

### <a name="loyalty-programs"></a>Loyaliteitsprogramma's

Loyaliteitsprogramma's voor prijzen en kortingen zijn in feite een aansluiting met een speciale naam. Prijzen en kortingen kunnen worden ingesteld voor een loyaliteitsprogramma, net zoals ze kunnen worden ingesteld voor een aansluiting. De manier waarop klanten loyaliteitsprijzen krijgen tijdens een transactie of order, verschilt echter van de manier waarop deze prijscalculatie voor aansluitingen plaatsvindt. Klanten kunnen alleen loyaliteitsprijzen als een loyaliteitskaart wordt toegevoegd aan de transactie. Wanneer een loyaliteitskaart die is toegevoegd aan een transactie, wordt ook het loyaliteitsprogramma toegevoegd. Met het loyaliteitsprogramma worden speciale prijzen en kortingen mogelijk gemaakt.

Loyaliteitsprogramma's kunnen verschillende lagen hebben en de kortingen voor verschillende lagen kunnen verschillen. Op deze manier kunnen detailhandelaren terugkerende klanten grotere beloningen geven zonder dat deze klanten handmatig in een speciale groep worden geplaatst.

Loyaliteitsprogramma's hebben extra functies naast prijzen en kortingen. Vanuit het perspectief van prijzen en kortingen zijn ze echter hetzelfde als aansluitingen.

### <a name="catalogs"></a>Catalogi

Sommige detailhandelaren gebruiken fysieke of virtuele catalogi om producten te verkopen en prijzen vast te stellen voor specifieke groepen klanten. Als onderdeel van hun bedrijfsmodel met gerichte marketing via een catalogus, kunnen deze detailhandelaren gedifferentieerde prijzen instellen voor verschillende catalogi. Microsoft Dynamics 365 ondersteunt deze functionaliteit met het definiëren van catalogusspecifieke kortingen en prijzen, net zoals u kortingen kunt definiëren voor kanalen of aansluitingen. Wanneer u een catalogus bewerkt, kunt u prijsgroepen koppelen aan de catalogus, net zoals u ze aan een kanaal, aansluiting of loyaliteitsprogramma kunt koppelen.

### <a name="best-practices-for-price-groups"></a>Aanbevolen procedures voor prijsgroepen

Gebruik geen een prijsgroep voor meerdere retailentiteitstypen. Gebruik in plaats daarvan één set met prijsgroepen voor kanalen, een andere set met prijsgroepen voor aansluitingen of loyaliteitsprogramma's, enzovoort. U kunt een voorvoegsel of achtervoegsel toevoegen aan de naam van de prijsgroep om de verschillende typen prijsgroepen visueel te groeperen.

Stel prijsgroepen niet rechtstreeks in op een klant. Gebruik in plaats daarvan een aansluiting. Op deze manier kunt u alle soorten prijzen en kortingen toewijzen aan klanten, niet alleen handelsovereenkomsten voor verkoopprijzen.

## <a name="pricing-priority"></a>Prioriteit prijscalculatie

Een prioriteit voor een prijscalculatie is in feite alleen een nummer en een omschrijving. Prioriteiten voor prijscalculaties kunnen worden toegepast op de prijsgroepen of rechtstreeks op kortingen. Wanneer prioriteiten voor prijscalculaties worden gebruikt, kan een detailhandelaar het principe van de beste prijs overschrijven door de volgorde te bepalen waarin prijzen en kortingen worden toegepast op producten. Een hoger prioriteitsnummer wordt geëvalueerd voor lager prioriteitsnummer. Ook als een prijs of korting op een willekeurig prioriteitsnummer wordt gevonden, worden alle prijzen of kortingen met een lager prioriteitsnummer genegeerd.

De prijs en korting kunnen afkomstig zijn uit twee verschillende prijsprioriteiten, omdat de prijsprioriteiten los van elkaar van toepassing zijn op prijzen en kortingen.

Als u prioriteit voor prijzen gebruikt, moet u een prioriteit voor prijscalculatie toewijzen aan een prijsgroep en vervolgens een handelsovereenkomst maken voor deze prijsgroep.

De functie prioriteit voor prijscalculatie is geïntroduceerd voor het scenario waarin een detailhandelaar hogere prijzen wil toepassen in een specifieke reeks winkels. Bijvoorbeeld: als een detailhandelaar regionale prijzen heeft gedefinieerd voor de oostkust van de Verenigde Staten, maar hogere prijzen wil berekenen voor bepaalde producten in winkels in New York City, omdat het duurder is om sommige producten daar te verkopen en/of omdat de plaatselijke markt bereid is een hogere prijs te betalen.

Zoals is aangegeven in de sectie 'Beste prijs' van dit onderwerp, selecteert de engine voor detailhandelsprijzen doorgaans de laagste van de twee prijzen. Daarom zal de detailhandelaar meestal niet de hoogste van twee prijzen hanteren in een winkel met prijsgroepen voor zowel oostkust en voor New York. Om dit probleem op te lossen moest de detailhandelaar, voordat de functie voor prioriteit prijscalculatie werd geïntroduceerd, voor elk product tweemaal prijzen definiëren en niet beide prijsgroepen toewijzen. Ook moest de detailhandelaar extra prijsgroepen maken om de producten met hogere prijzen af te scheiden van producten met de gebruikelijke, lagere prijzen.

Met de e functie prioriteit prijscalculatie kan de detailhandelaar echter een prijsprioriteit instellen voor winkelprijzen die hoger zijn dan de prijsprioriteit voor regionale prijzen. De detailhandelaar kan ook alleen een prioriteit prijscalculatie opstellen voor winkelprijzen en regionale prijzen op de standaard prijsprioriteit van 0 (nul) laten staan. Beide instellingen zorgen dat altijd winkelprijzen worden gebruikt vóór regionale prijzen.

### <a name="pricing-priority-example"></a>Voorbeeld prioriteit prijscalculatie

Laten we kijken naar een voorbeeld waarin winkelprijzen andere prijzen overschrijven.

Een nationale detailhandelaar stelt de meeste prijzen in per regio en werkt met vier gebieden: Noordoost, Zuidoost, Midden-west en West. Er zijn verschillende markten met hoge kosten aangegeven die in aanmerking komen voor hogere prijzen. Deze markten zijn in New York City, Chicago en het gebied van San Francisco Bay.

In dit voorbeeld zullen we op de regio Noordoost inzoomen. Winkel 1 is in Boston en winkel 2 in Manhattan. Voor de winkel in Boston zijn twee prijsgroepen gekoppeld aan het kanaal: Noordoost en Winkel 1. Voor de winkel in Manhattan zijn drie prijsgroepen gekoppeld aan het kanaal: Noordoost, NYC en Winkel 2.

De detailhandelaar stelt twee prioriteiten voor prijscalculatie: hoge kosten heeft een prioriteitsnummer van 5 en winkelprijzen een prioriteitsnummer van 10. (Houd er rekening mee dat de prioriteit prijscalculatie standaard 0 is \[nul\], en een prijs of korting met een hogere prioriteit voorrang krijgt op een prijs of korting met een lager prioriteitsnummer.) De prioriteit prijscalculatie voor de prijsgroep Noordoost staat op de standaardwaarde van **0** (nul). De de prijsgroep NYC is het prioriteitsnummer ingesteld op **5**, aangezien New York City een markt met hoge kosten is. Voor de prijsgroepen van winkel 1 en 2 is de prioriteit prijscalculatie ingesteld op **10**.

De detailhandelaar verkoopt deze twee producten: basisproduct 1 is een T-shirt en product 2 een merkspecifieke spijkerbroek.

| Product | Prijs Noordoost | Prijs NYC | Winkelprijs |
|---|---|---|---|
| T-shirt | $ 15 | Niet ingesteld | Niet ingesteld |
| Spijkerbroek | $ 50 | $ 70 | Niet ingesteld |

Het T-shirt wordt verkocht voor dezelfde prijs (dat wil zeggen $ 15) in de winkels in Boston en Manhattan, omdat slechts één prijs is ingesteld in de prijsgroep Noordoost die is gekoppeld aan beide kanalen. De jeans wordt verkocht voor $50 in de winkel in Boston omdat deze prijs de enige prijs is die beschikbaar is in deze winkel. Er zijn echter twee prijzen beschikbaar in de winkel in Manhattan: $ 50 en $ 70. Omdat de prioriteit prijscalculatie van 5 voor de prijsgroep NYC hoger is dan de prioriteit van 0 (nul) voor de prijsgroep Noordoost, wordt de prijs als $ 70 opgenomen in het POS-systeem.

> [!NOTE]
> Voor elke prioriteit prijscalculatie moet de logica van de engine voor detailhandelsprijzen volledig worden verwerkt. Om te garanderen dat de prijzen en kortingen correct worden berekend, moet u prijsprioriteiten spaarzaam toepassen.

## <a name="types-of-prices"></a>Typen prijzen

In Microsoft Dynamics 365 kunt u de prijs van een product op drie plaatsen instellen:

- Rechtstreeks op het product (basisprijs)
- In een handelsovereenkomst voor de verkoopprijs
- In een prijscorrectie

De basisprijs en de handelsovereenkomstprijs maken deel uit van de kernfuncties van Microsoft Dynamics 365 en zijn beschikbaar zelfs als u Retail niet gebruikt. De functionaliteit voor prijscorrectie is alleen beschikbaar in Retail. In de volgende sectie vindt u meer informatie over de opties voor het instellen van prijzen en wordt uitgelegd hoe de opties samenwerken.

## <a name="setting-prices"></a>Prijzen instellen

### <a name="base-price"></a>Basisprijs

De gemakkelijkste plaats om de prijs voor een product in te stellen is rechtstreeks op het product. De waarde die u rechtstreeks op een product instelt, wordt vaak de basisprijs voor het product genoemd. U stelt de basisprijs in in het veld **Prijs** van het tabblad **Verkopen** van de pagina **Vrijgegeven productdetails**. De ingevoerde waarde gebruikt de de valuta van het bedrijf. De prijs voor een hoeveelheid van 1 is standaard de maateenheid die is ingesteld in het veld **Eenheid** op het tabblad **Verkopen**. De werkelijke prijs per eenheid van een product is gebaseerd op de maateenheid, de prijshoeveelheid en de valuta.

Als een product één prijs heeft voor iedereen, is de basisprijs de meest efficiënte manier om de prijs van dat product te beheren. Zelfs als u handelsovereenkomstprijzen toepast, kunt u ook de basisprijs op een product instellen. Als u vervolgens niet een handelsovereenkomst van het type**Alle** gebruikt, hebt u een terugvalprijs die wordt gebruikt wanneer er geen handelsovereenkomst van toepassing is.

Als een detailhandelkanaalsvaluta afwijkt van de bedrijfsvaluta, wordt de basisprijs in dat detailhandelkanaal bepaald met behulp van valutaconversie op de prijs die is ingesteld op het product.

Hoewel de prijs per eenheid geen gebruikelijk detailhandelscenario is, wordt dit ondersteund door de engine voor detailhandelsprijzen. Als de prijs per eenheid is ingesteld op een andere waarde dan **0** (nul), is de prijs per eenheid gelijk aan prijs ÷ prijs per eenheid. Als de prijs van een product bijvoorbeeld $10,00 is en de prijs per eenheid 50, is de prijs voor een hoeveelheid van 1 $0,20 (= $10,00 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Handelsovereenkomst met verkoopprijs

U kunt met behulp van het handelsovereenkomstjournaal een verkoopprijshandelsovereenkomst voor elk product maken. In Microsoft Dynamics 365 zijn er drie klantbereiken voor verkoopprijshandelsovereenkomsten: **tabel**, **groep** en **alle**. Het bereik van de klant bepaalt de klanten waarvoor de handelsovereenkomst voor een bepaalde verkoopprijs geldt.

Een verkoopprijshandelsovereenkomst van het type **tabel** geldt voor één klant die rechtstreeks in de handelsovereenkomst is ingesteld. Dit scenario is geen normaal detailhandelscenario voor business-to-consumer (B2C). Als dit echter plaatsvindt, gebruikt de prijsbepalingsengine handelsovereenkomsten van het type **tabel** voor het bepalen van de prijs.

Een verkoopprijshandelsovereenkomst van het type **groep** wordt meestal gebruikt met de detailhandelsfunctionaliteit. Buiten Retail zijn verkoopprijshandelsovereenkomsten van het type **groep** van toepassing voor een eenvoudige klantengroep. In Retail is het concept van een klantgroep echter uitgebreid zodat deze een meer algemene detailhandelprijsgroep is. Een prijsgroep kan worden gekoppeld aan een detailhandelkanaal, aansluiting, loyaliteitsprogramma of catalogus. Zie de sectie 'Prijsgroepen' eerder in dit onderwerp voor gedetailleerde informatie over prijsgroepen.

> [!NOTE]
> Een prijs uit een handelsovereenkomst heeft altijd voorrang op de de basisprijs.

### <a name="price-adjustment"></a>Prijscorrectie

Zoals de naam al aangeeft, wordt een prijscorrectie gebruikt voor het wijzigen van de prijs die rechtstreeks op het product of met een handelsovereenkomst is ingesteld. Een prijscorrectie kan alleen worden gebruikt voor het verlagen van de prijs, niet voor het verhogen. Een prijscorrectie is de aanbevolen manier voor detailhandelaren voor het maken, bijhouden en beheren van prijsverlagingen voor hun producten.

Er zijn drie typen prijscorrecties: percentage, korting en prijs. Een prijscorrectie van het type percentage of kortingsbedrag wordt altijd toegepast op een verkooptransactie. Een prijscorrectie van het prijstype is echter alleen van toepassing als de gecorrigeerde prijs lager dan de prijs die is ingesteld met behulp van de basisprijs of de handelsovereenkomstprijs. Als dus de prijs die is ingesteld in een prijscorrectie hoger is dan de niet-gecorrigeerde prijs, wordt de prijscorrectie niet gebruikt.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Prijs voor een product in een transactie vaststellen

De berekening van de prijs en de korting op een transactie gebruikt het principe van het zoeken naar de beste prijs voor de klant. Volgens dit principe wordt de laagste prijs gebruikt, als meer dan één prijs wordt gevonden. Bovendien wordt de combinatie van kortingen gebruikt die het grootste kortingsbedrag voor de gehele transactie produceert. In sommige gevallen moet een kleinere korting worden gebruikt op één product, zodat extra kortingen kunnen worden toegepast op andere producten in de transactie.

De enige uitzondering op het principe van het zoeken naar de beste prijs voor de klant is een optie voor goedkoopste gecombineerde kortingen. Deze optie maakt de goedkoopste kortingen mogelijk ten gunste van de detailhandelaar wanneer producten worden geselecteerd en gegroepeerd. Wanneer een transactie meer producten bevat dan vereist zijn om in aanmerking te komen voor de goedkoopste korting, selecteert de prijsbepalingsengine de producten waarmee het kleinst mogelijke kortingsbedrag voor de klant wordt geproduceerd.

De prijsbepalingsengine retourneert drie prijzen voor elk product: de basisprijs, de prijs van de handelsovereenkomst en de actieve prijs.

De basisprijs is alleen de eigenschap van het product en is hetzelfde voor iedereen.

Voor de verkoopprijs uit de handelsovereenkomst wordt, als de optie **Volgende zoeken** is ingesteld op **Ja**, de laagste prijs die wordt gevonden voor de toepasselijke verkoopprijshandelsovereenkomsten gebruikt als de prijs van de handelsovereenkomst. U vindt handelsovereenkomsten met behulp van prijsgroepen of de rekeningcode **Alle**. Handelsovereenkomsten kunnen ook rechtstreeks aan een klant worden toegewezen. Als de optie **Volgende zoeken** is ingesteld op **Nee**, wordt de eerste handelsovereenkomstprijs gebruikt die is gevonden. Als er geen verkoopprijshandelsovereenkomsten worden gevonden, wordt de prijs van de handelsovereenkomst gelijk gesteld aan de basisprijs.

De actieve prijs wordt berekend door de prijs van de handelsovereenkomst te nemen en de grootste prijscorrectie toe te passen die voor het product geldt. Als er geen prijscorrecties worden gevonden of als de berekende actieve prijs groter is dan de prijs van de handelsovereenkomst, wordt de actieve prijs gelijk gesteld aan de prijs van de handelsovereenkomst. Vergeet niet dat u de prijs van een product niet kunt verhogen met een prijscorrectie. De toepasselijke prijscorrecties vindt u alleen met behulp van prijsgroepen die zijn toegewezen aan een kanaal, catalogus, aansluiting of loyaliteitsprogramma.

## <a name="category-price-rules"></a>Prijsregels van categorie

De categorieprijsregels in Retail bieden u een eenvoudige manier om nieuwe handelsovereenkomsten voor alle producten in een categorie maken. Met deze functie kunt u ook automatisch bestaande handelsovereenkomsten voor de producten in de categorie zoeken en ze laten verlopen.

Wanneer u de optie selecteert om bestaande handelsovereenkomsten te laten verlopen, maakt het systeem een nieuwe handelsovereenkomstjournaal voor de producten in de categorie die een actieve handelsovereenkomst hebben. Hhet journaal moet echter handmatig worden geboekt. Bovendien kunnen de categorieprijsregels alleen bestaande handelsovereenkomsten vinden als u dezelfde prijsregel gebruikt (dat wil zeggen als u een nieuwe prijsregel maakt die gebruikmaakt van dezelfde categorie als voorheen). Als u niet dezelfde prijsregel gebruikt, zullen de bestaande handelsovereenkomsten niet verlopen.

De prijzen kunnen worden verhoogd of verlaagd met de velden **Prijsregel** en **Prijsbasis** van de categorieprijsregels.

- Selecteer in het veld **Prijsregel** welk type prijswijziging u wilt gebruiken:

    - **Verhoging**: een percentage van de prijsbasis wordt gebruikt om de verkoopprijs te berekenen. Voorbeeld: een product dat 10,00 kost en voor 15,00 wordt verkocht, heeft een prijsverhoging van 50 procent.
    - **Marge**: een percentage van de verkoopprijs wordt gebruikt om het winstbedrag te berekenen. Voorbeeld: een product dat 10,00 kost en voor 15,00 wordt verkocht, heeft een marge van 33,3 procent.
    - **Vast bedrag**: een bedrag dat aan de gebruikte prijsbasis wordt toegevoegd om de verkoopprijs te berekenen. Voorbeeld: een product dat 10,00 kost en voor 15,00 wordt verkocht, heeft een vast bedrag van 5,00.

- Selecteer het type te wijzigen prijs in het veld **Prijsbasis**:

    - **Basiskosten**: het bedrag dat de detailhandelaar aan de leverancier betaalde.
    - **Basisprijs**: de verkoopprijs voordat handelsovereenkomsten en de prijscorrecties worden toegepast.
    - **Huidige prijs**: de verkoopprijs nadat handelsovereenkomsten en de prijscorrecties zijn toegepast.

Als u de prijzen van verschillende producten uit de verschillende productcategorieën eenvoudig wilt bijwerken, kunt u de aanvullende productcategorieën samen met de categorieprijsregels gebruiken.

## <a name="best-practices"></a>Aanbevolen procedures

Microsoft SQL Server Express wordt vaak gebruikt voor kanaaldatabases vanwege de kosten (gratis). Houd er rekening mee dat SQL Server Express hardwarebeperkingen en limieten heeft voor gegevensgrootte. Als u niet goed plant, kunt u snel de grenzen van de gegevensgrootte van SQL Server Express bereiken. Deze overweging geldt niet alleen voor prijzen, maar ook voor andere gebieden van het product. Hier volgen enkele aanbevelingen waarmee u de grootte van uw gegevens kunt verminderen:

- Als u handelsovereenkomsten gebruikt en uw prijzen veranderen, moet u de oude handelsovereenkomsten laten verlopen door een einddatum in te stellen. Na verloop van tijd daalt door deze benadering het aantal handelsovereenkomsten dat is opgeslagen in de kanaaldatabases. Ook vermindert de hoeveelheid gegevens waarmee het prijsberekeningsalgoritme moet werken.
- Als uw prijzen per productvariant verschillen, kunt u overwegen de basisprijs van het product als de prijs van de meest voorkomende variant te gebruiken. Gebruik vervolgens de handelsovereenkomsten alleen voor de variantprijzen die uitzonderingen zijn. Deze benadering vermindert het aantal records voor handelsovereenkomsten. Omdat het is eenvoudig is om gegevens te importeren in Microsoft Dynamics 365, wilt u wellicht een handelsovereenkomst importeren voor elke variant van elk product. Die benadering kan echter leiden tot veel handelsovereenkomsten die dezelfde waarde hebben. En daardoor onnodig de omvang van uw gegevens vergroten.
- Retail verwerkt variantspecifieke prijzen in volgorde van meest specifiek naar minst specifiek. Als een productdimensie geen invloed heeft op de prijs, hoeft u geen handelsovereenkomsten daarvoor te definiëren. Bijvoorbeeld: een product is beschikbaar in drie kleuren en vier afmetingen, maar de prijs varieert alleen door de grootte. Als u een handelsovereenkomst voor elke variant definieert, maakt u 12 records. U kunt in plaats daarvan alleen een handelsovereenkomst definiëren voor elke grootte en de kleurdimensie leeg laten. In dit geval hoeft u slechts 4 records te maken.

    Als niet alle waarden van een dimensie resulteren in een andere prijs, kunt u ook één handelsovereenkomst definiëren voor het productmodel en alle productdimensies leeg laten. Definieer vervolgens een aparte handelsovereenkomst voor elke dimensiewaarde die een andere prijs genereert. Bijvoorbeeld als de grootte XXL een hogere prijs heeft, maar alle andere afmetingen dezelfde prijs hebben, hoeft u slechts twee handelsovereenkomsten te maken: één voor het productmodel en één voor de grootte XXL.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Prijzen inclusief btw versus prijzen exclusief btw

Wanneer u verkoopprijzen in Microsoft Dynamics 365 instelt, geeft u niet aan of de waarde van de ingestelde prijs inclusief of exclusief btw is. De waarde is alleen de prijs. Met de instelling **Prijs inclusief btw** voor detailhandelkanalen kunt u echter detailhandelkanalen zo configureren dat de prijzen al dan niet inclusief btw zijn. Deze instelling is ingesteld voor het kanaal en kan zelfs in één bedrijf wijzigen.

Als u werkt met inclusief en exclusief btw, is het belangrijk dat u prijzen correct hebt ingesteld, omdat het totale bedrag dat de klant betaalt, niet verandert als de instelling **Prijs inclusief btw** in het kanaal wordt gewijzigd.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Verschillen tussen adviesprijs en niet-adviesprijs

Er wordt één prijscalculatie-engine gebruikt voor het berekenen van de detailhandelsprijzen voor alle kanalen: callcenters, winkels en online winkels. Dit is handig voor het inschakelen van de gecombineerde handelsscenario's.

Adviesprijs is ontworpen om te gebruiken met detailhandelsentiteiten in plaats van niet-detailhandelsentiteiten. Het is vooral ontworpen om prijzen in te stellen per winkel, niet per magazijn.

De adviseprijsengine ondersteunt niet de volgende prijsbepalingsfuncties:

- Prijs instellen met site- en magazijndimensies.
- Op kenmerken gebaseerde prijzen
- Leverancierskorting pass-through

Bovendien ondersteunt de adviseprijsengine **alleen** de volgende prijsbepalingsfuncties:

- De prijs is gebaseerd op de productdimensies in volgorde van de meest specifieke variantprijs naar de minst specifieke variantprijs voor de modelproductprijs. Een prijs die wordt ingesteld via twee productdimensies (bijvoorbeeld kleur en grootte) wordt gebruikt vóór een prijs die is ingesteld via slechts één productdimensie (bijvoorbeeld grootte).
- Dezelfde prijsgroep kan worden gebruikt om prijzen en kortingen te bepalen.

## <a name="pricing-api-enhancements"></a>Verbeteringen in API voor prijzen

Prijs is een van de belangrijkste factoren voor koopbeslissingen van veel klanten en veel klanten vergelijken de prijzen op verschillende locaties voordat ze overgaan tot koop. Om er zeker van te zijn dat ze concurrerende prijzen bieden, houden detailhandelaren hun concurrenten goed in de gaten en hebben ze vaak acties. Om deze detailhandelaren te helpen bij het aantrekken van klanten, is het zeer belangrijk dat bij het zoeken naar producten, in de bladerfunctie, lijsten en op de pagina met productdetails de meest nauwkeurige prijzen worden weergegeven.

In een aanstaande release van Retail retourneert de API **GetActivePrices** prijzen die eenvoudige kortingen bevatten (bijvoorbeeld kortingen van één regel die niet afhankelijk zijn van andere artikelen in de winkelwagen). Op deze manier liggen de prijzen die worden weergegeven dicht bij het werkelijke bedrag dat klanten voor artikelen betalen. Deze API bevat alle soorten eenvoudige kortingen: op relatie, loyaliteit, catalogus en kanaal gebaseerde kortingen. Daarnaast retourneert de API de namen en validiteitsgegevens voor de toegepaste kortingen, zodat detailhandelaren een meer gedetailleerde omschrijving van de prijs kunnen bieden en een gevoel van urgentie creëren als de geldigheid van de korting binnenkort verloopt.

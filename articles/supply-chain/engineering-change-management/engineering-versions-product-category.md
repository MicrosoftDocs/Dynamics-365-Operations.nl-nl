---
title: Technische versies van en categorieën voor technische producten
description: Dit onderwerp bevat informatie over het concept van technische versies. Technische versies zorgen ervoor dat de verschillende statussen van een product en de bijbehorende gegevens actueel en duidelijk blijven en dat ze in het systeem kunnen worden gevisualiseerd.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c15dcd0adfcf9b9022a919bd516dcf5117ea5041
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987474"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Technische versies van en categorieën voor technische producten

[!include [banner](../includes/banner.md)]

Technische producten ontwikkelen zich om verschillende redenen gedurende de levenscyclus. Er kunnen bijvoorbeeld wijzigingen worden aangebracht om het product onderhoudsvriendelijker te maken, een onderdeel te wijzigen omdat de leverancier deze niet meer aanbiedt, op nieuwe inzichten te reageren of fouten in het eerste ontwerp op te lossen. Er zijn ook verschillende redenen waarom deze wijzigingen moeten worden opgeslagen als onderdeel van een doorlopend product, op een manier waardoor vorige gegevens niet worden overschreven. Dit zijn enkele van deze redenen:

- U wilt het product kunnen traceren zoals het is geproduceerd en bij uw klanten is afgeleverd in eerdere levenscyclusstaten.
- U hebt een doorlooptijd nodig voordat u de wijzigingen goedkeurt en toepast.
- U wilt dat voor elke wijziging een tijdstempel wordt toegepast en u wilt eerder geproduceerde producten afzonderlijk van elkaar kunnen afleveren.

*Technische versies* zorgen ervoor dat de verscheidene statussen van een product en de bijbehorende gegevens actueel en duidelijk blijven en dat ze in het systeem kunnen worden gevisualiseerd. Dit concept helpt u consistentie te waarborgen, de stuklijsten voor productie te vergrendelen, variabiliteit te elimineren en wijzigingen eenvoudig te identificeren.

Meestal wordt de regel voor *geschiktheid/vorm/functie* toegepast om te bepalen of een wijziging een nieuw product, een nieuwe versie of een update van een bestaande versie vereist. Elk van de drie termen in de naam van deze regel verwijst naar een specifiek aspect van een onderdeel, waarmee technici onderdelen aan behoeften kunnen koppelen. De regel voor geschiktheid/vorm/functie vergroot de flexibiliteit van ontwerpwijzigingen omdat minimale documentatie- en ontwerpkosten nodig zijn om een onderdeel te wijzigen, op voorwaarde dat de geschiktheid/vorm/functie van het product behouden blijven.

- **Geschiktheid** verwijst naar de mogelijkheid van het onderdeel of kenmerk om te worden verbonden met of gekoppeld aan een andere onderdeel of kenmerk van een assemblage. De geschiktheid zorgt ervoor dat het onderdeel aan de vereiste assemblagetoleranties voldoet, zodat dit nuttig kan zijn.
- **Vorm** verwijst naar kenmerken van een onderdeel of assemblage, zoals de externe afmetingen, het gewicht, de grootte en het uiterlijk. De vorm is het aspect dat het meest wordt beïnvloed door de esthetische keuzes van een technicus. Het gaat om de behuizing, het chassis en het bedieningspaneel, die gezamenlijk het 'gezicht' van het product worden.
- De **functie** is een criterium waaraan wordt voldaan als het onderdeel het aangegeven doel effectief en betrouwbaar uitvoert. In een elektronicaproduct kan de functie bijvoorbeeld afhankelijk zijn van de vaste bestanddelen en de software of firmware die worden gebruikt. Het is vaak ook afhankelijk van de functies van de geselecteerde behuizing. Twee van de meestvoorkomende oorzaken voor het niet voldoen aan het functiecriterium voor behuizingen zijn niet goed geplaatste poorten of poorten met een onjuiste grootte en misleidende of ontbrekende labels. 

## <a name="engineering-versions"></a>Engineeringversies

Wanneer u werkt met technische producten, heeft elk product minstens één technische versie. De oorspronkelijke technische versie wordt automatisch gemaakt wanneer u een technisch product maakt. Voor elke technische versie worden de technisch relevante gegevens opgeslagen die specifiek zijn voor die versie. Hier volgen enkele voorbeelden van dergelijke gegevens:

- Het versienummer en vorige versienummer (indien van toepassing)
- De begin- en einddatum
- De actieve status van de productversie, waarmee wordt aangegeven of de versie kan worden vrijgegeven en gebruikt in transacties (zie [Productgereedheid](product-readiness.md) voor meer informatie)
- Het technische bedrijf dat het product heeft gemaakt en hiervan eigenaar is (zie [Technische bedrijven en regels voor gegevenseigendom](engineering-org-data-ownership-rules.md) voor meer informatie)
- Gerelateerde technische documenten, zoals assemblagehandboek, gebruikersinstructies, afbeeldingen en koppelingen
- De technische kenmerken (zie [Technische kenmerken en de zoekfunctie voor technische kenmerken](engineering-attributes-and-search.md) voor meer informatie)
- De technische stuklijsten
- De technische routes

U kunt deze gegevens bijwerken voor een bestaande versie of een nieuwe versie maken met behulp van een *order voor technische wijzigingen*. (Zie [Wijzigingen in technische producten beheren](engineering-change-management.md) voor meer informatie). Als u een nieuwe versie van een product maakt, kopieert het systeem alle technisch relevante gegevens naar die nieuwe versie. Vervolgens kunt u de gegevens voor die nieuwe versie wijzigen. Op deze manier kunt u specifieke gegevens voor elke opeenvolgende versie bijhouden. Als u de verschillen tussen opeenvolgende technische versies wilt vergelijken, inspecteert u de order voor technische wijzigingen, die typewijzigingen bevatten die alle wijzigingen aangeven.

Zoals aangegeven wordt de oorspronkelijke technische versie automatisch gemaakt wanneer u een technisch product maakt. Het versienummer voor deze versie volgt de regel voor versienummer die is gedefinieerd in de technische categorie voor het product. Als u naar een volgende versie wilt overstappen, moet u het product toevoegen als een regel aan een order voor technische wijzigingen toevoegen en het veld **Impact** instellen op *Nieuwe versie*. De order voor technische wijzigingen bevat de details van de wijziging van de huidige versie naar de volgende versie.

Houd er rekening mee dat een technisch product slechts in één order voor technische wijzigingen tegelijk kan worden opgenomen. Deze beperking zorgt voor een nauwkeurigheid van de gegevens en voorkomt overlappende of tegenstrijdige wijzigingen in het product. Het veld **Technicus** in de weergave **Koptekst** van de order voor technische wijzigingen toont de technicus die verantwoordelijk is voor de wijzigingsorder. Als de technicus bij een team hoort dat in het systeem is gedefinieerd, wordt in het veld **Verantwoordelijke** de leider van dat team weergegeven.

## <a name="track-versions-in-transactions"></a>Versies in transacties traceren

Wanneer u Technisch wijzigingsbeheer gebruikt, bevatten productmodelgegevens altijd een of meer technische versies. Bij het instellen van technische producten kunt u kiezen of de technische versie ook deel uitmaakt van *logistieke transacties*. (Zie het gedeelte [Categorieën voor technische producten instellen](#product-category) verderop in dit onderwerp). Als de logistieke impact relevant is, verschilt deze per product en per bedrijf. Soms wordt alleen de laatste versie van een product gebruikt. In dat geval kan de vorige versie niet meer worden gebruikt wanneer u een nieuwe versie introduceert. In andere gevallen is de vorige versie vereist in logistieke transacties om de volgende uitdagingen te overwinnen:

- De afdeling Logistiek moet twee stuks van een product naar een klant verzenden. In dit geval moet u beslissen of u twee verschillende versies wilt laten verzenden.
- Later wordt ontdekt dat er een probleem optreedt en dat het is gerelateerd aan een bepaalde wijziging. In dit geval kan het nuttig zijn om exact te kunnen bepalen welke versie in elke order is verzonden.
- Bedrijven willen doorgaans eerst oude versies verzenden, om deze geleidelijk uit voorraad te krijgen. Vooral voor producten met een laag volume kan deze aanpak vaak worden beheerd door de ingangsdatums van de nieuwe versie te bepalen ten opzichte van voorspellingen over wanneer voorraad van de oude versie op is. Soms is het echter niet mogelijk om deze vergelijking te maken of u kunt de voorspellingen van het voorraadniveau te onzeker vinden.

De beslissing of u versies zichtbaar wilt maken in voorraad, is afhankelijk van factoren zoals eerder vermeld, plus bedrijfspraktijken en andere aspecten die specifiek zijn voor elk bedrijf. U kunt het gedrag voor de *categorie voor technische producten* opgeven. Dit wordt vervolgens toegepast op alle producten die op basis van die categorie worden gemaakt, voor alle bedrijven waaraan het product is vrijgegeven.

Voor producten die zo zijn ingesteld dat ze logistieke impact hebben, moet de technische versie worden opgegeven voor elke transactie. Hoewel het systeem de *meest recente actieve versie* voorstelt, kunt u kiezen uit alle actieve versies die voor het bedrijf beschikbaar zijn. Voor producten die zo zijn ingesteld dat ze geen logistieke impact hebben, wordt de technische versie niet opgegeven voor transacties. Het systeem gebruikt echter de laatste actieve versie. Wanneer u een product aan een productiestuklijst toevoegt, wordt bijvoorbeeld de meest recente versie gebruikt en wanneer u de hoofdplanning uitvoert, wordt uitgegaan van de nieuwste versie.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Categorieën voor technische producten instellen

Een categorie voor technische producten vormt een basis voor het maken van een specifiek technisch product. Elke categorie brengt een set standaardwaarden en -beleid met zich mee. Daarom moet u bij het maken van een technisch product eerst de categorie selecteren waarin u deze wilt maken.

Er wordt automatisch een nieuw type categoriehiërarchie (*hiërarchie van technische product*) voor u ingesteld. U kunt de categorieën handmatig maken door naar **Technisch wijzigingsbeheer \> Instellen \> Details van categorieën voor technische producten** te gaan.

Elke categorie voor technische producten bepaalt het standaardgedrag van de technische producten die op basis van die categorie worden gemaakt. Nadat u een technisch product hebt gemaakt, kunt u de categorie niet meer wijzigen. Als u de verkeerde categorie selecteert, kunt u het product wel verwijderen en opnieuw maken.

Wanneer een categorie voor technische producten wordt gemaakt, kunt u de volgende instellingen niet wijzigen:

- Technisch bedrijf
- Producttype
- Subtype product
- Productdimensiegroep
- Configuratietype
- Versienummerregel

Andere instellingen kunnen standaardwaarden overnemen die zijn ingesteld voor de categorie voor technische producten. Volgens de systeemregels kunnen deze waarden echter worden gewijzigd.

Als u met categorieën voor technische producten wilt werken, gaat u naar **Technisch wijzigingsbeheer \> Instellen \> Details van categorieën voor technische producten**. Voer vervolgens een van deze stappen uit.

- Als u een nieuwe categorie wilt maken, selecteert u **Nieuw** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaande categorie wilt bewerken, selecteert u deze in het lijstvenster, selecteert u **Bewerken** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaande categorie wilt verwijderen, selecteert u deze in het lijstvenster en selecteert u **Verwijderen** in het actievenster.

### <a name="header"></a>Koptekst

Stel de volgende velden in de koptekst van een categorie voor een technisch product in.

| Veld | Beschrijving |
|---|---|
| Naam | Voer een naam in voor de categorie voor technische producten. |
| Technisch bedrijf | Selecteer het technische bedrijf waar producten in deze categorie voor technische producten kunnen worden gemaakt en waar ze worden onderhouden. |

### <a name="details-fasttab"></a>Het sneltabblad Details

Stel de volgende velden op het sneltabblad **Details** van een categorie voor een technisch product in.

| Veld | Beschrijving |
|---|---|
| Producttype | Selecteer of de categorie van toepassing is op producten of services. |
| Versies in transacties traceren | Selecteer of de versie van het product moet worden vermeld voor alle transacties (logistieke gevolgen). Als u de versie in transacties bijhoudt, geeft elke verkooporder bijvoorbeeld aan welke specifieke versie van het product in die verkooporder is verkocht. Als u de versie in transacties niet bijhoudt, wordt in verkooporders niet aangegeven welke specifieke versie is verkocht. In plaats daarvan wordt altijd de meest recente versie weergegeven.<ul><li>Als deze optie is ingesteld op *Ja*, wordt een productmodel gemaakt voor het product en is elke versie van het product een variant die de productdimensie *versie* gebruikt. Het veld **Subtype van product** wordt automatisch ingesteld op *Productmodel* en u moet een productdimensiegroep selecteren waarvoor de dimensie *versie* actief is. Alleen productdimensiegroepen waarvoor *versie* een actieve dimensie is, worden weergegeven. U kunt nieuwe productdimensiegroepen maken door de knop **Bewerken** (potloodsymbool) te selecteren.</li><li>Als deze optie is ingesteld op *Nee*, wordt de productdimensie *versie* niet gebruikt. U kunt vervolgens selecteren of u een product of een productmodel wilt maken waarin de andere dimensies worden gebruikt.</li></ul><p>Deze optie wordt vaak gebruikt voor producten waarvoor een kostenverschil bestaat tussen versies of producten waar verschillende voorwaarden van toepassing zijn met betrekking tot de klant. Het is daarom belangrijk om aan te geven welke versie in elke transactie is gebruikt.</p> |
| Subtype product | Selecteer of de categorie producten of productmodellen bevat. Voor productmodellen worden productdimensies gebruikt.
| Productdimensiegroep | Met de instelling **Versies in transacties traceren** kunt u het subtype van het product selecteren. Als u hebt opgegeven dat u de versie in transacties wilt bijhouden, worden de productdimensiegroepen weergegeven waarvoor de dimensie *versie* wordt gebruikt. Anders worden alleen productdimensiegroepen weergegeven waarvoor de dimensie *versie* niet wordt gebruikt. |
| Status in productlevenscyclus na aanmaken | Stel de standaard levenscyclusstatus in die een technisch product moet hebben wanneer het voor het eerst wordt gemaakt. Zie voor meer informatie [Levenscyclusstatussen en transacties van producten](product-lifecycle-state-transactions.md). |
| Versienummerregel | Selecteer de versienummerregel die van toepassing is op de categorie:<ul><li>**Handmatig**: u kiest het versienummer voor elke nieuwe versie.</li><li>**Automatisch**: het versienummer wordt ingesteld op basis van een indeling die u definieert. Wanneer u de notatie instelt, gebruikt u een hekje (\#) om een cijfer aan te duiden en elk ander teken voor een constante waarde. Als u de notatie bijvoorbeeld definieert als *V-\#\#*, is de eerste versie V-01, de tweede V-02, enzovoort.</li><li>**Lijst**: het volgende nummer wordt opgehaald uit een vooraf gedefinieerde lijst met aangepaste waarden die u definieert.</li></ul> |
| Geldigheid afdwingen | Geef op of de ingangsdatums van de technische versies aaneengesloten moeten zijn of dat er hiaten en overlappingen kunnen bestaan. Deze instelling is van invloed op de manier waarop u de velden **Geldig vanaf** en **Geldig tot** kunt gebruiken voor elke technische versie waarop de categorie van toepassing is.<ul><li>Als deze optie is ingesteld op *Ja*, moet er een waarde voor **Geldig vanaf** worden opgegeven voor elke versie en zijn hiaten en overlappingen niet toegestaan tussen versies. Het datumbereik voor elke technische versie is direct verbonden met de vorige en volgende technische versies, indien aanwezig. In dit scenario wordt altijd de nieuwste versie gebruikt en worden oudere versies niet meer gebruikt.</li><li>Als deze optie is ingesteld op **Nee**, gelden er geen beperkingen voor de geldigheidsdatumvelden voor technische versies en zijn zowel overlappingen als hiaten toegestaan. In dit scenario kunnen meerdere versies tegelijk actief zijn en kunt u met elke actieve versie werken.</li></ul><p>Deze optie is ook van invloed op stuklijsten en routes die zijn verbonden met een productversie. Zie de sectie [Stuklijsten en routes verbinden met technische versies](#boms-routes) verderop in dit onderwerp voor meer informatie.</p> |
| Nummerregel van nomenclatuur gebruiken | Stel deze optie in op *Ja* om regels in te schakelen voor het definiëren van een productnummer met behulp van nummerreeksen, namen en waarden van technische kenmerken en tekstconstanten als segmenten. Als u regels wilt maken of wijzigen, selecteert u de knop **Bewerken**. |
| Naamregel van nomenclatuur gebruiken | Stel deze optie in op *Ja* om regels in te schakelen voor het definiëren van een naam met behulp van de namen en waarden van technische kenmerken en tekstconstanten als segmenten. Als u regels wilt maken of wijzigen, selecteert u de knop **Bewerken**. |
| Omschrijvingsregel van nomenclatuur gebruiken | Stel deze optie in op *Ja* om regels in te schakelen voor het definiëren van de beschrijving met behulp van de namen en waarden van technische kenmerken en tekstconstanten als segmenten. Als u regels wilt maken of wijzigen, selecteert u de knop **Bewerken**. |

### <a name="attributes-fasttab"></a>Het sneltabblad Kenmerken

Gebruik het raster op het sneltabblad **Kenmerken** om de technische kenmerken in te stellen die van toepassing zijn op producten die tot deze categorie behoren. Zie [Technische kenmerken en de zoekfunctie voor technische kenmerken](engineering-attributes-and-search.md) voor meer informatie over het maken van technische kenmerken.

Gebruik de knoppen op het sneltabblad **Kenmerken** om kenmerken toe te voegen, te verwijderen en te rangschikken in het raster.

Als u de selectie van kenmerken voor een technische categorie wijzigt en er al producten bestaan die zijn gebaseerd op die categorie, moet u beslissen of u de wijzigingen op deze producten wilt toepassen. Als u wilt dat bestaande producten de wijzigingen weerspiegelen, selecteert u **Bestaande producten bijwerken** op het sneltabblad **Kenmerken**.

Stel de volgende velden in voor elke rij die u toevoegt aan het raster.

| Veld | Beschrijving |
|---|---|
| Naam | Het kenmerk selecteren om toe te voegen. |
| Waarde | De standaardwaarde voor het kenmerk selecteren. |
| Verplicht | Voor kenmerken van het type *Booleaans* moeten gebruikers het kenmerk instellen op *Ja* als deze optie is ingesteld op *Ja*. Als deze optie is ingesteld op *Nee*, kunnen gebruikers het kenmerk instellen op *Ja* of *Nee*. Voor andere gegevenstypen is de instelling van deze optie alleen informatief. |
| Batchkenmerk | Selecteren of het kenmerk moet worden doorgegeven via de batchfunctie. |

### <a name="readiness-policy-fasttab"></a>Het sneltabblad Gereedheidsbeleid

Gebruik het veld **Productgereedheidsbeleid** om het gereedheidsbeleid te selecteren dat van toepassing is op producten die tot deze categorie behoren. Zie voor meer informatie [Productgereedheid](product-readiness.md).

### <a name="release-policy-fasttab"></a>Het sneltabblad Vrijgavebeleid

Gebruik het veld **Productvrijgavebeleid** om het vrijgavebeleid te selecteren dat van toepassing is op producten die tot deze categorie behoren. Zie [Productstructuren van de vrijgave](release-product-structure.md) voor meer informatie.

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Stuklijsten en routes verbinden met technische versies

De instelling van de optie **Geldigheid afdwingen** is belangrijk voor het verbinden van stuklijsten en routes aan elke technische versie. U kunt meerdere stuklijsten of routes per product alleen activeren als er een verschil is met een van de volgende instellingen:

- Productdimensie
- Hoeveelheid
- Locatie
- Geldigheidsdatums

Technische stuklijsten en routes worden gemaakt op basis van de technische versie waarop ze van toepassing zijn. Deze kunnen worden herkend aan het vinkje in het selectievakje **Technisch beheerd**. Wanneer u werkt met technische stuklijsten en routes, kunt u deze meestal niet met verschillende hoeveelheden ontwerpen. Meestal ontwerpt u ook niet verschillende stuklijsten per site. Daarnaast worden de ingangsdatums voor technische stuklijsten en routes altijd uit de technische versie gehaald. Daarom hebben een technische versie, de stuklijst en de route allemaal dezelfde ingangsdatums.

Voor producten waarvoor u de productversie *dimensie* gebruikt (samen met logistieke impact op de transacties) wordt de versie ook toegevoegd aan de stuklijsten en routes. Dit gedrag zorgt voor het onderscheid tussen stuklijsten en routes van opeenvolgende versies, ongeacht de instelling voor **Geldigheid afdwingen**.

Voor producten waarvoor u de productversie *dimensie* niet gebruikt (zonder logistieke impact op de transacties) wordt de versie niet toegevoegd aan de stuklijsten of routes. Daarom is er geen verschil tussen de stuklijsten en routes van opeenvolgende versies. In dit geval is het raadzaam de optie **Geldigheid afdwingen** in te stellen op *Ja*. Op deze manier voorkomt u dat technische versies elkaar overlappen. U kunt ook de stuklijst en route van een nieuwere versie activeren zonder eerst de stuklijst en route van de vorige versie te deactiveren. Als u in dit geval de optie **Geldigheid afdwingen** op *Ja* instelt, moet u de stuklijsten en routes van oudere versies handmatig uitschakelen voordat u de meest recente versie kunt activeren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
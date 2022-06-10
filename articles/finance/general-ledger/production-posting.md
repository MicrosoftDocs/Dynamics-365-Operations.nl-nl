---
title: Productieorders boeken
description: Dit onderwerp bevat informatie over verschillende typen boekingen van productieorders.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: cd1b6c49e59f9480fd831ad5ff143033ca09792c
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/24/2022
ms.locfileid: "8802995"
---
# <a name="production-postings"></a>Productieorders boeken

Dit onderwerp bevat informatie over verschillende typen boekingen in het productieorderproces.


## <a name="material-consumption"></a>Materiaalverbruik

Materialen worden geregistreerd als verbruikt tijdens de productie wanneer de lijst van het productieorderverzamellijstjournaal is geboekt. Hiermee worden transacties gemaakt waarmee de voorhanden voorraad wordt afgetrokken. Bij **Productieparameters** kunt u opgeven of de waarde van grondstoffen die worden uitgevoerd (zogenaamd OHW/onderhanden werk) in het grootboek moeten worden geboekt.

De waarde van grondstoffen die in uitvoering zijn (OHW) wordt geboekt naar de rekeningen **Kostenraming van verbruikt materiaal** en **Geraamde kosten van verbruikte materialen, OHW**. Het orderverzamellijstproces voor de productieorder is een fysieke update van de voorraadtransacties die zijn gerelateerd aan de productieorder. Wanneer een productieorder wordt geregistreerd als beëindigd, worden de fysieke transacties ongedaan gemaakt en worden de gerelateerde voorraadtransacties financieel bijgewerkt. Wanneer het eindjournaal wordt geboekt, worden de boekingstypen **Kosten van verbruikte materialen** en **Kosten van verbruikte materialen, OHW** gebruikt.

Met het tabblad **Productie** op de pagina **Voorraadboekingsprofielen** wordt bepaald hoe productieorders naar het grootboek worden geboekt. Dit wordt gebruikt wanneer het veld **Boeking in grootboek** wordt ingesteld op **Artikel en resource** of **Artikel en categorie** op de pagina **Parameters van productiebeheer**. 

Als u een orderverzamellijstjournaal wilt boeken naar het grootboek voor een productieorder, moet er aan de volgende voorwaarden zijn voldaan:

-   Het selectievakje **Orderverzamellijst in grootboek boeken** moet zijn ingeschakeld op de pagina **Parameters van productiebeheer**. Deze instelling kan worden overschreven voor een specifieke site op de pagina **Parameters van productiebeheer per site**.
-   Het selectievakje **Fysieke voorraad boeken** moet zijn ingeschakeld op de pagina **Artikelmodelgroepen** voor het artikel dat op de inkooporderregel is geselecteerd.
-   Op de pagina **Voorraadboekingsprofiel** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
    -   **Kostenraming van verbruikt materiaal**
    -   **Geraamde kosten van verbruikte materialen, OHW**

## <a name="time-consumption"></a>Tijdverbruik

De tijd die werknemers besteden aan productietaken wordt geregistreerd in het **Routekaartjournaal** of het **Taakkaartjournaal**. Wanneer deze journalen worden geboekt, wordt de grootboekboeking naar een specifieke rekening voor resources die worden uitgevoerd (OHW) verwerkt. Deze boeking staat voor de waarde van de tijd die is besteed aan de productieorder. Nadat de productieorder als beëindigd is geregistreerd, worden de OHW-rekeningen vereffend.

Er zijn drie manieren om tijdverbruik te boeken, afhankelijk van de optie die is geselecteerd in het veld **Grootboekboeking** op de pagina **Parameters van productiebeheer**.

## <a name="reporting-finished-goods-and-error-quantities"></a>Afgewerkte goederen en fouthoeveelheden rapporteren

Wanneer een productieorder **Gereedgemeld** is, worden de eindproducten die zijn voltooid in de voorraad bijgewerkt via het journaal **Als gereed rapporteren**. Als u OHW-boekhouding gebruikt, wordt een grootboekjournaal geboekt om de OHW-rekeningen te verlagen en de voorraad van eindproducten te verhogen. In het journaal worden de standaardkosten gebruikt die voor het product zijn gedefinieerd. Als de optie **Geschatte kostprijs gebruiken** is geselecteerd op de pagina **Parameters van productiebeheer**, worden de geschatte kosten van de productieorder gebruikt.

De waarde van grondstoffen die in uitvoering zijn (OHW) wordt geboekt naar de rekeningen **Raming van productiekosten** en **Geraamde productiekosten, OHW**. Het proces **Als gereed rapporteren** voor de productieorder is een fysieke update van de voorraadtransacties die zijn gerelateerd aan de productieorder. Wanneer een productieorder wordt beëindigd, worden de fysieke transacties ongedaan gemaakt en worden de gerelateerde voorraadtransacties financieel bijgewerkt. Wanneer het eindjournaal wordt geboekt, worden de boekingstypen **Productiekosten** en **Productiekosten, OHW** gebruikt.

Het tabblad **Productie** op de pagina **Voorraadboekingsprofielen** wordt gebruikt om te bepalen hoe productieorders naar het grootboek worden geboekt. Dit wordt gebruikt wanneer het veld **Boeking in grootboek** wordt ingesteld op **Artikel en resource** of **Artikel en categorie** op de pagina **Parameters van productiebeheer**. Het sneltabblad **Grootboek - artikelen** op de pagina **Productiegroepen** kan ook worden gebruikt om de boeking voor productieorders te beheren wanneer het veld wordt ingesteld op **Productiegroepen**.

Als u een **Als gereed rapporteren**-journaal wilt boeken naar het grootboek voor een productieorder, moet er aan de volgende voorwaarden zijn voldaan:
-   Het selectievakje **Gereedmelding in grootboek boeken** moet zijn ingeschakeld op de pagina **Parameters van productiebeheer**. Deze instelling kan worden overschreven voor een specifieke site op de pagina **Parameters van productiebeheer per site**.
-   Het selectievakje **Fysieke voorraad boeken** moet zijn ingeschakeld op de pagina **Artikelmodelgroepen** voor het artikel dat op de inkooporderregel is geselecteerd.
-   Op de pagina **Voorraadboekingsprofiel** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
    -   **Raming van productiekosten**
    -   **Geraamde productiekosten, OHW**

## <a name="ending-the-production-order"></a>De productieorder beëindigen

Voordat een productieorder wordt beëindigd, worden de werkelijke kosten berekend voor de geproduceerde hoeveelheid. Alle geraamde kosten van materiaal, arbeid en overhead worden teruggeboekt en worden vervangen door de werkelijke kosten. De algehele kosten van het eindproduct worden gedebiteerd op de rekening **Productiekosten** en gecrediteerd op de rekening **Productiekosten, OHW**. De materialen die zijn verbruikt tijdens de productieorder, worden gecrediteerd op de **Kosten van verbruikte materialen** en gedebiteerd op de rekening **Kosten van verbruikte materialen, OHW**.

Als u het selectievakje **Taak beëindigen** inschakelt bij het uitvoeren van de kostenberekening, wordt de status van de productieorder gewijzigd in **Beëindigd**. Deze status wordt voorkomen dat extra kosten onbedoeld op een voltooide productieorder worden geboekt. U kunt opgeven dat de waarde van slechte hoeveelheden die tijdens het rapporteren gereedgemeld zijn, moeten worden toegewezen aan de goede hoeveelheden die gereedgemeld zijn. U kunt ook opgeven dat de waarde van slechte hoeveelheden naar een specifieke uitvalrekening moeten worden geboekt. 

Voer de volgende stappen uit om een specifieke uitvalrekening op te geven:
1.  Ga naar **Productiebeheer** > **Instellingen** > **Parameters van productiebeheer**.
2.  Selecteer het tabblad **Standaardupdate**.
3.  Selecteer **Uitvalrekening** in het veld **Uitvalmethode**.
4.  Selecteer in het veld **Uitvalrekening** de hoofdrekening waar de uitval voor slechte hoeveelheid moet worden geboekt wanneer de productieorder wordt beëindigd. Selecteer bijvoorbeeld een onkostenrekening, zoals 510380: productie-uitval.

Als u het eindjournaal wilt boeken naar het grootboek voor een productieorder, moet er aan de volgende voorwaarden zijn voldaan:
-   Op de pagina **Voorraadboekingsprofiel** of **Productiegroepen** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
    -   **Kosten van verbruikte materialen**
    -   **Kosten van verbruikte materialen, OHW**
    -   **Productiekosten**
    -   **Productiekosten, OHW**
-   De hoofdrekeningen moeten voor de volgende typen worden opgegeven op de pagina **Kostencategorieën**, **Resources** of **Resourcegroepen**:
    -   **Geabsorbeerde productiekosten**
    -   **Kosten van verbruikte productie, OHW**

## <a name="indirect-costs-for-production-orders"></a>Indirecte kosten voor productieorders

Wanneer u transacties voor een productieorder verwerkt, kunt u indirecte kosten configureren om overheadkosten of extra kosten in uw grootboek vast te leggen. Fysieke transacties voor indirecte kosten worden in de voorraad toegerekend wanneer u een orderverzamellijstjournaal of een gereedmeldingsjournaal boekt. Financiële transacties voor indirecte kosten worden in de voorraad toegerekend wanneer u het eindjournaal boekt.

U kunt indirecte kosten in uw tijdverbruik gerelateerd aan **Routekaartjournaal** of **Taakkaartjournaal** toerekenen. Deze transacties worden tegengeboekt en geboekt naar de financiële rekeningen wanneer u de productieorder beëindigt. Ga voor meer informatie naar [Kostprijsberekeningsbladen](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Het niveau van het grootboek beheren

Op de pagina **Parameters van productiebeheer** kunt u het veld **Boeking in grootboek** gebruiken om het niveau van grootboekboeking voor productieprocessen in te stellen. 

De volgende velden zijn beschikbaar:

### <a name="item-and-resource"></a>Artikel en resource

Wanneer u de optie **Artikel en resource** selecteert in het veld **Boeking in grootboek**, zijn de boekingsrekeningen afkomstig van de resource of resourcegroep in de bewerking in de route. Rekeningen van de specifieke resource zijn de eerste boekingsoptie. Als er geen rekening wordt opgegeven, worden de rekeningen gebruikt die in de resourcegroep zijn opgegeven. Elke bewerkingsregel in een route kan één resource hebben opgegeven als de **Kostprijsresource**. Deze resource wordt gebruikt voor het bepalen van de rekening die moet worden gebruikt. Deze optie wordt vaak gebruikt wanneer een organisatie bedrijfskosten aan de resources toewijst. Kosten zijn vaak hoger voor de resources en worden gebruikt bij het nemen van koop-/maakbeslissingen. Dit is de meest gedetailleerde boekingsconfiguratie en biedt de meest uitgebreide controle op de boekingen en zeer gedetailleerde analyses van het productieproces.

### <a name="item-and-category"></a>Artikel en categorie

Wanneer u de optie **Artikel en categorie** selecteert in het veld **Boeking in grootboek**, zijn de boekingsrekeningen afkomstig van de pagina **Kostencategorie** die aan elke regel in de route is gerelateerd. Elke bewerkingsregel in de route kan drie kostencategorieën hebben: **Insteltijd**, **Uitvoeringstijd** en **Hoeveelheid**. Deze optie wordt vaak gebruikt wanneer de belangrijkste focus van uw organisatie ligt op procesefficiëntie en activiteitsduur. Deze optie is een beknopte manier van boeken en biedt nog steeds een manier om kosten in categorieën te groeperen.

### <a name="production-group"></a>Productiegroep

Wanneer u de optie **Productiegroepen** selecteert in het veld **Boeking in grootboek**, zijn de boekingsrekeningen afkomstig van de pagina **Productiegroepen**. **Productiegroepen** worden meestal gebruikt wanneer meerdere productieregels vergelijkbare producten gebruiken of een vergelijkbare uitrusting hebben. U kunt deze optie gebruiken om de kosten van de verschillende productiegroepen met elkaar te vergelijken.  
  
> [!NOTE]
> Als de standaardmethode voor het berekenen van de kosten van het afgewerkte artikel wordt gebruikt, komt dit terug in de definitieve transacties. AIs de werkelijke kosten en de kosten die met de standaardmethode zijn berekend verschillen, worden de verschillen geboekt naar de rekening waarop de winst of het verlies is te zien.

### <a name="route-groups-and-ledger-posting"></a>Routegroepen en boeking in grootboek

Voor elke bewerkingsregel in een route is een **Routegroep** opgegeven. De velden **Insteltijd**, **Uitvoeringstijd** en **Hoeveelheid** in de **Routegroep** in de groep **Raming en kostprijsberekening** worden gebruikt om te bepalen of de tijd wordt gebruikt voor kostprijsberekening bij het boeken van een **Taakkaartjournaal** of **Routekaartjournaal** op de productieorder. Als de opties zijn uitgeschakeld, wordt er geen boekstuk gemaakt in het grootboek voor het tijdverbruik.

Als u een **Routekaartjournaal** of **Taakkaartjournaal** wilt boeken naar het grootboek voor een productieorder, moet er aan de volgende voorwaarden zijn voldaan:

-   Het veld **Insteltijd**, **Uitvoeringstijd** of **Hoeveelheid** moet worden geselecteerd in de groep **Raming en kostprijsberekening** op de pagina **Routegroep**.
-   Op de pagina **Kostencategorie**, **Route**, **Routegroep** of **Productiegroepen** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
    -   Geraamde geabsorbeerde productiekosten
    -   Geraamde kosten van verbruikte productie, OHW

In het volgende diagram wordt de relatie van de routegroep tot de berekening van de totale kosten voor elke bewerking (routeregel) in een bepaalde route weergegeven. Elke routeregel heeft één routegroep. Met de routegroep worden parameters voor insteltijd, uitvoeringstijd en hoeveelheid beheerd. Op het tabblad **Kostencategorie** zijn drie opties beschikbaar voor **Instellen**, **Uitvoeren** en **Hoeveelheid** die worden ingeschakeld op basis van de instelling van de routegroepen. Het sneltabblad **Timings** bevat drie velden die zijn gebaseerd op de routegroep.

De formule die wordt gebruikt, is gebaseerd op de vraag of de optie is ingeschakeld in de routegroep. De kosten van de geselecteerde kostencategorie worden vermenigvuldigd met de hoeveelheid die is ingevoerd in de timings bij het berekenen van de totale kosten.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="De relatie van routegroepen met de totale berekende kosten.":::
De relatie van routegroepen met de totale berekende kosten. Elke routeregel heeft één routegroep. Met de routegroep worden parameters voor insteltijd, uitvoeringstijd en hoeveelheid beheerd. Op het tabblad Kostencategorie zijn drie opties beschikbaar voor Instellen, Uitvoeren en Hoeveelheid die worden ingeschakeld op basis van de instelling van de routegroepen. Het sneltabblad Timings bevat drie velden die worden ingeschakeld en waarvan de kosten worden gebaseerd op de routegroep. De formule die wordt gebruikt, is gebaseerd op de vraag of de optie is ingeschakeld in de routegroep. De kosten van de geselecteerde kostencategorie worden vermenigvuldigd met de hoeveelheid die is ingevoerd in de timings bij het berekenen van de totale kosten.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Voorbeeldconfiguratie van boekingsprofiel

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen met voorbeeldhoofdrekeningen en omschrijvingen. 

 - De kolom **Debet/Credit** geeft aan of de transactie meestal debet of credit is of in sommige gevallen ook kan worden geboekt. 
 - De kolom **Vereffeningsrekening** geeft aan of het boekingstype een vereffeningsrekening is. Het bedrag dat op deze rekening wordt geboekt, wordt automatisch teruggeboekt wanneer een latere transactie wordt geboekt. 
 - In de kolom **P/F** verwijst **P** naar fysieke boeking en **F** naar financiële boeking. 
 - De kolom **Volgen** geeft aan of de hoofdrekening voor een bepaald boekingstype gewoonlijk hetzelfde is als een ander boekingstype. De waarde in de kolom geeft het type boeking aan dat normaal gesproken wordt gebruikt.

> [!NOTE]
> De voorgestelde hoofdrekeningen en hoofdrekeningnamen zijn alleen suggesties. Het is raadzaam om samen met uw accountant te bepalen wat de beste configuratie is voor uw bedrijfsbehoeften.


| Boekingstype  | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam| Rekeningtype | Debet/Credit? | Vereffeningsrekening | Fysiek of financieel | Volgen | Description |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Kostenraming van verbruikt materiaal      | 140100               | Materiaalvoorraad        | Activum        | Credit         | Y                | W                     | Kosten van verbruikte materialen                | Deze rekening wordt gebruikt wanneer u een orderverzamellijstjournaal voor een productieorder boekt. De verschuiving op deze rekening betreft de Geraamde kosten van materialen, OHW. Het bedrag op deze rekening wordt automatisch teruggeboekt wanneer de productieorder wordt beëindigd. Deze rekening vertegenwoordigt de voorraadrekening op de balans.       |
| Geraamde kosten van verbruikte materialen, OHW | 150150               | OHW productie – materialen | Activum        | Debet          | Y                | W                     | Geraamde productiekosten, OHW          | Deze rekening wordt gebruikt wanneer u een orderverzamellijstjournaal voor een productieorder boekt. De verschuiving op deze rekening betreft de Geraamde kosten van verbruikte materialen. Het bedrag op deze rekening wordt automatisch teruggeboekt wanneer een productieorder wordt beëindigd. Deze rekening vertegenwoordigt de OHW op uw balans.                  |
| Raming van productiekosten               | 140200               | Voorraad eindproducten   | Activum        | Debet          | Y                | W                     | Productiekosten                         | Deze rekening wordt gebruikt wanneer u een gereedmeldingsjournaal voor een productieorder boekt. De verschuiving op deze rekening betreft de Geraamde productiekosten, OHW. Het bedrag op deze rekening wordt automatisch teruggeboekt wanneer de productieorder wordt beëindigd. Deze rekening vertegenwoordigt de voorraadrekening op de balans. |
| Geraamde productiekosten, OHW          | 150150               | OHW productie – materialen | Activum        | Credit         | Y                | W                     | Productiekosten, OHW                    | Deze rekening wordt gebruikt wanneer u een gereedmeldingsjournaal voor een productieorder boekt. De verschuiving op deze rekening betreft de Geraamde productiekosten. Het bedrag op deze rekening wordt automatisch teruggeboekt wanneer een productieorder wordt beëindigd. Deze rekening vertegenwoordigt de OHW op uw balans.                     |
| Kosten van verbruikte materialen                | 140100               | Materiaalvoorraad        | Activum        | Credit         | N                 | Vr                     | Kostenraming van verbruikt materiaal      | Deze rekening wordt gebruikt om de materialen toe te rekenen die in de productieorder tijdens het beëindigingsproces worden verbruikt. De verschuiving op deze rekening betreft de Kosten van verbruikte materialen, OHW.                                                                                                    |
| Kosten van verbruikte materialen, OHW           | 150150               | OHW productie – materialen | Activum        | Debet          | N                 | Vr                     | Geraamde kosten van verbruikte materialen, OHW | Deze rekening wordt gebruikt om de materialen in OHW toe te rekenen die in de productieorder tijdens het beëindigingsproces worden verbruikt. De verschuiving op deze rekening betreft de Kosten van verbruikte materialen.                                                |
| Productiekosten                         | 140200               | Voorraad eindproducten   | Activum        | Debet          | N                 | Vr                     | Raming van productiekosten               | Deze rekening wordt gebruikt om de kosten van het eindproduct toe te rekenen dat wordt geproduceerd door een productieorder wanneer u de productieorder beëindigt. De verschuiving op deze rekening betreft de rekening Productiekosten, OHW.                                                                  |
| Productiekosten, OHW                    | 150150               | OHW productie – materialen | Activum        | Credit         | N                 | Vr                     | Geraamde productiekosten, OHW          | Deze rekening wordt gebruikt om de kosten van het eindproduct in OHW toe te rekenen dat wordt geproduceerd door een productieorder wanneer u de productieorder beëindigt. De verschuiving op deze rekening betreft de rekening Productiekosten.                                     |

> [!NOTE]
> **OHW-ontvangst van Lean service** en **OHW-vereffeningsrekening van Lean service** worden gebruikt met kostprijsberekening via terugwaarts afboeken voor lean manufacturing. Ga voor meer informatie naar [Kostprijsberekening via terugwaarts afboeken](/supply-chain/cost-management/backflush-costing.md).


---
title: Consolidatiebeleid voor zendingen configureren
description: In dit artikel wordt uitgelegd hoe u standaard- en aangepast consolidatiebeleid voor zendingen instelt.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427977"
---
# <a name="configure-shipment-consolidation-policies"></a>Consolidatiebeleid voor zendingen configureren

[!include [banner](../includes/banner.md)]

In het consolidatieproces voor zendingen waarbij wordt gebruikgemaakt van consolidatiebeleid voor zendingen kunnen zendingen automatisch worden geconsolideerd en handmatig worden vrijgegeven aan het magazijn. Nadat u deze functie hebt ingeschakeld, moet u het initiële beleid configureren. Als er geen beleid is geconfigureerd, wordt voor elke verkoopregel een afzonderlijke verzending met één ladingsregel gegenereerd.

De scenario's die in dit artikel worden weergegeven, laten zien hoe u standaard- en aangepast consolidatiebeleid voor zendingen instelt.

> [!WARNING]
> Als u een upgrade voor een Microsoft Dynamics 365 Supply Chain Management-systeem hebt uitgevoerd waarbij u de verouderde functie voor zendingsconsolidatie gebruikt, werkt de consolidatie mogelijk niet meer zoals u verwacht, tenzij u het hier gegeven advies volgt.
>
> Bij Supply Chain Management-installaties waarbij de functie *Consolidatiebeleid voor zendingen* is uitgeschakeld, kunt u consolidatie van zendingen inschakelen door voor elk magazijn de instelling **Zending bij vrijgave naar magazijn consolideren** te gebruiken. Deze functie is verplicht vanaf versie 10.0.29. Wanneer de functie is ingeschakeld, is de instelling **Zending bij vrijgave naar magazijn consolideren** verborgen. De functionaliteit wordt vervangen door de *beleidsregels voor zendingsconsolidatie*, zoals wordt beschreven in dit artikel. Elke beleidsregel legt consolidatieregels vast en bevat een query om te bepalen waar het beleid van toepassing is. Wanneer u de functie voor de eerste keer inschakelt, worden geen beleidsregels voor consolidatie van zendingen gedefinieerd op de pagina **Consolidatiebeleid voor zendingen**. Wanneer er geen beleid is gedefinieerd, gebruikt het systeem het gedrag van voorheen. Daarom blijft elk bestaand magazijn de instelling **Zending bij vrijgave naar magazijn consolideren** uitvoeren, ook al is die instelling nu verborgen. Maar nadat u ten minste één beleidsregel voor verzendingsconsolidatie hebt gemaakt, heeft de instelling **Zending bij vrijgave naar magazijn consolideren** geen effect meer en wordt de consolidatiefunctionaliteit volledig geregeld door het beleid.
>
> Nadat u ten minste één consolidatiebeleid voor zendingen hebt definiëren, controleert het systeem het consolidatiebeleid telkens wanneer een order wordt vrijgegeven naar het magazijn. Het systeem verwerkt de beleidsregels op basis van de volgorde die is gedefinieerd door de waarde voor **Beleidsreeks** van elk beleid. Het past de eerste beleidsregel toe als de query overeenkomt met de nieuwe order. Als geen query overeenkomt met de order, wordt voor elke verkoopregel een afzonderlijke verzending met één ladingsregel gegenereerd. Daarom is het raadzaam om, als terugval, een standaardbeleidsregel te maken die van toepassing is op alle magazijnen en groepen op ordernummer. Geef dit terugvalbeleid de hoogste waarde voor **Beleidsreeks**, zodat het als laatste wordt verwerkt.
>
> Om het oude gedrag te reproduceren, moet u een beleidsregel maken die niet op ordernummer groepeert en dat querycriteria heeft die alle relevante magazijnen bevatten.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>De functie voor consolidatiebeleid voor zendingen inschakelen

Voordat u de functie *Consolidatiebeleid voor zendingen* kunt gebruiken, moet u deze voor het systeem inschakelen. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Consolidatiebeleid voor zendingen* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a>Uw initiële beleidsregels voor consolidatie van zendingen instellen

Als u werkt met een nieuw systeem of een systeem waarbij u de functie *Consolidatiebeleid voor zendingen* voor de eerste keer hebt ingeschakeld, volgt u deze stappen om uw initiële consolidatiebeleid voor zendingen in te stellen.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Selecteer in het actievenster de optie **Standaardinstelling maken** om het volgende beleid te maken:

    - Een beleid met de naam *Standaard* voor het beleidstype *Verkooporder*.
    - Een beleid met de naam *Standaard* voor het beleidstype *Overboekingsuitgifte*.
    - Een beleid met de naam *CrossOrder* voor het beleidstype *Overboekingsuitgifte*. (Dit beleid wordt alleen gemaakt als u minimaal één magazijn had waarvoor de oude instelling **Zending bij vrijgave naar magazijn consolideren** was ingeschakeld.)
    - Een beleid met de naam *CrossOrder* voor het beleidstype *Verkooporder*. (Dit beleid wordt alleen gemaakt als u minimaal één magazijn had waarvoor de oude instelling **Zending bij vrijgave naar magazijn consolideren** was ingeschakeld.)

    > [!NOTE]
    > - Beide *CrossOrder*-beleidsregels nemen dezelfde reeks velden mee voor verwerking. Ze nemen echter ook het veld Ordernummer mee. (Dat veld wordt gebruikt om regels in zendingen te consolideren, op basis van factoren zoals het magazijn, de leveringsmethode en het adres.)
    > - Beide *Standaard*-beleidsregels nemen dezelfde reeks velden mee voor verwerking. Ze nemen echter ook het veld Ordernummer mee. (Dat veld wordt gebruikt om regels in zendingen te consolideren, op basis van factoren zoals het ordernummer, de leveringsmethode en het adres.)

1. Als het systeem een beleidsregel *CrossOrder* heeft gegenereerd voor het beleidstype *Verkooporders*, selecteer deze dan en selecteer vervolgens in het actievenster de optie **Query bewerken**. In de query-editor kunt u zien voor welke magazijnen de instelling **Zending bij vrijgave naar magazijn consolideren** eerder was ingeschakeld. Daarom reproduceert deze beleidsregel uw eerdere instellingen voor deze magazijnen.
1. Pas het nieuwe standaardbeleid waar nodig aan door velden toe te voegen of te verwijderen en/of de query's te bewerken. U kunt ook zoveel nieuwe beleidsregels toevoegen als u nodig hebt. Voor voorbeelden die laten zien hoe u het beleid kunt aanpassen en configureren, bekijkt u het voorbeeldscenario later in dit artikel.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Scenario: Aangepast beleid voor consolidatie van zendingen configureren

Dit scenario geeft een voorbeeld waarin u kunt zien hoe u aangepaste consolidatiebeleidsregels voor zendingen instelt en deze vervolgens test met de demogegevens. Aangepast beleid kan complexe bedrijfsvereisten ondersteunen, waarbij consolidatie van de zending afhankelijk is van verschillende voorwaarden. Voor elk voorbeeldbeleid verderop in dit scenario wordt een korte omschrijving van het bedrijfsscenario opgenomen. Deze voorbeelden van beleidsregels moeten worden ingesteld in een volgorde die een piramideachtige evaluatie van de query's waarborgt. (Met andere woorden, de beleidsregels met de meeste voorwaarden moeten worden geëvalueerd met de hoogste prioriteit.)

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Dit scenario verwijst naar waarden en records die zijn opgenomen in de [standaarddemogegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) die voor Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op *USMF* voordat u begint.

### <a name="prepare-master-data-for-this-scenario"></a>Hoofdgegevens voorbereiden voor dit scenario

Voordat u de oefeningen in dit scenario kunt doorlopen, moet u de vereiste hoofdgegevens voor het filteren voorbereiden, zoals wordt beschreven in de volgende subsecties. (Deze vereisten zijn ook van toepassing op de scenario's die worden vermeld in de sectie [Voorbeeldscenario's voor het gebruik van consolidatiebeleid voor zendingen](#example-scenarios).)

#### <a name="create-two-new-product-filter-codes"></a>Twee nieuwe productfiltercodes maken

1. Ga naar **Magazijnbeheer \> Instellen \> Productfilters \> Productfilters** en voeg twee productfilters toe:

    - Productfilter 1:

        - **Filtercode:** *Ontvlambaar*
        - **Filtertitel:** *Code 4*

    - Productfilter 2:

        - **Filtercode:** *Explosief*
        - **Filtertitel:** *Code 4*

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het product met artikelnummer *M9200*. (Het product dat u selecteert, moet zijn ingeschakeld voor geavanceerde \[WMS\]-magazijnprocessen en dit product is vooraf ingeschakeld voor WMS-processen in de **USMF**-demogegevens.)
1. Stel op het sneltabblad **Magazijn** het veld **Code 4** in op *Ontvlambaar*.
1. Sluit de pagina.
1. Open het product met artikelnummer *M9201*. (Dit product is ook vooraf ingeschakeld voor WMS-processen in de **USMF**-demogegevens.)
1. Stel op het sneltabblad **Magazijn** het veld **Code 4** in op *Explosief*.
1. Sluit de pagina.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Een nieuwe transportmodus voor levering maken

1. Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Modus**.
1. Maak een transportmodus die wordt gebruikt in consolidatiequery's en noem deze *Airways*.
1. Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Vervoerders**.
1. Maak een vervoerder met de volgende instellingen:

    - **Vervoerder:** *Airways*
    - **Naam:** *Airways*
    - **Modus:** *Airways*

1. Voeg op het sneltabblad **Services** voor de nieuwe vervoerder een rij toe met de volgende instellingen:

    - **Vervoerdersservice:** *Air*
    - **Transportmethode:** *Air*

1. Selecteer **Opslaan** in het actievenster.

    > [!NOTE]
    > Wanneer u de nieuwe vervoerder opslaat, wordt het veld **Leveringsmethode** voor de nieuwe rij in het raster **Services** automatisch ingesteld op *Airwa-Air*. Wanneer u de leveringsmethode *Airwa-Air* gebruikt voor een verkooporder, wordt de transportmodus *Airways* gebruikt voor gerelateerde zendingen.

#### <a name="create-an-order-pool"></a>Een ordergroep maken

1. Ga naar **Verkoop en marketing \> Instellingen \> Verkooporders \> Ordergroepen**.
1. Maak een ordergroep die wordt gebruikt voor de consolidatiequery. Deze ordergroep moet de volgende instellingen hebben:

    - **Groep:** voer een geheel getal in dat nog niet wordt gebruikt door andere groepen.
    - **Naam:** *ShipCons*

1. Ga naar **Verkoop en marketing \> Klanten \> Alle klanten**.
1. Open de klant met het rekeningnummer *US-003*.
1. Stel op het sneltabblad **Standaardwaarden verkooporders** het veld **Verkooporderpool** in op de ordergroep die u zojuist hebt gemaakt.
1. Sluit de pagina en herhaal de stappen 4 en 5 voor de klant met het rekeningnummer *US-004*.

### <a name="create-example-policy-1"></a>Voorbeeldbeleid 1 maken

In dit voorbeeld maakt u een beleid *Klant+modus* dat kan worden gebruikt voor het volgende bedrijfsscenario:

- Met het beleid wordt een query uitgevoerd voor een specifieke klantrekening (*US-001*) en een specifieke leveringsmethode (*Airwa-Air*).
- Consolidatie met openstaande zendingen is uitgeschakeld.
- Consolidatie wordt uitgevoerd per order-id. (Met andere woorden: er zijn afzonderlijke zendingen per order, magazijn, enzovoort.)

Voer de volgende stappen uit om het beleid voor consolidatie van de zending te maken voor dit bedrijfsscenario.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Stel het veld **Beleidstype** in op *Verkooporders*.
1. Selecteer in het actievenster de optie **Nieuw** om een beleid te maken met de volgende instellingen:

    - **Beleidsnaam:** *CustomerMode*
    - **Beleidsbeschrijving:** *Klantrekening en leveringsmethode*

1. Laat de optie **Consolideren met openstaande zendingen** ingesteld op *Nee*.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer op het sneltabblad **Consolidatievelden** in de lijst **Resterende velden** de rij waarin het veld **Veldnaam** is ingesteld op *Leveringsmethode*.
1. Selecteer de knop **Toevoegen** ![pijl naar rechts.](media/forward-button.png) om het veld naar de lijst **Geselecteerde velden** te verplaatsen.
1. Selecteer **Query bewerken** in het actievenster.
1. Zoek in het dialoogvenster van de query-editor op het tabblad **Bereik** in het raster de rij waar het veld **Veld** is ingesteld op *Klantrekening* en stel het veld **Criteria** voor die rij in op *US-001*.
1. Selecteer **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:

    - **Tabel:** *Orderregels*
    - **Afgeleide tabel:** *Orderregels*
    - **Veld:** *Leveringsmethode*
    - **Criteria:** *Airwa-Air*

1. Selecteer **OK** om het dialoogvenster te sluiten.

> [!NOTE]
> Voor dit bedrijfsscenario worden orderregels voor de klant *US-001* die gebruikmaken van de leveringsmethode *Airwa-Air* niet geconsolideerd tussen orders. Dit beleid is bedoeld om eerst in een reeks te worden gebruikt, in gevallen waarin zendingen voor alle andere leveringsmethoden voor deze klant worden geconsolideerd.

### <a name="create-example-policy-2"></a>Voorbeeldbeleid 2 maken

In dit voorbeeld maakt u een beleid *Gevaarlijke goederen* dat kan worden gebruikt voor het volgende bedrijfsscenario:

- Met het beleid wordt een query uitgevoerd voor een specifieke filtercode (*gevaarlijk*) en een specifieke leveringsmethode (*Airwa-Air*).
- Consolidatie met openstaande zendingen is ingeschakeld.
- Consolidatie wordt uitgevoerd tussen orders. (Met andere woorden: er zijn afzonderlijke zendingen per rekening, magazijn, enzovoort, maar alleen binnen de artikelgroep die is opgegeven in de query.)

Voer de volgende stappen uit om het beleid voor consolidatie van de zending te maken voor dit bedrijfsscenario.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Stel het veld **Beleidstype** in op *Verkooporders*.
1. Selecteer in het actievenster de optie **Nieuw** om een beleid te maken met de volgende instellingen:

    - **Beleidsnaam:** *Itemtype*
    - **Beleidsbeschrijving:** *Hetzelfde type artikel consolideren tussen orders*

1. Stel de optie **Consolideren met openstaande zendingen** in op *Ja*.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer op het sneltabblad **Consolidatievelden** in de lijst **Resterende velden** de rij waarin het veld **Veldnaam** is ingesteld op *Leveringsmethode*.
1. Selecteer de knop **Toevoegen** ![pijl naar rechts.](media/forward-button.png) om het veld naar de lijst **Geselecteerde velden** te verplaatsen.
1. Selecteer **Query bewerken** in het actievenster.
1. Vouw in het dialoogvenster van de query-editor op het tabblad **Joins** de structuur uit en selecteer **Tabellen \> Details laden**.
1. Selecteer **Tabeljoin toevoegen**.
1. In het raster met relaties dat wordt weergegeven, zoekt en selecteert u de rij waarin het veld **Relatie** is ingesteld op *Magazijnartikelnummer (artikelnummer)* en selecteert u **Selecteren**. 
1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:

    - **Tabel:** *Magazijnartikelnummer*
    - **Afgeleide tabel:** *Magazijnartikelnummer*
    - **Veld:** *Code 4*
    - **Criteria:** *Ontvlambaar*

1. Selecteer **OK** om het dialoogvenster te sluiten.

> [!NOTE]
> Voor dit bedrijfsscenario worden alle orderregels waarvoor artikelen een specifieke filtercode bevatten (de filtercode waarvan het veld **Code 4** is ingesteld op *Ontvlambaar*) met andere artikelen van hetzelfde type geconsolideerd tussen orders. Als er een openstaande zending voor dezelfde rekening, hetzelfde magazijn en dezelfde groep artikelen bestaat, worden de nieuwe regels hieraan gekoppeld.

### <a name="create-example-policy-3"></a>Voorbeeldbeleid 3 maken

In dit voorbeeld maakt u een beleid *Klantvereisten* dat kan worden gebruikt voor het volgende bedrijfsscenario:

- Met het beleid wordt een query voor een specifieke klantrekening uitgevoerd.
- Consolidatie met openstaande zendingen is ingeschakeld.
- Er wordt een consolidatie uitgevoerd tussen orders, maar deze is gebaseerd op de bestelopdrachten van de klant. (Meerdere orders worden in zendingen gegroepeerd, op basis van hetzelfde bestelopdrachtnummer van de klant en magazijn.)

Voer de volgende stappen uit om het beleid voor consolidatie van de zending te maken voor dit bedrijfsscenario.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Stel het veld **Beleidstype** in op *Verkooporders*.
1. Selecteer in het actievenster de optie **Nieuw** om een beleid te maken met de volgende instellingen:

    - **Beleidsnaam:** *CustomerOrderNo*
    - **Beleidsbeschrijving:** *Regels consolideren op basis van de klantinkooporder*

1. Stel de optie **Consolideren met openstaande zendingen** in op *Ja*.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer op het sneltabblad **Consolidatievelden** in de lijst **Resterende velden** de rij waarin het veld **Veldnaam** is ingesteld op *Bestelopdracht van klant*.
1. Selecteer de knop **Toevoegen** ![pijl naar rechts.](media/forward-button.png) om het veld naar de lijst **Geselecteerde velden** te verplaatsen.
1. Selecteer in de lijst **Resterende velden** de rij waarin het veld **Veldnaam** is ingesteld op *Leveringsmethode*.
1. Selecteer de knop **Toevoegen** ![pijl naar rechts.](media/forward-button.png) om het veld naar de lijst **Geselecteerde velden** te verplaatsen.
1. Selecteer **Query bewerken** in het actievenster.
1. Zoek in het dialoogvenster van de query-editor op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Klantrekening* en stel het veld **Criteria** voor die rij in op *US-001*.
1. Selecteer **OK** om het dialoogvenster te sluiten.

> [!NOTE]
> Voor dit bedrijfsscenario worden alle orderregels met verkooporders met hetzelfde bestelopdrachtnummer van de klant geconsolideerd in één zending, ongeacht het verkoopordernummer. (Het bestelopdrachtnummer van de klant wordt gebruikt als inkooporder \[IO\] van de klant.) Als er een openstaande zending voor dezelfde rekening, hetzelfde magazijn en een klantbestelopdracht bestaat, worden de nieuwe regels hieraan gekoppeld. Dit beleid kan worden gebruikt als de klant aanvullende meerdere keren gedurende een dag orderregels met hetzelfde IO-nummer stuurt en alle regels in één zending moeten worden gegroepeerd. (Met andere woorden: er is één vrachtbrief en één pakbon.)

### <a name="create-example-policy-4"></a>Voorbeeldbeleid 4 maken

In dit voorbeeld maakt u een beleid *Klanten die consolidatie toestaan* dat kan worden gebruikt voor het volgende bedrijfsscenario:

- Met het beleid wordt een query voor een specifieke ordergroep uitgevoerd om klanten te identificeren die geconsolideerde zendingen accepteren.
- Consolidatie met openstaande zendingen is uitgeschakeld.
- Consolidatie wordt uitgevoerd tussen orders met de velden die zijn geselecteerd op basis van het standaardbeleid CrossOrder (om het eerdere selectievakje **Zending bij vrijgave naar magazijn consolideren** te repliceren).

- U kunt de regel voor een verkooporder overschrijven door een andere order groep te selecteren.

Voer de volgende stappen uit om het beleid voor consolidatie van de zending te maken voor dit bedrijfsscenario.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Stel het veld **Beleidstype** in op *Verkooporders*.
1. Selecteer in het actievenster de optie **Nieuw** om een beleid te maken met de volgende instellingen:

    - **Beleidsnaam:** *Ordergroep*
    - **Beleidsbeschrijving:** *Consolideren tussen orders op basis van ordergroep*

1. Laat de optie **Consolideren met openstaande zendingen** ingesteld op *Nee*.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer op het sneltabblad **Consolidatievelden** in de lijst **Resterende velden** de rij waarin het veld **Veldnaam** is ingesteld op *Leveringsmethode*.
1. Selecteer de knop **Toevoegen** ![pijl naar rechts.](media/forward-button.png) om het veld naar de lijst **Geselecteerde velden** te verplaatsen.
1. Selecteer **Query bewerken** in het actievenster.
1. Selecteer in de het dialoogvenster van de query-editor op het tabblad **Bereik** de optie **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:

    - **Tabel:** *Verkooporders*
    - **Afgeleide tabel:** *Verkooporders*
    - **Veld:** *Groep*
    - **Criteria:** *ShipCons*

1. Selecteer **OK** om het dialoogvenster te sluiten.

> [!NOTE]
> Voor dit bedrijfsscenario worden alle orderregels waarvoor verkooporders tot dezelfde ordergroep behoren, geconsolideerd in één zending van verkooporders voor dezelfde rekening, hetzelfde magazijn en dezelfde transportmethode. In plaats van de ordergroep kunt u elk ander veld gebruiken om een groep klanten te onderscheiden en standaard de verkooporderkop gebruiken. U kunt deze aanpak gebruiken als de klant, niet het magazijn, achter de behoefte aan consolidatie zit. (In de eerdere consolidatielogica was de noodzaak van consolidatie afkomstig van het magazijn.)

### <a name="create-example-policy-5"></a>Voorbeeldbeleid 5 maken

In dit voorbeeld maakt u een beleid *Magazijnen die consolidatie toestaan* dat kan worden gebruikt voor het volgende bedrijfsscenario:

- Met het beleid wordt een query voor een specifieke ordergroep uitgevoerd om magazijnen te identificeren die zendingen kunnen consolideren.
- Consolidatie met openstaande zendingen is uitgeschakeld.
- Consolidatie wordt uitgevoerd tussen orders met de velden die zijn geselecteerd op basis van het standaardbeleid CrossOrder (om het eerdere selectievakje **Zending bij vrijgave naar magazijn consolideren** te repliceren).

Normaal gesproken kan voor dit bedrijfsscenario het standaardbeleid worden gebruikt dat u in de sectie [Uw initiële beleidsregels voor consolidatie van zendingen instellen](#initial-policies) hebt gemaakt. U kunt echter ook handmatig vergelijkbaar beleid maken door de volgende stappen uit te voeren.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Stel het veld **Beleidstype** in op *Verkooporders*.
1. Selecteer in het actievenster de optie **Nieuw** om een beleid te maken met de volgende instellingen:

    - **Beleidsnaam:** *Tussen orders*
    - **Beleidsbeschrijving:** *Consolidatie tussen orders voor specifieke magazijnen*

1. Laat de optie **Consolideren met openstaande zendingen** ingesteld op *Nee*.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer op het sneltabblad **Consolidatievelden** in het veld **Resterende velden** de rij waarin het veld **Veldnaam** is ingesteld op *Leveringsmethode*.
1. Selecteer de knop **Toevoegen** ![pijl naar rechts.](media/forward-button.png) om het veld naar de lijst **Geselecteerde velden** te verplaatsen.
1. Selecteer **Query bewerken** in het actievenster.
1. Zoek in het dialoogvenster van de query-editor op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Magazijn* en stel het veld **Criteria** voor die rij in op *61, 63*.
1. Selecteer **OK** om het dialoogvenster te sluiten.

### <a name="set-the-order"></a>De order instellen

Nu u al uw beleid hebt gemaakt, moet u de volgorde bepalen waarin deze beleidsregels worden toegepast. Als u een piramideachtige aanpak wilt gebruiken, waarbij de beleidsregels met de meeste voorwaarden worden geëvalueerd met de hoogste prioriteit, kunt u de volgende stappen uitvoeren.

1. Ga naar **Magazijnbeheer \> Instellen \> Vrijgave naar magazijn \> Consolidatiebeleid voor zendingen**.
1. Stel het veld **Beleidstype** in op *Verkooporders*.
1. Selecteer elk beleid dat wordt weergegeven in de linkerkolom en gebruik vervolgens de knoppen **Omhoog** en **Omlaag** in het actievenster om de beleidsregels in de volgende volgorde te rangschikken:

    1. CustomerMode
    1. Artikeltype
    1. CustomerOrderNo
    1. Ordergroep
    1. Tussen orders
    1. Standaard

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Voorbeeldscenario's voor het gebruik van consolidatiebeleid voor zendingen

In de volgende scenario's wordt beschreven hoe u het consolidatiebeleid voor zendingen kunt gebruiken dat u hebt gemaakt tijdens het lezen van dit artikel. In elk scenario wordt u door een consolidatieproces voor zendingen geleid waarbij wordt gebruikgemaakt van consolidatiebeleid voor zendingen tijdens automatische of handmatig vrijgave naar het magazijn:

- Scenario 1: [Zendingen consolideren wanneer deze naar het magazijn worden vrijgegeven met Automatische vrijgave van verkooporders](../warehousing/consolidate-shipments-automatic.md)
- Scenario 2: [Zendingen consolideren wanneer het consolidatiebeleid voor zendingen wordt overschreven via de pagina Vrijgave naar magazijn](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Scenario 3: [Zendingen consolideren met Vrijgave naar magazijn vanuit de workbench voor ladingplanning](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Scenario 4: [Zendingen consolideren met de workbench voor het consolideren van zendingen](../warehousing/consolidate-shipments-manual-workbench.md)
- Scenario 5: [Zendingen handmatig consolideren via de pagina Zendingen consolideren](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van consolidatiebeleid voor zendingen](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

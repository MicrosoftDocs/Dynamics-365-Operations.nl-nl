---
title: App Voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven hoe u de app Voorraadzichtbaarheid gebruikt.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344997"
---
# <a name="inventory-visibility-app"></a>App Voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In dit onderwerp wordt beschreven hoe u de app Voorraadzichtbaarheid gebruikt.

Voorraadzichtbaarheid biedt een modelgestuurde app voor visualisatie. De app bevat drie pagina's: **Configuratie**, **Operationele zichtbaarheid** en **Voorraadoverzicht**. De app biedt de volgende functies:

- De app biedt een gebruikersinterface (UI) voor een voorhanden configuratie en een zachte reservering.
- De app ondersteunt voorhanden voorraadquery's in realtime voor diverse dimensiecombinaties.
- De app biedt een gebruikersinterface voor het boeken van reserveringsaanvragen.
- De app biedt een aangepaste weergave van de voorhanden voorraad voor producten, samen met alle dimensies.

## <a name="prerequisites"></a>Vereisten

Installeer voordat u begint eerst de invoegtoepassing Voorraadzichtbaarheid en stel deze in zoals beschreven in [Voorraadzichtbaarheid instellen](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Configuratie

De pagina **Configuratie** helpt u bij het instellen van de voorhanden configuratie en de zachte reserveringsconfiguratie. Als de invoegtoepassing is geïnstalleerd, bevat de standaardconfiguratie de waarde van Microsoft Dynamics 365 Supply Chain Management (de `fno`-gegevensbron). U kunt de standaardinstelling controleren. Daarnaast kunt u op basis van uw bedrijfsbehoeften en de voorraadboekingsvereisten van uw externe systeem de configuratie wijzigen in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) om de manier te standaardiseren waarop voorraadwijzigingen kunnen worden geboekt, geordend en opgevraagd in de verschillende systemen.

### <a name="define-data-sources"></a>Gegevensbronnen definiëren

U definieert elke *gegevensbron* die u wilt integreren met Voorraadzichtbaarheid. Voorraadzichtbaarheid ondersteunt integratie met verschillende gegevensbronnen, zoals uw POS-systeem, Supply Chain Management en andere externe systemen. Standaard is Supply Chain Management ingesteld als een standaardgegevensbron (`fno`) in Voorraadzichtbaarheid.

Volg deze stappen om een gegevensbron toe te voegen.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Gegevensbron** de optie **Nieuwe gegevensbron** om een gegevensbron toe te voegen.

> [!NOTE]
> Wanneer u een gegevensbron toevoegt, moet u de naam, fysieke metingen en dimensietoewijzingen van uw gegevensbron valideren voordat u de configuratie voor de service voor Voorraadzichtbaarheid bijwerkt. U kunt deze instellingen niet meer wijzigen nadat u **Updateconfiguratie** hebt geselecteerd.

### <a name="set-up-dimension-mappings"></a>Dimensietoewijzingen instellen

Voorraadzichtbaarheid biedt een lijst met basisdimensies die kunnen worden toegewezen vanuit de dimensies van uw gegevensbron. Er zijn 33 dimensies beschikbaar voor toewijzing.

- Als u Supply Chain Management als een van uw gegevensbronnen gebruikt, worden er standaard 13 dimensies aan de standaarddimensies van Supply Chain Management toegewezen. 12 andere dimensies (`inventDimension1` tot en met `inventDimension12`) worden aan aangepaste dimensies in Supply Chain Management toegewezen. De resterende acht dimensies zijn uitgebreide dimensies die u aan externe gegevensbronnen kunt toewijzen.
- Als u Supply Chain Management niet als een van uw gegevensbronnen gebruikt, kunt u de dimensies naar wens toewijzen. In de volgende tabel wordt de volledige lijst met beschikbare dimensies weergegeven.

> [!NOTE]
> Als uw dimensie niet in de standaarddimensielijst staat en u een externe gegevensbron gebruikt, raden we u aan `ExtendedDimension1` tot en met `ExtendedDimension8` voor de toewijzing te gebruiken.

| Dimensietype | Dimensienaam |
|---|---|
| Artikel | `ColorId` |
| Artikel | `SizeId` |
| Artikel | `StyleId` |
| Artikel | `ConfigId` |
| Tracering | `BatchId` |
| Tracering | `SerialId` |
| Locatie | `LocationId` |
| Locatie | `SiteId` |
| Voorraadstatus | `StatusId` |
| Magazijnspecifiek | `WMSLocationId` |
| Magazijnspecifiek | `WMSPalletId` |
| Magazijnspecifiek | `LicensePlateId` |
| Anders | `VersionId` |
| Voorraad (aangepast) | `InventDimension1` tot en met `InventDimension12` |
| Anders | `ExtendedDimension1` tot en met `ExtendedDimension8` |

Ga als volgt te werk om dimensietoewijzingen toe te voegen.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Gegevensbron** in de sectie **Dimensietoewijzingen** de optie **Toevoegen** om dimensietoewijzingen toe te voegen.
1. Geef in het veld **Dimensienaam** de brondimensie op.
1. Selecteer in het veld **Naar basisdimensie** de dimensie in Voorraadzichtbaarheid die u wilt toewijzen.
1. Selecteer **Opslaan**.

![Dimensietoewijzingen toevoegen](media/inventory-visibility-dimension-mapping.png "Dimensietoewijzingen toevoegen")

Als uw gegevensbron bijvoorbeeld een productkleurdimensie bevat, kunt u deze aan de basisdimensie `ColorId` toevoegen om een aangepaste dimensie `ProductColor` aan de gegevensbron `exterchannel` toe te voegen. Deze wordt vervolgens aan de basisdimensie `ColorId` toegevoegd.

## <a name="create-a-physical-measure"></a>Een fysieke meting maken

Wanneer vanuit een gegevensbron een voorraadwijziging naar Voorraadzichtbaarheid wordt geboekt, wordt die wijziging met behulp van *fysieke metingen* geboekt. Fysieke metingen zijn modificators die de samengevatte voorraadtransactiestatus weergeven. Query's kunnen worden gebaseerd op de fysieke metingen.

Voorraadzichtbaarheid biedt een lijst met standaard fysieke metingen. Deze standaard fysieke metingen worden opgehaald uit de statussen van voorraadtransacties op de pagina **Voorhanden lijst** in Supply Chain Management (**Voorraadbeheer \> Vragen en rapport \> Voorhanden lijst**).

| Modificator | Naam |
|---|---|
| `PhysicalInvent` | Fysieke voorraad |
| `ReservPhysical` | Fysiek gereserveerd |
| `AvailPhysical` | Fysiek beschikbaar |
| `ReservOrdered` | Besteld en gereserveerd |
| `PostedQty` | Geboekte hoeveelheid |
| `Deducted` | Ingehouden |
| `Picked` | Opgenomen |
| `Received` | Ontvangen |
| `Registered` | Geregistreerd |
| `Arrived` | Gearriveerd |
| `Ordered` | Besteld |
| `OnOrder` | In bestelling |
| `QuotationReceipt` | Offerte-ontvangst |
| `QuotationIssue` | Offerte-uitgifte |

Als de gegevensbron Supply Chain Management is, hoeft u de standaard fysieke metingen niet opnieuw te maken. Voor externe gegevensbronnen kunt u echter nieuwe fysieke metingen maken door deze stappen uit te voeren.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Gegevensbron** in de sectie **Fysieke metingen** de optie **Toevoegen**, geef een naam voor de bronmeting op en sla de wijzigingen op.

## <a name="define-the-product-hierarchy-index"></a>De producthiërarchie-index definiëren

Door samengevoegde dimensiegroepen in te stellen, kunt u Voorraadzichtbaarheid gebruiken om een query uit te voeren op de status van de voorhanden voorraad. In Voorraadzichtbaarheid wordt elke dimensiegroep een *index* genoemd. Elke index komt overeen met een setnummer. U kunt bepalen welke dimensies worden gebruikt om de indexering in te stellen op basis van de manier waarop u een query uitvoert in Voorraadzichtbaarheid.

Ga als volgt te werk om uw producthiërarchie-index in te stellen.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Producthiërarchie-index** in de sectie **Dimensietoewijzingen** de optie **Toevoegen** om dimensietoewijzingen toe te voegen.
1. Standaard wordt een lijst met indexen weergegeven. Als u een bestaande index wilt wijzigen, selecteert u **Bewerken** of **Toevoegen** in de sectie voor de relevante index. Als u een nieuwe indexset wilt maken, selecteert u **Nieuwe indexset**. Selecteer voor elke rij in elke indexset in het veld **Dimensie** een dimensie in de lijst met basisdimensies. Waarden voor de volgende velden worden automatisch gegenereerd:

    - **Setnummer**: dimensies die tot dezelfde groep (index) behoren, worden gegroepeerd en krijgen hetzelfde setnummer toegewezen.
    - **Hiërarchie**: de hiërarchie wordt gebruikt om de ondersteunde dimensiecombinaties te definiëren waarop een query kan worden uitgevoerd in een dimensiegroep (index). Als u bijvoorbeeld een dimensiegroep instelt met de hiërarchievolgorde *Stijl*, *Kleur* en *Maat*, ondersteunt het systeem het resultaat van drie querygroepen. De eerste groep is alleen stijl. De tweede groep is een combinatie van stijl en kleur. En de derde groep is een combinatie van stijl, kleur en maat. De andere combinaties worden niet ondersteund.

Zie [Configuratie van productindexhiërarchie](inventory-visibility-configuration.md#index-configuration) voor meer informatie.

### <a name="example"></a>Voorbeeld

In deze sectie vindt u een voorbeeld van de manier waarop de hiërarchie werkt. In de volgende tabel vindt u een lijst met beschikbare voorraad voor dit voorbeeld.

| Artikel | Opmaakmodel | Kleur | Maat | Hoeveelheid |
|---|---|---|---|---|
| I0001 | Breed | Zwart | Klein | 1 |
| I0001 | Breed | Zwart | Groot | 2 |
| I0001 | Breed | Rood | Klein | 3 |
| I0001 | Normaal | Zwart | Klein | 4 |
| I0001 | Normaal | Zwart | Groot | 5 |
| I0001 | Normaal | Rood | Klein | 6 |
| I0001 | Normaal | Rood | Groot | 7 |

De volgende tabel toont hoe de indexhiërarchie is ingesteld.

| Sleutel | Setnummer | Hiërarchie |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Op basis van de voorgaande instellingen is de dimensiecombinatie voor de query Voorraadzichtbaarheid *Stijl*, *Kleur* en *Maat*. Door de hiërarchieinstellingen kunnen externe systemen op de volgende manieren query's uitvoeren op de voorhanden voorraad:

- `()`: gegroepeerd op alle. Dit is de uitvoer:

    - I0001, 28

- `(StyleId)`: groeperen op stijl. Dit is de uitvoer:

    - I0001, wide, 6
    - I0001, regular, 22

- `(StyleId, ColorId)`: gegroepeerd op de combinatie van stijl en kleur. Dit is de uitvoer:

    - I0001, wide, zwart, 3
    - I0001, wide, rood, 3
    - I0001, regular, zwart, 9
    - I0001, regular, rood, 13

- `(StyleId, ColorId, SizeId)`: gegroepeerd op de combinatie van stijl, kleur en maat. Dit is de uitvoer:

    - I0001, wide, zwart, small, 1
    - I0001, wide, zwart, large, 2
    - I0001, wide, rood, small, 3
    - I0001, regular, zwart, small, 4
    - I0001, regular, zwart, large, 5
    - I0001, regular, rood, small, 6
    - I0001, regular, rood, large, 7

## <a name="set-up-a-custom-calculated-measure"></a>Een aangepaste berekende meting instellen

U kunt Voorraadzichtbaarheid gebruiken om een query uit te voeren op zowel fysieke metingen van de voorraad als op *aangepaste berekende metingen*.

Met de configuratie kunt u een set modificators definiëren die worden opgeteld of afgetrokken om het totale samengevoegde uitvoeraantal te krijgen.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Berekende meting** de optie **Nieuwe berekende meting** om een berekende maat toe te voegen. Stel vervolgens de velden in aan de hand van de beschrijving in de volgende tabel.

    | Veld | Waarde |
    |---|---|
    | Naam van nieuwe berekende meting | Voer de naam van de berekende meting in. |
    | Gegevensbron | Het querysysteem is een gegevensbron. |
    | Gegevensbron van modificator | Voer de gegevensbron van de modificator in. |
    | Modificator | Voer de naam van de modificator in. |
    | Modificatortype | Selecteer het modificatortype (*Optellen* of *Aftrekken*). |

In de volgende tabel wordt een voorbeeld van de aangepaste berekende meting `MyCustomAvailableforReservation` weergegeven. Zie [Configuratie van de gegevensbron](inventory-visibility-configuration.md#data-source-configuration) voor meer informatie over dit voorbeeld.

| Gegevensbron van berekende meting | Berekende meting | Gegevensbron van modificator | Modificator | Modificatortype |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Een zachte reserveringstoewijzing instellen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Voordat u het tabblad **Zachte reserveringstoewijzing** kunt bewerken, moet u de functie *Voorhanden reservering* op het tabblad **Functiebeheer** inschakelen.

Door de toewijzing van de fysieke meting in te stellen op de berekende meting, schakelt u de service Voorraadzichtbaarheid in om automatisch de beschikbaarheid van reserveringen te valideren op basis van de fysieke meting.

Voordat u deze toewijzing instelt, moeten de fysieke metingen, berekende metingen en de bijbehorende gegevensbronnen worden gedefinieerd op de tabbladen **Gegevensbron** en **Berekende meting** van de pagina **Configuratie** in Power Apps (zoals eerder in dit onderwerp is beschreven).

Volg deze stappen om een zachte reserveringstoewijzing te definiëren.

1. Definieer de fysieke meting die als de zachte reserveringsmeting fungeert (bijvoorbeeld `softreservordered`).
1. Definieer op het tabblad **Berekende meting** van de pagina **Configuratie** de berekende meting *beschikbaar voor reservering* (AFR) die de AFR-berekeningsformule bevat die u aan de fysieke meting wilt toewijzen. U kunt bijvoorbeeld `availforreserv` instellen (beschikbaar voor reservering) zodat deze wordt toegewezen aan de eerder gedefinieerde fysieke meting `softreservordered`. Op deze manier kunt u zoeken welke hoeveelheden met de voorraadstatus `softreservordered` er beschikbaar zijn voor reservering. In de volgende tabel wordt de AFR-berekeningsformule weergegeven.

    | Modificator | Gegevensbron | Maat |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Open de pagina **Configuratie**.
1. Stel op het tabblad **Zachte reserveringstoewijzing** de toewijzing van de fysieke meting naar de berekende meting in. In het vorige voorbeeld kunt u de volgende instellingen gebruiken om `availforreserv` op de eerder gedefinieerde fysieke meting `softreservordered` toe te wijzen.

    | Gegevensbron van fysieke meting | Fysieke meting | Beschikbaar voor reserveringsgegevensbron | Beschikbaar voor reservering van berekende meting |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Een zachte reserveringshiërarchie instellen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Voordat u het tabblad **Zachte reserveringshiërarchie** kunt bewerken, moet u de functie *Voorhanden reservering* op het tabblad **Functiebeheer** inschakelen.

In de reserveringshiërarchie wordt de volgorde van dimensies beschreven die moeten worden opgegeven wanneer er reserveringen worden gemaakt. Dit werkt op dezelfde manier als de productindexhiërarchie voor voorhanden query's.

De reserveringshiërarchie kan verschillen van de voorhanden indexhiërarchie. Met deze onafhankelijkheid kunt u categoriebeheer implementeren, waarbij gebruikers de dimensies kunnen opsplitsen in details om de vereisten voor het maken van nauwkeurige reserveringen op te geven.

#### <a name="example"></a>Voorbeeld

De volgende reserveringshiërarchie is in uw systeem ingesteld.

| Dimensie | Hiërarchie |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Op basis van deze reserveringshiërarchie kunt u een reservering maken in de volgende dimensievolgorde:

- `()`: er is geen dimensie opgegeven.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

De dimensievolgorde moet strikt de reserveringshiërarchiereeks volgen, dimensie voor dimensie. Reserveringen met `(ColorId, StyleId)` zijn bijvoorbeeld niet toegestaan in dit voorbeeld, omdat deze reeks niet is gedefinieerd in de reserveringshiërarchie.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Functiebeheer beheren

De Invoegvoegservice Voorraadzichtbaarheid biedt functies *zoals OnHandReservation* en *OnHandMostSpecificBackservice*. Deze functies zijn standaard uitgeschakeld. Als u deze wilt gebruiken, opent u de pagina **Configuratie** in Power Apps en schakelt u ze vervolgens in op het tabblad **Functiebeheer**.

### <a name="complete-and-update-the-configuration"></a>De configuratie voltooien en bijwerken

Nadat u de configuratie hebt voltooid, moet u alle wijzigingen in Voorraadzichtbaarheid door te voeren. Selecteer **Configuratie bijwerken** in de rechterbovenhoek op de pagina **Configuratie** in Power Apps om de wijzigingen door te voeren.

De eerste keer dat u **Configuratie bijwerken** selecteert, vraagt het systeem om uw referenties.

- **Client-id**: de Azure-toepassings-id die u hebt gemaakt voor Voorraadzichtbaarheid.
- **Tenant-id**: uw Azure-tenant-id.
- **Clientgeheim**: het geheim van de Azure-toepassing die u hebt gemaakt voor Voorraadzichtbaarheid.

Nadat u zich hebt aangemeld, wordt de configuratie in de service Voorraadzichtbaarheid bijgewerkt.

> [!NOTE]
> Valideer de naam van uw gegevensbron, de fysieke metingen en de dimensietoewijzingen voordat u de configuratie voor de service voor Voorraadzichtbaarheid bijwerkt. U kunt deze instellingen niet meer wijzigen nadat u **Updateconfiguratie** hebt geselecteerd.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Het service-eindpunt zoeken

Als u het juiste eindpunt van de service Voorraadzichtbaarheid niet weet, opent u de pagina **Configuratie** in Power Apps en selecteert u vervolgens **Service-eindpunt weergeven** in de rechterbovenhoek. Op deze pagina wordt het juiste service-eindpunt weergegeven.

## <a name="operational-visibility"></a>Operationele zichtbaarheid

Op de pagina **Operationele zichtbaarheid** worden de resultaten van een realtime voorhanden voorraadquery weergegeven op basis van verschillende dimensiecombinaties. Wanneer de functie *OnHandReservion* is ingeschakeld, kunt u ook reserveringsaanvragen boeken vanaf de pagina **Operationele zichtbaarheid**.

### <a name="on-hand-query"></a>Voorhanden query

Op het tabblad **Voorhanden query** worden de resultaten weergegeven van een realtime voorhanden voorraadquery.

Wanneer u het tabblad **Voorhanden query** selecteert, vraagt het systeem om uw referenties zodat het de Bearer-token kan ophalen dat nodig is om de query op de service Voorraadzichtbaarheid uit te voeren. U hoeft het Bearer-token alleen maar in het veld **Bearer-token** te plakken en het dialoogvenster te sluiten. U kunt vervolgens een voorhanden queryaanvraag boeken.

Als het Bearer-token niet geldig is of als dit is verlopen, moet u een nieuw token in het veld **Bearer-token** plakken. Voer de juiste waarden voor **Client-id**, **Tenant-id** en **Clientgeheim** in en selecteer vervolgens **Vernieuwen**. Het systeem haalt automatisch een nieuw, geldig Bearer-token op.

Als u een voorhanden query wilt boeken, voert u de query in de aanvraagbody in. Gebruik het patroon dat in [Een query uitvoeren met de post-methode](inventory-visibility-api.md#query-with-post-method)

![Voorhanden query-instellingen](media/inventory-visibility-query-settings.png "Voorhanden query-instellingen")

### <a name="reservation-posting"></a>Reserveringen boeken

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Gebruik het tabblad **Reserveringen boeken** om een reserveringsaanvraag te boeken. Voordat u een reserveringsaanvraag kunt boeken, moet u de functie *OnHandReservation* inschakelen. Zie [Reserveringen van Voorraadzichtbaarheid](inventory-visibility-reservations.md) voor meer informatie over deze functie.

Als u een reserveringsaanvraag wilt boeken, moet u een waarde in de aanvraagbody invoeren. Gebruik het patroon dat is beschreven in [Eén reserveringsgebeurtenis maken](inventory-visibility-api.md#create-one-reservation-event). Selecteer vervolgens **Boeken**. Als u details van het antwoord op de aanvraag wilt weergeven, selecteert u **Details weergeven**. U kunt ook de waarde **reservationId** uit de antwoorddetails ophalen.

## <a name="inventory-summary"></a>Voorraadoverzicht

**Voorraadoverzicht** is een aangepaste weergave voor de *entiteit som voor voorhanden voorraad*. Het overzicht biedt een voorraadoverzicht voor producten samen met alle dimensies. Met het **Geavanceerde filter** dat Dataverse biedt, kunt u een persoonlijke weergave maken met de rijen die belangrijk voor u zijn. Met de opties van het geavanceerde filter kunt u een breed scala weergaven maken, van eenvoudig tot complex. Met deze filters kunt u ook gegroepeerde en geneste voorwaarden aan de filters toevoegen.

Zie [Persoonlijke weergaven maken met geavanceerde rasterfilters](/powerapps/user/grid-filters-advanced) voor meer informatie over het gebruik van **Geavanceerd filter**.

Boven aan de aangepaste weergave hebt u drie velden: **Standaarddimensie**, **Aangepaste dimensie** en **Meting**. U kunt deze velden gebruiken om te bepalen welke kolommen worden weergegeven.

U kunt de kolomkop selecteren om het huidige resultaat te filteren of te sorteren.

Onder aan de aangepaste weergave wordt informatie weergegeven, zoals '50 records (29 geselecteerd)' of '50 records'. Deze informatie verwijst naar de op dat moment geladen records van het resultaat van **Geavanceerd filter**. De tekst '29 geselecteerd' verwijst naar het aantal records dat is geselecteerd met het kolomkoptekstfilter voor de geladen records.

Onder aan de weergave bevindt zich de knop **Meer laden** waarmee u meer records van Dataverse kunt laden. Het standaardaantal records dat wordt geladen, is 50. Als u **Meer laden** selecteert, worden de volgende 1000 beschikbare records in de weergave geladen. Het getal op de knop **Meer laden** geeft het momenteel geladen aantal records en het totale aantal records voor het resultaat van het **Geavanceerde filter** aan.

![Voorraadoverzicht](media/inventory-visibility-onhand-list.png "Voorraadoverzicht")

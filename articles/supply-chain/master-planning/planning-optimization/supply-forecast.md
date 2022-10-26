---
title: Hoofdplanning met aanbodprognoses
description: In dit artikel wordt beschreven hoe aanbodprognoses tijdens de hoofdplanning worden gebruikt.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690076"
---
# <a name="master-planning-with-supply-forecasts"></a>Hoofdplanning met aanbodprognoses

[!include [banner](../../includes/banner.md)]

Met aanbodprognoses kunt u het aanbod opgeven dat u naar verwachting tijdens een toekomstige periode nodig hebt. Doorgaans baseert u de schatting op de verkoophistorie van het vorige jaar en gebruikt u vervolgens de prognose voor budgetdoeleinden. U kunt uw hoofdplannen ook zo instellen dat rekening wordt houden met prognoses tijdens de planning.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Een hoofdplan instellen om rekening te houden met aanbodprognoses

U kunt opgeven of bij elk hoofdplan rekening moet worden houden met prognoses wanneer dit wordt uitgevoerd. Met de volgende procedure kunt u prognoseopties instellen voor elk plan.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een bestaand hoofdplan in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuw hoofdplan te maken.
1. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Prognosemodel**: selecteer het model dat de aanbod- en/of vraagprognoses bevat die door het hoofdplan moeten worden gebruikt.
    - **Aanbodprognose opnemen**: stel deze optie in op *Ja* als in het hoofdplan rekening moet worden gehouden met aanbodprognoses.
    - **Vraagprognose opnemen**: stel deze optie in op *Ja* als in het hoofdplan rekening moet worden gehouden met vraagprognoses. Hoewel deze instelling niet afhankelijk is van de instelling **Aanbodprognose opnemen**, zijn enkele andere instellingen op de pagina van toepassing op zowel aanbodprognoses als vraagprognoses. Zie [Hoofdplanning met vraagprognoses](demand-forecast.md) voor meer informatie over planningen met vraagprognoses.
    - **Gebruikte methode om prognosebehoeften te verminderen**: selecteer de methode die moet worden gebruikt om prognosebehoeften te beperken tijdens de hoofdplanning:

        - *Geen*: prognosebehoeften worden niet beperkt tijdens de hoofdplanning.
        - *Percentage - reductiesleutel*: de prognosebehoeften worden gereduceerd volgens de percentages en perioden die zijn gedefinieerd in de reductiesleutel.
        - *Transacties - reductiesleutel*: de prognosebehoeften worden gereduceerd door de transacties die plaatsvinden tijdens de perioden die worden gedefinieerd in de reductiesleutel.
        - *Transacties - dynamische periode*: de prognosebehoeften worden gereduceerd met de werkelijke ordertransacties die tijdens de dynamische periode plaatsvinden. De dynamische periode bestrijkt de huidige prognosedatums en eindigt wanneer de volgende prognose begint. De methode *Transacties - dynamische periode* gebruikt of vereist geen reductiesleutel. Wanneer u de sleutel gebruikt, gelden de volgende voorwaarden:

            - Als de prognose volledig is gereduceerd, worden de prognosebehoeften voor de huidige prognose 0 (nul).
            - Als er geen toekomstige prognose is, worden de prognosebehoeften van de laatste prognose die is ingevoerd, gereduceerd.
            - De timefences worden opgenomen in de berekening van de prognosereductie.
            - Positieve dagen zijn opgenomen in de berekening van de prognosereductie.
            - Als de werkelijke ordertransacties de prognosebehoeften overschrijden, worden de resterende transacties niet naar de volgende prognoseperiode doorgestuurd.

        > [!NOTE]
        > De instelling **Gebruikte methode om prognosebehoeften te verminderen** is ook van toepassing op vraagprognoses als u deze hebt ingeschakeld voor het hoofdplan en deze instelling heeft dezelfde invloed. Zie voor meer informatie [Hoofdplanning met vraagprognoses](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Reductieopties voor dekkingsgroepen instellen

Volg deze stappen om opties in te stellen die bepalen hoe een behoefteplanningsgroep de prognosebehoeften reduceert voor hoofdplannen die gebruikmaken van op transacties gebaseerde reductie.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Behoefteplanningsgroepen**.
1. Selecteer een bestaande behoefteplanningsgroep in het lijstvenster of selecteer **Nieuw** in het actievenster om een nieuwe groep te maken.
1. Geef op het sneltabblad **Overig** in het veld **Prognose reduceren met** op hoe aanbodprognosebehoeften moeten worden verminderd voor artikelen in de behoefteplanningsgroep, voor hoofdplannen waarvoor het veld **Gebruikte methode om prognosebehoeften te verminderen** is ingesteld op *Transacties - reductiesleutel* of *Transacties - dynamische periode*. Selecteer een van de volgende waarden:

    - *Alle transacties*: alle transacties moeten de prognose verminderen.
    - *Orders*: alleen orders van hetzelfde type moeten de prognose verminderen.

    De standaardorderinstellingen voor een artikel geven bijvoorbeeld aan dat het artikel moet worden geproduceerd. Er is een aanbodprognoseregel voor een hoeveelheid van 50 en er is een bestaande inkooporder voor een hoeveelheid van 20. Als het veld **Prognose verlagen met** is ingesteld op *Orders*, wordt een geplande productieorder gemaakt voor een hoeveelheid van 50. Als de productieorder is ingesteld op *Alle transacties*, wordt het aantal productieorders verlaagd tot 30.

    Deze instelling geldt ook voor de reductie van vraagprognoses. Zie voor meer informatie [Hoofdplanning met vraagprognoses](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Een aanbodprognose voor een product invoeren

Volg deze stappen om een aanbodprognose voor een product in te voeren.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product waarvoor u een prognose wilt invoeren.
1. Selecteer in het actievenster op het tabblad **Plan** de optie **Aanbodprognose**.
1. Selecteer op de pagina **Aanbodprognose** in het actievenster de optie **Nieuw** om een prognose toe te voegen aan het raster.
1. Voer zo nodig informatie in op de nieuwe regel om uw prognose op te geven.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Plannen voor een artikel met aanbodprognoseregels

Wanneer u een hoofdplan uitvoert dat een artikel bevat waarvoor een aanbodprognose bestaat, wordt een inkooporder gemaakt voor de aanbodregels die zijn ingevoerd. Standaardorderinstellingen voor het artikel worden in acht genomen. Als met deze standaardorderinstellingen een waarde van **Standaardordertype** voor *Inkooporder* wordt opgegeven en er geen leveranciersrekening is opgegeven op de aanbodprognoseregel, wordt de standaardleverancier voor het artikel gebruikt.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Controleren of een geplande order een aanbodprognoseorder is

Gebruik de volgende procedure om te weten te komen of een geplande order is gemaakt als gevolg van een aanbodprognose.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Geplande orders**.
1. Open de geplande order die u wilt inspecteren.
1. Controleer op het sneltabblad **Algemeen** de waarde van het veld **Aanbodprognose**. Als de order is gemaakt om een aanbodprognose te dekken, wordt dit veld ingesteld op *Ja*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Voorbeelden van hoofdplanning met aanbodprognoses

In deze sectie vindt u enkele voorbeelden die laten zien wat de invloed van aanbodprognoses op de hoofdplanning is.

### <a name="example-1-supply-forecast-for-an-item"></a>Voorbeeld 1: Aanbodprognose voor een artikel

U hebt een artikel waarbij het standaardordertype *Inkooporder* is en de standaardleverancier *US-002*. Het bevat de volgende aanbodprognoseregel.

| Model    | Datum     | Leveranciersaccount | Leveranciersgroep | Quantity | Eenheid | Site | Magazijn |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10-10-22 |                |              | 35       | Stuk   | 1    | 11        |

Wanneer u de hoofdplanning uitvoert, wordt er een geplande inkooporder gemaakt voor *35 stuks* van leverancier *US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Voorbeeld 2: Verschillende aanbodprognoseregels, met en zonder leverancier

U hebt een artikel waarbij het standaardordertype *Inkooporder* is en de standaardleverancier *US-002*. Het bevat de volgende aanbodprognoseregels.

| Model    | Datum     | Leveranciersaccount | Leveranciersgroep | Quantity | Eenheid | Site | Magazijn |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10-10-22 |                |              | 35       | Stuk   | 1    | 11        |
| CurrentF | 10-10-22 | US-101         |              | 25       | Stuk   | 1    | 11        |

In dit geval wordt de regel waarop geen leverancier wordt opgegeven, behandeld als algemene prognose. Er wordt aangenomen dat de regel waarop een leverancier wordt opgegeven, moet worden afgetrokken van de algemene prognose. Daarom worden in de hoofdplanning de volgende geplande inkooporders voor het artikel gemaakt:

- Een geplande inkooporder voor een hoeveelheid van *25 st* van leverancier *US-101* (de leverancier en hoeveelheid die op de prognoseregel zijn opgegeven, worden gebruikt).
- Een geplande inkooporder voor een hoeveelheid van *10 stuks* van leverancier *US-002* (omdat er geen leverancier is opgegeven op de andere prognoseregel, wordt de standaardleverancier gebruikt en wordt de hoeveelheid van deze prognoseregel verminderd met de hoeveelheid van de leverancierspecifieke prognoseregel).

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Voorbeeld 3: Plannen waarbij de reductiemethode Transacties - dynamische periode wordt gebruikt in één prognoseperiode

Voor hoofdplannen die *Transacties - dynamische periode* als prognosereductiemethode gebruiken, worden prognosehoeveelheden verlaagd door de hoofdplanning als er bestaande transacties zijn die overeenkomen met deze aanbodkenmerken.

Stel dat u een artikel met het standaardordertype *Inkooporder* hebt. Het bevat de volgende aanbodprognoseregel.

| Model    | Datum     | Leveranciersaccount | Leveranciersgroep | Quantity | Eenheid | Site | Magazijn |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10-10-22 | US-101         |              | 25       | Stuk   | 1    | 11        |

Aangezien er slechts één aanbodprognoseregel is, is er slechts één prognoseperiode.

Wanneer u een hoofdplan uitvoert dat is ingesteld om *Transacties - dynamische periode* als de reductiemethode te gebruiken, kan het volgende gebeuren:

- Als er een inkooporder bestaat voor leverancier *US-101* en een hoeveelheid van *10 stuks* en het veld **Aanbodprognose** is ingesteld op *Ja*, wordt via de hoofdplanning een nieuwe geplande inkooporder gemaakt voor de resterende hoeveelheid van *10 stuks*. De prognoseregel wordt verlaagd omdat de leverancier overeenkomt met de bestaande inkooporder.
- Als er een inkooporder bestaat voor leverancier *US-102*, vestiging *1*, magazijn *11* en een hoeveelheid van *10 stuks* en het veld **Aanbodprognose** is ingesteld op *Ja*, wordt via de hoofdplanning een nieuwe geplande inkooporder gemaakt voor de volledige hoeveelheid van *25 stuks*. De prognoseregel kan niet worden verminderd omdat deze een andere leverancier heeft dan de bestaande inkooporder.

> [!NOTE]
> Deze situatie kan zich voordoen voor geplande inkooporders omdat hieraan een leverancier is gekoppeld. Voor transfer- en productieorders worden de bedragen van de aanbodprognose echter altijd verminderd met bestaande orders omdat er geen leverancier wordt opgegeven voor deze typen orders.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Voorbeeld 4: Plannen waarbij de reductiemethode Transacties - dynamische periode wordt gebruikt gedurende meerdere prognoseperioden

Stel dat u een artikel met het standaardordertype *Inkooporder* hebt. Het bevat de volgende aanbodprognoseregels.

| Model    | Datum     | Leveranciersaccount | Leveranciersgroep | Quantity | Eenheid | Site | Magazijn |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10-10-22 | US-101         |              | 25       | Stuk   | 1    | 11        |
| CurrentF | 15-10-22 | US-101         |              | 25       | Stuk   | 1    | 11        |

In dit voorbeeld zijn er twee prognoseregels, elk met een andere datum. Daarom bepalen de datums de grenzen van de prognoseperioden. De eerste periode is van 10 oktober tot en met 14 oktober 2022 (10-10-22 t/m 14-10-22). De tweede is vanaf 15 oktober 2022 (15-10-22).

Er is een bestaande inkooporder voor leverancier *US-101*, een hoeveelheid van *10 stuks* en de datum *12-10-22* (12 oktober 2022). Wanneer u een hoofdplan uitvoert dat is ingesteld om *Transacties - dynamische periode* als de reductiemethode te gebruiken, worde de volgende orders gemaakt:

- Een geplande order voor een hoeveelheid van *15 stuks* en de datum *10-10-22* (De hoeveelheid wordt verminderd met de bestaande inkooporder die gedurende dezelfde prognoseperiode is gedateerd.)
- Een geplande order voor een hoeveelheid van *25 stuks* en de datum *15-10-22* (De hoeveelheid is de volledige hoeveelheid van de prognose.)

### <a name="example-5-plans-that-use-no-reduction"></a>Voorbeeld 5: Plannen zonder vermindering

Wanneer u een plan uitvoert waarbij de prognosereductiemethode *Geen* is, wordt bij de hoofdplanning altijd een gepland aanbod gemaakt voor alle aanbodprognoseregels. Nadat het geplande aanbod is goedgekeurd, worden toekomstige geplande orders verminderd. Aanbodprognoseregels worden echter niet beperkt door inkooporders.

Stel dat u een artikel met het standaardordertype *Inkooporder* hebt. Het bevat de volgende aanbodprognoseregel.

| Model    | Datum     | Leveranciersaccount | Leveranciersgroep | Quantity | Eenheid | Site | Magazijn |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10-10-22 | US-101         |              | 25       | Stuk   | 1    | 11        |

Er is een bestaande inkooporder voor leverancier *US-101*, vestiging *1*, magazijn *11*, een hoeveelheid van *25* stuks en de datum *10-10-2022* (10 oktober 22). 

Wanneer u een hoofdplan uitvoert dat is ingesteld om *Geen* te gebruiken als reductiemethode, wordt een geplande inkooporder gemaakt voor leverancier *US-101*, vestiging *1*, magazijn *11*, een hoeveelheid van 25 *stuks* en de datum *10-10-22*. Met andere woorden, de bestaande inkooporder wordt niet verminderd omdat de prognosereductiemethode *Geen* is.

U bewerkt nu de geplande inkooporder die na de laatste planningsrun is gemaakt en wijzigt de hoeveelheid in *15 stuks*. Vervolgens keurt u de inkooporder goed. De volgende keer dat u het hoofdplan uitvoert, wordt een geplande inkooporder gemaakt voor leverancier *US-101*, vestiging *1*, magazijn *11*, een hoeveelheid van *10 stuks* en de datum *10-10-22*. Deze keer wordt de hoeveelheid verminderd om de hoeveelheid van de bestaande goedgekeurde order uit de vorige planningsrun weer te geven.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Verschillen tussen Planningsoptimalisatie en de ingebouwde planningsengine

Aanbodprognoses werken iets anders, afhankelijk van de planningsengine die u gebruikt (ingebouwde hoofdplanning of Planningsoptimalisatie). In deze sectie worden de verschillen beschreven.

### <a name="vendor-groups"></a>Leveranciersgroepen

Wanneer u een prognoseregel toevoegt, kunt u een leverancier en een leveranciersgroep opgeven. In de ingebouwde planningsengine worden gemaakte geplande orders gegroepeerd op de combinatie van de waarden voor leverancier en leveranciersgroep. In Planningsoptimalisatie worden geplande orders gegroepeerd op leverancier.

In de volgende tabel vindt u enkele voorbeelden van aanbodprognoseregels voor een artikel.

| Model    | Datum     | Leveranciersaccount | Leveranciersgroep | Quantity | Eenheid | Site | Magazijn |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10-10-22 |                | VendorGroupA | 5        | Stuk   | 1    | 11        |
| CurrentF | 10-10-22 |                | VendorGroupA | 6        | Stuk   | 1    | 11        |
| CurrentF | 10-10-22 |                |              | 7        | Stuk   | 1    | 11        |

Leverancier *VendorA* is de standaardleverancier voor leveranciersgroep *VendorGroupA*. Het is ook de standaardleverancier voor het artikel.

De ingebouwde planningsengine maakt de volgende orders:

- Een geplande inkooporder voor leverancier *VendorA*, leveranciersgroep *VendorGroupA* en een hoeveelheid van *11*
- Een geplande inkooporder voor leverancier *VendorA* en een hoeveelheid van *7*

Met Planningsoptimalisatie wordt slechts één order gemaakt:

- Een geplande inkooporder voor leverancier *VendorA*, leveranciersgroep *VendorGroupA* en een hoeveelheid van *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Vermindering van algemene prognoses met specifiekere prognoses

In de ingebouwde hoofdplanningsengine is het resultaat onvoorspelbaar als sommige prognoses wel een leverancier bevatten, maar andere niet.

In Planningsoptimalisatie worden algemene prognoses altijd verminderd met specifiekere prognoses, zoals in het volgende voorbeeld wordt laten zien.

In de volgende tabel vindt u enkele voorbeelden van aanbodprognoseregels voor een artikel.

| Datum       | Quantity | Leverancier   | Leveranciersgroep  |
|------------|----------|----------|---------------|
| 11-02-2022 | 5.00     | Vendor-A | VendorGroup-A |
| 11-02-2022 | 6,00     | Vendor-A | VendorGroup-A |
| 11-02-2022 | 15.00    |          |               |

De algemene prognose (voor 15,00 stuks) wordt verminderd met de specifiekere prognoses (voor 5,00 + 6,00 = 11,00 stuks). De rest wordt toegewezen aan de standaardleverancier. De volgende tabel bevat de geplande orders.

| Datum       | Quantity | Leverancier   | Leveranciersgroep  |
|------------|----------|----------|---------------|
| 11-02-2022 | 11.00    | Vendor-A | VendorGroup-A |
| 11-02-2022 | 4.00     | Vendor-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Respect voor standaardorderinstellingen bij het genereren van geplande orders

Elk artikel kan standaardorderinstellingen hebben, zoals een minimale inkooporderhoeveelheid. Deze instellingen worden door de ingebouwde planningsengine genegeerd en hierdoor worden prognoses omgezet in geplande orders met dezelfde hoeveelheid. Planningsoptimalisatie respecteert deze instellingen wanneer geplande orders worden gegenereerd op basis van aanbodprognoses. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Samenvoeging van geplande orders als gevolg van vermindering met goedgekeurde orders

De ingebouwde hoofdplanningsengine gaat ervanuit dat de bestaande aanbodprognose slechts met één order wordt verminderd. Als verschillende orders overeenkomen met een aanbodprognoseregel, wordt deze dus alleen met de eerste order verminderd. In Planningsoptimalisatie wordt de aanbodprognoseregel verminderd met alle orders die overeenkomen.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Alleen vermindering van prognoses met overeenkomende leveranciers

Wanneer de ingebouwde hoofdplanningsengine een prognose vermindert met bestaande vrijgegeven inkooporders, betekent dit niet dat de leverancier op de inkooporder overeenkomt met de leverancier uit de prognose. Planningsoptimalisatie vermindert prognoses alleen met inkooporders met een overeenkomende waarde in het leveranciersveld.

Voor transfer- en productieorders wordt het leveranciersveld altijd genegeerd, omdat dit niet relevant is voor die ordertypen.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Vermindering van prognoses door transferorders

Als het standaardordertype voor een artikel *Transfer* is, kunnen prognoses alleen worden verminderd met bestaande geplande transferorders. Voor productie- en inkooporders verminderen echter alleen vrijgegeven orders de aanbodprognose.

De ingebouwde planningsengine vermindert prognoses voor alle statussen van transferorders terwijl in Planningsoptimalisatie prognoses alleen worden verminderd met transferorders met de status *Vrijgegeven*.

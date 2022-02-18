---
title: Bewustzijn tussen grootboekvereffening en jaarafsluiting
description: Dit onderwerp bevat informatie over verbeteringen die van invloed zijn op grootboekvereffeningen en de jaarafsluiting van het grootboek.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: acfbcf1467363262769884063efbc1a6d6e21eb1
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075565"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Bewustzijn tussen grootboekvereffening en jaarafsluiting

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 Finance versie 10.0.25 is de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** beschikbaar in het werkgebied **Functiebeheer**. Met deze functie worden twee primaire verbeteringen toegevoegd die van invloed zijn op de grootboekvereffening en de jaarafsluiting van het grootboek.

Tijdens de jaarafsluiting van het grootboek worden grootboektransacties die zijn vereffend, niet meer opgenomen in het openingssaldo van het volgende fiscale jaar. Deze verbetering zorgt ervoor dat alleen niet-vereffende grootboektransacties in het openingssaldo worden opgenomen. Het is belangrijk wanneer herwaardering in vreemde valuta voor het grootboek wordt uitgevoerd. Herwaardering in vreemde valuta wordt alleen uitgevoerd voor grootboektransacties met de status **Niet vereffend**. Vóór release van de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** bevatte het openingssaldo zowel transacties met de status **Vereffend** als transacties met de status **Niet vereffend**, en werd de status van het samengevatte bedrag ingesteld op **Niet vereffend**.

Met de tweede verbetering kunt u gedetailleerde openingssaldotransacties tijdens de jaarafsluiting van het grootboek boeken. Als de optie **Details behouden tijdens jaarafsluiting** is ingesteld op **Ja**, wordt een afzonderlijk openingssaldo gemaakt voor elke grootboektransactie die niet is vereffend. Deze instelling wordt gedefinieerd voor elke hoofdrekening in de instellingen van de grootboekvereffening. Door gedetailleerde transacties voor het openingssaldo te behouden, kunt u de niet-vereffende grootboektransacties in het volgende fiscale jaar veel beter vereffenen.

Ter ondersteuning van de nieuwe verbeteringen zijn wijzigingen aangebracht in grootboekvereffening en de jaarafsluiting.

### <a name="changes-to-ledger-settlement"></a>Wijzigingen in grootboekvereffening

- Grootboekvereffening moet binnen een fiscaal jaar worden uitgevoerd.
- Grootboekvereffening moet worden uitgevoerd voor transacties in één hoofdrekening. De hoofdrekening is nu een vereist filter op de pagina **Grootboekvereffening**.
- Grootboekvereffening en terugboeking van grootboekvereffening kunnen niet worden uitgevoerd voor transacties die in een afgesloten fiscaal jaar zijn geboekt (met andere woorden: de jaarafsluiting is uitgevoerd).

### <a name="changes-to-year-end-close"></a>Wijzigingen in jaarafsluiting

- Een jaarafsluiting kan niet worden teruggeboekt als er openingssaldotransacties zijn vereffend in het volgende fiscale jaar. Deze wijziging is van toepassing wanneer een jaarafsluiting wordt teruggeboekt of wanneer een jaarafsluiting opnieuw wordt uitgevoerd en de optie **Bestaande jaarafsluitingsposten verwijderen bij het opnieuw afsluiten van het jaar** is ingesteld op **Ja** in grootboekparameters.
- Als de optie **Details behouden tijdens jaarafsluiting** is ingesteld op **Ja** voor een balansrekening in de grootboekvereffening, worden er gedetailleerdere openingssaldotransacties gemaakt voor die hoofdrekening.

## <a name="before-you-enable-the-feature"></a>Voordat u de functie inschakelt

Vanwege de wijzigingen in functionaliteit en het gegevensmodel is het belangrijk dat u rekening houdt met de volgende punten voordat u de functie inschakelt:

- Van alle transacties die zijn gemarkeerd voor vereffening maar nog niet zijn vereffend, wordt de markering automatisch ongedaan gemaakt als de functie wordt ingeschakeld. Om te voorkomen dat werk verloren gaat, vereffent u alle gemarkeerde transacties voordat u de functie inschakelt.
- In sommige organisaties wordt de jaarafsluiting meerdere keren voor hetzelfde fiscale jaar uitgevoerd. Schakel deze functie niet in als de jaarafsluiting al een keer is uitgevoerd en opnieuw wordt uitgevoerd voor hetzelfde fiscale jaar. De functie moet zijn ingeschakeld voordat u de eerste jaarafsluiting verwerkt of nadat u de laatste jaarafsluiting voor het fiscale jaar hebt verwerkt.

  Als u de functie wilt inschakelen, maar de jaarafsluiting al een keer uitgevoerd, moet u de jaarafsluiting terugboeken voordat u de functie kunt inschakelen.

- Aangezien vereffening in meerdere fiscale jaren niet langer is toegestaan, is het raadzaam de functie in te schakelen voordat u met het jaarafsluitingsproces begint. Om vervolgens te zorgen dat de openingssaldi van het volgende fiscale jaar niet worden beïnvloed door eerdere vereffeningen voor meerdere fiscale jaren, moet de openingssaldotransactie worden vereffend voor het fiscale jaar dat wordt afgesloten.
- Aangezien vereffening voor meerdere hoofdrekeningen niet langer is toegestaan, moet u het rekeningschema of de processen zo nodig aanpassen om ervoor te zorgen dat de grootboekvereffening voor dezelfde hoofdrekening kan worden uitgevoerd.
- De functie kan niet worden ingeschakeld als de jaarafsluiting voor de openbare sector wordt gebruikt.

## <a name="set-up-ledger-settlement"></a>Grootboekvereffening instellen

Nadat u de functie hebt ingeschakeld en voordat u de volgende jaarafsluiting uitvoert, moet elke organisatie bepalen of de transactiedetails tijdens de jaarafsluiting worden behouden. De keuze heeft geen invloed op openingssaldoboekingen van eerdere jaarafsluitingsprocessen.

De optie **Details behouden tijdens jaarafsluiting** wordt ingesteld voor elke hoofdrekening op de pagina **Grootboekvereffening instellen**.

1.  Ga naar **Grootboek** > **Grootboek instellen** > **Grootboekparameters**.
2.  Selecteer **Rekeningen voor grootboekvereffeningen** op het tabblad **Grootboekvereffeningen**.

– of –

1.  Ga naar **Grootboek** > **Periodieke taken** > **Grootboekvereffeningen**.
2.  Selecteer **Rekeningen voor grootboekvereffeningen**.

Er zijn twee kolommen toegevoegd aan de pagina **Grootboekvereffeningen**:
    
- **Type hoofdrekening**: deze kolom is alleen bedoeld ter informatie. Het geeft het type weer dat aan de hoofdrekening is toegewezen.
- **Details behouden tijdens jaarafsluiting**: standaard is de optie ingesteld op **Nee**. De waarde kan alleen op **Ja** worden ingesteld als de waarde in de kolom **Type hoofdrekening** **Balans**, **Activum** of **Passivum** is. Wanneer de optie is ingesteld op **Nee**, worden de openingssaldi verkort geboekt, zoals gebruikelijk is tijdens de jaarafsluiting. Als de optie is ingesteld op **Ja**, worden openingssaldi in gedetailleerde vorm gemaakt voor elke grootboektransactie die niet voor de hoofdrekening is vereffend.

## <a name="year-end-close"></a>Jaarafsluiting

Wanneer u de jaarafsluiting uitvoert door naar **Grootboek** > **Afgesloten periode** > **Jaarafsluiting** te gaan, worden tijdens het proces de openingssaldi gemaakt voor de hoofdrekeningen die voor grootboekvereffening zijn gedefinieerd. De openingssaldi worden in verkorte of gedetailleerde vorm gemaakt, afhankelijk van de bijbehorende instellingen voor grootboekvereffening. Grootboektransacties die worden vereffend, worden uitgesloten ongeacht of u het openingssaldo voor elke hoofdrekening verkort of gedetailleerd hebt geboekt.

Meerdere transacties worden bijvoorbeeld naar hoofdrekening 130100 in fiscaal jaar 2021 geboekt.

| Journaalnummer | Boekstuk  | Datum       | Type      | Grootboekrekening | Rekeningnaam        | Description       | Valuta | Bedrag in transactievaluta | Bedrag  | Bedrag in aangiftevaluta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 03-12-2021  | Bezig met uitvoeren | 130100-001-    | Debiteuren | Servicekosten       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 05-12-2021  | Bezig met uitvoeren | 130100-002-    | Debiteuren | Gas, water, elektriciteit         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16-12-2021 | Bezig met uitvoeren | 130100-001-    | Debiteuren | Restitutie            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 20-12-2021 | Bezig met uitvoeren | 130100-002-    | Debiteuren |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20-12-2021 | Bezig met uitvoeren | 130100-002-    | Debiteuren |                   | EUR      | -127,11                        | -174,12 | -174,12                      |
| 20856          | CMV-4010 | 21-12-2021 | Bezig met uitvoeren | 130100-002-    | Debiteuren | Tegoed op rekening | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28-12-2021 | Bezig met uitvoeren | 130100-001-    | Debiteuren | Gas, water, elektriciteit         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29-12-2021 | Bezig met uitvoeren | 130100-002-    | Debiteuren | Service           | USD      | 300                            | 300     | 300                          |

Van deze transacties worden er drie vereffend tijdens de grootboekvereffening.

Er is een factuur voor 175 US dollar (USD 175). Deze factuur is betaald met een betaling in euro (EUR) en er is een contantkorting gebruikt.

| Journaalnummer | Boekstuk  | Datum       | Type      | Grootboekrekening | Rekeningnaam        | Description | Valuta | Bedrag in transactievaluta | Bedrag  | Bedrag in aangiftevaluta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 05-12-2021  | Bezig met uitvoeren | 130100-002-    | Debiteuren | Gas, water, elektriciteit   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20-12-2021 | Bezig met uitvoeren | 130100-002-    | Debiteuren |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20-12-2021 | Bezig met uitvoeren | 130100-002-    | Debiteuren |             | EUR      | -127,11                        | -174,12 | -174,12                      |

De resultaten voor hoofdrekening 130100 zijn afhankelijk van de vraag of de functie is ingeschakeld voordat de jaarafsluiting wordt uitgevoerd. Als de functie is ingeschakeld, is het resultaat ook afhankelijk van de instelling van de optie Details behouden tijdens de jaarafsluiting.

### <a name="the-feature-isnt-enabled"></a>De functie is niet ingeschakeld
Bij de jaarafsluiting worden drie openingssaldotransacties gemaakt voor hoofdrekening 130100 in 2022. De som van de transacties in de valuta voor boekhouding is USD 525.

| Journaalnummer | Boekstuk  | Datum     | Type    | Grootboekrekening | Rekeningnaam        | Description | Valuta | Bedrag in transactievaluta | Bedrag  | Bedrag in aangiftevaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-002-    | Debiteuren |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-001-    | Debiteuren |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-002-    | Debiteuren |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Zelfs als de betalingstransactie voor EUR -127,11 in het grootboek is vereffend, komt de transactie nog steeds naar voren als een beginsaldo.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>De functie is ingeschakeld en de optie Details behouden tijdens de jaarafsluiting = Nee

Bij de jaarafsluiting worden twee openingssaldotransacties gemaakt voor hoofdrekening 130100 in 2022. De som van de transacties in de valuta voor boekhouding is nog steeds USD 525, maar de in het grootboek vereffende transacties worden uitgesloten van het openingssaldo. Het totaalbedrag voor rekening 130100-002- is USD 125 in plaats van USD 299,12 en de transactie voor EUR 127,11/USD 174,12 wordt geheel uitgesloten.

| Journaalnummer | Boekstuk  | Datum     | Type    | Grootboekrekening | Rekeningnaam        | Description | Valuta | Bedrag in transactievaluta | Bedrag | Bedrag in aangiftevaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-002-    | Debiteuren |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-001-    | Debiteuren |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>De functie is ingeschakeld en de optie Details behouden tijdens de jaarafsluiting = Ja

Bij de jaarafsluiting worden vijf openingssaldotransacties gemaakt voor hoofdrekening 130100 in 2022. Voor elk van de vijf transacties die niet zijn vereffend, wordt een afzonderlijke openingssaldotransactie gemaakt. De som van de transacties in de valuta voor boekhouding is nog steeds USD 525.

| Journaalnummer | Boekstuk  | Datum     | Type    | Grootboekrekening | Rekeningnaam        | Description       | Valuta | Bedrag in transactievaluta | Bedrag | Bedrag in aangiftevaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-001-    | Debiteuren | Servicekosten       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-001-    | Debiteuren | Restitutie            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-002-    | Debiteuren | Tegoed op rekening | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-001-    | Debiteuren | Gas, water, elektriciteit         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1-1-2022 | Opening | 130100-002-    | Debiteuren | Service           | USD      | 300                            | 300    | 300                          |

Wanneer transactiedetails worden behouden, heeft dit geen invloed op de oorspronkelijke gedetailleerde transacties. Deze blijven geboekt en niet-vereffend in het fiscale jaar dat wordt afgesloten. Er wordt een kopie van deze transacties gemaakt voor het openingssaldo. De volgende waarden van de oorspronkelijke transacties worden naar de openingssaldotransacties gekopieerd.

- Grootboekrekening (de hoofdrekening en alle financiële dimensies)
- Bedragen in de valuta´s voor transacties, boekhouding en rapportage
- Description
- Boekingslaag
- Boekingstype

   > [!NOTE]
   > Aan geen andere openingssaldotransacties wordt een boekingstype toegewezen. Daarom kan het boekingstype worden gebruikt om onderscheid te maken tussen openingstransacties die gedetailleerd naar voren zijn gebracht.

Sommige velden van de oorspronkelijke transacties moeten worden gewijzigd in gedetailleerde openingssaldotransacties. De datum van openingssaldotransacties is altijd de eerste dag van het volgende fiscale jaar. Het journaalnummer moet worden gewijzigd en het boekstuknummer wordt gewijzigd in de waarde die is ingevoerd in het dialoogvenster voor jaarafsluiting.

Informatie van de oorspronkelijke transacties vindt u op de pagina **Grootboekvereffening**. Elke gedetailleerde openingssaldotransactie bevat de kolom **Oorspronkelijke transactiedatum** in het raster. Deze kolom kan u helpen transacties in het nieuwe fiscale jaar af te stemmen. U kunt **Oorspronkelijke boekstuk weergeven** selecteren om weer in te zoomen op het volledige oorspronkelijke boekstuk.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Transacties vereffenen
Als u grootboektransacties wilt vereffenen, voert u de volgende stappen uit.

1. Ga naar **Grootboek** > **Periodieke taken** > **Grootboekvereffeningen**.
2.  Stel de filters bovenaan de pagina in.

    1. Selecteer een datumbereik. U kunt ook een datumintervalcode selecteren om automatisch in het datumbereik in te vullen.

       - Het datumbereik kan niet meerdere fiscale jaren beslaan. Als het datumbereik meerdere fiscale jaren beslaat, worden er geen transacties weergegeven als u **Transacties weergeven** selecteert.
       - Als het datumbereik in een open fiscaal jaar valt, kunnen transacties worden vereffend en kan de vereffening worden teruggeboekt. Als het datumbereik in een afgesloten fiscaal jaar valt of als de jaarafsluiting is voltooid, worden transacties weergegeven, maar kunnen ze niet worden vereffend of kan de vereffening ervan niet ongedaan worden gemaakt. U kunt de markering van transacties alleen in een afgesloten fiscaal jaar ongedaan maken. Als het datumbereik in een afgesloten fiscaal jaar valt, zijn de knoppen **Selectie markeren**, **Gemarkeerde transacties vereffenen** en **Gemarkeerde transacties omkeren** niet beschikbaar.

    2. Selecteer de hoofdrekening waarvoor u transacties wilt weergeven. Dit veld is verplicht. De opzoekactie toont alleen de hoofdrekeningen die zijn geselecteerd op de pagina **Grootboekvereffening** voor het rekeningschema van het bedrijf.
    3. Selecteer de boekingslaag. U kunt geen transacties vereffenen in verschillende boekingslagen.
    4. Als u de hoofdrekening en dimensies in afzonderlijke kolommen wilt weergeven, selecteert u een set met financiële dimensies.

3.  Selecteer **Transacties weergeven** als u alle transacties wilt weergeven die overeenkomen met de filters die u hebt ingesteld. Als u een van de filters of de dimensiesets wijzigt, moet u **Transacties weergegeven** opnieuw selecteren.
4.  Selecteer regels voor vereffening. De waarde in het veld **Geselecteerd bedrag** bovenaan de pagina wordt verhoogd of verlaagd om het totale bedrag op de geselecteerde regels weer te geven.
5.  Als u klaar bent met het selecteren van transacties, selecteert u **Selectie markeren**. Er wordt een vinkje weergegeven in de kolom **Gemarkeerd** voor elke geselecteerde transactie. De waarde in het veld **Gemarkeerd bedrag** bovenaan het raster wordt bovendien verhoogd of verlaagd om het totale bedrag op de gemarkeerde regels weer te geven.
6.  Als de waarde in het veld **Gemarkeerd bedrag** **0** (nul) is, selecteert u **Gemarkeerde transacties vereffenen**.

    - Gedeeltelijke vereffening is niet toegestaan. U kunt bijvoorbeeld een debettransactie van $100 niet vereffenen met een credittransactie van $90. De credittransactie van de resterende $10 moet ook worden gemarkeerd voor opname in de vereffening.
    - Voer een vereffeningsdatum in. De datum moet op of na de laatste datum van de transacties liggen die zijn gemarkeerd voor vereffening.

De status van de gemarkeerde transacties wordt bijgewerkt in **Vereffend**.

> [!IMPORTANT]
> Alle transacties die zijn gemarkeerd voor vereffening voor de actieve rechtspersoon en de geselecteerde hoofdrekening worden vereffend. De transacties hoeven niet op de pagina te worden weergegeven. Ze worden zelfs vereffend als ze verborgen zijn vanwege een filter.

Bij sommige processen, zoals het terugboeken van een transactie, worden grootboektransacties automatisch vereffend. Een betaling en factuur worden bijvoorbeeld vereffend in Klanten en met de vereffening wordt een gerealiseerde winst/verlies gegenereerd. Bij de vereffening van de betaling en factuur worden geen grootboektransacties vereffend, zoals transacties voor de grootboekrekening van Klanten. Als de vereffening van betaling en factuur echter ongedaan wordt gemaakt in Klanten, zorgt de stornoboekingspost die tijdens het terugdraaien van de vereffening in Klanten is geboekt, ervoor dat de oorspronkelijke en stornoboekingsposten in het grootboek worden vereffend. Als de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** is ingeschakeld, vindt de grootboekvereffening van een terugboeking niet automatisch plaats als de terugboekingsdatum in een ander fiscaal jaar valt.

## <a name="use-excel-for-ledger-settlement"></a>Excel gebruiken voor grootboekvereffening

Transacties die worden weergegeven op de pagina **Grootboekvereffening**, kunnen naar Excel worden geëxporteerd. In Excel kunt u transacties verder filteren om te bepalen welke transacties u wilt markeren voor vereffening.
Met beide grootboekvereffeningsentiteiten worden alleen grootboektransacties geëxporteerd voor de hoofdrekening die is geselecteerd op de pagina **Grootboekvereffening**. Hoewel markering van transacties voor afgesloten fiscale jaren nog steeds kan worden uitgevoerd of ongedaan kan worden gemaakt met Excel, kunnen ze niet worden vereffend. Bovendien kunnen vereffende transacties niet worden teruggeboekt voor dat fiscale jaar.

## <a name="make-transactions-easier-to-find"></a>Transacties eenvoudiger te vinden maken

De pagina **Grootboekvereffeningen** bevat mogelijkheden waardoor het gemakkelijker wordt om de transacties weer te geven die u nodig hebt voor vereffening.

•   Met het filter **Gemarkeerd** kunt u transacties filteren op basis van de vraag of het selectievakje **Gemarkeerd** ervoor is ingeschakeld.
•   Met het filter **Status** kunt u transacties filteren op basis van de status ervan.
•   Selecteer **Sorteren op absoluut bedrag** om de bedragen op absolute waarde te sorteren. Op deze manier kunt u debet- en creditbedragen met hetzelfde bedrag groeperen.

## <a name="reverse-a-settlement"></a>Een vereffening omkeren

U kunt een vereffening omkeren die ten onrechte is aangebracht.

1.  Voer stap 1 tot en met 3 uit in het gedeelte [Transacties vereffenen](#settle-transactions) om de transacties weer te geven waarin u geïnteresseerd bent.
2.  Selecteer in het filter **Status** **Vereffend**.
3.  Selecteer regels voor terugboeking.
4.  Selecteer **Gemarkeerde transacties omkeren**. De status van alle transacties met dezelfde vereffenings-id wordt gewijzigd in **Niet vereffend**.

> [!IMPORTANT]
> Alle transacties met dezelfde vereffenings-id worden omgekeerd, zelfs als ze niet zijn gemarkeerd. Er zijn bijvoorbeeld vier regels gemarkeerd en vereffend. Alle vier de regels hebben dezelfde vereffenings-id. Als u een van deze vier regels markeert en vervolgens **Gemarkeerde transacties omkeren** selecteert, worden alle vier de regels omgekeerd.







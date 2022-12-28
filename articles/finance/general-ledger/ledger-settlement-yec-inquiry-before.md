---
title: De functie Bewustzijn tussen grootboekvereffening vóór jaarafsluiting met de querypagina
description: In dit artikel wordt uitgelegd hoe u de functie Bewustzijn tussen grootboekvereffening moet gebruiken met behulp van de querypagina voordat het proces van jaarafsluiting van het grootboek wordt uitgevoerd.
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853134"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>De functie Bewustzijn tussen grootboekvereffening vóór jaarafsluiting met de querypagina

Een hoofdwijziging in de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** (de **Bewustzijn**-functie) is dat grootboekvereffening in meerdere fiscale jaren niet mogelijk is. Deze beperking van meerdere jaren is alleen relevant voor grootboekvereffening, niet voor vereffeningen van klanten of crediteuren.

Voordat u de **Bewustzijn**-functie inschakelt, mogen voor het fiscale jaar dat de jaarafsluiting ondergaat, geen grootboektransacties worden vereffend over meerdere fiscale jaren. Transacties die zijn geboekt in het fiscale jaar waarvoor u de jaarafsluiting doet, moeten worden vereffend vanuit transacties die naar een ander fiscaal jaar zijn geboekt. De transacties kunnen dan opnieuw worden vereffend voor transacties in hetzelfde fiscale jaar.

Dit artikel beschrijft de stappen die nodig zijn om grootboektransacties die zijn vereffend in meerdere boekjaren te identificeren, hun vereffeningen ongedaan te maken en opnieuw te vereffenen. In het geleverde voorbeeld is fiscaal jaar 2021 afgesloten en u bereidt u zich voor om de jaarafsluiting voor fiscaal jaar 2022 uit te voeren.

Vanaf Microsoft Dynamics 365 Finance release 10.0.29 kunt u grootboektransacties identificeren, hun vereffening opgedaan maken en ze opnieuw vereffenen door een nieuwe querypagina te gebruiken die beschikbaar is. Als u op dit moment nog niet Finance release 10.0.29 of hoger gebruikt, kunt u de stappen vinden voor het identificeren, de vereffening opgedaan maken en het opnieuw vereffenen van grootboektransacties in de volgende artikelen:

- [Bewustzijn tussen grootboekvereffening vóór jaarafsluiting](ledger-settle-yec.md)
- [Functie Bewustzijn tussen grootboekvereffening na jaarafsluiting](ledger-settle-yec-after.md)

Zie [Grootboekvereffeningsonderzoek](ledger-settlement-inquiry.md) voor meer informatie over het nieuwe queryvenster. 

## <a name="example-setup"></a>Voorbeeld van instellingen

In de volgende afbeelding worden de transacties weergegeven die voor hoofdrekening 110200 zijn geboekt. De grootboektransacties in het groen zijn grootboek-vereffend in hetzelfde fiscale jaar en hoeven niet te worden gewijzigd. De transacties in rood zijn grootboek-vereffend, maar ze hebben transactiedatums in verschillende fiscale jaren. Die transacties moeten worden geïdentificeerd en de grootboekvereffening moet mogelijk worden omgekeerd.

![Geboekte grootboektransacties.](./media/ledgersettlement.png)

## <a name="example"></a>voorbeeld

Volg deze stappen als uw organisatie de functie **Bewustzijn** wil gebruiken voordat u de jaarafsluiting voor fiscaal jaar 2022 uitvoert.

> [!NOTE]
> De jaarafsluiting voor 2021 en eerdere fiscale jaren moet alleen opnieuw worden uitgevoerd als nieuwe transacties worden geboekt naar fiscaal jaar 2021 of eerder. Wanneer u de volgende procedure uitvoert, worden er geen nieuwe transacties geboekt naar 2021. Daarom hoeft de jaarafsluiting niet opnieuw te worden uitgevoerd.
>
> Grootboektransacties die zijn vereffend in meerdere fiscale jaren, kunnen grootboekvereffend blijven als ze niet zijn vereffend met een transactie die naar 2022 (het jaar dat wordt afgesloten) of later is geboekt. Als u bijvoorbeeld transacties in 2019 en 2020 hebt vereffend, kunnen deze vereffend blijven.

1. Schakel de functie **Bewustzijn** **niet** in.
2. Selecteer **Vereffeningen over meerdere jaren controleren** op de pagina **Grootboekvereffeningen**.
3. Identificeer alle transacties die zijn geboekt in andere fiscale jaren, maar zijn vereffend met transacties die in 2022 zijn geboekt.

    1. Selecteer fiscaal jaar 2022, het jaar waarvoor u het jaarafsluitingsproces wilt uitvoeren.
    2. Selecteer in het veld **Financiële dimensieset** een waarde om de financiële dimensies weer te geven die u wilt bekijken voor de grootboekrekening. De hoofdrekening wordt altijd weergegeven, zelfs als de geselecteerde dimensiegroep geen hoofdrekening bevat.
    3. Selecteer **Transacties weergeven**.

    Op de querypagina worden alle transacties weergegeven voor alle grootboekrekeningen (zelfs als deze niet meer in de instellingen van de grootboekvereffening staan) van alle andere fiscale jaren die zijn vereffend met transacties die in 2022 zijn geboekt. Er worden drie verschillende grootboekrekeningen weergegeven.

    ![Vereffeningen van 2022 over meerdere jaren.](./media/review-cross-year.png)

3. Selecteer de kolom en houd deze vast (of klik met de rechtermuisknop) in het raster en selecteer vervolgens **Alle rijen exporteren**. Deze rijen zijn alle transacties die uit de transacties in 2022 moeten worden vereffend voordat de jaarafsluiting kan worden uitgevoerd. U wilt de gedetailleerde transactielijst, zodat u de transacties later op de juiste manier opnieuw kunt vereffenen.
4. Merk de fiscale jaren op waarvoor de transacties zijn geboekt. In dit voorbeeld zijn er transacties in 2021 en 2023.
5. Wijzig op de querypagina het fiscaal jaar in 2021, het eerste fiscaal jaar met transacties die zijn vereffend met transacties van 2022.
6. Filter op de kolom **Transactiedatum** , zodat alleen transacties worden opgenomen die naar 2022 zijn geboekt. Deze transacties zijn de gedetailleerde transacties uit 2022 die zijn vereffend met transacties in 2021.
7. Selecteer de kolom en houd deze vast (of klik met de rechtermuisknop) in het raster en selecteer vervolgens **Alle rijen exporteren**.

    > [!IMPORTANT]
    > In de volgende stappen wordt vereffening van deze transacties ongedaan gemaakt en vervolgens worden ze opnieuw vereffend met transacties in 2022. Het is van groot belang dat u dit detail behoudt in Excel.

    ![Vereffeningen van 2021 over meerdere jaren.](./media/review-cross-year.png)

8. Wijzig op de querypagina het fiscaal jaar in 2023, het volgende fiscaal jaar met transacties die zijn vereffend met transacties van 2022. 
9. Filter op de kolom **Transactiedatum** , zodat alleen transacties worden opgenomen die naar 2022 zijn geboekt. Deze transacties zijn de gedetailleerde transacties uit 2023 die zijn vereffend met transacties in 2022. 
10. Selecteer de kolom en houd deze vast (of klik met de rechtermuisknop) in het raster en selecteer vervolgens **Alle rijen exporteren**.

    > [!IMPORTANT]
    > In de volgende stappen wordt vereffening van deze transacties ongedaan gemaakt en vervolgens worden ze opnieuw vereffend met transacties in 2022. Het is van groot belang dat u dit detail behoudt in Excel.

    ![Vereffeningen van 2023 over meerdere jaren.](./media/filter-transactions.png)

11. Herhaal de vorige stappen voor elk fiscaal jaar met transacties die zijn vereffend met transacties in 2022. Exporteer altijd de gedetailleerde transacties naar Excel.

    Nadat alle gedetailleerde transacties van 2021 en 2023 naar Excel zijn geëxporteerd, kunt u de vereffening van transacties ongedaan maken via de nieuwe querypagina.

12. Wijzig het fiscaal jaar in 2022.
13. Selecteer alle records in het raster en selecteer vervolgens **Vereffening van gemarkeerde records ongedaan maken**. De vereffening van alle geselecteerde transacties in het raster worden ongedaan gemaakt.

    Er worden twee waarschuwingsberichten weergegeven om ervoor te zorgen dat de transactiedetails naar Excel worden geëxporteerd voordat de vereffening van de transacties ongedaan wordt gemaakt. Als u per ongeluk de vereffening van grootboektransacties ongedaan hebt gemaakt voordat u de details naar Excel hebt verzonden, kunt u het ongedaan maken niet meer terugdraaien.

    ![Vereffening van transacties voor meerdere vereffening ongedaan maken.](./media/revert-unsettle.png)

14. Gebruik de Excel-gegevens om het totaalbedrag te vinden van transacties in 2021 en 2023 die zijn vereffend met transacties in 2022. In dit voorbeeld zijn de transacties voor 2021 in totaal 525 USD en de transacties voor 2023 in totaal 700 USD.
15. Boek een corrigerend algemeen journaal om het openingssaldo voor 2022 op te splitsen in twee bedragen: het gedeelte dat was vereffend met fiscaal jaar 2021 en het gedeelte dat nog niet is vereffend voor 2022.

    - **Gedeelte van het openingssaldo dat is vereffend met het vorige jaar:** het eerste bedrag wordt 525 USD gebaseerd op de totalen die zijn gevonden en die zijn vereffend in 2021 en 2022.
    - **Gedeelte van het openingssaldo dat niet is vereffend met het vorige jaar:** het tweede bedrag is het verschil tussen het openingssaldo en het vereffende bedrag van 525 USD. Het resterende bedrag is 1025 - 525 = 500 USD.

    Op deze manier kunt u de transacties voor 2022 vereffenen met de 525 USD die oorspronkelijk was vereffend met de transactie van 2021. Deze stap is vereist omdat een grootboekvereffening geen gedeeltelijke vereffening toestaat.

    1. Ga naar het algemene journaal en boek de correctie. Uw organisatie moet op basis van de openstaande perioden bepalen welke transactiedatum er moet worden gebruikt. Deze transacties kunnen zijn vereffend met een vereffeningsdatum van januari of februari 2022, maar de correctie moet mogelijk in december worden geboekt als dat de enige openstaande periode is.
    2. Daarom kan het zijn dat u de parameter **Handmatige invoer niet toestaan** voor rekening 110200 op de pagina **Hoofdrekening** tijdelijk moet uitschakelen. Deze correctie wordt niet geboekt als handmatige invoer in de hoofdrekening niet is toegestaan.

    ![Een corrigerend algemeen journaal boeken.](./media/not-post.png)

16. U kunt de niet-vereffende transacties nu opnieuw vereffenen. Ga terug naar de pagina **Grootboekvereffeningen**, geef een datumbereik op van 1 januari tot en met 31 december 2022 en filter op hoofdrekening 110200. Gebruik vervolgens de gedetailleerde transacties die u naar Excel hebt geëxporteerd om de specifieke transacties te vinden die opnieuw moeten worden vereffend. De volgende afbeelding geeft de nu bestaande, niet-vereffende transacties weer.

    ![Niet-vereffende transacties.](./media/updated-unsettled.png)

    - Het openingssaldo van 1025 USD kan worden vereffend met de correctie voor -1025 USD.
    - De gedetailleerde transacties die niet zijn vereffend voor -400, -50 en -75 USD kunnen worden vereffend met de correctie voor 25 USD.

17. Schakel de functie **Bewustzijn** in. Nu kunt u de jaarafsluiting uitvoeren.

    - Voordat u de jaarafsluiting uitvoert, moet u de optie **Details behouden** selecteren in de instellingen voor de grootboekvereffening voor alle balansrekeningen. Kijk voor meer informatie in [Bewustzijn tussen grootboekvereffening en jaarafsluiting](awareness-between-ledger-settlement-year-end-close.md).
    - Wanneer u de jaarafsluiting voor 2022 start, als nog steeds transacties worden gevonden die in meerdere fiscale jaren waren vereffend, wordt u direct op de hoogte gesteld door het jaarafsluitingsproces. Deze situatie kan zich voordoen als gebruikers transacties in meerdere boekjaren hebben vereffend nadat u de vorige stappen hebt uitgevoerd.
    - Als transacties van 2021 en 2022 nog steeds zijn vereffend, moet u de functie **Bewustzijn** opnieuw uitschakelen en vervolgens de vorige stappen herhalen om de vereffening van de transacties ongedaan te maken. Deze benadering is vereist omdat 2021 is afgesloten en transacties niet kunnen worden vereffend in een afgesloten fiscaal jaar.
    - Als transacties van 2022 en 2023 nog steeds zijn vereffend, hoeft u de functie **Bewustzijn** niet uit te schakelen. Aangezien noch 2022 noch 2023 is afgesloten, kunt u de vorige stappen gebruiken om de transacties niet te vereffenen.

18. U kunt de 700 USD vanaf 2023 vereffenen met de gedetailleerde transacties die in 2023 als openingssaldi over zijn gebracht. Deze transactie wordt niet vereffend met de oorspronkelijke transactie in 2022.

Nadat de jaarafsluiting voor 2022 met succes is uitgevoerd, kunt u de functie **Bewustzijn** vanaf nu ingeschakeld laten.

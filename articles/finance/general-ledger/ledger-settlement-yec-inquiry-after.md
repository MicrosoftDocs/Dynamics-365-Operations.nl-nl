---
title: Bewustzijn tussen grootboekvereffening na jaarafsluiting met de querypagina
description: In dit artikel wordt uitgelegd hoe u de functie Bewustzijn tussen grootboekvereffening moet gebruiken met behulp van de querypagina nadat het proces van jaarafsluiting van het grootboek wordt uitgevoerd.
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
ms.openlocfilehash: 921d2a17409ae10cd9c22eeca11557ba1248b9bc
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853133"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close-using-the-inquiry-page"></a>Bewustzijn tussen grootboekvereffening na jaarafsluiting met de querypagina

Een hoofdwijziging in de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** (de **Bewustzijn**-functie) is dat grootboekvereffening in meerdere fiscale jaren niet mogelijk is. Deze beperking van meerdere jaren is alleen relevant voor grootboekvereffening, niet voor vereffeningen van klanten of crediteuren.

Voordat u de **Bewustzijn**-functie inschakelt, mogen voor het fiscale jaar dat de jaarafsluiting ondergaat, geen grootboektransacties worden vereffend over meerdere fiscale jaren. Transacties die zijn geboekt in het fiscale jaar waarvoor u de jaarafsluiting doet, moeten worden vereffend vanuit transacties die naar een ander fiscaal jaar zijn geboekt. De transacties kunnen dan opnieuw worden vereffend voor transacties in hetzelfde fiscale jaar.

Dit artikel beschrijft de stappen die nodig zijn om grootboektransacties die zijn vereffend in meerdere fiscale jaren te identificeren, hun vereffeningen ongedaan te maken en opnieuw te vereffenen. In het getoonde voorbeeld is fiscaal jaar 2022 afgesloten. De focus ligt op het voorbereiden van de grootboekvereffeningstransacties voordat de jaarafsluiting van 2023 wordt uitgevoerd.

Vanaf Microsoft Dynamics 365 Finance release 10.0.29 kunt u grootboektransacties identificeren, hun vereffening opgedaan maken en ze opnieuw vereffenen door een nieuwe querypagina te gebruiken die beschikbaar is. Als u op dit moment nog niet Microsoft Dynamics 365 Finance release 10.0.29 of hoger gebruikt, kunt u de stappen vinden voor het identificeren, de vereffening opgedaan maken en het opnieuw vereffenen van grootboektransacties in de volgende artikelen:

- [Bewustzijn tussen grootboekvereffening vóór jaarafsluiting](ledger-settle-yec.md)
- [Functie Bewustzijn tussen grootboekvereffening na jaarafsluiting](ledger-settle-yec-after.md)

Zie [Grootboekvereffeningsonderzoek](ledger-settlement-inquiry.md) voor meer informatie over het nieuwe queryvenster. 

## <a name="example-setup"></a>Voorbeeld van instellingen

In de volgende afbeelding worden de transacties weergegeven die voor hoofdrekening 110200 zijn geboekt. De grootboektransacties in het groen zijn grootboek-vereffend in hetzelfde fiscale jaar en hoeven niet te worden gewijzigd. De transacties in rood zijn grootboek-vereffend, maar ze hebben transactiedatums in verschillende fiscale jaren. Die transacties moeten worden geïdentificeerd en de grootboekvereffening moet mogelijk worden omgekeerd.

![Geboekte grootboektransacties.](./media/excel.png)

## <a name="example"></a>voorbeeld

Volg deze stappen als uw organisatie de functie **Bewustzijn** wil gebruiken nadat u de jaarafsluiting voor fiscaal jaar 2022 uitvoert.

> [!NOTE]
> De jaarafsluiting voor 2022 en eerdere fiscale jaren moet alleen opnieuw worden uitgevoerd als nieuwe transacties worden geboekt naar fiscaal jaar 2022 of eerder. Wanneer u de volgende procedure uitvoert, worden er geen nieuwe transacties geboekt naar 2022. Daarom hoeft de jaarafsluiting niet opnieuw te worden uitgevoerd.
>
> Grootboektransacties die zijn vereffend in meerdere fiscale jaren, kunnen grootboekvereffend blijven als ze niet zijn vereffend met een transactie die naar 2022 of later is geboekt. Als u bijvoorbeeld transacties in 2019 en 2020 hebt vereffend, kunnen deze vereffend blijven.

1. Voltooi de jaarafsluiting voor 2022 zonder dat de functie **Bewustzijn** is ingeschakeld.
2. Identificeer alle transacties die zijn geboekt in andere fiscale jaren, maar zijn vereffend met transacties die in 2023 zijn geboekt (het volgende fiscaal jaar dat wordt afgesloten).

    > [!NOTE]
    > Transacties van 2021 die zijn vereffend met 2022-transacties, zijn niet relevant omdat het jaar al is afgesloten voor 2022. Die transacties kunnen vereffend blijven.

    1. Selecteer **Vereffeningen over meerdere jaren controleren** op de pagina **Grootboekvereffeningen**.
    2. Selecteer fiscaal jaar 2023, het volgende jaar waarvoor u het jaarafsluitingsproces wilt uitvoeren.
    3. Selecteer in het veld **Financiële dimensieset** een waarde om de financiële dimensies weer te geven die u wilt bekijken voor de grootboekrekening. De hoofdrekening wordt altijd weergegeven, zelfs als de geselecteerde dimensiegroep geen hoofdrekening bevat.
    4. Selecteer **Transacties weergeven**.

    De querypagina toont alle transacties uit andere fiscale jaren die zijn vereffend met transacties die in 2023 zijn geboekt.

    ![Vereffeningen van 2023 over meerdere jaren.](./media/2023-cross-settlement.png)

3. Selecteer de kolom en houd deze vast (of klik met de rechtermuisknop) in het raster en selecteer vervolgens **Alle rijen exporteren**. Deze rijen zijn alle transacties die uit de transacties in 2022 moeten worden vereffend voordat de jaarafsluiting voor het volgende jaar (2023) kan worden uitgevoerd. U wilt een registratie van deze transacties.

    Nadat alle gedetailleerde transacties van 2022 naar Excel zijn geëxporteerd, kunt u de vereffening van transacties ongedaan maken via de querypagina.

4. Selecteer alle records in het raster en selecteer vervolgens **Vereffening van gemarkeerde records ongedaan maken**. De vereffening van alle geselecteerde transacties in het raster worden ongedaan gemaakt.

    Er worden twee waarschuwingsberichten weergegeven om ervoor te zorgen dat de transactiedetails naar Excel worden geëxporteerd voordat de vereffening van de transacties ongedaan wordt gemaakt. Als u per ongeluk de vereffening van grootboektransacties ongedaan hebt gemaakt voordat u de details naar Excel hebt verzonden, kunt u het ongedaan maken niet meer terugdraaien.

    ![Vereffeningen over meerdere jaren ongedaan maken.](./media/revert-settlement.png)

5. Gebruik de Excel-gegevens om het totaalbedrag te vinden van transacties in 2022 die zijn vereffend met transacties in 2023. In dit voorbeeld is het totaal van de transacties voor 2023 700 USD.
6. Boek een corrigerend algemeen journaal om het openingssaldo voor 2022 op te splitsen in twee bedragen: het gedeelte dat was vereffend de transactie van fiscaal jaar 2022 en het gedeelte dat nog niet is vereffend voor 2023.

    - **Gedeelte van het openingssaldo dat is vereffend met het vorige jaar:** het eerste bedrag wordt 700 USD gebaseerd op de totalen die zijn gevonden en die zijn vereffend in 2021 en 2022.
    - **Gedeelte van het openingssaldo dat niet is vereffend met het vorige jaar:** het tweede bedrag is het verschil tussen het openingssaldo en het vereffende bedrag van 700 USD. Het resterende bedrag is 1700 - 700 = 1000 USD.

    Op deze manier kunt u de transacties voor 2023 vereffenen met de 700 USD die oorspronkelijk was vereffend met de transactie van 2022. Deze stap is vereist omdat een grootboekvereffening geen gedeeltelijke vereffening toestaat.

    1. Ga naar het algemene journaal en boek de correctie. Uw organisatie moet op basis van de openstaande perioden in 2023 bepalen welke transactiedatum er moet worden gebruikt.
    2. Het kan zijn dat u de parameter **Handmatige invoer niet toestaan** op de pagina **Hoofdrekening** tijdelijk moet uitschakelen. Deze correctie wordt niet geboekt als handmatige invoer in de hoofdrekening niet is toegestaan.

    ![Een corrigerend algemeen journaal boeken.](./media/no-manual4.png)

7. U kunt de niet-vereffende transacties nu opnieuw vereffenen. Ga terug naar de pagina **Grootboekvereffening** en beperk het datumbereik tot: 1 januari tot en met 31 december 2023. Gebruik vervolgens de gedetailleerde transacties die u naar Excel hebt geëxporteerd om de specifieke transacties te vinden die opnieuw moeten worden vereffend. De volgende afbeelding geeft de nu bestaande, niet-vereffende transacties weer.

    ![Niet-vereffende 2023-transacties.](./media/2023-unsettled5.png)

    - Het openingssaldo van 1700 USD kan worden vereffend met de correctie voor -1700 USD.
    - De gedetailleerde transacties die niet zijn vereffend voor -700 USD kunnen worden vereffend met de correctie voor 700,00 USD.

8. Schakel de functie **Bewustzijn** in. Nu kunt u de jaarafsluiting uitvoeren.

    - Voordat u de jaarafsluiting voor 2023 uitvoert, moet u de optie **Details behouden** selecteren in de instellingen voor de grootboekvereffening voor alle balansrekeningen. Kijk voor meer informatie in [Bewustzijn tussen grootboekvereffening en jaarafsluiting](awareness-between-ledger-settlement-year-end-close.md).
    - Wanneer u de jaarafsluiting voor 2023 start, als nog steeds transacties worden gevonden die in meerdere fiscale jaren waren vereffend, wordt u direct op de hoogte gesteld door het jaarafsluitingsproces. Deze situatie kan zich voordoen als gebruikers transacties in fiscale jaren hebben vereffend voordat de functie **Bewustzijn** werd ingeschakeld.
    - Als transacties van 2022 en 2023 nog steeds zijn vereffend, moet u de functie **Bewustzijn** opnieuw uitschakelen en vervolgens de vorige stappen herhalen om de vereffening van de transacties ongedaan te maken. Deze benadering is vereist omdat 2022 is afgesloten en transacties niet kunnen worden vereffend in een afgesloten fiscaal jaar.

Nadat de jaarafsluiting voor 2022 met succes is uitgevoerd, kunt u de functie **Bewustzijn** vanaf nu ingeschakeld laten.

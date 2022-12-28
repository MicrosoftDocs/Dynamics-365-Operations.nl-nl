---
title: Functie Bewustzijn tussen grootboekvereffening vóór jaarafsluiting
description: In dit artikel wordt uitgelegd hoe u de functie Bewustzijn tussen grootboekvereffening moet gebruiken voordat het proces van jaarafsluiting van het grootboek wordt uitgevoerd.
author: kweekley
ms.date: 12/02/2022
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
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832157"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>Bewustzijn tussen grootboekvereffening vóór jaarafsluiting

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>Voorbereiding op Bewustzijn-functie van grootboekvereffening vóór jaarafsluiting

Een belangrijke wijziging in de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** (de **Bewustzijn**-functie) is dat grootboekvereffening in meerdere fiscale jaren niet mogelijk is. Deze beperking van meerdere jaren is alleen relevant voor grootboekvereffening, niet voor vereffeningen van klanten of crediteuren.

Voordat de **Bewustzijn**-functie is ingeschakeld, mogen voor het fiscale jaar dat de jaarafsluiting ondergaat, geen grootboektransacties worden vereffend over meerdere fiscale jaren. Transacties die zijn geboekt in het fiscale jaar waarvoor u de jaarafsluiting doet, moeten worden vereffend vanuit transacties die naar een ander fiscaal jaar zijn geboekt. De transacties kunnen dan opnieuw worden vereffend voor transacties in hetzelfde fiscale jaar.

Dit artikel beschrijft de stappen die nodig zijn om de grootboektransacties die zijn vereffend in meerdere fiscale jaren te identificeren, hun vereffeningen ongedaan te maken en opnieuw te vereffenen. In het geleverde voorbeeld is fiscaal jaar 2021 afgesloten en u bereidt u zich voor om de jaarafsluiting voor fiscaal jaar 2022 uit te voeren.

## <a name="example-setup"></a>Voorbeeld van instellingen

In de volgende afbeelding wordt de transacties weergegeven die voor hoofdrekening 110190 zijn geboekt. De grootboektransacties in het groen worden vereffend in hetzelfde fiscale jaar en hoeven niet te worden gewijzigd. De transacties in rood zijn grootboekvereffend, maar ze hebben transactiedatums in verschillende fiscale jaren. Die transacties moeten worden geïdentificeerd en de grootboekvereffening moet mogelijk worden omgekeerd.

![Grootboektransacties.](./media/YEC1.png)

## <a name="example"></a>voorbeeld

Volg deze stappen als uw organisatie de functie **Bewustzijn** wil gebruiken voordat de jaarafsluiting voor fiscaal jaar 2022 wordt uitgevoerd.

> [!NOTE]
> De jaarafsluiting voor 2021 en eerdere fiscale jaren moet alleen opnieuw worden uitgevoerd als nieuwe transacties worden geboekt naar fiscaal jaar 2021 of eerder. Wanneer u de volgende procedure uitvoert, worden er geen nieuwe transacties geboekt naar 2021. Daarom hoeft de jaarafsluiting niet opnieuw te worden uitgevoerd.
>
> Grootboektransacties die zijn vereffend in meerdere fiscale jaren, kunnen grootboekvereffend blijven als ze niet zijn vereffend met een transactie die naar 2022 of later is geboekt. Als u bijvoorbeeld transacties in heel 2019 en 2020 hebt vereffend, kunnen deze vereffend blijven.

1. Optioneel: de functie **Bewustzijn** tijdelijk inschakelen.

    - Als u ervoor kiest de functie in te schakelen, moet u deze later uitschakelen, zoals is aangegeven. Als u de functie nu inschakelt, kunt u tijdelijk voorkomen dat gebruikers grootboektransacties vereffenen die naar verschillende fiscale jaren zijn geboekt.
    - Als u ervoor kiest de functie niet in te schakelen, raden we u aan om uw team te vragen geen transacties in meerdere fiscale jaren te vereffenen. Als de vereffening over meerdere jaren plaatsvindt nadat de volgende stappen zijn voltooid, moet u de stappen herhalen om de grootboektransacties te bepalen en de vereffening van deze transacties ongedaan te maken.

2. Bepaal op de pagina **Grootboekvereffening** het totaal van alle transacties die zijn vereffend in fiscale jaren 2021 en 2022.

    1. Een datumbereik opgeven voor het hele fiscaal jaar 2021. Voer bijvoorbeeld 1 januari 2021 tot en met 31 december 2021 in als u een kalenderjaar als het fiscaal jaar gebruikt.

        Als de functie **Bewustzijn** is ingeschakeld, ontvangt u een waarschuwing dat transacties niet kunnen worden vereffend of niet vereffend voor een afgesloten fiscaal jaar. De waarschuwing is niet relevant omdat in deze stap geen vereffening of ongedaan maken van vereffening plaatsvindt.

    2. Selecteer **Vereffend** in het veld **Status**.
    3. Filter op één grootboekrekening tegelijk.

        - U moet deze stappen herhalen voor elke grootboekrekening waarvoor grootboekvereffening plaatsvindt.
        - Als er geen andere grootboekrekeningen meer zijn ingesteld voor grootboekvereffening, moet u deze mogelijk tijdelijk weer toevoegen aan de instellingen voor grootboekvereffening. Voltooi vervolgens deze stappen als die grootboekrekeningen transacties hebben in 2022 die zijn vereffend met transacties in een ander fiscaal jaar.

    4. Selecteer de kolom **Status** en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens om op deze kolom te groeperen.
    5. Selecteer de kolom **Bedrag in transactievaluta** en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens om het totaal te berekenen van deze kolom.

        - Als u alleen transacties hebt vereffend in 2021, is het totaal 0 (nul).
        - Als u transacties hebt die zijn vereffend in meerdere fiscale jaren, is het totaal niet 0 (nul).

        In de volgende afbeelding is er een saldo van 525,00 USD. Dit saldo is het totaal van de transacties die zijn vereffend met transacties in een ander fiscaal jaar. Uw totaal kan transacties bevatten die zijn vereffend tussen 2021 en 2022 en transacties die zijn vereffend tussen 2022 en 2023.

        ![Grootboektransacties 2021–2022.](./media/YEC2.png)

    6. Identificeren welke transacties zijn vereffend tussen 2020 en 2021 door verder te filteren op de waarde **Vereffeningsdatum**. Geef een datumbereikfilter op van 1 januari 2021 tot en met 31 december 2021. Er worden geen transacties weergegeven omdat er geen transacties van 2020 zijn vereffend met transacties die in 2021 zijn geboekt.
    7. Identificeren welke transacties zijn vereffend tussen 2021 en 2022 door het datumfilter te wijzigen van de waarde **Vereffeningsdatum**. Geef een datumbereikfilter op van 1 januari 2022 tot en met 31 december 2022. De transacties worden opnieuw weergegeven en het totaal wordt 525,00 USD omdat alle transacties zijn vereffend tussen 2021 en 2022.

3. Bepaal op de pagina **Grootboekvereffening** het totaal van alle transacties die zijn vereffend in fiscale jaren 2021 en 2022.

    1. Een datumbereik opgeven voor het hele fiscaal jaar 2022. Geef bijvoorbeeld 1 januari 2022 tot en met 31 december 2022 op als u een kalenderjaar als het fiscaal jaar gebruikt.
    2. Selecteer **Vereffend** in het veld **Status**.
    3. Filter op één grootboekrekening tegelijk.
    4. Selecteer de kolom **Status** en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens om op deze kolom te groeperen.
    5. Selecteer de kolom **Bedrag in transactievaluta** en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens om het totaal te berekenen van deze kolom.

        ![Totaal van grootboektransactiebedragen.](./media/YEC3.png)

    6. Voeg een extra filter toe aan de waarde van **Vereffeningsdatum**. Geef een datumbereikfilter op van 1 januari 2022 tot en met 31 december 2022. Het totaal van 525,00 USD wordt weergegeven. Dit resultaat valideert dat het totale bedrag aan transacties dat is vereffend in 2021 en 2022 is 525,00 USD.

        ![Grootboektransacties voor vereffeningsdatums in 2022 en 2023.](./media/YEC4.png)

    7. Wijzig het extra filter voor de waarde van **Vereffeningsdatum**. Geef een datumbereikfilter op van 1 januari 2023 tot en met 31 december 2023. Er wordt een nieuw totaal van 700 USD weergegeven. Dit totaal is het totaalbedrag van de transacties die zijn vereffend in 2022 en 2023.
 
4. Herhaal stap 3 voor fiscaal jaar 2023. Het totaal moet overeenkomen met 700 USD van 2022, omdat er geen transacties van 2023 zijn vereffend met transacties van 2024.
5. Als u de functie **Bewustzijn** hebt ingeschakeld in stap 1, schakelt u deze uit voordat u verder gaat naar stap 6. In de volgende stappen keert u de grootboekvereffening om die fiscale jaren heeft doorlopen. Als de functie **Bewustzijn** is ingeschakeld, kan grootboekvereffening voor fiscaal jaar 2021 niet worden omgekeerd. Daarom moet u de functie uitschakelen voordat u verdergaat.
6. Nadat de functie **Bewustzijn** is uitgeschakeld, gebruikt u dezelfde filters op de pagina **Grootboekvereffening** om de grootboekvereffening van de gedetailleerde transacties om te keren.

    1. Terug naar de pagina **Grootboekvereffening** en filter op transactiedatums voor 2021. Voeg een extra filter toe aan de waarde van **Vereffeningsdatum**. Geef een datumbereikfilter op vanaf 1 januari 2022 tot en met 31 december 2022. Zoek vervolgens de gedetailleerde transacties waar die samen het totaal van 525 USD vormen. Filteren voor deze informatie is mogelijk niet eenvoudig. U moet wellicht de gegevens verzenden naar Microsoft Excel om deze te beoordelen.
    2. Wanneer u de lijst met transacties hebt, selecteert u de grootboektransacties op de pagina **Grootboekvereffening** en selecteert u **Selectie markeren**. U hoeft niet beide zijden van de vereffende grootboektransacties te zien. Als u de debet- of de creditzijde markeert, worden alle gegevens met dezelfde **Vereffenings-id** omgekeerd, zelfs als de waarde **Gemarkeerd bedrag** niet **0** (nul) is.
    3. Selecteer **Gemarkeerde transacties omkeren** om de vereffening van de transacties ongedaan te maken.

    ![Keer gemarkeerde transacties om.](./media/YEC5.png)

7. Herhaal stap 6 om de vereffening om te keren voor de transacties die zijn vereffend in 2022 en 2023.

    ![Storneer grootboektransacties.](./media/YEC6.png)

8. Boek een corrigerend algemeen journaal om het openingssaldo voor 2022 op te splitsen in twee bedragen: het gedeelte dat is vereffend met de transactie van fiscaal jaar 2021 en het gedeelte dat nog niet is vereffend in 2022.

    - **Gedeelte van het openingssaldo dat is vereffend met het vorige jaar:** het eerste bedrag wordt 525 USD gebaseerd op de totalen die zijn gevonden en die zijn vereffend in 2021 en 2022.
    - **Gedeelte van het openingssaldo dat niet is vereffend met het vorige jaar:** het tweede bedrag is het verschil tussen het openingssaldo en het vereffende bedrag van 525 USD. Het resterende bedrag is 1025 - 525 = 500 USD.

    Op deze manier kunt u de transacties voor 2022 vereffenen met de 525 USD die oorspronkelijk was vereffend met de transactie van 2021. Deze stap is vereist omdat een grootboekvereffening geen gedeeltelijke vereffening toestaat.

    1. Ga naar het algemene journaal en boek de correctie. Uw organisatie moet op basis van de openstaande perioden bepalen welke transactiedatum er moet worden gebruikt. Deze transacties kunnen zijn vereffend met een vereffeningsdatum van januari of februari 2022, maar de correctie moet mogelijk in december worden geboekt als dat de enige openstaande periode is.
    2. Het kan zijn dat u de parameter **Handmatige invoer niet toestaan** op de pagina **Hoofdrekening** tijdelijk moet uitschakelen. Deze correctie wordt niet geboekt als handmatige invoer in de hoofdrekening niet is toegestaan.

    ![Correctie wordt niet geboekt.](./media/YEC7.png)

9. U kunt de niet-vereffende transacties nu opnieuw vereffenen. Ga terug naar de pagina **Grootboekvereffening** en beperk het datumbereik tot: 1 januari 2022 tot en met 31 december 2022. De volgende afbeelding geeft de nu bestaande, niet-vereffende transacties weer.

    ![Niet-vereffende transacties.](./media/YEC8.png)

    - Het openingssaldo van 1025 USD kan worden vereffend met de correctie voor -1025 USD.
    - De gedetailleerde transacties die niet zijn vereffend voor -400, -50 en -75 USD kunnen worden vereffend met de correctie voor 525,00 USD.

    ![Gedetailleerde transacties.](./media/YEC9.png)

10. Schakel de functie **Bewustzijn** in. Nu kunt u de jaarafsluiting uitvoeren.

    - Voordat u de jaarafsluiting uitvoert, moet u de optie **Details behouden** selecteren in de instellingen voor de grootboekvereffening voor alle balansrekeningen. Zie het Bewustzijn-document voor meer informatie over de voordelen van het uitvoeren van deze stap.
    - Wanneer u de jaarafsluiting voor 2022 start, als nog steeds transacties worden gevonden die in meerdere fiscale jaren zijn vereffend, wordt u direct op de hoogte gesteld door het jaarafsluitingsproces.
    - Als transacties van 2021 en 2022 nog steeds zijn vereffend, moet u de functie **Bewustzijn** opnieuw uitschakelen en de vorige stappen om de transacties niet te vereffenen opnieuw herhalen. Deze benadering is vereist omdat 2021 is afgesloten en transacties niet kunnen worden vereffend in een afgesloten fiscaal jaar.
    - Als transacties van 2022 en 2023 nog steeds zijn vereffend, hoeft u de functie **Bewustzijn** **niet** uit te schakelen. Aangezien noch 2022 noch 2023 is afgesloten, kunt u de vorige stappen gebruiken om de transacties niet te vereffenen.

Nadat de jaarafsluiting voor 2022 met succes is uitgevoerd, kunt u de functie **Bewustzijn** vanaf nu ingeschakeld laten.

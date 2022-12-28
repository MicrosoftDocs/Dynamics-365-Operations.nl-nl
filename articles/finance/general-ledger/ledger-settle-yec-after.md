---
title: Functie Bewustzijn tussen grootboekvereffening na de jaarafsluiting
description: In dit artikel wordt uitgelegd hoe u de functie Bewustzijn tussen grootboekvereffening moet gebruiken nadat het proces van jaarafsluiting van het grootboek wordt uitgevoerd.
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
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832160"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Functie Bewustzijn tussen grootboekvereffening na jaarafsluiting

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Voorbereiding op Bewustzijn-functie van grootboekvereffening na jaarafsluiting

Een belangrijke wijziging in de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** (de **Bewustzijn**-functie) is dat grootboekvereffening in meerdere fiscale jaren niet mogelijk is. Deze beperking van meerdere jaren is alleen relevant voor grootboekvereffening, niet voor vereffeningen van klanten of crediteuren.

Voordat de **Bewustzijn**-functie is ingeschakeld, mogen voor het fiscale jaar dat de jaarafsluiting ondergaat, geen grootboektransacties worden vereffend over meerdere fiscale jaren. Transacties die zijn geboekt in het fiscale jaar waarvoor u de jaarafsluiting doet, moeten worden vereffend vanuit transacties die naar een ander fiscaal jaar zijn geboekt. De transacties kunnen dan opnieuw worden vereffend voor transacties in hetzelfde fiscale jaar.

Dit artikel beschrijft de stappen die nodig zijn om de grootboektransacties die zijn vereffend in meerdere boekjaren te identificeren, hun vereffeningen ongedaan te maken en opnieuw te vereffenen. In het getoonde voorbeeld is fiscaal jaar 2022 afgesloten. De focus ligt op het voorbereiden van de grootboekvereffeningstransacties ruim voordat de jaarafsluiting van 2023 wordt uitgevoerd.

## <a name="example-setup"></a>Voorbeeld van instellingen

In de volgende afbeelding wordt de transacties weergegeven die voor hoofdrekening 110190 zijn geboekt. De grootboektransacties in het groen worden vereffend in hetzelfde fiscale jaar en hoeven niet te worden gewijzigd. De transacties in rood zijn grootboekvereffend, maar ze hebben transactiedatums in verschillende fiscale jaren. Die transacties moeten worden geïdentificeerd en de grootboekvereffening moet mogelijk worden omgekeerd.

![Grootboektransacties.](./media/afterYEC1.png)

## <a name="example"></a>voorbeeld

Volg deze stappen als uw organisatie de functie **Bewustzijn** wil gebruiken nadat u de jaarafsluiting voor fiscaal jaar 2022 uitvoert.

> [!NOTE]
> De jaarafsluiting voor 2022 en eerdere fiscale jaren moet alleen opnieuw worden uitgevoerd als nieuwe transacties worden geboekt naar fiscaal jaar 2022 of eerder. Wanneer u de volgende procedure uitvoert, mogen er geen nieuwe transacties worden geboekt naar 2022. Daarom hoeft de jaarafsluiting niet opnieuw te worden uitgevoerd.
>
> Grootboektransacties die zijn vereffend in meerdere fiscale jaren, kunnen grootboekvereffend blijven als ze niet zijn vereffend met een transactie die naar 2023 of later is geboekt. Als u bijvoorbeeld transacties in heel 2019 en 2020 hebt vereffend, kunnen deze vereffend blijven.

1. Voltooi de jaarafsluiting voor 2022 zonder dat de functie **Bewustzijn** is ingeschakeld.
2. Optioneel: nadat de jaarafsluiting voor 2022 is voltooid, schakelt u de functie **Bewustzijn** in. Als alle correcties zijn geboekt en het jaarafsluitingsproces niet opnieuw wordt uitgevoerd, wordt een jaarafsluiting als voltooid beschouwd.

    > [!IMPORTANT]
    > De functie **Bewustzijn** moet niet zijn ingeschakeld als de jaarafsluiting voor 2022 opnieuw wordt uitgevoerd. Als u de functie nu inschakelt, kunt u voorkomen dat gebruikers grootboektransacties vereffenen die naar verschillende fiscale jaren zijn geboekt.

    Als de jaarafsluiting niet is voltooid, kunt u toch de volgende stappen voltooien zonder de functie **Bewustzijn** in te schakelen. U moet de functie later inschakelen, zoals is aangegeven.

3. Bepaal op de pagina **Grootboekvereffening** het totaal van alle transacties die zijn vereffend in fiscale jaren 2022 en 2023. Merk op dat transacties van 2021 die zijn vereffend met 2022-transacties, niet relevant zijn, omdat het 2022 al is afgesloten. Die transacties kunnen vereffend blijven.

    1. Een datumbereik opgeven voor het hele fiscaal jaar 2022. Geef bijvoorbeeld 1 januari 2022 tot en met 31 december 2022 op als u een kalenderjaar als het fiscaal jaar gebruikt.
    2. Selecteer **Vereffend** in het veld **Status**.
    3. Filter op één grootboekrekening tegelijk.

        - U moet deze stappen herhalen voor elke grootboekrekening waarvoor grootboekvereffening plaatsvindt.
        - Als er geen andere grootboekrekeningen meer zijn ingesteld voor grootboekvereffening, moet u deze mogelijk tijdelijk weer toevoegen aan de instellingen voor grootboekvereffening. Voltooi vervolgens deze stappen als die grootboekrekeningen transacties hebben in 2023 die zijn vereffend met transacties in 2022 of eerder.

    4. Selecteer de kolom **Status** en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens om op deze kolom te groeperen.
    5. Selecteer de kolom **Bedrag in transactievaluta** en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens om het totaal te berekenen van deze kolom.

        - Als u alleen transacties hebt vereffend in 2022, is het totaal 0 (nul).
        - Als u transacties hebt die zijn vereffend in meerdere fiscale jaren, is het totaal niet 0 (nul).

    6. Identificeren welke transacties zijn vereffend tussen 2022 en 2023 door te filteren op de waarde **Vereffeningsdatum**. Als u filtert op een vereffeningsdatum van 1 januari 2023 tot en met 31 december 2023, krijgt u het totaal van 700 USD. Dit is het totaal van de transacties die in 2022 en 2023 zijn vereffend.

    ![Totaliseer 2022-grootboektransacties.](./media/afterYEC2.png)

4. Herhaal stap 3 voor fiscaal jaar 2023. Het totaal moet overeenkomen met 700 USD van 2022, omdat er geen transacties van 2023 zijn vereffend met transacties van 2024.

    ![Totaliseer 2023-grootboektransacties.](./media/afterYEC3.png)

5. Als u de functie **Bewustzijn** hebt ingeschakeld in stap 2, schakelt u deze uit voordat u verder gaat naar stap 6. In de volgende stappen keert u de grootboekvereffening om die fiscale jaren heeft doorlopen. Als de functie **Bewustzijn** is ingeschakeld, kan grootboekvereffening voor fiscaal jaar 2022 niet worden omgekeerd. Daarom moet u de functie uitschakelen voordat u verdergaat.
6. Nadat de functie **Bewustzijn** is uitgeschakeld, gebruikt u dezelfde filters op de pagina **Grootboekvereffening** om de grootboekvereffening van de gedetailleerde transacties om te keren.

    1. Terug naar de pagina **Grootboekvereffening** en filter op transactiedatums voor 2023. Zoek vervolgens de gedetailleerde transacties waar die samen het totaal van 700 USD vormen. Filteren voor deze informatie is mogelijk niet eenvoudig. U moet wellicht de gegevens verzenden naar Microsoft Excel om deze te beoordelen.
    2. Wanneer u de lijst met transacties hebt, selecteert u de grootboektransacties op de pagina **Grootboekvereffening** en selecteert u **Selectie markeren**. U hoeft niet beide zijden van de vereffende grootboektransacties te zien. Als u de debet- of de creditzijde markeert, worden alle gegevens met dezelfde **Vereffenings-id** omgekeerd, zelfs als de waarde **Gemarkeerd bedrag** niet **0** (nul) is.
    3. Selecteer **Gemarkeerde transacties omkeren** om de vereffening van de transacties ongedaan te maken.

    ![Boek transacties terug.](./media/afterYEC4.png)

7. Boek een corrigerend algemeen journaal om het openingssaldo voor 2023 op te splitsen in twee bedragen: het gedeelte dat is vereffend met de transactie van fiscaal jaar 2022 en het gedeelte dat nog niet is vereffend in 2023.

    - **Gedeelte van het openingssaldo dat is vereffend met het vorige jaar:** het eerste bedrag wordt 700 USD gebaseerd op de totalen die zijn gevonden en die zijn vereffend in 2022 en 2023.
    - **Gedeelte van het openingssaldo dat niet is vereffend met het vorige jaar:** het tweede bedrag is het verschil tussen het openingssaldo en het eerste bedrag van 525 USD. Het resterende bedrag is 1700 - 700 = 1000 USD.

    Op deze manier kunt u de transacties voor 2023 vereffenen met de $700 die oorspronkelijk was vereffend met de transactie van 2022. Deze stap is vereist omdat een grootboekvereffening geen gedeeltelijke vereffening toestaat.

    1. Ga naar het algemene journaal en boek de correctie. Uw organisatie moet op basis van de openstaande perioden in 2023 bepalen welke transactiedatum er moet worden gebruikt.
    2. Het kan zijn dat u de parameter **Handmatige invoer niet toestaan** op de pagina **Hoofdrekening** tijdelijk moet uitschakelen. Deze correctie wordt niet geboekt als handmatige invoer in de hoofdrekening niet is toegestaan.

    ![Correctie wordt niet geboekt.](./media/afterYEC5.png)

8. U kunt de niet-vereffende transacties nu opnieuw vereffenen. Ga terug naar de pagina **Grootboekvereffening** en beperk het datumbereik tot: 1 januari 2022 tot en met 31 december 2022. De volgende afbeelding geeft de nu bestaande, niet-vereffende transacties weer.

    ![Niet-vereffende transacties.](./media/afterYEC6.png)

    - Het openingssaldo van 1700 USD kan worden vereffend met de correctie voor -1700 USD.
    - De gedetailleerde transacties die niet zijn vereffend voor -700 USD kunnen worden vereffend met de correctie voor 700,00 USD.

9. Schakel de functie **Bewustzijn** weer in.
10. Nadat de functie **Bewustzijn** is ingeschakeld, kan grootboekvereffening voor meerdere fiscale jaren niet worden gedaan. Het kan zijn dat u het resterende saldo van 1000 USD verder moet opsplitsen in kleinere bedragen voordat u met nieuwe transacties kunt vereffenen in 2023. Sommige klanten kiezen ervoor om dat detail te boeken in stap 8, waarbij 1000 USD verder wordt opgesplitst om de niet-vereffende transacties uit 2022 weer te geven. Deze benadering geeft in wezen aan wat de functie **Bewustzijn** alleen voor het huidige jaar doet. Volgend jaar wordt dit automatisch uitgevoerd met de instelling **Details behouden** in de instellingen van de grootboekvereffening.

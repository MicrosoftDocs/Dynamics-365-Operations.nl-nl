---
title: Grootboekvereffeningen
description: In dit artikel wordt uitgelegd hoe u de grootboekvereffeningspagina gebruikt om grootboektransacties te vereffenen en vereffeningen om te keren.
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800626"
---
# <a name="ledger-settlements"></a>Grootboekvereffeningen

[!include [banner](../includes/banner.md)]

Grootboekvereffening is het proces waarin debet- en credittransacties in het grootboek worden afgestemd. De vereffening van de debet- en creditbedragen wordt gebruikt om het saldo van de grootboekrekening te vereffenen met de gedetailleerde transacties waaruit het saldo bestaat.

Vereffende transacties kunnen worden uitgesloten van onderzoeken en rapporten. Op deze manier is het eenvoudiger om de openstaande grootboektransacties te analyseren waaruit het saldo van de grootboekrekening bestaat.

> [!IMPORTANT] 
> De modules Klanten en Leveranciers werken ook met vereffening van facturen en betalingen. Wanneer vereffening plaatsvindt in de subjournalen van Klanten en Leveranciers, worden de bijbehorende grootboekposten niet automatisch vereffend.

## <a name="ledger-settlement-features"></a>Functies voor grootboekvereffening
In Microsoft Dynamics 365 Finance versie 10.0.21 is de optie **Geavanceerde grootboekvereffening inschakelen** verwijderd van de pagina **Grootboekparameters**. Geavanceerde grootboekvereffening is nu altijd ingeschakeld.
In Finance versie 10.0.25 is de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting van het grootboek** geïntroduceerd. Met deze functie wordt de basisfunctionaliteit in zowel grootboekvereffening als jaarafsluiting van het grootboek gewijzigd. Voordat u deze functie inschakelt in de werkruimte **Functiebeheer**, raadpleegt u [Bewustzijn tussen grootboekvereffening en jaarafsluiting van het grootboek](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Grootboekvereffening instellen
U moet de hoofdrekeningen selecteren waarvoor u grootboekvereffening wilt uitvoeren. U kunt deze hoofdrekeningen op twee manieren selecteren.

1. Ga naar **Grootboek** > **Grootboek instellen** > **Grootboekparameters**.
2. Selecteer op het tabblad **Grootboekvereffeningen** het rekeningschema waaruit u de hoofdrekeningen wilt selecteren.
3. Selecteer de hoofdrekeningen waarvoor u grootboekvereffening wilt uitvoeren. Omdat rekeningschema´s globaal zijn, hebben alle bedrijven waaraan het geselecteerde rekeningschema is toegewezen, dezelfde hoofdrekeningen voor grootboekvereffening geselecteerd.

  – of –

1. Ga naar **Grootboek** > **Periodieke taken** > **Grootboekvereffeningen**.
2. Selecteer **Rekeningen voor grootboekvereffeningen**.
3. Selecteer in het dialoogvenster de rekeningschema´s en hoofdrekeningen waarvoor u grootboekvereffening wilt uitvoeren. Dit dialoogvenster is een snelkoppeling. Alle hoofdrekeningen die u hier toevoegt, worden ook weergegeven op de pagina **Grootboekparameters**.

U kunt op elk gewenst moment dezelfde basisprocedures gebruiken om hoofdrekeningen te verwijderen uit grootboekvereffening. Het verwijderen van een hoofdrekening heeft geen effect op eerdere grootboekvereffeningen. De hoofdrekening en transacties worden echter niet meer weergegeven op de pagina **Grootboekvereffening**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Transacties vereffenen
Als u grootboektransacties wilt vereffenen, voert u de volgende stappen uit.

1. Ga naar **Grootboek** > **Periodieke taken** > **Grootboekvereffeningen**.
2. Stel de filters bovenaan de pagina in:

    - Selecteer een datumbereik. U kunt ook een datumintervalcode selecteren om automatisch in het datumbereik in te vullen. Het is niet aan te raden grootboekvereffening uit te voeren voor transacties die meerdere fiscale jaren beslaan.
    - Wijzig zo nodig de boekingslaag. U kunt geen transacties vereffenen in verschillende boekingslagen.
    - Als u de hoofdrekening en dimensies afzonderlijk wilt weergeven, selecteert u een financiële dimensieset.

3. Selecteer **Transacties weergegeven** om alle transacties weer te geven die overeenkomen met de filters die u hebt ingesteld, en de lijst met rekeningen die u hebt opgegeven toen u het rekeningschema instelde in de vorige sectie.

    - Als u een van de filters of de dimensiesets wijzigt, moet u **Transacties weergegeven** opnieuw selecteren.
    - Als u de transacties wilt filteren op een afzonderlijke hoofdrekening, gebruikt u het filter in het veld **Grootboekrekening**. Het is niet aan te raden grootboekvereffening uit te voeren voor transacties die naar verschillende hoofdrekeningen worden geboekt.

4. Selecteer regels voor vereffening. De waarde in het veld **Geselecteerd bedrag** bovenaan de pagina wordt verhoogd of verlaagd om het totale bedrag op de geselecteerde regels weer te geven.
5. Als u klaar bent met het selecteren van transacties, selecteert u **Selectie markeren**. Er wordt een vinkje weergegeven in de kolom **Gemarkeerd** voor elke geselecteerde transactie. De waarde in het veld **Gemarkeerd bedrag** bovenaan het raster wordt bovendien verhoogd of verlaagd om het totale bedrag op de gemarkeerde regels weer te geven.
6. Als de waarde in het veld **Gemarkeerd bedrag** **0** (nul) is, selecteert u **Gemarkeerde transacties vereffenen**. De status van de gemarkeerde transacties wordt bijgewerkt in **Vereffend**.

    > [!IMPORTANT]
    > Alle transacties die u hebt gemarkeerd voor vereffening voor de actieve rechtspersoon worden vereffend, zelfs als deze momenteel niet worden weergegeven op de pagina Grootboekvereffening omdat u een filter hebt toegepast.

## <a name="make-transactions-easier-to-find"></a>Transacties eenvoudiger te vinden maken
De pagina **Grootboekvereffeningen** bevat mogelijkheden waardoor het gemakkelijker wordt om de transacties weer te geven die u nodig hebt voor vereffening.

- Met het filter **Gemarkeerd** kunt u transacties filteren op basis van de vraag of het selectievakje **Gemarkeerd** ervoor is ingeschakeld.
- Met het filter **Status** kunt u transacties filteren op basis van de status ervan.
- Selecteer **Sorteren op absoluut bedrag** om de bedragen op absolute waarde te sorteren. Op deze manier kunt u debet- en creditbedragen met hetzelfde bedrag groeperen.

## <a name="reverse-a-settlement"></a>Een vereffening omkeren
U kunt een vereffening omkeren die ten onrechte is aangebracht.

1. Voer stap 1 tot en met 3 uit in het gedeelte [Transacties vereffenen](#settle-transactions) om de transacties weer te geven waarin u geïnteresseerd bent.
2. Selecteer in het filter **Status** **Vereffend**.
3. Selecteer regels voor terugboeking.
4. Selecteer **Gemarkeerde transacties omkeren**. De status van alle transacties met dezelfde vereffenings-id wordt gewijzigd in **Niet vereffend**.

    > [!IMPORTANT]
    > Alle transacties met dezelfde vereffenings-id worden omgekeerd, zelfs als ze niet zijn gemarkeerd. Er zijn bijvoorbeeld vier regels gemarkeerd en vereffend. Alle vier de regels hebben dezelfde vereffenings-id. Als u een van deze vier regels markeert en vervolgens **Gemarkeerde transacties omkeren** selecteert, worden alle vier de regels omgekeerd.

## <a name="unmark-for-selected-users"></a>Markering opheffen voor geselecteerde gebruikers
Schakel **Markering opheffen voor geselecteerde gebruikers** in om de markering van grootboekvereffende transacties voor alle rechtspersonen op gebruikers-id op te heffen. Hierdoor kan bijvoorbeeld een accounting manager de markering van transacties ongedaan maken voor een gebruiker die op vakantie is geweest voordat de vereffening is voltooid of voor een gebruiker die de organisatie heeft verlaten. De actie staat het markeringen van deze transacties toe voor vereffening door een andere gebruiker.


## <a name="unmark-all-transactions"></a>De markering van alle transacties ongedaan maken
Selecteer **De markering van alle transacties ongedaan maken** om de markering van alle grootboekvereffende transacties voor alle gebruikers en alle rechtspersonen op te heffen. Deze actie is beschikbaar voor de beheerdersrol.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

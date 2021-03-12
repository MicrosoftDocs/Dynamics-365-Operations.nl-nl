---
title: Leveranciersbetalingsvoorstellen automatiseren
description: In dit onderwerp wordt uitgelegd hoe organisaties die leveranciers periodiek betalen het proces van het genereren van betalingsvoorstellen voor leveranciers kunnen automatiseren.
author: kweekley
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 63f2d3dc55799efefaedb10134edb219fa8588e0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003573"
---
# <a name="automate-vendor-payment-proposals"></a>Leveranciersbetalingsvoorstellen automatiseren

[!include [banner](../includes/banner.md)]

Organisaties die leveranciers periodiek betalen, kunnen nu het proces van het genereren van betalingsvoorstellen voor leveranciers automatiseren. Door automatisering van betalingsvoorstellen voor leveranciers worden de volgende details gedefinieerd:

- Wanneer betalingsvoorstellen worden uitgevoerd
- Welke criteria worden gebruikt om de facturen te selecteren die moeten worden betaald
- In welk leveranciersbetalingsjournaal de resulterende betalingen worden opgeslagen

Bij de automatische betalingsvoorstellen worden de betalingen niet automatisch geboekt. Daarom kunt u alle validatie- en werkstroomprocessen gebruiken die u momenteel gebruikt om de gemaakte betalingen goed te keuren.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Het exemplaar van de betalingsvoorstellen voor leveranciers definiëren

Voor de automatisering van betalingsvoorstellen voor leveranciers wordt het raamwerk voor procesautomatisering gebruikt. Verschillende bedrijfsprocessen gebruiken dit raamwerk om het terugkeerpatroon van een geselecteerd proces te definiëren. Voor betalingsvoorstellen voor leveranciers is de automatisering toegankelijk via **Leveranciers \> Betalingsinstelling \> Procesautomatisering**.

Gebruik eerst de automatiseringsoptie **Nieuw proces maken** en selecteer **Betalingsvoorstel van leverancier**. Een wizard begeleidt u vervolgens bij het instellen van het betalingsvoorstel voor de leverancier.

## <a name="general-page"></a>Pagina Algemeen

Voer op de pagina **Algemeen** van de wizard de naam in van het betalingsvoorstel voor de leverancier dat u maakt. Als u bijvoorbeeld alle binnenlandse leveranciers per cheque betaalt op maandag, voert u een beschrijvende naam in, zoals **Binnenlands\_Cheque**. De naam die u invoert, wordt weergegeven in de weekweergave van de procesautomatisering in het werkgebied **Leveranciersbetalingen**.

Definieer vervolgens de eigenaar van het betalingsjournaal dat wordt gemaakt. De eigenaar is meestal de betalingsmedewerker voor leveranciers die verantwoordelijk is voor het betalingsjournaal nadat dit is gemaakt.

De overige instellingen op de pagina zijn algemeen en worden gebruikt om het periodieke patroon te definiëren voor deze versie van het betalingsvoorstel van de leverancier. Als de chequebetalingen steeds op maandag plaatsvinden, kunt u definiëren dat dit wekelijks wordt uitgevoerd en kunt u maandag als de dag van de week selecteren waarop dit wordt uitgevoerd. U kunt ook een vroege planningstijd invoeren, zoals 2:00 u, zodat de procesautomatisering vóór het begin van de volgende werkdag wordt voltooid.

Het is belangrijk dat u weet dat u de wizard gebruikt om te definiëren wanneer het betalingsvoorstel van de leverancier wordt verwerkt. U definieert niet wanneer de leveranciersbetalingen worden gegenereerd, afgedrukt en geboekt. In de weekweergave wordt de procesautomatisering voor betalingsvoorstellen voor leveranciers weergegeven op de dagen die zijn geselecteerd in het herhalingspatroon.

Zie de documentatie over procesautomatisering voor meer informatie over de andere velden op de pagina **Algemeen**.

## <a name="vendor-payment-proposal-page"></a>Pagina Betalingsvoorstel voor leverancier

De volgende pagina in de wizard is de pagina **Betalingsvoorstel voor leverancier**. Deze wordt gebruikt om de criteria te definiëren voor het selecteren van de te betalen leveranciersfacturen. In het algemeen zijn dezelfde opties beschikbaar in het betalingsvoorstel in het journaal met leveranciersbetalingen. Er zijn echter enkele uitzonderingen. Alle datums op deze pagina moeten bijvoorbeeld worden gedefinieerd als relatieve datums, omdat de datum van het betalingsvoorstel telkens wordt gewijzigd wanneer het voorstel wordt uitgevoerd.

### <a name="journal-name"></a>Journaalnaam

Het veld **Journaalnaam** geeft de journaalnaam aan waarin de leveranciersbetalingen worden gemaakt. De automatisering van het betalingsvoorstel voor leveranciers resulteren in betalingen in het gedefinieerde journaal, maar het journaal wordt niet geboekt.

### <a name="from-date-and-to-date"></a>Vanaf datum/Tot datum

In plaats van een 'vanaf'-datum en een 'tot'-datum te definiëren om facturen te selecteren op basis van de vervaldatum of de contantkortingsdatum, moet u de optie **Criteria voor 'tot'-datum definiëren** gebruiken en het veld **Aantal dagen corrigeren voor tot-datum** om de tot-datum aan te geven. Er is geen concept 'van'-datum in de automatisering van het betalingsvoorstel.

De optie **Criteria voor 'tot'-datum definiëren** is standaard ingesteld op **Nee**. Als u deze standaardwaarde gebruikt, worden bij het uitvoeren van het proces alle facturen voor de betaling geselecteerd, omdat er geen 'tot'-datum is gedefinieerd.

Als u de optie **Criteria voor 'tot'-datum definiëren** instelt op **Ja**, gebruikt u het veld **Aantal dagen corrigeren voor tot-datum** om de datum te definiëren waarop facturen worden geselecteerd als het opgegeven aantal dagen voor of na de datum waarop het proces wordt uitgevoerd. Het getal kan positief, negatief of 0 (nul) zijn. Facturen waarvan de vervaldatum of de contantkortingsdatum zijn opgegeven, worden vervolgens betaald met het opgegeven aantal dagen voor of na de datum waarop het proces wordt uitgevoerd. Voor bijvoorbeeld alle facturen die op of vóór vrijdag moeten worden betaald, worden in de betalingsreeks betalingen aan alle leveranciers per cheque op woensdag gemaakt. In dit geval stelt u het **Aantal dagen corrigeren voor tot-datum** in op **2**. Wanneer het betalingsvoorstel op woensdag 25 maart wordt uitgevoerd, worden alle facturen met een vervaldatum of een contantkortingsdatum op of voor 27 maart geselecteerd voor betaling.

### <a name="minimum-payment-date"></a>Datum minimumbetaling

De minimumbetaaldatum is de eerste datum die wordt gebruikt bij het maken van betalingen. U moet eerst de optie **Criteria voor minimumbetaaldatum definiëren** instellen op **Ja**. Met deze instelling kunt u de functie voor de minimumbetaaldatum gebruiken. Als u deze optie instelt op **Ja**, gebruikt u het veld **Aantal dagen corrigeren voor minimumbetaaldatum** om de minimumbetaaldatum te definiëren als het opgegeven aantal dagen voor of na de datum waarop het proces wordt uitgevoerd. Het getal kan positief, negatief of 0 (nul) zijn. De betalingsreeks genereert bijvoorbeeld betalingen op woensdag om alle betalingen op te nemen met een minimumbetaaldatum van de afgelopen maandag. In dit geval stelt u het **Aantal dagen corrigeren voor minimumbetaaldatum** in op **-2**.

In het volgende voorbeeld ziet u hoe de velden voor de 'tot'-datum en met de minimumbetaaldatum samenwerken. De automatisering van het betalingsvoorstel wordt ingesteld om op woensdag te worden uitgevoerd. Het veld **Aantal dagen corrigeren voor 'tot'-datum** wordt ingesteld op **1** om de 'tot'-datum te definiëren op basis van de vervaldatum. In dit geval wordt het **Aantal dagen corrigeren voor minimumbetaaldatum** ingesteld op **-2**. Als de automatisering van het betalingsproces begint op woensdag 25 maart, worden alle facturen die op of vóór 26 maart moeten worden betaald, opgenomen in het betalingsvoorstel. Betalingsvoorstellen worden op de volgende manier gegenereerd:

- Voor alle facturen die op of voor 23 maart moeten worden betaald, wordt de betalingsdatum 23 maart gebruikt.
- Voor facturen die op 24 maart moeten worden betaald, wordt de betalingsdatum 24 maart gebruikt.
- Voor facturen die op 25 maart moeten worden betaald, wordt de betalingsdatum 25 maart gebruikt.
- Voor facturen die op 26 maart moeten worden betaald, wordt de betalingsdatum 26 maart gebruikt.

### <a name="summarized-payment-date"></a>Samengevatte betalingsdatum

De samengevatte betalingsdatum wordt alleen gebruikt als het veld **Periode** voor de betalingsmethode is ingesteld op **Totaal**. Als het veld **Periode** is ingesteld op **Totaal** voor uw betalingsmethoden, moet u de optie **Criteria voor samengevatte betalingsdatum definiëren** instellen op **Ja**. Als u deze optie instelt op **Ja**, gebruikt u het veld **Aantal dagen corrigeren voor samengevatte betaaldatum** om de samengevatte betaaldatum te definiëren als het opgegeven aantal dagen voor of na de datum waarop het proces wordt uitgevoerd. Het getal kan positief, negatief of 0 (nul) zijn. De reeks genereert bijvoorbeeld betalingen op woensdag en het bedrijf wil een samengevatte betaling op woensdag maken. In dit geval stelt u het **Aantal dagen corrigeren voor samengevatte betaaldatum** in op **0**.

### <a name="records-to-include"></a>Op te nemen records

De filteropties kunnen nog steeds worden gedefinieerd voor het betalingsvoorstel. Als er een filter wordt gedefinieerd, worden de filtercriteria niet op de pagina van de wizard weergegeven. Ze kunnen echter wel worden weergegeven door het filter opnieuw te openen.

De resterende velden voor het voorstel werken net zoals ze werken voor het betalingsvoorstel in het betalingsjournaal voor leveranciers. Zie [Leveranciersbetalingen maken met behulp van een betalingsvoorstel](create-vendor-payments-payment-proposal.md) voor informatie over de andere velden.

> [!NOTE]
> Sommige land-/regiospecifieke velden en enkele openbare sectorvelden zijn nog niet beschikbaar in de automatisering van leveranciersbetalingsvoorstellen.

We raden u aan om te beoordelen of de automatisering voor uw organisatie nuttig is, op basis van uw behoeften.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>De resultaten van de automatisering van betalingsvoorstellen voor leveranciers weergeven

Nadat de automatsering voor het leveranciersbetalingsvoorstel is gemaakt, worden de herhalingen voor elke betaling weergegeven in de weekweergave van de procesautomatisering. Voor leveranciersbetalingen is de weekweergave voor procesautomatisering toegevoegd aan het werkgebied **Leveranciersbetalingen** en de pagina **Procesautomatisering**.

[![De weekweergave van procesautomatisering in het werkgebied Leveranciersbetalingen](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

De weekweergave van de procesautomatisering in het werkgebied **Leveranciersbetalingen** laat alleen automatiseringen van leveranciersbetalingsvoorstellen zien. Het geeft alle exemplaren van betalingen voor de huidige week weer, voor alle rechtspersonen waarvoor de aangemelde gebruiker beveiligingsmachtigingen heeft. Als de betalingsmedewerker bijvoorbeeld verantwoordelijk is voor betalingen in de bedrijven USMF en USSI, ziet hij de exemplaren voor de automatisering van de leveranciersbetalingsvoorstellen voor die twee bedrijven, maar niet voor andere bedrijven.

[![De weekweergave van procesautomatisering voor de bedrijven USMF en USSI](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Elk exemplaar geeft het bedrijf weer waarin het betalingsjournaal is of wordt gemaakt. Als betalingen worden gemaakt met behulp van gecentraliseerde betalingen, is het bedrijf dat wordt weergegeven het bedrijf waarin betalingen worden gemaakt. Het wordt niet noodzakelijkerwijs getoond welke facturen van de bedrijven worden betaald.

De naam van elk exemplaar wordt ook weergegeven om het betalingsvoorstel te identificeren.

Bovendien wordt de status van elk exemplaar weergegeven. De volgende statussen worden gebruikt:

- **Gepland**: het betalingsvoorstel is gepland, maar nog niet uitgevoerd.
- **Fout** : het betalingsvoorstel is uitgevoerd, maar er is een fout opgetreden. U kunt de fouten weergeven door de knop **Resultaten weergeven** te selecteren.
- **Voltooid**: het betalingsvoorstel is uitgevoerd. U kunt de betalingen weergeven door de koppeling **Betalingen weergeven** te selecteren. Met deze koppeling wordt het betalingsjournaal geopend dat door het exemplaar is gemaakt.

Nadat de betalingen zijn gemaakt, kunt u de betalingsbedragen weergeven in het journaal. De bedragen worden weergegeven in de transactievaluta. Als het betalingsjournaal bijvoorbeeld betalingen bevat in Amerikaanse dollars en Canadese dollars, worden de totale betalingen voor elke valuta weergegeven. 

Het betalingsjournaal kan worden verwijderd nadat het is gemaakt via procesautomatisering. Als een betaling volledig is verwijderd, vinden de volgende gebeurtenissen plaats:

- De status van de procesautomatisering voor de week blijft **Voltooid**.
- Het proces verwijdert de betalingstotalen en de koppeling **Betalingen weergeven** wordt vervangen door een knop **Resultaten weergeven**.
- Wanneer u de resultaten bekijkt, ontvangt u een bericht met de mededeling dat het oorspronkelijke journaal is verwijderd.

Nadat een betaling is verwijderd, worden de facturen opnieuw geopend voor betaling. U kunt vervolgens een nieuw exemplaar maken om de facturen opnieuw te betalen.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Automatisering van leveranciersbetalingsvoorstellen bewerken

Met het raamwerk voor procesautomatisering kunt u de betaling, de reeks en de exemplaren bewerken die voor het betalingsvoorstel worden gemaakt. De reeks kan worden bewerkt via de pagina **Procesautomatisering** of via de weekweergave van de procesautomatisering. Als de manager voor Leveranciers bijvoorbeeld alle cheques voor binnenlandse leveranciers op woensdag in plaats van op maandag wil genereren, kan hij een exemplaar selecteren in de weekweergave en vervolgens **Weergeven/bewerken – reeks**. Als u een reeks bewerkt, wordt u gevraagd om op te geven of de wijziging in alle bestaande exemplaren moet worden aangebracht of alleen in nieuwe exemplaren. Historische exemplaren die al de status **Voltooid** hebben of die met een **foutstatus** zijn beëindigd, worden niet gewijzigd.

U kunt ook een nieuw exemplaar toevoegen of een bestaand exemplaar wijzigen. Het volgende exemplaar van het betalingsvoorstel is bijvoorbeeld gepland voor uitvoering op woensdag 1 januari, maar deze datum is een feestdag. U kunt het exemplaar wijzigen via de weekweergave van de procesautomatisering of via de pagina **Procesautomatisering**. Er wordt een pagina geopend waarin de planningsdetails en de criteria voor het betalingsvoorstel worden weergegeven. Hier kunt u de geplande tijd en datum bewerken. U kunt ook de criteria voor het betalingsvoorstel bewerken als er wijzigingen zijn vereist. Als u bijvoorbeeld de geplande datum van het betalingsexemplaar wijzigt van 1 januari in 2 januari, wilt u mogelijk ook de relatieve datums wijzigen voor de 'tot'-datum.

U kunt ook een exemplaar of een reeks uitschakelen. Als u een exemplaar wilt uitschakelen en de verwerking wilt uitstellen, selecteert u dit in de weekweergave voor procesautomatisering en selecteert u **Uitschakelen**. U kunt een reeks uitschakelen op de pagina **Procesautomatisering**.

## <a name="security-for-payment-proposal-automations"></a>Beveiliging voor automatisering van betalingsvoorstellen

De volgende functies en bevoegdheden zijn toegevoegd voor de automatisering van voorstellen voor leveranciersbetalingen. Deze functies en bevoegdheden zijn de standaard beveiligingsinstellingen, maar ze kunnen worden gewijzigd op basis van de vereisten van uw organisatie. Als bijvoorbeeld niet alleen de manager voor Leveranciers, maar ook de betalingsmedewerker het terugkeerpatroon van een schema kan bewerken en maken, wijst u de functie **Planningsexemplaren onderhouden** toe aan de persoon in de rol Betalingsmedewerker Leveranciers.

| Functie                              | Rol                                                                       | Bevoegdheden |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Planningsreeksen onderhouden          | Leveranciersmanager                                                   | Deze functie verleent de rechten om de automatiseringsreeks voor betalingsvoorstellen en exemplaren te maken en te onderhouden via de volgende bevoegdheden:<ul><li>Planningsexemplaren onderhouden</li><li>Planningsreeksen onderhouden</li><li>ProcessScheduleOccurrenceListMaintain</li><li>De weekweergave met exemplaren bekijken</li></ul> |
| Informatie opvragen over geplande exemplaren | Betalingsmedewerker leveranciers, centrale betalingsmedewerker leveranciers | Deze functie verleent de rechten om de automatiseringsreeks voor betalingsvoorstellen en exemplaren weer te geven via de volgende bevoegdheden:<ul><li>Planningsexemplaren weergeven</li><li>De weekweergave met exemplaren bekijken</li></ul> |
| Informatie opvragen over planningsreeks      | None                                                                       | Deze functie verleent de rechten om de instellingen voor de reeks en exemplaren weer te geven via de volgende bevoegdheden:<ul><li>Planningsexemplaren weergeven</li><li>De lijstpagina met exemplaren weergeven</li><li>De weekweergave met exemplaren bekijken</li></ul>|
| Planningsexemplaren onderhouden     | None                                                                       | Deze functie geeft de rechten voor het maken en onderhouden van een exemplaar via de volgende bevoegdheden:<ul><li>Planningsexemplaren onderhouden</li><li>De weekweergave met exemplaren bekijken</li></ul> |

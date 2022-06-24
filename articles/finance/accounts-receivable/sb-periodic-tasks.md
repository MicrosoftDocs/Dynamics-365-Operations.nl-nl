---
title: Periodieke taken in Terugkerende contractfacturering
description: In dit artikel worden de periodieke taken beschreven die beschikbaar zijn in Terugkerende contractfacturering.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904783"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Periodieke taken in Terugkerende contractfacturering

In dit artikel worden de periodieke taken beschreven die beschikbaar zijn in Terugkerende contractfacturering.

## <a name="generate-invoice"></a>Factuur genereren

Gebruik de pagina **Factuur genereren** om maandelijks terugkerende facturen massaal te maken op basis van de gegevens die u hebt ingesteld op de pagina's **Alle factureringsschema's** en **Factureringsdetails weergeven**. Wanneer een factuur wordt gemaakt, wordt de artikelomschrijving voor de verkooporderverwerkingsregel bijgewerkt met de artikelomschrijving en de begin- en einddatums van de facturering voor de planningsregel die wordt gefactureerd.

## <a name="generate-invoice-batch-processing"></a>Batchverwerking voor facturen genereren

Met de pagina **Batchverwerking voor facturen genereren** kunt u terugkerende facturen maken door middel van een terugkerend batchproces. De beschikbare parameters zijn gelijk aan de parameters op de pagina **Factuur genereren**, maar ze kunnen worden opgeslagen in een batchproces dat meerdere keren kan worden uitgevoerd.

## <a name="price-update"></a>Prijs bijwerken

Met het hulpprogramma Prijs bijwerken kunt u de prijzen van verschillende artikelen bijwerken op meerdere factureringsschema's in één actie. De prijzen kunnen worden bijgewerkt op basis van een opgegeven percentage of een opgegeven bedrag. In de lijst met regels worden alleen de huidige eenheidsprijzen van de artikelen weergegeven. De prijzen na het bijwerken van de prijs worden niet weergegeven.

Houd rekening met de volgende punten over het hulpprogramma Prijs bijwerken:

- Als de verkooporder voor een bepaald jaar al is gemaakt (dat wil zeggen dat de artikelen zijn gefactureerd), heeft dit geen invloed op de prijs van de regelartikelen.
- Het hulpprogramma Prijs bijwerken kan worden gebruikt voor regelartikelen met de status **Actief** of **In wachtstand**. Voor artikelen die in de wacht staan, moet de optie **Schema aanpassen** zijn ingesteld op **Nee** op het moment dat de artikelen in de wacht werden geplaatst.
- Het hulpprogramma Prijs bijwerken kan niet worden gebruikt voor regelartikelen die gebruiksartikelen zijn die gebruikmaken van escalatie, facturering van mijlpalen of opbrengstsplitsing.

### <a name="price-update-example"></a>Voorbeeld van prijsbijwerking

Er wordt een factureringsschema gemaakt en er wordt een vernieuwingsartikel toegevoegd. De prijs per eenheid is € 750. Het eerste jaar van het artikel wordt betaald op 15 december 2021. Het factureringsschema wordt gemaakt voor de periode van 1 januari tot en met 31 december 2022.

Tijdens de verlenging wordt de verkooporder met het proces **Factuur genereren** voor het jaar 2022 gemaakt. Nadat het hulpprogramma Prijs bijwerken is uitgevoerd, wordt de prijs gewijzigd van € 750 in € 800.

De verkooporder en het factureringsschema voor 2022 worden niet beïnvloed en de eenheidsprijs blijft € 750, omdat het factureringsschema voor 2022 al is gefactureerd. De factureringsschemaregel en regeldetails voor 2023 worden gewijzigd in € 800, omdat het factureringsschema voor 2023 nog niet is gefactureerd.

### <a name="update-prices--flat-pricing-method"></a>Prijzen bijwerken - methode Vaste prijs

Wanneer u prijzen bijwerkt voor artikelen die de methode Vaste prijs gebruiken, kunt u een percentage of bedrag opgeven om de prijs te verhogen.

Voer de volgende stappen uit om het hulpprogramma Prijs bijwerken uit te voeren voor artikelen die de methode Vaste prijs gebruiken.

1. Selecteer op de pagina **Prijs bijwerken** de prijsmethode **Vast**.
2. Selecteer in het veld **Verhogingsmethode** de verhogingsmethode die wordt gebruikt om de prijs van de artikelen bij te werken.
3. Afhankelijk van de verhogingsmethode die u hebt geselecteerd, geeft u het percentage op in het veld **Percentage** of het bedrag in het veld **Bedrag**.
4. Gebruik op het sneltabblad **Op te nemen records** de knop **Filter** om gegevensfilters toe te voegen.
5. Selecteer **Voorbeeld weergeven** om het bereik records weer te geven.
6. Als u bepaalde regels niet wilt verwerken, markeert u deze en selecteert u vervolgens **Verwijderen**.
7. Selecteer **OK**.

### <a name="update-prices--standard-pricing-method"></a>Prijzen bijwerken - standaardprijsmethode

Als de prijs van een artikel is gewijzigd in de artikelrecord, kan deze worden bijgewerkt voor alle factureringsschemaregels als voor het artikel de standaardprijsmethode wordt gebruikt.

1. Selecteer op de pagina **Prijs bijwerken** de prijsmethode **Standaard**.
2. Gebruik op het sneltabblad **Op te nemen records** de knop **Filter** om gegevensfilters toe te voegen.
3. Selecteer **Voorbeeld weergeven** om het bereik records weer te geven.
4. Als u bepaalde regels niet wilt verwerken, markeert u deze en selecteert u vervolgens **Verwijderen**.
5. Selecteer **OK**.

## <a name="mass-hold-processing"></a>Massaal blokkeren verwerken

Als u blokkeringsopties wilt toepassen op verschillende factureringsschema´s tegelijk, gebruikt u de pagina **Massaal blokkeren**.

Als u slechts één factureringsschema of één factureringsschemaregel in de wacht wilt zetten, opent u de pagina **Alle factureringsschema's** en selecteert u **Blokkering plaatsen**. Als u een blokkering wilt verwijderen, gebruikt u de pagina **Blokkering verwijderen**.

### <a name="put-billing-schedules-on-hold"></a>Factureringsschema´s in de wachtstand plaatsen

Voer de volgende stappen uit om verschillende factureringsschema´s in de wachtstand te plaatsen.

1. Stel op de pagina **Massaal blokkeren** het veld **Procesoptie** in op **Blokkering toepassen**.
2. Selecteer in het veld **Redencode** een redencode.
3. Stel de optie **Schema aanpassen** in:

    - **Ja**: als u de optie op **Ja** instelt, geeft u een blokkeringsdatum op in het veld **Blokkeringsdatum**. Alle factureringsschemaregels na de blokkeringsdatum worden verwijderd.
    - **Nee**: de factureringsschemaregels worden niet gewijzigd. Alleen de status wordt gewijzigd. De status wordt gewijzigd in **In wachtstand**.

4. Gebruik op het sneltabblad **Op te nemen records** de knop **Filter** om gegevensfilters toe te voegen.
5. Selecteer **Voorbeeld weergeven** om het bereik records weer te geven.
6. Als u bepaalde regels niet wilt verwerken, markeert u deze en selecteert u vervolgens **Verwijderen**.
7. Selecteer **OK**.

Wanneer u terugkeert naar de lijst met factureringsschema's, ziet u dat de status van de factureringsschema's is gewijzigd in **In wachtstand**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Een blokkering verwijderen uit verschillende factureringsschema's

1. Stel op de pagina **Massaal blokkeren** het veld **Procesoptie** in op **Blokkering verwijderen**.
2. Voer in het veld **Redencode** een redencode in.
3. Selecteer in het veld **Datum verwijderen** de datum waarop de blokkering moet worden verwijderd.
4. Stel desgewenst de velden **Hervattingsdatum** en **Uitsteldatum** in. De uitsteldatum wordt toegevoegd aan alle regels die uitstelbaar zijn.
5. Gebruik op het sneltabblad **Op te nemen records** de knop **Filter** om gegevensfilters toe te voegen.
6. Selecteer **Voorbeeld weergeven** om het bereik records weer te geven.
7. Als u bepaalde regels niet wilt verwerken, markeert u deze en selecteert u vervolgens **Verwijderen**.
8. Selecteer **OK**.

> [!NOTE]
> Als u een blokkering wilt verwijderen, moet u de waarde **Verwijderen van blokkering voor gebruikersgroep overschrijven** op de **Terugkerende contractfactureringsparameters** instellen.

Een factureringsregel heeft bijvoorbeeld de begindatum 1 februari 2022 en de einddatum 28 februari 2022. Het factureringsbedrag is € 200. Het veld **Blokkeringsdatum** is ingesteld op 10 februari 2022. Daarom wordt de februariperiode gecorrigeerd om elke datum na 10 februari uit te sluiten. De nieuwe periode is van 1 februari tot en met 9 februari en het bedrag wordt € 64,29 (via dagelijkse verdeling naar rato). Alle factureringsschemaregels op of na 10 februari worden verwijderd.

Als het proces **Blokkering verwijderen** is voltooid en het veld **Datum verwijderen** is ingesteld op 10 februari 2022, zijn er twee factureringsperioden. De eerste factureringsperiode is van 1 februari tot en met 9 februari en het bedrag is € 64,29. De tweede factureringsperiode is van 10 februari tot en met 28 februari en het bedrag is € 135,71.

## <a name="mass-termination-processing"></a>Massaal beëindigen verwerken

Gebruik de pagina **Massaal beëindigen** om factureringsschemaregels te beëindigen die momenteel worden weergegeven door een datum voor beëindiging op te geven.

Als u uitstel van opbrengsten en onkosten gebruikt, komen factureringsschema's waarvan het veld **Beëindigingsdatum** is ingesteld op **Schema aanpassen** op de pagina **Alle factureringsschema's** in aanmerking voor restitutie.

Factureringsschema's die gebruikmaken van de functionaliteit voor het toewijzen van meerdere elementen (MEA) worden niet weergegeven op de pagina **Massaal beëindigen**. U kunt een afzonderlijk factureringsschema toch beëindigen door gebruik te maken van de functionaliteit voor beëindiging in het factureringsschema.

> [!NOTE]
> Factureringsschemaregels die momenteel zijn opgenomen in een **Factuur genereren**-batch, zijn niet beschikbaar voor dit proces.

Zie [Factureringsschema's beëindigen](terminate-billing-schedule.md) voor informatie over elk veld en het proces.

## <a name="mass-archive-process"></a>Proces voor massaal archiveren

U kunt op de pagina **Massaal archiveren** meerdere factureringsschema's archiveren. Alleen beëindigde factureringsschema's kunnen worden gearchiveerd.

Nadat een factureringsschema is gearchiveerd, treden de volgende gebeurtenissen op:

- De status is gewijzigd in **Gearchiveerd**.
- De factureringsschema's zijn permanent vergrendeld.
- De factureringsschemaregels zijn niet langer beschikbaar op querypagina's.

> [!NOTE]
> Het archiveren van een factureringsschema is een permanente actie en kan niet worden teruggedraaid.

Voer de volgende stappen uit om factureringsschema´s te archiveren.

1. Geef op de pagina **Massaal archiveren** in het veld **Einddatum facturering** een einddatum voor facturering op. Als u alle beëindigde factureringsschema's wilt weergeven, laat u dit veld leeg.
2. Gebruik op het sneltabblad **Op te nemen records** de knop **Filter** om de records die worden weergegeven te beperken.
3. Selecteer **Voorbeeld weergeven**.
4. Als u sommige records niet wilt archiveren, markeert u deze en selecteert u vervolgens **Verwijderen**.
5. Selecteer **OK** om de records op de pagina te archiveren.

## <a name="mass-stubbing-process"></a>Proces voor massale stubverwerking

U kunt op de pagina **Massale stubverwerking** alle geselecteerde factureringsschemaregels als gefactureerd (stub) of niet-gefactureerd (stub omkeren) markeren. Stubverwerking of omgekeerde stubverwerking wordt het meest uitgevoerd op geïmporteerde factureringsschemaregels die eerder in een ander systeem zijn gefactureerd. Factureringsschemaregels waarop stubverwerking is toegepast, worden weergegeven als stubs en maken geen factuur voor de klant.

### <a name="stub-records"></a>Stubrecords

1. Selecteer op de pagina **Massale stubverwerking** in het veld **Procesopties** de optie **Stub**.
2. Stel in het veld **Afsluitdatum** een afsluitdatum in om de regels op te geven waarop u het proces wilt toepassen. Alleen records waarvan de begindatum van de facturering valt op of eerder is dan de opgegeven afsluitdatum worden weergegeven.
3. Selecteer **Voorbeeld weergeven** om de regels weer te geven waarop u stubverwerking wilt toepassen.
4. Als u een regel wilt uitsluiten van het proces, markeert u deze en selecteert u **Verwijderen**.
5. Selecteer **Verwerken** om op de regels stubverwerking toe te passen.

### <a name="reverse-stub-records"></a>Stubverwerking op records omkeren

1. Selecteer op de pagina **Massale stubverwerking** in het veld **Procesopties** de optie **Stub omkeren**.
2. Stel in het veld **Afsluitdatum** een afsluitdatum in om de regels op te geven waarop u het proces wilt toepassen. Alleen records waarvan de begindatum van de facturering valt op of eerder is dan de opgegeven afsluitdatum worden weergegeven.
3. Selecteer **Voorbeeld weergeven** om de regels weer te geven waarvan u de stubverwerking wilt omkeren.
4. Als u een regel wilt uitsluiten van het proces, markeert u deze en selecteert u **Verwijderen**.
5. Selecteer **Verwerken** voor de regels waarvan u de stubverwerking wilt omkeren.

## <a name="update-completion-date-process"></a>Bijwerken van voltooiingsdatum verwerken

Gebruik de pagina **Voltooiingsdatum bijwerken** om de voltooiingsdatum voor specifieke mijlpaalartikelen bij te werken voor meerdere factureringsschema's of gebruikers. U kunt ook het voltooiingspercentage bijwerken voor artikelen in mijlpaalsjablonen die de methode **Percentage voltooid** gebruiken.

1. Ga op de pagina **Voltooiingsdatum bijwerken** naar **Mijlpaalverwerking** en selecteer **Voltooiingspercentage bijwerken**.
2. Voer in het veld **Percentagebedrag** het totale percentage in dat is voltooid.
3. Selecteer het artikelnummer dat is gerelateerd aan de mijlpaalsjabloon.
4. Selecteer op het sneltabblad **Op te nemen records** **Filter** om een specifieke waarde voor **Eindgebruikersrekening**, **Factureringsschemanummer** of **Artikelnummers** als filtercriterium te selecteren.
5. Selecteer **OK** om de wijziging te verwerken. Wanneer de verwerking is voltooid, wordt een nieuwe regel toegevoegd aan de mijlpaaltoewijzing. Deze regel staat voor het percentage dat is voltooid voor de mijlpaalsjabloon.

## <a name="unbilled-revenue-mass-processing"></a>Massale verwerking van niet-gefactureerde opbrengsten

Gebruik de pagina **Massale verwerking van niet-gefactureerde opbrengsten** om de niet-gefactureerde opbrengstjournaalpost te maken of om de journaalpost voor een of meer geselecteerde factureringsschema's of factureringsdetailregels te maken.

- **Journaalpost maken**: niet-gefactureerde opbrengstjournaalposten maken voor meerdere factureringsschemaregels. Gebruik de knop **Filter** op het sneltabblad **Op te nemen records** om het bereik met records te selecteren die in de lijst worden weergegeven. In de lijst worden alleen factureringsschemaregels weergegeven waarvoor geen niet-gefactureerde opbrengstjournaalposten zijn gemaakt. De eerste journaalposten worden gemaakt. Voor uitstelartikelen worden ook de uitstelplanningen gemaakt.
- **Journaalpost van stub**: de factureringsschemaregels markeren waarvoor de niet-gefactureerde journaalposten al zijn gemaakt. Deze optie wordt gebruikt als de niet-gefactureerde journaalpost al in een ander systeem is geboekt. Hiermee wordt het niet-gefactureerde opbrengstjournaal gemarkeerd als stubverwerking toegepast en wordt er geen transactie naar het grootboek geboekt.
- **Journaalpost van stub omkeren**: verwerkte stubjournaalposten omkeren. Als er een fout is gemaakt tijdens de verwerking van **Journaalpost van stub**, wordt met de optie het selectievakje **Als stub verwerkt** voor de factureringsschemaregel uitgeschakeld.
- **Detailregel van stubfacturering**: gebruik dit proces wanneer niet-gefactureerde opbrengst is verwerkt in een extern systeem en sommige factureringsdetailregels al zijn gefactureerd. Met dit proces zorgt u ervoor dat het juiste bedrag wordt weergegeven in de rekeningen voor niet-gefactureerde opbrengst.
- **Detailregel van stubfacturering omkeren**: alle acties voor **Detailregel van stubfacturering** omkeren.

Het veld **Journaalnaam** wordt gebruikt om **Journaalpost maken** naar het grootboek te boeken.

> [!NOTE]
> Met het stubproces worden geen bedragen naar het grootboek geboekt. Het veld **Journaalnaam** is niet voor alle processen van stubs verwerken en omkeren van stubs beschikbaar.

### <a name="unbilled-revenue-stub-example"></a>Voorbeeld van stub van niet-gefactureerde opbrengst

Een factureringsschema wordt ingesteld voor één jaar, van oktober 2021 tot en met september 2022. De niet-gefactureerde opbrengst is al in een extern systeem verwerkt. Negen maanden van het factureringsschema zijn al gefactureerd. Het bedrag voor elke factureringsperiode is € 250 per maand. Aan het begin van het jaar wordt het totale bedrag dat naar niet-gefactureerde opbrengst is geboekt, € 3.000. Na negen maanden is er al € 2250 gefactureerd en is € 750 nog steeds in niet-gefactureerde opbrengst.

Voer de volgende stappen uit om het factureringsschema in te stellen waarin slechts drie maanden aan niet-gefactureerde opbrengst overblijft.

1. Maak op de pagina **Factureringsdetails weergeven** een factureringsschema voor de periode van oktober 2021 tot en met september 2022, artikelnummer S0001 en een bedrag van € 250 per maand.
2. Selecteer **Journaalpost maken** voor het factureringsschema. Het bedrag van € 3.000 wordt naar niet-gefactureerde opbrengst geboekt.
3. Selecteer **Detailregel van stubfacturering** en geef een transactiedatum op van juni 2022 (negen maanden). De factureringsschemaregels worden niet weergegeven in het voorbeeld. De betrokken regels zijn gebaseerd op de transactiedatum.
4. Selecteer **OK**.

De eerste negen maanden die zijn gefactureerd, worden als stub verwerkt.

[![Detailregels van stubfacturering weergeven.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

€ 3.000 wordt tegengeboekt van niet-gefactureerde opbrengst en € 750 in niet-gefactureerde opbrengst die geboekt blijft. Als u de boekingen van niet-gefactureerde opbrengst wilt weergeven, selecteert u **Controle van niet-gefactureerde opbrengstjournaalboeking** op het tabblad **Verlengingen** van de regeldetailpagina.

[![Controle van niet-gefactureerde opbrengstjournaalboeking.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> De niet-gefactureerde opbrengstjournaalpost kan voor elke verlengingstermijn worden gemaakt, mits alle factureringsdetailregels van de vorige termijn zijn gefactureerd. Een factureringsschemaregel heeft bijvoorbeeld een maandelijkse factureringsfrequentie voor een periode van 12 maanden, van januari tot en met december 2021. De regel heeft drie termijnen: de eerste termijn, een tweede termijn (januari tot en met december 2022) en een derde termijn (januari tot en met december 2023). Nadat de factuur is gemaakt voor alle factureringsdetailregels van de eerste 12 maanden van 2021, kan de journaalboeking voor niet-gefactureerde opbrengst worden gemaakt voor de tweede termijn.
>
> Voor uitstelartikelen met de functie voor niet-gefactureerde opbrengst worden de factureringsregel en de kortingsregels verwerkt. Voor deze artikelen worden de niet-gefactureerde journaalboeking en de uitstelplanning voor de factureringsregel en de kortingsregel gemaakt.
>
> De journaalboekingen die worden gemaakt voor niet-uitstelbare artikelen en uitstelbare artikelen, maken een creditboeking naar verschillende opbrengstrekeningen.

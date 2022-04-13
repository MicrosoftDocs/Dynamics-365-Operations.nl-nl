---
title: Records groeperen en aggregatieberekeningen met behulp van GROUPBY-gegevensbronnen
description: In dit onderwerp wordt uitgelegd hoe u gegevensbronnen van het type GROUPBY kunt gebruiken in elektronische rapportage (ER).
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b79dfe62122a031ae9ed7f51ea7ff578cd47358
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462292"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Records groeperen en aggregatieberekeningen met behulp van GROUPBY-gegevensbronnen

[!include[banner](../includes/banner.md)]

Tijdens het configureren van ER-modeltoewijzingen of -indelingen ([elektronische rapportage](general-electronic-reporting.md)) kunt u vereiste gegevensbronnen [toevoegen](#AddMmDataSource2) van het type **GroupBy**.

Tijdens het ontwerpen wordt een **GroupBy**-gegevensbron geconfigureerd om de volgende elementen te identificeren:

- Een [basisgegevensbron](#BaseDataSource) die records bevat die worden gegroepeerd tijdens runtime
- [Groeperingsvelden](#GroupingFields) van de basisgegevensbron die worden gebruikt voor recordgroepering tijdens runtime
- [Aggregatiefuncties](#AggregateFunctions) waarmee de aggregatieberekeningen worden opgegeven die worden uitgevoerd voor elke gevonden groep tijdens runtime

Tijdens runtime worden met een geconfigureerde **GroupBy**-gegevensbron records gegroepeerd met dezelfde waarden in de groeperingsvelden, en wordt vervolgens een lijst met records geretourneerd. Elke record vertegenwoordigt één groep. Voor elke groep geeft de gegevensbron de veldwaarden weer waarop de initiële records zijn gegroepeerd, de waarden van de berekende aggregatiefuncties en de lijst met records van de basisgegevensbron die bij de groep hoort.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Aggregatiefuncties

Tijdens runtime wordt elke aggregatieberekening uitgevoerd voor elke groep records. Deze berekening wordt uitgevoerd met behulp van de waarde van één veld of een expressie in de records van een gegevensbron die is geselecteerd om te worden gegroepeerd in de bewerkbare gegevensbron van het type **GroupBy**. Momenteel worden de volgende aggregatiefuncties ondersteund:

- **AVG**: met deze functie retourneert u het gemiddelde van de waarden in een groep. Deze functie kan alleen worden gebruikt met numerieke velden.
- **COUNT**: met deze functie wordt het aantal in een groep gevonden artikelen geretourneerd.
- **Min**: met deze functie wordt de minimumwaarde van de waarden in een groep geretourneerd.
- **Max**: met deze functie wordt de maximumwaarde van de waarden in een groep geretourneerd.
- **SUM**: met deze functie wordt de som van alle waarden in een groep geretourneerd. Deze functie kan alleen worden gebruikt met numerieke velden.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Locatie van uitvoering

Wanneer u een **GroupBy**-gegevensbron bewerkt en de basisgegevensbron opgeeft die de records bevat die moeten worden gegroepeerd, wordt automatisch de meest efficiënte [locatie](#ExecutionLocation) voor uitvoering van die **GroupBy**-gegevensbron gedetecteerd. Als op de basisgegevensbron een [query kan worden uitgevoerd](er-functions-list-filter.md#usage-notes) (als deze kan worden uitgevoerd op databaseniveau), wordt de toepassingsdatabase ook opgegeven als de uitvoeringslocatie van de bewerkbare **GroupBy**-gegevensbron. Anders wordt het toepassingsservergeheugen opgegeven als de uitvoeringslocatie.

U kunt de automatisch gedetecteerde uitvoeringslocatie handmatig wijzigen door de locatie te selecteren die van toepassing is op de geconfigureerde gegevensbron. Als de uitvoeringslocatie die is geselecteerd niet van toepassing is, wordt een [validatiefout](er-components-inspections.md#i5) tijdens het ontwerpen gegeven.

> [!TIP]
> Het wordt aangeraden de databaselocatie te gebruiken om gegevensbronnen te groeperen die een groot aantal records weergeven.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Geheugenverbruik

Als een **GroupBy**-gegevensbron in het geheugen wordt uitgevoerd, wordt het toepassingsservergeheugen standaard gebruikt om records van de basisgegevensbron op te slaan die hoort bij elke aangetroffen groep als records van één groep. Als u het geheugenverbruik wilt verlagen, kunt u de recordopslag voor **GroupBy**-gegevensbronnen onderdrukken als deze zijn geconfigureerd om alleen samengevoegde functies te berekenen en de records van de groep niet tijdens runtime worden gebruikt. Als u op deze manier het geheugenverbruik wilt verminderen, moet u de functie **Geheugengebruik in ER verminderen wanneer recordgroepering alleen wordt gebruikt om aggregaties te berekenen** inschakelen in het werkgebied **Functiebeheer**.

## <a name="alternatives"></a><a name="Alternatives"></a>Alternatieven

Vergelijkbare aggregaties kunnen worden berekend met behulp van [verschillende](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) typen gegevensbronnen of ingebouwde functies voor ER.

Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Voorbeeld: gebruik een GROUPBY-gegevensbron voor aggregatieberekeningen en recordgroepering

Dit voorbeeld laat zien hoe een gebruiker met de rol Systeembeheerder of Functioneel consultant voor elektronische rapportage een ER-modeltoewijzing kan configureren met een **GROUPBY**-gegevensbron die wordt gebruikt om aggregatiefuncties te berekenen en records te groeperen. Deze modeltoewijzing wordt gebruikt om het controlerapport af te drukken wanneer de Intrastat-aangifte wordt gegenereerd. Met dit rapport kunt u gerapporteerde Intrastat-transacties bekijken.

De procedures in dit voorbeeld kunnen in het bedrijf **DEMF** worden uitgevoerd in Microsoft Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Voorbeeldgegevens voorbereiden

Zorg ervoor dat er Intrastat-transacties voor rapportage op de pagina **Intrastat** staan. U moet transacties hebben voor verschillende transportcodes, omdat u transacties in dit voorbeeld groepeert op het veld **Transport**.

![Intrastat-transacties op de Intrastat-pagina voorbereiden.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Het ER-raamwerk configureren

Voer de stappen in [Het ER-raamwerk configureren](er-quick-start2-customize-report.md#ConfigureFramework) uit om de minimale set ER-parameters in te stellen. U moet deze instellingen voltooien voordat u het ER-raamwerk gaat gebruiken om een ER-modeltoewijzing te ontwerpen.

### <a name="import-the-standard-er-format-configuration"></a>Standaardconfiguratie voor ER-indeling importeren

Volg de stappen in [Standaardconfiguratie voor ER-indeling importeren](er-quick-start2-customize-report.md#ImportERSolution1) om de standaard ER-configuraties toe te voegen aan de actuele instantie van Dynamics 365 Finance. Importeer versie 1 van de configuratie **Intrastat-model** uit de opslagplaats.

### <a name="create-a-custom-data-model-configuration"></a>Een aangepaste gegevensmodelconfiguratie maken

Voer de stappen in [Configuratie van een aangepast gegevensmodel toevoegen](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) uit om handmatig de nieuwe ER-gegevensmodelconfiguratie **Intrastat-model (Litware)** toe te voegen die u afleidt van de geïmporteerde configuratie **Intrastat-model**.

### <a name="configure-a-custom-data-model-component"></a>Een aangepast gegevensmodelonderdeel configureren

Voer de volgende stappen uit om de vereiste wijzigingen aan te brengen in het afgeleide gegevensmodel **Intrastat-model (Litware)**, zodat het kan worden gebruikt om transportcodes met de vereiste details weer te geven.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Intrastat-model (Litware)**.
3. Selecteer **Ontwerper**.
4. Selecteer op de pagina **Ontwerper gegevensmodel** in de modelstructuur de optie **Intrastat**.
5. Selecteer **Nieuw** om een nieuw genest knooppunt voor het geselecteerde **Intrastat**-knooppunt toe te voegen. Voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Voer in het veld **Naam** **Transport** in.
    2. Selecteer in het veld **Itemtype** **Recordlijst**.
    3. Selecteer **Toevoegen** om het nieuwe knooppunt toe te voegen.

6. Selecteer **Nieuw** om een nieuw genest knooppunt toe te voegen voor het knooppunt **Transport** dat u zojuist hebt toegevoegd. Voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Voer in het veld **Naam** **Code** in.
    2. Selecteer in het veld **Itemtype** **Tekenreeks**.
    3. Selecteer **Toevoegen** om het nieuwe knooppunt toe te voegen.

7. Selecteer **Nieuw** om een ander genest knooppunt toe te voegen voor het knooppunt **Transport**. Voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Voer in het veld **Naam** **TotalInvoicedAmount** in.
    2. Selecteer in het veld **Itemtype** **Werkelijk**.
    3. Selecteer **Toevoegen** om het nieuwe knooppunt toe te voegen.

8. Selecteer **Nieuw** om een ander genest knooppunt toe te voegen voor het knooppunt **Transport**. Voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Voer in het veld **Naam** **NumberOfTransactions** in.
    2. Selecteer in het veld **Itemtype** de waarde **Geheel getal**.
    3. Selecteer **Toevoegen** om het nieuwe knooppunt toe te voegen.

9. Selecteer **Nieuw** om een ander genest knooppunt toe te voegen voor het knooppunt **Transport**. Voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:

    1. Voer in het veld **Naam** **Transactie** in.
    2. Selecteer in het veld **Itemtype** **Recordlijst**.
    3. Selecteer **Toevoegen** om het nieuwe knooppunt toe te voegen.

10. Selecteer voor het knooppunt **Transactie** dat u zojuist hebt toegevoegd op het sneltabblad **Knooppunt** de optie **Artikelverwijzing omschakelen**.
11. Selecteer in het dialoogvenster **Artikelverwijzing omschakelen** in de gegevensmodelstructuur **CommodityRecord**. Selecteer vervolgens **OK**.

![Het geconfigureerde gegevensmodel in de ER-gegevensmodelontwerper.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Het ontwerp van een aangepast gegevensmodel voltooien

Voer de volgende stappen uit in [Het ontwerp van het gegevensmodel voltooien](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) om het ontwerp van het afgeleide gegevensmodel **Intrastat-model (Litware**) te voltooien.

### <a name="create-a-new-model-mapping-configuration"></a>Een nieuwe configuratie voor de modeltoewijzing maken

Voer de volgende stappen uit in [Een nieuwe modeltoewijzingsconfiguratie maken](er-quick-start1-new-solution.md#CreateModelMapping) om handmatig een nieuwe ER-modeltoewijzingsconfiguratie **Intrastat-voorbeeldtoewijzing** toe te voegen voor de afgeleide configuratie **Intrastat-model (Litware)**.

### <a name="add-a-new-model-mapping-component"></a>Een nieuw modeltoewijzingsonderdeel toevoegen

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur de configuratie **Intrastat-model** uit.
3. Selecteer de configuratie **Intrastat-voorbeeldtoewijzing**.
4. Selecteer **Ontwerper** om de lijst met toewijzingen te openen.
5. Selecteer **Verwijderen** om het bestaande toewijzingsonderdeel te verwijderen.
6. Selecteer **Nieuw** om een nieuw toewijzingsonderdeel toe te voegen.
7. Selecteer **Intrastat** in het veld **Definitie**.
8. Voer in het veld **Naam** **Intrastat-toewijzing** in.
9. Selecteer **Ontwerper** om de nieuwe toewijzing te configureren.

### <a name="design-the-added-model-mapping-component"></a>Het toegevoegde modeltoewijzingsonderdeel ontwerpen

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Een gegevensbron toevoegen voor toegang tot een toepassingstabel

Configureer een gegevensbron om toegang te krijgen tot de toepassingstabellen die de details van Intrastat-transacties bevatten.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.
2. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen** om een nieuwe gegevensbron toe te voegen die wordt gebruikt om de tabel **Intrastat** te openen. Elke record in de tabel **Intrastat** vertegenwoordigt één Intrastat-transactie.
3. Voer in het dialoogvenster **Gegevensbroneigenschappen** in het veld **Naam** **Transactie** in.
4. Voer in het veld **Tabel** **Intrastat** in.
5. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>Een gegevensbron toevoegen om Intrastat-transacties te groeperen

Configureer een **GroupBy**-gegevensbron om Intrastat-transacties te groeperen en aggregatiefuncties te berekenen.

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Functies\\Groeperen op**.
2. Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen** om een nieuwe gegevensbron toe te voegen die wordt gebruikt om Intrastat-transacties te groeperen en aggregatiefuncties te berekenen.
3. Voer in het dialoogvenster **Gegevensbroneigenschappen** in het veld **Naam** **TransportRecord** in.
4. Selecteer **Groeperen op bewerken** om groeperingsvoorwaarden te configureren.
5. Selecteer op de pagina **Groeperen op-parameters bewerken** in de lijst met gegevensbronnen in het rechterdeelvenster de gegevensbron **Transactie** en vouw deze uit.
6. Selecteer **Veld Toevoegen aan \> Wat groeperen** om aan te geven dat de gegevensbron **Transactie** is geselecteerd als de <a name="BaseDataSource">basisgegevensbron</a> voor de geconfigureerde **GroupBy**-gegevensbron. De records van de gegevensbron **Transactie** worden gegroepeerd en de veldwaarden van deze gegevensbron worden gebruikt voor berekeningen in aggregatiefuncties.
7. Selecteer het veld **Transaction\Transport** en selecteer vervolgens **Veld toevoegen aan \> Gegroepeerd veld** om aan te geven dat het veld **Transport** van de basisgegevensbron is geselecteerd als het <a name="GroupingFields">groeperingscriterium</a> voor de geconfigureerde **GroupBy**-gegevensbron. Met andere woorden, de records van de gegevensbron **Transactie** worden gegroepeerd op basis van de waarde van het veld **Transport**. Elke record van de geconfigureerde **GroupBy**-gegevensbron vertegenwoordigt één transportcode die is gevonden in records van de basisgegevensbron.
8. Selecteer het veld **Transaction\AmountMST** en voer vervolgens de volgende stappen uit:

    1. Selecteer **Veld toevoegen aan \> Aggregatievelden** om aan te geven dat een <a name="AggregateFunctions">aggregatiefunctie</a> voor dit veld wordt berekend.
    2. Selecteer de functie **Sum** in het deelvenster **Aggregaties** in de record die is toegevoegd voor het geselecteerde veld **Transaction\AmountMST** in het veld **Methode**.
    3. Voer in het optionele veld **Naam** **TotalInvoicedAmount** in.

    Deze instellingen bepalen dat voor elke transportgroep het totaalbedrag van het veld **Transaction\AmountMST** wordt berekend.

9. Selecteer het veld **Transaction\RecId** en voer vervolgens de volgende stappen uit:

    1. Selecteer **Veld toevoegen aan \> Aggregatievelden** om aan te geven dat een aggregatiefunctie voor dit veld wordt berekend.
    2. Selecteer de functie **Count** in het deelvenster **Aggregaties** in de record die is toegevoegd voor het geselecteerde veld **Transaction\RecId** in het veld **Methode**.
    3. Voer in het optionele veld **Naam** **NumberOfTransactions** in.

    Deze instellingen bepalen dat voor elke transportgroep het aantal transacties in de groep wordt berekend.

10. Selecteer **Opslaan**.
11. Bekijk de <a name="ExecutionLocation">uitvoering</a>sparameters van de bewerkbare gegevensbron. In het veld **Uitvoeringslocatie** is **Automatisch detecteren** automatisch geselecteerd en bevat het veld **Uitvoering** de waarde **SQL**. Met deze instellingen wordt aangegeven dat op de geselecteerde **Transactie**-basisgegevensbron momenteel een query kan worden uitgevoerd en u kunt de bewerkbare **GroupBy**-gegevensbron op databaseniveau uitvoeren.
12. Open de zoekactie voor het veld **Uitvoeringslocatie** om de lijst met beschikbare waarden te bekijken. U kunt **Query** of **In geheugen** selecteren als u wilt dat deze **GroupBy**-gegevensbron op databaseniveau of in het toepassingsservergeheugen wordt uitgevoerd.
13. Selecteer **Opslaan** en sluit de pagina **Groeperen op-parameters bewerken**.
14. Selecteer **OK** om de instellingen van de gegevensbron **GroupBy** in te vullen.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>De GroupBy-gegevensbron verbinden aan gegevensmodelvelden

Verbind de geconfigureerde gegevensbron aan de velden van het gegevensmodel om op te geven hoe het gegevensmodel tijdens runtime moet worden gevuld met toepassingsgegevens.

1. Vouw op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensmodel** het knooppunt **Transport** uit.
2. Vouw in het deelvenster **Gegevensbronnen** de gegevensbron **TransportRecord** uit.
3. Een binding toevoegen om de lijst met ontdekte transportgroepen weer te geven:

    1. Selecteer het item **Transport** in het deelvenster **Gegevensmodel**.
    2. Selecteer in het deelvenster **Gegevensbronnen** de gegevensbron **TransportRecord**.
    3. Selecteer **Binden**.

4. Een binding toevoegen om de transportcode van elke ontdekte transportgroep weer te geven:

    1. Selecteer het gegevensmodelitem **Transport.Code**.
    2. Selecteer het gegroepeerde veld **TransportRecord.grouped.TransportMode**.
    3. Selecteer **Binden**.

5. Voeg een binding toe om de waarden van berekende aggregatiefuncties voor elke ontdekte transportgroep weer te geven:

    1. Selecteer het gegevensmodelitem **Transport.NumberOfTransactions**.
    2. Selecteer het aggregatieveld **TransportRecord.aggregated.NumberOfTransactions**.
    3. Selecteer **Binden**.
    4. Selecteer het gegevensmodelitem **Transport.TotalInvoicedAmount**.
    5. Selecteer het aggregatieveld **TransportRecord.aggregated.TotalInvoicedAmount**.
    6. Selecteer **Binden**.

6. Een binding toevoegen om transactierecords die bij elke ontdekte transportgroep horen weer te geven:

    1. Selecteer het gegevensmodelitem **Transport.Transaction**.
    2. Selecteer het veld **TransportRecord.lines**.
    3. Selecteer **Binden**.

    U kunt bindingen blijven configureren voor de geneste items van het gegevensmodelitem **Transport.Transaction** en het gegevensbronveld **TransportRecord.lines** om tijdens runtime details weer te geven van de Intrastat-transacties die bij elke ontdekte transportgroep horen.

![Geconfigureerde modeltoewijzing in de ER-ontwerper voor de modeltoewijzing.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Fouten opsporen in het toegevoegde modeltoewijzingsonderdeel

Gebruik [Foutopsporing voor ER-gegevensbronnen](er-debug-data-sources.md) om de geconfigureerde modeltoewijzing te testen.

1. Selecteer **Foutopsporing starten** op de pagina **Ontwerper modeltoewijzing**.
2. Selecteer op de pagina **Fouten opsporen in gegevensbronnen** in het linkerdeelvenster de gegevensbron **TransportRecord** en selecteer vervolgens **Alle records lezen**.
3. Vouw de gegevensbron **TransportRecord** uit en voer vervolgens de volgende stappen uit:

    1. Selecteer de gegevensbron **TransportRecord.grouped.TransportMode**.
    2. Selecteer **Waarde ophalen**.
    3. Selecteer de gegevensbron **TransportRecord.grouped.NumberOfTransactions**.
    4. Selecteer **Waarde ophalen**.
    5. Selecteer de gegevensbron **TransportRecord.grouped.TotalInvoicedAmount**.
    6. Selecteer **Waarde ophalen**.

4. Selecteer **Alles uitvouwen** in het rechterdeelvenster.

Met de gegevensbron **TransportRecord** worden twee records weergegeven en twee transportcodes. Voor elke transportcode worden het aantal transacties en het totale gefactureerde bedrag berekend.

> [!NOTE]
> De methode 'lui lezen' wordt gebruikt wanneer een **GroupBy**-gegevensbron wordt aangeroepen om databaseoproepen te optimaliseren. Daarom worden sommige veldwaarden in een **GroupBy**-gegevensbron alleen berekend in de foutopsporing voor ER-gegevensbronnen wanneer deze zijn verbonden met gegevensmodelvelden.

![Resultaten van foutopsporing in gegevensbronnen op de pagina Fouten opsporen in gegevensbronnen.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Is er een manier om eindtotalen te berekenen wanneer de groepstotalen worden berekend?

Ja. Als u eindtotalen wilt berekenen, configureert u een andere **GroupBy**-gegevensbron waarbij de eerder geconfigureerde **GroupBy**-gegevensbron wordt gebruikt als basisgegevensbron. Hieronder ziet u een voorbeeld van de gegevensbron **Totalen** van het type **GroupBy** dat wordt gebruikt om de aggregatiefunctie **SUM** te berekenen op basis van de **SUM**-aggregatie van de gegevensbron **TransportRecord** van het type **GroupBy**.

![Gegevensbron Totalen in de ontwerper voor ER-modeltoewijzingen.](./media/er-groupby-data-sources-configure-model-mapping2.png)

In de volgende afbeelding ziet u de resultaten van de foutopsporing van de gegevensbron **Totalen**.

![Resultaten van foutopsporing in de gegevensbron Totalen op de pagina Fouten opsporen in gegevensbronnen.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [Fouten opsporen in gegevensbronnen van een uitgevoerde ER-indeling om gegevensstromen en transformatie te analyseren](er-debug-data-sources.md)
- [Gegevensbronnen voor GEGEVENSVERZAMELING in elektronische rapportageindelingen gebruiken](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

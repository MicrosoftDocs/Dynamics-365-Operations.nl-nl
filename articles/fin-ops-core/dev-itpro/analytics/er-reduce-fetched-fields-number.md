---
title: De prestaties van ER-oplossingen verbeteren door het aantal tabelvelden te beperken dat wordt opgehaald tijdens runtime
description: In dit artikel wordt uitgelegd hoe u de prestaties van ER-oplossingen kunt verbeteren door het aantal tabelvelden te beperken dat wordt opgehaald tijdens runtime.
author: kfend
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 5c9481f1021a5dba6e1d4020bbf85a10bd551ac0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278821"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>De prestaties van ER-oplossingen verbeteren door het aantal tabelvelden te beperken dat wordt opgehaald tijdens runtime

[!include[banner](../includes/banner.md)]

U kunt ER-[indelingen](er-overview-components.md#format-components-for-outgoing-electronic-documents) ([elektronische rapportage](general-electronic-reporting.md)) ontwerpen die uitgaande documenten genereren in verschillende indelingen. Wanneer een document wordt gegenereerd, roept een ER-indeling gegevensbronnen aan die zijn geconfigureerd in een corresponderende ER-[modeltoewijzing](er-overview-components.md#model-mapping-component). Als u toegang wilt configureren tot toepassingstabellen, query's of entiteiten voor het ophalen van records, kunt u ER-gegevensbronnen van het type *Tabelrecords* gebruiken. Met een gegevensbron van het type *Tabelrecords* worden standaard de waarden van alle velden in de aangevraagde records opgehaald. U kunt dit type gegevensbron echter zo configureren dat alleen de veldwaarden worden opgehaald die vereist zijn voor de actieve ER-indeling. Met deze configuratie wordt het geheugenverbruik beperkt van de toepassingsserver die gegevens ophaalt en bevordert u de caching van records.

Voer het voorbeeld in dit artikel uit voor meer informatie over het beperken van de lijst met opgehaalde velden met gegevensbronnen van het type *Tabelrecords*.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Voorbeeld: Het aantal tabelvelden beperken dat wordt opgehaald tijdens runtime

De volgende procedures laten zien hoe een gebruiker met de rol Systeembeheerder of Ontwikkelaar elektronische rapportage een ER-modeltoewijzing zo kan configureren dat alleen de velden worden opgehaald die nodig zijn om de ER-indeling uit te voeren, zodat het verbruik van het toepassingsservergeheugen wordt verkleind.

Deze procedures kunnen in het bedrijf **USMF** in Microsoft Dynamics 365 Finance worden uitgevoerd. U hoeft hiervoor geen code te schrijven.

Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot het bedrijf **USMF** voor een van de volgende rollen:

- Functioneel consultant elektronische rapportage
- Systeembeheerder

In dit voorbeeld gebruikt u de ER-[configuraties](general-electronic-reporting.md#Configuration) die beschikbaar zijn voor het voorbeeldbedrijf **Litware, Inc.**. Controleer of de configuratieprovider voor het voorbeeldbedrijf **Litware, Inc.** (`http://www.litware.com`) wordt vermeld voor het ER-raamwerk en of het is gemarkeerd is als **Actief**. Als deze configuratieprovider niet wordt vermeld of als deze niet is gemarkeerd als **Actief**, volgt u de stappen in het onderwerp [Een configuratieprovider maken en als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>Het ER-raamwerk configureren

Voer de stappen in [Het ER-raamwerk configureren](er-quick-start2-customize-report.md#ConfigureFramework) uit om de minimale set ER-parameters in te stellen. U moet deze instellingen voltooien voordat u het ER-raamwerk gaat gebruiken om gegevensbronnen van de beschikbare ER-oplossing te wijzigen.

### <a name="import-the-sample-er-configurations"></a>De voorbeeld-ER-configuraties importeren

Als u het voorbeeld in het artikel [Een nieuwe ER-oplossing ontwerpen om een aangepast rapport af te drukken](er-quick-start1-new-solution.md) nog niet hebt voltooid, moet u de XML-bestanden voor de volgende configuraties van de geleverde ER-oplossing downloaden en lokaal opslaan.

| Omschrijving inhoud            | Bestandsnaam |
|--------------------------------|-----------|
| Configuratie van model voor ER-gegevens    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| Configuratie van ER-modeltoewijzing | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER-indelingsconfiguratie        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Volg vervolgens deze stappen om de configuraties van de geleverde ER-oplossing naar uw exemplaar van Finance te uploaden.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer **Rapportageconfiguraties**.
3. Importeer de ER-gegevensmodelconfiguratie op de pagina **Configuraties**.

    1. Selecteer **Uitwisselen** en selecteer vervolgens **Laden uit XML-bestand**.
    2. Selecteer **Bladeren**, zoek en selecteer het bestand **Questionnaires model.version.1.xml** en selecteer **OK**.

4. Importeer de configuratie voor de ER-modeltoewijzing.

    1. Selecteer **Uitwisselen** en selecteer vervolgens **Laden uit XML-bestand**.
    2. Selecteer **Bladeren**, zoek en selecteer het bestand **Questionnaires mapping.1.1.xml** en selecteer **OK**.

5. Importeer de ER-indelingsconfiguratie.

    1. Selecteer **Uitwisselen** en selecteer vervolgens **Laden uit XML-bestand**.
    2. Selecteer **Bladeren**, zoek en selecteer het bestand **Questionnaires format.1.1.xml** en selecteer **OK**.

6. Vouw in de configuratiestructuur **Questionnaires model** uit.
7. Bekijk de lijst met geïmporteerde ER-configuraties in de configuratiestructuur.

    ![De lijst met geïmporteerde ER-configuraties op de pagina Configuraties controleren.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>De geleverde ER-modeltoewijzing controleren

1. Selecteer **Questionnaires mapping** op de pagina **Configuraties**.
2. Selecteer **Ontwerper** in het actievenster.
3. Selecteer **Ontwerper** op de pagina **Model voor gegevensbrontoewijzing** .
4. Selecteer op de pagina **Ontwerper modeltoewijzingen** in het actievenster de optie **Groepsweergave** om de weergave **Groep** in te schakelen.
5. Vouw **Vragenlijst** in het deelvenster **Gegevensmodel** uit.

    De gegevensbron **Vragenlijst** is geconfigureerd om toegang te krijgen tot de `KMCollection`-toepassingstabel.

6. Vouw in het deelvenster **Gegevensbronnen** de items **Tabelrecords** \> **Vragenlijst** \> **Velden** uit.

    Zie hoeveel velden in de toepassingstabel `KMCollection` beschikbaar worden gemaakt door de gegevensbron **Vragenlijst** van het type *Tabelrecords*.

    ![De geleverde modeltoewijzing op de pagina Ontwerper modeltoewijzingen met de ingeschakelde groepsweergave controleren.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Selecteer in het actievenster de optie **Groepsweergave** opnieuw om de weergave **Groep** uit te schakelen en selecteer vervolgens **Alles weergeven** \> **Alleen toegewezen weergeven**.

    Enkele velden van de toepassingstabel `KMCollection` worden gebruikt om de recordlijst **Vragenlijst** in het ER-gegevensmodel in te vullen:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![De geleverde modeltoewijzing op de pagina Ontwerper modeltoewijzingen met de uitgeschakelde groepsweergave controleren.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>De ER-prestatietracering inschakelen

Volg de stappen in [De ER-prestatietracering inschakelen](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) om de ER-gebruikersparameters in te stellen waarmee de uitvoering van ER-onderdelen kan worden getraceerd.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>De geleverde ER-indeling uitvoeren met de geleverde modeltoewijzing

Voer de stappen in [Een ontwerpindeling vanuit ER uitvoeren](er-quick-start1-new-solution.md#RunFormatFromER) uit om de geleverde ER-indeling voor één vragenlijst uit te voeren via de pagina **Configuraties**.

### <a name="review-the-execution-trace-of-the-first-run"></a>De trace van uitvoering van de eerste uitvoering controleren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage \> Configuraties**.
2. Vouw op de pagina **Configuraties** de optie **Questionnaires model** uit en selecteer **Questionnaires mapping**.

    > [!NOTE]
    > De details op het sneltabblad **Versies** geven aan dat u de conceptversie van de configuratie **Questionnaires mapping** hebt geselecteerd. Daarom kunt u de inhoud van deze modeltoewijzing wijzigen.

3. Selecteer **Ontwerper** in het actievenster.
4. Selecteer **Ontwerper** op de pagina **Model voor gegevensbrontoewijzing** .
5. Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Prestatietracering**.
6. Selecteer in het dialoogvenster **Instellingen voor resultaten prestatietracering** de trace die is gegenereerd tijdens de laatste uitvoeringsindeling.

    ![De trace selecteren in het dialoogvenster Instellingen voor resultaat van prestatietracering.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Selecteer **OK**. 
8. Filter op het sneltabblad **Details** het pad **Vragenlijst** dat naar de gegevensbron **Vragenlijst** wijst.
9. Bekijk de details van de databasequery die is gegenereerd toen de gegevensbron **Vragenlijst** werd aangeroepen.

    Alle velden van de toepassingstabel `KMCollection` zijn opgehaald tijdens runtime toen de gegevensbron **Vragenlijst** werd aangeroepen.

    ![De details van de databasequery bekijken op de pagina Ontwerper modeltoewijzingen.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>De geleverde ER-modeltoewijzing wijzigen

1. Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensbronnen** de gegevensbron **Vragenlijst**.
2. Selecteer **Bewerken** in het deelvenster **Gegevensbronnen**.
3. Selecteer in het dialoogvenster **Eigenschappen van gegevensbron** de optie **Velden selecteren** om de lijst met velden op te geven van de toepassingstabel `KMCollection` waarnaar wordt verwezen en die wordt opgehaald wanneer de bewerkbare gegevensbron **Vragenlijst** wordt aangeroepen.

    ![Velden selecteren in het dialoogvenster Eigenschappen van gegevensbron selecteren om de lijst met velden te configureren die moet worden opgehaald uit de toepassingstabel via de bewerkbare gegevensbron.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Selecteer **Automatisch invullen** op de pagina **Velden selecteren**.

    De lijst **Geselecteerde velden** wordt automatisch ingevuld op basis van voorgeconfigureerde artefacten van de modeltoewijzing. Alle velden en relaties van de tabel waarnaar wordt verwezen en die worden genoemd in een binding, formule of gegevensbron van de modeltoewijzing worden toegevoegd aan de lijst.

    ![De lijst met velden configureren die worden opgehaald uit de toepassingstabel op de pagina Velden selecteren.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Selecteer **Opslaan** en sluit de pagina **Velden selecteren**.
6. Selecteer **OK** om de aangebrachte wijzigingen in de gegevensbroninstellingen op te slaan.
7. Selecteer **Alles weergeven** in het actievenster.

    In de gegevensbron **Vragenlijst** wordt nu de tekst **\<Fields are filtered\>** weergegeven. Deze tekst geeft aan dat de gegevensbron is geconfigureerd om een beperkt aantal velden op te halen uit de toepassingstabel waarnaar wordt verwezen.

    ![De bijgewerkte modeltoewijzing op de pagina Ontwerper modeltoewijzingen controleren.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Selecteer **Opslaan** om de aangebrachte wijzigingen in de bewerkbare modeltoewijzing op te slaan.

    > [!NOTE]
    > Tijdens runtime worden de toegevoegde relaties geanalyseerd en worden alle hierin gebruikte velden aan de databasequery toegevoegd, zelfs als deze velden niet expliciet zijn toegevoegd aan de lijst met opgehaalde velden tijdens het ontwerpen.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>De geleverde ER-indeling uitvoeren met de bijgewerkte modeltoewijzing

Voer de stappen in [Een ontwerpindeling vanuit ER uitvoeren](er-quick-start1-new-solution.md#RunFormatFromER) uit om de geleverde ER-indeling voor één vragenlijst uit te voeren via de pagina **Configuraties**.

### <a name="review-the-execution-trace-of-the-second-run"></a>De trace van uitvoering van de tweede uitvoering controleren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** de optie **Questionnaires model** uit en selecteer **Questionnaires mapping**.
3. Selecteer **Ontwerper** in het actievenster.
4. Selecteer **Ontwerper** op de pagina **Model voor gegevensbrontoewijzing** .
5. Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Prestatietracering**.
6. Selecteer in het dialoogvenster **Instellingen voor resultaten prestatietracering** de trace die is gegenereerd tijdens de laatste uitvoeringsindeling.
7. Selecteer **OK**.
8. Filter op het sneltabblad **Details** het pad **Vragenlijst** dat naar de gegevensbron **Vragenlijst** wijst.
9. Bekijk de details van de databasequery die is gegenereerd toen de gegevensbron **Vragenlijst** werd aangeroepen.

    Alleen de velden die nodig zijn om de gegevensbron in te vullen, zijn tijdens runtime opgehaald uit de `KMCollection`-toepassingstabel toen de gegevensbron **Vragenlijst** werd aangeroepen.

    > [!NOTE]
    > Sommige velden, zoals de velden voor de partitie-id, gegevensgebieds-id en record-id, worden automatisch toegevoegd door het framework voor gegevensbeheer van de Finance-app.

    ![De details van de databasequery voor de bijgewerkte modeltoewijzing bekijken op de pagina Ontwerper modeltoewijzingen.](./media/er-reduce-fetched-fields-number-query2.png)

U kunt deze techniek gebruiken om het aantal opgehaalde records te verminderen wanneer u het geheugenverbruik moet verminderen via de actieve ER-modeltoewijzing en ER-indeling.

## <a name="limitations"></a>Beperkingen

Wanneer u het aantal opgehaalde velden voor een gegevensbron van het type *Tabelrecords* beperkt, kunt u de methoden van een toepassingstabel waarnaar de gegevensbron verwijst niet gebruiken, omdat de metagegevens van de toepassing geen informatie bevatten over tabelvelden die nodig zijn om deze methoden te kunnen aanroepen.

## <a name="usage-notes"></a>Gebruiksaanwijzingen

Hoewel met de opdracht **Automatisch invullen** automatisch velden worden toegevoegd, worden velden die eerder zijn toegevoegd niet automatisch verwijderd, ook niet als deze niet meer worden gebruikt in bindingen, formules en gegevensbronnen van de bewerkbare modeltoewijzing.

Wanneer u **Automatisch invullen** selecteert, worden de bindingen, formules en de gegevensbronnen geanalyseerd die de bewerkbare modeltoewijzing bevatte toen u deze opende om te bewerken. Als u bindingen, formules en gegevensbronnen van de bewerkbare modeltoewijzing wijzigt en u de opdracht **Automatisch invullen** wilt gebruiken, sluit u de modeltoewijzingsontwerper en opent u deze vervolgens opnieuw om de modeltoewijzing te bewerken. 

## <a name="additional-resources"></a>Aanvullende bronnen

- [De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)
- [Prestatieproblemen in ER-configuraties oplossen](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

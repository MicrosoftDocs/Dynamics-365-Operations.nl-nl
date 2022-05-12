---
title: ER-configuraties ontwerpen om in te vullen in PDF-sjablonen
description: Dit onderwerp bevat informatie over het ontwerpen van een indeling voor elektronische rapportage (ER) voor het invullen van een PDF-sjabloon.
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 706256300cf0b64bc5b5e1e7adb77c1da500d16f
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645102"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>ER-configuraties ontwerpen om in te vullen in PDF-sjablonen

[!include[banner](../includes/banner.md)]

De procedures in dit onderwerp zijn voorbeelden die aangeven hoe een gebruiker in de rol van **Systeembeheerder** of de rol van **Ontwikkelaar elektronische rapportage** een indeling voor elektronische rapportage (ER) kan configureren waarmee rapporten als PDF-bestanden worden gegenereerd door invulbare PDF-documenten als rapportsjablonen te gebruiken. Deze stappen kunnen worden uitgevoerd in elk bedrijf van Dynamics 365 Finance of in Regulatory Configuration Services (RCS).

## <a name="prerequisites"></a>Vereisten

Voordat u begint, moet u een van de volgende typen toegang hebben, afhankelijk van de service die u gebruikt om de procedures in dit onderwerp uit te voeren:

- Toegang tot Financiën voor een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Toegang tot RCS voor een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

U moet ook de procedure [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) uitvoeren.

Tot slot moet u de volgende bestanden downloaden.

| Omschrijving inhoud                       | Bestandsnaam                                     |
|-------------------------------------------|-----------------------------------------------|
| Sjabloon voor de eerste pagina van het rapport | [IntrastatReportTemplate1.pdf](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Sjabloon voor de overige pagina's van het rapport    | [IntrastatReportTemplate2.pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| Voorbeeld van ER-indeling - PDF                          | [Intrastat report (PDF).version.1.1.xml](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| Voorbeeld van ER-indeling - Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Voorbeeld van gegevensset                            | [Intrastat sample data.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>De indelingsconfiguratie ontwerpen

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Toegang krijgen tot de lijst met configuraties die door Microsoft zijn geleverd

1. Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.
2. Controleer of de leverancier **Litware, Inc.** beschikbaar is en als actief is gemarkeerd.
3. Ga naar de tegel voor de provider **Microsoft** en selecteer **Opslagplaatsen**.

    > [!NOTE]
    > Als er al een opslagplaats van het type **LCS** bestaat, slaat u de resterende stappen van deze procedure over.

4. Selecteer **Toevoegen**.
5. Ga naar het vervolgkeuzemenu en selecteer in de veldgroep **Type opslagplaats van configuratie** de optie **LCS**.
6. Selecteer **Opslagplaats maken**.
7. Selecteer **OK**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>De modelconfiguraties ophalen die door Microsoft worden geleverd

1. Selecteer aan de linkerkant van de pagina **Opslagplaatsen van configuraties** de knop **Filters weergeven** (het trechtersymbool).
2. Voeg een filter voor de waarde van **LCS** toe in het veld **Type** en gebruik de operator **begint met**.
3. Selecteer **Toepassing**.
4. Selecteer **Openen**.
5. Selecteer **Intrastat-model** in de structuur.
6. Selecteer op het sneltabblad **Versies** de versie **1**.

    > [!NOTE]
    > Als de knop **Importeren** op het sneltabblad **Versies** niet beschikbaar is, slaat u de resterende stappen van deze procedure over.

7. Selecteer **Importeren**.
8. Selecteer **Ja** om het importeren van de geselecteerde versie van de modelconfiguratie van **Intrastat-model** te bevestigen.

### <a name="create-a-new-format-configuration"></a>Een nieuwe indelingsconfiguratie maken

1. Selecteer in het werkgebied **Elektronische rapportage** de tegel **Rapportconfiguraties**.
2. Selecteer **Intrastat-model** in de structuur.
3. Selecteer **Configuratie maken**.

    > [!NOTE]
    > Als de knop **Configuratie maken** niet beschikbaar is, moet u de ontwerpmodus inschakelen op de pagina **Parameters van elektronische rapportage** die kan worden geopend vanuit het werkgebied **Elektronische rapportage**.

4. Ga naar het vervolgkeuzemenu en selecteer in de veldgroep **Nieuw** de optie **Indeling gebaseerd op gegevensmodel Intrastat**.
5. Voer in het veld **Naam** de waarde **Intrastat-rapport (PDF)** in.
6. Voer in het veld **Beschrijving** de waarde **Intrastat-rapport in PDF-indeling** in.

    > [!NOTE]
    > De actieve configuratieprovider wordt automatisch ingevoerd. Deze provider kan deze configuratie onderhouden. Hoewel andere providers deze configuratie wel kunnen gebruiken, kunnen zij deze niet onderhouden.

7. Optioneel: in het veld **indelingstype** kunt u een specifieke indeling voor het elektronische document selecteren. Als u **PDF** selecteert, biedt de ER Operations-ontwerper tijdens het ontwerp uitsluitend de opmaakelementen aan die alleen van toepassing zijn op documenten die worden gegenereerd in PDF-indeling (**PDF\Bestand**, **PDF\PDF-samenvoeger** enzovoort). Als u dit veld leeg laat, wordt tijdens het ontwerp een indeling van het elektronische document opgegeven in de ER Operations-ontwerper wanneer een eerste opmaakelement wordt toegevoegd. Als u bijvoorbeeld **Excel\File** toevoegt als eerste opmaakelement , biedt de ER Operations-ontwerper alleen de opmaakelementen die van toepassing zijn op documenten die zijn gegenereerd in Excel-indeling (**Excel\Cell**, **Excel\Range** enzovoort). opmaak.
8. Selecteer **Configuratie maken**.

Er wordt een nieuwe ER-indelingsconfiguratie gemaakt. U kunt de conceptversie van deze configuratie gebruiken om het onderdeel voor de ER-indeling op te slaan dat is ontworpen voor het genereren van elektronische documenten in PDF-indeling.

### <a name="design-the-format-of-an-electronic-document"></a>De indeling van een elektronisch document ontwerpen

Vervolgens ontwerpt u in de configuratie voor de ER-indeling die u hebt gemaakt, de ER-indeling waarmee het rapport **Intrastat-controle** wordt gegenereerd in PDF-indeling. Op de eerste pagina van dit rapport moet een overzicht van het rapport worden weergegeven plus details van de buitenlandse handelstransacties waarover wordt gerapporteerd. Op de overige pagina's mogen alleen details worden weergegeven van de buitenlandse handelstransacties waarover wordt gerapporteerd. Aangezien de gegenereerde rapportpagina's verschillende indelingen moeten hebben, worden er twee verschillende sjablonen in PDF-indeling gebruikt in de ER-indeling.

Open in een willekeurige PDF-viewer de PDF-sjablonen die u hebt gedownload. Zoals u ziet, bevat elke sjabloon meerdere velden die moeten worden ingevuld. In elke sjabloon worden details van de buitenlandse handelstransacties weergegeven als 42 rijen met elk negen velden. Het rijnummer staat aan het einde van de naam van elk veld (bijvoorbeeld **Datum 1**...**Datum 42** en **Basisproduct 1**...**Basisproduct 42**).

In de volgende afbeelding wordt de PDF-sjabloon weergegeven voor de eerste pagina van het rapport.

![Sjabloon 1.](media/rcs-ger-filloutpdf-template1.png)

In de volgende afbeelding wordt de PDF-sjabloon weergegeven voor andere pagina's van het rapport.

![Sjabloon 2.](media/rcs-ger-filloutpdf-template2.png)

1. Selecteer **Ontwerper** op de pagina **Configuraties**.
2. Selecteer **Basis toevoegen**.
3. Ga naar het vervolgkeuzemenu en selecteer **PDF \> PDF-samenvoeger** in de structuur.

    Wanneer u het element **PDF-samenvoeger** selecteert als basiselement van de indeling, worden alle PDF-documenten die tijdens de uitvoering worden gegenereerd samengevoegd tot een enkel definitief PDF-document. Als u slechts één PDF-sjabloon nodig hebt om alle vereiste documenten te genereren met de ER-indeling die u ontwerpt, kunt u **PDF-bestand** als basiselement selecteren.

4. Voer in het veld **Naam** de tekst **Uitvoer** in.
5. Selecteer in het veld **Taalvoorkeuren** de optie **Gebruikersvoorkeuren**. Het rapport wordt gegenereerd in de voorkeurstaal van de gebruiker die het rapport uitvoert.
6. Selecteer in het veld **Cultuurvoorkeuren** de optie **Gebruikersvoorkeuren**. Waarden en datums die op de pagina's van het rapport worden weergegeven, worden opgemaakt op basis van de geprefereerde landinstelling van de gebruiker die het rapport uitvoert.
7. Selecteer **OK**.
8. Selecteer in het actievenster op het tabblad **Importeren** de optie **Importeren vanuit PDF**.

    Wanneer een invulbaar PDF-document wordt geïmporteerd als een sjabloon voor deze ER-indeling, worden alle vereiste elementen voor ER-indelingen (de elementen **PDF-bestand**, **Veldgroep** en **Veld**) automatisch gemaakt in de indeling die wordt ontworpen op basis van de structuur van het PDF-document dat wordt geïmporteerd.

9. Selecteer **Bladeren**. Navigeer naar en selecteer het bestand **IntrastatReportTemplate1.pdf** dat u eerder hebt gedownload als vereiste.
10. Selecteer **OK**.

    Het geselecteerde bestand wordt geladen en het veld **Sjabloon** in het dialoogvenster **Importeren vanuit PDF** wordt ingevuld.

11. Stel de optie **Groepsvelden** in op **Ja**. Als het geselecteerde PDF-document veldgroepen bevat, worden deze gebruikt om de gemaakte elementen van de ER-indeling te groeperen. Hiervoor wordt een opmaakelement **Veldgroep** gemaakt.

    Als deze optie is ingesteld op **Nee**, worden de vereiste elementen van ER-indeling gemaakt als een platte lijst met elementen die zijn genest onder het indelingselement **PDF-bestand** dat wordt gemaakt.

12. Selecteer **OK**.

    ![Dialoogvenster Importeren vanuit PDF.](media/rcs-ger-filloutpdf-importtemplate.png)

13. Vouw in de structuur **Uitvoer** uit.

    Zoals u ziet, is het onderdeel **PDF-bestand** automatisch gemaakt om het maken van de eerste pagina van het rapport te beheren dat tijdens de uitvoering wordt gegenereerd.

14. Vouw in de structuur **Uitvoer \> PDF-bestand** uit.

    Zoals u ziet, wordt de gestructureerde lijst met opmaakelementen automatisch gemaakt in deze ER-indeling, op basis van de structuur van het invulbare PDF-document dat u eerder hebt geïmporteerd.

15. Selecteer in de structuur **Uitvoer \> PDF-bestand**.
16. Voer in het veld **Naam** de tekst **Pagina 1** in.

    Dit opmaakelement wordt gebruikt om de eerste pagina van het rapport **Intrastat-controle** te genereren. Op deze pagina wordt een overzicht weergegeven van het rapport plus details van de buitenlandse handelstransacties.

    Als u het veld **Taalvoorkeuren** leeg laat, bepaalt de instelling **Taalvoorkeuren** van het bovenliggende element **PDF-samenvoeger** in welke taal het rapport wordt gegenereerd door gebruik te maken van dit opmaakelement. U kunt een andere waarde selecteren om de instelling van het bovenliggende element te negeren.

    Als u het veld **Cultuurvoorkeuren** leeg laat, bepaalt de instelling **Cultuurvoorkeuren** van het bovenliggende element **PDF-samenvoeger** met welke landinstellingen het rapport wordt gegenereerd door gebruik te maken van dit opmaakelement. De landinstelling bepaalt de indeling van waarden en datums op de pagina's van het rapport. U kunt een andere waarde selecteren om de instelling van het bovenliggende element te negeren.

17. Selecteer in het deelvenster Actie het tabblad **Importeren**. Zoals u ziet, is de knop **Bijwerken vanuit PDF** beschikbaar gekomen voor het geselecteerde opmaakelement, **PDF-bestand**.

    U kunt deze knop gebruiken om de bijgewerkte PDF-sjabloon te importeren in de bewerkte indeling. Wanneer de bijgewerkte PDF-sjabloon wordt geïmporteerd, wordt de lijst met opmaakelementen dienovereenkomstig gewijzigd:

    - Voor nieuwe velden in de bijgewerkte PDF-sjabloon worden nieuwe opmaakelementen gemaakt in de bewerkte ER-indeling.
    - Als de bijgewerkte PDF-sjabloon geen velden meer bevat die overeenkomen met bestaande opmaakelementen in de bewerkte ER-indeling, worden deze opmaakelementen uit de ER-indeling verwijderd.

18. Selecteer op het tabblad **Opmaak** de optie **Bijlagen**.

    Zoals u ziet, wordt het geïmporteerde PDF-document gekoppeld aan de bewerkte ER-indeling gekoppeld.

    ![Voorbeeld van PDF-bijlage.](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Ga door met het ontwerpen van deze indeling door de tweede PDF-sjabloon te importeren, de benodigde bindingen aan gegevensbronnen toe te voegen enzovoort.
20. Selecteer **Opslaan**.
21. Sluit de pagina.
22. Selecteer **Verwijderen**.
23. Selecteer **Ja**.

Als u wilt weten hoe nieuwe opmaakelementen **PDF-samenvoeger**, **PDF-bestand**, **Veldgroep** en **Veld** kunnen worden gebruikt voor het genereren van documenten in PDF-indeling, kunt u het voorbeeld van de ER-indeling importeren en analyseren.

### <a name="import-the-format-configuration"></a>De indelingsconfiguratie importeren

Vervolgens importeert u het voorbeeld van de ER-indeling die u eerder hebt gedownload om het rappport **Intrastat-controle** in PDF-indeling te genereren. Op de eerste pagina van het rapport moet een overzicht van het rapport worden weergegeven plus details van de buitenlandse handelstransacties waarover wordt gerapporteerd. Op de overige pagina's mogen alleen details worden weergegeven van de buitenlandse handelstransacties waarover wordt gerapporteerd.

1. Selecteer op de pagina **Configuraties** de optie **Exchange \> Laden vanuit XML-bestand**.
2. Selecteer **Bladeren**. Navigeer naar en selecteer het bestand **Intrastat report (PDF).version.1.1.xml** dat u eerder hebt gedownload als vereiste.
3. Selecteer **OK**.

## <a name="analyze-the-format-configuration"></a>De indelingsconfiguratie analyseren

### <a name="format-layout"></a>Indelingslay-out

1. Selecteer op de pagina **Configuraties** in de structuur de optie **Intrastat-model \> Intrastat-rapport (PDF)**.
2. Selecteer **Ontwerper**.
3. Selecteer **Details weergeven**.
4. Vouw in de structuur **Uitvoer: PDF-samenvoeger** uit.

    Zoals u ziet, bevat deze ER-indeling twee elementen **PDF-bestand**, die elk een andere PDF-sjabloon gebruiken. Eén sjabloon wordt gebruikt om de eerste pagina van het rapport te genereren in PDF-indeling en de andere sjabloon wordt gebruikt om de andere pagina's te genereren.

5. Vouw in de structuur **Uitvoer: PDF-samenvoeger \> Pagina 1: PDF-bestand (IntrastatReportTemplate1)** uit.
6. Vouw in de structuur **Uitvoer: PDF-samenvoeger \> Pagina N: PDF-bestand (IntrastatReportTemplate2)** uit.

    Omdat de inhoud van de twee PDF-sjablonen afwijkt, is de structuur van de geneste opmaakelementen voor de twee elementen **PDF-bestand** eveneens verschillend.

### <a name="format-mapping"></a>Indelingstoewijzing

1. Ga naar de pagina **Indelingsontwerper** en selecteer het tabblad **Toewijzing**.
2. Vouw in de structuur **Paginering \> Pagina's** uit.

    ![Pagina Formuleontwerper waarop de modelstructuur is uitgevouwen.](media/rcs-ger-filloutpdf-reviewformat.png)

    Let op de volgende details:

    - Het opmaakelement **Uitvoer \> Pagina 1** van het type **PDF-bestand** type is niet aan een gegevensbron gekoppeld en de expressie **Ingeschakeld** van dit opmaakelement is leeg. Daarom wordt tijdens de uitvoering de PDF-sjabloon **IntrastatReportTemplate1** slechts één keer ingevuld wanneer een afzonderlijk PDF-document wordt gegenereerd.
    - Het opmaakelement **Uitvoer \> Pagina N** van het type **PDF-bestand** is gekoppeld aan de gegevensbron **Paging.PageN** van het type **Recordlijst** en de expressie **Ingeschakeld** van dit opmaakelement is leeg. Daarom wordt tijdens de uitvoering de PDF-sjabloon **IntrastatReportTemplate2** ingevuld voor elke record uit de lijst met gekoppelde records wanneer een afzonderlijk PDF-document wordt gegenereerd.
    - Omdat de opmaakelementen **Pagina 1: PDF-bestand** en **Pagina N: PDF-bestand** onderliggende elementen zijn van het opmaakelement **Uitvoer: PDF-samenvoeger**, worden alle ingevulde PDF-documenten samengevoegd in een enkel PDF-document.
    - De gegevensbronnen **Paging.Page1** en **Paging.PageN** worden geconfigureerd als filters van records uit de gegevensbron **Paging.Pages**. Deze gegevensbron is geconfigureerd voor het opsplitsen van de gehele set buitenlandse handelstransacties in batches. Elke batch bevat maximaal 42 records. De volgende ER-expressie wordt gebruikt om de transacties op te splitsen in batches:

        SPLITLIST(Totals.CommodityRecord,42)

    - De gegevensbron **Paging.Pages** bevat het element **Paging.Pages.Enumerated** waarmee de details worden geretourneerd van elke record die is opgenomen in een batch. Deze details omvatten de volgorde van de record in de huidige batch (het veld **Paging.Pages.Enumerated.Number**). Het veld **Paging.Pages.Enumerated.Number** wordt gebruikt in de expressie **Naam** van opmaakelementen **PDF-veld** om op dynamische wijze een veldnaam te genereren op basis van het transactienummer in een batch. De veldnaam die wordt gegenereerd wordt vervolgens gebruikt om het juiste PDF-veld in te vullen in de PDF-sjabloon die wordt gebruikt.
    - Het opmaakelement **Uitvoer \> Pagina N \> Details 2** van het type **PDF-groep** is gekoppeld aan de gegevensbron **Paging. PageN.Enumerated** (of **\@.Enumerated** als de weergavemodus **Relatief pad** wordt gebruikt) van het type **Recordlijst**. Daarom worden tijdens de uitvoering de geneste elementen van deze PDF-groep ingevuld voor elke record uit de lijst met gekoppelde records. Op deze manier worden afzonderlijke PDF-regels virtueel gegenereerd als voor elk Nde van 42 records uit de lijst **Paging.PageN.Enumerated** lijst de volgende PDF-velden worden ingevuld: Datum N, Richting N, Basisproduct N enzovoort. Daarom lijkt het gedrag van dit opmaakelement **Veldgroep** op het gedrag van de opmaakelementen **XML \> Volgorde** en **Tekst \> Volgorde**.

3. Vouw in de structuur **Uitvoer \> Pagina N \> Details2** uit.
4. Selecteer in de structuur **Uitvoer \> Pagina N \> Details2 \> PageFooter**.

    Zoals u ziet, is het kenmerk **Naam** van dit opmaakelement gedefinieerd als **PageFooter**. U ziet ook dat de expressie **Naam** van het opmaakelement leeg is.

5. Selecteer in de structuur **Uitvoer \> Pagina N \> Details2 \> Correction 1**.

    Zoals u ziet, is het kenmerk **Naam** van dit opmaakelement gedefinieerd als **Correction 1**. U ziet ook dat de expressie **Naam** van het opmaakelement is gedefinieerd als **Paging.FldName("Correction",\@.Number)**.

![Indelingsontwerper waarin een toewijzing is geselecteerd.](media/rcs-ger-filloutpdf-reviewformat2.png)

Zoals u ziet, wordt het opmaakelement **Veld** gebruikt voor het invullen van een afzonderlijk veld van een invulbaar PDF-document dat is gedefinieerd als sjabloon van het bovenliggende opmaakelement **PDF-bestand**. De koppeling van het opmaakelement **PDF-bestand** of de geneste elementen hiervan, als er geneste elementen element, geeft de waarde aan die zijn ingevoerd in overeenkomstige PDF-velden. Verschillende eigenschappen van het opmaakelement **Veld** kunnen worden gebruikt om op te geven welk PDF-veld wordt gevuld door een afzonderlijk opmaakelement:

- Op het tabblad **Opmaak** is dit het kenmerk **Naam** van het opmaakelement
- Op het tabblad **Toewijzing** is dit de expressie **Naam** van het opmaakelement

Omdat beide eigenschappen optioneel zijn voor een opmaakelement **Veld**, worden de volgende regels toegepast om het doel-PDF-veld op te geven:

- Als het kenmerk **Naam** leeg is en de expressie **Naam** tijdens de uitvoering een lege tekenreeks retourneert, wordt er tijdens de uitvoering een uitzondering gegenereerd om de gebruiker te laten weten dat er geen PDF-veld is gevonden in de PDF-sjabloon die wordt gebruikt om het PDF-document in te vullen.
- Als het kenmerk **Naam** is gedefinieerd en de expressie **Naam** leeg is, wordt het PDF-veld met dezelfde naam als het kenmerk **Naam** van het opmaakelement ingevuld.
- Als het kenmerk **Naam** is gedefinieerd en de expressie **Naam** is geconfigureerd, wordt het PDF-veld met dezelfde naam de waarde die wordt geretourneerd door de expressie **Naam** van het opmaakelement ingevuld.

> [!NOTE]
> Wanneer een selectievakje in de PDF-sjabloon geen onderdeel is van een groep selectievakjes, wordt dit in de bewerkbare ER-indeling weergegeven als een **veld** element dat is genest onder het **PDF-bestandselement**. Dit type PDF-selectievakje kan op de volgende manieren worden ingesteld:
>
> - Het overeenkomstige opmaakelement **Veld** is gekoppeld aan een gegevensbronveld van het gegevenstype *[Booleaans](er-formula-supported-data-types-primitive.md#boolean)* met de waarde **Waar**.
> - Het bijbehorende opmaakelement **Veld** bevat een genest opmaakelement **Tekenreeks** dat is gekoppeld aan een gegevensbronveld met een tekstwaarde van **1**, **Waar** of **Ja**.
>
> Uw sjabloon kan een groep selectievakjes bevatten waarbij slechts één selectievakje tegelijk kan worden ingeschakeld. Deze selectievakjes worden in een PDF-sjabloon weergegeven als meerdere formuliervelden van het type *SELECTIEVAKJE*. Elk veld heeft dezelfde naam maar een andere exportwaarde. Wanneer u de sjabloon in de bewerkbare ER-indeling importeert, wordt elk selectievakje in de indelingshiërarchiestructuur weergegeven als een element **Item van groep selectievakjes** dat is genest onder hetzelfde element **Groep selectievakjes**. De naam van het element **Groep selectievakjes** komt overeen met de naam van de selectievakjes in de PDF-sjabloon. De naam van elk element **Item van groep selectievakjes** komt overeen met de exportwaarde naam van het overeenkomstige selectievakjeveld in de PDF-sjabloon.
>
> U kunt een element **Item van groep selectievakjes** alleen aan een gegevensbronveld van het *Booleaanse* gegevenstype binden.

## <a name="run-the-format-configuration"></a>De indelingsconfiguratie uitvoeren

### <a name="import-the-format-configuration"></a>De indelingsconfiguratie importeren

Vervolgens laadt u het voorbeeld van de ER-indeling **Intrastat (importeren vanuit Excel)**. Deze indeling is bedoeld voor het parseren van een door de gebruiker geselecteerde Microsoft Excel-werkmap die buitenlandse handelstransacties simuleert.

1. Selecteer op de pagina **Configuraties** de optie **Exchange \> Laden vanuit XML-bestand**.
2. Selecteer **Bladeren**. Navigeer naar en selecteer het bestand **Intrastat (import from Excel).version.1.1.xml** dat u eerder hebt gedownload als vereiste.
3. Selecteer **OK**.
4. Selecteer in de structuur **Intrastat-model \> Intrastat (importeren vanuit Excel)**.
5. Selecteer **Bewerken**.
6. Stel de optie **Standaard voor modeltoewijzing** in op **Ja**.

    > [!NOTE]
    > Als u eerder de optie **Standaard voor modeltoewijzing** had ingesteld op **Ja** voor de configuratie **Intrastat-model** of een andere configuratie die is genest onder de configuratie **Intrastat-model**, stelt u deze optie in op **Nee**.

    Wanneer de optie **Standaard voor modeltoewijzing** is ingesteld op **Ja**, wordt de ER-indeling **Intrastat (importeren vanuit Excel)** toegewezen als de standaardgegevensbron voor de configuratie van de indeling **Intrastat-rapport (PDF)**. Wanneer vervolgens de configuratie van de indeling **Intrastat-rapport (PDF)** wordt uitgevoerd, simuleert de inhoud van de Excel-werkmap die wordt geparseerd door de ER-indeling **Intrastat (importeren vanuit Excel)** buitenlandse handelstransacties waarover moet worden gerapporteerd. In de volgende afbeelding ziet u een voorbeeld van een Excel-werkmap.

    ![Excel-werkmap met voorbeeldgegevens.](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>De indelingsconfiguratie uitvoeren

1. Selecteer op de pagina **Configuraties** in de structuur de optie **Intrastat-model \> Intrastat-rapport (PDF)**.
2. Selecteer **Uitvoeren**.
3. Selecteer **Bladeren**. Navigeer naar en selecteer het bestand **Intrastat sample data.xlsx** dat u eerder hebt gedownload als vereiste.
4. Selecteer **OK**.
5. Selecteer in het veld **Rapportrichting** de optie **Beide** om alle transacties uit de geïmporteerde Excel-werkmap in te vullen in het PDF-rapport dat wordt gegenereerd.
6. Selecteer **OK**.
7. Controleer het PDF-document dat is gegenereerd.

In de volgende afbeelding ziet u een voorbeeld van de eerste pagina van het gegenereerde rapport.

![Eerste pagina van het gegenereerde rapport.](media/rcs-ger-filloutpdf-generatedreport.png)

In de volgende afbeelding ziet u een voorbeeld van een andere pagina van het gegenereerde rapport.

![Andere pagina van het gegenereerde rapport.](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="limitations"></a>Beperkingen

De namen van invulbare velden moeten uniek zijn in het PDF-formulier dat u wilt gebruiken als rapportsjabloon. Voor elk veld wordt een afzonderlijk indelingselement met de bijbehorende naam in de bewerkbare ER-indeling gemaakt bij het importeren van een PDF-formulier. Als een PDF-formulier verschillende velden met dezelfde naam bevat, wordt één indelingselement gemaakt voor de velden die niet afzonderlijk kunnen worden ingevuld tijdens runtime.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="when-i-run-the-er-format-to-generate-a-report-in-pdf-format-why-do-i-get-the-following-errors--cannot-handle-iref-streams-the-current-implementation-of-pdfsharp-cannot-handle-this-pdf-feature-introduced-with-acrobat-6-and-a-pdf-name-must-start-with-a-slash-"></a>Waarom ontvang ik de volgende fouten wanneer ik de ER-indeling uit voer om een rapport in PDF-indeling te genereren: **kan iref-stromen niet verwerken. De huidige implementatie van PDFSharp kan deze PDF-functie uit  Acrobat 6 niet verwerken.** En **een PDF-naam moet beginnen met een slash (/).**

Voor het ER-raamwerk wordt versie 1.5 van de PDFSharp-bibliotheek gebruikt om deze PDF-rapporten te genereren. Een aantal functies van PDF 1.5 (Adobe Reader 6.0) is nog niet geïmplementeerd in deze bibliotheek. Daarom kan PDFSharp nog geen bestanden openen die zijn gemarkeerd **voor PDF 1.5 of hoger**, waardoor de fouten kunnen optreden. Gebruik een van de volgende oplossingen om het probleem op te lossen:

-   Wanneer u uw eigen PDF-sjabloon gebruikt: downgrade de sjabloon naar een eerdere Adobe-versie en start met een nieuwe sjabloon in uw ER-indeling.
-   Wanneer u een ER-indelingsjabloon gebruikt die met u als onderdeel van een ER-oplossing door een andere configuratieprovider werd gedeeld: neem contact op met de eigenaar van deze ER-oplossing en geef een omschrijving van het probleem op.
-   Wanneer u de ISV-oplossing gebruikt die een eerdere versie van de PDFSharp-bibliotheek bevat, neemt u contact op met de eigenaar van de oplossing en stelt u een upgrade voor naar de nieuwere PDFSharp-versie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [ER: een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling (november 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [ER-configuraties ontwerpen om rapporten in Word-indeling te genereren](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

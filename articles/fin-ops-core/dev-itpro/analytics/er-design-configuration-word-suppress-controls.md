---
title: Besturingselementen voor Word-inhoud onderdrukken in gegenereerde rapporten
description: In dit onderwerp wordt uitgelegd hoe u een ER-indeling (elektronische rapportage) configureert om rapporten te genereren als Microsoft Word-bestanden waarin inhoudsbesturingselementen worden onderdrukt.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: f8e74902e939355aba9bbadd8e7f8f8aa46fe5c5
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323920"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Besturingselementen voor Word-inhoud onderdrukken in gegenereerde rapporten

[!include [banner](../includes/banner.md)]

Als u rapporten wilt genereren als Microsoft Word-documenten, moet u een sjabloon voor de rapporten ontwerpen als een Word-document. Deze sjabloon moet besturingselementen voor Word-inhoud bevatten als tijdelijke aanduidingen voor gegevens die tijdens runtime worden ingevuld. Als u het Word-document wilt gebruiken is gemaakt als sjabloon voor uw rapporten, kunt u een nieuwe [ER (elektronische rapportage)](general-electronic-reporting.md)-[oplossing](er-quick-start1-new-solution.md) [configureren](er-design-configuration-word.md). De oplossing moet een ER-[configuratie](general-electronic-reporting.md#Configuration) bevatten die een onderdeel voor ER-indeling bevat. Deze ER-indeling moet worden geconfigureerd om de ontworpen sjabloon te gebruiken voor het genereren van een rapport.

In versie 10.0.6 en hoger van Dynamics 365 Finance kunt u formules configureren in de ER-indeling om bepaalde besturingselementen voor Word-inhoud in gegenereerde documenten te onderdrukken.

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol Systeembeheerder of Functioneel consultant elektronische rapportage een ER-indeling kan configureren die rapporten genereert als Word-bestanden en enkele van de inhoudsbesturingselementen onderdrukt in de gegenereerde rapporten die zijn geconfigureerd met behulp van een Word-sjabloon.

Deze stappen kunnen in het GBSI-bedrijf worden uitgevoerd.

## <a name="prerequisites"></a>Vereisten

Voordat u deze stappen uitvoert, moet u eerst de stappen in de volgende taakbegeleidingen uitvoeren:

- [Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](./tasks/er-design-reports-openxml-2016-11.md)
- [ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling](./tasks/er-design-configuration-word-2016-11.md)

Wanneer u de stappen van deze taakhandleidingen voltooit, worden de volgende items voorbereid:

- Een ER-indeling voor een **voorbeeldwerkbladrapport** dat is geconfigureerd om een document te genereren in Word-indeling
- Een [conceptversie](general-electronic-reporting.md#component-versioning) van de ER-indeling voor een **voorbeeldwerkbladrapport** dat is gemarkeerd als **Uitvoerbaar**
- Een **elektronische** betalingsmethode die is geconfigureerd voor het gebruik van de ER-indeling voor een **voorbeeldwerkbladrapport** voor de verwerking van leverancierbetalingen

U moet ook de volgende sjabloon downloaden en opslaan voor het voorbeeldrapport:

- [Gebonden sjabloon 2 van betalingsrapport (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>De gedownloade Word-sjabloon controleren

1. Open in de Word-bureaubladtoepassing het sjabloonbestand **SampleVendPaymDocReportBounded2.docx** dat u eerder hebt gedownload.
2. Controleer of het sjabloonbestand een overzichtssectie bevat met de totale betalingsbedragen voor elke valutacode die in de verwerkte betalingen is gehanteerd.

    - De overzichtssectie bevindt zich in een afzonderlijke tabel van het Word-document.
    - De eerste rij in deze tabel bevat de kopteksten van de tabelkolommen als sectiekoptekst.
    - De tweede rij van deze tabel bevat de terugkerende inhoudsbesturingselementen als de sectiedetails.
    - Dit inhoudsbesturingselement wordt toegewezen aan het veld **SummaryLines** van het aangepaste XML-onderdeel **Rapport**.
    - Op basis van deze toewijzing is het inhoudsbesturingselement gekoppeld aan het element **SummaryLines** van de bewerkbare ER-indeling.

    > [!NOTE]
    > Het besturingselement voor terugkerende inhoud wordt gelabeld door de sleutel **SummaryLines** die overeenkomt met het veld van het aangepaste XML-onderdeel waaraan het is toegewezen.

    ![Indeling van Word-sjabloon.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>De bestaande ER-rapportconfiguratie selecteren

Voor de volgende stappen gebruikt u de bestaande ER-configuratie die u hebt geconfigureerd bij het uitvoeren van de stappen in de eerder genoemde taakbegeleidingen.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer **Rapportageconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur **Betalingsmodel** uit en selecteer **Voorbeeldwerkbladrapport**.
4. Selecteer **Ontwerper** om de conceptversie van de geselecteerde ER-indeling te bewerken.

## <a name="replace-the-current-template-with-the-new-template"></a>De huidige sjabloon vervangen door de nieuwe sjabloon

Momenteel wordt het bestand SampleVendPaymDocReportBounded.docx gebruikt als sjabloon voor het genereren van de uitvoer in Word-indeling. In de volgende stappen vervangt deze Word=sjabloon door de nieuwe Word-sjabloon, SampleVendPaymDocReportBounded2.docx, die u eerder hebt gedownload.

1. Selecteer **Bijlagen** op de pagina **Indelingsontwerper**.
2. Selecteer op de pagina **Bijlagen** de optie **Verwijderen** om de bestaande sjabloon te verwijderen.
3. Selecteer **Ja** om de verwijdering te bevestigen.
4. Selecteer **Nieuw** \> **Bestand**.
5. Selecteer **Bladeren**, blader vervolgens naar het bestand **SampleVendPaymDocReportBounded2.docx** dat u eerder hebt gedownload en selecteer dit.
6. Selecteer **OK**.
7. Sluit de pagina **Bijlagen**.
8. Typ of selecteer op de pagina **Indelingsontwerper** in het veld **Sjabloon** het bestand **SampleVendPaymDocReportBounded2.docx**.

## <a name="run-the-format-to-create-word-output"></a>De indeling uitvoeren om Word-uitvoer te maken

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer alle betalingen op de pagina **Leverancierbetalingen** op het tabblad **Lijst**.
3. Selecteer **Betalingsstatus** \> **Geen**.
4. Selecteer **Betalingen genereren**.
5. Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.
6. Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.
7. Selecteer **OK**.
8. Selecteer **OK** in het dialoogvenster **Parameters elektronisch rapport** en analyseer de gegenereerde uitvoer.

    ![Betalingen voor verwerking op de pagina Leveranciersbetalingen.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    De uitvoer wordt weergegeven in Word-indeling en bevat de overzichtssectie.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>De bewerkbare indeling configureren om de overzichtssectie te onderdrukken

Als u de overzichtssectie in een gegenereerd document wilt onderdrukken op basis van de aanvraag van een gebruiker die deze ER-indeling gebruikt, moet u de bewerkbare ER-indeling wijzigen.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage** en open de conceptversie van de ER-indeling die u wilt bewerken.
2. Selecteer **Rapportageconfiguraties**. 
3. Vouw op de pagina **Configuraties** in de configuratiestructuur **Betalingsmodel** \> **Voorbeeldwerkbladrapport** uit.
4. Selecteer **Ontwerper**.
5. Vouw op de pagina **Indelingsontwerper** **Word** uit en selecteer **SummaryLines**.
6. Voeg op het tabblad **Toewijzing** een nieuwe gegevensbron toe om de gebruiker tijdens runtime te vragen of de overzichtssectie moet worden onderdrukt:

    1. Selecteer **Basis toevoegen**.
    2. Selecteer in het dialoogvenster **Gegevensbron toevoegen** de optie **Algemeen\gebruikersinvoerparameter** om het dialoogvenster **Gegevensbroneigenschappen 'gebruikersinvoerparameter'** te openen.
    3. Voer in het veld **Naam** de tekst **uipSuppress** in.
    4. Geef in het veld **Label** de optie **Overzichtssectie onderdrukken** op.
    5. Selecteer of typ **NoYes** in het veld **Naam van gegevenstype voor bewerkingen**.
    6. Selecteer **OK**.

7. Voeg een nieuwe gegevensbron toe van het opsommingstype **NoYes**:

    1. Selecteer **Basis toevoegen**.
    2. Selecteer in het dialoogvenster **Gegevensbron toevoegen** de optie **Dynamics 365 for Operations\Opsomming** om het dialoogvenster **Gegevensbroneigenschappen 'Opsomming'** te openen.
    3. Voer in het veld **Naam** de tekst **enumNoYes** in.
    4. Geef in het veld **Label** de optie **Onderdrukkingsopties** op.
    5. Selecteer of typ **NoYes** in het veld **Naam van gegevenstype voor bewerkingen**.
    6. Selecteer **OK**.

8. Configureer voor het geselecteerde element voor de indeling **SummaryLines** de formule om op te geven wanneer het besturingselement voor Word-inhoud dat aan het geselecteerde indelingselement is gekoppeld moet worden onderdrukt:

    1. Selecteer op het tabblad **Toewijzing** in de sectie **Verwijderd** de optie **Bewerken** om de pagina **[Formuleontwerper](general-electronic-reporting-formula-designer.md)** te openen.
    2. Voer in het veld **Formule** de formule `uipSuppress = enumNoYes.Yes` in.
    3. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.

        > [!NOTE]
        > Deze formule wordt toegepast op een gegenereerd document **nadat alle andere indelingselementen zijn uitgevoerd**. Als u deze formule wilt toepassen, wordt een besturingselement voor Word-inhoud dat is gelabeld als een indelingselement waarvoor de formule is geconfigureerd (**SummaryLines** in dit geval) gevonden in een gegenereerd document. Dit inhoudsbesturingselement wordt vervolgens volledig verwijderd samen met de rij in de Word-tabel die het bevat. De detailrij van de overzichtssectie wordt uit het gegenereerde document verwijderd.
        >
        > Op het moment van ontwerpen kunt u de formule **Verwijderd** configureren voor een indelingselement, zelfs als geen inhoudsbesturingselement in de Word-sjabloon die u gebruikt een label heeft die overeenkomt met de naam van een indelingselement waarvoor de eigenschap **Verwijderd** is geconfigureerd. Wanneer u de indeling valideert tijdens het ontwerpen, ontvangt u een [waarschuwing](er-components-inspections.md#i14) over deze inconsistentie.
        >
        > Tijdens de runtime wordt een uitzondering gemaakt als geen inhoudsbesturingselement in de Word-sjabloon die u gebruikt een label heeft die overeenkomt met de naam van een indelingselement waarvoor de eigenschap **Verwijderd** is geconfigureerd.

    4. Stel op het tabblad **Toewijzing** in de sectie **Verwijderd** de optie **Met bovenliggend element** in op **Ja**.

        > [!NOTE]
        > U moet deze optie op **Ja** instellen als u de gehele Word-tabel wilt verwijderen als het bovenliggende object van de rij met de details van de overzichtssectie. Als u deze optie op **Nee** instelt, blijft de koptekstrij in het gegenereerde document staan.

9. Selecteer **Opslaan** om de wijzigingen in de bewerkbare indeling op te slaan.

    ![De gegenereerde uitvoer in Word-indeling.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>De gewijzigde indeling uitvoeren om Word-uitvoer te maken

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer het betalingsjournaal dat u hebt gemaakt en selecteer vervolgens **Regels**.
3. Selecteer op de pagina **Leverancierbetalingen** alle rijen en selecteer vervolgens **Betalingsstatus** \> **Geen**.
4. Selecteer **Betalingen genereren**.
5. Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.
6. Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.
7. Selecteer **OK**.
8. Ga naar het dialoogvenster **Parameters elektronisch rapport** en selecteer **Ja** in het veld **Overzichtssectie onderdrukken**.
9. Selecteer **OK** en analyseer de gegenereerde uitvoer.

    ![Gegenereerde uitvoer in Word-indeling.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    De uitvoer bevat niet de overzichtssectie omdat deze is onderdrukt.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](./tasks/er-design-reports-openxml-2016-11.md)
- [Een nieuwe ER-configuratie ontwerpen om rapporten in Word-indeling te genereren](er-design-configuration-word.md)
- [ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling](./tasks/er-design-configuration-word-2016-11.md)
- [Het geconfigureerde ER-onderdeel inspecteren om runtimeproblemen te voorkomen](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

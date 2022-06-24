---
title: De uitvoeringsinterface voor de werkvloer ontwerpen
description: In dit artikel wordt uitgelegd hoe u formulierbesturingselementen configureert zodat de standaardstijlen voor de uitvoering op de werkvloer worden toegepast.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ad6ecd591353fe8ddc1a5b9049d65491fb58e98a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859135"
---
# <a name="style-the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer ontwerpen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u formulierbesturingselementen configureert zodat de standaardstijlen voor de uitvoering op de werkvloer worden toegepast.

## <a name="forms-and-dialogs"></a>Formulieren en dialoogvensters

Stijlen kunnen alleen op een formulier of dialoogvenster worden toegepast als aan de volgende vereisten is voldaan:

- Als het formulier op het bestaande formulier voor voortgangsrapportage moet lijken, moet de naam van uw formulier of dialoogvenster beginnen met `JmgProductionFloorExecutionCustomInputDialog`.
- Het formulier of dialoogvenster kan een detailformuliergedeelte bevatten. Als u er stijlen op wilt toepassen, moet de naam van het detailformuliergedeelte beginnen met `JmgProductionFloorExecutionCustomDetailsDialog`.
- Als het formulier of dialoogvenster een eenvoudige weergave moet hebben, moet de naam van de eenvoudige weergave beginnen met `JmgProductionFloorExecutionCustomDialog`. Voorbeelden van formulieren met een eenvoudige weergave zijn het beginformulier en het indirecte-activiteitenformulier.
- Alle besturingselementen in het dialoogvenster moeten worden geconfigureerd zoals beschreven in dit artikel.

> [!IMPORTANT]
> Voor de functies die in de eerste twee punt van deze lijst worden genoemd, is Supply Chain Management versie 10.0.19 of hoger nodig.

Stijlen kunnen alleen op de knop **OK** in een dialoogvenster worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met `OkButtonGroup`.

Stijlen kunnen alleen op de knop **Annuleren** in een dialoogvenster worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met `CancelButtonGroup`.

### <a name="header"></a>Koptekst

In de volgende afbeelding ziet u een standaardkoptekst voor een formulier of dialoogvenster.

![Standaardkoptekst voor formulier of dialoogvenster.](media/pfe-styles-header.png "Standaardkoptekst voor formulier of dialoogvenster")

In Visual Studio worden kopteksten gemaakt met een structuur zoals in de onderstaande afbeelding wordt weergegeven.

![Standaardcodestructuur voor het maken van een koptekst.](media/pfe-styles-header-code-structure.png "Standaardcodestructuur voor het maken van een koptekst")

Als u tekst wilt toevoegen aan uw koptekst, gebruikt u code zoals in het volgende voorbeeld.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Wanneer u uw koptekstcode schrijft, past u de volgende regels toe:

- De naam van de hoofdgroep moet `TableRowHeaderGroup` zijn.
- Elk tekstblok (gescheiden door opsommingstekens) moet beginnen met `HeaderFieldWithSeparatorText`.
- De laatste tekstnaam moet beginnen met `HeaderFieldText`.
- `CaptionImage` kan worden overgeslagen.

### <a name="progress-indicator"></a>Voortgangsindicator

U kunt een voortgangsindicator opnemen, die rechts van de koptekst wordt weergegeven. De volgende afbeelding toont een voortgangsindicator.

![Standaard voortgangsindicator.](media/pfe-styles-header-progress.png "Standaard voortgangsindicator")

Het tekstveld moet de naam `ShowProgress` hebben om de voortgangsindicator weer te geven.

## <a name="grid"></a>Raster

Stijlen worden automatisch toegepast. Er is geen specifieke configuratie vereist.

Het raster moet een `TabularView`-stijl hebben en de methode `run()` in het aangepaste formulier moet worden overschreven, omdat een nieuw raster nog niet wordt ondersteund. Voeg de volgende code toe:

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Als u de gegevens in de hoofdweergave wilt vernieuwen, wilt u mogelijk iets zoals `this.parmParentForm().updateLayout();` in een `click`-methode van uw actie gebruiken. (Kijk voor een voorbeeld naar de klasse `JmgProductionFloorExecutionReportFeedbackAction`.) Zorg ervoor dat `parmDataSource` is ingesteld in de methode `init` van uw nieuwe formulier (`formCaller.parmDataSource(this.dataSource(1));`). Kijk voor een voorbeeld naar het formulier `JmgProductionFloorExecutionMainGrid`.

## <a name="card-view"></a>Kaartweergave

Stijlen kunnen alleen op kaartweergave-besturingselementen worden toegepast als aan de volgende vereisten is voldaan:

- Elke kaartweergave is opgenomen in een formuliergroep.
- De groepsnaam begint met `CardGroup` (bijvoorbeeld `CardGroupJobsView`).

De volgende afbeelding toont een kaartweergave zonder besturingselementen.

![Kaartweergave zonder elementen.](media/pfe-styles-empty-card.png)

De volgende afbeeldingen tonen kaartweergaven mét besturingselementen.

![Kaart met elementen die Hz tonen.](media/pfe-styles-elements.png)

![Kaart met elementen voor een onderhoudsverzoek.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Visitekaartje

Stijlen kunnen alleen op besturingselementen voor visitekaartjes worden toegepast als aan de volgende vereisten is voldaan:

- Elk visitekaartje is opgenomen in een formuliergroep.
- De groepsnaam begint met `BusinessCardGroup` (bijvoorbeeld `BusinessCardGroupJobsList`).

Stel de volgende eigenschappen in op het visitekaartje:

- **Stijl**: *list*
- **Uitgebreide stijl:** *cardList*
- **Meerdere selecties:** *Nee*
- **Kolomlabels weergeven:** *Nee*

![Visitekaartje.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Keuzerondje

Stijlen kunnen alleen op keuzerondjes worden toegepast als aan de volgende vereisten is voldaan:

- Elk keuzerondje is opgenomen in een formuliergroep.
- De groepsnaam begint met `RadioTextBelow` of `RadioTextRight`, afhankelijk van waar u de tekst wilt laten verschijnen.

Stel de volgende eigenschappen voor het keuzerondje:

- **Wisselknop:** *Check*
- **Wisselknopwaarde:** *Aan* als het keuzerondje moet zijn geselecteerd en anders *Uit*

In de volgende afbeelding ziet u een voorbeeld waar de tekst onder de keuzerondjes verschijnt.

![Keuzerondjes met tekst eronder.](media/pfe-styles-radio-text-below.png)

In de volgende afbeelding ziet u een voorbeeld waar de tekst rechts van de keuzerondjes verschijnt.

![Keuzerondjes met tekst rechts.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Keuzerondjes in Internet Explorer

Stijlen voor keuzerondjes worden niet ondersteund in Internet Explorer. In de volgende afbeelding ziet u hoe keuzerondjes eruitzien in Internet Explorer.

![Keuzerondjes in Internet Explorer.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Knopen

Stijlen kunnen alleen op knoppen worden toegepast als aan de volgende vereisten is voldaan:

- Elk groep knoppen is opgenomen in een formuliergroep. Alle knoppen in de groep hebben dezelfde stijl.
- Er zijn geen vereisten voor de naam van de groep.

Stel de volgende eigenschappen voor de knoppen:

- **Knopweergave:** *TextWithImageLeft*
- **Normale afbeelding:** deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld *KoffieScript*.
- **Tekst:** deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld *Start pauze*.
- **Breedte:** *Auto* of *SizeToContent*
- **Hoogte:** *Auto* of *SizeToContent*

### <a name="primary-button"></a>Primaire knop

Stijlen kunnen alleen op een primaire knop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met `DefaultButtonGroup` of `PrimaryButtonGroup` (bijvoorbeeld `DefaultButtonGroup10`).

![Primaire knop.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Secundaire knop

Stijlen kunnen alleen op een secundaire knop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groep heeft de naam **Rechterpaneel** of de groepsnaam begint met `SecondaryButtonGroup`.

![Secundaire knop.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Derde-groepsknop

Stijlen kunnen alleen op een derde-groepsknop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groep heeft de naam **Linkerpaneel** of de groepsnaam begint met `ThirdButtonGroup`.

![Derde-groepsknop.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Vierde-groepsknop

Stijlen kunnen alleen op een vierde-groepsknop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met `FourthButtonGroup`.

Stel de volgende eigenschappen voor de knop:

- **Knopweergave:** *TextOnly*.
- **Normale afbeelding:** deze eigenschap moet leeg zijn.
- **Tekst:** deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld *Weergeven* of *Bewerken*.
- **Breedte:** *Auto*
- **Hoogte:** *Auto*

![Vierde-groepsknop.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Platte knop

Stijlen kunnen alleen op een platte knop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met `FlatButtonGroup`.

Stel de volgende eigenschappen voor de knop:

- **Knopweergave:** *ImageOnly*
- **Normale afbeelding:** deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld *KoffieScript*.
- **Tekst:** deze eigenschap moet leeg zijn.
- **Breedte:** *Auto* of *SizeToContent*
- **Hoogte:** *Auto* of *SizeToContent*

![Platte knop.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Knop Doorgaan

Stijlen kunnen alleen op de knop Doorgaan worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met `ContinueButtonGroup`.

Stel de volgende eigenschappen voor de knop:

- **Knopweergave:** *ImageOnly*
- **Normale afbeelding:** *Forward*
- **Tekst:** deze eigenschap moet leeg zijn.
- **Breedte:** *Auto* of *SizeToContent*
- **Hoogte:** *Auto* of *SizeToContent*

![Knop Doorgaan.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Keuzelijst met invoervak

Een keuzelijst met invoervak is een combinatie van drie besturingselementen: een invoervak, een knop waarmee het invoervak wordt gewist en een knop waarmee een zoekopdracht wordt uitgevoerd.

Stijlen kunnen alleen op keuzelijst met invoervak worden toegepast als aan de volgende vereisten is voldaan:

- De keuzelijst met invoervak is opgenomen in een formuliergroep.
- De groepsnaam begint met `Combobox`.
- Binnen de groep is het eerste besturingselement een `AxFormStringControl`-besturingselement. Dit besturingselement geeft de huidige waarde weer en hier voert de gebruiker de vereiste waarde in.
- Het tweede besturingselement is een `CommonButton`-besturingselement en de naam daarvan begint met `ClearButton`. Deze knop moet code bevatten waarin de eigenschap `enable` wordt gebruikt om de knop weer te geven of te verbergen. Als u bijvoorbeeld de knop **Clear** (Wissen) wilt weergeven of verbergen terwijl de gebruiker informatie typt in het invoervak, kunt u de volgende code gebruiken.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    U moet één methode hebben waarmee de gegevens worden ingesteld in het invoervak. Schakel in die methode de knop **Clear** in. Hier volgt een voorbeeld.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Gebruik de volgende code voor de methode `clicked` van de knop **Wissen**.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Stel de waarde van het invoerbesturingselement `AxFormStringControl` in wanneer het formulier wordt geïnitialiseerd met de methode `init`. Als de waarde niet leeg is, schakelt u de knop **Clear** (Wissen) in. Als de waarde leeg is, schakelt u de knop **Clear** uit.

- Het derde besturingselement is een `CommonButton`-besturingselement en de naam daarvan begint met `SearchButton`.

In de volgende afbeelding ziet u twee keuzelijst met invoervak-besturingselementen. De keuzelijst met invoervak links heeft een leeg tekstvak en de knop **Clear** is uitgeschakeld. De keuzelijst met invoervak rechts bevat tekst in het tekstvak en de knop **Clear** is ingeschakeld.

![Keuzelijsten met invoervak met en zonder de knop Clear.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Snelfilter

Met het snelfilterbesturingselement wordt een zoekveld aan de pagina toegevoegd. U kunt stijlen op een snelfilter toepassen als aan de volgende vereisten wordt voldaan:

- De snelfilter is opgenomen in een formuliergroep.
- De groepsnaam begint met `SearchInputGroup`.
- Binnen de groep is het eerste besturingselement een `QuickFilter`-besturingselement. (Hier voert de gebruiker de zoekreeks in.)
- Het tweede besturingselement is `FormStaticTextControl` met de naam `NumberOfResults`. (Dit besturingselement is optioneel. Als het is opgenomen, wordt het aantal gevonden items weergegeven.)
- Het derde besturingselement is een `CommonButton`-besturingselement en de naam daarvan begint met `ClearButton`.

In de volgende afbeelding ziet u twee snelfilterbesturingselementen. Het snelfilter aan de linkerkant heeft een leeg snelfilter en het aantal resultaten is niet zichtbaar. Het snelfilter aan de rechterkant bevat een zoekreeks en geeft het aantal resultaten weer.

![Voorbeelden van een snel filterbesturingselement met en zonder zoekreeks.](media/pfe-styles-quick-filter.png "Voorbeelden van een snelfilterbesturingselement met en zonder zoekreeks.")

## <a name="center-align-elements-on-a-tab"></a>Elementen op een tabblad in het midden uitlijnen

Als u elementen in het midden van een tabblad wilt uitlijnen, moet de groepsnaam beginnen met `TabContentGroup` en moet de groep de volgende eigenschappen hebben:

- **Breedtemodus:** `SizeToAvailable`
- **Hoogtemodus:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Een raster, detailgedeelte en snelfilter uitlijnen

Als u een aangepast raster, detailgedeelte en snelfilter zo wilt rangschikken dat deze op het standaardontwerp lijken, houdt u de volgende punten in gedachten wanneer u ze allemaal bij elkaar plaatst:

- Als het raster een snelfilter heeft, moeten zowel het raster als het snelfilter binnen de groep staan met een naam die begint met `GridGroup`.
- Als u stijlen wilt toepassen op een detailgedeelte, moet de groepsnaam beginnen met `DetailInformationGroup`.

De onderstaande afbeelding toont een standaardraster met een snelfilter en een detailgedeelte aan de rechterkant.

![Standaardraster dat een snelfilter en een detailgedeelte bevat](media/pfe-styles-align-grid.png "Standaardraster dat een snelfilter en een detailgedeelte bevat")

In Visual Studio kunnen een raster, detailgedeelte en snelfilter worden gemaakt met een structuur zoals in de onderstaande afbeelding wordt weergegeven.

![Standaardcodestructuur waarmee een raster, detailgedeelte en snelfilter worden uitgelijnd.](media/pfe-styles-header-code-structure2.png "Standaardcodestructuur waarmee een raster, detailgedeelte en snelfilter worden uitgelijnd")

## <a name="additional-resources"></a>Aanvullende bronnen

- [De uitvoeringsinterface voor de productievloer aanpassen](production-floor-execution-customize.md)
- [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

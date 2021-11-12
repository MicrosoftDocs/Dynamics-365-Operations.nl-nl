---
title: De uitvoeringsinterface voor de werkvloer vormgeven
description: In dit onderwerp wordt uitgelegd hoe u formulierbesturingselementen configureert zodat de standaardstijlen voor de uitvoering op de werkvloer worden toegepast.
author: johanhoffmann
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 32e49458f6ea7c484bc4200e414d930381b31891
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651961"
---
# <a name="style-the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer vormgeven

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u formulierbesturingselementen configureert zodat de standaardstijlen voor de uitvoering op de werkvloer worden toegepast.

## <a name="forms-and-dialogs"></a>Formulieren en dialoogvensters

Stijlen kunnen alleen op een formulier of dialoogvenster worden toegepast als aan de volgende vereisten is voldaan:

- Als het formulier op het bestaande formulier voor rapportage van de voortgang moet lijken, moet de naam van uw formulier of dialoogvenster beginnen met **JmgProductionFloorExecutionCustomInputDialog**.
- Het formulier of dialoogvenster kan een detailformuliergedeelte bevatten. Als u hierop de stijlen wilt toepassen, moet de naam van het detailformuliergedeelte beginnen met **JmgProductionFloorExecutionCustomDetailsDialog**.
- Als het formulier of dialoogvenster een eenvoudige weergave moet hebben, moet de naam van de eenvoudige weergave beginnen met **JmgProductionFloorExecutionCustomDialog**. Voorbeelden van formulieren met een eenvoudige weergave zijn het beginformulier en het indirecte-activiteitenformulier.
- Alle besturingselementen in het dialoogvenster moeten zo worden geconfigureerd als beschreven in dit onderwerp.

> [!IMPORTANT]
> Voor de functies die in de eerste twee punt van deze lijst worden genoemd, is Supply Chain Management versie 10.0.19 of hoger nodig.

Stijlen kunnen alleen op de knop **OK** in een dialoogvenster worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met **OkButtonGroup**.

Stijlen kunnen alleen op de knop **Annuleren** in een dialoogvenster worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met **CancelButtonGroup**.

## <a name="grid"></a>Raster

Stijlen worden automatisch toegepast. Er is geen specifieke configuratie vereist.

## <a name="card-view"></a>Kaartweergave

Stijlen kunnen alleen op kaartweergave-besturingselementen worden toegepast als aan de volgende vereisten is voldaan:

- Elke kaartweergave is opgenomen in een formuliergroep.
- De groepsnaam begint met **CardGroup** (bijvoorbeeld **CardGroupJobsView**).

De volgende afbeelding toont een kaartweergave zonder besturingselementen.

![Kaartweergave zonder elementen.](media/pfe-styles-empty-card.png)

De volgende afbeeldingen tonen kaartweergaven mét besturingselementen.

![Kaart met elementen die Hz tonen.](media/pfe-styles-elements.png)

![Kaart met elementen voor een onderhoudsverzoek.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Visitekaartje

Stijlen kunnen alleen op besturingselementen voor visitekaartjes worden toegepast als aan de volgende vereisten is voldaan:

- Elk visitekaartje is opgenomen in een formuliergroep.
- De groepsnaam begint met **BusinessCardGroup** (bijvoorbeeld **BusinessCardGroupJobsList**).

Stel de volgende eigenschappen in op het visitekaartje:

- **Stijl**: **list**
- **Uitgebreide stijl**: **cardList**
- **Meerdere selecties**: **Nee**
- **Kolomlabels weergeven**: **Nee**

![Visitekaartje.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Keuzerondje

Stijlen kunnen alleen op keuzerondjes worden toegepast als aan de volgende vereisten is voldaan:

- Elk keuzerondje is opgenomen in een formuliergroep.
- De groepsnaam begint met **RadioTextBelow** of **RadioTextRight**, afhankelijk van waar u de tekst wilt laten verschijnen.

Stel de volgende eigenschappen voor het keuzerondje:

- **Wisselknop**: **Check**
- **Wisselknopwaarde**: **Aan** als de radioknop moet zijn geselecteerd en anders **Uit**.

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

- **Knopweergave**: **TextWithImageLeft**.
- **Normale afbeelding**: Deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld **KoffieScript**.
- **Tekst**: Deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld **Start pauze**.
- **Breedte**: **Automatisch**.
- **Hoogte**: **Automatisch**.

### <a name="primary-button"></a>Primaire knop

Stijlen kunnen alleen op een primaire knop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met **DefaultButtonGroup** of **PrimaryButtonGroup** (bijvoorbeeld **DefaultButtonGroup10**).

![Primaire knop.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Secundaire knop

Stijlen kunnen alleen op een secundaire knop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groep heeft de naam **Rechterpaneel** of de groepsnaam begint met **SecondaryButtonGroup**.

![Secundaire knop.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Derde-groepsknop

Stijlen kunnen alleen op een derde-groepsknop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groep heeft de naam **Linkerpaneel** of de groepsnaam begint met **ThirdButtonGroup**.

![Derde-groepsknop.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Vierde-groepsknop

Stijlen kunnen alleen op een vierde-groepsknop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met **FourthButtonGroup**.

Stel de volgende eigenschappen voor de knop:

- **Knopweergave**: **TextOnly**.
- **Normale afbeelding**: Deze eigenschap moet leeg zijn.
- **Tekst**: Deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld **Weergeven** of **Bewerken**.
- **Breedte**: **Automatisch**.
- **Hoogte**: **Automatisch**.

![Vierde-groepsknop.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Platte knop

Stijlen kunnen alleen op een platte knop worden toegepast als aan de volgende vereisten is voldaan:

- De knop is opgenomen in een formuliergroep.
- De groepsnaam begint met **FlatButtonGroup**.

Stel de volgende eigenschappen voor de knop:

- **Knopweergave**: **ImageOnly**.
- **Normale afbeelding**: Deze eigenschap mag niet leeg zijn. Gebruik bijvoorbeeld **KoffieScript**.
- **Tekst**: Deze eigenschap moet leeg zijn.
- **Breedte**: **Automatisch**.
- **Hoogte**: **Automatisch**.

![Platte knop.](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a>Keuzelijst met invoervak

Een keuzelijst met invoervak is een combinatie van drie besturingselementen: een invoervak, een knop waarmee het invoervak wordt gewist en een knop waarmee een zoekopdracht wordt uitgevoerd.

Stijlen kunnen alleen op keuzelijst met invoervak worden toegepast als aan de volgende vereisten is voldaan:

- De keuzelijst met invoervak is opgenomen in een formuliergroep.
- De groepsnaam begint met **Combobox**.
- Binnen de groep is het eerste besturingselement een **AxFormStringControl**-besturingselement. Dit besturingselement geeft de huidige waarde weer en hier voert de gebruiker de vereiste waarde in.
- Het tweede besturingselement is een **CommonButton**-besturingselement en de naam daarvan begint met **ClearButton**. Deze knop moet code bevatten die de eigenschap **enable** gebruikt om de knop weer te geven of te verbergen. Als u bijvoorbeeld de knop **Clear** (Wissen) wilt weergeven of verbergen terwijl de gebruiker informatie typt in het invoervak, kunt u de volgende code gebruiken.

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

    Gebruik de volgende code voor de methode **clicked** van de knop **Clear**.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Stel de waarde van het invoervak **AxFormStringControl** in wanneer het formulier wordt geïnitialiseerd met de methode **init**. Als de waarde niet leeg is, schakelt u de knop **Clear** (Wissen) in. Als de waarde leeg is, schakelt u de knop **Clear** uit.

- Het derde besturingselement is een **CommonButton**-besturingselement en de naam daarvan begint met **SearchButton**.

In de volgende afbeelding ziet u twee keuzelijst met invoervak-besturingselementen. De keuzelijst met invoervak links heeft een leeg tekstvak en de knop **Clear** is uitgeschakeld. De keuzelijst met invoervak rechts bevat tekst in het tekstvak en de knop **Clear** is ingeschakeld.

![Keuzelijsten met invoervak met en zonder de knop Clear.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Snelfilter

Met het snelfilterbesturingselement wordt een zoekveld aan de pagina toegevoegd. U kunt stijlen op een snelfilter toepassen als aan de volgende vereisten wordt voldaan:

- De snelfilter is opgenomen in een formuliergroep.
- De groepsnaam begint met **SearchInputGroup**.
- Binnen de groep is het eerste besturingselement een **QuickFilter**-besturingselement. (Hier voert de gebruiker de zoekreeks in.)
- Het tweede besturingselement is een **FormStaticTextControl** met de naam **NumberOfResults**. (Dit is optioneel en geeft het aantal gevonden items weer, indien opgenomen.)
- Het derde besturingselement is een **CommonButton**-besturingselement met een naam die begint met **ClearButton**.

In de volgende afbeelding ziet u twee snelfilterbesturingselementen. Het snelfilter aan de linkerkant heeft een leeg snelfilter en het aantal resultaten is niet zichtbaar. Het snelfilter aan de rechterkant bevat een zoekreeks en geeft het aantal resultaten weer.

![Voorbeelden van een snel filterbesturingselement met en zonder zoekreeks.](media/pfe-styles-quick-filter.png "Voorbeelden van een snelfilterbesturingselement met en zonder zoekreeks.")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

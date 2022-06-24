---
title: De uitvoeringsinterface voor de productievloer aanpassen
description: In dit artikel wordt uitgelegd hoe u huidige formulieren kunt uitbreiden of nieuwe formulieren en knoppen kunt maken voor de uitvoeringsinterface voor de productievloer.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 13fa6c2f3c30a820585d1b5a758f57ec563664d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845977"
---
# <a name="customize-the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de productievloer aanpassen

[!include [banner](../includes/banner.md)]

Ontwikkelaars kunnen huidige formulieren uitbreiden of hun eigen formulieren en knoppen maken voor de uitvoeringsinterface voor de productievloer. Nadat u de code voor deze nieuwe elementen hebt toegevoegd, kunnen beheerders of werkvloermanagers deze eenvoudig aan de interface toevoegen met de standaard configuratiebesturingselementen.

Hier vindt u bijvoorbeeld enkele mogelijke oplossingen als er nieuwe kolommen in een hoofdformulier nodig zijn:

- Breid het formulier `JmgProductionFloorExecutionMainGrid` uit en voeg de gewenste velden toe.
- Maak een nieuw formulier en voeg het toe als een nieuwe hoofdweergave (tabblad).

## <a name="add-a-new-button-action"></a>Een nieuwe knop toevoegen (actie)

Als u een nieuwe knop (actie) wilt toevoegen, voert u de volgende stappen uit om een klasse te maken waarmee uw aangepaste actie wordt geïmplementeerd.

1. Maak een nieuwe klasse met de naam `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, waarin het volgende geldt:

    - `<ExtensionPrefix>` is een unieke identificatie van uw oplossing, meestal wordt uw bedrijfsnaam gebruikt.
    - `<ActionName>` is een unieke naam voor de klasse. Hiermee wordt meestal het soort actie aangegeven.

1. De nieuwe klasse moet de klasse `JmgProductionFloorExecutionAction` uitbreiden.
1. Alle vereiste methoden overschrijven.

Kijk voor voorbeelden naar de code voor de volgende klassen:

- `JmgProductionFloorExecutionBreakAction`: een klasse voor een eenvoudige actie die geen records nodig heeft.
- `JmgProductionFloorExecutionReportFeedbackAction`: een klasse die complexere functionaliteit biedt.

Wanneer u klaar bent, wordt de nieuwe knop (actie) automatisch weergegeven op de pagina **Tabbladen ontwerpen** in Microsoft Dynamics 365 Supply Chain Management. U (of een beheerder of werkvloermanager) kunt de knop eenvoudig toevoegen aan de primaire of secundaire werkbalk, net zoals u de standaardknoppen kunt toevoegen. Zie [Uitvoeringsinterface voor de productievloer ontwerpen](production-floor-execution-tabs.md) voor instructies.

## <a name="add-a-new-main-view"></a>Een nieuwe hoofdweergave toevoegen

1. Maak een nieuw formulier met de gewenste elementen en functionaliteit. Houd er rekening mee dat dit formulier een nieuw formulier is en geen extensie. Geef het formulier de naam `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, waarbij het volgende geldt:

    - `<ExtensionPrefix>` is een unieke identificatie van uw oplossing, meestal wordt uw bedrijfsnaam gebruikt.
    - `<FormName>` is een unieke naam voor het formulier.

1. Maak een menuopdracht met de naam `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Maak een extensie met de naam `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, waarbij de methode `getMainMenuItemsList` wordt uitgebreid door de nieuwe menuopdracht aan de lijst toe te voegen. De volgende code laat een voorbeeld zien.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Wanneer u klaar bent, wordt de nieuwe hoofdweergave automatisch weergegeven in de keuzelijst met invoervak **Hoofdweergave** op de pagina **Tabbladen ontwerpen** in Supply Chain Management. Daar kunt u (of een beheerder of werkvloermanager) de hoofdweergave eenvoudig toevoegen aan nieuwe of bestaande tabbladen, net zoals u de standaardhoofdweergaven kunt toevoegen. Zie [Uitvoeringsinterface voor de productievloer ontwerpen](production-floor-execution-tabs.md) voor instructies.

## <a name="add-a-details-view"></a>Een detailweergave toevoegen

1. Maak een nieuw formulier met de gewenste elementen en functionaliteit. Houd er rekening mee dat dit formulier een nieuw formulier is en geen extensie. Geef het formulier de naam `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, waarbij het volgende geldt: 

    - `<ExtensionPrefix>` is een unieke identificatie van uw oplossing, meestal wordt uw bedrijfsnaam gebruikt.
    - `<FormName>` is een unieke naam voor het formulier.

1. Maak een menuopdracht met de naam `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Maak een extensie met de naam `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, waarbij de methode `getDetailsMenuItemList` wordt uitgebreid door de nieuwe menuopdracht aan de lijst toe te voegen.

Wanneer u klaar bent, wordt de nieuwe detailweergave automatisch weergegeven in de keuzelijst met invoervak **Detailweergave** op de pagina **Tabbladen ontwerpen** in Supply Chain Management. Daar kunt u (of een beheerder of werkvloermanager) de detailweergave eenvoudig toevoegen aan nieuwe of bestaande tabbladen, net zoals u de standaarddetailweergaven kunt toevoegen. Zie [Uitvoeringsinterface voor de productievloer ontwerpen](production-floor-execution-tabs.md) voor instructies.

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Een numeriek toetsenblok aan een formulier of dialoogvenster toevoegen

In het volgende voorbeeld ziet u hoe u numerieke toetsenblokken aan een formulier toevoegt.

1. Het aantal numerieke toetsenblokcontrollers dat elk formulier bevat, moet gelijk zijn aan het aantal numerieke toetsenblokken in dat formulier.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Stel het gedrag in van elke numerieke toetsenblokcontroller en koppel elke numerieke toetsenblokcontroller aan een formuliergedeelte voor een numeriek toetsenblok.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Een numeriek toetsenblok gebruiken als pop-upvenster

In het volgende voorbeeld ziet u een manier om een numerieke toetsenblokcontroller in te stellen voor een pop-upvenster.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

In het volgende voorbeeld ziet u een manier om het pop-upvenster voor het numerieke toetsenblok aan te roepen.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Datum- en tijdbesturingselementen toevoegen aan een formulier of dialoogvenster

In deze sectie wordt aangegeven hoe u datum- en tijdbesturingselementen aan een formulier of dialoogvenster toevoegt. Met de datum- en tijdbesturingselementen met aanraakfunctie kunnen werknemers eenvoudig datums en tijden opgeven. In de volgende schermopnamen wordt weergegeven hoe de besturingselementen meestal op de pagina worden weergegeven. Het tijdbesturingselement is beschikbaar voor 12 uur en 24 uur. In de weergegeven versie wordt de ingestelde voorkeur voor het gebruikersaccount toegepast waaronder de interface wordt uitgevoerd.

![Voorbeeld van datumbesturingselement.](media/pfe-customize-date-control.png "Voorbeeld van datumbesturingselement")

![Voorbeeld van tijdbesturingselement met 12-uursklok.](media/pfe-customize-time-control-12h.png "Voorbeeld van tijdbesturingselement met 12-uursklok")

![Voorbeeld van tijdbesturingselement met 24-uursklok.](media/pfe-customize-time-control-24h.png "Voorbeeld van tijdbesturingselement met 24-uursklok")

In de volgende procedure wordt een voorbeeld gegeven voor het toevoegen van datum- en tijdbesturingselementen aan een formulier.

1. Voeg een controller toe aan het formulier voor elk datum- en tijdbesturingselement dat het formulier moet bevatten. (Het aantal controllers moet gelijk zijn aan het aantal datum- en tijdbesturingselementen in het formulier.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Declareer de vereiste variabelen (van het type `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Maak methoden waar de datum/tijd wordt bijgewerkt door de datetime-controllers. In het volgende voorbeeld ziet u deze methode.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Stel het gedrag in van elke datum/tijd-controller en koppel elke controller aan een formuliergedeelte. In het volgende voorbeeld ziet u hoe gegevens voor besturingselementen voor begindatum en begintijd worden ingesteld. U kunt vergelijkbare code toevoegen voor besturingselementen voor datum en tijd (niet weergegeven).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Als u alleen een datumbesturingselement nodig hebt, kunt u de instellingen voor het tijdbesturingselement overslaan en in plaats daarvan het datumbesturingselement instellen zoals in het volgende voorbeeld:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Aanvullende bronnen

- [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-styles.md)
- [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-tabs.md)

---
title: De uitvoeringsinterface voor de productievloer aanpassen
description: In dit onderwerp wordt uitgelegd hoe u huidige formulieren kunt uitbreiden of nieuwe formulieren en knoppen kunt maken voor de uitvoeringsinterface voor de productievloer.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790964"
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
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
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

## <a name="additional-resources"></a>Aanvullende bronnen

- [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-styles.md)
- [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-tabs.md)

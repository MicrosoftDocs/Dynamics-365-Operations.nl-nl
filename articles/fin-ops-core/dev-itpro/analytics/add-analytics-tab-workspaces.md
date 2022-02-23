---
title: Analyses aan werkgebieden toevoegen met Power BI Embedded
description: In dit onderwerp wordt beschreven hoe u een Power BI-rapport insluit op het tabblad Analyses van een werkgebied.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 53c9d6343422f64aed74ce436bafd2c8b2ce1c3e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680931"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Analyses aan werkgebieden toevoegen met Power BI Embedded

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Deze functie wordt ondersteund in Finance and Operations (versie 7.2 en hoger).

## <a name="introduction"></a>Introductie
In dit onderwerp wordt beschreven hoe u een Microsoft Power BI-rapport insluit op het tabblad **Analyses** van een werkgebied. In het hier gebruikte voorbeeld wordt het werkgebied **Reserveringenbeheer** in de toepassing Wagenparkbeheer uitgebreid om een analytisch werkgebied in te sluiten in het tabblad **Analyses**.

## <a name="prerequisites"></a>Vereisten
+ Open een ontwikkelaaromgeving waarop Platformupdate 8 of hoger wordt uitgevoerd.
+ Een analyserapport (.pbix-bestand) dat is gemaakt met Microsoft Power BI Desktop-bureaublad en dat een gegevensmodel bevat dat de entiteitsopslagdatabase als bron heeft.

## <a name="overview"></a>Overzicht
Of u een bestaand werkgebied van de toepassing uitbreidt of een nieuw werkgebied introduceert, u kunt in beide de ingesloten analytische weergaven gebruiken om begrijpelijke en interactieve weergaven van uw zakelijke gegevens te maken. Het proces voor het toevoegen van een analytisch werkgebiedtabblad bestaat uit vier stappen.

1. Een .pbix-bestand toevoegen als een Dynamics 365-resource.
2. Een tabblad voor het analytische werkgebied definiëren.
3. De .pbix-resource op het werkgebiedtabblad insluiten.
4. Optioneel: voeg extensies toe om de weergave aan te passen.

> [!NOTE]
> Meer informatie over het maken van analytische rapporten vindt u in [Aan de slag met Power BI Desktop-bureaublad](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). Deze pagina bevat veel inzichten waarmee u aantrekkelijke analytische rapportoplossingen kunt maken.

## <a name="add-a-pbix-file-as-a-resource"></a>Een .pbix-bestand toevoegen als een resource
Voordat u begint, moet u het Power BI-rapport dat u in het werkgebied wilt insluiten, maken of ophalen. Meer informatie over het maken van analytische rapporten vindt u in [Aan de slag met Power BI Desktop-bureaublad](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).

Volg deze stappen om een .pbix-bestand toe te voegen als een Visual Studio-projectartefact.

1. Maak een nieuw project in het juiste model.
2. Selecteer het project in Solution Explorer, klik met de rechtermuisknop en selecteer **Toevoegen** \> **Nieuw artikel**.
3. Selecteer in het dialoogvenster **Nieuw artikel toevoegen** onder **Operations-artefacten** de sjabloon **Resource**.
4. Voer een naam in die wordt gebruikt als referentie voor het rapport in X ++-metagegevens en klik vervolgens op **Toevoegen**.

    ![Dialoogvenster Nieuw artikel toevoegen](media/analytical-workspace-add.png)

5. Zoek het .pbix-bestand dat de definitie van het analytische rapport bevat en klik op **Openen**.

    ![Het dialoogvenster met een bronbestand selecteren](media/analytical-workspace-select-resource.png)

Nu u het .pbix-bestand hebt toegevoegd als een Dynamics 365-resource, kunt u rapporten insluiten in werkgebieden en rechtstreekse koppelingen toevoegen via menuopties.

## <a name="add-a-tab-control-to-an-application-workspace"></a>Een tabbesturingselement toevoegen aan een toepassingswerkgebied
In dit voorbeeld breiden we het werkgebied **Reserveringsbeheer** in het model Wagenparkbeheer uit door het toevoegen van het tabblad **Analyses** aan de definitie van het formulier **FMClerkWorkspace**.

In de volgende afbeelding ziet u hoe het formulier **FMClerkWorkspace** eruit ziet in de ontwerper in Microsoft Visual Studio.

![Formulier FMClerkWorkspace voor het wijzigen](media/analytical-workspace-definition-before.png)

Volg deze stappen om de formulierdefinitie voor het werkgebied **Reserveringsbeheer** uit te breiden.

1. Open de formulierontwerper om de ontwerpdefinitie uit te breiden.
2. Selecteer in de ontwerpdefinitie het bovenste element met de naam **Ontwerp | Patroon: Werkgebied Operationeel**.
3. Klik met de rechtermuisknop en selecteer vervolgens **Nieuw** \> **Tabblad** om een nieuw besturingselement toe te voegen met de naam **FormTabControl1**.
4. Selecteer **FormTabControl1** in de formulierontwerper.
5. Klik met de rechtermuisknop en selecteer **Nieuwe tabbladpagina** om een nieuwe tabbladpagina toe te voegen.
6. Wijzig de naam van de tabpagina in iets herkenbaars, zoals **Werkgebied**.
7. Selecteer **FormTabControl1** in de formulierontwerper.
8. Klik met de rechtermuisknop en selecteer **Nieuwe tabbladpagina**.
9. Wijzig de naam van de tabbladpagina in iets herkenbaars, zoals **Analyses**.
10. Selecteer in de formulierontwerper **Analyses (tabbladpagina)**.
11. Stel de eigenschap **Bijschrift** in op **Analyse** en stel de eigenschap **Automatische aangifte** inop **Ja**.
12. Klik met de rechtermuisknop en selecteer vervolgens **Nieuw** \> **Groep** om een besturingselement voor een nieuwe formuliergroep toe te voegen.
13. Wijzig de naam van de formuliergroepin iets herkenbaars, zoals **powerBIReportGroup**.
14. Selecteer in de formulierontwerper **PanoramaBody (tabblad)** en sleep het besturingselement naar het tabblad **Werkgebied**.
15. Selecteer in de ontwerpdefinitie het bovenste element met de naam **Ontwerp | Patroon: Werkgebied Operationeel**.
16. Klik met de rechtermuisknop en selecteer **Patroon verwijderen**.
17. Klik nogmaals met de rechtermuisknop en selecteer **Patroon toevoegen** \> **Werkgebied met tabbladen**.
18. Voer een build uit om uw wijzigingen te controleren.

In de volgende afbeelding ziet u hoe het ontwerp eruitziet nadat deze wijzigingen zijn toegepast.

![FMClerkWorkspace na wijzigingen](media/analytical-workspace-definition-after.png)

U hebt nu de besturingselementen voor het formulier toegevoegd die worden gebruikt voor het insluiten van het werkgebiedrapport. Vervolgens moet u de grootte van het bovenliggende besturingselement definiëren zodat dit geschikt is voor de lay-out. Standaard zijn de pagina **Filtervenster** en de pagina **Tabblad** zichtbaar in het rapport. U kunt echter de zichtbaarheid van deze besturingselementen wijzigen afhankelijk van de eindgebruiker van het rapport.

> [!NOTE]
> Voor ingesloten werkgebieden kunt u het beste uitbreidingen gebruiken om de pagina's **Filtervenster** en **Tabblad** te verbergen vanwege de consistentie.

U hebt nu de taak voor het uitbreiden van de formulierdefinitie van de toepassing voltooid. Voor meer informatie over het gebruik van uitbreidingen en aanpassingen zie [Aanpassen via extensies en overlayering](../extensibility/customization-overlayering-extensions.md).

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>X ++-bedrijfslogica toevoegen om een besturingselement voor weergave in te sluiten
Volg deze stappen om bedrijfslogica toe te voegen voor het initialiseren van het rapportweergave-besturingselement dat is ingesloten in het werkgebied **Reserveringsbeheer**.

1. Open de formulierontwerper **FMClerkWorkspace** om de ontwerpdefinitie uit te breiden.
2. Druk op F7 om toegang te krijgen tot de code achter de codedefinitie.
3. Voeg de volgende X++-code toe:

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Voer een build uit om uw wijzigingen te controleren.

U hebt nu de taak voltooid voor het toevoegen van bedrijfslogica voor het initialiseren van het ingesloten rapportweergave-besturingselement. In de volgende afbeelding ziet u hoe het werkgebied eruitziet nadat deze wijzigingen zijn toegepast.

![Rapport ingesloten in het werkgebied](media/analytical-workspace-final.png)

> [!NOTE]
> U kunt de bestaande operationele weergave openen met de werkgebiedtabbladen onder de paginatitel.

## <a name="reference"></a>Verwijzing

### <a name="pbireporthelperinitializereportcontrol-method"></a>Methode PBIReportHelper.initializeReportControl
Deze sectie bevat informatie over de helperklasse die wordt gebruikt om een Power BI-rapport (.pbix-resource) in te sluiten in een besturingselement voor een formuliergroep.

#### <a name="syntax"></a>Syntaxis
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>Parameters

| Naam             | Omschrijving                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| resourceName     | De naam van de .pbix-resource.                                                                              |
| formGroupControl | Het besturingselement van de formuliergroep waarop het Power BI-rapportbesturingselement wordt toegepast.                                              |
| defaultPageName  | De standaardpaginanaam.                                                                                       |
| showFilterPane   | Een Booleaanse waarde die aangeeft of het filtervenster moet worden weergegeven (**true**) of verborgen (**false**).     |
| showNavPane      | Een Booleaanse waarde die aangeeft of het navigatievenster moet worden weergegeven (**true**) of verborgen (**false**). |
| defaultFilters   | De standaardfilters voor het Power BI-rapport.                                                                 |

---
title: Sjablonen voor budgetplanning voor Excel
description: In dit onderwerp wordt beschreven hoe Microsoft Excel-sjablonen die kunnen worden gebruikt met budgetplannen maken.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Sjablonen voor budgetplanning voor Excel

In dit onderwerp wordt beschreven hoe Microsoft Excel-sjablonen die kunnen worden gebruikt met budgetplannen maken.

In dit onderwerp wordt beschreven hoe Excel-sjablonen die worden gebruikt met budgetplannen met behulp van de gegevensset standaard demo en de gebruiker Admin aanmelden. Zie voor meer informatie over het plannen van budgetten, [overzicht van de budgetplanning.](budget-planning-overview-configuration.md) U kunt ook volgen de [budgetplanning 101](budget-plan.md) zelfstudie voor de module basis configuratie en het gebruik van de beginselen.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Een werkblad met behulp van budget plan documentindeling genereren
Budget plan documenten kunnen worden weergegeven en bewerkt met behulp van een of meer indelingen. Een indeling mag hebben een gekoppeld document budgetplansjabloon weergeven en bewerken van de budgetplangegevens in een Excel-werkblad. In dit onderwerp wordt een documentsjabloon budget plan gegenereerd met behulp van een bestaande configuratie van de lay-out. Open de **budget plannen lijst** (**budgettering**&gt;**budgetplannen**). Klik op **New** voor het maken van een nieuwe budgetplandocument. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Gebruik de **Add** regel kunt u regels toevoegen. Klik op **indelingen** om het budget plan documentconfiguratie indeling weer te geven. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

U kunt de configuratie van de lay-out controleren en zo nodig aanpassen. Ga naar **sjabloon**&gt;**genereren** voor het maken van een Excel-bestand voor deze indeling. Nadat de sjabloon wordt gegenereerd, gaat u naar **sjabloon**&gt;**weergave** te openen en controleren van de documentsjabloon budget plan. U kunt het Excel-bestand naar uw lokale schijf opslaan. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> De documentindeling budget plan kan niet worden bewerkt nadat u een Excel-sjabloon is gekoppeld. De indeling wijzigen, verwijderen van het gekoppelde Excel-sjabloonbestand en deze opnieuw te genereren. Dit is noodzakelijk om de velden in de lay-out behouden en het werkblad worden gesynchroniseerd. 

De Excel-sjabloon bevat alle elementen van de documentindeling budget plan waarin de **beschikbaar in het werkblad** kolom is ingesteld op True. Overlappende elementen zijn niet toegestaan in de Excel-sjabloon. Bijvoorbeeld als de lay-out bevat aanvraag KW1 KW2 aanvraag, aanvraag K3, en aanvraag Q4 kolommen en een aanvraag voor totaalbedrag kolom een som van alle kolommen van 4 per kwartaal vertegenwoordigt, is alleen de kolommen per kwartaal of in de kolom Totaal beschikbaar in de Excel-sjabloon moet worden gebruikt. Het Excel-bestand bijwerken niet overlappende kolommen tijdens het bijwerken, omdat de gegevens in de tabel loopt een verouderd en onnauwkeurige.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Om te voorkomen van mogelijke problemen bij het weergeven en bewerken van budgetplangegevens met behulp van Excel, moet dezelfde gebruiker zijn aangemeld bij beide Dynamics 365 voor bewerkingen en de invoegtoepassing Microsoft Dynamics Office Data Connector.

## <a name="add-a-header-to-budget-plan-document-template"></a>Een koptekst toevoegen aan document budgetplansjabloon
Koptekstgegevens toevoegen, selecteert u de bovenste rij in het Excel-bestand en lege rijen invoegen. Klik op **ontwerp** in de **Data Connector** header-velden toevoegen aan het Excel-bestand.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

In de **ontwerp** tabblad ** ** Klik op **Add** velden en selecteer vervolgens **budgetPlanHeader** als de gegevensbron van de entiteit.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Plaats de cursor naar de gewenste locatie in het Excel-bestand. Klik op **label toevoegen** de veldlabel toevoegen aan de geselecteerde locatie. Selecteer **waarde toevoegen** het waardeveld toevoegen aan de geselecteerde plaats. Klik op **doen** om af te sluiten van de ontwerper.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Een berekende kolom toevoegen aan de tabel budget plan document-sjabloon
--------------------------------------------------------------

Next, berekende kolommen wordt toegevoegd aan gegenereerde budget plan documentsjabloon. A **totale aanvraag** kolom, een overzicht van de aanvraag KW1: aanvraag Q4 kolommen, en een **correctie** kolom, worden opnieuw berekend de **totale aanvraag** kolom met een vooraf gedefinieerde factor.

Klik op **ontwerp** in de **Data connector** kolommen toevoegen aan de tabel. Klik op **bewerken** naast **budgetPlanWorksheet** gegevensbron toe te voegen kolommen.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

De geselecteerde veldgroep wordt weergegeven in de kolommen die beschikbaar in de sjabloon zijn. Klik op **formule** een nieuwe kolom toevoegen. Naam voor de nieuwe kolom en plakt u de formule in de **formule** veld. Klik op **Update** de kolom in te voegen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Als u de formule definieert, de formule in het werkblad maken en te kopiëren naar de **ontwerp** venster. Een Dynamics 365 voor bewerkingen afhankelijke tabel meestal de naam 'AXTable1'. Bijvoorbeeld om samen te vatten KW1 aanvragen: aanvragen Q4 kolommen in het werkblad de formule = AxTable1\[KW1 aanvragen\]+ AxTable1\[aanvragen KW2\]+ AxTable1\[aanvragen K3\]+ AxTable1\[K4 aanvragen\].

Herhaal deze stappen om in te voegen de **correctie** kolom. Gebruik van de formule = AxTable1\[totale aanvraag\]\*$I$ 1 voor deze kolom. Zo nodig de waarde in cel I1 en vermenigvuldigt u de waarden in de **totale aanvraag** kolom voor het berekenen van correctiebedragen.

Opslaan en sluiten van het Excel-bestand. Terugkeren naar Dynamics 365 voor bewerkingen en in **indelingen**, klikt u op **sjabloon &gt;uploaden** voor het uploaden van de opgeslagen Excel-sjabloon moet worden gebruikt voor het budgetplan. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Sluit de **indelingen** schuifregelaar. In **budgetplan** -document, klikt u op **werkblad** weergeven en bewerken van het document in Excel. Houd er rekening mee dat de aangepaste Excel-sjabloon is gebruikt voor het maken van dit werkblad budgetplan en berekende kolommen worden bijgewerkt met de formules die zijn gedefinieerd in de vorige stappen. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips & trucs voor het maken van budgetplansjablonen
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Zijn er toevoegen en extra gegevensbronnen op een sjabloon voor budget plannen gebruiken?

Ja, kunt u de **ontwerp** menu Extra entiteiten toevoegen aan dezelfde of andere bladen in de Excel-sjabloon. U kunt bijvoorbeeld toevoegen de **budgetPlanProposedAsset** gegevensbron maakt en onderhoudt een lijst met voorgestelde projecten tegelijkertijd wanneer werken met budget plan gegevens in Excel. Houd er rekening mee dat met inbegrip van grote hoeveelheden gegevensbronnen mogelijk invloed op de prestaties van de Excel-werkmap. 

U kunt de **Filter** optie de **Data Connector** voor het toevoegen van de gewenste filters tot extra gegevensbronnen.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kan ik de optie ontwerp in de Data connector voor andere gebruikers verbergen?

Ja, opent u het **Data Connector** opties verbergen de **ontwerp** optie van andere gebruikers.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Vouw **Data connector opties** en schakelt u het **ontwerp schakelen** selectievakje. Dit wordt verborgen de **ontwerp** optie van de **Data connector**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kan ik voorkomen dat gebruikers per ongeluk de Data connector afsluiten tijdens het werken met gegevens?

Het is raadzaam om de vergrendeling van de sjabloon om te voorkomen dat gebruikers deze wordt gesloten. Als u de vergrendeling, klikt u op de **Data connector**, in de rechterbovenhoek een pijl wordt weergegeven. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klik op de pijl voor een extra menu. Selecteer **vergrendelen**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kan ik Excel-functies, zoals celopmaak, kleuren, voorwaardelijke opmaak en grafieken gebruiken met mijn budgetplansjablonen

Ja, werkt de meeste van de standaard Excel-capaciteiten in budgetplansjablonen. U wordt aangeraden gebruik kleurcodering voor gebruikers om te onderscheiden tussen kolommen alleen-lezen en kan worden bewerkt. Voorwaardelijke opmaak kan worden gebruikt om te markeren problematische gebieden van het budget. Kolomtotalen kunnen eenvoudig worden weergegeven met behulp van standaard Excel-formules boven de tabel.

U kunt ook maken en gebruiken van draaitabellen en diagrammen voor extra groeperingen en visualisaties van gegevens voor het projectbudget. Op de **gegevens** tabblad in het **verbindingen** groep, klikt u op **Alles vernieuwen**, en klik vervolgens op **eigenschappen**. Klik op de **gebruik** tabblad. Onder **vernieuwen**, selecteer de **gegevens vernieuwen bij het openen van het bestand** selectievakje. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)



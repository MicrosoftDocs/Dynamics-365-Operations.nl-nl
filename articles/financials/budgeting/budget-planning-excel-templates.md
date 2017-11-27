---
title: Budgetplanningssjablonen voor Excel
description: In dit onderwerp wordt beschreven hoe u Microsoft Excel-sjablonen kunt maken die voor budgetplannen kunnen worden gebruikt.
author: ryansandness
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 96df6bbfe5c9e158b616230c2b061762a5edda08
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="budget-planning-templates-for-excel"></a>Budgetplanningssjablonen voor Excel

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u Microsoft Excel-sjablonen kunt maken die voor budgetplannen kunnen worden gebruikt.

In dit onderwerp wordt beschreven hoe u Excel-sjablonen kunt maken die worden gebruikt voor budgetplannen met behulp van de standaard-demogegevensset en de beheerdersaanmelding. Zie [Overzicht van budgetplanning](budget-planning-overview-configuration.md) voor meer informatie over budgetplanning. U kunt ook de zelfstudie [Budgetplanning 101](budget-plan.md) volgen om de basismoduleconfiguratie en gebruiksbeginselen te leren.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Een werkblad genereren met de indeling voor het budgetplandocument

Budgetplandocumenten kunnen worden weergegeven en bewerkt met behulp van een of meer indelingen. Aan elke indeling kan een documentsjabloon voor het budgetplan worden gekoppeld om de budgetplangegevens in een Excel-werkblad weer te geven en te bewerken. In dit onderwerp wordt een documentsjabloon voor het budgetplan gegenereerd met behulp van een bestaande indelingsconfiguratie. 

1. Open de **Lijst met budgetplannen** (**Budgettering** &gt; **Budgetplannen**). 
2. Klik op **Nieuw** om een nieuw budgetplandocument te maken. 

  [![Budgetplanlijst](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Gebruik de optie **Regel toevoegen** om regels toe te voegen. Klik op **indelingen** om de documentindelingsconfiguratie voor het budgetplan weer te geven. 

  [![Budgetplannen toevoegen](./media/bpt2-1024x274.png)](./media/bpt2.png) 

U kunt de indelingsconfiguratie controleren en zo nodig aanpassen. 
1. Ga naar **Sjabloon** &gt; **Genereren** om een Excel-bestand voor deze indeling te maken. 
2. Nadat de sjabloon is gegenereerd, gaat u naar **Sjabloon** &gt; **Weergave** om de documentsjabloon voor het budgetplan te openen en te controleren. U kunt het Excel-bestand op uw lokale schijf opslaan. 

[![Opslaan als](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> De documentindeling van het budgetplan kan niet worden bewerkt nadat er een Excel-sjabloon aan is gekoppeld. Als u de indeling wilt wijzigen, verwijdert u het gekoppelde Excel-sjabloonbestand en genereert u het opnieuw. Dit is noodzakelijk om de indeling voor de velden te behouden en om het werkblad gesynchroniseerd te laten. 

De Excel-sjabloon bevat alle elementen van de documentindeling voor het budgetplan waarin de kolom **Beschikbaar in werkblad** is ingesteld op ´waar´. Overlappende elementen zijn niet toegestaan in de Excel-sjabloon. Als de indeling bijvoorbeeld de kolommen Aanvraag KW1, Aanvraag KW2, Aanvraag KW3 en Aanvraag KW4 bevat, en een kolom met de totale aanvraag waarin de som van alle 4 de kwartaalkolommen is opgenomen, zijn alleen de kwartaalkolommen of de kolom met het totaal beschikbaar voor gebruik in de Excel-sjabloon. In het Excel-bestand kunnen overlappende kolommen niet worden bijgewerkt tijdens de update, omdat gegevens in de tabel verouderd kunnen raken en onnauwkeurig worden.

[![Voorbeeld ](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Om mogelijke problemen te voorkomen bij het weergeven en bewerken van budgetplangegevens met behulp van Excel, moet dezelfde gebruiker zijn aangemeld bij zowel Microsoft Dynamics 365 for Finance and Operations als de invoegtoepassing Gegevensconnector van Microsoft Dynamics Office.

## <a name="add-a-header-to-budget-plan-document-template"></a>Een koptekst toevoegen aan de documentsjabloon voor het budgetplan
Als u koptekstgegevens wilt toevoegen, selecteert u de bovenste rij in het Excel-bestand en voegt u lege rijen in. Klik op **Ontwerp** in **Gegevensconnector** om koptekstvelden toe te voegen aan het Excel-bestand.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Klik op het tabblad **Ontwerp** op **Velden toevoegen** en selecteer vervolgens **BudgetPlanHeader** als de gegevensbron van de entiteit.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Wijs met de cursor de gewenste locatie in het Excel-bestand aan. Klik op **Label toevoegen** om het veldlabel aan de geselecteerde locatie toe te voegen. Selecteer **Waarde toevoegen** als u het waardeveld wilt toevoegen aan de geselecteerde plaats. Klik op **Gereed** om de ontwerper te sluiten.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Een berekende kolom aan de documentsjabloontabel voor het budgetplan toevoegen
--------------------------------------------------------------

Vervolgens worden berekende kolommen toegevoegd aan gegenereerde documentsjablonen voor het budgetplan. De kolom **Totale aanvraag**, waarin de kolommen Aanvraag KW1-Aanvraag KW4 worden samengevat, en de kolom **Correctie**, waarmee de kolom **Totale aanvraag** opnieuw wordt berekend met een vooraf gedefinieerde factor.

Klik op **Ontwerp** in **Gegevensconnector** om kolommen aan de tabel toe te voegen. Klik op **Bewerken** naast de gegevensbron **BudgetPlanWorksheet** om te beginnen met het toevoegen van kolommen.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

De geselecteerde veldgroep bevat de kolommen die in de sjabloon beschikbaar zijn. Klik op **Formule** om een nieuwe kolom toe te voegen. Geef de nieuwe kolom een naam en plak de formule in het veld **Formule**. Klik op **Bijwerken** om de kolom in te voegen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Als u de formule wilt definiëren, maakt u de formule in de spreadsheet en kopieert u deze naar het venster **Ontwerp**. Een aan Finance and Operations gerelateerde tabel heeft meestal de naam 'AXTable1'. Om bijvoorbeeld de kolommen Aanvraag KW1-Aanvraag KW4 in de spreadsheet samen te vatten, is de formule als volgt: AxTable1\[Aanvraag KW1\]+ AxTable1\[Aanvraag KW2\]+ AxTable1\[Aanvraag KW3\]+ AxTable1\[Aanvraag KW4\].

Herhaal deze stappen om de kolom **Correctie** in te voegen. Gebruik formule = AxTable1\[Totale aanvraag\]\*$I$1 voor deze kolom. Hiermee wordt de waarde in cel I1 gebruikt en worden de waarden in de kolom **Totale aanvraag** vermenigvuldigd om correctiebedragen te berekenen.

Sla het Excel-bestand op en sluit het. Keer terug naar Finance and Operations en klik in **Indelingen** op **Sjabloon &gt; Uploaden** om de opgeslagen Excel-sjabloon te uploaden die moet worden gebruikt voor het budgetplan. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Sluit de schuifregelaar **Indelingen**. Klik in het **Budgetplan**-document op **Werkblad** om het document in Excel weer te geven en te bewerken. Houd er rekening mee dat de aangepaste Excel-sjabloon is gebruikt om dit budgetplanwerkblad te maken en dat berekende kolommen worden bijgewerkt met de formules die zijn gedefinieerd in de vorige stappen. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips & trucs voor het maken van budgetplansjablonen
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kan ik extra gegevensbronnen gebruiken en toevoegen aan een budgetplansjabloon?

Ja, u kunt het menu **Ontwerp** gebruiken om extra entiteiten toe te voegen aan dezelfde of andere bladen in de Excel-sjabloon. U kunt bijvoorbeeld de gegevensbron **BudgetPlanProposedProject** toevoegen om een lijst met voorgestelde projecten te maken en te onderhouden terwijl u tegelijkertijd aan budgetplangegevens in Excel werkt. Houd er rekening mee dat grote hoeveelheden gegevensbronnen mogelijk van invloed zijn op de prestaties van het Excel-werkboek. 

U kunt de optie **Filter** in de **Gegevensconnector** gebruiken om gewenste filters aan extra gegevensbronnen toe te voegen.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kan ik de optie Ontwerp in de Gegevensconnector voor andere gebruikers verbergen?

Ja, open de **Gegevensconnector**-opties om de optie **Ontwerp** voor andere gebruikers te verbergen.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Vouw **Gegevensconnector-opties** uit en schakel het selectievakje **Ontwerp inschakelen** uit. Hiermee wordt de optie **Ontwerp** verborgen in de **Gegevensconnector**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kan ik voorkomen dat gebruikers per ongeluk de Gegevensconnector afsluiten tijdens het werken met gegevens?

Het is raadzaam om de sjabloon te vergrendelen om te voorkomen dat gebruikers deze sluiten. Als u de vergrendeling wilt inschakelen, klikt u op **Gegevensconnector**. In de rechterbovenhoek wordt een pijl weergegeven. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klik op de pijl voor een extra menu. Selecteer **Vergrendelen**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kan ik andere Excel-functies, zoals celopmaak, kleuren, voorwaardelijke opmaak en grafieken, gebruiken met mijn budgetplansjablonen?

Ja, de meeste Excel-standaardfuncties werken in budgetplansjablonen. Het is raadzaam kleurcodering te gebruiken voor gebruikers om een onderscheid te maken tussen alleen-lezen kolommen en bewerkbare kolommen. Voorwaardelijke opmaak kan worden gebruikt om problematische gebieden van het budget te markeren. Kolomtotalen kunnen eenvoudig worden weergegeven met behulp van Excel-standaardformules boven de tabel.

U kunt ook draaitabellen en diagrammen maken en gebruiken voor extra groeperingen en visualisaties van budgetgegevens. Klik op het tabblad **Gegevens** in de groep **Verbindingen** op **Alles vernieuwen**, en klik vervolgens op **Verbindingseigenschappen**. Klik op het tabblad **Gebruik** en schakel onder **Vernieuwen** het selectievakje **Gegevens vernieuwen bij openen van bestand** in. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)





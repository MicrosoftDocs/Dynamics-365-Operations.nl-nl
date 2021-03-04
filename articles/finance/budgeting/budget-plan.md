---
title: Budgetplanning
description: Het doel van dit lab is om Microsoft Dynamics 365 Finance-functionaliteitsupdates in het gebied Budgetplanning te laten zien. Het doel van dit lab is om een snel configuratievoorbeeld van de budgetplanningsmodule te laten zien en aan te tonen hoe budgetplanning kan worden gerealiseerd met deze configuratie.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9558013236a728e0fb9691f4edd719fe58d5457
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442092"
---
# <a name="budget-planning"></a>Budgetplanning

[!include [banner](../includes/banner.md)]

Het doel van dit lab is om Microsoft Dynamics 365 Finance-functionaliteitsupdates in het gebied Budgetplanning te laten zien. Het doel van dit lab is om een snel configuratievoorbeeld van de budgetplanningsmodule te laten zien en aan te tonen hoe budgetplanning kan worden gerealiseerd met deze configuratie.  Dit lab is specifiek gericht op de volgende bedrijfsprocessen of taken:
- Een organisatiehiërarchie maken voor budgetplanning en gebruikersbeveiliging configureren
- Budgetplanningsscenario's, budgetplanningskolommen, indelingen en Excel-sjablonen definiëren
- Een budgetplanningsproces maken en activeren
- Een budgetplanningsdocument maken door werkelijke waarden uit het grootboek te halen
- Toewijzingen gebruiken om gegevens voor budgetplanningsdocumenten aan te passen
- Gegevens voor budgetplanningsdocumenten bewerken in Excel 

<a name="prerequisites"></a>Vereisten 
------------------

Voor deze zelfstudie moet u toegang hebben tot de Microsoft Dynamics 365 Finance-omgeving met Contoso-demogegevens en moet u als beheerder zijn geconfigureerd voor het exemplaar. Gebruik niet de browsermodus Privé voor dit lab. Meld u indien nodig af bij een andere account in de browser en meld u aan met beheerdersreferenties. Wanneer u zich aanmeldt, **MOET** u het selectievakje “Aangemeld blijven” inschakelen. Hiermee wordt een permanente cookie gemaakt die de Excel-toepassing momenteel nodig heeft. Als u zich aanmeldt bij de toepassing met een andere browser dan IE, wordt u gevraagd om u aan te melden binnen de Excel-app. Wanneer u op Aanmelden in de Excel-app klikt, wordt een pop-upvenster van IE geopend en wanneer u zich aanmeldt, **MOET** u het selectievakje Aangemeld blijven inschakelen. Als u klikt op Aanmelden in de Excel-app en dat lijkt niets te doen, moet u de IE-cookiecache wissen.

## <a name="scenario-overview"></a>**Scenario-overzicht**
Julia werkt als financiële manager in Contoso Entertainment Systems in Duitsland (DEMF). Aangezien FY2016 dichterbij komt, moet ze zich gaan bezighouden met het budget van het bedrijf voor het komende jaar. Budgetvoorbereiding ziet er als volgt uit:

1.  Julia gebruikt de werkelijke bedragen van vorig jaar als uitgangspunt om het budget te maken.
2.  Op basis van de werkelijke cijfers van vorig jaar maakt ze ramingen voor 12 maanden in het komende jaar
3.  Julia controleert het budget met CFO. Wanneer ze klaar is, maakt ze de noodzakelijke correcties voor het budgetplan en rondt ze de budgetvoorbereiding af.

Configuratieschema voor budgetplanning ziet er voor het scenario als volgt uit:

![Schema voor budgetplanningsconfiguratie](./media/screenshot1-300x152.png)

Julia gebruikt de volgende Excel-sjabloon om het budget voor te bereiden:

[![Excel-sjabloon](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Oefening 1: Configuratie

### <a name="task-1-create-organizational-hierarchy"></a>**Taak 1: Organisatiehiërarchie maken**
Omdat het gehele budgetteringsproces op de financiële afdeling plaatsvindt, moet Julia een zeer eenvoudige organisatiehiërarchie maken die alleen bestaat uit de financiële afdeling. 

1.1. Navigeer naar Organisatiehiërarchieën (Organisatiebeheer &gt; Organisaties &gt; Organisatiehiërarchieën) en klik op de knop Nieuw.

![Organisatiehiërarchieën](./media/screenshot3.png) 

1.2. Typ de naam voor de organisatiehiërarchie in het vak Naam en klik op de knop Doel toewijzen.

1.3. Selecteer het doel Budgetplanning, klik op Toevoegen en wijs de nieuw gemaakte organisatiehiërarchie toe. 

[![Doel toewijzen](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Herhaal de bovenstaande stap voor het organisatorische doel Beveiliging. Sluit het formulier wanneer u klaar bent.

1.5. Klik in het formulier Organisatiehiërarchieën op Weergeven. Klik op Bewerken in de hiërarchieontwerper en maak een hiërarchie door op Invoegen te klikken.

[![Invoegen](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Selecteer de financiële afdeling voor de budgetteringshiërarchie. 

[![Financiën](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Wanneer u klaar bent, klikt u op Publiceren en sluiten. Selecteer 01-01-2015 als de ingangsdatum voor hiërarchiepublicatie.

[![Ingangsdatum](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Taak 2: Gebruikerbeveiliging configureren
In budgetplanning worden speciale beveiligingsbeleidsregels gebruikt om toegang tot de budgetplangegevens te configureren. Julia moet toegang verlenen tot financiële budgetplannen voor haarzelf. 

2.1. Schakel over naar DEMF-rechtspersooncontext. 


2.2. Navigeer naar Budgettering &gt; Instellen &gt; Budgetplanning &gt; Configuratie budgetplanning. Stel op het tabblad Parameters de waarde voor het beveiligingsmodel in op Op basis van beveiligingsorganisaties. 

[![Parameters](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Navigeer naar Systeembeheer &gt; Gebruikers &gt; Gebruikers. Geef beheerder (Julia Funderburk) de rol van budgetmanager. 

[![Budgetbeheerder](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Selecteer gebruikersrol en klik op Organisaties toewijzen. 

[![Organisaties toewijzen](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Selecteer “Toegang toewijzen aan specifieke organisaties”. Selecteer de organisatiehiërarchie die in de eerste stap is gemaakt. Selecteer het financiële knooppunt en klik op de knop Toewijzen met onderliggende organisaties. 

***Belangrijk!*** *Zorg ervoor dat u zich in DEMF-rechtspersooncontext bevindt bij het uitvoeren van deze taak aangezien organisatorische beveiliging wordt toegepast per rechtspersoon* 

### <a name="task-3-create-scenarios"></a>Taak 3: Scenario's maken
3.1. Navigeer naar Budgettering &gt; Instellen &gt; Budgetplanning &gt; Configuratie budgetplanning. Noteer op de pagina Scenario's de scenario's die we verder gaan gebruiken in dit lab: werkelijke en gebudgetteerde waarden van vorig jaar. 

*Opmerking: u kunt desgewenst nieuwe scenario's voor deze oefening maken deze gebruiken.* 

[![Nieuwe scenario's](./media/screenshot15.png)](./media/screenshot15.png) 

*Opmerking: omdat Julia geen formeel goedkeuringsproces voor budgetvoorbereiding gebruikt, wordt de instelling voor workflows, fasen en workflowfasen in dit lab overgeslagen en worden bestaande instellingen voor Workflow automatisch goedkeuren gebruikt.*

### <a name="task-4-create-budget-plan-columns"></a>Taak 4: Budgetplankolommen maken
De kolommen van het budgetplan zijn monetaire of op hoeveelheid gebaseerde kolommen die in de documentindeling van het budgetplan kunnen worden gebruikt. In ons voorbeeld moeten we een kolom maken voor werkelijke waarden van vorig jaar en 12 kolommen voor elke maand in een gebudgetteerd jaar. Kolommen kunnen worden gemaakt door eenvoudigweg te klikken op de knop Toevoegen en de waarden in te vullen of met behulp van een gegevensentiteit. In dit lab gebruiken we Gegevensentiteit om de waarden in te vullen. 

4.1. Open de pagina Kolommen in Budgettering &gt; Instellen &gt; Budgetplanning &gt; Configuratie budgetplanning. Klik op de knop Office rechtsboven in het formulier en selecteer kolommen (ongefilterd). 

[![Kolommen niet gefilterd](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Een Excel-werkmap wordt geopend die moet worden gebruikt voor het invullen van de waarden. Als u hierom wordt gevraagd, klikt u op Bewerken inschakelen en Deze app vertrouwen. 

4.3. Er zijn meer kolommen nodig om de waarden in te vullen. Klik op Ontwerp in het rechterdeelvenster om de kolommen toe te voegen aan het raster. 

[![Ontwerp](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Klik op de potloodknop naast PlanColumns om beschikbare kolommen te zien die u aan het raster kunt toevoegen. 

[![Bewerken](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Dubbelklik op elk beschikbaar veld om de velden toe te voegen aan Geselecteerde velden en klik op Bijwerken. 

4.6. Voeg in de Excel-tabel alle kolommen toe die moeten worden gemaakt. Gebruik de functie voor automatisch vullen in Excel om de regels snel toe te voegen. Zorg ervoor dat de regels worden toegevoegd als onderdeel van de tabel (wanneer u verticaal schuift, moet u kolomkopteksten boven in het raster zien). 

4.7. Ga terug naar de toepassing en vernieuw de pagina. Gepubliceerde waarden worden weergegeven. 

[![Vernieuwen](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Taak 5: Documentindelingen en sjablonen voor het budgetplan maken
Met de indeling wordt gedefinieerd hoe het raster met documentregels van het budgetplan eruit ziet wanneer een gebruiker het document van het budgetplan opent. Het is ook mogelijk om van indeling voor het document van het budgetplan te wisselen om dezelfde gegevens vanuit verschillende hoeken te bekijken. Nu Julia kolommen heeft gedefinieerd die in ons document van het budgetplan moeten worden gebruikt, moet ze een indeling voor het budgetplandocument maken, die er hetzelfde uitziet als de Excel-tabel waarmee ze budgetgegevens maakt (zie de sectie Scenario-overzicht in dit lab) 

5.1. Open de pagina Indelingen in Budgettering &gt; Instellen &gt; Budgetplanning &gt; Configuratie budgetplanning. Maak een nieuwe indeling voor Maandelijkse budgetinvoer:

-   Selecteer dimensie HR + BE om hoofdrekeningen en bedrijfseenheden voor de indeling op te nemen.
-   Geef alle budgetplankolommen weer die in de vorige stap zijn gemaakt in de sectie Elementen. Maak alle waarden bewerkbaar behalve de werkelijke waarden van vorig jaar.
-   Klik op de knop Omschrijvingen om te selecteren voor welke financiële dimensies Omschrijvingen in het raster moeten worden weergegeven.

[![Omschrijvingen](./media/screenshot24.png)](./media/screenshot24.png) 

Op basis van de definitie van de budgetplanindeling kunnen we een Excel-sjabloon maken die als een alternatieve manier moet worden gebruikt om budgetgegevens te bewerken. Omdat de Excel-sjabloon moet overeenkomen met de definitie van de budgetplanindeling, kunt u geen budgetplanindeling bewerken nadat de Excel-sjabloon is gegenereerd. Daarom moet deze taak worden uitgevoerd nadat alle indelingsonderdelen zijn gedefinieerd. 

5.2. Klik voor de indeling die in de stap 5.1. is gemaakt op de knop Sjabloon &gt; Genereren. Bevestig het waarschuwingsbericht. Als u de sjabloon wilt weergeven, klikt u op Sjabloon &gt; Weergeven. 

*Opmerking: controleer 'Opslaan als' en selecteer de plaats waar de sjabloon moet worden opgeslagen om deze te bewerken. Als de gebruiker 'Openen' in het dialoogvenster selecteert zonder op te slaan, worden de wijzigingen die zijn aangebracht in het bestand niet behouden wanneer het bestand wordt gesloten.* 
[![Sjabloonweergave](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Optionele stap&gt; Wijzig de Excel-sjabloon om deze er gebruikersvriendelijker te laten uitzien; voeg totale formules, koptekstvelden, opmaak enzovoort toe. Sla de wijzigingen op en upload het bestand naar budgetplanindeling door te klikken op Indeling &gt; Uploaden te klikken. 


### <a name="task-6-create-a-budget-planning-process"></a>Taak 6: Een budgetplanningsproces maken
Julia moet een nieuw budgetplanningsproces maken en activeren waarin alle bovenstaande instellingen worden gecombineerd om met het invoeren van budgetplannen te starten. Met het budgetplanningsproces wordt gedefinieerd welke budgetorganisaties, workflow, indelingen en sjablonen worden gebruikt voor het maken van budgetplannen. 

6.1. Navigeer naar Budgettering &gt; Instellen &gt; Budgetplanning &gt; Budgetplanningsproces en maak een nieuwe record.

-   Budgetplanningsproces: DEMF-budgettering FY2016
-   Budgetcyclus – FY2016
-   Grootboek: DEMF
-   Standaardrekeningstructuur: productie W&V
-   Organisatiehiërarchie: selecteer de hiërarchie die in het begin van het lab is gemaakt
-   Budgetplanningsworkflow - automatisch toewijzen - workflow goedkeuren voor financiële afdeling
-   Geef in de sjablonen en de regels van de budgetplanningsfase voor elke workflow aan of het toevoegen van regels en het wijzigen van regels zijn toegestaan en welke indeling standaard moet worden gebruikt

*Opmerking: u kunt aanvullende documentindelingen maken en deze toewijzen om beschikbaar te zijn in de workflowfase van de budgetplanning door te klikken op de knop Alternatieve indelingen.* 

[![Alternatieve indelingen](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Selecteer Acties &gt; Activeren om deze budgetplanningsworkflow te activeren. 

[![Activeren](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Oefening 2: Processimulatie

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Taak 7: Initiële gegevens genereren voor budgetplan vanuit grootboek
7.1. Navigeer naar Budgettering &gt; Periodiek &gt; Budgetplan genereren op basis van grootboek. Vul de periodieke procesparameters in en klik op Genereren. 

7.2. Navigeer naar Budgettering &gt; Budgetplannen om een budgetplan te vinden dat door het proces Genereren is gemaakt. 

[![Budgetplan](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Open documentdetails door te klikken op de hyperlink Documentnummer. Het budgetplan wordt weergegeven zoals is gedefinieerd in de indeling die tijdens dit lab is gemaakt. 

[![Budgetplanweergave](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Taak 8: Budget van het huidige jaar maken op basis van werkelijke waarden van vorig jaar
Toewijzingsmethoden kunnen worden gebruikt in het budgetplan om gegevens voor budgetplannen gemakkelijk te kopiëren tussen scenario´s/te verspreiden over perioden/toe te wijzen aan dimensies. We zullen toewijzingen gebruiken om het budget van het huidige jaar te maken op basis van de werkelijke waarden van vorig jaar. 

8.1. Selecteer alle regels in het raster van het budgetplandocument en klik op Budget toewijzen. 

[![Alle regels](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Selecteer de toewijzingsmethode, periodesleutel, bron- en bestemmingsscenario's en klik op Toewijzen. 

[![Toewijzen](./media/screenshot33.png)](./media/screenshot33.png)

De werkelijke bedragen van vorig jaar worden gekopieerd naar het huidige jaarbudget. Wijs deze aan de perioden toe met de periodesleutel voor verkoopcurve. 

[![Verkoopcurve](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Taak 9: Het budgetplandocument aanpassen met Excel en het document afronden
9.1. Klik op de knop Werkblad om documentinhoud in Excel te openen.

9.2. Wanneer de Excel-werkmap wordt geopend, past u de getallen in het budgetplandocument aan en klikt u op de knop Publiceren.

9.3. Ga terug naar het budgetplandocument. Klik op Workflow &gt; Verzenden om het document automatisch goed te keuren.

[![Automatisch goedkeuren](./media/screenshot37.png)](./media/screenshot37.png) 

Zodra de workflow is voltooid, wordt de budgetplandocumentfase gewijzigd in Goedgekeurd. [![Goedgekeurd](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Bijlage

### <a name="auto-approve-workflow-configuration"></a>Workflowconfiguratie automatisch goedkeuren

A. Budgettering &gt; Instellen &gt; Budgetplanning &gt; Budgetteringsworkflows. Een nieuwe workflow maken met de sjabloon Workflows budgetplanning:

[![Een nieuwe workflow maken](./media/screenshot39.png)](./media/screenshot39.png)

Deze workflow bevat slechts één taak: Faseovergang budgetplan. 

[![Faseovergang budgetplan](./media/screenshot40.png)](./media/screenshot40.png) 

Sla de workflow op en activeer deze. 

B. Navigeer naar Budgettering &gt; Instellen &gt; Budgetplanning &gt; Configuratie budgetplanning. Op het tabblad Fasen worden 2 fasen gemaakt: Eerste en Ingediend. 

[![Eerste en ingediend](./media/screenshot41.png)](./media/screenshot41.png)

C. Navigeer naar Budgettering &gt; Instellen &gt; Budgetplanning &gt; Configuratie budgetplanning. Koppel op het tabblad Workflowfasen de in stap A gemaakte workflow Automatisch goedkeuren aan de fasen Eerste en Ingediend.

[![Budgettering en budgetplanning](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
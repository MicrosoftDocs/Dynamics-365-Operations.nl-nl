---
title: Budgetplanning
description: "Het doel van deze cursus is een gestructureerde weergave van Microsoft Dynamics 365 bevatten voor het bijwerken van de functionaliteit voor bewerkingen in het gebied van de budgetplanning. Het doel van dit lab is om een snel configuratievoorbeeld van de budgetplanningsmodule te laten zien en aan te tonen hoe budgetplanning kan worden gerealiseerd met deze configuratie.  Deze cursus zal worden toegespitst specifiek op de volgende bedrijfsprocessen of -taken – organisatiehiërarchie maken voor budget, planning en configuratie van gebruikersbeveiliging - definiëren budgetplanscenario&quot;s, plan budgetkolommen, indelingen en Excel-sjablonen: maken en activeren van proces - maken budgetplandocument door te halen in de werkelijke waarden van grootboek - toewijzingen gebruiken om aan te passen document budgetplangegevens - bewerken budget plan document budgetplanninggegevens in Excel"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Budgetplanning

Het doel van deze cursus is een gestructureerde weergave van Microsoft Dynamics 365 bevatten voor het bijwerken van de functionaliteit voor bewerkingen in het gebied van de budgetplanning. Het doel van dit lab is om een snel configuratievoorbeeld van de budgetplanningsmodule te laten zien en aan te tonen hoe budgetplanning kan worden gerealiseerd met deze configuratie.  Deze cursus zal worden toegespitst specifiek op de volgende bedrijfsprocessen of -taken – organisatiehiërarchie maken voor budget, planning en configuratie van gebruikersbeveiliging - definiëren budgetplanscenario's, plan budgetkolommen, indelingen en Excel-sjablonen: maken en activeren van proces - maken budgetplandocument door te halen in de werkelijke waarden van grootboek - toewijzingen gebruiken om aan te passen document budgetplangegevens - bewerken budget plan document budgetplanninggegevens in Excel 

<a name="prerequisites"></a>Vereisten 
------------------

Voor deze zelfstudie moet u toegang tot de Dynamics 365 voor operationele omgevingen met Contoso demonstratiegegevens en als een beheerder op de instantie worden ingericht. Gebruik In particuliere modus van de browser niet afmelden van een andere rekening in de browser zo nodig voor dit lab - en zich aanmelden met Dynamics 365 voor bewerkingen administrator-referenties. Bij het aanmelden bij Dynamics 365 voor bewerkingen, u **moet** Vink het selectievakje 'Aangemeld blijven'. Hiermee wordt een permanente cookie gemaakt die de Excel-toepassing momenteel nodig heeft. Als u zich bij de Dynamics 365 voor bewerkingen met behulp van een andere browser dan Internet Explorer aanmeldt, klik u gevraagd aan te melden binnen de Excel-toepassing. Wanneer u op Aanmelden in de Excel-app klikt, wordt een pop-upvenster van IE geopend en wanneer u zich aanmeldt, **MOET** u het selectievakje Aangemeld blijven inschakelen. Als u klikt op Aanmelden in de Excel-app en dat lijkt niets te doen, moet u de IE-cookiecache wissen.

## <a name="scenario-overview"></a>**Scenario overview**
Julia werkt als financiële manager in Contoso Entertainment Systems in Duitsland (DEMF). Aangezien FY2016 dichterbij komt, moet ze zich gaan bezighouden met het budget van het bedrijf voor het komende jaar. Budgetvoorbereiding ziet er als volgt uit:

1.  Julia gebruikt de werkelijke bedragen van vorig jaar als uitgangspunt om het budget te maken.
2.  Op basis van de werkelijke cijfers van vorig jaar maakt ze ramingen voor 12 maanden in het komende jaar
3.  Julia controleert het budget met CFO. Wanneer ze klaar is, maakt ze de noodzakelijke correcties voor het budgetplan en rondt ze de budgetvoorbereiding af.

Configuratieschema voor het scenario budgetplanningsproces ziet er als volgt uit:

![Screenshot1](./media/screenshot1-300x152.png)

Julia gebruikt de volgende Excel-sjabloon voor het voorbereiden van het budget:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Oefening 1: Configuratie
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Taak 1: De organisatiehiërarchie maken**
Omdat het gehele budgetteringsproces op de financiële afdeling plaatsvindt, moet Julia een zeer eenvoudige organisatiehiërarchie maken die alleen bestaat uit de financiële afdeling. 1.1. Ga naar organisatiehiërarchieën (Organisatiebeheer &gt;organisaties &gt;organisatiehiërarchieën) en klik op knop Nieuw

![Screenshot3](./media/screenshot3.png) 

1.2. Typ de naam voor de organisatiehiërarchie en klik op de knop toewijzen doel

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Doel van de budgetplanning selecteren, klikt u op de knop toevoegen en nieuwe organisatiehiërarchie toewijzen: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Herhaal de bovenstaande stap voor het organisatorische doel Beveiliging. Sluit het formulier wanneer u klaar bent.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Klik in het formulier Organisatiehiërarchieën op de knop Weergeven. Klik op Bewerken in de hiërarchieontwerper en maak een hiërarchie door te klikken op de knop Invoegen.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Selecteer de financiële afdeling voor de budgetteringshiërarchie. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Wanneer u klaar bent, klikt u op de knop Publiceren en sluiten. Selecteer 01-01-2015 als ingangsdatum voor hiërarchiepublicatie.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Taak 2: Gebruikerbeveiliging configureren
In budgetplanning worden speciale beveiligingsbeleidsregels gebruikt om toegang tot de budgetplangegevens te configureren. Julia moet toegang verlenen tot financiële budgetplannen voor haarzelf. 2.1. Ga naar DEMF rechtspersoon context: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Ga naar de budgettering &gt;Setup &gt;budgetplanning &gt;budgetplanningconfiguratie. Tabblad Parameters de beveiliging model waarde instelt op op basis van de beveiliging van organisaties [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Ga naar Systeembeheer &gt;gebruikers &gt;gebruikers. Geef beheerder (Julia Funderburk) de rol van budgetmanager. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Rol van gebruiker verzamelen en organisaties toewijzen op [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Selecteer “Toegang toewijzen aan specifieke organisaties”. Selecteer de organisatiehiërarchie die in de eerste stap is gemaakt. Financiën knooppunt verzamelen en op subsidie met onderliggende knop ***belangrijk!*** *: Zorg ervoor dat u in de context van DEMF rechtspersoon bij het uitvoeren van deze taak als de beveiliging van de organisatie wordt toegepast per rechtspersoon*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Taak 3: Scenario's maken
3.1. Ga naar de budgettering&gt;Setup &gt;budgetplanning &gt;budgetplanningconfiguratie. Noteer op de pagina Scenario's de scenario's die we verder gaan gebruiken in dit lab: werkelijke en gebudgetteerde waarden van vorig jaar. *Opmerking: u kunt desgewenst nieuwe scenario's voor deze oefening maken deze gebruiken.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*opmerking: als Julia geen gebruik van formele goedkeuringsproces voor budget opstellen maakt, we workflows, fasen worden overgeslagen en werkstroomstadiums instellingen in deze cursus en bestaande instellingen wilt gebruiken voor automatische: workflow goedkeuren. Zie bijlage voor de configuratie van de workflow.*

## <a name="task-4-create-budget-plan-columns"></a>Taak 4: Budgetplankolommen maken
De kolommen van het budgetplan zijn monetaire of op hoeveelheid gebaseerde kolommen die in de documentindeling van het budgetplan kunnen worden gebruikt. In ons voorbeeld moeten we een kolom maken voor werkelijke waarden van vorig jaar en 12 kolommen voor elke maand in een gebudgetteerd jaar. Kolommen kunnen worden gemaakt door eenvoudigweg te klikken op de knop Toevoegen en de waarden in te vullen of met behulp van een gegevensentiteit. In dit lab gebruiken we Gegevensentiteit om de waarden in te vullen. 4.1. In budgettering&gt;Setup &gt;budgetplanning &gt;budget plannen configuratie kolommen pagina openen. Klik op de Office-knop in de rechterbovenhoek van het formulier en kies kolommen (niet gefilterd) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. De Excel-werkmap wordt geopend die moet worden gebruikt voor het invullen van de waarden. Als u wordt gevraagd, klikt u op bewerken inschakelen en deze toepassing vertrouwt [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Moeten we meer kolommen in te vullen de waarden. Klik op ontwerp in het rechterdeelvenster de kolommen toevoegen aan het raster: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Klik op weinig potloodknop klikt naast PlanColumns om te zien van de beschikbare kolommen toevoegen aan het raster [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Dubbelklik op elk beschikbaar veld wilt toevoegen aan de geselecteerde velden en klik op Update [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Voeg in de Excel-tabel alle kolommen toe die moeten worden gemaakt. Gebruik de functie voor automatisch vullen in Excel om de regels snel toe te voegen. Zorg ervoor dat de regels worden toegevoegd als onderdeel van de tabel (als u verticale schuifbalk gebruikt, moet u kolomkoppen boven aan het raster zien) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Terug naar Dynamics 365 for Operations en vernieuw de pagina. Gepubliceerde waarden worden weergegeven in Dynamics 365 voor bewerkingen. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Taak 5: Documentindelingen en sjablonen voor het budgetplan maken
Met de indeling wordt gedefinieerd hoe het raster met documentregels van het budgetplan eruit ziet wanneer een gebruiker het document van het budgetplan opent. Het is ook mogelijk om van indeling voor het document van het budgetplan te wisselen om dezelfde gegevens vanuit verschillende hoeken te bekijken. Nu Julia kolommen heeft gedefinieerd die in ons document van het budgetplan moeten worden gebruikt, moet ze een indeling voor het budgetplandocument maken, die er hetzelfde uitziet als de Excel-tabel waarmee ze budgetgegevens maakt (zie de sectie Scenario-overzicht in dit lab) 5.1. In budgettering&gt;Setup &gt;budgetplanning &gt;budget plannen configuratie indelingen pagina openen. Maak een nieuwe indeling voor Maandelijkse budgetinvoer:

-   Selecteer dimensie HR + BE om hoofdrekeningen en bedrijfseenheden voor de indeling op te nemen.
-   Geef alle budgetplankolommen weer die in de vorige stap zijn gemaakt in de sectie Elementen. Maak alle waarden bewerkbaar behalve de werkelijke waarden van vorig jaar.
-   Klik op de knop Omschrijvingen om te selecteren voor welke financiële dimensies Omschrijvingen in het raster moeten worden weergegeven.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) op basis van het budget plannen indelingsdefinitie maken we een Excel-sjabloon moet worden gebruikt als een andere manier om budget-gegevens te bewerken. Omdat de Excel-sjabloon moet overeenkomen met de definitie van de budgetplanindeling, kunt u geen budgetplanindeling bewerken nadat de Excel-sjabloon is gegenereerd. Daarom moet deze taak worden uitgevoerd nadat alle indelingsonderdelen zijn gedefinieerd. 5.2. Voor de indeling gemaakt in de 5.1. Stap, klikt u op de knop sjabloon &gt;genereren. Bevestig het waarschuwingsbericht. De sjabloon, klik op sjabloon &gt;weergeven. *opmerking: Controleer 'Opslaan als' en selecteer de plaats waar de sjabloon moet worden opgeslagen om deze te bewerken. Als de gebruiker selecteert 'Openen' in het dialoogvenster zonder op te slaan, worden de wijzigingen die zijn gedaan naar het bestand niet behouden wanneer het bestand wordt gesloten.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Optionele stap&gt; sjabloon Excel wijzigen zodat deze meer gebruiker beschrijvende: toevoegen totale formules, header-velden, opmaak, enz. De wijzigingen opslaan en het bestand uploaden naar budget plan indeling door te klikken op de indeling &gt;uploaden [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Taak 6: Een budgetplanningsproces maken
Julia moet een nieuw budgetplanningsproces maken en activeren waarin alle bovenstaande instellingen worden gecombineerd om met het invoeren van budgetplannen te starten. Met het budgetplanningsproces wordt gedefinieerd welke budgetorganisaties, workflow, indelingen en sjablonen worden gebruikt voor het maken van budgetplannen. 6.1. Navigeer naar de budgettering &gt;Setup &gt;budgetplanning &gt;voor het planningsproces budget en een nieuwe record maakt.

-   Budgetplanningsproces: DEMF-budgettering FY2016
-   Budgetcyclus – FY2016
-   Grootboek: DEMF
-   Standaardrekeningstructuur: productie W&V
-   Organisatiehiërarchie: selecteer de hiërarchie die in het begin van het lab is gemaakt
-   Budgetplanningsworkflow - automatisch toewijzen - workflow goedkeuren voor financiële afdeling
-   Geef in de sjablonen en de regels van de budgetplanningsfase voor elke workflow aan of het toevoegen van regels en het wijzigen van regels zijn toegestaan en welke indeling standaard moet worden gebruikt

*Opmerking: u kunt aanvullende documentindelingen maken en deze toewijzen om beschikbaar te zijn in de workflowfase van de budgetplanning door te klikken op de knop Alternatieve indelingen.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Selecteer de acties &gt;activeren om te activeren zodat deze budgetplanningwerkstroom [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Oefening 2: Processimulatie
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Taak 7: Initiële gegevens genereren voor budgetplan vanuit grootboek
7.1. Ga naar de budgettering &gt;periodiek &gt;budgetplan genereren vanuit het grootboek. Vul de periodieke procesparameters in en de klik op de knop Genereren. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Ga naar de budgettering &gt;budget wil zoeken naar een budgetplan gemaakt door proces genereren. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Open documentdetails door te klikken op de hyperlink Documentnummer. Budgetplan wordt weergegeven, zoals gedefinieerd in de indeling gemaakt tijdens deze cursus [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Taak 8: Budget van het huidige jaar maken op basis van werkelijke waarden van vorig jaar
Toewijzingsmethoden kunnen worden gebruikt in het budgetplan om gegevens voor budgetplannen gemakkelijk te kopiëren tussen scenario´s/te verspreiden over perioden/toe te wijzen aan dimensies. We zullen toewijzingen gebruiken om het budget van het huidige jaar te maken op basis van de werkelijke waarden van vorig jaar. 8.1. Alle regels in het raster budget plan document verzamelen en klik op de knop budgettoewijzingen [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Selecteer de toewijzingsmethode, periodesleutel, bron- en bestemmingsscenario's en klik op toewijzen 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

De werkelijke bedragen van vorig jaar naar het huidige jaar budget worden gekopieerd en de groep toewijzen over meerdere perioden met verkoop curve periodesleutel. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Taak 9: Het budgetplandocument aanpassen met Excel en het document afronden
9.1. Klik op de knop werkblad om de inhoud van het document openen in Excel

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Wanneer de Excel-werkmap wordt geopend, past u de getallen in het budgetplandocument aan en klikt u op de knop Publiceren.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Ga terug naar budgetplandocument in Dynamics 365 voor bewerkingen. Klik op workflow &gt;het document automatisch worden goedgekeurd indienen

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Als workflow is voltooid, wordt budgetplanfase document gewijzigd in goedgekeurd. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Bijlage
========

### <a name="auto-approve-workflow-configuration"></a>Workflowconfiguratie automatisch goedkeuren

A. Budgettering &gt;Setup &gt;budgetplanning &gt;budgetteringsworkflows een nieuwe workflow met behulp van sjabloon budgetplanningworkflows maken:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Deze workflow bevat slechts één taak: Faseovergang budgetplan 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Opslaan en activeren van de workflow. 

B. Ga naar de budgettering &gt;Setup &gt;budgetplanning &gt;budgetplanningconfiguratie. Maak in fasen tabblad 2 fasen: eerste en ingediend 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Ga naar de budgettering &gt;Setup &gt;budgetplanning &gt;budgetplanningconfiguratie. De werkstroom automatisch koppelen op het tabblad van de workflow fasen: goedkeuren gemaakt in stap met de fasen initiële en ingediend 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  



---
title: "Werkgebied voor afsluiten van financiële periode"
description: "Dit artikel geeft een overzicht van het werkgebied Afgesloten financiële periode en de bijbehorende configuratie."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Werkgebied voor afsluiten van financiële periode

Dit artikel geeft een overzicht van het werkgebied Afgesloten financiële periode en de bijbehorende configuratie.

Werkgebied voor afsluiten van financiële periode

De **financiële periode afsluiten** werkruimte kunt u het afsluitingsproces voor uw financiële volgen over bedrijven, gebieden en personen. Afhankelijk van uw weergave van de **financiële periode afsluiten** werkruimte, wordt er van alle taken en statussen voor de planning van een afsluiting of alleen de taken die aan u zijn toegewezen. 

U moet eerst een planning afsluiting boven aan de werkruimte selecteren. Alle gegevens die wordt weergegeven in de werkruimte wordt vervolgens gefilterd op de planning van de geselecteerde afsluiting.

### <a name="summary-tiles"></a>Overzichtstegels

De tegel **Overzicht** biedt een overzicht van het proces en indicatoren helpen u het afsluitingsproces op schema te houden. U ziet taken die zijn verleden verstreken of resterende taken voor vandaag, taken die vandaag moeten worden, maar worden geblokkeerd vanwege afhankelijkheden en alle resterende taken voor het proces. Deze informatie is voor alle bedrijven die zijn opgenomen in de planning van de geselecteerde afsluiting.

### <a name="tasks-and-status-section"></a>Sectie Taken en status

In de **taken en status** gedeelte van de status van het algehele afsluiting planning wordt uitgesplitst op verschillende manieren: status per bedrijf, status per gebied en status per persoon die verantwoordelijk is. U kunt de status voor alle taken in de afsluiting, alleen taken plannen die vandaag, moeten worden weergeven of taken die reeds voltooid hadden moeten door het filter boven aan de lijst kaart wijzigen. U kunt ook het Bedrijfsfilter de status bekijken voor een specifiek bedrijf selecteren. Elk tabblad status geeft een onderverdeling per percentage dat is voltooid en het aantal taken dat blijven. Klik op de kaart of de **details bekijken** actie voor het filteren van de gedetailleerde takenlijst door de geselecteerde kaart. 

Het laatste tabblad is voor de gedetailleerde takenlijst. Deze lijst wordt de volledige lijst weergegeven en kan worden gefilterd zodat alleen de taken die u geïnteresseerd bent in het veld geeft. U kunt de lijst met taken op verschillende manieren filteren. U kunt bijvoorbeeld filteren op taak vervaldatum, de verbonden onderneming en de bijbehorende gebied. U kunt ook weergeven of verbergen van voltooide taken in de lijst selecteren. 

Twee indicatoren worden gebruikt voor taken:

-   Een uitroepteken geeft aan dat de taak achterstallig is. Voor taken die reeds voltooid hadden, wordt de vervaldatum bovendien rood gemarkeerd.
-   Een hangslot geeft aan dat de taak afhankelijk is van andere taken die nog niet zijn ingevuld. Een taak die wordt geblokkeerd door afhankelijkheden kan niet worden gemarkeerd als voltooid. U kunt afhankelijkheden voor een taak instellen met behulp van de **afhankelijkheid instellen** actie.

Naam van de taak is een hyperlink naar de Microsoft Dynamics 365 voor pagina bewerkingen of andere webpagina waarin de gebruiker moet gaan om het werk te voltooien. U kunt deze hyperlink instellen met behulp van de **taakkoppeling** wanneer u een taak maken of bewerken. 

U kunt bestanden, notities, afbeeldingen en URL's aan een taak koppelen met behulp van de **bijlagen** actie. U kunt bijvoorbeeld journaalnummers die worden gebruikt als onderdeel van een taak aangeven, opmerkingen toevoegen over een specifieke taak of een rapportbestand dat is afgedrukt voor een taak koppelen. Een pictogram weergegeven in de **bijlage** kolom voor de taak als een bijlage aanwezig is. 

De **taak voltooien** optie moet handmatig worden geselecteerd wanneer de taak is voltooid. Als een taak is gemarkeerd als voltooid, de **datum voltooid** veld wordt automatisch bijgewerkt op de huidige datum en tijd. Afhankelijkheid indicatoren worden ook zo nodig bijgewerkt.

## <a name="all-financial-period-close-tasks-list-page"></a>Lijstpagina Alle taken voor het afsluiten van de financiële periode
U kunt alle huidige en vorige periode sluiten taken weergeven van de **taken voor alle financiële periode sluiten** (lijstpagina). Deze pagina moet worden gebruikt voor een historische analyse van het afsluitingsproces omdat deze informatie over de geplande bevat einddatum, de werkelijke einddatum en de persoon die de taak voltooid. U kunt de informatie op deze lijstpagina eenvoudig exporteren naar Microsoft Excel voor rapportage en controledoeleinden.

## <a name="financial-period-close-configuration-page"></a>Pagina Configuratie van afgesloten financiële periode
Voordat u kunt de **financiële periode afsluiten** werkruimte, moet u het proces in Microsoft Dynamics 365 for Operations configureren met behulp van de **financiële periode sluiten configuratie** pagina. (Klik op **grootboek**&gt;**periode sluiten**&gt;**financiële periode sluiten configuratie**.)

### <a name="resources"></a>Bronnen

Op de **Resources** tabblad, definieert u de mensen die betrokken bij het afsluitingsproces zijn. Elke werknemer die verantwoordelijk is voor een taak afsluiten moet hier eerst worden toegewezen. U moet ook de weergave van de werkruimte van de werknemer opgeven. De volgende opties zijn beschikbaar:

-   **Alleen toegewezen taken** - De gebruiker ziet alleen de taken die aan hem of haar zijn toegewezen.
-   **Alle taken en statussen** - De gebruiker ziet alle afsluitingstaken en de status van het algehele proces.

Gebruikers die machtigingen hebben om alleen de aan hen toegewezen taken te bekijken kunnen geen taken toevoegen aan de takenlijst, bewerken of uit de takenlijst verwijderen.

### <a name="task-areas"></a>Taakgebieden

U gebruikt taakgebieden om afsluitingstaken te groeperen in logische gebieden van eigendom in uw organisatie. Leveranciers, Klanten of Grootboek kunnen bijvoorbeeld als taakgebieden worden gebruikt.

### <a name="calendars"></a>Kalenders

Maken en bewerken van financiële afsluiting kalenders met behulp van het tabblad kalenders.  Dit is waar u de werkdagen voor het afsluiten van processen definiëren en wordt gebruikt voor het plannen van afsluitingstaken.  Een nieuwe kalender maken en geef de werkdagen moet worden gebruikt voor het plannen van taken.  Het is raadzaam een kalender voor een lange periode, zoals een jaar of meerdere jaren maken omdat deze kan worden bewerkt nadat u hebt gemaakt.  Nadat de kalender is gemaakt, klikt u op de knop bewerken om het bijwerken van de kalender voor bepaalde dagen, zoals vrije dagen.  Afsluiten van de taken worden gepland op wanneer de waarde van het besturingselement is ingesteld op Open dagen.  Als taken afsluiten mag geen planning op een specifieke dag, hoeven die dag de waarde van het besturingselement ingesteld op afgesloten.

### <a name="templates"></a>Sjablonen

Met een financiële sluiten sjabloon kunt u alle taken die deel uitmaken van een afsluitingsproces definiëren. Een taak afsluiten is een terugkerende verricht werk die is toegewezen aan een persoon wilt uitvoeren als onderdeel van elk afsluitingsproces. In de sjabloon voor een relatieve vervaldatum datum moet worden gedefinieerd voor elke taak afsluiten. De relatieve vervaldatum datum is het aantal dagen vóór of na het einde van de gedefinieerde periode datum op waarop de taak moet worden betaald per periode. Een vervaltijd wordt ook toegewezen aan elke taak. De vervaltijd wordt ingesteld via de context van uw tijdzone en worden geconverteerd naar de tijdzone voor elke gebruiker. 

U kunt een taak in de sjabloon kunt toewijzen aan een of meer bedrijven waar deze taak is van toepassing. Als een andere persoon is toegewezen wilt uitvoeren om dat werk te doen in elk bedrijf, is het mogelijk handig meerdere taken maken voor dezelfde werkzaamheden. Maak een taak voor elk bedrijf. 

De **taakkoppeling** menu-item is gekoppeld aan de taak verricht werk en Ga rechtstreeks naar de bewuste pagina via de taakkoppeling in de werkruimte kan worden gebruikt. Bijvoorbeeld een taak afsluiten herwaarderingsproces voor de valuta voor leveranciers kan worden gekoppeld aan de bijbehorende **herwaardering van vreemde valuta** pagina in Microsoft Dynamics 365 voor bewerkingen. U kunt ook koppelen aan een externe URL. 

> [! Hint] als u wilt dat een specifiek Management Reporter rapport koppelen aan een financiële periode sluiten taak, kunt u de rapport-URL. Open het rapport in de report designer voor toegang tot de rapport-URL en klik vervolgens op **bestand**&gt;**rapport weergeven** het rapport wilt openen in een webbrowser. U kunt de URL vervolgens kopiëren in de adresbalk van de browser en deze in het veld **Taakkoppeling** **URL** plakken. 

Afhankelijkheden van taken kunt u definiëren in de sjabloon. Als een taak is ingesteld, is afhankelijk van een of meer taken, kan deze taak kan niet worden gemarkeerd als voltooid totdat alle afhankelijkheden zijn voltooid. 

U kunt meerdere financiële sluiten sjablonen maken. Vervolgens kunt u de verschillende sjablonen voor het bijhouden van het afsluitingsproces voor verschillende periodetypen, zoals het einde van de maand of het einde van het jaar, of voor het bijhouden van bedrijven die gebruikmaken van verschillende afsluitingsproces. Nadat u een sjabloon hebt gemaakt, kunt u naar een nieuwe sjabloon kopiëren en de vereiste wijzigingen aanbrengen. U kunt slechts één sjabloon toewijzen aan elke planning afsluiting.

### <a name="closing-schedules"></a>Afsluitingsplanningen

Met de planning van een afsluiting kunt u een sjabloon voor financiële sluiten toewijzen aan een specifieke financiële periode die moet worden gesloten. De taken uit de sjabloon vervolgens automatisch worden gegenereerd voor de opgegeven periode en het afsluiten van de nieuwe planning wordt toegevoegd aan de werkruimte. Wanneer u een nieuwe planning van de afsluiting, maakt de **periode-einddatum** veld wordt gebruikt om te bepalen van de werkelijke vervaldatum voor de afsluitingstaken, op basis van de relatieve vervaldatum datum die is toegewezen in de sjabloon voor financiële sluiten. 

De kalender die geschikt zijn voor de planning van de afsluiting, om aan te geven van de werkdagen moet worden gebruikt bij het plannen van de taak toewijzen. Als u een specifieke kalender niet definieert, de einddatum voor de taak wordt datums gebruiken alle dagen van de week. 

U moet ook de bedrijven die gekoppeld aan de afsluiting planning zijn definiëren. Als de sjabloon taken zijn toegewezen aan meerdere bedrijven, afzonderlijke taken gemaakt voor elk bedrijf dat in de planning van de afsluiting en toegewezen aan de taak van de sjabloon. 

Nadat een afsluiting planning is voltooid, schakelt u het **afgesloten** optie is. De geschiedenis van taken nog steeds beschikbaar via de **taken voor alle financiële periode sluiten** (lijstpagina), maar de planning van de afsluiting wordt verwijderd uit de werkruimte. Nadat een afsluiting-schema is gemarkeerd als **afgesloten**, niet mogelijk op taken aan toe te voegen, bewerken, taken of taken verwijderen uit het.



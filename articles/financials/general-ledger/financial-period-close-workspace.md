---
title: "Werkgebied voor afsluiten van financiële periode"
description: "Dit artikel geeft een overzicht van het werkgebied Afgesloten financiële periode en de bijbehorende configuratie."
author: twheeloc
manager: AnnBe
ms.date: 11/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b999fd3c26304b81f24389a83faf73e1658c39b3
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="financial-period-close-workspace"></a>Werkgebied voor afsluiten van financiële periode

[!INCLUDE [banner](../includes/banner.md)]

Dit artikel geeft een overzicht van het werkgebied Afgesloten financiële periode en de bijbehorende configuratie.

Werkgebied voor afsluiten van financiële periode

Met het werkgebied **Afgesloten financiële periode** kunt u uw financiële afsluitingsprocessen voor bedrijven, gebieden en personen bijhouden. Afhankelijk van uw weergave van het werkgebied **Afgesloten financiële periode** ziet u alle taken en statussen voor een afsluitingsplanning, of alleen de taken die aan u zijn toegewezen. 

U moet eerst een afsluitingsplanning boven in het werkgebied selecteren. Alle gegevens die worden weergegeven in het werkgebied, worden vervolgens gefilterd op de geselecteerde afsluitingsplanning.

### <a name="summary-tiles"></a>Overzichtstegels

De tegel **Overzicht** biedt een overzicht van het proces en indicatoren helpen u het afsluitingsproces op schema te houden. U ziet achterstallige taken, resterende taken voor vandaag, taken die vandaag moeten worden uitgevoerd, maar worden geblokkeerd vanwege afhankelijkheden en alle resterende taken voor het proces. Deze informatie is bestemd voor alle bedrijven die zijn opgenomen in de geselecteerde afsluitingsplanning.

### <a name="tasks-and-status-section"></a>Sectie Taken en status

In de sectie **Taken en status** wordt de status van de algehele afsluitingsplanning op verschillende manieren gespecificeerd: status per bedrijf, status per gebied en status per persoon die verantwoordelijk is. U kunt de status weergeven voor alle taken in de afsluitingsplanning, voor alleen taken die vandaag vervallen of voor taken waarvan de vervaldatum is verlopen, door het filter boven aan de lijst met kaarten te wijzigen. U kunt ook het bedrijfsfilter selecteren om de status voor een specifiek bedrijf weer te geven. Elk statustabblad geeft een specificatie op basis van percentage voltooid en het aantal taken dat resteert. Klik op de kaart of de actie **Details weergeven** om de gedetailleerde takenlijst te filteren op de geselecteerde kaart. 

Het laatste tabblad is voor de gedetailleerde takenlijst. In deze lijst wordt de volledige takenlijst weergegeven. Deze kan worden gefilterd zodat alleen de taken worden weergegeven waarin u geïnteresseerd bent. U kunt de lijst met taken op verschillende manieren filteren. U kunt bijvoorbeeld filteren op vervaldatum van taak, gekoppeld bedrijf en gekoppeld gebied. U kunt ook aangeven of de voltooide taken in de lijst met taken moeten worden weergegeven of verborgen. 

Twee indicatoren worden gebruikt voor taken:

-   Een uitroepteken geeft aan dat de taak achterstallig is. Voor taken die achterstallig zijn, wordt de vervaldatum bovendien in rood gemarkeerd.
-   Een hangslot geeft aan dat de taak afhankelijk is van andere taken die nog niet zijn uitgevoerd. Een taak die wordt geblokkeerd door afhankelijkheden, kan niet als voltooid worden gemarkeerd. U kunt afhankelijkheden voor een taak instellen met behulp van de actie **Afhankelijkheid instellen**.

De taaknaam is een hyperlink naar de Microsoft Dynamics 365 for Operations-pagina of een andere webpagina waar de gebruiker naartoe moet gaan om het werk uit te voeren. U kunt deze hyperlink instellen met behulp van het veld **Taakkoppeling** wanneer u een taak maakt of bewerkt. 

U kunt bestanden, notities, afbeeldingen en URL's aan een taak koppelen met behulp van de actie **Bijlagen**. U kunt bijvoorbeeld journaalnummers aangeven die worden gebruikt als onderdeel van een taak, u kunt opmerkingen toevoegen over een specifieke taak of u kunt een rapportbestand koppelen dat voor een taak is afgedrukt. Er verschijnt een pictogram in de kolom **Bijlage** voor de taak als er een bijlage aanwezig is. 

De optie **Taak voltooid** moet handmatig worden geselecteerd nadat de taak is voltooid. Als een taak wordt gemarkeerd als voltooid, wordt het veld **Datum van voltooiing** automatisch bijgewerkt in de huidige datum en tijd. Afhankelijkheidsindicatoren worden ook zo nodig bijgewerkt.

## <a name="all-financial-period-close-tasks-list-page"></a>Lijstpagina Alle taken voor het afsluiten van de financiële periode
U kunt alle huidige en vorige taken voor het afsluiten van de periode weergeven via de lijstpagina **Alle taken voor het afsluiten van de financiële periode**. Deze lijstpagina kan het beste worden gebruikt voor een historische analyse van het afsluitingsproces omdat deze informatie over de geplande vervaldatum bevat, de werkelijke voltooiingsdatum en de persoon die de taak heeft voltooid. U kunt de informatie op deze lijstpagina eenvoudig exporteren naar Microsoft Excel voor rapportage- en controledoeleinden.

## <a name="financial-period-close-configuration-page"></a>Pagina Configuratie van afgesloten financiële periode
Voordat u het werkgebied **Afgesloten financiële periode** kunt gebruiken, moet u het proces in Microsoft Dynamics 365 for Finance and Operations configureren via de pagina **Configuratie van afgesloten financiële periode**. (Klik op **Grootboek** &gt; **Afgesloten periode** &gt; **Configuratie van afgesloten financiële periode**.)

### <a name="resources"></a>Bronnen

Op het tabblad **Resources** definieert u de mensen die betrokken zijn bij het afsluitingsproces. Elke werknemer die verantwoordelijk is voor een afsluitingstaak, moet hier eerst worden toegewezen. U moet ook de weergave van het werkgebied van de werknemer opgeven. De volgende opties zijn beschikbaar:

-   **Alleen toegewezen taken** - De gebruiker ziet alleen de taken die aan hem of haar zijn toegewezen.
-   **Alle taken en statussen** - De gebruiker ziet alle afsluitingstaken en de status van het algehele proces.

Gebruikers die machtigingen hebben om alleen de aan hen toegewezen taken te bekijken kunnen geen taken toevoegen aan de takenlijst, bewerken of uit de takenlijst verwijderen.

### <a name="task-areas"></a>Taakgebieden

U gebruikt taakgebieden om afsluitingstaken te groeperen in logische gebieden van eigendom in uw organisatie. Leveranciers, Klanten of Grootboek kunnen bijvoorbeeld als taakgebieden worden gebruikt.

### <a name="calendars"></a>Kalenders

Maak en bewerk financiële afsluitingskalenders met het tabblad Kalenders. Op dit tabblad definieert u de werkdagen voor afsluitingsprocessen en plant u afsluitingstaken.  Maak een nieuwe kalender en geef het aantal werkdagen aan dat moet worden gebruikt voor het plannen van taken.  U kunt het beste een kalender maken voor een lange periode, zoals een jaar of meerdere jaren. De kalender kan namelijk worden bewerkt nadat u deze hebt gemaakt.  Nadat de kalender is gemaakt, klikt u op de knop Bewerken om de kalender bij te werken voor bepaalde dagen, zoals vrije dagen.  Afsluitingstaken worden gepland op dagen waarop de waarde Controle is ingesteld op Open.  Als afsluitingstaken niet op een specifieke dag moeten worden ingepland, moet voor die dag de waarde Controle zijn ingesteld op Afgesloten.

### <a name="templates"></a>Sjablonen

U gebruikt een sjabloon voor financiële afsluiting om alle taken te definiëren die deel uitmaken van een afsluitingsproces. Een afsluitingstaak is een terugkerende werkinspanning die aan een persoon is toegewezen voor uitvoering als onderdeel van elk afsluitingsproces. In de sjabloon moet voor elke afsluitingstaak een relatieve vervaldatum worden gedefinieerd. De relatieve vervaldatum is het aantal dagen vóór of na de gedefinieerde periode-einddatum waarop de taak elke periode vervalt. Er wordt ook een vervaltijd aan elke taak toegewezen. De vervaltijd wordt ingesteld met behulp van de context van uw tijdzone en wordt naar de tijdzone voor elke gebruiker geconverteerd. 

U kunt een taak in de sjabloon toewijzen aan een of meer bedrijven waar deze taak van toepassing is. Als een andere persoon wordt toegewezen om die werkzaamheden in elk bedrijf te verrichten, is het mogelijk handig meerdere taken te maken voor dezelfde werkzaamheden. Maak een taak voor elk bedrijf. 

De menuoptie **Taakkoppeling** wordt gekoppeld aan de taakwerkinzet en kan worden gebruikt om rechtstreeks naar de gekoppelde pagina te gaan via de taakkoppeling in het werkgebied. Zo kan een afsluitingstaak om het herwaarderingsproces voor valuta uit te voeren voor leveranciers worden gekoppeld aan de bijbehorende pagina **Herwaardering van vreemde valuta** in Microsoft Dynamics 365 for Finance and Operations. U kunt ook koppelen aan een externe URL. 

> [!TIP]
> Als u een bepaald Management Reporter-rapport wilt koppelen aan een taak voor het afsluiten van de financiële periode, kunt u de rapport-URL gebruiken. Om de rapport-URL te openen, opent u het rapport in de rapportontwerper en klikt u op **Bestand** &gt; **Rapport weergeven** om het rapport in een webbrowser te openen. U kunt de URL vervolgens kopiëren in de adresbalk van de browser en deze in het veld **Taakkoppeling** **URL** plakken. 

U kunt taakafhankelijkheden definiëren in de sjabloon. Als een taak is ingesteld om afhankelijk te zijn van een of meer taken, kan deze taak niet als voltooid worden gemarkeerd voordat alle afhankelijkheden zijn voltooid. 

U kunt meerdere sjablonen voor financiële afsluiting maken. Vervolgens kunt u de verschillende sjablonen gebruiken om de afsluitingsprocessen te traceren voor verschillende periodetypen, zoals het einde van de maand of het einde van het jaar, of om bedrijven te traceren die gebruikmaken van verschillende afsluitingsprocessen. Nadat u één sjabloon hebt gemaakt, kunt u deze naar een nieuwe sjabloon kopiëren en de vereiste wijzigingen aanbrengen. U kunt slechts één sjabloon toewijzen aan elke afsluitingsplanning.

### <a name="closing-schedules"></a>Afsluitingsplanningen

Met de planning van een afsluiting kunt u een sjabloon voor financiële afsluiting toewijzen aan een specifieke financiële periode die moet worden afgesloten. De taken uit de sjabloon worden vervolgens automatisch gegenereerd voor de opgegeven periode en de nieuwe afsluitingsplanning wordt aan het werkgebied toegevoegd. Wanneer u een nieuwe afsluitingsplanning maakt, wordt het veld **Einddatum van periode** gebruikt om de werkelijke vervaldatums voor de afsluitingstaken te bepalen op basis van de relatieve vervaldatum die is toegewezen in de sjabloon voor financiële afsluiting. 

Wijs de kalender aan die geschikt is voor de planning van de afsluiting om de werkdagen aan te geven die moeten worden gebruikt bij de taakplanning. Als u geen specifieke kalender definieert, worden voor de vervaldatums van de taak alle dagen van de week gebruikt. 

U moet ook de bedrijven definiëren die worden gekoppeld aan de afsluitingsplanning. Als sjabloontaken worden toegewezen aan meerdere bedrijven, worden er afzonderlijke taken gemaakt voor elk bedrijf dat zich in de afsluitingsplanning bevindt en worden deze toegewezen aan de sjabloontaak. 

Nadat een afsluitingsplanning is voltooid, schakelt u de optie **Afgesloten** in. De taakhistorie blijft nog steeds beschikbaar via de lijstpagina **Alle taken voor het afsluiten van de financiële periode**, maar de afsluitingsplanning wordt verwijderd uit het werkgebied. Nadat een afsluitingsplanning is gemarkeerd als **Afgesloten**, kunt u er mogelijk geen taken aan toevoegen, taken bewerken of taken eruit verwijderen.





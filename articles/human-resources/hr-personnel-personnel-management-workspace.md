---
title: Werkgebied voor personeelsbeheer
description: In dit onderwerp worden de conceptelementen van het werkgebied voor personeelsbeheer beschreven.
author: andreabichsel
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3cb86f33e437a4f1fed4acf894c9bf48d6d5b1ef
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2021
ms.locfileid: "6333118"
---
# <a name="personnel-management-workspace"></a>Werkgebied voor personeelsbeheer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Het werkgebied **Personeelsbeheer** bevat een grote hoeveelheid inhoud. Het bevat personeelsverplaatsingen, het houdt werknemerswijzigingen, openstaande posities, adreswijzigingen, verlopende records en analyses bij en biedt koppelingen naar specifieke informatie. Dit onderwerp bevat gedetailleerde informatie over elk onderdeel van het werkgebied.

## <a name="activity-tab"></a>Tabblad Activiteit

Het tabblad **Activiteit** bevat secties waarin werknemers worden gegroepeerd op basis van hun fase in het arbeidsproces:

- Kandidaten om in dienst te nemen
- Start binnenkort
- Recente aanstellingen
- Afsluiten
- Vertrokken

Wanneer een werknemer zich in een van deze fasen bevindt, zijn specifieke acties beschikbaar als een knop op de kaart of in het menu dat verschijnt wanneer u het weglatingsteken (**...**) selecteert in de rechterbovenhoek. In de volgende subsecties worden de secties van het tabblad **Activiteit** beschreven en worden de beschikbare acties weergegeven.

### <a name="candidates-to-hire"></a>Kandidaten om in dienst te nemen

De sectie **Aan te stellen kandidaten** van het werkgebied wordt gevuld vanuit meerdere bronnen:

- Een OData-entiteit (Open Data Protocol)
- LinkedIn-integratie
- Gegevens die handmatig in het product worden ingevoerd

Wanneer de kandidaten in de sectie **Aan te stellen kandidaten** verschijnen, kunt u de volgende acties uitvoeren door het weglatingsteken op de kandidaatkaart te selecteren:

- Kandidaat negeren
- Niet in dienst nemen
- Aanstellen

> [!NOTE]
> Als de kandidatenlijst wordt ingevuld vanuit Microsoft Dataverse, worden dezelfde kandidaten weergegeven voor alle rechtspersonen, omdat er geen rechtspersoon aan de kandidaat is gekoppeld.

### <a name="starting-soon"></a>Start binnenkort

In de sectie **Begint binnenkort** worden werknemers vermeld die een begindatum in de toekomst hebben. De lijst wordt op begindatum gesorteerd. De begindatum die het dichtst bij de gegevens van vandaag ligt, wordt als eerste vermeld.

Als de manager niet op de kaart staat, is er geen positie toegewezen voor de medewerker.

> [!NOTE] 
> Het is raadzaam om een positie aan een medewerker toe te wijzen voordat u een controlelijst toewijst, omdat opnboardingtaken soms worden toegewezen aan de manager van een nieuwe werknemer. Als er echter geen positie is toegewezen, kan de manager van de nieuwe werknemer niet worden bepaald. In dat geval worden de onboardingtaken die voor de manager zijn bedoeld aan de eigenaar van de controlelijst toegewezen.

Wanneer medewerkers worden weergegeven in de sectie **Begint binnenkort**, zijn de volgende acties beschikbaar voor hen:

- Positie toewijzen
- Dienstverband controleren
- Vaste compensatie toewijzen
- Variabele compensatie toewijzen
- Weergeven in hiërarchie
- Controlelijst toepassen\*\*

\*\* Deze actie is de standaardactie. Deze wordt als knop op de kaart weergegeven.

### <a name="recent-hires"></a>Recente aanstellingen

In de sectie **Recent aangenomen werknemers** worden medewerkers vermeld die een begindatum in het recente verleden hebben. De lijst wordt op begindatum gesorteerd. De begindatum die het dichtst bij de datum van vandaag ligt, wordt als eerste vermeld.

De lijst bevat standaard medewerkers die in de afgelopen zeven dagen in dienst zijn genomen. Als u deze instelling wilt wijzigen, definieert u op de pagina **Human Resources-parameter** op het tabblad **Algemeen** een periode voor **Recent aangenomen werknemers**. De gegevens in de sectie **Recent aangenomen werknemers** kunnen worden weergegeven voor een bepaald aantal dagen, maanden of jaren. Als u bijvoorbeeld de lijst wilt weergeven met werknemers die in de afgelopen 14 dagen zijn aangenomen, stelt u het veld **Periode** in op **14** en stelt u het veld **Eenheid** in op **Dagen**.

> [!NOTE]
> De instellingen op de pagina **Human resources-parameters** zijn bedrijfsspecifiek. Daarom kan de periode waarvoor u recent aangenomen werknemers bekijkt verschillen per bedrijf. In het bedrijf USMF wilt u bijvoorbeeld mogelijk alle nieuwe werknemers van de laatste zeven dagen weergeven. In het bedrijf USSI wilt u echter alle nieuwe werknemers van de laatste 14 dagen weergeven. In dit geval moet u de pagina **Human resources-parameters** openen in elk bedrijf en de parameters zo nodig instellen.

Als de manager niet op de kaart staat, is er geen positie toegewezen voor de medewerker.

Wanneer medewerkers worden weergegeven in de sectie **Recent aangenomen werknemers**, zijn de volgende acties beschikbaar voor hen:

- Positie toewijzen
- Dienstverband controleren
- Vaste compensatie
- Variabele compensatie toewijzen
- Weergeven in hiërarchie
- Controlelijst toepassen\*\*

\*\* Deze actie is de standaardactie. Deze wordt als knop op de kaart weergegeven.

### <a name="exiting"></a>Afsluiten

In de sectie **Vertrekkende werknemers** worden medewerkers vermeld die een beëindigingsdatum in de toekomst hebben. De lijst wordt op beëindigingsdatum gesorteerd. De beëindigingsdatum die het dichtst bij de datum van vandaag ligt, wordt als eerste vermeld. 

De lijst bevat standaard mederwerkers met een beëindigingsdatum in de komende zeven dagen. Als u deze instelling wilt wijzigen, definieert u op de pagina **Human Resources-parameter** op het tabblad **Algemeen** een periode voor **Weergaven van vertrekkende werknemers**. De gegevens in de sectie **Vertrekkende werknemers** kunnen worden weergegeven voor een bepaald aantal dagen, maanden of jaren. Als u bijvoorbeeld de lijst wilt weergeven met werknemers die in de komende 14 dagen worden beëindigd, stelt u het veld **Periode** in op **14** en stelt u het veld **Eenheid** in op **Dagen**.

Wanneer medewerkers worden weergegeven in de sectie **Vertrekkende werknemers**, zijn de volgende acties beschikbaar voor hen:

- Controlelijst toepassen\*\*
- Dienstverband controleren
- Weergeven in hiërarchie

\*\* Deze actie is de standaardactie. Deze wordt als knop op de kaart weergegeven.

### <a name="exited"></a>Vertrokken

In de sectie **Vertrokken werknemers** worden medewerkers vermeld die een beëindigingsdatum in het recente verleden hebben. De lijst wordt op beëindigingsdatum gesorteerd. De beëindigingsdatum die het dichtst bij de datum van vandaag ligt, wordt als eerste vermeld.

De lijst bevat standaard mederwerkers met een beëindigingsdatum in de afgelopen zeven dagen. Als u deze instelling wilt wijzigen, definieert u op de pagina **Human Resources-parameter** op het tabblad **Algemeen** een periode voor **Weergaven van vertrokken werknemers**. De gegevens in de sectie **Vertrokken werknemers** kunnen worden weergegeven voor een bepaald aantal dagen, maanden of jaren. Als u bijvoorbeeld de lijst wilt weergeven met werknemers die in de afgelopen 14 dagen zijn beëindigd, stelt u het veld **Periode** in op **14** en stelt u het veld **Eenheid** in op **Dagen**.

Wanneer medewerkers worden weergegeven in de sectie **Vertrokken werknemers**, zijn de volgende acties beschikbaar voor hen:

- Controlelijst toepassen\*\*
- Dienstverband controleren
- Weergeven in hiërarchie

\*\* Deze actie is de standaardactie. Deze wordt als knop op de kaart weergegeven.

## <a name="employee-changes-tab"></a>Tabblad Werknemerwijzigingen

Op het tabblad **Werknemerwijzigingen** staat een lijst met alle personeelsacties van medewerkers. Deze lijst is niet standaard beschikbaar. Als u deze functie wilt inschakelen, stelt u op de pagina **Gedeelde Human Resources-parameters**, op het tabblad **Personeelsacties**, de optie **Werknemeracties** in op **Ja**.

Zie (Koppeling naar de pagina Personeelsacties) voor meer informatie over personeelsacties.

## <a name="position-changes-tab"></a>Tabblad Positiewijzigingen

Op het tabblad **Positiewijzigingen** staat een lijst met alle personeelsacties van posities. Deze lijst is niet standaard beschikbaar. Als u deze functie wilt inschakelen, stelt u op de pagina **Gedeelde Human Resources-parameters**, op het tabblad **Personeelsacties**, de optie **Positieacties inschakelen** in op **Ja**.

Zie (Koppeling naar de pagina Personeelsacties) voor meer informatie over personeelsacties.

## <a name="open-positions-tab"></a>Tabblad Openstaande posities

Op het tabblad **Openstaande posities** worden alle openstaande posities weergegeven. Posities moeten een activeringsdatum van vandaag of eerder hebben en mogen niet over een huidige werknemertoewijzing gaan om te worden weergegeven in de lijst.

> [!NOTE]
> In de lijst wordt rekening houden met de werknemertoewijzing vanaf vandaag. Elke positie met een toekomstige werknemertoewijzing blijft in de lijst staan. Nadat de ingangsdatum van de werknemertoewijzing is bereikt, wordt de positie echter uit de lijst verwijderd.

## <a name="expiring-records-tab"></a>Tabblad Verlopende records

Op het tabblad **Verlopende records** worden alle artikelen weergegeven die zijn verlopen of zullen verlopen voor de medewerkers in het bedrijf waarin de gebruiker is aangemeld. De volgende items worden weergegeven in de lijst:

- Getuigschriften
- Id
- Proeftijd
- Screenings
- Tests

Als u wilt opgeven of in de lijst verlopen records of verlopende records worden weergegeven, definieert u op de pagina **Human resources-parameters** op het tabblad **Algemeen** een periode voor **Verlopende records** of **Verlopen records**. De gegevens op het tabblad **Verlopende records** kunnen worden weergegeven gedurende een bepaald aantal dagen. Als u bijvoorbeeld de lijst met records wilt weergeven die vervallen in de volgende 14 dagen, stelt u het veld **Aantal dagen** in op **14**.

> [!NOTE] 
> Als u de periode voor **Verlopen records** of **Verlopende records** instelt op **0** op de pagina **Human resources-parameters**, worden die records niet weergegeven in de lijst.

## <a name="employees-tile"></a>Tegel Werknemers

De tegel **Werknemers** geeft het aantal werknemers aan dat in dienst is bij het bedrijf waar de gebruiker momenteel is aangemeld. Wanneer u de tegel **Werknemers** selecteert, wordt er een nieuwe pagina weergegeven met de details van de werknemers.

## <a name="contractors-tile"></a>Tegel Contractanten

De tegel **Contractanten** geeft het aantal contractanten aan dat is aangesteld door het bedrijf waar de gebruiker momenteel is aangemeld. Wanneer u de tegel **Contractanten** selecteert, wordt er een nieuwe pagina weergegeven met de details van de contractanten.

## <a name="open-positions-tile"></a>Tegel Openstaande posities

De tegel **Openstaande posities** bevat een telling van alle openstaande posities. Wanneer u de tegel **Openstaande posities** selecteert, wordt er een nieuwe pagina weergegeven met de details van de openstaande posities. Posities moeten een activeringsdatum van vandaag of eerder hebben en mogen niet over een huidige werknemertoewijzing gaan om te worden opgenomen in de telling.

> [!NOTE]
> In de tegel wordt rekening houden met de werknemertoewijzing vanaf vandaag. Elke positie met een toekomstige werknemertoewijzing blijft deel uitmaken van de telling. Nadat de ingangsdatum van de werknemertoewijzing is bereikt, wordt de positie echter uit de telling verwijderd.

## <a name="approvals-tile"></a>Tegel Goedkeuringen

De tegel **Goedkeuringen** bevat een telling van alle werkstroomitems die nog moeten worden goedgekeurd door de huidige gebruiker. Wanneer u de tegel **Goedkeuringen** selecteert, ziet u op een nieuwe pagina de details van de werkstroomitems die uw goedkeuring vereisen.

## <a name="address-changes-tile"></a>Tegel Adreswijzigingen

De tegel **Adreswijzigingen** bevat een telling van alle adreswijzigingen die hebben plaatsgevonden gedurende het aantal dagen dat is opgegeven op de pagina **Human resources-parameters**. Wanneer u de tegel **Adreswijzigingen** selecteert, worden op een nieuwe pagina de details van eventuele adreswijzigingen weergegeven. In de rechterbovenhoek van de pagina kunt u **Toekomstige adreswijzigingen opnemen** selecteren om adreswijzigingen met een toekomstige datum weer te geven.

Zie [Adreswijzigingen weergeven en beheren](hr-personnel-view-address-changes.md) voor meer informatie over het weergeven en beheren van adreswijzigingen.

---
title: De rol van verzuimmanager configureren
description: In dit onderwerp wordt uitgelegd hoe u de rol van verzuimmanager kunt instellen voor het beheren van werknemersverzuim.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e7865a0bb33944c803c628f94371a4c75cc38bd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693026"
---
# <a name="configure-the-absence-manager-role"></a>De rol van verzuimmanager configureren

>[!Important]
>De functionaliteit die in dit onderwerp wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In sommige organisaties beheren peoplemanagers het verlof voor hun team mogelijk niet. In plaats daarvan kan een verzuimmanager dit proces voor teamleden op meerdere afdelingen en in meerdere teams verwerken. Verzuimmanagers hebben de volgende mogelijkheden voor verlofbeheer:

- Verlof beoordelen en goedkeuren op basis van een alternatieve hiërarchie.
- Saldi van teamleden weergeven.
- De verzuimkalender weergeven.

## <a name="turn-on-the-feature"></a>De functie inschakelen

1. Selecteer in de werkruimte **Systeembeheer** de optie **Functiebeheer**.

2. Schakel op het tabblad **Functiebeheer** de functie **Verlof laten beheren door een verzuimmanager** in.

## <a name="define-a-custom-hierarchy"></a>Een aangepaste hiërarchie definiëren

De functionaliteit voor verzuimbeheer maakt gebruik van een aangepaste hiërarchie die moet worden geconfigureerd.

1. Selecteer in de werkruimte **Organisatiebeheer** de optie **Positiehiërarchietypen**.

2. Maak een positiehiërarchietype met de naam **Verlof**.

3. Selecteer in de werkruimte **Verlof en verzuim** onder **Koppelingen** de optie **Parameters voor verlof en verzuim**.

4. Selecteer op het tabblad **Algemeen** in de vervolgkeuzelijst **Verzuimhiërarchie** het hiërarchietype **Verlof** dat u eerder hebt gemaakt. Deze koppeling van verlofhiërarchie moet worden voltooid voor elke rechtspersoon waar de functionaliteit van verzuimbeheer wordt gebruikt.

Nadat het hiërarchietype is gedefinieerd, moet het positiehiërarchierapport aan de positie worden toegewezen.

1. Selecteer in de werkruimte **Organisatiebeheer** de optie **Alle posities**.

2. Selecteer de positie waaraan u de verlofhiërarchie wilt toevoegen.

3. Selecteer **Toevoegen** op het tabblad **Relaties**.

4. Selecteer **Verlof** in het veld **Hiërarchienaam**.

5. Selecteer een positie in het veld **Verantwoording aan positie**. De naam van de werknemer wordt automatisch ingevuld nadat u een positie hebt geselecteerd.

## <a name="assign-the-absence-manager-role-to-a-user"></a>De rol van verzuimmanager aan een gebruiker toewijzen

De rol van verzuimmanager moet aan werknemers worden toegewezen om verlofaanvragen goed of af te keuren.

1. Selecteer **Koppelingen** in de werkruimte **Systeembeheerder**.

2. Selecteer de koppeling **Gebruikers** in de sectie **Gebruikers**.

3. Selecteer in de lijst met gebruikers de gebruiker aan wie u de rol van verzuimmanager wilt toewijzen.

4. Selecteer op het tabblad **Rol van gebruiker** de optie **Rollen toewijzen**.

5. Selecteer de rol **Verzuimmanager** in de lijst. Selecteer vervolgens **OK**.

    > [!IMPORTANT]
    > Zorg ervoor dat de rol van werknemer eveneens is toegewezen aan de gebruiker aan wie u de rol van verzuimmanager toewijst. Anders kan de werknemer de functie niet gebruiken.

6. Nadat u de verlofhiërarchie hebt gemaakt, kunt u deze weergeven door de volgende stappen uit te voeren:

    1. Selecteer in de werkruimte **Organisatiebeheer** de optie **Positiehiërarchie**.
    
    2. Selecteer **Verlof** in het veld **Hiërarchietype**.

## <a name="absence-manager-workspace"></a>Werkgebied verzuimbeheer

In de werkruimte **Selfservice werknemer** worden op het tabblad **Verlofbeheer** de verzuimgegevens weergegeven over de werknemers die aan de verzuimmanager zijn toegewezen in de verlofhiërarchie. De verzuimmanager heeft verschillende opties tot zijn of haar beschikking: 
 - Verlofaanvragen beoordelen.</br>
 - Een aanvraag voor verlof indienen namens een werknemer.</br>
 - Alle werknemers weergeven die aan hem of haar zijn toegewezen als onderdeel van de verlofhiërarchie.</br>
 - De kalender voor verzuimbeheer weergeven.</br>

De werkruimte **Verlofbeheer** bevat twee tabbladen:
 - **Verlofaanvragen**: op dit tabblad worden alle verlofaanvragen weergegeven die in behandeling zijn en kunnen worden goedgekeurd door de verzuimmanager. De verzuimmanager kan meerdere records selecteren en er tegelijkertijd actie voor ondernemen. Als de verlofweergave voor meerdere bedrijven is ingeschakeld, worden in deze lijst de in behandeling zijnde verlofaanvragen weergegeven voor alle rechtspersonen tot wie ze toegang hebben. Anders worden de in behandeling zijnde verlofaanvragen voor de geselecteerde rechtspersoon vermeld. </br>
 - **Alle werknemers**: op dit tabblad worden alle werknemers weergegeven die zijn toegewezen aan de verzuimmanager in de verlofhiërarchie. Er zijn voor elke werknemer enkele opties beschikbaar:
    - **Verlof aanvragen** - Een nieuwe verlofaanvraag indienen voor de geselecteerde werknemer.</br>
    - **Verlof**: geef saldi, goedgekeurd verlof en verlofaanvragen weer voor de geselecteerde werknemer.</br>

## <a name="approve-time-off-requests"></a>Verlofaanvragen goedkeuren

Verzuimmanagers kunnen verlofaanvragen voor werknemers goed- of afkeuren. 

> [!IMPORTANT]
> Voordat verzuimmanagers verlofaanvragen kunnen goed- of afkeuren, moet de werkstroom voor verlofaanvragen zijn geconfigureerd om werkitems voor verlofaanvragen aan hen toe te wijzen ter beoordeling.
>
> 1. Selecteer of maak de werkstroom voor verlofaanvragen op de pagina **Werkstromen voor Human Resources**.
> 2. Selecteer de optie **Hiërarchie koppelen** en selecteer vervolgens **Verlof** in het veld **Hiërarchienaam**.
> 3. Werk de werkstroom bij in de werkstroomontwerper. Selecteer onder **Toewijzingstype** de optie **Hiërarchie** en selecteer vervolgens **Configureerbare hiërarchie** op het tabblad **Hiërarchieselectie**.
>
> Zie [Een werkstroom voor een verlofaanvraag maken](hr-leave-and-absence-workflow.md) voor meer informatie over het maken van de werkstroom voor verlofaanvragen.

1. Selecteer in de werkruimte **Selfservice werknemer** het tabblad **Verlofbeheer**.

2. Selecteer op het tabblad **Verlofaanvragen** de verlofaanvragen waar u actie op wilt ondernemen. U kunt in deze lijstweergave meerdere records selecteren.

3. Met de actieknoppen boven aan het raster kunt u een verlofaanvraag goedkeuren, weigeren of delegeren. 

De gebruiker kan ook de tegel voor **verlofaanvragen** aan de linkerkant gebruiken om naar de lijst met alle werkitems met verlofaanvragen te navigeren. 

## <a name="view-time-off-in-the-calendar"></a>Verlof op de kalender bekijken

Gebruikers met de rol van verzuimmanager kunnen verlofaanvragen op hun kalender bekijken. Voer deze stappen uit om toegang tot de verlofkalender te krijgen.

> [!IMPORTANT]
> Een systeembeheerder moet de weergaveopties configureren voor de kalender van de verzuimmanager. Op de pagina **Verlof- en verzuimparameters** op het tabblad **Kalender** kunt u verjaardagen, verzuim zonder details, verlof en uitstaande verlofaanvragen verbergen of weergeven. Er is ook een optie om de kalenderweergaveoptie te filteren op werknemertype.

1. Selecteer in de werkruimte **Selfservice werknemer** **Verlofbeheer** en vervolgens **Kalender verzuimmanager**.

2. Voer in het veld **Datum** de gewenste datum in.

3. Werk waar nodig de weergaveopties bij.

De kalender van de verzuimmanager bevat alle records voor de werknemers die rapporteren aan de verzuimmanager in de verlofhiërarchie.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Een werkstroom voor verlofaanvragen maken](hr-leave-and-absence-workflow.md)
- [Team- en bedrijfsagenda's weergeven](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

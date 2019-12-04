---
title: Vragenlijsten plannen en distribueren
description: In dit onderwerp wordt uitgelegd hoe u de vragenlijsten die u ontwerpt kunt distribueren, zodat ze beschikbaar zijn voor de persoon of groep personen die de lijsten gaat invullen.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 242e9fd5fd4b22f3081367cf33ff18ff5e4174a5
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814738"
---
# <a name="distribute-and-schedule-questionnaires"></a>Vragenlijsten plannen en distribueren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de vragenlijsten die u ontwerpt kunt distribueren, zodat ze beschikbaar zijn voor de persoon of groep personen die de lijsten gaat invullen. 

Er zijn meerdere manieren om een vragenlijst te verspreiden:

-   De vragenlijst als actief markeren. De vragenlijst is dan beschikbaar voor alle werknemers, tenzij een vragenlijstgroep is ingesteld om de toegang tot de vragenlijst te beperken.
-   Rechten aan een vragenlijstgroep toewijzen. De vragenlijst is dan beschikbaar voor alle leden van de geselecteerde groep.
-   Geplande antwoordsessies maken. De vragenlijst is dan alleen voor één bepaalde persoon beschikbaar.
-   Een planning maken. De vragenlijst kan dan voor meerdere mensen beschikbaar zijn.

## <a name="marking-a-questionnaire-as-active"></a>Een vragenlijst als actief markeren.
Als u het veld **Actief** instelt op **Ja** op de pagina **Vragenlijsten**, kunt u de vragenlijst beschikbaar maken voor alle werknemers zodat zij de lijst kunnen invullen. Respondenten kunnen de vragenlijst meerdere keren invullen. Deze functionaliteit is handig als u gedurende het hele jaar steeds feedback wilt verzamelen. U kunt bijvoorbeeld een vragenlijst maken die werknemers gebruiken om feedback te geven over de lunchservice in de kantine.

## <a name="questionnaire-groups"></a>Vragenlijstgroepen
U kunt vragenlijstgroepen instellen en vervolgens de respondenten opnemen waarnaar een vragenlijst moet worden verspreid. 

U kunt vragenlijstgroepen maken via de volgende pagina´s:

-   **Vragenlijstgroepen** – alleen personen in een vragenlijstgroep kunnen een geselecteerde vragenlijst invullen. Als uw doelgroep uit contractanten bestaat, kunt u een vragenlijstgroep maken die specifiek is voor die respondenten.
-   **Vragenlijstgroepsleden** – u kunt mensen aan vragenlijstgroepen toevoegen.

Als u een vragenlijstgroep wilt toewijzen aan een vragenlijst, klik u op de pagina **Vragenlijsten** op **Gebruikersrechten**. Nadat de vragenlijst is opgeslagen als actief, kunnen de leden van de vragenlijstgroep de vragenlijst invullen. Deze functionaliteit is handig als u een vragenlijst op een selecte groep mensen wilt testen voordat u deze beschikbaar stelt voor een grotere groep, of als u een vragenlijst door een zeer specifieke doelgroep wilt laten invullen.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Geplande antwoordsessies in een vragenlijst
Geplande antwoordsessies zijn vragenlijsten waarvoor u de respondenten hebt aangesteld en geselecteerd. 

> [!NOTE]
>   Voordat u geplande antwoordsessies kunt opzetten, dient u een vragenlijst te ontwerpen. 

Op de pagina **Geplande antwoordsessie** kunt u een geplande antwoordsessie voor een individuele werknemer maken. De lijst op de pagina toont alle geplande vragenlijsten. 

Geplande antwoordsessies worden ook gebruikt op de pagina **Vragenlijstplanningen**, waar u vragenlijsten voor meerdere mensen kunt plannen:

-   Werknemers
-   Deelnemers
-   Organisatie-eenheden;

Elke persoon kan de vragenlijst slechts één keer beantwoorden.

## <a name="scheduling-a-questionnaire"></a>Een vragenlijst plannen
U kunt ook een vragenlijst plannen voor meerdere respondenten.

### <a name="planning-types"></a>Planningstypen

Planningstypen zijn vereist als u geplande antwoordsessies voor meerdere respondenten wilt plannen. Planningstypen worden gebruikt voor het classificeren van vragenlijstplanningen. Zo kunt u bijvoorbeeld vragenlijsten plannen voor de volgende doeleinden:

-   Beoordeling
-   Onderzoek
-   Testen

U kunt planningstypen voor een vragenlijstplanning opgeven op de pagina **Vragenlijstplanningen**.

### <a name="reference-types-for-questionnaire"></a>Verwijzingstypen voor vragenlijst

U kunt verwijzingstypen gebruiken als hulpmiddel bij het invoeren van criteria die u gebruikt bij de selectie van respondenten wanneer u een vragenlijst plant. 

Gebruik de pagina **Verwijzingstypen** om referentietypen voor een vragenlijst in te stellen. Elk verwijzingstype komt overeen met een tabel in Microsoft Dynamics 365 Finance. Wanneer u de vragenlijstplanning maakt, kunt u afzonderlijke records in de tabel of een bereik van records opgeven waar de vragenlijst aan wordt gekoppeld. 

Als u bijvoorbeeld de tabel Cursussen selecteert, kunt u bepalen voor welke specifieke cursus de vragenlijst is. Wanneer u een verwijzingstype instelt voor de tabel Cursussen, zijn sommige velden en knoppen op de pagina **Cursussen** niet meer beschikbaar.

### <a name="questionnaire-schedules"></a>Vragenlijstplanningen

U kunt vragenlijstplanningen gebruiken om meerdere geplande antwoordsessies voor een groep gebruikers op basis van een verwijzingstype te genereren. Maak een planning op de pagina **Vragenlijstplanningen**. Selecteer het planningstype om de planning te categoriseren en ook om het verwijzingstype te selecteren dat moet worden gebruikt om in het systeem naar specifieke gebruikers te laten zoeken. Bijvoorbeeld: als u het verwijzingstype instelt op de tabel Cursussen, kunt u een bepaalde cursus in het veld **Verwijzing** selecteren. 

Klik op **Instellingsdetails** om de vragenlijst en andere criteria te selecteren. Bijvoorbeeld: geef de naam van de docent als een criterium op als de vragenlijst een evaluatie van de docent is. Als u de instellingsdetails hebt ingevoerd, worden geplande antwoordsessies gegenereerd voor de gebruikers die zijn opgenomen in de query. 

Klik op **Geplande antwoordsessies** om de antwoordsessie voor de planning weer te geven. U kunt vervolgens handmatig extra geplande antwoordsessies maken of geplande antwoordsessies verwijderen die niet zijn beantwoord. 

Klik op **Functies** &gt; **Starten** om de vragenlijst beschikbaar te maken voor de gebruikers in gerelateerde geplande antwoordsessies. Klik op **Antwoorden** om de ingevulde antwoorden in de vragenlijst weer te geven. U kunt de instellingen van de vragenlijstplanning, geplande antwoordsessies en de antwoorden ook kopiëren naar een nieuwe vragenlijstplanning.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Respondenten op de hoogte brengen als er vragenlijsten voor hen beschikbaar zijn
Wanneer u een vragenlijst distribueert, moet u respondenten waarschuwen dat vragenlijsten beschikbaar voor hen zijn. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Respondenten op de hoogte brengen van een geplande antwoordsessie

Als u een geplande antwoordsessie gebruikt, moet u de persoon direct, zoals telefonisch of via e-mail, op de hoogte brengen.

### <a name="notifying-respondents-about-a-scheduling"></a>Respondenten op de hoogte brengen van een planning

Gebruik de pagina **Vragenlijstplanningen** om een e-mailbericht op te stellen en te versturen naar alle respondenten die aan de vragenlijst zijn gekoppeld. Voer de e-mailtekst in op het tabblad **E-mail voor werknemersselfservice**. Nadat de planning is gestart, klikt u op **Functies** &gt; **E-mailbericht verzenden** om het e-mailbericht te genereren en te verzenden naar de respondenten. Respondenten kunnen zich vervolgens aanmelden bij de website en de vragenlijst invullen. 

> [!NOTE]
>   Voordat u de e-mailfunctionaliteit kunt gebruiken, moet de IT-beheerder de e-mailinstellingen op de pagina **E-mailparameters** invoeren.

## <a name="ending-a-scheduled-questionnaire"></a>Een geplande vragenlijst beëindigen
U kunt een geplande vragenlijst beëindigen nadat alle respondenten hun toegewezen antwoordsessies hebben voltooid. Nadat een geplande vragenlijst is beëindigd, kunt u de instellingen niet kopiëren naar een nieuwe planning. 

> [!NOTE]
>   Als een of meer respondenten de vragenlijst niet hebben ingevuld maar u de planning toch wilt beëindigen, moet u eerst die respondenten uit de lijst verwijderen op de pagina **Geplande antwoordsessie**. Vervolgens kunt u de planning beëindigen.

## <a name="completing-questionnaires"></a>Vragenlijsten invullen
Nadat u een vragenlijst hebt ontworpen en verspreid, kan de vragenlijst worden ingevuld door geselecteerde respondenten. U kunt de vragenlijsten die voor u beschikbaar zijn, op twee manieren openen:

-   Klik in het navigatievenster op **Vragenlijsten** &gt; **Verdelen** &gt; **Vragenlijst invullen**.
-   Klik in Selfservice werknemer op **In te vullen vragenlijsten**.

Vragenlijsten kunnen beschikbaar worden gesteld aan alle personen in een netwerk of aan specifieke gebruikers of groepen gebruikers.

<a name="additional-resources"></a>Aanvullende resources
--------

[Vragenlijsten ontwerpen](design-questionnaires.md)

[Vragenlijsten](questionnaires.md)

[De resultaten van vragenlijsten bekijken en evalueren](evaluate-questionnaire-results.md)



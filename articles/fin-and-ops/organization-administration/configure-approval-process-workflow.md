---
title: Goedkeuringsprocessen configureren in een workflow
description: Met behulp van de volgende procedure kunt u de eigenschappen van het goedkeuringsproces configureren.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08641eaac31813a8bee3231118f8e2bf802ea3e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555528"
---
# <a name="configure-approval-processes-in-a-workflow"></a>Goedkeuringsprocessen configureren in een workflow

[!include [banner](../includes/banner.md)]

Met behulp van de volgende procedure kunt u de eigenschappen van het goedkeuringsproces configureren.

Als u een goedkeuringsproces wilt configureren, klikt u in de workfloweditor met de rechtermuisknop op het goedkeuringselement en klikt u vervolgens op **Eigenschappen** om het formulier **Eigenschappen** te openen.

## <a name="name-the-approval-process"></a>Het goedkeuringsproces een naam geven

Voer deze stappen uit om een naam op te geven voor de goedkeuringsproces.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Geef in het veld **Naam** een unieke naam op voor het goedkeuringsproces.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Opgeven wanneer het systeem automatisch op het document reageert

U kunt het systeem zo configureren dat er automatisch wordt gereageerd het document als aan specifieke voorwaarden is voldaan. Het systeem kan bijvoorbeeld onkostennota´s goedkeuren met een totaalbedrag dat lager is dan 100 EUR. Voer de volgende stappen uit om op te geven wanneer het systeem op het document reageert.

1. Klik in het linkerdeelvenster op **Automatische acties**.
2. Vink het selectievakje **Automatische acties inschakelen** aan.
3. Klik op **Voorwaarde toevoegen**.
4. Een voorwaarde invoeren.
5. Geef desgewenst aanvullende voorwaarden op.
6. Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd.

    1. Klik op **Testen** om het formulier **Workflowvoorwaarde testen** te openen.
    2. Selecteer een record in het gebied **Voorwaarde valideren** van het formulier.
    3. Klik op **Testen**. Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.
    4. Klik op **OK** of **Annuleren** om terug te gaan naar het formulier **Eigenschappen**.

7. Selecteer in de lijst **Actie AutoAanvullen** de actie die het systeem op het document moet uitvoeren.

## <a name="specify-when-notifications-are-sent"></a>Opgeven wanneer meldingen worden verzonden

U kunt meldingen naar gebruikers verzenden wanneer een document is goedgekeurd, afgewezen, gedelegeerd of geëscaleerd, of wanneer een wijziging is aangevraagd. Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.

1. Klik in het linkerdeelvenster op **Meldingen**.
2. Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:

    - **Delegeren**: wanneer een document aan een andere gebruiker ter goedkeuring is toegewezen.
    - **Escaleren**: wanneer de toegewezen gebruiker niet binnen de toegekend tijd op het document heeft gereageerd.
    - **Goedkeuren**: wanneer een document is goedgekeurd.
    - **Afwijzen**: wanneer een document is afgewezen.
    - **Wijziging aanvraag**: wanneer de toegewezen gebruiker een wijziging van een ingediend document heeft aangevraagd.

3. Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.
4. Klik op het tabblad **Meldingstekst**.
5. Geef in het tekstvak de tekst voor de melding op.
6. Om de tekst te personaliseren, kunt u ook tijdelijke aanduidingen invoegen die worden vervangen door de gewenste gegevens wanneer de instructies worden weergegeven voor gebruikers. Volg deze stappen om een tijdelijke aanduiding in te voegen:

    1. Klik in het tekstvak op de locatie waar de tijdelijke aanduiding moet verschijnen.
    2. Klik op **Tijdelijke aanduiding invoegen**.
    3. Selecteer in de lijst die wordt weergegeven de tijdelijke aanduiding die u wilt invoegen.
    4. Klik op **Invoegen**.

7. Klik op **Vertalingen** om vertalingen van de melding toe te voegen. Selecteer de volgende stappen in het formulier dat wordt weergegeven:

    1. Klik op **Toevoegen**.
    2. Selecteer in de lijst die wordt weergegeven de taal waarin u de tekst wilt invoeren.
    3. Geef in het vak **Vertaalde tekst** de tekst op.
    4. Voeg tijdelijke aanduidingen in om de tekst te personaliseren.
    5. Klik op **Sluiten**.

8. Klik op het tabblad **Ontvanger**.
9. Vermeld naar wie de meldingen worden verzonden. Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de optie voordat u naar stap 10 gaat.

    <table>
    <thead>
    <tr>
    <th>Optie</th>
    <th>Ontvangers van meldingen</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><strong>Deelnemer</strong></td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td>
    <ol>
    <li>Selecteer het tabblad <strong>Deelnemer</strong> en klik op het tabblad <strong>Rolgebaseerd</strong>.</li>
    <li>Selecteer in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt verzenden.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Werkstroomgebruiker</strong></td>
    <td>Gebruikers die aan de huidige workflow deelnemen</td>
    <td>
    <ol>
    <li>Selecteer <strong>Workflowgebruiker</strong> en klik op het tabblad <strong>Workflowgebruiker</strong>.</li>
    <li>Selecteer in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Gebruiker</strong></td>
    <td>Specifieke Microsoft Dynamics 365 for Finance and Operations-gebruikers</td>
    <td>
    <ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle Microsoft Dynamics 365 for Finance and Operations-gebruikers. Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. Herhaal stappen 3 tot en met 9 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.

## <a name="specify-a-final-approver"></a>Een definitieve fiatteur opgeven

Mogelijk wilt u een definitieve fiatteur aanduiden voor gevallen waarin de fiatteur de persoon is die het document ter goedkeuring heeft ingediend. Volg deze stappen om een definitieve fiatteur op te geven.

1. Klik in het linkerdeelvenster op **Geavanceerde instellingen**.
2. Schakel het selectievakje **Definitieve fiatteur gebruiken** in.
3. Selecteer de gebruiker die de definitieve fiatteur is in de lijst.

## <a name="set-a-time-limit"></a>Een tijdslimiet instellen

Volg deze stappen als het goedkeuringsproces binnen een opgegeven tijd moet worden voltooid.

> [!NOTE]
> De opties die u in deze stappen selecteert, overschrijven de opties die u in de gebieden **Toewijzing** en **Escalatie** van elke goedkeuringsstap hebt geselecteerd.

1. Klik in het linkerdeelvenster op **Geavanceerde instellingen**.
2. Schakel het selectievakje **Een tijdslimiet instellen voor het** **workflowelement** in.
3. Geef in het veld **Duur** aan wanneer het goedkeuringsproces moet voltooid zijn. Een van de volgende opties selecteren:

    - **Uren**: het aantal uren invoeren waarin het goedkeuringsproces moet worden voltooid. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    - **Dagen**: het aantal dagen invoeren waarin het goedkeuringsproces moet worden voltooid. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    - **Weken**: het aantal weken invoeren waarin het goedkeuringsproces moet worden voltooid.
    - **Maanden**: de dag en week selecteren wanneer het goedkeuringsproces moet zijn voltooid. U kunt bijvoorbeeld aangeven dat het goedkeuringsproces vóór vrijdag in de derde week van de maand moet zijn voltooid.
    - **Jaren**: de dag, week en maand selecteren wanneer het goedkeuringsproces moet zijn voltooid. U kunt bijvoorbeeld aangeven dat het goedkeuringsproces vóór vrijdag in de derde week van december moet zijn voltooid.

4. Als de tijdslimiet is overschreden, reageert het systeem automatisch op het document. Selecteer de gewenste actie in de lijst **Actie**.

## <a name="specify-which-actions-are-available-to-the-user"></a>Geef op welke acties voor de gebruiker beschikbaar zijn

Wanneer een document voor goedkeuring is toegewezen aan een gebruiker, moet de gebruiker reageren op het document. Volg deze stappen om aan te geven welke acties de gebruiker kan ondernemen op het ingediende document.

1. Klik in het linkerdeelvenster op **Geavanceerde instellingen**.
2. Vink het selectievakje **Goedkeuren** aan als de gebruiker het document kan goedkeuren.
3. Vink het selectievakje **Afwijzen** aan als de gebruiker het document kan afwijzen.
4. Schakel het selectievakje **Wijziging aanvraag** in als u wilt dat de gebruiker wijzigingen in het document kan aanvragen.
5. Schakel het selectievakje **Delegeren** in als de gebruiker het document ter goedkeuring aan een andere gebruiker kan toewijzen.

> [!NOTE]
> Het selectievakje **Acties van de werklijst in Enterprise Portal activeren** is verwijderd.

## <a name="configure-the-approval-steps"></a> De goedkeuringsstappen configureren

Een goedkeuringsproces bestaat uit goedkeuringsstappen. Voer de volgende procedures uit om stappen aan het goedkeuringsproces toe te voegen en de stappen te configureren.

1. Dubbelklik in de workfloweditor op het goedkeuringsproces. De workfloweditor geeft de stappen van het goedkeuringsproces weer.
2. Sleep de goedkeuringsstappen die u wilt toevoegen van het gebied **Workflowelementen** naar het tekenpapier.
3. Zie [Een goedkeuringsstap configureren](configure-approval-step-workflow.md) als u een goedkeuringsstap wilt configureren.

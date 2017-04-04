---
title: Een handmatige taak configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige taak configureert.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 408e2bc6ca1cd506a89ba9676fb457df8fd4e214
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-manual-task-in-a-workflow"></a>Een handmatige taak configureren in een workflow

In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige taak configureert.

Om een handmatige taak te configureren, klikt u in de workfloweditor met de rechtermuisknop op de taak en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen. Configureer vervolgens aan de hand van de volgende procedures de eigenschappen voor de handmatige taak.

## <a name="name-the-task"></a>Een naam opgeven voor de taak
Voer deze stappen uit om een naam op te geven voor de handmatige taak.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Geef in het veld **Naam** een unieke naam voor de taak op.

## <a name="enter-a-subject-line-and-instructions"></a>Een onderwerpregel en instructies invoeren
U moet een onderwerpregel en instructies invoeren voor de gebruikers die aan de taak zijn toegewezen. Als u bijvoorbeeld een taak voor opdrachten tot inkoop configureert, ziet de gebruiker die aan de taak is toegewezen de onderwerpregel en instructies op de pagina **Opdrachten tot inkoop**. De onderwerpregel verschijnt in de berichtenbalk van de pagina. De gebruiker kan vervolgens klikken op het pictogram op de berichtenbalk om de instructies weer te geven. Voer deze stappen uit om een onderwerpregel en instructies in te voeren.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Voer in het veld **Onderwerp werkitem** de onderwerpregel in.
3.  Als u de onderwerpregel wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de onderwerpregel aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:
    1.  Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.
    2.  Klik op **Tijdelijke aanduiding invoegen**.
    3.  Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4.  Klik op **Invoegen**.

4.  Voer de onderstaande stappen uit om vertalingen van de onderwerpregel toe te voegen:
    1.  Klik op **Vertalingen**.
    2.  Klik in de pagina die wordt geopend op **Toevoegen**.
    3.  Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4.  Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5.  Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 3.
    6.  Klik op **Sluiten**.

5.  Voer in het veld **Instructies werkitem** de instructies in.
6.  Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:
    1.  Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.
    2.  Klik op **Tijdelijke aanduiding invoegen**.
    3.  Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4.  Klik op **Invoegen**.

7.  Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:
    1.  Klik op **Vertalingen**.
    2.  Klik in de pagina die wordt geopend op **Toevoegen**.
    3.  Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4.  Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5.  Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 6.
    6.  Klik op **Sluiten**.

## <a name="assign-the-task"></a>De taak toewijzen
Voer de volgende stappen uit om op te geven aan wie de handmatige taak moet worden toegewezen.

1.  Klik in het linkerdeelvensters op het pictogram **Toewijzing**.
2.  Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 3 gaat.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Optie</th>
    <th>Gebruikers aan wie de taak wordt toegewezen</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deelnemer</td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td><ol>
    <li>Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waaraan u de taak wilt toewijzen.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waaraan u de taak wilt toewijzen.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hiërarchie</td>
    <td>Gebruikers in een specifieke organisatiehiërarchie</td>
    <td><ol>
    <li>Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waaraan u de taak wilt toewijzen.</li>
    <li>Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen. Deze namen vertegenwoordigen gebruikers waaraan de taak kan worden toegewezen. Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:
    <ol>
    <li>Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</li>
    <li>Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven. Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</li>
    </ol></li>
    <li>Geeft op het tabblad <strong>Hiërarchieopties</strong> op aan welke gebruikers in het bereik de taak moet worden toegewezen:
    <ul>
    <li><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de taak wordt toegewezen aan alle gebruikers in het bereik.</li>
    <li><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de taak wordt alleen aan de laatste gebruiker in het bereik toegewezen.</li>
    <li><strong>Gebruikers met de volgende status uitsluiten</strong>: de taak wordt niet toegewezen aan een gebruiker in het bereik die aan een specifieke voorwaarde voldoet. Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers in de huidige workflow</td>
    <td><ul>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Gebruiker</td>
    <td>Specifieke Microsoft Dynamics 365 voor gebruikers van bewerkingen</td>
    <td><ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De <strong>beschikbare gebruikers</strong> lijst bevat alle Dynamics 365 voor gebruikers van bewerkingen. Selecteer de gebruikers aan wie u de taak wilt toewijzen en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Wachtrij</td>
    <td>Een wachtrij voor werkitems</td>
    <td><ol>
    <li>Selecteer het tabblad <strong>Wachtrij</strong> en klik op het tabblad <strong>Wachtrijgebaseerd</strong>.</li>
    <li>Voer deze stappen uit om de taak aan een specifieke wachtrij toe te wijzen:
    <ol>
    <li>Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Wachtrijen voor werkitems</strong>.</li>
    <li>Selecteer in de lijst <strong>Wachtrijnaam</strong> de gewenste wachtrij.</li>
    </ol></li>
    <li>Als een specifieke voorwaarde moet bepalen aan welke wachtrij de taak wordt toegewezen, volgt u deze stappen:
    <ol>
    <li>Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Voorwaardelijke wachtrijen voor werkitems</strong>.</li>
    <li>Selecteer in de lijst <strong>Wachtrijnaam</strong> de waarde <strong>Voorwaardelijke wachtrij</strong>.</li>
    </ol></li>
    </ol><ph id="t1">
    </ph><strong>opmerking:</strong> deze optie wordt gebruikt voor enkele workflows, zoals aanvraagbeheer.</td>
    </tr>
    </tbody>
    </table>

3.  Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de taak uit te voeren. Een van de volgende opties selecteren:
    -   **Uren**: voer het aantal uren in dat de gebruiker heeft om de taak uit te voeren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Dagen**: voer het aantal dagen in dat de gebruiker heeft om de taak uit te voeren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Weken**: voer het aantal weken in dat de gebruiker heeft om de taak uit te voeren.
    -   **Maanden**: selecteer de dag en week waarop de gebruiker de taak uiterlijk moet hebben voltooid. U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van de maand.
    -   **Jaren**: selecteer de dag, week en maand waarop de gebruiker de taak uiterlijk moet hebben voltooid. U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van december.

    Als de gebruiker de taak niet binnen de toegekende tijd voltooit, wordt de taak achterstallig. Een taak die achterstallig is, kan worden geëscaleerd op basis van de opties die u selecteert in het gebied **Escalatie** van deze pagina.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Aangeven wat moet gebeuren wanneer de taak achterstallig is
Als een gebruiker de handmatige taak niet binnen de toegekende tijd voltooit, wordt de taak achterstallig. Een taak die achterstallig is, kan worden geëscaleerd of automatisch aan een andere gebruiker worden toegewezen. Voer de volgende stappen uit om de taak te escaleren als deze achterstallig is.

1.  Klik in het linkerdeelvenster op **Escalatie**.
2.  Vink het selectievakje **Escalatiepad gebruiken** aan om een escalatiepad te maken. Het systeem wijst de taak automatisch toe aan de gebruikers die in het escalatiepad zijn vermeld. De volgende tabel kan bijvoorbeeld een escalatiepad voorstellen.
    | Reeks | Escalatiepad      |
    |----------|----------------------|
    | 1        | Toewijzen aan: Diana     |
    | 2        | Toewijzen aan: Erica      |
    | 3        | Laatste actie: Afwijzen |

    In dit voorbeeld wordt de achterstallige taak door het systeem automatisch toegewezen aan Diana. Als Diana niet tijdig de taak voltooit, wordt de taak door het systeem toegewezen aan Erica. Als Erica niet tijdig de taak voltooit, wijst het systeem het document af dat ter verwerking is ingediend.
3.  Klik op **Escalatie toevoegen** om gebruikers toe te voegen aan het escalatiepad. Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 4 gaat.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Optie</th>
    <th>Gebruikers naar wie de taak wordt geëscaleerd</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hiërarchie</td>
    <td>Gebruikers in een specifieke organisatiehiërarchie</td>
    <td><ol>
    <li>Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waarnaar u de taak wilt escaleren.</li>
    <li>Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen. Deze namen vertegenwoordigen gebruikers waarnaar de taak kan worden geëscaleerd. Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:
    <ol>
    <li>Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</li>
    <li>Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven. Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</li>
    </ol></li>
    <li>Geeft op het tabblad <strong>Hiërarchieopties</strong> op naar welke gebruikers in het bereik de taak moet worden geëscaleerd:
    <ul>
    <li><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de taak wordt geëscaleerd naar alle gebruikers in het bereik.</li>
    <li><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de taak wordt alleen geëscaleerd naar de laatste gebruiker in het bereik.</li>
    <li><strong>Gebruikers met de volgende status uitsluiten</strong>: de taak wordt niet geëscaleerd naar een gebruiker in het bereik die aan een specifieke voorwaarde voldoet. Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers in de huidige workflow</td>
    <td><ul>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Gebruiker</td>
    <td>Specifieke Dynamics 365 voor gebruikers van bewerkingen</td>
    <td><ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De <strong>beschikbare gebruikers</strong> lijst bevat alle Dynamics 365 voor gebruikers van bewerkingen. Selecteer de gebruikers naar wie u de taak wilt escaleren en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de taak uit te voeren. Een van de volgende opties selecteren:
    -   **Uren**: voer het aantal uren in dat de gebruiker heeft om de taak uit te voeren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Dagen**: voer het aantal dagen in dat de gebruiker heeft om de taak uit te voeren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Weken**: voer het aantal weken in dat de gebruiker heeft om de taak uit te voeren.
    -   **Maanden**: selecteer de dag en week waarop de gebruiker de taak uiterlijk moet hebben voltooid. U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van de maand.
    -   **Jaren**: selecteer de dag, week en maand waarop de gebruiker de taak uiterlijk moet hebben voltooid. U kunt bijvoorbeeld aangeven dat de gebruiker de taak uiterlijk moet hebben voltooid op de vrijdag in de derde week van december.

5.  Herhaal stappen 3 tot en met 4 voor elke gebruiker die u aan het escalatiepad wilt toevoegen. U kunt de volgorde van de gebruikers wijzigen.
6.  Als de gebruikers in het escalatiepad niet binnen de gestelde tijd de taak voltooit, voert het systeem automatisch actie uit voor de taak Om de actie in te stellen die het systeem moet uitvoeren, selecteert u de rij **Actie** en klikt u op het tabblad **Actie beëindigen**. Selecteer hier een actie.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Opgeven wanneer het systeem automatisch op de taak reageert
U kunt het systeem zo configureren dat het systeem onder bepaalde voorwaarden automatisch actie onderneemt voor de handmatige taak. Stel dat een taak vereist dat een lid van de afdeling Onkostennota´s de ontvangstbewijzen controleert die bij een onkostennota worden ingediend. Volgens het bedrijfsbeleid, kan deze taak moet worden uitgevoerd als het totale bedrag van de onkostennota groter dan USD 100 is. In dit scenario kunt u het systeem automatisch de taak markeren als **volledig** wanneer het totale bedrag lager is dan 100. Voer de volgende stappen uit om op te geven wanneer het systeem actie onderneemt op de handmatige taak.

1.  Klik in het linkerdeelvenster op **Automatische acties**.
2.  Vink het selectievakje **Automatische acties inschakelen** aan.
3.  Klik op **Voorwaarde toevoegen**.
4.  Een voorwaarde invoeren.
5.  Geef desgewenst vereiste extra voorwaarden op.
6.  Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd:
    1.  Klik op **Testen**.
    2.  Ga naar de pagina **Workflowvoorwaarde testen** en selecteer in het gebied **Voorwaarde valideren** een record.
    3.  Klik op **Testen**. Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.
    4.  Klik op **OK** of **Annuleren** om terug te gaan naar de pagina **Eigenschappen**.

7.  Selecteer in de lijst **Actie AutoAanvullen** de actie die het systeem op de taak moet uitvoeren.

## <a name="specify-when-notifications-are-sent"></a>Opgeven wanneer meldingen worden verzonden
U kunt meldingen naar gebruikers verzenden wanneer een handmatige taak is gedelegeerd, geëscaleerd, voltooid of afgewezen of wanneer een wijziging is aangevraagd. Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.

1.  Klik in het linkerdeelvenster op **Meldingen**.
2.  Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:
    -   **Delegeren**: de taak wordt toegewezen aan een andere gebruiker.
    -   **Escaleren**: de toegewezen gebruiker heeft de taak niet binnen de toegekend tijd voltooid.
    -   **Voltooien**: de toegewezen gebruiker heeft de taak voltooid.
    -   **Afwijzen**: de toegewezen gebruiker heeft het aangeboden document afgewezen.
    -   **Wijziging aanvragen**: de toegewezen gebruiker heeft een wijziging van het ingediende document aangevraagd.

3.  Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.
4.  Geef op het tabblad **Meldingstekst** de tekst van de melding op.
5.  Als u de melding wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de melding aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:
    1.  Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.
    2.  Klik op **Tijdelijke aanduiding invoegen**.
    3.  Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4.  Klik op **Invoegen**.

6.  Voer de onderstaande stappen uit om vertalingen van de melding toe te voegen:
    1.  Klik op **Vertalingen**.
    2.  Klik in de pagina die wordt geopend op **Toevoegen**.
    3.  Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4.  Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5.  Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 5.
    6.  Klik op **Sluiten**.

7.  Geef op het tabblad **Ontvanger** op aan wie de meldingen moeten worden verzonden. Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de betreffende optie voordat u naar stap 8 gaat.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Optie</th>
    <th>Ontvangers van meldingen</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deelnemer</td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td><ol>
    <li>Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt laten verzenden.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers in de huidige workflow</td>
    <td><ul>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Gebruiker</td>
    <td>Specifieke Dynamics 365 voor gebruikers van bewerkingen</td>
    <td><ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De <strong>beschikbare gebruikers</strong> lijst bevat alle Dynamics 365 voor gebruikers van bewerkingen. Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.

## <a name="set-a-time-limit"></a>Een tijdslimiet instellen
Volg deze stappen als de handmatige taak binnen een opgegeven tijd moet worden voltooid. **Opmerking:** De hier geselecteerde opties hebben voorrang op de opties die u in de gebieden **Toewijzing** en **Escalatie** van de pagina hebt geselecteerd.

1.  Klik in het linkerdeelvenster op **Geavanceerde instellingen**.
2.  Schakel het selectievakje **Een tijdslimiet instellen voor het workflowelement** in.
3.  Geef in het veld **Duur** aan wanneer de taak moet voltooid zijn. Een van de volgende opties selecteren:
    -   **Uren** : Voer het aantal uren dat de taak moet worden voltooid in. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Dagen** : Voer het aantal dagen dat de taak moet worden voltooid in. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Weken**: voer het aantal weken in waarin de taak moet worden voltooid.
    -   **Maanden**: selecteer de dag en week waarop de taak uiterlijk moet zijn uitgevoerd. U kunt bijvoorbeeld aangeven dat de taak uiterlijk op de vrijdag in de derde week van de maand moet zijn voltooid.
    -   **Jaren**: selecteer de dag, week en maand waarop de taak uiterlijk moet zijn uitgevoerd. U kunt bijvoorbeeld aangeven dat de taak uiterlijk op de vrijdag in de derde week van december moet zijn voltooid.

4.  Als de tijdslimiet is overschreden, onderneemt het systeem automatisch actie voor de taak. Selecteer de gewenste actie in de lijst **Actie**.

## <a name="specify-which-actions-are-available-to-the-user"></a>Geef op welke acties voor de gebruiker beschikbaar zijn
Wanneer de handmatige taak is toegewezen aan een gebruiker, moet de gebruiker actie ondernemen op de taak. Volg deze stappen om aan te geven welke acties de gebruiker op de taak kan uitvoeren. **Opmerking:** welke acties beschikbaar zijn, is afhankelijk van het ontwerp van de taak.

1.  Klik in het linkerdeelvenster op **Geavanceerde instellingen**.
2.  Schakel het selectievakje **Voltooid** in, als u wilt dat de gebruiker deze taak als **Voltooid** kan markeren.
3.  Schakel het selectievakje **Afwijzen** in als u wilt dat de gebruiker wijzigingen voor het ingediende document kan afwijzen.
4.  Schakel het selectievakje **Wijziging aanvraag** in als u wilt dat de gebruiker wijzigingen voor het ingediende document kan aanvragen.
5.  Schakel het selectievakje **Delegeren** in als u wilt dat de gebruiker deze taak aan een andere gebruiker kan toewijzen.
6.  Schakel het selectievakje **Opnieuw toewijzen** in als u wilt dat de gebruiker deze taak opnieuw aan een andere gebruiker in de wachtrij voor werkitems kan toewijzen.
7.  Schakel het selectievakje **Vrijgave** in als u wilt dat de gebruiker deze taak opnieuw aan een andere gebruiker in de wachtrij voor werkitems kan toewijzen. Een andere gebruiker kan de taak vervolgens voltooien.




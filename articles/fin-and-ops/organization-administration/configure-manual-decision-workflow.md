---
title: Handmatige beslissingen configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige beslissing configureert.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: e942942aac5e9973ebd0a4e3f3a134b0c667ff5b
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="configure-manual-decisions-in-a-workflow"></a>Handmatige beslissingen configureren in een workflow

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige beslissing configureert.

Om een handmatige beslissing te configureren, klikt u in de workfloweditor met de rechtermuisknop op de handmatige beslissing en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen. Vervolgens kunt u met de volgende procedures de eigenschappen van de handmatige beslissing configureren.

## <a name="name-the-decision"></a>Naam van de beslissing
Voer deze stappen uit om een naam op te geven voor de handmatige beslissing.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Voer in het veld **Naam** een unieke naam voor de handmatige beslissing in.

## <a name="enter-a-subject-line-and-instructions"></a>Een onderwerpregel en instructies invoeren
U moet een onderwerpregel en instructies invoeren voor de gebruikers die aan de handmatige beslissing zijn toegewezen. Als u bijvoorbeeld een beslissing voor opdrachten tot inkoop configureert, ziet de gebruiker die aan de beslissing is toegewezen de onderwerpregel en instructies op de pagina **Opdrachten tot inkoop**. De onderwerpregel verschijnt in de berichtenbalk van de pagina. De gebruiker kan vervolgens klikken op het pictogram op de berichtenbalk om de instructies weer te geven. Voer deze stappen uit om een onderwerpregel en instructies in te voeren.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Op het tabblad **Instructies** voert u in het veld **Onderwerp werkitem** de onderwerpregel in.
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

## <a name="specify-the-possible-outcomes-of-a-decision"></a>De mogelijke resultaten van een beslissing opgeven
Wanneer een document aan een besluitvormer is toewezen, krijgt de besluitvormer doorgaans een vraag voorgelegd. Het antwoord op deze vraag is doorgaans **Ja** of **Nee**, of **Waar** of **Onwaar**. Voer de volgende stappen uit om de mogelijk resultaten op te geven van de handmatige beslissing.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Geef op het tabblad **Resultaten** in het veld **Resultaat 1** de naam van het resultaat of de optie op.
3.  Voer de onderstaande stappen uit om vertalingen van het resultaat toe te voegen:
    1.  Klik op **Vertalingen**.
    2.  Klik in de pagina die wordt geopend op **Toevoegen**.
    3.  Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4.  Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5.  Klik op **Sluiten**.

4.  Geef in het veld **Uitkomst 2** de naam van het resultaat of de optie op.
5.  Voer de onderstaande stappen uit om vertalingen van het resultaat toe te voegen:
    1.  Klik op **Vertalingen**.
    2.  Klik in de pagina die wordt geopend op **Toevoegen**.
    3.  Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4.  Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5.  Klik op **Sluiten**.

## <a name="specify-when-notifications-are-sent"></a>Opgeven wanneer meldingen worden verzonden
U kunt meldingen naar gebruikers verzenden wanneer een beslissing is genomen, gedelegeerd, geëscaleerd. Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.

1.  Klik in het linkerdeelvenster op **Meldingen**.
2.  Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:
    -   **\[Keuze 1\]** – de toegewezen gebruiker heeft **\[Keuze 1\]** geselecteerd.
    -   **\[Keuze 2\]** – de toegewezen gebruiker heeft **\[Keuze 2\]** geselecteerd.
    -   **Delegeren**: de toegewezen gebruiker heeft de beslissing aan een andere gebruiker toegewezen.
    -   **Escaleren**: de toegewezen gebruiker heeft de beslssing niet niet binnen de toegekende tijd genomen.

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
    <td>Specifieke Microsoft Dynamics 365 for Finance and Operations-gebruikers</td>
    <td><ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers. Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.

## <a name="assign-a-decision"></a>Een beslissing toewijzen
Voer de volgende stappen uit om op te geven aan wie de handmatige beslissing moet worden toegewezen.

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
    <th>Gebruikers aan wie de beslissing is toegewezen</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deelnemer</td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td><ol>
    <li>Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waaraan u de beslissing wilt toewijzen.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> het type groep of rol waaraan u de beslissing wilt toewijzen.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hiërarchie</td>
    <td>Gebruikers in een specifieke organisatiehiërarchie</td>
    <td><ol>
    <li>Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waaraan u de beslissing wilt toewijzen.</li>
    <li>Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen. Deze namen stellen gebruikers voor waaraan de beslissing kan worden toegewezen. Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt: <ol>
    <li>Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</li>
    <li>Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven. Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</li>
    </ol></li>
    <li>Geeft op het tabblad <strong>Hiërarchieopties</strong> op aan welke gebruikers in het bereik de beslissing moet worden toegewezen: <ul>
    <li><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de beslissing wordt toegewezen aan alle gebruikers in het bereik.</li>
    <li><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de beslissing wordt alleen aan de laatste gebruiker in het bereik toegewezen.</li>
    <li><strong>Gebruikers met de volgende status uitsluiten</strong>: de beslissing wordt niet toegewezen aan een gebruiker in het bereik die aan een specifieke voorwaarde voldoet. Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</li>
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
    <td>Specifieke Finance and Operations-gebruikers</td>
    <td><ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers. Selecteer de gebruikers aan wie u de beslissing wilt toewijzen en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Wachtrij</td>
    <td>Een wachtrij voor werkitems</td>
    <td><ol>
    <li>Selecteer het tabblad <strong>Wachtrij</strong> en klik op het tabblad <strong>Wachtrijgebaseerd</strong>.</li>
    <li>Voer deze stappen uit om de beslissing aan een specifieke wachtrij toe te wijzen: <ol>
    <li>Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Wachtrijen voor werkitems</strong>.</li>
    <li>Selecteer in de lijst <strong>Wachtrijnaam</strong> de gewenste wachtrij.</li>
    </ol></li>
    <li>Als een specifieke voorwaarde moet bepalen aan welke wachtrij de beslissing wordt toegewezen, volgt u deze stappen: <ol>
    <li>Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Voorwaardelijke wachtrijen voor werkitems</strong>.</li>
    <li>Selecteer in de lijst <strong>Wachtrijnaam</strong> de waarde <strong>Voorwaardelijke wachtrij</strong>.</li>
    </ol></li>
    </ol>
    <strong>Opmerking:</strong> deze optie wordt alleen bij enkele workflows toegepast, zoals Aanvraagbeheer.</td>
    </tr>
    </tbody>
    </table>

3.  Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de beslissing te nemen. Een van de volgende opties selecteren:
    -   **Uren**: voer het aantal uren in dat de gebruiker heeft om de beslissing te nemen. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Dagen**: voer het aantal dagen in dat de gebruiker heeft om de beslissing te nemen. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Weken**: voer het aantal weken in dat de gebruiker heeft om de beslissing te nemen.
    -   **Maanden**: selecteer de dag en week waarop de gebruiker de beslissing uiterlijk moet hebben genomen. U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van de maand.
    -   **Jaren**: selecteer de dag, week en maand waarop de gebruiker de beslissing uiterlijk moet hebben genomen. U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van december.

    Als de gebruiker niet binnen de toegekende tijd de beslissing neemt, wordt de beslissing achterstallig. Een beslissing die achterstallig is, wordt geëscaleerd op basis van de opties die u selecteert in het gebied **Escalatie** van deze pagina.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Aangeven wat moet gebeuren wanneer een beslissing achterstallig is
Als een gebruiker niet binnen de toegekende tijd de beslissing neemt, wordt de beslissing achterstallig. Een achterstallige beslissing kan worden geëscaleerd of automatisch aan een andere gebruiker worden toegewezen. Voer de volgende stappen uit om de beslissing te escaleren als deze achterstallig is.

1. Klik in het linkerdeelvenster op **Escalatie**.
2. Vink het selectievakje **Escalatiepad gebruiken** aan om een escalatiepad te maken. Het systeem wijst de beslissing automatisch toe aan de gebruikers die in het escalatiepad zijn vermeld. De volgende tabel kan bijvoorbeeld een escalatiepad voorstellen.

   | Reeks | Escalatiepad            |
   |----------|----------------------------|
   | 1        | Toewijzen aan: Diana           |
   | 2        | Toewijzen aan: Erica            |
   | 3        | Laatste actie: \[Keuze 1\] |

   In dit voorbeeld wordt de achterstallige beslissing door het systeem automatisch toegewezen aan Diana. Als Diana niet tijdig de beslissing neemt, wordt de beslissing door het systeem toegewezen aan Erica. Als Erica niet tijdig de beslissing neemt, selecteert het systeem **\[Keuze 1\]** als beslissing
3. Klik op **Escalatie toevoegen** om gebruikers toe te voegen aan het escalatiepad. Selecteer een van de opties in de volgende tabel en volg de bijkomende stappen voor de betreffende optie voordat u naar stap 4 gaat.
   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th>Optie</th>
   <th>Gebruikers naar wie de beslissing wordt geëscaleerd</th>
   <th>Bijkomende stappen</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td>Hiërarchie</td>
   <td>Gebruikers in een specifieke organisatiehiërarchie</td>
   <td><ol>
   <li>Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waarnaar u de beslissing wilt escaleren.</li>
   <li>Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen. Deze namen vertegenwoordigen gebruikers naar wie de beslissing kan worden geëscaleerd. Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt: <ol>
   <li>Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</li>
   <li>Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven. Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</li>
   </ol></li>
   <li>Geeft op het tabblad <strong>Hiërarchieopties</strong> op naar welke gebruikers in het bereik de beslissing moet worden geëscaleerd: <ul>
   <li><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de beslissing wordt geëscaleerd naar alle gebruikers in het bereik.</li>
   <li><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de beslissing wordt alleen geëscaleerd naar de laatste gebruiker in het bereik.</li>
   <li><strong>Gebruikers met de volgende status uitsluiten</strong>: de beslissing wordt niet geëscaleerd naar een gebruiker in het bereik die aan een specifieke voorwaarde voldoet. Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</li>
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
   <td>Specifieke Finance and Operations-gebruikers</td>
   <td><ol>
   <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
   <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers. Selecteer de gebruikers naar wie u de beslissing wilt escaleren en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
   </ol></td>
   </tr>
   </tbody>
   </table>

4. Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de beslissing te nemen. Een van de volgende opties selecteren:
   -   **Uren**: voer het aantal uren in dat de gebruiker heeft om de beslissing te nemen. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
   -   **Dagen**: voer het aantal dagen in dat de gebruiker heeft om de beslissing te nemen. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
   -   **Weken**: voer het aantal weken in dat de gebruiker heeft om de beslissing te nemen.
   -   **Maanden**: selecteer de dag en week waarop de gebruiker de beslissing uiterlijk moet hebben genomen. U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van de maand.
   -   **Jaren**: selecteer de dag, week en maand waarop de gebruiker de beslissing uiterlijk moet hebben genomen. U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van december.

5. Herhaal stappen 3 tot en met 4 voor elke gebruiker die u aan het escalatiepad wilt toevoegen. U kunt de volgorde van de gebruikers wijzigen.
6. Als de gebruikers in het escalatiepad niet binnen de gestelde tijd de beslissing nemen, reageert het systeem automatisch op de beslissing. Om de optie in te stellen die het systeem selecteert, selecteert u de rij **Actie** en klikt u op het tabblad **Actie beëindigen**. Selecteer hier een optie.

## <a name="set-a-time-limit"></a>Een tijdslimiet instellen
Volg deze stappen als de beslissing binnen een opgegeven tijd moet worden genomen. **Opmerking:** De hier geselecteerde opties hebben voorrang op de opties die u in de gebieden **Toewijzing** en **Escalatie** van de pagina hebt geselecteerd.

1.  Klik in het linkerdeelvenster op **Geavanceerde instellingen**.
2.  Schakel het selectievakje **Een tijdslimiet instellen voor het workflowelement** in.
3.  Geef in het veld **Duur** aan wanneer de beslissing moet genomen zijn. Een van de volgende opties selecteren:
    -   **Uren**: voer het aantal uren in. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Dagen**: voer het aantal dagen in. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    -   **Weken**: voer het aantal weken in.
    -   **Maanden**: selecteer de dag en week waarop de beslissing uiterlijk moet zijn genomen. U kunt bijvoorbeeld aangeven dat de beslissing uiterlijk op de vrijdag in de derde week van de maand moet zijn genomen.
    -   **Jaren**: selecteer de dag, week en maand waarop de beslissing uiterlijk moet zijn genomen. U kunt bijvoorbeeld aangeven dat de beslissing uiterlijk op de vrijdag in de derde week van december moet zijn genomen.

4.  Als de tijdslimiet is overschreden, dan neemt het systeem automatisch de beslissing. Selecteer in de lijst **Actie** de optie die het systeem moet selecteren.






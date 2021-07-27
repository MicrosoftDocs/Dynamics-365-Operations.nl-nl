---
title: Goedkeuringsstappen configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een goedkeuringsstap configureert.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 988340d9e5fc12c9329a587c7401fe039c8e5722
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350689"
---
# <a name="configure-approval-steps-in-a-workflow"></a>Goedkeuringsstappen configureren in een workflow

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een goedkeuringsstap configureert.

Om een goedkeuringsstap te configureren, klikt u in de workfloweditor met de rechtermuisknop op de goedkeuringsstap en klikt u vervolgens op **Eigenschappen** om het formulier **Eigenschappen** te openen. Met de volgende procedures kunt u de eigenschappen van de goedkeuringsstap configureren.

## <a name="name-the-step"></a>De stap een naam geven
Voer deze stappen uit om een naam op te geven voor de goedkeuringsstap.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Geef in het veld **Naam** een unieke naam op voor de goedkeuringsstap.

## <a name="enter-a-subject-line-and-instructions"></a>Een onderwerpregel en instructies invoeren

U moet een onderwerpregel en instructies invoeren voor de gebruikers die aan de goedkeuringsstap zijn toegewezen. Als u bijvoorbeeld een goedkeuringsstap voor opdrachten tot inkoop configureert, ziet de gebruiker die aan de stap is toegewezen de onderwerpregel en instructies op de pagina **Opdrachten tot inkoop**. De onderwerpregel verschijnt in de berichtenbalk van de pagina. De gebruiker kan vervolgens klikken op het pictogram op de berichtenbalk om de instructies weer te geven. Voer deze stappen uit om een onderwerpregel en instructies in te voeren.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Voer in het veld **Onderwerp werkitem** de onderwerpregel in.
3. Als u de onderwerpregel wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de onderwerpregel aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:

    1. Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.
    2. Klik op **Tijdelijke aanduiding invoegen**.
    3. Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4. Klik op **Invoegen**.

4. Voer de onderstaande stappen uit om vertalingen van de onderwerpregel toe te voegen:

    1. Klik op **Vertalingen**.
    2. Klik in de pagina die wordt geopend op **Toevoegen**.
    3. Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4. Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5. Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 3.
    6. Klik op **Sluiten**.

5. Voer in het veld **Instructies werkitem** de instructies in.
6. Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:

    1. Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.
    2. Klik op **Tijdelijke aanduiding invoegen**.
    3. Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4. Klik op **Invoegen**.

7. Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:

    1. Klik op **Vertalingen**.
    2. Klik in de pagina die wordt geopend op **Toevoegen**.
    3. Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4. Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5. Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 6.
    6. Klik op **Sluiten**.

## <a name="assign-the-approval-step"></a>De goedkeuringsstap toewijzen

Voer de volgende stappen uit om op te geven aan wie de goedkeuringsstap moet worden toegewezen.

1. Klik in het linkerdeelvensters op het pictogram **Toewijzing**.
2. Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 3 gaat.

    <table>
    <thead>
    <tr>
    <th>Optie</th>
    <th>Gebruikers waaraan de goedkeuringsstap is toegewezen</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deelnemer</td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td>
    <ol>
    <li>Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waaraan u de stap wilt toewijzen.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waaraan u de stap wilt toewijzen.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hiërarchie</td>
    <td>Gebruikers in een specifieke organisatiehiërarchie</td>
    <td>
    <ol>
    <li>Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waaraan u de stap wilt toewijzen.</li>
    <li>Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen. Deze namen stellen gebruikers voor waaraan de stap kan worden toegewezen. Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt: <ol>
    <li>Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</li>
    <li>Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven. Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</li>
    </ol>
    </li>
    <li>Geef op het tabblad <strong>Hiërarchieopties</strong> op aan welke gebruikers in het bereik de stap moet worden toegewezen: <ul>
    <li><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de stap wordt toegewezen aan alle gebruikers in het bereik.</li>
    <li><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de stap wordt alleen aan de laatste gebruiker in het bereik toegewezen.</li>
    <li><strong>Gebruikers met de volgende status uitsluiten</strong>: de stap wordt niet toegewezen aan een gebruiker in het bereik die aan een specifieke voorwaarde voldoet. Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers in de huidige workflow</td>
    <td>
    <ul>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Gebruiker</td>
    <td>Specifieke gebruikers</td>
    <td>
    <ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle systeemgebruikers. Selecteer de gebruikers aan wie u de stap wilt toewijzen en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Ga naar het tabblad **Tijdslimiet** en geef in het veld **Duur** aan hoe lang de gebruiker heeft om actie te ondernemen of te reageren op documenten die de goedkeuringsstap hebben bereikt. Een van de volgende opties selecteren:

    - **Uren**: voer het aantal uren in dat de gebruiker heeft om te reageren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    - **Dagen**: voer het aantal dagen in dat de gebruiker heeft om te reageren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    - **Weken**: voer het aantal weken in dat de gebruiker heeft om te reageren.
    - **Maanden**: selecteer de dag en week waarop de gebruiker uiterlijk moet hebben gereageerd. U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week in de maand moet hebben gereageerd.
    - **Jaren**: selecteer de dag, week en maand waarop de gebruiker uiterlijk moet hebben gereageerd. U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week van december moet hebben gereageerd.

    Als de gebruiker niet binnen de toegekende tijd actie op een document onderneemt, wordt het document achterstallig. Een achterstallig document wordt geëscaleerd op basis van de opties die u selecteert in het gebied **Escalatie** van deze pagina.

4. Als u de goedkeuringsstap aan meerdere gebruikers of aan een groep gebruikers hebt toegewezen, klikt u op het tabblad **Voltooiingsbeleid** en selecteert u een van de volgende opties:

    - **Eén fiatteur**: de eerste persoon die reageert bepaalt welke actie op het document wordt toegepast. Stel dat Sam een onkostennota voor 15.000 EUR heeft ingediend. De onkostennota is op dit moment toegewezen aan Suzan, Jo en Bill. Als Suzan als eerste reageert, wordt de actie die zij uitvoert op het document toegepast. Wijst Suzan het document af, dan wordt het document afgewezen en teruggestuurd naar Sam. Als Suzan het document goedkeurt, wordt het ter goedkeuring naar Anne doorgezonden.

        ![Een werkstroom met een goedkeuringsproces.](./media/workflow_multipleusersinstep.gif)

    - **Meerderheid van fiatteurs**: welke actie op het document wordt toegepast wordt bepaald wanneer een meerderheid van de fiatteurs reageert. Stel dat Sam een onkostennota voor 15.000 EUR heeft ingediend. De onkostennota is op dit moment toegewezen aan Suzan, Jo en Bill. Als Suzan en Jo als eerste twee personen reageren, wordt de actie die zij uitvoeren op het document toegepast.

        - Als het document door Suzan wordt goedgekeurd, maar door Jo wordt afgewezen, wordt het document afgewezen en teruggestuurd naar Sam.
        - Als het document zowel door Suzan als door Jo wordt goedgekeurd, wordt het ter goedkeuring naar Anne doorgezonden.

    - **Percentage van fiatteurs**: welke actie op het document wordt toegepast, wordt bepaald wanneer een bepaald percentage van de fiatteurs reageert. Stel dat Sam een onkostennota voor 15.000 EUR heeft ingediend. De onkostennota is op dit moment toegewezen aan Suzan, Jo, and Bill en u hebt **50** als percentage ingevoerd. Als Suzan en Jo de eerste twee fiatteurs zijn die reageren, wordt de actie die zij uitvoeren op het document toegepast, omdat ze voldoen aan de vereiste voor 50 procent van de fiatteurs.

        - Als het document door Suzan wordt goedgekeurd, maar door Jo wordt afgewezen, wordt het document afgewezen en teruggestuurd naar Sam.
        - Als het document zowel door Suzan als door Jo wordt goedgekeurd, wordt het ter goedkeuring naar Anne doorgezonden.

    - **Alle fiatteurs**: alle fiatteurs moeten het document goedkeuren. Anders kan de workflow niet doorgaan. Stel dat Sam een onkostennota voor EUR 15.000 heeft ingediend. De onkostennota is op dit moment toegewezen aan Suzan, Jo en Bill. Als het document door Suzan en Jo wordt goedgekeurd, maar door Bill wordt afgewezen, wordt het document afgewezen en teruggestuurd naar Sam. Als het document zowel door Suzan als door Jo en Bill wordt goedgekeurd, wordt het ter goedkeuring naar Anne doorgezonden.

## <a name="specify-when-the-approval-step-is-required"></a>Opgeven wanneer de goedkeuringsstap verplicht is

U kunt opgeven wanneer de goedkeuringsstap verplicht is. De goedkeuringsstap kan altijd verplicht zijn of kan alleen verplicht zijn als aan specifieke voorwaarden is voldaan.

### <a name="the-approval-step-is-always-required"></a>De goedkeuringsstap is altijd verplicht

Volg deze stappen als de goedkeuringsstap altijd verplicht is.

1. Klik in het linkerdeelvenster op **Voorwaarde**.
2. Selecteer de optie **Deze stap altijd uitvoeren**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>De goedkeuringsstap is onder bepaalde voorwaarden verplicht

De goedkeuringsstap die u configureert, is mogelijk alleen verplicht als aan specifieke voorwaarden is voldaan. Als u bijvoorbeeld een goedkeuringsstap configureert voor een workflow voor opdrachten tot inkoop, kunt u bijvoorbeeld opgeven dat deze goedkeuringsstap alleen mag plaatsvinden voor een opdracht tot inkoop waarvan het bedrag hoger is dan EUR 10.000. Volg deze stappen om op te geven wanneer de goedkeuringsstap verplicht is.

1. Klik in het linkerdeelvenster op **Voorwaarde**.
2. Selecteer de optie **Voer deze stap alleen uit als aan de volgende voorwaarde wordt voldaan**.
3. Een voorwaarde invoeren.
4. Geef desgewenst vereiste extra voorwaarden op.
5. Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd:

    1. Klik op **Testen**.
    2. Ga naar de pagina **Workflowvoorwaarde testen** en selecteer in het gebied **Voorwaarde valideren** een record.
    3. Klik op **Testen**. Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.
    4. Klik op **OK** of **Annuleren** om terug te gaan naar de pagina **Eigenschappen**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Aangeven wat moet gebeuren wanneer het document achterstallig is

Als een gebruiker niet binnen de toegekende tijd actie onderneemt op een document, wordt het document achterstallig. Een document dat achterstallig is, kan worden geëscaleerd of automatisch ter goedkeuring aan een andere gebruiker worden toegewezen. Volg de volgende stappen om het document te escaleren als het achterstallig is.

1. Klik in het linkerdeelvenster op **Escalatie**.
2. Vink het selectievakje **Escalatiepad gebruiken** aan om een escalatiepad te maken. Het systeem wijst het document automatisch toe aan de gebruikers die in het escalatiepad zijn vermeld. De volgende tabel kan bijvoorbeeld een escalatiepad voorstellen.

    | Reeks | Escalatiepad      |
    |----------|----------------------|
    | 1        | Toewijzen aan: Diana     |
    | 2        | Toewijzen aan: Erica      |
    | 3        | Laatste actie: Afwijzen |

    In dit voorbeeld wordt het achterstallige document door het systeem automatisch toegewezen aan Diana. Als Diana niet tijdig op het document reageert, wordt het door het systeem toegewezen aan Erica. Als Erica niet tijdig op het document reageert, wordt het door het systeem afgewezen.

3. Klik op **Escalatie toevoegen** om gebruikers toe te voegen aan het escalatiepad. Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 4 gaat.

    <table>
    <thead>
    <tr>
    <th>Optie</th>
    <th>Gebruikers naar wie het document wordt geëscaleerd</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hiërarchie</td>
    <td>Gebruikers in een specifieke organisatiehiërarchie</td>
    <td>
    <ol>
    <li>Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waarnaar u het document wilt escaleren.</li>
    <li>Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen. Deze namen vertegenwoordigen gebruikers naar wie het document kan worden geëscaleerd. Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt: <ol>
    <li>Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</li>
    <li>Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven. Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</li>
    </ol>
    </li>
    <li>Geef op het tabblad <strong>Hiërarchieopties</strong> op naar welke gebruikers in het bereik het document moet worden geëscaleerd: <ul>
    <li><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: het document wordt geëscaleerd naar alle gebruikers in het bereik.</li>
    <li><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: het document wordt alleen geëscaleerd naar de laatste gebruiker in het bereik.</li>
    <li><strong>Gebruikers met de volgende status uitsluiten</strong>: het document wordt niet geëscaleerd naar een gebruiker in het bereik die aan een specifieke voorwaarde voldoet. Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers in de huidige workflow</td>
    <td>
    <ul>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Gebruiker</td>
    <td>Specifieke gebruikers</td>
    <td>
    <ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers. Selecteer de gebruikers naar wie u het document wilt escaleren en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Ga naar het tabblad **Tijdslimiet** en geef in het veld **Duur** aan hoe lang de gebruiker heeft om actie te ondernemen of te reageren op documenten. Een van de volgende opties selecteren:

    - **Uren**: voer het aantal uren in dat de gebruiker heeft om te reageren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    - **Dagen**: voer het aantal dagen in dat de gebruiker heeft om te reageren. Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.
    - **Weken**: voer het aantal weken in dat de gebruiker heeft om te reageren.
    - **Maanden**: selecteer de dag en week waarop de gebruiker uiterlijk moet hebben gereageerd. U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week in de maand moet hebben gereageerd.
    - **Jaren**: selecteer de dag, week en maand waarop de gebruiker uiterlijk moet hebben gereageerd. U kunt bijvoorbeeld instellen dat de gebruiker uiterlijk op de vrijdag van de derde week van december moet hebben gereageerd.

5. Herhaal stappen 3 tot en met 4 voor elke gebruiker die u aan het escalatiepad wilt toevoegen. U kunt de volgorde van de gebruikers wijzigen.
6. Als de gebruikers in het escalatiepad niet binnen de gestelde tijd op het document reageren, onderneemt het systeem automatisch actie op het document. Om de actie in te stellen die het systeem moet uitvoeren, selecteert u de rij **Actie** en klikt u op het tabblad **Actie beëindigen**. Selecteer hier een actie.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Door systeem gestuurde werksequentiëring
description: Dit artikel geeft informatie over door het systeem gestuurde werksequentiëring. Met deze functie kunt u de werkorders sorteren en filteren die door het systeem aan gebruikers worden gepresenteerd voor uitvoering. Het is nuttig in scenario's waarin extra criteria nodig zijn om het verzamelproces in het magazijn aan te sturen.
author: Mirzaab
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 1dab8d8bdace046f0f061713600fd1eab69e7c12
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335460"
---
# <a name="system-directed-work-sequencing"></a>Door systeem gestuurde werksequentiëring

[!include [banner](../includes/banner.md)]

Met door het systeem gestuurde werksequeuntiëring kunt u de werkorders sorteren en filteren die door het systeem aan gebruikers worden gepresenteerd voor uitvoering. Het is nuttig in scenario's waarin aanvullende criteria vereist zijn (zoals de verzendtijd, de orderverzamellocatie, het locatieprofiel of een combinatie van verschillende criteria) om het verzamelproces in het magazijn aan te sturen.

Deze functionaliteit breidt de huidige door het systeem gestuurde verzamelfunctionaliteit uit, door een queryvolgorde toe te voegen, waarin gebruikers een sequentie en een of meer query's kunnen instellen waarmee alle werkorders worden geëvalueerd die worden gemaakt. Alleen werkorders die voldoen aan de criteria die zijn opgegeven in de instellingen van de menuopdracht op mobiele apparaten, worden vastgelegd en gepresenteerd.

Deze functionaliteit biedt daarom verdere optimalisatie van verzamelprocessen in het magazijn, aangezien werkorders worden geïdentificeerd die aan de opgegeven criteria voldoen, deze toewijzen aan de juiste menuopdracht op het mobiele apparaat en deze vervolgens worden weergegeven aan een werknemer op basis van een specifieke reeks kwalificaties, apparatuur voor orderverzamelen of andere vereisten.

> [!NOTE]
> Als verschillende criteria nodig zijn, moeten meerdere menuopdrachten voor mobiele apparaten worden gebruikt.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>De functie Organisatiebrede, door het systeem gestuurde werksequentiëring inschakelen

Voordat u door het systeem gestuurde werksequentiëring kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Beheerders kunnen de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam** *Organisatiebrede, door het systeem gestuurde werksequentiëring*

## <a name="setup"></a>Instellen

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Om het scenario te doorlopen met de waarden die in dit artikel worden voorgesteld, moet u werken op een systeem waarop de standaard [demogegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren. In het scenario wordt magazijn *51* uit de demogegevens gebruikt.

> [!IMPORTANT]
> Voordat u de orders aan het magazijn vrijgeeft, moet u ervoor zorgen dat de orderverzamellocaties voldoende voorraad hebben voor alle artikelen op de orders.
>
> Dit scenario moet worden ondersteund door standaard USMF-gegevens. Als u geen gebruik maakt van de demogegevens, controleert u de instelling **Locatie-instructie** om te zien welke orderverzamellocaties worden gebruikt voor het verzamelen van verkooporders. Als u de voorraad moet corrigeren, kunt u handmatige verplaatsingen maken en aanvulling of elke andere stroom gebruiken.

### <a name="set-up-a-mobile-device-menu-item"></a>Een menuopdracht voor een mobiel apparaat instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in de lijst met menuopdrachten voor mobiele apparaten de optie **Verkoopverzamelen - systeem**. De vereiste menuopdracht zou al moeten bestaan. 
1. Bevestig de volgende instellingen:

    - Op het sneltabblad **Algemeen** moet het veld **Gestuurd door** zijn ingesteld op *Door systeem bestuurd*.
    - Op het sneltabblad **Werkklassen** moeten de volgende instellingen worden weergegeven.

        | Werkklasse-id | Werkordertype |
        |---|---|
        | Verkoop | Verkooporders |
        | VO verzamelen | Verkooporders |

1. Selecteer in het actievenster **Door het systeem gestuurde werkreeksquery's**.
1. Selecteer **Bewerken**.
1. Verwijder de bestaande regel en bevestig de actie door **Ja** te selecteren.
1. Selecteer in het actievenster **Nieuw** om een regel te maken.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Volgnummer:** *1*
    - **Veld Beschrijving:** *Werkhoeveelheid minder dan 20 en Aflopend*

1. Selecteer **Opslaan**.
1. Selecteer **Query bewerken** in het actievenster.
1. Vouw op het tabblad **Joins** de join-hiërarchie uit om de tabel **Werkregels** weer te geven.
1. Selecteer de tabeljoin **Werkregels**.
1. Selecteer **Tabeljoin toevoegen**.
1. Zoek en selecteer in de lijst die wordt weergegeven de rij met de volgende instellingen:

    - **Join-modus:** *n:1*
    - **Relatie:** *Locaties (Locatie)*

1. Selecteer **Selecteren**.

    Locaties worden toegevoegd aan de tabel-join.

1. Selecteer op het tabblad **Sorteren** de optie **Toevoegen** om een regel toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Werkhoeveelheid* (in het berichtvak dat wordt weergegeven, selecteert u **Ja** om aan dit veld sorteren toe te voegen.)
    - **Zoekrichting:** *Aflopend*

1. Selecteer het tabblad **Bereik**.

    Als in het sequentiëren alleen specifieke werkcriteria moeten worden opgenomen, kunt u deze opgeven op het tabblad **Bereik**. In dit voorbeeld wilt u alleen werk opnemen waarbij de hoeveelheid kleiner is dan 20 ea (de laagste maateenheid).

    Merk op dat sommige regels al zijn opgenomen. U moet deze regels niet verwijderen.

1. Selecteer **Toevoegen** om een regel toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Werkhoeveelheid voorraad*
    - **Criteria:** *\<20* (minder dan 20)

1. Selecteer **Toevoegen** om nog een regel toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Werkregels*
    - **Afgeleide tabel:** *Werkregels*
    - **Veld:** *Werktype*
    - **Criteria:** *Orderverzamelen*

1. Selecteer **Toevoegen** om nog een regel toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Afgeleide tabel:** *Locaties*
    - **Veld:** *Locatieprofiel-id*
    - **Criteria:** *!KLAARZETTEN*

        > [!IMPORTANT]
        > Vergeet niet het uitroepteken (*!*) in te voegen vóór *KLAARZETTEN*.

1. Selecteer **OK** om de query op te slaan en te sluiten.
1. Selecteer **Opslaan**.
1. Sluit de pagina om terug te gaan naar de pagina **Menuopties voor mobiel apparaat**.

> [!NOTE]
> Deze instelling bepaalt welke criteria worden gebruikt om het in aanmerking komende werk door te geven aan het menu-item op het mobiele apparaat. Als u meer criteriaregels aan de query toevoegt, wordt eerst de queryregel gebruikt die het laagste volgnummer heeft. Met andere woorden, alle in aanmerking komende werk voor volgnummer 1 wordt eerst aan de gebruiker gepresenteerd en vervolgens alle werk voor volgnummer 2. Als dus een specifiek bereik en specifieke sortering samen moeten worden gebruikt, moeten deze worden opgegeven in dezelfde query voor door het systeem gestuurde werksequentiëring.
>
> Met deze configuratie wordt al het werk vastgelegd dat ten minste één regel bevat waarvan de hoeveelheid minder is dan 20 ea. Als het werk bijvoorbeeld een regel heeft waarvan de hoeveelheid precies 20 ea of meer dan 20 ea is, is deze geldig, mits er ook minimaal één regel is met een hoeveelheid van minder dan 20 ea.

### <a name="location-directives"></a>Locatie-instructies

Als u standaard Contoso-gegevens gebruikt, zijn geen wijzigingen vereist in de query voor de locatie-instructieactie. Om er echter voor te zorgen dat de locatie-instructies de artikelen op de verkooporders vastleggen wanneer u de functie toepast in een omgeving buiten Contoso, maakt u een nieuwe locatie-instructie. Voer de volgende stappen uit om de instellingen in de demo-omgeving te controleren.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Locatie-instructies**.
1. Selecteer *Verkooporders* in het veld **Werkordertype**.
1. Selecteer de locatie-instructie met de naam *51 Pick*.
1. Ga naar het sneltabblad **Locatie-instructieacties** en selecteer de regel voor de actie **Orderverzamelen**.
1. Selecteer boven het raster de opdracht **Query bewerken**.
1. Controleer de query **Bereik**.

    1. Zoek de regel waarin het veld **Veld** is ingesteld op *Locatie*.
    2. Zorg ervoor dat het veld **Criteria** leeg is (dat wil zeggen dat er geen beperkingen zijn).

## <a name="scenario"></a>Scenario's

### <a name="create-sales-order-picking-work"></a>Werk voor orderverzamelen voor verkooporders maken

Voordat de door het systeem gestuurde orderverzameling wordt uitgevoerd, moet een deel van het uitgaande werk worden gemaakt. Voor dit scenario maakt u vier verkooporders die zijn gebaseerd op de opgegeven de query's voor door het systeem gestuurde werksequentiëring.

U gaat voorraadhoeveelheden reserveren voor elke verkooporder. Gereserveerde voorraad in het magazijn kan dus niet voor andere orders worden gebruikt, tenzij de reservering van de voorraad in zijn geheel of gedeeltelijk wordt geannuleerd.

Vervolgens geeft u elke verkooporder vrij naar het magazijn om het uitgaande werk te maken.

#### <a name="sales-order-1"></a>Verkooporder 1

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer in het actievenster **Nieuw** om verkooporder 1 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - Stel in de sectie **Klant** het veld **Klantaccount** in op *US-004*.
    - Stel in de sectie **Algemeen** het veld **Magazijn** in op *51*.

1. Selecteer **OK** om het dialoogvenster te sluiten. Noteer het nummer van de verkooporder.
1. Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:

    - **Artikelnummer:** *M9200*
    - **Hoeveelheid:** *20*

1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** de waarde **Partij reserveren** om de voorraad te reserveren.
1. Sluit de pagina **Reservering**.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgave naar magazijn** om werk voor het magazijn te maken.

    U ontvangt een informatieve melding waarin de wave-id en zendings-id worden vermeld die zijn aangemaakt voor de verkooporder.

#### <a name="sales-order-2"></a>Verkooporder 2

1. Selecteer in het actievenster **Nieuw** om verkooporder 2 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-007*
    - **Magazijn:** *51*

1. Selecteer **OK** om het dialoogvenster te sluiten. Noteer het nummer van de verkooporder.
1. Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:

    - **Artikelnummer:** *M9200*
    - **Hoeveelheid:** *5*

1. Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *M9201*
    - **Hoeveelheid:** *1*

1. Reserveer voorraad voor beide regels.
1. Geef de order vrij naar het magazijn.

#### <a name="sales-order-3"></a>Verkooporder 3

1. Selecteer in het actievenster **Nieuw** om verkooporder 3 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-009*
    - **Magazijn:** *51*

1. Selecteer **OK** om het dialoogvenster te sluiten. Noteer het nummer van de verkooporder.
1. Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:

    - **Artikelnummer:** *M9200*
    - **Hoeveelheid:** *7*

1. Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *M9202*
    - **Hoeveelheid:** *8*

1. Reserveer voorraad voor beide regels.
1. Geef de order vrij naar het magazijn.

#### <a name="sales-order-4"></a>Verkooporder 4

1. Selecteer in het actievenster **Nieuw** om verkooporder 4 te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-010*
    - **Magazijn:** *51*

1. Selecteer **OK** om het dialoogvenster te sluiten. Noteer het nummer van de verkooporder.
1. Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:

    - **Artikelnummer:** *M9200*
    - **Hoeveelheid:** *25*

1. Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *M9202*
    - **Hoeveelheid:** *10*

1. Reserveer voorraad voor beide regels.
1. Geef de order vrij naar het magazijn.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Werk-id's ophalen voor het gemaakte werk

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Filter op het veld **Magazijn**, zodat alleen werk voor magazijn *51* wordt weergegeven.
1. Er moeten vier werk-id's zijn gemaakt. Noteer de werk-id van elke verkooporder.

    | Verkooporder-id | Werk-id | Werkhoeveelheid |
    |---|---|---|
    | Verkooporder 1 | Werk-id 1 | 20 ea |
    | Verkooporder 2 | Werk-id 2 | 6 ea (som van beide regels) |
    | Verkooporder 3 | Werk-id 3 | 15 ea (som van beide regels) |
    | Verkooporder 4 | Werk-id 4 | 35 ea (som van beide regels) |

Voordat u de stroom uitvoert op het mobiele apparaat, moet u controleren of alleen het werk dat u zojuist hebt gemaakt de status *Open* heeft voor magazijn *51* en het werkordertype *Verkooporder* heeft. Anders kunnen de resultaten van de test afwijken, omdat de door het systeem gestuurde orderverzameling alle in aanmerking komende werk bevat.

1. Ga naar **Magazijnbeheer \> Werk \> Uitgaand \> Open verkoopwerk**.
1. Filter in het raster **Open verkoopwerk** op het veld **Magazijn**, zodat alleen werk voor magazijn *51* wordt weergegeven.
1. Controleer of alleen de vier werk-id's die u eerder hebt gemaakt, worden weergegeven.
1. Sluit de pagina **Werk**.

### <a name="mobile-device-flow-execution"></a>Uitvoering van stroom op mobiele apparaten

Op basis van de instellingen voert het systeem de gebruiker het werk, dat is gesorteerd van de hoogste werkregelhoeveelheid tot de laagste. De hoeveelheid op elke regel is minder dan 20 ea.

Onthoud dat met deze configuratie al het werk wordt vastgelegd dat ten minste één regel bevat waarvan de hoeveelheid minder is dan 20 ea. Als het werk een andere regel heeft waarop de hoeveelheid precies 20 ea of meer dan 20 ea ist, is die regel ook geldig.

#### <a name="mobile-app"></a>Mobiele app

1. Meld u aan bij de magazijnapp als een gebruiker in magazijn *51*.
1. Ga naar **Uitgaand \> Verkoopverzamelen - systeem**.

    De verzamelstap voor werk-id *4* wordt getoond. Deze werk-id wordt als eerste gepresenteerd vanwege de configuratie van de door het systeem gestuurde query-volgorde, waarin u hebt opgegeven dat het werk aflopend moet worden geordend op basis van de hoeveelheid op de werkregel.

1. Voltooi het vereiste verzamelen en wegzetten om de werk-id te sluiten.

    Vervolgens wordt werk-id *3* getoond. Een van de werkregels daarvan staat nu in de volgorde, op basis van de hoeveelheid op de werkregel.

1. Voltooi het verzamelen en wegzetten om de werk-id te sluiten.

    Vervolgens wordt werk-id *2* getoond. De verzamelregel van deze werkregel is de volgende in de volgorde.

1. Voltooi het verzamelen en wegzetten om de werk-id te sluiten.

    Daarna zou niet meer werk moeten worden getoond. Werk-id *1* komt niet in aanmerking voor dit menu-item op het mobiele apparaat, omdat de query opgeeft dat de werkkopteksten alleen worden meegenomen als de hoeveelheid op de werkregel minder is dan 20 ea.

## <a name="tips"></a>Tips

De door het systeem gestuurde query's voor werkvolgorde zijn *inclusief*. Het is belangrijk dat u dit voor sommige situaties onthoudt. U wilt bijvoorbeeld dat een bepaalde menuopdracht alleen werkt met de werk eenheid *ea* en u geeft deze beperking op op het tabblad **Bereik** van de query. In dit geval wordt al het werk waarin minstens voor één werkregel de werkeenheid is ingesteld op *ea* naar de werknemer geleid. Daarom kan dit werk ook werk bevatte waarbij werkregels een andere werk eenheid dan *ea* hebben (zoals *doos* of *pallet*). In de query wordt alleen het werk uitgesloten waarbij op geen enkele regel de werkeenheid is ingesteld op *ea*.

Daarom werd in het voorbeeld uit dit scenario ook werk-id *4* vastgelegd door de query. Toen deze id werd gemaakt, werden er twee regels toegevoegd: een voor 25 ea en een andere voor 10 ea. Het werk werd nog steeds getoond aan de gebruiker, omdat ten minste één werkregel een hoeveelheid van minder dan 20 ea heeft.

Afhankelijk van het scenario kunt u dit gedrag voorkomen door werkopsplitsingen te gebruiken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
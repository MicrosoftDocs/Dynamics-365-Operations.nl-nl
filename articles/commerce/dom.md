---
title: Gedistribueerd orderbeheer
description: In dit onderwerp wordt de functionaliteit voor gedistribueerd orderbeheer in Dynamics 365 Commerce beschreven.
author: josaw1
manager: AnnBe
ms.date: 01/08/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9ace77dba534615874e52ba95ee9dc6d71951d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204323"
---
# <a name="distributed-order-management-dom"></a>Gedistribueerd orderbeheer

[!include [banner](includes/banner.md)]

In het nieuwe model voor bedrijfsvoering in de handel streven detailhandelaren ernaar klanten een persoonlijke benadering, meerdere communicatiekanalen en vloeiende interactie te bieden. Vanwege de overvloed aan keuzemogelijkheden winkelen consumenten daar waar ze de beste ervaring wordt geboden. In veel gevallen zijn prijzen en producten niet meer de bepalende factoren voor consumenten.

Detailhandelaren moeten in realtime inzicht in hun voorraad hebben, via alle kanalen, om de klantervaring te kunnen verbeteren. Met één holistische weergave van alle voorraad kunnen de processen voor orderafhandeling, toewijzing en distributie worden geoptimaliseerd. Daarom wordt het voor detailhandelaren steeds belangrijker dat een DOM-systeem wordt geaccepteerd en geïmplementeerd.

DOM-systemen optimaliseren de orderafhandeling in een complex netwerk van systemen en processen. Met een dergelijk systeem wordt één algemene weergave van de voorraad van de hele organisatie gebruikt om orders intelligent te kunnen beheren en deze nauwkeurig en rendabeler af te handelen. Omdat een DOM-systeem de efficiëntie van de toeleveringsketen van een detailhandelaar verbetert, voldoet de detailhandelaar hiermee beter aan de verwachtingen van klanten.

In de volgende afbeelding wordt de levenscyclus van een verkooporder in een DOM-systeem weergegeven.

![Levenscyclus van verkooporders in de context van DOM](./media/flow.png "Levenscyclus van verkooporders in de context van DOM")

## <a name="set-up-dom"></a>DOM instellen

1. Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**.
2. Vouw op het tabblad **Configuratiesleutels** het knooppunt **Commerce** uit en schakel het selectievakje **Gedistribueerd orderbeheer** in.
3. Ga naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Instellingen \> DOM-parameters**.
4. Stel op het tabblad **Algemeen** de volgende waarden in:

    - **Gedistribueerd orderbeheer inschakelen**: stel deze optie in op **Ja**.
    - **Gebruik van Bing Kaarten voor DOM bevestigen**: stel deze optie in op **Ja**.


        > [!NOTE]
        > U kunt deze optie alleen op **Ja** instellen als de optie **Bing Kaarten inschakelen** op het tabblad **Bing Kaarten** van de pagina **Gedeelde handelparameters** (**Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde handelparameters**) ook is ingesteld op **Ja** en als een geldige sleutel is opgegeven in het veld **Bing Kaarten-sleutel**.
        >
        > Via de portal [Bing Maps Dev Center](https://www.bingmapsportal.com/) kunt u de toegang tot uw API-sleutels voor Bing Kaarten beperken tot een door u opgegeven set domeinen. Met deze functie kunnen klanten een beperkende verzameling verwijzende waarden of IP-adresbereiken opgeven op basis waarvan de sleutel wordt gevalideerd. Aanvragen die afkomstig zijn van waarden of IP-adressen uit uw lijst met toegestane waarden of IP-adressen worden op de normale manier verwerkt terwijl voor overige aanvragen de toegang wordt geweigerd. Het toevoegen van domeinbeveiliging aan uw API-sleutel is optioneel en sleutels waarvoor u dit niet doet, blijven gewoon functioneren. De toegestane lijst voor een sleutel is onafhankelijk van al uw andere sleutels, zodat u verschillende regels voor elk van uw sleutels kunt gebruiken. Gedistribueerd orderbeheer biedt geen ondersteuning voor het instellen van eigenschappen voor domeinverwijzing.


    - **Bewaarperiode in dagen**: geef op hoe lang de door het DOM-systeem gegenereerde afhandelingsplannen in het systeem moeten worden bewaard. Met de batchtaak **Instelling van taak voor verwijdering van DOM-afhandelingsgegevens** worden de afhandelingsplannen verwijderd die ouder zijn dan het aantal dagen dat u hier opgeeft.
    - **Afwijzingsperiode (in dagen)**: geef op hoeveel tijd moet verstrijken voordat een afgewezen orderregel aan dezelfde locatie kan worden toegewezen.

5. Stel op het tabblad **Oplossing** de volgende waarden in:

    - **Maximale aantal pogingen voor automatische afhandeling**: geef op hoe vaak de DOM-engine een orderregel moet proberen te bewerkstelligen en toe te wijzen aan een locatie. Als de DOM-engine een orderregel niet in het opgegeven aantal keren kan bewerkstelligen en toewijzen aan een locatie, wordt de orderregel gemarkeerd als een uitzondering. Vervolgens wordt deze regel in de toekomst overgeslagen totdat de status handmatig opnieuw wordt ingesteld.
    - **Radius voor lokale opslagregio**: geef een waarde op. Met de waarde in dit veld bepaalt u hoe locaties worden gegroepeerd en tot wanneer deze als op dezelfde afstand worden beschouwd. Als u **100** opgeeft, worden alle winkels en distributiecentra binnen een straal van 100 mijl of kilometer, afhankelijk van uw instellingen, van het adres voor afhandeling als op dezelfde afstand beschouwd.
    - **Type oplossing**: selecteer een waarde. In Commerce zijn twee typen oplossingen beschikbaar: **Productieoplossing** en **Vereenvoudigde oplossing**. Voor alle machines waarop een DOM-systeem wordt uitgevoerd (alle servers die deel uitmaken van de groep DOMBatch), moet **Productieoplossing** zijn geselecteerd. Voor de productieoplossing is de speciale licentiesleutel vereist die standaard in licentie wordt gegeven en wordt geïmplementeerd in productieomgevingen. Voor niet-productieomgevingen moet deze licentiesleutel handmatig worden geïmplementeerd. Ga als volgt te werk om de licentiesleutel handmatig te implementeren:

        1. Open de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services, selecteer **Model** als activatype en download het bestand met de **DOM-licentie**.
        1. Start Microsoft Internet Information Services (IIS) Manager, klik met de rechtermuisknop op **AOSService-website** en selecteer **Verkennen**. Windows Verkenner wordt geopend met **\<AOS service root\>\\webroot**. Noteer of onthoud het pad naar \<AOS Service root\>. U gebruikt dit pad in de volgende stap.
        1. Kopieer het configuratiebestand in de map **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Ga naar de Headquarters-client en open de pagina **DOM-parameters**. Selecteer op het tabblad **Oplossing** in het veld **Type oplossing** de optie **Productieoplossing** en controleer of er geen foutberichten worden weergegeven.


        > [!NOTE]
        > De optie Vereenvoudigde oplossing is beschikbaar om detailhandelaren in staat te stellen de DOM-functie uit te proberen zonder de speciale licentie te hoeven implementeren. Organisaties moeten de optie Vereenvoudigde oplossing niet gebruiken in productieomgevingen.
        >
        > Vereenvoudigde oplossing verbetert de prestaties (bijvoorbeeld het aantal orders en orderregels dat per keer kan worden verwerkt) en de convergentie van resultaten (aangezien een batch orders mogelijk niet het beste resultaat oplevert in sommige scenario's). Voor sommige regels, zoals de regel voor **gedeeltelijke orders** en het **maximale aantal locaties**, is Productieoplossing vereist.
     
6. Ga terug naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Instellingen \> DOM-parameters**.
7. Wijs op het tabblad **Nummerreeksen** het vereiste aantal nummerreeksen toe aan de verschillende DOM-entiteiten.

    > [!NOTE]
    > Voordat de nummerreeksen kunnen worden toegewezen aan de entiteiten, moeten ze worden gedefinieerd op de pagina **Nummerreeksen** (**Organisatiebeheer \> Nummerreeksen \> Nummerreeksen**).

8. De DOM-functie ondersteunt de definitie van verschillende typen DOM-regels. Organisaties kunnen meerdere regels configureren, afhankelijk van hun zakelijke behoeften. DOM-regels kunnen worden gedefinieerd voor een groep locaties of afzonderlijke locaties en voor een specifieke productcategorie, een specifiek product of een variant. Ga als volgt te werk om de locaties te groeperen die moeten worden gebruikt voor de DOM-regels:

    1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Uitvoeringsgroepen**.
    2. Selecteer **Nieuw** en geef een naam en beschrijving op voor de nieuwe groep.
    3. Selecteer **Opslaan**.
    4. Selecteer **Regel toevoegen** om één locatie toe te voegen aan de groep. Als u meerdere locaties wilt toevoegen, selecteert u **Regels toevoegen**.
    
    > [!NOTE]
    > In Commerce versie 10.0.12 en hoger moet **Mogelijkheid om locaties op te geven als 'Verzenden ' of 'Ophalen' binnen Afhandelingsgroep** zijn ingeschakeld in het werkgebied **Functiebeheer**.
    >
    > Met deze functie kunt u nieuwe configuraties toevoegen op de pagina **Afhandelingsgroep**, zodat u kunt definiëren of het magazijn kan worden gebruikt voor verzending of dat de combinatie van magazijn en winkel kan worden gebruikt voor verzenden, ophalen of beide. 
    >
    > Als u de functie inschakelt, worden de opties die beschikbaar zijn voor de selectie van locaties bij het maken van orders voor ophalen of verzenden, in POS bijgewerkt.
    >
    > Als u deze functie inschakelt, worden ook de pagina's in POS bijgewerkt wanneer de bewerkingen 'Alles verzenden ' of 'Geselecteerd verzenden' zijn geselecteerd.

9. Als u regels wilt opgeven, gaat u naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Instellingen \> Regels beheren**. Momenteel worden de volgende DOM-regels ondersteund:

    - **Regel voor minimumvoorraad**: met dit regeltype kunnen organisaties een bepaalde hoeveelheid van een product op voorraad houden voor andere doeleinden dan orderafhandeling. Organisaties kunnen het bijvoorbeeld onwenselijk vinden als alle beschikbare voorraad in een winkel door het DOM-systeem wordt gebruikt voor orderafhandeling. In plaats daarvan willen ze mogelijk enige voorraad reserveren voor klanten die de winkel bezoeken. Wanneer dit regeltype wordt gebruikt, kunt u per locatie of groep locaties opgeven welke voorraad minimaal moet worden behouden voor een categorie producten, een afzonderlijk product of een productvariant.
    - **Prioriteitsregel voor afhandelingslocatie**: met dit regeltype kunnen organisaties een hiërarchie voor locaties opgeven om de prioriteit te bepalen die door de DOM-engine moet worden gebruikt bij het identificeren van afhandelingslocaties voor bepaalde producten. Het geldige prioriteitsbereik is 1 tot en met 10, waarbij 1 voor de hoogste prioriteit staat en 10 voor de laagste. Locaties met een hogere prioriteit komen in aanmerking vóór locaties met een lagere prioriteit. Als de regel is gedefinieerd als een vaste beperking, worden orders alleen bewerkstelligd en toegewezen aan locaties waarvoor prioriteiten zijn opgegeven.
    - **Regel voor gedeeltelijke orders**: met deze regel kunnen organisaties opgeven of orders of orderregels gedeeltelijk kunnen worden afgehandeld. De volgende parameters zijn beschikbaar:

        - **Gedeeltelijke orders vervullen?** – Als deze optie is ingesteld op **Ja**, kan ook slechts een deel van de hoeveelheid op een orderregel worden afgehandeld. Deze gedeeltelijke afhandeling wordt uitgevoerd door de orderregel op te splitsen.
        - **Gedeeltelijke regels vervullen?** – Als deze optie is ingesteld op **Ja**, kan ook slechts een gedeeltelijke hoeveelheid van orderregels worden afgehandeld. Deze gedeeltelijke afhandeling wordt uitgevoerd door de orderregel op te splitsen.
        - **Order afhandelen vanaf slechts één locatie**: als deze optie is ingesteld op **Ja**, worden alle regels in een order afgehandeld via één locatie.


        In de volgende tabel wordt uitgelegd welk gedrag optreedt wanneer een combinatie van deze parameters wordt gedefinieerd.

        | Combinatienummer | Gedeeltelijke orders afhandelen | Gedeeltelijke regels afhandelen | Order afhandelen vanaf slechts één locatie | Beschrijving |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Ja                    | Ja                   | Ja                                  | Een paar regels van de order kunnen worden afgehandeld en afzonderlijke regels kunnen gedeeltelijk worden afgehandeld, maar alle regels moeten via dezelfde locatie worden afgehandeld in één DOM-uitvoering. (Deze combinatie wordt momenteel niet ondersteund.) |
        | 2    | Ja                    | Nee                    | Ja                                  | Een paar regels van de order kunnen worden afgehandeld, maar afzonderlijke regels kunnen niet gedeeltelijk worden afgehandeld en alle regels moeten via dezelfde locatie worden afgehandeld in één DOM-uitvoering. (Deze combinatie wordt momenteel niet ondersteund.) |
        | 3    | Ja                    | Ja                   | Nee                                   | Een paar regels van de order kunnen worden afgehandeld, afzonderlijke regels kunnen gedeeltelijk worden afgehandeld en alle regels kunnen via meerdere locaties worden afgehandeld in één DOM-uitvoering. |
        | 4\*  | Nee                     | Niet van toepassing        | Nee                                   | Alle orderregels moeten worden afgehandeld, afzonderlijke regels kunnen niet gedeeltelijk worden afgehandeld en elke orderregel kan via een andere locatie worden afgehandeld. |
        | 5\*  | Nee                     | Niet van toepassing        | Ja                                  | Alle orderregels moeten worden afgehandeld, afzonderlijke regels kunnen niet gedeeltelijk worden afgehandeld en alle orderregels kunnen slechts via één locatie worden geleverd. |
        | 6\*  | Nee                     | Niet van toepassing        | Nee                                   | Deze combinatie werkt als combinatie 4 omdat **Gedeeltelijke regels vervullen** niet op **Ja** kan worden ingesteld wanneer **Gedeeltelijke orders vervullen** is ingesteld op **Nee**. |
        | 7\*  | Nee                     | Niet van toepassing        | Ja                                  | Deze combinatie werkt als combinatie 5 omdat **Gedeeltelijke regels vervullen** niet op **Ja** kan worden ingesteld wanneer **Gedeeltelijke orders vervullen** is ingesteld op **Nee**. |
        | 8    | Ja                    | Nee                    | Nee                                   | Een paar regels van de order kunnen worden afgehandeld, maar afzonderlijke regels kunnen niet gedeeltelijk worden afgehandeld en de verschillende orderregels kunnen via meerdere locaties worden afgehandeld in één DOM-uitvoering. |
        | 9\*  | Nee                     | Niet van toepassing        | Ja                                  | Alle orderregels moeten worden afgehandeld en slechts via één locatie. |

        \* Als **Gedeeltelijke orders vervullen** is ingesteld op **Nee**, wordt er altijd van uitgegaan dat **Gedeeltelijke regels vervullen** ook is ingesteld op **Nee**, ook als dit niet het geval is.

        > [!NOTE]
        > In Retail versie 10.0.5 is de parameter **Order afhandelen vanaf slechts één locatie** gewijzigd in **Maximum afhandelingslocaties**. In plaats van een gebruiker in staat te stellen om te bepalen of orders alleen kunnen worden afgehandeld vanuit één locatie of vanuit zoveel locaties als mogelijk is, kunnen gebruikers nu opgeven of het afhandelen kan worden uitgevoerd vanuit een bepaalde set locaties (maximaal 5) of vanuit zoveel locaties als mogelijk is. Dit biedt meer flexibiliteit als het gaat om het aantal locaties waar de order kan worden afgehandeld. Deze regel werkt alleen met Productieoplossing. 

   - **Regel voor offline afhandelingslocatie**: met deze regel kunnen organisaties een locatie of groep locaties als offline of niet beschikbaar instellen voor DOM, zodat orders niet aan die locaties kunnen worden toegewezen voor afhandeling.
    - **Regel voor maximale afwijzingen**: met deze regel kunnen organisaties een drempelwaarde voor afwijzingen opgeven. Wanneer de drempelwaarde wordt bereikt, wordt een order of orderregel door de DOM-processor als uitzondering gemarkeerd en wordt deze uitgesloten van verdere verwerking.

        Als orderregels zijn toegewezen aan een locatie, kan de locatie een toegewezen orderregel afwijzen als deze om een of andere reden niet kan worden afgehandeld. Afgewezen regels worden als uitzondering gemarkeerd en weer opgenomen in de groep voor verwerking tijdens de volgende uitvoering. Tijdens de volgende uitvoering wordt geprobeerd de afgewezen regel toe te wijzen aan een andere locatie. Ook de nieuwe locatie kan de toegewezen orderregel afwijzen. Deze cyclus van toewijzing en afwijzing kan meerdere keren worden herhaald. Wanneer de opgegeven drempelwaarde voor het aantal afwijzingen wordt bereikt, wordt de orderregel als permanente uitzondering gemarkeerd en wordt de regel niet meer gekozen voor toewijzing. De orderregel komt pas weer in aanmerking voor toewijzing als een gebruiker de status van de orderregel opnieuw instelt.

   - **Regel voor maximale afstand**: met deze regel kunnen organisaties de maximale afstand van een locatie of groep locaties voor afhandeling van de order opgeven. Als er meerdere regels met verschillende maximumafstanden zijn opgegeven voor een locatie, wordt de kortste maximumafstand toegepast.
    - **Regel voor maximumorders**: met deze regel kunnen organisaties opgeven hoeveel orders maximaal kunnen worden verwerkt op een kalenderdag. Als het maximum aantal orders voor één dag is toegewezen aan een locatie, worden er de rest van die kalenderdag geen orders meer toegewezen aan die locatie.

   Voor alle bovenstaande regeltypen kunnen de volgende algemene kenmerken worden opgegeven:

   - **Begindatum** en **Einddatum**: met deze velden kunt u voor elke regel geldigheidsdatums instellen.
   - **Uitgeschakeld**: alleen regels met de waarde **Nee** voor dit veld worden gebruikt tijdens een DOM-uitvoering.
   - **Vaste beperking**: een regel kan als vaste beperking of niet-vaste beperking worden gedefinieerd. Elke DOM-uitvoering wordt op twee manieren uitgevoerd. De eerste keer wordt elke regel beschouwd als een vaste beperking, ongeacht de instelling van dit veld. Met andere woorden: elke regel wordt toegepast. De enige uitzondering is de regel **Prioriteit van locatie**. Voor de tweede uitvoering worden de regels verwijderd die niet als vaste beperking zijn ingesteld. De orders of orderregels die niet aan locaties waren toegewezen toen alle regels werden toegepast, worden toegewezen aan locaties.

10. Afhandelingsprofielen worden gebruikt om een verzameling regels, rechtspersonen, oorsprongen van verkooporders en leveringsmethoden te groeperen. Elke DOM-uitvoering vindt plaats voor een bepaald afhandelingsprofiel. Op deze manier kunnen organisaties een verzameling regels opgeven en uitvoeren voor een verzameling rechtspersonen, voor orders met bepaalde oorsprongen van verkooporders en leveringsmethoden. Als er verschillende verzamelingen regels moeten worden uitgevoerd voor verschillende verzamelingen oorsprongen van verkooporders of leveringsmethoden, kunnen de afhandelingsprofielen overeenkomstig worden gedefinieerd. Ga als volgt te werk om afhandelingsprofielen in te stellen:  

    1. Ga naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Instellingen \> Afhandelingsprofielen**.
    2. Selecteer **Nieuw**.
    3. Geef waarden op in de velden **Profiel** en **Beschrijving**.
    4. Stel de optie **Resultaat automatisch toepassen** in. Als u deze optie instelt op **Ja**, worden de resultaten van de DOM-uitvoering voor het profiel automatisch op de verkooporderregels toegepast. Stelt u **Nee** in, dan kunnen de resultaten alleen worden weergegeven in het afhandelingsplan. Deze worden niet toegepast op de verkooporderregels.
    5. Als het DOM-profiel moet worden uitgevoerd voor orders met alle oorsprongen van verkooporders, inclusief orders waarvoor geen oorsprong van de verkooporder is opgegeven, stelt u de optie **Orders met lege verkoopoorsprong verwerken** in op **Ja**. Als u het profiel voor slechts een paar oorsprongen van verkooporders wilt uitvoeren, kunt u deze opgeven op de pagina **Verkoopoorsprongen**, zoals verderop wordt uitgelegd.

    > [!NOTE]
    > In Commerce versie 10.0.12 en hoger moet de functie **Mogelijkheid om afhandelingsgroep toe te wijzen aan een afhandelingsprofiel** zijn ingeschakeld in het werkgebied **Functiebeheer**. 
    >
    > Deze functie voegt een nieuwe configuratie toe op de pagina **Afhandelingsprofiel** die kan worden gekoppeld aan één afhandelingsgroep. 
    >
    > Als u de afhandelingsgroep selecteert, worden de DOM-regels voor dat afhandelingsprofiel efficiënt uitgevoerd op basis van de verzendmagazijnen die in de afhandelingsgroep zijn opgenomen. 
    > 
    > Als u deze functie effectief wilt gebruiken, moet u ervoor zorgen dat er één afhandelingsgroep is die alle verzendmagazijnen bevat en vervolgens die afhandelingsgroep aan het afhandelingsprofiel koppelen.
    
    6. Selecteer op het sneltabblad **Rechtspersonen** de optie **Toevoegen** en selecteer vervolgens een rechtspersoon.
    7. Selecteer op het sneltabblad **Regels** de optie **Toevoegen** en selecteer de regel die u wilt koppelen aan het profiel.
    8. Herhaal de vorige twee stappen tot alle vereiste regels aan het profiel zijn gekoppeld.
    9. Selecteer **Opslaan**.
    10. Selecteer in het actievenster op het tabblad **Instellingen** de optie **Leveringsmethoden**.
    11. Selecteer **Nieuw** op de pagina **Leveringsmethoden**.
    12. Selecteer de rechtspersoon in het veld **Bedrijf**. De lijst met bedrijven blijft beperkt tot de rechtspersonen die u eerder hebt toegevoegd.
    13. Selecteer in het veld **Leveringsmethode** de leveringsmethode die aan dit profiel moet worden gekoppeld. Een leveringsmethode kan niet aan meerdere actieve profielen worden gekoppeld.
    14. Herhaal de vorige twee stappen tot alle vereiste leveringsmethoden aan het profiel zijn gekoppeld.
    15. Sluit de pagina **Leveringsmethoden**.
    16. Selecteer in het actievenster op het tabblad **Instellingen** de optie **Oorsprongen van verkooporders**.
    17. Selecteer **Nieuw** op de pagina **Verkoopoorsprongen**.
    18. Selecteer de rechtspersoon in het veld **Bedrijf**. De lijst met bedrijven blijft beperkt tot de rechtspersonen die u eerder hebt toegevoegd.
    19. Selecteer in het veld **Verkoopoorsprong** de verkoopoorsprong die u aan dit profiel wilt koppelen. Een verkoopoorsprong kan niet aan meerdere actieve profielen worden gekoppeld.
    20. Herhaal de vorige twee stappen tot alle vereiste verkoopoorsprongen aan het profiel zijn gekoppeld.
    21. Sluit de pagina **Verkoopoorsprongen**.
    22. Stel de optie **Profiel inschakelen** in op **Ja**. Bij eventuele fouten in de instellingen wordt een waarschuwingsbericht weergegeven.

## <a name="dom-processing"></a>DOM-verwerking

DOM wordt alleen uitgevoerd in een batchtaak. Ga als volgt te werk om de batchtaak voor DOM-uitvoeringen te configureren.

1. Ga naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Batchverwerking \> Taakinstellingen voor DOM-processor**.
1. Selecteer op het sneltabblad **Parameters** in het veld **Afhandelingsprofiel** een profiel waarvoor DOM moet worden uitgevoerd.
1. Selecteer een geconfigureerde batchgroep in het veld **Batchgroep** op het sneltabblad **Op de achtergrond uitvoeren**.
1. Geef in het veld **Taakbeschrijving** een naam op voor de batchtaak.
1. Selecteer **Terugkeer** en geef het terugkeerpatroon van de batchtaak op.
1. Selecteer **OK**.

De volgende orders en orderregels worden verwerkt in het DOM-systeem:

- Orderregels die voldoen aan de criteria voor oorsprongen van verkooporders, leveringsmethoden en rechtspersoon die zijn gedefinieerd in het DOM-profiel en die ook voldoen aan een van de volgende criteria:

    - Ze zijn gemaakt via afzetkanalen voor de handel.
    - Ze zijn nooit bewerkstelligd door het DOM-systeem.
    - Ze zijn eerder bewerkstelligd door het DOM-systeem, maar ze zijn als uitzonderingen gemarkeerd en de maximale drempelwaarde voor het aantal pogingen is nog niet bereikt.
    - De leveringsmethode is niet ophalen of elektronische levering.
    - Ze zijn niet gemarkeerd voor levering.
    - Ze zijn niet handmatig uitgesloten.

- Orders die niet in de wachtstand staan.

Nadat de regels, voorraadbeperkingen en optimalisatie zijn toegepast, wordt de locatie gekozen die het dichtst bij het afleveradres van de klant ligt.

![Criteria voor verkooporder](./media/ordercriteria.png "Criteria voor verkooporder")

## <a name="results-of-dom-runs"></a>Resultaten van DOM-uitvoeringen

Als het afhandelingsprofiel is ingesteld op **Automatisch toepassen**, worden de resultaten van de uitvoering automatisch toegepast op de verkooporderregels en kan het afhandelingsplan apart worden weergegeven. Is het afhandelingsprofiel echter niet ingesteld op **Automatisch toepassen**, dan kunnen de resultaten van de uitvoering alleen worden bekeken vanuit de weergave van het afhandelingsplan. 

Ga als volgt te werk om alle gegenereerde afhandelingsplannen weer te geven.

1. Ga naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Gedistribueerd orderbeheer**.
2. In het werkgebied **Gedistribueerd orderbeheer** selecteert u de tegel **Afhandelingsplannen**.
3. Selecteer de id van het betreffende orderafhandelingsplan.

    De sectie met orderdetails van het afhandelingsplan bevat de oorspronkelijke verkooporderregels die onderdeel waren van de uitvoering. Naast de standaardvelden van verkooporderregels bevat de sectie met orderdetails ook de volgende drie DOM-gerelateerde velden:

    - **Afhandelingstype**: in dit veld wordt aangegeven of de verkooporderregel volledig is bewerkstelligd, gedeeltelijk is bewerkstelligd of helemaal niet is bewerkstelligd en toegewezen aan een locatie.
    - **Splitsen**: in dit veld wordt aangegeven of één verkooporderregel is opgesplitst, en bewerkstelligd en toegewezen aan verschillende locaties.
    - **Aantal afhandelingslocaties**: in dit veld wordt aangegeven hoeveel afhandelingsregels zijn gemaakt voor één verkooporderregel (op basis van het aantal locaties waaraan de oorspronkelijke verkooporderregel is toegewezen).

    In de sectie met orderafhandelingsdetails wordt de toewijzing van de oorspronkelijke verkooporderregels, inclusief bijbehorende hoeveelheden, weergegeven.

## <a name="order-line-actions-and-statuses"></a>Acties voor en statussen van orderregels

Hieronder worden de instellingen beschreven die u kunt opgeven voor de orderregel. Als u de orderregel wilt openen, gaat u naar **Retail en Commerce \> Klanten \> Alle verkooporders**.
- Als u de optie **Uitsluiten van DOM-verwerking** op het tabblad **Algemeen** van de verkooporderregel instelt op **Ja**, wordt de order of orderregel uitgesloten van DOM-verwerking.
- Het veld **DOM-status** op het tabblad **Algemeen** van de verkooporderregel kan op een van de volgende waarden worden ingesteld:

    - **Geen**. de orderregel is nooit bewerkstelligd.
    - **Gereed**: de orderregel is bewerkstelligd en toegewezen aan een locatie.
    - **Gereed**: de orderregel is bewerkstelligd, maar kan niet worden toegewezen aan een locatie. Uitzonderingen hebben meerdere subtypen die kunnen worden bekeken vanuit het DOM-werkgebied:

        - **Geen hoeveelheid beschikbaar**: er is geen beschikbare voorraad om de order aan toe te wijzen in de locaties.
        - **Maximale aantal afwijzingen**: voor de orderregel is de drempelwaarde voor het maximale aantal afwijzingen bereikt.
        - **Gegevenswijzigingsconflict**: de verkooporderregel is gewijzigd sinds de order was bewerkstelligd. Daarom kan het afhandelingsplan niet worden toegepast op de order.
        - **Orderregelspecifieke uitzondering**: de orderregel bevat meerdere uitzonderingen.

- Tijdens het invoeren van verkooporders kan het DOM-systeem in een interactieve modus worden uitgevoerd. Wanneer u een orderregel invoert en het product en de hoeveelheid hebt opgegeven, kunt u **Regel bijwerken** en vervolgens onder **DOM** de optie **Afhandelingslocatie suggereren** selecteren. Vervolgens wordt een lijst met locaties weergegeven die is gebaseerd op DOM-regels waarmee de hoeveelheid op de orderregel kan worden afgehandeld. Deze lijst wordt gesorteerd op basis van afstand. Selecteer een locatie om de site en het magazijn in te stellen op de verkooporderregel. Deze functionaliteit werkt alleen als er een bestaand, actief afhandelingsprofiel bestaat dat overeenkomt met de verkoopoorsprong en leveringsmethode op de verkoopregel.
- Als u de DOM-uitvoeringslogboeken voor een verkooporderregel wilt weergeven, selecteert u **Verkooporderregel** en selecteert u onder **DOM** de optie **DOM-logboeken weergeven**. In de DOM-logboeken worden alle gebeurtenissen en logboeken weergegeven die zijn gegenereerd tijdens de DOM-uitvoering. De logboeken kunnen u meer inzicht bieden in de redenen waarom een bepaalde locatie is toegewezen aan de orderregel en welke regels en beperkingen bij het toewijzen een rol hebben gespeeld. Op het tabblad **Beheren** zijn de DOM-logboeken ook beschikbaar op het niveau van de koptekst van de verkooporder.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Een opschoontaak voor DOM-afhandelingsplannen uitvoeren

Terwijl de DOM-verwerking wordt uitgevoerd, worden er afhandelingsplannen gemaakt. In het systeem worden talloze afhandelingsplannen bewaard. Als u beperkingen wilt stellen aan het aantal afhandelingsplannen dat in het systeem wordt bewaard, kunt u een batchtaak maken om oudere afhandelingsplannen te verwijderen, op basis van de waarde **Bewaarperiode in dagen**.

1. Ga naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Batchverwerking \> Instelling van taak voor verwijdering van DOM-afhandelingsgegevens**. 
1. Selecteer een geconfigureerde batchgroep in het veld **Batchgroep**.
1. Selecteer **Terugkeer** en geef het terugkeerpatroon van de batchtaak op.
1. Selecteer **OK**.

## <a name="more-information"></a>Meer informatie

Houd rekening met het volgende als u de DOM-functie gebruikt:

- Momenteel wordt in DOM alleen gekeken naar orders die worden gemaakt via afzetkanalen voor handel. Verkooporders worden aangemerkt als detailhandelverkooporders wanneer de optie **Handelverkoop** is ingesteld op **Ja**.
- Microsoft heeft DOM niet getest met geavanceerde magazijnbeheerfuncties. Klanten en partners moeten een zorgvuldige afweging maken om te bepalen of DOM compatibel is met de geavanceerde magazijnbeheermogelijkheden en -processen die relevant voor hen zijn.
- DOM is alleen beschikbaar in de cloudversie van Commerce. DOM wordt niet ondersteund in on-premises implementaties.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Gedistribueerd orderbeheer (DOM)
description: In dit artikel wordt de functionaliteit voor gedistribueerd orderbeheer (DOM) in Dynamics 365 Commerce beschreven.
author: josaw1
ms.date: 02/08/2022
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 26817321753c8e39d61957b4ea2004f20daf1b2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878507"
---
# <a name="distributed-order-management-dom"></a>Gedistribueerd orderbeheer (DOM)

[!include [banner](includes/banner.md)]

In dit artikel wordt de functionaliteit voor gedistribueerd orderbeheer (DOM) in Microsoft Dynamics 365 Commerce beschreven.

DOM is een optimalisatieoplossing voor de afhandeling van orders via meerdere kanalen die u kunt gebruiken om de orderafhandeling in een toeleveringsketennetwerk te optimaliseren. Met DOM zorgt u ervoor dat producten in de juiste hoeveelheden, vanuit de juiste bronnen en op de juiste tijden aan uw klanten worden geleverd. Daarnaast kunt u hiermee de winst maximaliseren, de kosten minimaliseren en aan servicevereisten voldoen.

DOM gebruikt MIP (Mixed Integer Programming) en modellen voor voorspellende analyses om optimalisaties uit te voeren op batchniveau en op het niveau van afzonderlijke orders. Hierdoor kunnen detailhandelaren gedefinieerde regels gebruiken om een groot aantal tegenstrijdige behoeften ten aanzien van orderafhandeling in balans te brengen. In een modern toeleveringsnetwerk waarbij de afhandeling van producten via meerdere kanalen kan worden uitgevoerd, moeten organisaties zich snel aanpassen aan orderwijzigingen, problemen met de leveranciersbeschikbaarheid en een sterke toename in de vraag. Met DOM kunt u de afhandeling van orders optimaliseren en de juiste bronnen voor de levering van producten vinden op basis van zakelijke beperkingen en doelstellingen, zoals het minimaliseren van kosten door orders af te handelen via de dichtstbijzijnde bronnen. DOM gebruikt de afstand tussen bronnen voor productafhandeling en de verzenddoelen, kostenfactoren die zijn gedefinieerd als optimalisatiedoelstellingen en regels die als beperkingen zijn gedefinieerd, zoals voorraad op afhandelingsknooppunten, om de orderafhandeling te optimaliseren. Met DOM kunnen meerdere profielen worden gedefinieerd waarmee bedrijven verschillende optimalisatiestrategieën kunnen uitvoeren, afhankelijk van het type bedrijfs- of klantsegment. 

In de volgende afbeelding wordt de levenscyclus van een verkooporder in een DOM-systeem weergegeven.

![Levenscyclus van een verkooporder in de context van DOM.](./media/flow.png "Levenscyclus van verkooporders in de context van DOM")

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
    - **Type oplossing**: selecteer een waarde. In Commerce zijn twee typen oplossingen beschikbaar: **Productieoplossing** en **Vereenvoudigde oplossing**. Voor alle machines waarop een DOM-systeem wordt uitgevoerd (alle servers die deel uitmaken van de groep DOMBatch), moet **Productieoplossing** zijn geselecteerd. Voor Productieoplossing is de speciale licentiesleutel vereist die standaard in licentie wordt gegeven en wordt geïmplementeerd in productieomgevingen. In nieuwere Tier 2+-omgevingen is Productieoplossing al ingeschakeld. Voor niet-productieomgevingen moet deze licentiesleutel handmatig worden geïmplementeerd. Ga als volgt te werk om de licentiesleutel handmatig te implementeren:

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
    > In versies 10.0.12 en hoger van Commerce moet **Mogelijkheid om locaties op te geven als 'Verzenden ' of 'Ophalen' binnen Afhandelingsgroep** zijn ingeschakeld in het werkgebied **Functiebeheer**.
    >
    > Met deze functie kunt u nieuwe configuraties toevoegen op de pagina **Afhandelingsgroep**, zodat u kunt opgeven of het magazijn kan worden gebruikt voor verzending en dat de combinatie van magazijn en winkel kan worden gebruikt voor verzenden en/of ophalen. 
    >
    > Als u de functie inschakelt, worden de opties die beschikbaar zijn voor de selectie van locaties bij het maken van orders voor ophalen of verzenden, in POS bijgewerkt.
    >
    > Als u deze functie inschakelt, worden ook de pagina's in POS bijgewerkt wanneer de bewerkingen 'Alles verzenden ' of 'Geselecteerd verzenden' zijn geselecteerd.

9. Als u regels wilt opgeven, gaat u naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Instellingen \> Regels beheren**. Momenteel worden de volgende DOM-regels ondersteund:

    - **Regel voor minimumvoorraad**: met dit regeltype kunnen organisaties een bepaalde hoeveelheid van een product op voorraad houden voor andere doeleinden dan orderafhandeling. Organisaties kunnen het bijvoorbeeld onwenselijk vinden als alle beschikbare voorraad in een winkel door het DOM-systeem wordt gebruikt voor orderafhandeling. In plaats daarvan willen ze mogelijk enige voorraad reserveren voor klanten die de winkel bezoeken. Wanneer dit regeltype wordt gebruikt, kunt u per locatie of groep locaties opgeven welke voorraad minimaal moet worden behouden voor een categorie producten, een afzonderlijk product of een productvariant. U kunt de minimumvoorraad ook opgeven door een prioriteit voor aanvullende categorieën te gebruiken. Als een product in meerdere categorieën valt, krijgt een aanvullende categorie de hoogste prioriteit voor alle regels waarvoor u categorieën kunt gebruiken.
    - **Prioriteitsregel voor afhandelingslocatie**: met dit regeltype kunnen organisaties een hiërarchie voor locaties opgeven om de prioriteit te bepalen die door de DOM-engine moet worden gebruikt bij het identificeren van afhandelingslocaties voor bepaalde producten. Het geldige prioriteitsbereik is 1 tot en met 10, waarbij 1 voor de hoogste prioriteit staat en 10 voor de laagste. Locaties met een hogere prioriteit komen in aanmerking vóór locaties met een lagere prioriteit. Als de regel wordt gedefinieerd als een vaste beperking, worden orders alleen toegewezen aan locaties waarvoor prioriteiten zijn opgegeven. DOM geeft er de voorkeur aan om orders volledig vanaf één locatie te verzenden. Als een gehele order en de regels ervan niet beschikbaar zijn op een locatie met prioriteit 1, wordt daarom geprobeerd deze af te handelen vanaf een locatie met prioriteit 2.
    - **Regel voor gedeeltelijke orders**: in versie 10.0.5 van Retail is de parameter **Order afhandelen vanaf slechts één locatie** gewijzigd in **Maximum afhandelingslocaties**. Met de oude parameter konden gebruikers configureren of orders kunnen worden afgehandeld vanaf slechts één locatie of zoveel locaties als mogelijk is. Met de nieuwe parameter kunnen gebruikers opgeven of de order kan worden afgehandeld op basis van een bepaalde set locaties (maximaal 5) of zoveel locaties als mogelijk is. Voor alle opties, behalve de optie voor afhandeling vanaf één locatie, wordt de regel opgesplitst, omdat de verwerking van orders per regel wordt uitgevoerd. Deze regel werkt alleen met Productieoplossing.
    - **Regel voor offline afhandelingslocatie**: met deze regel kunnen organisaties een locatie of groep locaties als offline of niet beschikbaar instellen voor DOM, zodat orders niet aan die locaties kunnen worden toegewezen voor afhandeling.
    - **Regel voor maximale afwijzingen**: met deze regel kunnen organisaties een drempelwaarde voor afwijzingen opgeven. Wanneer de drempelwaarde wordt bereikt, wordt een order of orderregel door de DOM-processor als uitzondering gemarkeerd en wordt deze uitgesloten van verdere verwerking. Om de prestaties te waarborgen, wordt niet naar de geschiedenis van alle afwijzingen gekeken. 

        Als orderregels zijn toegewezen aan een locatie, kan de locatie een toegewezen orderregel afwijzen als deze om een of andere reden niet kan worden afgehandeld. Afgewezen regels worden als uitzondering gemarkeerd en weer opgenomen in de groep voor verwerking tijdens de volgende uitvoering. Tijdens de volgende uitvoering wordt geprobeerd de afgewezen regel toe te wijzen aan een andere locatie. Ook de nieuwe locatie kan de toegewezen orderregel afwijzen. Deze cyclus van toewijzing en afwijzing kan meerdere keren worden herhaald. Wanneer de opgegeven drempelwaarde voor het aantal afwijzingen wordt bereikt, wordt de orderregel als permanente uitzondering gemarkeerd en wordt de regel niet meer gekozen voor toewijzing. De orderregel komt pas weer in aanmerking voor toewijzing als een gebruiker de status van de orderregel opnieuw instelt.

    - **Regel voor maximale afstand**: met deze regel kunnen organisaties de maximale afstand van een locatie of groep locaties voor afhandeling van de order opgeven. Als er meerdere regels met verschillende maximumafstanden zijn opgegeven voor een locatie, wordt de kortste maximumafstand toegepast.
    - **Regel voor maximumorders**: met deze regel kunnen organisaties opgeven hoeveel orders maximaal kunnen worden verwerkt op een locatie of groep locaties. Tijdens het optimalisatieproces wordt door het systeem gekeken naar orders die niet vanaf deze locaties zijn verzonden. Deze controle wordt op alle profielen uitgevoerd. Als er overlappende maximum aantallen orders voor profielen voor dezelfde locatie worden gedefinieerd, wordt daarom rekening gehouden met het maximum aantal orders dat is gedefinieerd in alle profielen. 

    Voor alle bovenstaande regeltypen kunnen de volgende algemene kenmerken worden opgegeven:

    - **Begindatum** en **Einddatum**: u kunt deze velden gebruiken om voor elke regel geldigheidsdatums in te stellen.
    - **Uitgeschakeld**: alleen regels met de waarde **Nee** voor dit veld worden gebruikt tijdens een DOM-uitvoering.
    - **Vaste beperking**: een regel kan als vaste beperking of niet-vaste beperking worden gedefinieerd. Elke DOM-uitvoering wordt op twee manieren uitgevoerd. De eerste keer wordt elke regel beschouwd als een vaste beperking, ongeacht de instelling van dit veld. Met andere woorden: elke regel wordt toegepast. De enige uitzondering is de regel **Prioriteit van locatie**. Voor de tweede uitvoering worden de regels verwijderd die niet als vaste beperking zijn ingesteld. De orders of orderregels die niet aan locaties waren toegewezen toen alle regels werden toegepast, worden toegewezen aan locaties.

10. Afhandelingsprofielen worden gebruikt om een verzameling regels, rechtspersonen, oorsprongen van verkooporders en leveringsmethoden te groeperen. Elke DOM-uitvoering vindt plaats voor een bepaald afhandelingsprofiel. Op deze manier kunnen organisaties een verzameling regels opgeven en uitvoeren voor een verzameling rechtspersonen, voor orders met bepaalde oorsprongen van verkooporders en leveringsmethoden. Als er verschillende verzamelingen regels moeten worden uitgevoerd voor verschillende verzamelingen oorsprongen van verkooporders of leveringsmethoden, kunnen de afhandelingsprofielen overeenkomstig worden gedefinieerd. Ga als volgt te werk om afhandelingsprofielen in te stellen:  

    1. Ga naar **Retail en Commerce \> Gedistribueerd orderbeheer \> Instellingen \> Afhandelingsprofielen**.
    2. Selecteer **Nieuw**.
    3. Geef waarden op in de velden **Profiel** en **Beschrijving**.
    4. Stel de optie **Resultaat automatisch toepassen** in. Als u deze optie instelt op **Ja**, worden de resultaten van de DOM-uitvoering voor het profiel automatisch op de verkooporderregels toegepast. Stelt u **Nee** in, dan kunnen de resultaten alleen worden weergegeven in het afhandelingsplan. Deze worden niet toegepast op de verkooporderregels.
    5. Als het DOM-profiel moet worden uitgevoerd voor orders met alle oorsprongen van verkooporders, inclusief orders waarvoor geen oorsprong van de verkooporder is opgegeven, stelt u de optie **Orders met lege verkoopoorsprong verwerken** in op **Ja**. Als u het profiel voor slechts een paar oorsprongen van verkooporders wilt uitvoeren, kunt u deze opgeven op de pagina **Verkoopoorsprongen**, zoals verderop wordt uitgelegd.

        > [!NOTE]
        > In Commerce 10.0.12 en hogere versies moet de functie **Mogelijkheid om afhandelingsgroep toe te wijzen aan een afhandelingsprofiel** zijn ingeschakeld in het werkgebied **Functiebeheer**. Met deze functie kunt u een lijst met magazijnen opgeven die moeten worden gebruikt bij het uitvoeren van de optimalisatie met een afhandelingsprofiel. Als deze lijst met magazijnen niet is opgegeven, wordt gekeken naar alle magazijnen van rechtspersonen die in het profiel zijn opgegeven.
        >
        > Met deze functie wordt op de pagina **Afhandelingsprofiel** een nieuwe configuratie toegevoegd die kan worden gekoppeld aan één afhandelingsgroep. 
        >
        > Als u de afhandelingsgroep selecteert, worden de DOM-regels voor dat afhandelingsprofiel efficiënt uitgevoerd op basis van de verzendmagazijnen die in de afhandelingsgroep zijn opgenomen. 
        > 
        > Als u deze functie effectief wilt gebruiken, moet u ervoor zorgen dat er één afhandelingsgroep is die alle verzendmagazijnen bevat en vervolgens die afhandelingsgroep aan het afhandelingsprofiel koppelen.

    6. Selecteer op het sneltabblad **Rechtspersonen** de optie **Toevoegen** en selecteer vervolgens een rechtspersoon.
    7. Selecteer op het sneltabblad **Regels** de optie **Toevoegen** en selecteer de regel die u wilt koppelen aan het profiel.
    8. Herhaal de vorige twee stappen tot alle vereiste regels aan het profiel zijn gekoppeld.
    9. Selecteer **Opslaan**.
    10. Selecteer in het actiepaneel op het tabblad **Instellingen** de optie **Leveringsmethoden**.
    11. Selecteer **Nieuw** op de pagina **Leveringsmethoden**.
    12. Selecteer de rechtspersoon in het veld **Bedrijf**. De lijst met bedrijven blijft beperkt tot de rechtspersonen die u eerder hebt toegevoegd.
    13. Selecteer in het veld **Leveringsmethode** de leveringsmethode die aan dit profiel moet worden gekoppeld. Een leveringsmethode kan niet aan meerdere actieve profielen worden gekoppeld.
    14. Herhaal de vorige twee stappen tot alle vereiste leveringsmethoden aan het profiel zijn gekoppeld.
    15. Sluit de pagina **Leveringsmethoden**.
    16. Selecteer in het actiepaneel op het tabblad **Instellingen** de optie **Oorsprongen van verkooporders**.
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

Nadat de regels, voorraadbeperkingen en optimalisatie zijn toegepast, wordt de locatie gekozen die het dichtst bij het afleveradres van de klant ligt. In DOM worden adressen van het type **Levering** omgezet in breedte- en lengtegraden. Vervolgens wordt het afleveradres op de verkooporder omgezet in breedte- en lengtegraden en worden de breedte- en lengtegraden van het adres bijgewerkt voor toekomstig gebruik. DOM is afhankelijk van Bing Kaarten om nauwkeurige breedte- en lengtegraden op basis van adres-, plaats- en postcodegegevens te bepalen.

DOM gebruikt de API van Bing Kaarten om de afstand door de lucht of via de weg te berekenen, afhankelijk van de instellingen. Deze informatie wordt vervolgens gebruikt om de kosten van verzending te bepalen. Volgens het optimalisatiemodel wordt de voorkeur gegeven aan de afhandeling van een volledige order vanaf één locatie. Zelfs als een deel van een order beschikbaar is in dezelfde plaats of postcode, is het model geoptimaliseerd om het aantal zendingen te beperken. 

In DOM wordt gezocht naar beschikbare voorraad door voorhanden voorraad in magazijn V2-entiteiten te controleren. Tijdens elke batchuitvoering worden orders door DOM in batches opgesplitst, afhankelijk van de waarde van de parameter **DOM-processor** voor taken die in het profiel zijn gedefinieerd. Deze parameter heeft een standaardwaarde van **2000**. Als er 10.000 orderregels worden geoptimaliseerd tijdens een uitvoering en de parameter **DOM-processor** wordt ingesteld op de standaardwaarde **2000**, worden er bijvoorbeeld vijf batches gemaakt die tegelijk worden verwerkt. Vervolgens worden de afhandelingsplannen afkomstig uit het optimalisatiemodel toegepast op de regel. Als de orderregel tussen twee locaties moet worden opgesplitst, zorgt DOM ervoor dat prijzen en belastingen op de juiste manier over de regels worden verdeeld.

![Criteria voor de verkooporder.](./media/ordercriteria.png "Criteria voor verkooporder")

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
- Microsoft heeft DOM niet getest met geavanceerde magazijnbeheerfuncties. Daarom moeten klanten en partners een zorgvuldige afweging maken om te bepalen of DOM compatibel is met de geavanceerde magazijnbeheermogelijkheden en -processen die relevant voor hen zijn. Met geavanceerd magazijnbeheer kunnen configureerbare dimensies, zoals de voorraadstatus, worden geconfigureerd die geen nauwkeurig inzicht bieden in de beschikbare voorraad. DOM biedt een uitbreidbare methode voor het instellen van beschikbare voorraad voor implementaties met geavanceerd magazijnbeheer. DOM kan worden gebruikt om te werken met aangepaste waarden van voorraadstatussen en andere dimensies.

    De uitbreidbaarheid in DOM is beperkt omdat optimalisatie plaatsvindt in het vooraf ontwikkelde MIP-model waarin de optimalisatie en de beperkingen worden bepaald. Er zijn al verschillende uitbreidbare punten beschikbaar voor het instellen van de optimalisatie van voorraad en naverwerking. DOM-profielen kunnen per verkoopoorsprong en leveringsmethode verschillen. De oorsprong van verkooporders kan worden ingesteld tijdens de orderopname en er kunnen verschillende optimalisatiestrategieën worden gebruikt op basis van deze waarden. DOM ondersteunt ook het maken van aangepaste batchtaken waarmee de DOM-processortaak als invoer kan worden gebruikt en het profiel als een parameter kan worden doorgegeven. Daarom kan de ene optimalisatie na de andere worden uitgevoerd om verschillende bedrijfsscenario's te ondersteunen.

- DOM is alleen beschikbaar in de cloudversie van Commerce. DOM wordt niet ondersteund in on-premises implementaties.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

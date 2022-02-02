---
title: Loyaliteitsoverzicht
description: In dit onderwerp worden de loyaliteitsmogelijkheden in Dynamics 365 Commerce en de bijbehorende instellingsstappen beschreven om de detailhandelaar te helpen eenvoudig aan de slag te gaan met hun loyaliteitsprogramma's.
author: scott-tucker
ms.date: 07/21/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.custom:
- "16201"
- intro-internal
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 57512bbd735e26ba31e00518ca8179f2d9b14bc4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985157"
---
# <a name="loyalty-overview"></a>Overzicht van loyaliteit

[!include [banner](includes/banner.md)]

Loyaliteitsprogramma's kunnen helpen klantloyaliteit te verhogen door klanten te belonen voor hun interactie met het merk van de detailhandelaar. In Dynamics 365 Commerce kunt u eenvoudige of complexe loyaliteitsprogramma's instellen die gelden voor verschillende rechtspersonen in een handelskanaal. In dit onderwerp worden de loyaliteitsmogelijkheden in Commerce en de bijbehorende instellingsstappen beschreven om detailhandelaars te helpen eenvoudig aan de slag te gaan met hun loyaliteitsprogramma's.

U kunt uw loyaliteitsprogramma zo instellen dat het de volgende opties bevat.

- Stel meerdere typen beloningen in die u in uw loyaliteitsprogramma's aanbiedt en houdt de participatie in uw loyaliteitsprogramma's bij.
- Stel loyaliteitsprogramma's in die de verschillende beloningsincentives weergeven die u aanbiedt. U kunt loyaliteitsprogrammarijen opnemen om grotere incentives en beloningen aan te bieden aan klanten die vaker winkelen of meer geld uitgeven in uw winkels.
- Definieer verdienregels om de activiteiten te identificeren die een klant moet voltooien om beloningen te verdienen. U kunt ook inruilregels instellen om aan te geven wanneer en hoe een klant beloningen kan inruilen.
- Geef loyaliteitskaarten uit vanaf elk kanaal dat deelneemt aan uw loyaliteitsprogramma's, en koppel loyaliteitskaarten aan een of meer loyaliteitsprogramma's waaraan de klant kan deelnemen. U kunt ook een klantrecord koppelen aan een loyaliteitskaart om de klant loyaliteitspunten van meerdere kaarten samen te laten voegen en deze in te ruilen.
- Pas handmatig loyaliteitskaarten aan of boek het saldo van loyaliteitsbeloningen van een kaart naar een andere over om een klant bij te werken of te belonen.

## <a name="setting-up-loyalty-programs"></a>Loyaliteitsprogramma's instellen

U moet verschillende onderdelen instellen om de loyaliteitsfunctie in te schakelen in Commerce. Het volgende schema geeft de loyaliteitscomponenten aan en hoe ze met elkaar zijn verbonden.

![Processtroom loyaliteitsinstellingen.](./media/loyaltyprocess.gif "Loyaliteitscomponenten en onderlinge relaties")

## <a name="loyalty-components"></a>Loyaliteitscomponenten

De volgende tabel beschrijft elke component en waar deze in de loyaliteitsinstellingen wordt gebruikt.

| component                                        | Omschrijving | Waar deze wordt gebruikt |
|--------------------------------------------------|-------------|-----------------|
| Kortingen instellen (vereiste)                  | Stel de kortingen in die u aan uw loyaliteitsklanten aanbiedt. Bijvoorbeeld, u kunt 5 procent korting op alle kledingproducten bieden. | Kortingen moeten aan prijsgroepen worden toegevoegd voordat ze in een loyaliteitsprogramma kunnen worden opgenomen. Prijsgroepen worden toegewezen aan loyaliteitsprogramma's en loyaliteitsrijen. |
| Prijsgroepen instellen (vereiste)               | Prijsgroepen worden gebruikt om prijzen en kortingen voor producten te maken en te beheren. Stel de prijsgroepen in die de kortingen bevatten die op uw loyaliteitsprogramma's van toepassing zijn. | Prijsgroepen worden toegewezen aan loyaliteitsprogramma's en loyaliteitsprogrammarijen. |
| Kanalen instellen (vereiste)                   | Handelskanalen zijn de winkels die deelnemen aan uw loyaliteitsprogramma's, zoals een fysieke winkel, een online winkel of een callcenter. U moet uw kanalen instellen voordat u er loyaliteitsprogramma's kunt aan toewijzen. | U wijst kanalen toe aan een loyaliteitsprogramma als het kanaal aan het loyaliteitsprogramma deelneemt. |
| De loyaliteitsbetalingsmethode instellen (vereiste) | Om ervoor te zorgen dat de loyaliteitspunten in elk kanaal kunnen worden ingewisseld, zoals fysieke winkels, online winkels of call centers, moet u het opslaglocatiebereik instellen voor de loyaliteitskaarten op de pagina **Kaartnummers**. | Stel een betalingsmethode in van het type loyaliteit, en wijs vervolgens de loyaliteitsbetalingsmethode toe aan de kanalen die aan het loyaliteitsprogramma deelnemen. |
| Datumintervallen instellen                            | De datumintervallen bieden een flexibele manier om de periode in te stellen die op loyaliteitsrijen van toepassing is. Gebruik datumintervallen om op te geven hoe lang een klant in een rij kan blijven of hoe lang een klant een activiteit moet uitvoeren om voor een rij in aanmerking te komen. | Datumintervallen zijn alleen van toepassing als u rijen in uw loyaliteitsprogramma's gebruikt. U selecteert het datuminterval dat van toepassing is op programmarijen, en ook de datumintervallen die gelden voor programmarijregels. |
| Beloningspunten instellen                             | Beloningspunten zijn de types beloning die u uw klanten aanbiedt. Beloningenpunten kunnen inruilbaar of niet-inruilbaar zijn. Inruilbare beloningspunten kunnen worden ingeruild voor producten. Niet-inruilbare beloningspunten worden gebruikt om zaken bij te houden of om een klant in een andere rij in een loyaliteitsprogramma te plaatsen. | Er wordt verwezen naar beloningspunten in rijregels, en deze worden gebruikt om een klant aan een specifieke rij toe te wijzen. Er wordt ook naar de beloningspunten verwezen in loyaliteitsschema's voor verdien- en inruilregels. Bij verdienregels geeft u de beloningen op die een klant kan verdienen voor een specifieke activiteit. In inruilregels, geeft u de beloning op die de klant kan krijgen. |
| Loyaliteitsprogramma's instellen                          | Loyaliteitsprogramma's zijn belangrijkste loyaliteitsrechtpersoon die u aanbiedt. Aan elk loyaliteitsprogramma kunnen ook loyaliteitsrijen zijn toegewezen. Kortingen en de prijsgroepen worden toegewezen aan de loyaliteitsprogramma's op programmaniveau of op rijniveau. | U maakt loyaliteitsschema's voor uw loyaliteitsprogramma's. U wijst loyaliteitskaarten toe aan uw loyaliteitsprogramma's, en loyaliteitskaarten kunnen aan een klant worden toegewezen. Kanalen nemen deel aan de loyaliteitsprogramma's die aan de loyaliteitsschema's worden toegewezen. Elke klant die een loyaliteitskaart heeft, kan deelnemen aan de loyaliteitsprogramma's die aan de kaart zijn toegewezen. |
| Loyaliteitsrijen en rijregels instellen              | Loyaliteitsrijen zijn optionele niveaus die u kunt definiëren voor uw loyaliteitsprogramma's. U kunt basiskortingen en beloningen instellen voor alle klanten die aan het loyaliteitsprogramma deelnemen, en u kunt extra kortingen en beloningen instellen voor klanten die de verschillende niveaus in het programma behalen. Voor elke loyaliteitsrij die u definieert, kunt u de regels instellen waarmee een klant in aanmerking komt voor die rij. U kunt ook bepalen hoe lang klanten in die rij kunnen blijven nadat ze de rij hebben bereikt. | Loyaliteitsrijen en loyaliteitsrijregels worden gedefinieerd in de loyaliteitsprogramma's. Als u geen loyaliteitsrijen definieert, komen alle klanten die aan het loyaliteitsprogramma deelnemen in aanmerking voor kortingen die u in de loyaliteitsprogrammaprijsgroep toewijst. Als u loyaliteitsrijen definieert, kunt u verdienregels en inruilregels instellen voor de loyaliteitsrijen in het loyaliteitsschema. |
| Loyaliteitsschema's instellen                           | Loyaliteitsschema's geven de verdienregels en inruilregels op die gelden voor een geselecteerd loyaliteitsprogramma. U wijst kanalen toe aan een loyaliteitsschema om te identificeren welke loyaliteitsprogramma's, verdienregels en inruilregels gelden voor een winkel. | Een loyaliteitsschema wordt toegewezen aan een loyaliteitsprogramma en aan kanalen. U kunt meerdere loyaliteitsschema's toewijzen aan hetzelfde loyaliteitsprogramma, en u kunt meerdere loyaliteitsschema's toewijzen aan veel kanalen. |
| Loyaliteitskaarten instellen                             | Een loyaliteitskaart geeft de houder het recht om deel te nemen aan de loyaliteitsprogramma's die aan de kaart zijn toegewezen. Loyaliteitskaarten kunnen anoniem worden uitgegeven, of ze kunnen aan een specifieke klant worden toegewezen. U kunt de loyaliteitstransacties voor een specifieke kaart weergeven, en u kunt een overzicht weergeven van loyaliteitspunten die op de kaart zijn samengevoegd. U kunt loyaliteitskaarten uitgeven vanuit elk kanaal. U kunt een loyaliteitskaart ook handmatig aanpassen om de klant in een andere rij te plaatsen, loyaliteitspunten toe te voegen, of het loyaliteitspuntensaldo van de ene kaart overboeken naar de andere over te zetten. | U wijst loyaliteitsprogramma's toe aan een loyaliteitskaart. |

## <a name="loyalty-processes"></a>Loyaliteitsprocessen

De volgende tabel beschrijft de processen die moeten worden uitgevoerd om de loyaliteitsconfiguraties en gegevens naar uw winkels te verzenden, en om de loyaliteitstransacties van uw winkels op te halen.

| Procesnaam                         | Beschrijving | Paginanaam |
|--------------------------------------|-------------|-----------|
| 1050 (loyaliteitsinformatie)           | Voer dit proces uit om de loyaliteitsgegevens van Commerce naar de winkels te verzenden. Het is een goed idee dit proces te plannen om vaak te worden uitgevoerd, zodat de loyaliteitsgegevens naar alle winkels worden verzonden. | Distributieplanning |
| Loyaliteitsschema verwerken              | Voer dit proces uit om loyaliteitsschema's te koppelen aan de kanalen waaraan het loyaliteitsschema is toegewezen. Dit proces kan worden gepland om als een batchproces te worden uitgevoerd. U moet dit proces uitvoeren als u de gegevens van de loyaliteitsconfiguratie wijzigt, zoals loyaliteitsschema's, loyaliteitsprogramma's, of de punten van de loyaliteitsbeloning. | Loyaliteitsschema verwerken |
| Verdiende loyaliteitspunten boeken in batches | Voer dit proces uit om loyaliteitskaarten bij te werken zodat ze transacties bevatten die offline werden verwerkt. Dit proces is alleen van toepassing als het selectievakje **Verdiende punten in batches boeken** is ingeschakeld op de pagina **Gedeelde Commerce-parameters**, zodat de beloningen offline kunnen worden verdiend. | Verdiende loyaliteitspunten boeken in batches |
| Niveaus van loyaliteitskaarten bijwerken            | Voer dit proces uit om de verdienende activiteit van de klant te beoordelen volgens de rijregels voor een loyaliteitsprogramma en om de rijstatus van de klant bij te werken. Dit proces is alleen nodig als u de rijregels in loyaliteitsprogramma's wijzigt en u wilt dat de bijgewerkte regels retroactief worden toegepast op loyaliteitskaarten die reeds zijn uitgegeven. Dit proces kan worden uitgevoerd als een batchproces of voor afzonderlijke kaarten. | Niveaus van loyaliteitskaarten bijwerken |

## <a name="loyalty-capabilities"></a>Loyaliteitsmogelijkheden

- Met behulp van de prijsgroepen die zijn gekoppeld aan het loyaliteitsprogramma en de loyaliteitsniveaus, kunnen detailhandelaren eenvoudig speciale prijzen en kortingen voor loyaliteitsleden maken.

- Als onderdeel van een loyaliteitsschema kunnen detailhandelaren verschillende verdien- en inwisselregels op niveaus maken om de beloningen te differentiëren voor klanten op verschillende niveaus. Detailhandelaren kunnen nu ook 'lidmaatschappen' opnemen als onderdeel van de verdien- en inwisselregels, zodat bepaalde groepen klanten deel van bestaande niveaus kunnen uitmaken, maar toch verschillend kunnen worden beloond. Dit zorgt ervoor dat er geen aanvullende niveaus hoeven te worden gemaakt.
    
    > [!NOTE]
    > De verdienregels binnen een loyaliteitsschema zijn extra. Als u bijvoorbeeld een regel maakt om een gouden lid te belonen met 10 punten voor elke Amerikaanse dollar en u ook een regel maakt voor een klant met het lidmaatschap 'veteraan' om 5 punten beloning te geven voor elke Amerikaanse dollar, dan verdient een veteraan die ook een gouden lid is, 15 punten voor 1 Amerikaanse dollar, omdat de klant voor beide in aanmerking komt. Als de veteraan echter geen lid van het gouden niveau was, zou de klant 5 punten voor elke dollar verdienen. Voer in verband met de wijzigingen in de kanalen de taken **Loyaliteitsschema verwerken** en **1050** (loyaliteitsinformatie)-uit.
    
    ![Verdienen op basis van lidmaatschappen.](./media/Affiliation-based-earning.png "Verdienen op basis van lidmaatschappen")

- Detailhandelaren hebben vaak speciale prijzen voor een bepaalde groep klanten waar ze niet het loyaliteitsprogramma op willen toepassen. Bijvoorbeeld groothandelaren of werknemers die speciale prijzen krijgen en geen loyaliteitspunten. Vaak worden 'lidmaatschappen' gebruikt om dergelijke klantengroepen de speciale prijzen te bieden. Als de detailhandelaar wil verhinderen dat bepaalde klantengroepen loyaliteitspunten verdienen, kan deze een of meer lidmaatschappen opgeven in de sectie **Uitgesloten lidmaatschappen** van het loyaliteitsschema. Wanneer klanten die tot uitgesloten lidmaatschappen behoren, bestaande loyaliteitsleden zijn, kunnen ze geen loyaliteitspunten verdienen met hun aankopen. Voer in verband met de wijzigingen in de kanalen de taken **Loyaliteitsschema verwerken** en **1050** (loyaliteitsinformatie)-uit.

    ![Uitgesloten lidmaatschappen.](./media/Excluded-affiliations.png "Lidmaatschappen uitsluiten van loyaliteitspunten")
    
- Met het verkooppunt (POS) wordt aan detailhandelaren de flexibiliteit geboden om de fysieke loyaliteitskaarten te gebruiken of automatisch een uniek loyaliteitskaartnummer te genereren. Als u het automatisch genereren van loyaliteitskaarten in de winkels wilt inschakelen, schakelt u **Loyaliteitskaartnummer genereren** in het functionaliteitsprofiel in dat is gekoppeld aan de winkel. Voor online kanalen kunnen detailhandelaren de API IssueLoyaltyCard gebruiken om loyaliteitskaarten aan klanten uit te geven. Detailhandelaren kunnen een loyaliteitskaartnummer verstrekken aan deze API, dat wordt gebruikt voor het genereren van de loyaliteitskaart, of het systeem gebruikt de sequentie van loyaliteitskaartnummers die is ingesteld in Commerce. Echter, als de getalreeks niet aanwezig is en de detailhandelaar geen loyaliteitskaartnummer verstrekt bij de aanroep van de API, wordt een foutbericht weergegeven.

    ![Loyaliteitskaart genereren.](./media/Generate-loyalty-card.png "Automatisch loyaliteitskaartnummer genereren")

- Verdiende en ingewisselde loyaliteitspunten kunnen nu worden opgeslagen voor elke transactie en verkooporders ten opzichte van de verkoopregel, zodat hetzelfde bedrag kan worden terugbetaald of teruggekregen in het geval van volledige of gedeeltelijke retouren. Bovendien biedt zichtbaarheid van punten op het niveau van de verkoopregel de mogelijkheid voor callcentergebruikers om vragen van klanten te beantwoorden over hoeveel punten zijn verdiend of ingewisseld voor elke regel. Vóór deze wijziging werden beloningspunten altijd opnieuw berekend tijdens retourneringen, wat leidde tot een ander bedrag dan het origineel, als de verdien- of inwisselregels zijn gewijzigd en hadden callcentergebruikers geen inzicht in de specificatie van de punten. Het aantal punten kan worden weergegeven op het formulier **Kaarttransacties** voor elke loyaliteitskaart. Als u deze functie wilt inschakelen, schakelt u de configuratie **Loyaliteitspunten per verkoopregel boeken** onder het tabblad **Gedeelde Commerce-parameters** \> **Algemeen** in.

    > [!NOTE]
    > Het wordt ten zeerste aangeraden deze functie in te schakelen om ervoor te zorgen dat in het geval van retouren de juiste hoeveelheid punten kan worden gerestitueerd of overgenomen van de klant.

- Detailhandelaren kunnen nu de vestigingsperiode voor elk beloningspunt definiëren. Een configuratie van de vestigingsperiode definieert de duur vanaf de verdiendatum, waarna de beloningspunten beschikbaar worden voor de klanten. Niet-gevestigde punten kunnen worden weergegeven in de kolom **Niet-gevestigde punten** op de pagina **Loyaliteitskaarten**. Wanneer de klanten bepaalde artikelen retourneren waarvoor de loyaliteitspunten zijn verdiend, worden de voorwaardelijk toegekende punten eerst in het systeem afgetrokken en wordt het saldo afgetrokken van de beschikbare punten. U kunt echter alleen instellen dat de beschikbare punten worden afgetrokken in plaats van aftrek van voorwaardelijk toegekende punten.

Bovendien kunnen detailhandelaren de maximale limiet aan beloningspunten per loyaliteitskaart definiëren. Dit veld kan worden gebruikt om het effect van loyaliteitsfraude te verminderen. Wanneer de maximale toegekende punten zijn bereikt, kan de gebruiker geen punten meer verdienen. De detailhandelaar kan besluiten deze kaarten te blokkeren totdat ze op mogelijke fraude zijn onderzocht. Als de detailhandelaar fraude vaststelt, kan deze de loyaliteitskaart blokkeren voor de klant en de klant markeren als geblokkeerd. Hiervoor stelt u de eigenschap **Klant blokkeren voor loyaliteitsinschrijving** in op **Ja** onder **Alle klanten** op het sneltabblad **Commerce**. Aan de geblokkeerde klanten kan in geen van de kanalen een loyaliteitskaart worden uitgegeven.

   ![Toekennen en maximale beloningspunten.](./media/Vesting-and-maximum-reward-points.png "Toekennen en maximale beloningspunten definiëren")

- Lidmaatschappen worden gebruikt om speciale prijzen en kortingen te bieden, maar er zijn enkele lidmaatschappen waarvan detailhandelaren niet willen dat hun klanten ze zien. Een lidmaatschap met de titel 'Veel uitgevende klant' wordt mogelijk niet goed ontvangen door sommige klanten. Bovendien zijn er lidmaatschappen die niet in de winkel moeten worden beheerd, bijvoorbeeld werknemers, omdat u niet wilt dat kassiers bepalen wie een werknemer is en dus werknemerskortingen bieden. Detailhandelaren kunnen nu de lidmaatschappen selecteren die in de kanalen moeten worden verborgen. Lidmaatschappen die zijn gemarkeerd als **In kanalen verbergen**, kunnen worden bekeken, toegevoegd of verwijderd in het POS. Echter, de prijzen en kortingen die zijn gekoppeld aan het lidmaatschap, worden nog steeds toegepast op de producten.

    ![Aansluitingen verbergen.](./media/Hide-affiliations.png "Lidmaatschappen verbergen in kanalen")
    
- Callcentergebruikers kunnen nu gemakkelijker een klant zoeken met behulp van hun loyaliteitskaartgegevens en naar de loyaliteitskaart van de klant en de pagina's met loyaliteitskaarttransacties navigeren vanaf de pagina **Klantenservice**.

    ![Klantenservice.](./media/Customer-service.png "Loyaliteitsinformatie voor de klant zoeken")
    
- Als met een loyaliteitskaart geknoeid is, moet een vervangende kaart worden gegenereerd en moeten de bestaande punten worden overgedragen aan de nieuwe kaart. De stroom voor de vervangende kaart is in deze release vereenvoudigd. Bovendien kunnen klanten sommige of al hun loyaliteitspunten schenken aan vrienden en familie. Wanneer punten worden overgeboekt, worden de puntcorrectieposten gemaakt voor elke loyaliteitskaart. De functionaliteit voor de vervangende kaart en de saldo-overdracht is toegankelijk vanaf de pagina **Loyaliteitskaarten**.

    ![Punten vervangen en overdragen.](./media/Replace-and-transfer-points.png "Loyaliteitskaart vervangen of saldo overdragen")
    
- Detailhandelaren willen mogelijk de effectiviteit van een bepaald kanaal vastleggen om klanten in een loyaliteitsprogramma op te nemen. De bron van inschrijving voor de loyaliteitskaart wordt nu opgeslagen, zodat detailhandelaren rapporten op deze gegevens kunnen uitvoeren. De bron van inschrijvingen wordt automatisch vastgelegd voor alle uitgegeven loyaliteitskaarten vanuit MPOS/CPOS of e-commercekanalen. Voor de loyaliteitskaarten die worden uitgegeven vanuit de back office-toepassing, kan de callcentergebruiker een geschikt kanaal selecteren.
- In eerdere versies konden detailhandelaren MPOS/CPOS gebruiken om loyaliteitspunten in te wisselen voor klanten in een winkel. Aangezien het loyaliteitssaldo in deze release echter in loyaliteitspunten wordt weergegeven, kon de kassamedewerker het valutawaardebedrag niet zien dat kon worden toegepast op de huidige transactie. De kassamedewerker moest de conversie van punten naar valuta uitvoeren alvorens te betalen met loyaliteitspunten. In de huidige release, nadat regels zijn toegevoegd aan de transactie, kan de kassamedewerker het bedrag zien dat de loyaliteitspunten kunnen dekken voor de huidige transactie, zodat het gemakkelijker is sommige of alle loyaliteitspunten op de transactie toe te passen. Bovendien ziet de kassier de punten die binnen de komende 30 dagen verlopen, zodat deze upselling of cross-selling kan uitvoeren om de klant te motiveren de verlopende punten uit te geven voor die transactie.

    ![Punten gedekt door loyaliteitssaldo.](./media/Points-covered-by-loyalty-balance.png "Saldo weergeven dat wordt gedekt door loyaliteitspunten")

    ![Vervallende punten.](./media/Expiring-points.png "Vervallende punten weergeven")

- In release 8.1.3 is de optie 'Betalen met loyalititeitskaart' in het callcenterkanaal ingeschakeld. Als u deze optie wilt inschakelen, maakt u een loyaliteitsbetalingsmethode en koppelt u deze aan het callcenter. 

    > [!NOTE]
    > Omdat de loyaliteitsbetalingen zijn ingesteld als kaartbetalingen, moet u een kaart selecteren op de pagina **Kaartinstellingen**. 

    ![Loyaliteitskaart configureren.](./media/LoyaltyCardSetup.png "Loyaliteitskaart configureren")

    Nadat deze is ingesteld, kunnen klanten hun loyaliteitspunten in het callcenter inwisselen. Bovendien hebben we de gebruikerservaring verder verbeterd door "Bedrag gedekt door loyaliteitspunten" weer te geven, zodat de callcentergebruikers niet naar een ander scherm hoeven te navigeren om het loyaliteitssaldo weer te geven.

- Veel detailhandelaren kennen loyaliteitspunten alleen toe op basis van de verkooptransacties, maar meer klantgerichte detailhandelaren willen hun klanten belonen voor al hun betrokkenheid bij het merk. Ze willen bijvoorbeeld beloningen geven voor het invullen van een online enquête, bezoek aan een winkel, 'leuk vinden' van de detailhandelaar op Facebook, tweeten over de detailhandelaar en meer. Hiertoe kan de detailhandelaar een willekeurig aantal overige activiteittypen definiëren en de bijbehorende verdienregels voor deze activiteiten bepalen. Er is ook een zichtbare Commerce Scale Unit-API 'PostNonTransactionalActivityLoyaltyPoints', die kan worden aangeroepen wanneer een activiteit wordt geïdentificeerd die de klant met loyaliteitspunten beloont. Deze API verwacht de loyaliteitskaart-ID, kanaal-ID en de ID van een ander activiteittype, zodat de klant die moet worden beloond, kan worden gevonden en de verdienregel voor de activiteit kan worden geïdentificeerd. 

    Toekenning van punten voor niet-transactieactiviteiten omvat in het algemeen twee belangrijke stappen:

    - Een plaatsgevonden activiteit identificeren die moet worden beloond.
    - De juiste punten toekennen.

    De eerste stap is extern voor Commerce, zoals twitteren over het merk of het merk leuk vinden op Facebook. Nadat deze activiteit is herkend, kunnen de detailhandelaren de bovengenoemde Commerce Scale Unit-API aanroepen en loyaliteitspunten in real-time toekennen. In dergelijke gevallen is een controlestap niet nodig omdat er een activiteit heeft plaatsgevonden en de bijbehorende punten moeten worden toegekend. Er zijn echter scenario's waarin de detailhandelaar de records wil controleren vóór de toekenning van de punten. De detailhandelaar heeft bijvoorbeeld een workshop in de winkel waarvoor de klanten zich aanmelden bij de website voor e-Commerce of een andere toepassing voor inschrijving bij gebeurtenissen. Alleen de aanwezige klanten echter verdienen loyaliteitspunten. Voor dergelijke scenario's hebben we in versie 10.0 een gegevensentiteit geïntroduceerd met de naam **Regels andere activiteittypen voor loyaliteit detailhandel**. Met deze gegevensentiteit kunnen de detailhandelaren Raamwerk voor gegevensimport/-export (DIXF) of OData-API gebruiken voor het vastleggen van de activiteiten waarvoor klanten met loyaliteitspunten worden beloond. Met de gegevensentiteit worden de activiteiten opgeslagen in een journaal met de naam **Loyaliteitsregels voor andere activiteiten**, die kan worden gebruikt voor controle- en wijzigingsdoeleinden. Nadat de gegevens zijn gecontroleerd, kan de IT-gebruiker de activiteitregels handmatig boeken of een taak uitvoeren met de naam **Ander activiteitstype voor loyaliteitsregels verwerken**. Hiermee worden alle niet-geboekte activiteitregels geboekt en worden de punten toegekend aan de klanten toegekend op basis van de verdienregels. In het bovenstaande geval roept de toepassing voor inschrijving bij gebeurtenissen OData-API aan om de klantgegevens naar Commerce te sturen. De IT-gebruiker kan de activiteitregels echter alleen voor die klanten boeken die de workshop hebben bijgewoond en de activiteitregels verwijderen voor de overige klanten. 

    > [!NOTE]
    > Momenteel moeten gebruikers een nummerreeks voor andere activiteitstypen instellen, maar dit is geen vereiste stap in toekomstige releases. Als u een nummerreeks wilt instellen, gaat u naar **Gedeelde Commerce-parameters** \> **Nummerreeksen** en selecteert u een nummerreeks voor **ID overige activiteittypen voor loyaliteit**.

- Voor een goede klantenservice en effectieve oplossing van klantvragen is het belangrijk dat de kassiers toegang hebben om het profiel van de klant in te vullen. Met release 10.0 kunnen kassiers details over de loyaliteitshistorie bekijken met het bijbehorende loyaliteitsprogramma en laaggegevens in POS.
- Gratis verzending of verzendkortingen is een van de zeer motiverende factoren voor klanten om online te kopen. Om detailhandelaren de mogelijkheid te bieden verzendpromoties in te stellen in release 10.0, gaan we een nieuw type promotie introduceren waarbij de detailhandelaar de drempels kan definiëren die, wanneer eraan wordt voldaan, klanten in aanmerking laten komen voor verzending met korting of gratis verzending. Bijvoorbeeld: besteed € 35 voor gratis twee dagen verzending of gratis twee dagen verzending voor alle loyaliteitsklanten. Deze functie maakt gebruik van de nieuwe mogelijkheid van geavanceerde automatische toeslagen. Raadpleeg de [documentatie over geavanceerde automatische toeslagen](/dynamics365/unified-operations/retail/omni-auto-charges). Deze geavanceerde automatische toeslagen moeten worden ingeschakeld zodat verzendpromoties werken. Deze kunnen worden ingeschakeld via het tabblad **Klantorders** op de pagina **Commerce-parameters** en door de configuratie 'Geavanceerde automatische toeslagen gebruiken' in te schakelen. Omdat een detailhandelaar meerdere typen toeslagen kan instellen, zoals afhandeling of installatie, moet deze bovendien opgeven welke kosten worden beschouwd als verzendkosten. De verzendkortingen worden alleen toegepast op de verzendkosten. Als u kosten als verzendkosten wilt opgeven, gaat u naar het formulier **Kostencodes** dat aanwezig is onder **Detailhandel en commerce** \> **IT detailhandel en commerce** \> **Kanaalinstellingen** \> **Toeslagen** en schakelt u het selectievakje Verzendkosten voor de gewenste toeslagen in. Nu kunt u navigeren naar het formulier **Verzenddrempelkorting** en kunt u de korting instellen.

    Net als bij productkortingen worden bij deze korting alle bestaande standaardkortingsmogelijkheden meegenomen. Zo mag de detailhandelaar deze kortingen beperken met de coupons zodat alleen klanten met coupons deze kortingen kunnen krijgen. Bij deze kortingen wordt ook gebruik gemaakt van de mogelijkheid Prijsgroepen om te bepalen of men in aanmerking komt voor deze kortingen. De detailhandelaar kan er bijvoorbeeld voor kiezen deze promoties alleen uit te voeren via de online kanalen en/of via kanalen voor bepaalde klantengroepen, zoals loyaliteitsklanten. Nadat de orderregels met de opgegeven leveringsmethode de gedefinieerde drempel hebben bereikt, wordt de verzendkorting toegepast en worden de verzendkosten op basis van de kortingsinstellingen verlaagd. 

    > [!NOTE]
    > In tegenstelling tot andere periodieke kortingen, zoals hoeveelheidskorting, eenvoudige korting, combinatiekorting en drempelkorting, worden met de verzendkorting geen kortingsregels gemaakt. Wijzigingen in de verzendkosten worden echter rechtstreeks aangebracht en de naam van de korting wordt toegevoegd aan de omschrijving van de kosten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
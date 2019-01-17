---
title: Overzicht van loyaliteit
description: Dit onderwerp beschrijft de loyaliteitsmogelijkheden in Microsoft Dynamics 365 for Retail en de bijbehorende instellingsstappen om de detailhandelaar te helpen eenvoudig aan de slag te gaan met hun loyaliteitsprogramma's.
author: scott-tucker
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 09d4e46694e89b648981352f64da4a43ab1522e1
ms.contentlocale: nl-nl
ms.lasthandoff: 01/04/2019

---

# <a name="loyalty-overview"></a>Overzicht van loyaliteit

[!include [banner](includes/banner.md)]

Loyaliteitsprogramma's kunnen helpen klantloyaliteit te verhogen door klanten te belonen voor hun interactie met het merk van de detailhandelaar. In Microsoft Dynamics 365 for Retail kunt u eenvoudige of complexe loyaliteitsprogramma's instellen die gelden voor verschillende rechtspersonen in een detailhandelskanaal. Dit onderwerp beschrijft de loyaliteitsmogelijkheden in Microsoft Dynamics 365 for Retail en de bijbehorende instellingsstappen om de detailhandelaar te helpen eenvoudig aan de slag te gaan met hun loyaliteitsprogramma's.

U kunt uw loyaliteitsprogramma zo instellen dat het de volgende opties bevat.

- Stel meerdere typen beloningen in die u in uw loyaliteitsprogramma's aanbiedt en houdt de participatie in uw loyaliteitsprogramma's bij.
- Stel loyaliteitsprogramma's in die de verschillende beloningsincentives weergeven die u aanbiedt. U kunt loyaliteitsprogrammarijen opnemen om grotere incentives en beloningen aan te bieden aan klanten die vaker winkelen of meer geld uitgeven in uw winkels.
- Definieer verdienregels om de activiteiten te identificeren die een klant moet voltooien om beloningen te verdienen. U kunt ook inruilregels instellen om aan te geven wanneer en hoe een klant beloningen kan inruilen.
- Geef loyaliteitskaarten uit vanaf elk detailhandelskanaal dat deelneemt aan uw loyaliteitsprogramma's, en koppel loyaliteitskaarten aan een of meer loyaliteitsprogramma's waaraan de klant kan deelnemen. U kunt ook een klantrecord koppelen aan een loyaliteitskaart om de klant loyaliteitspunten van meerdere kaarten samen te laten voegen en deze in te ruilen.
- Pas handmatig loyaliteitskaarten aan of boek het saldo van loyaliteitsbeloningen van een kaart naar een andere over om een klant bij te werken of te belonen.

## <a name="setting-up-loyalty-programs"></a>Loyaliteitsprogramma's instellen

U moet verschillende onderdelen instellen om de loyaliteitsfunctie in Dynamics 365 for Retail in te schakelen. Het volgende schema geeft de loyaliteitscomponenten aan en hoe ze met elkaar zijn verbonden.

![Processtroom voor loyaliteitsinstelling](./media/loyaltyprocess.gif "Loyaliteitsonderdelen en hoe deze aan elkaar zijn gerelateerd")

## <a name="loyalty-components"></a>Loyaliteitscomponenten

De volgende tabel beschrijft elke component en waar deze in de loyaliteitsinstellingen wordt gebruikt.

| component                                        | Omschrijving | Waar deze wordt gebruikt |
|--------------------------------------------------|-------------|-----------------|
| Kortingen instellen (vereiste)                  | Stel de kortingen in die u aan uw loyaliteitsklanten aanbiedt. Bijvoorbeeld, u kunt 5 procent korting op alle kledingproducten bieden. | Kortingen moeten aan prijsgroepen worden toegevoegd voordat ze in een loyaliteitsprogramma kunnen worden opgenomen. Prijsgroepen worden toegewezen aan loyaliteitsprogramma's en loyaliteitsrijen. |
| Prijsgroepen instellen (vereiste)               | Prijsgroepen worden gebruikt om prijzen en kortingen voor detailhandelproducten te maken en te beheren. Stel de prijsgroepen in die de kortingen bevatten die op uw loyaliteitsprogramma's van toepassing zijn. | Prijsgroepen worden toegewezen aan loyaliteitsprogramma's en loyaliteitsprogrammarijen. |
| Kanalen instellen (vereiste)                   | Detailhandelskanalen zijn de winkels die deelnemen aan uw loyaliteitsprogramma's, zoals een fysieke winkel, een online winkel of een callcenter. U moet uw detailhandelskanalen instellen voordat u er loyaliteitsprogramma's kunt aan toewijzen. | U wijst detailhandelskanalen toe aan een loyaliteitsprogramma als het detailhandelskanaal aan het loyaliteitsprogramma deelneemt. |
| De loyaliteitsbetalingsmethode instellen (vereiste) | Voordat een loyaliteitskaart kan worden gebruikt op een kassa en er loyaliteitspunten kunnen worden ingewisseld als onderdeel van een loyaliteitsprogramma, moet u een betalingsmethode instellen. U moet ook de loyaliteitsbetalingsmethode aan het detailhandelskanaal toevoegen voordat klanten hun loyaliteitspunten kunnen inruilen als betaling voor producten. | Stel een betalingsmethode in van het type loyaliteit, en wijs vervolgens de loyaliteitsbetalingsmethode toe aan de detailhandelskanalen die aan het loyaliteitsprogramma deelnemen. |
| Datumintervallen instellen                            | De datumintervallen bieden een flexibele manier om de periode in te stellen die op loyaliteitsrijen van toepassing is. Gebruik datumintervallen om op te geven hoe lang een klant in een rij kan blijven of hoe lang een klant een activiteit moet uitvoeren om voor een rij in aanmerking te komen. | Datumintervallen zijn alleen van toepassing als u rijen in uw loyaliteitsprogramma's gebruikt. U selecteert het datuminterval dat van toepassing is op programmarijen, en ook de datumintervallen die gelden voor programmarijregels. |
| Beloningspunten instellen                             | Beloningspunten zijn de types beloning die u uw klanten aanbiedt. Beloningenpunten kunnen inruilbaar of niet-inruilbaar zijn. Inruilbare beloningspunten kunnen worden ingeruild voor producten. Niet-inruilbare beloningspunten worden gebruikt om zaken bij te houden of om een klant in een andere rij in een loyaliteitsprogramma te plaatsen. | Er wordt verwezen naar beloningspunten in rijregels, en deze worden gebruikt om een klant aan een specifieke rij toe te wijzen. Er wordt ook naar de beloningspunten verwezen in loyaliteitsschema's voor verdien- en inruilregels. Bij verdienregels geeft u de beloningen op die een klant kan verdienen voor een specifieke activiteit. In inruilregels, geeft u de beloning op die de klant kan krijgen. |
| Loyaliteitsprogramma's instellen                          | Loyaliteitsprogramma's zijn belangrijkste loyaliteitsrechtpersoon die u aanbiedt. Aan elk loyaliteitsprogramma kunnen ook loyaliteitsrijen zijn toegewezen. Kortingen en de prijsgroepen worden toegewezen aan de loyaliteitsprogramma's op programmaniveau of op rijniveau. | U maakt loyaliteitsschema's voor uw loyaliteitsprogramma's. U wijst loyaliteitskaarten toe aan uw loyaliteitsprogramma's, en loyaliteitskaarten kunnen aan een klant worden toegewezen. Detailhandelskanalen nemen deel aan de loyaliteitsprogramma's die aan de loyaliteitsschema's worden toegewezen. Elke klant die een loyaliteitskaart heeft, kan deelnemen aan de loyaliteitsprogramma's die aan de kaart zijn toegewezen. |
| Loyaliteitsrijen en rijregels instellen              | Loyaliteitsrijen zijn optionele niveaus die u kunt definiëren voor uw loyaliteitsprogramma's. U kunt basiskortingen en beloningen instellen voor alle klanten die aan het loyaliteitsprogramma deelnemen, en u kunt extra kortingen en beloningen instellen voor klanten die de verschillende niveaus in het programma behalen. Voor elke loyaliteitsrij die u definieert, kunt u de regels instellen waarmee een klant in aanmerking komt voor die rij. U kunt ook bepalen hoe lang klanten in die rij kunnen blijven nadat ze de rij hebben bereikt. | Loyaliteitsrijen en loyaliteitsrijregels worden gedefinieerd in de loyaliteitsprogramma's. Als u geen loyaliteitsrijen definieert, komen alle klanten die aan het loyaliteitsprogramma deelnemen in aanmerking voor kortingen die u in de loyaliteitsprogrammaprijsgroep toewijst. Als u loyaliteitsrijen definieert, kunt u verdienregels en inruilregels instellen voor de loyaliteitsrijen in het loyaliteitsschema. |
| Loyaliteitsschema's instellen                           | Loyaliteitsschema's geven de verdienregels en inruilregels op die gelden voor een geselecteerd loyaliteitsprogramma. U wijst detailhandelskanalen toe aan een loyaliteitsschema om te identificeren welke loyaliteitsprogramma's, verdienregels en inruilregels gelden voor een detailhandel. | Een loyaliteitsschema wordt toegewezen aan een loyaliteitsprogramma en aan detailhandelskanalen. U kunt meerdere loyaliteitsschema's toewijzen aan hetzelfde loyaliteitsprogramma, en u kunt meerdere loyaliteitsschema's toewijzen aan veel detailhandelskanalen. |
| Loyaliteitskaarten instellen                             | Een loyaliteitskaart geeft de houder het recht om deel te nemen aan de loyaliteitsprogramma's die aan de kaart zijn toegewezen. Loyaliteitskaarten kunnen anoniem worden uitgegeven, of ze kunnen aan een specifieke klant worden toegewezen. U kunt de loyaliteitstransacties voor een specifieke kaart weergeven, en u kunt een overzicht weergeven van loyaliteitspunten die op de kaart zijn samengevoegd. U kunt loyaliteitskaarten uitgeven vanuit elk detailhandelkanaal. U kunt een loyaliteitskaart ook handmatig aanpassen om de klant in een andere rij te plaatsen, loyaliteitspunten toe te voegen, of het loyaliteitspuntensaldo van de ene kaart overboeken naar de andere over te zetten. | U wijst loyaliteitsprogramma's toe aan een loyaliteitskaart. |

## <a name="loyalty-processes"></a>Loyaliteitsprocessen

De volgende tabel beschrijft de processen die moeten worden uitgevoerd om de loyaliteitsconfiguraties en gegevens naar uw winkels te verzenden, en om de loyaliteitstransacties van uw winkels op te halen.

| Procesnaam                         | Beschrijving | Paginanaam |
|--------------------------------------|-------------|-----------|
| 1050 (loyaliteitsinformatie)           | Voer dit proces uit om de loyaliteitsgegevens van Dynamics 365 for Retail naar de winkels te verzenden. Het is een goed idee dit proces te plannen om vaak te worden uitgevoerd, zodat de loyaliteitsgegevens naar alle winkels worden verzonden. | Distributieplanning |
| Loyaliteitsschema verwerken              | Voer dit proces uit om loyaliteitsschema's te koppelen aan de detailhandelskanalen waaraan het loyaliteitsschema is toegewezen. Dit proces kan worden gepland om als een batchproces te worden uitgevoerd. U moet dit proces uitvoeren als u de gegevens van de loyaliteitsconfiguratie wijzigt, zoals loyaliteitsschema's, loyaliteitsprogramma's, of de punten van de loyaliteitsbeloning. | Loyaliteitsschema verwerken |
| Offline loyaliteitstransacties verwerken | Voer dit proces uit om loyaliteitskaarten bij te werken zodat ze transacties bevatten die offline werden verwerkt. Dit proces is alleen van toepassing als het selectievakje **Offline verdienen** is ingeschakeld op de pagina **Gedeelde parameters detailhandel**, zodat de beloningen offline kunnen worden verdiend. | Offline loyaliteitstransacties verwerken |
| Niveaus van loyaliteitskaarten bijwerken            | Voer dit proces uit om de verdienende activiteit van de klant te beoordelen volgens de rijregels voor een loyaliteitsprogramma en om de rijstatus van de klant bij te werken. Dit proces is alleen nodig als u de rijregels in loyaliteitsprogramma's wijzigt en u wilt dat de bijgewerkte regels retroactief worden toegepast op loyaliteitskaarten die reeds zijn uitgegeven. Dit proces kan worden uitgevoerd als een batchproces of voor afzonderlijke kaarten. | Niveaus van loyaliteitskaarten bijwerken |

## <a name="loyalty-enhancements"></a>Verbeteringen in loyaliteit

Detailhandel bevat nieuwe loyaliteitsfunctionaliteit als onderdeel van de release van oktober 2018. Elk van de nieuwe verbeteringen wordt hieronder nader verklaard.

- Als onderdeel van een loyaliteitsschema in vorige releases konden detailhandelaren verschillende verdien- en inwisselregels op niveaus maken om de beloningen te differentiëren voor klanten op verschillende niveaus. Detailhandelaren kunnen nu 'lidmaatschappen' opnemen als onderdeel van de verdien- en inwisselregels, zodat bepaalde groepen klanten deel van bestaande niveaus kunnen uitmaken, maar toch verschillend kunnen worden beloond. Dit zorgt ervoor dat er geen aanvullende niveaus hoeven te worden gemaakt.
    
    > [!NOTE]
    > De verdienregels binnen een loyaliteitsschema zijn extra. Als u bijvoorbeeld een regel maakt om een gouden lid te belonen met 10 punten voor elke Amerikaanse dollar en u ook een regel maakt voor een klant met het lidmaatschap 'veteraan' om 5 punten beloning te geven voor elke Amerikaanse dollar, dan verdient een veteraan die ook een gouden lid is, 15 punten voor 1 Amerikaanse dollar, omdat de klant voor beide in aanmerking komt. Als de veteraan echter geen lid van het gouden niveau was, zou hij 5 punten voor elke dollar verdienen. Voer in verband met de wijzigingen in de kanalen de taken **Loyaliteitsschema verwerken** en **1050** (loyaliteitsinformatie)-uit.
    
    ![Verdienen op basis van lidmaatschappen](./media/Affiliation%20based%20earning.png "Verdienen op basis van lidmaatschappen")

- Detailhandelaren hebben vaak speciale prijzen voor een bepaalde groep klanten waar ze niet het loyaliteitsprogramma op willen toepassen. Bijvoorbeeld groothandelaren of werknemers die speciale prijzen krijgen en geen loyaliteitspunten. Vaak worden 'lidmaatschappen' gebruikt om dergelijke klantengroepen de speciale prijzen te bieden. Als de detailhandelaar wil verhinderen dat bepaalde klantengroepen loyaliteitspunten verdienen, kan deze een of meer lidmaatschappen opgeven in de sectie **Uitgesloten lidmaatschappen** van het loyaliteitsschema. Wanneer klanten die tot uitgesloten lidmaatschappen behoren, bestaande loyaliteitsleden zijn, kunnen ze geen loyaliteitspunten verdienen met hun aankopen. Voer in verband met de wijzigingen in de kanalen de taken **Loyaliteitsschema verwerken** en **1050** (loyaliteitsinformatie)-uit.

    ![Uitgesloten lidmaatschappen](./media/Excluded%20affiliations.png "Lidmaatschappen uitsluiten van loyaliteitspunten")
    
- Detailhandelaren kunnen loyaliteitskaartnummers genereren in de kanalen. Vóór de update van oktober 2018 konden detailhandelaren fysieke loyaliteitskaarten gebruiken of een loyaliteitskaart genereren met unieke klantgegevens, zoals een telefoonnummer. Als u het automatisch genereren van loyaliteitskaarten in de winkels wilt inschakelen, schakelt u **Loyaliteitskaartnummer genereren** in het functionaliteitsprofiel in dat is gekoppeld aan de winkel. Voor online kanalen kunnen detailhandelaren de API IssueLoyaltyCard gebruiken om loyaliteitskaarten aan klanten uit te geven. Detailhandelaren kunnen een loyaliteitskaartnummer verstrekken aan deze API, dat wordt gebruikt voor het genereren van de loyaliteitskaart, of het systeem gebruikt de sequentie van loyaliteitskaartnummers die is ingesteld in Dynamics 365 for Retail. Echter, als de getalreeks niet aanwezig is en de detailhandelaar geen loyaliteitskaartnummer verstrekt bij de aanroep van de API, wordt een foutbericht weergegeven.

    ![Loyaliteitskaart genereren](./media/Generate%20loyalty%20card.png "Automatisch loyaliteitskaartnummer genereren")

- Verdiende en ingewisselde loyaliteitspunten worden nu opgeslagen voor elke transactie en verkooporders ten opzichte van de verkoopregel, zodat hetzelfde bedrag kan worden terugbetaald of teruggekregen in het geval van volledige of gedeeltelijke retourneringen. Bovendien biedt zichtbaarheid van punten op het niveau van de verkoopregel de mogelijkheid voor callcentergebruikers om vragen van klanten te beantwoorden over hoeveel punten zijn verdiend of ingewisseld voor elke regel. Vóór deze wijziging werden beloningspunten altijd opnieuw berekend tijdens retourneringen, wat leidde tot een ander bedrag dan het origineel, als de verdien- of inwisselregels zijn gewijzigd en hadden callcentergebruikers geen inzicht in de specificatie van de punten. Het aantal punten kan worden weergegeven op het formulier **Kaarttransacties** voor elke loyaliteitskaart.    
- Detailhandelaren kunnen nu de vestigingsperiode voor elk beloningspunt definiëren. Een configuratie van de vestigingsperiode definieert de duur vanaf de verdiendatum, waarna de beloningspunten beschikbaar worden voor de klanten. Niet-gevestigde punten kunnen worden weergegeven in de kolom **Niet-gevestigde punten** op de pagina **Loyaliteitskaarten**. Bovendien kunnen detailhandelaren de maximale limiet aan beloningspunten per loyaliteitskaart definiëren. Dit veld kan worden gebruikt om het effect van loyaliteitsfraude te verminderen. Wanneer de maximale toegekende punten zijn bereikt, kan de gebruiker geen punten meer verdienen. De detailhandelaar kan besluiten deze kaarten te blokkeren totdat ze op mogelijke fraude zijn onderzocht. Als de detailhandelaar fraude vaststelt, kan de detailhandelaar niet alleen de loyaliteitskaart blokkeren voor de klant, maar ook de klant markeren als geblokkeerd. Hiervoor stelt u de eigenschap **Klant blokkeren voor loyaliteitsinschrijving** op **Ja** in onder **Alle klanten** op het sneltabblad **Detailhandel**. Aan de geblokkeerde klanten kan in geen van de kanalen een loyaliteitskaart worden uitgegeven.

    ![Vestiging en maximale beloningspunten](./media/Vesting%20and%20maximum%20reward%20points.png "Vestiging en maximale beloningspunten definiëren")

- Lidmaatschappen worden gebruikt om speciale prijzen en kortingen te bieden, maar er zijn enkele lidmaatschappen waarvan detailhandelaren niet willen dat hun klanten ze zien. Een lidmaatschap met de titel 'Veel uitgevende klant' wordt mogelijk niet goed ontvangen door sommige klanten. Bovendien zijn er lidmaatschappen die niet in de winkel moeten worden beheerd, bijvoorbeeld werknemers, omdat u niet wilt dat kassiers bepalen wie een werknemer is en dus werknemerskortingen bieden. Detailhandelaren kunnen nu de lidmaatschappen selecteren die in de detailhandelkanalen moeten worden verborgen. Lidmaatschappen die zijn gemarkeerd als **In kanalen verbergen**, kunnen worden bekeken, toegevoegd of verwijderd in het POS. Echter, de prijzen en kortingen die zijn gekoppeld aan het lidmaatschap, worden nog steeds toegepast op de producten.

    ![Lidmaatschappen verbergen](./media/Hide%20affiliations.png "Lidmaatschappen verbergen in kanalen")
    
- Callcentergebruikers kunnen nu gemakkelijker een klant zoeken met behulp van hun loyaliteitskaartgegevens en naar de loyaliteitskaart van de klant en de pagina's met loyaliteitskaarttransacties navigeren vanaf de pagina **Klantenservice**.

    ![Klantenservice](./media/Customer%20service.png "Loyaliteitsinformatie voor de klant zoeken")
    
- Als met een loyaliteitskaart geknoeid is, moet een vervangende kaart worden gegenereerd en moeten de bestaande punten worden overgedragen aan de nieuwe kaart. De stroom voor de vervangende kaart is in deze release vereenvoudigd. Bovendien kunnen klanten sommige of al hun loyaliteitspunten schenken aan vrienden en familie. Wanneer punten worden overgeboekt, worden de puntcorrectieposten gemaakt voor elke loyaliteitskaart. De functionaliteit voor de vervangende kaart en de saldo-overdracht is toegankelijk vanaf de pagina **Loyaliteitskaarten**.

    ![Vervangen en punten overdragen](./media/Replace%20and%20transfer%20points.png "Loyaliteitskaart vervangen of saldo overdragen")
    
- Detailhandelaren willen mogelijk de effectiviteit van een bepaald kanaal vastleggen om klanten in een loyaliteitsprogramma op te nemen. De bron van inschrijving voor de loyaliteitskaart wordt nu opgeslagen, zodat detailhandelaren rapporten op deze gegevens kunnen uitvoeren. De bron van inschrijvingen wordt automatisch vastgelegd voor alle uitgegeven loyaliteitskaarten vanuit MPOS/CPOS of e-commercekanalen. Voor de loyaliteitskaarten die worden uitgegeven vanuit de back office-toepassing, kan de callcentergebruiker een geschikt kanaal selecteren.
- In eerdere versies konden detailhandelaren MPOS/CPOS gebruiken om loyaliteitspunten in te wisselen voor klanten in een winkel. Aangezien het loyaliteitssaldo in deze release echter in loyaliteitspunten wordt weergegeven, kon de kassamedewerker het valutawaardebedrag niet zien dat kon worden toegepast op de huidige transactie. De kassamedewerker moest de conversie van punten naar valuta uitvoeren alvorens te betalen met loyaliteitspunten. In de huidige release, nadat regels zijn toegevoegd aan de transactie, kan de kassamedewerker het bedrag zien dat de loyaliteitspunten kunnen dekken voor de huidige transactie, zodat het gemakkelijker is sommige of alle loyaliteitspunten op de transactie toe te passen. Bovendien ziet de kassier de punten die binnen de komende 30 dagen verlopen, zodat deze upselling of cross-selling kan uitvoeren om de klant te motiveren de verlopende punten uit te geven voor die transactie.

    ![Punten die vallen onder loyaliteitssaldo](./media/Points%20covered%20by%20loyalty%20balance.png "Saldo weergeven dat wordt gedekt door loyaliteitspunten")

    ![Vervallende punten](./media/Expiring%20points.png "Vervallende punten weergeven")
    
## <a name="upcoming-enhancements"></a>Aankomende verbeteringen

De volgende functies zijn beschikbaar in de toekomstige maandelijkse updates van Dynamics 365 for Retail.
    
- Klanten willen hun loyaliteitsaldodetails kunnen zien in naar de consument gerichte kanalen. Daarnaast is het belangrijk voor de kassiers om de historie van de loyaliteitspunten van de klant te zien in MPOS/CPOS om snel vragen te beantwoorden van de klant. In een toekomstige maandelijkse release kunnen klanten en kassiers loyaliteitshistoriedetails weergeven.
- Veel detailhandelaren kunnen loyaliteitspunten alleen verlenen op basis van de verkooptransacties, maar meer klantgerichte detailhandelaren willen hun klanten belonen voor al hun betrokkenheid bij het merk. Ze willen bijvoorbeeld beloningen geven voor het invullen van een online enquête, bezoek aan een winkel, 'leuk vinden' van de detailhandelaar op Facebook, tweeten over de detailhandelaar en meer. In de toekomst voegen we de mogelijkheid toe loyaliteitspunten toe te kennen voor elke klantactiviteit. Hiertoe kan de detailhandelaar een 'Overig activiteittype' definiëren en de verdienregels voor deze activiteiten definiëren. We maken ook een Retail Server API beschikbaar die kan worden aangeroepen wanneer een activiteit wordt geïdentificeerd die de verdienregel gebruikt om de vereiste loyaliteitspunten toe te kennen.
- Om een ware multikanaals detailhandelservaring mogelijk te maken staan we klanten toe loyaliteitspunten te verdienen en in te wisselen via alle kanalen.
- Gratis verzending of verzendkortingen is een van de zeer motiverende factoren voor klanten om online te kopen. Om detailhandelaren de mogelijkheid te bieden verzendpromoties in te stellen gaan we een nieuw type promotie introduceren waarbij de detailhandelaar de drempels kan definiëren die, wanneer eraan wordt voldaan, klanten in aanmerking laten komen voor verzending met korting of gratis verzending.


---
title: "Eén boekstuk"
description: "Met één boekstuk voor financiële journalen (algemeen journaal, vaste-activajournaal, leveranciersbetalingsjournaal, enzovoort) kunt u meerdere subgrootboekransacties invoeren in de context van één boekstuk."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Eén boekstuk

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
>  Deze functionaliteit is beschikbaar in Dynamics 365 for Finance and Operations versie 8.0, die beschikbaar is in de release van voorjaar 2018.   

<a name="what-is-one-voucher"></a>Wat is 'Eén boekstuk'?
======================

Met de bestaande functionaliteit voor financiële journalen (algemeen journaal, vaste-activajournaal, leveranciersbetalingsjournaal, enzovoort) kunt u meerdere subadministratietransacties invoeren in de context van één boekstuk. We verwijzen naar deze functionaliteit als 'Eén boekstuk'. U kunt een van de volgende methoden gebruiken om Eén boekstuk te maken:

-   Stel de journaalnaam in (**Grootboek** \> **Journaal instellen** \> **Journaalnamen**) zodat het veld **Nieuw boekstuk** wordt ingesteld op **Maximaal één boekstuknummer**. * Elke regel die u aan het journaal toevoegt, wordt nu opgenomen op hetzelfde boekstuk. Omdat elke regel wordt toegevoegd aan hetzelfde boekstuk, kan het boekstuk worden ingevoerd als een boekstuk met meerdere regels, als een rekening/tegenrekening op dezelfde regel, of als een combinatie.

[![Eén regel](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Houd er rekening mee dat de definitie van 'Eén boekstuk' geen journaalnamen bevat die alleen zijn ingesteld als **Eén boekstuknummer** en waarvoor de gebruiker vervolgens een boekstuk invoert dat alleen soorten grootboekrekeningen bevat.  In dit document betekent 'Eén boekstuk' dat er één boekstuk is met meer dan een leverancier, klant, bank, vaste activa of project. 

-   Voer een boekstuk met meerdere regels in wanneer er geen tegenrekening is.

[![Boekstuk met meerdere regels](./media/Multi-line.png)](./media/Multi-line.png)

-   Voer een boekstuk in als zowel de rekening en de tegenrekening een subgrootboekrekeningtype bevatten, zoals leverancier/leverancier, klant/klant, leverancier/klant of bank/bank.

[![Boekstuk van subgrootboek](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Problemen met één boekstuk
=======================

De functionaliteit van één boekstuk veroorzaakt problemen bij de vereffening, belastingberekening, afstemming van subgrootboek naar grootboek, financiële rapportage en meer. (Meer informatie over problemen die bij de vereffening optreden, vindt u in [Eén boekstuk met meerdere klant- of leveranciersrecords](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Als u correct wilt werken en rapporteren, zijn voor deze processen en rapporten transactiedetails nodig. Hoewel sommige scenario's mogelijk nog goed werken, op basis van de instellingen van uw organisatie, zijn er vaak problemen als meerdere transacties in één boekstuk worden ingevoerd.

U boekt bijvoorbeeld het volgende boekstuk met meerdere regels.

[![Voorbeeld ](./media/example.png)](./media/example.png)

Vervolgens genereert u het rapport **Onkosten per leverancier** in het werkgebied **Financial Insights**. Het rapport groepeert onkostenrekeningsaldi onder leveranciersgroep en leverancier. Wanneer u het rapport genereert, kan het systeem niet bepalen voor welke groepen leveranciers of leveranciers de onkosten van EUR 250,00 zijn gemaakt. Omdat transactiedetails ontbreken, wordt ervan uitgegaan dat het hele bedrag van 250,00 is gemaakt door de eerste leverancier in het boekstuk. De 250,00 die zijn opgenomen in het saldo voor de hoofdrekening 600120, wordt weergegeven onder de desbetreffende leveranciersgroep/leverancier. Het is zeer waarschijnlijk dat de eerste leverancier in het boekstuk niet de juiste leverancier is, zodat het rapport onjuist is.

[![Onkosten](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>De toekomst van Eén boekstuk
=========================

Vanwege de hierboven vermelde problemen wordt de functionaliteit van Eén boekstuk niet verder ontwikkeld. Omdat deze functionaliteit echter in bepaalde gevallen wordt toegepast, zal de functie niet in één keer worden verwijderd. Dit gebeurt volgens het volgende schema: 

- **Release voorjaar 2018**: de functionaliteit wordt standaard uitgeschakeld in een grootboekparameter. U kunt de functie echter inschakelen als uw organisatie een scenario heeft dat werkt met de zakelijke scenario's die verderop in dit onderwerp worden vermeld.

  -   Als een klant een zakelijke scenario's heeft, waarvoor Eén boekstuk niet nodig is, schakelt u de functie niet in. Er worden geen 'fouten' opgelost voor de gebieden die verderop in dit onderwerp worden aangegeven, als deze functionaliteit wordt gebruikt terwijl een andere oplossing bestaat.

  -   Stop met het gebruiken van Eén boekstuk voor integratie in Microsoft Dynamics 365 Finance and Operations, tenzij de functionaliteit vereist is.

- **Releases najaar 2018 en later**: de functionaliteit wordt ingevuld. Nadat de functionaliteit is ingevuld, wordt Eén boekstuk permanent uitgeschakeld.

- > [!IMPORTANT]
  > Houd er rekening mee dat de optie **Maximaal één boekstuknummer** NIET is verwijderd uit de instellingen voor journaalnamen.  Deze optie wordt nog steeds ondersteund als het boekstuk alleen soorten grootboekrekeningen bevat.  Klanten moeten voorzichtig zijn met deze instelling omdat het boekstuk niet kan worden geboekt als ze **Maximaal één boekstuknummer** gebruiken en meer dan een klant, leverancier, bank, vaste activa of project invoeren.  Bovendien kunnen klanten toch een combinatie van subgrootboekrekeningtypen invoeren, zoals een betaling binnen één boekstuk die rekeningtypen bevat van leverancier/bank.  

<a name="why-use-one-voucher"></a>Waarom gebruikt u Eén boekstuk?
====================

Op basis van informatie van klanten hebben we de volgende lijst opgesteld met scenario's waarin klanten de functionaliteit Eén boekstuk gebruiken en met de redenen waarom zij hiervan gebruikmaken. Aan bepaalde bedrijfsvereisten kan alleen worden voldaan met Eén boekstuk. Voor veel scenario's bestaan echter alternatieven die voldoen aan deze bedrijfsvereisten.

<a name="scenarios-that-require-one-voucher"></a>Scenario's waarvoor Eén boekstuk is vereist
----------------------------------

De volgende scenario's kunnen alleen met de functionaliteit Eén boekstuk worden uitgevoerd. Deze functionaliteit wordt vanaf de release van najaar 2018 en latere versies ingevuld via andere functies.

-   **Betalingen van leverancier of klant als een overzicht naar een bankrekening boeken**

    -   Een organisatie geeft een lijst met leveranciers en bedragen door aan de bank en de bank gebruikt deze lijst om de leveranciers te betalen uit naam van de organisatie. De bank boekt het totaal van de betalingen als één enkele opname op de bankrekening.

>   Samenvatting van leverancierbetalingen wordt alleen ondersteund door Eén boekstuk. Elke leverancier wordt als een aparte regel met details ingevoerd in het leverancierssubgrootboek, maar het samengevatte bedrag voor alle betalingen wordt tegengeboekt op één regel voor de bankrekening. De opname wordt dus weergegeven als één samengevat bedrag in de subadministratie van de bank.

-   Een organisatie stort klantbetalingen of de bank stort klantbetalingen in opdracht van de organisatie en de storting wordt weergegeven als een totaalbedrag op de bankrekening.

>   Samenvatting van klantbetalingen wordt meestal via de depositofunctionaliteit ondersteund. Als u echter overbrugging gebruikt voor de betalingsmethode, wordt dit scenario alleen ondersteund door Eén boekstuk. Betalingen van klanten worden ingevoerd op dezelfde manier die wordt beschreven voor samenvatting van leverancierbetalingen.

-   **Mechanisme voor het groeperen van transacties voor een zakelijke gebeurtenis**

    -   Een organisatie heeft één zakelijke gebeurtenis waardoor meerdere transacties worden geactiveerd. De afdeling Boekhouding wil de boekhoudgegevens echter bij elkaar weergeven voor betere controleerbaarheid.

>   Als een organisatie de boekhoudregels van een zakelijke gebeurtenis samen moet weergeven, gebruikt u Eén boekstuk. 

- **Landafhankelijke functies**

  -   De functie Enig Document (ED) voor Polen vereist momenteel dat één boekstuk wordt gebruikt. Totdat een groeperingsoptie voor deze functie beschikbaar is, moet u doorgaan met het gebruik van de functionaliteit van één boekstuk. Er zijn mogelijk extra landspecifieke functies waarvoor de functionaliteit van één boekstuk nodig is.

- **Vooruitbetalingsjournaal van klant bevat belastingen op meerdere 'regels'**

  -   Een klant doet een vooruitbetaling voor een order en de regels van de order hebben verschillende belastingen die voor de vooruitbetaling moeten worden vastgelegd. De vooruitbetaalde klantbetaling is één transactie die overeenkomt met de regels van de order, zodat het correcte belastingpercentage kan worden vastgelegd voor het bedrag op elke regel.

In dit scenario zijn de klanten in het ene boekstuk dezelfde klant, omdat de transactie de regels van een klantorder simuleert. De vooruitbetaling moet worden ingevoerd in één boekstuk, omdat de btw-berekening moet worden uitgevoerd op de 'regels' van de betaling die de klant heeft gedaan.

-   **Onderhoud vaste activa: achterstallige afschrijving, splitsen van activa, afschrijving berekenen voor afstoting**

Met de volgende vaste-activatransacties worden ook meerdere transacties gemaakt in één boekstuk:
-   Er worden extra aanschafkosten voor een activum gemaakt en 'achterstallige' afschrijving wordt berekend.
-   Een activum wordt opgesplitst.
-   Een parameter voor het berekenen van afschrijving bij buitengebruikstelling is ingeschakeld en vervolgens het activum wordt afgestoten.

<a name="scenarios-that-dont-require-one-voucher"></a>Scenario's waarvoor Eén boekstuk niet is vereist
----------------------------------------

De volgende scenario's kunnen met behulp van andere middelen worden uitgevoerd. Hier hoeft geen gebruik te worden gemaakt van Eén boekstuk.

-   **Betalingen van klant als een overzicht naar de bankrekening boeken**

Een organisatie stort klantbetalingen of de bank stort klantbetalingen in opdracht van de organisatie en de storting wordt weergegeven als een totaalbedrag op de bankrekening.

Samenvatting van betalingen van klanten wordt ondersteund door de deposito-functionaliteit wanneer overbrugging niet als betalingsmethode wordt gebruikt.

-   **Verrekening**

Bij het vereffenen worden saldi voor een leverancier en klant ten opzichte van elkaar vereffend omdat de leverancier en klant dezelfde partij zijn. Hierdoor wordt zo min mogelijk geld uitgewisseld tussen een organisatie en de klant-/leverancierpartij.

Vereffening kan worden uitgevoerd door toename en afname in te voeren in afzonderlijke boekstukken en het verschil te boeken naar een speciale grootboekrekening.

-   **Overzicht naar het grootboek boeken**

Organisaties willen vaak een overzicht naar het grootboek boeken om de hoeveelheid gegevens te minimaliseren. De organisaties vereisen echter meestal wel dat de transactiedetails worden beheerd. Wanneer de boeking is voltooid door middel van één boekstuk, zijn de details van de transactie niet bekend en kunnen ze niet worden beheerd.

   -   Omdat de transactiedetails momenteel niet kunnen worden onderhouden, raden we aan om Eén boekstuk niet te gebruiken voor het boeken van de samenvatting.
   -   Als de ondersteuning voor Eén boekstuk is verwijderd, kunnen we raamwerken voor brondocument en boekhouding in de journalen implementeren. Deze raamwerken zorgen vervolgens voor het onderhouden van de transactiedetails en ondersteuning van de samenvatting in het grootboek.

-   **Meerdere niet-geboekte betalingen aan dezelfde factuur vereffenen**

Dit scenario komt meestal voor in detailhandelorganisaties waar klanten met meerdere betalingsmethoden voor hun aankopen kunnen betalen. In dit scenario moet de organisatie meerdere niet-geboekte betalingen kunnen vastleggen en deze ten opzichte van de factuur vereffenen.

Een nieuwe functie die is toegevoegd in Microsoft Dynamics 365 for Operations versie 1611 (november 2016) zorgt dat meerdere niet-geboekte betalingen worden vereffend met één factuur. U hoeft niet langer meerdere klantbetalingen in één boekstuk in te voeren.

-   **Bankafschrifttransacties importeren**

Banken verrichten en ontvangen vaak betalingen namens een organisatie en deze transacties worden geregistreerd in Finance and Operations in een bestand dat is ontvangen van de bank. Organisaties willen die transacties vaak groeperen met behulp van het bankafschriftnummer in het bestand. Omdat elke transactie in detail op het bankafschrift wordt weergegeven, is samenvatting niet vereist in het banksubgrootboek.

Transacties kunnen worden gegroepeerd met behulp van andere velden op het journaal, zoals het journaalpartijnummer zelf of het documentnummer.

-   **Saldi overboeken**

Een organisatie moet mogelijk een saldo van de ene leverancier overboeken naar een andere leverancier, ofwel vanwege een fout of omdat een andere leverancier de aansprakelijkheid heeft overgenomen. Overdrachten van dit type worden ook uitgevoerd voor rekeningtypen zoals klanten en bankrekeningen.

Overboekingen van de ene rekening (leverancier, klant, bankrekening, enzovoort) naar een andere rekening kunnen worden uitgevoerd via afzonderlijke boekstukken en het verschil kan worden geboekt naar een speciale grootboekrekening.

-   **Beginsaldi invoeren**

Organisaties voeren vaak beginsaldi in voor rekeningen in het subgrootboek (leveranciers, klanten, vaste activa, enzovoort) als één boekstuktransactie. Beginsaldi voor elke rekening in het subgrootboek kunnen worden ingevoerd als afzonderlijke boekstukken en het verschil kan worden geboekt naar een speciale grootboekrekening.

-   **De journaalregel van een geboekt klant- of leverancierdocument corrigeren**

Een organisatie moet mogelijk de grootboekrekening van Klanten of Leveranciers corrigeren voor een journaalregel van een geboekte factuur, maar deze factuur kan niet worden gestorneerd of gecorrigeerd door een ander mechanisme.

Als een correctie moet worden uitgevoerd in de grootboekrekening voor klanten of leveranciers, moet de correctie rechtstreeks worden toegepast op de grootboekrekening. De correctie kan niet worden uitgevoerd door boeken via de leverancier of klant. Deze benadering vereist dat de correctie wordt uitgevoerd als het systeem niet wordt gebruikt, zodat tijdelijk handmatig invoer mogelijk is voor de grootboekrekening.

-   **Het systeem laat het toe**

Organisaties gebruiken de functionaliteit van één boekstuk vaak alleen maar omdat het systeem het toelaat, zonder dat de gevolgen duidelijk zijn.


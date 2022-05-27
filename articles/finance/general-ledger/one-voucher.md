---
title: Eén boekstuk
description: Met één boekstuk voor financiële journalen (algemeen journaal, vaste-activajournaal, leveranciersbetalingsjournaal, enzovoort) kunt u meerdere subgrootboekransacties invoeren in de context van één boekstuk.
author: kweekley
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 9a0a9a3f23a3aec0077fd1a64c55fea567b72800
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722487"
---
# <a name="one-voucher"></a>Eén boekstuk

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


## <a name="what-is-one-voucher"></a>Wat is Eén boekstuk?

Met de bestaande functionaliteit voor financiële journalen (algemeen journaal, vaste-activajournaal, leveranciersbetalingsjournaal, enzovoort) kunt u meerdere subadministratietransacties (klant, leverancier, vaste activa, project en bank) invoeren in de context van één boekstuk. Microsoft verwijst naar deze functionaliteit als *Eén boekstuk*. U kunt een van de volgende methoden gebruiken om één boekstuk te maken:

- Stel de journaalnaam in (**Grootboek** \> **Journaal instellen** \> **Journaalnamen**) zodat het veld **Nieuw boekstuk** wordt ingesteld op **Maximaal één boekstuknummer**. Elke regel die u aan het journaal toevoegt, wordt nu opgenomen in hetzelfde boekstuk. Omdat elke regel wordt toegevoegd aan hetzelfde boekstuk, kan het boekstuk dus worden ingevoerd als een boekstuk met meerdere regels, als een rekening/tegenrekening op dezelfde regel of als een combinatie.

    [![Eén regel.](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > De definitie van Eén boekstuk omvat **geen** gevallen waarin journaalnamen zijn ingesteld als **Maximaal één boekstuknummer**, maar waarvoor de gebruiker vervolgens een boekstuk invoert dat alleen soorten grootboekrekeningen bevat. In dit onderwerp betekent Eén boekstuk dat er één boekstuk is met meer dan één leverancier, klant, bank, vaste activa of project.

- Voer een boekstuk met meerdere regels in wanneer er geen tegenrekening is.

    [![Boekstuk met meerdere regels.](./media/Multi-line.png)](./media/Multi-line.png)

- Voer een boekstuk in waarbij zowel de rekening als de tegenrekening een subgrootboekrekeningtype bevatten, zoals **Leverancier**/**Leverancier**, **Klant**/**Klant**, **Leverancier**/**Klant** of **Bank**/**Bank**.

    [![Boekstuk van subgrootboek.](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Problemen met één boekstuk

De functionaliteit van één boekstuk veroorzaakt problemen bij de vereffening, belastingberekening, transactieterugboeking, afstemming van subgrootboek naar grootboek, financiële rapportage en meer. (Meer informatie over problemen die bij de vereffening optreden, vindt u bijvoorbeeld in [Eén boekstuk met meerdere klant- of leveranciersrecords](../accounts-payable/single-voucher-multiple-customer-vendor-records.md).) Als u correct wilt werken en rapporteren, zijn voor deze processen en rapporten transactiedetails nodig. Hoewel sommige scenario's mogelijk nog goed werken, afhankelijk van de instellingen van uw organisatie, zijn er vaak problemen als meerdere transacties in één boekstuk worden ingevoerd.

U boekt bijvoorbeeld het volgende boekstuk met meerdere regels.

[![Voorbeeld van een boekstuk met meerdere regels.](./media/example.png)](./media/example.png)

Vervolgens genereert u het rapport **Onkosten per leverancier** in het werkgebied **Financial Insights**. Dit rapport groepeert onkostenrekeningsaldi onder leveranciersgroep en vervolgens leverancier. Wanneer het rapport wordt genereerd, kan het systeem niet bepalen voor welke groepen leveranciers of leveranciers de onkosten van EUR 250,00 zijn gemaakt. Omdat transactiedetails ontbreken, wordt ervan uitgegaan dat de hele kosten van 250,00 zijn gemaakt door de eerste leverancier die is gevonden in het boekstuk. De kosten van 250,00 die zijn opgenomen in het saldo voor de hoofdrekening 600120, worden daarom weergegeven onder de desbetreffende leveranciersgroep/leverancier. Het is echter zeer waarschijnlijk dat de eerste leverancier in het boekstuk niet de juiste leverancier is. Het rapport is daarom waarschijnlijk onjuist.

[![Onkosten per leveranciersrapport.](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>De toekomst van Eén boekstuk

Vanwege de problemen die kunnen optreden bij het gebruik van één boekstuk, wordt deze functionaliteit uiteindelijk afgeschaft. Omdat er echter functionele hiaten zijn die afhankelijk zijn van deze functionaliteit, zal de functie niet in één keer worden verwijderd. Dit gebeurt volgens het volgende schema:

- **Release van voorjaar 2018**: deze functionaliteit werd standaard uitgeschakeld via de parameter **Meerdere transacties binnen één boekstuk toestaan** op het tabblad **Algemeen** van de **Grootboekparameters**. U kunt de functie echter weer inschakelen als uw organisatie een scenario heeft dat valt in een van de functionele hiaten die verderop in dit onderwerp worden vermeld.

    - Als één boekstuk niet is vereist in uw bedrijfsscenario, raden we u aan de functionaliteit uit te schakelen. Als u de functionaliteit gebruikt terwijl er een andere oplossing beschikbaar is, lost Microsoft geen fouten op in de gebieden die verderop in dit onderwerp worden aangegeven.
    - We raden u aan te stoppen met het gebruik van één boekstuk voor integraties, tenzij de functionaliteit nodig hebt voor een van de gedocumenteerde functionele hiaten.

- **Nieuwere versies**: aan meerdere bedrijfsvereisten kan alleen worden voldaan met Eén boekstuk. Microsoft moet ervoor zorgen dat er nog aan alle geïdentificeerde bedrijfsvereisten in het systeem kan worden voldaan nadat de functionaliteit is afgeschaft. Daarom moeten er waarschijnlijk nieuwe functies worden toegevoegd om de functionele hiaten op te vullen. Microsoft kan geen specifieke oplossing leveren, omdat elke hiaat in de functionaliteit anders is en op basis van de behoeften van de zakelijke vereisten moet worden geëvalueerd. Sommige functionele hiaten worden waarschijnlijk vervangen door functies die helpen om aan specifieke bedrijfsvereisten te voldoen. Andere hiaten worden mogelijk opgevuld door invoer in een journaal te blijven toestaan, op een manier zoals bij het gebruik van één boekstuk, maar waardoor het systeem zo nodig meer details kan bijhouden.

Nadat alle functionele hiaten zijn opgevuld, geeft Microsoft door dat de functie wordt afgeschaft. De functie wordt echter pas na minimaal één jaar na die communicatie afgeschaft. Hoewel Microsoft niet precies kan zeggen wanneer de functie Eén boekstuk wordt afgeschaft, zal dit waarschijnlijk nog ten minste twee jaar duren. Het Microsoft-beleid is om minimaal 12 maanden te wachten tussen de aankondiging van afgeschafte functionaliteit en de werkelijke afschaffing, zodat klanten en onafhankelijke softwareleveranciers (ISV's) tijd hebben om te reageren op de wijziging. Het kan zijn dat een organisatie bijvoorbeeld hun bedrijfsprocessen, entiteiten en integraties nog moeten bijwerken.

De afschaffing van één boekstuk is een aanzienlijke wijziging die op tal van manieren wordt doorgegeven. Als onderdeel van die communicatie zal Microsoft dit onderwerp bijwerken, een blogpost op het Microsoft Dynamics 365 Finance-blog plaatsen, het onderwerp 'Verwijderde of afgeschafte functies' bijwerken, de wijziging communiceren op de juiste Microsoft-conferenties enzovoort.

## <a name="why-use-one-voucher"></a>Waarom gebruikt u Eén boekstuk?

Op basis van informatie van klanten heeft Microsoft de volgende lijst opgesteld met scenario's waarin klanten de functionaliteit Eén boekstuk gebruiken en met de redenen waarom zij hiervan gebruikmaken. Aan bepaalde bedrijfsvereisten kan alleen worden voldaan met Eén boekstuk. Voor veel scenario's bestaan echter alternatieven die voldoen aan deze bedrijfsvereisten.

### <a name="scenarios-that-require-one-voucher"></a>Scenario's waarvoor Eén boekstuk is vereist

De volgende scenario's kunnen alleen met de functionaliteit Eén boekstuk worden uitgevoerd. Als uw organisatie een van deze scenario's heeft, moet u inschakelen dat meerdere transacties kunnen worden ingevoerd in een boekstuk door wijziging van de instelling van de parameter **Meerdere transacties binnen één boekstuk toestaan** op de pagina **Grootboekparameters**. Deze functionele hiaten worden door andere functies opgevuld in latere releases.

> [!NOTE]
> [Voor elk van de volgende scenario's moet het veld **Meerdere transacties binnen één boekstuk toestaan** zijn ingesteld op Ja op het sneltabblad **Algemeen** op de pagina **Grootboekparameters**.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Betalingen van leverancier of klant als een overzicht naar een bankrekening boeken

**Scenario** Een organisatie geeft een lijst met leveranciers en bedragen door aan de bank en de bank gebruikt deze lijst om de leveranciers te betalen uit naam van de organisatie. De bank boekt het totaal van de betalingen als één enkele opname op de bankrekening.

Samenvatting van leverancierbetalingen wordt alleen ondersteund door Eén boekstuk. Elke leverancier wordt ingevoerd als een aparte regel om details te onderhouden in de subadministratie Leveranciers. Het aggregatiebedrag voor alle betalingen wordt echter tegengeboekt op één regel voor de bankrekening. De opname wordt dus weergegeven als één samengevat bedrag in de subadministratie van de bank.

**Scenario** Een organisatie stort klantbetalingen of de bank stort klantbetalingen in opdracht van de organisatie en de storting wordt weergegeven als een totaalbedrag op de bankrekening.

Samenvatting van klantbetalingen wordt meestal via de depositofunctionaliteit ondersteund. Als u echter overbrugging gebruikt voor de betalingsmethode, wordt dit scenario alleen ondersteund door Eén boekstuk. Betalingen van klanten worden ingevoerd op dezelfde manier die wordt beschreven voor samenvatting van leverancierbetalingen.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Mechanisme voor het groeperen van transacties voor een zakelijke gebeurtenis

**Scenario** Een organisatie heeft één zakelijke gebeurtenis waardoor meerdere transacties worden geactiveerd. De afdeling Boekhouding wil de boekhoudgegevens echter bij elkaar weergeven voor betere controleerbaarheid.

Als een organisatie de boekhoudregels van een zakelijke gebeurtenis samen moet weergeven, gebruikt u Eén boekstuk. 

### <a name="country-specific-features"></a>Landafhankelijke functies

**Scenario** De functie Enig Document (ED) voor Polen vereist momenteel dat één boekstuk wordt gebruikt. Totdat een groeperingsoptie voor deze functie beschikbaar is, moet u doorgaan met het gebruik van de functionaliteit van één boekstuk. Er zijn mogelijk extra landspecifieke functies waarvoor de functionaliteit van één boekstuk nodig is.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Vooruitbetalingsjournaal van klant bevat belastingen op meerdere 'regels'

In dit scenario zijn de klanten in het ene boekstuk dezelfde klant, omdat de transactie de regels van een klantorder simuleert. De vooruitbetaling moet worden ingevoerd in één boekstuk, omdat de btw-berekening moet worden uitgevoerd op de 'regels' van de betaling die de klant heeft gedaan.

### <a name="customer-reimbursement"></a>Terugbetaling aan klant

**Scenario** Een klant doet een vooruitbetaling voor een order en de regels van de order hebben verschillende belastingen die voor de vooruitbetaling moeten worden vastgelegd. De vooruitbetaalde klantbetaling is één transactie die overeenkomt met de regels van de order, zodat het correcte belastingpercentage kan worden vastgelegd voor het bedrag op elke regel.

Als de periodieke taak Terugbetaling wordt uitgevoerd vanuit de module Klanten, wordt een transactie gemaakt om het saldo van een klant naar een leverancier te verplaatsen. In dit scenario moet Eén boekstuk worden gebruikt om de klant terug te betalen.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Onderhoud vaste activa: achterstallige afschrijving, splitsen van activa, afschrijving berekenen voor afstoting
In versie 10.0.21 en hoger worden transacties van vaste activa voor een inhaalafschrijving, voor het splitsen van een activum en voor het berekenen van de afschrijving voor de vervreemding van een activum gecreëerd met verschillende boekstuknummers.

### <a name="bills-of-exchange-and-promissory-notes"></a> Wissels en promessen
Wissels en promessen vereisen dat Eén boekstuk wordt gebruikt, omdat de transacties het klant- of leverancierssaldo van de ene Klanten/Leveranciers-grootboekrekening naar de andere verplaatsen, op basis van de status van de betaling.

## <a name="scenarios-that-dont-require-one-voucher"></a>Scenario's waarvoor Eén boekstuk niet is vereist

De volgende scenario's kunnen met behulp van andere middelen worden uitgevoerd. Hier hoeft geen gebruik te worden gemaakt van de Eén boekstuk-functionaliteit.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Betalingen van klant als een overzicht naar de bankrekening boeken

Een organisatie stort klantbetalingen of de bank stort klantbetalingen in opdracht van de organisatie en de storting wordt weergegeven als een totaalbedrag op de bankrekening.

Samenvatting van betalingen van klanten wordt ondersteund door de deposito-functionaliteit wanneer overbrugging niet als betalingsmethode wordt gebruikt.

### <a name="netting"></a>Verrekening

Bij het vereffenen worden saldi voor een leverancier en klant ten opzichte van elkaar vereffend omdat de leverancier en klant dezelfde partij zijn. Hierdoor wordt zo min mogelijk geld uitgewisseld tussen een organisatie en de klant-/leverancierpartij.

Vereffening kan worden uitgevoerd door toename en afname in te voeren in afzonderlijke boekstukken en vervolgens het verschil te boeken naar een speciale grootboekrekening.

### <a name="post-in-summary-to-the-general-ledger"></a>Overzicht naar het grootboek boeken

Organisaties willen vaak een overzicht naar het grootboek boeken om de hoeveelheid gegevens te minimaliseren. Deze organisaties vereisen echter meestal wel dat de transactiedetails worden beheerd. Wanneer de boeking is voltooid door middel van één boekstuk, zijn de details van de transactie niet bekend en kunnen ze niet worden beheerd.

- Omdat de transactiedetails momenteel niet kunnen worden onderhouden, raden we organisaties aan om Eén boekstuk **niet** te gebruiken voor het boeken van de samenvatting.
- Als de ondersteuning voor Eén boekstuk is verwijderd, kunnen raamwerken voor brondocument en boekhouding in de journalen worden geïmplementeerd. Deze raamwerken zorgen vervolgens voor het onderhouden van de transactiedetails en ondersteuning van de samenvatting in het grootboek.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Meerdere niet-geboekte betalingen aan dezelfde factuur vereffenen

Dit scenario komt meestal voor in organisaties waar klanten met meerdere betalingsmethoden voor hun aankopen kunnen betalen. In dit scenario moet de organisatie meerdere niet-geboekte betalingen kunnen vastleggen en deze ten opzichte van de factuur vereffenen.

Een nieuwe functie die is toegevoegd in Microsoft Dynamics 365 for Operations versie 1611 (november 2016) zorgt dat meerdere niet-geboekte betalingen worden vereffend met één factuur. U hoeft niet langer meerdere klantbetalingen in één boekstuk in te voeren.

### <a name="import-bank-statement-transactions"></a>Bankafschrifttransacties importeren

Banken verrichten en ontvangen vaak betalingen namens een organisatie en deze transacties worden geregistreerd in Finance in een bestand dat is ontvangen van de bank. Organisaties willen die transacties vaak groeperen met behulp van het bankafschriftnummer in het bestand. Omdat elke transactie in detail op het bankafschrift wordt weergegeven, is samenvatting niet vereist in het banksubgrootboek.

Transacties kunnen worden gegroepeerd met behulp van andere velden op het journaal, zoals het journaalpartijnummer zelf of het documentnummer.


### <a name="transfer-balances"></a>Saldi overboeken

Een organisatie moet mogelijk een saldo van de ene leverancier overboeken naar een andere leverancier, ofwel vanwege een fout of omdat een andere leverancier de aansprakelijkheid heeft overgenomen. Overdrachten van dit type worden ook uitgevoerd voor rekeningtypen zoals **Klant** en **Bank**.

Overboekingen van de ene rekening (leverancier, klant, bank, enzovoort) naar een andere rekening kunnen worden uitgevoerd via afzonderlijke boekstukken en het verschil kan worden geboekt naar een speciale grootboekrekening.

### <a name="enter-beginning-balances"></a>Beginsaldi invoeren

Organisaties voeren vaak beginsaldi in voor rekeningen in het subgrootboek (leveranciers, klanten, vaste activa, enzovoort) als één boekstuktransactie. Beginsaldi voor elke rekening in het subgrootboek kunnen worden ingevoerd als afzonderlijke boekstukken en het verschil kan worden geboekt naar een speciale grootboekrekening.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>De journaalregel van een geboekt klant- of leverancierdocument corrigeren

Een organisatie moet mogelijk de grootboekrekening van Klanten of Leveranciers corrigeren voor een journaalregel van een geboekte factuur, maar deze factuur kan niet worden gestorneerd of gecorrigeerd door een ander mechanisme.

Als een correctie moet worden uitgevoerd in de grootboekrekening voor Klanten of Leveranciers, moet de correctie rechtstreeks worden toegepast op de grootboekrekening. De correctie kan niet worden uitgevoerd door boeken via de leverancier of klant. Deze benadering vereist dat de correctie wordt uitgevoerd als het systeem niet wordt gebruikt, zodat tijdelijk handmatig invoer mogelijk is voor de grootboekrekening.

### <a name="the-system-allows-it"></a>Het systeem laat het toe

Organisaties gebruiken de functionaliteit van één boekstuk vaak alleen maar omdat het systeem het toelaat, zonder dat de gevolgen duidelijk zijn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

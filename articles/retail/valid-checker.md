<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="nl-NL">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Consistentiecontrole voor detailhandeltransacties</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit onderwerp wordt de functie voor de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 for Retail beschreven.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Consistentiecontrole voor detailhandeltransacties</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit onderwerp wordt de nieuwe functie voor de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 for Finance and Operations versie 8.1.3 beschreven.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">In de consistentiecontrole worden inconsistente transacties geïdentificeerd en geïsoleerd voordat ze worden verzameld door het boekingsproces voor overzichten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Wanneer een overzicht wordt geboekt in Microsoft Dynamics 365 for Retail, kan de boeking mislukken vanwege inconsistente gegevens in de tabellen met detailhandeltransacties.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Het gegevensprobleem kan worden veroorzaakt door onvoorziene problemen in de verkooppunttoepassing (POS) of door incorrect geïmporteerde transacties uit POS-systemen van derden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Enkele voorbeelden van hoe deze inconsistenties kunnen worden weergegeven:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het transactietotaal in de kopteksttabel komt niet overeen met het transactietotaal op de regels.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het aantal regels in de kopteksttabel komt niet overeen met het aantal regels in de transactietabel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De btw in de kopteksttabel komen niet overeen met het btw-bedrag op de regels.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer er inconsistente transacties worden verzameld door het boekingsproces voor overzichten, worden er inconsistente verkoopfacturen en betalingsjournalen gemaakt en mislukt het gehele boekingsproces voor overzichten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dergelijke overzichten kunnen alleen nog worden hersteld door middel van gecompliceerde gegevenscorrecties via meerdere transactietabellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Met de consistentiecontrole voor detailhandeltransacties kunnen dit soort problemen worden voorkomen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het volgende diagram biedt inzicht in het boekingsproces met de consistentiecontrole voor detailhandeltransacties.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Boekingsproces voor overzichten met consistentiecontrole voor detailhandeltransacties<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Boekingsproces voor overzichten met consistentiecontrole voor detailhandeltransacties<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Met het batchproces <bpt id="p1">**</bpt>Winkeltransacties valideren<ept id="p1">**</ept> wordt de consistentie van de tabellen met detailhandeltransacties gecontroleerd voor de volgende scenario's.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Klantrekening<ept id="p1">**</ept>: hiermee wordt gevalideerd of de klantrekening in de tabellen met detailhandeltransacties bestaat in het HQ-klantmodel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Regeltelling<ept id="p1">**</ept>: hiermee wordt gevalideerd of het aantal regels, zoals vastgelegd in de transactiekopteksttabel, overeenkomt met het aantal regels in de verkooptransactietabellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Prijs inclusief belasting<ept id="p1">**</ept>: hiermee wordt gevalideerd of de parameter <bpt id="p2">**</bpt>Prijs inclusief belasting<ept id="p2">**</ept> consistent is binnen de transactieregels.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Brutobedrag<ept id="p1">**</ept>: hiermee wordt gevalideerd of het brutobedrag in de kop het totaal is van de nettobedragen op de regels plus het bedrag van de belasting.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Nettobedrag<ept id="p1">**</ept>: hiermee wordt gevalideerd of het nettobedrag in de kop het totaal is van de nettobedragen op de regels.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Over-/onderbetaling<ept id="p1">**</ept>: hiermee wordt gevalideerd of het verschil tussen het brutobedrag in de kop en het betalingsbedrag niet hoger is dan het maximum voor de configuratie voor over-/onderbetaling.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kortingsbedrag<ept id="p1">**</ept>: hiermee wordt gevalideerd of het kortingsbedrag in de kortingstabellen en het kortingsbedrag in de tabellen met de detailhandelstransactieregels consistent zijn, of het kortingsbedrag in de kop het totaal is van de kortingsbedragen op de regels.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="56" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Regelkorting<ept id="p1">**</ept>: hiermee wordt gevalideerd dat de regelkorting op de transactieregel het totaal is van alle regels in de kortingstabel die overeenkomt met de transactieregel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="55" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Geschenkbonartikel<ept id="p1">**</ept>: Retail ondersteunt niet het retourneren van geschenkbonartikelen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="0" state="translated">Het saldo op een geschenkbon kan echter wel contant worden uitbetaald. Geschenkbonartikelen die worden verwerkt als een retourregel in plaats van een uitbetalingsregel mislukken voor het boekingsproces voor overzichten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="0" state="translated">Het validatieproces voor geschenkbonartikelen zorgt dat de enige retourregels voor geschenkbonartikelen in de detailhandelstransactietabellen uitbetalingsregels voor de geschenkbon zijn.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Negatieve prijs<ept id="p1">**</ept>: hiermee wordt gevalideerd of er geen transactieregels met een negatieve prijs zijn.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Artikel en variant<ept id="p1">**</ept>: hiermee wordt gevalideerd of artikelen en varianten op de transactieregels bestaan in het stambestand met artikelen en varianten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">De consistentiecontrole instellen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Configureer het batchproces Winkeltransacties valideren via <bpt id="p1">**</bpt>Detailhandel <ph id="ph1">\&gt;</ph> IT detailhandel <ph id="ph2">\&gt;</ph> POS-boekingen<ept id="p1">**</ept> voor periodieke uitvoering.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De batchverwerking kan worden gepland op basis van de organisatiehiërarchie van de winkel, op dezelfde wijze als de processen Overzichten in batch berekenen en Overzichten in batch boeken zijn ingesteld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">We raden u aan dit batchproces zo te configureren dat het meerdere keren per dag wordt uitgevoerd en zo te plannen dat het na elke P-taak wordt uitgevoerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Resultaten van validatieproces</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De resultaten van de validatie door het batchproces worden toegevoegd aan de betreffende detailhandeltransactie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het veld <bpt id="p1">**</bpt>Validatiestatus<ept id="p1">**</ept> in de record van de detailhandeltransactie wordt ingesteld op <bpt id="p2">**</bpt>Geslaagd<ept id="p2">**</ept> of <bpt id="p3">**</bpt>Fout<ept id="p3">**</ept> en de datum van de laatste validatie wordt weergegeven in het veld <bpt id="p4">**</bpt>Laatste validatietijd<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u meer beschrijvende fouttekst voor een validatiefout wilt weergeven, selecteert u de betreffende transactierecord voor de detailhandelwinkel en klikt u op de knop <bpt id="p1">**</bpt>Validatiefouten<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Transacties die de validatie niet doorstaan en transacties die nog niet zijn gevalideerd, worden niet in overzichten opgenomen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tijdens het proces Overzicht berekenen wordt voor gebruikers een melding weergegeven als er transacties zijn die door een validatiefout niet in het overzicht zijn opgenomen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als een validatiefout wordt gevonden, kunt u de fout alleen herstelen door contact op te nemen met Microsoft Support.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In een toekomstige versie wordt het voor gebruikers mogelijk om de betreffende records te herstellen via de gebruikersinterface.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daarnaast worden functies voor logboekregistratie en controle toegevoegd, zodat de geschiedenis van de wijzigingen kan worden bijgehouden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In een toekomstige versie worden extra validatieregels toegevoegd om meer scenario's te ondersteunen.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
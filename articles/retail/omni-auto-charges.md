<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="nl-NL">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Geavanceerde automatische toeslagen voor meerdere kanalen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit onderwerp beschrijft de mogelijkheden voor het beheren van extra toeslagen voor detailhandelskanaalorders met behulp van de geavanceerde functie voor automatische toeslagen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Geavanceerde automatische toeslagen voor meerdere kanalen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit onderwerp bevat informatie over de configuratie en implementatie van de geavanceerde functie voor automatische-toeslagen die beschikbaar is in Dynamics 365 for Retail versie 10.0.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer de geavanceerde functie voor automatische toeslagen is ingeschakeld, kunnen orders die zijn gemaakt in een ondersteund detailhandelsafzetkanaal (verkooppunt (POS), callcenter en online), profiteren van de <bpt id="p1">[</bpt>automatische toeslagen<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept>-configuraties gedefinieerd in de ERP-toepassing voor zowel toeslagen op koptekst als op regelniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In releases vóór Dynamics 365 for Retail versie 10.0 zijn <bpt id="p1">[</bpt>automatische toeslag<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept>-configuraties alleen toegankelijk voor orders die zijn gemaakt in e-commerce- callcenterkanalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In versie 10.0 of hoger, kunnen POS-orders gebruikmaken van de automatische-toeslagenconfiguraties.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op die manier kunnen extra diverse toeslagen systematisch worden toegevoegd aan de verkooptransacties.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bij gebruik van versies ouder dan versie 10.0 wordt een POS-gebruiker gevraagd handmatig verzendkosten in te voeren tijdens het maken van een 'alles verzenden' of 'geselecteerd verzenden' POS-transactie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Terwijl de mogelijkheden van de diverse toeslagen van de toepassing worden gebruikt met betrekking tot de manier waarop de toeslagen op de order worden geschreven, wordt er geen systematische berekening geboden; de berekening is afhankelijk van de invoer van de gebruiker om de hoogte van de toeslagen te bepalen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De toeslagen kunnen alleen worden toegevoegd als een enkele 'verzending'-gerelateerde toeslagencode en kunnen niet eenvoudig worden bewerkt of gewijzigd in het POS nadat ze zijn gemaakt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het gebruik van handmatige prompts om verzendkosten toe te voegen is nog steeds beschikbaar in versies 10.0 en hoger.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als een organisatie de <bpt id="p1">**</bpt>Geavanceerde automatische toeslagen<ept id="p1">**</ept>-parameter niet inschakelt, blijven de POS-prompts voor handmatige invoer van toeslagen hetzelfde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Met de geavanceerde functie voor automatische toeslagen beschikken POS-gebruikers over systematische berekeningen voor alle gedefinieerde diverse toeslagen op basis van de instellingentabellen voor automatische toeslagen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daarnaast hebben gebruikers de mogelijkheid een onbeperkt aantal extra toeslagen en kosten aan een POS-verkooptransactie toe te voegen of te bewerken op kop- of regelniveau (voor contante transacties of een klantorder).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Geavanceerde automatische toeslagen inschakelen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Op de pagina <bpt id="p1">**</bpt>Detailhandel <ph id="ph1">\&gt;</ph> Instellingen hoofdkwartier <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Parameters detailhandel<ept id="p1">**</ept> gaat u naar het tabblad <bpt id="p2">**</bpt>Klantorders<ept id="p2">**</ept>. Op het sneltabblad <bpt id="p3">**</bpt>Toeslagen<ept id="p3">**</ept> stelt u <bpt id="p4">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p4">**</ept> in op <bpt id="p5">**</bpt>Ja<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Parameter geavanceerde automatische toeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer geavanceerde automatische toeslagen zijn ingeschakeld, wordt gebruikers niet meer gevraagd handmatig verzendkosten in te voeren in de POS-terminal bij het maken van een klantorder met alles verzenden of geselecteerd verzenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toeslagen op de POS-order worden automatisch berekend en toegevoegd aan de POS-transactie (als een bijbehorende automatische-toeslagen-tabel die overeenkomt met het criterium van de order die wordt gemaakt, wordt gevonden).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruikers kunnen ook toeslagen op kop- of regelniveau handmatig toevoegen of onderhouden via de toegevoegde POS-bewerkingen die kunnen worden toegevoegd aan de POS-schermindelingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer geavanceerde automatische toeslagen zijn ingeschakeld, worden de bestaande <bpt id="p1">**</bpt>Parameters detailhandel<ept id="p1">**</ept> voor <bpt id="p2">**</bpt>Verzendkostencode<ept id="p2">**</ept> en <bpt id="p3">**</bpt>Verzendkosten terugbetalen<ept id="p3">**</ept> niet meer gebruikt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze parameters zijn alleen van toepassing als de <bpt id="p1">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p1">**</ept>-parameter is ingesteld op <bpt id="p2">**</bpt>Nee<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zorg ervoor dat voordat u deze functie inschakelt uw medewerkers zijn opgeleid en getest, want het bedrijfsproces voor het berekenen van verzend- of andere kosten en deze toevoegen aan de POS-verkooporder zal hiermee wijzigen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zorg ervoor dat u weet wat de impact is van de processtroom op het maken van transacties vanuit het POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor callcenter- en e-Commerce-orders is de impact van het inschakelen van geavanceerde automatische toeslagen minimaal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Callcenter- en e-Commerce-toepassingen gedragen zich als voorheen ten aanzien van de tabellen voor automatische toeslagen voor het berekenen van extra toeslagen of kosten voor een order.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruikers van het callcenterkanaal behouden de mogelijkheid om door het systeem berekende automatische toeslagen handmatig te verwerken op kop- of regelniveau of extra diverse toeslagen handmatig toe te voegen op kop- of regelniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aanvullende POS-bewerkingen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Om geavanceerde automatische toeslagen goed te laten werken in uw POS-omgeving, zijn nieuwe POS-bewerkingen toegevoegd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze bewerkingen moeten worden toegevoegd aan uw <bpt id="p1">[</bpt>POS-schermindelingen<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> en gedistribueerd naar de POS-apparaten als u geavanceerde automatische toeslagen implementeert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als deze bewerkingen niet worden toegevoegd, is het voor gebruikers niet mogelijk diverse toeslagen op de POS-transacties te beheren of onderhouden en kunnen ze op geen enkele wijze de toeslagwaarden die systematisch worden berekend op basis van automatische-toeslagen-configuraties aanpassen of wijzigen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ten minste wordt voorgesteld dat u de bewerking <bpt id="p1">**</bpt>Toeslagen beheren<ept id="p1">**</ept> in uw POS-indeling installeert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">De nieuwe bewerkingen zijn als volgt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>142 - toeslagen beheren<ept id="p1">**</ept>: u kunt deze bewerking gebruiken om POS-gebruikers de mogelijkheid te geven om diverse toeslagen voor de POS-transactie die handmatig of systematisch via berekeningen van automatische toeslagen zijn toegevoegd, weer te geven en te bewerken.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>141 - toeslagen koptekst toevoegen<ept id="p1">**</ept>: gebruik deze bewerking om de gebruiker de mogelijkheid te geven om handmatig diverse toeslagen op koptekstniveau toe te voegen aan een POS-verkooptransactie (en de toeslagencode die moet worden gebruikt te selecteren).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>140 - regeltoeslagen toevoegen<ept id="p1">**</ept>: gebruik deze bewerking om de gebruiker de mogelijkheid te geven om handmatig diverse toeslagen op regelniveau toe te voegen aan een POS-verkooptransactieregel (en de toeslagencode te selecteren die moet worden gebruikt).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>143 - toeslagen herberekenen<ept id="p1">**</ept>: gebruik deze bewerking om een volledige nieuwe berekening van de toeslagen voor de verkooptransactie uit te voeren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eventuele eerdere door de gebruiker overschreven automatische toeslagen worden herberekend op basis van de huidige configuratie in de winkelwagen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zoals bij alle POS-bewerkingen kunnen beveiligingsconfiguraties worden gemaakt zodat goedkeuring van een manager is vereist om de bewerking te kunnen uitvoeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het is belangrijk te weten dat de hierboven vermelde POS-bewerkingen ook kunnen worden toegevoegd aan de POS-indeling, zelfs als de parameter <bpt id="p1">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p1">**</ept> is uitgeschakeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit scenario krijgen organisaties nog steeds extra voordelen omdat ze handmatig toegevoegde toeslagen kunnen bekijken en bewerken met behulp van de bewerking <bpt id="p1">**</bpt>Toeslagen beheren<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruikers kunnen ook de bewerkingen <bpt id="p1">**</bpt>Toeslagen koptekst toevoegen<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Regeltoeslagen toevoegen<ept id="p2">**</ept> voor POS-transacties gebruiken, zelfs wanneer de parameter <bpt id="p3">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p3">**</ept> is uitgeschakeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De bewerking <bpt id="p1">**</bpt>Toeslagen herberekenen<ept id="p1">**</ept> heeft minder functionaliteit als deze wordt gebruikt als <bpt id="p2">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p2">**</ept> is uitgeschakeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit scenario wordt niets herberekend en worden alle handmatig aan de transactie toegevoegde toeslagen opnieuw ingesteld op $0,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeldzaken gebruiken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In deze sectie zie u voorbeelden van gebruik die u helpen de configuratie en het gebruik van automatische toeslagen en diverse toeslagen binnen de context van orders in het detailhandelskanaal te begrijpen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze voorbeelden illustreren de werking van de toepassing wanneer de parameter <bpt id="p1">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p1">**</ept> is ingeschakeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld automatische toeslagen kopteksttoeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeldscenario gebruiken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een retailer wil automatisch vrachtkosten in rekening brengen wanneer er transacties worden aangemaakt in een cdetailhandelskanaal die een verzending van producten naar de klant vereisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailhandelaar biedt 2 methoden van levering: grond en lucht.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als een klant voor grondlevering kiest en de orderwaarde kleiner is dan € 100, wil de detailhandelaar de klant een vrachttoeslag van € 10 in rekening brengen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de order hoger is dan € 100 en de klant kiest voor grondverzending, dan worden geen extra vrachtkosten in rekening gebracht.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de klant kiest voor luchtlevering voor alle orders dan gelden vrachtkosten van € 20, ongeacht hun totaalwaarde,</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instellingen en configuratie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit scenario vereist de configuratie van twee tabellen met automatische toeslagen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ga naar <bpt id="p1">**</bpt>Klanten <ph id="ph1">\&gt;</ph> Instelling van toeslagen <ph id="ph2">\&gt;</ph> Automatische toeslagen<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Configureer twee verschillende automatische toeslagen op koptekstniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Configureer er een voor de 'grondleveringsmethode' en een voor de 'luchtleveringsmethode'.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stel ze in dit scenario in als gebruiken voor 'Alle klanten'.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor de toeslagen van de grondlevering definieert u in het regelgedeelte van de pagina <bpt id="p1">**</bpt>Automatische toeslagen<ept id="p1">**</ept> een toeslag van € 10 die wordt toegepast voor orders tussen € ,01 en € 100.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maak een andere toeslagenregel om aan te geven dat voor bestellingen van meer dan € 100,01 geen toeslag geldt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld automatische toeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor de toeslagen van de luchtlevering definieert u in het regelgedeelte van het formuleer automatische toeslagen een toeslag van € 20 die wordt toegepast op alle orders (tussen € ,01 en € 9.999.999).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verzend de wijzigingen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak <bpt id="p1">**</bpt>1040 distributieplanning<ept id="p1">**</ept> uit te voeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkoopverwerking voor dit scenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nadat de bovenstaande configuratiestappen zijn voltooid en de wijzigingen zijn toegepast op de kanaaldatabase, zal elke klantbestelling of verkooptransactie gemaakt in het POS-, callcenter- of e-Commerce-kanaal dat de methoden grond- en luchtlevering heeft ingesteld op koptekstniveau deze toeslagen gebruiken en deze automatisch toepassen op de verkoop.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op dit moment zijn de kosten van toepassing op alle verkooptransacties gemaakt binnen de rechtspersoon die gebruikmaakt van deze leveringsmethoden, omdat er geen functionaliteit is om aan te geven dat een automatische-toeslag-configuratie alleen van toepassing is op een specifiek verkoopkanaal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor POS- en e-commerce-scenario's, omdat er geen duidelijke 'koptekst' voor deze orders is gedefinieerd, gelden toeslagen op koptekstniveau alleen als voor alle verkoopregels van de transactie dezelfde leveringsmethode is ingesteld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als er 'gemengde-leveringsmethoden' zijn voor de transacties die zijn gemaakt door het POS of in e-commerce, worden alleen automatische toeslagen op regelniveau beschouwd en toegepast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In callcenterscenario's heeft de gebruiker controle over de instelling van de leveringsmethode op de orderkoptekst, daarom worden toeslagen op koptekstniveau van op deze orders toegepast, ook als sommige van de verkoopregels zijn geconfigureerd voor het gebruik van een andere leveringsmethode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toeslagen op koptekstniveau voor callcenterorders altijd gebaseerd op de leveringsmethode die is gedefinieerd op het niveau van de koptekst van de verkooporder.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld automatische toeslagen regeltoeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeldscenario gebruiken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een leverancier wil een extra toeslag toevoegen voor installatiekosten wanneer de klant een bepaald model computer koopt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze computer vereist extra niet-optionele installatietaken die door de detailhandelaar voor de klant wordt uitgevoerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailhandelaar heeft klanten laten weten dat er extra kosten voor deze instelling zijn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De retailer geeft er de voorkeur aan om de toeslagen met betrekking tot deze vergoeding apart te beheren van de verkoopprijs van het product ten behoeve van de financiële verslaglegging.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Installatiekosten van € 19,99 zullen in rekening worden gebracht aan de klant wanneer deze specifieke computer wordt gekocht in een van de detailhandelskanalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instellingen en configuratie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit scenario vereist de configuratie van een tabel voor automatische toeslagen op regelniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ga naar <bpt id="p1">**</bpt>Klanten <ph id="ph1">\&gt;</ph> Instelling van toeslagen <ph id="ph2">\&gt;</ph> Automatische toeslagen<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stel in <bpt id="p1">**</bpt>Niveau<ept id="p1">**</ept> het vervolgkeuzemenu op <bpt id="p2">**</bpt>Regel<ept id="p2">**</ept> en maak een nieuwe record voor automatische toeslagen voor alle klanten en voor het specifieke product of de productgroep waarvoor de installatiekosten worden berekend.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld automatische toeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verzend de toeslagen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak <bpt id="p1">**</bpt>1040 distributieplanning<ept id="p1">**</ept> uit te voeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkoopverwerking voor dit scenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nadat de bovenstaande configuratiestappen zijn voltooid en de wijzigingen zijn toegepast op de kanaaldatabase, zal elke klantbestelling of verkooptransactie gemaakt in het POS-, callcenter- of e-Commerce-kanaal dat dit item op de order heeft staan een regeltoeslag oproepen die systematisch aan het ordertotaal wordt toegevoegd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op dit moment zijn de kosten van toepassing op elke verkoopregel die overeenkomt met de configuratie van de automatische toeslag op regelniveau binnen de rechtspersoon, omdat er geen functionaliteit is om een automatische toeslag op regelniveau te configuratie die alleen van toepassing is op een specifiek verkoopkanaal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld van handmatige koptoeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beschrijving voorbeeldscenario gebruiken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een detailhandelaar maakt een uitzondering op kenmerkende processen door speciale thuisbezorging aan te bieden aan klanten die producten in de winkel bestellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailhandelaar en de klant zijn overeengekomen dat de klant € 25 administratiekosten voor deze service zal betalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op de order moet deze toeslag worden toegevoegd aan de transactie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omdat de vergoeding een algemene vergoeding is en niet is gerelateerd aan een enkel product op de order, moet een koptoeslag worden gebruikt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instellingen en configuratie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zorg ervoor dat de toeslagencode die wordt gebruikt in dit scenario juist is geconfigureerd door naar <bpt id="p1">**</bpt>Klanten <ph id="ph1">\&gt;</ph> Instelling toeslagen <ph id="ph2">\&gt;</ph> Toeslagen<ept id="p1">**</ept> te gaan om een juiste toeslagencode voor dit scenario te definiëren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld toeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Als de toeslag moet worden beschouwd als 'verzendkosten' met het oog op verzendingsgerelateerde kortingen of promoties, stelt u <bpt id="p1">**</bpt>Verzendkosten<ept id="p1">**</ept> voor de toeslagencode in op <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als deze toeslag ook systematisch mag worden terugbetaald tijdens de verwerking van een retourtransactie in de POS-toepassing, stelt u <bpt id="p1">**</bpt>Terug te betalen<ept id="p1">**</ept> in op <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De markering <bpt id="p1">**</bpt>Terug te betalen<ept id="p1">**</ept> is alleen toe te passen wanneer de parameter <bpt id="p2">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p2">**</ept> is ingesteld op <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verzend de toeslagen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak <bpt id="p1">**</bpt>1040 distributieplanning<ept id="p1">**</ept> uit te voeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De bewerking <bpt id="p1">**</bpt>Koptoeslag toevoegen<ept id="p1">**</ept> moet worden geconfigureerd uw <bpt id="p2">[</bpt>POS-schermindeling<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> zodat een knop die toegankelijk is voor de gebruiker vanuit het POS deze bewerking kan uitvoeren (bewerking 141).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wijzigingen in de schermindeling moeten ook naar de detailhandel worden gedistribueerd via de functie voor distributieplanning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkoopverwerking van handmatige koptoeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor het uitvoeren van het scenario in de POS-toepassing, maakt de POS-gebruiker de verkooptransactie zoals gebruikelijk door de producten en eventuele andere configuraties toe te voegen aan de verkoop.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vóór het innen van de betaling moet de gebruiker de bewerking <bpt id="p1">**</bpt>Koptoeslag toevoegen<ept id="p1">**</ept> uitvoeren, de gebruiker wordt dan gevraagd om een toeslagencode te selecteren en het bedrag van de toeslag in te voeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nadat de gebruiker het proces heeft voltooid, wordt de toeslag toegevoegd aan de verkooporder als een toeslag op kopniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit proces kan worden toegepast in het callcenter met behulp van de bestaande <bpt id="p1">**</bpt>Toeslagen<ept id="p1">**</ept>-functie in het tabblad <bpt id="p2">**</bpt>Verkopen<ept id="p2">**</ept> op de werkbalk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op de pagina <bpt id="p1">**</bpt>Toeslagen onderhouden<ept id="p1">**</ept> kan de gebruiker kan een nieuwe toeslagregel toevoegen aan de orderkop.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld van handmatige regeltoeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeldscenario gebruiken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een klant heeft gevraagd om 2 van de 5 artikelen op de verkooporder als cadeau te verpakken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailhandelaar biedt deze optionele service voor een vergoeding van € 2,00 per artikel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op de order moeten deze kosten specifiek worden toegevoegd aan de artikelen die moeten worden ingepakt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instellingen en configuratie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zorg ervoor dat de toeslagencode die wordt gebruikt in dit scenario juist is geconfigureerd door naar <bpt id="p1">**</bpt>Klanten <ph id="ph1">\&gt;</ph> Instelling toeslagen <ph id="ph2">\&gt;</ph> Toeslagen<ept id="p1">**</ept> te gaan om een juiste toeslagencode voor dit scenario te definiëren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de toeslag moet worden beschouwd als 'verzendkosten' met het oog op verzendingsgerelateerde kortingen of promoties, zet u de <bpt id="p1">**</bpt>Verzendkosten<ept id="p1">**</ept> op de toeslagencode op <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de toeslag ook systematisch mag worden terugbetaald tijdens de verwerking van een retourtransactie in de POS-toepassing, stelt u <bpt id="p1">**</bpt>Terug te betalen<ept id="p1">**</ept> in op <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De markering <bpt id="p1">**</bpt>Terug te betalen<ept id="p1">**</ept> is alleen toe te passen wanneer de parameter <bpt id="p2">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p2">**</ept> is ingesteld op <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verzend de toeslagen naar de Retail Server/afzetkanaal DB, zodat het POS ze kan gebruiken door de taak <bpt id="p1">**</bpt>1040 distributieplanning<ept id="p1">**</ept> uit te voeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De bewerking <bpt id="p1">**</bpt>Regeltoeslag toevoegen<ept id="p1">**</ept> moet worden geconfigureerd uw <bpt id="p2">[</bpt>POS-schermindeling<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> zodat een knop die toegankelijk is voor de gebruiker vanuit het POS deze bewerking kan uitvoeren (bewerking 140).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wijzigingen in de schermindeling moeten ook naar de detailhandel worden gedistribueerd via de functie voor distributieplanning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkoopverwerking van de handmatige regeltoeslag</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor het uitvoeren van het scenario in de POS-toepassing, maakt de POS-gebruiker de verkooptransactie zoals gebruikelijk door de producten en eventuele andere configuraties toe te voegen aan de verkoop.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vóór het innen van de betaling, moet de gebruiker de specifieke regel selecteren waarop de toeslag van toepassing zal zijn in de weergegeven lijst met POS-artikelen en de bewerking <bpt id="p1">**</bpt>Regeltoeslag toevoegen<ept id="p1">**</ept> uitvoeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De gebruiker wordt gevraagd om een toeslagencode te selecteren en het bedrag van de toeslag in te voeren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nadat de gebruiker het proces heeft voltooid, wordt de toeslag gekoppeld aan de regel en toegevoegd aan de verkooporder als een toeslag op regelniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De gebruiker kan het proces herhalen om extra kosten toe te voegen aan andere artikelregels van de transactie indien nodig.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hetzelfde proces kan worden toegepast in het callcenter met de functie 'toeslagen onderhouden' gevonden onder de <bpt id="p1">**</bpt>Financiën<ept id="p1">**</ept> vervolgkeuzelijst in het gedeelte <bpt id="p2">**</bpt>Verkooporderregels<ept id="p2">**</ept> op de pagina <bpt id="p3">**</bpt>Verkooporder<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hiermee opent u de pagina <bpt id="p1">**</bpt>Toeslagen onderhouden<ept id="p1">**</ept> waarin de gebruiker een nieuwe toeslag voor een specifieke regel aan de transactie kan toevoegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Extra functies</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toeslagen op een POS-verkooptransactie bewerken</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De bewerking <bpt id="p1">**</bpt>Toeslagen beheren<ept id="p1">**</ept> (142) moet worden toegevoegd aan de <bpt id="p2">[</bpt>POS-schermindeling<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> zodat een gebruiker alle systeemberekende of handmatig gemaakte kop- of regeltoeslagen kan bekijken en bewerken of overschrijven.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de bewerking niet wordt toegevoegd, zullen gebruikers niet in staat zijn om het bedrag van de toeslagen op de POS-transactie aan te passen, noch zullen zij in staat zijn om de details van de toeslagen, zoals het type toeslagencode gekoppeld aan de toeslag te bekijken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op de pagina <bpt id="p1">**</bpt>Toeslagen beheren<ept id="p1">**</ept> op het POS kan de gebruiker de details van de toeslagen op kop- en regelniveau bekijken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De gebruiker kan de functie <bpt id="p1">**</bpt>Bewerken<ept id="p1">**</ept> die beschikbaar is op deze pagina gebruiken om het bedrag in een specifieke toeslagregel te wijzigen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer een toeslagregel handmatig is overschreven, wordt deze niet systematisch herberekend tenzij de gebruiker de bewerking <bpt id="p1">**</bpt>Toeslagen herberekenen<ept id="p1">**</ept> start.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de <bpt id="p1">**</bpt>Redencode voor overschrijven toeslag<ept id="p1">**</ept> is geconfigureerd op de instellingspagina <bpt id="p2">**</bpt>Parameters detailhandel<ept id="p2">**</ept> wordt de gebruiker gevraagd een redencode op te geven wanneer de toeslagen zijn gewijzigd in de POS-toepassing.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als er redencodes zijn vastgelegd voor overschreven toeslagen, is er ook een nieuw rapport beschikbaar om deze overschrijvingen te bekijken en te controleren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het rapport kunt u vinden in <bpt id="p1">**</bpt>Detailhandel <ph id="ph1">\&gt;</ph> Query's en rapporten <ph id="ph2">\&gt;</ph> Geschiedenis toeslag overschrijven<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toeslagen terugbetalen op een POS-retourtransactie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de parameter <bpt id="p1">**</bpt>Geavanceerde automatische toeslagen gebruiken<ept id="p1">**</ept> is ingesteld op <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>, is de bestaande retail-parameter voor <bpt id="p3">**</bpt>Verzendkosten terugbetalen<ept id="p3">**</ept> niet langer van toepassing.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Om aan te geven welke kosten systematisch moeten worden terugbetaald aan een klant bij het gebruik van geavanceerde automatische toeslagen, moe u ervoor zorgen dat de bijbehorende toeslagencode is geconfigureerd als <bpt id="p1">**</bpt>Terug te betalen<ept id="p1">**</ept> op de instellingspagina <bpt id="p2">**</bpt>Toeslagencode<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zorg ervoor dat de instellingen zijn gesynchroniseerd met de databases van uw detailhandelskanaal via de verwerking van de distributieplanning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toeslagen terugbetalen op een retourordertransactie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toeslagen worden niet systematisch terugbetaald in <bpt id="p1">**</bpt>Retourorders<ept id="p1">**</ept> gemaakt in de detailhandel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruikers moeten de optie <bpt id="p1">**</bpt>Toeslagen kopiëren<ept id="p1">**</ept> selecteren bij het maken van de <bpt id="p2">**</bpt>Retourorder<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als <bpt id="p1">**</bpt>Toeslagen kopiëren<ept id="p1">**</ept> niet is geselecteerd, worden de toeslagen uit de oorspronkelijke verkooptransactie niet automatisch terugbetaald.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als <bpt id="p1">**</bpt>Toeslagen kopiëren<ept id="p1">**</ept> is geselecteerd, dan worden alle toeslagen gekopieerd naar de retourorder en kan de gebruiker handmatig de toeslagen bewerken of verwijderen die ze niet willen terugbetalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het callcenter retourorderproces herkent momenteel niet de markering <bpt id="p1">**</bpt>Terug te betalen<ept id="p1">**</ept> in de <bpt id="p2">**</bpt>Toeslagencode<ept id="p2">**</ept>-instellingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Configureren van POS-ontvangstbewijzen om toeslagen weer te geven</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">De volgende elementen voor het ontvangstbewijs zijn toegevoegd aan de ontvangstregel- en voetteksten ter ondersteuning van de functionaliteit van geavanceerde automatische toeslagen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Regel verzendkosten<ept id="p1">**</ept>: dit element op regelniveau kan worden gebruikt om specifieke toeslagencodes die zijn toegepast op de verkoopregel samen te vatten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Alleen codes die zijn gemarkeerd als <bpt id="p1">**</bpt>Verzend<ept id="p1">**</ept>-kosten op de pagina <bpt id="p2">**</bpt>Toeslagencode<ept id="p2">**</ept> worden weergegeven.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Regel andere toeslagen<ept id="p1">**</ept>: dit element op regelniveau kan worden gebruikt om niet-verzendingsspecifieke toeslagencodes samen te vatten die zijn toegepast op de verkoopregel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Dit zijn toeslagencodes waarvoor de markering <bpt id="p1">**</bpt>Verzending<ept id="p1">**</ept> op de pagina <bpt id="p2">**</bpt>Toeslagencode<ept id="p2">**</ept> niet is ingeschakeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Details verzendkosten order<ept id="p1">**</ept>: dit element op voettekstniveau bevat de omschrijvingen van de toeslagencodes toegepast op de order die zijn gemarkeerd als <bpt id="p2">**</bpt>Verzendkosten<ept id="p2">**</ept> op de instellingspagina <bpt id="p3">**</bpt>Toeslagencode<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Verzendkosten order<ept id="p1">**</ept>: dit element op voettekstniveau toont de eurowaarde van de toeslagen voor verzending.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Details overige toeslagen<ept id="p1">**</ept>: dit element op voettekstniveau bevat de omschrijving van de toeslagencodes toegepast op de order die niet zijn gemarkeerd als Verzendkosten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Overige toeslagen order<ept id="p1">**</ept>: dit element op voettekstniveau toont de eurowaarde van de overige toeslagen die niet gerelateerd zijn aan de verzending.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het is raadzaam dat de organisatie ook vrije-tekstvelden toevoegt aan de voettekst van het ontvangstbewijs, om de gebieden te kunnen definiëren waar toeslagen worden samengevat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorkomen dat toeslagen worden berekend voordat de POS-order is voltooid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sommige organisaties kunnen er de voorkeur aan geven om te wachten totdat de gebruiker alle verkoopregels aan de POS-transactie heeft toegevoegd vóór de toeslagen worden berekend.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Om te voorkomen dat de berekening van toeslagen wordt gemaakt wanneer artikelen worden toegevoegd aan de POS-transactie stelt u de parameter <bpt id="p1">**</bpt>Toeslag handmatig berekenen<ept id="p1">**</ept> in in het <bpt id="p2">**</bpt>Functieprofiel<ept id="p2">**</ept> van de winkel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u deze parameter inschakelt, dient de POS-gebruiker de bewerking <bpt id="p1">**</bpt>Totalen berekenen<ept id="p1">**</ept> te gebruiken wanneer die gereed is met het toevoegen van producten aan de POS-transactie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De bewerking <bpt id="p1">**</bpt>Totalen berekenen<ept id="p1">**</ept> activeert vervolgens de berekening van eventuele automatische toeslagen voor de orderkop of -regels indien van toepassing.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rapporten voor overschrijven van toeslagen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als gebruikers de berekende toeslagen handmatig overschrijven of een handmatige toeslag aan de transactie toevoegen, zijn deze gegevens beschikbaar voor controle in het rapport <bpt id="p1">**</bpt>Geschiedenis toeslag overschrijven<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het rapport kan worden geopend via <bpt id="p1">**</bpt>Detailhandel <ph id="ph1">\&gt;</ph> Query's en rapporten <ph id="ph2">\&gt;</ph> Geschiedenis toeslag overschrijven<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het is belangrijk te weten dat de gegevens die nodig zijn voor dit rapport, vanuit de afzetkanaaldatabase in HQ worden geïmporteerd via de 'P'-distributieplanningstaken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daarom is het mogelijk dat informatie over overschrijvingen die zojuist zijn uitgevoerd in het POS, pas direct beschikbaar zijn in dit rapport als met deze taak de transactiegegevens van de winkel naar HQ zijn geüpload.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>
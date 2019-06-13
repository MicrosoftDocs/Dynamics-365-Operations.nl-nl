<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="nl-NL">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="56" state="translated" state-qualifier="fuzzy-match">Kostenconfiguratie voor Gedistribueerd orderbeheer (DOM)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">In dit onderwerp wordt de kostenconfiguratie voor Gedistribueerd orderbeheer (DOM) in Microsoft Dynamics 365 for Retail beschreven.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="56" state="translated" state-qualifier="leveraged-inherited">Kostenconfiguratie voor Gedistribueerd orderbeheer (DOM)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="0" state="translated">Organisaties houden rekening met meerdere kostencomponenten om de optimale locatie te bepalen voor het afhandelen van een order.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="0" state="translated">Deze kostencomponenten kunnen bestaan uit verzendkosten, afhandelingskosten en verpakkingskosten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="0" state="translated">Er wordt een berekening gemaakt van de combinatie van deze kosten om de afhandelingslocatie te bepalen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="0" state="translated">Toen de toewijzing van orders aan afhandelingslocatie voor het eerst met Gedistribueerd orderbeheer (DOM) werd geoptimaliseerd in Microsoft Dynamics 365 for Retail, werd alleen rekening gehouden met de afstand.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="0" state="translated">Hoewel afstand kan samenhangen met kosten, is het niet hetzelfde als kosten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="0" state="translated">Het verzenden van producten in één dag is bijvoorbeeld duurder dan verzendmethoden over dezelfde afstand die drie of zeven dagen in beslag nemen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="0" state="translated">Met de functie voor kostenconfiguratie kunnen detailhandelaren aanvullende kostencomponenten definiëren en configureren die worden berekend en meegenomen bij het bepalen van de optimale locatie voor het afhandelen van orderregels.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="52" state="translated" state-qualifier="fuzzy-match">Wanneer kostencomponenten worden geconfigureerd, maakt de DOM-oplossingsfunctie alleen gebruik van deze kostendefinities om de optimale locatie te bepalen voor het afhandelen van een order.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="0" state="translated">De afstandcomponent wordt niet als een kostenpost beschouwd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Als er echter geen kostencomponenten worden geconfigureerd, maakt de DOM-oplossingsfunctie wel gebruik van de afstandscomponent als kostenpost om de optimale locatie te bepalen voor het afhandelen van een order.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kostencomponenten instellen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">Er kunnen twee belangrijke kostencomponenttypen worden gedefinieerd in het systeem: <bpt id="p1">**</bpt>Verzending<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Overig<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="0" state="translated">Maar beide kostencomponenttypen ondersteunen meerdere berekeningsbases, zoals wordt getoond in de volgende tabel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Kostencomponenttype</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Berekeningsbasis</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Verzenden</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Eenvoudig</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Gelaagd</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Overig</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Verkooporder</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Verkoopregel</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Locatie</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kostencomponenttype voor verzending</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="0" state="translated">In deze sectie wordt uitgelegd hoe u de verschillende combinaties van het kostencomponenttype <bpt id="p1">**</bpt>Verzending<ept id="p1">**</ept> en de berekeningsbasis voor de verzendkosten kunt instellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="0" state="translated">Ook wordt uitgelegd hoe de DOM-oplossingsfunctie deze combinaties toepast.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="0" state="translated">Kostencomponenttype = Verzending en Berekeningsbasis = Eenvoudig</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="51" state="translated" state-qualifier="fuzzy-match">Als een combinatie van het kostencomponenttype <bpt id="p1">**</bpt>Verzending<ept id="p1">**</ept> en de berekeningsbasis <bpt id="p2">**</bpt>Eenvoudig<ept id="p2">**</ept> wordt gebruikt, zijn de verzendkosten voor een leveringsmethode gebaseerd op een vast tarief of afstand.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="62" state="translated" state-qualifier="fuzzy-match">U moet de volgende velden instellen voor deze combinatie:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="60" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kostenfactor<ept id="p1">**</ept>: voer een unieke id voor de kostenfactor in.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Beschrijving<ept id="p1">**</ept>: voer de naam en de omschrijving van de kostenfactor in.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="52" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Begindatum<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Einddatum<ept id="p2">**</ept>: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="0" state="translated">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="59" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Actief<ept id="p1">**</ept>: geef aan of de kostenfactor actief is.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="52" state="translated" state-qualifier="fuzzy-match">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Bedrijf<ept id="p1">**</ept>: geef de rechtspersoon op waarvoor de kostenfactor wordt geconfigureerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="0" state="translated">Alle regels van de berekeningscriteria moeten gelden voor dezelfde rechtspersoon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="59" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Leveringsmethoden<ept id="p1">**</ept>: geef de leveringsmethoden op waarvoor de kostenfactor wordt geconfigureerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Berekeningstype<ept id="p1">**</ept>: geef op hoe de kosten moeten worden berekend voor een specifieke leveringsmethode.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="62" state="translated" state-qualifier="fuzzy-match">Er worden twee berekeningstypen ondersteund:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="62" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Vast<ept id="p1">**</ept>: er wordt een standaardtarief gebruikt voor de leveringsmethode.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="0" state="translated">Als u dit berekeningstype selecteert, wordt het standaardtarief gedefinieerd in het veld <bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Per afstandseenheid<ept id="p1">**</ept>: de kosten voor de leveringsmethode worden berekend als de waarde die is opgegeven in het veld <bpt id="p2">**</bpt>Kosten<ept id="p2">**</ept> maal de afstand tussen het afleveradres en de locaties.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: geef de waarde op die wordt gebruikt in combinatie met het veld <bpt id="p2">**</bpt>Berekeningstype<ept id="p2">**</ept> om de kosten voor de leveringsmethode te berekenen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Kostencomponenttype = Verzending en Berekeningsbasis = Gelaagd</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">Als een combinatie van het kostencomponenttype <bpt id="p1">**</bpt>Verzending<ept id="p1">**</ept> en de berekeningsbasis <bpt id="p2">**</bpt>Gelaagd<ept id="p2">**</ept> wordt gebruikt, zijn de verzendkosten voor een leveringsmethode gebaseerd op een vast tarief of afstand.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="0" state="translated">In deze combinatie is de afstand echter gebaseerd op een gelaagd bereik met afstanden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">U moet de volgende velden instellen voor deze combinatie:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="60" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfactor<ept id="p1">**</ept>: voer een unieke id voor de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="77" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschrijving<ept id="p1">**</ept>: voer de naam en de omschrijving van de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="61" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Standaardkosten<ept id="p1">**</ept>: geef de kosten op voor een leveringsmethode als de afstand tussen het afleveradres en de locatie niet binnen een van de gelaagde afstanden voor de leveringsmethode vast.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Begindatum<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Einddatum<ept id="p2">**</ept>: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Actief<ept id="p1">**</ept>: geef aan of de kostenfactor actief is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Bedrijf<ept id="p1">**</ept>: geef de rechtspersoon op waarvoor de kostenfactor wordt geconfigureerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Alle regels van de berekeningscriteria moeten gelden voor dezelfde rechtspersoon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Leveringsmethoden<ept id="p1">**</ept>: geef de leveringsmethoden op waarvoor de kostenfactor wordt geconfigureerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Afstandstype<ept id="p1">**</ept>: geef op of de gelaagde afstandsdefinitie een afstand hemelsbreed is of over de weg.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="53" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Afstandseenheden<ept id="p1">**</ept>: geef de eenheid op waarin de gelaagde afstand wordt gemeten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="56" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Afstand van<ept id="p1">**</ept>: geef het beginbereik van de gelaagde afstand op.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Afstand tot<ept id="p1">**</ept>: geef het eindbereik van de gelaagde afstand op.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Berekeningstype<ept id="p1">**</ept>: geef op hoe de kosten moeten worden berekend voor een specifieke leveringsmethode en de gelaagde afstand.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Er worden twee berekeningstypen ondersteund:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Vast<ept id="p1">**</ept>: er wordt een standaardtarief gebruikt voor de leveringsmethode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Als u dit berekeningstype selecteert, wordt het standaardtarief gedefinieerd in het veld <bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Per afstandseenheid<ept id="p1">**</ept>: de kosten voor de leveringsmethode en de gelaagde afstand worden berekend als de waarde die is opgegeven in het veld <bpt id="p2">**</bpt>Kosten<ept id="p2">**</ept> maal de afstand tussen het afleveradres en de locaties.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: geef de waarde op die wordt gebruikt in combinatie met het veld <bpt id="p2">**</bpt>Berekeningstype<ept id="p2">**</ept> om de kosten voor de leveringsmethode te berekenen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="0" state="translated">Wanneer u gelaagde afstanden definieert, wordt door het systeem gecontroleerd of er geen ontbrekende of overlappende afstanden zijn.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="0" state="translated">Het afstandstype dat voor een leveringsmethode wordt gebruikt moet hetzelfde zijn voor alle gelaagde afstanden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Kostencomponenttype Overig</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">In deze sectie wordt uitgelegd hoe u de verschillende combinaties van het kostencomponenttype <bpt id="p1">**</bpt>Overig<ept id="p1">**</ept> en een overig kostentype voor niet-verzendkosten kunt instellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Ook wordt uitgelegd hoe de DOM-oplossingsfunctie deze combinaties toepast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="0" state="translated">Kostencomponenttype = Overig en Overig kostentype = Verkooporder</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="60" state="translated" state-qualifier="fuzzy-match">Een combinatie van het kostencomponenttype <bpt id="p1">**</bpt>Overig<ept id="p1">**</ept> en het overige kostentype <bpt id="p2">**</bpt>Verkooporder<ept id="p2">**</ept> wordt gebruikt voor het definiëren van niet-verzendkosten op het niveau van de verkooporder.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">U moet de volgende velden instellen voor deze combinatie:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="60" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfactor<ept id="p1">**</ept>: voer een unieke id voor de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="77" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschrijving<ept id="p1">**</ept>: voer de naam en de omschrijving van de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Begindatum<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Einddatum<ept id="p2">**</ept>: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Actief<ept id="p1">**</ept>: geef aan of de kostenfactor actief is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de verkooporder.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Kostencomponenttype = Overig en Overig kostentype = Verkoopregel</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">Een combinatie van het kostencomponenttype <bpt id="p1">**</bpt>Overig<ept id="p1">**</ept> en het overige kostentype <bpt id="p2">**</bpt>Verkoopregel<ept id="p2">**</ept> wordt gebruikt voor het definiëren van niet-verzendkosten op het niveau van de verkooporderregel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">U moet de volgende velden instellen voor deze combinatie:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="60" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfactor<ept id="p1">**</ept>: voer een unieke id voor de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="77" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschrijving<ept id="p1">**</ept>: voer de naam en de omschrijving van de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Begindatum<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Einddatum<ept id="p2">**</ept>: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Actief<ept id="p1">**</ept>: geef aan of de kostenfactor actief is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de verkooporderregel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Kostencomponenttype = Overig en Overig kostentype = Locatie</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Een combinatie van het kostencomponenttype <bpt id="p1">**</bpt>Overig<ept id="p1">**</ept> en het overige kostentype <bpt id="p2">**</bpt>Locatie<ept id="p2">**</ept> wordt gebruikt voor het definiëren van niet-verzendkosten voor een groep van locaties of een individuele locatie.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">U moet de volgende velden instellen voor deze combinatie:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="60" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfactor<ept id="p1">**</ept>: voer een unieke id voor de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="77" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschrijving<ept id="p1">**</ept>: voer de naam en de omschrijving van de kostenfactor in.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Begindatum<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Einddatum<ept id="p2">**</ept>: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Actief<ept id="p1">**</ept>: geef aan of de kostenfactor actief is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Afhandelingsgroep<ept id="p1">**</ept>: geef de groep met locaties op waarvoor de niet-verzendkosten worden gedefinieerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Afhandelingslocatie<ept id="p1">**</ept>: geef de locatie op waarvoor de niet-verzendkosten worden gedefinieerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="0" state="translated">U kunt niet op dezelfde regel een afhandelingsgroep en een afhandelingslocatie opgeven voor op locatie gebaseerde berekeningscriteria.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de afhandelingsgroep of de afhandelingslocatie.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="0" state="translated">Voordat deze kosten in Gedistribueerd orderbeheer (DOM) worden meegenomen, moet u de kostenfactor toevoegen aan het relevante afhandelingsprofiel.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>
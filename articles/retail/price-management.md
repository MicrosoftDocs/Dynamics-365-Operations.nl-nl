<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="price-management.md" target-language="nl-NL">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>price-management.9d0b0e.afa553fd0562b306f720f2a30c7f901db7ad1b3a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>afa553fd0562b306f720f2a30c7f901db7ad1b3a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>0fbfb9b0ab78c804f3931a083028d2ce313d6521</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/21/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\price-management.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkoopprijsbeheer detailhandel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the concepts for creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit onderwerp beschrijft de concepten voor het maken en beheren van verkoopprijzen in Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkoopprijsbeheer van detailhandel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information about the process of creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit onderwerp bevat informatie over het proces voor het maken en beheren van verkoopprijzen in Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>It focuses on the concepts that are involved in this process, and on the effects of the various configuration options for sales prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het richt zich op de concepten die betrokken zijn bij dit proces, en op de effecten van de verschillende configuratieopties voor verkoopprijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Terminology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Terminologie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The following terms are used in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De volgende termen worden gebruikt in dit onderwerp.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Term</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorwaarde</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Definition, usage, and notes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definitie, gebruik en notities</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The single unit amount that a product sells for in a point of sale (POS) client or on a sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het bedrag voor één eenheid waarvoor een product wordt verkocht in een verkooppunt-client (POS) of op een verkooporder.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this topic, the term <bpt id="p1">*</bpt>price<ept id="p1">*</ept> always refers to the sales price, not the inventory price or cost price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit onderwerp heeft de term <bpt id="p1">*</bpt>prijs<ept id="p1">*</ept> altijd betrekking op de verkoopprijs niet op de voorraadprijs of de kostprijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basisprijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The price that is set in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on a released product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De prijs die is ingesteld in het veld <bpt id="p1">**</bpt>Prijs<ept id="p1">**</ept> voor een vrijgegeven product.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Trade agreement price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handelsovereenkomstprijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The price that is set on a product or variant by using a trade agreement of the <bpt id="p1">**</bpt>Price (sales)<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De prijs die is ingesteld voor een product of variant op basis van een handelsovereenkomst van het type <bpt id="p1">**</bpt>Prijs (verkoop)<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Best price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beste prijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When more than one price or discount can be applied to a product, the smallest price amount and/or the largest discount amount that produces the lowest possible net amount that the customer must pay.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer meerdere prijzen of kortingen kunnen worden toegepast op een product, het kleinste prijsbedrag en/of het grootste kortingsbedrag wat leidt tot het laagst mogelijke nettobedrag dat de klant moet betalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In this topic, the concept of best price is always referred to as "the best price."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit onderwerp wordt het concept van de beste prijs altijd aangeduid als 'de beste prijs.'</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This best price differs from and should not be confused with the <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> enumeration value for a discount's concurrency mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze beste prijs verschilt van en moet niet worden verward met de opsommingswaarde <bpt id="p1">**</bpt>Beste prijs<ept id="p1">**</ept> voor een gelijktijdigheidsmodus voor korting.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijsgroepen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Price groups are at the heart of price and discount management in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijsgroepen vormen de kern van het prijzen- en kortingenbeheer in Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Price groups are used to assign prices and discounts to retail entities (that is, channels, catalogs, affiliations, and loyalty programs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijsgroepen worden gebruikt om prijzen en kortingen toe te wijzen aan detailhandelentiteiten (zoals kanalen, catalogi, aansluitingen en loyaliteitsprogramma's).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Because price groups are used for all pricing and discounts, it's very important that you plan how you will use them before you start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aangezien prijsgroepen worden gebruikt voor alle prijzen en kortingen, is het belangrijk dat u plant hoe u ze gebruikt voordat u begint.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>By itself, a price group is just a name, a description, and, optionally, a pricing priority.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijsgroep is in feite alleen een naam, een omschrijving en eventueel een prioriteit voor prijscalculatie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The main point to remember about price groups is that they are used to manage the many-to-many relationships that discounts and prices have with retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het belangrijkste punt om te onthouden over prijsgroepen is dat ze worden gebruikt om de veel-op-veel-relaties van kortingen en prijzen met retailentiteiten te beheren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following illustration shows how price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De volgende afbeelding laat zien hoe prijsgroepen worden gebruikt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In this illustration, notice that "Price group" is literally at the center of pricing and discount management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In deze afbeelding ziet u dat 'Prijsgroep' letterlijk het middelpunt is van prijzen- en kortingsbeheer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The retail entities that you can use to manage differential prices and discounts are on the left, and the actual price and discount records are on the right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De retailentiteiten die u kunt gebruiken voor het beheren van gedifferentieerde prijzen en kortingen staan aan de linkerkant en de werkelijke prijzen- en kortingsrecords aan de rechterkant.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">![</bpt>Price groups<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>Price groups<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Prijsgroepen<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>Prijsgroepen<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>When you create price groups, you should not use a single price group for multiple types of retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer u prijsgroepen maakt, moet u niet één prijsgroep gebruiken voor meerdere soorten retailentiteiten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Otherwise, it can be difficult to determine why a specific price or discount is being applied to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Anders kan het lastig zijn om te bepalen waarom een bepaalde prijs of korting op een transactie wordt toegepast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>As the red dashed line in the illustration shows, Retail does support the core Microsoft Dynamics 365 functionality of a price group that is set directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zoals de rode streepjeslijn in de afbeelding laat zien, ondersteunt Retail de basisfunctie van Microsoft Dynamics 365 van prijsgroepen die direct voor een klant zijn ingesteld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>However, in this case, you get only sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit geval krijgt u echter alleen verkoopprijshandelsovereenkomsten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you want to apply customer-specific prices, we recommend that you not set price groups directly on the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u klantspecifieke prijzen wilt toepassen, raden wij aan dat u niet prijsgroepen rechtstreeks voor de klant instelt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Instead, you should use affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In plaats daarvan moet u aansluitingen gebruiken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The following sections provide more information about the retail entities that you can use to set distinct prices when the price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De volgende secties bevatten meer informatie over de retailentiteiten die u kunt gebruiken om verschillende prijzen in te stellen wanneer prijsgroepen worden gebruikt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The configuration of prices and discounts for all these entities is a two-step process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De configuratie van prijzen en kortingen voor alle entiteiten is een tweeledig proces.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>These steps can be done in either order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze stappen kunnen in een willekeurige volgorde worden uitgevoerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>However, the logical order is to set the price groups on the entities first, because this step is likely to be a one-time setup that is done during implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De logische volgorde is echter om de prijsgroepen eerst in te stellen voor de entiteiten, omdat deze stap waarschijnlijk een eenmalige instelling is die wordt uitgevoerd tijdens de implementatie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Then, as prices and discounts are created, you can set the price groups on those prices and discounts individually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vervolgens kunt u, als prijzen en kortingen zijn gemaakt, de prijsgroepen afzonderlijk instellen voor deze prijzen en kortingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Channels</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afzetkanalen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the retail industry, it's very typical to have different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In de detailhandel is het heel gebruikelijk om verschillende prijzen te hanteren voor verschillende kanalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The two primary factors that affect channel-specific prices are costs and local market conditions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De twee primaire factoren die invloed hebben op specifieke kanaalprijzen zijn kosten en voorwaarden van de lokale markt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Costs<ept id="p1">**</ept> – The farther away a channel is from the product source, the more it costs to stock a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept> : hoe verder een kanaal van de productbron verwijderd is, hoe meer het kost om een product op te slaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For example, fresh produce has a limited shelf life and specific production requirements (for example, a growing season).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verse producten hebben bijvoorbeeld een beperkte houdbaarheid en specifieke productievereisten (bijvoorbeeld een groeiseizoen).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>During the winter, fresh lettuce likely costs more in northern climates than in southern climates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In de winter kosten kost sla waarschijnlijk meer in noordelijke klimaten dan in zuidelijke klimaten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If you're setting prices for channels over a large geographical area, you will probably want to set different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u de prijzen voor kanalen over een groot geografisch gebied instelt, wilt u waarschijnlijk verschillende prijzen instellen in verschillende kanalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Local market conditions<ept id="p1">**</ept> – A store that has a direct competitor across the street will be much more price-sensitive than a store that doesn't have a direct competitor nearby.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Lokale marktvoorwaarden<ept id="p1">**</ept>: een winkel die een directe concurrent in de straat heeft, werkt veel prijsgevoeliger dan een winkel die geen directe concurrent in de buurt heeft.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Affiliations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aansluitingen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The general definition of an affiliation is a link to or association with a group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De algemene definitie van een aansluiting is een koppeling naar of de koppeling met een groep.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In Retail, affiliations are groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Retail zijn aansluitingen groepen met klanten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Affiliations are a much more flexible tool for customer pricing and discounts than the core Microsoft Dynamics 365 concept of customer groups and discount groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aansluitingen zijn een flexibelere manier voor klantprijzen en kortingen dan het basisconcept van Microsoft Dynamics 365 voor klantgroepen en kortingsgroepen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>First, an affiliation can be used for both prices and discounts, whereas non-retail pricing has a different group for each type of discount and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In de eerste plaats kan een aansluiting worden gebruikt voor prijzen en kortingen, terwijl bij niet-detailhandelsprijzen voor elk type prijs en korting een andere groep bestaat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Next, a customer can belong to multiple affiliations but can belong to only one non-retail pricing group of each type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vervolgens kan een klant deel uitmaken van meerdere aansluitingen maar van slechts één niet-detailhandelsprijsgroep van elk type.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Finally, although affiliations can be set up so that they are linked to a customer, they don't have to be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ten slotte kunnen aansluitingen zo worden ingesteld dat ze aan een klant zijn gekoppeld, maar dat hoeft niet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An ad-hoc affiliation can be used for anonymous customers at the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een ad-hoc-aansluiting kan worden gebruikt voor anonieme klanten op het POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>A typical example of an anonymous affiliation discount is a senior or student discount, where a customer can receive a discount just by showing a group membership card.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een typisch voorbeeld van een anonieme aansluitingskorting is een korting voor senioren of studenten waar een klant een korting kan ontvangen door een lidmaatschapskaart te tonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Although affiliations are most often associated with discounts, you can also use them to set differential pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hoewel aansluitingen meestal zijn gekoppeld aan kortingen, kunt u ze ook gebruiken om gedifferentieerde prijzen in te stellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For example, when a retailer sells to an employee, it might want to change the selling price instead of applying a discount on top of the regular price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer een detailhandelaar bijvoorbeeld aan een werknemer verkoopt, kan de verkoopprijs worden aangepast in plaats van het toepassen van een korting boven op de normale prijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>As another example, a retailer that sells to both consumer customers and business customers might offer business customers better prices, based on their purchasing volume.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ook kan een detailhandelaar die aan particuliere en zakelijke klanten verkoopt, zakelijke klanten betere prijzen bieden, op basis van hun inkoopvolume.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Affiliations enable both these scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aansluitingen maken beide scenario's mogelijk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Loyalty programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Loyaliteitsprogramma's</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In relation to prices and discounts, loyalty programs are basically just an affiliation that has a special name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Loyaliteitsprogramma's voor prijzen en kortingen zijn in feite een aansluiting met een speciale naam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Both prices and discounts can be set for a loyalty program, just as they can be set for an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijzen en kortingen kunnen worden ingesteld voor een loyaliteitsprogramma, net zoals ze kunnen worden ingesteld voor een aansluiting.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>However, the way that customers get loyalty pricing during a transaction or order differs from the way that they get affiliation pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De manier waarop klanten loyaliteitsprijzen krijgen tijdens een transactie of order, verschilt echter van de manier waarop deze prijscalculatie voor aansluitingen plaatsvindt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Customers can get loyalty pricing only if a loyalty card is added to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klanten kunnen alleen loyaliteitsprijzen als een loyaliteitskaart wordt toegevoegd aan de transactie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>When a loyalty card is added to a transaction, the loyalty program is also added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer een loyaliteitskaart die is toegevoegd aan een transactie, wordt ook het loyaliteitsprogramma toegevoegd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The loyalty program then enables special prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Met het loyaliteitsprogramma worden speciale prijzen en kortingen mogelijk gemaakt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Loyalty programs can have multiple tiers, and the discounts can differ for different tiers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Loyaliteitsprogramma's kunnen verschillende lagen hebben en de kortingen voor verschillende lagen kunnen verschillen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In this way, retailers can give frequent customers larger rewards without having to manually put those customers into a special group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op deze manier kunnen detailhandelaren terugkerende klanten grotere beloningen geven zonder dat deze klanten handmatig in een speciale groep worden geplaatst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Loyalty programs have additional functionality besides prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Loyaliteitsprogramma's hebben extra functies naast prijzen en kortingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>However, from the perspective of pricing and discounts, they are the same as affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vanuit het perspectief van prijzen en kortingen zijn ze echter hetzelfde als aansluitingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Catalogs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Catalogi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Some retailers use physical or virtual catalogs to market products to, and price them for, focused groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sommige detailhandelaren gebruiken fysieke of virtuele catalogi om producten te verkopen en prijzen vast te stellen voor specifieke groepen klanten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>As part of their business model to target marketing via a catalog, these retailers can set differential prices on their various catalogs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als onderdeel van hun bedrijfsmodel met gerichte marketing via een catalogus, kunnen deze detailhandelaren gedifferentieerde prijzen instellen voor verschillende catalogi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Microsoft Dynamics 365 supports this capability by letting you define catalog-specific discounts and prices, just as you can define channel-specific or affiliation-specific discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 ondersteunt deze functionaliteit met het definiëren van catalogusspecifieke kortingen en prijzen, net zoals u kortingen kunt definiëren voor kanalen of aansluitingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>When you edit a catalog, you can associate price groups with the catalog, just as you can associate them with a channel, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer u een catalogus bewerkt, kunt u prijsgroepen koppelen aan de catalogus, net zoals u ze aan een kanaal, aansluiting of loyaliteitsprogramma kunt koppelen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Best practices for price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aanbevolen procedures voor prijsgroepen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Don't use a price group for multiple retail entity types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruik geen een prijsgroep voor meerdere retailentiteitstypen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Instead, use one set of price groups for channels, a different set of price groups for affiliations or loyalty programs, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruik in plaats daarvan één set met prijsgroepen voor kanalen, een andere set met prijsgroepen voor aansluitingen of loyaliteitsprogramma's, enzovoort.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You can use a prefix or suffix in the name of the price group to visually group the various types of price groups that you're using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U kunt een voorvoegsel of achtervoegsel toevoegen aan de naam van de prijsgroep om de verschillende typen prijsgroepen visueel te groeperen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Avoid setting price groups directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stel prijsgroepen niet rechtstreeks in op een klant.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Instead, use an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruik in plaats daarvan een aansluiting.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this way, you can assign all types of prices and discounts to customers, not just sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op deze manier kunt u alle soorten prijzen en kortingen toewijzen aan klanten, niet alleen handelsovereenkomsten voor verkoopprijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Pricing priority</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prioriteit prijscalculatie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>By itself, a pricing priority is just a number and a description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prioriteit voor een prijscalculatie is in feite alleen een nummer en een omschrijving.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Pricing priorities can be applied to price groups, or they can be applied directly to discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prioriteiten voor prijscalculaties kunnen worden toegepast op de prijsgroepen of rechtstreeks op kortingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>When pricing priorities are used, they let a retailer override the principle of the best price by controlling the order in which prices and discounts are applied to products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer prioriteiten voor prijscalculaties worden gebruikt, kan een detailhandelaar het principe van de beste prijs overschrijven door de volgorde te bepalen waarin prijzen en kortingen worden toegepast op producten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>A larger pricing priority number is evaluated before a lower pricing priority number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een hoger prioriteitsnummer wordt geëvalueerd voor lager prioriteitsnummer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Additionally, if a price or discount is found at any priority number, all prices or discounts that have lower priority numbers are ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ook als een prijs of korting op een willekeurig prioriteitsnummer wordt gevonden, worden alle prijzen of kortingen met een lager prioriteitsnummer genegeerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The price and a discount can come from two different pricing priorities, because pricing priorities apply to prices and discounts independently.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De prijs en korting kunnen afkomstig zijn uit twee verschillende prijsprioriteiten, omdat de prijsprioriteiten los van elkaar van toepassing zijn op prijzen en kortingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>To use pricing priority for prices, you must assign a pricing priority to a price group and then create a sales price trade agreement for that price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u prioriteit voor prijzen gebruikt, moet u een prioriteit voor prijscalculatie toewijzen aan een prijsgroep en vervolgens een handelsovereenkomst maken voor deze prijsgroep.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The pricing priority feature was introduced to support the scenario where a retailer wants to apply higher prices in a specific set of stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De functie prioriteit voor prijscalculatie is geïntroduceerd voor het scenario waarin een detailhandelaar hogere prijzen wil toepassen in een specifieke reeks winkels.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For example, a retailer has defined regional prices for the east coast of the United States but wants higher prices for some products in New York City stores, because it costs more to sell some products in the city, and/or because the local market will bear a higher price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bijvoorbeeld: als een detailhandelaar regionale prijzen heeft gedefinieerd voor de oostkust van de Verenigde Staten, maar hogere prijzen wil berekenen voor bepaalde producten in winkels in New York City, omdat het duurder is om sommige producten daar te verkopen en/of omdat de plaatselijke markt bereid is een hogere prijs te betalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>As was described in the "Best price" section of this topic, the retail pricing engine typically selects the lower of two prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zoals is aangegeven in de sectie 'Beste prijs' van dit onderwerp, selecteert de engine voor detailhandelsprijzen doorgaans de laagste van de twee prijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Therefore, the retailer is usually prevented from using the higher of two prices in a store that has both the East coast and New York price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daarom zal de detailhandelaar meestal niet de hoogste van twee prijzen hanteren in een winkel met prijsgroepen voor zowel oostkust en voor New York.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>To resolve this issue before the pricing priority feature was introduced, the retailer had to define prices for every product two times and not assign both price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Om dit probleem op te lossen moest de detailhandelaar, voordat de functie voor prioriteit prijscalculatie werd geïntroduceerd, voor elk product tweemaal prijzen definiëren en niet beide prijsgroepen toewijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Alternatively, the retailer had to create extra price groups to isolate the products that have higher prices from products that have the usual, lower prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ook moest de detailhandelaar extra prijsgroepen maken om de producten met hogere prijzen af te scheiden van producten met de gebruikelijke, lagere prijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>However, the pricing priority feature lets the retailer create a pricing priority for store prices that is higher than the pricing priority for regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Met de e functie prioriteit prijscalculatie kan de detailhandelaar echter een prijsprioriteit instellen voor winkelprijzen die hoger zijn dan de prijsprioriteit voor regionale prijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Alternatively, the retailer can create a pricing priority just for store prices and leave regional prices at the default pricing priority, which is 0 (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailhandelaar kan ook alleen een prioriteit prijscalculatie opstellen voor winkelprijzen en regionale prijzen op de standaard prijsprioriteit van 0 (nul) laten staan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Both setups help guarantee that store prices will always be used before regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beide instellingen zorgen dat altijd winkelprijzen worden gebruikt vóór regionale prijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Pricing priority example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld prioriteit prijscalculatie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Let's look at an example where store prices override other prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laten we kijken naar een voorbeeld waarin winkelprijzen andere prijzen overschrijven.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>A national retailer sets most prices per region, and it has four regions: North east, South east, Mid-west and West.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een nationale detailhandelaar stelt de meeste prijzen in per regio en werkt met vier gebieden: Noordoost, Zuidoost, Midden-west en West.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It has identified several high-cost markets that can support higher prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Er zijn verschillende markten met hoge kosten aangegeven die in aanmerking komen voor hogere prijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These markets are in New York City, Chicago, and the San Francisco Bay area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze markten zijn in New York City, Chicago en het gebied van San Francisco Bay.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>For this example, we will drill into the North east region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit voorbeeld zullen we op de regio Noordoost inzoomen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Store 1 is in Boston, and store 2 is in Manhattan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winkel 1 is in Boston en winkel 2 in Manhattan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For the Boston store, two price groups are linked to the channel: North East and Store 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor de winkel in Boston zijn twee prijsgroepen gekoppeld aan het kanaal: Noordoost en Winkel 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>For the Manhattan store, three price groups are linked to the channel: North East, NYC, and Store 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor de winkel in Manhattan zijn drie prijsgroepen gekoppeld aan het kanaal: Noordoost, NYC en Winkel 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The retailer sets up two pricing priorities: High cost has a priority number of 5, and Store prices has a priority number of 10.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailhandelaar stelt twee prioriteiten voor prijscalculatie: hoge kosten heeft een prioriteitsnummer van 5 en winkelprijzen een prioriteitsnummer van 10.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>(Remember that, by default, the pricing priority is 0 <ph id="ph1">\[</ph>zero<ph id="ph2">\]</ph>, and a price or discount that has a higher priority number is used before a price or discount that has a lower priority number.) For the North East price group, the pricing priority is left at the default value of <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Houd er rekening mee dat de prioriteit prijscalculatie standaard 0 is <ph id="ph1">\[</ph>nul<ph id="ph2">\]</ph>, en een prijs of korting met een hogere prioriteit voorrang krijgt op een prijs of korting met een lager prioriteitsnummer.) De prioriteit prijscalculatie voor de prijsgroep Noordoost staat op de standaardwaarde van <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (nul).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>For the NYC price group, the pricing priority is set to <bpt id="p1">**</bpt>5<ept id="p1">**</ept>, because New York City is a high-cost market.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De de prijsgroep NYC is het prioriteitsnummer ingesteld op <bpt id="p1">**</bpt>5<ept id="p1">**</ept>, aangezien New York City een markt met hoge kosten is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For the Store 1 and Store 2 price groups, the pricing priority is set to <bpt id="p1">**</bpt>10<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor de prijsgroepen van winkel 1 en 2 is de prioriteit prijscalculatie ingesteld op <bpt id="p1">**</bpt>10<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Two products that the retailer sells are product 1, a commodity T-shirt, and product 2, brand-specific fashion jeans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailhandelaar verkoopt deze twee producten: basisproduct 1 is een T-shirt en product 2 een merkspecifieke spijkerbroek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Product</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Product</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>North East price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijs Noordoost</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>NYC price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijs NYC</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Store price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winkelprijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>T-shirt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">T-shirt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>$15</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$ 15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Niet ingesteld</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Niet ingesteld</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Fashion jeans</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spijkerbroek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>$50</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$ 50</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>$70</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$ 70</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Niet ingesteld</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The T-shirt sells for the same price (that is, $15) at both the Boston and Manhattan stores, because only one price is set in the North East price group that is linked to both channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het T-shirt wordt verkocht voor dezelfde prijs (dat wil zeggen $ 15) in de winkels in Boston en Manhattan, omdat slechts één prijs is ingesteld in de prijsgroep Noordoost die is gekoppeld aan beide kanalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The fashion jeans sell for $50 in the Boston store, because that price is the only price that is available in that store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De jeans wordt verkocht voor $50 in de winkel in Boston omdat deze prijs de enige prijs is die beschikbaar is in deze winkel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>However, in the Manhattan store, two prices are available: $50 and $70.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Er zijn echter twee prijzen beschikbaar in de winkel in Manhattan: $ 50 en $ 70.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Because the pricing priority of 5 for the NYC price group is higher than the pricing priority of 0 (zero) for the North East price group, the price will be rung up as $70 in the POS system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omdat de prioriteit prijscalculatie van 5 voor de prijsgroep NYC hoger is dan de prioriteit van 0 (nul) voor de prijsgroep Noordoost, wordt de prijs als $ 70 opgenomen in het POS-systeem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>For each pricing priority, a full pass through the logic for the retail pricing engine is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor elke prioriteit prijscalculatie moet de logica van de engine voor detailhandelsprijzen volledig worden verwerkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Therefore, to help maintain the performance of the price and discount calculation, you should use pricing priorities sparingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Om te garanderen dat de prijzen en kortingen correct worden berekend, moet u prijsprioriteiten spaarzaam toepassen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Types of prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Typen prijzen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In Microsoft Dynamics 365, you can set the price of a product in three places:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Microsoft Dynamics 365 kunt u de prijs van een product op drie plaatsen instellen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Directly on the product (base price)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rechtstreeks op het product (basisprijs)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In a sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In een handelsovereenkomst voor de verkoopprijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>In a price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In een prijscorrectie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The base price and trade agreement price are part of core Microsoft Dynamics 365, and are available even if you don't use Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De basisprijs en de handelsovereenkomstprijs maken deel uit van de kernfuncties van Microsoft Dynamics 365 en zijn beschikbaar zelfs als u Retail niet gebruikt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The price adjustment functionality is available only in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De functionaliteit voor prijscorrectie is alleen beschikbaar in Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The next section provides more information about each of these options for setting prices and explains how the options work together.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In de volgende sectie vindt u meer informatie over de opties voor het instellen van prijzen en wordt uitgelegd hoe de opties samenwerken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Setting prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijzen instellen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basisprijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The easiest place to set the price for a product is directly on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De gemakkelijkste plaats om de prijs voor een product in te stellen is rechtstreeks op het product.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The value that you set directly on a product is often referred to as the base price for the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De waarde die u rechtstreeks op een product instelt, wordt vaak de basisprijs voor het product genoemd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>You set the base price in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Released product details<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U stelt de basisprijs in in het veld <bpt id="p1">**</bpt>Prijs<ept id="p1">**</ept> van het tabblad <bpt id="p2">**</bpt>Verkopen<ept id="p2">**</ept> van de pagina <bpt id="p3">**</bpt>Vrijgegeven productdetails<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The value that you enter is in the company currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De ingevoerde waarde gebruikt de de valuta van het bedrijf.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>By default, the price is for a quantity of 1 of the unit of measure (UoM) that is set in the <bpt id="p1">**</bpt>Unit<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab. The actual price per unit of a product is based on the UoM, the price quantity, and the currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De prijs voor een hoeveelheid van 1 is standaard de maateenheid die is ingesteld in het veld <bpt id="p1">**</bpt>Eenheid<ept id="p1">**</ept> op het tabblad <bpt id="p2">**</bpt>Verkopen<ept id="p2">**</ept>. De werkelijke prijs per eenheid van een product is gebaseerd op de maateenheid, de prijshoeveelheid en de valuta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If a product has one price for everyone, the base price offers the most efficient way to manage the price of that product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als een product één prijs heeft voor iedereen, is de basisprijs de meest efficiënte manier om de prijs van dat product te beheren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Even if you use trade agreements to set prices, you might also set the base price on a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zelfs als u handelsovereenkomstprijzen toepast, kunt u ook de basisprijs op een product instellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Then, if you don't use an <bpt id="p1">**</bpt>All<ept id="p1">**</ept> trade agreement, you have a fallback price that is used when no trade agreement applies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u vervolgens niet een handelsovereenkomst van het type<bpt id="p1">**</bpt>Alle<ept id="p1">**</ept> gebruikt, hebt u een terugvalprijs die wordt gebruikt wanneer er geen handelsovereenkomst van toepassing is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>If a retail channel's currency differs from the company currency, the base price in that retail channel is determined by using currency conversion on the price that is set on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als een detailhandelkanaalsvaluta afwijkt van de bedrijfsvaluta, wordt de basisprijs in dat detailhandelkanaal bepaald met behulp van valutaconversie op de prijs die is ingesteld op het product.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Although the price unit isn't a common retail scenario, the retail pricing engine supports it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hoewel de prijs per eenheid geen gebruikelijk detailhandelscenario is, wordt dit ondersteund door de engine voor detailhandelsprijzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>If the price unit is set to a value other than <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero), the price per unit equals Price ÷ Price unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de prijs per eenheid is ingesteld op een andere waarde dan <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (nul), is de prijs per eenheid gelijk aan prijs ÷ prijs per eenheid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>For example, if a product's price is $10.00, and the price unit is 50, the price for a quantity of 1 is $0.20 (= $10.00 ÷ 50).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de prijs van een product bijvoorbeeld $10,00 is en de prijs per eenheid 50, is de prijs voor een hoeveelheid van 1 $0,20 (= $10,00 ÷ 50).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handelsovereenkomst met verkoopprijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>By using the trade agreement journal, you can create sales price trade agreements for each product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U kunt met behulp van het handelsovereenkomstjournaal een verkoopprijshandelsovereenkomst voor elk product maken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>In Microsoft Dynamics 365, there are three customer scopes for sales price trade agreements: <bpt id="p1">**</bpt>Table<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Group<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>All<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Microsoft Dynamics 365 zijn er drie klantbereiken voor verkoopprijshandelsovereenkomsten: <bpt id="p1">**</bpt>tabel<ept id="p1">**</ept>, <bpt id="p2">**</bpt>groep<ept id="p2">**</ept> en <bpt id="p3">**</bpt>alle<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The customer scope determines the customers that a given sales price trade agreement applies to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het bereik van de klant bepaalt de klanten waarvoor de handelsovereenkomst voor een bepaalde verkoopprijs geldt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>A <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> sales price trade agreement is for a single customer that is set directly on the trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een verkoopprijshandelsovereenkomst van het type <bpt id="p1">**</bpt>tabel<ept id="p1">**</ept> geldt voor één klant die rechtstreeks in de handelsovereenkomst is ingesteld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>This scenario isn't a typical retail business-to-consumer (B2C) scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit scenario is geen normaal detailhandelscenario voor business-to-consumer (B2C).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>However, if it occurs, the retail pricing engine uses <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> trade agreements when it determines price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als dit echter plaatsvindt, gebruikt de prijsbepalingsengine handelsovereenkomsten van het type <bpt id="p1">**</bpt>tabel<ept id="p1">**</ept> voor het bepalen van de prijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>A <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreement is the type that is most often used with retail functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een verkoopprijshandelsovereenkomst van het type <bpt id="p1">**</bpt>groep<ept id="p1">**</ept> wordt meestal gebruikt met de detailhandelsfunctionaliteit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Outside Retail, <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreements are for a simple customer group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Buiten Retail zijn verkoopprijshandelsovereenkomsten van het type <bpt id="p1">**</bpt>groep<ept id="p1">**</ept> van toepassing voor een eenvoudige klantengroep.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>However, in Retail, the concept of a customer group has been extended so that it's a more generic retail price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Retail is het concept van een klantgroep echter uitgebreid zodat deze een meer algemene detailhandelprijsgroep is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>A price group can be linked to a retail channel, affiliation, loyalty program, or catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijsgroep kan worden gekoppeld aan een detailhandelkanaal, aansluiting, loyaliteitsprogramma of catalogus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>For detailed information about price groups, see the "Price groups" section earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zie de sectie 'Prijsgroepen' eerder in dit onderwerp voor gedetailleerde informatie over prijsgroepen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>A trade agreement price is always used before the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijs uit een handelsovereenkomst heeft altijd voorrang op de de basisprijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijscorrectie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>As the name implies, a price adjustment is used to modify the price that was either set directly on the product or set by using a trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zoals de naam al aangeeft, wordt een prijscorrectie gebruikt voor het wijzigen van de prijs die rechtstreeks op het product of met een handelsovereenkomst is ingesteld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>A price adjustment can be used only to lower the price, not raise it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijscorrectie kan alleen worden gebruikt voor het verlagen van de prijs, niet voor het verhogen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>A price adjustment is the recommended way for retailers to create, track, and manage price markdowns for their products over time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijscorrectie is de aanbevolen manier voor detailhandelaren voor het maken, bijhouden en beheren van prijsverlagingen voor hun producten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>There are three types of price adjustments: percentage off, amount off, and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Er zijn drie typen prijscorrecties: percentage, korting en prijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>A price adjustment of the percentage off or amount off type is always applied to a sale transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijscorrectie van het type percentage of kortingsbedrag wordt altijd toegepast op een verkooptransactie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>However, a price adjustment of the price type is applied only if the adjusted price is less than the price that was set by using the base price or trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijscorrectie van het prijstype is echter alleen van toepassing als de gecorrigeerde prijs lager dan de prijs die is ingesteld met behulp van de basisprijs of de handelsovereenkomstprijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Therefore, if the price that is set in a price adjustment is more than the unadjusted price, the price adjustment isn't used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als dus de prijs die is ingesteld in een prijscorrectie hoger is dan de niet-gecorrigeerde prijs, wordt de prijscorrectie niet gebruikt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Determining price for a product in a transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijs voor een product in een transactie vaststellen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The calculation of the price and discount on a transaction uses the principle of finding the best price for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De berekening van de prijs en de korting op een transactie gebruikt het principe van het zoeken naar de beste prijs voor de klant.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>According to this principle, if more than one price is found, the lowest price is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Volgens dit principe wordt de laagste prijs gebruikt, als meer dan één prijs wordt gevonden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Additionally, the combination of discounts that produces the largest discount amount for the whole transaction is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bovendien wordt de combinatie van kortingen gebruikt die het grootste kortingsbedrag voor de gehele transactie produceert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>In some cases, a smaller discount must be used on a single product, so that additional discounts can be applied to other products in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In sommige gevallen moet een kleinere korting worden gebruikt op één product, zodat extra kortingen kunnen worden toegepast op andere producten in de transactie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The only exception to the principle of finding the best price for the customer is an option for mix-and-match least-expensive discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De enige uitzondering op het principe van het zoeken naar de beste prijs voor de klant is een optie voor goedkoopste gecombineerde kortingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>This option enables least-expensive discounts that favor the retailer when products are selected and grouped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze optie maakt de goedkoopste kortingen mogelijk ten gunste van de detailhandelaar wanneer producten worden geselecteerd en gegroepeerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Therefore, when a transaction includes more products than are required to qualify for the least-expensive discount, the retail pricing engine selects the products that produce the smallest possible discount amount for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer een transactie meer producten bevat dan vereist zijn om in aanmerking te komen voor de goedkoopste korting, selecteert de prijsbepalingsengine de producten waarmee het kleinst mogelijke kortingsbedrag voor de klant wordt geproduceerd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The retail pricing engine returns three prices for every product: the base price, the trade agreement price, and the active price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De prijsbepalingsengine retourneert drie prijzen voor elk product: de basisprijs, de prijs van de handelsovereenkomst en de actieve prijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The base price is just the property on the product and is the same for everyone everywhere.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De basisprijs is alleen de eigenschap van het product en is hetzelfde voor iedereen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>On the sales price trade agreement, if the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the lowest price that is found for applicable sales price trade agreements is used as the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voor de verkoopprijs uit de handelsovereenkomst wordt, als de optie <bpt id="p1">**</bpt>Volgende zoeken<ept id="p1">**</ept> is ingesteld op <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>, de laagste prijs die wordt gevonden voor de toepasselijke verkoopprijshandelsovereenkomsten gebruikt als de prijs van de handelsovereenkomst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Trade agreements can be found by using price groups or the <bpt id="p1">**</bpt>ALL<ept id="p1">**</ept> account code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U vindt handelsovereenkomsten met behulp van prijsgroepen of de rekeningcode <bpt id="p1">**</bpt>Alle<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Alternatively, trade agreements can be assigned directly to a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handelsovereenkomsten kunnen ook rechtstreeks aan een klant worden toegewezen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>If the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>, the first trade agreement price that is found is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als de optie <bpt id="p1">**</bpt>Volgende zoeken<ept id="p1">**</ept> is ingesteld op <bpt id="p2">**</bpt>Nee<ept id="p2">**</ept>, wordt de eerste handelsovereenkomstprijs gebruikt die is gevonden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>If no sales price trade agreements are found, then the trade agreement price is set equal to the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als er geen verkoopprijshandelsovereenkomsten worden gevonden, wordt de prijs van de handelsovereenkomst gelijk gesteld aan de basisprijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The active price is calculated by taking the trade agreement price and applying the largest price adjustment that applies to the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De actieve prijs wordt berekend door de prijs van de handelsovereenkomst te nemen en de grootste prijscorrectie toe te passen die voor het product geldt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>If no price adjustments are found, or if the calculated active price is more than the trade agreement price, the active price is set equal to the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als er geen prijscorrecties worden gevonden of als de berekende actieve prijs groter is dan de prijs van de handelsovereenkomst, wordt de actieve prijs gelijk gesteld aan de prijs van de handelsovereenkomst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Remember that you can't raise the price of a product by using a price adjustment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vergeet niet dat u de prijs van een product niet kunt verhogen met een prijscorrectie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The applicable price adjustments can be found only by using price groups that are assigned to a channel, catalog, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De toepasselijke prijscorrecties vindt u alleen met behulp van prijsgroepen die zijn toegewezen aan een kanaal, catalogus, aansluiting of loyaliteitsprogramma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Category price rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijsregels van categorie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>The category price rules feature in Retail gives you an easy way to create new trade agreements for all the products in a category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De categorieprijsregels in Retail bieden u een eenvoudige manier om nieuwe handelsovereenkomsten voor alle producten in een categorie maken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>This feature also lets you automatically find existing trade agreements for the products in the category and expire them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Met deze functie kunt u ook automatisch bestaande handelsovereenkomsten voor de producten in de categorie zoeken en ze laten verlopen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>When you select the option to expire existing trade agreements, the system creates a new trade agreement journal for the products in the category that have an active trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer u de optie selecteert om bestaande handelsovereenkomsten te laten verlopen, maakt het systeem een nieuwe handelsovereenkomstjournaal voor de producten in de categorie die een actieve handelsovereenkomst hebben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>However, the journal must be manually posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hhet journaal moet echter handmatig worden geboekt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Additionally, the category price rules can find existing trade agreements only if you're using the same price rule (that is, if you create a new price rule that uses the same category that was before).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bovendien kunnen de categorieprijsregels alleen bestaande handelsovereenkomsten vinden als u dezelfde prijsregel gebruikt (dat wil zeggen als u een nieuwe prijsregel maakt die gebruikmaakt van dezelfde categorie als voorheen).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>If you aren't using the same price rule, the existing trade agreements won't be expired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u niet dezelfde prijsregel gebruikt, zullen de bestaande handelsovereenkomsten niet verlopen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The prices can be increased or decreased by using the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Price basis<ept id="p2">**</ept> fields of the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De prijzen kunnen worden verhoogd of verlaagd met de velden <bpt id="p1">**</bpt>Prijsregel<ept id="p1">**</ept> en <bpt id="p2">**</bpt>Prijsbasis<ept id="p2">**</ept> van de categorieprijsregels.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>In the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> field, select the type of price change to use:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selecteer in het veld <bpt id="p1">**</bpt>Prijsregel<ept id="p1">**</ept> welk type prijswijziging u wilt gebruiken:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">**</bpt>Markup<ept id="p1">**</ept> – A percentage of the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Verhoging<ept id="p1">**</ept>: een percentage van de prijsbasis wordt gebruikt om de verkoopprijs te berekenen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a markup of 50 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld: een product dat 10,00 kost en voor 15,00 wordt verkocht, heeft een prijsverhoging van 50 procent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source><bpt id="p1">**</bpt>Margin<ept id="p1">**</ept> – A percentage of the sales price is used to calculate the amount of profit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Marge<ept id="p1">**</ept>: een percentage van de verkoopprijs wordt gebruikt om het winstbedrag te berekenen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a margin of 33.3 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld: een product dat 10,00 kost en voor 15,00 wordt verkocht, heeft een marge van 33,3 procent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source><bpt id="p1">**</bpt>Fixed amount<ept id="p1">**</ept> – An amount that is added to the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Vast bedrag<ept id="p1">**</ept>: een bedrag dat aan de gebruikte prijsbasis wordt toegevoegd om de verkoopprijs te berekenen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a fixed amount of 5.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voorbeeld: een product dat 10,00 kost en voor 15,00 wordt verkocht, heeft een vast bedrag van 5,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In the <bpt id="p1">**</bpt>Price basis<ept id="p1">**</ept> field, select the type of price to modify:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selecteer het type te wijzigen prijs in het veld <bpt id="p1">**</bpt>Prijsbasis<ept id="p1">**</ept>:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source><bpt id="p1">**</bpt>Base cost<ept id="p1">**</ept> – The amount that the retailer paid to the supplier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Basiskosten<ept id="p1">**</ept>: het bedrag dat de detailhandelaar aan de leverancier betaalde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source><bpt id="p1">**</bpt>Base price<ept id="p1">**</ept> – The sales price before trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Basisprijs<ept id="p1">**</ept>: de verkoopprijs voordat handelsovereenkomsten en de prijscorrecties worden toegepast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source><bpt id="p1">**</bpt>Current price<ept id="p1">**</ept> – The sales price after trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Huidige prijs<ept id="p1">**</ept>: de verkoopprijs nadat handelsovereenkomsten en de prijscorrecties zijn toegepast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>To easily update the prices of various products from different product categories, you can use the supplemental product categories together with the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u de prijzen van verschillende producten uit de verschillende productcategorieën eenvoudig wilt bijwerken, kunt u de aanvullende productcategorieën samen met de categorieprijsregels gebruiken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Best practices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aanbevolen procedures</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Microsoft SQL Server Express is often used for channel databases because of the cost (free).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server Express wordt vaak gebruikt voor kanaaldatabases vanwege de kosten (gratis).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Keep in mind that SQL Server Express has hardware limitations and limits on data size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Houd er rekening mee dat SQL Server Express hardwarebeperkingen en limieten heeft voor gegevensgrootte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>If you don't plan correctly, you can quickly reach the data size limits of SQL Server Express.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u niet goed plant, kunt u snel de grenzen van de gegevensgrootte van SQL Server Express bereiken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>This consideration applies not only to pricing but also to other areas of the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze overweging geldt niet alleen voor prijzen, maar ook voor andere gebieden van het product.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Here are a few best practices that can help you reduce the size of your data:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hier volgen enkele aanbevelingen waarmee u de grootte van uw gegevens kunt verminderen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>If you're using trade agreements, and your prices change, you should expire the old trade agreements by setting an end date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u handelsovereenkomsten gebruikt en uw prijzen veranderen, moet u de oude handelsovereenkomsten laten verlopen door een einddatum in te stellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Over time, this approach helps reduce the number of trade agreements that are kept in channel databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na verloop van tijd daalt door deze benadering het aantal handelsovereenkomsten dat is opgeslagen in de kanaaldatabases.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>It also helps reduce the amount of data that the price calculation algorithm must work with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ook vermindert de hoeveelheid gegevens waarmee het prijsberekeningsalgoritme moet werken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>If your prices vary by product variant, consider using the product base price as the price of the most common variant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als uw prijzen per productvariant verschillen, kunt u overwegen de basisprijs van het product als de prijs van de meest voorkomende variant te gebruiken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Then use trade agreements only for the variant prices that are exceptions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebruik vervolgens de handelsovereenkomsten alleen voor de variantprijzen die uitzonderingen zijn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>This approach helps reduce the number of trade agreement records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze benadering vermindert het aantal records voor handelsovereenkomsten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Because it's so easy to import data into Microsoft Dynamics 365, you might be tempted to import a trade agreement for every variant of every product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omdat het is eenvoudig is om gegevens te importeren in Microsoft Dynamics 365, wilt u wellicht een handelsovereenkomst importeren voor elke variant van elk product.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>However, that approach can produce many trade agreements that have the same value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die benadering kan echter leiden tot veel handelsovereenkomsten die dezelfde waarde hebben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Therefore, it can needlessly increase the size of your data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En daardoor onnodig de omvang van uw gegevens vergroten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Retail processes variant-specific prices in order from most specific to least specific.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail verwerkt variantspecifieke prijzen in volgorde van meest specifiek naar minst specifiek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>If a product dimension doesn't affect the price, you don't have to define trade agreements for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als een productdimensie geen invloed heeft op de prijs, hoeft u geen handelsovereenkomsten daarvoor te definiëren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>For example, a product is available in three colors and four sizes, but the price varies only by size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bijvoorbeeld: een product is beschikbaar in drie kleuren en vier afmetingen, maar de prijs varieert alleen door de grootte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>If you define a trade agreement for every variant, you create 12 records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u een handelsovereenkomst voor elke variant definieert, maakt u 12 records.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Instead, you can define a trade agreement just for each size and leave the Color dimension blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U kunt in plaats daarvan alleen een handelsovereenkomst definiëren voor elke grootte en de kleurdimensie leeg laten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>In this case, you produce only four records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dit geval hoeft u slechts 4 records te maken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Alternatively, if not every value of a dimension produces a different price, you can define one trade agreement for the product master and leave all product dimensions blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als niet alle waarden van een dimensie resulteren in een andere prijs, kunt u ook één handelsovereenkomst definiëren voor het productmodel en alle productdimensies leeg laten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Then define a separate trade agreement just for each dimension value that produces a different price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definieer vervolgens een aparte handelsovereenkomst voor elke dimensiewaarde die een andere prijs genereert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>For example, if the XXL size has a higher price, but all other sizes have the same price, you require only two trade agreements: one for the product master and one for the XXL size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bijvoorbeeld als de grootte XXL een hogere prijs heeft, maar alle andere afmetingen dezelfde prijs hebben, hoeft u slechts twee handelsovereenkomsten te maken: één voor het productmodel en één voor de grootte XXL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Prices that include tax vs. prices that exclude tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijzen inclusief btw versus prijzen exclusief btw</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>When you set sales prices in Microsoft Dynamics 365, you don't specify whether the price value that you're setting includes or excludes tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wanneer u verkoopprijzen in Microsoft Dynamics 365 instelt, geeft u niet aan of de waarde van de ingestelde prijs inclusief of exclusief btw is.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>The value is just the price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De waarde is alleen de prijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>However, the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on retail channels lets you configure retail channels so that they either include or exclude tax from prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Met de instelling <bpt id="p1">**</bpt>Prijs inclusief btw<ept id="p1">**</ept> voor detailhandelkanalen kunt u echter detailhandelkanalen zo configureren dat de prijzen al dan niet inclusief btw zijn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>This setting is set on the channel and can change even in a single company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Deze instelling is ingesteld voor het kanaal en kan zelfs in één bedrijf wijzigen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>If you work with both inclusive and exclusive types of tax, it's very important that you set prices correctly, because the total amount that the customer pays will change if the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on the channel is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Als u werkt met inclusief en exclusief btw, is het belangrijk dat u prijzen correct hebt ingesteld, omdat het totale bedrag dat de klant betaalt, niet verandert als de instelling <bpt id="p1">**</bpt>Prijs inclusief btw<ept id="p1">**</ept> in het kanaal wordt gewijzigd.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Differences between retail pricing and non-retail pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verschillen tussen adviesprijs en niet-adviesprijs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>A single pricing engine is used to calculate retail prices across all channels: Call center, Retail store, and Online stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Er wordt één prijscalculatie-engine gebruikt voor het berekenen van de detailhandelsprijzen voor alle kanalen: callcenters, winkels en online winkels.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>This helps in enabling the unified commerce scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dit is handig voor het inschakelen van de gecombineerde handelsscenario's.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Retail pricing is designed to work with retail entities instead of non-retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Adviesprijs is ontworpen om te gebruiken met detailhandelsentiteiten in plaats van niet-detailhandelsentiteiten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Specifically, it's designed to set prices by store, not by warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Het is vooral ontworpen om prijzen in te stellen per winkel, niet per magazijn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The retail pricing engine doesn't support the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De adviseprijsengine ondersteunt niet de volgende prijsbepalingsfuncties:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Setting price by using the Site and Warehouse storage dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prijs instellen met site- en magazijndimensies.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Attribute-based pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Op kenmerken gebaseerde prijzen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Vendor discount pass-through</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Leverancierskorting pass-through</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>In addition, <bpt id="p1">**</bpt>only<ept id="p1">**</ept> the retail pricing engine supports the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bovendien ondersteunt de adviseprijsengine <bpt id="p1">**</bpt>alleen<ept id="p1">**</ept> de volgende prijsbepalingsfuncties:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>The price is based on product dimensions, in order from the most-specific variant price to the least-specific variant price to the product master price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De prijs is gebaseerd op de productdimensies in volgorde van de meest specifieke variantprijs naar de minst specifieke variantprijs voor de modelproductprijs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>A price that is set by using two product dimensions (for example, Color and Size) is used before a price that is set by using only one product dimension (for example, Size).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Een prijs die wordt ingesteld via twee productdimensies (bijvoorbeeld kleur en grootte) wordt gebruikt vóór een prijs die is ingesteld via slechts één productdimensie (bijvoorbeeld grootte).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>The same price group can be used to control pricing and discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Dezelfde prijsgroep kan worden gebruikt om prijzen en kortingen te bepalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Pricing API enhancements</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verbeteringen in API voor prijzen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Price is one of the most important factors that govern the buying decisions of many customers, and many customers compare prices on various sites before they make a purchase.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Prijs is een van de belangrijkste factoren voor koopbeslissingen van veel klanten en veel klanten vergelijken de prijzen op verschillende locaties voordat ze overgaan tot koop.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>To help guarantee that they provide competitive prices, retailers keep a close eye on their competitors and often run promotions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Om er zeker van te zijn dat ze concurrerende prijzen bieden, houden detailhandelaren hun concurrenten goed in de gaten en hebben ze vaak acties.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Therefore, to help these retailers attract customers, it's very important that product search, the browse feature, lists, and the product details page show the most accurate prices.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Om deze detailhandelaren te helpen bij het aantrekken van klanten, is het zeer belangrijk dat bij het zoeken naar producten, in de bladerfunctie, lijsten en op de pagina met productdetails de meest nauwkeurige prijzen worden weergegeven.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>In an upcoming release of Retail, the <bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept> application programming interface (API) will return prices that include simple discounts (for example, single-line discounts that don't depend on other items in the cart).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In een aanstaande release van Retail retourneert de API <bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept> prijzen die eenvoudige kortingen bevatten (bijvoorbeeld kortingen van één regel die niet afhankelijk zijn van andere artikelen in de winkelwagen).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>In this way, the prices that are shown are close to the actual amount that customers will pay for items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Op deze manier liggen de prijzen die worden weergegeven dicht bij het werkelijke bedrag dat klanten voor artikelen betalen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>This API will include all the types of simple discounts: affiliation-based, loyalty-based, catalog-based, and channel-based discounts.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Deze API bevat alle soorten eenvoudige kortingen: op relatie, loyaliteit, catalogus en kanaal gebaseerde kortingen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Additionally, the API will return the names and validity information for the applied discounts, so that retailers can provide a more detailed description of the price and create a sense of urgency if the discount's validity will expire soon.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Daarnaast retourneert de API de namen en validiteitsgegevens voor de toegepaste kortingen, zodat detailhandelaren een meer gedetailleerde omschrijving van de prijs kunnen bieden en een gevoel van urgentie creëren als de geldigheid van de korting binnenkort verloopt.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>
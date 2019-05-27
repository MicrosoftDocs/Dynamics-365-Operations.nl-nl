---
title: Verkoopretouren
description: In dit onderwerp vindt u informatie over het proces voor retourorders. Het behandelt de afhandeling van klantretouren en het effect daarvan op kostprijsberekening en de voorhanden voorraadhoeveelheden.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dfeb393698431b1bbb0eb5069cc0930dc122374
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559141"
---
# <a name="sales-returns"></a>Verkoopretouren

[!include [banner](../includes/banner.md)]

In dit onderwerp vindt u informatie over het proces voor retourorders. Het behandelt de afhandeling van klantretouren en het effect daarvan op kostprijsberekening en de voorhanden voorraadhoeveelheden.

Klanten kunnen artikelen retourneren om verschillende redenen. Een artikel kan bijvoorbeeld beschadigd zijn of niet voldoen aan de verwachtingen van de klant. Het retourproces begint wanneer een klant een verzoek indient om een artikel te retourneren. Nadat het verzoek van de klant is ontvangen, wordt een retourorder gemaakt in Microsoft Dynamics 365 for Finance and Operations.

## <a name="return-order-process"></a>Het retourorderproces
De volgende afbeelding geeft een overzicht van het proces voor retourorders.  

[![Het retourorderproces](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Er zijn twee typen retourorderproces: Fysieke retouren en Alleen krediet.

-   **Fysieke retouren:** De retourorder autoriseert het fysiek retourneren van producten.
-   **Alleen credit:** De retourorder autoriseert het krediteren van een klant, zonder dat wordt vereist dat de klant de producten fysiek retourneert.

### <a name="physical-return-order-process"></a>Het proces voor fysieke retouren

1.  **Maak een retourorder.** Leg formeel de autorisatie vast voor de klant om een gebrekkig of ongewenste product te retourneren. De retourorder vereist niet dat het bedrijf de geretourneerde producten accepteert of de klant crediteert. Als de retour wordt geaccepteerd, kunt u een vervangend artikel laten verzenden voordat het gebrekkige artikel is geretourneerd.
2.  **Product komt aan in magazijn voor inspectie.** Voer een initiële inspectie uit en valideer het product op basis van het retourorderdocument. De retourorder ondersteunt ook quarantaine van de geretourneerde artikelen voor aanvullende inspectie en kwaliteitscontrole.
3.  **Bepaal de beschikking.** Rond het inspectieproces af en bepaal wat moet gebeuren met de geretourneerde producten. Bepaal in deze stap of u de klant crediteert, de productretour afwijst of accepteert, het product boekt als uitval en een vervangend product naar de klant zendt.
4.  **Genereer een pakbon.** Genereer een pakbon en leg de beschikking vast die u in stap 3 hebt genomen. Rond de logistieke processen af.
5.  **Genereer een factuur.** Sluit de retourorder af.

### <a name="credit-only-process"></a>Proces Alleen krediet

1.  **Maak een retourorder.** Leg formeel de autorisatie vast om de klant te crediteren zonder dat deze een gebrekkig of ongewenste product retourneert. De beschikkingscode **Alleen krediet** autoriseert de beslissing om de klant te crediteren zonder fysieke retour.
2.  **Genereer een factuur.** Genereer de creditnota en sluit vervolgens de retourorder.

## <a name="return-material-authorization"></a>Return Materials Authorization (RMA)
De verwerking van de Return Material Authorization (RMA) is gebaseerd op verkooporder-functionaliteit. Een RMA wordt geregistreerd als een retourorder. Deze wordt gemaakt als een verkooporder en er kan een andere verkooporder aan zijn gekoppeld, die een vervangingsorder wordt genoemd. Beide verkooporders zijn gekoppel aan het bron-RMA-nummer.

-   **Retourorder:** Om een RMA te registreren, maakt u een retourorder (d.w.z. een verkooporder waaraan het **Geretourneerde order** is toegewezen). Eventuele wijzigingen die u aanbrengt in de RMA-gegevens wordt automatisch bijgewerkt in de verkooporder. Totdat de status van de retourorder is gewijzigd in **Open**, is deze niet zichtbaar in de lijst met verkooporders. Met RMA's handelt u de ontvangst van geretourneerde artikelen af. Ook kunt u er beschikkingsacties van het type Alleen krediet mee afhandelen (zie de sectie **Beschikkingscodes en beschikkingsacties**). Alle andere opvolgingsprocessen moeten worden afgehandeld in de verkooporder.
-   **Vervangingsorder:** Wanneer een vervangingsorder moet worden verzonden naar de klant, kan de RMA een tweede gekoppelde verkooporder bevatten. U kunt de vervangingsorder voor de RMA handmatig aanmaken zodat deze onmiddellijk wordt verzonden. U kunt ook de vervangingsorder automatisch laten maken nadat ontvangst en inspectie zijn afgerond voor het RMA-regelartikel met een beschikkingscode die vervanging aangeeft. De vervangingsorder heeft dezelfde functionaliteit die een verkooporder heeft. Zo kunt u daarmee een aangepast product configureren als het vervangende artikel, een productieorder maken voor het herstel van een geretourneerd artikel, een inkooporder voor directe levering maken voor verzending van het vervangend artikel door een leverancier of andere doelen ondersteunen.

## <a name="create-a-return-order"></a>Retourorder maken
Het retourorderproces begint wanneer een klant contact opneemt met uw organisatie om keren een gebrekkig of ongewenst product te retourneren en/of daarvoor te worden gecrediteerd. Nadat uw organisatie de retour heeft geaccepteerd, wordt deze wordt vastgelegd in een retourorder. Deze retourorder wordt de focus van de interne verwerking van het geretourneerde product. In de volgende afbeelding ziet u de procedure voor het maken van een retourorder.  

[![Procedure voor het maken van een retourorder](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Een retourorderkoptekst maken.

Wanneer u een retourorder maakt, moeten de gegevens uit de volgende tabel worden opgenomen.

| Veld              | Omschrijving                                              | Opmerkingen                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klantrekening   | Een verwijzing naar de tabel Klanten                       | U moet een bestaande klantaccount opgeven.                                                                                                                                                                                                                                                                                                  |
| Afleveradres   | Het adres waarnaar het artikel wordt geretourneerd.                 | Standaard wordt het adres van de organisatie gebruikt. Als een bepaald magazijn is geselecteerd in de koptekst, wordt het afleveradres gewijzigd in het afleveradres van het magazijn. U kunt dit adres wijzigen op de pagina **Retourorderdetails**.                                                                                                  |
| Locatie/magazijn     | De locatie of het magazijn waar het geretourneerde product aankomt | Het afleveradres voor de retourorder wordt bepaald op basis van het afleveradres van de locatie of het magazijn.                                                                                                                                                                                                                                 |
| RMA-nummer         | De ID die is toegewezen aan de retourorder              | Het RMA-nummer wordt gebruikt als een alternatieve sleutel in het retourorderproces. Het RMA-nummer dat wordt toegewezen, is gebaseerd op de RMA-nummerreeks die is ingesteld op de pagina **Parameters van module Klanten**.                                                                                                                              |
| Uiterste datum           | De laatste datum waarop een artikel kan worden geretourneerd.               | De standaardwaarde wordt berekend als de huidige datum plus de geldigheidsperiode. Als bijvoorbeeld een retour geldig is voor 90 dagen vanaf de datum waarop de retourorder wordt gemaakt, en de retourorder is gemaakt op 1 mei, is de waarde in het veld **30 juli**. De geldigheidsperiode wordt ingesteld op de pagina **Parameters van module Klanten**. |
| Redencode retour | De reden van de klant voor het retourneren van het product          | De redencode wordt geselecteerd in de lijst met door de gebruiker gedefinieerde redencodes. U kunt dit veld op elk gewenst moment bijwerken.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Retourorderregels maken

Nadat u de retourorderkoptekst hebt voltooid, kunt u retourregels kunt maken met een van de volgende methoden:

-   U voert handmatig de artikelgegevens, hoeveelheden en overige gegevens voor elke retourregel in.
-   U maakt een retourregel met behulp van de functie **Verkooporder zoeken**. Het wordt aangeraden om deze functie te gebruiken wanneer u een retourorder maakt. De functie **Verkooporder zoeken** maakt een verwijzing van de retourregel naar de regel in de gefactureerde verkooporder en haalt regelgegevens op uit de verkoopregel, zoals de waarden voor artikelnummer, hoeveelheid, prijs, korting en kosten. De verwijzing zorgt ervoor dat, als het product wordt geretourneerd naar het bedrijf, het wordt gewaardeerd tegen dezelfde kostprijs waarvoor het werd verkocht. De verwijzing valideert ook dat geen retourorder worden gemaakt voor een hoeveelheid die groter is dan de hoeveelheid die op de factuur is verkocht.

>[Opmerking!] Retourregels die naar een verkooporder verwijzen, worden verwerkt als correcties of omkering van de verkoop. Zie voor meer informatie de sectie 'Boeken naar het grootboek' verderop in dit onderwerp.

### <a name="charges"></a>Toeslagen

Kosten en toeslagen kunnen worden toegevoegd aan de retourorder met een of meer van de volgende methoden:

-   U kunt toeslagen handmatig toevoegen aan de koptekst van retourorder, de retourorderregel of aan beide.
-   Toeslagen kunnen automatisch worden toegevoegd aan de koptekst van de retourorder als een functie van de retourredencode.
-   Toeslagen kunnen automatisch worden toegevoegd aan de retourorderregel, op basis van de beschikkingscode van die regel.

Toeslagen worden automatisch toegevoegd nadat een retourredencode of beschikkingscode is toegewezen aan de regel. Als de redencode later wordt gewijzigd, wordt de bestaande vermelding voor de toeslag niet verwijderd, maar een nieuwe post voor toeslagen kan worden toegevoegd op basis van de nieuwe redencode. Als u toeslagen aan retourorderregels toevoegt, worden toeslagen die zijn berekend als een percentage van de waarde van de regel of order negatief wanneer de regel of regelorder negatief is, tenzij het percentage ook een negatief getal is. Een toeslag met een negatieve waarde betekent dat de klant wordt gecrediteerd.

### <a name="return-reason-codes"></a>Redencodes retour

U kunt redencodes op retouren toepassen, zodat u gemakkelijker patronen in de retouren kunt analyseren. Redencodes bevatten informatie over de reden waarom een klant artikelen wil retourneren. Sommige organisaties hebben veel redencodes. De organisatie kan de redencodes samenvoegen in redencodegroepen, om een beter overzicht te krijgen en om cumulatieve rapporten te kunnen maken.

### <a name="disposition-codes-and-disposition-actions"></a>Beschikkingscodes en beschikkingsacties

Een belangrijke stap in het retourorderproces is het toewijzen van een beschikkingscode aan de retourorderregel als onderdeel van de aankomstregistratie. De beschikkingscode bepaalt de volgende gegevens:

-   **De financiële implicaties:** Moet de klant worden gecrediteerd voor de geretourneerde artikelen en moeten eventuele toeslagen worden toegevoegd aan de retourorderregel?
-   **De beschikking voor het geretourneerde artikel:** Moet het artikel worden toegevoegd aan de voorraad, moet het worden geboekt als uitval of moet het aan de klant worden geretourneerd?
-   **De logistiek van het geretourneerde artikel:** Moet een vervangend artikel naar de klant worden gezonden?

Niet alleen kunt u met beschikkingscodes bepalen wat met de geretourneerde goederen gebeurt, ook kunt u er toeslagen met laten toepassen op de retourregel. U kunt ze ook gebruiken om retouren te groeperen voor statistische analyses. Beschikkingscodes worden gedefinieerd bij de configuratie van retourorders. Elke beschikkingscode moet echter verwijzen naar een van de ingebouwde beschikkingsacties. De volgende tabel geeft een overzicht van de beschikkingcodes en hun acties. **Belangrijk:** Als een artikel niet wordt geretourneerd maar de klant nog steeds moet worden gecrediteerd, wijst u de beschikkingscode **alleen krediet** toe aan de retourregel.

<table>
<thead>
<tr class="header">
<th>Beschikkingscode</th>
<th>Financiële implicaties</th>
<th>Implicaties voor logistiek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alleen credit</td>
<td><ul>
<li>De klant krijgt de verkoopprijs minus eventuele kosten of toeslagen gecrediteerd.</li>
<li>Verlies door uitval van het artikel wordt in het grootboek geboekt.</li>
</ul></td>
<td>Het artikel hoeft niet te worden geretourneerd. Deze beschikkingsactie wordt in de volgende gevallen gebruikt:
<ul>
<li>Er bestaat een goede vertrouwensrelatie tussen de partijen.</li>
<li>De kosten voor retourneren van het gebrekkige artikel retourneert zijn te hoog.</li>
<li>De artikelen mogen niet worden teruggebracht in de voorraad. Vanwege andere omstandigheden is een fysieke retour niet vereist.</li>
</ul></td>
</tr>
<tr class="even">
<td>Krediet</td>
<td><ul>
<li>De klant krijgt de verkoopprijs minus eventuele kosten of toeslagen gecrediteerd.</li>
<li>De voorraadwaarde wordt verhoogd met de kosten van het geretourneerde artikel.</li>
</ul></td>
<td>Het item wordt geretourneerd en in de voorraad teruggebracht.</td>
</tr>
<tr class="odd">
<td>Vervangen en crediteren</td>
<td><ul>
<li>De klant krijgt de verkoopprijs minus eventuele kosten of toeslagen gecrediteerd.</li>
<li>De voorraadwaarde wordt verhoogd met de kosten van het geretourneerde artikel.</li>
<li>Een aparte verkooporder voor een vervanging wordt gemaakt en afzonderlijk verwerkt.</li>
</ul></td>
<td>Het item wordt geretourneerd en in de voorraad teruggebracht.</td>
</tr>
<tr class="even">
<td>Vervangen en uitvallen</td>
<td><ul>
<li>De klant krijgt de verkoopprijs minus eventuele kosten of toeslagen gecrediteerd.</li>
<li>Verlies door uitval van het artikel wordt in het grootboek geboekt.</li>
<li>Een aparte verkooporder voor een vervanging wordt gemaakt en afzonderlijk verwerkt.</li>
</ul></td>
<td>Het artikel is geretourneerd en geboekt als uitval.</td>
</tr>
<tr class="odd">
<td>Retour naar klant</td>
<td>Geen, met uitzondering van eventuele kosten of toeslagen.</td>
<td>Het artikel wordt wordt geretourneerd maar wordt na inspectie teruggestuurd naar de klant. Deze beschikkingsactie kan worden gebruikt als het artikel met opzet is beschadigd is of als de garantie is vervallen.</td>
</tr>
<tr class="even">
<td>Uitval</td>
<td><ul>
<li>De klant krijgt de verkoopprijs minus eventuele kosten of toeslagen gecrediteerd.</li>
<li>Verlies door uitval van het artikel wordt in het grootboek geboekt.</li>
</ul></td>
<td>Het artikel wordt geretourneerd of geboekt als uitval.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Aankomst in magazijn voor inspectie
Voordat u geretourneerde artikelen fysiek weer aan de voorraad kunt toevoegen via het boeken van een pakbon, moeten de artikelen aankomstregistratie en een optionele inspectie doorlopen. In de volgende afbeelding ziet u een overzicht van het ontvangstproces. De daaropvolgende secties beschrijven elke stap die in de afbeelding is afgebeeld.  

[![Ontvangstproces](./media/salesreturn03.png)](./media/salesreturn03.png)  

Het proces bevat verschillende andere varianten die niet in dit onderwerp worden behandeld. Dit zijn enkele van deze variaties:

-   U maakt niet gebruik van de lijst **Overzicht aankomst** om een ontvangstjournaal te maken. In plaats daarvan maakt u het ontvangstjournaal handmatig aan. Retourorders krijgen **Verkooporder** als verwijzing.
-   Als u Magazijnbeheer gebruikt, genereert u pallettransporten. De retourregel krijgt de status **aangekomen** tijdens het pallettransport.
-   U registreert de aankomst van het geretourneerde artikel rechtstreeks vanuit de retourorderregel met behulp van de functie **Registratie**.

Tijdens het ontvangstproces worden retouren geïntegreerd met het algemene proces voor magazijnontvangsten. Het ontvangstproces ondersteunt ook het maken van quarantaineorders voor geretourneerde artikelen die afzonderlijk moeten worden geïnspecteerd.

### <a name="identify-products-in-the-arrival-overview-list"></a>Producten identificeren in de lijst Overzicht aankomst

De pagina **Overzicht aankomst** biedt een overzicht van alle geplande inkomende ontvangsten. 
>[Opmerking!] Aankomsten van retourorders moeten afzonderlijk van andere soorten aankomsttransacties worden verwerkt. Nadat u hebt een binnenkomend pakket hebt aangegeven op de pagina **Overzicht aankomst** (bijvoorbeeld met behulp van het begeleidende RMA-document), klikt u in het actievenster op **Begin aankomst** en maakt en initialiseert u een ontvangstjournaal dat overeenkomt met de aankomst.

### <a name="edit-the-arrival-journal"></a>Het aankomstjournaal bewerken.

Als u de optie **Quarantainebeheer** instelt op **Ja**, makt u een quarantaineorder voor de retourregel. Als een regel naar de quarantaine is verzonden voor inspectie, kunt u geen beschikkingscode opgeven. 
 
Als u de optie **Quarantainebeheer** instelt op **Ja** in de voorraadmodelgroep van het artikel, wordt de optie **Quarantainebeheer** op de pagina **Journaalregels** voor de ontvangstjournaalregel gemarkeerd. Deze kan niet worden gewijzigd. Als de regel naar quarantaine wordt verzonden, moet u het bijbehorende quarantainemagazijn opgeven. 

Als de aankomstregel niet wordt verzonden voor inspectie, moet de ontvangstmedewerker van het magazijn de beschikkingscode rechtstreeks op de ontvangstjournaalregel opgeven en vervolgens het ontvangstjournaal boeken. Als dezelfde beschikkingscode niet moet worden toegewezen aan de volledige hoeveelheid van de retourregel of als de volledige hoeveelheid van de regel niet is ontvangen, moet u de regel splitsen. Wanneer u een ontvangstjournaalregel splitst, moet u ook de retourregel splitsen (**SalesLine**) en maakt u een nieuwe partij-ID. U kunt de regel splitsen door de hoeveelheid van de ontvangstjournaalregel te verlagen. Wanneer het journaal wordt geboekt, wordt een nieuwe retourregel gemaakt met de status **Verwacht** voor de resterende hoeveelheid. U kunt de regel ook splitsen door te klikken op **Functies** &gt; **Splitsen**.

### <a name="process-the-quarantine-order"></a>De quarantaineorder verwerken

Als de geretourneerde producten voor inspectie in het quarantainemagazijn worden verzonden, wordt geen extra verwerking uitgevoerd in een quarantaineorder. Eén quarantaineorder wordt gemaakt voor elke aankomstregel die naar het quarantainemagazijn is verzonden. De beschikkingscode geeft het resultaat van het inspectieproces aan. 

U kunt een quarantaineorder opsplitsen, net zoals u het ontvangstjournaal splitst. Als u de quarantainecode splitst, wordt de retourregel op dezelfde wijze gesplitst. Nadat de beschikkingscode is ingevoerd, rondt u de quarantaineorder af met behulp van de functie **Beëindigen** of de functie **Gereedmelden**. Als u **Gereedmelden** selecteert, wordt een nieuwe ontvangst aangemaakt in het aangewezen magazijn. U kunt vervolgens deze aankomst verwerken op de pagina **Overzicht aankomst**. 

Als de aankomst afkomstig is uit een quarantaineorder is, kunt u de beschikkingscode die is toegewezen tijdens de inspectie niet wijzigen. Als u de quarantaineorder met behulp van de functie **Beëindigen** afrondt, wordt de partij automatisch geregistreerd. Soms wordt een artikel van het quarantainemagazijn teruggestuurd naar de afdeling Verzending en ontvangst. De quarantaine-inspecteur weet bijvoorbeeld niet waar het artikel in de voorraad moet worden opgeslagen. In dit geval moet de bijbehorende pakbon worden bijgewerkt om de beschikkingscode juist te registreren en op te volgen, die is opgegeven als gevolg van de quarantaine. 

Een ontvangstbevestiging kan naar de klant worden verzonden wanneer de retourregel is geregistreerd. Het rapport **Retourbevestiging** lijkt op het retourorderdocument. Het rapport **Retourbevestiging** wordt niet gejournaliseerd of op andere wijze in het systeem geregistreerd en het is geen vereiste stap in het retourorderproces.

## <a name="replace-a-product"></a>Een product vervangen
Er zijn twee methoden voor het beheer van vervangende producten:

-   **Vervanging bij aanvang:** Een product vervangen voordat het geretourneerde product van de klant is ontvangen.
-   **Vervanging door beschikkingscode:** Automatisch een nieuwe vervangingsorderregel maken.

### <a name="up-front-replacement"></a>Vervanging bij aanvang

Bij vervanging bij aanvang (¨vervanging van tevoren¨) kan het vervangende artikel worden geleverd aan de klant voordat het artikel is geretourneerd. Deze methode is nuttig als het artikel is bijvoorbeeld een machineonderdeel is dat niet kan worden verwijderd tenzij een reserveonderdeel beschikbaar is om het te vervangen, of als u gewoon wilt dat uw klant het vervangende product zo snel mogelijk heeft. De order van het type Vervanging bij aanvang is een onafhankelijke verkooporder. De koptekstgegeven worden geïnitialiseerd vanuit de klant en de regelgegevens worden geïnitialiseerd vanuit de retourorder. U kunt de vervangingsorder onafhankelijk van de retourorder bewerken, verwerken en verwijderen. Wanneer u een vervangingsorder verwijdert, ontvangt u een bericht dat de order is aangemaakt als een vervangingsorder. In de volgende afbeelding ziet u het proces voor vervanging bij aanvang.  

![Het proces Vervanging bij aanvang](./media/SalesReturn04.png)

De retourorder bevat een verwijzing naar de vervangingsorder. Als een vervangingsorder van het type Vervanging bij aanvang wordt gemaakt voor een retourorder voordat het gebrekkige artikel is geretourneerd, kunt u geen beschikkingscodes voor vervanging selecteren nadat het beschadigde artikel is ontvangen.

### <a name="replacement-by-disposition-code"></a>Vervanging door beschikkingscode

Als u een vervangend artikel naar de klant verzendt en op de retourorder gebruik maakt van de beschikkingsacties **Vervangen en uitvallen** of **Vervangen en crediteren**, gebruikt u het proces dat wordt weergegeven in de volgende afbeelding.  

![Vervangingsproces bij gebruik van een beschikkingscode](./media/SalesReturn05.png)

Het vervangende artikel wordt geleverd door middel van een onafhankelijke verkooporder, de vervangende verkooporder. Deze verkooporder wordt gemaakt wanneer de pakbon voor de retourorder wordt gegenereerd. De orderkoptekst gebruikt gegevens van de klant, waarnaar wordt verwezen in de retourorderkoptekst. De regelgegevens worden verzameld van de informatie die is ingevoerd op de pagina **Vervangingsartikel**. De pagina **Vervangingsartikel** moet worden ingevuld voor regels met beschikkingsacties die beginnen met het woord 'vervangen'. Zowel de hoeveelheid als de identiteit van het vervangingsartikel worden echter niet gevalideerd of beperkt. Dankzij dit gedrag kan de klant hetzelfde artikel toegezonden krijgen maar in een andere configuratie of maat, of zelfs een geheel ander artikel. Standaard wordt een identiek artikel ingevoerd op de pagina **Vervangingsartikel**. U kunt echter een ander item selecteren op voorwaarde dat de functie is geconfigureerd. 

>[Opmerking!] U kunt de vervangende verkooporder bewerken en verwijderen nadat deze is gemaakt.

## <a name="generate-a-packing-slip"></a>Een pakbon genereren
Voordat geretourneerde artikelen weer in de voorraad kunnen worden opgenomen, moet u de pakbon bijwerken voor de order waartoe deze artikelen behoren. Net zoals u met het factuurbijwerkproces de financiële transactie bijwerkt, werkt u met het pakbonbijwerkproces fysiek de voorraadrecord bij. Dit betekent dat u met dit proces wijzigingen in de voorraad doorvoert. In het geval van geretourneerde artikelen worden de stappen die zijn toegewezen aan de beschikkingsactie, geïmplementeerd tijdens het bijwerken van de pakbon. Wanneer u de pakbon genereert, vinden de volgende gebeurtenissen plaats:

-   In het magazijn wordt het standaardproces voor het uitvoeren van een fysieke ontvangst gebruikt. Boekingen in grootboek worden gegenereerd als de voorraadmodelgroep (**Fysieke voorraad boeken**) en de parameters van de module Klanten (**Pakbon in grootboek boeken**) correct zijn ingesteld.
-   Artikelen die zijn gemarkeerd met een beschikkingsactie met het woord 'uitval' worden geboekt als uitval en het voorraadverlies wordt geboekt naar het grootboek.
-   Artikelen die zijn gemarkeerd met de beschikkingsactie **Retour naar klant** worden ontvangen en aan de klant geleverd. Deze artikelen hebben geen netto-invloed op voorraad.
-   Een vervangende verkooporder wordt gemaakt. Deze verkooporder is gebaseerd op informatie op de pagina **Vervangingsartikel**.

U kunt de pakbon alleen genereren voor regels met de retourstatus **Geregistreerd** en alleen voor de volledige hoeveelheid op de retourregel. Als meerdere regels op de retourorder de status **Geregistreerd** hebben, kunt u de pakbon voor een subset van de regels genereren door de andere regels te verwijderen van de pagina **Pakbon boeken**. 

Gedeeltelijke retouren worden gedefinieerd in termen van retourorderregels en niet in termen van retourorderleveringen. Wanneer u dus de volledige hoeveelheid ontvangt die is aangegeven op één retourorderregel, maar niets van de andere regels in de retourorder, de levering geen gedeeltelijke levering is. Als echter voor een retourorderregel bijvoorbeeld tien eenheden van een artikel moeten worden geretourneerd en u er maar vier ontvangt, is dit een gedeeltelijke levering. Als niet alle verwachte retourartikelen zijn ontvangen, kunt u de verzending apart zetten en wachten totdat de rest van de geretourneerde hoeveelheid aankomt. U kunt echter ook de gedeeltelijke hoeveelheid registreren en boeken. Als onderdeel van het boekingsproces voor pakbonnen kunt u het referentienummer van de pakbon uit de verzenddocumenten van de klant koppelen aan de orderregels. Deze koppeling is optioneel en dient alleen ter informatie. Er worden geen transacties bijgewerkt. 

In het algemeen kunt u de pakbonproces overslaan en direct doorgaan naar de facturering. In dit geval worden de stappen die u zou uitvoeren tijdens het genereren van de pakbon, uitgevoerd tijdens het factureren.

## <a name="generate-an-invoice"></a>Een factuur genereren
Alhoewel de pagina **Retourorder** de informatie en acties bevat die nodig zijn om de speciale logistieke aspecten van de retourorder te kunnen verwerken, moet u de pagina **Verkooporder** gebruiken om het factureringsproces af te ronden. Uw organisatie kan dan desgewenst het retourorders en verkooporders tegelijkertijd factureren en dezelfde persoon kan het factureringsproces uitvoeren. Om de retourorder vanuit de pagina **Verkooporder** weer te geven, klikt u op de koppeling voor het verkoopordernummer om de bijbehorende verkooporder te openen. U vindt de retourorder ook op de pagina **Alle verkooporders**. Retourorders zijn verkooporders met het ordertype **Geretourneerde order**.

### <a name="credit-correction"></a>Creditcorrectie

Als onderdeel van het factureringsproces moet u controleren of diverse toeslagen correct zijn. Als u wilt dat de boekingen in grootboek correcties worden (storno), kunt u overwegen de optie **Creditcorrectie** op het tabblad **Andere** van de pagina **Factuur wordt geboekt** te gebruiken, wanneer u de factuur/creditnota boekt. 
>[Opmerking!] Standaard wordt de optie **Creditcorrectie** ingeschakeld als de optie **Creditnota als correctie** op de pagina **Parameters van module Klanten** is ingeschakeld. Het wordt echter afgeraden om retouren te boeken met storno.

## <a name="create-intercompany-return-orders"></a>Intercompany-retourorders maken
Retourorders kunnen worden uitgevoerd tussen twee bedrijven binnen uw organisatie. De volgende scenario's worden ondersteund:

-   Eenvoudige intercompany-retouren tussen twee bedrijven die deel uitmaken van een intercompany-relatie
-   Een intercompany-keten die wordt opgezet wanneer een klantretourorder wordt gemaakt in het verkopende bedrijf
-   Een intercompany-keten die wordt vastgesteld wanneer een retourorder voor de klant wordt gemaakt in het verkopende bedrijf
-   Retouren bij zendingen met directe levering tussen een externe klant en twee bedrijven die deel uitmaken van een intercompany-relatie

### <a name="setup"></a>Instellen

In de volgende afbeelding ziet u de minimale configuratie die is vereist voor twee bedrijven die deelnemen aan een intercompany-relatie en profiteren van de intercompany-handel.  

![Minimale instellingen](./media/SalesReturn06.png)

In het volgende scenario is CompBuy het inkopende bedrijf en CompSell de verkopende partij. Meestal verzendt het verkopende bedrijf goederen naar het inkopende bedrijf of, bij directe leveringen, rechtstreeks naar de eindklant. In CompBuy, de leverancier IC\_CompSell is gedefinieerd als een intercompany-eindpunt dat is gekoppeld aan het bedrijf CompSell. Tegelijkertijd is in CompSell de klant IC\_CompBuy is gedefinieerd als een intercompany-eindpunt dat is gekoppeld aan het bedrijf CompBuy. De juiste gegevens en waardetoewijzingen voor actiebeleid moeten zijn gedefinieerd in beide bedrijven. In een scenario met directe leveringen wordt een intercompany-retourorder, die ook een intercompany-verkooporder is, aangemaakt in het verkopende bedrijf. Het RMA-nummer van de intercompany-retourorder kan worden gekozen uit de RMA-nummerreeks in CompSell of deze kan worden gekopieerd van het RMA-nummer dat is toegewezen aan de oorspronkelijke retourorder in CompBuy. De RMA-nummer-instellingen op het actiebeleid **PurchaseRequisition** in CompBuy bepalen deze acties. Als het RMA-nummer wordt gesynchroniseerd, moet u maatregelen nemen om het risico van nummerconflicten te vermijden als de twee bedrijven dezelfde nummerreeks gebruiken.

### <a name="simple-intercompany-returns"></a>Eenvoudige intercompany-retouren

Dit scenario omvat twee bedrijven in dezelfde organisatie, zoals te zien in de volgende afbeelding.  

![Eenvoudige intercompany-retouren](./media/SalesReturn07.png)

De orderketen kan worden opgesteld wanneer een leverancierretourorder wordt gemaakt in het inkopende bedrijf of een klantretourorder wordt gemaakt in het verkopende bedrijf. In Finance and Operations wordt de bijbehorende order gemaakt in het andere bedrijf. Er wordt voor gezorgd dat de koptekst en regelgegevens voor de leverancierretourorder overeenkomen met de instellingen op de klantretourorder. De retourorder die is opgesteld kan de verwijzing (**Verkooporder zoeken**) naar een bestaande klantfactuur bevatten of juist niet. De pakbonnen en facturen van de twee orders kunnen afzonderlijk worden verwerkt. U hoeft bijvoorbeeld geen pakbon te genereren voor de leverancierretourorder voordat u de pakbon voor de klantretourorder genereert.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Retouren bij zendingen met directe levering tussen drie partijen

Dit scenario kan worden opgesteld als een vorige verkoop van het type **Directe levering** is voltooid en als een factuur voor de klant bestaat in het bedrijf dat het contact met de klant afhandelt. In de onderstaande afbeelding heeft het bedrijf CompBuy eerder producten verkocht aan de klant Extern en deze gefactureerd. De producten zijn rechtstreeks vanuit het bedrijf CompSell verzonden naar de klant via een intercompany-orderketen.  

![Retouren bij zendingen met directe levering tussen drie partijen](./media/SalesReturn08.png)

Als de klant Extern de producten wil retourneren, wordt een retourorder (RMA02) gemaakt voor de klant in het bedrijf CompBuy. Om de intercompany-keten op te stellen, moet de retourorder worden gemarkeerd voor directe levering. Als u werkt met de functie **Verkooporder zoeken** voor het verzamelen van de klantfactuur die moet worden geretourneerd, wordt een intercompany-orderketen opgesteld die uit de volgende documenten bestaat:

-   **Oorspronkelijke retourorder:** RMA02 (bedrijf CompBuy)
-   **Inkooporder:** PO02 (bedrijf CompBuy)
-   **Intercompany-retourorder:** RMA\_00032 (bedrijf CompSell)

Nadat de intercompany-keten voor directe levering is aangemaakt, moet alle fysieke afhandeling en verwerking van de geretourneerde artikelen plaatsvinden in de context van de intercompany-retourorder RMA\_00032 in het bedrijf CompSell. De producten kunnen niet worden ontvangen in het bedrijf CompBuy. Wanneer een beschikkingscode wordt toegewezen aan de intercompany-retourorder, wordt deze gesynchroniseerd met de oorspronkelijke retourorder zodat de oorspronkelijke order correct kan worden gefactureerd.

## <a name="post-to-the-ledger"></a>Boeken naar het grootboek
De grootboekboekingen die worden gegenereerd wanneer de retourorder wordt gefactureerd, worden beïnvloed door enkele belangrijke instellingen en parameters:

-   **Kostprijs retour:** Voor andere voorraadmodellen dan **Standaardkosten** bepaalt de parameter **Kostprijs retour** de kosten van het artikel wanneer dit wordt geaccepteerd in de voorraad of als uitval wordt geboekt. Om de voorraadwaarde correct te kunnen berekenen, is het belangrijk dat u de parameter **Kostprijs retour** correct instelt. Als u met de functie **Verkooporder zoeken** een retourorderregel maakt die een verwijzing naar een klantfactuur bevat, is de waarde van **Kostprijs retour** gelijk aan de kostprijs van het artikel dat is verkocht. Anders wordt de kostprijswaarde opgehaald uit de artikelinstellingen of handmatig ingevoerd.
-   **Creditcorrectie/Storno:** De parameter **Creditcorrectie** op de pagina **Ractuur wordt geboekt** bepaalt of boekingen worden opgenomen als positieve (Debet/Credit) posten of corrigerende, negatieve posten.

In de volgende voorbeelden wordt de retourkostprijs vertegenwoordigd door **Voorraadkostprijs**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Voorbeeld 1: De retourorder verwijst niet naar een klantfactuur

De retourorder verwijst niet naar een klantfactuur. Het geretourneerde artikel wordt gecrediteerd. De parameter **Creditcorrectie** is niet geselecteerd wanneer de retourorderfactuur of creditnota wordt gegenereerd.  

![De retourorder verwijst niet naar een klantfactuur.](./media/SalesReturn09.png)  

>[Opmerking!] De hoofdrecordprijs wordt gebruikt als de standaardwaarde voor de parameter **Retourkostprijs**. De standaardprijs wijkt af van de kostprijs op het moment van voorraaduitgifte. Daarom is de implicatie dat een verlies van 3 is gemaakt. De retourorder omvat bovendien niet de korting die op de verkooporder aan de klant is gegeven. Daarom wordt een te hoge creditering uitgevoerd.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Voorbeeld 2: Creditcorrectie is ingeschakeld voor de retourorder

Voorbeeld 2 is hetzelfde als voorbeeld 1, maar de parameter **Creditcorrectie** wordt geselecteerd wanneer de retourorderfactuur wordt gegenereerd.  

![Retourorder waarbij creditcorrectie is ingeschakeld ](./media/SalesReturn10.png)  

>[Opmerking!] De grootboekboekingen worden ingevoerd als negatieve correcties.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Voorbeeld 3: De retourorderregel wordt gemaakt door middel van de functie Verkooporder zoeken

In dit voorbeeld wordt de retourorderregel gemaakt door middel van de functie **Verkooporder zoeken**. De parameter **Creditcorrectie** is niet geselecteerd wanneer de factuur wordt gemaakt.  

![Een retourorderregel die is gemaakt door middel van de functie Verkooporder zoeken ](./media/SalesReturn11.png)  

>[Opmerking!] **Korting** en **Kostprijs retour** zijn correct ingesteld. Daarom wordt precies het bedrag van de klantfactuur teruggeboekt.




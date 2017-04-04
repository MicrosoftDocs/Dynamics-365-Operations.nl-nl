---
title: Verkoopretouren
description: Dit onderwerp biedt informatie over het proces voor retourorders. Deze bevat informatie over retouren van klanten en hun effect op het kostenblad en de voorhanden voorraadhoeveelheden.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Verkoopretouren

Dit onderwerp biedt informatie over het proces voor retourorders. Deze bevat informatie over retouren van klanten en hun effect op het kostenblad en de voorhanden voorraadhoeveelheden.

Klanten kunnen artikelen retourneren om verschillende redenen. Bijvoorbeeld een artikel beschadigd zijn of het voldoet niet aan de verwachtingen van de klant. Het retourproces begint wanneer een klant heeft verzocht een artikel te retourneren. Nadat het verzoek van de klant is ontvangen, moet een retourorder wordt gemaakt in Microsoft Dynamics 365 voor bewerkingen.

## <a name="return-order-process"></a>Retourorderproces
De volgende afbeelding geeft een overzicht van het retourorderproces.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Er zijn twee typen van retourorderproces: fysieke retourneren en alleen creditnota.

-   **Fysieke opbrengst** : de retourorder autoriseert producten fysiek worden geretourneerd.
-   **Alleen credit** : de retourorder autoriseert van een klantkrediet maar niet vereist dat de klant de producten zijn fysiek geretourneerd.

### <a name="physical-return-order-process"></a>Fysieke retourorderproces

1.  **Een retourorder maken.** De vergunning voor de klant om terug te keren defect of ongewenste producten formeel document. De retourorder nodig niet dat het bedrijf de geretourneerde producten accepteren of een creditnota voor de klant bevatten. Als de retour wordt geaccepteerd, kunt u een vervangend artikel moet worden verzonden voordat het beschadigde artikel is geretourneerd autoriseren.
2.  **Magazijn voor inspectie aankomt.** Voer een initiële inspectie en de validatie op basis van het retourorderdocument. De retourorder ondersteunt ook quarantaine van de geretourneerde artikelen voor aanvullende inspectie en kwaliteitscontrole.
3.  **Beschikking bepalen.** Het inspectieproces is voltooid en bepalen wat er moet gebeuren met de geretourneerde producten. Bepalen of u de klant crediteren, afwijzen van de productretour of worden geaccepteerd product, uitvallen van het product en vervolgens naar de klant een vervangend product verzendt als onderdeel van deze stap.
4.  **Een pakbon genereren.** Genereren van een pakbon en de beschikking beslissing die u in stap 3 vast te leggen. De processen logistiek voltooien.
5.  **Een factuur genereren.** Sluit de retourorder.

### <a name="credit-only-process"></a>Credit alleen verwerken

1.  **Een retourorder maken.** Formeel document voor de vergunning voor de klant voor creditering van zonder dat u de defecte of ongewenste producten terugkeert. De **alleen Credit** beschikkingscode autoriseert de beslissing voor creditering van de klant zonder fysiek worden geretourneerd.
2.  **Een factuur genereren.** Genereren van de creditnota en sluit vervolgens de retourorder.

## <a name="return-material-authorization"></a>Materiaal authorization retourneren
Return Material Authorization (RMA)-verwerking is gebaseerd op verkooporder-functionaliteit. Een RMA wordt geregistreerd als een retourorder, dat als een verkooporder wordt gemaakt en wellicht een andere verkooporder is gekoppeld, een vervangingsorder genoemd. Verkooporders koppelen aan het oorspronkelijke RMA-nummer.

-   **Retourorder** : voor het registreren van een RMA maken van een retourorder een verkooporder met het type toegewezen is, **order geretourneerd.** Eventuele wijzigingen die u aanbrengt in het RMA-informatie wordt automatisch bijgewerkt in de verkooporder. Totdat de status van de retourorder heeft **openen**, verschijnt niet in de lijst met verkooporders. U RMA gebruiken voor het verwerken van de ontvangst en de ontvangst van geretourneerde artikelen, alsmede een credit alleen beschikkingsactie toe te staan (Zie de sectie **beschikkingscodes en beschikkingsacties**). Alle andere opvolgingsactiviteit processen moeten worden verwerkt in de verkooporder.
-   **Vervangingsorder** : wanneer een vervangingsorder moet worden verzonden naar de klant het RMA wel mogelijk om een tweede gekoppelde verkooporder. U kunt de vervangingsorder voor RMA ter ondersteuning van onmiddellijke zending handmatig maken. U kunt ook kan de vervangingsorder worden gemaakt automatisch nadat de aankomst, de inspectie en de ontvangst zijn voltooid voor het RMA-regelartikel met een beschikkingscode die vervangende aangeeft. De vervangingsorder heeft dezelfde functionaliteit die is gekoppeld aan een verkooporder. Zo kunt u het configureren van een aangepast product als het vervangingsartikel, maak een productieorder wilt herstellen van een geretourneerd artikel, een inkooporder voor directe levering voor het verzenden van de vervanging van een leverancier maken of ondersteuning voor andere doeleinden.

## <a name="create-a-return-order"></a>Retourorder maken
Het retourorderproces begint wanneer een klant contact op met uw organisatie om terug te keren een defect of ongewenste product en/of moet worden gecrediteerd. Nadat uw organisatie de retourzending heeft geaccepteerd, wordt de retour wordt beschreven door een retourorder. Deze retourorder, wordt het brandpunt van de interne verwerking van het geretourneerde product. De volgende afbeelding ziet de procedure voor het maken van een retourorder.  

[![Procedure voor het maken van de retourorder.](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Koptekst retourorder maken

Wanneer u een retourorder maakt, moet de informatie in de volgende tabel worden opgenomen.

| Veld              | Omschrijving                                              | Opmerkingen                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klantrekening   | Een verwijzing naar de tabel Klanten                       | U moet een bestaande klantrekening bevatten.                                                                                                                                                                                                                                                                                                  |
| Afleveradres   | Het adres dat aan het artikel is geretourneerd                 | Adres van de organisatie wordt standaard gebruikt. Als een bepaald magazijn is geselecteerd in de koptekst, wordt het afleveradres gewijzigd in het afleveradres van het magazijn. U kunt dit adres wijzigen in de **Retourorderdetails** pagina.                                                                                                  |
| Locatie/magazijn     | De locatie of magazijn dat het geretourneerde product ontvangt | Het afleveradres voor de retourorder wordt bepaald op basis van het afleveradres van de locatie of magazijn.                                                                                                                                                                                                                                 |
| RMA-nummer         | De ID die is toegewezen aan de retourorder              | Het RMA-nummer wordt gebruikt als een alternatieve sleutel gedurende het verwerken van de retourorder. Het RMA-nummer dat is toegewezen, is gebaseerd op het RMA-nummerreeks die is ingesteld op de **parameters van module klanten** pagina.                                                                                                                              |
| Uiterste datum           | De laatste datum waarop een artikel kan worden geretourneerd.               | De standaardwaarde wordt berekend als de huidige datum plus de geldigheidsduur. Als een retour alleen 90 dagen na de datum waarop de retourorder wordt gemaakt, en de retourorder is gemaakt op 1 mei geldig is, de waarde in het veld is bijvoorbeeld **30 juli**. De geldigheidsduur is ingesteld op de **parameters van module klanten** pagina. |
| Redencode retour | De reden van de klant voor het retourneren van het product          | De redencode die is geselecteerd in de lijst met redencodes die door de gebruiker gedefinieerde. U kunt dit veld op elk gewenst moment bijwerken.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Retourorderregels maken

Nadat u de kop hebt voltooid, kunt u retourregels kunt maken met een van de volgende methoden:

-   Handmatig de artikelgegevens, hoeveelheid en andere informatie voor elke regel invoeren.
-   Een regel maken met behulp van de **verkooporder zoeken** functie. Het is raadzaam dat u deze functie gebruiken wanneer u een retourorder maken. De **verkooporder zoeken** functie maakt een verwijzing van de retourregel naar de regel van de gefactureerde verkooporder en haalt regeldetails zoals artikelnummer, hoeveelheid, prijs, korting en kostenwaarden van de verkoopregel. De verwijzing zorgt u ervoor dat, als het product wordt geretourneerd naar het bedrijf, het heeft gewaardeerd tegen dezelfde kostprijs dat deze werd verkocht op. De verwijzing valideert die resulteren in orders zijn niet gemaakt voor een hoeveelheid die groter is dan de hoeveelheid op de factuur is verkocht.

**opmerking:** retourregels die naar een verkooporder verwijzen worden verwerkt als correcties of terugboekingen van de verkoop. Zie de sectie 'Naar het grootboek boeken' verderop in dit onderwerp voor meer informatie.

### <a name="charges"></a>Toeslagen

Tarieven en vergoedingen kunnen worden toegevoegd aan de retourorder via een of meer van de volgende methoden:

-   U kunt toeslagen handmatig toevoegen aan de koptekst retourorder en/of de retourorderregel.
-   Toeslagen kunnen automatisch worden toegevoegd aan de koptekst van de retourorder als een functie van de redencode retour.
-   Toeslagen kunnen automatisch worden toegevoegd aan de retourorderregel op basis van de beschikkingscode van de regel.

Toeslagen automatisch worden toegevoegd na een retourredencode of beschikkingscode die is toegewezen aan de regel. Als de redencode die later wordt gewijzigd, de bestaande vermelding van de toeslagen worden niet verwijderd, maar een nieuwe post voor toeslagen kan worden toegevoegd, gebaseerd op de nieuwe redencode. Als u toeslagen aan retourorderregels toevoegt, worden toeslagen die zijn berekend als een percentage van de waarde van de regel of order negatieve wanneer de regel of regel order negatief is, tenzij het percentage ook een negatief getal is. Een toeslag met een negatieve waarde staat voor een creditpost aan de klant.

### <a name="return-reason-codes"></a>Redencodes retour

U kunt redencodes voor retouren door toe te passen retour patronen gemakkelijker te analyseren. Redencodes bevatten informatie over waarom een klant wil retourneren van artikelen. Sommige organisaties hebben veel redencodes. Deze organisatie kan de redencodes in redencodegroepen om een beter overzicht te krijgen en voor het melden van samengevoegde groeperen.

### <a name="disposition-codes-and-disposition-actions"></a>Beschikkingscodes en beschikkingsacties

Een belangrijke stap bij het retourorderproces is het toewijzen van een beschikkingscode aan de retourorderregel als onderdeel van de van aankomstregistratie. De beschikkingscode bepaalt de volgende informatie:

-   **De financiële gevolgen** : moet de klant worden gecrediteerd voor de geretourneerde artikelen en moeten eventuele toeslagen worden toegevoegd aan de retourorderregel?
-   **De beschikking van het geretourneerde artikel** : moet het artikel kan worden toegevoegd naar de voorraad, moet deze worden buiten gebruik gesteld of moet deze aan de klant worden geretourneerd?
-   **De logistiek van het geretourneerde artikel** : een vervangend artikel wordt verzonden naar de klant?

Naast de om te bepalen hoe de geretourneerde goederen zijn afgestoten, beschikkingscodes kunnen leiden tot toeslagen moet worden toegepast op de regel. Ze kunnen ook gebruikt om te groeperen van retouren voor statistische analyses. Beschikkingscodes worden gedefinieerd als onderdeel van de instellingen van retourorders. Echter elke beschikkingscode moet verwijzen naar een van de ingebouwde beschikkingsacties. De volgende tabel worden de ingebouwde beschikkingscodes en de bijbehorende acties. **Belangrijk:** toewijzen als een artikel niet moet worden geretourneerd, maar de klant nog steeds moet worden gecrediteerd, de **alleen Credit** beschikkingscode die aan de retourregels.

<table>
<thead>
<tr class="header">
<th>Beschikkingscode</th>
<th>Financiële gevolgen</th>
<th>Implicaties voor de logistiek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alleen credit</td>
<td><ul>
<li>De klant gecrediteerd de verkoopprijs min eventuele bijzondere kosten of toeslagen.</li>
<li>Verlies uit het vernietigen van het artikel wordt naar het grootboek geboekt.</li>
</ul></td>
<td>Het artikel moet niet worden geretourneerd. Deze beschikkingsactie wordt gebruikt voor de volgende gevallen:
<ul>
<li>Er is voldoende vertrouwensrelatie tussen de partijen.</li>
<li>De kosten van het defecte artikel retourneert is duur.</li>
<li>De artikelen kunnen niet worden toegestaan in de voorraad. Vanwege andere voorwaarden is een fysieke retour niet vereist.</li>
</ul></td>
</tr>
<tr class="even">
<td>Krediet</td>
<td><ul>
<li>De klant gecrediteerd de verkoopprijs min eventuele bijzondere kosten of toeslagen.</li>
<li>De voorraadwaarde wordt verhoogd met de kosten van het geretourneerde artikel.</li>
</ul></td>
<td>Het item wordt geretourneerd en in de voorraad wordt toegevoegd.</td>
</tr>
<tr class="odd">
<td>Vervangen en crediteren</td>
<td><ul>
<li>De klant gecrediteerd de verkoopprijs min eventuele bijzondere kosten of toeslagen.</li>
<li>Voorraadwaarde wordt verhoogd met de kosten van het geretourneerde artikel.</li>
<li>Een aparte verkooporder voor een vervanging is gemaakt en afzonderlijk te verwerken.</li>
</ul></td>
<td>Het item wordt geretourneerd en in de voorraad wordt toegevoegd.</td>
</tr>
<tr class="even">
<td>Vervangen en uitvallen</td>
<td><ul>
<li>Klant gecrediteerd, wordt de verkoopprijs, min eventuele bijzondere kosten of toeslagen.</li>
<li>Verlies uit het vernietigen van het artikel wordt naar het grootboek geboekt.</li>
<li>Een aparte verkooporder voor een vervanging is gemaakt en afzonderlijk te verwerken.</li>
</ul></td>
<td>Het artikel is geretourneerd en buiten gebruik gesteld.</td>
</tr>
<tr class="odd">
<td>Retour naar klant</td>
<td>Geen, met uitzondering van eventuele vergoedingen of heffingen.</td>
<td>Het artikel wordt wordt geretourneerd maar teruggestuurd naar de klant na inspectie. Deze actie beschikkingscode kan worden gebruikt als het artikel met opzet beschadigd is of als de garantie ongeldig is gemaakt.</td>
</tr>
<tr class="even">
<td>Uitval</td>
<td><ul>
<li>De klant gecrediteerd de verkoopprijs min eventuele bijzondere kosten of toeslagen.</li>
<li>Verlies uit het vernietigen van het artikel wordt naar het grootboek geboekt.</li>
</ul></td>
<td>Het artikel is geretourneerd of buiten gebruik gesteld.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Aankomst in het magazijn voor inspectie
Voordat u fysiek geretourneerde artikelen in de voorraad ontvangen kunt via het boeken van een pakbon, moeten de artikelen doorlopen aankomstregistratie en een optionele inspectie. De volgende afbeelding geeft een overzicht van het ontvangstproces. De volgende secties beschrijven elke stap die wordt weergegeven in de afbeelding.  

[![Ontvangstproces](./media/salesreturn03.png)](./media/salesreturn03.png)  

Het proces heeft verschillende andere varianten die in dit onderwerp worden niet gedekt. Hier volgen enkele van deze variaties:

-   Gebruik niet de **Overzicht aankomst** lijst om een ontvangstjournaal te maken. In plaats daarvan het ontvangstjournaal handmatig maken. Orders zal hebben **verkooporder** als de verwijzing.
-   Als u magazijnbeheer gebruikt, genereert u pallettransporten. De retourregel hebben de status **' aangekomen '** tijdens het pallettransport.
-   Registreer de aankomst van het geretourneerde artikel rechtstreeks vanuit de retourorderregel met behulp van de **registratie** functie.

Tijdens het ontvangstproces worden met deze eigenschap wordt geïntegreerd met het algemene proces voor het magazijn-ontvangsten. Het ontvangstproces ondersteunt ook het maken van quarantaineorders voor geretourneerde artikelen die moeten worden onderworpen aan een afzonderlijke controles.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identificatie van producten in de lijst van de Overzicht aankomst

De **Overzicht aankomst** pagina biedt een overzicht van alle geplande inkomende ontvangsten. **opmerking:** aankomsten van retourorders afzonderlijk van andere soorten aankomst transacties moeten worden verwerkt. Nadat u hebt een binnenkomend pakket aangegeven op de **Overzicht aankomst** (bijvoorbeeld met behulp van het geleidedocument RMA), pagina in het actievenster en klik op **Begin aankomst** maakt en initialiseert een ontvangstjournaal die overeenkomt met de aankomst.

### <a name="edit-the-arrival-journal"></a>Het ontvangstjournaal bewerken

Door in te stellen de **management quarantaine** optie naar **Ja**, kunt u een quarantaineorder voor de regel. Als een regel is verzonden naar het quarantainemagazijn voor inspectie, kunt u niet een beschikkingscode opgeven. **opmerking:** als u de **management quarantaine** optie naar **Ja** in de voorraadmodelgroep van het artikel, de **management quarantaine** optie op de **journaalregels** pagina voor de ontvangstjournaalregel worden gemarkeerd en kan niet worden gewijzigd. Als de regel naar het quarantainemagazijn wordt geplaatst, moet u het juiste quarantainemagazijn opgeven. Als de aankomstregel niet is verzonden voor inspectie, moet de medewerker van de aankomst magazijn de beschikkingscode die rechtstreeks op de ontvangstjournaalregel opgeven en vervolgens het ontvangstjournaal boeken. Als de beschikkingscode niet moet worden toegewezen aan de gehele hoeveelheid van de retourregel of als de volledige hoeveelheid van de regel nog niet zijn ontvangen, moet u de regel splitsen. Wanneer u een ontvangstjournaalregel splitsen, u ook de retourregel splitsen (**SalesLine**) en maak een nieuwe partij-ID. U kunt de regel door vermindering van de hoeveelheid van de ontvangstjournaalregel splitsen. Wanneer het journaal wordt geboekt, wordt een nieuwe regel gemaakt met de status van **verwachte** voor de resterende hoeveelheid. U kunt de regel ook splitsen door te klikken op **functies**&gt;**splitsen**.

### <a name="process-the-quarantine-order"></a>Verwerken van de quarantaineorder

Als de geretourneerde producten voor inspectie in het quarantainemagazijn worden verzonden, wordt er geen extra verwerkingen in een quarantaineorder voltooid. Een quarantaineorder gemaakt voor elke aankomstregel die naar het quarantainemagazijn is geplaatst. De beschikkingscode geeft het resultaat van het inspectieproces. U kunt een quarantaineorder opsplitsen.Net zoals u kunt het ontvangstjournaal splitsen. Als u de quarantainecode splitsen, zorgt u ervoor dat een bijbehorende splitsing van de retourregel. Nadat de beschikkingscode die is ingevoerd, gaat u de quarantaineorder met behulp van de **End** functie of het **gereedmelden** functie. Als u **gereedmelden**, een nieuwe ontvangst wordt gemaakt in het aangewezen warenhuis. U kunt vervolgens deze aankomst verwerken met behulp van de **Overzicht aankomst** pagina. Als de aankomst van het afkomstig uit een quarantaineorder is, kunt u de beschikkingscode die is toegewezen tijdens de inspectie niet wijzigen. Als u de quarantaineorder met behulp van uitvoeren de **End** functie, de partij wordt automatisch geregistreerd. Soms kan een artikel van het quarantainemagazijn worden teruggestuurd naar de expeditie en ontvangst van de afdeling. De quarantaine-inspecteur kan bijvoorbeeld niet weet waar het artikel in voorraad. In dit geval moet de bijbehorende pakbon worden bijgewerkt om juist te registreren en reageren op de beschikkingscode die vanwege de quarantaine is opgegeven. Bevestiging van ontvangst kan worden verzonden naar de klant wanneer de regel is geregistreerd. De **retourbevestiging** rapport lijkt op het retourorderdocument. De **retourbevestiging** rapport niet gejournaliseerd of anders in het systeem is geregistreerd en het is niet een vereiste stap in het retourorderproces.

## <a name="replace-a-product"></a>Een product vervangen
Er zijn twee methoden voor het beheer van vervangende product:

-   **Vervanging bij aanvang** : een product vervangen voordat het geretourneerde product van de klant is ontvangen.
-   **Vervanging door beschikkingscode** : automatisch maken van een nieuwe orderregel vervanging.

### <a name="up-front-replacement"></a>Vervanging bij aanvang

In vervanging bij aanvang, het vervangende artikel kan worden geleverd aan de klant voordat het artikel is geretourneerd. Deze methode is handig als het artikel is bijvoorbeeld een onderdeel van een machine die niet kan worden verwijderd tenzij u een reserveonderdeel is beschikbaar voor de plaatsvinden of als u alleen uw klant om zo snel mogelijk het vervangende product wilt. De volgorde van de vervanging bij aanvang is een onafhankelijke verkooporder. De koptekstgegevens van de klant wordt geïnitialiseerd en de regelgegevens van de retourorder wordt geïnitialiseerd. U kunt bewerken, verwerken en verwijderen van de vervangingsorder onafhankelijk van de retourorder. Wanneer u een vervangingsorder verwijdert, ontvangt u een bericht dat de order als een vervangingsorder is gemaakt. De volgende afbeelding ziet het proces voor vervanging bij aanvang.  

[![Vervanging bij aanvang proces](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

De retourorder bevat een verwijzing naar de vervangingsorder. Als een vervanging bij aanvang wordt gemaakt voor een retourorder voordat het beschadigde artikel is geretourneerd, kunt u beschikkingscodes voor vervanging niet selecteren nadat het beschadigde artikel is geretourneerd.

### <a name="replacement-by-disposition-code"></a>Vervanging door beschikkingscode

Als u een vervangend artikel naar de klant kunt verzenden en u gebruikt de **vervangen en uitvallen** of **vervangen en crediteren** beschikkingsactie van de retourorder maakt, gebruikt u het proces dat wordt weergegeven in de volgende afbeelding.  

[![Als u een beschikkingscode gebruikt-proces](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Het vervangingsartikel wordt geleverd met behulp van een onafhankelijke verkooporder, wordt de verkooporder voor vervanging. Deze verkooporder wordt gemaakt wanneer de pakbon voor de retourorder wordt gegenereerd. De koptekst van de hand van de klant waarnaar wordt verwezen in de retourorderkoptekst. De gegevens worden verzameld van de informatie die is ingevoerd op de **vervangingsartikel** pagina. De **vervangingsartikel** pagina moet worden ingevuld voor regels met beschikkingsacties die beginnen met het woord 'vervangen'. De hoeveelheid noch de identiteit van het vervangingsartikel wordt gevalideerd of echter beperkt. Dit gedrag kan voor gevallen waarin de klant wil voor hetzelfde artikel, maar in een andere configuratie of de grootte en gevallen waarin de klanten wil een ander artikel. Standaard wordt een identieke artikel ingevoerd op de **vervangingsartikel** pagina. U kunt echter een ander item selecteren op voorwaarde dat de functie is ingesteld. **opmerking:** u kunt bewerken en verwijderen van de verkooporder voor vervanging nadat deze gemaakt.

## <a name="generate-a-packing-slip"></a>Een pakbon genereren
Voordat geretourneerde artikelen in voorraad kunnen worden ontvangen, moet u de pakbon voor de order die de artikelen deel uitmaken van bijwerken. Net als het bijwerkproces van de factuur wordt het bijwerken van de financiële transactie, de pakbon bijwerken de fysieke bijwerking van de voorraadrecord. Dit proces toezegt met andere woorden, de wijzigingen in de voorraad. In het geval van geretourneerde artikelen worden de stappen die zijn toegewezen aan de beschikkingsactie, geïmplementeerd tijdens het bijwerken van de pakbon. Wanneer u de pakbon genereert, wordt de volgende gebeurtenissen plaats:

-   In het magazijn, wordt het standaardproces voor het uitvoeren van een fysieke ontvangst gebruikt. Boekingen in grootboek worden gegenereerd als de voorraad groep modelleren (**fysieke voorraad boeken**) en de parameters van module Klanten (**pakbon in grootboek boeken**) correct zijn ingesteld.
-   Artikelen die zijn gemarkeerd met een beschikkingsactie met het woord 'uitval' worden buiten gebruik gesteld en het voorraadverlies wordt geboekt naar het grootboek.
-   Artikelen die zijn gemarkeerd met de **retour naar klant** beschikkingsactie worden ontvangen en aan de klant geleverd. Deze artikelen hebben geen netto effect op voorraad.
-   De verkoop van een vervangingsorder is gemaakt. Deze verkooporder is gebaseerd op informatie in de **vervangingsartikel** pagina.

U kunt genereren dat de pakbon alleen voor regels met een status van het resultaat van **geregistreerde**, en alleen voor de volledige hoeveelheid op de regel. Als meerdere regels op de retourorder de **geregistreerde** status, kunt u de pakbon voor een subset van de regels genereren door het verwijderen van de andere regels van de **pakbon boeken** pagina. Gedeeltelijke retouren worden gedefinieerd in termen van retourorderregels en niet in de vorm van zendingen van de retourorder. Dus als u de volledige hoeveelheid ontvangt die wordt aangegeven op één retourorderregel, maar u niets van de andere regels voor de retourorder ontvangt, de levering is niet een gedeeltelijke levering. Als een retourorderregel bijvoorbeeld 10 eenheden van een artikel retourneren, maar u maar vier eenheden ontvangt, is de levering een gedeeltelijke levering. Als niet alle verwachte retourartikelen zijn ontvangen, kunt u de verzending apart worden gezet en wachten totdat de rest van de geretourneerde hoeveelheid om binnen te komen. U kunt ook registreren en boeken van de gedeeltelijke hoeveelheid. U kunt het referentienummer pakbon uit de zendingsdocumenten koppelen aan de orderregels als onderdeel van het boekingsproces voor pakbonnen. Deze koppeling is optioneel en dient alleen ter referentie. Het maakt geen transactiewijzigingen aangebracht. In het algemeen kunt u de pakbon overslaan proces van de pakbon en ga direct naar de facturering. In dit geval zijn de stappen die u zou nog uitgevoerd tijdens het genereren van de pakbon voltooid tijdens het factureren.

## <a name="generate-an-invoice"></a>Een factuur genereren
Hoewel de **retourorder** pagina bevat de informatie en de acties die nodig zijn om te kunnen verwerken van de speciale logistieke aspecten van de retourorder maakt, moet u de **verkooporder** pagina van het factureringsproces. Uw organisatie kan dan het factuurbedrag retourorders en verkooporders tegelijkertijd en het factureringsproces, zoals vereist door dezelfde persoon kunt uitvoeren. Om weer te geven van de retourorder van de **verkooporder** pagina, klikt u op de koppeling voor het verkoopordernummer voor het openen van de bijbehorende verkooporder. U kunt ook de retourorder vinden op de **alle verkooporders** pagina. Orders zijn verkooporders met een ordertype van **geretourneerde order**.

### <a name="credit-correction"></a>Creditcorrectie

Als onderdeel van het factureringsproces of diverse toeslagen juist zijn. Als u de boekingen in grootboek overgaat correcties (storneren), kunt u overwegen de **correctie creditnota** optie op de **andere** tabblad van de **factuur wordt geboekt** pagina wanneer u de factuur/creditnota boekt. **opmerking:** standaard de **correctie creditnota** -optie wordt geactiveerd als de **creditnota als correctie** optie op de **parameters van module klanten** pagina is ingeschakeld. We raden echter aan dat u niet boeken met storneren retourneert.

## <a name="create-intercompany-return-orders"></a>Intercompany-retourorders maken
Retourorders kunnen worden uitgevoerd tussen twee bedrijven binnen uw organisatie. De volgende scenario's worden ondersteund:

-   Eenvoudige intercompany-retouren tussen twee bedrijven die deel uitmaken van een intercompany-relatie
-   Een intercompany-keten die wordt vastgesteld wanneer een retourorder voor de klant wordt gemaakt in de verkopende partij
-   Een intercompany-keten die wordt vastgesteld wanneer een retourorder voor de leverancier wordt gemaakt in het inkopende bedrijf
-   Directe levering zending retourneert tussen een externe klant en twee bedrijven die deel uitmaken van een intercompany-relatie

### <a name="setup"></a>Instellen

De volgende afbeelding is de minimale instelling die is vereist voor twee bedrijven die deelnemen aan een intercompany-relatie en profiteren van de intercompany-handel.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

In het volgende scenario CompBuy is het inkopende bedrijf en CompSell is het verkoopbedrijf. Meestal verzonden het verkopende bedrijf goederen aan het inkopende bedrijf of, in directe levering zending scenario's, rechtstreeks naar de eindklant. In CompBuy, de leverancier IC\_CompSell is gedefinieerd als een intercompany-eindpunt dat is gekoppeld aan het bedrijf CompSell. Tegelijkertijd wordt in CompSell, de klant IC\_CompBuy is gedefinieerd als een intercompany-eindpunt dat is gekoppeld aan het bedrijf CompBuy. De juiste actie beleidsdetails en de waardetoewijzingen moeten worden gedefinieerd in beide bedrijven. Een intercompany-retourorder, die ook een intercompany-verkooporder, wordt in een scenario van de zending directe levering in het verkopende bedrijf gemaakt. Het RMA-nummer van de intercompany-retourorder kan worden gekozen uit de nummerreeks van RMA in CompSell of deze kan worden gekopieerd uit het RMA-nummer dat is toegewezen aan de oorspronkelijke retourorder in CompBuy. De RMA-nummer-instellingen op de **PurchaseRequisition** actiebeleid in CompBuy bepalen deze acties. Als het RMA-nummer wordt gesynchroniseerd, moet u het risico is strijdig nummer als de twee bedrijven dezelfde nummerreeks wilt.

### <a name="simple-intercompany-returns"></a>Eenvoudige intercompany-retouren

Dit scenario omvat twee bedrijven in dezelfde organisatie, zoals in de volgende afbeelding.  

[![Eenvoudige intercompany-retour](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

De orderketen kan worden gemaakt wanneer een retourorder voor de leverancier wordt gemaakt in het inkopende bedrijf of een retourorder voor de klant wordt gemaakt in de verkopende partij. Dynamics 365 voor bewerkingen wordt de bijbehorende order gemaakt in het andere bedrijf en zorgt ervoor dat de koptekst en regelgegevens voor de leverancier in retourneren volgorde komt overeen met dat de instellingen op de klant de order retourneren. De retourorder die tot stand is gebracht kunt opnemen of uitsluiten van de verwijzing (**verkooporder zoeken**) met een bestaande klantfactuur. De pakbonnen en facturen van de twee orders kunnen afzonderlijk worden verwerkt. U hoeft bijvoorbeeld te genereren van een pakbon voor de retourorder leverancier voordat u de pakbon voor de retourorder van de klant genereren.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Directe levering zending geretourneerd tussen de drie partijen

Dit scenario kan worden vastgesteld als een vorige verkoop van de **de directe leveringen** type is voltooid en als een factuur tegen de klant bestaat in het bedrijf dat werkt samen met de klant. Het bedrijf CompBuy heeft in de volgende afbeelding wordt eerder verkocht en gefactureerde producten aan de klant Extern. De producten zijn rechtstreeks van het bedrijf CompSell verzonden naar de klant via een intercompany-orderketen.  

[![Directe levering zending retourneert tussen drie partijen](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Als de klant Extern wil retourneren van de producten, een retourorder (RMA02) is gemaakt voor de klant in het bedrijf CompBuy. Om te bepalen de intercompany-keten, moet de retourorder worden gemarkeerd voor directe levering. Als u werkt met de **verkooporder zoeken** functie voor het verzamelen van de klantfactuur moet worden geretourneerd een intercompany-orderketen die uit de volgende documenten bestaat wordt vastgesteld:

-   **Oorspronkelijke retourorder:** RMA02 (CompBuy bedrijf)
-   **Inkooporder:** PO02 (CompBuy bedrijf)
-   **Intercompany-retourorder:** RMA\_00032 (bedrijf CompSell)

Nadat de intercompany-keten voor directe levering is gemaakt, alle fysieke verwerking en verwerking van de geretourneerde artikelen moeten plaatsvinden in de context van de intercompany-retourorder RMA\_00032 in het bedrijf CompSell. De producten kunnen niet worden ontvangen in het bedrijf CompBuy. Een beschikkingscode is toegewezen aan de intercompany-retourorder, wordt gesynchroniseerd met de oorspronkelijke retourorder om toe te staan voor de juiste facturering van de oorspronkelijke order.

## <a name="post-to-the-ledger"></a>Naar het grootboek boeken
De grootboekboekingen die worden gegenereerd wanneer de retourorder wordt gefactureerd, worden beïnvloed door een paar belangrijke instellingen en parameters:

-   **Kostprijs retour** : voor voorraad als model voor andere dan **standaardkosten**, wordt het **kostprijs retour** parameter bepaalt de kosten van het artikel wanneer dit wordt geaccepteerd in de voorraad of buiten gebruik gesteld. Voor het berekenen van een juiste waardering van voorraad, is het belangrijk dat u de **kostprijs retour** parameter correct. Als u de **verkooporder zoeken** functie voor het maken van een retourorderregel bevat een verwijzing naar een klantfactuur de **kostprijs retour** waarde gelijk is aan de kostprijs van het artikel dat wordt verkocht. Anders wordt de waarde van de kostprijs opgehaald uit de artikelinstellingen of kan handmatig worden ingevoerd.
-   **Correctie/storneren crediteren** : de **correctie creditnota** parameter in de **factuur wordt geboekt** pagina bepaalt of boekingen opgenomen als positieve (Debet/Credit) posten of corrigeren, negatieve posten moeten worden.

In de voorbeelden die voldoen aan de kostprijs retour wordt vertegenwoordigd door **kostprijs van het veld Factuurkorting**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Voorbeeld 1: De retourorder niet verwijzen naar een klantfactuur

De retourorder niet verwijzen naar een klantfactuur. Het geretourneerde artikel wordt gecrediteerd. De **correctie creditnota** parameter niet is geselecteerd wanneer de factuur van de retourorder of creditnota, wordt gegenereerd.  

[![Retourorder niet verwijzen naar een klant-invoic](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**opmerking:** de artikelprijs van de hoofdplanning wordt gebruikt als de standaardwaarde voor de **kostprijs retour** parameter. De standaardprijs wijkt af van de kostprijs op het moment van uitgifte uit voorraad. Daarom is de implicatie dat verlies van 3 zijn gemaakt. De retourorder omvat bovendien niet de korting die op de verkooporder naar de klant hebt opgegeven. Daarom een veel credit wordt uitgevoerd.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Voorbeeld 2: Creditcorrectie is ingeschakeld voor de retourorder

Voorbeeld 2 is hetzelfde als voorbeeld 1, maar de **correctie creditnota** parameter wordt geselecteerd wanneer de factuur voor de retourorder wordt gegenereerd.  

[![Retourorder waarbij creditcorrectie wordt geselecteerd](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**opmerking:** de grootboekboekingen worden ingevoerd als negatieve correcties.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Voorbeeld 3: De retourorderregel wordt gemaakt met de functie van de verkooporder zoeken

In dit voorbeeld de retourorderregel wordt gemaakt met behulp van de **verkooporder zoeken** functie. De **correctie creditnota** parameter niet is geselecteerd wanneer de factuur wordt gemaakt.  

[![Resultaat orderregel die is gemaakt met behulp van de verkooporder zoeken](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**opmerking:****korting** en **kostprijs retour** correct zijn ingesteld. Daarom een exacte terugboeking van de klantfactuur wordt uitgevoerd.



---
title: Magazijnverwerking van inkomende ladingen voor inkooporders
description: In dit onderwerp wordt het magazijnverwerkingsproces voor inkomende ladingen voor inkooporders beschreven.
author: omulvad
manager: tfehr
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 991da4a1056bec933698d043fe45fe4e280f555a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004822"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Magazijnverwerking van inkomende ladingen voor inkooporders

In dit onderwerp wordt het magazijnverwerkingsproces voor inkomende ladingen voor inkooporders beschreven.

Voor elke inkomende lading moet het systeem al een gerelateerde verkooporder bevatten en kan het ook een gerelateerde ladingspecificatie en/of transportplan bevatten. Zie [Bedrijfsproces: Transport plannen voor inkomende ladingen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads) voor meer informatie over het maken en beheren van inkomende ladingen.

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Overzicht: hoe inkomende ladingen worden gemaakt, geregistreerd en ontvangen

In de volgende afbeelding ziet u de gangbare stroom voor het verwerken van inkomende ladingen met inkooporderhoeveelheden wanneer deze in uw magazijn aankomen.

![Het verwerkingsproces voor inkomende ladingen](media/inbound-process.png "Het verwerkingsproces voor inkomende ladingen")

1. **De leverancier bevestigt de inkooporder.**

    Het proces begint wanneer een inkooporder wordt ingevoerd in het systeem en vervolgens aan een leverancier wordt geleverd, die de order bevestigt. De inkooporder moet bestaan voordat u een record voor een inkomende lading kunt maken. U kunt de binnenkomende lading echter ook maken als de order niet is bevestigd. Zie [Inkooprders goedkeuren en bevestigen](../procurement/purchase-order-approval-confirmation.md) voor meer informatie.

1. **Er wordt een record voor een inkomende lading gemaakt om de ontvangst en de inhoud te plannen.**

    De record voor inkomende lading vertegenwoordigt een leverancierszending met een of meer inkooporders. De lading komt naar verwachting in het magazijn aan als één fysieke transporteenheid (bijvoorbeeld een trucklading). De record met de inkomende lading wordt gebruikt voor planningsdoeleinden en laat de logistiek coördinator de voortgang van de lading van de leverancier volgen. De record wordt ook gebruikt om orderregelhoeveelheden te registreren en de voortgang te beheren via magazijnbewerkingen, zoals ontvangst en opslag. Ladingen kunnen automatisch of handmatig worden gemaakt, en worden gebaseerd op een inkooporder of een geavanceerde verzendmelding (Advanced Shipment Notice, ASN) van de leverancier. Zie [Een inkomende lading maken of wijzigen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load) voor meer informatie.

1. **De leverancier bevestigt de verzending van de lading.**

    Wanneer de leverancier de lading verzendt, bevestigt de logistiek coördinator in het ontvangende magazijn de verzending van de lading. Als het ontvangende bedrijf gebruikmaakt van de module **Transportbeheer**, worden door de bevestiging van de inkomende zending andere taakverdelingsprocessen geactiveerd die aan de binnenkomende ladingen zijn gekoppeld. Zie [Een lading voor verzending bevestigen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping) voor meer informatie.

1. **De lading arriveert in het magazijn en werknemers registreren hoeveelheden.**

    Wanneer een trucklading in het ontvangende magazijn binnenkomt, registreren de magazijnmedewerkers de laadhoeveelheden. Wanneer de module **Magazijnbeheer** wordt gebruikt, voeren werknemers de registratie uit via mobiele apparaten. Zie [Productontvangst op basis van inkooporders - registratie](../procurement/product-receipt-against-purchase-orders.md#registration) en de [Artikelhoeveelheden registreren die arriveren in een inkomende lading](#register-item-quantities-arriving) voor meer informatie.

1. **Geregistreerde ladinghoeveelheden worden geboekt op inkooporders.**

    Nadat de ladinghoeveelheden als aangekomen zijn geregistreerd, moeten deze hoeveelheden worden geboekt als productontvangst in het voorraadgrootboek van het bedrijf om de fysieke voorraadverhoging vast te leggen. Zie [Productontvangst op basis van inkooporders - productontvangst](../procurement/product-receipt-against-purchase-orders.md#product-receipt) en [Geregistreerde producthoeveelheden boeken op inkooporders](#post-registered-quantities) voor meer informatie.

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Artikelhoeveelheden registreren die binnenkomen op een inkomende lading

Microsoft Dynamics 365 Supply Chain Management ondersteunt diverse operationele benaderingen voor het vastleggen van de aankomst van bestelde producten. Daarom kunt u het systeem zo configureren dat het aan uw specifieke bedrijfsvereisten voldoet. In deze sectie wordt beschreven hoe u binnenkomende artikelhoeveelheden registreert via een mobiel apparaat wanneer Geavanceerd magazijnbeheer is ingeschakeld in het systeem. Er is echter een alternatieve stroom die is gebaseerd op het gebruik van het artikelontvangstjournaal in plaats van een mobiel apparaat. Zie [Artikelen registreren voor een artikel waarvoor geavanceerd magazijnbeheer mogelijk is met een artikelontvangstjournaal](tasks/register-items-advanced-warehousing.md) voor meer informatie over die stroom.

Wanneer een inkomende lading voor het eerst in het magazijn arriveert, moeten magazijnmedewerkers de artikelhoeveelheden registreren die in de zending zijn opgenomen. Normaal gesproken gebruiken ze draagbare scanners. Deze werkstroom is alleen beschikbaar als het systeem de volgende items bevat:

- **Een record voor de inkomende lading waarmee de artikelhoeveelheden worden beschreven die in de zending worden verwacht**

    De leverancier bevestigt doorgaans de inkomende ladingrecord voordat de zending in het magazijn arriveert. De lading heeft daarom de status _Verzonden_. Magazijnmedewerkers kunnen echter ook artikelhoeveelheden registreren voor ladingen met de status _Open_ of _Ontvangen_.

- **Een menu op het mobiele apparaat dat is geconfigureerd om het ontvangen van ladingen te ondersteunen**

    De [magazijnapp](install-configure-warehousing-app.md) voor mobiele apparaten ondersteunt de volgende processen voor het maken van werk:

    - Artikelontvangst laden
    - Ontvangen en wegzetten van artikel laden
    - Gemengde nummerplaatontvangst, waarbij het veld **Identificatiemethode brondocumentregel** voor het menu-item van het mobiele apparaat is ingesteld op _Artikelontvangst laden_. Zie [Ontvangst van gemengde nummerplaatsen](mixed-license-plate-receiving.md) voor meer informatie.
    - Gemengde nummerplaatontvangst en wegzetten, waarbij het veld **Identificatiemethode brondocumentregel** voor het menu-item van het mobiele apparaat is ingesteld op _Artikelontvangst laden_. Zie [Ontvangst van gemengde nummerplaatsen](mixed-license-plate-receiving.md) voor meer informatie.

    > [!NOTE]
    > Ongeacht het proces zal het systeem het werk genereren waarbij hoeveelheden worden genomen die zijn geregistreerd op de ontvangstlocatie en deze worden weggezet op de normale opslaglocatie. Wanneer het proces _Ontvangen en wegzetten van artikel laden_ of _Nummerplaat ontvangen en wegzetten_ wordt gebruikt, wordt de werknemer die de ladinghoeveelheid heeft geregistreerd ook door het apparaat geïnstrueerd om de opslag als onderdeel van de registratietaak uit te voeren. In tegenstelling tot de processen _Artikelontvangst laden_ en _Gecombineerde nummerplaat ontvangen_, is de veronderstelling dat het opslagwerk onafhankelijk van de registratietaak wordt uitgevoerd.

- **Een werksjabloon waarmee verzamelde en opgeslagen werk voor inkomende ladingen worden gedefinieerd**

    Dit onderwerp hangt samen met de vorige onderwerpen. U moet minimaal over één werksjabloon beschikken voor het werkordertype _Inkooporder_ en die moet een set met de werksoorten verzamelen/wegzetten bevatten.

Het mobiele apparaat begeleidt de ontvangstadministrateur van het magazijn door de stroom voor het registreren van de ladinghoeveelheid. Deze stroom omvat minimaal de volgende stappen voor elke lading-id:

1. Voer de lading-id in.
2. Voer het artikelnummer in voor een ontvangen artikel.
3. Voer de hoeveelheid in van het ontvangen artikelnummer.
4. Voer het nummerplaatnummer in voor de eerste locatie van het artikel, als het systeem niet is ingesteld om dit nummer automatisch te genereren.
5. Tik op **OK**.

Nadat de werknemer deze stappen heeft voltooid, maakt het systeem de volgende updates voor de desbetreffende entiteiten, op voorwaarde dat de hoeveelheid op de inkooporderregel is aangekomen in één lading en dat alle ladinghoeveelheden zijn geregistreerd:

| Entiteit | Updates | Notitie |
|---|---|---|
| Inlezen | Het veld **Hoeveelheid werk gemaakt** op de ladingregel wordt bijgewerkt om de geregistreerde hoeveelheid weer te geven. | De waarde voor **Ladingsstatus** blijft _Verzonden_ of _Geopend_ als er geen bevestiging van de verzending is uitgevoerd voor de lading. Als er minimaal één regel met wegzettaken is gestart, wordt dit gewijzigd in _Onderhanden_. |
| Voorraadtransactie van een inkooporder waarvoor de bijbehorende ladinghoeveelheden zijn geregistreerd |<p>Het volgende velden zijn bijgewerkt:</p><ul><li>Het veld <b>Ontvangst</b> is ingesteld op <i>Geregistreerd.</i></li><li>Het veld <b>Locatie</b> wordt bijgewerkt met de locatiecode van het ontvangende dok. (Deze code wordt opgegeven in het veld <b>Standaard ontvangstlocatie</b> voor elk magazijn.)</li><li>Het veld <b>Nummerplaat</b> wordt bijgewerkt met het nummerplaatnummer dat tijdens de registratie is ingevoerd of gegenereerd.</li><li>Het veld <b>Lading-id</b> wordt bijgewerkt met het nummer van de lading waarvoor de hoeveelheid is geregistreerd. (Zie de opmerking.)</li></ul> | De mogelijkheid om te koppelen tussen de voorraadtransactie van de inkooporder en de hoeveelheden die zijn geregistreerd voor de lading, is ingevoerd in versie 10.0.9 als een optionele functie met de naam _Voorraadtransacties inkooporder koppelen met lading_. Deze functie is vooral nuttig voor operationele stromen waarbij één enkele order van ingekochte goederen wordt geleverd als meerdere ladingen of wanneer een lading hoeveelheden bevat voor meerdere inkooporders. |
| Magazijnopslag | Er wordt een taak gemaakt op basis van een werksjabloon om de werknemer te instrueren de geregistreerde hoeveelheden van de ontvangstlocatie naar een normale opslaglocatie te verplaatsen. | De keuze van de opslaglocatie wordt bepaald door de instructie voor de opslaglocatie. Als er geen locatierichtlijn is gedefinieerd, is de opslaglocatie voor het werk leeg. |

Magazijnmedewerkers kunnen de ontvangst van een inkooporder met een of meer gekoppelde lading registreren zonder het proces _Artikelontvangst laden_ te gebruiken. De volgende methoden zijn beschikbaar:

- **Op het mobiele apparaat:** gebruik de processen _Ontvangen van inkooporderregel_ en _Ontvangen van inkooporderregel en wegzetten_. (Als er meer dan een lading bestaat voor de hoeveelheid op de inkooporderregel, kan de werknemer het ontvangst proces _Ontvangen van inkooporderregel_ niet gebruiken. In plaats daarvan wordt de werk nemer geïnstrueerd de actie te gebruiken die is gekoppeld aan het proces _Artikelontvangst laden_.)
- **Op de client:** gebruik het artikelontvangstjournaal.
- **Op de client:** gebruik de actie **Registratie** die toegankelijk is vanuit de inkooporderregel.

> [!NOTE]
> Als de ontvangst van de inkooporder wordt geregistreerd via een van de voorgaande methoden, wordt er geen koppeling gemaakt tussen de voorraadtransactie van de inkooporder en de lading, zelfs wanneer de functie _Voorraadtransacties inkooporder koppelen met lading_ is ingeschakeld. Een uitzondering op deze regel is wanneer u de optie **Ontvangen van inkooporderregel** gebruikt en slechts één lading een andere status heeft dan _Ontvangen_ voor de orderregel.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Verschillen verwerken tijdens registratie van inkomende ladinghoeveelheden

Magazijnmedewerkers kunnen een ontvangstregistratie voor een gedeeltelijke ladinghoeveelheid uitvoeren. Voor elke ontvangst van een gedeeltelijke ladinghoeveelheid wordt vervolgens een afzonderlijke voorraadtransactie gemaakt met de ontvangststatus _Geregistreerd_ voor de geregistreerde hoeveelheid en de partij-id verwijst naar de oorspronkelijke inkooporderregel.

#### <a name="load-under-receiving"></a>Minder ontvangen lading

Als een lading arriveert en de artikelhoeveelheden kleiner zijn dan de hoeveelheden die in de ladingrecord zijn opgegeven, kunnen de magazijnmedewerkers rechtstreeks in de client dit verschil bevestigen door de hoeveelheid op de ladingsregel te verminderen zodat deze overeenkomt met de werkelijke hoeveelheid die is binnengekomen en geregistreerd.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Meer ontvangen lading

Meerontvangst vindt plaats wanneer een lading arriveert en de artikelhoeveelheden hoger zijn dan de verwachte hoeveelheid van de ladingsregel. U kunt instellen of en in welke mate meerontvangst is toegestaan tijdens de registratie van de lading.

Gebruik het veld **Meerontvangst lading** voor de relevante menuopties op het mobiele apparaat om te bepalen wat er gebeurt wanneer een magazijn medewerker een meerlevering probeert te registreren. Dit veld is beschikbaar voor menuopdrachten van mobiele apparaten die gebruikmaken van de volgende typen processen voor het maken van werk:

- Artikelontvangst laden
- Ontvangen en wegzetten van artikel laden
- Gemengde nummerplaatontvangst, waarbij het veld **Identificatiemethode brondocumentregel** is ingesteld op _Artikelontvangst laden_.
- Gemengde nummerplaatontvangst en wegzetten, waarbij het veld **Identificatiemethode brondocumentregel** is ingesteld op _Artikelontvangst laden_.

De volgende tabel beschrijft de opties die beschikbaar zijn voor het veld **Meerontvangst lading**.

| Waarde | Omschrijving |
|---|---|
| Toestaan | Werknemers kunnen de ontvangst registreren van hoeveelheden die de resterende niet-geregistreerde hoeveelheid overschrijden voor een geselecteerde lading, maar alleen als de totale geregistreerde hoeveelheid niet groter is dan de hoeveelheid van de inkooporderregel die aan de lading is gekoppeld (na correctie voor het meerleveringspercentage). |
| Blokkeren | <p>Werknemers kunnen de ontvangst registreren van hoeveelheden die groter zijn dan de resterende niet-geregistreerde hoeveelheid voor een geselecteerde lading (na correctie voor het meerleveringspercentage). Een werknemer die de ontvangsten registreert, ontvangt een fout en kan pas doorgaan nadat een hoeveelheid is geregistreerd die gelijk is aan of kleiner is dan de resterende niet-geregistreerde ladinghoeveelheid.</p><p>Standaard wordt de waarde van het meerleveringspercentage op een ladingsregel gekopieerd van de bijbehorende inkooporderregel. Wanneer het veld <b>Meerontvangst lading</b> is ingesteld op <i>Blokkeren</i>, gebruikt het systeem de waarde van het meerleveringspercentage om de totale hoeveelheid te berekenen die voor een ladingsregel kan worden geregistreerd. Deze waarde kan echter voor afzonderlijke ladingen worden overschreven. Dit gedrag is van belang bij het ontvangen van stromen waarbij de extra hoeveelheid die het meerleveringspercentage van de orderregel vertegenwoordigt, helemaal of gedeeltelijk wordt verdeeld over meerdere ladingen. Dit is een voorbeeldscenario:</p><ul><li>Er zijn meerdere ladingen voor één inkooporderregel.</li><li>De inkooporderregel heeft een meerleveringspercentage dat hoger is dan 0 (nul).</li><li>Er zijn reeds hoeveelheden geregistreerd voor een of meer ladingen, zonder rekening te houden met het meerleveringspercentage.</li><li>De hoeveelheid voor meerlevering arriveert bij de laatste lading.</li></ul><p>In dit scenario kan een mobiel apparaat alleen worden gebruikt om de extra hoeveelheid voor de laatste lading te registreren als de magazijnsupervisor het meerleveringspercentage voor de desbetreffende ladingsregel verhoogt van de standaardwaarde naar een waarde die groot genoeg is, zodat de volledige meerlevering kan worden geregistreerd met de laatste lading.</p> |
| Alleen blokkeren voor afgesloten ladingen | Werknemers kunnen de meerontvangsten doen voor hoeveelheden op de ladingsregel voor openstaande ladingen, maar niet voor ladingen met de status _Ontvangen_. |

> [!NOTE]
> De standaardwaarde van het veld **Meerontvangst lading** is _Toestaan_. Wanneer deze waarde wordt gebruikt, komt het gedrag overeen met het standaardgedrag dat beschikbaar was voordat de functie _Meerontvangst voor ladinghoeveelheden_ werd toegevoegd in versie 10.0.11.

### <a name="put-away-the-registered-quantities"></a>De geregistreerde hoeveelheden opslaan

Wanneer de registratie op het mobiele apparaat is voltooid, worden door de actie _Registratie van ontvangsthoeveelheid_ de voorraad- en magazijnrecords bijgewerkt om aan te geven dat de hoeveelheden nu op de ontvangende doklocatie staan en beschikbaar zijn voor reservering. De magazijnbewerkingen van een bedrijf vereisen echter meestal dat de hoeveelheden worden verplaatst van de ontvangstdok naar de normale magazijnopslag, zodat de volgende orderverzamelprocessen kunnen plaatsvinden. Instructies voor de opslag worden vastgelegd in de opslagtaken die automatisch worden gegenereerd wanneer de binnenkomende lading als ontvangen wordt geregistreerd.

Wanneer de magazijnmedewerker de opslagwerkzaamheden heeft voltooid, registreert en traceert het systeem het resultaat door diverse entiteiten bij te werken, zoals in de volgende tabel wordt samengevat.

| Entiteit | Updates | Notitie |
|---|---|---|
| Inlezen | <p>Het volgende velden zijn bijgewerkt:</p><ul><li>De waarde van <b>Ladingsstatus</b> wordt gewijzigd in <i>Onderhanden</i>.</li><li>De waarde van <b>Werkstatus</b> wordt gewijzigd in <i>100,00% van werk voltooid</i>.</li></ul> | De waarde van **Ladingsstatus** wordt gewijzigd in _Onderhanden_ wanneer de werknemer de opslagtaak start voor minimaal één regel met wegzettaken. |
| Voorraadtransacties van werk waarvoor toegewezen hoeveelheden zijn opgeslagen | De velden **Ontvangst** en **Locatie** en andere relevante velden worden bijgewerkt om de verplaatsing van de ontvangstlocatie naar de opslaglocatie weer te geven. | De waarde voor **Ontvangststatus** van de voorraadtransactie van de inkooporder blijft _Geregistreerd_. |
| Magazijnopslag | De waarde van **Werkstatus** verandert in _Gesloten_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Geregistreerde ladinghoeveelheden boeken op inkooporders

Nadat de inkomende producthoeveelheden in het systeem zijn geregistreerd, worden ze beschikbaar voor reservering in verband met verkoop en andere uitgaande en interne bewerkingen. Het systeem werkt echter de voorraadrekeningen (interim) nog niet bij. Deze update kan alleen plaatsvinden wanneer het team geregistreerde productontvangsten boekt.

Als u een pagina wilt openen waarop ze een productontvangst kunnen boeken, kunnen de leden van het operationele team _één_ van de volgende stappen uitvoeren:

- Open de betreffende ladingsrecord en selecteer vervolgens de actie **Productontvangst**.
- Ga naar **Magazijnbeheer \> Periodieke taken \> Productontvangsten bijwerken** en geef vervolgens in het veld **Lading-id** de te boeken lading op.
- Open de betreffende inkooporder en selecteer vervolgens de actie **Productontvangst**.
- Ga naar **Inkoop en sourcing \> Inkooporders \> Producten ontvangen \> Productontvangsttaak boeken**.

De actie **Productontvangst** die beschikbaar is op de pagina **Lading** (en op de equivalente pagina voor de updatetaak de pagina **Productontvangsten bijwerken**) kan alleen productontvangsthoeveelheden bijwerken voor hoeveelheden op de inkooporder met de status _Geregistreerd_. De actie **Productontvangst** die beschikbaar is op de pagina **Inkooporder** kan echter hoeveelheden bevatten in beide verwerkingsstatussen (_Besteld_ en _Geregistreerd_). Dit kan ook de omvang van de productontvangstboeking bepalen via extra parameters, zoals _Hoeveelheid nu ontvangen_ en _Geregistreerde hoeveelheid en services_.

Alleen orders met de status _Bevestigd_ kunnen worden geboekt als productontvangst. Voor niet-bevestigde inkooporders wordt de actie **Productontvangst** weergegeven als niet beschikbaar.

### <a name="post-registered-quantities-from-the-load-page"></a>Geregistreerde hoeveelheden boeken vanaf de pagina Lading

Voor het boeken van geregistreerde hoeveelheden voor productontvangsten vanaf de pagina **Lading** moet aan de volgende vereisten zijn voldaan:

- De lading moet ten minste één hoeveelheidseenheid hebben met de status _Geregistreerd_.
- De ladingsstatus moet _Verzonden_ zijn.
- De inkooporder die aan de lading is gekoppeld, moet de status _Bevestigd_ hebben.

> [!NOTE]
> Als de ladingsstatus nog niet is ingesteld op _Verzonden_, wordt de lading automatisch bevestigd voordat het bijwerken van de productontvangst wordt uitgevoerd. (De ladingsstatus wordt ingesteld op _Verzonden_ wanneer een gebruiker de inkomende zending van de lading registreert.)

Voor het boeken van de productontvangst voor ontvangstregistraties die zijn gekoppeld aan een geselecteerde lading, selecteert de werknemer de actie **Productontvangst** op de pagina **Lading**. De pagina die wordt geopend, heeft de volgende belangrijke details:

- In het veld **Hoeveelheid** in de sectie **Parameters** op het tabblad **Instellingen** wordt de _geregistreerde hoeveelheid_ weergegeven. Er zijn hier geen andere opties beschikbaar.
- In het raster op het sneltabblad **Overzicht** staan alle inkooporders die in de geselecteerde lading zijn opgenomen.
- Het raster op het sneltabblad **Regels** vermeldt alle orderregels met een geregistreerde hoeveelheid.

> [!NOTE]
> Hoeveelheden voor orderregels die op het tabblad **Regel** worden weergegeven, worden anders berekend, afhankelijk van of de functie _Meerdere productontvangsten toestaan per lading_ beschikbaar is en is ingeschakeld in uw versie van Supply Chain Management.
>
> | Versie | Berekening |
> |---|---|
> | Versies vóór versie 10.0.10 en nieuwere versies waarvoor de functie _Meerdere productontvangsten toestaan per lading_ niet is ingeschakeld | De regelhoeveelheid is het totaal van alle geregistreerde hoeveelheden _voor die inkooporderregel_, ongeacht of de registratie is uitgevoerd voor meerdere ladingen, onafhankelijk van de lading, vanaf een mobiel apparaat of van de client. |
> | Versie 10.0.10 en later, waarvoor de functie _Meerdere productontvangsten toestaan per lading_ is ingeschakeld | De regelhoeveelheid is het totaal van alle geregistreerde hoeveelheden _voor de ladingrecord_ vanwaaruit de actie **Productontvangst boeken** is geïnitieerd. |

Wanneer de gebruiker **OK** selecteert om het boeken van de productontvangst te bevestigen, voert het systeem de volgende updates uit op de desbetreffende entiteiten.

| Entiteit | Updates |
|---|---|
| Voorraadtransactie van de inkooporder waarvoor de regelhoeveelheden zijn opgenomen in het boekingsbereik | <p>De volgende velden worden bijgewerkt (maar er zijn echter ook meerdere andere updates):</p><ul><li>Het veld <b>Ontvangst</b> is ingesteld op <i>Ontvangen</i>.</li><li>Het veld <b>Fysieke datum</b> wordt bijgewerkt met de datum van de boeking.</li></ul> |
| Lading vanwaaruit de productontvangst door de gebruiker is geboekt | Updates van de ladingen zijn afhankelijk van de gebruikte versie en de instelling van het veld **Meerdere productontvangsten toestaan per lading**. De regels worden beschreven in de tabel die later in deze sectie wordt weergegeven. |

Met het veld **Meerdere productontvangsten toestaan per lading** kunnen bedrijven een beleid voor inkomende ontvangsten kiezen. Afhankelijk van hun operationele stromen kunnen bedrijven ervoor kiezen om meerdere productontvangstboekingen voor dezelfde lading toe te staan of te weigeren. Wij raden aan dat de logistiek manager het veld **Meerdere productontvangsten toestaan per lading** instelt op een van de volgende waarden:

- **Nee**: selecteer deze waarde als de magazijnmedewerkers alle orderhoeveelheden altijd registreren die bij elke lading binnen een toegewezen tijdsbestek arriveren. Als er geen ladinghoeveelheden zijn geregistreerd, wordt ervan uitgegaan dat ze niet zijn aangekomen of niet in de lading zijn opgenomen en dus niet als onderdeel van de lading moeten worden beschouwd. De boeking van de productontvangst op basis van een lading gebruikt dezelfde veronderstelling. Behalve dat alle geregistreerde hoeveelheden (de hoofdfunctie) worden bijgewerkt met de productontvangst, wordt de lading als volledig gedeclareerd en gesloten voor verdere verwerking. In dit geval worden alle hoeveelheden op de ladingsregels automatisch bijgewerkt naar de geregistreerde hoeveelheden, worden ladingsregels zonder geregistreerde hoeveelheden verwijderd en wordt de ladingsstatus gewijzigd in _Ontvangen_.
- **Ja**: selecteer deze waarde als magazijnmedewerkers meer tijd nodig hebben om alle hoeveelheden van de ontvangen lading te registreren, maar de hoeveelheden van de productontvangst die al zijn geregistreerd, wel moeten worden geboekt. In dit geval moet de logistiek manager een lading open houden, zelfs nadat de boekingstaak voor de productontvangst is uitgevoerd, zodat resterende ladinghoeveelheden kunnen worden geregistreerd en de productontvangst doorlopend wordt bijgewerkt naar het grootboek.
- **Vragen**: selecteer deze waarde als u verschillende ontvangstpraktijken gebruikt en er telkens een beslissing moet worden genomen wanneer de productontvangstboeking wordt uitgevoerd.

De volgende tabel geeft een overzicht van de effecten van de instelling **Meerdere productontvangsten toestaan per lading**.

| Meerdere productontvangsten toestaan per lading | Ladinghoeveelheid | Status lading | Notitie |
|---|---|---|---|
| Als dit veld niet beschikbaar is (versies vóór 10.0.10) | <p>De ladinghoeveelheid wordt zo ingesteld dat deze gelijk is aan de geregistreerde hoeveelheid.</p><p>Als de ladinghoeveelheid wordt gewijzigd in 0 (nul), betekent dit dat er geen registratie is uitgevoerd, en wordt de ladingsregel verwijderd.</p><p>Als er geen ladingsregels in de lading zijn, wordt de lading verwijderd.</p> | _Ontvangen_ | Als er meerdere ladingen bestaan voor de geregistreerde hoeveelheid van de orderregel, wordt alleen de status van de lading waarvoor de ontvangst is geboekt, bijgewerkt naar _Ontvangen_. |
| No | <p>De ladinghoeveelheid wordt zo ingesteld dat deze gelijk is aan de geregistreerde hoeveelheid die aan de lading-id is gekoppeld.</p><p>Als er geen lading-id wordt geregistreerd voor de voorraadtransactie, komt het gedrag overeen met de versies vóór 10.0.10.</p> | _Ontvangen_ | |
| Ja | Geen updates | _Ontvangen_, als de totale geregistreerde ladinghoeveelheid gelijk is aan of groter is dan de ladinghoeveelheid | |
| Ja | Geen updates | _Verzonden_ of _Onderhanden_, als de totale geregistreerde ladinghoeveelheid kleiner is dan de ladinghoeveelheid | |

Nadat het veld **Ladingsstatus** is ingesteld op _Ontvangen_, kunnen er geen productontvangstboekingen meer worden uitgevoerd voor die lading. De werknemer kan de resterende orderhoeveelheid voor de ontvangen lading echter registreren onder de volgende voorwaarden. (Zie de sectie [Meer ontvangen lading](#load-over-receiving) eerder in dit onderwerp voor meer informatie.)

- De versie van Supply Chain Management is ouder dan versie 10.0.11.
- De functie _Meerontvangst voor ladinghoeveelheden_ is ingeschakeld en het veld **Meerontvangst voor hoeveelheid ladingsregel** in de menuopdracht van het mobiele apparaat voor de actie Artikelontvangst laden is ingesteld op _Toestaan_.

Voor het boeken van aanvullende geregistreerde ladinghoeveelheden voor de productontvangst op basis van een lading met de status _Ontvangen_, moet de gebruiker de boekingsactie uitvoeren vanuit de gekoppelde inkooporder.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Geregistreerde hoeveelheden boeken vanaf de pagina Inkooporder

Voor het boeken van geregistreerde ladinghoeveelheden voor de productontvangst vanaf de pagina **Inkooporder**, voert de gebruiker de volgende taken uit voordat de actie **Productontvangst** wordt geselecteerd:

- Stel het veld **Hoeveelheid** in de sectie **Parameters** op het tabblad **Instellingen** in op _Geregistreerde hoeveelheid_.
- Voer in het veld **Productontvangst** de nummers in van de inkooporders die in de boeking zijn opgenomen.

> [!NOTE]
> De regelhoeveelheid die wordt opgenomen in het boekingsbereik is het totaal van alle geregistreerde hoeveelheden voor de orderregel, ongeacht of de registratie van de hoeveelheid is uitgevoerd voor meerdere ladingen, onafhankelijk van de lading, vanaf een mobiel apparaat of van de client. Dezelfde regel is van toepassing wanneer de productontvangstboeking wordt uitgevoerd vanuit een lading, als dit wordt gedaan wanneer het veld **Meerdere productontvangsten toestaan per lading** niet beschikbaar is of niet is ingeschakeld.

Wanneer de gebruiker **OK** selecteert om het boeken van de productontvangst te bevestigen, voert het systeem de volgende updates uit op de desbetreffende entiteiten.

| Entiteit | Updates |
|---|---|
| Voorraadtransactie van de inkooporder waarvoor de regelhoeveelheden zijn opgenomen in het boekingsbereik | <p>De volgende velden worden bijgewerkt (maar er zijn echter ook meerdere andere updates):</p><ul><li>Het veld <b>Ontvangst</b> is ingesteld op <i>Ontvangen</i>.</li><li>Het veld <b>Fysieke datum</b> wordt bijgewerkt met de datum van de boekingsactie voor de productontvangst.</li></ul> |
| Inlezen | Updates van de ladingen zijn afhankelijk van het feit of het veld **Meerdere productontvangsten toestaan per lading** beschikbaar en ingeschakeld is. De regels worden in de volgende tabel beschreven. |

De volgende tabel geeft een overzicht van de effecten van de instelling **Meerdere productontvangsten toestaan per lading**.

| Meerdere productontvangstbonnen per lading toestaan | Ladinghoeveelheid | Status lading | Notitie |
|---|---|---|---|
| Als dit veld is uitgeschakeld of niet beschikbaar is (in versies vóór 10.0.10) | Geen updates | Er worden geen updates uitgevoerd. (De status blijft _Open_, _Verzonden_ of _Onderhanden_.) | Omdat de boeking van de productontvangst wordt gestart vanuit een inkooporder, bevat de bijwerklogica geen informatie over de koppeling tussen de geregistreerde hoeveelheden binnen het bereik en de ladingen waarvoor de registratie is geregistreerd. Hierdoor kan de lading niet worden geselecteerd voor de statuswijziging. |
| Ingeschakeld | Geen updates | <p>Een van de volgende acties wordt uitgevoerd:</p><ul><li>De status wordt gewijzigd in <i>Ontvangen</i> als de totale ontvangen en gekochte hoeveelheden van de voorraadtransacties in de inkooporder meer zijn dan of gelijk zijn aan de hoeveelheid van de lading waaraan ze zijn gekoppeld.</li><li>De status blijft <i>Open</i>, <i>Verzonden</i>of <i>Onderhanden</i> als niet aan de vorige voorwaarde is voldaan voor alle regels in de lading.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Selecteer de gewenste boekingsoptie voor de productontvangst voor uw logistieke activiteiten

Zoals eerder is beschreven, biedt het systeem twee boekingsopties voor productontvangsten. U vindt de opties op de volgende plaatsen:

- Op de pagina **Lading** of vanuit het menu **Magazijnbeheer \> Periodieke taken** als updatetaak
- Op de pagina **Inkooporder** of vanuit het menu **Inkoop en sourcing \> Inkooporders \> Producten ontvangen** als updatetaak

Bedrijven die ladingen gebruiken om transporten en magazijnverwerking van hun inkomende orders te plannen en te beheren, wordt aangeraden de volgende functies te gebruiken, die zijn ontworpen om met ladingen te werken:

- Acties voor **Artikelontvangst laden** op hun mobiele magazijnapparaten, voor het registreren van de aankomst van de producthoeveelheid voor de lading
- Acties voor **Productontvangsten boeken** die worden geïnitieerd vanuit een lading om het voorraadgrootboek bij te werken

> [!NOTE]
> Andere functies voor het registreren van hoeveelheden en het boeken van productontvangsten kunnen worden gebruikt om de bijbehorende operationele ontvangstprocessen te ondersteunen. Als u deze echter uitwisselbaar gebruikt met of in plaats van de specifieke ladingsfuncties, kan de nauwkeurigheid van de ladingsgegevens verslechteren en daarmee de werking van de laadbeheerstromen.

## <a name="example-scenarios"></a>Voorbeeldscenario's

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Uw systeem voorbereiden voor het uitvoeren van de voorbeeldscenario's

Als u de in deze sectie beschreven voorbeeldscenario's wilt doorlopen, moet u eerst controleren of alle vereiste functies in uw systeem zijn ingeschakeld. De vereiste voorbeeldgegevens moeten ook in het systeem beschikbaar zijn.

#### <a name="turn-on-the-required-features"></a>De vereiste functies inschakelen

Voor deze scenario's hebt u de functie _Meerdere productontvangsten toestaan per lading_ en de bijbehorende vereiste functie nodig. Beheerders kunnen deze functies inschakelen door de volgende stappen uit te voeren.

1. Open het het werkgebied **Functiebeheer**. (Zie [Overzicht van Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor gedetailleerde informatie over het zoeken en gebruiken van dit werkgebied.)

1. Schakel de functie _Voorraadtransacties inkooporder koppelen met lading_ in die op de volgende manier wordt weergegeven:

    - **Module:** _Magazijnbeheer_
    - **Functienaam:** _Voorraadtransacties inkooporder koppelen met lading_

1. Schakel de functie _Meerdere productontvangsten toestaan per lading_ in, die op de volgende manier wordt weergegeven:

    - **Module:** _Magazijnbeheer_
    - **Functienaam:** _Meerdere productontvangsten toestaan per lading_

#### <a name="enable-sample-data"></a>Voorbeeldgegevens inschakelen

Als u deze scenario's wilt doorlopen met de opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard demogegevens zijn geïnstalleerd. U moet ook de rechtspersoon **USMF** selecteren voordat u begint.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Een menuopdracht voor het ontvangen van ladingartikelen toevoegen wanneer een mobiel apparaat wordt gebruikt

Voordat magazijnmedewerkers een mobiel apparaat kunnen gebruiken om een inkomende voorraad te registreren die aan een lading is gekoppeld, moet u hiervoor een menuopdracht van mobiel apparaat maken.

In deze sectie maakt u een menuopdracht voor een mobiel apparaat en voegt u deze toe aan een bestaand menu. Een magazijnmedewerker kan vervolgens de menuoptie selecteren in de magazijnapp.

1. Ga naar **Magazijnbeheer \> Instellingen \> Mobiel apparaat \> Menuopties voor mobiel apparaat** en zorg ervoor dat het menu met mobiele apparaten een menuoptie bevat met de volgende instellingen:

    - **Modus:** _werk_
    - **Proces van werkaanmaak:** _Artikelontvangst laden_
    - **Nummerplaat maken:** _Ja_

    U kunt alle andere instellingen op de standaardwaarden laten staan.

    ![Instellingen voor menuopdracht van mobiel apparaat](media/inbound-mobile-menu-items.png "Instellingen voor menuopdracht van mobiel apparaat")

    Zie [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md) voor meer informatie over het instellen van menuopties voor mobiele apparaten.

2. Nadat u de menuoptie hebt ingesteld, gaat u naar **Magazijnbeheer \> Instellingen \> Mobiel apparaat \> Menuopties voor mobiel apparaat** en voegt u deze toe aan de menustructuur voor uw mobiele apparaten.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>Voorbeeldscenario 1: Een lading registreren waarbij sommige artikelen ontbreken

Dit scenario geeft aan hoe u hoeveelheden voor een inkomende lading registreert, waarbij niet alle verwachte hoeveelheden aanwezig zijn. Vervolgens wordt weergegeven hoe de productontvangst voor de inkooporder wordt geboekt.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Een lading maken om de ontvangst van een inkooporder te plannen

In deze procedure maakt u handmatig een inkooporder en een bijbehorende lading. U gaat de lading vervolgens bijwerken om te simuleren dat deze van de leverancier is verzonden (waardoor de ladingsstatus wordt bijgewerkt). Magazijnplanners kunnen vervolgens de ladingen filteren op **Ladingsstatus** om verwachte binnenkomende ladingen te vinden.

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw**.
1. Stel in het dialoogvenster **Inkooporder maken** het veld **Leveranciersrekening** in op _1001_.
1. Selecteer **OK** om het dialoogvenster te sluiten en de inkooporder te maken.
1. De nieuwe inkooporder bevat al een regel onder **Inkooporderregels**. Stel de volgende waarden in voor deze regel:

    - **Artikelnummer:** _A0001_
    - **Magazijn:** _24_
    - **Hoeveelheid:** _10_

1. Selecteer in het actievenster op het tabblad **Inkoop** de optie **Acties \> Bevestigen**. De status van de order is nu _Bevestigd_.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Acties \> Workbench ladingplanning**.
1. Selecteer op de pagina **Workbench ladingplanning** in het actievenster op het tabblad **Vraag en aanbod** de optie **Toevoegen \> Aan nieuwe lading**.
1. Stel in het dialoogvenster **Ladingsslabloon toewijzen** het veld **Ladingsslabloon-id** in op _20'-container_.
1. Selecteer **OK** om het dialoogvenster te sluiten en terug te gaan naar de workbench.
1. Selecteer in de sectie **Ladingen** de optie **Lading-id** om de nieuwe lading te openen.
1. Bekijk de koptekst en regeldetails van de lading en let op de volgende punten:

    - Op het sneltabblad **Lading** is het veld **Ladingsstatus** ingesteld op _Open_.
    - In de sectie **Ladingregels** staat één regel waarvoor het veld **Hoeveelheid** is ingesteld op _10_ en het veld **Hoeveelheid werk gemaakt** op _0_ (nul).

    ![Gegevens lading](media/inbound-load-details.png "Gegevens lading")

1. Selecteer in het actievenster op het tabblad **Verzenden en ontvangen** de optie **Bevestigen \> Inkomende zending**. Zoals u ziet, is de **Ladingsstatus** gewijzigd in _Verzonden_.
1. Noteer de waarde van de **Lading-id** zodat u deze in de volgende procedure kunt gebruiken.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>De ontvangst registreren van de hoeveelheden die bij de lading zijn ontvangen

Wanneer de lading arriveert in het ontvangende magazijn, registreert een ontvangstmedewerker de ladinghoeveelheden op een mobiel apparaat.

1. Meld u aan bij magazijn 24 met uw mobiele apparaat. (In de standaard demogegevens meldt u zich aan met _24_ als gebruikers-id en _1_ als wachtwoord.)
1. Selecteer de menuoptie _Artikelontvangst laden_ die u voor dit scenario hebt gemaakt.
1. Voer de volgende waarden in aan de hand van de instructies voor gegevensinvoer op het scherm. (De volgorde kan variëren, afhankelijk van het mobiele apparaat of de emulator die u gebruikt.)

    - **Lading**: voer de lading-id in die u in de vorige procedure hebt gemaakt.
    - **Artikel**: voer _A0001_ in. Dit is het artikel dat wordt verwacht voor deze lading.
    - **Hoeveelheid**: voer _9_ in als de werkelijke hoeveelheid die aanwezig is in de lading. Deze hoeveelheid is kleiner dan het verwachte aantal.

1. Ga verder met de werkstroom en laat alle andere velden leeg of stel deze in op de standaardwaarden, totdat het apparaat u informeert dat het werk is voltooid.

De ontvangsttaak is nu voltooid en de ontvangstmedewerker kan de volgende taak gaan uitvoeren. De magazijnmedewerkers kunnen de ladingrecord later controleren en vaststellen dat de ontvangen hoeveelheid kleiner was dan de verwachte hoeveelheid. Vervolgens wordt de volgende procedure uitgevoerd met behulp van de webclient.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Zoek in de lijst de lading die u zojuist hebt ontvangen. (Mogelijk moet u het selectievakje **Gesloten weergeven** inschakelen om de binnenkomende ladingen met de ladingsstatus _Verzonden_ op te nemen.) Selecteer vervolgens de koppeling in de kolom **Lading-id** om de lading te openen.
1. In de ladingrecord blijft de waarde van de **Ladingsstatus** staan op _Verzonden_, maar de waarde voor **Hoeveelheid werk gemaakt** op de ladingregel wordt gewijzigd in _9_.
1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Zoek in de lijst de inkooporder die u zojuist hebt ontvangen en selecteer vervolgens de koppeling in de kolom **Inkooporder** om de order te openen.
\
1. Selecteer op het sneltabblad **Inkooporderregels** de optie **Voorraad \> Weergeven \> Transacties**.
1. Controleer de details van de twee inkoopordertransacties. (Mogelijk moet u de pagina **Voorraadtransacties** aanpassen om het veld **Lading-id** weer te geven in het raster.) Er moeten twee transacties worden weergegeven:

    - De transactie met een ontvangst in de _Geregistreerde_ status vertegenwoordigt de registratiehoeveelheid van _9_ die werd uitgevoerd voor een specifieke lading via het mobiele apparaat. De **Lading-id** wordt gekoppeld aan de desbetreffende transactie.
    - De transactie met een ontvangst in de status _Besteld_ vertegenwoordigt de resterende niet-geregistreerde orderregelhoeveelheid van _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Ontvangst van geregistreerde ladinghoeveelheden boeken op inkooporders

In deze procedure gaat u de productontvangst die u voor een lading hebt geregistreerd, in de voorraad boeken. Het resultaat is dat de ontvangen voorraad en de gerelateerde kosten aan het grootboek van het bedrijf worden toegevoegd.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Zoek in de lijst de lading die u hebt ontvangen. (Mogelijk moet u het selectievakje **Gesloten weergeven** inschakelen om de binnenkomende ladingen met de ladingsstatus _Verzonden_ op te nemen.) Selecteer vervolgens de koppeling in de kolom **Lading-id** om de lading te openen.
1. Selecteer in het actievenster op het tabblad **Verzenden en ontvangen** de optie **Ontvangen \> Productontvangst**. Klik op **Ja** als u wordt gevraagd de actie te bevestigen.
1. Bekijk het raster in het dialoogvenster **Productontvangst boeken** op het sneltabblad **Regels**. U zou de inkooporderregel moeten zien waarvoor de hoeveelheid is geregistreerd voor de geselecteerde lading.

    > [!NOTE]
    > In versies waarvoor de functie _Meerdere productontvangsten toestaan per lading_ niet beschikbaar is of niet is ingeschakeld, is de standaardhoeveelheid die wordt weergegeven in het raster **Ladingregels** de totale hoeveelheid die is geregistreerd voor alle ladingen die aan de inkooporderregel zijn gekoppeld.

1. Bekijk het raster in het dialoogvenster **Productontvangst** op het sneltabblad **Overzicht**. U ziet dat dit is ingesteld op een aantal de id van de geselecteerde lading bevat.
1. Selecteer **OK** om de productontvangst te boeken en sluit het dialoogvenster **Productontvangst boeken**.
1. U keert terug naar de ladinggegevens. Let op de volgende punten:

    - Het veld **Ladingsstatus** is nu ingesteld op _Ontvangen_.
    - Op de ladingregel is de waarde **Hoeveelheid** voor de lading gewijzigd van _10_ in _9_ stuks wat overeenkomt met de geregistreerde hoeveelheid, maar de waarde van **Hoeveelheid werk gemaakt** blijft _9_.

Als het inkoopteam niet verwacht dat de leverancier de resterende orderhoeveelheid van 1 zal leveren, kan de order worden gesloten door het leveringsrestant van de regel te wijzigen in _0_. Als er echter snel wordt vastgesteld dat het ontbrekende stuk van de oorspronkelijke lading is aangekomen, kunnen de magazijnmedewerkers een van de volgende acties uitvoeren:

- De hoeveelheid registreren voor dezelfde lading. In dit geval wordt het veld **Ladingsstatus** opnieuw ingesteld op _Verzonden_ en wordt de waarde **Hoeveelheid werk gemaakt** gewijzigd in _10_. Deze keuze is alleen beschikbaar in de volgende situaties:

    - De functie _Meerontvangst voor ladinghoeveelheden_ is niet beschikbaar of is niet ingeschakeld.
    - De functie _Meerontvangst voor ladinghoeveelheden_ is beschikbaar en ingeschakeld en het veld **Meerontvangst voor hoeveelheid ladingsregel** is ingesteld op _Toestaan_.

- De hoeveelheid toevoegen aan een nieuwe of een bestaande lading en deze op de gebruikelijke manier verwerken.
- De hoeveelheid registreren en/of ontvangen op een manier die geen ladingverwerking omvat.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>Voorbeeldscenario 2: Hoeveelheden registreren die arriveren op meerdere binnenkomende ladingen waarbij een aantal artikelen ontbreekt

In dit scenario wordt een inkomende zending die betrekking heeft op één inkooporderregel opgesplitst in twee ladingen. Een inkooporderregel kan bijvoorbeeld worden opgesplitst in meerdere ladingen als gevolg van fysieke ladingbeperkingen op gewicht en/of volume.

In dit scenario wordt ook beschreven hoe u meerdere productontvangstboekingen voor dezelfde lading verwerkt. U registreert hoeveelheden die op meerdere inkomende ladingen arriveren, maar de hoeveelheden komen niet overeen met de verwachte hoeveelheden. De kostenwijzigingen die plaatsvinden via de boeking van de productontvangst worden meerdere keren uitgevoerd voor dezelfde lading.

#### <a name="set-up-load-receiving-policies"></a>Ontvangstbeleid voor ladingen instellen

In deze procedure schakelt u meerdere productontvangstboekingen van dezelfde lading in.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het tabblad **Ladingen** het veld **Meerdere productontvangsten toestaan per lading** in op _Ja_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Twee ladingen maken om de ontvangst van een inkooporder te plannen

In deze procedure maakt u een inkooporder en twee ladingen. U gaat elke lading vervolgens handmatig bijwerken om te simuleren dat deze door de leverancier is verzonden (waardoor de ladingsstatus wordt bijgewerkt). Magazijnplanners kunnen vervolgens de ladingen filteren op **Ladingsstatus** om verwachte binnenkomende ladingen te vinden.

Verder leert u hoe u de inkooporderregel instelt, zodat u een hoeveelheid kunt ontvangen die 20 procent hoger is dan de hoeveelheid die voor de regel is opgegeven.

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw**.
1. Stel op het sneltabblad **Leverancier** het veld **Leveranciersrekening** in op _1001_ en selecteer **OK**.
1. De nieuwe inkooporder wordt geopend en bevat een lege regel in het raster **Inkooporderregels**. Stel de volgende waarden in voor deze orderregel:

    - **Artikelnummer:** _A0001_
    - **Magazijn:** _24_
    - **Hoeveelheid:** _10_

1. Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Meerlevering** in op _20_.
1. Selecteer in het actievenster op het tabblad **Inkoop** de optie **Acties \> Bevestigen**. De status van de order is nu _Bevestigd_.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Acties \> Workbench ladingplanning**.
1. Selecteer op de pagina **Workbench ladingplanning** in het actievenster op het tabblad **Vraag en aanbod** de optie **Toevoegen \> Aan nieuwe lading**.
1. Stel in het dialoogvenster **Ladingsslabloon toewijzen** het veld **Ladingsslabloon-id** in op _20'-container_. Wijzig op het tabblad **Details** de **Hoeveelheid** van _10_ in _5_ om de hoeveelheid op de inkooporderregel gedeeltelijk toe te voegen.
1. Selecteer **OK** om de instellingen toe te passen en het dialoogvenster te sluiten.
1. Herhaal stap 8 tot en met 10 om een tweede lading te maken. Dit keer moet het veld **Hoeveelheid** al zijn ingesteld op _5_.
1. Selecteer op de pagina **Workbench ladingplanning** in het raster **Ladingen** de waarde bij **Lading-id** voor de eerste lading die u hebt gemaakt. De pagina **Ladingdetails** wordt weergegeven en toont de geselecteerde lading. Volg vervolgens deze stappen:

    1. Selecteer in het actievenster op het tabblad **Verzenden en ontvangen** de optie **Bevestigen \> Inkomende zending**.
    1. Zoals u ziet, is de waarde bij **Ladingsstatus** gewijzigd in _Verzonden_.
    1. Selecteer de knop Sluiten om terug te keren naar de pagina **Workbench ladingplanning**.

1. Herhaal de vorige stap voor de tweede lading die u hebt gemaakt.
1. Noteer de twee waarde voor **Lading-id** die in het raster **Ladingen** worden weergegeven.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Gedeeltelijke ontvangst registreren van de hoeveelheden die bij de eerste lading zijn ontvangen en de geregistreerde ladinghoeveelheden boeken

Wanneer de ladingen arriveren in het ontvangende magazijn, registreert een ontvangstmedewerker de ladinghoeveelheden op een mobiel apparaat. De geregistreerde voorraad die aan een lading is gekoppeld, wordt vervolgens in het grootboek van het bedrijf bijgewerkt door de productontvangst op basis van de lading te boeken.

In deze procedure wordt aangegeven hoe een ontvangstmedewerker ladinghoeveelheden registreert op een mobiel apparaat.

1. Meld u aan bij magazijn 24 met uw mobiele apparaat. (In de standaard demogegevens meldt u zich aan met _24_ als gebruikers-id en _1_ als wachtwoord.)
1. Selecteer de menuoptie _Artikelontvangst laden_ die u voor dit scenario hebt gemaakt.
1. Voer de volgende waarden in aan de hand van de instructies voor gegevensinvoer op het scherm. (De volgorde kan variëren, afhankelijk van het mobiele apparaat of de emulator die u gebruikt.)

    - **Lading**: voer de eerste lading-id in die u in de vorige procedure hebt gemaakt.
    - **Artikel**: voer _A0001_ in. Dit is het artikel dat wordt verwacht voor deze lading.
    - **Hoeveelheid**: voer _3_ in. Deze hoeveelheid is kleiner dan het verwachte aantal. Stel dat u, als ontvangstmedewerker, geen tijd hebt om alle hoeveelheden voor deze lading te registreren. Verderop in deze procedure registreert u de resterende artikelen door deze stap te herhalen en het veld **Hoeveelheid** in te stellen op _2_.

1. Ga verder met de werkstroom en laat alle andere velden leeg of stel deze in op de standaardwaarden, totdat het apparaat u informeert dat het werk is voltooid.
1. Ga in de webclient naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Zoek in de lijst de lading die u zojuist hebt ontvangen en selecteer de waarde van de **Lading-id** om de lading te openen. Merk op dat de ladingrecord de waarde van de **Ladingsstatus** blijft staan op _Verzonden_, maar de waarde voor **Hoeveelheid werk gemaakt** op de ladingregel wordt gewijzigd in _3_.
1. Selecteer in het actievenster op het tabblad **Verzenden en ontvangen** de optie **Ontvangen \> Productontvangst**. Klik op **Ja** als u wordt gevraagd de actie te bevestigen.
1. Bekijk in het dialoogvenster **Productontvangst boeken** de weergegeven waarden maar wijzig deze niet en selecteer vervolgens **OK**.
1. U keert terug naar de pagina **Ladingdetails** voor de geselecteerde lading. Let op de volgende punten:

    - Het veld **Ladingsstatus** blijf ingesteld op _Verzonden_.
    - Op de ladingregel blijft de waarde voor **Hoeveelheid** _5_ stuks, wat de oorspronkelijke ladinghoeveelheid is, en blijft de waarde voor **Hoeveelheid gemaakt werk** op _3_ staan.

1. Voer de registratie van de resterende hoeveelheid in deze lading uit door deze procedure te herhalen. In stap 3 stelt u echter het veld **Hoeveelheid** in op _2_.

De ontvangsttaak voor de eerste lading is nu voltooid. Er zijn twee ontvangstjournalen gemaakt, één voor elke wijziging van de twee productontvangsten die u hebt uitgevoerd.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>De ontvangst registreren van de hoeveelheden die zijn ontvangen op de tweede lading en de meergeleverde hoeveelheid verantwoorden

Voor dit scenario zal de ontvangstmedewerker de inkomende hoeveelheid registreren die hoger is dan de hoeveelheid op de lading. De meerontvangst wordt toegestaan omdat het systeem is ingesteld voor het toestaan van meerlevering.

1. Meld u aan bij magazijn 24 met uw mobiele apparaat. (In de standaard demogegevens meldt u zich aan met _24_ als gebruikers-id en _1_ als wachtwoord.)
1. Selecteer de menuoptie _Artikelontvangst laden_ die u voor dit scenario hebt gemaakt.
1. Voer de volgende waarden in aan de hand van de instructies voor gegevensinvoer op het scherm. (De volgorde kan variëren, afhankelijk van het mobiele apparaat of de emulator die u gebruikt.)

    - **Lading**: voer de id in van de tweede lading die u eerder hebt gemaakt.
    - **Artikel**: voer _A0001_ in. Dit is het artikel dat wordt verwacht voor deze lading.
    - **Hoeveelheid**: geef _7_ op. Dit is de resterende hoeveelheid die de leverancier mag leveren als onderdeel van de totale inkooporderhoeveelheid van 12 (waarbij 10 de oorspronkelijke orderhoeveelheid is en 2 de toegestane meerleveringshoeveelheid van 20 procent). Houd er rekening mee dat 5 stuks al zijn geregistreerd voor de eerste lading.

De tweede lading is nu bijgewerkt met de hoeveelheid van 7 en de productontvangst kan worden bijgewerkt op basis van deze hoeveelheid.

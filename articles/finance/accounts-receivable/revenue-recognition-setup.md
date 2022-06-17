---
title: Instellingen opbrengsttoerekening
description: In dit artikel worden de instellingsopties voor de toerekening van opbrengsten en de implicaties hiervan beschreven.
author: kweekley
ms.date: 04/28/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: ef294af8d3a8f39a80b98aeba293267dcca1f29b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900008"
---
# <a name="revenue-recognition-setup"></a>Instellingen opbrengsttoerekening
[!include [banner](../includes/banner.md)]

Er is een nieuwe module **Opbrengsttoerekening** toegevoegd die menu-items bevat voor alle vereiste instellingen. In dit artikel worden de instellingsopties en de implicaties ervan beschreven.

> [!NOTE]
> De functie voor opbrengsttoerekening is nu standaard ingeschakeld via Functiebeheer. Als uw organisatie deze functie niet gebruikt, kunt u deze uitschakelen in de werkruimte van **Functiebeheer**.
>
> Opbrengsttoerekening, inclusief bundelfunctionaliteit, wordt niet ondersteund in Commerce-kanalen (e-commerce, POS en callcenter). Artikelen die zijn geconfigureerd voor opbrengsttoerekening, mogen niet worden toegevoegd aan orders of transacties die zijn gemaakt in Commerce-kanalen.

De module **Opbrengsttoerekening** bevat de volgende configuratieopties:

- Journalen voor opbrengsttoerekening
- Parameters voor toerekening van opbrengsten
- Opbrengstschema's 
- Voorraadinstellingen

    - Artikelgroepen en vrijgegeven producten
    - Opbrengstschema definiëren
    - Opbrengstprijs definiëren
    - Voorraadinstellingen

        - Opbrengstschema definiëren
        - Opbrengstprijs definiëren

    - Boekingsprofielen
    - Bundels

        - Bundelcomponenten
        - Bundelartikel

- Projectinstellingen

## <a name="revenue-recognition-journals"></a>Journalen voor opbrengsttoerekening

Er is een nieuw journaaltype geïntroduceerd voor het toerekenen van opbrengsten. Het journaal is vereist en wordt in twee scenario's gebruikt.

Het eerste scenario doet zich voor nadat aan alle contractuele verplichtingen is voldaan, als de uitgestelde opbrengst wordt toegerekend door een journaal voor opbrengsttoerekening te maken dat is gebaseerd op de details van het opbrengstschema. Het journaal bevat een journaalregel waarmee het saldo van de grootboekrekening voor uitgestelde opbrengst wordt verplaatst naar de grootboekrekening voor opbrengst.

Het tweede scenario doet zich voor als een journaal wordt gemaakt nadat hertoewijzing is uitgevoerd. Hertoewijzing vindt plaats wanneer een verkooporderregel aan een eerder gefactureerde verkooporder wordt toegevoegd of wanneer een nieuwe verkooporder wordt gemaakt die een regel bevat die deel uitmaakt van het oorspronkelijke contract. Als een factuur werd geboekt voordat de nieuwe verkooporderregel was toegevoegd, moet er een corrigerende journaalregel worden gemaakt voor de geboekte klantfactuur.

Het journaal kan worden ingesteld op de pagina **Journaalnamen** (**Opbrengsttoerekening \> Instellingen \> Journaalnamen**). Het journaaltype moet worden ingesteld op **Opbrengsttoerekening**. 

## <a name="parameters-for-revenue-recognition"></a>Parameters voor toerekening van opbrengsten

De instellingen voor opbrengsttoerekening worden geconfigureerd op het tabblad **Opbrengsttoerekening** van de pagina **Grootboekparameters** (**Opbrengsttoerekening \> Instellingen \> Grootboekparameters**). De volgende instellingen zijn beschikbaar:

- **Naam journaal voor opbrengsttoerekening**: selecteer het journaal dat is gemaakt voor de toerekening van opbrengst. Het journaal is vereist wanneer de opbrengst wordt toegerekend vanuit het opbrengstschema of wanneer u een hertoewijzing uitvoert voor een verkooporder die al is gefactureerd.
- **Methode voor toewijzing van korting inschakelen**: stel deze optie in op **Ja** om de opbrengstprijs te bepalen door toewijzing van de billijke marktwaarde die voor elk vrijgegeven product is gedefinieerd bij de opbrengstprijs. Deze toewijzing omvat onder andere het toewijzen van eventuele regelkortingen voor de artikelen. Als deze optie is ingesteld op **Nee** gebruikt het systeem de gemiddelde prijs die voor elk vrijgegeven product is gedefinieerd in de opbrengstprijs. Als deze optie is ingesteld op **Nee** maar er geen gemiddelde prijs is ingesteld voor de vrijgegeven producten, wordt de toewijzing van de opbrengstprijs niet uitgevoerd.
- **Kortingen in koptekst opnemen**: stel deze optie in op **Ja** om de opbrengstprijs te bepalen door kortingen in de koptekst toe te wijzen aan producten. Als deze optie is ingesteld op **Nee** wordt de korting in de koptekst niet opgenomen in de toewijzing van de opbrengstprijs.
- **Contractvoorwaarden uitschakelen**: stel deze optie in op **Ja** als producten met het opbrengsttype **Contractondersteuning boeken** kunnen worden vrijgegeven, zelfs als er voor de producten geen begin- en einddatum voor het contract zijn gedefinieerd. Normaal gesproken zijn er voor het contract begin- en einddatums vereist voor artikelen met het opbrengsttype **Contractondersteuning boeken**. Wanneer de begin- en einddatum van het contract niet worden gedefinieerd, worden de details van het opbrengstschema voor de boeking berekend met behulp van het aantal voorvallen en de factuurdatum.
- **Factuurcorrecties naar klanten boeken bij hertoewijzing**: wanneer u hertoewijzing uitvoert voor facturen die al zijn geboekt, moet de journaalregel voor de geboekte factuur worden gecorrigeerd. Gebruik deze optie om op te geven hoe de correctie moet worden uitgevoerd.

    - Stel deze optie in op **Nee** om het boeken van de corrigerende transactie naar het grootboek te beperken. Als deze optie is ingesteld op **Nee** worden er geen extra documenten gemaakt in Klanten voor de interne boekhoudcorrectie. Wanneer de factuur is betaald, wordt tijdens het vereffeningsproces de oude journaalregel gebruikt om contantkortingen of gerealiseerde winsten of verliezen te boeken.
    - Stel deze optie in op **Ja** om voor de corrigerende transactie automatisch een terugboekingsdocument en een nieuwe factuur te maken in Klanten. Omdat deze correctie een interne boekhoudcorrectie is, worden de nieuwe documenten niet naar de klant verzonden of aan de klant gemeld. Het terugboekingsdocument wordt vereffend met de oorspronkelijke factuur en de nieuwe gecorrigeerde factuur wordt door de klant betaald. Zoals u zult zien, worden alle drie de documenten weergegeven in rapporten, zoals het klantoverzicht.

[![Instellingsgegevens.](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Opbrengstschema's

Er moet een opbrengstschema worden gemaakt voor elk voorval waarvoor de opbrengst kan worden uitgesteld. Als uw organisatie bijvoorbeeld ondersteuning biedt voor perioden van 6, 12, 18 en 24 maanden, moet u voor elke periode een opbrengstschema maken. De instellingen van het opbrengstschema bepalen hoe de opbrengstprijs wordt verspreid over het aantal perioden dat u selecteert. Dit bepaalt ook welke standaarddatums worden ingevoerd voor het opbrengstschema dat wordt gemaakt als de factuur wordt geboekt.

Als u opbrengsten per mijlpaal toekent, kunt u het beste een schema voor de toerekening van opbrengsten maken voor het aantal mijlpalen, ongeacht de toerekeningsdatums. Nadat u de schema's hebt gemaakt, kunt u deze bewerken zodat ze de verwachte mijlpaaldatums bevatten. U kunt deze records in de wachtstand plaatsen totdat u wordt gewaarschuwd dat de mijlpaal is gehaald en de opbrengst kan worden toegerekend.

De opbrengstschema's worden gemaakt op de pagina **Opbrengstschema's** (**Opbrengsttoerekening \> Instellingen \> Opbrengstschema's**).

[![Opbrengstschema's.](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Geef beschrijvende waarden op in de velden **Opbrengstschema** en **Beschrijving**. De volgende aanvullende instellingen worden gebruikt om het opbrengstschema te maken als de factuur wordt geboekt.

- **Voorvallen**: voer voor het uitstellen van de opbrengst het aantal maanden of voorvallen in.
- **Automatisch in wachtstand plaatsen**: schakel dit selectievakje in als alle regels van het opbrengstschema automatisch in de wachtstand moeten worden geplaatst wanneer de factuur wordt geboekt. De wachtstand moet handmatig van elke regel van het schema worden verwijderd voordat de uitgestelde opbrengst van de regel kan worden toegerekend.
- **Automatische contractvoorwaarden**: schakel dit selectievakje in als de begin- en einddatum van het contract automatisch moeten worden ingesteld. Deze datums worden automatisch ingesteld voor vrijgegeven producten van het opbrengsttype **Contractondersteuning boeken**. De begindatum van het contract wordt automatisch ingesteld op de gewenste verzenddatum van de verkooporderregel, en de einddatum van het contract wordt automatisch ingesteld op de begindatum plus het aantal maanden of voorvallen dat is gedefinieerd bij de instellingen van het opbrengstschema. Het product op de verkooporderregel heeft bijvoorbeeld een garantieperiode van één jaar. Het standaard opbrengstschema is **12M** (12 maanden) en het selectievakje **Automatische contractvoorwaarden** is voor dit opbrengstschema ingeschakeld. Als de verkooporderregel een gewenste verzenddatum heeft van 16 december 2019, is de begindatum van het contract standaard 16 december 2019 en is de einddatum van het contract standaard 15 december 2020.
- **Toerekeningsbasis**: de toerekeningsbasis bepaalt hoe de opbrengstprijs wordt toegewezen aan de diverse voorvallen.

    - **Maandelijks op dagen**: het bedrag wordt toegewezen op basis van de werkelijke dagen in elke kalendermaand.
    - **Maandelijks**: het bedrag wordt gelijkmatig verspreid over het aantal maanden dat is gedefinieerd voor de voorvallen.
    - **Voorvallen**: het bedrag wordt gelijkmatig verdeeld over de voorvallen, maar kan een extra periode bevatten als u de **Werkelijke begindatum** als de toerekeningsconventie selecteert.
    - **Boekperioden op dagen**: het bedrag wordt toegewezen op basis van de werkelijke dagen in elke boekperiode. 

         - De resultaten van **Maandelijks op dagen** en **Boekperiode op dagen** zijn gelijk wanneer de boekperioden de kalendermaanden volgen. De enige uitzondering is wanneer de toerekeningsconventie is ingesteld op **Einde maand/periode** en de velden **Begindatum** en **Einddatum** van het contract leeg zijn op een verkooporderregel.

- **Toerekeningsconventie**: de toerekeningsconventie bepaalt de datums die zijn ingesteld voor het opbrengstschema voor de factuur.

    - **Werkelijke begindatum**: het schema wordt gemaakt met de begindatum van het contract (voor PCS-artikelen \[Contractondersteuning boeken\]) of met de factuurdatum (voor essentiële en niet-essentiële artikelen).
    - **1e van maand/periode**: de datum op de eerste schemaregel is de begindatum van het contract (of de factuurdatum). Alle volgende schemaregels worden echter voor de eerste van de maand of boekperiode gemaakt.
    - **Midden maand - gesplitst**: de datum op de eerste schemaregel hangt samen met de factuurdatum. Als de factuur wordt geboekt op een datum tussen de eerste en de vijftiende van de maand, wordt het opbrengstschema gemaakt op basis van de eerste dag van de maand. Als de factuur wordt geboekt op de zestiende van de maand of later, wordt het opbrengstschema gemaakt op basis van de eerste dag van de volgende maand.

        - **Midden maand - gesplitst** kan niet worden geselecteerd als de toerekeningsbasis is ingesteld op **Boekperiode op dagen**.

    - **1e dag van de volgende maand/periode**: de datum waarop het schema begint, is de eerste dag van de volgende maand of boekperiode.
    - **Einde van maand/periode**: de datum op de eerste schemaregel is de begindatum van het contract (of de factuurdatum). Alle volgende schemaregels worden echter voor de laatste dag van de maand of boekperiode gemaakt. 

Selecteer de knop **Details van het schema voor opbrengsttoerekening** om de algemene perioden en percentages weer te geven die in elke periode worden toegerekend. De waarde voor **Percentage toerekenen** wordt standaard verdeeld over het aantal perioden. Als de toerekeningsbasis is ingesteld op **Maandelijks**, kan het toerekeningspercentage worden gewijzigd. Tijdens het wijzigen van het toerekeningspercentage, wordt er een waarschuwingsbericht weergegeven met de melding dat het totaal niet gelijk is aan 100 procent. Als u dit bericht ontvangt, kunt u doorgaan met het bewerken van regels. Het totale percentage moet echter gelijk zijn aan 100 voordat u de pagina sluit.

[![Details van opbrengstschema.](./media/revenue-schedule-details-2nd-scrn.png)](./media/revenue-schedule-details-2nd-scrn.png)

## <a name="inventory-setup"></a>Voorraadinstellingen

U kunt opbrengst voor vrijgegeven producten op verkooporders toerekenen, echter niet als er verkoopcategorieën op de verkooporders voorkomen of bij vrije-tekstfacturen, als er geen artikelen in het document zijn opgenomen. De selecties die u maakt wanneer u vrijgegeven producten instelt, bepalen hoe de opbrengst van het artikel wordt toegerekend. De selecties bepalen bijvoorbeeld of de opbrengstprijs wordt toegewezen en of de opbrengst wordt uitgesteld door een opbrengstschema te gebruiken.

U kunt de instellingen starten op het sneltabblad **Opbrengsttoerekening** van de pagina **Artikelgroep** (**Opbrengsttoerekening \> Instellingen \> Voorraad- en productinstellingen \> Artikelgroep**). Deze pagina bevat verschillende instellingsvelden. Deze velden worden gebruikt om standaardwaarden in te stellen voor nieuwe vrijgegeven producten die in het systeem worden gemaakt. Wanneer er nieuwe producten worden gemaakt, worden de waarden die u hier instelt standaard ingevoerd voor de artikelgroep. U kunt de standaardwaarden voor vrijgegeven producten overschrijven op de pagina **Vrijgegeven producten** (**Opbrengsttoerekening \> Instellingen \> Voorraad- en productinstellingen \> Vrijgegeven producten**). De standaardwaarden die voor de vrijgegeven producten zijn ingesteld, worden vervolgens naar de verkooporder getransporteerd.

## <a name="item-groups-and-released-products"></a>Artikelgroepen en vrijgegeven producten

### <a name="define-the-revenue-schedule"></a>Het opbrengstschema definiëren

Opbrengst op de verkooporderregel wordt uitgesteld als er een opbrengstschema wordt gedefinieerd voor het vrijgegeven product en standaard op de verkooporderregel wordt gebruikt. Als de instelling standaard voor het product moet worden gebruikt, kunt u het opbrengstschema definiëren op het sneltabblad **Opbrengsttoerekening** van de pagina **Artikelgroep** (**Opbrengsttoerekening \> Instellingen \> Voorraad- en productinstellingen \> Artikelgroep**). U kunt ook de instelling voor het vrijgegeven product definiëren op het sneltabblad **Opbrengsttoerekening** van de pagina **Vrijgegeven producten** (**Opbrengsttoerekening \> Instellingen \> Voorraadinstellingen \> Vrijgegeven producten**).

Selecteer in het veld **Opbrengstschema** het opbrengstschema dat de periode aanduidt waarvoor de opbrengst moet worden uitgesteld. Het opbrengstschema wordt automatisch ingevoerd op de verkooporderregel en de schemadetails worden gemaakt op het moment dat de verkooporderfactuur wordt geboekt.

### <a name="define-the-revenue-price"></a>De opbrengstprijs definiëren

Artikelgroepen en vrijgegeven producten kunnen worden ingesteld met behulp van de gemiddelde prijzen-methode of de methode voor het toewijzen van kortingen. Voor beide methoden zijn diverse instellingen vereist op de pagina **Vrijgegeven producten**:

- **Is de opbrengsttoewijzing actief**: stel deze optie op **Ja** als u het vrijgegeven product wilt opnemen in de berekening van de opbrengsttoewijzing. Als deze optie is ingesteld op **Nee** gebruikt het vrijgegeven product de gemiddelde prijs-methode als de gemiddelde prijs is gedefinieerd. Als de gemiddelde prijs niet is gedefinieerd, wordt de eenheidsprijs op de verkooporderregel gebruikt om opbrengst of uitgestelde opbrengst te boeken.
- **Opbrengsttype**: selecteer het opbrengsttype dat het vrijgegeven product aanduidt:

    - **Essentieel** : het artikel is een primaire opbrengstenbron van een organisatie. Deze waarde is de standaardinstelling.
    - **Niet-essentieel**: het artikel is geen primaire opbrengstenbron van een organisatie. Wanneer de gemiddelde-prijsinstellingen worden gebruikt, wordt de prijs aangepast tot deze gelijk is aan de gemiddelde prijs en vervolgens toegewezen. Een essentieel artikel heeft bijvoorbeeld een vaste prijs die moet worden toegerekend aan de opbrengst. Als er een korting is, kan de korting worden gehaald uit de opbrengst van het essentiële artikel, maar **alleen** tot het vaste-prijsbedrag is bereikt. De rest van de korting wordt uit de opbrengst voor niet-essentiële artikelen gehaald. Het is ook mogelijk dat de korting niet uit de opbrengst van het essentiële artikel wordt gehaald.
    - **Contractondersteuning boeken**: het artikel ondersteunt andere elementen die in de verkoop aan de klant worden opgenomen. De opbrengstprijs wordt verdeeld over de essentiële en niet-essentiële producten die in de verkoop zijn opgenomen. Afhankelijk van de instellingen, is het voor PCS-artikelen niet vereist om een begin- en einddatum van het contract te definiëren op de verkooporderregel.

- **Uitsluiten van aanpassing**: stel deze optie in op **Ja** om aan te geven dat de gemiddelde prijs van het artikel niet kan worden aangepast onder het minimumpercentage dat is gedefinieerd, of boven het maximumpercentage. De opbrengstprijs wordt afgeleid van de opbrengstprijs van een ander vrijgegeven product dat is opgenomen in de verkooporder. Als deze optie is ingesteld op **Nee** kan de gemiddelde prijs van het artikel worden aangepast of uit de opbrengsten worden gehaald. Als u meer dan één artikel verkoopt dat is ingesteld als gemiddelde prijs, moet er minimaal één vrijgegeven product worden ingesteld waarbij de optie **Uitsluiting van aanpassing** is ingesteld op **Nee**. Op deze manier is er minimaal één artikel waaraan eventuele verschillen in de opbrengstprijs kunnen worden toegewezen.
- **Gemiddelde prijs**: stel deze optie in op **Ja** om aan te geven dat de opbrengstprijs van het artikel moet worden aangepast, zodat deze gelijk is aan de gemiddelde prijs als deze onder de minimumtolerantie valt die u opgeeft, of boven de maximumtolerantie uitkomt en het uit de opbrengst gehaalde bedrag moet worden toegewezen aan regels met producten waarvoor de optie **Uitsluiten van aanpassing** is ingesteld op **Nee**.

    - **Maximumtolerantie**: voer het percentage boven de gemiddelde prijs in dat is toegestaan.
    - **Minimumtolerantie**: voer het percentage onder de gemiddelde prijs in dat is toegestaan.

Nadat u de instellingen voor het vrijgegeven product hebt geconfigureerd, moet u de opbrengstprijs handmatig definiëren door de reële prijswaarde of de gemiddelde prijs in te voeren (als u de gemiddelde prijs-methode gebruikt) op de pagina **Opbrengstprijzen** (ga naar **Opbrengsttoerekening \> Instellingen \> Voorraadinstellingen \> Vrijgegeven producten** en selecteer vervolgens in het actiepaneel op het tabblad **Verkopen** in de groep **Opbrengsttoerekening** de optie **Opbrengstprijzen**).

[![Opbrengstprijzen.](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

De opbrengstprijs die op deze pagina handmatig wordt gedefinieerd, wordt gebruikt om de toewijzing van de opbrengstprijs voor elke verkooporder te bepalen op basis van de criteria die zijn gedefinieerd. Elk criterium wordt afgestemd op de verkooporderregel om de opbrengstprijs te bepalen die in het toewijzingsproces moet worden gebruikt.

- **Artikelcode** en **Artikelrelatie** : er kan een opbrengstprijs worden gedefinieerd voor een afzonderlijk product of een groep producten. Als u **Tabel** selecteert in het veld **Artikelcode**, selecteert u het vrijgegeven product in het veld **Artikelrelatie**. Als u **Groep** selecteert in het veld **Artikelcode**, selecteert u de artikelgroep in het veld **Artikelrelatie**.
- **Rekeningcode** en **Rekening/groepsnummer**: een opbrengstprijs kan worden gedefinieerd voor alle klanten, een individuele klant of een groep klanten. Als u **Alle** selecteert in het veld **Rekeningcode** wordt de prijs voor alle klanten gebruikt. Als u **Tabel** selecteert in het veld **Rekeningcode**, selecteert u de klant in het veld **Rekening/groepsnummer**. Als u **Groep** selecteert in het veld **Rekeningcode**, selecteert u de klantengroep in het veld **Rekening/groepsnummer**.
- **Valuta**: u moet een afzonderlijke opbrengstprijs invoeren voor elke valuta waarin u een verkooporder invoert. Als u momenteel bijvoorbeeld uw verkooptransacties uitvoert in Amerikaanse dollars, Canadese dollars en euro's, moet u een opbrengstprijs in alle drie de valuta's definiëren. De opbrengstprijs wordt niet omgerekend vanuit één valuta, zoals de valuta voor boekhouding, naar andere eventuele transactievaluta's die u gebruikt.
- **Bedrag of percentage van catalogusprijs**: geef op of de opbrengstprijs is ingesteld als een bedrag of als een percentage van de catalogusprijs. Als u **Percentage van catalogusprijs** selecteert, kunnen gebruikers de gemiddelde prijs invoeren als een percentage van de catalogusprijs in plaats van een bedrag. De waarde van **Percentage van catalogusprijs** wordt alleen gebruikt voor vrijgegeven producten die zijn ingesteld als PCS-artikelen.
- **Opbrengsttoewijzingsprijs**: afhankelijk van de waarde die u hebt geselecteerd in het veld **Bedrag of percentage van catalogusprijs**, voert u een bedrag of een percentage in voor de opbrengstprijs die wordt gebruikt om de opbrengst toe te wijzen aan alle elementen op de verkooporder.
- **Begindatum** en **Einddatum**: voer het datumbereik in waarvoor de opbrengstprijs van toepassing is. Deze velden zijn optioneel.

Als de optie **Methode voor toewijzing van korting inschakelen** op de pagina **Grootboekparameters** is ingesteld op **Ja** en als het veld **Opbrengsttype** voor uw vrijgegeven product is ingesteld op **Contractondersteuning boeken**, moet u ook de artikelen opgeven die door het vrijgegeven product worden ondersteund. Deze instellingen worden ingesteld op de pagina **Basis instellen** (ga naar **Opbrengsttoerekening \> Instellingen \> Voorraadinstellingen \> Vrijgegeven producten** en selecteer vervolgens in het actiepaneel op het tabblad **Verkopen** in de groep **Opbrengsttoerekening** de optie **Basis instellen**).

Voeg op de pagina **Basis instellen** een record toe voor elke artikelengroep waarvoor het artikel ondersteuning biedt. Wanneer de opbrengsten worden toegewezen, wordt de opbrengstprijs verdeeld over de essentiële en niet-essentiële componenten voor het PCS-artikel.

### <a name="posting-profiles"></a>Boekingsprofielen

Er zijn drie aanvullende boekingstypen die de mogelijkheid ondersteunen om opbrengst uit te stellen. Deze boekingstypen worden ingesteld op het tabblad **Verkooporder** van de pagina **Boeking** (**Opbrengsttoerekening \> Instellingen \> Voorraad- en productinstellingen \> Boeking**).

- **Uitgestelde opbrengst**: voer de hoofdrekening in voor de opbrengstprijs die wordt geboekt naar uitgestelde opbrengst (in plaats van naar opbrengst). De opbrengstprijs wordt uitgesteld als de verkooporderregel een opbrengstschema bevat.
- **Uitgestelde kosten van verkochte goederen**: voer de hoofdrekening in voor de kosten van het bedrag van de verkochte goederen die worden geboekt naar uitgestelde kosten van verkochte goederen als de opbrengst ook wordt uitgesteld.
- **Vereffening opbrengst gedeeltelijke factuur**: voer de hoofdrekening in voor de vereffeningsrekening die wordt gebruikt wanneer de verkooporder gedeeltelijk wordt gefactureerd of wanneer er hertoewijzing plaatsvindt. Het saldo op deze rekening wordt weer 0 (nul) wanneer de verkooporders volledig zijn gefactureerd.

### <a name="bundles"></a>Bundels

Bundelartikelen zijn unieke vrijgegeven producten die zo zijn ingesteld dat ze componenten bevatten. Deze instelling kan worden uitgevoerd met behulp van de stuklijstfunctionaliteit. Wanneer een bundelartikel op een verkooporder wordt ingevoerd, worden de afzonderlijke componenten gebruikt om de opbrengstprijzen en opbrengstschema's vast te stellen. Op afgedrukte documenten voor de klant, zoals de verkooporder en de factuur, wordt echter het bundelartikel weergegeven.

#### <a name="bundle-components"></a>Bundelcomponenten

De componenten die deel uitmaken van de bundel, moeten worden ingesteld op de pagina **Vrijgegeven producten** (**Opbrengsttoerekening \> Instellingen \> Voorraad- en productinstellingen \> Vrijgegeven producten**). Deze componenten zijn vrijgegeven producten en moeten op dezelfde manier worden ingesteld als producten die zijn opgenomen in een stuklijst. Een vrijgegeven product kan bijvoorbeeld een artikel van het type **Artikel** of van het type **Service** zijn, maar het moet worden toegewezen aan een artikelmodelgroep waar de optie **Product in voorraad** is ingesteld op **Ja**. Zie de documentatie voor stuklijstartikelen voor meer informatie.

De componenten moeten ook worden ingesteld voor opbrengsttoerekening, net alsof het producten zijn die afzonderlijk via een verkooporder kunnen worden verkocht. Controleer bijvoorbeeld of de juiste opbrengstprijs is gedefinieerd voor elke component en of de prijsbasis is ingesteld voor PCS-artikelen.

#### <a name="bundle-items"></a>Bundelartikelen

Als u een bundelartikel instelt, moet u twee velden instellen op de pagina **Vrijgegeven producten** (**Opbrengsttoerekening \> Instellingen \> Voorraad- en productinstellingen \> Vrijgegeven producten**):

- Op het sneltabblad **Technicus** in het veld **Productietype** moet het artikel worden ingesteld als een stuklijstartikel.
- Op het sneltabblad **Algemeen** in het veld **Bundel** moet het artikel zijn gemarkeerd als een bundelartikel.

De componenten moeten vervolgens worden toegewezen aan het hoofdartikel van de bundel/stuklijst op de pagina **Stuklijstversies** (ga naar **Opbrengsttoerekening \> Instellingen \> Voorraad- en productinstellingen \> Vrijgegeven producten** en selecteer vervolgens in het actiepaneel op het tabblad **Technicus** in de groep **Stuklijst** de optie **Stuklijstversies**). Zie de documentatie over het instellen van stuklijsten voor meer informatie.

[![Vrijgegeven producten, stuklijstschema's.](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Als het hoofdartikel en de bundelcomponenten zijn ingesteld om te worden toegewezen, wordt de opbrengstprijs van de bundel gedistribueerd naar de componenten op basis van de percentages waarmee ze aan de opbrengst bijdragen.

## <a name="project-setup"></a>Projectinstellingen

Opbrengsttoerekening kan ook worden gebruikt voor verkooporders die zijn gemaakt via een tijd- en materiaalproject. Voor verkooporders die afkomstig zijn van projecten, hoeft u alleen de hoofdrekeningen te definiëren in de projectboekingsprofielen die worden gebruikt voor het boeken van projectfacturen. De hoofdrekeningen worden gedefinieerd op de pagina **Boeking in grootboek instellen** (**Opbrengsttoerekening \> Instellingen \> Projectinstellingen \> Boeking in grootboek instellen**).

- **Uitgestelde factuuropbrengst** (onder **Opbrengstrekeningen**): voer de hoofdrekening in voor de opbrengstprijs die wordt geboekt naar uitgestelde opbrengst (in plaats van naar opbrengst). De opbrengstprijs wordt uitgesteld als de verkooporderregel een opbrengstschema bevat.
- **Uitgestelde kosten** (onder **Kostenrekeningen**): voer de hoofdrekening in voor de kosten van het bedrag van de verkochte goederen die worden geboekt naar uitgestelde kosten van verkochte goederen als de opbrengst ook wordt uitgesteld.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

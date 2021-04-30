---
title: Aan de slag met Activalease
description: In dit onderwerp wordt de functie Activalease beschreven en wordt u begeleid bij de stappen voor het maken van een activalease en leert u informatie voor deze leases weer te geven.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeasingWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8141badab2561707e2055d7084323ed4310d2421
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892428"
---
# <a name="asset-leasing-get-started"></a>Aan de slag met Activalease

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de functie Activalease beschreven en wordt u begeleid bij de stappen voor het maken van een activalease en leert u informatie voor deze leases weer te geven. In het onderwerp wordt ook de terminologie gedefinieerd die wordt gebruikt in de gebruikersinterface en de documentatie. Activalease is een geavanceerde functie voor het beheren, bijhouden en automatiseren van financiële transacties voor geleasde activa in Microsoft Dynamics 365 Finance. Activalease voldoet aan de internationale boekhoudstandaarden (IFRS 16) en de US GAAP-normen (ASC 842). In Activalease worden de gegevens over de leases vastgelegd en verwerkt en worden journaalboekingen gegenereerd voor de gehele levenscyclus van de lease, vanaf de eerste toerekening, maandelijkse journaalboekingen, tot en met waardevermindering en beëindiging van de lease. Activalease wordt naadloos geïntegreerd met andere componenten van Dynamics 365 Finance, zoals Vaste activa, Leveranciers en Grootboek.

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied **Functiebeheer** gebruiken om de status van de functie te controleren en desgewenst in te schakelen. Zoek in het werkgebied **Functiebeheer** de functie **Activaleasing** en klik op de knop **Nu inschakelen**.

Zie de standaarddocumentatie voor IFRS 16 en US GAAP ASC 842 voor meer informatie over boekhoudstandaarden.

## <a name="asset-leasing-elements"></a>Elementen van activalease
In het volgende diagram worden de belangrijkste elementen van het bedrijfsproces voor leases weergegeven.

[![Elementen van activalease](./media/overview-01.png)](./media/overview-01.png)

Een geleasd activum bevat de volgende hoofdcomponenten:

- **Leaseovereenkomst**: de leaseverstrekker is eigenaar van het activum en komt met de leasenemer overeen om een activum te leasen voor een bepaalde periode in ruil voor periodieke leasebetalingen. Naast de juridische overeenkomst tussen de leaseverstrekker en de leasenemer worden in de leaseovereenkomst beheerbeslissingen vastgelegd, zoals de waarschijnlijkheid van het toepassen van een verlengingsoptie en eigendomsoverdracht.

- **Leaseberekening en classificatie per boekhoudstandaard**: met de leaseberekening en -classificatie wordt de boekhoudstandaard aangegeven die wordt toegepast bij de eerste en de latere meting, alsmede de classificatietest waarmee wordt bepaald wat het leasetype is. Een lease kan een financiële lease zijn, een operationele lease, een kortlopende lease of een lease met geringe waarde. Het systeem berekent ook de huidige nettowaarde van toekomstige minimale leasebetalingen met het oog op waardering en classificatie.

- **Leasetransacties**: Activalease ondersteunt de eerste toerekening van het activum met gebruiksrecht voor leases op de balans, alsmede volgende metingen voor leases op de balans of leases niet op de balans. Met de transactie van eerste toerekening wordt de huidige nettowaarde van toekomstige minimale leasebetalingen gemeten. Deze gegevens worden gebruikt om de waarde van het eerste activum met gebruiksrecht en leaseverplichtingen te bepalen, die van invloed zijn op de balans van de organisatie. De volgende meting van maandelijkse leasetransacties heeft betrekking op de accumulatie van rente over de leaseverplichting, waarmee de leaseverplichting wordt verhoogd. Ook wordt de toerekening van leasebetalingen gemeten waarmee de leaseverplichting wordt verlaagd en die later aan de leaseverstrekker wordt betaald. De meting omvat ook de afschrijving van het activum met gebruiksrecht.

  Voor leases buiten de balans berekent het systeem de lineaire leasekosten over dat wat minder is: de economische levensduur van het activum of de leaseperiode. Met leasecorrecties worden contractwijzigingen, zoals een lease-uitbreiding, en de waardeverminderingstransactie gemeten waarin het activum met gebruiksrecht voor niet-terugvorderbare kosten wordt gebruikt.

  Activalease wordt geïntegreerd met Grootboek om ervoor te zorgen dat uw rekeningschema met alle geboekte leasetransacties wordt bijgewerkt. Activalease wordt geïntegreerd met Leveranciers om facturen van de leaseverstrekker bij te houden in Leveranciers en toekomstige betalingen vanuit Leveranciers te verrichten. Dankzij de integratie met Vaste activa kunt u vanuit Vaste activa leases in het register van vaste activa bijhouden en transacties voor activa met gebruiksrecht boeken, zoals de eerste toerekening, afschrijving en waardevermindering van het activum.   

## <a name="asset-leasing-components"></a>Componenten van Activalease 
In Activalease worden leasegegevens, betalingsschema's, begin- en einddatums en de betalingsfrequentie toegewezen. Ook worden berekeningen van de huidige nettowaarde, maandelijkse leasebetalingen, rente en lease-afschrijving geautomatiseerd. Het systeem voert leaseclassificatietests uit, afhankelijk van de configuratie. Ook worden de bijbehorende leasetransacties gemaakt en geboekt, die zijn gebaseerd op het kader dat is gedefinieerd door de boekhoudstandaard die u volgt.

In het volgende diagram ziet u het leaseboek, de lease, het berekende betalingsschema, de classificatietests voor leases en leaseboeken en de bijbehorende boekhoudtransacties.

[![Leasen, leaseboek en betalingsschema](./media/overview-02.png)](./media/overview-02.png)

- **Leaseboek**: het leaseboek bevat alle informatie over leasecontracten, zoals de leasevoorwaarden, de reële waarde en leasebetalingen. Het bevat ook de boekhoudstandaard die u volgt, het leasetype en de drempels die in aanmerking worden genomen bij de leaseclassificatietest. Het leaseboek bevat ook de leasetransacties die naar het grootboek zijn geboekt. 
  
- **Lease**: de lease bevat de activaleasegegevens die de basis vormen van de activalease. De leasegegevensbron is het leasecontract en de beheerbeslissing die beide worden uitgevoerd buiten Dynamics 365 Finance. De reële waarde van het activum is de prijs die voor een activum wordt betaald in een transactie op de datum van meting. Deze waarde kan afhankelijk zijn van het activumtype, de marktvoorwaarden en andere criteria die in aanmerking kunnen worden genomen bij de evaluatie. De reële waarde van het activum wordt in aanmerking genomen in de classificatietestvergelijking.

- **Economische levensduur activum**: dit zijn de resterende perioden van de economische levensduur van een activum vanaf de begindatum van de lease. De economische levensduur van een activum wordt in aanmerking genomen in de classificatietestvergelijking. Deze verschilt van de economische levensduur zoals gedefinieerd in Vaste activa.

- **Verhoogd leningtarief**: dit is het rentepercentage dat wordt gebruikt om de huidige nettowaarde te berekenen. Het systeem gebruikt het impliciete tarief als het is gedefinieerd in de leasegegevens om de huidige nettowaarde van de leasebetalingen te berekenen. Als het impliciete tarief niet is gedefinieerd, gebruikt het systeem het verhoogde leningtarief.

- **Type annuïteit**: dit is de leasebetaling die verschuldigd is aan het begin van de betalingsperiode of aan het einde van de periode. Dit kan een vooruitbetaling of te betalen annuïteit zijn (aan het begin van de leasebetalingsperiode) of een normale annuïteit (aan het einde van de leasebetalingsperiode).

  De eerste maand wordt als periodenummer nul voor vooruitbetaling beschouwd. De eerste maand wordt beschouwd als periode één voor achterstallige betalingen.

- **Samenstellingsinterval**: hiermee wordt het aantal perioden vertegenwoordigd waarover rente per jaar wordt samengesteld. Dit kan maandelijks zijn (12 perioden per jaar), per kwartaal (4 perioden per jaar), halfjaarlijks (2 perioden per jaar) of jaarlijks (1 periode per jaar). Het aantal perioden wordt meegenomen in de berekening van de huidige nettowaarde.

- **Begindatum**: dit is de datum waarop de leaseverstrekker het activum beschikbaar maakt voor gebruik door de leasenemer. Alle leaseberekeningen en -transacties worden gebaseerd op de begindatum. De begindatum moet aan het begin van een periode (eerste van de maand) zijn om de nauwkeurigheid van volgende berekeningen te garanderen. U kunt het veld **Handtekeningdatum contract** gebruiken om de werkelijke datum waarop het contract is ondertekend in te voeren.

- **Leasetermijn**: dit is de duur van de leaseperiode in maanden.

> [!NOTE] 
> De definitie van de leasetermijn is gebaseerd op het aantal perioden, of intervallen, in de regels van het betalingsschema. Het gedefinieerde aantal intervallen wordt geconverteerd naar maanden.

- **Betalingsschemaregel**: hiermee worden de leasebetalingen per periode vastgelegd. Ook wordt aangegeven of er een vernieuwingsperiode wordt toegepast en opgenomen in de eerste meting van het activum met gebruiksrecht en de leaseverplichtingen. U kunt de begindatum van de verschuldigde leasebetalingen definiëren en de periode-intervallen die de duur van de lease aangeven, dat wil zeggen dagen, maanden of jaren.

- **Betalingsfrequentie**: hiermee wordt aangegeven of de betaling maandelijks, per kwartaal, halfjaarlijks of jaarlijks wordt uitgevoerd. De einddatum wordt automatisch berekend op basis van de begindatum en het aantal ingevoerde perioden.

- **Betalingsschema**: dit is de berekende huidige nettowaarde, gebaseerd op de tijdsduur van de leasebetalingen, het bedrag van de betalingen, de samenstellingsperioden en het type annuïteit.

- **Perioden**: dit zijn de leaseperioden die het samenstellingsinterval en het annuïteitstype aangeven. Het samenstellingsinterval bepaalt hoe perioden worden verdeeld. U kunt de volgende samenstellingsintervallen instellen:

  - Per maand, 12 perioden per jaar
  - Per kwartaal, 4 perioden per jaar
  - Halfjaarlijks, 2 perioden per jaar
  - Jaarlijks, 1 periode per jaar

De eerste periode begint met periode nul als het annuïteitstype te betalen annuïteit is. Anders begint de eerste periode met één als het annuïteitstype achterstallige betalingen is.

- **Maanden**: hiermee wordt het aantal kalendermaanden aangegeven voor de duur van de lease. Het betalingsbedrag is het verschuldigde bedrag zoals gedefinieerd in de betalingsfrequentie. De berekende huidige nettowaarde is de op de huidige nettowaarde gebaseerde leasebetaling per periode, de samenstellingsintervallen en het verhoogde leentarief.

> [!NOTE] 
> De huidige nettowaarde wordt berekend op basis van de verdisconteerde cashflowvergelijking.

- **Boeken**: dit zijn de vooraf geconfigureerde instellingen die aan elke lease worden gekoppeld. Met het boek worden de toegepaste boekhoudstandaard, leasetypen en drempel gedefinieerd die worden gebruikt als de basis voor de classificatietests. Classificatietests worden gebruikt om het leasetype automatisch op te geven.

- **Boekhoudkundig kader**: hiermee wordt de geselecteerde door u ondersteunde boekhoudstandaard weergegeven: IFRS 16 of ASC 842. De boekhoudstandaard wordt toegewezen aan het boek dat is gekoppeld aan de lease. De boekhoudstandaard bepaalt de grootboekrekeningen die in het boekingsprofiel zijn opgegeven.

- **Leasetypen**: hiermee wordt aangegeven welke van de twee typen leases worden gebruikt: een financiële lease of een operationele lease. Bij een financiële lease worden de risico's en beloningen die betrekking hebben op het geleasde activum overgeboekt naar de leasenemer. Bij een operationele lease blijven risico's en beloningen die betrekking hebben op het geleasde activum bij de leaseverstrekker. Een derde optie is een automatische identificatie van het leasetype, financieel of operationeel, op basis van de gedefinieerde drempels in het boek. Deze automatische identificatie wordt uitgevoerd tijdens de herclassificatietest voor de lease.

- **Drempels**: dit wordt in de classificatietests voor leases gebruikt om te bepalen of het activum als een van de volgende mogelijkheden is geclassificeerd:

  - **Leasetermijn**: dit is het percentage van de economische levensduur die in de classificatietest moet worden gebruikt. De lease wordt door het systeem geclassificeerd als financieel als het leasetype is ingesteld op automatisch en als de leasetermijn voor de economische levensduur van het activum groter is dan of gelijk is aan het hier gedefinieerde percentage.

  - **Huidige nettowaarde**: dit is het percentage van de reële waarde van het activum, die in de classificatietest moet worden gebruikt. De lease wordt door het systeem geclassificeerd als financieel als het leasetype is ingesteld op automatisch en als de huidige nettowaarde van toekomstige leasebetalingen voor de reële waarde van het activum groter is dan of gelijk is aan het hier gedefinieerde percentage.

  - **Kortlopend lease**: als de leasetermijn kleiner is dan of gelijk is aan de gedefinieerde waarde, wordt de lease geclassificeerd als een kortlopende lease.

  - **Geringe waarde**: als de reële waarde van het activum kleiner is dan of gelijk is aan de gedefinieerde waarde, wordt de lease geclassificeerd als een lease met geringe waarde.

  - **Leaseclassificatie en -transacties**: de leaseclassificatie is een geautomatiseerd proces om de leases te classificeren op basis van de gedefinieerde drempels in boeken naast andere classificatietestcriteria om te bepalen of de lease een financiële lease, operationele lease, kortlopende lease of lease met geringe waarde is. Dit wordt ook gebruikt om aan te geven of de uitgestelde gebruiksvergoeding wordt gevolgd.

Classificatietests omvatten de overdracht van eigendom, de aankoopoptie, de leasetermijn, de huidige nettowaarde en het unieke activum. In het volgende diagram worden de classificatietests voor de lease getoond.

[![Classificatietests voor lease](./media/overview-03.png)](./media/overview-03.png)

Elk leasetype verwerkt boekhouding anders voor verschillende leasetransacties. De transacties omvatten eerste toerekening, rentelasten, verschuldigde leasebetalingen en lease-afschrijving, en ze zijn gebaseerd op de boekhoudstandaarden die u volgt (IFRS 16 of ASC 842). Grootboekrekeningen worden gedefinieerd op basis van het leaseboekingsprofiel voor elk transactietype en boekhoudkader.

## <a name="asset-leasing-transactions"></a>Transacties voor Activalease

#### <a name="initial-recognition"></a>Initiële toerekening 
Met de eerste toerekening van een geleaset activum wordt de berekende huidige nettowaarde gebruikt, zodat het activum op de balans kan worden gerapporteerd. De journaalregel hiervoor wordt automatisch gegenereerd. Met deze transactie wordt de rekening van het activum met gebruiksrecht gedebiteerd en wordt de passivarekening van de operationele lease gecrediteerd. Dit gaat als volgt: Als een vast activum aan de lease is gekoppeld, wordt de invoer voor eerste toerekening weergegeven als een bijboeking van vaste activa. In dit scenario moet u een boekingsprofiel voor vaste activa definiëren om te boeken naar de rekening van het activum met gebruiksrecht. 

> [!NOTE]
> Operationele leases worden alleen ondersteund door US GAAP ASC 842.

|     Type                                          |     Debet                     |     Krediet                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operationele lease onder US GAAP            |     Activum met gebruiksrecht        |     Verplichtingen operationele lease     |
|     Financiële lease onder IFRS en US GAAP      |     Activum met gebruiksrecht        |     Financiële leaseverplichtingen       |

#### <a name="lease-liability-amortization-interest-expense"></a>Afschrijving van leaseverplichtingen (rentelasten) 
De rente voor een lease wordt toegerekend door rente te berekenen voor het beginsaldo van de lease, de periodeleasebetaling, het verhoogde leningtarief en de samengestelde intervalperioden per jaar. Met het rentebedrag wordt de passivarekening van de operationele lease verhoogd door deze te crediteren. Dit wordt op de balans van de organisatie weergegeven. De transactie bevat ook een debetpost voor de rekening voor rentelasten, die wordt weergegeven in de winst- en verliesrekening voor financiële leases, en voor de rekening voor leasekosten voor operationele leases.

|     Type                                          |     Debet                     |     Krediet                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Invoer van verplichtingen van operationele lease onder US GAAP ASC 842    |     Onkosten van lease         |     Verplichtingen operationele lease         |
|     Invoer van verplichtingen van financiële lease onder IFRS en US GAAP      |     Rente-uitgaven          |     Financiële leaseverplichtingen           |

#### <a name="accrued-lease-payment"></a>Transitorische leasebetaling
Een transitorische leasebetaling wordt toegerekend als een toekomstige leasebetaling die moet worden verwerkt als een betalingstransactie van de bank- of kasrekeningen. Met de leasebetaling die verschuldigd is, worden de leaseverplichtingen verlaagd door de passivarekening van de lease te debiteren op basis van de vraag of de subadministratie van een leverancier in het geval van de leaseverstrekker is gedefinieerd als een leverancier, of door de creditzijde te boeken naar een grootboekrekening voor nog te betalen bedragen. De betaling wordt dan uitgevoerd op basis van de leverancier of de nog te betalen bedragen.

|     Type                                          |     Debet                     |     Krediet                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operationele lease onder US GAAP              |  Verplichtingen operationele lease    |   Leveranciersaansprakelijkheid (subadministratie)/nog te betalen bedragen  |
|     Financiële lease onder IFRS en US GAAP        |  Financiële leaseverplichtingen      |   Leveranciersaansprakelijkheid (subadministratie)/nog te betalen bedragen  |

#### <a name="asset-depreciation"></a>Afschrijving van activa
Het activum met gebruiksrecht wordt afgeschreven over datgene wat minder is, de economische levensduur van het activum of de leasetermijn. De methode voor het berekenen van de afschrijving voor de operationele lease onder US GAAP (ASC 842) is gebaseerd op het verschil tussen de lineaire onkosten van de lease en het rentebedrag. Afschrijving op financiële leases wordt berekend met een standaard lineaire methode. De lease-afschrijving is van invloed op de winst- en verliesrekening door de rentelasten te debiteren. De balans wordt beïnvloed door de samengevoegde rekening van het activum met gebruiksrecht voor financiële leases te crediteren. Als de lease aan een vast activum is gekoppeld, worden de afschrijvingstransacties alleen vanuit de module voor vaste activa uitgevoerd. 

|     Type                                          |     Debet                     |     Krediet                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operationele lease onder US GAAP              |  Onkosten van lease                |   De samengevoegde afschrijving van het activum met gebruiksrecht     |
|     Financiële lease onder IFRS en US GAAP        |   Afschrijving van onkosten van het activum met gebruiksrecht   |   De samengevoegde afschrijving van het activum met gebruiksrecht    |

#### <a name="short-term-lease"></a>Kortlopende lease
Een kortlopende lease wordt toegerekend als onkosten, die van invloed zijn op het inkomensoverzicht van een organisatie. Met de gegenereerde verschuldigde leasebetaling wordt de rekening voor leasekosten gedebiteerd en wordt de subgrootboekrekening voor nog te betalen bedragen of leveranciers gecrediteerd.

|     Type                                          |     Debet                     |     Krediet                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Invoer van kortlopende lease onder IFRS en US GAAP     |  Onkosten van lease                |   Leveranciersaansprakelijkheid (subadministratie)/nog te betalen bedragen  |

#### <a name="low-value-lease"></a>Lease met geringe waarde
Een lease met geringe waarde wordt toegerekend als onkosten, die van invloed zijn op het inkomensoverzicht van uw organisatie. Met de gegenereerde verschuldigde leasebetaling worden de leasekosten gedebiteerd en wordt het subgrootboek voor nog te betalen bedragen of leveranciers gecrediteerd.

|     Type                                          |     Debet                     |     Krediet                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Invoer van lease met geringe waarde onder IFRS en US GAAP      |  Onkosten van lease                |   Leveranciersaansprakelijkheid (subadministratie)/nog te betalen bedragen  |


#### <a name="index-revaluation"></a>Herwaardering index
Dit is de activaleaserekening voor variabele leasebetalingen die worden gemeten door een indextarief. Wijzigingen in leasebetalingen die worden veroorzaakt door indextariefschommelingen, vormen een leasecorrectie onder IFRS 16. De leaseverplichtingen en de activa met gebruiksrecht worden gecorrigeerd met de nieuwe betalingen. 

|     Type                                          |     Debet                             |     Krediet                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Invoer van indexherwaardering onder IFRS in geval van verhoging  |  Activum met gebruiksrecht       |   Verplichtingen operationele lease |
|   Invoer van indexherwaardering onder IFRS in geval van verlaging  |  Verplichtingen operationele lease  |   Activum met gebruiksrecht      |

Wanneer betalingen worden gewijzigd als gevolg van een wijziging in het indextarief, worden alleen de variabele betalingen gewijzigd, tenzij er extra wijzigingen zijn in cashflows, zoals een wijziging in leasevoorwaarden met betrekking tot rentetarieven onder US GAAP ASC 842.

#### <a name="lease-adjustment"></a>Leasecorrectie
Met activalease kunnen leases worden gecorrigeerd als de leasevoorwaarden worden gewijzigd, de lease wordt verlengd of als er aanvullende omstandigheden zijn waarvoor een lease moet worden gecorrigeerd. Leasecorrecties worden geboekt om het activum met gebruiksrecht en leaseverplichtingen te verhogen of te verlagen. Met het correctieproces vindt overdracht van eindsaldi van aansprakelijkheidsafschrijving en activasaldo op de correctiedatum plaats. Wanneer een lease aan vaste activa wordt gekoppeld, wordt de correctie van het activum met gebruiksrecht geboekt met de ID die is toegewezen in Vaste activa. 

|     Type                                          |     Debet                             |     Krediet                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Invoer van leasecorrectie voor IFRS en US GAAP in geval van verhoging     |  Activum met gebruiksrecht       |   Verplichtingen operationele lease |
|   Invoer van leasecorrectie voor IFRS en US GAAP in geval van verlaging     |  Verplichtingen operationele lease  |   Activum met gebruiksrecht      |


#### <a name="lease-impairment"></a>Waardevermindering van lease
Hiermee wordt de verlaging van het overdrachtssaldo van het activum met gebruiksrecht aangegeven. Geef het waardeverminderingsbedrag, de transactiedatum en de resterende perioden aan. Het resterende activum met gebruiksrecht wordt lineair afgeschreven. In de logica voor waardevermindering van lease wordt de overdrachtswaarde van het activum meegenomen die aanwezig is in het afschrijvingsschema voor activa.  

|     Type                                          |     Debet                             |     Krediet                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Invoer van waardevermindering voor IFRS en US GAAP           |  Waardeverminderingskosten                   |    Activum met gebruiksrecht     |

>[!NOTE]
> Als de lease aan een vast activum wordt gekoppeld, moet de waardevermindering van de lease worden geboekt vanuit Vaste activa, omdat de activumafschrijving vanuit de module Vaste activa wordt uitgevoerd.

**Twee valuta´s**: leasetransacties kunnen in een andere valuta dan de valuta voor boekhouding en rapportage worden geboekt. De wisselkoers van de valuta wordt op de begindatum in het grootboek gedefinieerd. U kunt de wisselkoersen wijzigen door het veld **Vaste wisselkoers** in te stellen op **Ja** wanneer u de lease maakt. Wanneer u leasetransacties invoert, wordt bij de eerste toerekening en volgende afschrijvingstransacties de wisselkoers vanaf de begindatum gebruikt. Bij de volgende betalings- en rentetransacties wordt de huidige actieve wisselkoers gebruikt. 

## <a name="create-an-asset-lease"></a>Een activalease maken
Voer de volgende stappen uit om een nieuwe lease te maken. 

1. Als u **Activalease** wilt gebruiken, moet u deze inschakelen in de werkruimte **Functiebeheer**. Selecteer in de werkruimte **Functiebeheer** **Alle** zodat alle functies op de pagina worden weergegeven. Selecteer **Activalease** en selecteer vervolgens **Nu inschakelen**.
2. Ga naar **Activalease > Algemeen > Leaseoverzicht**. Voer de vereiste velden op het sneltabblad **Algemeen** in. 
   - **Leasegegevens**
   - **Economische levensduur activum (maanden)**
   - **Leasegroep**
   - **Verhoogd leningtarief (%)**
   - **Samenstellingsinterval**
   - **Type annuïteit**
   - **Valuta**
   - **Begindatum**

3. Ga naar het sneltabblad **Regels van betalingsschema** en voer een betalingsregel in. Selecteer vervolgens **Schema's maken**.

4. Selecteer **Boeken**. 

5. Schakel over naar het sneltabblad **Algemeen**. Het **eerste activum met gebruiksrecht** en **leaseverplichtingen** worden berekend. 

6. Ga naar het sneltabblad **Classificatietest voor lease** om de waarde in het veld **Leasetype** te controleren. 

   Het automatische **leasetype** wordt geclassificeerd op basis van de criteria die zijn gedefinieerd op de pagina **Boeken**.

7.  Ga naar **Betalingsschema** onder de sectie **Functie**.  

   Op de pagina **Betalingsschema** worden toekomstige betalingsschema's voor een lease-ID weergegeven. Selecteer **Schema bevestigen** zodat u de transacties voor **Eerste toerekening** kunt boeken. 

[![Functie Eerste toerekening](./media/overview-13.png)](./media/overview-13.png)

8. Selecteer **Eerste toerekening** om het journaal van de eerste toerekening te maken. 

9. Selecteer **Activaleasejournalen** om de transactie van eerste toerekening te boeken. 

   Vanuit het betalingsschema kunt u een gedetailleerde pagina openen met een overzicht van de transacties voor de activa met gebruiksrecht. 
 
   In het **Afschrijvingsschema leaseverplichtingen** wordt het rentebedrag weergegeven dat voor elke periode is berekend.
   
10. Maak het journaal en ga vervolgens naar **Activaleasejournalen**. Het **Afschrijvingsschema leaseverplichtingen** wordt ook weergegeven in de rentetransacties.

   Op de pagina **Afschrijvingsschema activa** worden de afschrijvingstransacties voor de geselecteerde lease-ID weergegeven. 

   [![Pagina RoU-activatransacties](./media/overview-20.png)](./media/overview-20.png)

   Op de pagina **RoU-activatransacties** worden de eerste toerekening, de samengevoegde afschrijving en het activasaldo weergegeven. 

   Op de pagina **Transacties leaseverplichtingen** worden de eerste toerekening, rentebetaling voor lease, leasebetaling en het saldo van leaseverplichtingen weergegeven. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

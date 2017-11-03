---
title: Projectcontracten
description: Dit artikel bevat beschrijvingen en voorbeelden van projectcontracten die u voor typen projecten en financieringsbronnen kunt maken. Daarnaast wordt aangegeven hoe u contracten en factuurprojectklanten kunt beheren in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="project-contracts"></a>Projectcontracten

[!include[banner](../includes/banner.md)]


Dit artikel bevat beschrijvingen en voorbeelden van projectcontracten die u voor typen projecten en financieringsbronnen kunt maken. Daarnaast wordt aangegeven hoe u contracten en factuurprojectklanten kunt beheren in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

Het type project dat u maakt voor een projectcontract bepaalt de wijze waarop projectklanten gefactureerd worden. U kunt een projectcontract en het gerelateerde project wijzigen, maar u kunt het projecttype niet wijzigen. 

Als u een projectcontract gebruikt, kunt u meerdere projecten tegelijkertijd factureren. Het projectcontract zorgt ook voor een consistente factureringsprocedure voor elk subproject in een projectstructuur. 

Elk project dat wordt gefactureerd, moet worden gekoppeld aan een projectcontract. De instellingen voor een projectcontract gelden voor alle projecten en subprojecten die gekoppeld zijn aan het projectcontract. 

In een projectcontract kunnen meerdere financieringsbronnen worden gespecificeerd. Hierdoor kunt u facturering tussen meerdere financiers instellen, financieringslimieten instellen zodat financieringsbronnen voor niet meer dan een bepaald bedrag worden gefactureerd, en kunt u financieringsregels instellen voor in rekening gebrachte uitgaven.

## <a name="funding-for-project-contracts"></a>Financieren van projectcontracten
Bepaalde projectcontracten kunnen bepalen dat meerdere partijen de financieringsverantwoordelijkheden voor de projectkosten delen. Hieronder vindt u enkele voorbeelden:

-   Een grote klant kan bijvoorbeeld vragen om de financiering van een project te splitsen onder meerdere divisies.
-   Uw bedrijf deelt de kosten van een groot project met een externe organisatie.
-   Een wegenplan wordt medegefinancierd door twee gemeenten.
-   Een brugproject wordt gefinancierd door een overheidssubsidie en een particulier bedrijf.

In Finance and Operations kunt u de facturering voor één transactie of een volledig project splitsen tussen meerdere klanten, subsidies of organisaties. 

Bij projecten met meerdere financiers, worden alle partijen die bijdragen tot de financiering van een geavanceerd financieringsproject financieringsbronnen genoemd. Nadat een klant, organisatie of subsidie als financieringsbron is gedefinieerd, kan deze aan één of meer financieringsregels worden toegewezen. De financieringsregels bevatten de criteria die bepalen hoe kosten aan verschillende financieringsbronnen voor een project moeten worden toegekend. 

Omdat voorraadartikelen, zoals de artikelen op opdrachten tot inkoop en inkooporders, niet kunnen worden opgesplitst, kan het kostenbedrag bij de distributie ook niet worden opgesplitst tussen meerdere financieringsbronnen. Daarom blijft de financieringsbronwaarde 0 (nul) tot de voorraaduitgifte wordt geboekt. Wanneer de voorraaduitgifte wordt geboekt, wordt het kostenbedrag verdeeld volgens de rekeningdistributieregels voor het project.

U kunt het volgende doen om het gemakkelijker te maken om de facturering tussen meerdere financieringsbronnen te splitsen:

-   Specificeer dat alle transacties die voor een project worden ingevoerd, dezelfde verkoopvaluta gebruiken als het projectcontract.
-   Stel financieringslimieten in zodat een financieringsbron niet meer wordt gefactureerd dan een opgegeven bedrag voor een project.
-   Configureer financieringsregels en financieringslimieten voor elke werknemer, artikel, categorie, categoriegroep en transactietype (of voor alle transactietypes).
-   Selecteer optionele start- en einddatums om de periode te definiëren waarvoor elke financieringsregel geldt.
-   Specificeer het percentage waarvoor elke financieringsbron verantwoordelijk is.
-   Specificeer welke financieringsbron verantwoordelijk is voor afrondingsverschillen als gevolg van financieringstoewijzingsberekeningen.
-   Stel regels in voor de wijze waarop projectkosten aan externe klanten worden gefactureerd en aan interne organisaties in rekening worden gebracht.
-   Registreer transacties in een financieringsrekening in wachtstand tot extra financiering kan worden verkregen of u beslist om de kosten intern te dragen.

Om te bepalen welke btw-groep aan een transactie moet worden gekoppeld, wordt het project doorzocht op een btw-groepstoewijzing. Als er geen btw-groepstoewijzing is uitgevoerd op projectniveau, wordt het projectcontract doorzocht.

### <a name="example-multiple-funding-sources-simple"></a>Voorbeeld: meerdere financieringsbronnen (eenvoudig)

De volgende tabel bevat scenario's voor het beheren van financieringstoewijzingen over meerdere financieringsbronnen. Deze scenario's zijn gebaseerd op de volgende veronderstellingen:

-   Prioriteitsinstellingen worden toegepast in de toewijzing van middelen, voordat de andere financieringsregels worden toegepast.
-   Er is geen datumbereik opgegeven voor de periode wanneer de financieringsregel geldt.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenario</strong></td>
<td><strong>Financieringsbron </strong></td>
<td><strong>Toewijzingspercentage </strong></td>
<td><strong>Toewijzingsprioriteit </strong></td>
</tr>
<tr class="even">
<td>U wilt kosten toewijzen aan een financieringsbron totdat de middelen zijn uitgeput, kosten toewijzen aan een tweede financieringsbron totdat de middelen zijn uitgeput en ten slotte de resterende kosten toewijzen aan een derde financieringsbron toewijzen.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
<li>Financieringsbron 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron. Wanneer een van deze financieringsbronnen is opgebruikt, wilt u de resterende kosten betalen van een derde financieringsbron.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
<li>Financieringsbron 3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron. Wanneer een van beide financieringsbronnen is opgebruikt, wilt u de resterende kosten delen tussen een derde en vierde financieringsbron.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
<li>Financieringsbron 3</li>
<li>Financieringsbron 4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>U wilt de eerste 25 procent van de kosten toewijzen aan één financieringsbron en de rest aan een andere.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Voorbeeld: meerdere financieringsbronnen (complex)

U hebt drie financieringsbronnen en u wilt ze gebruiken in de volgende volgorde:

1.  Financieringsbron 2 en 3 financieringsbron 3 evenveel gebruiken tot financieringsbron 2 is uitgeput.
2.  Financieringsbron 3 verder gebruiken totdat deze is uitgeput.
3.  Financieringsbron 1 gebruiken nadat financieringsbron 3 is uitgeput.

Om dit doel te bereiken, moet u het volgende doen:

-   Stel financieringslimieten in voor financieringsbron 2 en financieringsbron 3 voor hun respectieve bedragen.
-   Maak de volgende financieringsregels:
    -   Regel 1 (prioriteit 1): Wijs 50 procent van de transacties toe aan financieringsbron 2 en 50 procent aan financieringsbron 3.
    -   Regel 2 (prioriteit 2): Wijs 100 procent van de transacties toe aan financieringsbron 3.
    -   Regel 3 (prioriteit 3): Wijs 100 procent van de transacties toe aan financieringsbron 1.

Deze configuratie werkt omdat de transacties worden vergeleken met de regels en limieten om te zien of deze van toepassing zijn op de transactie. Als u er geen specifieke regels of limieten van toepassing zijn op de transactie, geldt de regel alle transacties. De regel Alle transacties stemt overeen met alle transacties. 

Als een regel wordt gevonden die overeenkomt met een transactie, wordt het percentage dat is toegewezen in die regel eerst toegepast, maar alleen nadat de overeenkomsten zijn gecontroleerd op eventuele limieten die zijn ingesteld. Als een limiet is bereikt en een financieringsbron is uitgeput, wordt de financieringsregel die is gekoppeld aan de financieringslimiet genegeerd en controleert het programma de volgende regel die van toepassing is. 

In sommige gevallen kan slechts een deel van een transactie onder een regel worden toegepast. Dit kan gebeuren omdat een limiet wordt bereikt wanneer de transactie wordt toegewezen. In dit geval wordt alleen een bepaald bedrag toegewezen volgens die regel, bijvoorbeeld 50 procent aan elke financieringsbron. Dit is het geval in regel 1, zoals eerder in dit gedeelte wordt beschreven. De rest wordt toegewezen volgens de volgende regel in de reeks. 

In de volgende tabel wordt dit scenario nader onderzocht.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Focus</strong></td>
<td><strong>Details</strong></td>
</tr>
<tr class="even">
<td>Financieringsregels</td>
<td><ul>
<li>Regel 1 (prioriteit 1): Alle transacties. Financieringsbron 2 bij 50% en financieringsbron 3 bij 50%.</li>
<li>Regel 2 (prioriteit 2): Alle transacties. Financieringsbron 3 toewijzen bij 100%.</li>
<li>Regel 3 (prioriteit 2): Alle transacties. Financieringsbron 1 toewijzen bij 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Financieringslimieten</td>
<td><ul>
<li>Limiet financieringsbron 1 = 10.000,00</li>
<li>Limiet financieringsbron 2 = 500,00</li>
<li>Limiet financieringsbron 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transactie 1</td>
<td><strong>Transactiebedrag:</strong> 100,00<strong>Financiering:</strong> De transactie wordt alleen betaald volgens regel 1, aangezien de transactie volledig is betaald nadat regel 1 is toegepast. De transactie wordt gelijk verdeeld tussen financieringsbron 2 en 3.
<ul>
<li>Financieringsbron 2: 50,00</li>
<li>Financieringsbron 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transactie 2</td>
<td><strong>Transactiebedrag:</strong> 5000,00<strong>Financiering:</strong> De transactie is betaald volgens alle drie de regels.<strong>Regel 1</strong>
<ul>
<li>Financieringsbron 2: 450,00</li>
<li>Financieringsbron 3: 450,00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Financieringsbron: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Financieringsbron 1: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Totale middelen die worden verdeeld voor elke financieringsbron</td>
<td><ul>
<li>Financieringsbron 1: 3.850,00</li>
<li>Financieringsbron 2: 500,00</li>
<li>Financieringsbron 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Factureringsregels
Wanneer u over een projectcontract met een klant onderhandelt, definieert u hoe en wanneer u de klant kunt factureren voor werkzaamheden aan een project. Nadat u het projectcontract en het project hebt ingesteld, kunt u factureringsregels voor het project instellen. De factureringsregels zijn gebaseerd op de projectvoorwaarden die in het projectcontract zijn gespecificeerd. De factureringsregels die u kunt maken, hangen af van de voorwaarden in het projectcontract en het type project dat u aan de factureringsregel koppelt, bijvoorbeeld tijd en materiaal of vaste prijs. Voor een projectcontract kunnen meerdere factureringsregels worden gemaakt. U kunt ook een factureringsregel toewijzen aan meerdere projecten die zijn gekoppeld aan hetzelfde projectcontract en soortgelijke facturatievoorwaarden hebben. 

U kunt de volgende soorten factureringsregels instellen:

-   **Leveringseenheid** – Factureer een klant wanneer u een leveringseenheid hebt voltooid. U bepaalt de leveringseenheden in het contract.
-   **Voortgang** – Factureer een klant wanneer u een gespecificeerd percentage van het project hebt voltooid. U kunt een factureringsregel instellen die automatisch het percentage voltooid werk berekent, of u kunt handmatig het percentage voltooid werk en het te factureren bedrag aan de klant berekenen.
-   **Mijlpaal** – Factureer een klant voor het volledige bedrag van een mijlpaal wanneer een projectmijlpaal wordt bereikt.
-   **Kosten** – Factureer een klant voor uw diensten plus een beheertarief. Dit beheertarief betreft gewoonlijk een percentage van de kosten van diensten.
-   **Tijd en materiaal** – Factureer een klant voor de waarde van tijd en materiaal die voor een project wordt gebruikt.

Voor alle typen factureringsregels kunt u een inhoudingspercentage opgeven om van klantfacturen af te trekken tot een project een vooraf overeengekomen fase bereikt. Het betalingsinhoudingspercentage is opgegeven in het projectcontract. Het bedrag wordt berekend voor en afgetrokken van de totale waarde van de regels in een klantfactuur. 

Voor de factureringsregels **Tijd en materiaal** en **Voortgang** kunt u toerekenbare categorieën toewijzen. Toerekenbare categorieën geven de transacties aan die in klantfacturen opgenomen moeten worden. 

Wanneer u klaar bent om de klant te factureren, wordt het te factureren bedrag voor het project berekend op basis van de factureringsregels en wordt er een projectfactuurvoorstel gegenereerd. 

De volgende secties bieden voorbeelden ter illustratie van het instellen en beheren van factureringregels voor een project.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Voorbeeld: Een factureringsregel maken die is gebaseerd op het aantal geleverde eenheden

Uw organisatie gaat een overeenkomst aan om in totaal vijf trainingssessies aan de werknemers van een klant te leveren met een waarde van 10.000 per trainingssessie. U factureert de klant na elke trainingssessie. 

Stel de factureringsregels voor het contract in met de volgende waarden:

-   De leveringseenheid is één trainingssessie.
-   De eenheidsprijs is 10.000 per trainingssessie.
-   Het totale aantal eenheden bedraagt vijf trainingssessies.

Wanneer u een trainingssessie hebt voltooid, kunt u een factuur voor 10.000 maken voor de eerste geleverde eenheid en deze naar de klant verzenden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Voorbeeld: Een factureringsregel maken op basis van een gespecificeerd voltooiingspercentage (handmatige berekening)

Uw organisatie, een bedrijf op het gebied van softwareadvies, gaat een overeenkomst aan met een klant voor het ontwikkelen van een deel van een product dat door de klant wordt ontwikkeld. Uw organisatie stemt ermee in om de softwarecode in de loop van een periode van zes maanden te leveren. De klant stemt ermee in om uw organisatie in totaal 100.000 te betalen voor de werkzaamheden. U maakt een factureringsregel om de klant te factureren op basis van een percentage voltooide werkzaamheden voor het project, zoals aangegeven in het contract.

-   Aan het einde van de eerste maand ontmoet u de klant om te bepalen welk percentage van de werkzaamheden is voltooid. Na evaluatie van het project besluiten u en uw klant dat 15% van het project is voltooid.
-   U maakt een factuur voor een bedrag van 15.000 (15% van 100.000) en stuurt deze naar uw klant.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Voorbeeld: Een factureringsregel maken op basis van een gespecificeerd voltooiingspercentage (automatische berekening)

Uw organisatie, een bedrijf dat zich bezighoudt met het ontwikkelen van software, komt met een klant overeen om een salarisadministratiepakket te ontwikkelen voor een bedrag van 30.000. De klant stemt ermee in om uw organisatie te betalen op basis van het percentage van de werkzaamheden dat is voltooid. U schat dat de projectkosten 20.000 bedragen. In het projectcontract zijn de categorieën werkzaamheden gespecificeerd die u in het factureringsproces kunt gebruiken. U stelt factureringsregels in die automatisch de factuurbedragen berekenen voor het percentage voltooide werkzaamheden voor de afzonderlijke categorieën. U stelt voor elke categorie een budget in:

-   **Ontwikkeling** – De kosten bedragen 15.000 en de opbrengsten 20.000.
-   **Installatie** – De kosten bedragen 5.000 en de opbrengsten 10.000.

Wanneer u de klant voor de eerste keer factureert, wordt het factuurbedrag automatisch berekend op basis van de volgende informatie:

-   De werknemer op het project dient na een maand een urenstaat voor het project in. De kosten van de werknemersuren bedragen 5.000 voor ontwikkeling en 1.000 voor installatie. De ontwikkelingswerkzaamheden zijn voor 33% voltooid (5000 daadwerkelijke kosten/15.000 budgetkosten) en de installatiewerkzaamheden zijn voor 20% voltooid (1000 daadwerkelijke kosten/5000 budgetkosten).
-   Het factuurbedrag van 8667 wordt automatisch berekend (33 procent van 20.000 + 20 procent van 10.000).
-   U maakt een factuur voor een bedrag van 8667 en stuurt deze naar de klant.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Voorbeeld: Een factureringsregel maken op basis van afgesproken mijlpalen

Uw organisatie, een bedrijf op het gebied van beheeradvies, stemt ermee in diensten op het vlak van het uitvoeren van marktonderzoek te leveren voor een consumentenproduct dat uw klant wil gaan verkopen. U komt met de klant overeen dat deze uw diensten met ingang van maart zal gaan gebruiken voor een periode van drie maanden en dat de klant uw organisatie hiervoor een bedrag van 50.000 verschuldigd is. Het project heeft drie mijlpalen:

-   Mijlpaal 1: Verzamelen consumentgegevens – 31 maart
-   Mijlpaal 2: Analyseren consumentgegevens – 30 april
-   Mijlpaal 3: Een voorstel presenteren met betrekking tot de levensvatbaarheid van het product – 31 mei

U komt met de klant overeen dat deze uw organisatie 10.000 betaalt voor de eerste mijlpaal en 20.000 voor elk van de volgende twee mijlpalen. 

U spreekt bij het opstellen van het projectcontract met de klant af dat u telkens factureert op basis van een voltooide mijlpaal. Het instellen van de factureringsregel omvat de volgende stappen:

-   Definieer de projectmijlpalen.
-   Definieer het bedrag waarvoor de klant moet worden gefactureerd wanneer elke projectmijlpaal wordt behaald.

Nadat u de eerste mijlpaal op 31 maart hebt voltooid, markeert u de mijlpaal als voltooid en maakt u een factuur voor een bedrag van 10.000 om naar de klant te sturen. U kunt pas een factuur voor een mijlpaal maken als u de mijlpaal als voltooid hebt gemarkeerd.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Voorbeeld: Een factureringsregel maken op basis van diensten plus een beheertarief

Uw organisatie, een bedrijf op het gebied van beheeradvies, stemt ermee in marktonderzoek uit te voeren om de levensvatbaarheid te beoordelen van een product dat de klant, een retailbedrijf, in ontwikkeling heeft. Volgens de bepalingen van de overeenkomst levert u de diensten van uw drie belangrijkste beheerconsultants voor het uitvoeren van onderzoek op een tijd-en-materialen-basis. U komt met de klant overeen dat deze 100 per uur betaalt, plus een managementtarief van 10% voor de adviesuren die voor het project in rekening worden gebracht. 

U maakt tijdens het instellen van het projectcontract een factureringsregel om het managementtarief van 10% toe te voegen aan de adviesuren die voor het project in rekening worden gebracht. 

Wanneer u een factuur voor de klant maakt, factureert u een managementtarief van 10% plus de kosten van de adviesuren. Wanneer de drie consultants in totaal bijvoorbeeld 200 uur aan het project hebben gewerkt, wordt er een factuur gemaakt voor het bedrag van 22.000 op basis van de volgende berekening:

-   200 uur tegen een tarief van 100 per uur = 20.000
-   10 procent managementtarief = 2.000
-   Totaal factuurbedrag = 22.000

Als de kosten voor een klant belastbaar zijn, en u selecteert een btw-groep in het projectcontract, wordt de btw-groep automatisch ingevoerd in een factureringsregel voor kosten.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Voorbeeld: Een factureringsregel voor de waarde van de tijd en de materialen maken

Uw organisatie, een bedrijf dat zich bezighoudt met diensten op het gebied van softwareadvies, is overeengekomen dat u voorziet in vijf technische consultants die de komende zes maanden voor een klant aan een softwareontwikkelingsproject zullen werken. U komt met de klant overeen dat deze 150 betaalt voor elk adviesuur plus de kosten van kantoorbenodigdheden. Uw organisatie stuurt aan het einde van elke maand een factuur aan de klant. 

Wanneer u het projectcontract instelt, gaat u ermee akkoord dat u de klant maandelijks de tijd en het materiaal voor het project in rekening brengt. U maakt een factureringsregel die de volgende informatie bevat:

-   De contractperiode is zes maanden.
-   De adviestijd wordt berekend op basis van een tarief van 150 per uur.
-   Kantoorbenodigdheden worden gefactureerd tegen de kosten, maar de totale kosten voor het project mogen niet hoger zijn dan 10.000.
-   U maakt gedurende het project aan het einde van elke kalendermaand een klantfactuur.

Tijdens de eerste maand worden er door de adviseurs in totaal 800 uren voor het project geregistreerd. De kosten van kantoorbenodigdheden die voor het project in rekening worden gebracht, zijn 2000. Daarom maakt u aan het eind van de maand een factuur voor 122.000, berekend als 800 uur tegen 150 per uur, plus 2000 voor kantoorbenodigdheden.





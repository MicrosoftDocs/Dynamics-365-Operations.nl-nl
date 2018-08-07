---
title: Alternatieven voor levering
description: Verkoopordermedewerkers kunnen de pagina Alternatieven voor levering gebruiken om alternatieve opties voor orderafhandeling te ontdekken.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 855fdd0e57a7001628b715038785379d5a986789
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="delivery-alternatives"></a>Alternatieven voor levering

[!include [banner](../includes/banner.md)]

Verkoopordermedewerkers kunnen de pagina **Alternatieven voor levering** gebruiken om alternatieve opties voor orderafhandeling te ontdekken.

De paginalay-out **Alternatieven voor levering** biedt een beter overzicht van alle alternatieve opties. Het stelt ordermedewerkers tevens in staat verder te kijken dan het huidige bedrijf voor afhandelingsmogelijkheden. Zij kunnen nu zowel intercompany-mogelijkheden als kansen van externe leveranciers bekijken. Door de opties te sorteren op leveringsdatum kunnen verkoopordermedewerkers een intelligente lijst van alternatieven voor levering bekijken. Daarnaast helpen parameters hen de voorgestelde leveringen beter te beheren. Aangezien de transporttijd van invloed kan zijn op leveringsdatums, kunnen verkoopordermedwerkers de verschillende transportopties verkennen die vervoerders aanbieden. Omdat voor elke suggestie gedetailleerde informatie wordt weergegeven, kunnen ordermedewerkers rechtstreeks vanaf de pagina **Alternatieven voor levering** beslissingen nemen.

## <a name="open-the-delivery-alternatives-page"></a>De pagina Alternatieven voor levering openen
U kunt pagina **Alternatieven voor levering** openen vanaf de verkooporderregel.

1.  Klik op **Producten en aanbod** &gt; **Alternatieven voor levering**.
2.  Klik op **Regeldetails** &gt; **Levering** &gt; **Alternatieven voor levering**.

U kunt ook de pagina **Alternatieven voor levering** openen door het werkgebied **Verkooporderverwerking en -onderzoek** te openen en vervolgens op **Orders en favorieten** &gt; **Vertraagde orderregels** &gt; **Alternatieven voor levering** te klikken. **Opmerking:** u kunt de pagina **Alternatieven voor levering** alleen openen als aan beide volgende voorwaarden is voldaan:

-   Alle verplichte verkoopregelgegevens zijn ingevuld.
-   Het veld **Controle leveringsdatum** veld is ingesteld op een andere waarde dan **Geen**.

## <a name="delivery-date-control-methods"></a>Methoden voor controle van leveringsdatum
De methode voor controle van de leveringsdatum bepaalt hoe het systeem leveringsdatums vaststelt, hoe alternatieven voor levering worden berekend en welke informatie wordt weergegeven. Houd er rekening mee dat bij de controle van leveringsgegevens rekening wordt gehouden met kalenders. Daarom zijn de volgende agenda's mogelijk van invloed op de voorgestelde ontvangstdatum: magazijnkalender, transportkalender, leverancierskalender en klantkalender. In de volgende tabel wordt elke methode voor controle van de leveringsdatum beschreven.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Methode</strong></td>
<td><strong>Beschrijving</strong></td>
</tr>
<tr class="even">
<td><strong>Geen</strong></td>
<td><ul>
<li>Leveringsalternatieven voor verkoopregels worden niet ondersteund. Met deze optie wordt controle van de leveringsdatum uitgeschakeld.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verkooplevertijd</strong></td>
<td><ul>
<li>Alternatieven voor levering worden berekend op basis van de vooraf gedefinieerde verkooplevertijd. De transportdagen worden berekend op basis van de leveringsmethode.</li>
<li>Alternatieven voor leveringenj omvatten magazijnen met voorhanden voorraad en vraag-/aanbodorders.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Alternatieven voor levering worden berekend op basis van ATP-logica (available to promise). Er wordt rekening gehouden met de huidige beschikbaarheid en verwachte toekomstige beschikbaarheid. De transportdagen worden berekend op basis van de leveringsmethode.</li>
<li>Alternatieven voor leveringenj omvatten magazijnen met voorhanden voorraad en vraag-/aanbodorders.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + uitgiftemarge</strong></td>
<td><ul>
<li>Alternatieven voor levering worden berekend volgens de ATP-methode, maar de uitgiftemarge wordt meegenomen bij de berekening.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>Alternatieven voor levering worden berekend op basis van CTP-logica (capable to promise). MRP-explosie wordt gebruikt om de beschikbaarheid te bepalen. Houd er rekening mee dat CTP leveringsdatums compenseert op basis van verkooplevertijd. De transportdagen worden berekend op basis van de leveringsmethode.</li>
<li>Alternatieven voor levering bevatten suggesties voor de volgende magazijnen:
<ul>
<li>Huidig magazijn</li>
<li>Standaardmagazijn</li>
<li>Alle magazijnen met beschikbare voorhanden voorraad</li>
<li>Alle magazijnen met aanbodorders</li>
<li>Alle magazijnen die actieve stuklijstversies</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Informatie weergeven over andere alternatieven voor levering
In deze sectie wordt beschreven welke informatie over alternatieven voor levering beschikbaar is op elk tabblad van de pagina **Alternatieven voor levering**.

### <a name="products"></a>Producten

Op dit tabblad wordt een overzicht van het product en de details van de huidige verkoopregel getoond.

### <a name="delivery-alternatives"></a>Alternatieven voor levering

Dit tabblad toont een lijst met alternatieven voor levering die is gesorteerd op ontvangstgegevens. Boven de lijst kunt u selecteren op welke opties de suggesties moeten zijn gebaseerd. U kunt ook de leveringsmethode selecteren, die het aantal transportdagen bepaalt. De volgende opties zijn beschikbaar:

-   **Andere productvarianten opnemen** - Deze optie is beschikbaar voor producten met productvarianten. Dit bevat alternatieven voor levering van andere varianten van het product. Deze optie is niet beschikbaar voor CTP.
-   **Gedeeltelijke hoeveelheid opnemen** - Standaard worden alleen suggesties opgenomen waarmee de volledige hoeveelheid van de verkoopregel kan worden vervuld. Selecteer deze optie om suggesties op te nemen die de orderregel slechts gedeeltelijk vervullen. Deze optie is handig wanneer de klant om een eerdere leverdatum vraagt en gedeeltelijke levering accepteert.
-   **Latere datums opnemen** - Standaard worden alleen suggesties die beter (eerder) zijn dan de huidige datums op de verkoopregel weergegeven. Selecteer deze optie om latere datums op te nemen. Deze optie kan handig zijn in situaties waarin andere parameters dan de datum prioriteit hebben. Zo wordt bijvoorbeeld mogelijk de voorkeur gegeven aan een specifieke leverancier of een specifiek magazijn.
-   **Leveringsmethode** - Selecteer de gewenste leveringsmethode om transporttijd en -kosten te optimaliseren. U ziet onmiddellijk het effect op de voorgestelde alternatieven voor levering. Daarom is het gemakkelijk om de alternatieven te vergelijken.
-   **Aanschaffing opnemen** - Wanneer aanschaffing is geselecteerd, omvatten de voorgestelde alternatieven voor levering van opties voor verwerving van zowel externe leveranciers als andere bedrijven in de onderneming (intercompany). De optie **Aanschaffing opnemen** wordt ondersteund voor de methoden voor controle van leveringsdatums ATP en ATP + uitgiftemarge. Aanschaffingsopties van de standaardleverancier voor het product en alle goedgekeurde leveranciers voor het product worden opgenomen.
-   Voor externe leveranciers is de berekening gebaseerd op de inkoopdoorlooptijd.
-   Voor intercompany, wordt bij de berekening rekening gehouden met wat beschikbaar vanuit het sourcingbedrijf, op basis van de controle van leveringsdatum in het sourcingbedrijf.
-   **Leveringstype** (relevant voor aanschaffing)
    -   **Voorraad** - Producten worden verzonden vanuit het sourcingmagazijn naar de locatie/het magazijn op de verkoopregel. Zij worden vervolgens vanuit dat magazijn naar de klant verzonden.
    -   **Directe levering** - Producten worden rechtstreeks vanuit het sourcingmagazijn naar de klant verzonden.

### <a name="availability-information"></a>Beschikbaarheidsinformatie

Informatie op dit tabblad houdt verband met de regel voor alternatieve levering die is geselecteerd. De volgende informatie wordt weergegeven, afhankelijk van de controle van de leveringsdatum voor de verkoopregel:

-   **Verkooplevertijd**
    -   **Vandaag beschikbaar** - Geef de huidige fysieke voorhanden voorraad, fysiek gereserveerde en beschikbare fysieke voorraad weer.
    -   **Parameters** - Geef de voorraadeenheid en de verkooplevertijd weer.

-   **ATP en ATP + Uitgiftemarge**
    -   **Vandaag beschikbaar** - Geef de huidige fysieke voorhanden voorraad, fysiek gereserveerde en beschikbare fysieke voorraad weer.
    -   **Parameters** - Geef de voorraadeenheid en de verkooplevertijd weer.
    -   **Toekomstige beschikbaarheid** - Geef een grafische weergave van de huidige en toekomstige beschikbaarheid voor de geselecteerde locatie en magazijn weer onder **Alternatieven voor levering**. U kunt op de grafiekkolommen klikken voor meer gedetailleerde informatie over de toekomstige beschikbaarheid van het product. De schuifregelaar geeft een lijst weer met relevante vraag- en aanbodorders binnen de time fence van ATP.

-   **CTP**
    -   **Vandaag beschikbaar** - Geef de huidige fysieke voorhanden voorraad, fysiek gereserveerde en beschikbare fysieke voorraad weer.
    -   **Parameters** - Geef de voorraadeenheid en de verkooplevertijd weer.
    -   **Explosie** - Geef een aanbodexplosie weer van het geselecteerde alternatief voor levering. U kunt **Instelling** gebruiken om de velden en voorraaddimensies te wijzigen die worden weergegeven in de explosie.

### <a name="impact-of-selected-alternative"></a>Impact van geselecteerd alternatief

Op dit tabblad wordt de impact weergegeven van het geselecteerde alternatief voor levering. Als u op **OK** klikt, wordt de verkoopregel bijgewerkt met de geselecteerde waarden in de kolommen GESELECTEERD. Houd er rekening mee dat, als de hoeveelheid in het geselecteerde alternatief voor levering kleiner is dan de hoeveelheid op de verkoopregel, een afleveringsschema wordt gemaakt en de orderregel wordt opgesplitst in twee regels: één regel voor de geselecteerde hoeveelheid en één regel voor de resterende hoeveelheid. U kunt ook de commerciële regel bijwerken zodat deze overeenkomt met de schemaregels en van invloed is op de prijzen.

<a name="additional-resources"></a>Aanvullende resources
--------

[Orderbelofte](delivery-dates-available-promise-calculations.md)






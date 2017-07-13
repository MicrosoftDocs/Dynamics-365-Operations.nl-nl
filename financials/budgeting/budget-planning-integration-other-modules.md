---
title: Budgetplanningsintegratie met andere modules
description: "Budgetplannen kunnen worden gegenereerd meerdere, verschillende bronnen: De basiselementen van het periodieke proces zijn hetzelfde voor alle bronnen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 975497e8ed0c9738c225bad4db9165bf2ebc0192
ms.openlocfilehash: 7f3dc8089153a6c67c1666aa8f859d63dcc9d3c9
ms.contentlocale: nl-nl
ms.lasthandoff: 06/05/2017


---

# <a name="budget-planning-integration-with-other-modules"></a>Budgetplanningsintegratie met andere modules

[!include[banner](../includes/banner.md)]




<a name="periodic-processes-for-generating-budget-plans"></a>De periodieke processen voor het genereren van budgetplannen
----------------------------------------------

Budgetplannen kunnen worden gegenereerd vanuit de volgende bronnen:

-   Grootboektransacties
-   Vaste activa
-   Prognoseposities
-   Projectprognoses
-   Aanbodprognoses
-   Vraagprognoses
-   Budgetregisterposten
-   Andere budgetplannen

De basiselementen van het periodieke proces zijn hetzelfde voor alle processen. Met de tabbladen kunt u de gegevens, de kenmerken van het doel (budgetplan) en de opties voor het uitvoeren van het proces op de achtergrond als batchproces instellen. Latere onderdelen van dit artikel beschrijven zaken die wellicht niet voor zich spreken in elk proces.

### <a name="actions"></a>Acties

Voor elk genereerproces zijn drie acties beschikbaar:

-   Met **Een nieuw budgetplan maken** wordt een nieuw plan gemaakt dat de kenmerken bevat die in de sectie Doel worden geselecteerd. Deze kenmerken hoeven niet uniek te zijn. Daarom kunnen twee plannen dezelfde naam en andere waarden hebben.
-   **Vervang het bestaande budgetplanscenario** verwijdert alle gegevens in het doelbudgetplan in het geselecteerde budgetplanscenario en maakt nieuwe regels die de geselecteerde brongegevens gebruiken.
-   **Het bestaande budgetplanscenario bijwerken en nieuwe gegevens toevoegen** werkt bestaande regels in het doelplan bij die overeenkomen met de bronregels en voegt nieuwe regels voor nieuwe gegevens toe. De vereffening is gebaseerd op de grootboekrekening, de datum, de budgetklasse, en verschillende andere velden. Wanneer u bijvoorbeeld budgetplannen genereert vanuit prognoseposities, is het positienummer een belangrijk veld. Alle regels die een positienummer hebben dat overeenkomt met de bronpositie, worden vervangen door de nieuwe regels uit de bron.

### <a name="source"></a>Bron

Voor alle processen kunt u op het tabblad **Bron** gegevens filteren met behulp van de knop **Filter**. Bepaalde velden worden standaard toegevoegd aan het filter voor elk proces. Voor het proces **Budgetplan genereren op basis van grootboek** zijn bijvoorbeeld de categorieën **Grootboekrekening** en **Hoofdrekening** beschikbaar en deze worden weergegeven op de genereerpagina. Alle velden die u toevoegt aan het filter, worden ook toegevoegd aan de pagina, samen met criteria die u toevoegt.

### <a name="target"></a>Doel

Met de optie **Historisch** op het tabblad **Doel** kunt u de datums van de brongegevens als ingangsdatumdatum in het budgetplan gebruiken. Doorgaans moet de datum in de levenscyclus binnen de budgetcyclus van het plan vallen. Wanneer u de optie **Historisch** instelt op **Ja**, wordt de datum (zelfs het jaar) van de bron is gebruikt, zodat u gegevens over het verleden als basis voor vergelijkingen kunt gebruiken. U kunt geen historische gegevens in het budgetplan wijzigen en het schema wordt ingesteld op een goedgekeurde workflowstatus. U kunt de status echter opnieuw instellen als andere scenario's in het plan wijzigingen vereisen.

Het veld **Totaal samentellen volgens** bovenaan de pagina bepaalt ook de datum die wordt gebruikt. Dit veld bevat totale bedragen en stelt desgewenst de ingangsdatum in op de eerste dag van het boekjaar of de boekperiode. 

Veel van de velden op het **Doel** tabblad kunnen worden bewerkt of zijn alleen-lezen, afhankelijk van de actie die u selecteert. Wanneer u echter overgaat van het maken van een nieuw budgetplan naar het bijwerken van een bestaand plan, is het veld **Naam van budgetplan** niet langer beschikbaar, en worden de velden voor het selecteren van een bestaand plan beschikbaar. Op zowel het tabblad **Doel** als het tabblad Bron is het veld **Grootboek** altijd niet-beschikbaar, omdat de waarde door het geselecteerde budgetplanningsproces wordt bepaald. 

In het veld **Budgetklasse** kunt u de regels van het budgetplan instellen als onkostentransacties of opbrengsttransacties. Doorgaans worden de opbrengsttransacties als kredieten opgenomen in een grootboekrekening en daarom als negatieve bedragen opgeslagen. Doorgaans worden deze transacties ook als negatieve bedragen in het budgetplan weergegeven. Door de budgetklasse als een veld aan de planindeling toe te voegen kunt u opbrengst weer laten geven als positieve bedragen.

### <a name="generation-rules"></a>Regels voor het genereren

Drie velden bevatten aanvullende functionaliteit: **Factor**, **Min.voorraad** en **Afrondings****regel**. 

De waarde in het veld **Factor** wordt vermenigvuldigd met het bronbedrag om het bedrag in het budgetplan in te stellen. U kunt vervolgens correcties maken wanneer u budgetplanregels maakt. U kunt bijvoorbeeld **1,03** invoeren voor een stijging van 3%. De factor moet een positief getal zijn. 

In het veld **Minimum** kunt u het drempelbedrag instellen voor het maken van een budgetplanregel. Als het bronbedrag kleiner is dan dit getal is, wordt de budgetplanregel niet gemaakt. Met een waarde van **0,00** zijn alle bedragen toegestaan, maar zijn regels niet beperkt tot positieve bedragen. (Als geen waarde wordt ingevuld, worden regels beperkt tot positieve bedragen. Negatieve bedragen worden altijd opgenomen en vertegenwoordigen meestal creditposten.)

In het veld **Afrondingsregel** kunt u de nauwkeurigheid van de budgetplanregels instellen die worden gemaakt. U kunt bedragen afronden naar de dichtstbijzijnde 1,00, 10,00, 100,00, enzovoort van valuta.

## <a name="notes-for-specific-processes"></a>Opmerkingen voor specifieke processen
### <a name="generate-budget-plan-from-general-ledger"></a>Budgetplan genereren op basis van grootboek

Wanneer u een budgetplan van grootboekgegevens maakt, moet u het veld **Totaal samentellen volgens** instellen op **Fiscaal jaar** als de optie **Historisch** is ingesteld op **Nee**. De perioden en de datums in de bron komen mogelijk niet overeen met de perioden in datums in het doel. Omdat het proces geen betrouwbare manier heeft om deze waarden toe te wijzen, moet u het proces tot de eerste van het jaar beperken. 

In het doel is het veld **Budgetklasse** ingesteld op **Onkosten** of **Opbrengst**. Deze instelling wordt gebruikt om het kenmerk **Budgettype** te selecteren voor regels die worden gemaakt, wanneer de hoofdrekening op een regel niet van het type **Opbrengst** of **Onkosten** is.

### <a name="generate-budget-plan-from-fixed-assets"></a>Budgetplan genereren op basis van vaste activa

Het proces **Budgetplan genereren op basis van vaste activa** heeft geen optie voor samenvoeging per periode of dag. Er is ook geen optie om het plan als historisch in te stellen. U kunt dit periodieke proces gebruiken om verwachte transacties voor vaste activa in uw budgetplanning op te nemen.

### <a name="generate-budget-plan-from-forecast-positions"></a>Budgetplan genereren op basis van prognoseposities

Het proces **Budgetplan genereren op basis van prognoseposities** wijst de bronprognosepositie toe aan de budgetplanregel. U kunt de positie weergeven door de prognosepositie toe te voegen als rij in de budgetplanindeling of door de query **Budgetplanregels** te gebruiken. Als u niet wilt dat de prognosepositie wordt toegewezen aan budgetplanregels, stelt u de optie **Positie opnemen op budgetplanregel** in op **Nee**.

Regels in het budgetplan worden samengevoegd per grootboekrekening en positie. U kunt het positienummer echter uitsluiten zodat regels alleen per grootboekrekening worden samengevoegd. Op het **Doel** tabblad, stelt u de optie **Positie opnemen op budgetplanregel** in op **Nee**.

In het veld **FTE-scenario voor budgetplan** kunt u een scenario selecteren om het aantal fulltime equivalenten (FTE's) in het budgetplan op te nemen. Dit veld is alleen beschikbaar voor scenario's met hoeveelheidstype die zijn opgenomen in de indeling van het doelbudgetplan. Als u een FTE-scenario selecteert, moet u ook een FTE-hoofdrekening selecteren. Deze rekening wordt gebruikt om de regels van hoeveelheidsbudgetplan te maken. 

Het budgetplanningsproces en budgetplanscenario die in de bron zijn geselecteerd stellen het budgetplanningsproces en budgetplanscenario van het doelscenario in. Omdat deze kenmerken aan prognoseposities worden toegewezen, moeten ze overeenkomen met het budgetplan. Daarom kunnen deze kenmerken niet worden gewijzigd in de doelstelling.

### <a name="generate-budget-plan-from-project-forecasts"></a>Budgetplan genereren op basis van projectprognoses

Het proces **Budgetplan genereren op basis van projectprognoses** bevat net zoals het proces **Budgetplan genereren op basis van prognoseposities** een optie om projecthoeveelheden (uren, onkosten, en artikelen) in een hoeveelheidsscenario op te nemen. De twee processen hebben tevens vergelijkbare filters voor de kolommen in de budgetplanindeling. 

Op het **Bron** tabblad, definiëren drie opties in de sectie **Overzicht opnemen** welke budgetplanregels worden gemaakt. Deze opties zijn gelijk aan de opties die beschikbaar zijn als u rechtstreeks budgetjournaalposten maakt van projectprognoses. Stel de **Verlies-en-winstrekening** optie in op **Ja** om regels voor kosten en voor opbrengsten te maken. Stel de **OHW** optie in op **Ja** als u onderhandenwerkinvoeren wilt maken. Stel de **Salaristoewijzing** optie in op **Ja** om regels te maken voor loonlijsttegenrekeningen voor uurtransacties. 

Er is geen veld **Butgetklasse**, omdat de budgetklasse (**Onkosten** of **Opbrengst**) wordt bepaald door de bron. 

U kunt projectbudgetten als bron gebruiken door het prognosemodel te selecteren dat de projectbudgetbedragen bevat. Denk eraan dat de projectbudgetten projectprognoseregels maken als ze worden goedgekeurd.

Om alleen kosten en opbrengsten voor de budgetplanregels te selecteren, gebruikt u het filter om **Updates budget: Type bedrag = Kosten** te selecteren. Als u slechts één type prognose wilt selecteren, gebruikt u het filter **Budgetupdates: Transactietype = *xxx*** te selecteren. 

Slechts één prognosemodel kan worden gebruikt om een scenario van het budgetplanscenario te genereren. Als u het proces voor een prognosemodel en dan een update uitvoert en probeert een ander model op te geven, wordt het eerste model overschreven als hetzelfde project en dezelfde grootboekrekeningen van toepassing zijn. U kunt een budgetplanscenario genereren van meer dan één prognosemodel door in verschillende budgetplanscenario's te genereren en de toewijzingsopties te gebruiken om deze samen te voegen in een ander scenario. 

Het proces **Budgetplan genereren op basis van projectprognoses** wijst ook het bronproject toe aan de budgetplanregel.

### <a name="generate-budget-plan-from-supply-forecast"></a>Budgetplan genereren op basis van aanbodprognose

De opties van het bronfilter in het proces **Budgetplan genereren op basis van aanbodprognose** waren gemodelleerd op basis van opties in de functie **Inkoopbudget naar grootboek overboeken**, vanwege gelijkenissen tussen het proces en de functie.

### <a name="generate-budget-plan-from-demand-forecast"></a>Budgetplan genereren op basis van vraagprognose

Voor het proces **Budgetplan genereren op basis van vraagprognoses** kunt u de optie **Verkooporder** instellen op **Ja** om opbrengstregels in het budgetplan te genereren, het **Verbruik** instellen op **Ja** om onkostenregels te maken of beide opties instellen op **Ja**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Budgetplan genereren op basis van budgetregistervermeldingen

Voor het proces **Budgetplan genereren op basis van budgetregistervermeldingen** moet de bron één submodel, één budgetcode, en één invoernummer opgeven. Met andere woorden, kunt u de budgetplanregels voor slechts één budgetjournaalregel tegelijk maken. U kunt extra vermeldingen in hetzelfde budgetplan gebruiken door één proces uit te voeren voor elke broninvoer.

### <a name="generate-budget-plan-from-budget-plan"></a>Budgetplan genereren op basis van budgetplan

Voor het proces **Budgetplan genereren op basis van budgetplan** kunt u een met aanvullende reeks opties op het tabblad **Doel** nieuwe financiële dimensies toewijzen. Als een financiële dimensie wordt geselecteerd, wordt die waarde gebruikt voor alle regels van het budgetplan. Daarom kunt u één budgetplan gebruiken als basis voor andere budgetplannen, maar kunt u ook, bijvoorbeeld, een andere afdeling of kostenplaats toewijzen aan de nieuwe budgetplannen.

## <a name="looking-back-from-the-budget-plan"></a>Terugkijken vanuit het budgetplan
### <a name="budget-plans-by-dimension-set-inquiry"></a>Budgetplannen weergeven per dimensiesetquery

De query **Budgetplannen per dimensieset** bevat meerdere opties waarmee u een query kunt uitvoeren om de bron van de budgetplangegevens te identificeren. 

Selecteer een regel en klik op de knop **Budgetplanregels** om de query **Budgetplanregels** uit te voeren. De resultaten worden gefilterd voor de dimensiewaarden van de geselecteerde regel. U kunt vervolgens aanvullende parameters toepassen. 

Gebruik de knoppen **Aanbodprognose** en **Vraagprognose** om deze query's uit te voeren. In beide gevallen zoekt de query prognoseregels die de budgetplanregels gemaakt zouden kunnen hebben. 

Extra rapporten die beschikbaar zijn, omvatten het rapport **Prognoseposities per budgetplan**. Dit rapport is vooral nuttig als u wilt bepalen of een positie correct aan budgetplannen is toegewezen.





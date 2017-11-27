---
title: Stuklijstberekeningsgroepen
description: Dit artikel bevat informatie over berekeningsgroepen voor stuklijsten en het instellen hiervan. Als u een stuklijstberekening wilt uitvoeren, moet u berekeningsgroepen instellen en deze toewijzen aan afzonderlijke artikelen, of een standaardberekeningsgroep instellen. De berekeningsinstellingen van de berekeningsgroep worden vervolgens gebruikt als standaardwaarden op de pagina Sstuklijstberekening op het moment van de berekening van de stuklijst.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 48d1bc67038c6080bb96d524a549deddbc8d4e0b
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="bom-calculations-groups"></a>Stuklijstberekeningsgroepen

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie over berekeningsgroepen voor stuklijsten en het instellen hiervan. Als u een stuklijstberekening wilt uitvoeren, moet u berekeningsgroepen instellen en deze toewijzen aan afzonderlijke artikelen, of een standaardberekeningsgroep instellen. De berekeningsinstellingen van de berekeningsgroep worden vervolgens gebruikt als standaardwaarden op de pagina Sstuklijstberekening op het moment van de berekening van de stuklijst. 

Een standaard berekeningsgroep is vereist op de pagina **Parameters voor voorraad- en magazijnbeheer** of een productspecifieke berekeningsgroep is vereist op de pagina **Vrijgegeven productdetails**. Er wordt eerst gezocht naar de configuratie van de berekeningsgroep op de pagina **Vrijgegeven productdetails**. Als er daar geen berekeningsgroep wordt gevonden, wordt op de pagina **Parameters voor voorraad- en magazijnbeheer** gezocht. Als geen berekeningsgroep kan worden gevonden, ontvangt de gebruiker een foutbericht tijdens de berekening. Een berekeningsgroep bevat beleidsregels voor het kostprijsmodel, het verkoopprijsmodel en de controlelijst voor waarschuwingen. De berekeningsinstellingen van de berekeningsgroep worden gebruikt als standaardwaarden op de pagina **Sstuklijstberekening** op het moment van de berekening van de stuklijst.

## <a name="purposes-of-bom-calculation-groups"></a>Toepassing van stuklijstberekeningsgroepen
U wijst een stuklijstberekeningsgroep om verschillende redenen toe aan artikelen:

-   Door het veld **Kostprijsmodel** in te stellen, geeft u de bron van de kostenbijdragegegevens van een ingekocht onderdeel aan bij het berekenen van de geplande kosten van een gefabriceerd artikel. Sommige fabrikanten berekenen geplande kosten door de gesloten overeenkomsten over de inkoopprijs voor ingekochte onderdelen of een andere basis te gebruiken, zoals de records met inkoopprijzen in een kostprijsberekeningsversie.
-   Door het veld **Verkoopprijsmodel** in te stellen, geeft u aan hoe de gegevens van het artikel worden gebruikt om een voorgestelde verkoopprijs te berekenen. U kunt de verkoopprijs van het artikel of de kostengroep opgeven. Sommige fabrikanten willen een voorgestelde verkoopprijs voor gefabriceerde artikelen berekenen. De berekende verkoopprijs kan een aanpak met een totaalprijs zijn die is gebaseerd op de verkoopprijsrecord van het onderdeel. De berekende verkoopprijs kan ook een aanpak van kostprijs plus opslag weerspiegelen die is gebaseerd op de kostprijs van het onderdeel en het toepasselijke winstpercentage, dat is gekoppeld aan de kostengroep van het artikel.
-   Door gebruik te maken van het veld **Explosie stoppen**, geeft u aan dat een gefabriceerd artikel moet worden beschouwd als een ingekocht artikel voor kostenaggregatie tijdens stuklijstberekeningen. Veelvoorkomende scenario's zijn een ingekocht artikel dat soms wordt gefabriceerd of een gefabriceerd artikel dat nu wordt ingekocht. Het artikel wordt in eerste instantie aangemerkt als een gefabriceerd artikel om de stuklijsten en routegegevens te kunnen definiëren en om de productieorders voor het artikel te kunnen ondersteunen. De vlag **Explosie stoppen** voorkomt echter dat bij kostenberekeningen gebruik wordt gemaakt van de stuklijst en route van het artikel. In plaats daarvan worden bij de stuklijstberekening de opgegeven kosten van het artikel gebruikt.

## <a name="calculation-groups"></a>Berekeningsgroepen
U definieert berekeningsgroepen onder **Instelling vooraf bepaald kostenbeleid** in Kostenbeheer. Via berekeningsgroepen die zijn toegewezen aan artikelen kunt u opgeven hoe de kostprijs of verkoopprijs van onderdelen, zoals aangegeven door de berekeningsgroep, als bron voor de berekening worden gebruikt. Op de pagina **Berekeningsgroepen** kunt u een kostprijsmodel, een alternatieve kostprijsmodel, een verkoopprijsmodel en waarschuwingen definiëren.

### <a name="cost-price-model"></a>Kostprijsmodel

Er zijn vier opties voor het veld **Kostprijsmodel**:

-   **Kostprijs van artikel** – De kostprijs uit de tabel **Vrijgegeven product** wordt gebruikt, of de combinatie van artikeldimensies wordt als kostprijs gebruikt.
-   **Inkoopsprijs van artikel** – De inkoopprijs uit het veld **Kostprijs** op het tabblad **Inkoop** van de pagina **Vrijgegeven productlijst** wordt gebruikt.
-   **Handelsovereenkomsten** – U kunt handelsovereenkomsten configureren voor specifieke combinaties van artikelen en leveranciers of voor specifieke locaties. Vervolgens worden, als u hier de optie **Handelsovereenkomsten** selecteert, de handelsovereenkomst die u hebt gemaakt voor de inkoopprijs samen met het artikel en de locatie gebruikt.
-   **Voorraadprijs** – De huidige voorraadwaarde van het artikel wordt gebruikt voor het berekenen van de kosten per eenheid bij de berekening van de stuklijst. Een kostprijs per eenheid wordt alleen berekend als de geboekte hoeveelheid en de fysieke hoeveelheid groter zijn dan 0 (nul).

### <a name="alternative-cost-price"></a>Alternatieve kostprijs

Het veld **Alternatieve kostprijs** heeft dezelfde opties als het veld **Kostprijsmodel**. Dit veld wordt echter alleen gebruikt als geen prijs kan worden gevonden in het primaire kostprijsmodel.

### <a name="sales-price-model"></a>Verkoopprijsmodel

Er zijn twee opties voor de berekening van het veld **verkoopprijzen**:

-   **Kostengroep** – Wanneer deze optie is geselecteerd, wordt de verkoopprijs berekend op basis van de kostprijs en het winstinstellingspercentage uit de kostengroep.
-   **Verkoopprijs van artikel** – Wanneer deze optie is geselecteerd, wordt de verkoopprijs op het sneltabblad **Verkoop** uit de tabel Vrijgegeven product gebruikt.

### <a name="stop-explosion"></a>Explosie stoppen

Het selectievakje **Explosie stoppen** wordt gebruikt om aan te geven wanneer een geproduceerd artikel moet worden behandeld als een inkoopartikel. Normaal gesproken laat u het selectievakje **Explosie stoppen** uitgeschakeld. Door dit selectievakje in te schakelen, geeft u aan dat een gefabriceerd artikel bij de stuklijstberekening moet worden behandeld als ingekocht onderdeel in plaats van als gefabriceerd onderdeel. Afhankelijk van de site, kunnen de kosten van het artikel nog steeds worden berekend via stuklijstberekeningen. De explosie van geplande inkooporders en productie-orders wordt gestopt voor de stuklijst waarvan de onderdelen zijn gekoppeld aan de berekeningsgroep waarvoor het selectievakje **Explosie stoppen** is ingeschakeld. Via de hoofdplanning worden de geplande orders op de stuklijst zelf gegenereerd en niet op de artikelen die zijn opgenomen in de stuklijst. In principe geeft u door het inschakelen van dit selectievakje aan dat een kostenpost niet wordt toegevoegd bij de stuklijstberekening voor artikelen met deze berekeningsgroep.

### <a name="warnings"></a>Waarschuwingen

Op het sneltabblad **Waarschuwingen** selecteert u de opties voor alle waarschuwingsberichten die gebruikers ontvangen als zij stuklijstberekeningen uitvoeren. 

Als u bijvoorbeeld het selectievakje **Geen stuklijst** inschakelt, ontvangt de gebruiker een waarschuwing als er geen actieve stuklijstversie is gevonden voor een van de onderdelen of voor het bovenliggende artikel waarvoor de berekening van de stuklijst wordt uitgevoerd. Als u het selectievakje **Geen route** inschakelt, ontvangt de gebruiker een waarschuwing als geen actieve routeversie is gevonden. Als u bronnen op uw routes en bewerkingen gebruikt, kunt u het systeem instrueren om te controleren op deze bronnen. Als vervolgens geen bron wordt gevonden op elke regel in de actieve route, ontvangt de gebruiker een waarschuwing. 

U kunt ook verifiëren en controleren voor verbruik. Verbruik is de hoeveelheid in een bepaalde route. Meestal geeft dit de hoeveelheid tijd aan die nodig is om een specifieke bewerking in een productieproces uit te voeren. U kunt controleren of een artikel geen kostprijs heeft. Als er geen actieve kostprijs voor een artikel is, worden geen kosten opgeteld bij de berekening van de stuklijst. 

U kunt ook de leeftijd van de kostprijs controleren en verifiëren. Voer bijvoorbeeld **60** in om aan te geven dat de kostprijs per eenheid na 60 dagen opnieuw moet worden geëvalueerd. Als deze limiet is bereikt, wordt een waarschuwing gegenereerd in het systeem. Stel bijvoorbeeld dat een kostprijs is ingevoerd voor een artikel in januari van dit jaar. Als het nu augustus is, oftewel meer dan 60 dagen nadat de kostprijs is ingevoerd, ontvangt de gebruiker een waarschuwing wanneer de stuklijstberekening wordt uitgevoerd. U kunt eenj percentage invoeren in het veld **Minimale brutowinstbijdrage**. Deze waarde geeft het punt aan waarop de minimale brutowinstbijdrage niet wordt gehaald. Als de brutowinstbijdrage voor een bepaald onderdeel niet is gehaald, ontvangt de gebruiker een waarschuwing. Daarom helpt dit veld garanderen dat u de kosten en de extra opslagkosten die mogelijk zijn vereist voor uw artikelen niet onderbiedt.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Standaardinstellingen in Parameters voor voorraad- en magazijnbeheer

Omdat berekeningsgroepen zijn vereist voor de uitvoering van berekeningen, moet u een standaardberekeningsgroep instellen in de parameters voor voorraadbeheer. Deze instellingen stellen bedrijven in staat een standaardkostengroep en winstinstelling te hebben voor alle artikelen. Als vervolgens voor een bepaald artikel speciale berekeningsvereisten gelden, kan de gebruiker een andere berekeningsgroep toewijzen aan dat artikel. Normaal gesproken kunt u berekeningsgroepen instellen op artikelen in onderdelen van de stuklijst in plaats van op stuklijstartikelen. Als echter waarschuwingsberichten worden weergegeven, kunnen berekeningsgroepen worden toegepast. Een berekeningsgroep die wordt toegewezen aan artikelen heeft voorrang op de standaardwaarde die is ingesteld in de parameters voor voorraadbeheer. 

U kunt de standaardparameter instellen onder **Kostenbeheer** &gt; **Instelling voor boekhoudingbeleid voorraad** &gt; **Parameters** &gt; **Voorraadboekhouding** &gt; **Berekeningsgroep**. Door een standaardconfiguratiegroep in te stellen, kunt u tevens de waarschuwingsvoorwaarden configureren waarin gebruikers wordt gevraagd tijdens de berekening van de stuklijst of de geselecteerde onderdelen mogelijk berekeningsfouten kunnen veroorzaken.

### <a name="view-warning-messages-on-the-complete-page"></a>Waarschuwingsberichten weergeven op de pagina Voltooid

Een stuklijstberekening genereert waarschuwingsberichten. U kunt de waarschuwingen over een geselecteerd artikel weergeven. Maak bijvoorbeeld een nieuwe verkooporder voor artikel D0001 in Verkoop en marketing. Klik vervolgens op de verkooporderregel in het menu **Regel bijwerken** op **Gebaseerd op stuklijst/formule** om de berekeningsdetails en waarschuwingen weer te geven. U kunt resultaten van stuklijstberekeningen ook weergeven op de pagina **Voltooid**. Voor de waarschuwingsberichten gelden er slechts twee waarschuwingsvoorwaarden voor gefabriceerde artikelen, terwijl er vier waarschuwingsvoorwaarden gelden voor elk artikel:
-   Er wordt aangegeven wanneer er voor een gefabriceerd artikel geen actieve stuklijst aanwezig is.
-   Er wordt aangegeven wanneer er voor een gefabriceerd artikel geen actieve route aanwezig is.
-   Er wordt aangegeven wanneer het artikel op een stuklijstregel een hoeveelheid van nul (0) heeft.
-   Er wordt een waarschuwing aangegeven wanneer het artikel op een stuklijstregel een kostprijs van nul (0) heeft of wanneer er geen kostenrecord is.
-   Er wordt een waarschuwing aangegeven wanneer de kostprijs voor het artikel op een stuklijstregel is verlopen. De waarschuwing bevat een vergelijking van de berekeningsdatum met de opgegeven dagen voor een maximale levensduur van kostprijzen.
-   Er wordt een waarschuwing aangegeven wanneer het artikel op een stuklijstregel een lager winstpercentage dan gewenst heeft.

Afhankelijk van uw vereisten voor variaties in waarschuwingsberichten kunt u meerdere stuklijstberekeningsgroepen definiëren. Eén stuklijstberekeningsgroep met waarschuwingsvoorwaarden over een actieve stuklijst, een hoeveelheid van 0 (nul) onderdelen en een kostprijs van de onderdelen van 0 (nul) kan bijvoorbeeld voldoende zijn. Wanneer u een stuklijstberekening start, kunt u de toepasselijke waarschuwingsvoorwaarden die aan de stuklijstberekeningsgroep zijn gekoppeld, overschrijven. U kunt ook waarschuwingsvoorwaarden toevoegen of verwijderen. Wanneer bijvoorbeeld geen routegegevens nodig zijn voor de huidige situatie, kunt u de waarschuwingsvoorwaarde over een actieve route verwijderen. **Opmerking:** Tijd en aanwezigheid bevat een pagina **Berekeningsgroepen**, maar die pagina heeft geen betrekking op stuklijstberekeningsgroepen. In Tijd en aanwezigheid kunnen werknemers worden toegewezen aan berekeningsgroepen die de groepering weergeven van werknemers die zijn gekoppeld aan dezelfde supervisor of manager. Het berekenen van de registratie van werknemers kan automatisch plaatsvinden of handmatig door een supervisor of manager worden uitgevoerd.





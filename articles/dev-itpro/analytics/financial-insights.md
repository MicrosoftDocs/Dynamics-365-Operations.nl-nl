---
title: Financial Insights
description: "Financial Insights gebruikt Microsoft Power BI om KPI's, grafieken en financiële overzichten samen te voegen."
author: kweekley
manager: AnnBe
ms.date: 02/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6679215a664ddf938a204196b00f3bc28bf65f8f
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="financial-insights"></a>Financial Insights

[!include [banner](../includes/banner.md)]

**Financial Insights** gebruikt Microsoft Power BI om KPI's, grafieken en financiële overzichten samen te voegen. Power BI is ingesloten in Microsoft Dynamics 365 Finance and Operations.
De focus van **Financial Insights** is analytische rapportage. Persoonlijkheden binnen een organisatie kunnen weergeven, onderzoeken en reageren. 

**Financial Insights** combineert gegevens uit het grootboek en subjournalen om een completer beeld te geven van de financiële toestand van een organisatie.

> [!NOTE] 
> Dit document gebruikt de volgende Power BI-terminologie:                                                                           
**Rapport**: een enkel .pbix-bestand waarin alle visuele elementen op alle tabbladen worden opgeslagen.                                                          
**Pagina**: een tabblad in een enkel .pbix-bestand. Elke pagina kan een of meer visuele elementen bevatten.                                                     
**Zichtbaar**: één bron van gegevens, zoals een kaart, KPI, diagram, grafiek, matrix of financieel overzicht. Een pagina met een financieel overzicht als visueel element kan geen andere visuele elementen hebben vanwege de grootte van de gegevens waarover wordt gerapporteerd.


Op dit moment wordt **Financial Insights** gebruikt om gegevens voor de actieve rechtspersoon of alle rechtspersonen te bekijken. In toekomstige versies verandert de werkruimte tot een plaats waar u Power BI kunt gebruiken om visuele elementen te bewerken en te maken.

De werkruimte **CFO-overzicht** toont de dezelfde visuele elementen als **Financial Insights**, maar is gericht op laten weergeven en filteren van de gegevens in bestaande rapporten. In toekomstige versies is het mogelijk nieuwe visuele elementen toe te voegen aan de werkruimte **Financial Insights**. De nieuwe visuele elementen zijn wellicht ook beschikbaar in werkruimten die zijn gericht op andere functies, zoals projectmanagers of leveranciermanagers. De werkruimte **CFO overzicht** blijft gegevens tonen voor alle rechtspersonen, ongeacht de rechtspersonen waartoe de rol toegang heeft.

## <a name="finance-and-operations-setup"></a>Instelling van Finance and Operations
**Grootboek**

Het hoofdrekeningtype en de hoofdrekeningcategorieën worden gebruikt om de juiste standaardhoofdrekeningen in te vullen op het financieel overzicht **Balans** en de verschillende **winst- en verliesrekeningen** in **Financial Insights**.

Op de pagina **Hoofdrekeningen** moet u uw hoofdrekening definiëren zodat er een van de volgende typen aan wordt toegewezen:

•   Opbrengst

•   Onkosten

•   Activa

•   Verplichtingen

•   Eigen vermogen

Wijs geen ander hoofdrekeningtype, zoals **Balans** of **Winst en verlies**, aan uw hoofdrekeningen toe. Rapportage kan niet het type hoofdrekening bepalen wanneer andere typen hoofdrekeningen worden toegewezen, omdat deze niet gedetailleerd genoeg zijn. Het type hoofdrekening moet worden bepaald om verplichtingen en opbrengst weer te geven als positieve bedragen in financiële rapporten.

Om op de financiële overzichten te worden weergegeven en te worden opgenomen in diverse andere visuele elementen, zoals KPI's, moet aan elke hoofdrekening een hoofdrekeningcategorie worden toegewezen. De hoofdrekeningcategorieën zijn verbeterd, zodat ze een weergavevolgorde bevatten. De weergavevolgorde wordt specifiek gebruikt in financiële overzichten in **Financial Insights**. Nadat u een hoofdrekeningcategorie hebt bewerkt of toegevoegd, kunt u de waarde van de **weergavevolgorde** wijzigen om de volgorde te definiëren waarin hoofdrekeningcategorieën kunnen worden weergegeven in een financieel overzicht. Als u de weergavevolgorde voor veel hoofdrekeningcategorieën moet wijzigen, kunt u de functie Openen in Excel gebruiken om snel te bewerken en de wijzigingen weer te publiceren in Finance and Operations.


## <a name="entity-store"></a>Entiteitopslag
De gegevens voor **Financial Insights** worden gehaald uit de entiteitopslag (**Systeembeheer** > **Instellen** > **Entiteitopslag**). Als u de werkruimte **CFO-overzicht** of **Financial Insights** opent en het volgende waarschuwingsbericht wordt weergegeven in de visuele elementen, moet u de entiteiten bijwerken.
 
![Waarschuwing](./media/Cantdisplay.png)

U moet de volgende entiteiten bijwerken om gegevens te zien in de werkruimten **Financial Insights** en **CFO-overzicht**:

•   CustCollectionsBIMeasurements

•   FinancialReportingOtherData

•   FinancialReportingReferenceData

•   FinancialReportingTransactionData

•   LedgerCovLiquidityMeasurement

•   Inkoop-cube

•   Verkoop-cube

In de vorige versie werden de entiteiten LedgerActivityMeasure en VendPaymentBIMeasure gebruikt voor gegevens in de werkruimte **CFO-overzicht**. Ze worden echter niet meer gebruikt in de huidige versie.

U kunt een terugkerende batch definiëren om de gegevens in de entiteiten regelmatig bij te werken. Omdat elke entiteit volledig opnieuw wordt gemaakt tijdens een update, selecteert u de tijd en de frequentie van entiteitupdates zorgvuldig. De primaire entiteit die wordt gebruikt voor financiële overzichten, is de FinancialReportingTransactionData-entiteit. U kunt daarom die entiteit vaker bijwerken.

## <a name="security"></a>Beveiliging
De gegevens in ingesloten Power BI-rapporten kunnen momenteel niet worden beperkt tot de rechtspersonen waartoe de gebruiker toegang heeft. Daarom worden de ingesloten Power BI-rapporten beheerd via functies in de instelling van de beveiliging. De functies die zijn gedefinieerd, verlenen toegang tot gegevens voor alle rechtspersonen of alleen het actieve bedrijf. In de volgende tabel ziet u de functies die beschikbaar zijn en de rollen waaraan ze zijn toegewezen. De functies kunnen worden verwijderd of toegewezen aan andere rollen, op basis van de behoeften van uw organisatie.

| **Functie**                     | **Rollen**                                       | Beschrijving                     |
|------------------------------|-------------------------------------------------|-----------------|
| Werkgebied CFO-overzicht weergeven  | CFO (Chief Financial Officer)                         | •    Deze functie biedt toegang tot de werkruimte CFO-overzicht. •  Standaard wordt het actieve bedrijf gebruikt als filter. U kunt echter alle rechtspersonen toevoegen, ongeacht of de gebruiker toegang tot de andere rechtspersonen heeft.               |
| Financiële inzichten voor huidig bedrijf weergeven | •   Accountant • Accounting manager • Accounting supervisor • Auditor • Budgetmanager • CEO • CFO • Financieel controller  |   • Deze functie geeft toegang tot Financial Insights. •  Standaard wordt het actieve bedrijf gebruikt als filter. U kunt geen andere rechtspersonen toevoegen.            |
| Financiële inzichten voor geheel bedrijf weergeven   | •   In Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3, is deze functie niet toegewezen aan een rol. • In de volgende versie wordt deze functie toegewezen aan de rol van CFO. | •    Deze functie biedt toegang tot de menuoptie voor de werkruimte CFO-overzicht. •    Standaard wordt het actieve bedrijf gebruikt als filter. U kunt echter alle rechtspersonen toevoegen, ongeacht of de gebruiker toegang tot de andere rechtspersonen heeft.             |


## <a name="financial-reporting-vs-finanical-insights"></a>Financiële rapportage versus Financial Insights
Hoewel **Financial Insights** financiële overzichten bevat, is het geen vervanging voor Financiële rapportage in Finance and Operations. De standaard financiële overzichten in **Financial Insights** zijn beperkt in bereik en bevatten niet alle soorten financiële overzichten. Financiële rapportage is nog steeds het primaire hulpmiddel voor het ontwerpen, maken en genereren van wettelijke financiële overzichten.

Op basis van het volgende vergelijkingsdiagram kunt u onderscheid maken tussen de twee opties:


|                                                                       |               <strong>Financiële rapportage</strong>                |                                      <strong>Financial Insights</strong>                                      |
|-----------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
|                 <strong>Standaardrapporten bewerken</strong>                 |                                Ja                                |                                                      Nee                                                       |
|                  <strong>Nieuwe rapporten maken</strong>                  |                                Ja                                |                                                      Nee                                                       |
|                    <strong>Rapporten afdrukken</strong>                     |                                Ja                                |                                                      Nee                                                       |
|                   <strong>Exporteren naar Excel</strong>                    |                                Ja                                |                           Beperkt Exporteert onbewerkte gegevens naar Excel, niet opgemaakt rapport                           |
|  <strong>Ondersteuning van rapporthiërarchie/organisatiehiërarchie</strong>  |                                Ja                                |                                                      Nee                                                       |
|               <strong>Rapport van gegevens in subadministratie</strong>               |               Ja Beperkt tot alleen leverancier, klant                |                 Ja Leverancier, klant, leverancier-/klantgroepen, leverancier-/klantadressen, enz.                 |
|                  <strong>Aangiftevaluta</strong>                  |    Ja Valuta voor boekhouding en omzetten naar aangiftevaluta    |                                          Nee Alleen valuta voor boekhouding                                          |
|                       <strong>Beveiliging</strong>                       | Ja Voldoet aan Finance and Operations beveiliging van rapportstructuur | Beperkt Rapporten weergeven voor alle bedrijven (ongeacht de beveiliging van Finance and Operations) of alleen actief bedrijf |
| <strong>Ondersteuning voor verschillende rekeningschema's en fiscale jaren</strong> |                                Ja                                |                                                      Nee                                                       |
|               <strong>Rapport van externe gegevens</strong>                |                                Nee                                 |                                                      Nee                                                       |
|                <strong>Consolidaties ondersteunen</strong>                |                                Ja                                |                   Beperkt Kan rapporteren over meerdere bedrijven, maar alleen valuta voor boekhouding gebruiken                   |

Naast de gebruikersinterface in het oorspronkelijke werkgebied **CFO-overzicht** zijn nu nieuwe KPI's, diagrammen en financiële overzichten beschikbaar. De volgende financiële overzichten zijn beschikbaar:

•   Proefbalans

•   Balans

•   Winst- en verliesrekening per regio

•   Winst- en verliesrekening - werkelijk versus budget

•   Winst- en verliesrekening met afwijkingen

•   Trendinkomensoverzicht van 12 maanden

•   Onkosten driejarige trend

•   Onkosten per leverancier

•   Verkopen per klant

## <a name="edit-visuals"></a>Visuele elementen bewerken
In de eerste versie van **Financial Insights** kan geen van de visuele elementen worden bewerkt. In toekomstige versies kunnen gebruikers met de juiste beveiliging nieuwe visuele elementen maken, bestaande visuele elementen kopiëren en visuele elementen bewerken. Hoewel de .pbix-bestanden die de rapporten bevatten als resources beschikbaar zijn, wordt niet aanbevolen dat u de standaardrapporten bewerkt. Er worden aanvullende wijzigingen aangebracht in de visuele elementen gegevensmodel, standaardrapporten en aangepaste financiële overzichten die worden gebruikt om de financiële overzichten te maken. Dus als u wilt profiteren van nieuwe functies en wijzigingen aan het gegevensmodel in de volgende versie, moet u eventuele wijzigingen die u hebt aangebracht aan de standaardrapporten via Microsoft Power BI-bureaublad opnieuw aanbrengen.


## <a name="filtering"></a>Filteren
Gebruikers kunnen het rapport filteren met behulp van het deelvenster **Filter** aan de linkerzijde. Dit venster is het hetzelfde venster dat beschikbaar is via Power BI-bureaublad.
Er zijn verschillende niveaus van filteren, waarvan sommige mogelijk niet beschikbaar zijn, afhankelijk van wat u hebt geselecteerd op een pagina (tabblad) en of u de detailanalysemogelijkheden gebruikt:

•   **Filters op rapportniveau**: deze filters worden toegepast op alle visuele elementen op alle pagina's (tabbladen).

•   **Filters op paginaniveau**: deze filters worden toegepast op alle visuele elementen op het actieve tabblad. Deze filters worden toegepast boven op filters op rapportniveau.

•   **Filters op het niveau van visuele elementen**: deze filters worden alleen toegepast op het geselecteerde visuele element. Deze filters worden toegepast boven op de filters op paginaniveau.

•   **Detailanalysefilter** : dit filter filtert van een visueel 'bron'-element dat op het huidige visuele element wordt toegepast wanneer u vanuit het visuele bronelement inzoomt op het huidige visuele element.

![Filter](./media/filter.png)


Als u een specifieke filterwaarde wilt verwijderen, selecteert u het gumsymbool ernaast. Verwijder geen filter door de X te selecteren. Als u de X selecteert, wordt het veld waarop u filtert verwijderd als filteroptie. Als u per ongeluk een veld uit het filter verwijdert, sluit u de werkruimte en opent u deze opnieuw. De standaardinstellingen voor het filter worden opnieuw toegepast.

Wanneer u werkruimten voor het eerst opent wordt standaard de actieve rechtspersoon gebruikt als filter op rapportniveau. Afhankelijk van hun beveiliging kunnen gebruikers mogelijk andere rechtspersonen toevoegen of de standaardrechtspersoon wijzigen die is geselecteerd in het filter.

Het filter **fiscale kalender** is vereist, zodat de juiste kalender wordt gebruikt voor het visuele element. Het filter op rapportniveau is standaard ingesteld op de fiscale kalender van de actieve rechtspersoon. Als u het filter wijzigt in een fiscale kalender met een andere begin- of einddatum, worden de beginsaldi niet opgenomen. Daarom geven uw **Balans** financiële overzichten niet de juiste saldi weer. Als u een extra fiscale kalender in het filter selecteert, hebt u een aanvullende reeks kolommen. Elke aanvullende reeks kolommen bevat de bedragen voor een andere fiscale kalender.

Het filter **boekingslaag** is ook vereist. Standaard is het filter ingesteld op Huidig. U kunt extra boekingslagen selecteren in het filter om de samengevoegde bedragen weer te geven.

Filters zijn ook beschikbaar voor de velden **Datum** en **Boekjaar**. Deze filters worden meestal toegepast op het paginaniveau. Standaard gebruikt het filter **Datum** een relationele datum die u kunt wijzigen. U kunt ook het relationele datumfilter verwijderen en in plaats daarvan het filter **Boekjaar** gebruiken.

## <a name="currency"></a>Valuta

Alle visuele elementen die over grootboekgegevens rapporteren tonen bedragen in de valuta voor boekhouding. Als u op de rechtspersoon filtert, moet u dus voorzichtig zijn dat u alleen rechtspersonen opneemt die dezelfde valuta voor boekhouding hebben. Anders voegt u gegevens in verschillende valuta's samen.

Alle visuele elementen die rapporteren over subjournaalgegevens, zoals de visuele elementen **Cashflowprognose** en **Top 10**, tonen bedragen in de systeemvaluta. De systeemvaluta en het systeemwisselkoerstype zijn gedefinieerd op de pagina **Systeemparameters**.

Het visuele element **Saldo per bankrekening** gebruikt bedragen in de valuta van de bankrekeningen.

## <a name="dimensions"></a>Dimensies

De financiële standaardoverzichten bevatten geen financiële dimensies, maar zijn alleen gericht op de hoofdrekening. Ondersteuning voor financiële dimensies zal beschikbaar zijn in toekomstige versies, wanneer de rapporten bewerkbaar worden. Organisaties kunnen vervolgens filteren op financiële-dimensiewaarden.

Sommige financiële overzichten bevatten dimensies die zijn gebaseerd op subjournaaltransacties. Het doel van de nieuwe financiële overzichten is te kunnen filteren op dimensies die niet zijn ingesteld als financiële dimensies. Met het standaardrapport Onkosten per leverancier kunt u bijvoorbeeld verder gaan dan de hoofdrekening, zodat u de saldi uitgesplitst per leverancier kunt zien. De leverancier is niet ingesteld als een financiële dimensie. In plaats daarvan keert het systeem terug naar de oorspronkelijke subjournaaltransactie om de leverancier te vinden.

De volgende dimensies worden gebruikt in de standaardrapporten. Geen van deze dimensies zijn financiële dimensies.

•   Leverancier

•   Leveranciersgroep

•   Klant

•   Klantgroep

•   Land/regio

•   Provincie

•   Plaats

> [!IMPORTANT] 
> Als u transacties voor meerdere leveranciers of klanten in één boekstuk samenvat met behulp van de financiële journalen, zijn de gegevens onjuist. Rapportage kan niet bepalen welke leverancier of klant is gekoppeld aan een bepaalde grootboekrekening in een journaalpost, omdat deze informatie nergens wordt onderhouden. Daarom raden we niet aan dat u meerdere leveranciers, klanten, vaste activa of projecten in één boekstuk invoert.

## <a name="drill-on-data"></a>Inzoomen op gegevens

Verschillende niveaus van inzoomen zijn beschikbaar via Power BI. Elk niveau heeft een andere naam en een andere functie. U kunt ook inzoomen op rijen en kolommen. In dit gedeelte worden de verschillende opties besproken met behulp van het financieel overzicht **Proefbalans** als een voorbeeld en het laat zien hoe u kunt inzoomen op de rijen. Dezelfde functionaliteit bestaat voor kolommen. U hoeft alleen de instelling **Inzoomen op** te wijzigen.

In het volgende voorbeeld is de **proefbalans**-instructie samengevouwen tot het hoogste niveau van de rijhiërarchie, het hoofdrekeningtype.

![Proefbalans](./media/trial-balance.png)

 
Als u het volgende niveau van de hiërarchie, de hoofdrekeningcategorieën, wilt weergeven, kunt u het veld **Inzoomen op** instellen op **Rijen** en vervolgens de knop **Uitvouwen** selecteren (de derde knop na het veld Inzoomen op). U ziet nu alle hoofdrekeningcategorieën uitgevouwen. Op dit moment kunt u met Power BI niet één rij of kolom uitvouwen, maar nog steeds alle andere rijen of kolommen zien.
 
![Proefbalans](./media/trial-balance2.png)
 
  
Als u wilt uitvouwen naar de hoofdrekeningen voor alle rijen, kunt u weer de knop **Uitvouwen** gebruiken. Echter, als u wilt inzoomen naar de hoofdrekeningen voor slechts één rij, selecteert u eerst de knop **Inzoomen** (de enkele pijl-omlaag aan de rechterkant van het venster) en selecteert u vervolgens de rij waarop u wilt inzoomen. In de volgende afbeelding ziet u het resultaat wanneer de rij **Verkoop** is geselecteerd nadat de knop **Inzoomen** is geselecteerd.

![Proefbalans](./media/trial-balance3.png)

Nadat u op één rij inzoomt, zijn er meerdere klikken nodig om terug te keren naar de volledige proefbalans. De knop **Uitzoomen** (de eerste knop na **inzoomen** op veld) zoomt alleen uit in de context van de categorie **Verkoop**, zoals in de volgende afbeelding wordt weergegeven.
 
![Proefbalans](./media/trial-balance4.png)
 
 
U kunt de knop **Uitzoomen** blijven gebruiken om terug te keren naar het hoogste niveau van samenvatting voor de rijen.

Power BI heeft ook een knop waarmee u naar het volgende niveau in de hiërarchie gaat (de tweede knop na het veld **Inzoomen op**). Het effect van deze knop verschilt van het effect van de knop **Uitvouwen** (de derde knop na het veld **Inzoomen op**), die wordt gebruikt om de hiërarchie uit te vouwen. Wanneer u de hiërarchie uitvouwt, wordt de hiërarchie onderhouden in het rapport. Zoals u bijvoorbeeld eerder gezien hebt, als u uitvouwt op het hoofdrekeningtype, ziet u nog steeds het hoofdrekeningtype in het rapport. Echter wanneer u naar een hoger niveau in de hiërarchie gaat, toont het rapport niet langer de bovenliggende in de hiërarchie, zoals in de volgende afbeelding wordt weergegeven.

![Proefbalans](./media/trial-balance5.png)

 
Als u de transactiedetails achter de samengevatte saldi wilt zien, kunt u enkele bedragen selecteren om terug te zoomen naar Finance and Operations.

Door terug te zoomen vanuit de financiële overzichten gaat u naar de Bronverkenner voor boekhouding (ASE), niet naar de boekstuktransacties. De ASE toont niet alleen de boekhoudingsposten in het grootboek. In plaats daarvan worden de details van de subjournaaltransactie getoond. Daarom krijgt u veel meer informatie over de brontransactie en kunt u deze gebruiken voor analyse. U kunt bijvoorbeeld zien wie de leverancier of klant was, wat de klant heeft gekocht of de leverancier heeft verkocht, en zelfs welk project zich in de transactie bevond.

De volgende filters uit de financiële overzichten worden verzonden naar de ASE, zodat de ASE de transacties samengevoegd weergeeft:

Vereiste velden voor het filteren van:

  - Rechtspersoon
 
  - Fiscale kalender
 
  - Jaar
 
  - Hoofdrekening-ID

Optionele velden voor filteren:

  - Kwartaal

  - Maand

  - Periode

Als u niet ver genoeg omlaag uitvouwt op een rij, werkt het inzoomen niet. Als u bijvoorbeeld alleen omlaag uitvouwt naar de hoofdrekeningcategorie, kunt u niet inzoomen in de ASE op de balans omdat de hoofdrekening een verplicht veld is voor filteren in de ASE.

Als u te ver omlaag uitvouwt op een rij, worden de extra filters op de financiële overzichten niet verzonden naar de ASE. Daarom kan er een verschil ontstaat in uw getallen. Bijvoorbeeld: als u omlaag uitvouwt naar het land of de regio in de rijen van het financiële overzicht Winst- en verliesrekening per regio, wordt het land of de regio niet opgenomen als een filter in de ASE.

> [!NOTE]
> U kunt verder omlaag inzoomen op rijen en kolommen van het financiële overzicht dan de ASE momenteel voor filteren ondersteunt. Daarom komt in sommige situaties de som van gedetailleerde transacties in de ASE niet overeen met het saldo waarop u uitzoomt. Deze functionaliteit wordt in de toekomst verder verbeterd.

## <a name="hierarchies"></a>Hierarchieën

De financiële standaardoverzichten gebruiken twee hiërarchieën om in te zoomen en uit te vouwen op de gegevens. Eén hiërarchie is voor de rijen en de andere hiërarchie is voor de kolommen. Beide hiërarchieën zijn vooraf ingesteld in het ontwerp van het financiële overzicht. Voor de meeste financiële overzichten is de rijhiërarchie **Hoofdrekeningtype** > **Hoofdrekeningcategorieën** > **Hoofdrekening**. Sommige rapporten hebben echter extra velden, zoals Land en Regio. De extra knooppunten van de hiërarchie zijn gebaseerd op subjournaalgegevens voor elke transactie.

Voor de kolommen is de hiërarchie gericht op de rechtspersonen en de fiscale perioden. Voor de meeste financiële overzichten is de kolomhiërarchie **Rechtspersoon** > **Fiscale kalender** > **Boekjaar** > **Kwartaal** > **Periode**.

Op dit moment ondersteunen de financiële overzichten niet de organisatiehiërarchieën waarmee u gegevens kunt samenvoegen.

## <a name="data-limitations"></a>Gegevensbeperkingen
De visuele elementen van het financiële overzicht hebben een limiet op het aantal rijen dat kan worden weergegeven. Op dit moment is de limiet ingesteld op 30.000. Als u deze limiet overschrijdt, krijgt het visuele element een waarschuwingssymbool om u te informeren over deze situatie.
 
![Gegevensbeperkingen](./media/data-limit.png)


Als het maximum wordt overschreden, zijn de totalen die worden weergegeven in het financiële overzicht, niet meer correct, omdat niet alle rijen in het visuele element zijn geladen.

### <a name="empty-rows"></a>Lege rijen
Power BI bevat geen optie om lege rijen te verbergen en weer te geven. Als een rij geen gegevens bevat, wordt de rij niet weergegeven in het visuele element.

## <a name="what-is-coming-in-future-releases"></a>Wat is er nieuw in toekomstige releases?
De nieuwe werkruimten en financiële overzichten die gebruikmaken van Power BI, worden steeds verbeterd. Hier volgen enkele van de nieuwe functies die worden overwogen voor toekomstige versies:

 - De mogelijkheid om visuele elementen te kopiëren, bewerken, verwijderen en maken, zelfs de financiële overzichten                                                  
 - Extra standaardrapporten                                                                                                            
    - Ondersteuning voor extra subjournaalgegevens                                                                                            
 - Ondersteuning van een aangiftevaluta                                                                                                      
 - Aangepaste berekeningen voor rijen en kolommen toevoegen                                                                                          
 - De mogelijkheid de financiële overzichten naar Microsoft Excel te exporteren                                                                     
   - De indeling behouden van het financieel overzicht tijdens export.                                                                          
   - Gegevens analyseren in Excel met behulp van een draaitabel die gebruikmaakt van de informatie in het visuele element.                                              
 - Ondersteuning voor landinstelling                                                                                                                        
 - De mogelijkheid rapportagehiërarchieën te definiëren zodat u hoofdrekeninghiërarchieën of een organisatiehiërarchie kunt definiëren die kan worden gebruikt in financiële overzichten voor ontwerpen, filtering en beveiliging.                                                                    
 - Ondersteuning voor afdrukken

De nieuwe functies worden meegedeeld via de website van de routekaart zodra werk wordt gestart: https://roadmap.dynamics.com/.

## <a name="additional-resources-for-power-bi"></a>Extra resources voor Power BI

De informatie in de volgende bronnen is niet vereist is om de ingesloten rapporten voor de werkruimte **CFO overzicht** of **Financial Insights** in te schakelen in een productieomgeving. In plaats daarvan zijn ze handig voor ontwikkelaarsmachines en als u uw eigen rapporten Power BI-rapporten wilt insluiten in Finance and Operations.

https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/

https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces


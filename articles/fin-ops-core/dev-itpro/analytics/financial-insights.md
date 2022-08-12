---
title: Financiële analyse
description: Financiële analyse gebruikt Microsoft Power BI om financiële KPI's, grafieken en financiële overzichten samen te voegen.
author: kweekley
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 21d7d045c812c54d6776394ad9a0b025b55df8e1
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109107"
---
# <a name="financial-analysis"></a>Financiële analyse

[!include [banner](../includes/banner.md)]

**Financiële analyse** gebruikt Microsoft Power BI om financiële KPI's, grafieken en financiële overzichten samen te voegen. Power BI is ingesloten in de toepassing. De focus van **Financiële analyse** is analytische rapportage. Persoonlijkheden binnen een organisatie kunnen weergeven, onderzoeken en reageren. 

**Financiële analyse** combineert gegevens uit het grootboek en subjournalen om een completer beeld te geven van de financiële toestand van een organisatie.

> [!NOTE]
> Dit document gebruikt de volgende Power BI-terminologie:
> 
> - **Rapport**: een enkel .pbix-bestand waarin alle visuele elementen op alle tabbladen worden opgeslagen.
> - **Pagina**: een tabblad in een enkel .pbix-bestand. Elke pagina kan een of meer visuele elementen bevatten.
> - **Zichtbaar**: één bron van gegevens, zoals een kaart, KPI, diagram, grafiek, matrix of financieel overzicht. Een pagina met een financieel overzicht als visueel element kan geen andere visuele elementen hebben vanwege de grootte van de gegevens waarover wordt gerapporteerd.

De werkruimte **Financiële analyse** is gericht op het bekijken en filteren van de gegevens in bestaande rapporten. Het is mogelijk om nieuwe visuele elementen toe te voegen aan de werkruimte **Financiële analyse**. De werkruimte **Financiële analyse** is beschikbaar voor het huidige bedrijf en alle bedrijven om gegevens voor alle rechtspersonen weer te geven, ongeacht de rechtspersonen tot wie de rol toegang heeft.

- [Power BI-visualisaties op uw dashboard toevoegen of bewerken](/powerapps/user/add-powerbi-dashboards)

## <a name="dynamics-365-finance-setup"></a>Dynamics 365 Finance instellen
**Grootboek**

Het hoofdrekeningtype en de hoofdrekeningcategorieën worden gebruikt om de juiste standaardhoofdrekeningen in te vullen op het financieel overzicht **Balans** en de verschillende **winst- en verliesrekeningen** in **Financiële analyse**.

Op de pagina **Hoofdrekeningen** moet u uw hoofdrekening definiëren zodat er een van de volgende typen aan wordt toegewezen:

- Omzet
- Expense
- Activa
- Verplichtingen
- Eigen vermogen

Wijs geen ander hoofdrekeningtype, zoals **Balans** of **Winst en verlies**, aan uw hoofdrekeningen toe. Rapportage kan niet het type hoofdrekening bepalen wanneer andere typen hoofdrekeningen worden toegewezen, omdat deze niet gedetailleerd genoeg zijn. Het type hoofdrekening moet worden bepaald om verplichtingen en opbrengst weer te geven als positieve bedragen in financiële rapporten.

Om op de financiële overzichten te worden weergegeven en te worden opgenomen in diverse andere visuele elementen, zoals KPI's, moet aan elke hoofdrekening een hoofdrekeningcategorie worden toegewezen. De hoofdrekeningcategorieën zijn verbeterd, zodat ze een weergavevolgorde bevatten. De weergavevolgorde wordt specifiek gebruikt in financiële overzichten in **Financiële analyse**. Nadat u een hoofdrekeningcategorie hebt bewerkt of toegevoegd, kunt u de waarde van de **weergavevolgorde** wijzigen om de volgorde te definiëren waarin hoofdrekeningcategorieën kunnen worden weergegeven in een financieel overzicht. Als u de weergavevolgorde voor veel hoofdrekeningcategorieën moet wijzigen, kunt u de functie Openen in Excel gebruiken om snel te bewerken en de wijzigingen weer te publiceren in de toepassing.

## <a name="entity-store"></a>Entiteitopslag
De gegevens voor **Financiële analyse** worden gehaald uit de entiteitopslag (**Systeembeheer** \> **Instellen** \> **Entiteitopslag**). Als u de werkruimte **CFO-overzicht** of **Financiële analyse** opent en het volgende waarschuwingsbericht wordt weergegeven in de visuele elementen, moet u de entiteiten bijwerken.

![Waarschuwing.](./media/Cantdisplay.png)

U moet de volgende entiteiten bijwerken om gegevens te zien in de werkruimte **Financiële analyse**:

- Transactiegegevens financiële rapportage versie 3 
- Crediteringen en aanmaningen V2
- LedgerCovLiquidityMeasurement
- Inkoop-cube
- Verkoop-cube

U kunt een terugkerende batch definiëren om de gegevens in de entiteiten regelmatig bij te werken. Omdat elke entiteit volledig opnieuw wordt gemaakt tijdens een update, selecteert u de tijd en de frequentie van entiteitupdates zorgvuldig. De primaire entiteit die wordt gebruikt voor financiële overzichten, is de FinancialReportingTransactionData-entiteit. U kunt daarom die entiteit vaker bijwerken.

## <a name="security"></a>Beveiliging
De gegevens in ingesloten Power BI-rapporten kunnen momenteel niet worden beperkt tot de rechtspersonen waartoe de gebruiker toegang heeft. Daarom worden de ingesloten Power BI-rapporten beheerd via functies in de instelling van de beveiliging. De functies die zijn gedefinieerd, verlenen toegang tot gegevens voor alle rechtspersonen of alleen het actieve bedrijf. In de volgende tabel ziet u de functies die beschikbaar zijn en de rollen waaraan ze zijn toegewezen. De functies kunnen worden verwijderd of toegewezen aan andere rollen, op basis van de behoeften van uw organisatie.

| Functie                                    | Rollen | Beschrijving |
|-----------------------------------------|-------|------------|
| Financiële analyse voor huidig bedrijf weergeven | <ul><li>Accountant</li><li>Accountingmanager</li><li>Accounting supervisor</li><li>Accountant</li><li>Budgetbeheerder</li><li>President-directeur</li><li>Hoofdmedewerker financiën</li><li>Financieel controller</li></ul> | Deze functie geeft toegang tot Financiële analyse. Standaard wordt het actieve bedrijf gebruikt als filter. U kunt geen andere rechtspersonen toevoegen. |
| Financiële analyse voor hele bedrijf weergeven   | In Microsoft Dynamics 365 Finance, Enterprise edition 7.3 is deze functie niet toegewezen aan een rol. In de volgende versie wordt deze functie toegewezen aan de rol van CFO. | Deze functie biedt toegang tot de menuoptie voor de werkruimte CFO-overzicht. Standaard wordt het actieve bedrijf gebruikt als filter. U kunt echter alle rechtspersonen toevoegen, ongeacht of de gebruiker toegang tot de andere rechtspersonen heeft. |


## <a name="financial-reporting-vs-financial-analysis"></a>Financiële rapportage versus Financiële analyse
Hoewel **Financiële analyse** financiële overzichten bevat, is het geen vervanging voor Financiële rapportage in de toepassing. De standaard financiële overzichten in **Financiële analyse** zijn beperkt in bereik en bevatten niet alle soorten financiële overzichten. Financiële rapportage is nog steeds het primaire hulpmiddel voor het ontwerpen, maken en genereren van wettelijke financiële overzichten.

Op basis van het volgende vergelijkingsdiagram kunt u onderscheid maken tussen de twee opties:


| Functie                                                   | Financial Reporting                                               | Financiële analyse |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Standaardrapporten bewerken**                                 | Ja                                                               | Nee |
| **Nieuwe rapporten maken**                                   | Ja                                                               | Nee |
| **Druk rapporten af**                                        | Ja                                                               | Nee |
| **Exporteren naar Excel**                                      | Ja                                                               | Beperkt Exporteert onbewerkte gegevens naar Excel, niet opgemaakt rapport |
| **Ondersteuning van rapporthiërarchie/organisatiehiërarchie**   | Ja                                                               | Nee |
| **Rapport van gegevens in subadministratie**                             | Ja Beperkt tot alleen leverancier, klant                              | Ja Leverancier, klant, leverancier-/klantgroepen, leverancier-/klantadressen, enz. |
| **Aangiftevaluta**                                   | Ja Valuta voor boekhouding en omzetten naar aangiftevaluta       | Nee Alleen valuta voor boekhouding |
| **Beveiliging**                                             | Ja Voldoet aan Finance-beveiliging van rapportstructuur | Rapporten met beperkte weergave voor alle bedrijven (ongeacht de beveiliging van apps voor financiën en bedrijfsactiviteiten) of alleen actief bedrijf |
| **Ondersteuning voor verschillende rekeningschema's en fiscale jaren** | Ja                                                               | Nee |
| **Rapport van externe gegevens**                              | Nee                                                                | Nee |
| **Consolidaties ondersteunen**                               | Ja                                                               | Beperkt Kan rapporteren over meerdere bedrijven, maar alleen valuta voor boekhouding gebruiken |

De volgende financiële overzichten zijn beschikbaar:

- Proefbalans
- Balans
- Winst- en verliesrekening per regio
- Winst- en verliesrekening - werkelijk versus budget
- Winst- en verliesrekening met afwijkingen
- Trendinkomensoverzicht van 12 maanden
- Onkosten driejarige trend
- Onkosten per leverancier
- Verkopen per klant

## <a name="edit-visuals"></a>Visuele elementen bewerken
In eerdere versies van **Financiële analyse** kon geen van de visuele elementen worden bewerkt. In toekomstige versies kunnen gebruikers met de juiste beveiliging nieuwe visuele elementen maken, bestaande visuele elementen kopiëren en visuele elementen bewerken. Hoewel de .pbix-bestanden die de rapporten bevatten als resources beschikbaar zijn, wordt niet aanbevolen dat u de standaardrapporten bewerkt. Er worden aanvullende wijzigingen aangebracht in de visuele elementen gegevensmodel, standaardrapporten en aangepaste financiële overzichten die worden gebruikt om de financiële overzichten te maken. Dus als u wilt profiteren van nieuwe functies en wijzigingen in het gegevensmodel in de volgende versie, moet u eventuele wijzigingen die u hebt aangebracht in de standaardrapporten via Microsoft Power BI Desktop opnieuw aanbrengen.

## <a name="filtering"></a>Filteren
Gebruikers kunnen het rapport filteren met behulp van het deelvenster **Filter** aan de linkerzijde. Dit venster is het hetzelfde venster dat beschikbaar is via Power BI Desktop. Er zijn verschillende niveaus van filteren, waarvan sommige mogelijk niet beschikbaar zijn, afhankelijk van wat u hebt geselecteerd op een pagina (tabblad) en of u de detailanalysemogelijkheden gebruikt:

- **Filters op rapportniveau**: deze filters worden toegepast op alle visuele elementen op alle pagina's (tabbladen).
- **Filters op paginaniveau**: deze filters worden toegepast op alle visuele elementen op het actieve tabblad. Deze filters worden toegepast boven op filters op rapportniveau.
- **Filters op het niveau van visuele elementen**: deze filters worden alleen toegepast op het geselecteerde visuele element. Deze filters worden toegepast boven op de filters op paginaniveau.
- **Detailanalysefilter** : dit filter filtert van een visueel 'bron'-element dat op het huidige visuele element wordt toegepast wanneer u vanuit het visuele bronelement inzoomt op het huidige visuele element.

![Filteropties.](./media/filter.png)

Als u een specifieke filterwaarde wilt verwijderen, selecteert u het gumsymbool ernaast. Verwijder geen filter door de X te selecteren. Als u de X selecteert, wordt het veld waarop u filtert verwijderd als filteroptie. Als u per ongeluk een veld uit het filter verwijdert, sluit u de werkruimte en opent u deze opnieuw. De standaardinstellingen voor het filter worden opnieuw toegepast.

Wanneer u werkruimten voor het eerst opent wordt standaard de actieve rechtspersoon gebruikt als filter op rapportniveau. Afhankelijk van hun beveiliging kunnen gebruikers mogelijk andere rechtspersonen toevoegen of de standaardrechtspersoon wijzigen die is geselecteerd in het filter.

Het filter **fiscale kalender** is vereist, zodat de juiste kalender wordt gebruikt voor het visuele element. Het filter op rapportniveau is standaard ingesteld op de fiscale kalender van de actieve rechtspersoon. Als u het filter wijzigt in een fiscale kalender met een andere begin- of einddatum, worden de beginsaldi niet opgenomen. Daarom geven uw financiële overzichten van **Balans** niet de juiste saldi weer. Als u een extra fiscale kalender in het filter selecteert, hebt u een aanvullende reeks kolommen. Elke aanvullende reeks kolommen bevat de bedragen voor een andere fiscale kalender.

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

- Leverancier
- Leveranciersgroep
- Klant
- Klantgroep
- Land/regio
- Provincie
- Plaats

> [!IMPORTANT] 
> Als u transacties voor meerdere leveranciers of klanten in één boekstuk samenvat met behulp van de financiële journalen, zijn de gegevens onjuist. Het rapportageproces kan niet bepalen welke leverancier of klant is gekoppeld aan een bepaalde grootboekrekening in een journaalpost, omdat deze informatie nergens wordt onderhouden. Daarom raden we niet aan dat u meerdere leveranciers, klanten, vaste activa of projecten in één boekstuk invoert.

## <a name="drill-on-data"></a>Inzoomen op gegevens

Verschillende niveaus van inzoomen zijn beschikbaar via Power BI. Elk niveau heeft een andere naam en een andere functie. U kunt ook inzoomen op rijen en kolommen. In dit gedeelte worden de verschillende opties besproken met behulp van het financieel overzicht **Proefbalans** als een voorbeeld en het laat zien hoe u kunt inzoomen op de rijen. Dezelfde functionaliteit bestaat voor kolommen. U hoeft alleen de instelling **Inzoomen op** te wijzigen.

In het volgende voorbeeld is de **proefbalans**-instructie samengevouwen tot het hoogste niveau van de rijhiërarchie, het hoofdrekeningtype.

![Overzicht van proefbalans.](./media/trial-balance.png)

Als u het volgende niveau van de hiërarchie, de hoofdrekeningcategorieën, wilt weergeven, kunt u het veld **Inzoomen op** instellen op **Rijen** en vervolgens de knop **Uitvouwen** selecteren (de derde knop na het veld Inzoomen op). U ziet nu alle hoofdrekeningcategorieën uitgevouwen. Op dit moment kunt u met Power BI niet één rij of kolom uitvouwen, maar nog steeds alle andere rijen of kolommen zien.

![Inzoomen op rijen in proefbalans.](./media/trial-balance2.png)

Als u wilt uitvouwen naar de hoofdrekeningen voor alle rijen, kunt u weer de knop **Uitvouwen** gebruiken. Echter, als u wilt inzoomen naar de hoofdrekeningen voor slechts één rij, selecteert u eerst de knop **Inzoomen** (de enkele pijl-omlaag aan de rechterkant van het venster) en selecteert u vervolgens de rij waarop u wilt inzoomen. In de volgende afbeelding ziet u het resultaat wanneer de rij **Verkoop** is geselecteerd nadat de knop **Inzoomen** is geselecteerd.

![Knop Uitvouwen voor proefbalans.](./media/trial-balance3.png)

Nadat u op één rij inzoomt, zijn er meerdere klikken nodig om terug te keren naar de volledige proefbalans. De knop **Uitzoomen** (de eerste knop na **inzoomen** op veld) zoomt alleen uit in de context van de categorie **Verkoop**, zoals in de volgende afbeelding wordt weergegeven.

![Knop Uitzoomen voor proefbalans.](./media/trial-balance4.png)

U kunt de knop **Uitzoomen** blijven gebruiken om terug te keren naar het hoogste niveau van samenvatting voor de rijen.

Power BI heeft ook een knop waarmee u naar het volgende niveau in de hiërarchie gaat (de tweede knop na het veld **Inzoomen op**). Het effect van deze knop verschilt van het effect van de knop **Uitvouwen** (de derde knop na het veld **Inzoomen op**), die wordt gebruikt om de hiërarchie uit te vouwen. Wanneer u de hiërarchie uitvouwt, wordt de hiërarchie onderhouden in het rapport. Zoals u bijvoorbeeld eerder gezien hebt, als u uitvouwt op het hoofdrekeningtype, ziet u nog steeds het hoofdrekeningtype in het rapport. Echter wanneer u naar een hoger niveau in de hiërarchie gaat, toont het rapport niet langer de bovenliggende in de hiërarchie, zoals in de volgende afbeelding wordt weergegeven.

![Knop Inzoomen voor proefbalans.](./media/trial-balance5.png)

Als u de transactiedetails achter de samengevatte saldi wilt zien, kunt u enkele bedragen selecteren om terug te zoomen naar apps voor financiën en bedrijfsactiviteiten.

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

De financiële standaardoverzichten gebruiken twee hiërarchieën om in te zoomen en uit te vouwen op de gegevens. Eén hiërarchie is voor de rijen en de andere hiërarchie is voor de kolommen. Beide hiërarchieën zijn vooraf ingesteld in het ontwerp van het financiële overzicht. Voor de meeste financiële overzichten is de rijhiërarchie **Hoofdrekeningtype** \> **Hoofdrekeningcategorieën** \> **Hoofdrekening**. Sommige rapporten hebben echter extra velden, zoals Land en Regio. De extra knooppunten van de hiërarchie zijn gebaseerd op subjournaalgegevens voor elke transactie.

Voor de kolommen is de hiërarchie gericht op de rechtspersonen en de fiscale perioden. Voor de meeste financiële overzichten is de kolomhiërarchie **Rechtspersoon** \> **Fiscale kalender** \> **Boekjaar** \> **Kwartaal** \> **Periode**.

Op dit moment ondersteunen de financiële overzichten niet de organisatiehiërarchieën waarmee u gegevens kunt samenvoegen.

## <a name="data-limitations"></a>Gegevensbeperkingen
De visuele elementen van het financiële overzicht hebben een limiet op het aantal rijen dat kan worden weergegeven. Op dit moment is de limiet ingesteld op 30.000. Als u deze limiet overschrijdt, krijgt het visuele element een waarschuwingssymbool om u te informeren over deze situatie.

![Gegevensbeperkingen.](./media/data-limit.png)

Als het maximum wordt overschreden, zijn de totalen die worden weergegeven in het financiële overzicht, niet meer correct, omdat niet alle rijen in het visuele element zijn geladen.

### <a name="empty-rows"></a>Lege rijen
Power BI bevat geen optie om lege rijen te verbergen en weer te geven. Als een rij geen gegevens bevat, wordt de rij niet weergegeven in het visuele element.


## <a name="additional-resources-for-power-bi"></a>Aanvullende bronnen voor Power BI

De informatie in de volgende bronnen is niet vereist is om de ingesloten rapporten voor de werkruimte **Financiële analyse** in te schakelen in een productieomgeving. In plaats daarvan zijn ze handig voor ontwikkelaarsmachines en als u uw eigen Power BI-rapporten wilt insluiten in Finance.

- [Toegang krijgen tot analytische werkruimten en rapporten voor een omgeving met één computer](/archive/blogs/dynamicsaxbi/accessing-analytical-workspaces-on-1box-environment)

- [Analyses aan werkgebieden toevoegen met Power BI Embedded](/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


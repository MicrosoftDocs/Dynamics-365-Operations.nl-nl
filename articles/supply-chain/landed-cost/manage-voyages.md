---
title: Reizen beheren
description: In dit onderwerp wordt beschreven hoe u met reizen werkt. Een reis vertegenwoordigt doorgaans een vaartuig. Afhankelijk van uw werkwijzen en procedures kan het echter ook een leverancier, een inkooporder of een ander artikel vertegenwoordigen dat betekenis heeft voor uw organisatie.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 50b6f306da1d32b1fd98da68bd997de1f1c23ffb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570941"
---
# <a name="manage-voyages"></a>Reizen beheren

[!include [banner](../../includes/banner.md)]

Een reis vertegenwoordigt doorgaans een vaartuig. Afhankelijk van uw werkwijzen en procedures kan het echter ook een leverancier, een inkooporder of een ander artikel vertegenwoordigen dat betekenis heeft voor uw organisatie.

De pagina **Alle reizen** biedt details over reizen, levering en informatie over kostprijsberekening en informatie over artikelen, inkooporders en overboekingsorders. U opent de pagina **Alle reizen** door naar **Francoprijzen \> Reizen \> Alle reizen** te gaan. Op deze pagina wordt een lijst met alle huidige reizen weergegeven. U kunt de knoppen in het actievenster gebruiken om reizen te maken, te verwijderen en met reizen te werken. Selecteer een reis in de lijst om de details van de reis weer te geven.

> [!NOTE]
> containers en folio's zijn aan een reis gekoppeld. Inkoopregels zijn aan een container gekoppeld. Als containers en folio's zijn uitgeschakeld, kunnen ze ook rechtstreeks aan een reis worden gekoppeld. Bovendien worden kosten die hier worden ingevoerd, verdeeld over alle gekoppelde inkoopregels.

## <a name="action-pane"></a>Actievenster

Het actievenster van de pagina **Reizen** bevat knoppen die u kunt gebruiken om met een geselecteerde reis te werken. Met elke knop voert u één actie uit. Het actievenster bevat ook tabbladen die elk op hun beurt een reeks verwante knoppen bieden. Behalve daar waar aangegeven, zijn alle knoppen en tabbladen beschikbaar, zowel in de lijstweergave van de pagina **Alle reizen** als in de gedetailleerde weergave voor één geselecteerde reis.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Knoppen die rechtstreeks in het actievenster worden weergegeven

In de volgende tabel wordt de knoppen beschreven die rechtstreeks in het actievenster beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Nieuw | Een reis maken. <!-- KFM: Link to scenario --> |
| Delete | De huidige reis verwijderen. Alleen reizen met de status *Bevestigd* kunnen worden verwijderd. Wanneer een reis de haven verlaat en goederen in transit verwerkt, kan de reis niet meer worden verwijderd. |
| Reiseditor | Hiermee opent u de pagina **Reiseditor**, waar u inkoopregels voor de reis kunt toevoegen of verwijderen, nieuwe containers kunt maken en details van de reis zelf kunt wijzigen. |
| Reiskosten | Open de pagina **Reiskosten**, waar u reiskosten kunt bekijken en toevoegen aan alle goederen in de reis. Wanneer reiskosten handmatig aan de reis worden toegevoegd, worden ze automatisch toegevoegd aan de pagina **Vraag naar kostenposten** en verdeeld over elk artikel volgens de methode die is opgegeven op de pagina **Reiskosten**. |

### <a name="buttons-on-the-voyage-tab"></a>Knoppen op het tabblad Reis

In de volgende tabel worden de knoppen beschreven die op het tabblad **Reis** van het actievenster beschikbaar zijn. Dit tabblad is alleen beschikbaar wanneer u in de lijstweergave van de pagina **Alle reizen** werkt.

| Knop | Beschrijving |
|---|---|
| container | Hiermee opent u een pagina waarop alle containers worden weergegeven die aan de geselecteerde reis zijn gekoppeld. Dit kan één container of een groot aantal containers zijn. |
| Folio | Hiermee opent u een pagina waarop alle folio's worden weergegeven die aan de geselecteerde reis zijn gekoppeld. Dit kan één folio of een groot aantal folio's zijn. |

### <a name="buttons-on-the-manage-tab"></a>Knoppen op het tabblad Beheren

In de volgende tabel worden de acties beschreven die op het tabblad **Beheren** van het actievenster beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Documenten ontvangen | Werk de reis bij zodat de optie **Documenten ontvangen** wordt ingesteld op *Ja*. Met deze knop kunt u het artikel en/of de inkoopregel vergrendelen zodat deze niet verder kan worden bijgewerkt. |
| In transit | Werk het veld **Reisstatus** bij naar de status in transit die is ingesteld op de pagina **[Parameters voor Francoprijzen](landed-cost-parameters.md)**. Er is geen verdere logica voor dit proces. Een reis kan ook automatisch worden bijgewerkt naar de status in transit op basis van de instellingen in het [Traceringsbeheercentrum](delivery-information-setup.md).
| Gereed voor kostprijsberekening | Werk het veld **Reisstatus** bij naar de status Gereed voor kostprijsberekening die is ingesteld op de pagina **[Parameters voor francoprijzen](landed-cost-parameters.md)**. Er kan een kostprijs worden berekend wanneer alle facturen zijn verwerkt (zowel voorraadfacturen als reiskostenfacturen) en de goederen zijn ontvangen. Als de geschatte kosten die aan een reis zijn gekoppeld, niet zijn berekend, treedt er een fout op wanneer u probeert de kostprijsberekening van een reis te verwerken. |
| Kostprijs berekend | Alle onregelmatigheden in de kostprijsberekening opschonen nadat er een factuur bestaat voor alle inkooporders en reiskosten. Wanneer u deze knop selecteert, wordt het dialoogvenster **Reisupdate - kostprijs berekend** weergegeven. Hier kunt u selecteren of u wilt boeken op de standaard financiële datum of een boekingsdatum wilt opgeven en vervolgens de actie uitvoeren. U kunt de actie zo vaak uitvoeren als u wilt. U kunt ook het dialoogvenster **Reisupdate - kostprijs berekend** gebruiken om een planning in te stellen waarmee de actie als periodieke taak (batchtaak) wordt uitgevoerd. We raden u aan om de actie regelmatig uit te voeren door de actie in te stellen als batchtaak. |
| Ontvangstlijst boeken | Boek een ontvangstlijst voor alle inkooporderregels in de reis. Als er reizen naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van ontvangstlijsten geopend voor elk bedrijf die moet worden verwerkt in elke rechtspersoon. |
| Productontvangstbon boeken | Boek een productontvangstbon voor alle inkooporderregels in de reis. Het proces van de productontvangstbon voor de inkooporderregels die aan een reis zijn gekoppeld, wordt alleen gebruikt als de goederen **niet** worden verwerkt via de verwerking van goederen in transit. Als de goederen worden verwerkt via de verwerking van goederen in transit, ontvangt u een foutmelding wanneer u probeert de productontvangstbon voor een inkooporderregel te boeken. Als er reizen naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van afleveringsbewijzen geopend voor elk bedrijf. |
| Factuur boeken | Boek een factuur voor alle inkooporderregels in de reis. Als de goederen van de reis via de verwerking van goederen in transit worden verwerkt, worden de inkooporderregels gefactureerd voordat het ontvangstproces is uitgevoerd. Wanneer de oorspronkelijke inkooporder wordt gefactureerd, worden de orders voor goederen in transit gemaakt die aan de oorspronkelijke inkooporderregels zijn gekoppeld. Die orders kunnen vervolgens door het magazijn worden ontvangen. Als er zendingen naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van facturen geopend voor elk bedrijf. |
| Verzenden overboekingsorders | Boek een overboekingsorderreis voor alle overboekingsorderregels in de reis. Wanneer deze knop is geselecteerd, zijn er alleen overboekingsorders beschikbaar voor bijwerken. |
| overboekingsorder ontvangen | Boek een overboekingsorderontvangst voor alle overboekingsorderregels in de reis. |
| Goederen in transit ontvangen | Ontvang alle orderregels die in transit zijn in de reis. Deze knop is een van de drie opties die beschikbaar zijn voor het ontvangen van goederen in transit op een reis. (De andere twee opties zijn de knop **Ontvangstjournaal maken** die verderop in deze tabel wordt beschreven, en de mobiele app Magazijnbeheer.) Deze optie is de eenvoudigste optie waarmee de goederen in transit in het transitmagazijn en in het definitieve bestemmingsmagazijn worden verwerkt. Als u meer controle wilt hebben over het proces, gebruikt u het ontvangstjournaal of een mobiel apparaat om de ontvangst van goederen te verwerken. |
| Automatisch kosten zoeken | Zoek relevante reiskosten. Als deze kosten al zijn gevonden of bijgewerkt, ontvangt u het volgende bericht: 'Er bestaan niet-gefactureerde kostenregels. Wilt u deze overschrijven?' Eventuele kosten die op het moment van aanmaken niet aan de reis zijn gekoppeld, worden gevonden. Reiskosten die aan een reis zijn gekoppeld en die zijn gefactureerd, niet worden overschreven. |
| Ontvangstjournaal maken | <p>Open het dialoogvenster **Ontvangstjournaal maken**, waarin u een ontvangstjournaal kunt maken die een locatie aangeeft. Het dialoogvenster biedt de volgende opties:</p><ul><li>**Maken op basis van goederen in transit** of **Maken op basis van overboekingsorder**: Het label voor deze optie verandert, afhankelijk van of u het proces voor goederen in transit gebruikt. Stel de optie in op *Ja* om een ontvangstjournaalpagina te openen waarop u een standaardaankomstjournaal kunt verwerken voor de goederen in transit die aan de reis zijn gekoppeld. Als het artikel al in het definitieve bestemmingsmagazijn is ontvangen, wordt het niet toegevoegd aan de ontvangstjournaalregels.</li><li>**Hoeveelheid initialiseren**: Stel deze optie in op *Ja* om de hoeveelheid die wordt ontvangen te initialiseren op basis van de hoeveelheid goederen die op de reisregel is opgegeven. Als de reisregel gedeeltelijk is ontvangen, is deze hoeveelheid de resterende hoeveelheid. U kunt deze optie het beste op *Ja* instellen.</li><li>**Maken op basis orderregels**: Stel deze optie in op *Ja* om de waarde uit de orderregels op te nemen.</li></ul><p>Deze knop is een van de drie opties die beschikbaar zijn voor het ontvangen van goederen in een reis. (De andere opties zijn de knop **Goederen in transit ontvangen** die eerder in deze tabel is beschreven en de mobiele app Magazijnbeheer.)</p> |
| Kosten toerekenen | U kunt kosten toerekenen voor een kostentype waarvoor een grootboekrekening is opgegeven voor de afschrijving. Deze knop wordt meestal gebruikt wanneer de voorraad in transit is of wanneer goederen zijn ontvangen en gefactureerd. |
| Cumulatieve kosten | Kosten verplaatsen van het niveau van de container naar het reisniveau. U kunt deze knop gebruiken in een scenario met gedeelde services/verzendingen, waarbij meerdere entiteiten een container of kartonnen ruimte delen. De reis heeft bijvoorbeeld een container van 12 meter en een container van 6 meter en de verdeling wordt op volume uitgevoerd. In dit geval kunnen de goederen/entiteiten die de ruimte in de container van 6 meter delen of gebruiken, worden aangepast. Om de kosten eerlijk te verdelen, willen sommige organisaties de kosten mogelijk overbrengen naar de reis en ze verdelen op basis van de verdelingsmethode van het reisniveau. |
| Trajectsjabloon wijzigen | Open een dialoogvenster waarin u het trajectsjabloon kunt wijzigen. Nadat u de sjabloon hebt gewijzigd, worden de reiskosten verwijderd. U moet dus mogelijk **Automatische kosten zoeken** selecteren (zie de beschrijving eerder in deze tabel) of handmatig kosten opnieuw toevoegen. |

### <a name="buttons-on-the-general-tab"></a>Knoppen op het tabblad Algemeen

In de volgende tabel worden de knoppen beschreven die op het tabblad **Algemeen** van het actievenster beschikbaar zijn.

| Knop | Beschrijving |
|---|---|
| Ontvangstlijst | Open een lijst met productontvangstbonnen voor alle inkooporderregels in de reis. Als er reizen naar meerdere bedrijven worden gebruikt, wordt er een nieuw dialoogvenster voor het boeken van ontvangstlijsten geopend voor elk bedrijf. Als er geen lijsten met productontvangstbonnen zijn verwerkt, is deze knop niet beschikbaar. |
| Ontvangst van producten | Open de record van de productontvangstbon voor de inkooporderregels die aan de reis zijn gekoppeld, als die record wordt gebruikt. Als er geen productontvangstbonnen zijn verwerkt, is deze knop niet beschikbaar. Het proces van de productontvangstbon wordt niet gebruikt als u de verwerking voor goederen in transit gebruikt. |
| Artikelontvangst | Open het artikelontvangstjournaal, als het is gebruikt. |
| Tracering | Open de pagina **Inkomende tracering**, waar u de verwachte aankomstdatum van goederen in een container en een reis kunt bijwerken en vervolgens verwachte leveringsdatums van inkooporderregels kunt bijwerken. |
| Vraag naar kostenposten | <p>Open de pagina **Vraag naar kostenposten** waarop alle kosten van een reis worden weergegeven.</p><p>Selecteer **Weergeven** in het actievenster om de weergave aan te passen. U kunt elk niveau weergeven plus het artikel en de kostentypecode.</p><p>Alleen kostentypecodes die rechtstreeks zijn gerelateerd aan voorraadtransacties, worden op de pagina **Vraag naar kostenposten** weergegeven. Als u deze kostentypecodes verwijdert, kunt u de pagina aanpassen door kosten te groeperen. Deze mogelijkheid kan handig zijn als u afmetingen en kleuren gebruikt.</p><p>Op de pagina **Vraag naar kostenposten** worden alleen kostentypecodes weergegeven waarbij het veld **Debet** is ingesteld op *Artikel*.</p> |
| Orders voor goederen in transit | Open de pagina **Orders voor goederen in transit**, waar alleen de records voor goederen in transit voor de geselecteerde reis worden weergegeven. |

## <a name="lines-view"></a>Regelweergave

Als u de weergave **Regels** wilt openen, opent u een reis en selecteert u vervolgens het tabblad **Regels** in de rechterbovenhoek van de reisheader.

### <a name="information-on-the-voyage-header-fasttab"></a>Informatie op het sneltabblad Reisheader

Het sneltabblad **Reisheader** in de weergave **Regels** van een reis bevat basisinformatie over de reis. Veel van de velden die op dit sneltabblad worden weergegeven, worden ook weergegeven in de weergave **Header**, zoals verderop in dit onderwerp wordt beschreven.

### <a name="information-on-the-voyage-lines-fasttab"></a>Informatie op het sneltabblad Reisregels

Het sneltabblad **Reisregels** in de weergave **Regels** van een reis is gerelateerd aan de reisdetails en informatie over kostprijsberekening die op het reisniveau van toepassing zijn. Hier kunt u de containers, folio's en artikelen bekijken die aan de reis zijn gekoppeld. Daarnaast worden ook de prijs en hoeveelheid van de artikelen van de reis weergegeven. U kunt alle containers of folio's weergeven die in de lijst worden vermeld door de desbetreffende koppeling te selecteren.

### <a name="information-on-the-line-details-fasttab"></a>Informatie op het sneltabblad Regeldetails

Het sneltabblad **Regeldetails** in de weergave **Regels** van een reis wordt meer informatie gegeven over de regel die op dat moment is geselecteerd op het sneltabblad **Reisregels**. Dit sneltabblad bevat details over de positie die elke regel in de container inneemt en de bijbehorende gedeclareerde hoeveelheid.

## <a name="header-view"></a>Weergave headers

Als u de weergave **Header** wilt openen, opent u een reis en selecteert u vervolgens het tabblad **Header** in de rechterbovenhoek van de reisheader.

### <a name="settings-on-the-general-fasttab"></a>Instellingen op het sneltabblad Algemeen

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Algemeen** van de weergave **Header** van een reis.

| Veld | Beschrijving |
|---|---|
| Reis | Voer de reis of het vluchtnummer in. |
| Boekingsverwijzing | Als uw expediteur of verzendcentrum een referentienummer verstrekt om de reis te identificeren (dat wil zeggen de interne verwijzing van de expediteur of het verzendcentrum), voert u dit nummer hier in. |
| Vaartuig | Voer een vaartuig in of selecteer een vaartuig. Als het vaartuig niet als waarde wordt vermeld, kunt u de vaartuig-id als vrije tekst invoeren. In dat geval wordt de hoofdtabel niet bijgewerkt, zodat de vaartuig-id later in dit veld kan worden geselecteerd. |
| Externe reis-id | Voer de openbaar beschikbare id voor de reis in (zoals het vluchtnummer). |
| Hoofdluchtvrachtbrief/Vrachtbrief | Voer de hoofdluchtvrachtbrief- of vrachtbriefnummer in. U kunt deze waarde opgeven wanneer u goederen per vliegtuig wilt verzenden. |
| Interne (lucht)vrachtbrief | Voer de luchtvrachtbrief of vrachtbrief voor de container in. |
| Verhuur | Schakel dit selectievakje in om aan te geven dat de container een huurcontainer is die moet worden geretourneerd. |
| Beschrijving | Voer een beschrijving van de reis in om de reis gemakkelijker te kunnen herkennen. |
| Reisstatus | De status van de reis. De waarden zijn *Gemaakt*, *In transit*, *Documenten ontvangen* en *Kostprijs berekend*. Dit veld wordt niet berekend op basis van logica. Het veld wordt alleen bijgewerkt via de boekingsactie. De waarde *Kostprijs berekend* geeft aan dat er een factuur voor de voorraad en alle kosten van de reis zijn ontvangen. Een reis kan de status *Kostprijs berekend* niet krijgen, tenzij er een factuur is ontvangen. |
| Status inkooporder | De hoogste status die is bereikt van alle inkooporders die aan de reis zijn gekoppeld. |
| Documenten ontvangen | Een waarde die aangeeft of uw bedrijf alle documenten heeft ontvangen die aan de reis zijn gekoppeld. Als u de waarde wilt wijzigen, selecteert u **Documenten ontvangen** in de groep **Reis bijwerken** op het tabblad **Beheren** van het actievenster. |
| Expeditiebedrijf | Selecteer het expeditiebedrijf voor deze reis. U kunt dit veld gebruiken om de automatische kosten te bepalen. |
| Naam | De naam van het bedrijf dat u hebt geselecteerd in het veld **Expeditiebedrijf**. |
| Afmeting | Met dit veld kunt u een meting opgeven bij automatische kosten. Metingen worden vaak gebruikt door organisaties die niet het individuele volume of gewicht van de goederen weten, maar die een nauwkeurigere verdeling vereisen dan met de opties Bedrag en Hoeveelheid mogelijk is. De expediteur verstrekt het gewicht of de kubieke meting en u kunt deze instellen op het niveau van een artikel of de inkooporder. Dit kan automatisch worden bijgewerkt als de parameter is geselecteerd of handmatig wordt ingevoerd. |
| Maateenheid | De maateenheid die van toepassing is op de waarde in het veld **Meting**. |
| Aantal pallets | Geef het aantal pallets op de reisregel op. Dit veld wordt automatisch bijgewerkt als de optie **Automatisch aantal kartonnen dozen bijwerken** is ingesteld op *Ja* op het tabblad **Algemeen** van de pagina **Parameters voor francoprijzen**. |

### <a name="settings-on-the-delivery-fasttab"></a>Instellingen op het sneltabblad Levering

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Levering** van de weergave **Header** van een reis.

| Veld | Beschrijving |
|---|---|
| Aanmaakdatum en -tijd | De datum en tijd waarop de reisrecord is gemaakt. |
| Datum af-fabriek | Met de datum in dit veld wordt de vroegste datum af fabriek geselecteerd van de inkooporders die aan de reis zijn gekoppeld. De datum af fabriek is beschikbaar in de header van de inkooporder en wordt bijgewerkt met de functie voor traceringsbeheer. |
| Verzenddatum | De geschatte datum wanneer het vliegtuig of vaartuig het punt van vertrek verlaat. |
| Vertrekdatum | De vertrekdatum is meestal de datum waarop het vliegtuig of het vaartuig daadwerkelijk de overzeese haven verlaat. De verzenddatum en de vertrekdatum hoeven niet overeen te komen. Het veld **Vertrekdatum** dient alleen ter informatie. Dit veld wordt niet gebruikt als schatting voor de verwachte leveringsdatum. De functie voor traceringsbeheer wordt gebruikt om de verwachte leveringsdatum te schatten. U kunt dit veld zo instellen dat dit veld automatisch door de functie voor traceringsbeheer wordt ingevuld. |
| Datum in winkel | Met de datum in dit veld wordt de vroegste datum geselecteerd waarop de goederen van de inkooporders die aan de reis zijn gekoppeld, beschikbaar zijn voor verkoop. |
| Geraamde leveringsdatum | De geschatte leveringsdatum is meestal de datum waarop de goederen moeten binnenkomen in het magazijn. Dit veld is alleen bedoeld voor informatieve doeleinden. De datum wordt niet gebruikt voor de hoofdplanning voor goederen. De verwachte leveringsdatum op de inkooporderregel wordt gebruikt voor de hoofdplanning van goederen op een reis en wordt bijgewerkt met de functie voor traceringsbeheer. U kunt dit veld zo instellen dat het wordt ingevuld door de functie voor traceringsbeheer. |
| Werkelijke leverdatum | De vroegste leveringsdatum, op basis van de goederen die aan de reis zijn gekoppeld. |
| ETA in haven | Voer de datum in waarop u verwacht dat de reis in de haven aankomt op basis van de informatie die uw expediteur heeft verstrekt. |
| Oorspronkelijke documenten ontvangen | Voer de datum waarop de oorspronkelijke documenten zijn ontvangen. |
| Aanbevolen door makelaar | Voer de datum waarop de tussenpersoon is geadviseerd. |
| Oorspronkelijke vrachtbrief verzonden | Voer de datum in waarop de oorspronkelijke vrachtbrief is verzonden. |
| Goederen vrijgegeven | Voer de datum in waarop de goederen zijn vrijgegeven door de douane. |
| Klantafspraak | Voer de afspraakdatum van de klant in. Dit is de datum waarop u verwacht dat de klant de goederen in eigendom neemt. |
| Afgeleverd in magazijn | Voer de datum waarop de goederen zijn afgeleverd bij het magazijn. |
| Verificatiedatum | Voer de verificatiedatum in. |
| Leveringsinstructies | Voer de datum in waarop de leveringsinstructies zijn ontvangen. |
| Leveringsmethode | Dit veld bevat informatie over de methode die wordt gebruikt om de reis te leveren en de kostenselectie van automatische kosten die aan deze leveringsmethode zijn gekoppeld. |
| Vertrekhaven | De haven van waaruit de reis vertrekt. |
| Aankomsthaven | De haven waar de reis aankomt. De containers kunnen verschillende havens hebben, omdat het schip mogelijk meerdere havens aandoet. Door de 'naar'-haven op containerniveau te verifiëren, biedt u nauwkeurige details over de haven voor elke container op een reis. De automatische kosten die aan de vracht zijn gekoppeld, worden bepaald op basis van de combinatie van het type container, de 'naar'-haven en de 'van'-haven. |
| Lokale doorstuurder | Dit veld is alleen bedoeld voor informatieve doeleinden. De lokale expediteur kan worden geselecteerd in de leverancierstabel. |
| Datum van lokaal transport | De datum waarop het lokale transport is geboekt. Dit veld kan het magazijn helpen bij het plannen. |
| Tijd van lokaal transport | Het tijdvak waarop het lokale transport is geboekt. Dit veld kan het magazijn helpen bij het plannen. |
| Trajectsjabloon | De trajectsjabloon die voor de reis is opgegeven. De trajectsjabloon wordt gebruikt om de 'naar'-haven en de 'van'-haven van de container en de reis in te voeren. Deze waarden identificeren op hun beurt de automatische kosten die aan de reis zijn gekoppeld. |

### <a name="settings-on-the-other-fasttab"></a>Instellingen op het sneltabblad Overige

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Overige** van de weergave **Header** van een reis.

| Veld | Beschrijving |
|---|---|
| Opmerkingen | Voer eventuele aanvullende informatie in die betrekking heeft op de reis. |
| Waarderingsdatum | Selecteer de vroegste datum af fabriek voor de inkooporders die aan de reis zijn gekoppeld. |
| Reis in behandeling | U kunt dit veld gebruiken om aan te geven of uw zending of reis al onderweg is. Deze gegevens dienen alleen ter informatie.  |
| De naam van containers wijzigen | Voor reizen met meer dan één container is dit het aantal containers dat nog niet is ontvangen. |

## <a name="voyage-update-periodic-tasks"></a>Periodieke taken voor het bijwerken van reizen

De module **Francoprijzen** bevat verschillende periodieke taken voor reizen waarmee diverse aspecten van reizen bulksgewijs kunnen worden bijgewerkt. Als u deze periodieke taken wilt uitvoeren of plannen, gaat u naar **Francoprijzen \> \> Reizen bijwerken** en selecteert u een van de volgende taaktypen:

- **Documenten ontvangen**: Met deze taak kunt u **Documenten ontvangen** voor meerdere reizen tegelijk instellen op *Ja*. Gebruik de instellingen voor **Filteren** om de reeks reizen op te geven die u wilt bijwerken.
- **In transit**: Met deze taak kunt u het veld **Reisstatus** voor meerdere taken tegelijk instellen op de status in transit die is ingesteld op de pagina **[Parameters voor francoprijzen](landed-cost-parameters.md)**. Gebruik de instellingen voor **Filteren** om de reeks reizen op te geven die u wilt bijwerken.
- **Gereed voor kostprijsberekening**: Met deze taak kunt u het veld **Reisstatus** voor meerdere reizen tegelijk instellen op de status gereed voor kostprijsberekening die is ingesteld op de pagina **[Parameters voor francoprijzen](landed-cost-parameters.md)**. Meestal stelt u deze taak zo in dat deze volgens een regelmatige planning wordt uitgevoerd.
- **Kostprijs berekend**: Met deze taak kunt u het veld **Reisstatus** instellen op de status kostprijs berekend die op de pagina **[Francoprijzen](landed-cost-parameters.md)** voor meerdere taken tegelijk is ingesteld, mits voor deze reiszen de kostprijs is berekend, maar nog niet zijn bijgewerkt voor de reis. Meestal stelt u deze taak zo in dat deze volgens een regelmatige planning wordt uitgevoerd.

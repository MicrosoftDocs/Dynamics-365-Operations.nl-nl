---
title: Werkgebied voor kostenbeheer
description: Dit onderwerp bevat informatie over het werkgebied Kostenbeheer. Dit werkgebied is een centraal punt waar managers die verantwoordelijk zijn voor het beheer van een kostenobject of een reeks kostenobjecten in een dimensie of meerdere dimensies toegang kunnen krijgen tot rapporten.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 82eb312d534a43d48be2dabbf9f9ae3e32545bac
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841652"
---
# <a name="cost-control-overview"></a>Overzicht van kostenbeheer 

[!include [banner](../includes/banner.md)]

Het werkgebied **Kostenbeheer** is een centraal punt waar managers die verantwoordelijk zijn voor het beheer van een kostenobject of een reeks kostenobjecten in een dimensie of meerdere dimensies (bijvoorbeeld kostenplaatsen en productgroepen) toegang kunnen krijgen tot rapporten. De rapporten in het werkgebied worden volledig beheerd door kostenaccountants, zodat de indeling en gegevens die worden gebruikt voor rapportage in de gehele organisatie consistent zijn.

## <a name="cost-control-workspace-configuration"></a>Configuratie van werkgebied voor kostenbeheer

Kostenaccountants kunnen zoveel rapportconfiguraties definiëren als ze nodig hebben voor de gewenste gegevenssamenstelling of -indeling. Een rapportconfiguratie bestaat uit zes secties, waarvan elke sectie bijdraagt aan de selectie van de beoogde gegevenssamenstelling of de indeling.

Als u een werkgebied voor kostenbeheer wilt configureren, klikt u op **Kostprijsboekhouding** \> **Instellen** \> **Configuratie van werkgebied voor kostenbeheer**.

### <a name="general"></a>Algemeen

Op het sneltabblad **Algemeen** kunt u een unieke rapportindeling maken. De naam van het rapport is een unieke identificatie die gebruikers kunnen herkennen in het werkgebied **Kostenbeheer**. U kunt ook opgeven of het rapport moet worden gedeeld of intern moet blijven voor kostenaccountants.

| Veld       | Omschrijving |
|-------------|-------------|
| Naam        | Voer een unieke naam voor de indeling in. |
| Omschrijving | Voer een gedetailleerde omschrijving in. |
| Gepubliceerd   | Als u dit veld instelt op **Ja**, kan een gebruiker die is toegewezen aan een van de volgende rollen, het rapport in het werkgebied **Kostenbeheer** zien:<ul><li>Manager van kostprijsboekhouding</li><li>Kostenaccountant</li><li>Assistent kostenaccountant</li><li>Controller voor kostenobjecten</li></ul>Als u dit veld instelt op **Nee**, kunnen alleen gebruikers die zijn toegewezen aan een van de volgende rollen, het rapport in het werkgebied **Kostenbeheer** zien:<ul><li>Manager van kostprijsboekhouding</li><li>Kostenaccountant</li><li>Assistent kostenaccountant</li></ul> |

### <a name="data-filtering"></a>Gegevens filteren

Op het sneltabblad **Gegevens filteren** definieert u de basis van de gegevens voor het rapport. Gebruikers van dit rapport zien waarden in het rapport nadat brongegevens zijn verwerkt.

| Veld                                                             | Omschrijving |
|-------------------------------------------------------------------|-------------|
| Grootboek van kostprijsboekhouding                                            | **Grootboek van kostprijsboekhouding** waarop het rapport is gebaseerd. De waarde wordt afgeleid van het veld **Kostenbeheereenheid**. |
| Kostenbeheereenheid                                                 | De waarde die u selecteert bepaalt het grootboek voor kostprijsboekhouding en kostenobjecten waarop dit rapport wordt gebaseerd. |
| Statistische dimensiehiërarchie, Dimensiehiërarchie van een kostenelement | Met een configuratierecord van het werkgebied **Kostenbeheer** kunnen niet-monetaire of monetaire waarden worden gerapporteerd, maar niet in dezelfde indeling. Selecteer een waarde in het veld **Dimensiehiërarchie van een kostenelement** om monetaire waarden te rapporteren. Selecteer een waarde in het veld **Statistische dimensiehiërarchie** om niet-monetaire waarden te rapporteren. De record van de dimensiehiërarchie die u selecteert, bepaalt de structuur van de rapportage- en samenvoegingsniveaus.<blockquote>[!NOTE]<br>Als u niet-monetaire en monetaire waarden naast elkaar wilt weergeven, kunt u gegevens exporteren naar Microsoft Excel voor het Microsoft Power BI-inhoudpakket.</blockquote> |
| Dimensiehiërarchie van een kostenobject                                   | Selecteer de dimensiehiërarchie van de kostenobjectdimensie die aansluit bij het doel van de rapportage die u definieert. |
| Oorspronkelijk versie van budget                                           | Selecteer de budgetversie-id die fungeert als het oorspronkelijke budget in de context van dit rapport. |
| Herziene versie van budget                                            | Selecteer de budgetversie-id die fungeert als het herziene budget in de context van dit rapport. |

### <a name="assign-calculation-records"></a>Berekeningsrecords toewijzen

Met de overheadberekening worden verschillende berekeningsstappen op de brongegevens uitgevoerd, zoals kostengedragclassificatie, kostenverdeling en kostentoewijzing. Meerdere overheadberekeningen kunnen worden uitgevoerd voor dezelfde boekperiode, in het geval ontbrekende brongegevens worden ontdekt of regels moeten worden bijgewerkt. Elke overheadberekening wordt opgeslagen met een unieke id. De kostenaccountant kan een specifieke berekenings-id selecteren. Gebruikers van het rapport, zoals managers, zien de resultaten van de overheadberekening in het werkgebied **Kostenbeheer**.

| Veld                  | Omschrijving |
|------------------------|-------------|
| Fiscale kalenderperiode | Selecteer de fiscale kalenderperiode waaraan u een overheadberekenings-id wilt toewijzen.<blockquote>[!NOTE]<br>De boekperioden die in het veld worden weergegeven, zijn afkomstig van de fiscale kalender die is gekoppeld aan het grootboek van kostprijsboekhouding.</blockquote> |
| Actuele versie         | Selecteer de juiste overheadberekenings-id. |
| Budgetversie         | Selecteer de juiste overheadberekenings-id. |
| Herziene budgetversie | Selecteer de juiste overheadberekenings-id. |

### <a name="fiscal-periods-per-column"></a>Boekperioden per kolom

Op het sneltabblad **Boekperioden per kolom** bepaalt de kostenaccountant welke boekperiode moet worden weergegeven in de rapportindeling.

De waarden in de geselecteerde kolommen worden vermenigvuldigd met de geselecteerde waarden op het sneltabblad **Boekperioden per kolom**.

| Veld                | Omschrijving |
|----------------------|-------------|
| Huidige periode       | Het saldo van de huidige boekperiode wordt weergegeven.<blockquote>[!NOTE]<br>Standaard wordt de huidige periode bepaald door de sessiedatum. In het werkgebied **Kostenbeheer** kan een specifieke boekperiode worden geselecteerd. De geselecteerde waarde vertegenwoordigt vervolgens de huidige periode.</blockquote> |
| Vorige periode      | Het saldo van de vorige boekperiode wordt weergegeven. De volgende formule wordt hierbij gebruikt:<br>Huidige boekperiode: 1<blockquote>[!NOTE]<br>Standaard wordt de vorige periode afgeleid van de sessiedatum. In het werkgebied **Kostenbeheer** kan een specifieke boekperiode worden geselecteerd als de huidige periode. Vervolgens wordt **Vorige periode** dienovereenkomstig opnieuw berekend.</blockquote> |
| Jaar tot heden         | De datum van jaar tot heden wordt weergegeven. De volgende formule wordt hierbij gebruikt:<br>Jaar tot heden (huidige boekperiode)<blockquote>[!NOTE]<br>Standaard wordt de huidige periode bepaald door de sessiedatum. In het werkgebied **Kostenbeheer** kan een specifieke boekperiode worden geselecteerd. De geselecteerde waarde vertegenwoordigt vervolgens de huidige periode en de waarde bij **Jaar tot heden** wordt dienovereenkomstig bijgewerkt.</blockquote> |
| Gemiddelde van jaar tot heden | Het gemiddelde voor jaar tot heden wordt weergegeven. De volgende formule wordt hierbij gebruikt:<br>(Jaar tot heden [huidige boekperiode]) ÷ (aantal [huidige boekperiode])<p><strong>Voorbeeld</strong></p><ul><li>**Lid statistische dimensie:** voltijdse werknemers</li><li>**Huidige datum:** 21-3-2017</li><li>**Periode:** boekperiode 1, boekperiode 2, boekperiode 3</li><li>**Grootte:** 10, 10, 12</li></ul>In dit geval **Gemiddelde van jaar tot heden** (10 + 10 + 12) ÷ 3 = 10,67<p>De waarde van **Gemiddelde van jaar tot heden** kan worden berekend voor kostenelementdimensieleden en statistische dimensieleden.</p><blockquote>[!NOTE]<br>Standaard wordt de huidige periode bepaald door de sessiedatum. In het werkgebied **Kostenbeheer** kan een specifieke boekperiode worden geselecteerd. De geselecteerde waarde vertegenwoordigt vervolgens de huidige periode en de waarden bij **Jaar tot heden** en **Gemiddelde van jaar tot heden** wordt dienovereenkomstig bijgewerkt.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Weer te geven kolommen voor kosten

Op het sneltabblad **Weer te geven kolommen voor kosten** bepaalt de kostenaccountant welke kolommen de rapportindeling moet bevatten. Er zijn drie categorieën: vaste kosten, variabele kosten en niet-geclassificeerde kosten.

| Veld                 | Omschrijving |
|-----------------------|-------------|
| Vaste kosten            | Dit kolomtype bevat de vaste kosten op basis van de geselecteerde overheadberekenings-id.<blockquote>[!NOTE]<br>Dit kolomtype toont alleen een saldo wanneer een overheadberekenings-id voor de boekperiode wordt geselecteerd.</blockquote> |
| Variabele kosten         | Dit kolomtype bevat de variabele kosten op basis van de geselecteerde overheadberekenings-id.<blockquote>[!NOTE]<br>Dit kolomtype toont alleen een saldo wanneer een overheadberekenings-id voor de boekperiode wordt geselecteerd.</blockquote> |
| Vaste + variabele kosten | Dit kolomtype bevat de vaste kosten en de variabele kosten op basis van de geselecteerde overheadberekenings-id.<blockquote>[!NOTE]<br>Dit kolomtype toont alleen een saldo wanneer een overheadberekenings-id voor de boekperiode wordt geselecteerd.</blockquote> |
| Totale kosten            | Dit kolomtype bevat de totale kosten (niet-geclassificeerde kosten, vaste kosten en variabele kosten).<blockquote>[!NOTE]<br>Het kolomtype bevat het saldo te allen tijde.</blockquote> |
| Ongeclassificeerde kosten     | Dit kolomtype bevat de niet-geclassificeerde kosten.<blockquote>[!NOTE]<br>Deze kolom kan worden gebruikt om te controleren of alle kosten correct zijn geclassificeerd door de overheadberekening en of regels voor kostengedrag moeten worden gecorrigeerd.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Weer te geven kolommen voor gebudgetteerde kosten

Op het sneltabblad **Weer te geven kolommen voor gebudgetteerde kosten** bepaalt de kostenaccountant welke kolommen moeten worden weergegeven voor de geselecteerde budgetversies. Afzonderlijke selecties kunnen worden gemaakt voor het oorspronkelijke en het herziene budget.

> [!NOTE]
> Omdat de volgende velden zich op dezelfde manier gedragen voor het oorspronkelijke budget en het herziene budget, worden ze slechts één keer uitgelegd.

| Veld                     | Omschrijving |
|---------------------------|-------------|
| Budget                    | Budgetsaldi worden op basis van geselecteerde kolommen weergegeven.<blockquote>[!NOTE]<br>De saldi worden gebaseerd op de budgetversies die zijn geselecteerd op het sneltabblad **Gegevens filteren**.</blockquote> |
| Budgetafwijking           | Bereken het verschil tussen de werkelijke en gebudgetteerde waarden. De volgende formule wordt hierbij gebruikt:<br>Budgetsaldo: werkelijk saldo |
| Budgetafwijking in %      | Bereken en toon het verschil in een percentage tussen de werkelijke en gebudgetteerde waarden. De volgende formule wordt hierbij gebruikt:<br>(Budgetsaldo: werkelijk saldo) ÷ budgetsaldo |
| Drempel voor afwijkingsperiode | Stel een drempel voor de afwijking in een monetair bedrag in voor de huidige periode. Als de drempel wordt overschreden, wordt de regel gemarkeerd in rood in het werkgebied **Kostenbeheer**.<blockquote>[!NOTE]<br>Dit veld geldt alleen voor de kostenelementen die staan voor uitgaven.</blockquote> |
| Drempel voor afwijkingsjaar   | Stel een drempel voor de afwijking in een monetair bedrag in voor het jaar. Als de drempel wordt overschreden, wordt de regel gemarkeerd in rood in het werkgebied **Kostenbeheer**. |
| Drempel voor afwijking %      | Stel een drempel voor de afwijking in een percentage in. Als de drempel wordt overschreden, wordt de regel gemarkeerd in rood in het werkgebied **Kostenbeheer**.<blockquote>[!NOTE]<br>Dezelfde percentagedrempel geldt voor de huidige periode en het huidige jaar.</blockquote> |

## <a name="cost-control-workspace"></a>Werkgebied voor kostenbeheer

Het werkgebied **Kostenbeheer** is ontworpen als een webrapport. Daarom kan aan alle managers die verantwoordelijk voor een kostenobject zijn, toegang worden verleend, zoals beschreven in [Toegangsrechten definiëren voor controllers van kostenobjecten](access-rights-cost-object-controller.md).

De lijst met rapporten die beschikbaar zijn voor gebruikers, zoals managers, wordt bepaald door de instelling van de optie **Gepubliceerd** op de pagina **Configuraties van werkgebied voor kostenbeheer**.

![Een rapport dat gebruikers in het werkgebied Kostenbeheer kunnen zien](./media/report-cost-control.png)

Een manager kan de fiscale kalenderperiode selecteren om weer te geven. De huidige standaardperiode wordt bepaald door de sessiedatum.

De waarden in de fiscale kalenderperiode worden bepaald door de rapportnaam en de fiscale kalender die is geselecteerd voor het grootboek van kostprijsboekhouding die is gekoppeld aan de naam van het rapport op de pagina **Configuraties van werkgebied voor kostenbeheer**.

Gebruikers kunnen het aggregatieniveau waarop saldi moeten worden weergegeven, selecteren in de dimensiehiërarchie voor kostenobjecten. Door beveiliging op toegangsniveau in te schakelen, beheert u de machtigingen, zodat gebruikers alleen de hiërarchieniveaus kunnen selecteren waarvoor aan hen toegang is verleend. Ze kunnen daarom alleen de samengevoegde saldi zien waarvoor aan hen toegang is verleend.

### <a name="add-or-remove-columns"></a>Kolommen toevoegen of verwijderen

Gebruikers kunnen de kolommen in een rapport aanpassen aan hun behoeften.

### <a name="view-details"></a>Details weergeven

Gebruikers kunnen inzoomen op de gegevens achter de saldi die worden weergegeven in het werkgebied. Als gebruikers een dimensiehiërarchieknooppunt voor kostenelementen selecteren en vervolgens klikken op **Details weergeven**, bevat het dialoogvenster **Kostenelementgegevens** gedetailleerde informatie voor het knooppunt.

Een raster bevat elk kostenelement dat is gekoppeld aan het knooppunt van de kostenelementdimensiehiërarchie en de bijbehorende waarden. De kolommen die worden weergegeven in het raster, komen overeen met de werkgebiedinstellingen.

Twee grafieken bevatten een overzicht van werkelijke versus gebudgetteerde waarden en budgetafwijking per periode.

![Grafieken die een overzicht van werkelijke versus gebudgetteerde waarden en budgetafwijking per periode bevatten.](./media/cost-element-details-operations.png)

Gebruikers kunnen klikken op **Kosteninvoer** om indien nodig in te zoomen op de invoergegevens.

![Kosteninvoer](./media/cost-entries.png)

Huur is bijvoorbeeld een uitgave die naar kostenplaatsen wordt gedistribueerd. Een gebruiker die inzicht wil krijgen in de huurkosten die zijn of haar kostenplaats moet dragen, kan inzoomen om te zien hoe huur wordt berekend.

Als gebruikers klikken op **Toewijzingsgrondslag** op de pagina **Kosteninvoer**, verschijnt er een dialoogvenster. Gebruikers kunnen vervolgens de toewijzingsgrondslag toewijzen aan de regel en de bijbehorende statistische maateenheden weergeven die zijn geregistreerd voor de periode.

In het volgende voorbeeld is de toewijzingsgrondslag van het type **Toewijzingsgrondslag van formule** en wordt de formule weergegeven. De factoren waarmee de formule wordt gedefinieerd, worden weergegeven. Bovendien wordt in een raster de berekening weergegeven die per kostenplaats wordt uitgevoerd.

![Berekeningen per kostenobject](./media/cost-entries-allocation-base.png)

Aanvullende resources 

[Toegangsrechten definiëren voor controllers voor kostenobjecten](access-rights-cost-object-controller.md)



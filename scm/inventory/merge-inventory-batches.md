---
title: Voorraadbatches samenvoegen
description: "Dit artikel bevat informatie over het consolideren van twee of meer voorraadbatches in één samengevoegde batch."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 49ed9255e58053b747bc66af8a0f8e0400eee1b0
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="merge-inventory-batches"></a>Voorraadbatches samenvoegen

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie over het consolideren van twee of meer voorraadbatches in één samengevoegde batch. 

Wanneer u batches samenvoegt, kunnen berekeningen helpen bij het optimaliseren van de eigenschappen en batchkenmerken van de samengevoegde batch. Nadat de bronbatches zijn geselecteerd, kan de samengevoegde batch worden beoordeeld en aangepast voordat u deze boekt. U kunt ook de batchsamenvoeging overboeken naar een voorraadjournaal voor goedkeuring. De voorraad kan vervolgens direct vanaf dat voorraadjournaal worden gereserveerd of worden geboekt. Wanneer u een samengevoegde batch boekt, wordt de voorraad aangepast voor de bronbatches en de samengevoegde batch.

## <a name="are-there-any-prerequisites"></a>Zijn er vereisten?
Ja, er zijn bepaalde zaken die u moet instellen voordat u de gereedschappen kunt gebruiken om batches samen te voegen. De onderstaande tabel geeft een overzicht van de vereisten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pagina</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Journaalnamen, voorraad</td>
<td>U moet de journaalnaam maken die standaard wordt gebruikt wanneer u batchsamenvoegingen in voorraadjournalen boekt. Optioneel, maar wel aanbevolen: u kunt opgeven dat reservaties automatisch worden uitgevoerd wanneer de batchsamenvoeging wordt overgedragen naar het voorraadjournaal. Anders bestaat het risico dat er een wijziging wordt uitgevoerd aan de voorhanden voorraad nadat de details van de batchsamenvoeging zijn ingesteld en het journaal is geboekt. Om automatische reserveringen in te schakelen voor de journaalnaam, selecteert u <strong>Automatisch</strong> in het veld <strong><strong>Reservering</strong></strong>.</td>
</tr>
<tr class="even">
<td>Parameters voor voorraad- en magazijnbeheer</td>
<td>U moet de standaard journaalnaam opgeven voor het voorraadjournaal.</td>
</tr>
<tr class="odd">
<td>Vrijgegeven producten</td>
<td>De aanbevolen instellingen voor het artikel zijn:
<ul>
<li>Als u automatisch batchnummers wilt genereren voor samengevoegde batches, moet u het vrijgegeven product toewijzen aan een batchnummergroep. U kunt ook handmatig een batchnummer invoeren wanneer u een samengevoegde batch maakt, of een bestaand batchnummer selecteren. Als u een bestaand nummer selecteert, moet u ervoor zorgen dat de geselecteerde batch niet is opgenomen in voorraadtransacties.</li>
<li>Als u de houdbaarheid of de uiterste houdbaarheidsdatum gebruikt voor het vrijgegeven product, worden de datums voor een samengevoegde batch berekend op basis van de selectie van het veld <strong>Berekening datum van batchsamenvoeging</strong>. De volgende opties zijn beschikbaar:
<ul>
<li><strong>Vroegste</strong> – De berekening is gebaseerd op de vroegste datum die is opgegeven voor een bronbatch die is geselecteerd voor de batchsamenvoeging.</li>
<li><strong>Laatste</strong> – De berekening is gebaseerd op de laatste datum die is opgegeven voor een bronbatch die is geselecteerd voor de batchsamenvoeging.</li>
<li><strong>Handmatig</strong> - Er wordt geen berekening gemaakt. Als een datum dezelfde is bij alle bronbatches, wordt een datum voorgesteld. U kunt deze datum wijzigen. Als een datum niet dezelfde is op de bronbatches, kunt u deze handmatig invoeren.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Batchnummergroep</td>
<td>Optioneel: als u een batchnummer wilt genereren wanneer u een samengevoegde batch maakt, moet u een batchnummergroep toewijzen aan het vrijgegeven product. Anders kunt u handmatig een batchnummer invoeren.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Wanneer zou ik voorraadbatches willen samenvoegen?
De volgende scenario's zijn voorbeelden van wanneer het nuttig zou zijn om batches samen te voegen:

-   Sammy wandelt door zijn magazijn en merkt dat er verschillende batches van hetzelfde product weinig voorraad hebben. Hij verwacht verschillende nieuwe zendingen en hij realiseert dat hij vloerruimte kan vrijmaken door de kleine hoeveelheden samen te voegen in een nieuwe batch.
-   Sammy ontvangt voorraad en wil de nieuwe batch combineren met de batch die hij al heeft ontvangen om de waarde batchkenmerk van de bestaande batch te verbeteren.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Kan ik batches van verschillende locaties en rechtspersonen samenvoegen?
Nee. U kunt alleen batches samenvoegen met dezelfde locatie en magazijnopslagdimensies in één rechtspersoon. U kunt echter een andere locatie en pallet-id opgeven voor de samengevoegde batch.

## <a name="can-i-merge-partial-quantities"></a>Kan ik gedeeltelijke hoeveelheden samenvoegen?
Nee, u kunt alleen de volledige hoeveelheid van batches samenvoegen. De functionaliteit van batch samenvoegen is bedoeld als voorraadfunctie, geen productiefunctie.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Wat als de batches verschillende batchkenmerkwaarden hebben?
Wanneer u de bronbatches selecteert om te combineren in de samengevoegde batch, zal Microsoft Dynamics 365 for Operations controleren of alle batches de eigenschappen of kenmerkwaarden hebben. Wanneer een kenmerkwaarde dezelfde is, wordt een waarde voorgesteld voor de samengevoegde batch. U kunt deze waarde wijzigen. Kenmerkwaarden die niet dezelfde zijn, worden leeg gelaten voor de samengevoegde batch en u kunt deze waarden handmatig invoeren. Als het type batchkenmerk voor de kenmerkwaarde een geheel getal of een breuk is, en de waarden zijn niet dezelfde voor alle bronbatches, wordt de waarde berekend met behulp van een gewogen gemiddelde. De berekende waarde wordt naar boven of beneden afgerond naar de dichtste stap. Als de waarde leeg is voor een bronbatch, worden de batch en de hoeveelheid niet opgenomen in de berekening. **Voorbeeld** Het volgende voorbeeld toont de berekening van een gewogen gemiddelde voor een samengevoegde batch. Twee van de bronbatches hebben een blanco waarde voor een batchkenmerktype dat een geheel getal is. Het volgende kenmerk wordt toegewezen aan de bronbatches.

| Kenmerk | Min.voorraad | Verhoging | Max.voorraad |
|-----------|---------|-----------|---------|
| Cijfer     | 3       | 3         | 30      |

De bronbatches hebben de volgende kenmerkwaarden voor het kenmerk **Schaal**.

| Batch | Hoeveelheid | Kenmerk | Kenmerkwaarde |
|-------|----------|-----------|-----------------|
| B1    | 10       | Cijfer     | Leeg           |
| B2    | 15       | Cijfer     | 15              |
| B3    | 20       | Cijfer     | 20              |
| B4    | 25       | Cijfer     | Leeg           |
| B5    | 30       | Cijfer     | 25              |

Wanneer u deze batches toevoegt als bronbatches, worden de volgende waarden toegekend aan de samengevoegde batch.

| Batch | Hoeveelheid | Kenmerk | Kenmerkwaarde |
|-------|----------|-----------|-----------------|
| B6    | 100      | Cijfer     | 21              |

De waarden en hoeveelheden voor batches B1 en B4 zijn niet opgenomen in de berekening van het gewogen gemiddelde. Daarom wordt de waarde voor de samengevoegde batch als volgt berekend.

| Waarde | Hoeveelheid (gewicht)                              | Relatief gewicht | Relatief gewicht × waarde                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0.230769231     | 3.461538462                                                           |
| 20    | 20                                             | 0.307692308     | 6.153846154                                                           |
| 25    | 30                                             | 0.461538462     | 11.53846154                                                           |
|       | **Totaal:** 65, het totaal van de gewichten |                 | **Totaal:** 21,5384615, afgerond naar 21, wat de dichtstbijzijnde stap is. |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Wat als de batches verschillende batchdatums hebben?
Als de batches verschillende batchdatums hebben, worden sommige datums berekend op basis van de waarden in de groep **Batchdatums** op het sneltabblad **Samengevoegde batch** van de pagina **Batchsamenvoeging**. Het systeem berekent waarden voor de velden in de groep **Batchdatums**. Deze omvatten de productiedatum, vervaldatum, houdbaarheidsadviesdatum en uiterste houdbaarheidsdatum. De datums worden berekend op basis van instellingen voor het artikel in de veldgroep **Artikelgegevens** van de pagina **Vrijgegeven productdetails**. U kunt de waarden wijzigen of handmatig invoeren. Er worden geen berekeningen gemaakt voor alle andere datums. Hetzelfde principe wordt gebruikt voor batchkenmerkwaarden. Als een datum dezelfde is voor alle bronbatches, wordt deze datum voorgesteld voor de samengevoegde batch. Als de datum niet dezelfde is voor alle bronbatches, is de datum leeg op de samengevoegde batch en kunt u deze handmatig invoeren.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Wat als de dimensies verschillend zijn voor de batches die ik wil samenvoegen?
Productdimensies, traceringsdimensies en opslagdimensies worden als volgt verwerkt:

-   **Productdimensies** – Alle productdimensies voor het geselecteerde artikel moeten hetzelfde zijn. U kunt geen batches samenvoegen van verschillende productdimensies.
-   **Traceringsdimensies** – Er wordt automatisch een nieuw batchnummer gemaakt als een batchnummergroep wordt opgegeven voor het artikel. Als een batchnummergroep niet aan een artikel wordt toegewezen, kunt u een bestaande batch selecteren of het nummer handmatig invoeren. Serienummers worden overgebracht van de bronbatch naar de voorraadjournaalregels voor de samengevoegde batch.
-   **Opslagdimensies** - De locatie- en magazijnopslagdimensies moeten dezelfde zijn voor alle bronbatches en de samengevoegde batch. U kunt echter een nieuwe locatie en pallet-id opgeven voor de samengevoegde batch.

## <a name="how-does-posting-work"></a>Hoe werkt boeken?
De boekingen werken op twee manieren, afhankelijk van hoe u een goedkeuringsproces gebruikt voor journalen. U kunt de knoppen **Overboeken naar journaal** en **De batchsamenvoeging boeken** gebruiken om de batchsamenvoeging over te brengen naar een journaal waar deze kan worden gecontroleerd en geboekt, of u kunt de batchsamenvoeging direct boeken. Het belangrijkste verschil tussen de twee acties is dat overdragen naar een journaal de batchsamenvoeging niet boekt. Beide acties creëren een nieuwe batch als een bestaande batch niet is geselecteerd, werken alle batchgegevens en kenmerkwaarden bij en maken een voorraadjournaal.

-   **Overboeken naar journaal** - Brengt de batchsamenvoegingsdetails over naar een nieuw voorraadjournaal. Als u automatische reserveringen hebt ingesteld, zijn de hoeveelheden in de bronbatches gereserveerd. De details van de batchsamenvoeging kunnen niet worden gewijzigd. Als u de batchsamenvoeging wilt wijzigen, moet u het journaal verwijderen. Het journaal kan als een taak worden gebruikt die een andere werknemer later moet uitvoeren. De reservering van de batchhoeveelheid voor de journaalregel is beveiligd. Met deze toewijzing kan een kwaliteitsplanner of een magazijnmanager taken voor zijn of haar werknemers maken.
-   **De batchsamenvoeging boeken** - Boekt de batchsamenvoeging direct. Deze actie kan worden uitgevoerd nadat de fysieke samenvoeging heeft plaatsgevonden.

U kunt het voorraadjournaal goedkeuren voor de batchsamenvoeging vanaf de lijstpagina **Alle batchsamenvoegingen**. Klik op **Journaal** &gt; **Boeken**. Nadat een journaal is geboekt, kunt u de details niet wijzigen in de samengevoegde batch. Nadat u een batchsamenvoeging naar een voorraadjournaal overdraagt, kunt u de details alleen wijzigen als het journaal wordt verwijderd.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Waarom kan ik de informatie over variabel gewicht niet zien in het voorraadjournaal nadat ik een artikel met variabel gewicht heb samengevoegd?
U kunt batches van catch weight-artikels samenvoegen, net zoals alle andere artikels. De catch weight-informatie wordt echter niet weergegeven op het voorraadjournaal. Wij raden u aan de catch weight-informatie na te gaan voordat u de batchsamenvoeging overdraagt naar het voorraadjournaal.





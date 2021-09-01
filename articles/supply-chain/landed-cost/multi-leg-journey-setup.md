---
title: Een traject met meerdere etappes instellen
description: In dit onderwerp wordt beschreven hoe u trajecten met meerdere etappes kunt instellen voor de module Francoprijzen.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 045ded1fb881b0572f4490ab3a5d4ca1cb8c341a4d245e6d98991228a90aadb7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774073"
---
# <a name="multi-leg-journey-setup"></a>Een traject met meerdere etappes instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u trajecten met meerdere etappes kunt instellen voor de module **Francoprijzen**.

## <a name="legs"></a>Etappes

Etappes worden gebruikt om afzonderlijke delen van een traject te identificeren. Elke etappe wordt gemaakt door de aankomst- en vertrekhavens te selecteren en de transportmethode te selecteren die voor de etappe wordt gebruikt. Er kunnen doorlooptijden worden gekoppeld aan elke etappe. Doorlooptijden kunnen helpen bij het bijhouden van een zending en kunnen ook worden gebruikt om de geschatte leveringsdatum van de goederen tijdens een reis te berekenen. Wanneer er een etappe van een traject is voltooid, kan bovendien de status van de reis, de container en de bijbehorende inkooporderregels, via de instellingen van traceringsbeheer worden bijgewerkt. Etappes kunnen worden gebruikt in één trajectsjabloon, maar kunnen ook steeds opnieuw worden gebruikt in meerdere trajectsjablonen. Het laden van containers, de gang langs de douane en lokaal transport worden meestal ingesteld als etappes en hiervoor wordt een niet-specifieke haven gebruikt.

Als u met etappes wilt werken, gaat u naar **Francoprijzen \> Een traject met meerdere etappes instellen \> Etappes**. Hier kunt u records voor etappes weergeven, openen, maken en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Etappe | Voer een unieke identificatienaam of een uniek identificatienummer in voor de etappe van het traject. |
| Beschrijving | Voer een korte beschrijving in van de etappe van het traject. Gewoonlijk worden in deze beschrijving de aankomst- en vertrekhavens aangeduid of de stap van het traject. |
| Vertrekhaven | Voer het punt van vertrek van de goederen op de etappe in. |
| Aankomsthaven | Voer het punt van bestemming van de goederen op de etappe in. |
| Leveringswijze | Voer de transportmethode voor de etappe in. |

## <a name="journey-templates"></a>Trajectsjablonen

In een trajectsjabloon wordt het traject gedefinieerd dat goederen afleggen tussen twee havens tijdens een reis en dit traject bestaat uit meerdere etappes. De etappes van een traject worden gecombineerd om de tijd vast te stellen die nodig is voor goederen om van het punt van vertrek bij de leverancier naar de eindbestemming, het magazijn, te reizen. Wanneer de etappes in een bepaalde volgorde in de trajectsjabloon wordt geplaatst, bepalen de doorlooptijden de datum van elke etappe en de status van de reis, de container en de inkoopregels voor de reis. U kunt het [Traceringsbeheercentrum](delivery-information-setup.md) gebruiken om de doorlooptijden in te stellen die zijn gekoppeld aan elke etappe in de trajectjabloon. De trajectsjabloon wordt ook gebruikt wanneer de automatische kosten van een reis worden ingesteld. Wanneer er een traject is gedefinieerd, kunnen de kosten die aan het transport van de goederen zijn gekoppeld, worden gedefinieerd op de pagina voor automatische kosten.

Als u met trajectsjablonen wilt werken **Francoprijzen \> Een traject met meerdere etappes instellen \> Trajectsjablonen**. Hier kunt u trajectsjablonen weergeven, openen, maken en verwijderen.

Stel voor elke trajectsjabloon de volgende velden in de header in.

| Veld | Beschrijving |
|---|---|
| Trajectsjabloon | Voer een unieke identificatienaam of een uniek identificatienummer in voor de trajectsjabloon. De trajectsjabloon beschrijft doorgaans het punt van vertrek en het punt van bestemming voor het traject. |
| Beschrijving | Voer een beschrijving van de trajectsjabloon in. In de beschrijving worden normaal gesproken de vertrek- en aankomsthavens en het type reis aangeduid. |

Voeg in de sectie **Regels** een regel toe voor elke etappe van het traject en plaats de regels in de juiste volgorde. Gebruik de pijlen **Omhoog** en **Omlaag** op de werkbalk om de volgorde van de regels te wijzigen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke regel.

| Veld | Beschrijving |
|---|---|
| Etappe | Selecteer een etappe om toe te voegen aan het traject. |
| Beschrijving | De beschrijving van de etappe. |
| Vertrekhaven | De haven die het punt van vertrek is van de goederen op de etappe. Deze haven is de aankomsthaven die wordt gebruikt om de automatische kosten voor een reis te bepalen. |
| Aankomsthaven | Voer het punt van bestemming van de goederen op de etappe in. |
| Leveringsmethode | De methode van levering die wordt gebruikt voor de etappe. |
| Vertrekhaven van traject | Als de haven die is opgegeven voor de etappe, wordt gebruikt om de automatische kosten te bepalen, schakelt u dit selectievakje in om de haven aan te duiden als vertrekhaven van het traject. Deze haven wordt in de header van de reis weergegeven. |
| Aankomsthaven van traject | Als de haven die is opgegeven voor de etappe, wordt gebruikt om de automatische kosten te bepalen, schakelt u dit selectievakje in om de haven aan te duiden als aankomsthaven van het traject. Deze haven wordt in de header van de reis weergegeven. |
| Expeditiebedrijf | Selecteer het expeditiebedrijf dat wordt gebruikt voor de etappe. |

## <a name="activities"></a>Activiteiten

De instellingen op de pagina **Activiteiten** bepalen de typen activiteiten die kunnen plaatsvinden in de bestemmingshaven van een etappe. Gebruikers die de pagina **Alle containers** gebruiken, kunnen uit deze waarden kiezen wanneer ze de duur van elke activiteit schatten en de werkelijke duur registreren voor vergelijkingsdoeleinden.

Als u activiteiten wilt instellen, gaat u naar **Francoprijzen \> Een traject met meerdere etappes instellen \> Activiteiten**. Hier kunt u activiteiten toevoegen, verwijderen en bewerken met de knoppen in het actievenster.

In de volgende tabel worden de velden beschreven die voor elke activiteit in het raster beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Activiteit | De naam van de activiteit. |
| Beschrijving | Een beschrijving van de activiteit. |
| Expeditiebedrijf | De leveranciersrekening van het expeditiebedrijf dat is gekoppeld aan de activiteit. |

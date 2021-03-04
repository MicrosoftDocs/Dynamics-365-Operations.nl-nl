---
title: Beleid voor totalisering van kosten en overheadberekening
description: Dit onderwerp bevat informatie over het bepalen van het juiste niveau van secundaire kostenelementen en het maken van regels voor kostentotalisering die passen in de organisatierapportage en de traceerbaarheid van kosten.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy, CAMOverheadRatePolicy
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b02bfd83cfc4f1585c9044ebca8b20413042124a
ms.sourcegitcommit: b40d6ce45aeb07724fc41d1a41923970b007fbcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2020
ms.locfileid: "4442127"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Beleid voor totalisering van kosten en overheadberekening 

[!include [banner](../includes/banner.md)]

Met Kostprijsboekhouding kunt u inzicht verkrijgen in hoe de kostenstroom in relatie staat tot de producten en services die worden geleverd binnen een organisatie. Als u de transparantie van de kosten wilt zien, is het van groot belang om kostentoewijzing te bereiken tussen kostenobjecten op basis van een juiste toewijzingsgrondslag. Standaard wordt de kostentoewijzing bereikt voor het primaire kostenelement. Dit is in bepaalde situaties wenselijk. Het heeft echter een paar gevolgen die in aanmerking moeten worden genomen.

-   Bijkomende kostenobjecten eindigen met een nulsaldo voor het primaire kostenelement na overheadberekening.

-   Het volume van kosteninvoer gegenereerd door overheadberekening kan zeer hoog zijn.

-   Het is niet mogelijk om de kostenstroom tussen kostenobjecten bij te houden.

Om deze gevolgen te voorkomen, kunt u met Kostprijsboekhouding kostentoewijzing configureren zodat deze past binnen de vereisten voor managementrapporten in uw organisatie. In dit onderwerp wordt besproken hoe u het juiste niveau van secundaire kostenelementen kunt bepalen en regels voor kostentotalisering kunt maken die passen in de organisatierapportage en de traceerbaarheid van kosten.

> [!NOTE]
> U kunt configuraties wijzigen als rapportagevereisten veranderen.

## <a name="example-of-cost-rollup-policy-setup"></a>Voorbeeld van het instellen van beleid voor kostentotalisering

Stel dat een organisatie de volgende structuur heeft met 4 kostenplaatsen.

![Voorbeeld van een organisatiestructuur](./media/dimension-hierarchy-org.png)

**Dimensie van kostenobject**

| Kostenplaatsen | Omschrijving          |
|--------------|-----------|
| CC001        | HR        |
| CC002        | Financiën   |
| CC003        | Assembleren  |
| CC004        | Verpakking |

**Dimensie van kostenelement**

| Kostenelementen | Omschrijving | Type    |
|---------------|-------------|---------|
| 1001          | Elektriciteit | Primair |
| 1002          | Salarissen    | Primair |
| 1003          | Reclame | Primair |

Een dimensiehiërarchie die voldoet aan de rapportagevereisten van de organisatie kan als volgt worden ingesteld.

**Gegevens van dimensiehiërarchie**

| Naam van dimensiehiërarchie | Dimensie    | Naam van type dimensiehiërarchie      | Hiërarchie van toegangslijsten |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatie             | Kostenplaatsen | Hiërarchie dimensieclassificatie | Nee                    |

**Dimensiehiërarchie**

|    &nbsp;    | Bereiken van dimensieleden | &nbsp;              |
|--------------|-------------------------|---------------------|
| **Knooppunten**        | **Van dimensielid**   | **Tot dimensielid** |
| Organisatie |                         |                     |
| &nbsp;&nbsp;Beheer             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Financiën              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;HR               | CC002                   | CC002               |
| &nbsp;&nbsp;Productie               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Verpakking              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembleren             | CC004                   | CC004               |

Een dimensiehiërarchie die voldoet aan de beleidsvereiste kan als volgt worden ingesteld.

**Gegevens van dimensiehiërarchie**

| Naam van dimensiehiërarchie | Dimensie     | Naam van type dimensiehiërarchie      |
|--------------------------|---------------|------------------------------------|
| Winst- en verliesrekening  | Kostenelementen | Hiërarchie dimensieclassificatie |

**Dimensiehiërarchie**

|      &nbsp;             | Bereiken van dimensieleden |      &nbsp;         |
|-------------------------|-------------------------|---------------------|
| Knooppunten                   | Van dimensielid   | Tot dimensielid |
| Winst- en verliesrekening |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primaire kosten                    | 10001                   | 10003               |

Nadat de grootboekposten zijn verwerkt, ziet het kosteninvoersaldo per kostenobject er als volgt uit.

|      &nbsp;          | **Kostenobject** | &nbsp;    |  &nbsp;   |  &nbsp;   | **Totaal**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Kostenelement**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Elektriciteit** | 100,00          | 200.000    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Salarissen**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Advertenties** | 0.00            | 4.000,00  | 0.00      | 0.00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Statistische dimensie**

| Statistische elementen |    Omschrijving   |
|----------------------|------------------|
| SE-1                 | HR-services      |
| SE-2                 | Financiële services |

Kostenobject CC001 HR draagt HR-services bij aan verschillende kostenobjecten.

HR-services worden verbruikt door de volgende verdeling van de magnitude.

| Kostenobject | Omschrijving |   HR-services |
|-------------|-------------|----|
| CC002       | Financiën     | 35 |
| CC003       | Assembleren    | 55 |
| CC004       | Verpakking   | 10 |

Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.

Financiële services worden verbruikt door de volgende verdeling van magnitude.

| Kostenobject |   Omschrijving    |  Financiële services   |
|-------------|------------------|----|
| CC003       | Assembleren         | 65 |
| CC004       | Verpakking        | 35 |

Kostentoewijzingbeleidsregels kunnen als volgt worden ingesteld.

| Beleidsnaam | Omschrijving     | Dimensiehiërarchie van een kostenobject | Statistische dimensie | Dimensie van kostenelement |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Kostentoewijzing | Organisatie                    | Statistische elementen  | Kostenelementen          |

Kostentoewijzingsregels kunnen als volgt worden ingesteld.

| Dimensiehiërarchieknooppunt van een kostenobject | Kostengedrag | Toewijzingsgrondslag        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Totaal         | **HR-services**        |
| CC002                                | Totaal         | **Financiële services** |

<a name="brhow-cost-flows-between-cost-centers"></a><br>Hoe kosten tussen kostenplaatsen stromen 
---------------------------------------------------

Als u wilt weten hoe kosten stromen tussen de kostenplaatsen in de organisatie, kunt u kostenelementen van het type **Secundair** voor elke kostenplaats maken. Deze kostenelementen worden vervolgens gebruikt om saldi tussen de kostenplaatsen over te brengen tijdens het berekenen van overhead.

Kostenelementdimensieleden kunnen als volgt worden ingesteld.

| Kostenelementen | Type          |     &nbsp;    |
|---------------|---------------|---------------|
| 1001          | Elektriciteit   | Primair       |
| 1002          | Salarissen      | Primair       |
| 1003          | Reclame   | Primair       |
| **SC-CC001**  | **HR**        | **Secundair** |
| **SC-CC002**  | **Financiën**   | **Secundair** |
| **SC-CC003**  | **Assembleren**  | **Secundair** |
| **SC-CC004**  | **Verpakking** | **Secundair** |

De dimensiehiërarchie **Winst- en verliesrekening** moet worden bijgewerkt met de nieuwe dimensieleden zodat de dimensiehiërarchie de juiste gegevens bevat die kunnen worden gebruikt voor het definiëren van rapportage en beleid.

**Gegevens van dimensiehiërarchie**

| Naam van dimensiehiërarchie | Dimensie     | Naam van type dimensiehiërarchie      |
|--------------------------|---------------|------------------------------------|
| Winst- en verliesrekening  | Kostenelementen | Hiërarchie dimensieclassificatie |

**Dimensiehiërarchie**

|      &nbsp;             | Bereiken van dimensieleden |  &nbsp;             |
|-------------------------|-------------------------|---------------------|
| Knooppunten                   | Van dimensielid   | Tot dimensielid |
| Winst- en verliesrekening |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primaire kosten                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Secundaire kosten                         | **SC-CC001**            | **SC-CC004**        |

Maak een **Beleid voor totalisering van kosten** waarbij elke kostenplaats wordt toegewezen aan een corresponderend kostenelement van het type **Secundair**.

**Beleid voor totalisering van kosten**

| Beleidsnaam | Omschrijving | Dimensiehiërarchie van een kostenobject | Dimensiehiërarchie van een kostenelement |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Kostenstroom   | Organisatie                    | Winst- en verliesrekening          |

**Regels voor totalisering van kosten**

| Dimensiehiërarchieknooppunt van een kostenobject | Dimensiehiërarchieknooppunt van een kostenelement | Secundair kostenelement |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Winst- en verliesrekening               | **SC-CC001**           |
| CC002                                | Winst- en verliesrekening               | **SC-CC002**           |
| CC003                                | Winst- en verliesrekening               | **SC-CC003**           |
| CC004                                | Winst- en verliesrekening               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Overheadberekening uitvoeren

**Journaal**

| Journaal | Type journaal            | Fiscale kalenderperiode | Jaar | Periode | Versie       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Kostentoewijzingsjournaal | Fiscaal                 | 2017    | Periode 1 | Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1 |

**Beleid voor totalisering van kosten** wordt nu toegepast wanneer **Journaalboekingen voor kostenobjectsaldo** worden gemaakt.

**Journaalboekingen voor kostenobjectsaldo**

| Grootboekdatum | Kostenobject | Omschrijving  | Kostenelement | Omschrijving |  Bedrag |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31-01-2017      | CC001       | HR           | SC-CC001 | HR        | 10.100,00 |
| 31-01-2017      | CC002       | Financiën      | SC-CC002 | Financiën   | 17.735,00 |
| 31-01-2017      | CC003       | Assembleren     | SC-CC003 | Assembleren  | 31.082,75 |
| 31-01-2017      | CC004       | Verpakking    | SC-CC004 | Verpakking | 15.717,25 |

> [!NOTE]
> De journaalposten worden gemaakt op basis van de regels in **Beleid voor totalisering van kosten** als een beleid bestaat. Het saldo dat wordt weergegeven, is het saldo van de overheadberekening.

De pagina **Details van kostensaldoregel voor kostenobject** die wordt geopend vanuit de journaalposten toont hoe het saldo wordt verkregen.

**Voorbeeld: de journaalpost voor kostenobject CC002 Financiën**

**Details van kostensaldoregel voor kostenobject**

| Dimensielid van kostenelement | Omschrijving |  Bedrag   |
|-------------------------------|-------------|-----------|
| 1001                          | Elektriciteit | 200.000    |
| 1002                          | Salarissen    | 10.000,00 |
| 1003                          | Reclame | 4.000,00  |
| SC-CC001                      | HR          | 3.535,00  |

**Kosteninvoer gegenereerd door de overheadberekening**

| Kostenobject | Omschrijving  | Kostenelement   | Omschrijving  |        Bedrag     |       Grootboekdatum     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | HR           | SC-CC001 | HR              | 10.100,00\- | 31-01-2017 |
| CC002       | Financiën      | SC-CC001 | HR              | 3.535,00    | 31-01-2017 |
| CC003       | Assembleren     | SC-CC001 | HR              | 5.555,00    | 31-01-2017 |
| CC004       | Verpakking    | SC-CC001 | HR              | 1.010,00    | 31-01-2017 |
| CC002       | Financiën      | SC-CC002 | Financiën         | 17.735,00\- | 31-01-2017 |
| CC003       | Assembleren     | SC-CC002 | Financiën         | 11.527,75   | 31-01-2017 |
| CC004       | Verpakking    | SC-CC002 | Financiën         | 6.207,25    | 31-01-2017 |

Nadat de **Overheadberekening** is voltooid, kunt u de resultaten rapporteren met behulp van programma's zoals Microsoft SharePoint Workspace, Excel of Power BI.

## <a name="view-reporting-in-excel"></a>Rapportage in Excel weergeven 

Met de dimensiehiërarchieën kunt u gegevens weergeven op verschillende samenvoegingsniveaus.

Hier volgt een voorbeeld van een Power Pivot-rapportage in Excel.

| **Winst- en verliesrekening** | **Kostenobject** |      &nbsp;    |   &nbsp;      |     &nbsp;    |  **Totaal**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Primaire kosten**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| 1001&nbsp;&nbsp;&nbsp;&nbsp;                            | 100,00          | 200.000         | 6.000,00      | 2.000,00      | **8.300,00**  |
| 1002&nbsp;&nbsp;&nbsp;&nbsp;                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|1003&nbsp;&nbsp;&nbsp;&nbsp;                             | 0.00            | 4.000,00       | 0.00          | 0.00          | **4.000,00**  |
|**Secundaire kosten**                            | **-10.100,00**  | **-14.200,00** | **17.082.75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | 10.100,00\-     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0.00            | 17.735,00\-    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0.00            | 0.00           | 0.00          | 0.00          | 0.00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0.00            | 0.00           | 0.00          | 0.00          | 0.00          |
| **Totaal**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Met behulp van **Beleid voor totalisering van kosten** en **Kostenelementen van het type secundaire** kunt u de primaire kosten per kostenobject voor interne rapportage laten als de primaire kosten die overblijven na **Overheadberekening**.

Als hetzelfde voorbeeld zou zijn uitgevoerd zonder het **Beleid voor totalisering van kosten** te maken, zou het rapportageresultaat zijn zoals hieronder wordt weergegeven. De kostenstromen zijn correct, maar de traceerbaarheid en het inzicht in hoe kosten stromen tussen de kostenplaatsen gaan verloren.

| **Winst- en verliesrekening** | **Kostenobject** |   &nbsp;  |    &nbsp;     |  &nbsp;       |          **Totaal**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Primaire kosten**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|1001&nbsp;&nbsp;&nbsp;&nbsp;                              | 0.00            | 0.00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| 1002&nbsp;&nbsp;&nbsp;&nbsp;                             | 0.00            | 0.00      | 22.275,00     | 12.225,00     | **34.500,00** |
|1003&nbsp;&nbsp;&nbsp;&nbsp;                              | 0.00            | 0.00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Secundaire kosten**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0.00            | 0.00      | 0.00          | 0.00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0.00            | 0.00      | 0.00          | 0.00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0.00            | 0.00      | 0.00          | 0.00          | 0.00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0.00            | 0.00      | 0.00          | 0.00          | 0.00          |
| **Totaal**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Afhankelijk van de rapportage- en traceerbaarheidsvereisten in uw organisatie kunt u het juiste niveau bepalen van secundaire kostenelementen en regels voor kostentotalisering maken die passen bij uw behoeften.

De duidelijke scheiding tussen **Kostentoewijzing** en **Beleid voor totalisering van kosten** biedt de flexibiliteit om voortdurend updates uit te voeren zonder elkaar te beïnvloeden.



## <a name="additional-resources"></a>Aanvullende resources
-  [Dimensies van kostenobject](cost-objects.md)
-  [Dimensies van kostenelement](cost-elements.md)
-  [Dimensiehiërarchie](dimension-hierarchy.md)
-  [Overheadberekening](overhead-calculation.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
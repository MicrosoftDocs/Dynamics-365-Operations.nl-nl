---
title: Boekdefinities
description: Dit artikel bevat voorbeelden die laten zien hoe boekdefinities worden gebruikt voor vorderingen van inkooporders en budgettoewijzingen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5fb08a86639e9a9a79dca5fc1200e73e5870432
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564688"
---
# <a name="posting-definition-examples"></a>voorbeelden van boekdefinities

[!include [banner](../includes/banner.md)]

Dit artikel bevat voorbeelden die laten zien hoe boekdefinities worden gebruikt voor vorderingen van inkooporders en budgettoewijzingen.

Voordat u dit onderwerp leest, moet u vertrouwd zijn met de boekingsdefinities en transactieboekingsdefinities. Meer informatie vindt u onder [Boekdefinities](posting-definitions.md). De volgende voorbeelden kunnen worden ingesteld op de pagina **Boekdefinities**. Elk voorbeeld bevat deze secties:

-   Boekdefinitie – Matchcriteria
-   Boekingsdefinitie – Gegenereerde vermeldingen
-   Transacties met de rekeningen dimensiewaarden en bedragen
-   Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd

Wanneer er een match is tussen de rekeningen en dimensiewaarden in het deelvenster **Criteria voor overeenkomst** voor de boekdefinitie en de rekeningen en dimensiewaarden in de transactie, worden er grootboekboekingen gegenereerd op basis van het deelvenster **Gegenereerde vermeldingen** voor de boekdefinitie. 
> [!NOTE]
> Gebruik de pagina **Boekdefinities voor transacties** om een boekdefinitie aan een specifiek transactietype te koppelen. Nadat u een boekdefinitie aan een transactietype hebt gekoppeld en **Boekdefinities gebruiken** hebt geselecteerd op de pagina **Grootboekparameters**, moeten alle transacties van het geselecteerde transactietype gebruikmaken van boekdefinities.

## <a name="example-purchase-order-encumbrances"></a>Voorbeeld: Vorderingen van inkooporders
Wanneer u de verwerking van vorderingen inschakelt door **Vorderingsproces inschakelen** te selecteren op de pagina **Grootboekparameters**, moeten boekdefinities worden gebruikt om vorderingen in het grootboek te registreren voor rekeningen die moeten worden gereserveerd. In de meeste gevallen worden alle onkostenrekeningen op de balans gereserveerd. 

Boekdefinities voor vorderingen worden ingesteld voor de module **Inkoop** op de pagina **Boekdefinities**. Daarna kunt u in het gebied **Inkoop** van de pagina **Boekdefinities voor transacties** het transactietype **Inkooporder** selecteren om de boekdefinitie aan inkooporders te koppelen. 

Alle boekstuktransacties voor inkoopordervorderingen moeten in evenwicht zijn (met andere woorden, debet moet gelijk zijn aan credit) in elke unieke dimensie op een boekstuk.

### <a name="posting-definition--match-criteria"></a>Boekdefinitie – Matchcriteria

| Rekeningstructuur       | Rekeningnummerovereenkomst | Prioriteit  |
|-------------------------|----------------------|----------|
| Rekeningstructuur - W&V | \*                   | 1        |

<em>Een lege waarde in het veld **Vereffeningsrekeningnummer</em>* betekent dat alle overeenkomende rekeningen in de gedefinieerde rekeningstructuur deel uitmaken van de afstemmingsregel.

### <a name="posting-definition--generated-entries"></a>Boekingsdefinitie – Gegenereerde vermeldingen

| Rekeningstructuur | Gegenereerd rekeningnummer                    | Gegenereerd debet/credit |
|-------------------|---------------------------------------------|------------------------|
| Saldo           | 300143 - -(vorderingsrekening)             | Zelfde                   |
| Saldo           | 300144 - -(reserveren voor vorderingsrekening) | Balanceren              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transacties met de rekeningen dimensiewaarden en bedragen

De rekeningen en dimensiewaarden zijn afkomstig van de boekhoudingsverdelingen die u invoert voor een inkooporderregel of zijn afkomstig van de rekeningen en dimensies die automatisch worden gegenereerd op basis van de standaardinstellingen voor leveranciers, artikelen, categorieën en dimensiesjablonen.

| Rekening + dimensies           | Debet  | Krediet | Opmerking |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Training | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd

Grootboekboekingen worden gemaakt om de vorderingen te registreren.

| Rekening + dimensies           | Debet  | Krediet | Opmerking |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Training | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-Training |        | 250,00 |         |

In dit voorbeeld komt elke rekening die onderdeel is van de Rekeningstructuur - W&V overeen met de criteria van de boekdefinitie. Wanneer dus 606500-OU\_1-OU\_3566-Training wordt beoordeeld, worden gegenereerde boekingen gemaakt voor de rekeningen die in het deelvenster **Gegenereerde vermeldingen** voor de boekdefinitie zijn gedefinieerd.

## <a name="example-budget-appropriations"></a>Voorbeeld: Budgettoewijzingen
Wanneer u budgettoewijzingen inschakelt door **Aanwending van budget inschakelen** te selecteren op de pagina **Grootboekparameters**, moeten boekdefinities worden gebruikt om budgetregistervermeldingen te registeren in het grootboek. Wanneer een budgetbeheerconfiguratie actief is en is ingeschakeld, kunnen boekdefinities en transactieboekdefinities worden gebruikt om de registratie van toewijzingen, revisies, overboekingen, projecten, vaste activa en prognoseboekingen voor vraag en aanbod in het grootboek te ondersteunen. 

U kunt een boekdefinitie voor budgetregisterregels die een budgettype **Oorspronkelijk budget** hebben en waarvoor toewijzingen zijn ingeschakeld, instellen door de module **Budget** te selecteren op de pagina **Boekdefinities**. Vervolgens kunt u in het gebied **Budget** van de pagina **Boekdefinities van transacties** budgetcodes gebruiken om de boekdefinitie te koppelen aan budgetregisterregels met een budgettype **Oorspronkelijk budget**. 

Wanneer budgettoewijzingen en boekdefinities zijn ingeschakeld, worden de budgetregisterregels geregistreerd voor budgetbeheer en in het grootboek.

### <a name="posting-definition--match-criteria"></a>Boekdefinitie – Matchcriteria

| Rekeningstructuur       | Rekeningnummerovereenkomst | Prioriteit  |
|-------------------------|----------------------|----------|
| Rekeningstructuur - W&V | \*                   | 1        |

<em>Een lege waarde in het veld **Vereffeningsrekeningnummer</em>* betekent dat alle overeenkomende rekeningen in de gedefinieerde rekeningstructuur deel uitmaken van de afstemmingsregel.

### <a name="posting-definition--generated-entries"></a>Boekingsdefinitie – Gegenereerde vermeldingen

| Rekeningstructuur | Gegenereerd rekeningnummer              | Gegenereerd debet/credit |
|-------------------|---------------------------------------|------------------------|
| Rekeningstructuur | 300145 - -(geschatte opbrengstrekening) | Zelfde                   |
| Rekeningstructuur | 300146 - -(toewijzingsrekening)     | Balanceren              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transacties met de rekeningen dimensiewaarden en bedragen

U voert de rekeningen, dimensiewaarden en bedragen voor de budgetjournaalregel in op de pagina **Budgetregisterpost**.

| Rekening + dimensies           | Debet | Krediet | Opmerking |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Training |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Grootboekvermeldingen die op basis van de boekdefinitie zijn gegenereerd

Gegenereerde grootboekboekingen worden gemaakt om het oorspronkelijke budget in elke dimensie te registreren.

| Rekening + dimensies           | Debet  | Krediet | Opmerking |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Training |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-Training | 250,00 |        |         |

In dit voorbeeld komt elke rekening die onderdeel is van de Rekeningstructuur - W&V overeen met de criteria van de boekdefinitie. Daarom worden de gegenereerde grootboekboekingen gemaakt wanneer 606400-OU\_1-OU\_3566-Training wordt beoordeeld.






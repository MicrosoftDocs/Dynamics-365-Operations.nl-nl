---
title: Formuleontwerper voor TDS-berekeningen
description: In dit onderwerp wordt een voorbeeld beschreven van hoe TDS (Tax Ducted at Source, belasting ingehouden op bron) wordt berekend op basis van de formule die is gedefinieerd voor elke TDS-belastingcode in de TDS-groep die aan de transactie is gekoppeld.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d0f644da640b56761a52baec9ff01c898e895d19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023139"
---
# <a name="formula-designer-for-tds-calculations"></a>Formuleontwerper voor TDS-berekeningen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een voorbeeld gegeven van hoe TDS (Tax Ducted at Source, belasting ingehouden op bron) wordt berekend op basis van de formule die voor elke TDS-belastingcode is gedefinieerd. TDS-belastingcodes worden gedefinieerd in de TDS-groep die aan de transactie is gekoppeld. Voordat u TDS-formules ontwerpt, moet u de basisinstellingen voor TDS voltooien, zoals wordt vermeld in de volgende stappen. 

- Stel TDS-componentgroepen in met de pagina **Componentgroepen voor bronbelasting**. 
- Stel TDS-componenten in en koppel de TDS-componentgroep aan de TDS-componenten met de pagina **Bronbelastingcomponenten**. 
- Stel TDS-belastingcodes in en koppel de TDS-componenten aan de belastingcodes met de pagina **Bronbelastingcodes**. 
- Stel TDS-belastinggroepen in met de pagina **Bronbelastinggroepen**. Koppel vervolgens de TDS-belastingcodes aan de belastinggroep en definieer de formule met de pagina **Formuleontwerper**. 

**Voorbeeld van formule**

In dit voorbeeld is de TDS-groep Huur gekoppeld aan een inkoopfactuur die voor leverancier A is gemaakt. Het factuurbedrag is $ 100.000. Zie de volgende tabel voor de TDS-berekening voor de factuur.

| TDS-groep                                                   | TDS-belastingcodes die aan de TDS-groep zijn gekoppeld | Waarde              | Belastbare basis (Formuleontwerper) | Berekeningsexpressie (Formuleontwerper) | Basisbedrag | Berekend TDS-bedrag |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Huur                                                         | TDS (TDS-component - TDS)                | 10%                | Brutobedrag                      |                                            | 100,000      | 10,000                 |
| Toeslag (TDS-component - Toeslag)                         | 10%                                     | Excl. brutobedrag | +TDS                              |                   10000                    | 1.000        |                       |
| PE-Cess (TDS-component - PE-Cess)                            | 2%                                      | Excl. brutobedrag | +TDS+Toeslag                    |                   11000                    | 220         |                       |
| SHE Cess (TDS-component - SHE Cess)                          | 1%                                      | Excl. brutobedrag | +TDS+Toeslag                    |                   11000                    | 110         |                       |
| **Totale** **TDS**  **die** **voor** **de** **factuur is berekend** | **11,330**                               |                    |                                   |                                            |             |                       |

De boekstukposten worden als volgt gemaakt.

| Rekening           | Debet  | Krediet |
| ----------------- | ------ | ------ |
| Huur              | 100,000 |        |
| Leverancier A          |        | 100,000 |
| Leverancier A          | 11,330  |        |
| TDS te betalen       |        | 10,000  |
| Toeslag te betalen |        | 1.000   |
| PE-Cess te betalen   |        | 220    |
| SHE Cess te betalen  |        | 110    |

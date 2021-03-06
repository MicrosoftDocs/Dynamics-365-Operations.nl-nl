---
title: Een inkooporder maken die wordt geregeld door een budget
description: Via deze procedure kunt u een inkooporder maken die is gecontroleerd op beschikbaar budget.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a79b19ce4ff35ecc1f691edea1bdc5e30010b433
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821364"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Een inkooporder maken die wordt geregeld door een budget

[!include [banner](../../includes/banner.md)]

Via deze procedure kunt u een inkooporder maken die is gecontroleerd op beschikbaar budget. Deze registratie gebruikt het USMF-demogegevensbedrijf.


## <a name="review-the-budget-control-configuration"></a>De budgetbeheerconfiguratie controleren
1. Ga naar Budgettering > Instelling > Budgetbeheer > Configuratie budgetbeheer.
2. Klik op het tabblad Beschikbare budgetfondsen.
3. Klik op het tabblad Documenten en journalen.
4. Klik op het tabblad Regels voor budgetbeheer definiëren.
5. Klik op het tabblad Budgetgroepen definiëren.
6. Sluit de pagina.

## <a name="create-the-purchase-order-header"></a>De koptekst van de inkooporder maken
1. Ga naar Inkoop en sourcing > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Leveranciersrekening.
4. Vouw de sectie Algemeen uit.
5. Stel in het veld Boekingsdatum de datum in op '2016-01-01'.
6. Klik op OK.

## <a name="add-a-purchase-order-line"></a>Een inkooporderregel toevoegen
1. Typ of selecteer een waarde in het veld Aanschaffingscategorie.
2. Stel Hoeveelheid in op '2'.
3. Typ of selecteer een waarde in het veld Eenheid.
4. Stel Eenheidsprijs in op '10000'.
5. Klik op Financiële items.
6. Klik op Bedragen verdelen.
7. Geef in het veld Grootboekrekening de waarde '601300-001-023--' op.
8. Sluit de pagina.

## <a name="perform-budget-checking"></a>Budgetcontrole uitvoeren
1. Klik op Financiële items.
2. Klik op Budgetcontrole uitvoeren.
3. Klik op Financiële items.
4. Klik op Fouten of waarschuwingen van budgetcontrole.
5. Klik op Sluiten.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
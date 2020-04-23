---
title: Een inkooporder maken die wordt geregeld door een budget
description: Via deze procedure kunt u een inkooporder maken die is gecontroleerd op beschikbaar budget.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa16955e0ea407555c7b52b0af37c5891be9bdbb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214280"
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


---
title: Een inkooporder maken die wordt geregeld door een budget
description: Via deze procedure kunt u een inkooporder maken die is gecontroleerd op beschikbaar budget.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016183"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Een inkooporder maken die wordt geregeld door een budget

[!include [banner](../../includes/banner.md)]

Via deze procedure kunt u een inkooporder maken die is gecontroleerd op beschikbaar budget.

## <a name="review-the-budget-control-configuration"></a>De budgetbeheerconfiguratie controleren

1. Ga naar **Budgettering > Instelling > Budgetbeheer > Configuratie budgetbeheer**.
1. Selecteer het tabblad **Beschikbare budgetfondsen**.
1. Selecteer het tabblad **Documenten en journalen**.
1. Selecteer het tabblad **Regels voor budgetbeheer definiëren**.
1. Selecteer het tabblad **Budgetgroepen definiëren**.
1. Sluit de pagina.

## <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Inkoop en sourcing > Inkooporders > Alle inkooporders**.
1. Selecteer **Nieuw**.
1. In het veld **Leveranciersrekening** typt of selecteert u een waarde.
1. Vouw de het sneltabblad **Algemeen**.
1. Stel in het veld **Boekingsdatum** de datum in.
1. Selecteer **OK** om het dialoogvenster te sluiten en de nieuwe inkooporder te openen.
1. Selecteer op het sneltabblad **Inkooporderregels** de optie **Regel toevoegen** op de werkbalk om een nieuwe regel toe te voegen en de regel zo nodig in te vullen om een artikel aan de order toe te voegen.
1. Selecteer **Financiële items \> Bedragen verdelen** op de werkbalk van het sneltabblad **Inkooporderregels**.
1. Geef een rekening op in het veld **Grootboekrekening**.
1. Sluit de pagina.

## <a name="perform-budget-checking"></a>Budgetcontrole uitvoeren

1. Ga verder met de inkooporder waar u zojuist een regel aan hebt toegevoegd.
1. Selecteer **Financiële items \> Budgetcontrole uitvoeren** op de werkbalk van het sneltabblad **Inkooporderregels**.
1. Selecteer **Financiële items \> Fouten of waarschuwingen van budgetcontrole** op de werkbalk van het sneltabblad **Inkooporderregels**.
1. Het dialoogvenster **Fouten of waarschuwingen van budgetcontrole** wordt geopend. Controleer de resultaten van de controle en selecteer **Sluiten** om het dialoogvenster te sluiten.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
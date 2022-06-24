---
title: Uitgaande zendingen vanuit batchtaken bevestigen
description: In dit artikel wordt beschreven hoe u een batchtaak instelt waarmee automatisch uitgaande overboekingsorderzendingen worden bevestigd voor ladingen die gereed zijn om te verzenden.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875096"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Uitgaande zendingen vanuit batchtaken bevestigen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een batchtaak instelt waarmee automatisch uitgaande overboekingsorderzendingen worden bevestigd voor ladingen die gereed zijn om te verzenden. De batchtaak die hier wordt beschreven, is alleen van toepassing op overboekingsorders, niet op verkooporders.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>De functie Uitgaande zendingen vanuit batchtaken bevestigen in- of uitschakelen

Als u de functionaliteit wilt gebruiken die in dit artikel wordt beschreven, moet de functie *Uitgaande zendingen vanuit batchtaken bevestigen* zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Uitgaande zendingen vanuit batchtaken bevestigen* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="process-outbound-shipments"></a>Uitgaande zendingen verwerken

Een geplande batchtaak instellen voor het uitvoeren van de bevestiging van de uitgaande zending voor ladingen die gereed zijn voor verzending:

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Uitgaande zendingen verwerken**.
1. Het dialoogvenster **Verzending bevestigen** wordt geopend. Selecteer **Filter** op het sneltabblad **Op te nemen records**.
1. Het dialoogvenster Query-editor wordt geopend. Voeg op het tabblad **Bereik** een rij met de volgende waarden toe.
    - **Tabel** - *Ladingen*
    - **Afgeleide tabel** - *Ladingen*
    - **Veld** - *Status lading*
    - **Criteria** - *Geladen*
1. Selecteer **OK** om terug te gaan naar het dialoogvenster **Verzending bevestigen**.
1. Stel op het sneltabblad **Op de achtergrond uitvoeren** **Batchverwerking** in op **Ja**.
1. Selecteer op het tabblad **Op de achtergrond uitvoeren** de optie **Terugkeer**.
1. Het dialoogvenster **Terugkeerpatroon definiëren** wordt geopend. Stel het uitvoeringsschema in voor uw bedrijf.
1. Selecteer **OK** om terug te gaan naar het dialoogvenster **Verzending bevestigen**.
1. Selecteer **OK** in het dialoogvenster **Verzending bevestigen** om de batchtaak aan de batchwachtrij toe te voegen.

Zie voor meer informatie [Overzicht van batchverwerking](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
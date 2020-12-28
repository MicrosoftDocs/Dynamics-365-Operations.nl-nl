---
title: Uitgaande zendingen vanuit batchtaken bevestigen
description: In dit onderwerp wordt beschreven hoe u een batchtaak instelt waarmee automatisch uitgaande transferorderzendingen worden bevestigd voor ladingen die gereed zijn om te verzenden.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425208"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Uitgaande zendingen vanuit batchtaken bevestigen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een batchtaak instelt waarmee automatisch uitgaande transferorderzendingen worden bevestigd voor ladingen die gereed zijn om te verzenden. De batchtaak die hier wordt beschreven, is alleen van toepassing op transferorders, niet op verkooporders.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Schakel de functie Uitgaande zendingen vanuit batchtaken bevestigen in

Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem. Beheerders kunnen gebruikmaken van de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen. U ziet de functie als:

- **Module** - *Magazijnbeheer*
- **Functienaam** - *Uitgaande zendingen vanuit batchtaken bevestigen*

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

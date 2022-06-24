---
title: Asynchrone klanten converteren naar synchrone klanten
description: In dit artikel wordt uitgelegd hoe u asynchrone klanten converteert naar synchrone klanten in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 0ce4906816deab8824b1079a34489e55651c0e03
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884386"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asynchrone klanten converteren naar synchrone klanten

[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe u asynchrone klanten converteert naar synchrone klanten in Microsoft Dynamics 365 Commerce.

Ga als volgt te werk om asynchrone klanten te converteren naar synchrone klanten.

1. Voer in Commerce Headquarters de **P-taak** uit om de asynchrone klanten naar Commerce Headquartes te verzenden.
1. Voer de taak **Klanten en zakenpartner synchroniseren vanuit de asynchrone modus** uit om klantrekening-id's te maken. (Deze taak had voorheen de taak **Klanten en zakenpartners synchroniseren vanuit de asynchrone modus**.)
1. Voer de taak **1010** uit om de nieuwe klantrekening-id's te synchroniseren met de afzetkanalen.

Als een order verwijst naar een asynchrone klant of een adres dat nog niet is gesynchroniseerd met Commerce Headquarters, wordt de klant of het adres gesynchroniseerd als onderdeel van de batchtaak **Orders synchroniseren**. Als een contante transactie verwijst naar een asynchrone klant of een asynchroon adres, wordt de klant of het adres gesynchroniseerd vóór de EOD-boeking (end-of-day).

## <a name="additional-resources"></a>Aanvullende bronnen

[Klantbeheer in winkels](customer-mgmt-stores.md)

[Modus voor het maken van asynchrone klanten](async-customer-mode.md)

[Klantkenmerken](dev-itpro/customer-attributes.md)

[Uitsluiting van offlinegegevens](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

---
title: Intercompany-handel instellen
description: In dit onderwerp wordt beschreven hoe u intercompany-handel instelt
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 75d6679152a056f6883658911f93464252e5fe87
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548183"
---
# <a name="set-up-intercompany-trade"></a>Intercompany-handel instellen

[!include [banner](../../includes/banner.md)]

Als u intercompany-handel in Microsoft Dynamics 365 Supply Chain Management wilt uitvoeren, moet u eerst klanten en leveranciers instellen. U moet ook Leveranciers, Klanten, Inkoopbeheer en Verkoop en marketing instellen.

## <a name="before-you-set-up-intercompany-trade"></a>Voordat u intercompany-handel instelt

Voordat u intercompany-handel instelt, moet u bepalen welke van uw klanten intercompany-klanten zijn en welke van uw leveranciers intercompany-leveranciers zijn. Voor elke rechtspersoon in Microsoft Dynamics 365 Supply Chain Management moet u beslissen welk handelsbeleid moet worden toegepast op de intercompany-handelsrelatie met de specifieke intercompany-klant of -leverancier.

U wordt aangeraden om uzelf en uw organisatie vertrouwd te maken met de intercompany-parameters.

- Bespreek de gevolgen van de instellingen met de beheerders die verantwoordelijk zijn voor de intercompany-handel in elke rechtspersoon.
- Stel de juiste waarden voor elke rechtspersoon in.

## <a name="set-up-trading-relations"></a>Handelsrelaties instellen

Ga als volgt te werk om intercompany-handel in te stellen voor klanten en leveranciers.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Een klantrekening selecteren.
1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Intercompany**.
1. Geef instellingen voor intercompany-parameters op voor de klantrekening. Deze parameters omvatten de rechtspersoon die de desbetreffende leverancier en de leveranciersrekening bevat. De parameters omvatten ook het inkooporderbeleid, het verkooporderbeleid, de waardetoewijzing en het beleid voor verkoop- en inkoopovereenkomsten. U geeft ook op of de waarden van de basisgegevens van de klantrekening of van de leveranciersrekening in de andere rechtspersoon gebruikt moeten worden.
1. Herhaal de stappen 1 tot en met 4 voor de overige intercompany-klanten in de rechtspersoon.
1. Ga naar **Leveranciers \> Leveranciers \> Alle leveranciers**.
1. Selecteer een leveranciersrekening.
1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Intercompany**.
1. Geef instellingen voor intercompany-parameters op voor de leveranciersrekening. Deze parameters omvatten de rechtspersoon die de desbetreffende klant en klantrekening bevat. De parameters omvatten ook het beleid voor verkooporders en inkooporders, de waardetoewijzing en het beleid voor inkoop- en verkoopovereenkomsten. U geeft ook op of de waarden van de basisgegevens van de leveranciersrekening of van de klantrekening in de andere rechtspersoon gebruikt moeten worden.
1. Herhaal de stappen 6 tot en met 9 voor de overige intercompany-leveranciers in de rechtspersoon.

## <a name="set-up-products"></a>Producten instellen

Ga als volgt te werk om intercompany-handel in te stellen voor klanten en leveranciers.

1. Ga naar **Productgegevensbeheer \> Producten \> Alle producten en productmodellen**.
1. Definieer de producten die worden vrijgegeven aan de rechtspersonen waarmee u intercompany-handel wilt doen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

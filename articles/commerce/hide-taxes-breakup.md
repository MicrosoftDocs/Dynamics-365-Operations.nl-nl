---
title: Informatie over btw-opsplitsing verbergen in orderoverzichten
description: In dit onderwerp wordt beschreven hoe u informatie over btw-opsplitsing kunt verbergen in overzichten voor winkelwagens, uitchecken, orderbevestiging en orderdetailpagina's in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645215"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Informatie over btw-opsplitsing verbergen in orderoverzichten

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u informatie over btw-opsplitsing kunt verbergen in overzichten voor winkelwagens, uitchecken, orderbevestiging en orderdetailpagina's in Microsoft Dynamics 365 Commerce.

Standaard worden in Dynamics 365 Commerce informatie over btw-opsplitsing weergegeven in overzichten voor winkelwagens, uitchecken, orderbevestiging en orderdetailpagina's. Vanaf Commerce versie 10.0.27 bevat Commerce Site Builder een optie waarmee u de informatie over btw-opsplitsing kunt verbergen in orderoverzichten.

In de volgende afbeelding ziet u een voorbeeld van twee orderoverzichten. Het eerste geeft informatie over btw-opsplitsing weer, en het tweede verbergt deze.

![Voorbeelden van winkelwagens met informatie over btw-opsplitsing weergegeven en verborgen.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - De optie om informatie over btw-opsplitsing in orderoverzichten te verbergen is alleen beschikbaar wanneer de optie **Prijzen inclusief btw** voor het e-commercekanaal is ingesteld op **Ja** in Commerce Headquarters bij **Retail en commerce \> Kanalen \> Winkels \> Alle winkels**. 
> - Standaard is de optie **Btw-opsplitsing weergeven in orderoverzicht** ingeschakeld in Site Builder.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Informatie over btw-opsplitsing verbergen in orderoverzichten

Volg deze stappen om de informatie over btw-opsplitsing te verbergen in orderoverzichten

1. Ga in Commerce Site Builder naar de site die u wilt bijwerken.
1. Ga naar **Vestigingsinstellingen \> Uitbreidingen**.
1. Wis het selectievakje **Btw-opsplitsing weergeven in orderoverzicht**.

Als u informatie over btw-opsplitsing in orderoverzichten wilt bekijken, schakelt u het selectievakje **Btw-opsplitsing weergeven in orderoverzicht** in.  

In de volgende afbeelding ziet u een voorbeeld van het selectievakje **Btw-opsplitsing weergeven in orderoverzicht** dat is gemarkeerd en is ingeschakeld in Site Builder.

![De optie Btw-opsplitsing weergeven in orderoverzicht in Site Builder.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Btw-overzicht](/finance/general-ledger/indirect-taxes-overview)

[Btw voor online orders configureren](sales-tax-config.md)

[Problemen oplossen: De btw op online orders wordt onjuist berekend](troubleshoot/tax-miscalculated-online-order.md)

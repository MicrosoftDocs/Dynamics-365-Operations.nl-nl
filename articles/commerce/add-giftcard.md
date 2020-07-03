---
title: Geschenkbonmodule
description: In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a8428963e105e422dcd048863c17df0926a409ac
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411107"
---
# <a name="gift-card-module"></a>Geschenkbonmodule

[!include [banner](includes/banner.md)]

In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Geschenkbonnen vormen een algemene betalingswijze en de geschenkbonmodule kan in een kassamodule worden gebruikt om geschenkbonnen te accepteren. De geschenkbonmodule ondersteunt Dynamics 365, SVS en Givex-geschenkbonnen. SVS- en Givex geschenkbonnen worden ingewisseld via de Adyen-betalingsprovider.

Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) voor meer informatie over ondersteuning voor externe geschenkbonnen, zoals SVS en Givex.

De volgende afbeelding toont een voorbeeld van een geschenkbonmodule op een betalingspagina.

![Voorbeeld van een geschenkbonmodule](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Module-eigenschappen

- **Extra velden weergeven**: met deze eigenschap wordt gedefinieerd welke velden voor geschenkbonnen moeten worden weergegeven naast het nummer van de geschenkbon, dat altijd standaard wordt weergegeven. Sommige geschenkbonnen ondersteunen bijvoorbeeld het weergeven van een persoonlijk identificatienummer (PIN) en andere bieden ondersteuning voor het weergeven van een pincode en een vervaldatum. Het kan ook zijn dat deze eigenschap is ingesteld op "Geen", zodat alleen het nummer van de geschenkbon en geen extra velden worden weergegeven.

Ondersteunde waarden:
-   Pincode
-   Vervaldatum
-   PIN en vervaldatum 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Site-instellingen voor geschenkbonmodules

In Commerce Site Builder onder **Site-instellingen \> Uitbreidingen** is er een geschenkbonmodule met de naam **Ondersteund geschenkbontype**. Deze instelling ondersteunt drie waarden:
- **Dynamics 365-geschenkbon**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-geschenkbonnen worden ingewisseld. Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.
- **SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er SVS- en Givex-geschenkbonnen worden ingewisseld. Deze instelling wordt alleen ondersteund voor aangemelde en anonieme gebruikers op de e-Commerce-site.
- **Dynamics 365-, SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-, SVS- en Givex-geschenkbonnen worden ingewisseld. Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.

## <a name="add-a-gift-card-module-to-a-page"></a>Een geschenkbonmodule toevoegen aan een pagina

Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een geschenkbonmodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht starterskit](starter-kit-overview.md)

[Kassamodule](add-checkout-module.md)

[Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md)

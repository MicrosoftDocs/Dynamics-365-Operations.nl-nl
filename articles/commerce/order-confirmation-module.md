---
title: Orderbevestigingsmodule
description: In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698321"
---
# <a name="order-confirmation-module"></a>Orderbevestigingsmodule

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Er wordt een orderbevestigingsmodule gebruikt om een bevestigingsbericht weer te geven op de pagina orderbevestiging nadat een order is geplaatst. In de orderbevestigingsmodule wordt het nummer van de orderbevestiging en het e-mailadres van de klant weergegeven dat tijdens het uitchecken is opgegeven.

Wanneer een order tijdens het uitchecken wordt geplaatst, worden het orderbevestigingsnummer en het e-mailadres van de klant doorgegeven aan de orderbevestigingspagina als een queryreeks in de URL van de pagina. De orderbevestigingsmodule ontvangt deze informatie en geeft de orderstatus weer op de orderbevestigingspagina. De orderbevestigingsmodule vereist deze paginacontext om de status van de order op te geven.

## <a name="order-confirmation-module-properties"></a>Eigenschappen van orderbevestigingsmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Koptekst       | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | De orderbevestigingsmodule kan een koptekst hebben. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Modules die kunnen worden gebruikt in de pagina van de orderbevestigingsmodule 

- **Aanbevelingen**: de aanbevelingsmodule kan op de orderbevestigingspagina worden geplaatst om andere producten voor te stellen aan de klant.
- **Marketing** : de module marketing kan marketinginhoud toevoegen aan de pagina orderbevestiging.

## <a name="create-an-order-confirmation-page-module"></a>Een module voor de orderbevestigingspagina maken

1. Maak een paginasjabloon met de naam **orderbevestigingssjabloon**.
1. Voeg in het **hoofdvak** van de standaardpagina een orderbevestigingsmodule toe.
1. Voeg in de module orderbevestiging een aanbevelingsmodule toe.
1. Sla de sjabloon op en bekijk een voorbeeld. De orderbevestigingsmodule kan niet worden weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.
1. Check de sjabloon in en publiceer deze.
1. Gebruik de orderbevestigingssjabloon die u zojuist hebt gemaakt om een pagina met de naam **Orderbevestigingspagina** te maken.
1. Voeg de standaardpagina toe aan het paginaoverzicht.
1. Voeg in het vak **Koptekst** een koptekstfragment toe.
1. Voeg in het vak **Voettekst** een voettekstfragment toe.
1. Voeg in het **hoofdvak** een orderbevestigingsmodule toe.
1. Voeg in het eigenschappenvenster van de orderbevestigingsmodule de kop **Orderbevestiging** toe.
1. Voeg onder de orderbevestigingsmodule een aanbevelingsmodule toe en configureer deze zo dat de instellingen **Nieuw** en **Best verkocht** worden gebruikt.
1. Sla de pagina op, geef een voorbeeld weer, check in en publiceer de pagina.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)

---
title: Module voor orderdetails
description: In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026012"
---
# <a name="order-details-module"></a>Module voor orderdetails


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De module voor orderdetails wordt gebruikt om orderbevestigingsdetails weer te geven nadat een order is geplaatst. De id van de orderbevestiging, de contactgegevens van de order en andere ordergegevens worden weergegeven, zoals de gekochte artikelen, betalingsgegevens en verzendmethode.

## <a name="order-confirmation-module-properties"></a>Eigenschappen van orderbevestigingsmodule

| Naam van eigenschap.  | Waarden | Beschrijving |
|----------------|--------|-------------|
| Koptekst        | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | De orderbevestigingsmodule kan een koptekst hebben. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |
| Contactnummer | Text | Er kan een contactnummer worden opgegeven voor vragen met betrekking tot de order. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Modules die kunnen worden gebruikt op een pagina met orderdetails

Wanneer u een pagina met orderdetails maakt, kunt u behalve de module voor orderdetails ook andere relevante modules toevoegen. Hieronder volgen een aantal voorbeelden:

- **Aanbevelingsmodule**: de aanbevelingsmodule kan aan de pagina met orderdetails worden toegevoegd om suggesties voor andere producten te doen aan de klant.
- **Marketingmodules**: elke marketingmodule kan worden toegevoegd aan de pagina met orderdetails om marketinginhoud weer te geven.

## <a name="create-an-order-details-page-module"></a>Een module voor de pagina met orderdetails maken

1. Maak een paginasjabloon met de naam **Sjabloon voor orderdetails**.
1. Voeg in het **hoofdvak** van de standaardpagina een module voor orderdetails toe.
1. Voeg in de module orderdetails een aanbevelingsmodule toe.
1. Sla de sjabloon op en bekijk een voorbeeld. De module voor orderdetails wordt niet weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.
1. Voltooi het bewerken van de sjabloon en publiceer deze.
1. Gebruik de sjabloon voor orderdetails die u zojuist hebt gemaakt om een pagina met de naam **Pagina met orderdetails** te maken.
1. Voeg de standaardpagina toe aan het paginaoverzicht.
1. Voeg in het vak **Koptekst** een koptekstfragment toe.
1. Voeg in het vak **Voettekst** een voettekstfragment toe.
1. Voeg in het **hoofdvak** een module voor orderdetails toe.
1. Voeg in het eigenschappenvenster van de module voor orderdetails de kop **Orderdetails** toe.
1. Voeg onder de module voor orderdetails een aanbevelingsmodule toe en configureer deze zo dat de instellingen **Nieuw** en **Best verkocht** worden gebruikt.
1. Sla de pagina op en bekijk een voorbeeld.
1. Voltooi het bewerken van de pagina en publiceer deze.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)

---
title: Module voor orderdetails
description: In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464925"
---
# <a name="order-details-module"></a>Module voor orderdetails


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De module voor orderdetails wordt gebruikt om orderbevestigingsdetails weer te geven nadat een order is geplaatst. De id van de orderbevestiging, de contactgegevens van de order en andere ordergegevens worden weergegeven, zoals de gekochte artikelen, betalingsgegevens en verzendmethode.

## <a name="order-details-module-properties"></a>Eigenschappen van module voor orderdetails

| Naam van eigenschap.  | Waarden | Omschrijving |
|----------------|--------|-------------|
| Kop        | Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**) | De module voor orderdetails kan een koptekst hebben. Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst. De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen. |
| Contactnummer | Text | Er kan een contactnummer worden opgegeven voor vragen met betrekking tot de order. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Modules die kunnen worden gebruikt op een pagina met orderdetails

Wanneer u een pagina met orderdetails maakt, kunt u behalve de module voor orderdetails ook andere relevante modules toevoegen. Hieronder volgen een aantal voorbeelden:

- **Aanbevelingsmodule**: de aanbevelingsmodule kan aan de pagina met orderdetails worden toegevoegd om suggesties voor andere producten te doen aan de klant.
- **Marketingmodules**: elke marketingmodule kan worden toegevoegd aan de pagina met orderdetails om marketinginhoud weer te geven.

## <a name="add-an-order-details-module-to-a-page"></a>Een module voor orderdetails toevoegen aan een pagina

Voer de volgende stappen uit om een module voor orderdetails aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** de naam in voor **Sjabloon voor orderdetails** en selecteer **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderdetails** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de sjabloon te bekijken. De module voor orderdetails wordt niet weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** de **Sjabloon voor orderdetails**. Voer onder **Paginanaam** **Pagina voor orderdetails** in en selecteer vervolgens **OK**.
1. Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderdetails** en selecteer vervolgens **OK**.
1. Selecteer in het eigenschappenvenster van de module voor orderdetails de optie **Kop** naast het potloodsymbool.
1. Voer in het veld **Koptekst** van het dialoogvenster **Koptekst** de koptekst **OrderDetails** in en selecteer **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht starterskit](starter-kit-overview.md)

[Containermodule](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

[Winkelwagenmodule](add-cart-module.md)

[Kassamodule](add-checkout-module.md)

[Koptekstmodule](author-header-module.md)

[Voettekstmodule](author-footer-module.md)

---
title: Module voor snelle weergave
description: In dit onderwerp wordt beschreven wat modules voor snelle weergave zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7e8244a06c515029b559b2061d9a25c7355e9e14
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097047"
---
# <a name="quick-view-module"></a>Module voor snelle weergave

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit onderwerp wordt beschreven wat modules voor snelle weergave zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Met de module voor snelle weergave kunnen gebruikers snel productgegevens weergeven wanneer ze door producten bladeren op een lijstpagina en een of meer producten aan het winkelwagentje toevoegen vanaf de lijstpagina, zonder naar de pagina met productgegevens te hoeven gaan. De module voor snelle weergave biedt een overzicht van de productgegevens die gebruikers nodig hebben om een beslissing over een toevoeging aan een winkelwagen te nemen. Daarnaast biedt de module een koppeling naar de pagina met productgegevens, zodat gebruikers aanvullende productdetails en inkoopopties kunnen bekijken.

De module voor snelle weergave wordt ondersteund door de modules voor [productverzameling](product-collection-module-overview.md) en [zoekresultaten](search-result-module.md).

> [!IMPORTANT]
> De module voor snelle weergave is beschikbaar vanaf Commerce 10.0.17.

De volgende afbeelding toont een voorbeeld van een module voor snelle weergave op een pagina met een productlijst.

![Voorbeeld van een module voor snelle weergave op een pagina met een productlijst](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Module-eigenschappen

De module voor snelle weergave ondersteunt enkele van dezelfde functies als de koopvakmodule. Daarom lijken de eigenschappen van een module voor snelle weergave op die van een koopvakmodule.

| Eigenschap | Waarden | Beschrijving |
|----------------|--------|-------------|
| Koptekstlabel | **H1**, **H2**, **H3**, **H4**, **H5** of **H6** | Deze eigenschap bepaalt het koptekstlabel voor de producttitel. Als de module voor snelle weergave boven aan de pagina staat, moet deze eigenschap worden ingesteld op **H1** om te voldoen aan toegankelijkheidsstandaarden. |
| Aangepaste prijs toestaan | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, kan de gebruiker een aangepaste prijs invoeren. |
| Minimumprijs | Geheel getal | Deze eigenschap is alleen van toepassing als de eigenschap **Aangepaste prijs toestaan** is ingesteld op **Waar**. Hiermee wordt de minimumprijs bepaald die de gebruiker kan invoeren (bijvoorbeeld $ 1). |
| Maximumprijs | Geheel getal | Deze eigenschap is alleen van toepassing als de eigenschap **Aangepaste prijs toestaan** is ingesteld op **Waar**. Hiermee wordt de maximumprijs bepaald die de gebruiker kan invoeren (bijvoorbeeld $ 1000). |

## <a name="commerce-site-builder-settings"></a>Commerce Site Builder-instellingen

Net als voor de koopvakmodule gelden voor de module voor snelle weergave de instellingen in **Site-instellingen \> Extensies \> Product toevoegen aan winkelwagen**. De instelling van **Navigeren naar winkelwagen** wordt echter genegeerd omdat deze niet past bij het doel van de module voor snelle weergave, namelijk gebruikers in staat stellen meerdere producten op een lijstpagina te bekijken en deze aan de winkelwagen toe te voegen zonder de lijstpagina te verlaten.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Een module voor snelle weergave aan een productverzamelingsmodule toevoegen

Een module voor snelle weergave kan worden toegevoegd aan de modules voor productverzameling en zoekresultaten.

Voer de volgende stappen uit om een module voor snelle weergave toe te voegen aan productverzamelingsmodule in Commerce Site Builder.

1. Ga naar **Pagina's** en selecteer de startpagina voor de Fabrikam-site.
1. Ga naar een module **Productverzameling** op de startpagina, selecteer het weglatingsteken (**...**) en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de module **Snelle weergave** en selecteer vervolgens **OK**.
1. Selecteer **Koptekst** in het eigenschappenvenster van de module **Snelle weergave**. Stel in het dialoogvenster **Koptekst** het veld **Koptekstniveau** in op **H2** en selecteer **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Productverzamelingsmodule](product-collection-module-overview.md)

[Module voor zoekresultaten](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
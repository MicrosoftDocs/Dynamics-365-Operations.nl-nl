---
title: Beoordelingen en recensies configureren
description: In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7ac91dd1d3dfffbf98733bbd8fe8beda538250da
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473544"
---
# <a name="configure-ratings-and-reviews"></a>Beoordelingen en recensies configureren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.

Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een inkoopbeslissing nemen, door te laten zien wat andere klanten van deze producten vinden. Voor e-commerce-websites zijn beoordelingen en recensies ook een mechanisme voor het verzamelen van klantfeedback over producten. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Een site met beoordelingen en recensies configureren

Configuratiewaarden voor beoordelingen en recensies, zoals de tenant-id, de lengte van de recensietekst en de lengte van de recensietitel worden op siteniveau geconfigureerd. 

Voer de volgende stappen uit om een site te configureren voor het weergeven van beoordelingen en recensies. 

1. Ga naar **Startpagina \> Sites**.
1. Selecteer de naam van uw site. 
1. Ga naar **Vestigingsinstellingen \> Uitbreidingen**. 
1. Voer in het veld **Maximale lengte recensietekst** het maximumaantal tekens in dat de recensietekst kan bevatten (bijvoorbeeld **1000**). 
1. Voer in het veld **Maximale lengte recensietitel** het maximumaantal tekens in dat de recensietitel kan bevatten (bijvoorbeeld **55**). 
1. Selecteer **Opslaan en publiceren**. 

In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.

![Een site met beoordelingen en recensies configureren.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Een productbeoordeling koppelen aan de sectie Recensies van een PDP

Een productbeoordeling wordt onder de producttitel boven aan de PDP weergegeven. De productbeoordeling kan zo worden geconfigureerd dat deze wordt gekoppeld aan de sectie **Recensies** van dezelfde PDP. 

Voer de volgende stappen uit om een productbeoordeling te koppelen aan de sectie **Recensies** van de PDP.

1. Open de PDP-sjabloon. 
1. Ga naar **Instellingen van module voor koopvakcontainer**.
1. Selecteer onder **Koopvak** de optie **Productbeoordelingen** en schakel vervolgens het selectievakje **Klikken koppelen aan module met volledige recensies** in.

In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.

![Een productbeoordeling koppelen aan de sectie Recensies van een PDP.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>De koppeling naar de pagina Privacy en beleid configureren

Volg deze stappen om de koppeling naar de pagina Privacy en beleid te configureren

1. Ga naar **Startpagina \> Sites**.
1. Selecteer de naam van uw site. 
1. Ga naar **Vestigingsinstellingen \> Uitbreidingen**.
1. Selecteer op het tabblad **Routes** onder **RNR privacy en beleid** de optie **Een koppeling toevoegen**. Als er al een koppeling is ingevoerd en u deze wilt vervangen, selecteert u de koppeling. 
1. Selecteer in het dialoogvenster **Een koppeling toevoegen** de koppeling voor de pagina Privacy en beleid en selecteer vervolgens **OK.** 
1. Selecteer **Opslaan en publiceren**. 

In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.

![De koppeling naar de pagina Privacy en beleid configureren.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Modules voor beoordelingen en recensies configureren op pagina's met productdetails

Zie [Modules voor beoordelingen en recensies](ratings-reviews-modules.md) voor meer informatie over het configureren van de modules voor beoordelingen en recensies op pagina's met productdetails.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Aanmelden om beoordelingen en recensies te gebruiken](opt-in-ratings-reviews.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Modules voor beoordelingen en recensies configureren op pagina's met productdetails](ratings-reviews-modules.md)

[Productbeoordelingen synchroniseren in Dynamics 365 Retail](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

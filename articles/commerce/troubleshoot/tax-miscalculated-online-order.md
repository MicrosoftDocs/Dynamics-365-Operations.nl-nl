---
title: De btw op online orders wordt onjuist berekend
description: Dit artikel bevat richtlijnen voor het oplossen van problemen die kunnen helpen bij het foutief berekenen van btw op online orders of wanneer de btw-groep op de verkoopregel niet juist is ingesteld.
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: a85b03cb6245c7c2e3622abc61a7887030927432
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285573"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>De btw op online orders wordt onjuist berekend

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor het oplossen van problemen die kunnen helpen bij het foutief berekenen van btw op online orders of wanneer de btw-groep op de verkoopregel niet juist is ingesteld.

## <a name="description"></a>Beschrijving

Wanneer een e-commerce-order wordt geplaatst, wordt de btw onjuist berekend of wordt de btw-groep op de verkoopregel onjuist ingesteld.

## <a name="resolution"></a>Oplossing

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Algemene btw-groepen configureren in Commerce headquarters

Voer deze stappen uit om algemene btw-groepen te configureren in Commerce Headquarters.

1. Ga naar **Btw \> Indirecte belastingen \> Btw \> Btw-groep**.
1. Selecteer in het navigatiedeelvenster aan de linkerkant de btw-groep die u wilt configureren.
1. Configureer op het sneltabblad **Op retailbestemming gebaseerde btw** de btw voor de btw-groep.

> [!NOTE]
> Voor verzending waarbij geen btw is opgenomen die wordt bepaald door het adres van de klant, wordt de btw-groep bepaald door het afleveradres van de regel en de op bestemming gebaseerde btw die zijn geconfigureerd voor de btw-groep. Zie [Belastingen voor online winkels instellen op basis van de bestemming](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination) voor meer informatie.

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>De btw configureren voor een detailhandelwinkel in Commerce Headquarters

Voer deze stappen uit om btw te configureren voor een detailhandelwinkel in Commerce Headquarters.

1. Ga naar **Retail en commerce \> Afzetkanalen \> Alle winkels**.
1. Selecteer de winkel waarvoor u btw wilt configureren.
1. Configureer op het sneltabblad **Algemeen** in de sectie **Btw** de btw-gegevens voor de winkel.

> [!NOTE]
> Als een product uit een winkel wordt opgehaald, wordt de btw-groep opgehaald uit de winkel die is geselecteerd om bij op te halen. Zie [Andere btw-opties voor winkels instellen](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores) voor meer informatie.

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>De btw configureren voor het adres van een klant in Commerce Headquarters

Voer deze stappen uit om btw te configureren voor het adres van een klant in Commerce Headquarters.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Selecteer de klant voor wie u btw wilt configureren.
1. Selecteer op het sneltabblad **Adressen** het adres waarvoor u btw wilt configureren, selecteer **Meer opties** en selecteer vervolgens **Geavanceerd**.
1. Selecteer de optie **Btw-groep** op het tabblad **Algemeen**.
1. Selecteer de juiste waarde in het veld **Btw**.

> [!NOTE]
> Voor verzending waarbij btw op het adres van de klant is betrokken, bepaalt het afleveradres van de regel de btw-groep voor de regel. Als de klant verzendt naar een bestaand adres dat al een btw-groep heeft geconfigureerd, wordt de bestaande btw-groep gebruikt. Adressen hebben standaard geen btw-groep wanneer ze worden gemaakt.

## <a name="additional-resources"></a>Aanvullende bronnen

[Btw voor online orders configureren](../sales-tax-config.md)

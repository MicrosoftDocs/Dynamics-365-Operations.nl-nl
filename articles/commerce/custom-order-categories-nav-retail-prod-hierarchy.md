---
title: De sorteervolgorde voor entiteiten voor merchandising wijzigen
description: In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten in Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 67807c53a6ffc6dd09cc6f0e48218e2ee2de559f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207770"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>De sorteervolgorde voor entiteiten voor merchandising wijzigen


[!include [banner](includes/banner.md)]

Voor detailhandelaren is het kunnen vinden van producten een primair hulpmiddel voor de interactie met klanten in alle kanalen. Met behulp van diverse functies kunnen klanten gemakkelijk producten ontdekken. Ze kunnen bijvoorbeeld bladeren in categorieën, zoeken en filteren.

In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten. Ook wordt uitgelegd hoe u de sorteervolgorde kunt wijzigen.

## <a name="overview"></a>Overzicht

De ondersteuning voor het sorteren van diverse entiteiten voor merchandising is verbeterd. Deze ondersteuning is nu beter afgestemd op bestaande klantenscenario's waarvoor eerder extensies nodig waren van de implementatiepartners.

In versies van Retail van voor 10.0.5 was de sorteervolgorde voor categorieën in de navigatiehiërarchie in alfabetische volgorde. Met de nieuwe aangepaste sorteervolgorde kunt u ervoor zorgen dat merchandisingmanagers de sorteervolgorde configureren voor diverse merchandisingentiteiten voor alle eindgebruikers. Dit omvat Headquarters (HQ) en callcenters.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>De weergavevolgorde configureren voor categorieën in de producthiërarchie

Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Commerce-producthiërarchie**.
2. Klik op **Categoriehiërarchie bewerken**.
3. Klik op **Bewerken**.
4. Vouw in de structuur **ALLE \> Actiesporten** uit.
5. Vouw in de structuur **ALLE \> Teamsporten** uit.
6. Voer een nummer in het veld **Weergavevolgorde** in. (Het nummer kan negatief zijn.)
7. Herhaal stap 4 tot en met 6 voor alle andere categorieën waarvan u de volgorde wilt wijzigen.

De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weergegeven in HQ voor de Commerce-producthiërarchie en de vrijgegeven producten per categorie.

![Aangepaste sortering van producthiërarchie met negatieve waarden](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Aangepaste sortering van vrijgegeven producten op categorie op basis van de producthiërarchie](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>De weergavevolgorde configureren voor categorieën in de kanaalnavigatiehiërarchie

Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Kanaalnavigatiecategorieën**.
2. Selecteer de **navigatiehiërarchie voor Mode** in de lijst.
3. Klik op **Categoriehiërarchie bewerken**.
4. Klik op **Bewerken**.
5. Selecteer in de structuur **Mode \> Dameskleding \> Damesschoenen**.
6. Voer een nummer in het veld **Weergavevolgorde** in.
7. Selecteer in de structuur **Mode \> Dameskleding \> Tops**.

    Op dezelfde manier kunt u de sorteervolgorde voor de subcategorieën definiëren.

8. Selecteer in de structuur **Mode \> Herenkleding \> Casual shirts**.
9. Voer een nummer in het veld **Weergavevolgorde** in.
10. Selecteer in de structuur **Mode \> Herenkleding \> Jassen en jacks**.
11. Voer een nummer in het veld **Weergavevolgorde** in.
12. Herhaal dit voor alle andere categorieën waarvan u de volgorde wilt wijzigen.

De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weerspiegeld in HQ, catalogus en kanalen.

![Aangepaste sortering voor hiërarchie van detailhandelafzetkanaal](./media/ChannelNavCustomSorted.png)

![Aangepaste sorteren van catalogusnavigatiehiërarchie op basis van de kanaalnavigatiehiërarchie](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS met aangepaste gesorteerde categorieën](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> De functie voor aangepast sorteren is standaard uitgeschakeld. Zie [Functiebeheer](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview) voor meer informatie over het inschakelen van deze functie en andere functies.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
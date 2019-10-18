---
title: De sorteervolgorde voor entiteiten voor merchandising wijzigen
description: In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten in Dynamics 365 Retail.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c159ff869d6c504fdebbef1fa68115a410c81d85
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019411"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>De sorteervolgorde voor entiteiten voor merchandising wijzigen


[!include [banner](includes/banner.md)]

Voor detailhandelaren is het kunnen vinden van producten een primair hulpmiddel voor de interactie met klanten in alle detailhandelkanalen. Met behulp van diverse functies kunnen klanten gemakkelijk producten ontdekken. Ze kunnen bijvoorbeeld bladeren in categorieën, zoeken en filteren.

In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten. Ook wordt uitgelegd hoe u de sorteervolgorde kunt wijzigen.

## <a name="overview"></a>Overzicht

De ondersteuning voor het sorteren van diverse entiteiten voor merchandising is verbeterd. Deze ondersteuning is nu beter afgestemd op bestaande klantenscenario's waarvoor eerder extensies nodig waren van de implementatiepartners.

In versies van Retail van voor 10.0.5 was de sorteervolgorde voor categorieën in de navigatiehiërarchie in alfabetische volgorde. Met de nieuwe aangepaste sorteervolgorde kunt u ervoor zorgen dat merchandisingmanagers de sorteervolgorde configureren voor diverse merchandisingentiteiten voor alle eindgebruikers. Dit omvat Headquarters (HQ) en callcenters.

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a>De weergavevolgorde configureren voor categorieën in de producthiërarchie voor detailhandel

Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.

1. Ga naar **Detailhandel \> Producten en categorieën \> Producthiërarchie detailhandel**.
2. Klik op **Categoriehiërarchie bewerken**.
3. Klik op **Bewerken**.
4. Vouw in de structuur **ALLE \> Actiesporten** uit.
5. Vouw in de structuur **ALLE \> Teamsporten** uit.
6. Voer een nummer in het veld **Weergavevolgorde** in. (Het nummer kan negatief zijn.)
7. Herhaal stap 4 tot en met 6 voor alle andere categorieën waarvan u de volgorde wilt wijzigen.

De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weergegeven in HQ voor de detailhandelproducthiërarchie en de vrijgegeven producten per categorie.

![Aangepaste sortering van detailhandelproducthiërarchie met negatieve waarden](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Aangepaste sortering van vrijgegeven producten op categorie op basis van de detailhandelproducthiërarchie](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>De weergavevolgorde configureren voor categorieën in de kanaalnavigatiehiërarchie

Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.

1. Ga naar **Detailhandel \> Producten en categorieën \> Categorieën voor afzetkanaalnavigatie**.
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

De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weerspiegeld in HQ, catalogus en detailhandelafzetkanalen.

![Aangepaste sortering voor hiërarchie van detailhandelafzetkanaal](./media/ChannelNavCustomSorted.png)

![Aangepaste sorteren van catalogusnavigatiehiërarchie op basis van de kanaalnavigatiehiërarchie](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS met aangepaste gesorteerde categorieën](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> De functie voor aangepast sorteren is standaard uitgeschakeld. Zie [Functiebeheer](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview) voor meer informatie over het inschakelen van deze functie en andere functies.

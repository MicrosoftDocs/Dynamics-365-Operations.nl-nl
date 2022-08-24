---
title: De sorteervolgorde voor entiteiten voor merchandising wijzigen
description: In dit artikel worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten in Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265831"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>De sorteervolgorde voor entiteiten voor merchandising wijzigen


[!Include [banner](includes/banner.md)]

Voor detailhandelaren is het kunnen vinden van producten een primair hulpmiddel voor de interactie met klanten in alle kanalen. Er zijn verscheidene functies die klanten kunnen helpen om producten eenvoudig te ontdekken. Klanten kunnen bijvoorbeeld bladeren in categorieën, zoeken en filteren.

In dit artikel worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten. Ook wordt uitgelegd hoe u de sorteervolgorde kunt wijzigen.

## <a name="overview"></a>Overzicht

In Commerce is het sorteren van verschillende entiteiten die aan deze zaken zijn gerelateerd afgestemd op bestaande klantscenario's en zijn uitbreidingen van implementatiepartners niet langer nodig.

In Commerce-versies 10.0.5 en lager was de sorteervolgorde voor categorieën in de navigatiehiërarchie in alfabetische volgorde. Met de huidige aangepaste sorteervolgorde zorgt ervoor dat merchandisingmanagers de sorteervolgorde kunnen configureren voor diverse merchandisingentiteiten voor alle eindgebruikers. Dit omvat Headquarters (HQ) en callcenters.

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

![Aangepaste sortering van producthiërarchie met negatieve waarden.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Aangepaste sortering van vrijgegeven producten op categorie op basis van de producthiërarchie.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>De weergavevolgorde configureren voor categorieën in de kanaalnavigatiehiërarchie

Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Kanaalnavigatiecategorieën**.
2. Selecteer de **navigatiehiërarchie voor Mode** in de lijst.
3. Klik op **Categoriehiërarchie bewerken**.
4. Klik op **Bewerken**.
5. Selecteer in de boomstructuur **Mode \> Dameskleding \> Damesschoenen**.
6. Voer een nummer in het veld **Weergavevolgorde** in.
7. Selecteer in de structuur **Mode \> Dameskleding \> Tops**.

Op dezelfde manier kunt u de sorteervolgorde voor de subcategorieën definiëren.

8. Selecteer in de structuur **Mode \> Herenkleding \> Casual shirts**.
9. Voer een nummer in het veld **Weergavevolgorde** in.
10. Selecteer in de structuur **Mode \> Herenkleding \> Jassen en jacks**.
11. Voer een nummer in het veld **Weergavevolgorde** in.
12. Herhaal dit voor alle andere categorieën waarvan u de volgorde wilt wijzigen.

De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weerspiegeld in HQ, catalogus en kanalen.

![Aangepaste sortering voor hiërarchie van detailhandelafzetkanaal.](./media/ChannelNavCustomSorted.png)

![Aangepaste sorteren van catalogusnavigatiehiërarchie op basis van de kanaalnavigatiehiërarchie.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS met aangepaste gesorteerde categorieën.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> De functie **Weergavevolgorde inschakelen voor merchandisingentiteiten** is standaard uitgeschakeld. Gebruik [Functiebeheer](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om deze in te schakelen. Voer na het inschakelen van de functie op de pagina de taak **Globale configuratie - 1110** CDX uit vanuit het distributieschema.
> Als de volgorde van uw categorieën in POS niet wordt bijgewerkt, moet u het apparaat opnieuw activeren. Categorie-informatie wordt opgehaald wanneer activering van het apparaat plaatsvindt, dus het kan voorkomen dat het apparaat de categorie-informatie opnieuw moet voorzien van bijgewerkte weergavevolgordes. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]

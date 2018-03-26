---
title: Productcategoriebeheer
description: "In dit onderwerp wordt beschreven hoe merchandisingmanagers de detailhandelproductcategorieën gebruiken om relaties tussen de detailhandelproducthiërarchie en vrijgegeven productdetails te beheren."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: nl-nl
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Verbeterd categorie- en productbeheer

[!include[banner](./includes/banner.md)]

In dit onderwerp wordt een verbeterde manier beschreven om de detailhandelproductcategorieën en producten te beheren in Dynamics 365 for Retail. Dankzij deze verbeteringen kunnen merchandisingmanagers een algemeen overzicht met producteigenschappen weergeven tussen de detailhandelproducthiërarchie en details van vrijgegeven producten.

Voor meer informatie over het beheren van detailhandelproductcategorieën gaat u naar **Producthiërarchie detailhandel** in het werkgebied **Categorie- en productbeheer** en geeft u de verbeterde structuur van de pagina **Productcategorie detailhandel** weer.

![Werkgebied categorie- en productbeheer](media/LaunchRetailProductHierarchy.png)

In eerdere versies waren producteigenschappen onderverdeeld in **basisproducteigenschappen** en **detailhandelproducteigenschappen**, op basis van het bereik van hun toepassing. **Detailhandelproducteigenschappen** zijn *algemeen* voor het toepassingsbereik, wat inhoudt dat voor een bepaalde **detailhandelproducteigenschap** dezelfde waarde wordt gedeeld door alle rechtspersonen. **Basisproducteigenschappen** zijn *specifieke eigenschappen voor rechtspersonen*. De waarde van een bepaalde **basisproducteigenschap** kan dus verschillen tussen rechtspersonen, op basis van individuele zakelijke behoeften.

Met de verbeterde opzet voor producteigenschappen in de detailhandel blijven producteigenschappen logisch gescheiden, op basis van hun toepassing binnen een groep, om de formulierstructuur voor details van vrijgegeven producten te weerspiegelen.

![Groepering van de velden op basis van hun toepassingsbereik](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

U kunt schakelen tussen het beheren van specifieke eigenschappen voor rechtspersonen voor alle rechtspersonen en het beheren van deze eigenschappen voor een specifieke rechtspersoon. Selecteer hiervoor **Weergeven/bewerken voor alle rechtspersonen** of **Weergeven/bewerken voor een specifieke rechtspersoon**.

![Schakelen tussen één persoon en alle rechtspersonen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Schakelen tussen één persoon en alle rechtspersonen](media/ToggleToEditForAllLegalEntities.PNG)  

Ten opzichte van vorige versies kan een merchandisingmanager in de nieuwe productstructuur voor detailhandelproducten ook standaardwaarden definiëren voor een aanvullende reeks producteigenschappen op het niveau van een individuele categorie. Bij het maken van producten worden deze standaardwaarden voor producteigenschappen overgenomen door een product, op basis van de koppeling met een individuele categorie uit de hiërarchie voor detailhandelproducten. Deze overgenomen producteigenschappen kunnen ook worden aangepast voor elk product om te voldoen aan individuele zakelijke behoeften.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Eigenschappen selecteren om producten uit het formulier Productcategorie van detailhandel bij te werken 
 
Gebruik de nieuwe uitgebreide structuur voor producteigenschappen om te selecteren welke producteigenschappen moeten worden verplaatst naar de bijbehorende producten. 

![Nieuwe uitgebreide weergave van Producten bijwerken](media/NewUpdateProductsEnhancedView.PNG) 

Merchandisingmanagers kunnen deze overgenomen producteigenschappen voor elk product overnemen om te voldoen aan individuele zakelijke behoeften.



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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2246024d7d70947690173f3d0768292abe43efd7
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="manage-retail-product-categories-and-products"></a>Productcategorieën en producten detailhandel beheren

[!INCLUDE [banner](./includes/banner.md)]

In dit onderwerp wordt een verbeterde manier beschreven om de detailhandelproductcategorieën en producten te beheren in Microsoft Dynamics 365 for Retail. Dankzij deze verbeteringen kunnen merchandisingmanagers een overzicht met producteigenschappen weergeven die worden gedeeld tussen de detailhandelproducthiërarchie en details van vrijgegeven producten.

Voor meer informatie over het beheren van Retail-productcategorieën selecteert u in het werkgebied **Categorie- en productbeheer** de tegel **Producthiërarchie detailhandel**.

U ziet de verbeterde structuur van de pagina **Producthiërarchie detailhandel**. In eerdere versies van Retail waren producteigenschappen onderverdeeld in *basisproducteigenschappen* en *detailhandelproducteigenschappen*, op basis van het bereik van hun toepassing. Eigenschappen van detailhandelproducten zijn *globaal* in hun toepassingsbereik. Dit betekent dat voor een bepaalde producteigenschap dezelfde waarde wordt gedeeld door alle rechtspersonen. Basisproducteigenschappen daarentegen zijn *specifieke eigenschappen voor rechtspersonen*. De waarde van een bepaalde basisproducteigenschap kan dus verschillen tussen rechtspersonen, op basis van individuele zakelijke behoeften van elke rechtspersoon.

Met de verbeterde opzet voor producteigenschappen in de detailhandel blijven producteigenschappen logisch gescheiden, op basis van hun toepassing in een groep, om de formulierstructuur voor details van vrijgegeven producten te weerspiegelen.

![Groepering van de velden op basis van het toepassingsbereik van de eigenschappen](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

U kunt schakelen tussen het beheren van specifieke eigenschappen voor rechtspersonen voor alle rechtspersonen en het beheren van deze eigenschappen voor een specifieke rechtspersoon.

Als u eigenschappen wilt beheren voor alle rechtspersonen, selecteert u **Weergeven voor alle rechtspersonen** (of **Bewerken voor alle rechtspersonen**).

![Weergeven/bewerken voor alle rechtspersonen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Als u eigenschappen wilt beheren voor een specifieke rechtspersoon, selecteert u **Weergeven voor een specifieke rechtspersoon** (of **Bewerken voor een specifieke rechtspersoon**).

![Weergeven/bewerken voor een specifieke rechtspersoon](media/ToggleToEditForAllLegalEntities.PNG)

In de verbeterde productstructuur voor detailhandelproducten kan een merchandisingmanager nu ook standaardwaarden definiëren voor een aanvullende reeks producteigenschappen op het niveau van een individuele categorie. Wanneer de producten worden gemaakt, nemen ze deze standaardwaarden voor producteigenschappen over, op basis van de koppeling van deze eigenschappen met een individuele categorie uit de hiërarchie voor detailhandelproducten. Deze overgenomen producteigenschappen kunnen ook worden aangepast voor elk product om te voldoen aan individuele zakelijke behoeften.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Eigenschappen selecteren om producten uit de pagina Productcategorie van detailhandel bij te werken

Gebruik de nieuwe uitgebreide structuur voor producteigenschappen om te selecteren welke producteigenschappen moeten worden verplaatst naar de bijbehorende producten. Op de pagina **Producthiërarchie detailhandel** selecteert u in het actievenster **Categorie** en vervolgens **Producten bijwerken** om het dialoogvenster **Producten bijwerken** te openen.

![Het dialoogvenster Producten bijwerken](media/NewUpdateProductsEnhancedView.PNG)



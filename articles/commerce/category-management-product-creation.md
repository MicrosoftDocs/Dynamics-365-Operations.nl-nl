---
title: Productcategorieën en producten beheren
description: In dit onderwerp wordt beschreven hoe merchandisingmanagers productcategorieën gebruiken om relaties tussen de producthiërarchie en vrijgegeven productdetails in Commerce te beheren.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9d47a866703b830e84e3f2e37a02d9d58f73987b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411344"
---
# <a name="manage-product-categories-and-products"></a>Productcategorieën en producten beheren

[!include [banner](./includes/banner.md)]

In dit onderwerp wordt een verbeterde manier beschreven om de productcategorieën en producten te beheren in Dynamics 365 Commerce. Dankzij deze verbeteringen kunnen merchandisingmanagers een overzicht met producteigenschappen weergeven die worden gedeeld tussen de producthiërarchie en details van vrijgegeven producten.

Voor meer informatie over het beheren van productcategorieën selecteert u in het werkgebied **Categorie- en productbeheer** de tegel **Producthiërarchie in Commerce**.

U ziet de verbeterde structuur van de pagina **Producthiërarchie in Commerce**. In eerdere versies van de app waren producteigenschappen onderverdeeld in *basisproducteigenschappen* en *detailhandelproducteigenschappen*, op basis van het bereik van hun toepassing. Eigenschappen van detailhandelproducten zijn *globaal* in hun toepassingsbereik. Dit betekent dat voor een bepaalde producteigenschap dezelfde waarde wordt gedeeld door alle rechtspersonen. Basisproducteigenschappen daarentegen zijn *specifieke eigenschappen voor rechtspersonen*. De waarde van een bepaalde basisproducteigenschap kan dus verschillen tussen rechtspersonen, op basis van individuele zakelijke behoeften van elke rechtspersoon.

Met de verbeterde opzet voor producteigenschappen blijven producteigenschappen logisch gescheiden, op basis van hun toepassing in een groep, om de formulierstructuur voor details van vrijgegeven producten te weerspiegelen.

![Groepering van de velden op basis van het toepassingsbereik van de eigenschappen](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

U kunt schakelen tussen het beheren van specifieke eigenschappen voor rechtspersonen voor alle rechtspersonen en het beheren van deze eigenschappen voor een specifieke rechtspersoon.

Als u eigenschappen wilt beheren voor alle rechtspersonen, selecteert u **Weergeven voor alle rechtspersonen** (of **Bewerken voor alle rechtspersonen**).

![Weergeven/bewerken voor alle rechtspersonen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Als u eigenschappen wilt beheren voor een specifieke rechtspersoon, selecteert u **Weergeven voor een specifieke rechtspersoon** (of **Bewerken voor een specifieke rechtspersoon**).

![Weergeven/bewerken voor een specifieke rechtspersoon](media/ToggleToEditForAllLegalEntities.PNG)

In de verbeterde productcategoriestructuur kan een merchandisingmanager nu ook standaardwaarden definiëren voor een aanvullende reeks producteigenschappen op het niveau van een individuele categorie. Wanneer de producten worden gemaakt, nemen ze deze standaardwaarden voor producteigenschappen over, op basis van de koppeling van deze eigenschappen met een individuele categorie uit de producthiërarchie. Deze overgenomen producteigenschappen kunnen ook worden aangepast voor elk product om te voldoen aan individuele zakelijke behoeften.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Eigenschappen selecteren om producten uit de pagina Productcategorie in Commerce bij te werken

Gebruik de nieuwe uitgebreide structuur voor producteigenschappen om te selecteren welke producteigenschappen moeten worden verplaatst naar de bijbehorende producten. Op de pagina **Producthiërarchie in Commerce** selecteert u in het actievenster **Categorie** en vervolgens **Producten bijwerken** om het dialoogvenster **Producten bijwerken** te openen.

![Het dialoogvenster Producten bijwerken](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
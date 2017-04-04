---
title: Productdimensies
description: Er zijn vier productdimensies - kleur, configuratie, grootte en stijl. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8854ab94a71cc363bcd073d2df47bc01a243b6cd
ms.lasthandoff: 03/31/2017


---

# <a name="product-dimensions"></a>Productdimensies

Er zijn vier productdimensies - kleur, configuratie, grootte en stijl. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.

Productdimensies zijn kenmerkend als ze dienen ter identificatie van de variant van een product. U kunt combinaties van productdimensies gebruiken om varianten van het product te definiëren. Als u een productvariant wilt maken, moet u ten minste één productdimensie definiëren voor een productmodel.
Productvarianten
----------------

Productvarianten worden ook artikelen genoemd. Een artikel is een tastbaar product, dat niet hetzelfde is als een service. Het is ook mogelijk om te definiëren van een productmodel met het servicetype. Met behulp van het type Service kunt u productvarianten specificeren die services omvatten. U kunt bijvoorbeeld een productmodel opgeven voor advieswerk en productvarianten voor werk dat is uitgevoerd door senior en junior consultants.

## <a name="product-dimensions"></a>Productdimensies
De volgende productdimensies zijn beschikbaar: configuratie, kleur, grootte en stijl. Een productvariant kan worden gegenereerd op basis van de dimensiewaarden van het product.

Productdimensies waarden, zoals grootte, kleur en stijl kan worden gemaakt op de **grootte**, **kleur** en **stijl** pagina's waarmee kunnen worden geopend vanuit de volgende locaties: **productgegevensbeheer**&gt;**Setup**&gt;**dimensie en variant groepen**&gt;**maten/kleuren of stijlen**. Waarden voor productdimensies voor de Configuratiedimensie worden doorgaans gemaakt met de functie voor productconfiguratie of op dimensies gebaseerde configuratie. Productdimensies kunnen tevens worden gemaakt en beheerd op de pagina **Productdimensies**, die kan worden geopend vanaf de volgende locaties:
-   Klik op **productgegevensbeheer**&gt;**producten**&gt;**productmodellen**. Op de **actievenster**, klikt u op **productdimensies**.
-   Klik op **productgegevensbeheer**&gt;**producten**&gt;**alle producten en productmodellen**. Een productmodel selecteren. Op de **actievenster**, klikt u op **productdimensies**.
-   Klik op **productgegevensbeheer**&gt;**vrijgegeven producten**. Een productmodel selecteren. Op de **actievenster**, klikt u op **product**. Klik in de groep **Productmodel** op **Productdimensies**.

Het aantal varianten dat u voor een artikel maakt, wordt beperkt door het aantal mogelijke productdimensiecombinaties.
| **Tip **                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wanneer u een product bijvoorbeeld op een orderregel gebruikt, selecteert u de productdimensies om de productvariant waarmee u wilt werken, te identificeren. |

## <a name="example"></a>Voorbeeld
Een bedrijf verkoopt spijkerbroeken. Het artikel Spijkerbroeken gebruikt de productdimensies Kleur en Maat. De spijkerbroeken worden in drie verschillende kleuren en in zes verschillende maten verkocht. Kleuren: Blauw, Zwart, Bruin Maten: XS, S, M, L, XL, XXL Niet alle maten zijn beschikbaar in alle drie kleuren. Als alle combinaties beschikbaar zijn, zijn er 18 typen spijkerbroeken. In dit voorbeeld worden alleen de volgende negen combinaties van productvarianten geproduceerd.

| Kleur | Grootte |
|-------|------|
| Blauw  | XS   |
| Blauw  | Z    |
| Blauw  | M    |
| Zwart | M    |
| Zwart | L    |
| Zwart | XL   |
| Bruin | L    |
| Bruin | XL   |
| Bruin | XXL  |





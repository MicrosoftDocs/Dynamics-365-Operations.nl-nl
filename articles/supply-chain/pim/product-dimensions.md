---
title: Productdimensies
description: 'Er zijn vier productdimensies: stijl, configuratie, grootte en kleur. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.'
author: cvocph
manager: tfehr
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5e9b10fa18ada9534ce5e279d4f1f09973a802b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208427"
---
# <a name="product-dimensions"></a>Productdimensies

[!include [banner](../includes/banner.md)]

Er zijn vier productdimensies: stijl, configuratie, grootte en kleur. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.

Productdimensies zijn kenmerkend als ze dienen ter identificatie van de variant van een product. U kunt combinaties van productdimensies gebruiken om varianten van het product te definiëren. Als u een productvariant wilt maken, moet u ten minste één productdimensie definiëren voor een productmodel.

## <a name="product-variants"></a>Productvarianten

Productvarianten worden ook artikelen genoemd. Een artikel is een tastbaar product, dat niet hetzelfde is als een service. Het is echter ook mogelijk om een productmodel te definiëren van het type Service. Met behulp van het type Service kunt u productvarianten specificeren die services omvatten. U kunt bijvoorbeeld een productmodel opgeven voor advieswerk en productvarianten voor werk dat is uitgevoerd door senior en junior consultants.

## <a name="product-dimensions"></a>Productdimensies
De volgende vier productdimensies zijn beschikbaar: stijl, configuratie, grootte en kleur. Een productvarianten kan worden gegenereerd op basis van de waarden van de productdimensies.

Waarden voor productdimensies, zoals Grootte, Kleur en Stijl kunnen worden gemaakt op de pagina's **Maat**, **Kleur** en **Stijl**, die toegankelijk zijn vanaf de volgende locaties: **Productgegevensbeheer** &gt; **Instellingen** &gt; **Dimensie- en variantgroepen** &gt; **Maten/kleuren/stijlen**. Waarden voor productdimensies voor de Configuratiedimensie worden doorgaans gemaakt met de functie voor productconfiguratie of op dimensies gebaseerde configuratie. Productdimensies kunnen tevens worden gemaakt en beheerd op de pagina **Productdimensies**, die kan worden geopend vanaf de volgende locaties:
-   Klik op **Productgegevensbeheer** &gt; **Producten** &gt; **Productmodellen**. Klik in het **Actievenster** op **Productdimensies**.
-   Klik op **Productgegevensbeheer** &gt; **Producten** &gt; **Alle producten en productmodellen**. Een productmodel selecteren. Klik in het **Actievenster** op **Productdimensies**.
-   Klik op **Productgegevensbeheer** &gt; **Vrijgegeven producten**. Een productmodel selecteren. Klik in het **Actievenster** op **Product**. Klik in de groep **Productmodel** op **Productdimensies**.

Het aantal varianten dat u voor een artikel maakt, wordt beperkt door het aantal mogelijke productdimensiecombinaties.

| **Tip**                                                                                                                                              |
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






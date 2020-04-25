---
title: Productgegevensentiteiten
description: Dit onderwerp bevat informatie over de verschillende entiteiten die kunnen worden gebruikt voor het importeren en exporteren van productgegevens.
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 340cb33537c7ba07555e1f0b6437fa4a3458a11a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208611"
---
# <a name="product-data-entities"></a>Productgegevensentiteiten

[!include [banner](../includes/banner.md)]

U moet gegevensentiteiten gebruiken om productgegevens te importeren en te exporteren. De volgende tabel bevat details over de productgerelateerde gegevensentiteiten en beschrijft het doel van elk.

| Entiteit | Naam (type) van Application Object Tree (AOT) | Opmerkingen |
|--------|-------------------------------------------|-------|
| Producten V2 | EcoResProductV2Entity | Deze entiteit wordt gebruikt voor het importeren en exporteren van gedeelde producten, zowel afzonderlijke producten als productmodellen. Updates worden ondersteund. De entiteit biedt geen ondersteuning voor op sets gebaseerde SQL-bewerkingen. De entiteit is wel geschikt voor Open Data Protocol (OData). |
| Vrijgegeven producten V2 | EcoResReleasedProductV2Entity | Deze entiteit wordt gebruikt voor het importeren en exporteren van uitgebrachte producten, zowel afzonderlijke producten als productmodellen. Updates worden ondersteund. Het gedeelde product moet al zijn gemaakt. Wanneer een nieuw vrijgegeven product wordt geïmporteerd, vindt een vrijgave van het gedeelde product plaats. Er zijn ook afzonderlijke entiteiten die kunnen worden gebruikt voor het importeren en exporteren van vrijgegeven productmodellen en vrijgegeven verschillende varianten. Deze entiteit biedt geen ondersteuning voor op sets gebaseerde SQL-bewerkingen of verwijderbewerkingen. De entiteit is wel geschikt voor OData. |
| Vrijgegeven product maken V2 | EcoResReleasedProductCreationV2Entity | Deze entiteit wordt gebruikt om gedeelde producten en vrijgegeven producten in één stap te importeren. Hoewel exporteren wordt ondersteund, wordt dat gebruik niet aanbevolen, omdat het doel van de entiteit het maken van een product is. Updates worden niet ondersteund. Een beperkt aantal velden (velden die beschikbaar zijn in het dialoogvenster voor het maken van producten) wordt ondersteund. De entiteit biedt geen ondersteuning voor op sets gebaseerde SQL-bewerkingen. Deze entiteit wordt niet weergegeven via OData. |
| Productvarianten | EcoResProductVariantEntity | Deze entiteit wordt gebruikt voor het importeren en exporteren van gedeelde productvarianten. Updates worden ondersteund. Hiervoor moeten dimensiewaarden al zijn gemaakt. De integratiesleutel is het productmodel plus productdimensies. Deze entiteit biedt geen ondersteuning voor op sets gebaseerde SQL-bewerkingen. De entiteit is wel geschikt voor OData. De entiteit ondersteunt verwijderbewerkingen. De entiteit kan niet worden uitgebreid door nieuwe productdimensies toe te voegen. |
| Productvarianten per productnummer-id | EcoResProductNumberIdentifiedProductVariantEntity | Deze entiteit wordt gebruikt voor het importeren en exporteren van gedeelde productvarianten. Updates worden ondersteund. Hiervoor moeten dimensiewaarden al zijn gemaakt. De integratiesleutel is het productnummer (terwijl de integratiesleutel voor de entiteit **Productvarianten** het productmodel plus productdimensies is). |
| Vrijgegeven productvarianten | EcoResReleasedProductVariantEntity | Deze entiteit wordt gebruikt voor het importeren en exporteren van vrijgegeven productvarianten. Updates worden ondersteund. Gedeelde productvarianten moeten al zijn gemaakt. Wanneer een nieuw vrijgegeven productvariant wordt geïmporteerd, vindt een vrijgave van de gedeelde productvariant plaats. Deze entiteit biedt geen ondersteuning voor op sets gebaseerde SQL-bewerkingen. De entiteit is wel geschikt voor OData. Hoewel verwijderbewerkingen worden ondersteund, resulteren deze momenteel in gegevensbeschadiging vanwege een bug in het huidige platform. Deze entiteit kan niet worden uitgebreid door nieuwe productdimensies toe te voegen. |
| Vrijgegeven productvarianten per productnummer-id | EcoResProductNumberIdentifiedReleasedProductVariantEntity | Deze entiteit lijkt op de entiteit **Vrijgegeven productvarianten**, maar de integratiesleutel is het productnummer in plaats van het productmodel plus productdimensies. De entiteit kan worden uitgebreid door nieuwe productdimensies toe te voegen. |
| Verkoopbare vrijgegeven producten | EcoResSellableReleasedProductEntity | Deze entiteit wordt gebruikt om alleen verkoopbare producten te exporteren. Verkoopbare producten zijn producten die de informatie bevatten die ze nodig hebben om te kunnen worden gebruikt in een verkooporder. Dezelfde regels zijn van toepassing wanneer een product wordt gevalideerd met de functie **Valideren** op de pagina **Vrijgegeven producten**. |
| Vrijgegeven verschillende producten V2 | EcoResDistinctProductV2Entity | Deze entiteit wordt gebruikt om verschillende producten te exporteren. Deze verschillende producten kunnen, producten, subtypeproducten en productvarianten zijn. |
| Vrijgegeven productmodellen V2 | EcoResProductMasterV2Entity | Deze entiteit wordt gebruikt voor het importeren en exporteren van productmodellen. De entiteit is niet geschikt voor gegevensbeheer. |
| Artikel - streepjescode | EcoResProductBarcodeEntity | Deze entiteit wordt gebruikt om producten en streepjescodes te exporteren. |
| Statussen van productlevenscyclus | EcoResProductLifecycleSateEntity | Deze entiteit wordt gebruikt voor het importeren en exporteren van de verschillende levenscyclusstatussen die kunnen worden toegewezen aan een product. |

> [!NOTE]
> U kunt de gegevensentiteit **Vrijgegeven producten V2** alleen gebruiken om producten in het systeem te importeren als het gedeelde product al is gemaakt. Anders moet u de gegevensentiteit **Product maken** gebruiken om producten in het systeem te importeren.

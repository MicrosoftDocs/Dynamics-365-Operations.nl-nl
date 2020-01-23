---
title: Conversie van maateenheid per productvariant
description: In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935094"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Conversie van maateenheid per productvariant

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten. Het bevat een voorbeeld van de instellingen.

Met deze functie kunnen bedrijven verschillende eenheidconversies tussen de varianten van hetzelfde product definiëren. Het volgende voorbeeld wordt gebruikt in dit onderwerp. Een bedrijf verkoopt T-shirts in de maten Small, Medium, Large en Extra large. Het T-shirt is gedefinieerd als een product en de verschillende maten zijn gedefinieerd als varianten van het product. De T-shirts zijn verpakt in dozen en er passen vijf T-shirts in een doos, met uitzondering van de T-shirts met de maat Extra large, waarvan er maar vier passen in een doos. Het bedrijf wil de verschillende varianten van de T-shirts in de eenheid **Stuks** bijhouden, maar verkoopt de T-shirts in de eenheid **Dozen**. De conversie tussen de voorraadeenheid en de verkoopeenheid is 1 doos = 5 stuks, met uitzondering van de variant Extra large waarvoor de conversie 1 doos = 4 stuks geldt.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Een product voor eenheidconversie per variant instellen

Productvarianten kunnen alleen worden gemaakt voor producten van het **productsubtype** **Productmodel**. Zie [Een productmodel maken](tasks/create-product-master.md) voor meer informatie.

De functie is niet ingeschakeld voor producten die zijn ingesteld voor processen van het type Variabel gewicht. 

Wanneer het productmodel met vrijgegeven productvarianten is gemaakt, kunnen eenheidconversies per variant worden ingesteld. U kunt het menu-item voor het openen van de pagina voor eenheidconversie in de context van een product of productvariant vinden op de volgende pagina's.

-   De pagina **Productgegevens**
-   De pagina **Details van vrijgegeven producten**
-   De pagina **Vrijgegeven productvarianten**

Wanneer u de pagina **Eenheidsomrekening** in de context van een productmodel of vrijgegeven productvariant opent, kunt u opgeven of u de eenheidconversie voor het product of een productvariant wilt instellen. U doet dit door **Productvariant** of **Product** te selecteren in het veld **Conversie maken voor**.

### <a name="product-variant"></a>Productvariant

Als u **Productvariant** selecteert, kunt u in het veld **Productvariant** opgeven voor welke variant u de eenheidconversie wilt instellen.

### <a name="product"></a>Artikel

Als u **Product** selecteert, kunt u een eenheidconversie instellen voor het productmodel. Deze eenheidconversie geldt voor alle productvarianten zonder gedefinieerde eenheidconversie.

### <a name="example"></a>Voorbeeld

Een productmodel, **T-Shirt**, heeft vier vrijgegeven productvarianten: Small, Medium, Large en Extra large. De T-shirts zijn verpakt in dozen en er passen vijf T-shirts in een doos, met uitzondering van de T-shirts met de maat Extra large, waarvan er maar vier passen in een doos.

Open eerst de pagina **Eenheidsomrekening** via de pagina met vrijgegeven productgegevens voor **T-shirt**.

Stel op de pagina **Eenheidsomrekening** de eenheidconversie voor de productvariant Extra large in.

| **Veld**             | **Instelling**             |
|-----------------------|-------------------------|
| Conversie maken voor | Productvariant         |
| Productvariant       | T-Shirt : : Extra large : : |
| Van eenheid             | Dozen                   |
| Factor                | 4                       |
| Naar eenheid               | Stuks                  |

Voor de vrijgegeven productvarianten Small, Medium en Large geldt dezelfde eenheidconversie tussen de eenheden Dozen en Stuks, wat betekent dat u de eenheidconversie voor deze productvarianten in het productmodel kunt definiëren.

| **Veld**             | **Instelling** |
|-----------------------|-------------|
| Conversie maken voor | Artikel     |
| Artikel               | T-shirt     |
| Van eenheid             | Dozen       |
| Factor                | 5           |
| Naar eenheid               | Stuks      |

### <a name="using-excel-to-update-the-unit-conversions"></a>De eenheidconversies bijwerken met Excel

Als een product veel productvarianten met verschillende eenheidsconversies heeft, is het verstandig om de eenheidsconversies van de pagina **Eenheidsconversie** te exporteren naar een Excel-werkblad, de conversies bij te werken en deze vervolgens weer te publiceren naar Supply Chain Mangement.

De optie voor het exporteren naar Excel en het publiceren van de bewerkingen naar Supply Chain Mangement. kan worden ingeschakeld via het menu-item **Openen in Microsoft Office** in het actievenster op de pagina **Eenheidsconversie**.

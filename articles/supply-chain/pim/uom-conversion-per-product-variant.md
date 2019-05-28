---
title: Conversie van maateenheid per productvariant
description: In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573229"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Conversie van maateenheid per productvariant

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten. Het bevat een voorbeeld van de instellingen.

Met deze functie kunnen bedrijven verschillende eenheidconversies tussen de varianten van hetzelfde product definiëren. Het volgende voorbeeld wordt gebruikt in dit onderwerp. Een bedrijf verkoopt T-shirts in de maten Small, Medium, Large en Extra large. Het T-shirt is gedefinieerd als een product en de verschillende maten zijn gedefinieerd als varianten van het product. De T-shirts zijn verpakt in dozen en er passen vijf T-shirts in een doos, met uitzondering van de T-shirts met de maat Extra large, waarvan er maar vier passen in een doos. Het bedrijf wil de verschillende varianten van de T-shirts in de eenheid **Stuks** bijhouden, maar verkoopt de T-shirts in de eenheid **Dozen**. De conversie tussen de voorraadeenheid en de verkoopeenheid is 1 doos = 5 stuks, met uitzondering van de variant Extra large waarvoor de conversie 1 doos = 4 stuks geldt.

## <a name="setup"></a>Instellen

U kunt de parameters configureren voor het gebruik van de functie voor producten die zijn ingeschakeld voor **Alle processen** of alleen voor het product dat is ingeschakeld voor **Magazijnprocessen**. Gebruik hiervoor de optie **Maateenheidconversies inschakelen** op de pagina **Productgegevensparameters instellen**.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Een product voor eenheidconversie per variant instellen

Productvarianten kunnen alleen worden gemaakt voor producten van het **productsubtype** **Productmodel**. Zie [Een productmodel maken](tasks/create-product-master.md) voor meer informatie.

De functie is niet ingeschakeld voor producten die zijn ingesteld voor processen van het type Variabel gewicht. 

Schakel tijdens het maken van een productmodel maateenheidconversie in met de optie **Maateenheidconversies inschakelen** op de pagina **Productdetails**.

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

Als een product veel productvarianten met verschillende eenheidconversies heeft, is het verstandig om de eenheidconversies van de pagina **Eenheidsomrekening** te exporteren naar een Excel-werkblad, de conversies bij te werken en deze vervolgens weer te publiceren naar Finance and Operations.

De optie voor het exporteren naar Excel en het publiceren van de bewerkingen naar Finance and Operations kan worden ingeschakeld via het menu-item **Openen in Microsoft Office** in het actievenster op de pagina **Eenheidsomrekening**.

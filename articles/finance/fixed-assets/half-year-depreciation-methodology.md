---
title: Methodologie van afschrijvingsconventie van een half jaar
description: In dit onderwerp wordt beschreven welke methode voor vaste activa wordt gebruikt om de afschrijving te berekenen op basis van de conventie van een half jaar, waarmee zes maanden van afschrijving wordt berekend tijdens het eerste en laatste jaar van gebruik van het activum.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441824"
---
# <a name="half-year-depreciation-convention-methodology"></a>Methodologie van afschrijvingsconventie van een half jaar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt beschreven welke methode voor vaste activa wordt gebruikt om afschrijving te berekenen op basis van de conventie van een half jaar. De conventie van een half jaar berekent zes maanden afschrijving gedurende het eerste en laatste gebruiksjaar van het activum. Zie voor meer informatie [Afschrijvingsmethoden en conventies](Fixed-asset-depreciation-conventions.md). 

Wanneer u de afschrijvingsconventie van zes maanden gebruikt, gebruikt het systeem het aankoopjaar of het jaar waarin het activum in gebruik is genomen, worden de vijf jaar afschrijving vanaf dat jaar berekend en worden er vervolgens zes maanden bij opgeteld. Stel dat een activum is aangeschaft voor de prijs van 50.000 en in gebruik is genomen in april 2020. Stel daarnaast dat het activum een levensduur van vijf jaar heeft.

Het eerste jaar wordt afgesloten in december 2020, wat betekent dat het einde van de levensduur van vijf jaar in december 2024 is. De afschrijvingsconventie van een half jaar telt zes maanden op bij de levensduur van het activum, wat betekent dat de levensduur van het activum eindigt op 2025 juni. 

> Jaarlijkse afschrijving 50.000/5 = 10.000 maandelijkse afschrijving 10.000/12 = 833,33 <br>
> Afschrijving eerste jaar 10.000/2 = 5.000 en de volgende maandelijkse afschrijving 5000/9 = 555,56

   [![Afschrijvingsschema voor afschrijvingsconventie van half jaar](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

De uitgebreide afschrijvingsperioden die door de conventie van een half jaar worden toegevoegd, bieden een meer nauwkeurige toewijzing van afschrijving. De conventie van zes maanden resulteert in gelijkmatigere afschrijvingskosten, wat handig is voor rapportage over winst- en verliesrekening.

---
title: Een toevoeging aan een vast activum invoeren
description: Deze procedure laat zien hoe u een toevoeging aan een bestaand vast activum toevoegt.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc1e13863ae13daaa641f52f7a55e01fc1353dc1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441976"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Een toevoeging aan een vast activum invoeren

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een toevoeging aan een bestaand vast activum toevoegt. Het doel van vaste-activatoevoegingen is artikeltoevoegingen, onderhoud, of verbeteringen voor een activum bij te houden, en is alleen ter informatie. Eventuele wijzigingen in de waarde van de vaste activa of levensduur moeten afzonderlijk worden gemaakt.   

De procedure gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.

1. Ga in het navigatievenster naar **Modules > Vaste activa > Vaste activa > Vaste activa**.
2. Zoek en selecteer in de lijst het vaste activum voor de toevoeging.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het actievenster op **Vaste activa**.
5. Klik op **Toevoegingen van vaste activa**.
6. Klik op **Nieuw**.
7. Typ een waarde in het veld **Naam**.
8. Stel in het veld **Verwervingsdatum** de datum van de toegevoegde aankoop of service in.
9. Voer in het veld **Eenheidskosten** de kosten van het artikel, het onderhoud of andere verbeteringen voor het activum in.
10. Voer een getal in het veld **Hoeveelheid** in. De totale kosten hebben geen gevolg voor de waarde van vaste activa en zijn voor tracering en ter informatie. Als de kosten worden gekapitaliseerd, moet een opwaarderingscorrectietransactie apart worden geboekt.  
11. Klik op het tabblad **Algemeen**.

    * Stel **Hiermee wordt de levensduur verlengd** in op **Ja** als de levensduur van de vaste activa toeneemt door de toevoeging.  
    * Dit veld is alleen ter informatie. Als u de levensduur wilt verlengen, wijzigt u de levensduur in de waardemodellen en/of afschrijvingsboeken voor het activum.  


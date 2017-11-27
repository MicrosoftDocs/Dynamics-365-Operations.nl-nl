---
title: Boeken met afgeleide boeken
description: In dit artikel wordt beschreven hoe u afgeleide boeken gebruikt.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 94eb82936da2a51a25105b26723088fb7dee9ae5
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="post-with-derived-books"></a>Boeken met afgeleide boeken

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u afgeleide boeken gebruikt.

Wanneer u transacties boekt voor een boek dat afgeleide afschrijvingsboeken bevat, worden transacties met afgeleide boeken automatisch in journalen, inkooporders of vrije-tekstfacturen geboekt. Als u echter de transacties voor het primaire boek in het journaal Vaste activa gereedmaakt, kunt u de bedragen van de afgeleide transacties bekijken en wijzigen voordat u ze boekt.
-   Bepaalde bedragen, zoals btw en de klant- en leveranciersrekeningen, worden slechts één keer bijgewerkt door boekingen van het primaire boek. De transacties met afgeleide boeken worden naar de rekeningen geboekt die voor het afgeleide boek in de pagina Boekingsprofielen voor vaste activa zijn opgegeven.
-   Verwerving wordt vaak gebruikt als het transactietype voor de afgeleide boeken. U gebruikt dit transactietype wanneer het boek en het afgeleide boek vanaf de tijd van de verwerving van de vaste activa op de vaste activa moeten worden toegepast.
-   Andere waarden voor het transactietype kunnen ook worden toegepast. Als bijvoorbeeld het primaire boek en de afgeleide boeken dezelfde intervallen voor verkoop of afboeking hebben, kunnen alle typen vaste-activatransacties worden gebruikt bij het instellen van een afgeleid boek.

> [!WARNING]
> De afschrijving die in het afgeleide boek is geboekt, wordt hetzelfde bedrag als het bedrag dat voor het primaire boek is geboekt. Als de afschrijvingsmethoden bij de boeken verschillen, moet u geen afschrijvingstransacties met behulp van het afgeleide proces genereren. |

## <a name="example"></a>Voorbeeld 
Hieronder wordt beschreven hoe u verwervingsmethoden instelt met de functionaliteit van het afgeleide boek.

1.  Maak de boeken op de pagina Boeken.
    -   Het boek voor boekhouding: VM 1, huidige boekingslaag
    -   Het boek voor belasting: VM 2, boekingslaag belasting

2.  Klik voor VM 1 op het tabblad Afgeleide boeken. Selecteer VM 2 in het veld Boek en Verwerving in het veld Transactietype.

De boeken kunnen aan een specifieke vaste activa worden gekoppeld. 

Wanneer een verwerving wordt geboekt voor een vast activum met boek VM 1, wordt de verwerking niet alleen op VM 1, maar ook op het afgeleide afgeleide boek VM 2 geboekt. De status van beide vaste-activaboeken wordt gewijzigd in Open.

> [!NOTE]                                                                                                         
> Als u geen afgeleide boeken gebruikt, moet u de verwerving van de vaste activa voor zowel boek VM 1 als voor boek VM 2 afschrijven.

Zie voor meer informatie [Afgeleide boeken](derived-books.md).





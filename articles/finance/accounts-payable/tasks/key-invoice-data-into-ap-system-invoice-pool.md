---
title: Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep
description: In dit onderwerp wordt beschreven hoe u het facturenregister gebruikt om facturen te maken.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf781089469f87dc0a98279003c94fd1e8bf9dbe
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717329"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u het facturenregister gebruikt om facturen te maken. Gebruik vervolgens de facturenpool om de factuur af te stemmen op een inkooporder en de onkosten te finaliseren op de pagina voor leveranciersfacturen.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Inkooporders**.
2. Selecteer **Nieuw** om een inkooporder te maken.
3. Selecteer in het veld **Leverancierrekening** de vervolgkeuzelijst om een leverancier te selecteren. Selecteer bijvoorbeeld leverancier **1001**.
4. Selecteer **OK**.
5. Selecteer in het veld **Artikelnummer** de het artikelnummer van de service in de vervolgkeuzelijst. Selecteer bijvoorbeeld **S0001**. Het nettobedrag is 75,00.  Dat is het bedrag dat we verwachten op de factuur.  
6. Selecteer in het actievenster de optie **Inkoop**.
7. Selecteer **Bevestigen**.

## <a name="create-and-post-and-invoice"></a>Een factuur maken en boeken
1. Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Facturenregister**.
2. Selecteer **Nieuw**.
3. Open de zoekopdracht om de naam te selecteren van het facturenregister dat u wilt gebruiken.
4. Selecteer de naam van het facturenregister dat u wilt gebruiken.
5. Selecteer **Regels** om het register te openen en onkostenregels in te voeren.
6. Selecteer een leverancier in de zoekopdracht. Selecteer bijvoorbeeld leverancier **1001**.
7. Voer in het veld **Factuur** het factuurnummer in.
8. Typ een waarde in het veld **Beschrijving**.
9. Voer in het veld **Krediet** een numerieke waarde in.
10. Open in het veld **Inkooporder** de vervolgkeuzelijst om de inkooporder te selecteren die u eerder hebt gemaakt.
11. Markeer in het veld **Goedgekeurd door** een fiatteur in de vervolgkeuzelijst en klik op **Selecteren** om die fiatteur te selecteren.
12. Selecteer **Boeken**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Open een factuur vanuit de pool en vereffen deze met een inkooporder om het factureringsproces te voltooien
1. Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Facturenpool**.
2. Selecteer **Inkooporder** om een leveranciersfactuur te maken op basis van de factuur in de pool.
3. Selecteer de factuur die u wilt bekijken.
4. Selecteer **Vereffeningsstatus bijwerken** om de vereffening te voltooien.
5. Selecteer **Opties** in het actievenster.
6. Selecteer **Weergave wijzigen**.
7. Selecteer **Rasterweergave**.
8. Selecteer **Boeken**.
9. Sluit de pagina.
10. Ga in het navigatievenster naar **Modules > Leveranciers > Leveranciers > Leveranciers**.
11. Selecteer de leverancier die op de inkooporder staat vermeld. Selecteer bijvoorbeeld leverancier **1001**.
12. Selecteer **Leverancier** in het Actievenster.
13. Selecteer **Transacties**.
14. Selecteer de factuur die u hebt gemaakt. De toerekening van het facturenregister is omgekeerd en geboekt naar de juiste onkostenrekening.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Garanties op activa en activatypen
description: In dit artikel wordt uitgelegd hoe u garanties op activa en activatypen kunt instellen in Activabeheer.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fa4fe7af46996e8de76ea61d5395327e7617e736
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906119"
---
# <a name="warranties-on-assets-and-asset-types"></a>Garanties op activa en activatypen

[!include [banner](../../includes/banner.md)]

 


In dit artikel wordt uitgelegd hoe u garanties op activa en activatypen kunt instellen in Activabeheer.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Garantie voor activatypen instellen

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activatypen** \> **Activatypen**.
2. Selecteer in het linkerdeelvenster het activatype waaraan u een leveranciersgarantieovereenkomst wilt koppelen en selecteer vervolgens **Standaardwaarden van activatype**.
3. Selecteer de overeenkomst in het veld **Leveranciersgarantie** van het sneltabblad **Algemeen**.

## <a name="set-up-a-warranty-on-an-asset"></a>Garantie voor een activum instellen

1. Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**.
2. Selecteer het activum en selecteer vervolgens **Bewerken**.
3. Selecteer de garantieovereenkomst in de sectie **Leveranciersgarantie** van het sneltabblad **Leverancier** in het veld **Garantie**.
4. Selecteer in de velden **Begindatum garantie** en **Einddatum garantie** de begin- en einddatums.

    > [!IMPORTANT]
    > Als een datum is geselecteerd in het veld **Begindatum garantie** voor een werkorder, wordt de garantie geldig voor de werkorder op die datum. Wanneer u een werkorder maakt, wordt het veld **Begindatum garantie** automatisch ingesteld op de datum van aanmaak. U kunt de datum echter wijzigen, zodat deze overeenkomt met bijvoorbeeld de begindatum van een garantieovereenkomst.
    >
    > ![Pagina Werkorder.](media/02-warranty.png)

> [!NOTE]
> Wanneer u een werkorder maakt voor een activum dat wordt gedekt door een garantie van een leverancier, ontvangt u een melding over de garantieovereenkomst als de werkorder een verwachte begindatum heeft gedurende de garantieperiode. U kunt de werkorder vervolgens desgewenst annuleren.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
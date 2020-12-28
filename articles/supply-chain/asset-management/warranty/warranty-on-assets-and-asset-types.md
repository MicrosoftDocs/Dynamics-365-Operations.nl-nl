---
title: Garanties op activa en activatypen
description: In dit onderwerp wordt uitgelegd hoe u garanties op activa en activatypen kunt instellen in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 75de9a51560dcd8fea7998425fee14a27e891972
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425582"
---
# <a name="warranties-on-assets-and-asset-types"></a>Garanties op activa en activatypen

[!include [banner](../../includes/banner.md)]

 


In dit onderwerp wordt uitgelegd hoe u garanties op activa en activatypen kunt instellen in Activabeheer.

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
    > ![Pagina Werkorder](media/02-warranty.png)

> [!NOTE]
> Wanneer u een werkorder maakt voor een activum dat wordt gedekt door een garantie van een leverancier, ontvangt u een melding over de garantieovereenkomst als de werkorder een verwachte begindatum heeft gedurende de garantieperiode. U kunt de werkorder vervolgens desgewenst annuleren.

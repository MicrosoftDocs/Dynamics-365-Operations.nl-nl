---
title: Boekstuk is niet gegenereerd
description: Dit onderwerp bevat informatie voor het oplossen van problemen wanneer een boekstuk gegenereerd had moeten worden maar dat niet is gebeurd.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eb45b79fa710699cfa267e7c6359ba3ce761d62d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693222"
---
# <a name="voucher-isnt-generated"></a>Boekstuk is niet gegenereerd

[!include [banner](../includes/banner.md)]

Als er een boekstuk moet worden gegenereerd maar op de pagina **Boekstuktransacties** wordt geen boekstuk weergegeven, volgt u de stappen in de volgende secties die nodig zijn om dit probleem op te lossen.

[![Pagina met boekstuktransacties zonder boekstuk.](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Controleer de toepasbaarheid van de belasting

1. Ga naar **Belasting** \> **Periodieke taken** \> **Nog niet overgeboekte journaalposten in subadministratie**.
2. Als er een journaalrecord is, selecteert u deze en vervolgens selecteert u **Nu overboeken**.

    [![Knop Nu overboeken op de pagina Nog niet overgeboekte journaalposten in subadministratie.](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Open de pagina **Boekstuktransacties** opnieuw om te bekijken of het boekstuk werd gegenereerd.

## <a name="determine-whether-customization-exists"></a>Bekijk of er een aanpassing bestaat

Als u de stappen in de vorige sectie hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat. Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

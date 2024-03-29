---
title: Algemene bronbelasting
description: Dit artikel biedt informatie over de functionaliteit voor algemene bronbelasting en over het instellen ervan. De functionaliteit voor algemene bronbelasting is verbeterd voor leveranciers- en klanttransacties, zodat bronbelasting wordt berekend op artikelniveau.
author: kailiang
ms.date: 01/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 49d5048b9df30e94d959cf9f22b8ae837b74abdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846823"
---
# <a name="global-withholding-tax"></a>Algemene bronbelasting

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over de functionaliteit voor algemene bronbelasting en legt uit hoe u deze instelt. De nieuwe functionaliteit is beschikbaar in versie 10.0.17 en hoger.

De functionaliteit voor algemene bronbelasting is verbeterd voor leveranciers- en klanttransacties, zodat bronbelasting wordt berekend op artikelniveau. Het saldo op de bronbelastingrekening van inkooptransacties kan worden vereffend door de taak voor bronbelastingbetaling uit te voeren tegen de vereffeningsrekening voor bronbelasting.

> [!NOTE]
> Algemene bronbelasting ondersteunt niet de functie **Toeslagen onderhouden** op de inkooporder-, leveranciersfactuur- en verkooporderpagina's.

## <a name="turn-on-global-withholding-tax"></a>Algemene bronbelasting inschakelen

1. Selecteer in de werkruimte **Functiebeheer** de optie **Algemene bronbelasting** en selecteer **Nu inschakelen**.
2. Ga naar **Belasting \> Instellen \> Parameters \> Grootboekparameters** en stel op het tabblad **Bronbelasting** de optie **Algemene bronbelasting** in op **Ja**.
3. Selecteer **Opslaan**.
4. Vernieuw de pagina in de webbrowser.

> [!NOTE]
> De functionaliteit voor algemene bronbelasting kan niet worden ingeschakeld voor landen/regio's waar al lokale bronbelastingoplossingen bestaan. Deze gebieden zijn onder andere, maar niet uitsluitend India, Brazilië, Thailand, Saudi-Arabië, Ierland, Groot-Brittannië en de Verenigde Staten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

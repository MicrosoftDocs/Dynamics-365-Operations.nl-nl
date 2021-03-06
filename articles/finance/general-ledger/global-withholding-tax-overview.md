---
title: Algemene bronbelasting
description: Dit onderwerp biedt informatie over de functionaliteit voor algemene bronbelasting en over het instellen ervan. De functionaliteit voor algemene bronbelasting is verbeterd voor leveranciers- en klanttransacties, zodat bronbelasting wordt berekend op artikelniveau.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9a73d34fb4fbf007cbb5a996cfa6e9719532869c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826661"
---
# <a name="global-withholding-tax"></a>Algemene bronbelasting

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over de functionaliteit voor algemene bronbelasting en legt uit hoe u deze instelt. De nieuwe functionaliteit is beschikbaar in versie 10.0.17 en hoger.

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
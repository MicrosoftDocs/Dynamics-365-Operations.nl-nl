---
title: TDS berekenen voor intercompany-transacties
description: Dit artikel beschrijft het proces dat wordt gebruikt om belasting ingehouden op bron (TDS) te berekenen op intercompany-transacties in fasen.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c27bea997804f2c5eff6be2b20064b272ccd062f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888968"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS berekenen voor intercompany-transacties

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft het proces dat wordt gebruikt om belasting ingehouden op bron (TDS) te berekenen op intercompany-transacties in fasen.

Wanneer een intercompany-inkooporder of -verkooporder wordt gemaakt, wordt de standaard-TDS-groep die voor de klant of leverancier is gedefinieerd gebruikt om het TDS-bedrag te berekenen. Het TDS-bedrag wordt geboekt naar de rekening voor terug te vorderen of te betalen nadat de factuur is geboekt.

Voor de oorspronkelijke inkoop- of verkooporder wordt automatisch een intercompany-verkooporder of -inkooporder gemaakt. De standaard-TDS-groep wordt weergegeven op de intercompany-order, zodat TDS kan worden berekend. U kunt de TDS-groep wijzigen. De factuur kan alleen worden geboekt als het nettofactuurbedrag op de intercompany-order die automatisch wordt gemaakt, overeenkomt met het nettofactuurbedrag op de oorspronkelijke order. (Het nettobedrag is het factuurbedrag nadat TDS is ingehouden.)

Er wordt bijvoorbeeld een verkoopfactuur van 50.000 gemaakt en daar is de TDS-groep van **10%** aan gekoppeld. Het geboekte factuurbedrag is 45.000 en het geboekte TDS-bedrag voor de verkoopfactuur is 5.000. Er wordt automatisch een inkooporder gemaakt voor de intercompany-verkooporder en de TDS-groep van **10%** wordt eraan gekoppeld. Als u de TDS-groep wijzigt in **15%**, kunt u de factuur niet boeken, omdat het nettofactuurbedrag van de intercompany-verkooporder die automatisch is gemaakt, niet gelijk is aan het nettofactuurbedrag van de oorspronkelijke verkooporder.

Er wordt automatisch een betalingsjournaal geboekt dat voor een intercompany-factuur is gemaakt. Dat betalingsjournaal kan alleen worden geboekt als het nettobetalingsbedrag hier overeenkomt met het nettobetalingsbedrag in het oorspronkelijke betalingsjournaal.

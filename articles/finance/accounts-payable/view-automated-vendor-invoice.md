---
title: Resultaten van de automatisering van leveranciersfacturering weergeven (preview)
description: In dit onderwerp wordt uitgelegd hoe u de status van leveranciersfacturen kunt weergeven die zich in het geautomatiseerde proces voor indiening bij de werkstroom bevinden.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 872ec404da0cce41c4ea0f882a3fa8af56316ce3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837220"
---
# <a name="view-vendor-invoice-automation-results"></a>Resultaten van de automatisering van leveranciersfacturering weergeven

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de status van leveranciersfacturen kunt weergeven die zich in het geautomatiseerde proces voor indiening bij de werkstroom bevinden. Details van de automatiseringsgeschiedenis worden bijgehouden voor elke geïmporteerde leveranciersfactuur. Afhankelijk van de bedrijfsprocessen die u hebt geautomatiseerd, worden op de pagina **Leveranciersfacturen in behandeling** de waarden **Afstemmingsstatus van automatische ontvangst** en **Automatisch indienen bij werkstroomstatus** weergegeven. U kunt de details bekijken en een plan maken om zich te concentreren op de facturen waarvoor een geautomatiseerde stap is mislukt. Nadat u het probleem hebt opgelost, kunt u het geautomatiseerde proces voor de geïmporteerde factuur hervatten.

Voordat u een factuur kunt bewerken die is ingediend, moet u de geautomatiseerde verwerking onderbreken. Als een factuur in het geautomatiseerde proces voor indiening bij de werkstroom moet worden onderbroken, stelt u het veld **Opnemen in geautomatiseerde verwerking** in op **Nee** op de pagina **Leveranciersfacturen**. Automation wordt vervolgens pas uitgevoerd als **Opnemen in geautomatiseerde verwerking** is ingesteld op **Ja**. Een factuur kan worden onderbroken voor verdere automatisering als deze nog niet in het werkstroomsysteem is opgenomen en niet wordt gebruikt door het geautomatiseerde proces.

Als een geïmporteerde factuur afhankelijk is van het proces voor indiening bij de werkstroom, kunt u de waarde **Automatiseringsstatus** weergeven op de pagina **Leveranciersfacturen**. De volgende statussen worden bijgehouden:

- **Opgenomen**: de geautomatiseerde processen die op de pagina **Parameters van module Leveranciers** zijn gedefinieerd, worden correct uitgevoerd, maar zijn nog niet voltooid.
- **Onderbroken**: de geautomatiseerde processen die zijn gedefinieerd op de pagina **Parameters van module Leveranciers** zijn uitgevoerd, maar ten minste één stap in het proces is mislukt. De status **Onderbroken** wordt ook toegepast als het veld **Opnemen in geautomatiseerde verwerking** is ingesteld op **Nee**. U kunt de fouten weergeven door **Meest recente resultaten weergeven** te selecteren.
- **In werkstroom**: de geïmporteerde factuur is bij het werkstroomsysteem ingediend via het geautomatiseerde proces voor indiening bij de werkstroom of handmatig.
- **Werkstroom voltooid**: het werkstroomproces is voltooid voor de geïmporteerde factuur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
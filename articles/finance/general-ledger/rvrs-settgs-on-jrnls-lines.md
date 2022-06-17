---
title: Terugboekingsinstellingen voor journalen en regels
description: In dit artikel wordt aangegeven waarom een ingevoerde stornopost in een journaal mogelijk niet wordt opgenomen in de geboekte transactie.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e36a3ea1736e4d7f60a5a6ce588ad3e66c950c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899837"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Terugboekingsinstellingen voor journalen en regels

[!include [banner](../includes/banner.md)]

In dit artikel wordt aangegeven waarom een ingevoerde stornopost in een journaal mogelijk niet wordt opgenomen in de geboekte transactie.  

## <a name="symptom"></a>Symptoom

Een journaal bevat een stornopost en -datum. Wanneer u het journaal boekt, wordt geen van de boekstukken teruggeboekt. Waarom gebeurt dit?

## <a name="resolution"></a>Oplossing

Wanneer het journaal wordt geboekt, wordt in het terugboekingsproces alleen gekeken naar de instellingen **Stornopost** en **Stornodatum** in de sectie **Regels** van het boekstuk. Bij deze aanpak kan een journaal enkele boekstukken bevatten die zijn gemarkeerd voor terugboeken en andere boekstukken waarvoor dit niet geldt.

De waarden uit het journaal worden alleen als standaardinstellingen gebruikt bij het toevoegen van *nieuwe* regels. Als u de waarden in het journaal wijzigt, heeft dit geen invloed op bestaande regels. In dit voorbeeld zijn de boekstukregels eerst ingevoerd. Wanneer u de regeldetails invoert voordat u het journaal aanduidt als stornojournaal, wordt de aanduiding als stornopost en stornodatum niet toegepast op bestaande regels.

Als u de stornopost of -datum op een bestaande regel wijzigt, worden die wijzigingen doorgegeven aan andere regels in hetzelfde boekstuk. Om de prestaties te optimaliseren, wordt het raster niet vernieuwd nadat wijzigingen zijn doorgegeven aan andere regels. U kunt de bijgewerkte waarden weergeven door het raster te vernieuwen.



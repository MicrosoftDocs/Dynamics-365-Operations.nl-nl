---
title: Terugboekingsinstellingen voor journalen en regels
description: In dit onderwerp wordt aangegeven waarom een ingevoerde stornopost in een journaal mogelijk niet wordt opgenomen in de geboekte transactie.
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
ms.openlocfilehash: ff8c0bda8e750e95261039b373cfb96a76034f6f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724440"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Terugboekingsinstellingen voor journalen en regels

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt aangegeven waarom een ingevoerde stornopost in een journaal mogelijk niet wordt opgenomen in de geboekte transactie.  

## <a name="symptom"></a>Symptoom

Een journaal bevat een stornopost en -datum. Wanneer u het journaal boekt, wordt geen van de boekstukken teruggeboekt. Waarom gebeurt dit?

## <a name="resolution"></a>Oplossing

Wanneer het journaal wordt geboekt, wordt in het terugboekingsproces alleen gekeken naar de instellingen **Stornopost** en **Stornodatum** in de sectie **Regels** van het boekstuk. Bij deze aanpak kan een journaal enkele boekstukken bevatten die zijn gemarkeerd voor terugboeken en andere boekstukken waarvoor dit niet geldt.

De waarden uit het journaal worden alleen als standaardinstellingen gebruikt bij het toevoegen van *nieuwe* regels. Als u de waarden in het journaal wijzigt, heeft dit geen invloed op bestaande regels. In dit voorbeeld zijn de boekstukregels eerst ingevoerd. Wanneer u de regeldetails invoert voordat u het journaal aanduidt als stornojournaal, wordt de aanduiding als stornopost en stornodatum niet toegepast op bestaande regels.

Als u de stornopost of -datum op een bestaande regel wijzigt, worden die wijzigingen doorgegeven aan andere regels in hetzelfde boekstuk. Om de prestaties te optimaliseren, wordt het raster niet vernieuwd nadat wijzigingen zijn doorgegeven aan andere regels. U kunt de bijgewerkte waarden weergeven door het raster te vernieuwen.



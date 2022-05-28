---
title: Redencodes voor de gebruiksfase
description: U gebruikt een redencode om aan te geven waarom een SLA (Service Level Agreement) is geannuleerd of waarom een serviceorder de tijdslimiet die u in de SLA hebt gedefinieerd, heeft overschreden.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06c2b6a2b338dbfdbecdeb75e12fa1c20af8e56d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669511"
---
# <a name="use-stage-reason-codes"></a>Redencodes voor de gebruiksfase 

[!include [banner](../includes/banner.md)]


U gebruikt een redencode om aan te geven waarom een SLA (Service Level Agreement) is geannuleerd of waarom een serviceorder de tijdslimiet die u in de SLA hebt gedefinieerd, heeft overschreden.

U kunt ook opgeven dat een redencode vereist is wanneer een SLA wordt geannuleerd, of wanneer de tijdslimiet de tijd overschrijdt die is opgegeven in de SLA voor de serviceorder.

Als u hebt opgegeven dat een redencode vereist is, moet u een redencode invoeren in de volgende situaties:

  - Wanneer de serviceorder wordt verplaatst naar een fase waarin de tijdregistratie van de SLA wordt gestopt voor de serviceorder.

  - Wanneer de serviceorder wordt afgemeld.

  - Wanneer de tijdregistratie handmatig wordt gestopt.

## <a name="set-up-reason-codes"></a>Redencodes instellen

1.  Klik op **Servicebeheer** \> **Instellen** \> **Serviceorders** \> **Redencodes voor fase**.

2.  Klik in het formulier **Redencode voor de fase** op **Nieuw** om een nieuwe redencode te maken.

3.  Voer in het veld **Redencode voor de fase** een unieke redencode voor de fase in.

4.  Voer in het veld **Beschrijving** een omschrijving van de redencode voor de fase in.

5.  Sluit het formulier om de wijzigingen op te slaan.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Redencodes vereisen wanneer een SLA wordt geannuleerd

1.  Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.

2.  Klik in het formulier **Parameters voor servicebeheer** op de koppeling **Algemeen** en schakel vervolgens het selectievakje **Redencode bij annuleren** in.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Redencodes vereisen wanneer een serviceorder de ingestelde tijdslimiet voor de SLA overschrijdt

1.  Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.

2.  Klik in het formulier **Parameters voor servicebeheer** op de koppeling **Algemeen** en schakel vervolgens het selectievakje **Redencode bij overschrijden van tijd** in.

## <a name="see-also"></a>Zie ook

[Tijdregistratie voor een serviceorder starten en stoppen](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
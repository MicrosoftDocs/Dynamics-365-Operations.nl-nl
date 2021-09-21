---
title: De standaardbelastinggroep en de contantkorting worden niet ingevuld vanuit het factureringsaccount
description: Een standaardbelastinggroep en een standaardcontantkorting worden niet ingevuld vanuit het factureringsaccount
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476005"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>De standaardbelastinggroep en de contantkorting worden niet ingevuld vanuit het factureringsaccount

## <a name="symptoms"></a>Symptomen

Als u een factuurrekening gebruikt die verschilt van de klantrekening, worden er geen standaardbelastinggroep en standaardcontantkorting ingevuld op basis van de factuurrekening wanneer er een inkooporder wordt gemaakt.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. De standaardwaarden voor de belastinggroep, contantkortingen en andere prijsgegevens zijn gebaseerd op de klantrekening, niet op de factuurrekening.

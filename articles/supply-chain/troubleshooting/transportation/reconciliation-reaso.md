---
title: U kunt om afstemmingsredenen alleen de hoofdrekening als de creditrekening toevoegen
description: Wanneer u in Transportbeheer een afstemmingsreden in stelt, kunt u alleen de hoofdrekening als de creditrekening toevoegen.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026391"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>U kunt om afstemmingsredenen alleen de hoofdrekening als de creditrekening toevoegen

KB-nummer: 4603538

## <a name="symptoms"></a>Symptomen

Wanneer u in Transportbeheer een afstemmingsreden in stelt, kunt u alleen de hoofdrekening als de creditrekening toevoegen. U kunt geen kostenplaats of een andere dimensie toevoegen als de creditrekening. Met de debetrekening kunt u echter andere dimensies selecteren.

## <a name="resolution"></a>Oplossing

Als het afstemmingsproces niet is uitgevoerd om de leverancier te betalen maar een bepaalde hoofdrekening te crediteren, staat het systeem u niet toe om een financiële dimensie voor de creditrekening te selecteren wanneer u de afstemmingsreden instelt.

Als voor de rekeningstructuur een specifieke waarde voor de financiële dimensie nodig is voor de credithoofdrekening, kan het resulterende leveranciersjournaal niet automatisch worden geboekt, omdat de waarde voor de financiële dimensie ontbreekt. Daarom moet u de creditrekening eerst handmatig opgeven via de pagina **Factuurjournaal**.

Omdat er een dimensiewaarde vereist is voor de creditrekening, kan het leveranciersfactuurjournaal niet automatisch worden geboekt. U moet dit handmatig doen nadat u de dimensiewaarde handmatig aan de hoofdrekening voor de creditregel hebt toegevoegd.

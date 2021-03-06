---
title: Door het omkeren van de gereedmelding wordt een onverwachte openstaande transactie gemaakt
description: Door het omkeren van gereedmelding met markering wordt een openstaande transactie gemaakt waarin de omgekeerde hoeveelheid dezelfde voorraaddimenssies heeft als de omgekeerde transactie.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026417"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Door het omkeren van de gereedmelding wordt een onverwachte openstaande transactie gemaakt

KB-nummer: 4612469

## <a name="symptoms"></a>Symptomen

Door het omkeren van gereedmelding met markering wordt een openstaande transactie gemaakt waarin de omgekeerde hoeveelheid dezelfde voorraaddimenssies heeft als de omgekeerde transactie.

## <a name="resolution"></a>Oplossing

Wanneer u een gereedmeldingsbewerking omkeert, wordt de voorraaddimensie vanuit het productiejournaal geïnitialiseerd. Daarom krijgt deze het batchnummer. Vanwege de markering nemen de verkoopordertransacties het batchnummer over.

De dimensie kan opnieuw worden ingesteld wanneer de gereedgemelding wordt geboekt.

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
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714205"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Door het omkeren van de gereedmelding wordt een onverwachte openstaande transactie gemaakt

KB-nummer: 4612469

## <a name="symptoms"></a>Symptomen

Door het omkeren van gereedmelding met markering wordt een openstaande transactie gemaakt waarin de omgekeerde hoeveelheid dezelfde voorraaddimenssies heeft als de omgekeerde transactie.

## <a name="resolution"></a>Oplossing

Wanneer u een gereedmeldingsbewerking omkeert, wordt de voorraaddimensie vanuit het productiejournaal geïnitialiseerd. Daarom krijgt deze het batchnummer. Vanwege de markering nemen de verkoopordertransacties het batchnummer over.

De dimensie kan opnieuw worden ingesteld wanneer de gereedgemelding wordt geboekt.

---
title: Kan geen laadregel maken vanwege ongeldige voorraaddimensies
description: Wanneer u probeert een retourverkooporder vrij te geven naar het magazijn, wordt er mogelijk een foutbericht weergegeven over ongeldige voorraaddimenssie. Verwijder deze uit de orderregel.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476028"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Kan geen laadregel voor retourverkooporder maken vanwege ongeldige voorraaddimensies

## <a name="symptoms"></a>Symptomen

Wanneer u probeert een retourverkooporder vrij te geven aan het magazijn, ontvangt u mogelijk het volgende foutbericht:

> U kunt geen ladingsregel maken voor deze orderregel omdat deze voorraaddimensies bevat die ongeldig zijn. U kunt niet verwijzen naar voorraaddimensies die zich onder de locatiedimensie in de reserveringshiërarchie bevinden. Verwijder de ongeldige dimensies uit de orderregel.

## <a name="resolution"></a>Oplossing

Helaas ondersteunt het product geen ladingsverwerking voor een verkoopretourproces. Daarom kunt u de retourverkooporder niet vrijgeven aan het magazijn.

Op verkoopordertransacties kunt u niet verwijzen naar voorraaddimensies die zich onder de **Locatie**-dimensie in de reserveringshiërarchie bevinden. Verwijder de ongeldige dimensies uit de orderregel om het probleem op te lossen.

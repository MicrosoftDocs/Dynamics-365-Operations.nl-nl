---
title: Kan geen laadregel maken vanwege ongeldige voorraaddimensies
description: Wanneer u probeert een retourverkooporder vrij te geven naar het magazijn, wordt er mogelijk een foutbericht weergegeven over ongeldige voorraaddimenssie. Verwijder deze uit de orderregel.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119207"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Kan geen laadregel voor retourverkooporder maken vanwege ongeldige voorraaddimensies

## <a name="symptoms"></a>Symptomen

Wanneer u probeert een retourverkooporder vrij te geven aan het magazijn, ontvangt u mogelijk het volgende foutbericht:

> U kunt geen ladingsregel maken voor deze orderregel omdat deze voorraaddimensies bevat die ongeldig zijn. U kunt niet verwijzen naar voorraaddimensies die zich onder de locatiedimensie in de reserveringshiërarchie bevinden. Verwijder de ongeldige dimensies uit de orderregel.

## <a name="resolution"></a>Oplossing

Helaas ondersteunt het product geen ladingsverwerking voor een verkoopretourproces. Daarom kunt u de retourverkooporder niet vrijgeven aan het magazijn.

Op verkoopordertransacties kunt u niet verwijzen naar voorraaddimensies die zich onder de **Locatie**-dimensie in de reserveringshiërarchie bevinden. Verwijder de ongeldige dimensies uit de orderregel om het probleem op te lossen.

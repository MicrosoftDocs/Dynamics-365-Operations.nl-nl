---
title: U kunt een vrijgegeven product niet verwijderen
description: U kunt een vrijgegeven product en alle varianten alleen verwijderen als er geen transacties met betrekking tot het vrijgegeven product zijn.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476044"
---
# <a name="you-cant-delete-a-released-product"></a>U kunt een vrijgegeven product niet verwijderen

## <a name="symptoms"></a>Symptomen

U kunt een vrijgegeven product en alle varianten alleen verwijderen als er geen transacties met betrekking tot het vrijgegeven product zijn.

## <a name="resolution"></a>Oplossing

Voer de volgende stappen uit om een vrijgegeven product of productmodel te verwijderen.

1. Sluit alle openstaande transacties voor de artikelen.
1. Verminder de voorraad tot 0 (nul).
1. Voor een voorraadafsluiting uit.
1. Verwijder alle productvarianten voor het productmodel dat u wilt verwijderen.

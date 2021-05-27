---
title: U kunt een verkooporder voor de klant niet factureren
description: U kunt de oorspronkelijke verkooporder en de inkooporder voor directe levering niet meer factureren nadat u de optie Factuur automatisch boeken hebt ingeschakeld.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026401"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>U kunt een verkooporder voor de klant niet factureren

KB-nummer: 4611793

## <a name="symptoms"></a>Symptomen

U kunt de oorspronkelijke verkooporder en de inkooporder voor directe levering niet meer factureren nadat u de optie **Factuur automatisch boeken** hebt ingeschakeld op de pagina **Intercompany** voor een leverancier.

## <a name="resolution"></a>Oplossing

Het synchronisatiegedrag voor intercompany-facturen en facturen voor directe leveringsorders wordt gecontroleerd en verplicht gemaakt door de parameters die zijn beschreven in [Parameters instellen voor boeken naar een intercompany-order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Nadat u deze parameters hebt ingesteld, moet u eerst de intercompany-verkooporder factureren. De oorspronkelijke verkooporders en inkooporders worden vervolgens gesynchroniseerd.

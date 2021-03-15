---
title: Serviceorderfasen
description: Door de fasen voor een serviceorder te definiëren en deze aan werknemers toe te wijzen, controleert u de stroom van een serviceorder met de verschillende taken die mensen in de serviceorganisatie uitvoeren.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d126b68bea8d2083fcf1d08e168b9ead1511b25c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001244"
---
# <a name="service-order-stages"></a>Serviceorderfasen   

[!include [banner](../includes/banner.md)]


U kunt fasen instellen voor een serviceorder om de taken die moeten worden voltooid, de volgorde waarin ze zijn afgerond, en de werknemers die van de voltooiing van deze verantwoordelijk is te definiëren. Door de fasen voor een serviceorder te definiëren en deze aan werknemers toe te wijzen, kunt u de stroom controleren van een serviceorder met de verschillende taken die mensen in de serviceorganisatie uitvoeren. De volgorde van fasen moet een eerste fase opnemen.

U kunt ook definiëren de acties die zijn toegestaan in elke fase. Als u bijvoorbeeld het selectievakje **Boeken** voor alle fasen behalve de laatste uitschakelt, kunnen serviceorders pas worden geboekt als deze de volledige fasereeks hebben doorlopen.

## <a name="branching-in-service-order-stages"></a>De vertakking in serviceorderfasen

Wanneer u een servicefase instelt, u meerdere opties, of vertakkingen maken, om uit te selecteren voor de volgende servicefase. Alle vertakkingen die u maakt zijn beschikbaar om uit te kiezen wanneer de eerste fase is voltooid. Bijvoorbeeld, stelt u **Planning** als eerste fase. U maakt twee fasen genaamd **Onderhanden** en **Annuleren**, en selecteer vervolgens **Planning** als deze bovenliggende voor. U kunt de fase **Planning** aan verkooporder toewijzen. Wanneer de planningsfase voor de verkooporder is voltooid, kunt u de fase **Onderhanden** selecteren als de verkooporder gereed is om te werken, of u kunt de fase **Annuleren** selecteren als de verkooporder wordt geannuleerd.

## <a name="see-also"></a>Zie ook

[Serviceorderfasen instellen](set-up-service-order-stages.md)

[De fase van de serviceorder wijzigen](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
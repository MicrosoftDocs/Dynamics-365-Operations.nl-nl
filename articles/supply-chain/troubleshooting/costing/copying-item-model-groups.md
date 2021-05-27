---
title: Ontbrekende veldinstellingen wanneer artikelmodelgroepen naar een andere rechtspersoon worden gekopieerd
description: Veldinstellingen ontbreken wanneer artikelmodelgroepen naar een andere rechtspersoon worden gekopieerd.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026400"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Ontbrekende veldinstellingen wanneer artikelmodelgroepen naar een andere rechtspersoon worden gekopieerd

KB-nummer: 4612800

## <a name="symptoms"></a>Symptomen

Wanneer u artikelmodelgroepen kopieert naar een andere rechtspersoon (bedrijf) met behulp van de entiteit *Voorraadbeleid van artikelmodelgroep*, ontbreken sommige veldinstellingen (bijvoorbeeld het voorraadmodel en de omschrijving) in de nieuwe modelgroep in de doelrechtspersoon.

## <a name="resolution"></a>Oplossing

Als u een volledige kopie van een artikelmodelgroep naar een andere rechtspersoon wilt maken, moet u ook het voorraadbeleid van de artikelmodelgroep (`InventInventoryPolicyEntity`) en de beleidsregels voor kostenstroomveronderstelling (`InventCostFlowAssumptionPolicyEntity`) selecteren die aan de artikelmodelgroep zijn gekoppeld.

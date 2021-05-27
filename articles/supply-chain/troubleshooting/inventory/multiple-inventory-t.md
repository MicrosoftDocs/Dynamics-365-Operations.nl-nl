---
title: Meerdere voorraadtransacties voor batchnummers als de optie Bij fysiek bijwerken is uitgeschakeld
description: Er worden meerdere voorraadtransacties gemaakt nadat u een inkooporderregel hebt aangepast voor artikelen waarbij de optie Bij fysiek bijwerken van de batchnummergroep is ingesteld op Nee.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026419"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Meerdere voorraadtransacties voor batchnummers als de optie Bij fysiek bijwerken is uitgeschakeld

KB-nummer: 4613390

## <a name="symptoms"></a>Symptomen

Er worden meerdere voorraadtransacties gemaakt nadat u een inkooporderregel hebt aangepast voor artikelen waarbij de optie **Bij fysiek bijwerken** van de batchnummergroep is ingesteld op *Nee*.

Wanneer u een artikel maakt waarbij de optie **Bij fysiek bijwerken** van de batchnummergroep is ingesteld op *Nee*, wordt automatisch een nieuw batchnummer gemaakt als u de hoeveelheid op de inkoopregel wijzigt en de inkooporderpagina opslaat.

## <a name="resolution"></a>Oplossing

De instelling **Bij fysiek bijwerken** voor batchnummergroepen werkt als volgt:

- Wanneer de optie is ingesteld op *Ja*, worden er alleen nieuwe batchnummers gemaakt na fysiek bijwerken (bijvoorbeeld wanneer artikelen worden verzonden of ontvangen).
- Wanneer de optie is ingesteld op *Nee*, wordt er telkens een nieuw batchnummer gemaakt wanneer een toepasselijke update wordt toegepast (bijvoorbeeld wanneer een nieuwe hoeveelheid aan een inkooporder wordt toegevoegd).

---
title: Er is geen begindatumwaarde op het tabblad Actieve prijzen van de pagina Artikelprijs
description: Er is geen begindatumwaarde op het tabblad Actieve prijzen van de pagina Artikelprijs.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026420"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Er is geen begindatumwaarde op het tabblad Actieve prijzen van de pagina Artikelprijs

KB-nummer: 4613548

## <a name="symptoms"></a>Symptomen

Er is geen waarde bij **Begindatum** op het tabblad **Actieve prijzen** van de pagina **Artikelprijs**.

## <a name="resolution"></a>Oplossing

De waarde van **Begindatum** (ingangsdatum) die is ingesteld op de prijs in behandeling is niet overgezet naar de actieve prijs.

Een artikelkostenrecord wordt eerst ingevoerd met de status *In behandeling* en met een gewenste ingangsdatum. Als u de artikelkostenrecord activeert, wordt de status naar *Actief* en de begindatum naar de activeringsdatum bijgewerkt. Daarom is de activeringsdatum van de actieve prijs altijd de werkelijke datum van de activering.

Zie [Overzicht van Kostprijsberekeningsversies](../../cost-management/costing-versions.md) voor meer informatie.

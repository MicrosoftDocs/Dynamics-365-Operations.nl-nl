---
title: Transacties kunnen naar een uitgestelde grootboekrekening worden geboekt
description: Als een productontvangstbon wordt geannuleerd, kunnen transacties naar uitgestelde grootboekrekeningen worden geboekt, zelfs als de hoofdrekeningen zijn opgeschort
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476060"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Transacties kunnen naar een uitgestelde grootboekrekening worden geboekt

## <a name="symptoms"></a>Symptomen

Als een productontvangstbon wordt geannuleerd, kunnen transacties naar uitgestelde grootboekrekeningen worden geboekt, zelfs als de hoofdrekeningen zijn opgeschort.

## <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Controleer op de pagina **Parameters van module Leveranciers** op het tabblad **Algemeen** of de optie **Productontvangstbon in grootboek boeken** is ingesteld op *Ja*.
1. Maak een inkooporder en voeg een orderregel toe met een hoeveelheid van *1000* voor een product.
1. Bevestig de inkooporder.
1. Boek de productontvangstbon en controleer de boekstukken.
1. Schort de relevante hoofdrekeningen, *200140* en *140200*, op.
1. Annuleer de geboekte productontvangstbon.
1. U ziet dat transacties naar de uitgestelde grootboekrekeningen kunnen worden geboekt.

## <a name="resolution"></a>Oplossing

Transacties kunnen worden geboekt naar de opgeschorte grootboekrekeningen wanneer productontvangstbonnen worden geannuleerd, omdat met dit gedrag correcte boekingen mogelijk zijn.

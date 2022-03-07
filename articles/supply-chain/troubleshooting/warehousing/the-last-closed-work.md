---
title: De laatst afgesloten werkregel moet een wegzetten zijn
description: De laatst afgesloten werkregel moet een wegzetten zijn
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bbc5797df2b7465b36ec5ea546a67441626daeb1c72f82dfca4eb7db3503b713
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760269"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>De laatst afgesloten werkregel moet een wegzetten zijn

Foutcode: WAX1285

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> De laatst afgesloten werkregel moet een wegzetten zijn.

## <a name="cause"></a>Oorzaak

Het werk kan in de huidige status niet worden geannuleerd.

Op de laatste werkregel is het veld **Werkstatus** ingesteld op *Afgesloten*, maar het veld **Werktype** is niet ingesteld op *Wegzetten*.

## <a name="resolution"></a>Oplossing

Volg deze stappen om werk te annuleren.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.
1. In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren.
1. Selecteer **OK**.
1. Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.

Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.

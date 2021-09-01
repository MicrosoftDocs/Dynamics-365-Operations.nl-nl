---
title: U kunt werk dat aan een gebruiker is toegewezen, niet annuleren
description: U kunt werk dat aan een gebruiker is toegewezen, niet annuleren
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748686"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>U kunt werk dat aan een gebruiker is toegewezen, niet annuleren

Foutcode: WAX708

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> U kunt geen werk annuleren dat op een naam van een gebruiker staat.

## <a name="cause"></a>Oorzaak

Het werk is vergrendeld door een gebruiker en kan niet worden geannuleerd. Om dit te bevestigen, opent u de werk-id en vervolgens opent u het tabblad **Algemeen**. Als het werk is vergrendeld, is het veld **Werkstatus** ingesteld op *Wordt uitgevoerd* en het veld **Vergrendeld door** is ingesteld op een gebruikers-id.

## <a name="resolution"></a>Oplossing

Volg deze stappen om werk te annuleren.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.
1. In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren.
1. Selecteer **OK**.
1. Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.

Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.

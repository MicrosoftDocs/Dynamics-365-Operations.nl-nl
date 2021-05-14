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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924396"
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

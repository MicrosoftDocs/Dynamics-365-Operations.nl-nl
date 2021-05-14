---
title: Werk kan niet worden geannuleerd vanwege de status ervan
description: Werk kan niet worden geannuleerd vanwege de status ervan
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924250"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Werk kan niet worden geannuleerd vanwege de status ervan

Foutcode: WAX2190

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> U kunt het werk %1 niet annuleren omdat het een status van %2 heeft.

## <a name="cause"></a>Oorzaak

Het werk kan in de huidige status niet worden geannuleerd.

De werkkoptekst of werkregels hebben niet de verwachte **Werkstatus**-waarde. Het veld **Werkstatus** in de werkkoptekst is niet ingesteld op *Open* of *Wordt uitgevoerd*.

## <a name="resolution"></a>Oplossing

Volg deze stappen om werk te annuleren.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.
1. In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren.
1. Selecteer **OK**.
1. Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.

Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.

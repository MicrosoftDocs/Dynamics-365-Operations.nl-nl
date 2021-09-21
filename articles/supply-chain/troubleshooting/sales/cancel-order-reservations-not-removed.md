---
title: Reserveringen kunnen niet worden verwijderd wanneer een order wordt geannuleerd
description: U kunt een verkooporder niet annuleren tot het werk dat aan die order is gekoppeld, is geannuleerd en teruggedraaid. Voer hiervoor de volgende drie stappen uit.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476023"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Reserveringen kunnen niet worden verwijderd wanneer een order wordt geannuleerd

## <a name="symptoms"></a>Symptomen

Als er werk aan een verkooporder is gekoppeld en u probeert die order te annuleren, wordt het volgende foutbericht weergegeven:

> Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen.

U kunt de verkooporder niet annuleren tot het werk is geannuleerd en teruggedraaid. Deze vereiste geldt ook als het werk dat aan de verkooporder is gekoppeld, is afgesloten.

## <a name="resolution"></a>Oplossing

Volg deze stappen om dit probleem op te lossen:

1. Annuleer het werk en plaats de voorraad terug op de gewenste locatie. Ga naar de desbetreffende belasting van de verkooporder en selecteer **Opgenomen hoeveelheid reduceren** op de ladingsregel of **Werk omkeren** in het actievenster.

    Het werk heeft nu de status *Geannuleerd* en er wordt automatisch werk voor een nieuwe voorraadverplaatsing gemaakt en verwerkt om de voorraad terug te zetten op de locatie die op het moment van de omkering is beschreven.

2. Verwijder de lading. De verzending wordt ook verwijderd.

3. U moet nu naar de verkooporder kunnen gaan en deze kunnen annuleren.

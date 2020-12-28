---
title: Automatisch serviceorders maken
description: U kunt serviceorders maken voor één serviceovereenkomst of voor meerdere serviceovereenkomsten.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 914df1626b02110264b895e82dc9301f3aa0afce
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425631"
---
# <a name="create-service-orders-automatically"></a>Automatisch serviceorders maken    

[!include [banner](../includes/banner.md)]


U kunt serviceorders maken voor één serviceovereenkomst of voor meerdere serviceovereenkomsten. Wanneer deze zijn gemaakt, kunt u uw serviceorders weergeven in het formulier **Serviceorders**.

Serviceorders worden alleen gemaakt voor de geldige periode van de serviceovereenkomst. Als het interval dat u opgeeft in het dialoogvenster **Serviceorders maken**, vóór de begindatum of na de einddatum van de serviceovereenkomst valt, worden alleen serviceorders gemaakt voor dat deel van het interval dat binnen de datums van de serviceovereenkomst valt.

Wanneer u handmatig of automatisch serviceorders maakt vanaf de serviceovereenkomstregel, moet de serviceorder binnen het interval vallen dat met de begindatum en de einddatum voor de regel is ingesteld, tenzij u op de regel geen einddatum hebt ingesteld.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Automatisch serviceorders maken voor een serviceovereenkomst

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.

2.  Selecteer een serviceovereenkomst.

3.  Klik op het tabblad **Leveren** en klik vervolgens op **Geplande serviceorders**.

4.  Geef datums op in de velden **Datum vanaf** en **Datum t/m** om de serviceperiode te definiëren.

5.  Schakel het selectievakje **Infologboek weergeven** in om een lijst weer te geven van de serviceorders die zijn gemaakt.

6.  Selecteer transactietypen in de veldgroep **Transactietypen opnemen**. De transactietypen vertegenwoordigen de regels die zijn gemaakt in de serviceovereenkomst en elk transactietype dat u selecteert, genereert verscheidene serviceorders, afhankelijk van de service-interval die is opgegeven op de serviceovereenkomstregel.

7.  Schakel het selectievakje **Continu** in om eventuele ontbrekende serviceorders in een continue serie van serviceorders te maken.

8.  Klik tot slot op **OK**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Automatisch serviceorders maken voor meerdere serviceovereenkomsten

1.  Klik op **Servicebeheer** \> **Periodiek** \> **Serviceorders** \> **Serviceorders maken**.

2.  Klik op **Selecteren** om criteria voor het maken van serviceorders te selecteren en toe te voegen of te verwijderen.

3.  Klik op **OK**.

## <a name="see-also"></a>Zie ook

[Serviceorders](service-orders.md)

[Automatisch serviceorders maken](auto-create-service-orders.md)

  



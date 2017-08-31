--- 
title: Betalingsmethode voor ISO20022 automatische incasso instellen
description: In deze procedure ziet u hoe u de betalingsmethode van de klanten instelt voor ISO20022 automatische incasso of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16ff0cc28b272add80b08ae43b9fe5b8e7370b70
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>Betalingsmethode voor ISO20022 automatische incasso instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

In deze procedure ziet u hoe u de betalingsmethode van de klanten instelt voor ISO20022 automatische incasso of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt. 



Voordat u deze taak uitvoert, moet u indelingconfiguraties voor export en betaalrekeningen hebben ingesteld.



Deze procedure is gemaakt met het demobedrijf DEMF.



Dit is de derde van vijf taken die het proces voor klantenbetalingen toelichten door middel van elektronische rapportageconfiguraties.

1. Ga naar Klanten > Betalingsinstelling > Betalingsmethoden.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Betalingsmethode met een waarde van 'ELECTRONIC'.
3. Klik op Bewerken.
4. Geef de waarden 'DEMF OPER' op in het veld Betalingsrekening.
5. Vouw de sectie Bestandsindelingen uit.
6. Selecteer Ja in het veld Algemene elektronische rapportage.
7. Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.
    * Selecteer in de lijst de waarde ISO20022 Automatische incasso (DE).  Als de lijst leeg is, betekent dit dat er geen configuratie voor de exportindeling voor klantenbetalingen is geïmporteerd en geactiveerd.  
8. Selecteer Ja in het veld Mandaat vereisen.
    * Selecteer de parameter Mandaat vereisen voor klantbetalingsindelingen, die vereist dat mandaatinformatie deel uitmaakt van het betalingbericht, zoals SEPA automatische incasso.  
9. Klik op Opslaan.



--- 
title: Betalingsmethode voor ISO20022-kredietoverdracht instellen
description: IN deze procedure ziet u hoe u de betalingsmethode van de leverancier instelt voor ISO20022-kredietoverdracht of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.openlocfilehash: cc30912d15549c9519133c6ea12ee4d8edea7214
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Betalingsmethode voor ISO20022-kredietoverdracht instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

IN deze procedure ziet u hoe u de betalingsmethode van de leverancier instelt voor ISO20022-kredietoverdracht of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt. 

Voordat u deze taak uitvoert, moet u indelingconfiguraties voor export en betaalrekeningen hebben ingesteld.

Deze taak is gemaakt met het demobedrijf DEMF.

Dit is de derde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties. Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.

1. Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Betalingsmethode met een waarde van 'SEPA CT'.
3. Klik op Bewerken.
4. Selecteer Totaal in het veld Periode.
5. Selecteer Elektronische betaling in het veld Betalingstype.
6. Vouw de sectie Bestandsindelingen uit.
7. Selecteer Ja in het veld Algemene elektronische rapportage.
8. Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.
    * Selecteer in de lijst de waarde ISO20022 Kredietoverdracht (DE). Als de lijst leeg is, betekent dit dat er geen configuratie voor de exportindeling voor leveranciersbetalingen is geïmporteerd en geactiveerd.  
9. Selecteer Bank in het veld Bankrekening.
10. Geef de waarden 'DEMF OPER' op in het veld Betalingsrekening.
11. Klik op Opslaan.


---
title: Betalingsmethode voor ISO20022 automatische afschrijving instellen
description: In deze procedure ziet u hoe u de betalingsmethode van de klanten instelt voor ISO20022 automatische incasso of een ander type betaling door middel van elektronische rapportage en zo een bestand aanmaakt.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441847"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Betalingsmethode voor ISO20022 automatische afschrijving instellen

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
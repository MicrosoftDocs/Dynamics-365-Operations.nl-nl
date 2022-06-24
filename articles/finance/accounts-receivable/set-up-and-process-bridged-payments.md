---
title: Overbruggingsbetalingen instellen en verwerken
description: In dit artikel wordt uitgelegd hoe u overbruggingsbetalingen instelt en verwerkt. Een overbruggingsbetaling is een betaling die in twee stappen naar het grootboek wordt geboekt.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f0609e333fb16ba189b6a971f88fbb5bf900fec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887972"
---
# <a name="set-up-and-process-bridged-payments"></a>Overbruggingsbetalingen instellen en verwerken

[!include [banner](../includes/banner.md)]

Een overbruggingsbetaling is een betaling die in twee stappen naar het grootboek wordt geboekt. Deze methode wordt meestal gebruikt wanneer de betalingsmethode is ingesteld op **Bank** en u transacties alleen naar de bankrekening overmaakt als de transactie door de bank is verwerkt. U kunt dit echter ook voor een grootboekrekening gebruiken. In dit geval wordt het bedrag van de ene hoofdrekening naar een andere hoofdrekening verplaatst wanneer de overbruggingsboeking wordt verwerkt.

U kunt overbruggingsbetalingen maken vanuit Leveranciers of Klanten. Hoewel in dit artikel wordt uitgelegd hoe u overbruggingsboekingen voor Klanten configureert, zijn de stappen voor crediteurentransacties vergelijkbaar.

## <a name="set-up-bridging-posting"></a>Overbruggingsboeking instellen

Om overbruggingsboekingen te gebruiken, moet u voor een of meer betalingsmethoden instellen dat ze de **overbruggingsboeking** gebruiken. U moet vervolgens een overbruggingsrekening selecteren.

1. Ga naar **Klanten &gt; Betalingsinstelling &gt; Betalingsmethoden**.
2. Selecteer een bestaande betalingsmethode waarvoor u overbruggingsboekingen mogelijk wilt maken. Of maakt een nieuwe betalingsmethode.
3. Schakel het selectievakje **Overbruggingsboeking** in.
4. Selecteer in het veld **Overbruggingsrekening** de hoofdrekening waarop betalingen moeten worden geboekt voordat ze naar de bankrekening worden verplaatst.
5. Sluit de pagina.

## <a name="process-and-transfer-bridging-posting"></a>Overbruggingsboekingen verwerken en overboeken

Volg deze stappen om een overbruggingsboeking te maken en te verwerken.

1. Ga naar **Klanten &gt; Betalingen &gt; Journaal met betalingen van klant**.
2. Selecteer **Nieuw** om een journaal te maken.
3. Selecteer in het veld **Naam** een naam.
4. Voeg regels toe aan het betalingsjournaal van de klant en selecteer de betalingsmethode die is geconfigureerd voor overbruggingsboekingen.
5. Het journaal boeken. De transacties worden geboekt naar de hoofdrekening die u hebt geselecteerd in het veld **Overbruggingsrekening** in de vorige procedure.

Wanneer de transacties door de bank zijn verwerkt en u de betaling wilt overboeken van de overbruggingsrekening naar de betalingsrekening die is opgegeven voor de betalingsmethode, volgt u deze stappen.

1. Ga naar **Grootboek &gt; Journaalboekingen &gt; Algemene journalen**.
2. Selecteer **Nieuw** om een journaal te maken.
3. Selecteer in het veld **Naam** een naam.
4. Selecteer **Regels** om de journaaldetails te openen.
5. Selecteer **Functies &gt; Overbruggingstransacties selecteren**.
6. Markeer elke betaling die is verwerkt, en selecteer vervolgens **Accepteren**.
7. Het journaal boeken.

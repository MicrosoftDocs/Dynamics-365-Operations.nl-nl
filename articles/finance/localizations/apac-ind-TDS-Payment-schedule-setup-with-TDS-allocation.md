---
title: Betalingsschema's met TDS-toewijzing instellen
description: In dit onderwerp wordt uitgelegd hoe u betalingsschema's moet instellen met toewijzing van TDS (belasting ingehouden op bron).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023156"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Betalingsschema's met TDS-toewijzing instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u betalingsschema's moet instellen met toewijzing van TDS (belasting ingehouden op bron).

1. Ga naar **Leveranciers \> Betalingsinstelling \> Betalingsschema's**.

    [![Pagina Betalingsschema's](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Selecteer in het actievenster **Nieuw** om een betalingsschema te maken en voer de vereiste gegevens in.
3. Selecteer in het veld **Toewijzing** de methode die u wilt gebruiken om de betaling toe te wijzen voor het betalingsschema:

    - Totaal
    - Vast bedrag
    - Vaste hoeveelheid
    - Opgegeven

    In het veld **Bronbelastingtoewijzing** wordt de TDS-toewijzingsmethode voor het betalingsschema getoond. Als u **Totaal** selecteert in het veld **Toewijzing**, wordt het veld **Bronbelastingtoewijzing** automatisch ingesteld op **Totaal**. Als u **Vast bedrag**, **Vaste hoeveelheid** of **Opgegeven** in het veld **Toewijzing** selecteert, wordt het veld **Bronbelastingtoewijzing** automatisch ingesteld op **Evenredig**.

    > [!NOTE]
    > Als het veld **Bronbelastingtoewijzing** is ingesteld op **Totaal**, worden de betalingstermijnen berekend op basis van het brutobedrag, inclusief het TDS-bedrag. Als het veld **Bronbelastingtoewijzing** is ingesteld op **Evenredig**, worden de betalingstermijnen berekend op basis van het nettobedrag, nadat het TDS-bedrag is ingehouden.

4. Geef de andere vereiste gegevens op in het formulier en sluit de pagina.

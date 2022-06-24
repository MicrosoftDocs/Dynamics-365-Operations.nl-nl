---
title: Betalingsschema's met TDS-toewijzing instellen
description: In dit artikel wordt uitgelegd hoe u betalingsschema's moet instellen met toewijzing van TDS (belasting ingehouden op bron).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 48891c32f39b743ce26e265c5682dab28ecb4b27
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868307"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Betalingsschema's met TDS-toewijzing instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u betalingsschema's moet instellen met toewijzing van TDS (belasting ingehouden op bron).

1. Ga naar **Leveranciers \> Betalingsinstelling \> Betalingsschema's**.

    [![Pagina Betalingsschema's.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

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

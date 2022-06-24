---
title: De TDS-parameters instellen
description: In dit artikel wordt beschreven hoe u parameters in kunt stellen om de functionaliteit TDS (belasting ingehouden op bron) in opgegeven transacties te activeren. Dit is een noodzakelijke stap om de functie voor belasting ingehouden op bron (TDS) te gebruiken.
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
ms.openlocfilehash: 3390cad6979858fbff73769d0d25132ba18a2157
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865608"
---
# <a name="set-the-tds-parameters"></a>De TDS-parameters instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u parameters in kunt stellen om de functionaliteit TDS (belasting ingehouden op bron) in opgegeven transacties te activeren. Dit is een noodzakelijke stap om de functie voor belasting ingehouden op bron (TDS) te gebruiken.

1. Ga naar **Grootboek \> Grootboek instellen \> Grootboekparameters**.
2. Stel op het tabblad **Directe belastingen** in de sectie **belasting ingehouden op bron** de optie **TDS activeren** in op **Ja** om de TDS-functionaliteit te activeren en de pagina's en velden die hiervoor worden gebruikt.
3. Stel de optie **Factuuroptie** in op **Ja** om de velden te activeren die worden gebruikt om TDS op factuurniveau te berekenen en in te houden.
4. Stel de optie **Betaling** in op **Ja** om de velden te activeren die worden gebruikt om TDS op betalingsniveau te berekenen en in te houden.

    [![Tabblad Directe belastingen.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Zoek op het tabblad **Nummerreeksen** de rij waarin het veld **Verwijzing** is ingesteld op **Bronbelastingbetaling**. Selecteer in het veld **Nummerreekscode** voor de rij de nummerreekscode. De nummerreekscode wordt gebruikt om boekstuknummers te genereren voor het periodieke TDS-vereffeningsproces.

    > [!NOTE]
    > Als u het periodieke TDS-vereffeningsproces wilt uitvoeren, gaat u naar **Belasting \> Aangiften \> Bronbelasting \> Bronbelastingbetaling**.

    [![Tabblad Nummerreeksen.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Sluit de pagina.

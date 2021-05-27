---
title: De TDS-parameters instellen
description: In dit onderwerp wordt beschreven hoe u parameters in kunt stellen om de functionaliteit TDS (belasting ingehouden op bron) in opgegeven transacties te activeren. Dit is een noodzakelijke stap om de functie voor belasting ingehouden op bron (TDS) te gebruiken.
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023146"
---
# <a name="set-the-tds-parameters"></a>De TDS-parameters instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u parameters in kunt stellen om de functionaliteit TDS (belasting ingehouden op bron) in opgegeven transacties te activeren. Dit is een noodzakelijke stap om de functie voor belasting ingehouden op bron (TDS) te gebruiken.

1. Ga naar **Grootboek \> Grootboek instellen \> Grootboekparameters**.
2. Stel op het tabblad **Directe belastingen** in de sectie **belasting ingehouden op bron** de optie **TDS activeren** in op **Ja** om de TDS-functionaliteit te activeren en de pagina's en velden die hiervoor worden gebruikt.
3. Stel de optie **Factuuroptie** in op **Ja** om de velden te activeren die worden gebruikt om TDS op factuurniveau te berekenen en in te houden.
4. Stel de optie **Betaling** in op **Ja** om de velden te activeren die worden gebruikt om TDS op betalingsniveau te berekenen en in te houden.

    [![Tabblad Directe belastingen](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Zoek op het tabblad **Nummerreeksen** de rij waarin het veld **Verwijzing** is ingesteld op **Bronbelastingbetaling**. Selecteer in het veld **Nummerreekscode** voor de rij de nummerreekscode. De nummerreekscode wordt gebruikt om boekstuknummers te genereren voor het periodieke TDS-vereffeningsproces.

    > [!NOTE]
    > Als u het periodieke TDS-vereffeningsproces wilt uitvoeren, gaat u naar **Belasting \> Aangiften \> Bronbelasting \> Bronbelastingbetaling**.

    [![Tabblad Nummerreeksen](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Sluit de pagina.

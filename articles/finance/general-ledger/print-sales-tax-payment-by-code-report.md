---
title: Rapport Btw-betaling per code afdrukken
description: Dit artikel bevat informatie over de instellingen en acties die vereist zijn om het rapport Btw-betaling per code af te drukken in de valuta van de boekhouding of de btw-code.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 9c6b51da41f2aaa3206f8ad97a364a9cd5ca6d49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856649"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Rapport Btw-betaling per code afdrukken 

[!include [banner](../includes/banner.md)]

Als u het rapport **Btw-betaling per code** wilt afdrukken, gaat u naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-betaling per code**. Standaard worden rapportbedragen gegenereerd in de valuta voor boekhouding van de rechtspersoon voor alle aangiftecodes die zijn ingesteld op de pagina **Btw-aangiftecodes**.

U kunt dit rapport ook zo genereren dat de btw-betalingsbedragen worden weergegeven in de valuta van de btw-codes voor alle aangiftecodes die aan btw-codes zijn toegewezen op de pagina **Btw-codes**.

## <a name="turn-on-the-feature"></a>De functie inschakelen

Schakel in het werkgebied **Functiebeheer** de volgende functie in: **Het rapport btw-betaling per code genereren in de valuta van de btw-code**.

## <a name="run-the-report"></a>Het rapport uitvoeren

1. Ga naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **Btw-betaling per code**.
2. Selecteer in het veld **Rapportvaluta** een van de volgende waarden:

    - **Valuta voor boekhouding**: druk de rapportbedragen af in de valuta voor boekhouding.
    - **Valuta van btw-code**: druk de rapportbedragen af in de valuta van de btw-codes.

    ![Dialoogvenster Btw-betaling per code.](media/Sales-tax-payment-by-code.png)

In de volgende afbeelding ziet u een voorbeeld van het gegenereerde rapport. In het rapport wordt aangegeven dat de aangiftecode **101** de valuta **EUR** gebruikt als het veld **Btw-valuta** wordt ingesteld op **EUR** voor de btw-code waaraan de aangiftecode is toegewezen.

![Voorbeeld van rapport Btw-betaling per code.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
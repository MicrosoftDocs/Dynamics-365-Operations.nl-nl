---
title: Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling
description: In deze procedure ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1df738e3925dc23e7723d93f33acf6a9d811b113
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964536"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Leveranciersbetalingen maken en exporteren met de ISO20022-betalingsindeling

[!include [banner](../../includes/banner.md)]

In dit onderwerp ziet u hoe betalingsregels voor SEPA-kredietoverdracht kunnen worden gemaakt in het betalingsjournaal van de leverancier en hoe een bestand met leveranciersbetalingen kan worden gegenereerd door middel van het ISO2022-kredietoverdrachtvoorbeeld.

Dit is de vijfde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties. Gebruik de DEMF-demogegevens om dit voorbeeld te voltooien.

## <a name="example"></a>Voorbeeld

1.    Ga naar **Leveranciers > Betalingen > Betalingsjournaal**.
2.    Klik op **Nieuw**.
3.    Typ of selecteer een waarde in het veld **Naam**.
4.    Klik op **Regels > Betalingsvoorstel > Betalingsvoorstel maken**.
5.    Vouw de sectie **Op te nemen records** uit.
6.    Klik op **Filter**.
7.    Selecteer in de lijst de rij voor de **tabel Leveranciers** en het **veld Leveranciersrekening**.
8.    Typ of selecteer een waarde in het veld **Criteria**. U kunt willekeurige criteria toepassen om van leverancierstransacties te selecteren; gebruik in dit voorbeeldgebruik DE-001 als leveranciersrekening.
12.    Klik tot slot op **OK**.
13.    Klik tot slot op **OK**.
14.    Klik op **Betalingen maken**.
15. Een ISO20022-betalingsbestand genereren.
    1.    Klik op **Betalingen genereren.**
    2.    Typ of selecteer een waarde in het veld **Betalingsmethode.**
    3.    Typ een waarde in het veld **Bestandsnaam**. In dit voorbeeld is vanwege de EUR-betaling het gegenereerde bestand compatibel is met SEPA. ISO20022 kredietoverdracht alsmede andere indelingen voor betalingen van leverancier kunnen ook worden gebruikt voor het genereren van betalingen in andere valuta's.
    4.    Typ of selecteer een waarde in het veld **Bankrekening**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
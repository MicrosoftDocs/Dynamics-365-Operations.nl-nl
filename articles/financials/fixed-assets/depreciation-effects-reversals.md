---
title: Afschrijvingseffecten met omkeringen
description: In dit artikel worden mogelijke implicaties van het terugboeken van een vaste-activatransactie beschreven.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d061ad8df477943259bff853d032c3df620e0b27
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="depreciation-effects-with-reversals"></a>Afschrijvingseffecten met omkeringen

[!include[banner](../includes/banner.md)]


In dit artikel worden mogelijke implicaties van het terugboeken van een vaste-activatransactie beschreven. 

U kunt vaste-activatransacties omkeren, net als de transacties die zijn gekoppeld aan een vast activum. U kunt een omgekeerde transactie ook intrekken. 

U kunt een transactie omkeren of intrekken, zolang als dit niet de meest recente transactie is die is geboekt op het boek voor het activum. U moet eerst bepalen of er geen afschrijvingstransacties zijn geboekt na de transactie die u wilt omkeren. De reden hiervoor is dat de afschrijving niet opnieuw wordt berekend wanneer u een transactie omkeert. Dit betekent dat afschrijvingen vaak te hoog of te laag zijn na de omkering, zoals wordt geïllustreerd in de voorbeelden. 

Als u ervoor wilt zorgen dat de afschrijving juist is wanneer u een transactie omkeert, gaat u niet door met de omkering als u een bericht ontvangt waarin wordt uitgelegd dat de afschrijving niet opnieuw wordt berekend. Keer in plaats hiervan eerst de afschrijvingstransactie om die is geboekt na de transactie die u wilt omkeren, en ga vervolgens door met de omkering. U wordt niet gewaarschuwd voor herberekeningen van de afschrijving en u kunt doorgaan met de omkering. 

In de volgende voorbeelden worden de berekeningen getoond die worden uitgevoerd als u het waarschuwingsbericht negeert en doorgaat zonder de afschrijvingstransacties eerst om te keren.

## <a name="example-1-depreciation-is-overstated"></a>Voorbeeld 1: een te hoge afschrijving
Een activum wordt ingesteld op een levensduur van vijf jaar en een lineaire afschrijving (60 afschrijvingsperioden). In dit voorbeeld is de afschrijving te hoog.
#### <a name="asset-transaction-history"></a>Activumtransactiehistorie

| Datum       | Transactietype                                                          | Bedrag                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1 januari  | Verwerving                                                               | 59.000,00                                 |
| 1 januari  | Verwervingscorrectie                                                    | 1.000,00                                  |
| 31 januari | Afschrijving (gemaakt met een voorstel voor één afschrijvingsperiode) | 1000,00-berekening: boekwaarde (59.000 + 1000 afschrijving) / aantal resterende afschrijvingsperioden (60) |

#### <a name="reversal-action"></a>Omkeringsactie

| Datum      | Transactietype                | Bedrag    |
|-----------|---------------------------------|-----------|
| 1 januari | Omkering van verwervingscorrectie | –1.000,00 |

#### <a name="depreciation-effect"></a>Afschrijvingseffect

| Datum        | Transactietype        | Bedrag                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28 februari | Afschrijving (voorstel) | 983,05-berekening: boekwaarde (59.000 - 1000 afschrijving) / aantal resterende afschrijvingsperioden (59) |

De afschrijving is 16,95 (1000 - 983,05) te hoog.

## <a name="example-2-depreciation-is-understated"></a>Voorbeeld 2: een te lage afschrijving
Een activum wordt ingesteld op een levensduur van vijf jaar en een lineaire afschrijving (60 afschrijvingsperioden). In dit voorbeeld is de afschrijving te laag.
#### <a name="asset-transaction-history"></a>Activumtransactiehistorie

| Datum       | Transactietype                                                          | Bedrag                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1 januari  | Verwerving                                                               | 59.000,00                                   |
| 1 januari  | Afwaarderingscorrectie                                                     | 1.000,00                                    |
| 31 januari | Afschrijving (gemaakt met een voorstel voor één afschrijvingsperiode) | 966,67-berekening: boekwaarde (59.000 - 1000 afschrijving) / aantal resterende afschrijvingsperioden (60) |

#### <a name="reversal-action"></a>Omkeringsactie

| Datum      | Transactietype               | Bedrag    |
|-----------|--------------------------------|-----------|
| 1 januari | Omkering van afwaarderingscorrectie | –1.000,00 |

#### <a name="depreciation-effect"></a>Afschrijvingseffect

| Datum        | Transactietype        | Bedrag                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28 februari | Afschrijving (voorstel) | 983,62-berekening: boekwaarde (59.000 - 966,67 afschrijving) / aantal resterende afschrijvingsperioden (59) |

De afschrijving is 16,95 (983,62 - 966,67) te laag.



<a name="see-also"></a>Zie ook
--------

[Afschrijving vaste activa](fixed-asset-depreciation.md)



